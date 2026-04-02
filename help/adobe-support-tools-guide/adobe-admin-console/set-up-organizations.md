---
title: Hantera organisationshierarki
description: Läs om hur globala administratörer kan hantera organisationens hierarki i Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1479'
ht-degree: 0%

---

# Hantera organisationshierarki

Gäller företag.

Läs om hur globala administratörer kan hantera organisationens hierarki i Global Admin Console.

När du har fått [åtkomst till  [!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console) kan du skapa nya organisationer, lägga till befintliga organisationer i hierarkin, ta bort organisationer och ändra en överordnad organisation. Gå hit för att [logga in på Global Admin Console](https://global-admin-console.adobe.com/)

En organisation är en struktur som används för att hantera Adobe produkter och användare. Med [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) kan administratörer hantera distribution och konfiguration av produkter och användare i organisationen. Med [[!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration) kan globala administratörer skapa, hantera och ta bort flera organ.

## Skapa en underordnad organisation

Som [global administratör](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators) kan du skapa underordnade organisationer för alla organisationer i hierarkin och ange namn, land, användargrupper, produkter, produktprofiler, administratörer och profiler.

När en ny underordnad organisation skapas ärvs följande automatiskt från den överordnade omedelbart:

- Organisationens [principinställningar](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) (inklusive lås om sådana finns).
- Listan över systemadministratörer (styrs av **[!UICONTROL Inherit System Admins on creation]** [policy](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).
Följande kan förhindra att systemadministratörer ärvs:
   - [Domänförtroende](https://helpx.adobe.com/enterprise/using/directory-trust.html) saknas.
   - Begränsningar för användartyp (lägg till användarprofiler för Adobe ID/Enterprise ID/Federated ID). Läs mer om [principinformation](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Åtkomst till [[!DNL Federated ID]] eller [[!DNL Enterprise ID]] användare från domäner som den överordnade organisationen har åtkomst till. Detta gör domänanvändarna i den överordnade organisationen tillgängliga i den underordnade organisationen. Arv av användaråtkomst styrs av **Ärv användare från kataloger som hanteras av den överordnade organisationen** [policy](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Delningsprincip, lösenordsprincip och säkerhetskontakter (kontrolleras av **Ärv delningsinställningar när en underordnad organisation skapas** [policy](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/). På fliken **[!UICONTROL Organizations]** väljer du den organisation du vill lägga till en underordnad organisation i.
2. Välj ikonen **[!UICONTROL Add+]**.
   ![Lägg till organisation](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Ange ett **namn** och **land** för organisationen.\
   Organisationens enkla namn måste innehålla mellan 4 och 100 tecken. Sökvägen får innehålla högst 255 tecken.
   ![Lägg till underordnad organisation](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. Välj **[!UICONTROL Save]**.
5. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Ta bort en underordnad organisation

Som [global administratör](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators) kan du ta bort underordnade organisationer. Borttagningsåtgärden kan inte ångras och rotorganisationen kan inte tas bort. Resurserna som tilldelats den borttagna organisationen returneras till den överordnade organisationen. Innan en organisation tas bort blir dess överordnade automatiskt överordnad någon av dess underordnade organisationer.

En organisation kan bara tas bort om följande villkor uppfylls:

- Det finns inga Sign-konton, Adobe Stock-köp eller lagringsdatabaser i organisationen.
- Det finns inga domäner som tagits i anspråk i organisationen.
- Det finns inga instansierade produkter i organisationen.
- Det finns inga Experience Cloud-produkter som kan innehålla instansieringar i organisationen.

>[!WARNING]
>
>Om du tar bort en organisation påverkas användarna. Se till att det inte finns någon åtkomst eller information som går förlorad när en organisation tas bort.

1. Logga in på [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/). Gå till fliken **[!UICONTROL Organizations]** och markera den organisation du vill ta bort.
1. Välj ikonen **[!UICONTROL Delete]**.
   ![Ta bort organisation](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. Välj **[!UICONTROL Delete Organization]** i dialogrutan **[!UICONTROL OK]**.
1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Byta namn på en organisation

Organisationsnamnet är det officiella namnet på ditt företag eller din institution som anges vid köpet. Användarna ser det här namnet när de väljer en profil under inloggningen, särskilt om de har tillgång till Adobe-produkter från flera organisationer eller behöver välja mellan en företagsprofil och en personlig profil.

Som [global administratör](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators) kan du redigera namnet på en överordnad eller underordnad organisation för att hjälpa användare att identifiera rätt profil när de loggar in på [[!DNL Creative Cloud]] produkter och tjänster.

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/). På fliken **[!UICONTROL Organizations]** väljer du den organisation som du vill byta namn på.
1. Välj ikonen **[!UICONTROL Edit]**.
   ![Byt namn på organisation](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Uppdatera organisationens namn och välj **[!UICONTROL Save]**.

>[!TIP]
>
>Använd ett tydligt och identifierbart organisationsnamn på upp till 255 tecken för att hjälpa användarna att välja rätt profil. Undvik att använda specialtecken och överväg att ta med region, avdelning eller berättigande. Undvik också ovanliga akronymer och otydliga eller liknande namn i hela organisationshierarkin.

Ändringar loggas i granskningsloggen, alla användare meddelas via e-post och namnet kan inte uppdateras igen på 24 timmar. [Lär dig hur du visar och hämtar granskningsloggar](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports).

## Ändra överordnad för en organisation

Som [!DNL Global Administrator](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators) kan du reparera en organisation i organisationshierarkin med knappen **[!UICONTROL Change hierarchy]**.

Om du ändrar överordnad för en organisation påverkas följande:

- Om du representerar en organisation flyttas hela underträdet som är rotat i den överordnade organisationen med det. Sökvägarna för den reparerade organisationen och dess underordnade uppdateras för att återspegla deras nya plats.
- Organisationens [principer](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) för flyttade organisationer uppdateras så att alla lås på profiler hålls av en organisation i den nya hierarkin.
- Om du ändrar en organisations position i hierarkin kan organisationens globala administratörer ändras. Globala administrationsroller ärvs nedåt i hierarkin så att globala administratörer för den nya överordnade organisationen automatiskt blir globala administratörer för den flyttade organisationen. På samma sätt kan globala administratörer förlora sin roll i den flyttade organisationen om de har den rollen genom att vara en global administratör för den gamla överordnade. De ärvda globala administrationsrollerna visas inte i organisationens administratörspanel.
- Omorienteringen påverkar även de tillgängliga produkterna i de flyttade organisationerna. När det är möjligt uppdateras [produktallokeringar](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) så att de kommer via den nya överordnade platsen.
- Om produktallokeringar inte kan uppdateras för att komma från det nya överordnade objektet tas produkterna bort tillsammans med produktprofilerna för dessa produkter. Användare kan förlora åtkomsten som ett resultat av den här åtgärden. För att produkten ska vara tillgänglig på den nya platsen måste produkten vara tillgänglig för den närmaste överordnade för den gamla och nya platsen.

>[!WARNING]
>
>Om produkter tas bort som ett resultat av reparationer förlorar användarna åtkomsten till dessa produkter.

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/). På fliken **[!UICONTROL Organizations]** väljer du **[!UICONTROL Change hierarchy]** för att aktivera reparering av organisationerna.
2. Välj **[!UICONTROL OK]** på popup-skärmen som visas.
3. Om du vill förbereda drar du den underordnade organisationen till önskad organisation.
4. Välj **[!UICONTROL Save]** när du är klar med att kommentera dina organisationer.
5. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

När jobbet är klart kan du navigera till Produktallokering och [ändra bidragsvärdena](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) för att återspegla ändringen i allokeringen av produktresurser.

## Lägg till befintliga organisationer med Organisationsmapparen

Som [global administratör](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators) kan du lägga till befintliga organisationer som för närvarande inte ingår i din Global Admin Console-hierarki i organisationshierarkin.

Du kan också lägga till teamorganisationer i organisationshierarkin. Teamorganisationer deltar inte i produktallokering eller sammanslagning av produktanvändning, och hanteringen av teamorganisationer i Global Admin Console är begränsad. Du kan lägga till dem i organisationshierarkin för att hålla reda på dem och se vilka produkter de köper. Teamorganisationer kan inte ha underordnade organisationer under sig och har inte många av företagsorganisationernas funktioner.

Läs mer om [begränsningarna för produktallokering](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Du kan bara lägga till underordnade organisationer i rotorganisationer som är baserade på samma lagringsmodell. Underordnade organisationer som baseras på användarlagringsmodellen kan alltså bara läggas till i rotorganisationer baserat på användarlagringsmodellen. Underordnade organisationer baserade på företagets lagringsmodell kan dessutom bara läggas till i rotorganisationer baserat på företagets lagringsmodell.

På fliken **[!UICONTROL Organization Mapper]** visas följande:

1. En listruta med en lista över möjliga överordnade organisationer där du kan lägga till en underordnad organisation. Det här är organisationer som du är global administratör för.
1. En lista med underordnade organisationer som kan läggas till under den överordnade som valts i steg 1. Det här är organisationer som du är systemadministratör för och som inte redan är underordnade en annan organisation.

När en organisation läggs till i den globala administrationen behålls produkter i de organisationer som läggs till med hjälp av organisationsmappning som inköp. [Nummer för produkttilldelning](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) slutar att samlas i de här organisationerna.

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/) och navigera till **[!UICONTROL Organization Mapper]**.
2. Välj en överordnad organisation i listrutan.\
   Det här är de organisationer som du har lagts till direkt som global administratör för. Om du inte ser någon organisation som du vill använda som överordnad i listrutan väljer du en högre upp i hierarkin. När organisationsmappningsåtgärden har slutförts kan du använda [Ändra hierarki](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization) för att flytta den nya organisationen nedåt i trädet till den överordnade som du vill använda.
3. Välj de organisationer som ska läggas till som underordnade till den organisation som valdes i föregående steg.
4. Välj **[!UICONTROL Review Pending Changes]**.  Välj sedan **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.
5. När du har utfört ändringarna kan du upprepa stegen ovan för att lägga till ytterligare underordnade organisationer i organisationshierarkin.

När en organisation finns i hierarkin kan du justera organisationsprofiler, administratörer eller andra inställningar genom att gå till fliken **[!UICONTROL Organizations]**.
