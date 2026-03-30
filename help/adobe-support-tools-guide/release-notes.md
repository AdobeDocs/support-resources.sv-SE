---
title: Versionsinformation om Experience League support
description: Den senaste versionsinformationen om Experience League support.
feature: Release Notes
source-git-commit: 25bfd2450594c3fbb361cb80fe16e1a438f73b89
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---


# Versionsinformation om Experience League support

Versionsinformationen innehåller uppdateringar av Experience League support och innehåller:

![Nya](../adobe-support-tools-guide/assets/new.svg) nya funktioner
![Korrigera &#x200B;](../adobe-support-tools-guide/assets/fix.svg) Korrigeringar och förbättringar
![Fel](../adobe-support-tools-guide/assets/bug.svg) Kända fel

## 30 mars 2026 - Förbättrat ansökningsformulär

![Nytt](../adobe-support-tools-guide/assets/new.svg) Ärendeformuläret är organiserat i ett guidat flöde som hjälper användarna att förstå vilken information som krävs i varje steg:

- [!UICONTROL Product Selection]
- [!UICONTROL Problem Description]
- [!UICONTROL System Information]
- [!UICONTROL Priority and Business Impact]
- [!UICONTROL Contact Information & Watchers List]
- [!UICONTROL Review and Submit]

![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till automatisk titelgenerering baserat på **[!UICONTROL Issue Description]**, vilket gör att titeln kan genereras automatiskt samtidigt som användaren fortfarande kan redigera den innan ärendet skickas.

![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till ett **[!UICONTROL "Is the issue reproducible?"]**-alternativ för att förbättra felsökningen. Om användare väljer **[!UICONTROL Yes]** uppmanas de att ange de åtgärder som har vidtagits för att återskapa problemet. Om *Nej* är markerat kan användare fortsätta med ärendeöverföringen.

![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till ett alternativ som anger om några senaste ändringar har gjorts i miljön eller instansen. Om **[!UICONTROL Yes]** väljs uppmanas användarna att ange ytterligare information om ändringarna.

![Nytt](../adobe-support-tools-guide/assets/new.svg) **Ytterligare [!UICONTROL Environment Context] fält** har lagts till för berättigade produkter för att hämta viktig information:

- **Marketo**
   - MUNCHKIN ID
- **Adobe Target**
   - Aktivitetsnamn
   - Webbplats-URL(egenskapsnamn för taggar)
- **Adobe Analytics**
   - RSID
   - Webbplats-URL(taggegenskapsnamn) / cURL
   - Workspace Shortlink
- **Adobe Journey Optimizer (AJO)**
   - Resurs-ID eller URL/kampanj-ID eller URL/kanal-ID eller URL/Offer Decisioning-ID eller URL
   - Exempel på profil
   - Namn på sandlåda
- **Real-Time Customer Data Platform (RTCDP)**
   - Berört komponent-ID (mål-ID/målgrupps-ID/datauppsättnings-ID/dataflödes-ID/sammanfogningsprincip-ID/schema-ID/Source-ID/batch-ID)
   - Exempel på profil
   - Namn på sandlåda
- **Adobe Experience Platform (AEP)**
   - Berört komponent-ID (mål-ID/målgrupps-ID/datauppsättnings-ID/dataflödes-ID/sammanfogningsprincip-ID/schema-ID/Source-ID/batch-ID)
   - Exempel på profil
   - Namn på sandlåda
- **Customer Journey Analytics (CJA)**
   - Workspace projekt-URL
   - Anslutnings-ID / Felmeddelande / Kod
   - Datavy-ID

![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till en **AI-driven[!UICONTROL Recommendations Panel]** som visar användbar vägledning utan att störa skapandet av ärendet.

![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till ett **[!UICONTROL Review Summary]**-steg för att ge en samlad vy över all angiven information och tillåta användare att:

- Granska ärendeinformationen på ett och samma ställe
- Gå tillbaka till föregående steg för att göra ändringar
- Återgå till sammanfattningen utan att förlora förloppet

![Åtgärda](../adobe-support-tools-guide/assets/fix.svg) Fältet Ärendebeskrivning har bytt namn till *[!UICONTROL "Please describe the issue"]* för att bli tydligare.

![Korrigera](../adobe-support-tools-guide/assets/fix.svg) asterisk (*) har lagts till som obligatoriska fältindikatorer för att säkerställa fullständighet och minska antalet inskickningsfel.

## 18 mars 2026 - Utökning av funktionen Begär återanrop

Experience League erbjuder nu ett alternativ för att begära återanrop, vilket möjliggör självbetjäning för schemaläggning av webbmöten med möjlighet till skärmdelning för snabbare problemlösning.
- Den här funktionen är tillgänglig för Adobe Experience Manager, Campaign och Workfront.
- Kunderna kan boka möten när det passar och få inbjudningar direkt.
- I Adobe Experience Manager P1-fall säkerställer direkta återanrop ett snabbare engagemang under allvarliga problem, vilket minimerar driftavbrott och påverkan på verksamheten.
