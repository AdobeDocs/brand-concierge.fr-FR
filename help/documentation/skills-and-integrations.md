---
title: Cadre de compétences et d’intégration
description: Découvrez comment les compétences et les intégrations fonctionnent ensemble dans le cadre de la conciergerie. Les compétences définissent le comportement, tandis que les intégrations se connectent aux données et fournissent les fonctionnalités.
role: User, Admin
level: Beginner
source-git-commit: 16136f0d5470a39cbf260f4b1eadc6918d0212b4
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# Cadre de compétences et d’intégration {#skills-and-integrations}

Une intégration (anciennement appelée outil) est une connexion à une source de données ou à un serveur principal. Une compétence est un comportement.

Une intégration peut être utilisée par de nombreuses compétences. Une compétence peut utiliser plusieurs intégrations. Vous pouvez les configurer indépendamment et les mapper.

## Compétences

Une compétence est la couche de comportement d&#39;un concierge. Il s’agit d’une unité nommée et réutilisable qui définit un seul travail que le concierge peut effectuer : ce qu’il gère, quand il intervient et comment il répond. Une compétence ne contient pas de données qui lui soient propres ; elle emprunte des capacités aux intégrations qui lui sont associées.

Chaque compétence est composée de cinq parties :

| Partie | Signification |
| --- | --- |
| Nom | Identifiant de la compétence |
| Description | À quoi sert la compétence, son objectif en termes simples |
| Utiliser lorsque | Condition de déclenchement. C&#39;est le signal de routage qui indique au concierge quand invoquer cette compétence plutôt qu&#39;une autre |
| Intégrations | Les outils spécifiques que cette compétence est autorisée à appeler pour faire son travail. Une compétence ne peut utiliser que ce qui est joint ici |
| Fichier d&#39;instructions | Instructions détaillées régissant le comportement de la compétence et la manière dont elle interprète une requête, formate sa réponse et applique ses mécanismes de sécurisation |

Comportement d’une compétence au moment de l’exécution : lorsqu’un message utilisateur arrive, la plateforme le compare au déclencheur « Utiliser quand » de chaque compétence active et achemine le message vers la compétence correspondante. Cette compétence exécute ensuite ses instructions et appelle uniquement les intégrations qui lui sont associées. Ses instructions sont composées dans le comportement d&#39;exécution global du concierge avec le profil de marque et toute autre compétence active.

Une compétence décide de ce qu’il faut faire et quand. Il ne se connecte lui-même à aucune donnée ; c’est le rôle de l’intégration.

_Exemple de compétence en conseil sur le site_

![Panneau des détails de compétence des conseils sur le site présentant sa description, Utilisation lors des déclencheurs, intégration de la recherche dans la base de connaissances jointe et instructions sur les compétences](assets/skills-and-integrations-1.png){width="800" zoomable="yes"}

## Intégrations

Une intégration est la couche de capacité d’un concierge. Il s’agit d’une connexion à un système externe ou principal (une base de connaissances, une source de contenu, un catalogue de commerce en direct) qui récupère réellement des données ou effectue une action. Lorsqu&#39;une compétence est un jugement, une intégration est une capacité.

Chaque intégration présente les caractéristiques suivantes :

| Caractéristique | Signification |
| --- | --- |
| Connexion et informations d’identification | Une intégration s’authentifie sur son serveur principal à l’aide de sa propre configuration, par exemple un identifiant d’environnement de commerce et une clé API. Cette configuration permet de la diriger vers la bonne source de données |
| Fonctionnalités exposées | Une intégration rend disponible une ou plusieurs fonctionnalités appelables, les actions individuelles qu’une compétence peut appeler. Commerce MCP, par exemple, présente la recherche de produits, les détails de produits, les variantes et la découverte de facettes comme des fonctionnalités distinctes |
| Réutilisable | Une seule intégration peut être associée à de nombreuses compétences, et la même intégration sert de nombreux concierges et clients. Cette réutilisation est l’efficacité fondamentale du framework |

Comportement d’une intégration au moment de l’exécution : lorsqu’une compétence se déclenche et décide qu’elle a besoin de données, elle appelle l’un des outils de l’intégration. L’intégration exécute les qui s’appliquent au serveur principal actif et renvoie des données structurées à la compétence, que la compétence utilise ensuite pour former sa réponse.

Une intégration fournit une capacité, mais n&#39;exerce aucun jugement. Il attend d’être appelé par une compétence, effectue la tâche spécifique qui lui est demandée et renvoie le résultat.

### Capacités et limites (limite du libre-service)

- **Libre-service, aucune ingénierie :** modifiez les instructions, modifiez les déclencheurs « utiliser quand », joignez ou déconnectez les intégrations existantes, activez ou désactivez une compétence et connectez une intégration prise en charge (comme Commerce MCP avec des informations d’identification valides).

- **Pas en libre-service, nécessite une ingénierie :** créez un tout nouvel outil ou connecteur qui n’existe pas encore dans le catalogue, ajoutez une nouvelle catégorie de mécanisme de sécurisation que le framework ne prend pas en charge, ou modifiez les données exposées par un serveur principal.

- **Le chevauchement des déclencheurs entre deux compétences est un risque de configuration :** si deux compétences peuvent vraisemblablement se déclencher sur le même message, le routage peut être incohérent. Écrivez des déclencheurs pour éviter toute ambiguïté réelle plutôt que de compter sur le routeur pour la résoudre.

## Intégrations prêtes à l’emploi

Vous trouverez ci-dessous les quatre intégrations présentées dans le panneau **Parcourir les intégrations** de Composer.

| Intégration | Ce qu&#39;il fait | Remarques |
| --- | --- | --- |
| Recherche dans la base de connaissances | Source pour les informations sur les produits, le prix, les fonctionnalités et la documentation d’une marque, renseigné via l’explore du site | Celui-ci est créé automatiquement lors de la création du concierge, renseigné par l’explore du site |
| Recherche optimisée par l&#39;IA de contenu | Recherche le contenu de la marque via l’IA dédiée au contenu | Autre source de contenu. En règle générale, une seule source parmi la recherche dans la base de connaissances ou la Recherche optimisée par l&#39;IA de contenu est nécessaire à la fois |
| Mappage Liaison d’entité/Catalogue de produits | Résout les produits ou les mentions de marque dans le message d’un utilisateur sur des entités de catalogue spécifiques | Prise en charge de l’intégration, utilisée avec une intégration de recherche plutôt que seule |
| COMMERCE MCP | Serveur MCP Commerce géré par Adobe : recherche de produits, détails, variantes et découverte de facettes/attributs, soutenue par la recherche Adobe Live | Pas dans la ligne de base ; ajouté manuellement pour les cas d’utilisation de Commerce |

![Parcourir le panneau des intégrations présentant quatre cartes d’intégration : Recherche optimisée par l&#39;IA de contenu, liaison d’entité, recherche dans la base de connaissances et MCP Commerce](assets/skills-and-integrations-2.png){width="800" zoomable="yes"}

## Compétences prêtes à l’emploi

Quatre compétences sont proposées dans le catalogue. Chacune d’elles répertorie ses intégrations recommandées.

| Compétence | À quoi cela sert-il ? | Intégrations recommandées |
| --- | --- | --- |
| Conseil sur le site | Questions générales sur la marque : politiques, FAQ, programmes, procédures et assistance | Recherche dans la base de connaissances, Recherche optimisée par l&#39;IA de contenu et liaison d’entités |
| Conseil sur le produit | Découvrir et rechercher des produits : fiches produits nommées et questions sur les produits en prose | Recherche dans la base de connaissances, mappage liaison d’entités/catalogue |
| Découverte des catalogues Adobe Commerce | Rechercher, parcourir, filtrer et obtenir des détails complets sur les produits d’un catalogue dynamique | Outils de MCP Commerce : recherche dans les produits Commerce, détails du produit, variantes de produit, facettes de produit et attributs consultables |
| Comparaison des produits Adobe Commerce | Comparaison côte à côte de plusieurs produits nommés dans un tableau pour Commerce | Outils de MCP Commerce : recherche dans les produits Commerce, détails du produit |

Les deux compétences commerciales sont des fonctionnalités de catalogue uniquement et dépendent de l’intégration de Commerce MCP, qui ne fait pas partie de la base. Dans un service de conciergerie hors commerce, les services de conseil sur le site et de conseil sur les produits s’exécutent sur la recherche dans la base de connaissances créée automatiquement à la place.

![Parcourez le panneau des compétences présentant quatre cartes de compétences : conseil sur les produits, découverte du catalogue Adobe Commerce, comparaison des produits Adobe Commerce et conseil sur le site](assets/skills-and-integrations-3.png){width="800" zoomable="yes"}

## Ce qui est câblé à la création du concierge

Lorsqu&#39;un concierge est créé via une configuration en un clic, la ligne de base est assemblée pour vous.

| Câblé à la création | Détail |
| --- | --- |
| Base de connaissances (données) | L’explore préliminaire crée une base de connaissances à partir des 10 à 15 premières pages du site, disponibles via le plan du site. Il s’agit du magasin de contenu, et non d’une compétence ou d’une intégration |
| Recherche dans la base de connaissances (intégration) | Intégration intégrée, connectée à la base de connaissances explorée et utilisée pour effectuer des recherches. Ce n&#39;est pas l&#39;explore qui crée cela; elle pointe vers ce que l&#39;explore a produit |
| Conseil sur le site (compétences) | Actif dans la base de données, câblé pour appeler la recherche de la base de connaissances, qui interroge la base de connaissances explorée |

## Questions fréquentes

**Quelle est la différence entre une compétence et une intégration ?**

Une intégration est une connexion à une source de données ou à un serveur principal ; il s’agit de ce que le concierge peut contacter, comme une base de connaissances ou un catalogue commercial en direct. Une compétence est un comportement : elle décide de ce que fait le concierge, du moment où il le fait et des intégrations qu’il est autorisé à utiliser.

**Règle de base :** une intégration est une capacité ; une compétence correspond au jugement sur le moment et la manière d’utiliser cette capacité.

**La même intégration peut-elle être utilisée par plusieurs compétences ?**

Oui, et c&#39;est intentionnel. Les outils de Commerce MCP sont partagés à la fois dans la découverte de catalogues et la comparaison de produits. La création d’une intégration une fois et sa réutilisation sur de nombreuses compétences et de nombreux clients sont les éléments clés de l’efficacité du framework 2.0. C’est ce qui supprime la version personnalisée par client.

**Un praticien peut-il ajouter une fonctionnalité entièrement nouvelle sans ingénierie ?**

Uniquement si une intégration existe déjà pour lui dans le catalogue. Un praticien peut librement mapper, configurer et indiquer toute intégration existante, c’est-à-dire en libre-service. Cependant, si cette fonctionnalité nécessite un serveur principal ou un connecteur qui n’existe pas encore (une nouvelle API ou un nouveau type de source de données), il s’agit d’une tâche d’ingénierie consistant à créer d’abord l’intégration. Une fois qu’il existe dans le catalogue, le configurer devient à nouveau en libre-service.

**En quoi cela diffère-t-il de l’invite système unique de BC 1.0 ?**

Dans la version 1.0, le comportement était dicté par une grande invite système (le manifeste), difficile à modifier en toute sécurité et qui nécessitait généralement des modifications techniques. Dans la version 2.0, le manifeste existe toujours, mais il est composé de pièces modulaires plutôt que d&#39;être écrit en un seul bloc. C’est ce qui rend le comportement configurable par un praticien et rend les mécanismes de sécurisation et les instructions individuelles lisibles et contrôlables au lieu d’être enfouis dans une seule invite.

**Que crée exactement l’explore anticipée ?**

L’explore permet de créer une base de connaissances, un magasin consultable du contenu du site, à partir des 10 à 15 premières pages trouvées via le plan du site. Il s’agit uniquement de la couche de données. L’explore ne crée pas de compétence ni d’intégration ; elle produit le contenu sur lequel elles agissent ultérieurement.

**Si l&#39;explore crée la base de connaissances, qu&#39;est-ce que l&#39;intégration Recherche de la base de connaissances ?**

La recherche dans la base de connaissances est une intégration intégrée dont la tâche consiste à rechercher cette base de connaissances. La base de connaissances est constituée des données ; la recherche dans la base de connaissances est la fonctionnalité qui les interroge. Ce sont deux choses distinctes : l’une est le contenu, l’autre est l’outil qui lit le contenu. C&#39;est une erreur courante de les traiter de la même façon; ce n&#39;est pas le cas.

**Comment le concierge répond-il à une question générale à la création, de bout en bout ?**

Trois calques fonctionnent en séquence et ils correspondent exactement au modèle de compétence, d’intégration et de données :

- L’explore anticipée crée la base de connaissances à partir des pages (données) du site.
- L’intégration de recherche de la base de connaissances intégrée effectue une recherche dans cette base de connaissances (intégration ).
- La compétence Conseil sur le site est connectée pour appeler Recherche dans la base de connaissances (comportement).
