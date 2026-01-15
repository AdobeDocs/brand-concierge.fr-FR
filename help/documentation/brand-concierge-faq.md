---
title: Questions fréquentes
description: Obtenez des réponses aux questions fréquentes sur Adobe Brand Concierge.
role: User,Admin
level: Beginner
source-git-commit: 0f010472e3f49c5d84e9875a33215d56e020bef8
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 1%

---

# Questions fréquentes

Lisez cette section pour obtenir des réponses aux questions fréquentes sur Brand Concierge.

## Général

### En quoi Brand Concierge est-il différent des chatbots ?

Brand Concierge se démarque des chatbots traditionnels en exploitant une IA générative spécifiquement formée au contenu et aux données client de votre entreprise, plutôt que de s&#39;appuyer sur des réponses scriptées ou des résultats web génériques. Cela permet à l’assistant de fournir des réponses personnalisées basées sur le comportement individuel du client, de s’intégrer profondément à vos outils et données Adobe, d’apprendre en permanence de chaque interaction et d’interpréter avec précision l’intention du client au-delà de la simple correspondance de mots-clés.

### Puis-je utiliser Brand Concierge pour le B2C et le B2B ?

Oui. Les cas d’utilisation incluent :

* **B2C :** découverte de produits, assistance d’achat, assistance clientèle, recommandations personnalisées.
* **B2B:** Évaluations guidées, comparaisons de fonctionnalités, planification des réunions, routage des représentants commerciaux, réservation de consultation.

### Quels secteurs d’activité peuvent utiliser Brand Concierge ?

Brand Concierge peut être utilisé dans un large éventail de secteurs, notamment la vente au détail et le commerce électronique, les voyages et l’hôtellerie, les services financiers, les soins de santé (avec contrôles de conformité), les médias et le divertissement, ainsi que la technologie et les logiciels. Pour résumer, tout secteur qui aide les clients à trouver des informations et à prendre des décisions peut tirer parti de la mise en œuvre de Brand Concierge.

## Données et confidentialité

### Les données clients sont-elles protégées ?

Oui. Brand Concierge garantit la sécurité des données client en se conformant au RGPD et au CCPA, en traitant les données sur l’infrastructure sécurisée d’Adobe, en vous permettant de contrôler l’utilisation des données et en protégeant les conversations par le biais du chiffrement et de la journalisation d’audit.

Toutes les conversations ont lieu sur vos propriétés, et non sur des serveurs tiers.

### Quelles sources de données puis-je connecter ?

Vous pouvez connecter les types de sources de données suivants à Brand Concierge :

| Type de Source de données | Sources/Détails disponibles |
|------------------|---------------------------|
| **Produit et contenu** | Catalogues de produits<br>Systèmes d’inventaire<br>Bases de connaissances et documentation<br>Contenu de site web via le chargement d’URL CSV<br>Contenu Adobe Experience Manager<br>Données Adobe Commerce |
| **Données client** | Profils Adobe Experience Platform<br>Données de comportement d’Adobe Analytics<br>Attributs de client propriétaires<br>API tierces (configurées) |
| **Format de fichier CSV** | Une colonne contenant les URL du site Web<br>Brand Concierge analyse les URL et extrait automatiquement le contenu<br>les mises à jour de statut de traitement en temps réel<br>Plusieurs fichiers CSV peuvent être chargés pour différentes zones de contenu |

Toutes les données suivent vos règles de gouvernance.

### Les clients peuvent-ils se désabonner de la personnalisation ?

Oui. Les clients qui se désinscrivent reçoivent des réponses utiles sans personnalisation comportementale. Vous configurez la gestion des désinscriptions pour qu&#39;elle corresponde à vos politiques de confidentialité.

## Configuration et contrôle

### Comment puis-je contrôler la voix de la marque ?

Vous pouvez contrôler la voix de votre marque directement dans l’interface utilisateur en configurant des éléments tels que le ton (du formel au décontracté), la langue (du simple au technique) et la personnalité (par exemple, serviable, enthousiaste ou professionnel). En outre, vous pouvez définir des modèles de réponse à l’aide de modèles et d’exemples, et établir des mécanismes de sécurisation pour appliquer les règles de conformité et les limites. Commencez par les invites de référence d&#39;Adobe et adaptez ces paramètres pour refléter l&#39;identité unique de votre marque.

### Que se passe-t-il lorsque Brand Concierge ne peut pas répondre à une question ?

Vous pouvez configurer des comportements de secours afin de déterminer comment Brand Concierge répond lorsqu’il ne peut pas répondre à une question. Les options comprennent l&#39;affichage d&#39;un message « Je ne peux pas m&#39;en empêcher », la suggestion d&#39;autres questions, l&#39;établissement d&#39;un lien vers des ressources en libre-service ou l&#39;escalade automatique de la demande à un agent humain. Choisissez ce qui convient le mieux à votre marque.

### Puis-je personnaliser le design visuel ?

Oui. Personnalisez tous les éléments visuels, notamment :

* Couleurs et branding
* Polices et typographie
* Styles de bouton
* Positionnement du widget
* Dispositions de cartes
* Formatage de la réponse

Les SDK fournissent des composants par défaut et des options de personnalisation complètes.

### Combien de temps la configuration prend-elle ?

La durée de la configuration peut dépendre de votre type d’implémentation. Une implémentation de base comprenant un catalogue de produits existant, un contenu de FAQ standard et des paramètres par défaut peut prendre entre 3 et 5 jours pour être configurée. D’un autre côté, les implémentations avancées avec des intégrations personnalisées, une personnalisation complète, des workflows complexes et des règles de conformité personnalisées peuvent prendre entre 2 et 4 semaines.

### Comment fonctionnent l’aperçu et le test ?

Brand Concierge comprend des outils de test intégrés :

| Outil de test | Fonctionnalités |
|--------------|----------|
| **Mode de prévisualisation** | Simuler des conversations client<br>ajuster les paramètres en temps réel<br>voir les modifications instantanément<br>partager des liens de prévisualisation avec votre équipe ; |
| **Vue Testeur** | Évaluer les réponses avec les pouces levés/baissés<br>Fournir des commentaires structurés sur 4 catégories<br>Ajouter des commentaires détaillés<br>Suivre les commentaires dans le tableau de bord |

Tous les tests sont effectués avant le déploiement sur les clients.

### Les clients peuvent-ils planifier des réunions avec notre équipe ?

Oui, les clients peuvent planifier des réunions avec votre équipe à l&#39;aide de la compétence Réservation de réunion. Pour activer cette fonctionnalité, activez la compétence dans la configuration des compétences, définissez les intentions d’activation (telles que « parler avec les ventes »), connectez votre calendrier ou votre système de planification, et définissez vos types de disponibilité et de réunion. Une fois la configuration effectuée, les clients peuvent demander des réunions pendant les conversations et Brand Concierge facilite le processus de planification sans qu&#39;ils aient à quitter la conversation.

### Qui gère l’ingénierie rapide ?

Les consultants Adobe gèrent l’ingénierie rapide en arrière-plan :

1. Vous pouvez répondre aux questions relatives à la configuration dans la page Compétences.
1. Fournissez des connaissances sur les produits, les règles métier et évitez les mots-clés.
1. Envoyez vos entrées.
1. Les consultants Adobe utilisent vos réponses pour concevoir des invites optimisées.
1. Les modifications sont répercutées automatiquement dans votre concierge.

Votre concierge peut ainsi utiliser les modèles d’invite d’IA correspondant aux bonnes pratiques tout en conservant les exigences spécifiques de votre marque.

## Performances et analyse

### Comment puis-je mesurer le succès ?

Vous pouvez mesurer le succès à l’aide du tableau de bord Brand Concierge. Utilisez le tableau de bord pour effectuer le suivi de mesures telles que :

| Mesure | Ce qu’il suit |
|--------|----------------|
| **Engagement** | Volume de la conversation, durée de la session |
| **Satisfaction** | Scores de sentiment, évaluations |
| **Conversion** | Taux d’achat pour les utilisateurs assistés et non assistés |
| **Rubriques** | Questions et requêtes les plus courantes |
| **Remise** | Taux d’escalade et raisons |
| **Performances** | Précision de la réponse, temps de résolution |

Vous pouvez également intégrer à Adobe Analytics pour une analyse plus approfondie.

### Que dois-je faire si le sentiment chute ?

Si vous constatez une baisse de sentiment, recherchez les causes sous-jacentes en examinant les requêtes récentes qui ont échoué, en recherchant les lacunes de contenu, en analysant les commentaires négatifs, en testant le ton approprié et en vérifiant les problèmes techniques. Une fois les causes profondes identifiées, il convient de les traiter rapidement et de continuer à surveiller les améliorations possibles.

## Intégration et aspects techniques

### Ai-je besoin d’autres produits Adobe ?

Non, mais ils améliorent les performances :

| Option d’intégration | Fonctionnalités |
|-------------------|--------------|
| **Autonome** | Fonctionne avec votre catalogue de produits et votre contenu. |
| **Avec Adobe Experience Platform** | Profils client unifiés <br>personnalisation avancée<br>cohérence cross-canal |
| **Avec Adobe Commerce** | Inventaire en temps réel<br>historique des commandes<br>intégration au panier |
| **Avec Adobe Experience Manager** | Gestion de contenu<br>Mises à jour dynamiques<br>Prise en charge multi-site |

### Que se passe-t-il si mon site n’est pas sur Adobe ?

Brand Concierge fonctionne avec n’importe quelle plateforme. JavaScript SDK s’intègre à n’importe quel site web et les SDK mobiles fonctionnent avec n’importe quel serveur principal d’application.

### Comment fonctionne la remise de l’agent ?

Lorsque la remise de l’agent est déclenchée, Brand Concierge transmet à l’agent l’historique complet des conversations, le profil et l’ID du client, l’intention identifiée, les détails des produits abordés et toutes les tentatives de résolution. Cela garantit que les agents disposent d’un contexte complet et peuvent poursuivre la conversation en toute simplicité, sans que les clients aient à répéter les informations.

### Puis-je prendre en charge plusieurs langues ?

Oui. Configurez la prise en charge linguistique par assistant en fonction de votre base de clients. Brand Concierge détecte la langue du client et répond en conséquence.
