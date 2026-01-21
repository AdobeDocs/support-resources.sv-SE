---
title: Versionsinformation om nytt EXL-formulär
description: Den senaste versionsinformationen för EXL-ärendeformuläret.
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 4%

---


# Versionsinformation om nytt EXL-formulär

Den nya funktionen för att skapa ärenden innehåller ett uppdaterat formulär som utformats för att effektivisera problemlösningen och som innehåller:

![Nytt](../adobe-support-tools-guide/assets/new.svg) – Nya funktioner
![Korrigering](../adobe-support-tools-guide/assets/fix.svg) – Korrigeringar och förbättringar
![Fel](../adobe-support-tools-guide/assets/bug.svg) – Kända problem

## Version 1.0 - Formulär för framtagning av utökat ärende

*15 januari 2026*

![Nytt](../adobe-support-tools-guide/assets/new.svg) Ärendeformuläret är organiserat i ett guidat flöde, vilket hjälper användarna att förstå vilken information som krävs i varje steg:

- [!UICONTROL Product Selection]
- [!UICONTROL Issue Details]
- [!UICONTROL System Information]
- [!UICONTROL Impact]
- [!UICONTROL Contact Information]
- [!UICONTROL Review and Submit]

![Nytt](../adobe-support-tools-guide/assets/new.svg) **Nytt [!UICONTROL Steps to Reproduce] fält** har lagts till för att samla in åtgärdbar information och snabba upp felsökningen.

![Nytt](../adobe-support-tools-guide/assets/new.svg) **Ytterligare [!UICONTROL Environment Context] fält** har lagts till för berättigade produkter för att hämta viktig information:

- **Marketo**
   - MUNCHKIN ID
- **Adobe Target**
   - Aktivitetsnamn
   - Webbplats-URL (taggegenskapsnamn)/VAR- eller Assurance-logg
- **Adobe Analytics**
   - RSID
   - Webbplats-URL (taggegenskapsnamn)/VU- eller Assurance-logg/cURL/felsökningslogg
   - Workspace-genväg
- **Adobe Journey Optimizer (AJO)**
   - Rese-ID eller rese-URL
   - Exempel på profil
- **Real-Time Customer Data Platform (RTCDP)**
   - Berört komponent-ID (mål-ID, profil-ID, målgrupps-ID, datauppsättnings-ID eller dataflödes-ID)
   - HAR-fil/Assurance-loggar
- **Customer Journey Analytics (CJA)**
   - Workspace-projekt
   - Namn på taggegenskap


![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till en **AI-driven[!UICONTROL Recommendations Panel]** som visar användbar vägledning utan att störa skapandet av ärendet.

![Nytt](../adobe-support-tools-guide/assets/new.svg) har lagt till ett [!UICONTROL Review Summary]-steg för att ge en samlad vy över all angiven information och tillåta användare att:

- Granska ärendeinformationen på ett och samma ställe
- Gå tillbaka till föregående steg för att göra ändringar
- Återgå till sammanfattningen utan att förlora förloppet

![Åtgärda](../adobe-support-tools-guide/assets/fix.svg) Fältet för skiftlägesbeskrivning har bytt namn till *[!UICONTROL "Please describe the issue"]* för att bli tydligare.

![Korrigera](../adobe-support-tools-guide/assets/fix.svg) asterisk (*) har lagts till som obligatoriska fältindikatorer för att säkerställa fullständighet och minska antalet inskickningsfel.
