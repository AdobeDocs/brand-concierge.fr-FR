---
title: Activer le chat en direct et la réservation de réunion
description: Connectez les intégrations Live Chat et Réservation de réunion dans le compositeur, puis activez la compétence Remise aux ventes afin que votre concierge sache quand proposer un humain.
role: User, Admin
level: Beginner
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 4751ce408fb2aa6d1affae4dd7a5d81ca43ffc8a
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 1%
---
# Activer le chat en direct et la réservation de réunion {#configure-in-composer}

Deux éléments doivent être en place dans le compositeur. Les intégrations **[!UICONTROL Réservation de réunion]** et **[!UICONTROL Chat en direct]** donnent au concierge la *possibilité* de vérifier la disponibilité, de lancer une conversation et de réserver une place. La compétence **[!UICONTROL Remise aux ventes]** lui indique *quand* utiliser cette capacité.

>[!NOTE]
>
>Terminez [d’abord configurer des représentants dans Adobe Marketo Qualifier](representative-setup.md). Les intégrations vérifient les calendriers connectés et la disponibilité du chat en direct, et ne s’activeront pas sans eux.

## Connecter l&#39;intégration Réservation de réunion {#connect-meeting-booking}

1. Dans le compositeur, ouvrez votre concierge et sélectionnez **[!UICONTROL Intégrations]** > **[!UICONTROL Parcourir les intégrations]**.

   **[!UICONTROL Réservation de réunion]** et **[!UICONTROL Discussion en direct]** apparaissent sous **[!UICONTROL Intégrations intégrées]**.

   ![Parcourez le panneau des intégrations dans le compositeur affichant les cartes Chat en direct et Réservation de réunion sous Intégrations intégrées](../assets/sales-handoff-composer-1.png){width="800" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Réservation de réunion]**, puis sélectionnez **[!UICONTROL Configurer]**.

1. Saisissez un nom et une description.

   Nommez l’intégration pour ce qu’elle fait dans ce service de conciergerie, par exemple `Meeting booking - US region` ou `Meeting booking - round robin`. Vous pouvez connecter plusieurs éléments. Le nom est donc la manière de les différencier ultérieurement.

1. Vérifiez le statut de la connexion au calendrier.

   L’intégration vérifie qu’au moins un représentant de votre organisation a connecté un calendrier.

   * Si aucun n&#39;a de date, une erreur vous indique de connecter au moins un calendrier avant d&#39;activer la réservation de réunion. Revenez à [!DNL Adobe Marketo Qualifier] et terminez [Connecter votre calendrier](representative-setup.md#connect).
   * Si au moins l’un d’eux l’a fait, une confirmation indique que des représentants sont disponibles.

1. Sélectionnez un type de routage : **[!UICONTROL Routage circulaire]**, **[!UICONTROL Agent direct]** ou **[!UICONTROL Routage personnalisé]**.

   Si vous sélectionnez **[!UICONTROL Agent direct]**, choisissez le représentant qui reçoit chaque réunion réservée par ce concierge. Si vous sélectionnez **[!UICONTROL Routage personnalisé]**, les règles de routage que vous avez créées [!DNL Adobe Marketo Qualifier] sont appliquées. Pour connaître le comportement de chacun, voir [Acheminer les conversations vers les représentants](routing-rules.md).

1. Sélectionnez **[!UICONTROL Connexion]**.

## Connecter l’intégration de la discussion en direct {#connect-live-chat}

1. Dans **[!UICONTROL Parcourir les intégrations]**, sélectionnez **[!UICONTROL Discussion en direct]**, puis sélectionnez **[!UICONTROL Configurer]**.

1. Saisissez un nom et une description, par exemple `Live chat - round robin`.

1. Vérifiez le statut de disponibilité du chat en direct.

   L’intégration vérifie qu’au moins un représentant a défini la disponibilité du chat en direct.

   * Si aucun ne l&#39;a fait, un message vous indique d&#39;ajouter des représentants qui ont configuré leur disponibilité de chat en direct. Revenez à [!DNL Adobe Marketo Qualifier] et terminez [Définir la disponibilité du chat en direct](representative-setup.md#chat-availability).
   * Si au moins l’un d’eux l’a fait, une confirmation indique que des représentants sont disponibles.

1. Sélectionnez un type de routage.

   Le chat en direct prend en charge les trois mêmes types de routage que la réservation de réunion. Avec **[!UICONTROL Round-robin]**, chaque représentant éligible est averti immédiatement et le premier à accepter prend le chat.

1. Sélectionnez **[!UICONTROL Connexion]**.

## Activer la remise des compétences aux ventes {#activate-skill}

Les intégrations sont maintenant connectées, mais le concierge doit encore savoir quand les proposer. C&#39;est le travail de la compétence.

1. Dans le compositeur, sélectionnez **[!UICONTROL Compétences]** > **[!UICONTROL Parcourir les compétences]**, puis sélectionnez **[!UICONTROL Remise aux ventes]**.

   Le panneau des détails affiche la description de la compétence, ses conditions **[!UICONTROL Utiliser quand]**, les **[!UICONTROL intégrations]** recommandées et les instructions **[!UICONTROL Compétence]**.

   ![Parcourez le panneau des compétences avec la compétence Remise aux ventes sélectionnée, affichant Utiliser lorsque les conditions, les intégrations recommandées et les instructions de compétence](../assets/sales-handoff-composer-2.png){width="800" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Modifier]**.

   ![Remise à la compétence commerciale en mode de modification avec le nom, la description et l’utilisation de la compétence modifiable dans des conditions](../assets/sales-handoff-composer-3.png){width="800" zoomable="yes"}

1. Passez en revue le nom et la description de la compétence, puis modifiez-les si vous le souhaitez.

1. Examinez les conditions **[!UICONTROL Utiliser quand]**.

   Ce sont les intentions qui déclenchent un transfert. La compétence est fournie avec un ensemble par défaut :

   | Condition | Déclencheurs sur |
   | --- | --- |
   | Accès aux consultants | Réservation ou planification d’une réunion, démarrage d’un chat en direct ou demande à contacter un représentant d’entreprise |
   | Ventes et achats | Prix, devis, remises, assistance à l’achat ou licences d’entreprise |
   | Comparaison avec la concurrence | Comparaison de vos solutions avec celles d&#39;autres concurrents, différenciation ou migration depuis une plateforme concurrente |
   | Accès à la version d’évaluation et à la preuve de concept | Configurations d’essai, accès au terrain de jeu, preuves de concept ou pilotes |
   | Modifications de contrat et de licence | Renouvellements de contrat, prolongations de contrat ou mises à niveau de plan |
   | Appel d&#39;offres ou demande d&#39;information d&#39;approvisionnement | Envois, réponses, questionnaires fournisseur, formulaires d&#39;approvisionnement ou documentation sur la conformité |
   | Démonstrations | Démonstrations ou explications de produit |

   Sélectionnez **[!UICONTROL Ajouter une condition]** pour ajouter votre propre intention, ou supprimez toute condition qui ne s’applique pas à votre entreprise.

1. Ajoutez les intégrations connectées.

   Ajoutez **[!UICONTROL Discussion en direct]**, **[!UICONTROL Réservation de réunion]** ou les deux, selon ce que vous souhaitez que ce concierge offre.

1. Consultez les **[!UICONTROL instructions relatives aux compétences]**.

   Les instructions sont générées à partir des conditions et intégrations que vous avez sélectionnées. Par conséquent, aucune modification n’est nécessaire dans la plupart des cas.

   Modifiez-les en langage clair lorsque vous souhaitez mieux contrôler quelle intention mène à quelle option. Par exemple, vous pouvez demander au concierge d’offrir un chat en direct pour les questions de tarification, d’offrir une réunion pour les demandes de démonstration et d’offrir les deux pour les questions d’approvisionnement.

1. Sélectionnez **[!UICONTROL Enregistrer]**.

## Test et publication {#test-and-publish}

Ouvrez l’aperçu et demandez au concierge quelque chose qui correspond à l’une des conditions **[!UICONTROL Utiliser quand]**, telles que la demande d’une démonstration. Le concierge doit vous proposer de vous mettre en relation avec un spécialiste, de montrer l&#39;option de chat, l&#39;option de réunion, ou les deux, et de présenter une réelle disponibilité.

Lorsque le comportement est correct, publiez votre concierge pour que la remise soit activée sur votre site.

## Étape suivante {#next}

Vos représentants peuvent maintenant recevoir des chats. Voir [Boîte de réception de conversation](chat-inbox.md).
