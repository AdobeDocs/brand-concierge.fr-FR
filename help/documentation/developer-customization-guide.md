---
title: Guide de développement et de personnalisation
description: Découvrez comment installer Brand Concierge Web SDK et le client web, personnaliser l’apparence et le contenu, gérer les événements côté client et exporter les données de conversation.
role: Developer,Admin
level: Experienced
toc: true
source-git-commit: 13db0491c987a08492820ac216e20feb87f30e44
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 4%

---


# Guide de développement et de personnalisation {#developer-customization-guide}

Ce guide est destiné aux développeurs et aux équipes techniques qui implémentent ou personnalisent un déploiement Brand Concierge. Il couvre l’installation de Web SDK et du client Web, la personnalisation de l’apparence et du contenu, l’écoute des événements côté client par le biais de fonctions de rappel et l’exportation de données de conversation pour la création de rapports.

## Installation de Web SDK et de Web Client {#installation}

### Conditions préalables {#prerequisites}

* L’organisation est un client Adobe Experience Platform (AEP).
* La page est instrumentée avec Adobe Experience Platform Web SDK.
* L’identifiant du flux de données utilisé sur la page est activé pour Brand Concierge.

### Étape 1 : injecter le SDK Web {#inject-web-sdk}

Ajoutez les éléments suivants à la section `<head>` de la page :

```html
<script>
  !(function (n, o) {
    o.forEach(function (o) {
      n[o] ||
        ((n.__alloyNS = n.__alloyNS || []).push(o),
        (n[o] = function () {
          var u = arguments;
          return new Promise(function (i, l) {
            n[o].q.push([i, l, u]);
          });
        }),
        (n[o].q = []));
    });
  })(window, ["alloy"]);
</script>
<script src="https://cdn1.adoberesources.net/alloy/2.31.1/alloy.min.js"></script>
```

### Étape 2 : injecter le client web {#inject-web-client}

Ajoutez ce qui suit après le script Web SDK, toujours dans la section `<head>` :

```html
<script src="https://experience.adobe.net/solutions/experience-platform-brand-concierge-web-agent/static-assets/main.js"></script>
```

### Étape 3 : configuration de Web SDK {#configure-web-sdk}

Appelez `alloy("configure", ...)` avec les valeurs de votre entreprise à la place des espaces réservés ci-dessous :

```javascript
alloy("configure", {
  defaultConsent: "in",
  edgeDomain: "edge.adobedc.net",
  edgeBasePath: "ee",
  datastreamId: "YOUR_DATASTREAM_ID",
  orgId: "YOUR_IMS_ORG_ID",
  debugEnabled: true,
  idMigrationEnabled: false,
  thirdPartyCookiesEnabled: false,
  prehidingStyle: ".personalization-container { opacity: 0 !important }",
  onBeforeEventSend: (options) => {
    const x = options.xdm;
    const params = new URLSearchParams(window.location.search);
    const titleParam = params.get("title");
    if (titleParam) {
      x.web.webPageDetails.name = titleParam;
    } else {
      x.web.webPageDetails.name = "default-page";
    }
    return true;
  }
});
alloy("sendEvent", {});
```

| Champ | Description |
|---|---|
| `datastreamId` | Identifiant du flux de données configuré pour cette page, activé pour Brand Concierge. |
| `orgId` | L’identifiant d’organisation IMS sous lequel le concierge est configuré. |
| `debugEnabled` | Définissez sur `false` en production une fois l’intégration vérifiée. |
| `prehidingStyle` | CSS appliqué avant le chargement du contenu de personnalisation, pour éviter un flash de contenu non stylisé. |
| `onBeforeEventSend` | Un hook facultatif permettant de modifier la payload XDM avant son envoi, généralement utilisé pour définir le nom de la page ou le contexte. |

### Étape 4 : initialiser le client web {#initialize-web-client}

Après l’appel de configuration de Web SDK, initialisez le client Web en appelant l’API bootstrap :

```javascript
window.adobe.concierge.bootstrap({
  instanceName: "alloy",
  stylingConfigurations: window.styleConfigurations,
  selector: "#brand-concierge-mount"
});
```

| Paramètre | Type | Obligatoire | Description |
|---|---|---|---|
| `instanceName` | string | Oui | Nom de l’instance de Web SDK. |
| `stylingConfigurations` | Objet JSON | Oui | La configuration de style du client web (voir [Personnalisation visuelle et de contenu](#customization)). |
| `selector` | string | Oui | Sélecteur CSS de l’élément HTML dans lequel le client Web se monte. |
| `onEvent` | fonction | Non | Rappel d’événements côté client (voir [Événements côté client et fonctions de rappel](#events)). |

## Personnalisation visuelle et du contenu {#customization}

L’objet `stylingConfigurations` transmis à `bootstrap()` contrôle l’apparence, le comportement et le texte dans l’ensemble du client Web. Il est organisé en plusieurs zones.

### Métadonnées {#metadata}

```javascript
"metadata": {
  "brandName": "Your Brand",
  "version": "1.0.0",
  "language": "en-US",
  "namespace": "brand-concierge"
}
```

### Comportement {#behavior}

Contrôle le comportement fonctionnel des fonctionnalités de conversation individuelles.

```javascript
"behavior": {
  "input": {
    "enableVoiceInput": true
  },
  "chat": {
    "messageAlignment": "left",
    "messageWidth": "80%"
  },
  "privacyNotice": {
    "title": "Privacy Notice",
    "text": "By using this automated chatbot, you consent that any personal information you provide in the chat may be collected, used, analyzed, disclosed, and retained by Adobe and its service providers, in accordance with the Adobe Privacy Policy. Please do not enter any sensitive personal information (e.g., financial or health data)."
  },
  "disclaimer": {
    "attachWithInput": true
  },
  "chatTranscript": {
    "enabled": true,
    "maxSessions": 1,
    "maxMessagesPerSession": 20,
    "cleanupInterval": 24
  },
  "meetingForm": {
    "fieldsPerRow": 2,
    "title": { "text": "Schedule meeting", "alignment": "left" },
    "subtitle": { "text": "I'd be happy to help you schedule a meeting! Please fill out the form below, and we'll follow up with a calendar to confirm your day and time.", "alignment": "left" },
    "buttons": {
      "submit": { "text": "Schedule meeting", "alignment": "left" },
      "cancel": { "text": "Cancel", "alignment": "left" }
    }
  },
  "calendarWidget": {
    "title": { "text": "Book a meeting", "alignment": "left" },
    "subtitle": { "text": "Thanks! Here's a calendar where you can choose a time that works best for your schedule:", "alignment": "left" },
    "postTitle": { "text": "Once confirmed, you'll receive a calendar invite with all the details.", "alignment": "left" },
    "buttons": {
      "confirm": { "text": "Schedule a meeting", "alignment": "left" },
      "cancel": { "text": "Cancel", "alignment": "left" }
    }
  }
}
```

### Clause de non-responsabilité {#disclaimer}

```javascript
"disclaimer": {
  "text": "AI responses may be inaccurate or misleading. Be sure to double check answers and sources."
}
```

### Chaînes de texte {#text-strings}

Toutes les copies visibles par l’utilisateur peuvent être remplacées par l’objet `text`. Clés courantes :

| Clé | Rôle |
|---|---|
| `welcome.heading` / `welcome.subheading` | Titre et sous-texte de l’écran de bienvenue |
| `input.placeholder` | Texte de l’espace réservé du champ de saisie |
| `input.messageInput.aria` / `input.send.aria` / `input.mic.aria` | Libellés d’accessibilité des commandes de saisie |
| `error.network` / `error.general` | Messages d’erreur affichés au visiteur |
| `loading.message` | Texte affiché lors de la génération d’une réponse |
| `feedback.dialog.title.positive` / `.negative` | Titres de la boîte de dialogue Commentaires |
| `feedback.dialog.question.positive` / `.negative` | Texte d’invite de la boîte de dialogue Commentaires |
| `feedback.toast.success` | Toast de confirmation après envoi des commentaires |
| `feedback.thumbsUp.aria` / `feedback.thumbsDown.aria` | Libellés d’accessibilité des boutons de commentaires |

### Tableaux {#arrays}

Listes de contenu configurables :

```javascript
"arrays": {
  "welcome.examples": [
    {
      "text": "I want to edit and enhance my photos",
      "image": "https://example.com/idea-1.png",
      "backgroundColor": "#66BFE7"
    }
  ],
  "feedback.positive.options": [
    "Helpful and relevant recommendations",
    "Clear and easy to understand",
    "Friendly and conversational tone",
    "Visually appealing presentation",
    "Other"
  ],
  "feedback.negative.options": [
    "Not helpful or relevant",
    "Confusing or unclear",
    "Too formal or robotic",
    "Poor visual presentation",
    "Other"
  ]
}
```

### Ressources {#assets}

```javascript
"assets": {
  "icons": {
    "company": "<svg>...</svg>"
  }
}
```

### Thème {#theme}

Propriétés personnalisées CSS contrôlant les couleurs, les polices et la disposition :

```css
"theme": {
  "--color-primary": "#1473e6",
  "--color-primary-hover": "#0056b3",
  "--color-button-primary": "#3B63FB",
  "--color-accent": "#9085ED",
  "--color-button-submit": "#4759e6",
  "--color-button-submit-hover": "#3a4bce",
  "--color-message-user": "#1473e6",
  "--font-family": "'Adobe Clean', adobe-clean, 'Trebuchet MS', sans-serif",
  "--main-container-background": "linear-gradient(135deg, #66ccff, #cc99ff, #ffcc99, #ccff99)",
  "--submit-button-fill-color": "white",
  "--card-text-background": "var(--color-background)",
  "--card-text-border-radius": "var(--border-radius-card)",
  "--message-concierge-link-decoration": "underline",
  "--message-max-width": "100%"
}
```

## Événements côté client et fonctions de rappel {#events}

Le système de rappel d’événement permet à une page d’observer en temps réel les événements du cycle de vie du client Web, les interactions utilisateur, les réponses, les commentaires et les erreurs, ce qui est utile pour envoyer des données d’engagement à Adobe Analytics, Google Analytics ou d’autres systèmes tiers.

### Principales caractéristiques {#key-characteristics}

* **Rappel unique** : une fonction `onEvent` reçoit tous les types d’événements, distingués par des `event.eventType`.
* **Lecture seule** — Les données d’événement sont un instantané cloné et ne peuvent pas être utilisées pour modifier le comportement du client.
* **isolé en cas d’erreur** — les exceptions renvoyées dans le rappel sont interceptées et consignées ; elles n’interrompent pas le client Web.
* **Enregistré via`bootstrap()`** — transmis de la même manière que `onBeforeEventSend`.

### Démarrage rapide {#quick-start}

```javascript
window.adobe.concierge.bootstrap({
  instanceName: "my-instance",
  selector: "#brand-concierge-mount",
  stylingConfigurations: { /* ... */ },
  onEvent: (event) => {
    console.log(event.eventType, event.timestamp, event.data);
  }
});
```

### Filtrage par type d’événement {#filtering}

```javascript
onEvent: (event) => {
  switch (event.eventType) {
    case "query:submitted":
      console.log("User query:", event.data.query);
      break;
    case "response:completed":
      console.log("Response received:", event.data.conversationId);
      break;
    case "card:clicked":
      console.log("Card clicked:", event.data.element.entity_info.productName);
      break;
    case "error:occurred":
      console.log("Error:", event.data.errorMessage);
      break;
  }
}
```

### Types d’événements {#event-types}

| Type d’événement | Valeur | Catégorie | Lorsqu’il se déclenche |
|---|---|---|---|
| `WEBCLIENT_INITIALIZED` | `webclient:initialized` | Cycle de vie | Le client termine l&#39;initialisation (DOM monté, contenu chargé) |
| `QUERY_SUBMITTED` | `query:submitted` | Interaction utilisateur | L’utilisateur envoie un message (saisi ou suggéré) |
| `PROMPT_SUGGESTION_CLICKED` | `promptSuggestion:clicked` | Interaction utilisateur | L’utilisateur clique sur un pilule de suggestion à l’invite |
| `CARD_CLICKED` | `card:clicked` | Interaction utilisateur | L’utilisateur clique sur une carte |
| `HISTORY_CLEARED` | `history:cleared` | Interaction utilisateur | L’utilisateur efface l’historique de la conversation |
| `RESPONSE_STARTED` | `response:started` | Réponse | Le premier bloc de diffusion en continu arrive de l’API |
| `RESPONSE_COMPLETED` | `response:completed` | Réponse | La réponse complète est reçue et rendue. |
| `CARDS_RENDERED` | `cards:rendered` | Réponse | Le rendu des cartes (image unique ou carrousel) se termine. |
| `FEEDBACK_SUBMITTED` | `feedback:submitted` | Commentaires | L’utilisateur envoie un formulaire de commentaire (pouces vers le haut/vers le bas avec des détails) |
| `ERROR_OCCURRED` | `error:occurred` | Erreur | Une erreur se produit (réseau, API ou runtime) |

### Événements de cycle de vie {#lifecycle-events}

`webclient:initialized` se déclenche après l’initialisation complète du client : contenu chargé, injection CSS, interface utilisateur de conversation générée dans le DOM.

```json
{
  "eventType": "webclient:initialized",
  "timestamp": 1741638123789,
  "data": {
    "instanceName": "my-instance"
  }
}
```

### Événements d’interaction utilisateur {#user-interaction-events}

`query:submitted` se déclenche lorsque l’utilisateur envoie un message, qu’il soit saisi, à partir d’une suggestion d’invite ou d’une option de widget.

```json
{
  "eventType": "query:submitted",
  "timestamp": 1741638124000,
  "data": {
    "query": "What photo editing tools do you offer?"
  }
}
```

`promptSuggestion:clicked` se déclenche lorsque l’utilisateur clique sur un cachet de suggestion. Il se déclenche *avant* l’événement `query:submitted` suivant.

```json
{
  "eventType": "promptSuggestion:clicked",
  "timestamp": 1741638124100,
  "data": {
    "suggestion": "Tell me more about Photoshop"
  }
}
```

`card:clicked` se déclenche lorsque l’utilisateur clique sur une carte.

```json
{
  "eventType": "card:clicked",
  "timestamp": 1741638124200,
  "data": {
    "element": {
      "entity_info": {
        "productName": "Adobe Photoshop",
        "productDescription": "Photo editing software",
        "productPageURL": "https://www.adobe.com/products/photoshop.html",
        "productImageURL": "https://example.com/photoshop.png"
      }
    }
  }
}
```

`history:cleared` se déclenche lorsque l’utilisateur clique sur le bouton effacer-l’historique-du-chat.

```json
{
  "eventType": "history:cleared",
  "timestamp": 1741638124400,
  "data": {}
}
```

### Événements de réponse {#response-events}

`response:started` se déclenche lorsque le premier bloc de diffusion en continu arrive de l’API.

```json
{
  "eventType": "response:started",
  "timestamp": 1741638125000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456"
  }
}
```

`response:completed` se déclenche lorsque la réponse complète a été reçue.

```json
{
  "eventType": "response:completed",
  "timestamp": 1741638126000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456"
  }
}
```

`cards:rendered` se déclenche après le rendu des cartes dans le DOM. Il se déclenche séparément de `response:completed` et indique le mode d’affichage utilisé.

```json
{
  "eventType": "cards:rendered",
  "timestamp": 1741638126100,
  "data": {
    "element": [
      { "entity_info": { "productName": "Adobe Photoshop" } },
      { "entity_info": { "productName": "Adobe Illustrator" } }
    ],
    "displayMode": "carousel"
  }
}
```

### Événements de retour {#feedback-events}

`feedback:submitted` se déclenche lorsque l’utilisateur remplit et envoie un formulaire de commentaires (après les pouces vers le haut/bas).

```json
{
  "eventType": "feedback:submitted",
  "timestamp": 1741638127000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456",
    "feedbackType": "negative",
    "selectedOptions": ["Incorrect information", "Not relevant"],
    "notes": "The response did not address my question about pricing."
  }
}
```

### Événements d’erreur {#error-events}

`error:occurred` se déclenche lorsque le client rencontre une erreur de réseau, d’API ou d’exécution.

```json
{
  "eventType": "error:occurred",
  "timestamp": 1741638128000,
  "data": {
    "errorMessage": "Something went wrong. Please try again."
  }
}
```

### Structure de l’objet événement {#event-object-structure}

Chaque événement partage la même forme de niveau supérieur :

```typescript
interface BrandConciergeEvent {
  eventType: string;  // e.g. "query:submitted"
  timestamp: number;  // Unix epoch, milliseconds
  data: object;       // Event-specific payload
}
```

### Référence du type de données : Élément (fiche produit) {#element-reference}

```typescript
interface Element {
  id?: string;
  type?: string;
  entity_info: {
    productName: string;
    productDescription: string;
    description: string;
    productPageURL: string;
    details: string;
    backgroundColor: string;
    learningResource: string;
    productImageURL: string;
    logo: string;
    variants?: Record<string, ElementVariant>;
    primary: ElementAction;
    secondary: ElementAction;
  };
}

interface ElementAction {
  label: string;
  url: string;
}
```

### Bonnes pratiques {#best-practices}

* **À utiliser pour l’analyse et la surveillance.** Suivre l’engagement, les modèles de requête et l’intérêt du produit ; transférer les `error:occurred` vers un service de suivi des erreurs ; suivre les clics sur les cartes pour l’analyse des conversions.
* **Rappelez-vous rapidement.** Il s’exécute de manière synchrone sur le thread principal, afin d’éviter de bloquer les appels réseau :

```javascript
// Good — fire and forget
onEvent: (event) => {
  navigator.sendBeacon("/analytics", JSON.stringify(event));
}

// Avoid — blocking network call
onEvent: async (event) => {
  await fetch("/analytics", { body: JSON.stringify(event) });
}
```

* **Ne vous fiez pas à un ordre d’événement strict** pour les machines d’état. Les événements se déclenchent dans une séquence logique, mais utilisez `conversationId` et `interactionId` pour corréler les événements associés au lieu d’assumer l’ordre.
* **Gérer les erreurs dans votre propre rappel.** Le client isole et consigne les erreurs de rappel, mais les erreurs non gérées dans le rappel peuvent toujours entraîner une perte des données d’analyse :

```javascript
onEvent: (event) => {
  try {
    myAnalytics.track(event);
  } catch (e) {
    console.warn("Analytics tracking failed", e);
  }
}
```

## Exporter des conversations à l’aide d’AEP Query Service {#export-conversations}

Brand Concierge écrit les données de conversation (invites, réponses et commentaires) dans les jeux de données Adobe Experience Platform (AEP). Vous pouvez les interroger directement avec Query Service (SQL) pour créer des rapports personnalisés.

### Rechercher le nom du jeu de données et de la table {#find-dataset}

1. Ouvrez Adobe Experience Platform.

1. Accédez à **[!UICONTROL Jeux de données]**.

1. Recherchez des `cja_brand_concierge` pour répertorier les jeux de données liés à Brand Concierge.

1. Ouvrez le jeu de données dont vous avez besoin (par exemple, réponses ou autres flux, si plusieurs flux existent).

1. Dans la vue des détails du jeu de données, recherchez le **[!UICONTROL Nom de la table]** utilisé par Query Service, et examinez l’exemple ou les données de prévisualisation pour confirmer les colonnes (invites, réponses, commentaires, horodatages, etc.).

>[!NOTE]
>
>Les noms des tables sont liés à chaque jeu de données et diffèrent selon l’environnement et le sandbox. Si vous disposez de plusieurs sandbox ou déploiements, répétez ces étapes dans le bon sandbox afin que le nom de la table corresponde à l’endroit où les données sont écrites.

### Exemple de requête {#example-query}

```sql
SELECT *
FROM cja_brand_concierge_responses_dataset_5f5105bd_1c38_4ebc_8505_bd
WHERE timestamp >= TIMESTAMP '2026-03-16 00:00:00'
  AND timestamp <= NOW()
ORDER BY timestamp ASC;
```

>[!IMPORTANT]
>
>Le nom du tableau ci-dessus n’est qu’une illustration : ne le codez pas en dur. Confirmez d’abord le nom réel de la table pour votre jeu de données dans AEP (voir [Rechercher le jeu de données et le nom de la table](#find-dataset)), puis ajustez le filtre temporel, l’ordre de tri ou d’autres clauses pour répondre à vos besoins de création de rapports. Exécutez la requête à partir du workflow Query Service de votre organisation (interface utilisateur, API ou client connecté), en utilisant le même sandbox que le jeu de données.

### Exécuter une requête dans l’interface utilisateur de Query Service {#run-query-ui}

Si vous avez besoin d’une extraction de données manuelle pour la création de rapports, l’interface utilisateur de Query Service permet d’exécuter et de télécharger directement les résultats :

1. Dans Adobe Experience Platform, accédez à **[!UICONTROL Requêtes]**.

1. Saisissez la requête dans l’éditeur et cliquez sur **[!UICONTROL Exécuter la requête]**.

1. Une fois la requête terminée, les résultats apparaissent dans l’onglet **[!UICONTROL Résultats]** sous l’éditeur. De là, vous pouvez télécharger les résultats.

### Informations complémentaires {#further-reading}

* [Documentation de l’API Query Service](https://experienceleague.adobe.com/fr/docs/experience-platform/query/home){target="_blank"} : référence officielle d’Adobe pour le comportement, les limites, l’authentification et les chemins d’accès à l’API Query Service, qui changent au fil du temps indépendamment de ce guide.
