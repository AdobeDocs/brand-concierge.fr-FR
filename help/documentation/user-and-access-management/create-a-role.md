---
title: Création d’un rôle avec l’autorisation Brand Concierge
description: Découvrez comment créer un rôle et lui accorder l’autorisation requise pour accéder à Brand Concierge.
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# Création d’un rôle avec l’autorisation Brand Concierge

Créez un rôle dans Autorisations Adobe Experience Platform pour accorder aux utilisateurs l’accès à Brand Concierge.

>[!PREREQUISITES]
>
>- Vous devez disposer des autorisations d’administrateur requises pour gérer les rôles et les autorisations.
>- L’utilisateur doit d’abord être ajouté à l’organisation Adobe Experience Platform. Pour plus d’informations, voir [Ajouter un utilisateur à l’organisation](./add-a-user-to-the-org.md).

## Créer le rôle

1. Connectez-vous à `experienceplatform.adobe.com`.

   >[!NOTE]
   >
   >Confirmez l’URL de production auprès des ingénieurs avant de publier cette procédure. L’enregistrement source utilisait une URL informelle ou éventuellement mal transcrite.

1. Dans le volet de navigation de gauche, faites défiler l’écran jusqu’à et sélectionnez **Autorisations**.
1. Accédez à **Rôles** pour afficher les rôles existants, puis sélectionnez **Créer un rôle**.
1. Saisissez un nom pour le rôle, tel que `Brand Concierge Access Users`, ajoutez une description et confirmez la création.
1. Ouvrez le nouveau rôle et attribuez les autorisations :

   1. Recherchez **&#x200B;**&#x200B;dans la liste des autorisations.
   1. Sélectionnez **Gérer Brand Concierge**.

   Actuellement, **Gérer Brand Concierge** est la seule autorisation Brand Concierge disponible ; les niveaux d’autorisation granulaires ne sont pas encore disponibles.

1. Sélectionnez le ou les sandbox auxquels le rôle peut accéder.

   Une organisation peut contenir plusieurs sandbox, qui sont des espaces de travail isolés. Sélectionnez uniquement les sandbox appropriés pour ce rôle.

1. Sélectionnez **Enregistrer**.

## Étapes suivantes

Une fois le rôle créé, ajoutez-y des utilisateurs et utilisatrices. Pour plus d’informations, voir [&#x200B; Ajouter des utilisateurs au rôle Brand Concierge &#x200B;](./add-a-user-to-the-role.md).

## Éléments à noter

- Le processus de création et de gestion des sandbox n’entre pas dans le cadre de cette procédure.
- Vérifiez si des autorisations Brand Concierge granulaires supplémentaires sont prévues avant de définir un modèle de rôle à long terme.
