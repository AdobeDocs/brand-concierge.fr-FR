---
title: Acheminer les conversations vers les représentants
description: Choisissez la manière dont Brand Concierge décide quel commercial reçoit une discussion en direct ou une réservation de réunion, à l’aide d’une rotation, d’un agent direct ou de règles de routage personnalisées.
role: User, Admin
level: Beginner
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 4751ce408fb2aa6d1affae4dd7a5d81ca43ffc8a
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# Acheminer les conversations vers les représentants {#routing}

Le routage répond à une question : lorsque ce visiteur demande une personne, *quelle* personne obtient-il ?

Vous choisissez un type de routage séparément pour l&#39;intégration **[!UICONTROL Réservation de réunion]** et l&#39;intégration **[!UICONTROL Discussion en direct]**, afin qu&#39;un concierge puisse distribuer les réunions de manière uniforme tout en envoyant chaque conversation à un spécialiste, ou toute autre combinaison.

## Types de routage {#routing-types}

| Type de routage | Qui a la conversation ? | Nécessite [!DNL Marketo Engage] |
| --- | --- | --- |
| **[!UICONTROL Round robin]** | Distribué à tous les représentants éligibles | Non |
| **[!UICONTROL Agent direct]** | Un représentant que vous nommez | Non |
| **[!UICONTROL Routage personnalisé]** | Représentants affectés à la règle de routage de priorité la plus élevée pour laquelle le visiteur est éligible | Oui |

La rotation est disponible par défaut et ne nécessite aucune configuration. Vous définissez le type de routage sur l’intégration elle-même. Voir [&#x200B; Activer le chat en direct et la réservation de réunions](configure-in-composer.md).

### Round-robin {#round-robin}

Le round robin se comporte différemment pour les réunions et pour les chats, car les deux ont des objectifs différents.

**Pour la réservation de réunions**, la rotation répartit les réunions de manière égale. Le premier représentant éligible qui a connecté un calendrier est proposé en premier. Une fois qu&#39;une réunion est réservée avec eux, ils sont retirés de la piscine et le représentant suivant est offert. Avec cinq représentants, les cinq premières réunions sont réservées à cinq personnes différentes. Une fois que tout le monde en a reçu un, le pool se réinitialise et le cycle recommence.

La piscine se réinitialise également toutes les 24 heures, de sorte que les réunions de chaque jour soient réparties équitablement.

>[!NOTE]
>
>La réinitialisation circulaire de 24 heures s’exécute sur UTC, et non sur le fuseau horaire local du représentant.

**Pour le chat en direct**, il n’y a pas de rotation séquentielle. Chaque représentant éligible est averti de la conversation entrante en même temps, et le premier à accepter prend la conversation.

### Agent direct {#direct-agent}

Chaque réunion ou conversation de ce concierge va au représentant unique que vous sélectionnez. Utilisez cette option pour une page de destination de campagne appartenant à un chargé de compte ou pour une région comptant un spécialiste.

### Routage personnalisé {#custom-routing}

Le routage personnalisé évalue les règles que vous créez en [!DNL Adobe Marketo Qualifier] par rapport aux attributs de prospect [!DNL Marketo] et d’entreprise du visiteur. Utilisez-le lorsque le bon représentant dépend d’une information que vous connaissez sur le visiteur, par exemple :

* **Géographie** — des visiteurs d&#39;un ensemble de pays font partie de l&#39;équipe régionale.
* **Intérêt du produit** — Les visiteurs intéressés par un produit spécifique s&#39;adressent aux spécialistes de ce produit.
* **Unité opérationnelle, taille de l&#39;entreprise ou secteur d&#39;activité** — toute combinaison d&#39;attributs de prospect et d&#39;entreprise.

>[!IMPORTANT]
>
>Le routage personnalisé est la partie du chat en direct et de la réservation de réunion qui nécessite des [!DNL Adobe Marketo Engage], car les règles sont créées sur [!DNL Marketo] attributs de lead et d’entreprise. Round-robin et direct agent travaillent sans lui.

## Créer une règle de routage personnalisée {#create-rule}

1. Dans [!DNL Adobe Marketo Qualifier], sous **[!UICONTROL Administration]**, sélectionnez **[!UICONTROL Règles de routage]**.

   La liste affiche chaque règle de votre organisation avec sa priorité, son nom, son créateur et sa date de création.

   ![Page Règles de transmission répertoriant les règles existantes avec les colonnes Priorité, Nom, Créé par et Créé sur &#x200B;](../assets/sales-handoff-routing-1.png){width="800" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Créer une règle]** et donnez un nom à la règle.

1. Créez les critères.

   Le panneau de gauche répertorie les attributs de [!DNL Marketo] disponibles à partir des objets **[!UICONTROL Société]** et **[!UICONTROL Lead]** (personne). Recherchez un attribut, puis faites-le glisser sur la zone de travail pour ajouter une condition.

1. Définissez un opérateur et une valeur pour chaque condition.

   Les opérateurs incluent **[!UICONTROL égal]**, **[!UICONTROL n’est pas égal]** et **[!UICONTROL contient]**, entre autres. Par exemple, `Country` **[!UICONTROL est égal]** `United States`.

1. Combinez des conditions en groupes.

   Ajoutez plusieurs conditions à un groupe et joignez-les avec **[!UICONTROL AND]** ou **[!UICONTROL OR]**. Ajoutez d’autres groupes et rejoignez-les également avec **[!UICONTROL AND]** ou **[!UICONTROL OR]**. Les conditions d’imbrication dans des groupes de cette manière vous permettent d’exprimer des critères complexes, tels que *(le pays est les États-Unis OU le Canada) ET (l’intérêt du produit contient Analytics)*.

1. Attribuez la règle aux représentants.

   Dans la section Affectation , recherchez un représentant par nom et sélectionnez-le dans la liste. Ajoutez autant de représentants que vous le souhaitez. Chacun d’eux peut recevoir une conversation correspondant à la règle.

1. Sélectionnez **[!UICONTROL Enregistrer]**.

## Application de la priorité {#priority}

Chaque règle de routage a une priorité. La priorité n’a d’importance que lorsqu’un visiteur est éligible à plusieurs règles.

Dans ce cas, seule la règle de correspondance de priorité la plus élevée est appliquée et la conversation est acheminée vers les représentants affectés à cette règle. Les règles pour lesquelles le visiteur est également admissible, mais qui sont de rang inférieur, sont ignorées.

>[!NOTE]
>
>Un nombre inférieur signifie une priorité supérieure. Une règle de priorité 1 l’emporte sur une règle de priorité 2. La personne qui crée une règle définit sa priorité.

Dans la règle gagnante, les représentants qui lui sont assignés sont le pool éligible, et le tour de table et le comportement de tous les agents décrits ci-dessus s&#39;appliquent à ce pool.

## Étape suivante {#next}

Une fois les représentants configurés et le routage décidé, ajoutez les capacités à un concierge. Voir [&#x200B; Activer le chat en direct et la réservation de réunions](configure-in-composer.md).
