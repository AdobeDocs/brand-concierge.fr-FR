---
title: Boîte de réception de conversation
description: Découvrez comment un commercial reçoit, gère, note et termine une discussion en direct Brand Concierge dans la boîte de réception de conversation Adobe Marketo Qualifier.
role: User
level: Beginner
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 91cbec8d6f4e4800e3bdc8c8f60bfe9ed168a963
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 1%
---
# Boîte de réception du chat {#chat-inbox}

Lorsqu’un visiteur demande à parler à quelqu’un, le chat arrive dans la boîte de réception **[!UICONTROL Chat]** en [!DNL Adobe Marketo Qualifier]. Cette page présente le point de vue du représentant d’un chat en direct : ce que vous voyez lorsqu’il arrive, le contexte que vous obtenez et ce que vous devez faire avant de pouvoir le fermer.

Pour ouvrir la boîte de réception de conversation, dans le panneau de gauche sous **[!UICONTROL Activités]**, sélectionnez **[!UICONTROL Boîte de réception de conversation]**.

## Recevoir une conversation {#receive}

Votre statut s’affiche dans le coin supérieur droit de la boîte de réception. **[!UICONTROL Disponible]** signifie que vous pouvez recevoir des chats maintenant. Vos heures de disponibilité du chat en direct déterminent si vous êtes éligible ; voir [Définir la disponibilité du chat en direct](representative-setup.md#chat-availability).

La façon dont une conversation vous parvient dépend du type de routage défini sur l’intégration **[!UICONTROL conversation en direct]** :

* Avec la rotation, chaque représentant éligible est averti en même temps et le premier à accepter prend la conversation.
* Avec l&#39;agent direct, le chat vient toujours au représentant nommé.
* Avec le routage personnalisé, la conversation a lieu avec les représentants affectés à la règle de priorité la plus élevée à laquelle le visiteur correspond.

Deux onglets organisent vos conversations :

* **[!UICONTROL Actif]** — conversations en cours.
* **[!UICONTROL Toutes]** — toutes les conversations, y compris celles qui sont terminées.

## Prenez la conversation {#pick-up}

On ne commence jamais à froid. Avant de taper quoi que ce soit, la boîte de réception vous donne tout ce que le visiteur a déjà dit au concierge.

![Boîte de réception de conversation présentant le résumé de la conversation avec le visiteur, les sujets abordés et le panneau des détails du profil](../assets/sales-handoff-inbox-1.png){width="800" zoomable="yes"}

| Ce que vous voyez | Ce que ça donne |
| --- | --- |
| **[!UICONTROL Récapitulatif de la conversation des visiteurs]** | Un **[!UICONTROL résumé]** de la conversation que le visiteur a eue avec le concierge et les **[!UICONTROL sujets abordés]** |
| Transcription de la conversation | L&#39;échange complet avec le concierge, au-dessus du point où le chat en direct a été initié |
| **[!UICONTROL Détails du formulaire]** | Ce que le visiteur a saisi dans le formulaire de préconversation avant que vous ne vous inscriviez, tel que l’e-mail, l’intérêt du produit et la société |

La transcription marque la remise avec deux lignes système, `Live chat session has been initiated` et `Agent <name> has joined the chat`, afin que vous puissiez toujours dire quelle partie de la conversation était le concierge et quelle partie est la vôtre.

Saisissez dans la zone de message et sélectionnez **[!UICONTROL Envoyer]** pour répondre.

![Discussion en direct en cours entre le représentant et le visiteur](../assets/sales-handoff-inbox-2.png){width="800" zoomable="yes"}

## Noter la conversation {#conversation-score}

Avant de terminer une conversation, évaluez la qualification du visiteur. Le score est fixé par vous, le représentant qui a réellement parlé au visiteur, ce qui le rend digne de confiance en aval.

Dans le panneau **[!UICONTROL Détails du profil]**, sous **[!UICONTROL Note de conversation]**, sélectionnez une note. Le tiret signifie aucun score, et les icônes de flamme évaluent la conversation du moins qualifié au plus qualifié.

![Infobulle du score de conversation expliquant que les scores sont stockés dans l’enregistrement du prospect comme 0, 1, 2 et 3](../assets/sales-handoff-inbox-4.png){width="600" zoomable="yes"}

| Sélection | Valeur stockée | Signification |
| --- | --- | --- |
| Tiret | 0 | Moins qualifié |
| Une flamme | 1 | Assez qualifié |
| Deux flammes | 2 | Qualifié |
| Trois flammes | 3 | Les plus qualifiés |

>[!IMPORTANT]
>
>La notation est obligatoire. Si vous essayez de fermer une conversation sans la noter, le `Please score the conversation before you close the chat` d’erreur s’affiche et la conversation reste ouverte. Une fois que vous l’avez noté, une confirmation s’affiche et vous pouvez fermer la conversation.

![Confirmation que le score de conversation a été enregistré](../assets/sales-handoff-inbox-3.png){width="800" zoomable="yes"}

Le score est écrit dans l’activité **[!UICONTROL Engage avec un chat en direct dans Concierge]** en [!DNL Marketo Engage], où il est disponible comme contrainte sur les filtres et les déclencheurs. Utilisez-le pour effectuer le reciblage, la notation des prospects, la personnalisation et la remise du CRM. Voir [Données Brand Concierge dans Marketo Engage](marketo-activities.md).

## Terminer la conversation {#end-chat}

Sélectionnez **[!UICONTROL Terminer la conversation]** pour fermer la conversation. Le visiteur peut également l’envoyer de son côté et est invité à confirmer son choix en premier.

Lorsqu’une conversation se ferme, son statut de conversation est enregistré comme l’une des deux valeurs suivantes :

* **Terminé** — la conversation a été clôturée délibérément, par vous ou par le visiteur.
* **Abandonné** — le visiteur a quitté le site et la conversation a expiré suite à une période d&#39;inactivité.

>[!NOTE]
>
>Les conversations en direct sont conservées pendant 30 jours.

## Étape suivante {#next}

Découvrez ce que tout cela écrit dans votre base de données marketing dans les données [Brand Concierge de Marketo Engage](marketo-activities.md).
