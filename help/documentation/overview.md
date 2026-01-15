---
title: Documentation du produit
description: Découvrez comment configurer et utiliser les principales fonctionnalités de Brand Concierge.
role: User,Admin
level: Beginner
source-git-commit: 2c3f3d009d8fef3eaf5bf32d73672eeda7ba05c8
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 1%

---

# Aide de Brand Concierge

Découvrez comment configurer et utiliser les principales fonctionnalités de Brand Concierge. Trouvez des réponses aux questions courantes sur la configuration, l’intégration des données, la confidentialité, la personnalisation, la mesure des performances et les exigences techniques.

## Principales fonctionnalités {#key-features}

Brand Concierge dispose de plusieurs fonctionnalités essentielles, notamment :

* **Intégration guidée :** suivez une configuration détaillée pour les connaissances, les compétences et l’expression de la marque.
* **Intégration des connaissances :** chargez et gérez des sources telles que des fichiers CSV avec des liens vers des sites web.
* **Configurer les compétences** Intégrer des compétences telles que les conseils sur les produits.
* **Contrôler l’image de marque :** ajustez la voix, le ton et la longueur de réponse pour répondre aux normes et à l’approche de votre marque.
* **Prévisualisation et itération :** utilisez une interface de prévisualisation complète pour simuler des conversations et effectuer des réglages en direct.
* **Système de retour d’informations :** utilisez un système de retour d’informations qui permet aux utilisateurs de fournir des notes favorables ou défavorables, ainsi que des formulaires de retour d’informations détaillés couvrant la couverture de la réponse, le ton, la qualité et les fonctionnalités.
* **Tableau de bord Analytics :** tirez parti d’un tableau de bord Analytics optimisé par Customer Journey Analytics pour les mesures telles que les conversations, les sentiments et l’engagement.

## Commencer {#getting-started}

Vous pouvez accéder à Brand Concierge à partir du tableau de bord Adobe Experience Cloud. À un niveau élevé, vous effectuez les tâches suivantes dans la présentation de la page d’accueil :

1. [Créer un concierge](#homepage)
1. [Ajouter des sources de connaissances](#knowledge-sources)
1. [Configurer les compétences](#skills-configuration)
1. [Spécifiez votre expression de marque](#brand-expression).

Pour un tutoriel vidéo, voir [Créer votre premier concierge](../getting-started/create-first-concierge.md)

Les sections suivantes décrivent en détail chaque tâche et les options de l’interface.

## Créer un concierge {#homepage}

La page d’accueil de Brand Concierge est conçue pour être facile à utiliser et efficace. Elle vous guide tout au long des étapes de configuration essentielles, avec une présentation dédiée aux nouveaux utilisateurs et utilisatrices. Une bannière supérieure bien en vue décrit les principales actions, comme préciser le nom et l&#39;objectif de votre concierge, ajouter des sources de connaissances, configurer des compétences pertinentes et définir l&#39;expression de votre marque.

Au fur et à mesure que vous avancez, un suivi visuel affiche clairement les composants de configuration terminés et met en évidence les tâches restantes. Pour soutenir davantage vos efforts, la page d’accueil comporte une section inspirante avec des vidéos et des démonstrations des fonctionnalités de conciergerie, telles que des recommandations de produits. Vous pouvez également accéder rapidement à la documentation d’Experience League pour obtenir des informations techniques plus détaillées.

Une fois la configuration terminée, un résumé de la configuration fournit une vue complète de vos détails, organisés avec des onglets pour faciliter les ajustements et les ajustements continus.

**Éléments clés**

* **Première présentation à l’utilisateur** : bannière supérieure contenant les étapes de configuration de votre concierge (nom/objectif, sources de connaissances, compétences, expression de la marque).
* **Suivi de progression** : indicateurs visuels des composants d’installation terminés ou en attente.
* **Section inspirante** : vidéos et démonstrations présentant les fonctionnalités du concierge (par exemple, les recommandations de produits).
* **Liens de documentation** : accès rapide aux ressources Experience League pour obtenir des informations plus détaillées sur les technologies.
* **Résumé de la configuration** : vue de tous les détails après la configuration, avec des onglets pour l’affinement.

**Pour créer un concierge**

1. Accédez à la bannière de présentation , puis cliquez sur **[!UICONTROL Commencer]**.
1. Attribuez un nom à votre concierge et définissez son objectif (par exemple, _Recommander des produits personnalisés_).
1. Suivez les étapes guidées pour continuer.
1. Une fois la configuration terminée, revenez à la page d’accueil pour surveiller ou modifier votre concierge.

>[!TIP]
>
>Brand Concierge enregistre automatiquement votre progression. Une configuration incomplète peut limiter les fonctionnalités, mais ne bloquera aucune tentative de prévisualisation.

### Sources de connaissances {#knowledge-sources}

[!UICONTROL Sources de connaissances] vous aide à gérer les sources de données qui alimentent les réponses de votre concierge. Vous pouvez accéder aux [!UICONTROL sources de connaissances] après avoir chargé vos fichiers initiaux. [!UICONTROL Sources de connaissances] comporte un certain nombre d’éléments clés à prendre en compte, notamment :

* **Liste Source :** affiche tous les éléments chargés, tels que les fichiers CSV contenant des liens vers des sites Web, et indique s&#39;ils sont traités ou en attente.
* **Interface de chargement :** vous permet de faire un glisser-déposer ou de rechercher des fichiers CSV contenant des URL que le système analysera pour extraire des connaissances.
* **Options de connexion :** permet de lier des sources de connaissances spécifiques à des compétences pertinentes pour une utilisation plus ciblée.

**Pour ajouter une source de connaissances**

1. Sur la page d’accueil, cliquez sur **[!UICONTROL Sources de connaissances]**.

1. Nommez la source de connaissances.

1. Cliquez sur **[!UICONTROL Ajouter]** pour charger un fichier CSV.

   Assurez-vous qu’il comprend une colonne pour les URL du site web.

1. Patientez quelques instants pour le traitement.

   Cette étape se résout assez rapidement à mesure que les statuts sont mis à jour en temps réel.

1. Une fois l’ajout effectué, revenez à la page d’accueil.

   À ce stade, vous devriez voir la nouvelle source ajoutée à la page d’accueil.

   Utilisez la page d’accueil pour modifier ou supprimer vos sources de connaissances selon vos besoins. Vous pouvez également reconnecter une source de connaissances si des modifications se produisent.

### Configurer les compétences {#skills-configuration}

Utilisez l’interface [!UICONTROL Configuration des compétences] pour définir l’expertise de votre concierge en configurant des compétences telles que **Product Advisory**. Répondez au questionnaire pour fournir des informations que les consultants Adobe utiliseront ultérieurement pour une ingénierie rapide. La configuration des compétences comporte un certain nombre d’éléments clés à prendre en compte, tels que :

* **Sélecteur de compétences :** vous pouvez choisir parmi les compétences disponibles, telles que les Conseils sur le produit pour formuler des recommandations de produit.
* **Questionnaire :** vous devez remplir une série d’invites pour fournir des connaissances sur le produit, les règles métier, les mots-clés à éviter et les connexions source.
* **Aperçu :** vous avez la possibilité d’effectuer des ajustements en direct et de voir comment vos ajustements affectent les réponses, avec des liens vers la page d’aperçu.
* **Activer la réservation de réunion :** vous pouvez permettre aux visiteurs de planifier des réunions directement avec des représentants d’entreprise.

**Pour configurer des compétences**

1. Accédez au suivi de la progression dans la page d’accueil, puis cliquez sur **[!UICONTROL Configurer les compétences]**.
1. Sélectionnez une compétence (par exemple, Conseils sur les produits).
1. Répondez aux questions de configuration qui suivent.

   Voici quelques exemples de questions : _Que doit savoir le concierge au sujet des produits ?_, _quelles règles d’entreprise faut-il suivre ?_, _quels mots-clés doivent être évités ?_

1. Connecter les [sources de connaissances](#knowledge-sources) pertinentes.
1. Activer les fonctionnalités supplémentaires (réservation de réunion).
1. Envoyer pour traitement.

### Expression de la marque {#brand-expression}

Vous pouvez utiliser l’interface _[!UICONTROL Expression de marque]_ pour personnaliser la personnalité et le style des réponses de votre concierge. Vous pouvez accéder à Brand Expression à partir des étapes de configuration ou via la barre latérale de prévisualisation pour les modifications en cours.

Avec Brand Expression, vous pouvez utiliser des curseurs pour personnaliser les paramètres de voix et de tonalité de votre concierge. Vous pouvez choisir parmi des options telles que « Amical », « Professionnel » et « Énergétique ». De plus, vous pouvez configurer les longueurs de réponse selon vos besoins. Vous pouvez configurer votre concierge pour qu&#39;il renvoie des sorties courtes, moyennes ou longues, selon la vision de votre marque.

**Pour personnaliser l’expression de votre marque**

1. Sur la page d’accueil, cliquez sur **[!UICONTROL Personnaliser l’expression de marque]**.
2. Ensuite, configurez la voix, le ton et la longueur de réponse préférée de votre marque.
3. Sélectionnez **[!UICONTROL Enregistrer]** pour vous assurer que les modifications sont répercutées dans les réponses futures.

### Prévisualisation et test {#preview-and-test}

Testez votre concierge avant de vous lancer pour les clients qui utilisent les modes Aperçu et Tester la vue .

>[!BEGINTABS]

>[!TAB Mode de prévisualisation]

Utilisez le mode Prévisualisation pour simuler des conversations tout en effectuant des réglages en temps réel.

1. Après la configuration, revenez à la page d’accueil et cliquez sur **[!UICONTROL Aperçu]**.
1. Utilisez l&#39;interface de chat pour saisir votre requête (par exemple, _Recommander un ordinateur portable de moins de 1000 $_).
1. Vérifiez les réponses du concierge.
1. Utilisez le panneau de droite pour ajuster les paramètres d’expression de votre marque.
1. Cliquez sur **[!UICONTROL Partager]** pour générer un lien pour les commentaires de l’équipe.

>[!TAB Vue Tester]

Utilisez la vue Testeur pour recueillir des commentaires structurés sur les performances du concierge et simuler l’expérience de l’utilisateur final.

1. Dans l’aperçu, cliquez sur **[!UICONTROL Mode Testeur]**.
1. Utilisez la vue Testeur pour simuler les conversations de l’utilisateur final.
1. Utilisez le mécanisme de pouces vers le haut et vers le bas pour évaluer chaque réponse que vous recevez.
1. Remplissez le formulaire de commentaires pour les pouces vers le bas :
   **Couverture de la réponse :** a-t-elle répondu à l’intention ?
   **Ton de la marque :** Aligné avec la personnalité ?
   **Qualité de la réponse :** clair et structuré ?
   **Fonctionnalités de réponse :** suivis utiles ?
1. Ajouter des commentaires et des observations spécifiques.
1. Envoyez vos commentaires pour révision du tableau de bord.

>[!ENDTABS]

### Commentaires {#feedback}

Une fois le test terminé, vous pouvez utiliser l’onglet Commentaires sur la page d’accueil pour fournir des commentaires et des révisions détaillées.

La section des commentaires propose plusieurs fonctionnalités importantes pour vous aider à surveiller et à évaluer les performances de Brand Concierge. Les éléments disponibles sont les suivants :

* **Capture instantanée des performances :** affiche des cartes résumant les mesures clés, y compris le nombre total de conversations, les utilisateurs uniques, les tendances de sentiment et le taux d’engagement.
* **Bouton Afficher le rapport :** permet d’ouvrir un tableau de bord optimisé par Customer Journey Analytics pour un accès en profondeur aux analyses avancées et aux mesures de performances.
* **Liste de commentaires :** présente un tableau des sessions de commentaires. Vous pouvez cliquer sur des lignes individuelles pour afficher le relevé de notes complet de la conversation pour chaque session.
* **Panneau Commentaires :** affiche les cartes de performance sur le côté droit de l’interface. Pointez ou cliquez sur ces cartes pour mettre en surbrillance les parties pertinentes du relevé de notes de conversation afin d’en faciliter la consultation.

**Pour envoyer des commentaires**

1. Accédez à la page d’accueil de Brand Concierge et sélectionnez **[!UICONTROL Commentaires]**.
1. Utilisez l’instantané fourni pour afficher des informations sur les tendances de haut niveau.
1. Pour accéder à une exploration approfondie optimisée par Customer Journey Analytics, sélectionnez **[!UICONTROL Afficher le rapport]**.
1. Vous pouvez également examiner le panneau pour obtenir d’autres commentaires connectés.
1. Lorsque vous avez terminé, vous pouvez exporter les informations pour les utiliser ultérieurement et affiner votre workflow.

### Configurations {#configurations}

L’onglet _[!UICONTROL Configurations]_ est une vue récapitulative en lecture seule que vous pouvez utiliser pour consulter la configuration complète de votre concierge. Cela reflète directement la page d’accueil une fois la configuration initiale terminée et fournit des résumés de vos détails, de vos sources de connaissances, de vos compétences et de votre expression de marque configurée. Vous pouvez utiliser cette fonctionnalité comme référence avant de prévisualiser ou de partager votre concierge.

## Utilisation de Brand Concierge

Découvrez les fonctionnalités du client, les capacités de l’entreprise et les cas d’utilisation de Brand Concierge.

### Fonctionnalités du client

Brand Concierge offre une interface de conversation qui permet aux clients de rechercher des produits, de comparer des options et d’obtenir des réponses en utilisant le langage naturel. Grâce aux recommandations personnalisées, aux comparaisons riches des produits et à la possibilité de passer à un agent en direct, les clients bénéficient d’une expérience transparente et intuitive. Les interactions sont flexibles : les clients peuvent utiliser du texte, de la voix ou des images. En outre, chaque réponse est basée sur la documentation fiable de votre marque et sur le contexte client.

* Posez vos questions en langage naturel et obtenez des recommandations personnalisées.
* Comparez les produits côte à côte avec les affichages visuels.
* Obtenez des réponses provenant de la documentation de votre marque.
* Basculez vers un agent en direct avec un historique de conversations complet.

### Fonctionnalités commerciales

Brand Concierge dote les entreprises de fonctionnalités d’IA conversationnelle avancées pour l’engagement des clients. Il aide les marques à stimuler la conversion en guidant les clients vers les bons produits, réduit les coûts de support grâce à des réponses instantanées et précises et assure une voix et une conformité cohérentes de la marque. Grâce à des analyses fiables, une transmission transparente de l’IA à l’utilisateur et des intégrations Adobe profondes, Brand Concierge optimise l’expérience client et les performances commerciales.

* Guidez les clients vers les bons produits pour augmenter la conversion.
* Réduisez les coûts d’assistance grâce à des réponses instantanées et précises.
* Contrôlez les exigences en matière de voix, de ton et de conformité de la marque.
* Suivez les performances avec le tableau de bord Customer Journey Analytics.
* Activer la transmission transparente de l’IA à l’utilisateur, y compris la planification des réunions.
* Intégrez-la à Adobe Experience Platform et Experience Manager.

## Cas d’utilisation

Brand Concierge prend en charge les cas d’utilisation B2C et B2B dans plusieurs secteurs d’activité.

| Secteur industriel | Cas d’utilisation |
|---|---|
| Commerce de détail et e-commerce | Les clients peuvent découvrir des produits et recevoir des recommandations personnalisées. Brand Concierge fournit des conseils sur le dimensionnement et l’ajustement, aide les utilisateurs à trouver les cadeaux adaptés et associe les styles ou les préférences en fonction des entrées du client. |
| Ventes B2B | Brand Concierge guide les clients à travers les évaluations de produits, offre des comparaisons détaillées de fonctionnalités et de prix, aide à la planification de réunions de vente et fournit des recommandations spécifiques au secteur adaptées aux clients professionnels. |
| Service clientèle | Les utilisateurs peuvent recevoir des réponses instantanées provenant directement de la base de connaissances. Brand Concierge fournit des informations sur les politiques et les procédures, aide à résoudre les problèmes et fournit des mises à jour sur le statut et le suivi des commandes. |
| Voyage et hébergement | Les clients reçoivent des recommandations de destination personnalisées, une assistance pour la planification des itinéraires, une assistance tout au long du processus de réservation et des réponses aux questions de politique de voyage. |
| Services financiers | Brand Concierge propose des comparaisons de produits pour aider les clients à choisir les bonnes solutions financières, fournit des informations sur les comptes, fournit des conseils en matière de conformité et permet de planifier les réunions avec des conseillers financiers. |

