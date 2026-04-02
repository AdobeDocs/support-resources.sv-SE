---
title: Hantera policymallar i Global Admin Console
description: Läs om hur globala administratörer kan tillämpa principmallar på alla underordnade organisationer, direkt eller indirekt från den organisation där de lagras i Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cf30f2a656ccb28b678ea6fcd8e4d56d7c8a8fb4
workflow-type: tm+mt
source-wordcount: 655
ht-degree: 0%

---

# Hantera policymallar i Global Admin Console

**Gäller för:** Enterprise

Läs om hur globala administratörer kan tillämpa principmallar på alla underordnade organisationer, direkt eller indirekt från den organisation där de lagras i Global Admin Console.

>[!NOTE]
>
>I [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) väljer du en organisation som ska redigeras och navigerar till fliken **Principmallar** för att effektivisera konfigurationen och underlätta konsekvent policyhantering i olika organisationer.
>
> [Logga in på Global Admin Console](https://global-admin-console.adobe.com/)

## Hur policymallar fungerar

Policymallar lagras med en organisation och är synliga för alla globala administratörer i den organisationen. När posterna i policymallen har tillämpats anges de individuellt i respektive organisation. När en principmall tillämpas på en organisation används varje post i principmallen på organisationens profiler, vilket ersätter befintliga principvärden.

### Låst principbeteende

Uppdateringar av låsta principer utförs bara om användaren som utför uppdateringen är en global administratör för organisationen som anges av ikonen **[!UICONTROL Locked By]** för den princip som uppdateras.

Om användaren som använder mallen har behörighet att låsa upp profilen, hämtar principen värdena från den mall som används (låst eller olåst). Om mallen anger att låset ska vara kvar som det är, förblir värdet för låset i profilen detsamma som tidigare.

### Viktigt att notera när du sparar

>[!NOTE]
>
>Till skillnad från andra ändringar i Global Admin Console börjar ändringar i principmallar gälla omedelbart utan att du behöver gå igenom **[!UICONTROL Review Pending Changes - Submit]**-processen. Om du vill implementera väntande ändringar i organisationer där principmallen används, måste du [skicka](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Skapa en principmall

1. I [Global Admin Console](https://global-admin-console.adobe.com/) väljer du en organisation att redigera och går sedan till fliken **[!UICONTROL Policy Templates]**.
1. Välj **[!UICONTROL Create Template]**.<br>
   ![Pic1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. Ange principmallens **[!UICONTROL Create Policy Template]** namn **och** beskrivning **i dialogrutan**.<br>Principmallens namn får innehålla högst 100 tecken.
1. Välj de profiler som ska ingå i mallen.
1. Ange värden för de valda profilerna (se [Ange principvärden](#setting-policy-values) nedan).
1. Välj **Spara**.

### Ställa in principvärden {#setting-policy-values}

Konfigurera två inställningar för varje princip som ingår i mallen:

* **Tillåten/inte tillåten:** Ange det önskade värdet för skjutreglaget. Läs mer om [principinformation](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#policy-details).
* **Lås värde:** Ändra principens låsstatus med något av följande alternativ:
   * **Lås** - Principen kommer att låsas när mallen har tillämpats.
   * **Lås upp** - Principen låses upp när mallen har tillämpats.
   * **Behåll som** - Principens låsstatus ändras inte innan mallen tillämpades.<br>
     ![Pic2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## Tillämpa en mall på organisationer

1. I [Global Admin Console](https://global-admin-console.adobe.com/) väljer du en organisation att redigera och går sedan till fliken **[!UICONTROL Policy Templates]**.
1. Välj ikonen **[!UICONTROL More Options]** ![Fler alternativ](./assets/manage-product-profiles_more-options.png) för den aktuella principmallen och välj **[!UICONTROL Apply template to organization]**.<br>
   ![Pic3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. Välj de organisationer som du vill tillämpa mallen på. Du kan välja flera organisationer.<br>
   ![Pic4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. Välj **[!UICONTROL Apply template]**.
1. Om du vill implementera väntande ändringar i organisationer där principmallen används väljer du **[!UICONTROL Review Pending Changes]**. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

Om alla principvärden i de organisationer som du har valt redan matchar värdena i mallen visas ett meddelande om att inga ändringar har gjorts. Dessutom är **[!UICONTROL Review Pending Changes]** inte aktiverat om det inte finns några andra väntande redigeringar.

## Redigera en mall

1. I [Global Admin Console](https://global-admin-console.adobe.com/) väljer du en organisation att redigera och går sedan till fliken **[!UICONTROL Policy Templates]**.
1. Välj ikonen **[!UICONTROL More Options]** ![Fler alternativ](./assets/manage-product-profiles_more-options.png) för den aktuella mallen och välj **[!UICONTROL Edit template]**.<br>
   ![Pic5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. Uppdatera principmallen och välj **[!UICONTROL Update Now]**.
1. Om du vill implementera väntande ändringar i organisationer där principmallen används väljer du **[!UICONTROL Review Pending Changes]**. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Ta bort en mall

1. I [Global Admin Console](https://global-admin-console.adobe.com/) väljer du en organisation att redigera och går sedan till fliken **[!UICONTROL Policy Templates]**.
1. Välj ikonen **[!UICONTROL More Options]** ![Fler alternativ](./assets/manage-product-profiles_more-options.png) för den aktuella mallen och välj **[!UICONTROL Delete Template]**.<br>
   ![PIC6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. Välj *Ja* i dialogrutan som visas.
