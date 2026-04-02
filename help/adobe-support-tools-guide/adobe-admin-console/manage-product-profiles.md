---
title: Hantera produktprofiler i Global Admin Console
description: Läs om hur globala administratörer kan lägga till, redigera och ta bort produktprofiler i Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: 527
ht-degree: 0%

---

# Hantera produktprofiler i Global Admin Console

**Gäller för:** Enterprise

Globala administratörer kan lägga till, redigera och ta bort produktprofiler i [Global Admin Console](https://global-admin-console.adobe.com/).

>[!NOTE]
>
>I [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console) väljer du en organisation och navigerar till **[!UICONTROL Products]**. Du kan aktivera alla eller utvalda tjänster för en produkt med hjälp av produktprofiler.

Precis som i Admin Console kan du med produktprofiler finjustera användningen av produkter inom en organisation. Du kan också tilldela administratörer - som kallas **[!UICONTROL Product Profile administrators]** - till produktprofiler. Dessa administratörer kan lägga till slutanvändare i de produktprofiler som de hanterar.

Välj en produkt om du vill hantera produktprofiler. Kontrollerna för att lägga till, redigera och ta bort produktprofiler visas.

>[!NOTE]
>
>För vissa produkter går det inte att skapa eller redigera produktprofiler i Global Admin Console. I så fall använder du [Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) i stället.

## Lägg till en produktprofil

1. I [Global Admin Console](https://global-admin-console.adobe.com/) väljer du en organisation att redigera och går sedan till fliken **[!UICONTROL Products]**.
1. Välj en produkt som du vill lägga till en produktprofil i.
1. Välj **[!UICONTROL Add Profile]**.
1. Ange följande information i dialogrutan **[!UICONTROL Add Profile]**:

   | Fält | Beskrivning |
   |---|---|
   | **[!UICONTROL Name]** | Ett unikt namn för produktprofilen inom organisationen, som skiljer sig från andra produktprofiler och användargrupper. |
   | **[!UICONTROL Quota]** | Det målantal licenser som tilldelats den här profilen. |
   | **[!UICONTROL User Groups]** | Välj i listrutan eller skriv ett användargruppnamn. Om användargruppen inte finns än skapar du den först på fliken [**[!UICONTROL User Groups]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html). |
   | **[!UICONTROL Admins]** | Välj i listrutan eller ange en administratörs e-postadress. Om administratören inte finns än skapar du dem först på fliken [**[!UICONTROL Admins]**](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators). |

   Angiven [!UICONTROL User Groups] tilldelas produktprofilen. De angivna administratörerna blir **[!UICONTROL Product Profile Admins]**, som kan hantera profilen via Adobe Admin Console för den aktuella organisationen.

   ![Lägg till profil](./assets/manage-product-profiles_add-profile.png)

1. Använd växlingsknappen **[!UICONTROL Notifications]** för att aktivera eller inaktivera e-postmeddelanden. När det här alternativet är aktiverat meddelas användare via e-post när de läggs till eller tas bort från profilen.
1. Använd de enskilda **[!UICONTROL Services]**-växlarna för att aktivera eller inaktivera specifika tjänster för produktprofilen. Mer information finns i [Aktivera/inaktivera tjänster för en produktprofil](https://helpx.adobe.com/enterprise/using/enable-disable-services.html).
1. Välj **[!UICONTROL Save]**.
1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Redigera en produktprofil

1. Välj en organisation att redigera, navigera till fliken **[!UICONTROL Products]** och välj en produkt.
1. Välj ikonen **[!UICONTROL More Options]** ![Fler alternativ](./assets/manage-product-profiles_more-options.png) för den aktuella produktprofilen och välj sedan **[!UICONTROL Edit Profile]**.
1. Uppdatera produktprofilinformationen efter behov och välj **[!UICONTROL Save]**.
1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Ta bort en produktprofil

>[!WARNING]
>
> Om du tar bort en produktprofil tas produktåtkomsten bort för alla användare som var medlemmar i den profilen, eller som tillhör användargrupper som är kopplade till den profilen.

1. Välj en organisation att redigera, navigera till fliken **[!UICONTROL Products]** och välj en produkt.
1. Välj ikonen **[!UICONTROL More Options]** ![Fler alternativ](./assets/manage-product-profiles_more-options.png) för den aktuella produktprofilen och välj sedan **[!UICONTROL Delete Profile]**.
1. Välj **[!UICONTROL OK]** i bekräftelsedialogrutan.
1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.


## Relaterad läsning

- [Använd global administration](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)
- [Hantera administratörer](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)
- [Hantera användargrupper](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-user-groups)
- [Tilldela produkter till underordnade organisationer](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/allocate-products)
- [Kör väntande jobb](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [Aktivera/inaktivera tjänster](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Admin Console - översikt](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
