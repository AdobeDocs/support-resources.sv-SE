---
title: Välj en organisation i Global Admin Console
description: Lär dig hur du väljer en organisation för redigering i Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 0bc0dbd8c7040e0be7e7bd45945edb0fb24cb7cc
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---


# Välj en organisation i Global Admin Console

Lär dig hur du väljer en organisation för redigering i Global Admin Console.

>[!NOTE]
>
>När du har tillgång till [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access) kan du börja med att välja en organisation som ska visa och hantera organisationens namn, användargrupper, produktprofiler, administratörer och organisationsprofiler. [Klicka här](https://global-admin-console.adobe.com/) om du vill logga in på Global Admin Console.

Global Admin Console fungerar som ett centralt förvaltningscentrum för Adobe resurser. Globala administratörer kan:

- Skapa underordnade organisationer under deras organisation
- Tilldela systemadministratörer att hantera dem
- Distribuera resurser till underordnade organisationer för hantering och tilldelning till användare i dessa organisationer

>[!NOTE]
>
> Användare och administratörer i en organisation har inte synlighet för användare, lagring eller andra resurser utanför sin organisation.

## Välj organisation

Organisationer som listas i listrutan **[!UICONTROL organization selector]** är de som du uttryckligen är global administratör för, det vill säga du har lagts till i administratörslistan för den organisationen med en global administratörsroll eller global visningsprogramroll. Du är implicit global administratör (eller globalt visningsprogram) för alla organisationer under den punkten i hierarkin, men dessa organisationer är inte listade i [!UICONTROL org picker].

![Organisationsväljaren](/help/adobe-support-tools-guide/assets/org-picker.png)

Om du vill att de ska visas i listan lägger du till dig själv som global administratör till de organisationer som du vill ska visas i listan. När du väljer en organisation i [!UICONTROL organization selector] baseras dina administrativa behörigheter på att vara global administratör för den valda organisationen. Du kan också vara listad som global administratör för en överordnad organisation högre upp i trädet, vilket kan ge dig fler behörigheter. Du måste välja den högnivåorganisationen för att få de extra behörigheterna.

När du har valt en organisation i [!UICONTROL hierarchy tree] i Global Admin Console kan du börja redigera information för en viss organisation.

**Redigeringar kan påverka:**

- Organisationsnamn
- Användargrupper
- Produktprofiler
- Administratörer
- Organisationspolicy

**Redigeringar kan inte påverka:**

- Användare (utom för borttagning av grupper eller produktprofiler)
- Lägga till användare (utom för administratörer)

När en organisation väljs från hierarkiträdet visas följande information:

- Organisationsnamn
- Län
- Antal användare
- Produktlista
- Produktprofiler
- Användargrupper
- Administratörer
- Anspråk domäner
- Organisationens policyvärden

Om du vill visa eller redigera produkter, användargrupper, administratörer, domäner, profiler eller principmallar väljer du lämplig flik. Du kan i de flesta fall använda fältet [!UICONTROL search] för att hitta ett visst objekt på fliken.

![Redigera en organisation](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

Alla administratörer som läggs till eller tas bort från en organisation får ett e-postmeddelande. Vissa principändringar i en organisation resulterar i ett meddelande i organisationens [!DNL Admin Console].

## Läs mer om begränsningar och nödvändiga villkor

- Det maximala djupet för kapslade organisationer är fem. Det innebär att a/b/c/d/e tillåts, men a/b/c/d/e/f är ett fel. Exempel: Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London är tillåtet, men Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair är ett fel.

- Den maximala sökvägen (inklusive alla organisationer) är 255 tecken (inklusive&quot;/&quot;). Ett organisationsnamn får innehålla högst 4 till 100 tecken.

- Organisationens sökvägsnamn är unikt, men det enkla namnet är bara unikt bland de andra på samma nivå. Det kan finnas organisationer med samma enkla namn någon annanstans i organisationshierarkin.

- Du kan bara visa listan över domäner som är länkade till den valda organisationen med hjälp av konsolen Global Admin. Om du är systemadministratör för den valda organisationen väljer du **[!UICONTROL Open in Admin Console]** för att [hantera domäner](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html). Information som visas på fliken Domäner finns i [Exportera och importera scheman](https://helpx.adobe.com/enterprise/global-admin-console/export-and-import-data.html#export-and-import-schemas).

- IE 11 stöds inte för global administrationsåtkomst. Använd en annan webbläsare eller en senare version av IE-webbläsaren.
