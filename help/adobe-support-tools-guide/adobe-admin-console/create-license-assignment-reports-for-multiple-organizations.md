---
title: Skapa licenstilldelningsrapporter för flera organisationer och produkter
description: Generera, visa och ladda ned licenstilldelningsrapporter för olika organisationer och produkter från Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 1ab0cf0f1e813e3d7cd594c60cd2d58e4f09c072
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Skapa licenstilldelningsrapporter för flera organisationer och produkter

Se hur globala administratörer kan generera och ladda ned detaljerade licensrapporter för flera organisationer och produkter för specifika datumintervall för att underlätta exakt spårning av licensprovisionering.

&#x200B;> [!NOTE]
>
> Om du vill skapa, visa och exportera en licenstilldelningsrapport loggar du in på [Global Admin Console](https://global-admin-console.adobe.com/) och går till **[!UICONTROL Insights]** > **[!UICONTROL Reports]** > **[!UICONTROL License assignment]**.

## Skapa en rapport

Med licenstilldelningsrapporter kan ni proaktivt övervaka licensetableringen och minska den manuella spårningen. Globala administratörer kan skapa en licenstilldelningsrapport för utvalda produkter för ett valfritt antal underordnade organisationer för att övervaka programvarulicensprovisioneringsdata för alla avdelningar.

1. Gå till fliken **[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)** i Global Admin Console.
2. Välj **[!UICONTROL License Assignment]** på sidan **[!UICONTROL Create report]**.
3. Markera organisationerna och välj **[!UICONTROL Next]**. Du kan välja varje organisation separat eller välja alla underordnade organ inom en överordnad med knappen **[!UICONTROL Select all]**.
   &#x200B;> [!NOTE]
   >
   >**Ta reda på varför du inte kan välja vissa organisationer**:
   >Om en underordnad organisation inte har ett kontrakt eller har ett separat Enterprise-kontrakt med samma produkt som den överordnade organisationen, inaktiveras den från att skapa en licenstilldelningsrapport. Om huvudorganisationens kontrakt till exempel har Adobe Acrobat, och den underordnade organisationen har samma avtal som en del av ett annat kontrakt, är produkten begränsad för allokering. På grund av detta är den också begränsad för att skapa rapporter i Global Admin Console. [Lär dig hur du spårar etablering för sådana organ med deras respektive Admin Console](https://helpx.adobe.com/se/enterprise/using/assignment-reports.html).
   >
   > [!NOTE]
   >
   > Du kan bara skapa uppdragsrapporter för organisationer med ett aktivt kontrakt.
4. Välj de produkter som ska inkluderas i rapporten och välj **[!UICONTROL Next]**.
   &#x200B;> [!NOTE]
   >
   >**Ta reda på varför du inte kan välja vissa produkter**:
   >Produkter som inte kan allokeras i Global Admin Console inkluderas inte för att skapa rapporter. Detta inkluderar för närvarande vissa Digital Experience-produkter som [!DNL Workfront], [!DNL Adobe Experience Manager] och [!DNL Adobe Experience Platform] samt produkter som [!DNL Adobe Firefly Services], [!DNL Acrobat Sign] och [!DNL Adobe Stock]. [Du använder Adobe Admin Console för att hitta licensprovisioneringsdata för dessa produkter](https://helpx.adobe.com/se/enterprise/using/assignment-reports.html).
5. Välj om rapporten ska sammanställas per månad eller år.
6. Välj ett anpassat datumintervall eller välj bland förinställda alternativ. Du kan välja valfritt startdatum från 18 juni 2020 fram till föregående dag, så länge det inte föregår avtalets startdatum.
7. Välj **[!UICONTROL Download]** om du vill exportera rapporten som en CSV-fil.

Rapporten börjar bearbetas och visas på sidan **[!UICONTROL License Assignment]** med information om namn, skapare, skapandetid, datumintervall och status. När du är klar får du ett e-postmeddelande och rapporten hämtas automatiskt.

Alla globala administratörer kan ladda ned rapporten när som helst efter att den är klar med hjälp av ikonen **[!UICONTROL Download]** bredvid rapportnamnet.

>[!NOTE]
>
>- Generera rapporter 48 timmar efter varje allokering för att säkerställa att de senaste uppgifterna återspeglas.
>- Rapporterna sparas i 90 dagar efter att de har skapats.

## Visa och hämta tidigare genererade rapporter

Globala administratörer kan visa och hämta licenstilldelningsrapporter som genererats av andra globala administratörer i organisationen. Globala visningsprogram kan dock bara visa listan med licenstilldelningsrapporter.

1. Gå till fliken **[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)** i Global Admin Console.
1. På sidan **[!UICONTROL License Assignment]** visas alla rapporter med följande information:

   | Fält | Beskrivning |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | Namn | Automatiskt genererad och kan inte redigeras. |
   | Skapare | Den globala administratören som genererade rapporten. |
   | Skapad | Systemtiden när rapporten skapades. |
   | Datumintervall | Rapportens valda datumintervall. |
   | Status | **Slutfördes** om rapporten är klar för hämtning, eller **Bearbetar** om den fortfarande genereras. |

1. Om du vill exportera rapporten som en CSV-fil väljer du ikonen **[!UICONTROL Download]** bredvid rapporten.

## Ta reda på rapporten om licenstilldelningen

Den rapport du laddar ned innehåller följande information för varje händelse:

| Fält | Beskrivning |
| -------------------------------- | -------------------------------------------------------- |
| Organisations-ID | Unikt ID kopplat till den överordnade organisationen |
| Org | Den överordnade organisationens namn |
| ID för underordnad organisation | Unik identifierare för den valda underordnade organisationen |
| Namn på underordnad organisation | Namnet på den underordnade organisationen |
| Licens-ID | Unikt ID för produktlicensen |
| Produktnamn | Namn på den valda produkten |
| Datum | Val av datum |
| Total licensmängd | Totalt antal licenser på överordnad organisationsnivå |
| Underordnade licenser | Antal licenser som har tilldelats den underordnade organisationen |
| Tilldelad kvantitet per månad/år | Sammanlagt värde för licenstilldelning (månadsvis/årsvis) |
