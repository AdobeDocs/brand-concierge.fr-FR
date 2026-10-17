---
title: Exporter des conversations à l’aide de Query Service et du terminal
description: Découvrez comment exporter des conversations Brand Concierge au format CSV à l’aide d’Experience Platform Query Service et de Terminal Server, avec des conseils sur les informations d’identification et les données personnelles.
topic: Development
role: Developer
level: Experienced
doc-type: Tutorial
duration: 260
last-substantial-update: 2026-10-15
jira: KT-22874
source-git-commit: 04c844e16a8fb13e54dfcbb29c776896674532b9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%
---
# Exporter des conversations à l’aide de Query Service et du terminal

Découvrez comment enregistrer et exporter des conversations Adobe Brand Concierge à l’aide de Adobe Experience Platform Query Service et de Terminal Server. Cette vidéo montre comment trouver les noms des tables de jeux de données, configurer le client de ligne de commande PostgreSQL et exporter les données de conversation pour une période dans un fichier CSV.

## À qui s&#39;adresse cette vidéo ?

* Développeurs qui doivent exporter des données de conversation Brand Concierge à l’aide d’outils de ligne de commande

## Contenu vidéo

* Rechercher des jeux de données de conversation dans Experience Platform et copier leurs noms de table
* Installez le client PostgreSQL avec Homebrew et configurez son chemin de ligne de commande
* Copiez la commande de connexion PSQL depuis l’onglet Informations d’identification de Query Service
* Sélectionnez un jeu de données et une période, puis exportez les résultats de la requête vers un fichier CSV local
* Vérifiez les résultats exportés et actualisez les informations d’identification expirées si nécessaire.

>[!VIDEO](https://video.tv.adobe.com/v/3504645?captions=fre_fr)

```bash
psql "sslmode=require host=... password=..." --csv -o ~/brand-concierge-conversation-export/oct-1-2026-till-today-responses.csv -c "SELECT * FROM cja_brand_concierge_responses_dataset_b4c15126_bd9b_4d52_8151_26 WHERE timestamp >= TIMESTAMP '2026-10-01 00:00:00' AND timestamp <= NOW() ORDER BY timestamp ASC LIMIT 1000"
```

>[!IMPORTANT]
>
> La commande de connexion PSQL contient un mot de passe actif. Ne le partagez pas et ne le collez pas dans des conversations, des agents d’IA ou des e-mails. Si l’authentification échoue après l’expiration du mot de passe, copiez une nouvelle commande à partir de l’onglet Informations d’identification de Query Service .

>[!NOTE]
>
> Les conversations exportées peuvent contenir des informations d’identification personnelle (PII). Respectez la politique de gestion des données de votre entreprise lors du stockage de fichiers CSV.

Pour consulter la documentation, voir l’aide de [&#128279;](../documentation/overview.md).

## Tutoriels connexes

* [Exporter des conversations à l’aide d’Adobe CX Enterprise Coworker](exporting-conversations-using-adobe-cx-enterprise-coworker.md)
