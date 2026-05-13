---
title: Questions fréquentes
description: Obtenez des réponses aux questions fréquentes sur Adobe Brand Concierge.
role: User,Admin
level: Beginner
TQID: https://experienceleague.adobe.com/R-s7wgJ5jtCXnBiLMVdW-6db7cTgSgaJwq4x6IlEJqY
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: be0b12f950b911baf48596f7b145fcaa2c6880cf
workflow-type: tm+mt
source-wordcount: 1537
ht-degree: 1%

---

# Questions fréquentes

Lisez cette section pour obtenir des réponses aux questions fréquentes sur Brand Concierge.

## Général

### Pourquoi utiliser Brand Concierge ? Quel problème cela résout-il ?

D’autres recherches sont effectuées sur des outils d’IA externes (par exemple, ChatGPT, Gemini) plutôt que sur des sites web de marque. Les visiteurs veulent de plus en plus « aller au but », par exemple, « Parlez-moi de X », « Puis-je faire Y ? » Brand Concierge vous aide à maintenir cette conversation sur votre site : lorsque les visiteurs arrivent sur vos pages (y compris depuis un assistant d’IA), ils peuvent poursuivre la conversation avec un assistant formé à votre contenu. Vous offrez une expérience cohérente sur la marque au lieu de les perdre dans des réponses génériques ailleurs.

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
| **Format de fichier CSV** | Une colonne contenant les URL du site Web<br>Brand Concierge explore les URL et extrait automatiquement le contenu. <br>Les mises à jour de statut de traitement en temps réel<br>Plusieurs fichiers CSV peuvent être chargés pour différentes zones de contenu |

Toutes les données suivent vos règles de gouvernance.

### Les clients peuvent-ils se désabonner de la personnalisation ?

Oui. Les clients qui se désinscrivent reçoivent des réponses utiles sans personnalisation comportementale. Vous configurez la gestion des désinscriptions pour qu&#39;elle corresponde à vos politiques de confidentialité.

### Y a-t-il des implications en matière de consentement ou de confidentialité ?

Oui. **Données de conversation :** si la conversation comprend des informations personnelles ou identifiables, la collecte, le stockage et l’utilisation doivent respecter votre consentement et votre politique de confidentialité (par exemple, le RGPD et le CCPA). **Analytics :** lorsque le Concierge envoie des événements à Experience Platform ou à Analytics, ces événements peuvent être soumis à votre consentement et à votre gouvernance actuels (par exemple, chaînes de consentement, libellés d’utilisation des données). Nous vous recommandons de traiter Concierge comme toute autre expérience digitale propriétaire : de vous assurer que la bannière de consentement et les préférences de votre site couvrent les données et analyses de conversation et de chat, et d’aligner les données d’événement sur votre stratégie de consentement. Faites vérifier la conformité et la conformité avant la mise en production.

## Profils et personnalisation

### Concierge utilise-t-il les profils client (par exemple, Real-Time CDP) pour personnaliser les réponses ? Que se passe-t-il si le visiteur est à mi-chemin d’un parcours ?

Dans sa portée actuelle, Concierge se concentre sur les visiteurs anonymes : il répond à partir de la conversation et de votre base de connaissances (site web et catalogue), et non d’une recherche en direct d’identité ou de l’état du parcours dans Real-Time CDP. Les fonctionnalités de la feuille de route comprennent la formation de prospects, le transfert aux ventes et le reciblage, qui s’aligneront davantage sur les profils connus et le contexte du parcours. Adaptation des réponses en fonction de l’option « ce visiteur a-t-il un profil ? » ou « où sont-ils dans un parcours ? » est une amélioration future. Pour l’instant, l’expérience est cohérente pour les visiteurs anonymes.

## Déploiement et calendrier

### Combien de temps faut-il généralement pour mettre en ligne ?

Grâce à un travail parallèle et à une collaboration active, de nombreuses implémentations sont mises en service en 6 à 9 semaines environ. L’évaluation peut commencer rapidement une fois que vos entrées (URL, catalogue, directives de la marque) sont prêtes. Après la configuration de l’accord et de la production, vous passez à l’optimisation de la qualité et au déploiement contrôlé (par exemple, 5 %, puis mise à l’échelle à 100 % sur une semaine environ).

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

## Expression et ton de la marque

### Si je définit « ludique et enthousiaste » dans l’expression de la marque, l’IA va-t-elle en faire trop ?

Ça peut. Certains clients ont signalé que l’IA a tendance à surcharger l’enthousiasme lorsqu’elle est définie sur « ludique et enthousiaste », par exemple, des points d’exclamation doubles ou des superlatifs forts. Pour les publics réglementés ou médicaux (par exemple, les pharmaciens, la nutrition en début de vie), nous recommandons de diminuer l&#39;enthousiasme et le jeu tout en gardant le ton conversationnel et décontracté. Utilisez des paramètres modérés et ajustez en fonction des commentaires ; pour les secteurs réglementés, privilégiez la « conversation » à l’enthousiasme.

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

### Que dois-je faire si le sentiment tombe ?

Si vous constatez une baisse du sentiment, recherchez les causes sous-jacentes en examinant les requêtes récentes qui ont échoué, en recherchant les lacunes dans le contenu, en analysant les commentaires négatifs, en testant le ton approprié et en vérifiant les problèmes techniques. Une fois les causes profondes identifiées, il convient de les traiter rapidement et de continuer à surveiller les améliorations possibles.

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
