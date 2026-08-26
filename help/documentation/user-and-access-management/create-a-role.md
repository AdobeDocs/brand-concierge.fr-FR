---
title: Création d’un rôle avec l’autorisation Brand Concierge
description: Découvrez comment créer un rôle et lui accorder l’autorisation requise pour accéder à Brand Concierge.
source-git-commit: 591bd1600e586a0a4ce484dbff3f9fb97e24d43d
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Création d’un rôle avec l’autorisation Brand Concierge

Créez un rôle dans Autorisations Adobe Experience Platform pour accorder aux utilisateurs l’accès à Brand Concierge.

## Conditions préalables

* Vous devez disposer des autorisations d’administrateur requises pour gérer les rôles et les autorisations.
* L’utilisateur doit d’abord être ajouté à l’organisation Adobe Experience Platform. Pour plus d’informations, voir « Ajouter un utilisateur à l’organisation » (LIEN).

## Créer le rôle

1. Connectez-vous à `experienceplatform.adobe.com`.

   >[!NOTE]
   >
   >Confirmez l’URL de production auprès des ingénieurs avant de publier cette procédure. L’enregistrement source utilisait une URL informelle ou éventuellement mal transcrite.

2. Dans le volet de navigation de gauche, faites défiler l’écran jusqu’à et sélectionnez **Autorisations**.
3. Sélectionnez **Rôles** pour afficher les rôles existants, puis sélectionnez **Créer un rôle**.
4. Saisissez un nom pour le rôle, tel que `Brand Concierge Access Users`, ajoutez une description et confirmez la création.
5. Ouvrez le nouveau rôle et attribuez les autorisations :

   1. Recherchez **&#x200B;**&#x200B;dans la liste des autorisations.
   2. Sélectionnez **Gérer Brand Concierge**.

   Actuellement, **Gérer Brand Concierge** est la seule autorisation Brand Concierge disponible. Les niveaux d’autorisation granulaires ne sont actuellement pas disponibles.

6. Sélectionnez le ou les sandbox auxquels le rôle peut accéder.

   Une organisation peut contenir plusieurs sandbox, qui sont des espaces de travail isolés. Sélectionnez uniquement les sandbox appropriés pour ce rôle.

7. Sélectionnez **Enregistrer**.

## Étapes suivantes

Une fois le rôle créé, ajoutez-y des utilisateurs et utilisatrices. Pour plus d’informations, voir « Ajouter des utilisateurs au rôle » (LIEN).

## Considérations connexes

* Le processus de création et de gestion des sandbox n’entre pas dans le cadre de cette procédure.
* Vérifiez si des autorisations Brand Concierge granulaires supplémentaires sont prévues avant de définir un modèle de rôle à long terme.
