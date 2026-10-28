---
title: Données Brand Concierge dans Marketo Engage
description: Découvrez les champs sources de prospect et les trois types d’activités Concierge écrits dans Adobe Marketo Engage, ainsi que leur utilisation dans les listes intelligentes et les campagnes intelligentes.
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
source-git-commit: 91cbec8d6f4e4800e3bdc8c8f60bfe9ed168a963
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 4%
---
# Données Brand Concierge dans Marketo Engage {#marketo-activities}

Lorsque [!DNL Adobe Marketo Engage] est connecté, chaque visiteur qui remplit un formulaire, réserve une réunion ou commence une discussion en direct devient un enregistrement de personne dans [!DNL Marketo], et son engagement auprès du concierge est écrit dans cet enregistrement en tant que type d’activité natif. Cela signifie que vous pouvez créer des listes intelligentes et des campagnes intelligentes sur le comportement du concierge exactement comme vous le feriez pour toute autre activité de [!DNL Marketo].

>[!NOTE]
>
>Le chat en direct et la réservation de réunions eux-mêmes ne nécessitent pas de [!DNL Marketo Engage]. Sans cela, les données décrites sur cette page restent en [!DNL Adobe Marketo Qualifier]. Voir [Présentation des discussions en direct et des réservations de réunion](overview.md#prerequisites).

## Création de leads et attribution de sources {#lead-creation}

Une personne créée par l&#39;intermédiaire d&#39;un concierge est identifiée afin que vous puissiez toujours savoir d&#39;où elle vient.

| Champ | Valeur |
| --- | --- |
| Source Personne **&#x200B;**&#x200B;| `Brand Concierge` |
| **[!UICONTROL Type Source d’origine]** | `Chat` |
| **[!UICONTROL Informations Source d’origine]** | `Concierge` |
| **[!UICONTROL Type de Source d’enregistrement]** | `Chat` |
| **[!UICONTROL Informations d’enregistrement Source]** | `Concierge` |

![Onglet Informations sur l’enregistrement de personne Marketo affichant le Source de personne défini sur Brand Concierge et les champs source de conversation et de concierge](../assets/sales-handoff-marketo-1.png){width="800" zoomable="yes"}

## Types d’activités {#activity-types}

Trois types d’activité natifs sont transmis à l’enregistrement de personne. Tous trois sont disponibles en tant que déclencheurs et filtres.

![Journal d&#39;activités Marketo pour une personne affichant Engage with Concierge, Schedule Meeting in Concierge, et Engage with Live Chat dans les entrées Concierge](../assets/sales-handoff-marketo-2.png){width="800" zoomable="yes"}

### Communiquer avec le concierge {#engage-with-concierge}

Consigné lorsqu’un visiteur interagit avec le concierge.

| Attribut | Description |
| --- | --- |
| Nom du concierge | Le concierge avec lequel le visiteur a été engagé |
| ID de conversation | Identifiant de la conversation. Utilisez-le dans le compositeur pour ouvrir la transcription complète. |
| Page URL (URL de la page) | Page sur laquelle s’est produit l’engagement |
| Créé le | Date de création de la conversation |
| Durée | Combien de temps a duré la conversation ? |

>[!NOTE]
>
>Certains attributs de ce type d’activité, notamment les rubriques abordées, le résumé et la langue, sont prévus pour une version ultérieure.

### Planifier une réunion au Concierge {#schedule-meeting}

Connecté deux fois pour une seule réservation, ce qui permet de séparer l’intention du résultat.

Tout d&#39;abord, à l&#39;initiation : le visiteur a sélectionné l&#39;option de planifier une réunion et le formulaire de réservation s&#39;est affiché. Le statut de la réunion est `Started`.

| Attribut | Description |
| --- | --- |
| Statut de la réunion | `Started` |
| Page URL (URL de la page) | Page sur laquelle le visiteur a effectué la réservation |
| ID Concierge | Le concierge avec lequel le visiteur a été engagé |
| ID de personne | Enregistrement de personne [!DNL Marketo] |

Ensuite, lors de la réservation : le visiteur a confirmé un créneau horaire. Le statut de la réunion est `Scheduled`.

| Attribut | Description |
| --- | --- |
| Statut de la réunion | `Scheduled` |
| Nom du représentant commercial | Représentant avec lequel la réunion a été réservée |
| E-mail du représentant commercial | Adresse e-mail du représentant |
| Planifié pour | Date et heure de la réunion |
| Durée de la réunion | Durée de la réunion réservée |
| Type de transmission | Type de routage qui a sélectionné ce représentant |
| Page URL (URL de la page) | Page sur laquelle le visiteur a réservé |
| ID Concierge | Le concierge avec lequel le visiteur a été engagé |
| ID de personne | Enregistrement de personne [!DNL Marketo] |

>[!TIP]
>
>Créez une liste dynamique des personnes dont le `Meeting Status` est `Started`, mais pas `Scheduled` de trouver toutes les personnes qui ont commencé à réserver une réunion et l’ont abandonnée. Il s’agit d’une audience prête à l’emploi ou de reciblage.

### Communiquer avec le service de conversation en direct de Concierge {#engage-with-live-chat}

Consigné après la fin d’une conversation en direct.

| Attribut | Description |
| --- | --- |
| Statut de la conversation | `Ended` si la conversation a été fermée délibérément, `Dropped` si le visiteur a quitté le site et que la conversation a expiré |
| Agents notifiés | Les adresses e-mail de chaque représentant qui a été averti de cette conversation |
| Score de la conversation | La note de 0 à 3 attribuée au représentant a donné la conversation. Voir [&#x200B; Noter la conversation &#x200B;](chat-inbox.md#conversation-score) |
| Page URL (URL de la page) | Page sur laquelle le chat en direct a été lancé |
| ID Concierge | Le concierge avec lequel le visiteur a été engagé |
| Identifiant de session | Identifiant de session de conversation en direct |
| Heure de début | Quand la conversation a commencé |

>[!TIP]
>
>Le score de conversation est ici l’attribut avec la valeur la plus élevée, car c’est un humain qui a réellement parlé au visiteur qui l’a défini. Utilisez-le pour la notation des prospects, le reciblage, la personnalisation et la remise à l’équipe commerciale et au CRM.

## Utilisation des données du Concierge dans une campagne dynamique {#smart-campaign}

Dans la **[!UICONTROL liste dynamique]** d’une campagne dynamique, recherchez `concierge` pour afficher tous les éléments disponibles.

![Liste dynamique Marketo présentant les déclencheurs et filtres de concierge disponibles pour l’activité Brand Concierge](../assets/sales-handoff-marketo-3.png){width="800" zoomable="yes"}

| Catégorie | Éléments disponibles |
| --- | --- |
| **[!UICONTROL Triggers]** | Dialoguer avec Concierge, Dialoguer avec Concierge en direct, Organiser une réunion avec Concierge |
| **[!UICONTROL Filtres]** > **[!UICONTROL Historique des activités]** | Engagé avec Concierge, Engagé avec le chat en direct dans Concierge, Réunion programmée dans Concierge |
| **[!UICONTROL Filtres]** > **[!UICONTROL Filtres d’inactivité]** | Pas d’engagement avec le concierge, Pas d’engagement avec le chat en direct avec le concierge, Pas de réunion programmée avec le concierge |

Faites glisser un déclencheur ou un filtre sur la zone de travail, puis sélectionnez **[!UICONTROL Ajouter une contrainte]** pour le réduire.

### Contraintes {#constraints}

| Déclencheur ou filtre | Contraintes |
| --- | --- |
| Communiqué avec le concierge | Nom du concierge, URL de la page, Date de création, Durée, Date de l’activité |
| Réunion programmée au Concierge | Nom du concierge, nom du représentant commercial, statut de la réunion, prévu pour, durée de la réunion, type de transmission, URL de la page, date de l’activité |
| Engagé avec le chat en direct dans Concierge | Nom du concierge, nom du représentant commercial, statut de la conversation, score de la conversation, heure de début, heure acceptée, heure de fin, date de clôture, durée, sujet abordé, URL de la page, langue, date de l’activité |

## Étape suivante {#next}

Examinez les performances des réunions et des conversations dans [Surveillez les réunions et les conversations en direct](monitor.md).
