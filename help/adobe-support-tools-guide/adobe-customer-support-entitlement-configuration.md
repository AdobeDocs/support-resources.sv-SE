---
title: Konfiguration av Adobe kundsupportberättigande
description: Hur Adobe-kunder kan lägga upp och hantera supportärenden i Admin Console så att man får tillgång till supportresurser, skicka in ärenden och hantera ärendeaktiviteten.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 7f7a394874014fb5333ed9fb39f84b7137562726
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Konfiguration av Adobe kundsupportberättigande

Om du vill konfigurera supportberättiganden för din organisation måste du först lägga till eller bjuda in användaren via Admin Console.

## Lägga till behörighetsroller för support i en organisation

Rollen **[!UICONTROL Support administrator]** är en icke-administrativ roll som har åtkomst till supportrelaterad information. En **[!UICONTROL Support administrator]** kan visa, skapa och hantera problemrapporter.

Så här lägger du till eller bjuder in en administratör:

1. I Admin Console väljer du **[!UICONTROL Users]** > **[!UICONTROL Administrators]**.
1. Klicka på **[!UICONTROL Add Admin]**.
1. Ange namn eller e-postadress.

   Du kan söka efter befintliga användare eller lägga till en ny användare genom att ange en giltig e-postadress och fylla i informationen på skärmen.

   ![Lägg till administratör](assets/admin-console-add-admin.png)

1. Klicka på **[!UICONTROL Next]**. En lista med administratörsroller visas.

Så här tilldelar du en **[!UICONTROL Support administrator]**-roll till en användare (aktivera en användare som kan kontakta support):

1. Välj alternativet **[!UICONTROL Support administrator]**.

   ![Redigera administratörsrättigheter](assets/edit-admin-rights.png)

1. Välj något av följande två alternativ:

   * Alternativ 1: **[!UICONTROL Basic support administrator]**. Välj det här alternativet om du vill ge användarsupporten åtkomst till alla lösningar (förutom Marketo Engage).
   * Alternativ 2: **[!UICONTROL Product support administrator]**: Välj det här alternativet för Marketo Engage support. Välj vilka Marketo Engage-instanser som ska ge användarsupporten åtkomst.

   ![Redigera administratörsrättigheter för Marketo](assets/edit-admin-rights-advanced.png)

1. När du har gjort markeringarna klickar du på **[!UICONTROL Save]**.

Användaren får en e-postinbjudan om de nya administratörsbehörigheterna från `message@adobe.com`.

Användarna måste klicka på **[!UICONTROL Get started]** i e-postmeddelandet för att gå med i organisationen. Om nya administratörer inte använder länken **[!UICONTROL Get started]** i e-postinbjudan kan de inte logga in på Admin Console.

Som en del av inloggningsprocessen kan användare uppmanas att konfigurera en Adobe-profil om de inte redan har en. Om användare har flera profiler associerade med sin e-postadress måste användarna välja **[!UICONTROL Join Team]** (om de uppmanas till det) och sedan välja den profil som är associerad med den nya organisationen.

![Bekräftelse av administratörsrättigheter](assets/admin-rights-confirmation.png)

Mer information finns i [Redigera Enterprise-administratörsroll](admin-roles.md#edit-enterprise-admin-role) -instruktionerna i dokumentationen för administrativa roller. Observera att endast en systemadministratör för din organisation kan tilldela den här rollen. Mer information om administrativ hierarki finns i dokumentationen för [administrativa roller](admin-roles.md).
