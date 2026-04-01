---
title: Hämta granskningsloggar och exportrapporter
description: Läs om hur globala administratörer visar, filtrerar och exporterar granskningsloggar och rapporter i Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 5573d0f0e58b7ba799726740ae0d29b1053122aa
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Hämta granskningsloggar och exportrapporter

Gäller företag.

Läs om hur globala administratörer kan visa, filtrera och exportera granskningsloggar och rapporter med Global Admin Console.

Logga in på [Global Admin Console](https://global-admin-console.adobe.com/) för att komma igång. Gå sedan till fliken **[!UICONTROL Insights]** och välj **[!UICONTROL Audit Logs]** för att spåra alla ändringar som gjorts i olika organisationer.

## Visa och hämta granskningsloggar

Som global administratör har du fullständig insyn i de ändringar du har gjort i Global Admin Console. Du kan söka i granskningsloggar i alla organisationer efter åtgärder som har vidtagits de senaste 90 dagarna, inklusive när de inträffade och vem som utförde dem.
- Granskningsloggar säkerställer fortsatt regelefterlevnad genom att skydda mot felaktig systemåtkomst och genom att granska misstänkt beteende i organisationen.
- Loggarna i Global Admin Console innehåller endast händelser som en global administratör har åtkomst till. De innehåller inte användartilldelningar eller användarhändelser. [Läs mer](https://helpx.adobe.com/se/enterprise/using/admin-console.html) om de olika funktioner som varje konsol erbjuder.
- Loggarna täcker händelser för alla organisationer i hierarkin, vilket gör att du kan söka i granskningsloggar för alla organisationer samtidigt.

>[!NOTE]
>
> Som systemadministratör i en [Adobe Admin Console](https://adminconsole.adobe.com) -organisation kan du använda [granskningsloggen](https://helpx.adobe.com/enterprise/using/audit-logs.html) för att granska användartilldelningar och användarhändelser. Åtgärder som utförs av systemadministratörer i underordnade organisationer i den valda organisationen ingår också i granskningsloggarna. Läs mer om hur systemadministratörer kan [spåra ändringar](https://helpx.adobe.com/enterprise/using/audit-logs.html) som gjorts i Admin Console.

Så här visar eller hämtar du granskningsloggar för din organisation:

1. Som global administratör loggar du in på [Global Admin Console](https://global-admin-console.adobe.com/insights).
1. Välj **[!UICONTROL Insights]** > **[!UICONTROL Audit Logs]**.

Granskningsloggarna visar följande information om filtrerade händelser:

| Fält | Beskrivning |
|------ |-------------|
| Datum | Datum och tid för händelsen, som visas i den lokala tidszonen. |
| Händelsenamn | Beskrivning av åtgärden som utfördes. |
| Händelseinformation | Ytterligare händelseinformation, om sådan finns. |
| Objektnamn | Namn på den produkt, produktprofil eller användargrupp som berörs av händelsen, beroende på vad som är tillämpligt. |
| Berörd användare | E-postadress till den berörda användaren, om tillämpligt. |
| Administratör | E-postadress till den administratör som utförde åtgärden. *System* visas om åtgärden utfördes av ett Adobe-serverdelssystem. |
| IP-adress | IP-adress till datorn där åtgärden utfördes. Detta återspeglar vanligtvis den fysiska platsen, men kan vara en proxyserver eller VPN-adress. |
| Organisation | Namnet på den organisation som påverkas av händelsen. |

1. Du kan filtrera granskningsloggar med följande alternativ:

   - Sök efter påverkad användare eller administratör.
   - Markera en eller flera organisationer.
   - Definiera ett datumintervall.
   - Filtrera efter händelsenamn.
   - Kombinera filter för att begränsa resultaten, till exempel visa händelser från de senaste sju dagarna för en viss organisation.

   ![granskningsloggar](assets/audit-logs.png)

   *Filtrera granskningsloggarna baserat på händelsenamnet, den berörda organisationen eller datumintervallet.*

   ![select-organization](assets/select-organizations.png)

   *Välj organisationer för att filtrera granskningsloggarna.*

1. Om du vill exportera granskningsloggar väljer du **[!UICONTROL Export CSV]** för att exportera filtrerade resultat. Resultaten hämtas i CSV-format.

Mer information om fälten som ingår i exporten finns i [Loggschema](#log-schema).

>[!NOTE]
>
>Exporterade granskningsloggrapporter sparas i 90 dagar efter att de har skapats.


## Förstå granskningsloggsrapporten {#log-schema}

Den exporterade granskningsloggsrapporten innehåller följande fält för varje organisation:

| Fält | Beskrivning |
|------|------------|
| id | Händelse-ID |
| eventTime | Datum och tid för händelsen (lokal tidszon) |
| eventType | Händelsens namn |
| eventSubType | Ytterligare händelseinformation, om sådan finns |
| actorEmail | E-postadress till den administratör som utförde händelsen. *System* visas om händelsen utfördes av ett bakomliggande Adobe-system. |
| targetUserEmail | E-postadress till den berörda användaren, om tillämpligt |
| targetGroupName | Berörd användargrupp, om tillämpligt |
| targetProductName | Berörd produkt, om tillämpligt |
| targetProfileName | Berörd produktprofil, om tillämpligt |
| ipAddress | IP-adress till datorn där åtgärden utfördes. Normalt återspeglas den fysiska platsen, men det kan vara en proxyserver eller en VPN-adress. |
| organizationName | Namn på den berörda organisationen |

## Hämta exportrapporter

När en global administratör exporterar organisationsdata från [Global Admin Console](https://global-admin-console.adobe.com/insights) bearbetas rapporten och görs tillgänglig på fliken **[!UICONTROL Insights]** i **[!UICONTROL Export Reports]**.

Alla rapporter som genereras av globala administratörer är tillgängliga på ett och samma ställe. Funktionen för exportrapporter är användbar i följande scenarier:

- Om du har en stor hierarki med många organisationer behöver du inte längre vänta på att exportfilen ska bearbetas. Du kan använda rapporter som genererats av dina andra administratörer.
- Du behöver inte längre spara eller behålla dessa rapporter för att jämföra dem senare. Rapporterna sparas i 90 dagar och du kan ladda ned dem när som helst för att jämföra rapporter.


Så här hämtar du en exportrapport:

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/insights) och gå till **[!UICONTROL Insights]** > **[!UICONTROL Export Reports]**.

   Rapporterna som genererats de senaste 90 dagarna visas. När 90 dagar är klara kan du generera rapporten igen. Lär dig hur du kan generera rapporter för [organisationsstrukturen](https://helpx.adobe.com/enterprise/global-admin-console/export-and-import-data.html#export-and-import-organization-structure).


   | Fält | Beskrivning |
   |------|------------|
   | Rapportera | Datum och tid när rapporten skapades (lokal tidszon) |
   | Format | Filformat (CSV, JSON, XLSX) |
   | Storlek | Filstorlek |
   | Skapad av | E-postadress till den administratör som skapade rapporten |
   | Åtgärd | Länk för att ladda ned rapporten |

1. Välj **[!UICONTROL Download]** om du vill hämta en rapport.

   Om rapporten som du just genererade inte visas i listan väljer du **[!UICONTROL Refresh]**.

   ![export-reports](assets/export-reports.png)

*Hämta alla rapporter som har skapats under de senaste 90 dagarna.*
