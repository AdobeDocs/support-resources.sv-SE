---
title: Adobe DX Solutions Unified Holiday Readiness Guide
description: Den här artikeln innehåller en guide om beredskap för semester för DX Solutions.
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
source-git-commit: 3ae8c97072cd6f8ae09aa8dc1e3ce0249fe6fcb7
workflow-type: tm+mt
source-wordcount: '3694'
ht-degree: 0%

---

# Adobe DX Solutions Unified Holiday Readiness Guide


Adobe DX Solutions Unified Holiday Readiness Guide hjälper dig att förbereda dig för semestersäsongen genom att fokusera på proaktiv planering istället för att reaktiv problemlösning. Den innehåller praktiska åtgärder för att säkerställa att instanserna är klara och minimerar eventuella problem innan de uppstår. Adobe team har teknisk expertis, ett brett utbud av funktioner och beprövade metoder för att leverera rätt nivå av support och vägledning - både teknisk och strategisk - så att ert företag är väl förberett.

Följ dessa metodtips för att försäkra dig om att era Adobe Digital Experience-lösningar är flexibla, säkra och redo för högtrafik på semester:

* Planera för ökad trafik.
* Undvik större förändringar under fönstertoppar; schemalägg uppdateringar före eller efter helgerna.
* Använd kontrollpaneler och varningar för att övervaka prestanda och upptäcka flaskhalsar tidigt.
* Se till att dina auktoriserade supportkontakter är aktuella.
* [Kontakta Adobe support](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket) i förväg när det är möjligt.

Information om lösningsspecifika rekommendationer för beredskap för semester från Adobe finns i följande avsnitt.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>Klicka på varje avsnitt för att expandera det.

<details>
<summary><h2 id="aep" style="display: inline-block;">Guide för beredskap för helgdagar i Adobe Experience Platform (AEP)</h2></summary>

Adobe Experience Platform (AEP) spelar en viktig roll när det gäller att skapa kundupplevelser i realtid. När helgen närmar sig är det viktigt att se till att AEP-implementeringen är optimerad för ökad trafik, säker datahantering och skalbart intag.

## Förutspå säsongsbunden efterfrågan

Adobe rekommenderar att man planerar för kapacitet och övervakar inmatning av strömningsprofiler för att förbereda sig för säsongstrafiken. Detta inkluderar prognoser av datavolymer och säkerställer att systemet kan hantera ökat dataflöde. Se [Planera för kapacitet och säsongstrafik](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) för referens.

## Förbered för skalning

Adobe har flera strategier för att säkerställa att din miljö är redo för semestertrafik:

* Öka tilldelad kapacitet för sandlådor.
* Identifiera dataflöden med hög genomströmning på [övervakningsinstrumentpanelen](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) och tillämpa strypning eller filtrering där det behövs.
* Använd gruppinmatning för användning med låg fördröjning för att optimera prestanda enligt beskrivningen i [Licensanvändning och -kapacitet: Bästa praxis för direktuppspelning](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions).

Dessa metoder bidrar till att upprätthålla tillförlitligheten vid intag och minska fördröjningen under perioder med hög belastning.

## Bästa praxis och skyddsmetoder

För att hålla er inom de operativa gränserna och undvika avbrott i tjänsten rekommenderar Adobe att ni följer anvisningarna om intag och profil:

* [Bästa praxis för direktuppspelad genomströmning](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions)
* [Garantier för datainmatning](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/guardrails)
* [Standardskyddsräcken för kundprofildata och segmentering i realtid](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails)
* [AEP-utkast: Guardrails](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-overview/guardrails)

## Säkerhet och styrning

Adobe betonar starka säkerhets- och styrningsrutiner, särskilt under trafiksäsonger när datakänsligheten ökar.

Se [Styrning, sekretess och säkerhet i Adobe Experience Platform: Säkerhet](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/overview#security) för rekommendationer om hur du skyddar kunddata, tillämpar sekretesskontroller och upprätthåller regelefterlevnad i hela AEP-implementeringen.

Genom att följa dessa riktlinjer och utnyttja Adobe offentliga dokumentation kan man säkerställa att deras Adobe Experience Platform är flexibel, säker och redo att leverera enastående kundupplevelser under helgen.

</details>

<details>
<summary><h2 id="ajo" style="display: inline-block;">Guide för beredskap för helgdagar i Adobe Journey Optimizer (AJO)</h2></summary>

För att förbereda Adobe Journey Optimizer för semestersäsongen bör man kunna förutse händelseförlopp och komplexa flerkanalsaktiviteter, konfigurera rese- och frekvensregler samt säkerställa datahygien och beslutslogik. De måste också validera resultatet i stor skala, tillämpa säkerhetsregler och API-skyddsutkast och tillämpa insikter efter det att ni nått topp för att förfina framtida kampanjer.

## Förutsägelseefterfrågan

* Baserat på komprimering av semestersäsongen och större kampanjvolym kan du förvänta dig följande:
   * En topp i realtidshändelser och triggade resor (övergivna varukorgar, erbjudanden i sista minuten)
   * Risker för meddelandemättnad (högre avanmälan, trötthet)
   * Ökad flerkanalskomplexitet (e-post + push + SMS + i appen)
* Använd föregående års mätvärden (öppnings-/klickfrekvens/avanmälningsfrekvens, antal besökare) för att modellera förväntade laster och ange tröskelvärden för era meddelandesystem.
* Identifiera sannolika&quot;tysta fönster&quot; eller perioder med låg prestanda (t.ex. helger, helgdagar) och planera sändning av volymer i enlighet med detta.

## Förbered för skalning

* Kontrollera att alla kanalkonfigurationer i AJO är korrekt konfigurerade: e-post, push, SMS, webb, i appen. Se [Konfigurera kanalkonfigurationer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces).
* Konfigurera regler för frekvensbegränsning och capping för att styra meddelandevolymer. Se artikeln [Fästfrekvens](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules).
* Konfigurera regeluppsättningar för kanaler/resor: [Arbeta med regeluppsättningar](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets).
* Förbered era data-hygienen/händelseströmmar i realtid och segmenteringsramverk.
* Se till att ni har definierat målgrupper för semesterkampanjer, som:
   * värdefulla kunder
   * lojala segment
   * övergivna varukorgar
   * förstagångsköpare
* Läs in mallar i förväg eller förbered mallar för semesterresor, utnyttja beslutslogik (erbjudanden/begränsningar) så att du kan anpassa dynamiskt baserat på lager, tidskänsliga erbjudanden och kanalpreferenser. Se exemplet i artikeln [Lägg till begränsningar i ett erbjudande](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints).
* Teknisk beredskap: Bekräfta inläsningskapacitet för API/slutpunkt, regler för begränsning/begränsning för anpassade åtgärder och externa integreringar. Mer information finns i [Guardrutor och begränsningar](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/guardrails).

## Testa och validera

* Använd ditt experimentramverk för att testa viktiga variabelförändringar:
   * sändningstid
   * erbjudandetyp
   * kanalmix
Läs [AJO Experimentation Accelerator bästa praxis](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices).
* Genomför komplett validering av resan:
   * händelseutlösare
   * segmenteringspost
   * resevägsflöden
   * personaliseringslogik
   * begränsningar
   * avslutningskriterier
* Kontrollera regler för capping och konflikt. Läs artikeln [Resebegränsning och skiljeförfarande](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/journey-capping).
* Stresstest av skalade volymer för topputskick eller toppspikar: Simulera stora utlösande volymer för att validera systembeteendet under belastning.
* Validera leveransen: Värm upp e-postdomäner/avsändare, bekräfta push-konfigurationer för mobila enheter och kontrollera reservkanaler för SMS/i-appen.

## Bästa praxis

* Använd flerkanalsmarknadsföring. Läs artikeln [Essential omnichannel customer travel for engagement and growth](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) på bloggen som visar ett exempel på semestersäsong med AJO.
* Prioritera triggers i realtid där det är lämpligt. Exempel: kundvagn, överge, bläddra och visa varningar när semestershoppare blir mer reaktiva.
* Utnyttja segmentering och personalisering: inrikta er på segment med hög återgivning, skräddarsy erbjudanden baserat på tidigare köpbeteende och önskemål.
* Minsta meddelandetrötthet: Tvinga ändpunkter och tysta timmar för att undvika överdriven oskärpa. Se blogginlägget [Förbättra kundupplevelsen med funktionen för daglig frekvensbegränsning i AJO](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510).
* Tidsplanering: Planen skickar tidigare i helger (komprimerad årstid) och anpassar kanalerna till tidszoner och lokala målgruppsbeteenden.
* Erbjud dynamiska/tidsbegränsade erbjudanden för att skapa ett trängande behov, men koordinera över olika kanaler för att undvika dubbelarbete och konflikter.
* Använd inaktiveringslogik: Undvik målgrupper som just har köpt, eller använd kundresor för att undvika redundanta meddelanden.

## Säkerhet och styrning

* Se till att åtkomstkontroll och behörigheter är konfigurerade så att bara de användare som krävs kan distribuera resor eller ändra affärsreglerna.
* Övervaka och framtvinga API-anrop/anslutningsbegränsning: Se t.ex. [API:t för att hämta | Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/connect-systems/external-systems/capping) -artikel.
* Använd rena förstahandsdata och säkerställ korrekt identitetssammanfogning så att meddelanden är kundcentrerade och inte dubbleras/feljusteras.
* Se till att leveransdomänerna värms upp och vidta åtgärder mot skräppost, särskilt för högvolymsmejl.
* Granska granskningsloggar och förändringar av resor ofta under högsäsong för att upptäcka felaktiga körningar eller felaktiga resor tidigt.

## Post peak learns

* Efter toppbelastningar kan du utföra en granskning av antalet resenärer, antalet inaktiveringar, avanmälningsfrekvensen, leveransstatistik och kanalprestanda.
* Rensa upp undertryckta segment och pausa eller pensionera resor som har byggts för semesterperioden för att undvika trötthet i samband med överföring.
* Använd insikter från realtidsprestanda för att förfina nästa års planering (till exempel: tidsjusteringar för sändning, kanalmixning och meddelandevolym).

Genom att proaktivt förutse säsongsrelaterade efterfrågan, konfigurera kanaler och regler, validera reseprestanda samt upprätthålla säkerhet och styrning kan man säkerställa att Adobe Journey Optimizer levererar smidiga, personaliserade och flexibla kundupplevelser under hela semestersäsongen och framåt.

</details>

<details>
<summary><h2 id="cja" style="display: inline-block;">Guide för beredskap för helgdagar i Adobe Customer Journey Analytics (CJA)</h2></summary>

Customer Journey Analytics använder The 5 PS för att uppnå beredskap för semester/högsäsong.

## Customer Journey Analytics - beredskap för semester/högsäsong: De 5 PS

### Förbered för skalning

* Granska CJA-anslutningar och datavyer; fastställa vilka anslutningar och datavyer som kräver förbättrad övervakning och etablering.
* Bekräftelseetableringen räcker för semesterskala; skala upp viktiga anslutningar och datavyer efter behov. Mer information finns i [Hantera anslutningar](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/manage-connections).

### Bildskärmsprestanda

* Utnyttja RAM ([[!UICONTROL Reporting Activity Manager] översikt](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) för att övervaka aktiva och köade rapportbegäranden i realtid, identifiera kapacitetsanslutningar och hitta flaskhalsar.
* Håll utkik efter ökad fördröjning vid toppbelastning med artiklarna [Felsök och Felsökningsguide](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) och [Kända begränsningar](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations) .
* Gör det möjligt för administratörer att i förväg pausa eller avbryta långvariga/blockerade begäranden via RAM. Läs artikeln [Avbryt rapportbegäranden i CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests).

### Bästa praxis

* Schemalägg export/rapporter under lågtrafikperioder för att jämna ut belastningen och minimera latensen. Läs artikeln [Schemalagda rapporter](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/scheduled-projects-manager).
* Sprid ut begäranden: Schemalägg rapporter med olika intervall under dagen.
* Minska antalet paneler, förenkla segment, korta datumintervall och undvik överflödiga samtidiga jobb. Mer information finns i artikeln [Optimera prestanda för CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance).

### Felsökning

* Vid felsökning av arbetsytefel bör du läsa felmeddelanden för orsaken och rekommenderade åtgärder. Använd RAM ([!UICONTROL Reporting Activity Manager]) för att rensa flaskhalsar och hantera samtidighet effektivt. Mer information finns i [Felhantering för CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages).
* Använd RAM ([[!UICONTROL Reporting Activity Manager] i CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) för att identifiera problematiska användare, frågor eller projekt. Prioritera och avsluta/avbryt efter behov.

### Post peak learns

* Efter semester-/toppperioden ska du granska prestandan och incidentloggarna för att utvärdera effekten av bästa praxis.
* Granska långsamma frågor och användaruppgifter för att identifiera mönster och trender som kan optimeras för nästa säsong.
* Samla in feedback från användare och intressenter - uppdatera era egna runbooks och beredskapsplaner med hjälp av nya insikter.
* Ge Adobe-teamen feedback via ert kontoteam.

</details>

<details>
<summary><h2 id="commerce" style="display: inline-block;">Beredskapshandbok för helgdagar i Adobe Commerce</h2></summary>

För att få en bra högsäsong i er organisation är det viktigt att ni förbereder er på Adobe Commerce digitala butik för högtrafik.

## Förutsägelseefterfrågan

* Under perioden för högsäkring av helgerna (mitten av november till mitten av januari) rekommenderar Adobe att alla Adobe Commerce-handlare som finns på vår molninfrastruktur aktivt planerar att öka antalet besökare genom att skicka in begäran om överkapacitet på semester. Mer information finns i [Förfrågningar om överkapacitet på helgdag för Adobe Commerce i vår molninfrastruktur](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud).

## Förbered för skalning

Följ rekommendationerna i guiden [Planering och pivotering: En strategisk strategi för högsäsong 2025](https://experienceleague.adobe.com/en/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025) som innehåller åtgärdbara strategier med Adobe Commerce (och valfria Adobe Experience Cloud-verktyg) som hjälper dig att planera, pivotera och leverera enastående kundupplevelser under årets livligaste tid.

## Bästa praxis

* Följ Adobe guide [Så här förbereder du din infrastruktur för hög trafik - de 5 Ps med högsäsong &#x200B;](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic).
* Ta en titt på [Tekniska tips om hur du kan förbereda din infrastruktur för högtrafik, förhindra driftstopp och optimera prestanda under semesterperioden.](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness)

</details>

<details>
<summary><h2 id="aem" style="display: inline-block;">Guide för beredskap för helgdagar i Adobe Experience Manager (AEM)</h2></summary>

Semestersäsongen närmar sig snabbt, och för många Adobe-kunder innebär detta att man börjar få säsong. Vi vill försäkra oss om att ni är fullt förberedda inför den kommande trafiktoppen.

## Adobe Experience Manager (AEM) Cloud Services

Om er organisation upplever de största stunderna under semestersäsongen kanske ni funderar på hur ni ska optimera er Adobe Experience Manager webbplats för att passa trafiktopparna. Som tur är har din webbplats med Adobe Experience Manager Cloud Services redan funktioner för automatisk skalning, vilket ger en smidig upplevelse för besökarna, oavsett om det sker några plötsliga trafikförändringar.

## Förbered för skalning

* Mer information och vägledning om hur du förbereder dig för hög trafik med Adobe Experience Manager Cloud Services finns på följande länkar:

   * [CDN i AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Service-cachning](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/caching/overview)

* Om du är Ultimate Success-kund och nyligen har delat information om volymprognoser med ditt Adobe-kontoteam behöver du inte skicka det till oss igen eftersom vi redan har en vy.

Vi är här för att hjälpa dig under varje steg av din resa. Om du har några frågor eller funderingar kan du [skicka in en supportanmälan](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Om du vill förbereda dig för en marknadsföringskampanj under semestersäsongen läser du dokumentationen för [AEMaaCS User Guide: Introduction - Marketing campaign parameters](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters) .

## Säkerhet och styrning

Mer information om trafiksäkerhet/skydd för AEM webbplatser finns i artikeln [Översikt - Skydda AEM webbplatser](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) i AEM as a Cloud Service självstudiekurser.

## Planering av underhåll av semester

Adobe har schemalagda undantagsperioder för underhåll för att säkerställa oavbruten service under kritiska helgdagar:

* **Inga automatiska uppdateringar** inträffar mellan:
   * 24 november 2025-2 december 2025
   * 15 december 2025-2 januari 2026

Detta garanterar stabilitet under trafikperioder. Fullständiga releasescheman och underhållsperioder finns i [AEM-releasemartan](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap).

## Adobe Experience Manager (AEM) med Adobe Managed Services (AMS)

AEM-kunder som utnyttjar Adobe Managed Services kan arbeta proaktivt med sina CSE-skivor för att planera för helgdagens behov.

</details>

<details>
<summary><h2 id="marketo" style="display: inline-block;">Adobe Marketo guide om beredskap för semester</h2></summary>

För att säkerställa lyckade semesterkampanjer med Adobe Marketo bör teamen kontrollera inställningarna för e-postautentisering, rensa och skydda sin databas, optimera kampanjlogik och schemaläggning, noggrant testa återgivning och leverans av e-post och effektivisera supportberedskapen för bästa prestanda och engagemang.

## Förbered för skalning

* Kontrollera inställningarna för SPF/DKIM och se till att allt fortfarande är konfigurerat och fungerar som det ska. Mer information finns i artikeln [Konfigurera SPF och DKIM för din e-postleverans](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability).
* Granska och rensa Marketo-databasen genom att rensa inaktiva/ogiltiga poster. Detta ökar chanserna att era marksändningar hamnar i inkorgen på era mest säljfärdiga leads. Mer information finns i artikeln [Hälsokontroll för Marketo-databaser och Så här håller du den ren](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563).
* Bekräfta att dina teammedlemmar har rätt behörigheter för att utföra uppgifter och förhindra oavsiktlig åtkomst eller ändringar av e-postmeddelanden. Oavsett om du gör ändringar via **[!UICONTROL Admin]** eller via **[!UICONTROL Admin Console]** så har vi det du behöver. Läs artikeln [Hantera användarroller och behörigheter](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions).
* Granska era Launchpad-integreringar för att säkerställa korrekt autentisering och åtgärda eventuella fel innan de används. Se artikeln [Marketo Developer Guide: Authentication](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication).

## Bästa praxis

Effektiviteten börjar med att förstå exakt hur Marketo prioriterar och bearbetar kampanjer. Ge era kampanjer snabbhet med dessa optimeringstips.

* Det är viktigt att förstå hur Marketo prioriterar behandlingen av kampanjflödessteg för att undvika att oavsiktligt försena e-postmeddelanden med brådskande eller hög prioritet. Se artikeln [How Campaign Processing Works](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Med hjälp av smart listlogik kan ni se till att era kampanjer körs snabbt och med högsta prestanda. Läs artikeln [Best Practices for Smart Lists](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists).
* **[!UICONTROL Head Start]** eller **[!UICONTROL Recipient Time Zone]** kan börja skapa e-postmeddelanden innan du skickar dem, minska fördröjningar och ge ytterligare förberedelsetid för kvalificerande leads med högresurslogik. Mer information finns i artiklarna [Head Start for Email Programs](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs) och [Schedule Email Programs with Recipient Time Zone](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone) .
* Kampanjen är aktiv och leads flödar igenom, och sedan märker du ett misstag med flödessteg. Det är frestande att laga med en snabb justering, men om du är medveten om vad som händer när du ändrar ett live-väntesteg eller ändrar ordning på dina flöden kan du undvika en massa problem och rensa upp senare. Se artikeln [Redigera kampanjflöde med medlemmar i väntesteg](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

## Testa och validera

Innan du trycker på **[!UICONTROL Send]** måste du se till att dina e-postmeddelanden ser ut och fungerar exakt som de ska.

* Marketo erbjuder flera olika sätt att testa hur ett e-postmeddelande ser ut för att säkerställa att det ser ut exakt som du tänkt dig.
   * Använd funktionen **[!UICONTROL Preview]** för att kontrollera att ditt dynamiska innehåll och dina token återges korrekt genom att förhandsgranska med segmentering eller enskilda leads. Se artikeln [Förhandsgranska ett e-postmeddelande med dynamiskt innehåll](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content).
   * Skicka ett e-postmeddelande till testposterna snabbt och enkelt för att se hur e-postmeddelandet ser ut på olika klienter/enheter. Se artikeln [Kör ett enda flödessteg från en smart lista](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list).
   * För [!DNL Litmus]-användare är det nu enklare än någonsin att integrera ditt konto och initiera återgivningstester direkt från e-postredigeraren. Se artikeln [Testa e-poståtergivning med  [!DNL Litmus]](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering).
* Ta en titt på rapportfunktionen för skräppost, som är integrerad med [!DNL SpamAssassin], för att granska ditt e-postinnehåll och tilldela ett poängvärde för hur sannolikt det är att det kommer att gå till inkorgen eller markeras som *spam*. Se artikeln [Skicka skräppostrapport](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report).
* Håll ett öga på [!UICONTROL Campaign Queue] för att verifiera att era kampanjer bearbetas och prioriterar brådskande objekt korrekt. Se [Körs min kampanj?](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662) artikel.

## Effektivisera supportupplevelsen

När något går fel är snabbheten viktig och Marketo Support är här för att hjälpa dig! Inkludera dessa uppgifter i ditt supportärende för att undvika fram och tillbaka och hjälpa vårt team att arbeta för en snabbare lösning. Läs artikeln [Best Practices for Working With Marketo Support](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491) (Bästa praxis för arbete med-support).

Med den här guiden kan du vila lite enklare i vetskap om att du börjar från en stark position för att skapa engagemang och konverteringar under det här viktiga fönstret. Insatserna är höga, men du behöver inte vara stressad. Påbörja dina förberedelser idag och gör den här helgen till din mest framgångsrika hittills.

</details>

<details>
<summary><h2 id="workfront" style="display: inline-block;">Beredskapshandbok för helgdagar i Adobe Workfront</h2></summary>

För att förbereda Adobe Workfront för semestersäsongen bör teamen uppdatera supportkontakterna, anpassa sina interna scheman till Adobe, undvika större förändringar under fönstertoppar och proaktivt övervaka automatisering och integreringar för att säkerställa smidiga operationer.

## Förbered för skalning

För att säkerställa en smidig supportupplevelse under helger:

* Granska och uppdatera era auktoriserade supportkontakter i förväg.
* Verifiera att viktiga intressenter är tillgängliga för samarbete med support om allvarliga problem uppstår.
* Om du planerar produkt- eller arbetsflödesändringar under semesterperioden bör du överväga att planera dem före mitten av november eller efter början av januari för bästa vändningstider.
* Skicka interna helgscheman till dina Adobe-kontaktpersoner för att säkerställa att de passar in.

## Testa och validera

Håll dig informerad om Workfront och testa nya funktioner i sandlådemiljöer:

* [Förbered dig för en Adobe Workfront-release](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Workfront versionsinformationsarkiv](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/product-releases)
* [Q1 2025 versionsöversikt](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Workfront Release Webinar Recording](https://experienceleague.adobe.com/en/docs/events/workfront-recordings/releases/25-1-release-webinar)

## Bästa praxis

* Proaktiv planering: Identifiera eventuella systemberoenden eller schemalagda automatiseringar som kan påverkas av interna tidplaner.
* Kontinuerlig kommunikation: Håll dina interna team och Adobe Support informerade om planerat underhåll eller viktiga händelser.
* Använd kontrollpaneler: Övervaka viktiga integreringar och automatiseringar för att upptäcka tidiga tecken på prestandaproblem.
* Eskalera tidigt: Om du förutser eller observerar en försämring av tjänsten ska du öppna en supportanmälan omedelbart - vänta inte på att den ska bli kritisk.

Genom att planera i förväg, upprätthålla tydlig kommunikation och eskalera problem tidigt kan man minimera störningarna och säkerställa att Workfront fortsätter att stödja viktiga arbetsflöden under semesterperioden.

</details>

<details>
<summary><h2 id="campaign" style="display: inline-block;">Beredskapshandbok för helgdagar i Adobe Campaign</h2></summary>

För att förbereda Adobe Campaign för beredskap inför semester bör teamen proaktivt validera leveransinställningarna, optimera målgruppssegmentering och meddelandefrekvens, säkra infrastrukturen och testa kanalövergripande kampanjsamordning för att hantera säsongsrelaterade volymer och engagemangspikar effektivt.

## Experttips som får dina semesterkampanjer att sticka ut

Precis som det aldrig är för tidigt att börja handla på semester är det aldrig för tidigt att börja planera för en verkligt framgångsrik kampanj för semestermarknadsföring. Med Adobe Campaign kan ni utforma, planera och genomföra kampanjer som får alla era helgdagar att komma till rätta. Men vet ni alla tips för att köra kampanjer som kommer att avsluta året med en bang? Kolla in den här videon, [Experttips för att få dina semesterkampanjer att sticka ut](https://experienceleague.adobe.com/en/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03), där du diskuterar god praxis för leverans och utförande och visar hur du gör allt i Adobe Campaign.

## Överväganden och förberedelser inför semesterperioden

Den här videon, [Adobe Campaign: Readiness - Considerations and Preparations for the Holiday Period](https://helpx.adobe.com/customer-care-office-hours/campaign/campaign-holiday-readiness.html), omfattar:

* Engaging the Campaign community
* Leverans - Överväganden för helger och annat!
* Tekniska rekommendationer för Adobe Campaign Classic (ACC) och Adobe Campaign Standard (ACS)

För att Adobe Campaign ska vara redo för högsäsong bör man slutföra leveranskontrollerna, validera kampanjkonfigurationer och se till att det finns skalbar infrastruktur och flerkanalssamordning för att kunna genomföra stora volymer, tidskänsliga kampanjer under helger.

</details>

<details>
<summary><h2 id="analytics" style="display: inline-block;">Beredskapshandbok för helgdagar i Adobe Analytics</h2></summary>

När semestersäsongen närmar sig bör organisationer som använder Adobe Analytics vidta proaktiva åtgärder för att säkerställa datakvalitet, plattformsprestanda och rapporttillförlitlighet under trafiktoppar. Adobe tillhandahåller flera resurser och metodtips som hjälper team att förbereda sig effektivt.

## Förutspå trafik

För att säkerställa korrekt maskinvaruallokering och systemrespons rekommenderar Adobe att du skickar **toppvolymer för träffar/anrop per timme och dag** i förväg.

* Kontrollera [Ledtider för trafiktoppschemaläggning och maskinvaruallokering](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times) eftersom det är viktigt att förstå hur snabbt data blir tillgängliga för beslutsfattande i realtid under stora volymer.

* Lär dig vad som påverkar datatillgänglighet och fördröjning i Adobe Analytics i [Adobe Analytics datatlatenöversikt](https://experienceleague.adobe.com/en/docs/analytics/technotes/latency), inklusive oväntade trafiktoppar och maskinvaruproblem, och upptäck rekommenderade strategier för att minska fördröjningar av data.

## Bästa praxis

För team som använder dataflöden för att exportera råanalysdata tillhandahåller Adobe vägledning om hur man optimerar flödeskonfigurationer och undviker vanliga fallgropar.

* [Bästa tillvägagångssätt för dataflöden från Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

För att få snabb och tillförlitlig rapportering under helger rekommenderar Adobe:

* [Optimera Analysis Workspace prestanda](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Felsökning och metodtips för Report Builder: Rekommendationer för optimering av begäranden](https://experienceleague.adobe.com/en/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Handbok för analyskomponenter: Schemalagd rapportkö](https://experienceleague.adobe.com/en/docs/analytics/components/scheduled-reports-admin)

## Planering av underhåll av semester

Adobe använder vanligtvis **underhållsundantag** under högbelastade helgperioder för att säkerställa oavbruten service. Kunderna bör övervaka Adobe releaser- och underhållsscheman via Experience League och samordna med sina Adobe kontoteam för supportplanering.

Genom att följa dessa riktlinjer och dra nytta av Adobe offentliga dokumentation kan man säkerställa att Adobe Analytics implementering är robust, responsiv och redo för helgtidens krav.

</details>

<details>
<summary><h2 id="target" style="display: inline-block;">Beredskapshandbok för helgdagar i Adobe Target</h2></summary>

Semestersäsongen ger spännande möjligheter till engagemang, men den har också utmaningar som trafiktoppar och ökad efterfrågan på personaliseringssystem. Vi har sammanställt viktiga rekommendationer för att säkerställa att Adobe Target implementering är klar, så att ni kan leverera sömlösa upplevelser under den här kritiska perioden.

## Förutsägelseefterfrågan

Börja med att förutse trafiktoppar på 20-50 % eller mer och validera att infrastrukturen kan hantera belastningen. Prognostisera aktivitet och datavolymer i Adobe Target, Analytics och AEP för att undvika överraskningar.

Det är också viktigt att identifiera verksamhetskritiska resor - till exempel utcheckning, produktrekommendationer och kampanjerbjudanden - så att personaliseringen fokuserar där de är som mest viktiga.

Mer information finns i [Bästa tillvägagångssätt för optimering med Adobe Target](https://experienceleague.adobe.com/en/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization).

## Förbered för skalning

* Planera för ökad trafik på webbplatsen och mobila enheter och informera Target-supportteamet om att öka serverkapaciteten för att undvika blockerade samtal.
* För varje belastnings-/ritstiftstest ska Target support-teamet informeras i förväg.
* Uppgradera till de senaste versionerna av `at.js`/leverans-API.
* Frys icke-kritiska ändringar - förbered dig för reservupplevelser.
* Justera support- och eskaleringsprocesserna och aktivera proaktiva aviseringar.

## Testa och validera

Verifiera innehållsleverans med [QA-länkar](https://experienceleague.adobe.com/en/docs/target/using/activities/activity-qa/activity-qa) för att bekräfta att allt fungerar som förväntat. Använd växeln **[!UICONTROL Match audience rules to see experiences]** för att kontrollera att rätt målgrupp kvalificerar för aktiviteten som du testar. Dubbelkontrollera att din **[!UICONTROL Goal Metric]**-konfiguration är justerad efter aktivitetens **[!UICONTROL Objective]**. Och ha alltid en backupplan klar - bara ifall det skulle behövas.

## Bästa praxis

Behåll implementeringen inom [Adobe Target-gränser](https://experienceleague.adobe.com/en/docs/target/using/troubleshoot/target-limits) och verifiera [GDPR- och CCPA-kompatibilitet](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation) innan du startar programmet. Underhåll färre än 100 aktiva aktiviteter och arkivera äldre för att effektivisera arbetet. Dra nytta av **[!UICONTROL Auto-Allocate]**/**[!UICONTROL Auto-Target]** för AI-driven optimering. Upprätta återställningsplaner och kontrollpaneler för övervakning i realtid.

## Säkerhet och styrning

Innan ni personaliserar upplevelserna måste ni bekräfta att ni godkänner villkoren i GDPR och CCPA. Undvik att lagra personligt identifierbar information (PII) i profilparametrar och validera API-säkerheten för att skydda kunddata.

</details>
