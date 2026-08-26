---
title: Présentation de Brand Concierge
description: Découvrez Brand Concierge, comment ses principaux composants s’intègrent et le glossaire des termes clés que vous rencontrerez dans l’interface du compositeur.
source-git-commit: 3da67605a43e949046260651253bbe0f2f0215fc
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 1%

---

# Présentation de Brand Concierge

Brand Concierge est une plateforme agentique qui permet aux entreprises et aux marques de lancer des expériences de conversation personnalisées sur leurs surfaces orientées client : sites web, applications mobiles et autres propriétés numériques. Chaque conversation est basée sur le contenu et les mécanismes de sécurisation de la marque. Les intégrations permettent aux informations de ces conversations de se propager dans le reste de l’écosystème de la marque, tel que Marketo Engage.

## Composants principaux

Un déploiement Brand Concierge comporte deux éléments principaux :

| Pièce | Signification |
|---|---|
| **Expérience visiteur** | Surface face à la marque, telle qu’un site web ou une application mobile, où les visiteurs interagissent avec le concierge et obtiennent des réponses en temps réel. |
| **Compositeur** | Interface utilisateur utilisée pour concevoir des expériences de concierge et gérer les concierges, les intégrations, les configurations, les évaluations, le déploiement et les analyses. |

## Modules de compositeur abordés dans ce guide

Dans Composer, les principaux modules (et leur emplacement dans ce guide) sont les suivants :

- Gestion des utilisateurs (section 3)
- Création et gestion des sources de connaissances, partagées entre les concierges (Section 4)
- Gestion du concierge : intégrations, compétences, instructions du concierge, tonalité et voix, style visuel et composants de chat (section 5)
- Évaluation (Section 6)
- Déploiement (Section 7)
- Liste de contrôle d’activation (section 8)
- Analytics (Section 9)

## Comment les pièces se connectent

Une source de connaissances (contenu) est interrogée par une intégration (connexion), appelée par une compétence (comportement), le tout encapsulé dans un concierge (expérience globale) avec lequel les visiteurs interagissent.

## Glossaire

Ces termes apparaissent dans l’interface du compositeur.

| Terme | Définition |
|---|---|
| **Concierge** | L’expérience de chat dans l’IA elle-même : une par marque, site web ou cas d’utilisation. Un compte peut en avoir plusieurs. |
| **Compositeur** | L’interface utilisée pour créer et gérer des concierges, distincts de ce que voient les visiteurs et visiteuses du site Web. |
| **Source de connaissances** | Contenu qu’un concierge est autorisé à utiliser pour répondre à des questions, telles que des pages de site web ou une liste de produits. Sans cela, le concierge n&#39;a rien à répondre. |
| **Intégration** | Connexion à un système pouvant récupérer des informations, telles que du contenu de site web ou un catalogue de produits en direct. |
| **Compétences** | Une fonctionnalité spécifique que le concierge peut effectuer, comme répondre à des questions générales, comparer des produits ou réserver une réunion. Une compétence utilise une ou plusieurs intégrations pour remplir sa fonction. |
| **Mécanismes de sécurisation** | Règles définissant ce que le concierge ne doit pas faire ou discuter, comme les concurrents ou les conseils juridiques. |
| **Évaluation** | Test structuré composé d’exemples de questions associés aux réponses attendues, utilisé pour évaluer les performances du concierge. |
| **Identifiant du flux de données** | Identifiant technique spécifiant l’endroit où les données d’activité des visiteurs sont envoyées dans les systèmes Adobe. Il est fourni par l’équipe informatique ou d’analyse. |
| **Sandbox** | Espace de travail isolé au sein d’une organisation. Une organisation peut en avoir plusieurs ; chacune peut accueillir plusieurs concierges. |
| **Organisation IMS** | Terme Adobe désignant le compte global d’une organisation. |
| **MCP** (par exemple, MCP Commerce) | Connecteur géré par Adobe vers un système spécifique, tel qu’un catalogue de produits en ligne, configuré à l’aide de codes ou de clés fournis par l’équipe informatique ou l’équipe commerciale. |
| **CJA (Customer Journey Analytics)** | produit Adobe analytics. Brand Concierge met automatiquement en service ici un tableau de bord de démarrage sans configuration supplémentaire requise. |

>[!NOTE]
>
>Les marketeurs peuvent généralement ignorer la section 3, *Gestion des utilisateurs et des accès*, entièrement (un informaticien la termine une fois) et commencer la section 4, *Sources de connaissances*. Revenez à la section 3 uniquement lors de la configuration de nouveaux coéquipiers.
