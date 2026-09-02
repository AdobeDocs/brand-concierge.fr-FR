---
title: Déployer un concierge
description: Découvrez comment déployer un Brand Concierge en configurant un flux de données, en installant le script de déploiement, en définissant des règles de surface et en vérifiant le déploiement.
hide: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Déployer un concierge

Le déploiement de met un concierge à la disposition des véritables visiteurs du site web. Le spécialiste marketing configure les paramètres de déploiement, tandis que l’équipe informatique ou d’analyse fournit l’identifiant du flux de données et que l’équipe du site web installe le script de déploiement sur le site web.

Le déploiement est généralement une configuration brève et unique pour chaque site. Prévoyez environ 15 minutes du côté du spécialiste marketing, ainsi que le temps nécessaire à l’équipe du site web pour installer le script.

>[!IMPORTANT]
>
>Impliquez rapidement l’équipe informatique ou d’analyse et l’équipe du site web. Leur participation est requise pour fournir l’identifiant du flux de données et installer le script. Par conséquent, le déploiement ne doit pas être traité comme la dernière étape de la mise en œuvre.

## Avant de commencer

- Coordonnez-vous avec l’équipe informatique ou d’analyse pour obtenir un identifiant de flux de données.
- Identifiez l’équipe responsable du site web ou du gestionnaire de balises. Cet article désigne ce groupe comme l’équipe du site web.
- Décidez si le concierge doit apparaître en tant que composant sur les pages existantes ou en tant que page dédiée complète.
- Identifiez les domaines et les chemins de page où le concierge doit apparaître.

## Configurer le flux de données

Un flux de données est la destination des données d’activité générées par les interactions des visiteurs avec le concierge. Parmi ces interactions, citons notamment les clics, les envois de formulaire, les réunions réservées et les conversations en direct. Le flux de données permet d’afficher cette activité ultérieurement dans Analytics.

Vous n’avez pas besoin de créer un flux de données dans le cadre de cette procédure. Vous n’avez besoin que de son identifiant.

### Obtention de l’identifiant du flux de données

Demandez l’identifiant du flux de données à l’équipe informatique ou à l’équipe d’analyse. L’identifiant se trouve dans Adobe Experience Platform sous **Collecte de données** > **Flux de données**.

### Ajouter la configuration du flux de données

1. Préparez l’identifiant du flux de données.
1. Dans la section Déploiement de Brand Concierge , sélectionnez **Ajouter la configuration**.
1. Collez l’identifiant du flux de données.
1. Enregistrez la configuration.
1. Une fois la configuration enregistrée, sélectionnez l’option d’installation appropriée :
   - **Installation du composant :** utilisez un fragment de code que l’équipe du site web place à un emplacement spécifique sur le site web.
   - **Installation en page entière :** utilisez une page complète, prête à héberger pour une page de destination de concierge dédiée.
1. Fournissez le script ou la page sélectionné à l’équipe du site web.
1. Demandez à l’équipe du site web d’installer le script directement dans le code de page ou par le biais d’un gestionnaire de balises.

>[!NOTE]
>
>L’installation est généralement gérée par l’équipe du site web, comme l’ajout d’une balise d’outil d’analyse ou de conversation.

## Configuration de la surface

Une fois le script installé, la configuration de la surface contrôle les pages sur lesquelles apparaît le concierge. Par exemple, vous pouvez configurer le service de conciergerie pour qu’il apparaisse sur les pages de produits, mais pas sur une page de carrières.

### Ajout de règles de domaine et de page

1. Ajoutez un domaine, tel que `blog.example.com`.
1. Choisissez la manière dont les chemins d’accès sur le domaine doivent correspondre. Les modèles correspondants disponibles sont les suivants :
   - N’importe quelle page sous le domaine.
   - Chemins commençant par une valeur spécifiée.
   - Chemins qui se terminent par une valeur spécifiée.
   - Correspondance de chemin exacte.
1. Combinez plusieurs règles pour définir une couverture de page plus précise.
1. Enregistrez la configuration de la surface.

## Vérification du déploiement

Une fois que l’équipe du site web a installé le script et que les règles de surface sont enregistrées, vérifiez que :

- Le script est présent sur les pages du site web prévues.
- Le concierge s’affiche uniquement sur les pages couvertes par les règles configurées.
- Le concierge n’apparaît pas sur les pages exclues.
- Les interactions des visiteurs génèrent des données d’activité pour le flux de données configuré.

>[!TIP]
>
>Testez une page incluse et une page exclue. Cela confirme que les règles de surface fonctionnent comme prévu avant que le concierge ne soit largement disponible.

## Questions ouvertes et notes de portée

Le matériau source ne définit pas les détails suivants :

- Liste complète et canonique des types d’événements envoyés au flux de données. Les exemples fournis incluent les clics, les envois de formulaire, les réunions réservées et les conversations en direct, mais la liste complète doit être confirmée par l’ingénierie.
- Si la configuration du flux de données diffère entre les clients d’évaluation et payants.
- Le produit d’analyse spécifique dans lequel l’activité de flux de données est affichée. Le document source fait uniquement référence à ce produit en tant qu’« Analytics ».

Ces questions peuvent faire double emploi avec des exigences de télémétrie distinctes et doivent être résolues avec l’équipe d’ingénierie ou l’équipe produit appropriée avant de publier les directives de déploiement comme référence définitive.

## Contenu source incomplet

La source fournie se termine brutalement à l&#39;étape 8, qui n&#39;a pas de contenu.
