---
title: Tilldela produkter till underordnade organisationer som använder Global Admin Console
description: Läs om hur globala administratörer kan distribuera resurser till underordnade organisationer, vilket möjliggör effektiv resurshantering och användartilldelning inom varje organisation.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: f14254a77ce3620208389b36222f89be8f9d15b6
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# Tilldela produkter till underordnade organisationer som använder Global Admin Console

Gäller företag.

Läs om hur globala administratörer kan distribuera resurser till underordnade organisationer, vilket möjliggör effektiv resurshantering och användartilldelning inom varje organisation.

Gå till fliken [&#x200B; i &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)Global Admin Console **[!UICONTROL Product Allocation]** och välj sedan en produkt som ska tilldelas underordnade organisationer.

Logga in på [Global Admin Console](https://global-admin-console.adobe.com).

>[!NOTE]
>
>**[!UICONTROL Product Allocation]** är bara tillgängligt för Enterprise Term License Agreement (ETLA)-kontrakt.

En del av distributionen och administreringen av Adobe-produkter i olika organisationer är att dela upp inköpta resurser i resursallokeringar i de organisationer som ska hanteras. Du kan distribuera administreringen av produktresurser till andra organisationer genom att ge alla eller vissa resurser. Alla resurser för alla produkter kan inte allokeras. Vissa produkter kan inte distribueras till andra organisationer. Sådana produkter visas på fliken **[!UICONTROL Product Allocation]** men har inga kontroller för att lägga till dem i andra organisationer.

>[!WARNING]
>
>Du kan inte tilldela produkter till en underordnad organisation från ett kontrakt som har **gått ut** eller om organisationen har statusen **inaktiv**. Läs mer om [kontraktets förfallodatum](https://helpx.adobe.com/enterprise/using/contract-expiry.html) eller kontakta företagets administratör för hjälp med att förhindra att användare i den underordnade organisationen förlorar åtkomst till sina Adobe-program och -tjänster.

## Sammansatt lagring

Detta gäller kunder som har en lagringflik i sin Admin Console. Om du inte ser någon lagringsflik har din Admin Console ännu inte uppdaterats till Enterprise Storage Model. När din organisation har migrerats ser du följande ändringar:

- Globala administratörer får åtkomst till lagringskvot och -användning i hela hierarkin och kan tilldela lagring till organisationer via fliken **[!UICONTROL Product Allocation]** i [Global Admin Console](https://adminconsole.adobe.com/).
- Systemadministratörer och lagringsadministratörer har fullständig kontroll över och synlighet för lagring i hela organisationen. De kan spåra och hantera lagring på fliken **[!UICONTROL Storage]** i [Adobe Admin Console](https://adminconsole.adobe.com/).

Tack vare uppdateringarna av Adobe Creative Cloud lagringsutrymme är lagringskvoterna flexibla för slutanvändarna, upp till den lagringsmängd som köpts av organisationen. [Läs mer](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html).

## Tilldela produkter

Fliken **[!UICONTROL Product Allocation]** i Global Admin Console visar allokeringsenheter för produkter som köpts i hela organisationshierarkin. Som [global administratör](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins) kan du allokera dessa produktresurser till en annan organisation i organisationsträdet och ange allokeringskvantiteten. Som [globalt visningsprogram](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins) kan du visa och exportera data, men inte göra några uppdateringar.

Så här tilldelar du produkter till en organisation:

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com) och gå till **[!UICONTROL Product Allocation]**.
1. Välj en produkt i listrutan för att se hur den tilldelas olika organisationer.\
   Om en organisation inte har produkten visas ikonen **[!UICONTROL Add +]**.

   >[ !Note]
   >
   >Om den underordnade organisationen redan har ett inköpsavtal kan produktallokeringen från den överordnade till den underordnade organisationen vara begränsad. [Läs mer](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. Om du vill tilldela produkten väljer du ikonen **[!UICONTROL Add +]** för den relevanta organisationen.\
   Vissa produkter innehåller mer än en allokeringsbar resurs. I så fall visas flera resurser i dialogrutan och du måste ange värden för varje resurs. Adobe Stock kan till exempel innehålla Adobe Stock Image-krediter och premiumkrediter.
   ![Adobe Stock-bilder](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. Ange produktkvantiteten i dialogrutan som visas.
1. Välj **[!UICONTROL Save]**.
1. Om du vill tillåta eller neka överallokering av en resurs väljer du relevant växlingsknapp.
   ![Överbeläggning](/help/adobe-support-tools-guide/assets/overallocation.png)
1. Välj **[!UICONTROL Review Pending Changes]** när du har allokerat resurser. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Tilldela och distribuera Adobe Acrobat Sign användarlicenser eller transaktioner

Med Global Admin Console kan ni fördela och distribuera Acrobat Sign användarlicenser eller transaktioner i hela organisationshierarkin. Varje organisation i hierarkin som har tilldelats licenser eller transaktioner från Acrobat Sign skapar ett eget separat Acrobat Sign-konto.

- Varje Acrobat Sign-konto som skapas är oberoende och placeras på samma plats vad gäller administration och innehåll.
- Varje Acrobat Sign-konto har ingen kännedom om andra Acrobat Sign-konton (t.ex. i förälder- eller systerorganisationer).

Läs mer om att [hantera Adobe Acrobat Sign i Admin Console](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html).

Om du vill hantera autentiseringstillägg som kunskapsbaserad autentisering (KBA) och telefonautentisering (PA) kontaktar du Adobe representant eller Customer Success Manager.


## Begränsningar för produkttilldelning

Allokering från en överordnad organisation till en underordnad organisation är begränsad i följande fall:

- Om båda organisationerna har olika kontrakt och produkten som du försöker tilldela finns i båda, går det inte att blanda samma erbjudande mellan kontrakt.
- Om båda organisationerna har samma kontrakt kan du begära tillstånd att tilldela produkten genom att kontakta din Adobe-representant eller genom att [skicka in ett supportärende](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html) som anger att **[!UICONTROL Product Allocation]** i Global Admin Console är blockerad.

## Överbeläggning

Som [global administratör](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins) kan du tillåta överallokering av resurser.

En [princip](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies) för allokering som är associerad med produkten och organisationen anger om överallokering är tillåten.

Överbeläggning ger fler produktresurser till en underordnad organisation än vad som är tillgängligt i den överordnade organisationen. Det är användbart när allokeringarna är ungefärliga och administratören inte vill belastas med att resursallokeringarna läggs ihop.
Om överbeläggning är inaktiverat för en produktresurs i en organisation får summan av underordnade bidrag inte överstiga det överordnade anslaget. Begäranden om överallokering av en resurs som är markerad med överallokering inaktiverad utförs inte.
När växlingen för överallokering växlas från aktiverad till inaktiverad måste bidragsvärdena justeras för att eliminera överallokering innan anslagsuppdateringar kan utföras, om det finns en överallokeringssituation i anslagskvantiteterna för en resurs.

![Överbeläggning](/help/adobe-support-tools-guide/assets/overallocation.png)

## Utgångna kontrakt i hierarkin

Du kan inte tilldela produkter till en underordnad organisation från ett ETLA-kontrakt som har gått ut. Banderoller och meddelanden i appen, som följande, på sidorna **[!UICONTROL Overview]** och **[!UICONTROL Product Allocation]** visar tydligt när kontraktet för en eller flera underordnade organisationer kommer att upphöra, har gått ut eller är inaktivt.

![Produktallokering](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !Iviktig]
>
>När ett ETLA-kontrakt som ingår i hierarkin är inaktivt tas produkterna bort från sidorna **[!UICONTROL Overview]** och **[!UICONTROL Product Allocation]**.

[Läs mer om avtalets förfallodatum](https://helpx.adobe.com/enterprise/using/contract-expiry.html) eller kontakta företagets administratör för hjälp med att förhindra att användare i den underordnade organisationen förlorar åtkomst till sina Adobe-appar och -tjänster.
