---
title: Hantera administratörer
description: Hur Adobe-kunder kan konfigurera och hantera administratörer i Global Admin Console för att styra användaråtkomst, produktlicenser och organisationsresurser.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 41c00379-98ee-4922-8eba-cc373c23a019
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---

# Hantera administratörer

*Gäller för företag.*

Utforska de globala administratörsfunktionerna och lär dig hur du delegerar och distribuerar administration av användare, produktlicenser och grupper till administratörer för varje enskild organisation.

I Global Admin Console kan du välja en organisation och navigera till fliken **[!UICONTROL Admins]** för att lägga till, redigera eller ta bort administratörsrättigheter. Mer information finns i [Adobes globala administration](https://helpx.adobe.com/se/enterprise/global-admin-console/adopt-global-administration.html). Gå hit för att [logga in på Admin Console](https://adminconsole.adobe.com).


Global Admin Console introducerar en roll som kallas global administratör. Den här rollen skiljer sig från en systemadministratör och gör följande:

- Se det globala landskapet för din totala investering i Adobe för alla Admin Consoles som lagts till i Global Admin Console-hierarkin.
- Övervaka Adobe licens- och resurstilldelningar och användning i flera administrationskonsoler.
- Skapa administrationskonsoler eller -organisationer.
- Tilldela produktlicenser från en rot- eller överordnad Admin Console till underordnade Admin Consoles som sitter nedanför i hierarkin.
- Underhåll den dagliga driften medan systemadministratörer fortsätter att hantera sina egna Admin Consoles. En global administratör kan till exempel tilldela en produkt till en underordnad Admin Console men inte tilldela den till användare. Systemadministratören får licenserna inom sin Admin Console och tilldelar produkterna till sina användare.
- Du kan också tillämpa organisationsprofiler på alla Admin Consoles i hierarkin.

## Grundläggande administrativa uppgifter

Global Admin Console är utformat för att fungera i olika organisationer och på olika Admin Consoles. Följande tabell visar de olika funktionerna och var de kan fyllas i - Admin Console eller Global Admin Console.

<table>
  <tr>
    <th colspan="2">Uppgift</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">Skapa, reparera och ta bort underordnade organisationer</td>
    <td align="center">Ja</td>
    <td align="center">Nej</td>
  </tr>

<tr>
    <td colspan="2">Arbeta i flera organisationer</td>
    <td align="center">Ja</td>
    <td align="center">Nej</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">Hantera administratörer</td>
    <td>För en eller flera organisationer</td>
    <td align="center">Ja</td>
    <td align="center">Nej</td>
  </tr>

<tr>
    <td>För en organisation</td>
    <td align="center">Ja</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Hantera produktprofiler och användargrupper</td>
    <td align="center">Ja</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Definiera och hantera policyer</td>
    <td align="center">Ja</td>
    <td align="center">Nej</td>
  </tr>

<tr>
    <td colspan="2">Fördela produkter i olika organisationer</td>
    <td align="center">Ja</td>
    <td align="center">Nej</td>
  </tr>

<tr>
    <td colspan="2">Tilldela produkter till användare</td>
    <td align="center">Nej</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Hantera användare</td>
    <td align="center">Nej</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Hantera paket</td>
    <td align="center">Nej</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Konfigurera domäner och kataloger</td>
    <td align="center">Nej</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Hantera Enterprise-lagring och kryptering</td>
    <td align="center">Nej</td>
    <td align="center">Ja</td>
  </tr>
</table>

## Hantera administratörer

Du kan skapa en flexibel administrativ hierarki som detaljerat kan hantera åtkomst och användning av Adobe-produkter. I likhet med Adobe Admin Console kan du med Global Admin Console lägga till systemadministratörer, produktadministratörer, produktprofiladministratörer, användargruppadministratörer, distributionsadministratörer, supportadministratörer och lagringsadministratörer. Dessa administratörer kan utföra sina respektive administrativa uppgifter i de organisationer som de är administratörer i. Förutom dessa roller finns det två nya roller för den globala administrationen: Global Admin och Global Viewer.

Global administratör är en transitiv roll. Att göra en användare till global administratör för en organisation gör automatiskt användaren till global administratör för alla underordnade i organisationen, direkt eller indirekt. Om en ny organisation skapas i organisationshierarkin blir dessutom alla globala administratörer för alla överordnade i den organisationen omedelbart globala administratörer för den nya organisationen.

Följande funktioner finns i den globala administratörsrollen:

- Skapa och ta bort underordnade organisationer
- Ange och redigera profiler
- Ange och ändra administrativa roller
- Lägga till och ta bort produkter i underordnade organisationer
- Ange eller ändra resursallokeringar för underordnade organisationer
- Hantera produktprofiler och användargrupper

Följande funktioner finns i rollen Global Viewer:

- Visa listan över användargrupper, produkter, produktprofiler, administratörer, policyer och resurser i organisationen och i de underordnade organisationerna.

## Distribuerad administration

Genom att hantera administratörer kan en global administratör delegera och distribuera administrationen av användare, produktlicenser och grupper till administratörer för varje enskild organisation. Administratören som lagts till i en organisation av en global administratör får flexibilitet att hantera organisationen utan att ha någon insyn i administrationen av andra organ. Den globala administratören kan delegera administration av resurser och användare som håller data om dessa resurser och användare isolerade.

En global administratör kan skapa organisationer, distribuera produkter och lagring till dessa organisationer, hantera identitetsinställningar samt skapa och tillämpa mallar för organisationsprinciper. En systemadministratör som har lagts till i en organisation av en global administratör kan tilldela produkter till användare, inbyggda användare, skapa och hantera produktprofiler och utföra andra administrativa uppgifter inom organisationen.

## Lägg till en administratör

1. I [Global Admin Console](https://global-admin-console.adobe.com/) väljer du en organisation att redigera och går sedan till fliken **[!UICONTROL Admins]**.

1. Välj **[!UICONTROL Add Admin]**.

   ![Lägg till administratör för Global Admin Console](../assets/global-admin-console-add-admin.png)

1. I dialogrutan **[!UICONTROL Add Admin]** anger du **[!UICONTROL User Details]**: E-post, Förnamn, Efternamn, Kontotyp och Landskod.

   Om du försöker lägga till en befintlig användare som administratör väljer du samma kontotyp som den befintliga användaren, annars misslyckas åtgärden för att lägga till.

   >[!NOTE]
   >
   > Organisationer kan ha begränsningar för vilka kontotyper som kan läggas till. Dessa kan vara baserade på [principer](https://helpx.adobe.com/se/enterprise/global-admin-console/update-policies.html) eller andra konfigurationsparametrar för en organisation. Organisationer tillåter inte att både AdobeID-användare och BusinessID-användare läggs till samtidigt. I allmänhet bör det inte finnas användare av båda typerna i en organisation, men beroende på i vilken ordning reglerna anges kan det finnas vissa användare av en viss kontotyp som fördaterar tillämpningen av policyer eller regler.

1. Välj en eller flera administratörsroller i avsnittet **[!UICONTROL Admin Rights]**.

   För roller som produktadministratör, produktprofiladministratör och användargruppadministratör väljer du de specifika produkterna, profilerna och grupperna.

   ![Lägg till administratör för Global Admin Console](../assets/global-admin-console-add-admin-detail.png)

1. Välj **[!UICONTROL Save]**.

1. När du har redigerat organisationer väljer du **[!UICONTROL Review Pending Changes]** och sedan **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/se/enterprise/global-admin-console/execute-jobs.html) ändringarna.

När en administratörsroll läggs till får användaren ett e-postmeddelande som informerar dem om ändringen av deras roll.

När administratören har lagts till får han/hon ett e-postmeddelande med en inbjudan om att godkänna sin roll och ge honom/henne en länk till Admin Console. Om de läggs till som både global administratör och som en annan roll får de två inbjudningar, en till Global Admin Console och en till Admin Console.

## Redigera en administratör

1. Välj en organisation som du vill redigera och navigera till fliken **[!UICONTROL Admins]**.

1. Välj ikonen **[!UICONTROL More Options]** ( ⋮) för den aktuella administratören och välj sedan **[!UICONTROL Edit Admin]**.

   ![Global Admin Console Redigera administratörsrättigheter](../assets/global-admin-console-edit-admin-right.png)

1. Uppdatera administratörsinformationen och välj sedan **[!UICONTROL Save]**.

1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna.

Ett separat kommando visas i listan över väntande ändringar för varje tillagd eller borttagen administratörsroll. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/se/enterprise/global-admin-console/execute-jobs.html) dem.

## Ta bort administratörsrättigheter

1. Välj en organisation som du vill redigera och navigera till fliken **[!UICONTROL Admins]**.

1. Välj ikonen **[!UICONTROL More Options]** ( ⋮) för den aktuella administratören och välj sedan **[!UICONTROL Remove Admin Rights]**.

   ![Global Admin Console - ta bort administratörsrättigheter](../assets/global-admin-console-remove-admin-right.png)

1. Välj **[!UICONTROL OK]** i bekräftelsedialogrutan.

1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/se/enterprise/global-admin-console/execute-jobs.html) dem.

När du har tagit bort en administratör får användaren ett e-postmeddelande som informerar användaren om att åtkomst till administrationskonsolen för organisationen har förlorats.
