---
description: Notes de mise à jour actuelles d’Adobe Brand Concierge.
title: Notes de mise à jour actuelles
hide: true
feature: Release Information
source-git-commit: 234b1b699970c97c6f3f997d790416d45c1c3a24
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Informations sur la version actuelle {#current-release-notes}

Adobe Brand Concierge suit un modèle de diffusion continu, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, améliorations et correctifs.

Toutes les fonctionnalités sont généralement disponibles, sauf indication contraire.

## Avril 2026 {#april-2026}

* **Intégration de Brand Concierge à Real-Time CDP (disponibilité limitée)** : améliorez la qualité et la pertinence des réponses conversationnelles en incorporant le contexte Real-Time CDP, tel que les attributs utilisateur, les signaux comportementaux et les interactions antérieures, afin de mieux aligner les réponses sur l’intention de l’utilisateur.

* **Amélioration de l’optimisation en libre-service** : le compositeur Brand Concierge évalue automatiquement les performances de la conversation et met à jour les configurations d’invite pour améliorer la qualité de la réponse. Ces optimisations sont continuellement appliquées en fonction des résultats d’évaluation automatisés, ce qui réduit la nécessité d’un réglage manuel.

* **Recommandations de produits contextuelles** : Brand Concierge fournit des recommandations de produits basées sur l’intention de l’utilisateur déduite, en exploitant les données structurées du catalogue de produits et la capacité d’intégration aux systèmes d’enregistrement de recherche et de recommandation de produits pour améliorer la pertinence et la précision. Des cartes produits sont présentées le cas échéant, prenant en charge les recommandations multi-produits et s’alignant sur les intentions de découverte ou d’achat.

* **Comparaison côte à côte** : permet la comparaison côte à côte de plusieurs produits dans la conversation par le biais d’une vue de tableau structurée, en mettant en évidence les attributs, fonctionnalités et différences clés. La comparaison est générée dynamiquement en fonction de l’intention de l’utilisateur et des produits sélectionnés, ce qui permet une évaluation et une prise de décision plus éclairées.

* **Agent d’assistance (dépannage et conseils pratiques)** : activez l’assistance guidée au cours de la conversation en aidant les utilisateurs à résoudre les problèmes et à effectuer des tâches pratiques grâce à une assistance contextuelle. L’agent adapte les réponses en fonction des entrées de l’utilisateur afin de résoudre efficacement les problèmes sans nécessiter d’escalade.

## Mars 2026 {#march-2026}

* **Configuration d’AEM Site Advisor dans le compositeur** : la configuration d’AEM Site Advisor dans le compositeur permet aux clients AEM de configurer facilement l’ingestion de la source de connaissances directement dans le compositeur, avec le contenu du site web AEM comme source de connaissances principale. Cela réduit les frictions d’intégration tout en garantissant des réponses précises, conformes et prévisibles, fondées sur le propre contenu AEM du client.

* **Ingestion complète du site** : l’ingestion complète du site permet aux clients d’ingérer automatiquement l’ensemble de leur site web à l’aide d’un seul plan de site, éliminant la nécessité de charger des URL manuellement. Cela garantit une couverture de contenu complète et à jour avec une intégration évolutive et à faible effort, ainsi qu’une fraîcheur continue du contenu.

* **Création automatisée d’invite (disponibilité limitée)** : la création automatisée d’invite permet aux clients de créer une expérience Brand Concierge de haute qualité par le biais d’un flux simple en libre-service. Brand Concierge génère automatiquement des invites de conciergerie à partir d&#39;entrées utilisateur minimales sans exposer ni nécessiter d&#39;invite d&#39;ingénierie. Les utilisateurs non techniques peuvent rapidement obtenir un concierge fonctionnel dont la qualité est validée grâce à la validation guidée du profil de marque et à la configuration pilotée par l’IA.

* **BYOA - Agent Firefly dans Adobe.com Brand Concierge** : la génération d’images Firefly est désormais intégrée à Adobe.com Brand Concierge, ce qui permet aux utilisateurs et utilisatrices de créer, télécharger et continuer à modifier des images ou des moodboards dans Firefly. Il s’agit de notre premier lancement de l’intégration « Apportez votre propre agent », qui permet aux agents clients et tiers de se connecter à Brand Concierge via Agent Orchestrator.

## Février 2026 {#february-2026}

* **Génération automatisée de jeux de données Eval** : générez automatiquement des jeux de données d’évaluation de haute qualité pour les évaluations fonctionnelles, hors portée et de sauvegarde. Le jeu de données d’évaluation est directement ancré dans la base de connaissances de la marque, ce qui garantit des tests fiables et de haute confiance.

* **Automated Evaluation &amp; LLM-Based Quality Loop** : validez les performances de Concierge en un seul clic à l’aide de la notation basée sur LLM sur plusieurs dimensions de qualité, notamment l’exactitude, l’utilité et l’adhésion à la marque. Cela permet d’effectuer des évaluations de qualité objectives et reproductibles qui donnent confiance aux clients avant chaque lancement.

* **Automatisation des tâches de création et de lancement de Concierge (interface utilisateur développeur)** : il s’agit d’une fonctionnalité interne destinée aux développeurs qui permet aux équipes de s’activer et de lancer rapidement une expérience Concierge, avec des options de gestion des configurations Sandbox et Concierge, de l’interface utilisateur/style et d’optimisation rapide. Cela accélère la mise en production et permet aux équipes de créer des instances de concierge personnalisées et de haute qualité à grande échelle.

* **Amélioration de la Source de connaissances : chargement/actualisation incrémentiel d’URL et prise en charge de types de fichiers supplémentaires** : la fonctionnalité de gestion incrémentielle des URL permet aux clients de mettre à jour (ajouter/supprimer/actualiser) facilement et uniquement les pages qui ont été modifiées, sans retraiter l’ensemble de la source de connaissances. Cela réduit le temps de mise à jour et les frais généraux d’exploitation. En outre, Brand Concierge prend désormais en charge le téléchargement de fichiers PDF/DOCX.

* **Prise en charge des schémas de produit personnalisés** : la fonctionnalité de prise en charge des schémas personnalisés permet aux clients de charger et de gérer des catalogues de produits qui suivent leur propre structure de données plutôt qu’un format fixe. Cela permet une validation appropriée, un mappage des champs et une génération précise des fiches produits entre les marques avec différents modèles de catalogue.

* **Mobile SDK** : Brand Concierge Mobile SDK (pour les applications mobiles) permet aux marques d’intégrer Brand Concierge directement dans leurs applications mobiles, en prenant en charge les interactions de texte, de voix et d’images. Il fournit une interface prête à l’emploi et une intégration back-end afin que les consommateurs puissent facilement accéder à Brand Concierge dans l’application de la marque.
