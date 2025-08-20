---
title: Hantera resultat i  [!DNL Adobe Success] portalen
description: I den här guiden beskrivs hur du får tillgång till, tolkar och agerar utifrån resultaten i  [!DNL Adobe Success] portalen, så att du proaktivt kan hantera produktprestanda, säkerhet och funktionsrisker.
source-git-commit: 435931272f25caa6997a16d371aafcf70cf9facd
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Hantera resultat i portalen [!DNL Adobe Success]

I den här guiden förklaras hur du får tillgång till, kan tolka och agera på resultat i [!DNL Adobe Success]-portalen, så att du proaktivt kan hantera produktprestanda, säkerhet och funktionsrisker.

På sidan [!DNL Adobe Success] portal **[!UICONTROL Findings]** visas problem eller risker som upptäckts i din Adobe-produktinstans. Resultaten inkluderar problem med prestanda, säkerhet och funktionalitet samt status och risknivå. Genom att övervaka den här sidan kan du åtgärda problem tidigt - innan de påverkar dina miljöer.

**Vad är resultaten?**

Sökningar är aviseringar om supportinsikter som visas i portalen [!DNL Adobe Success]. De sätter fokus på potentiella problem i din Adobe-produktkonfiguration, t.ex. prestandaförsämringar, säkerhetsrisker eller felaktiga konfigurationer. Dessa aviseringar baseras på telemetridata som samlats in från verktyg som API:er, [!DNL New Relic] och [!DNL Splunk].

**Hur skapas upptäckter?**

Adobe team undersöker regelbundet de vanligaste supportproblemen och trenderna. Baserat på insikterna lägger de till nya kontroller i systemet. En gång om dagen genomsöker [!DNL Adobe Success]-portalen produktdata för att identifiera problem, till exempel felkonfigurationer, fastnade jobb eller något som kan leda till ett systemavbrott. Om en kontroll hittar något som ligger utanför säkerhetsområdet (enligt Adobe produkts- och supportteam) visas det som en fynd.

**Varför är upptäckter viktiga**?

Med jämna mellanrum kan du fånga upp problem tidigt - innan de påverkar ditt system eller dina kunder. Detta proaktiva tillvägagångssätt förbättrar systemets stabilitet, minskar driftstoppen och stöder bästa praxis.

**Så här åtgärdar du brister**

Varje möte innehåller rekommendationer och tydliga instruktioner om hur problemet ska lösas, tillsammans med länkar till relevant dokumentation, om sådana finns. Dela med er IT-avdelning, tekniker eller Adobe-partner och arbeta tillsammans för att åtgärda detta. Genom att åtgärda dessa problem tidigt kan du förhindra större problem och få systemet att fungera smidigt.


## Åtkomstresultat

Så här visar du insikter om en produkt:

1. Navigera till **[!UICONTROL Support & Insights]**.
1. Välj relevant produktkort. Klicka på fliken **[!UICONTROL Findings]**.  

   ![asp-support-inisghts-finding](../../assets/asp-support-inisghts-findings.png)


1. Du ser en lista över alla resultat för den valda produkten.

   ![adobe-success-portal-finding](../../assets/adobe-success-portal-findings.png)

1. Här kan du:

   ![adobe-success-portal-download](../../assets/adobe-success-portal-download.png)

   * Sök efter specifika poster.
   * Exportera listan med resultat genom att välja **[!UICONTROL Download Findings]**. Om du vill exportera en rapport för en sökning markerar du kryssrutan bredvid den relevanta sökningen i kolumnen **[!UICONTROL Finding Name]**. Om du inte väljer någon sökning innehåller PDF som standard en lista med alla resultat.
   * Se information om en sökning, inklusive en rekommenderad upplösning genom att välja en sökning under **[!UICONTROL Finding Name]**. På sidan Sökinformation visas den valda sökningen med ytterligare kontext och en rekommendation. Välj nedladdningspilen för att se den här rapporten.


     ![finding-details](../../assets/findings-details.png)


## Åtgärdsresultat

Följ de här stegen för att validera om varje upptäckt fortfarande kan användas eller avvisas.

>[!NOTE]
>:
>
>Standardkontroller körs på dina instanser. Om det inte går att hitta problemet i din instans har statusen **[!UICONTROL Not Detected]**.

1. Navigera till **[!UICONTROL Support & Insights]**.
1. Välj relevant produktkort.
1. Öppna fliken **[!UICONTROL Findings]**. Du ser alla resultat för den valda produkten.
1. Välj en post under **[!UICONTROL Finding Name]**. På sidan Sökinformation kan du:
   * Välj **[!UICONTROL Validate]** om du vill kontrollera om problemet fortfarande kvarstår (knappen **[!UICONTROL Validate]** är utformad som en bekräftelse på att problemet har lösts):

   ![adobe-success-portal-validate](../../assets/adobe-success-portal-validate.png)


   * Om problemet kvarstår visas följande meddelande: *[!UICONTROL Validation complete. Finding still detected]*. Använd informationen och rekommendationen på sidan Hitta detaljer för att undersöka och lösa problemet.
   * Om problemet inte längre förekommer visas följande meddelande: *[!UICONTROL Validation Complete. Finding no longer detected]*. När sökningen inte längre identifieras blir resultatet grått och statusen ändras till **[!UICONTROL Not Detected]**. Sökningar med statusen **[!UICONTROL Not Detected]** finns längst ned i resultatlistan.
   * Om problemet inte är relevant eller relevant för dig kan du stänga det genom att välja **[!UICONTROL Dismiss]**. När sökningen stängs blir resultatet grått och statusen ändras till **[!UICONTROL Dismissed]**.  Sökningar med statusen **[!UICONTROL Dismissed]** finns längst ned i resultatlistan.

## Förstå resultaten

* **[!UICONTROL Finding Name]** - Välj för detaljerade insikter och rekommenderade lösningssteg.
* **[!UICONTROL Type]** - Kategoriserad som *Funcality*, *Performance* och *Security*.
* **[!UICONTROL Risk Level]** - Allvarlighetsindikator, med visuella indikatorer.
* **[!UICONTROL Status]** - Sökningens aktuella tillstånd (t.ex. *Upptäckt*, *Ej upptäckt*, *Avvisad*).
* **[!UICONTROL Check Last Run]** - Tidsstämpel för den senaste kontrollen som uppdaterade sökningen.


## Bästa praxis

Sidan **[!UICONTROL Findings]** innehåller rekommendationer med följande risknivåer: **[!UICONTROL High]**, **[!UICONTROL Elevated]** och **[!UICONTROL Medium]**. **[!UICONTROL High]** är kritiskt, **[!UICONTROL Elevated]** är brådskande och **[!UICONTROL Medium]** är icke-kritiskt. För att bevara webbplatsens hälsa och prestanda:

* Åtgärda **[!UICONTROL High risk]**-upptäckter snabbt eftersom de utgör allvarliga hot.
* Lös **[!UICONTROL Elevated]** riskproblem snart för att undvika eskalering.
* Övervaka **[!UICONTROL Medium]**-riskfynden regelbundet och agera efter behov.




