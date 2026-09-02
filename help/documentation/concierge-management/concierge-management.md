---
title: Gérer un concierge
description: Découvrez comment créer un Brand Concierge à partir d’un site web, configurer ses intégrations, ses compétences, ses instructions, son ton et son style visuel, et le tester avant le déploiement.
toc: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 1%

---


# Gérer un concierge

Un concierge est créé à partir d’un site web de marque et peut être affiné avec des intégrations, des compétences, des instructions, des paramètres de ton et de voix, des styles visuels et des composants de chat. Utilisez l’aperçu pour tester les modifications avant de déployer délibérément le concierge pour les visiteurs.

## Vue d’ensemble

| Élément | Détails |
|---|---|
| utilisateur du Principal | Professionnel du marketing utilisant la configuration en libre-service |
| Support supplémentaire | Les intégrations Commerce et B2B peuvent nécessiter des codes, des clés ou une configuration de la part d’une équipe informatique, commerciale ou commerciale |
| Heure type | Environ 5 minutes pour créer un concierge de base ; du temps continu est nécessaire pour le raffinement et les tests |
| Déploiement | Cette étape est distincte de la création. La création d’un concierge ne le rend pas visible pour les visiteurs et visiteuses du site web |

>[!NOTE]
>
>Un sandbox peut contenir plusieurs convergeurs. Chaque concierge a sa propre configuration, et les concierges peuvent être supprimés de la liste des concierges.

## Créer un concierge

La création d’un service de conciergerie à partir d’une seule URL de site web est le point de départ recommandé pour un nouvel utilisateur. Le système crée une ligne de base de travail sans nécessiter de configuration manuelle.

1. Saisissez l’URL du site web de la marque et sélectionnez **Créer**.

1. Examinez l’expression de marque générée. Le système analyse le ton du site web et propose des attributs tels que la formalité, la chaleur, le jeu et l&#39;énergie. Ajustez les valeurs selon vos besoins et sélectionnez **Continuer**.

1. Examinez le profil de marque généré. Le profil peut inclure l’objectif de la marque, les produits et services, le public cible, les valeurs de la marque, les principaux facteurs de différenciation et les cas d’utilisation courants. Modifiez le profil selon vos besoins et sélectionnez **Continuer**.

1. Consultez les instructions de démarrage, les mécanismes de sécurisation et les suggestions générés. Par exemple, les mécanismes de sécurisation peuvent exclure des sujets juridiques, des sujets relatifs à la conformité ou des discussions avec les concurrents, tandis que les suggestions peuvent fournir des idées rapides de suivi. Modifiez le contenu selon vos besoins et sélectionnez **Enregistrer**.

1. Attendez que le système applique la configuration de base. Le système crée également un style visuel par défaut à l’aide de couleurs et de polices tirées du site web et active des compétences et des intégrations de base, telles qu’une compétence générale de questions-réponses liée au contenu du site web.

1. Testez le concierge dans l’aperçu. Les vues bureau et mobile sont disponibles. Sélectionnez **Nouveau** pour redémarrer une conversation de test.

>[!IMPORTANT]
>
>La création d&#39;un concierge ne le rend pas visible pour les visiteurs. Le déploiement est une étape distincte et délibérée. Vous pouvez réviser la configuration à tout moment avant le déploiement.

## Comprendre ce qui est configuré automatiquement

Les éléments suivants sont configurés automatiquement lorsque vous créez un concierge :

| Élément | Configuration |
|---|---|
| Contenu de la base de connaissances | Construit à partir des pages principales du site par le biais d’une explore d’arrière-plan qui démarre automatiquement |
| Intégration de la recherche dans la base de connaissances | Pointe automatiquement vers le contenu exploré |
| Compétence de conseil sur le site | Actif par défaut afin que le concierge puisse répondre immédiatement aux questions générales |

## Comprendre les compétences et les intégrations

Le compositeur, l’interface utilisée pour créer et configurer un concierge, utilise deux concepts associés :

- **Intégration :** connexion à une source de données, telle qu’un contenu de site web ou un catalogue de produits en ligne. Une intégration récupère des informations, mais ne prend pas de décisions par elle-même.
- **Compétence :** comportement qui détermine ce que fait le concierge, le moment où il le fait et les intégrations qu’il peut utiliser.

Une intégration peut proposer plusieurs compétences, tandis qu’une compétence peut utiliser plusieurs intégrations. Par exemple, une seule connexion au catalogue de produits peut prendre en charge plusieurs cas d’utilisation liés à un produit sans être reconstruite pour chaque compétence.

## Configuration des intégrations

Sélectionnez **Parcourir les intégrations** pour afficher le catalogue d’intégration disponible.

| Intégration | Rôle | Remarques |
|---|---|---|
| Recherche dans la base de connaissances | Recherche le contenu d’un site web | Configuré automatiquement lors de la création du concierge |
| Recherche optimisée par l&#39;IA de contenu | Recherche du contenu AEM Sites | Pertinent pour les clients d’AEM Sites as a Cloud Service |
| Catalogue de produits | Affiche des cartes de produits ou des liens depuis une liste de produits chargée. | Conçu pour des catalogues non commerciaux plus petits |
| COMMERCE MCP | Se connecte à un catalogue Adobe Commerce actif pour rechercher des produits, obtenir des détails sur les produits et des comparaisons | Non activé par défaut ; nécessite des codes ou des clés de l’équipe commerciale ou informatique |
| Réservation de réunion | Permet aux visiteurs de réserver une réunion avec un représentant commercial | Fonctionnalité B2B |
| Conversation en direct | Connecte les visiteurs à un représentant commercial en direct | Fonctionnalité B2B |

### Activer et configurer une intégration

1. Ouvrez la mosaïque Intégration et sélectionnez **Modifier**.

1. Pour **Recherche dans la base de connaissances**, sélectionnez la source de connaissances à rechercher. Vous pouvez renommer la connexion, par exemple `Website content`.

1. Pour **Commerce MCP**, saisissez les valeurs suivantes fournies par l&#39;équipe Adobe Commerce ou IT et connectez-vous :
   - Identifiant de l’environnement
   - Code du site web
   - Code de magasin
   - Code d’affichage du magasin
   - Clé API

1. Sélectionnez **Enregistrer**. L’intégration s’affiche comme connectée et peut être prévisualisée, modifiée ou supprimée.

Vous pouvez ajouter plusieurs instances d’une même intégration, telles que des instances pointant vers différentes sources de connaissances. Une compétence peut être configurée pour utiliser une instance d’intégration spécifique.

### Informations d’intégration qui nécessitent une confirmation

Les détails suivants n’ont pas été établis dans la matière première et doivent être confirmés avant la publication en tant que documentation du produit :

- URL de production complète pour la connexion à `experienceplatform.adobe.com`.
- Indique si un concierge a une limite de nombre d’instances d’intégration.
- La feuille de route et le processus pour les intégrations personnalisées ou personnalisées, qui ont été mentionnés comme prévus, mais non détaillés.

## Configurer les compétences

Les compétences déterminent ce qu&#39;un concierge peut faire pour les visiteurs. Sélectionnez **Parcourir les compétences** pour afficher le catalogue de compétences disponible.

| Compétence | Rôle | Intégration ou configuration requise |
|---|---|---|
| Conseil sur le site | Répond aux questions générales sur la marque, y compris les FAQ, les politiques, les prix, les conseils pratiques et les rubriques d’assistance | Contenu de site web ; actif par défaut |
| Découverte des catalogues Adobe Commerce | Recherche, parcourt, filtre et récupère des détails sur les produits d’un catalogue dynamique | Intégration de Commerce MCP |
| Comparaison des produits Adobe Commerce | Fournit une comparaison côte à côte des produits nommés | Intégration de Commerce MCP |
| Réserver une réunion avec les ventes | Suggère et facilite la réservation d’une réunion | Intégration de la réservation de réunion |
| Conversation en direct avec les ventes | Suggère et facilite une remise en direct par chat | Intégration de la discussion en direct |

### Activer et configurer une compétence

1. Ouvrez la mosaïque Compétence et sélectionnez **Modifier**.

1. Définissez le nom, la description et les intentions de la compétence. Les intentions sont les phrases ou les sujets qui doivent déclencher la compétence, tels que `pricing` ou `compare products`. Vous pouvez ajouter plusieurs modes.

1. Si la compétence nécessite une intégration, joignez l’intégration requise. Par exemple, une compétence en commerce nécessite Commerce MCP. Vous pouvez également sélectionner **Utiliser recommandé** pour permettre au compositeur de sélectionner automatiquement une intégration appropriée.

1. Passez en revue et modifiez les instructions de début de la compétence selon les besoins.

1. Sélectionnez **Enregistrer** et testez la modification dans l’aperçu dynamique.

>[!TIP]
>
>Si deux compétences peuvent répondre à la même question, le routage peut devenir incohérent. Gardez les déclencheurs de compétence distincts et spécifiques au lieu d’utiliser des intentions qui se chevauchent.

### Informations sur les compétences personnalisées qui nécessitent une confirmation

Le document source mentionne une fonctionnalité prévue pour la création de compétences entièrement personnalisées, mais ne fournit pas de feuille de route ni de processus. Confirmez les étapes de disponibilité et de création avant de documenter cette fonctionnalité comme prise en charge.

## Ajout d’instructions au concierge

Utilisez le champ Instructions du concierge pour que les réponses restent conformes aux directives de la marque. Les instructions peuvent définir les éléments suivants :

- Utilisation des marques
- Structure de réponse
- Rubriques à éviter

Saisissez les instructions directement dans le champ de texte. Lorsque vous enregistrez les instructions, le concierge met automatiquement à jour son comportement. Testez immédiatement le résultat dans l’aperçu en direct.

La même zone inclut également le contenu modifiable suivant :

- **Mécanismes de sécurisation :** comportements ou sujets que le concierge doit éviter.
- **Suggestions :** des idées d’invite de suivi qui peuvent être affichées après une réponse.

## Configurer le ton et la voix

Les paramètres de tonalité et de voix contrôlent la longueur de réponse et les attributs de tonalité, notamment :

- Formel ou informel
- Chaud ou neutre
- Joueur ou sérieux

Les sélections sont enregistrées automatiquement. Testez le résultat dans l’aperçu dynamique après avoir apporté des modifications.

## Configurer le style visuel

Les paramètres de style visuel contrôlent l&#39;apparence du concierge, y compris mais sans s&#39;y limiter :

- Couleurs
- Polices
- Texte du message de bienvenue
- Texte de clause de non-responsabilité
- Couleurs de carte

Modifiez les paramètres dans l’interface utilisateur et utilisez l’aperçu en direct pour passer en revue les modifications. Sélectionnez **Enregistrer** pour rendre les modifications permanentes.

>[!NOTE]
>
>Le matériau source indique qu’une apparence entièrement personnalisée est possible au-delà des options disponibles dans l’interface utilisateur, via un script de déploiement distinct. La procédure de script de déploiement n’a pas été incluse et doit être documentée séparément après confirmation.

## Configuration des composants de conversation

Les composants de conversation contrôlent les éléments individuels que les visiteurs voient dans la fenêtre de conversation. Sélectionnez un composant dans l’interface utilisateur pour ouvrir ses paramètres dans un panneau latéral.

| Composant | Ce qu’il contrôle |
|---|---|
| Bulle de conversation | L’aspect des messages du visiteur et des messages du concierge |
| Démarrer l&#39;invite ou les pilules d&#39;invite | Questions d’ouverture suggérées, en particulier celles affichées sur mobile |
| Suggestions de suivi | Propositions de questions suivantes après une réponse |
| Barre de saisie | La boîte de message que les visiteurs et visiteuses utilisent pour saisir une question |
| Citations | Si et comment les références sources apparaissent dans une réponse |
| Commentaires | Contrôle d’évaluation pouces vers le haut ou vers le bas affiché après chaque réponse |
| Fiche produit | La disposition et le style des cartes de produits, y compris les couleurs et les boutons |

## Configuration des fonctionnalités B2B

Réservation de réunion et discussion en direct permettent aux visiteurs de réserver des réunions avec des représentants commerciaux ou de commencer une discussion en direct avec un représentant. Ces fonctionnalités sont optimisées par un produit associé appelé Sales Qualifier.

### Rôles et responsabilités

- **Spécialiste marketing :** configure les compétences et l’intégration dans Brand Concierge.
- **Représentant commercial :** connecte son propre calendrier et configure la disponibilité.

### Configurer la réservation de réunion ou le chat en direct

1. Dans **Parcourir les intégrations**, ouvrez **Réservation de réunion** ou **Discussion en direct**. Par défaut, tous les membres de l’organisation sont disponibles en tant que membres potentiels de l’équipe ; aucune étape distincte n’est nécessaire à ce stade pour ajouter des membres de l’équipe.

1. Demandez à chaque représentant de se connecter à `experienceplatform.adobe.com`, ouvrez **Sales Qualifier** et accédez à **Paramètres du profil**.

1. Demandez à chaque représentant de connecter un calendrier, tel qu&#39;Outlook. Microsoft Teams peut éventuellement être inclus. Le représentant peut également définir l&#39;objet de l&#39;invitation à la réunion et le texte de l&#39;e-mail.

1. Configurez la disponibilité. La disponibilité est extraite du calendrier par défaut et peut être limitée davantage par :
   - Durée de la réunion
   - Durée de la mémoire tampon entre les réunions
   - Préavis minimum requis
   - Fenêtres de temps disponibles spécifiques

1. Configurez la disponibilité du Live Chat séparément, en utilisant un processus similaire.

1. Dans Brand Concierge, ouvrez **Membres gérés** et confirmez que les représentants s&#39;affichent comme disponibles.

1. Activez l’intégration **Réservation de réunion** et/ou **Discussion en direct**.

1. Accédez à **Parcourir les compétences** et sélectionnez **Réserver une réunion avec les ventes** et/ou **Chat en direct avec les ventes**. Définissez les déclencheurs, joignez l’intégration correspondante et enregistrez la compétence.

1. Sélectionnez **Simuler** pour tester l’expérience de bout en bout. Saisissez un exemple de question et confirmez qu’elle mène au flux correct de compétences et d’engagement.

### Comportement après le déploiement

Lorsque les fonctionnalités sont actives :

- Les discussions en direct entrantes s’affichent pour les représentants disponibles en temps réel.
- Les réunions réservées s&#39;affichent dans une vue de réunions.
- Un rapport sur les performances des réunions est disponible dans Analytics.
- Les réunions et conversations sont envoyées à Marketo sous forme d’activités, avec les données d’activité existantes.

### Informations B2B qui nécessitent une confirmation

Les matières premières identifient les éléments suivants comme non résolus :

- Le chat en direct ne dispose pas de son propre tableau de bord d’analyse ; cela a été décrit comme une lacune de produit en cours plutôt que comme une lacune de documentation.
- Chemin de connexion `experienceplatform.adobe.com` exact pour Sales Qualifier.
- Si Meeting Booking et Live Chat nécessitent des licences ou des droits distincts.

## Partage d’un lien d’aperçu

Un lien d’aperçu partageable permet aux parties prenantes de consulter un concierge et d’interagir avec lui sans accès du compositeur et sans déployer le concierge sur un site web actif.

1. Dans l’écran d’aperçu du concierge, générez un lien d’aperçu partageable.

1. Partager le lien avec les réviseurs.

1. Les réviseurs peuvent interagir avec le concierge via le lien sans se connecter au compositeur.

### Informations sur le lien de prévisualisation qui nécessitent une confirmation.

Confirmez les détails suivants avant de publier cette procédure en tant que workflow de produit complet :

- Emplacement et libellé exacts de l’action de partage dans l’interface utilisateur.
- Indique si les liens d’aperçu expirent ou peuvent être révoqués.
- Indique si l’utilisation du lien de prévisualisation est suivie séparément des analyses en direct.

## Test avant déploiement

Utilisez l’aperçu ou l’expérience de simulation après chaque modification de configuration significative. Vérifiez au minimum les éléments suivants :

- Le concierge répond à des questions générales à partir du contenu du site web prévu.
- Chaque compétence ne répond qu’à ses déclencheurs prévus.
- Les intégrations requises sont connectées et pointent vers la source de données appropriée.
- Les recherches et comparaisons de produits utilisent le MCP Commerce ou l’instance de catalogue de produits prévue.
- Réservation de réunion et conversation en direct vers les représentants prévus.
- Le ton, la voix, les instructions, les mécanismes de sécurisation et les suggestions produisent les réponses attendues.
- Les styles visuels et les composants de conversation s’affichent correctement dans les vues bureau et mobile.
- Les parties prenantes peuvent examiner l’expérience par le biais du lien d’aperçu partageable, le cas échéant.
