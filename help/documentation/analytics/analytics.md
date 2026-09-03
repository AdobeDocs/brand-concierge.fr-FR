---
title: Analyse des performances du concierge
description: Découvrez comment vérifier les analyses du concierge, examiner les transcriptions de conversation, ajouter des questions aux visiteurs des ensembles d’évaluation et ouvrir les rapports Customer Journey Analytics.
hide: true
source-git-commit: da4b30fa292b911987aebec378af420b293ea594
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---


# Analyse des performances du concierge

**À qui cela s’adresse** professionnels du marketing qui utilisent l’expérience en libre-service. Aucune configuration n’est requise après le déploiement du concierge.

**Cadence recommandée :** passez en revue les analyses si nécessaire. Un enregistrement hebdomadaire est un point de départ raisonnable.

Analytics vous aide à comprendre comment les visiteurs interagissent avec un concierge en direct. Après le déploiement, l’onglet **Analytics** affiche automatiquement les mesures de conversation et permet d’accéder à des transcriptions individuelles et à un rapport Customer Journey Analytics plus détaillé.

## Afficher les analyses

1. Ouvrez le Concierge et sélectionnez l’onglet **Analytics**.

1. Définissez la période que vous souhaitez consulter.

1. Vous pouvez éventuellement filtrer les résultats par type de conversation.

L’onglet Analytics affiche automatiquement les mesures suivantes :

| Mesure | Description |
|---|---|
| Conversations | Nombre de conversations au cours de la période sélectionnée. |
| Visiteurs engagés | Nombre de visiteurs et visiteuses qui ont contacté le concierge. |
| Sentiment positif | Quantité de sentiments positifs détectés dans les conversations. |
| Messages par conversation | Nombre moyen de messages échangés au cours d’une conversation. |

>[!NOTE]
>
>Aucune configuration n’est requise pour afficher ces mesures après le déploiement du concierge.

## Vérifier les transcriptions de conversation

Les transcriptions de conversation vous permettent de consulter les demandes des visiteurs et les réponses du concierge.

1. Dans l’onglet Analytics , sélectionnez une conversation.

1. Lisez la transcription complète.

1. Vérifiez si les visiteurs ont sélectionné une note de pouces vers le haut ou vers le bas pour chaque réponse.

Chaque conversation possède un identifiant de conversation unique. Utilisez cet identifiant pour faire correspondre la transcription aux enregistrements d’autres systèmes lorsque votre implémentation prend en charge ce workflow.

### Ajouter une conversation à un jeu d’évaluation

Si un visiteur pose une question utile pour des tests ultérieurs, ajoutez-la directement à un jeu d’évaluation à partir du relevé de notes.

1. Ouvrez le relevé de notes de la conversation.

1. Sélectionnez **Ajouter à l’évaluation**.

L’ajout de questions réelles aux visiteurs aide à maintenir les jeux d’évaluation basés sur les questions réelles des visiteurs. Pour plus d’informations sur les jeux d’évaluation, voir [ Évaluer un concierge ](../evaluation/evaluation.md).

>[!TIP]
>
>Passez régulièrement en revue les transcriptions et ajoutez des questions représentatives, et pas seulement des questions qui ont reçu une rétroaction négative, pour aider à maintenir un ensemble d&#39;évaluation équilibré.

## Ouvrir le rapport Customer Journey Analytics

Sélectionnez **Afficher le rapport** pour afficher un tableau de bord plus détaillé dans Adobe Customer Journey Analytics (CJA). Le tableau de bord est automatiquement configuré et ne nécessite aucune configuration supplémentaire.

Le tableau de bord CJA comprend les éléments suivants :

- Tendances hebdomadaires des conversations.
- Engagement répété, y compris les conversations par personne.
- Messages par conversation.
- Tendances des commentaires des visiteurs.
- Intention du visiteur.
- Sentiment et tonalité du visiteur.
- Recommandations du concierge lors des conversations.

Utilisez le tableau de bord pour examiner les tendances au fil du temps et identifier les changements dans l’engagement des visiteurs, les commentaires, l’intention et le sentiment.

>[!IMPORTANT]
>
>Ne pas traiter les ID de conversation comme un workflow d’exportation. Une présentation dédiée du produit ou de l’ingénierie est nécessaire avant de documenter comment exporter des conversations ou des transcriptions.
