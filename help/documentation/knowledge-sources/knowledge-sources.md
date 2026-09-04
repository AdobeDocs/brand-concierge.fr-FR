---
title: Création et gestion des sources de connaissances pour Brand Concierge
description: Découvrez comment créer AEM Sites, des liens de site web et des sources de connaissances de catalogue de produits pour Brand Concierge, surveiller l’état du traitement et résoudre les problèmes d’explore.
hide: true
source-git-commit: 3f05cb0dd8c11620b0ed7e254d0f4f9b24408b08
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 1%

---


# Création et gestion des sources de connaissances pour Brand Concierge

Une source de connaissances est le contenu qu’un concierge peut utiliser pour répondre aux questions des visiteurs. Chaque concierge nécessite au moins une source de connaissances configurée. Les sources de connaissances sont créées indépendamment et peuvent être réutilisées par plusieurs concierges.

Un concierge répond aux questions en utilisant uniquement ses sources de connaissances configurées. Il ne répond pas à partir des connaissances générales du monde.

>[!NOTE]
>
>Si un visiteur pose des questions sur des informations en dehors des sources de connaissances configurées, le concierge est conçu pour indiquer qu’il ne dispose pas des informations nécessaires, au lieu de générer une réponse non prise en charge. Utilisez le processus d’évaluation pour vérifier ce comportement.

## Choisir une source de connaissances

Brand Concierge prend en charge les types de sources de connaissances suivants :

| Source de connaissances | Utilisez-le lorsque | Fonctionnalité principale |
| --- | --- | --- |
| AEM Sites (index IA dédiée au contenu) | Le client utilise AEM Sites as a Cloud Service avec l’IA dédiée au contenu activée. | Utilise un index IA dédiée au contenu existant et rend le contenu AEM Sites mis à jour disponible sans explore distincte ni étape d’actualisation. |
| Liens de site web | Le ou la client(e) doit explorer à un site web, quelle que soit la plateforme utilisée pour le créer. | Explore un plan de site, des URL individuelles sélectionnées ou des URL fournies dans un fichier CSV. |
| Catalogue de produits | Le client dispose d’un catalogue de produits ou de services relativement petit et n’utilise pas Adobe Commerce. | Active les liens profonds du produit et les cartes produit dans les réponses du concierge. |

>[!IMPORTANT]
>
>Les clients qui vendent via Adobe Commerce avec un catalogue volumineux doivent utiliser l’intégration MCP de Commerce à la place.

## Création d’une source de connaissances AEM Sites

Utilisez une source de connaissances AEM Sites lorsque le client utilise déjà AEM Sites as a Cloud Service avec l’IA dédiée au contenu activée.

1. Sélectionnez **Créer une Source de connaissances**.
1. Choisissez **** puis sélectionnez **Continuer**.
1. Saisissez un nom et une description pour la source de connaissances. Par exemple, utilisez `My main website` comme nom.
1. Sélectionnez un index IA dédiée au contenu existant dans la liste. La liste est renseignée à partir de l’instance AEM Sites as a Cloud Service.
1. Sélectionnez **Enregistrer**.

Cette intégration native met automatiquement le contenu AEM Sites mis à jour à la disposition de Brand Concierge. Une explore distincte ou une étape d’actualisation ne sont pas requises.

## Création d’une source de connaissances sur les liens de sites Web

Utiliser une source de connaissances sur les liens de sites Web pour un site Web explorable. Cette option fonctionne pour les sites web créés sur n’importe quelle plateforme et est recommandée pour la plupart des nouveaux utilisateurs.

1. Sélectionnez **Créer une Source de connaissances**.
1. Choisissez **Liens de site web** puis sélectionnez **Continuer**.
1. Saisissez un nom pour la source de connaissances.
1. Ajoutez les sources de contenu à l’aide de l’une des méthodes suivantes :

   - **URL du plan de site :** ajoutez une URL qui répertorie les pages du site. Toutes les pages répertoriées dans le plan du site sont explorées.
   - **URL individuelles :** ajoutez des URL de page spécifiques une par une. Seules les pages ajoutées sont explorées.
   - **Chargement CSV :** téléchargez l’exemple de fichier, ajoutez les URL et chargez le fichier CSV terminé.

1. (Facultatif) Planifiez une fréquence d’actualisation, par exemple une fois par semaine à un jour et à une heure spécifiques, pour que la source de connaissances reste à jour au fur et à mesure des modifications du site web.
1. Sélectionnez **Ajouter** ou **Créer**.

Le système explore les URL spécifiées et gratte leur contenu pour créer la source de connaissances.

>[!TIP]
>
>Un plan de site est généralement disponible à l’adresse `yourwebsite.com/sitemap.xml`. Si le site web ne fournit pas de plan de site, ajoutez des URL de page individuelles à la place.

## Créer une source de connaissances sur le catalogue de produits

Utilisez une source de connaissances du catalogue de produits pour les clients disposant d’un plus petit ensemble de produits ou de services, environ moins de 100, qui n’utilisent pas Adobe Commerce.

Lorsqu’une réponse du concierge fait référence à un produit, le catalogue de produits peut fournir un lien profond vers la page produit et activer une fiche produit. Une fiche produit peut inclure une image, un titre, une description et un ou deux boutons.

1. Sélectionnez **Créer une Source de connaissances**.
1. Choisissez **Catalogue de produits** puis sélectionnez **Continuer**.
1. Saisissez un nom pour la source de connaissances. Par exemple, utilisez `My product catalog - US region` comme nom.
1. Sélectionnez un schéma. Le schéma définit les champs de produit (tels que l’image, le titre, la description et les boutons) qui sont affichés, ainsi que l’emplacement du lien entre les boutons.
1. Téléchargez l’exemple de feuille de calcul pour le schéma sélectionné.
1. Ajoutez les données de produit à la feuille de calcul et chargez-les.
1. Sélectionnez **Enregistrer**.

Des configurations de bouton différentes nécessitent des schémas différents.

## Surveiller l’état de la source de connaissances

Chaque source de connaissances affiche un statut de traitement.

| État | Signification |
| --- | --- |
| En cours | La source de connaissances est en cours de traitement. |
| Réussite | La source de connaissances est entièrement traitée et prête à être utilisée. |
| Planifiée | La source de connaissances sera traitée à une heure planifiée ultérieure. |
| Succès partiel | Certaines pages ont été traitées avec succès et d’autres ont échoué. |

La page Détails de la source de connaissances fournit des informations telles que :

- Le créateur.
- Date de création.
- Nombre de liens ou de pages fournis.
- Nombre de liens ou de pages qui ont réussi ou échoué.
- La dernière actualisation.
- Les URL prises en compte pour le traitement.

## Résolution des problèmes liés aux échecs de traitement

Si une source de connaissances affiche un statut Succès partiel, utilisez le rapport de problème pour identifier les URL qui n’ont pas pu être traitées.

1. Ouvrez la page des détails de la source de connaissances.
1. Sélectionnez **Corriger les problèmes** pour télécharger un fichier contenant les URL endommagées ou non nettoyées, ainsi que les détails de leur erreur.
1. Corrigez les URL non valides ou supprimez-les de la liste source.
1. Chargez à nouveau la liste d’URL corrigée, le cas échéant.
1. Demandez un retraitement afin que le contenu corrigé soit ajouté à la source de connaissances.
