---
title: Évaluer un concierge
description: Découvrez comment créer des jeux d’évaluation et exécuter des évaluations fonctionnelles, hors champ d’application et de protection pour évaluer l’exactitude et la sécurité des réponses d’un concierge.
hide: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---


# Évaluer un concierge

**À qui cela s’adresse** professionnels du marketing qui utilisent l’expérience en libre-service. Aucune assistance informatique n’est requise.

**Temps requis :** quelques minutes pour créer un jeu d’évaluation. L’exécution d’une évaluation prend plus de temps en fonction de la taille de la visionneuse.

Les évaluations vous aident à vous assurer que les réponses d&#39;un concierge sont exactes avant que le concierge ne soit examiné par quelqu&#39;un en dehors de votre équipe immédiate. Contrairement aux tests ad hoc dans l’expérience de prévisualisation, les évaluations offrent un moyen répétable de mesurer les réponses par rapport aux réponses attendues.

## Types d’évaluation

Les évaluations se répartissent en trois catégories :

| Type | Rôle |
|---|---|
| Fonctionnel | Vérifie les réponses aux questions normales et pertinentes sur vos produits ou services. |
| Hors de portée | Vérifie la manière dont le concierge traite les questions auxquelles il ne doit pas répondre mais qui ne sont pas préjudiciables, telles que les questions sur un concurrent ou un sujet sans rapport. |
| Sauvegarde | Vérifie la façon dont le concierge gère les informations préjudiciables ou contradictoires, y compris les questions pièges, les obscénités et les tentatives de manipulation. |

## Création d’un jeu d’évaluation

Un jeu d’évaluation, également appelé *jeu de données doré* ou *vérité au sol*, est une liste d’exemples de questions associés aux réponses considérées comme correctes. Les réponses réelles du concierge sont comparées à ces réponses attendues au cours d&#39;une évaluation.

### Création d’un jeu d’évaluation

1. Nommez le jeu d’évaluation. Par exemple : `About my products`.

1. Choisissez le mode de création de la visionneuse :

   * **généré par l’IA :** le compositeur lit la source de connaissances et rédige une liste de questions probables et de réponses attendues pour révision.
   * **Chargement manuel ou feuille de calcul :** fournissez directement une liste de questions et de réponses.

1. Si vous créez une visionneuse générée par l’IA, assurez-vous que la source de connaissances est entièrement configurée avant de générer la visionneuse. Le compositeur utilise la source de connaissances pour rédiger les questions et les réponses.

1. Examinez chaque paire question-réponse générée :

   * Modifiez une réponse pour ajuster son expression.
   * Supprimez une question qui n’est pas pertinente.

1. Vous pouvez éventuellement télécharger la visionneuse sous forme de feuille de calcul pour qu’elle soit examinée par un collègue. Après révision, chargez à nouveau la feuille de calcul.

>[!TIP]
>
>Les jeux d’évaluation générés par l’IA sont des brouillons basés sur la source de connaissances. Examinez-les et corrigez-les de la même manière que vous examinez le profil et les instructions de la marque lors de la création du concierge.

## Exécuter une évaluation

1. Sélectionnez **Exécuter une évaluation**.

1. Sélectionnez le jeu d’évaluation à exécuter, puis sélectionnez **Exécuter**.

1. Attendez que le concierge se fasse poser toutes les questions. Les réponses réelles du concierge sont comparées aux réponses attendues.

   Le temps de traitement augmente avec le nombre de questions dans l’ensemble. La progression s’affiche sous la forme d’un pourcentage.

1. Une fois le traitement terminé, passez en revue le score global et le nombre de réponses marquées.

Les réponses marquées sont des réponses potentiellement problématiques qui peuvent nécessiter un examen supplémentaire.

## Consulter les résultats de l’évaluation

**Résultats de l’évaluation** affiche chaque exécution précédente d’un jeu d’évaluation, de sorte que vous puissiez effectuer le suivi des résultats au fil du temps.

Pour passer en revue une exécution :

1. Ouvrez une exécution d’évaluation à partir de **Résultats de l’évaluation**.

1. Passez en revue chaque question avec la réponse réelle du concierge et la réponse attendue.

1. Examinez l’évaluation attribuée à chaque résultat. Les résultats reçoivent une note **élevée**, **moyenne** ou **faible** et incluent une note expliquant le raisonnement. Par exemple, un résultat peut être marqué **nécessite votre attention** avec une raison pour l’évaluation.

1. Examinez directement les réponses marquées pour vous concentrer sur les résultats potentiellement problématiques sans lire chaque résultat de l’exécution.

## Bonnes pratiques

* Configurez entièrement la source de connaissances avant de générer un jeu d’évaluation basé sur l’IA. Un contenu source plus complet génère de meilleures questions de brouillon.
* Créez au moins un petit jeu d’évaluation pour chaque type d’évaluation : fonctionnel, hors de portée et de sauvegarde. Chaque type correspond à une catégorie d’émission différente.
* Réexécutez les évaluations après toute modification de configuration significative, y compris les modifications apportées aux instructions, aux mécanismes de sécurisation, aux compétences ou aux intégrations. Traiter les évaluations comme une pratique continue plutôt qu&#39;un point de contrôle ponctuel.
* Ajoutez des questions réelles aux visiteurs d’Analytics à un jeu d’évaluation lorsqu’elles révèlent une lacune méritant d’être testée.
