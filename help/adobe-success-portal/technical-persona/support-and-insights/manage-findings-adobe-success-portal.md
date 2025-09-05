---
title: 'Hantera resultat i portalen  [!DNL Adobe Success] '
description: Den här guiden förklarar hur du får tillgång till, tolkar och agerar utifrån resultat i portalen  [!DNL Adobe Success]  för att proaktivt hantera risker gällande produktprestanda, säkerhet och funktionalitet.
exl-id: c787ce29-993c-498c-9e39-8a04c2eeedda
source-git-commit: b05c238726c88ae0c51f40f077192dc136c0ae59
workflow-type: ht
source-wordcount: '708'
ht-degree: 100%

---

# Hantera resultat i portalen [!DNL Adobe Success]

I den här guiden förklaras hur du får tillgång till, kan tolka och agera på resultat i portalen [!DNL Adobe Success] så att du proaktivt kan hantera produktprestanda, säkerhet och funktionsrisker.

På sidan [!DNL Adobe Success] i portalen **[!UICONTROL Findings]** visas problem eller risker som upptäckts i din Adobe-produktinstans. Resultaten inkluderar problem med prestanda, säkerhet och funktionalitet samt status och risknivå. Genom att övervaka den här sidan kan du åtgärda problem tidigt – innan de påverkar dina miljöer.

**Vad är resultat?**

Resultat är aviseringar om supportinsikter som visas i portalen [!DNL Adobe Success]. De sätter fokus på potentiella problem i din Adobe-produktkonfiguration, t.ex. prestandaförsämringar, säkerhetsrisker eller felaktiga konfigurationer. Dessa aviseringar baseras på telemetridata som samlats in från verktyg som API:er, [!DNL New Relic] och [!DNL Splunk].

**Hur skapas resultat?**

Adobe-team undersöker regelbundet de vanligaste supportproblemen och trenderna. Baserat på insikterna lägger de till nya kontroller i systemet. En gång om dagen genomsöker portalen [!DNL Adobe Success] produktdata för att identifiera problem, till exempel felkonfigurationer, jobb som har fastnat eller något som kan leda till ett systemavbrott. Om en kontroll hittar något som ligger utanför säkerhetsområdet (enligt Adobe produkts- och supportteam) visas det som ett resultat.

**Varför resultat är viktiga**

Med jämna mellanrum kan du fånga upp problem tidigt – innan de påverkar ditt system eller dina kunder. Detta proaktiva tillvägagångssätt förbättrar systemets stabilitet, minskar driftstoppen och stöder bästa praxis.

**Så här åtgärdar du resultat**

Varje möte innehåller rekommendationer och tydliga instruktioner om hur problemet ska lösas, tillsammans med länkar till relevant dokumentation, om sådana finns. Dela dessa resultat med ditt IT-team, din teknikavdelning eller Adobe-partner och samarbeta för att åtgärda dem. Genom att åtgärda dessa problem tidigt kan du förhindra större problem och få systemet att fungera smidigt.


## Åtkomstresultat

Så här visar du insikter om en produkt:

1. Navigera till **[!UICONTROL Support & Insights]**.
1. Välj relevant produktkort. Klicka på fliken **[!UICONTROL Findings]**.  

   ![asp-support-inisghts-findings](../../assets/asp-support-inisghts-findings.png)


1. Du ser en lista över alla resultat för den valda produkten.

   ![adobe-success-portal-findings](../../assets/adobe-success-portal-findings.png)

1. Här kan du:

   ![adobe-success-portal-download](../../assets/adobe-success-portal-download.png)

   * Sök efter specifika poster.
   * Exportera listan med resultat genom att välja **[!UICONTROL Download Findings]**. Om du vill exportera en rapport för en sökning markerar du kryssrutan bredvid den relevanta sökningen i kolumnen **[!UICONTROL Finding Name]**. Om du inte väljer något resultat innehåller PDF-filen som standard en lista med alla resultat.
   * Se information om ett resultat, inklusive en rekommenderad upplösning genom att välja ett resultat under **[!UICONTROL Finding Name]**. På sidan Resultatinformation visas den valda sökningen med ytterligare kontext och en rekommendation. Välj hämtningspilen för att se den här rapporten.


     ![findings-details](../../assets/findings-details.png)


## Åtgärdsresultat

Följ de här stegen för att validera om varje resultat fortfarande kan användas eller avvisas.

>[!NOTE]:
>
>Standardkontroller körs på dina instanser. Om kontrollerna inte visar att problemet finns i din instans har den statusen **[!UICONTROL Not Detected]**.

1. Navigera till **[!UICONTROL Support & Insights]**.
1. Välj relevant produktkort.
1. Öppna fliken **[!UICONTROL Findings]**. Du ser alla resultat för den valda produkten.
1. Välj en post under **[!UICONTROL Finding Name]**. På sidan Resultatinformation kan du:
   * Välj **[!UICONTROL Validate]** om du vill kontrollera om problemet fortfarande kvarstår (knappen **[!UICONTROL Validate]** är en bekräftelse på att problemet har lösts):

   ![adobe-success-portal-validate](../../assets/adobe-success-portal-validate.png)


   * Om problemet kvarstår visas följande meddelande: *[!UICONTROL Validation complete. Finding still detected]*. Använd informationen och rekommendationen på sidan Information om upptäckt för att undersöka och lösa problemet.
   * Om problemet inte längre finns visas följande meddelande: *[!UICONTROL Validation Complete. Finding no longer detected]*. När upptäckten inte längre identifieras blir den gråtonad och statusen ändras till **[!UICONTROL Not Detected]**. Upptäckter med statusen **[!UICONTROL Not Detected]** finns längst ned i upptäcktslistan.
   * Om problemet inte gäller eller är relevant för dig kan du avfärda det genom att välja **[!UICONTROL Dismiss]**. När upptäckten avfärdats blir den gråtonad och statusen ändras till **[!UICONTROL Dismissed]**. Upptäckter med statusen **[!UICONTROL Dismissed]** finns längst ned i upptäcktslistan.

## Förstå upptäckterna

* **[!UICONTROL Finding Name]** – Välj för detaljerade insikter och rekommenderade lösningssteg.
* **[!UICONTROL Type]** – Kategoriserad som *Funktion*, *Prestanda* och *Säkerhet*.
* **[!UICONTROL Risk Level]** – Allvarlighetsindikator, med visuella indikatorer.
* **[!UICONTROL Status]** – Upptäcktens aktuella tillstånd (t.ex. *Upptäckt*, *Ej upptäckt*, *Avfärdad*).
* **[!UICONTROL Check Last Run]** – Tidsstämpel för den senaste kontrollen som uppdaterade upptäckten.


## Bästa praxis

Sidan **[!UICONTROL Findings]** innehåller rekommendationer med följande risknivåer: **[!UICONTROL High]**, **[!UICONTROL Elevated]** och **[!UICONTROL Medium]**. **[!UICONTROL High]** är kritisk, **[!UICONTROL Elevated]** är brådskande och **[!UICONTROL Medium]** är inte kritisk. För att bibehålla webbplatsens hälsa och prestanda:

* Åtgärda **[!UICONTROL High risk]**-upptäckter snabbt eftersom de utgör allvarliga hot.
* Lös **[!UICONTROL Elevated]**-riskproblem snart för att undvika eskalering.
* Övervaka **[!UICONTROL Medium]**-riskupptäckter regelbundet och agera efter behov.
