---
title: Migrera befintliga användare till Adobe Admin Console
description: Vägledning för organisationer som använder Adobe prenumerationslicenser och behöver migrera befintliga användare i Admin Console till ett annat inköpsprogram eller licenstyp.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 42ab19551ba5c70712245236ffc7daf687486fb2
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# Migrera befintliga användare till Adobe Admin Console

Gäller företag och team.

Det här dokumentet är avsett för organisationer med befintliga Creative Cloud-, Document Cloud- och Acrobat-licenser via ett Enterprise Term License Agreement (ETLA) eller Value Incentive Plan (VIP) som migrerar till ett annat inköpsprogram eller licenstyp.

>[!NOTE]
>
>Om du är i Nordamerika och behöver hjälp med förnyelsen av ditt årsavtal för Adobe VIP från din Account Manager kan du skicka ett e-postmeddelande till **renewalhelp@adobe.com** så kontaktar vi dig inom kort.

För att undvika avbrott i slutanvändarnas produktåtkomst tilldelar du licenser i Adobe Admin Console innan den befintliga prenumerationsperioden för VIP löper ut.

* För ETLA-kunder kan det ta minst 30 dagar innan produkterna överlappar varandra. Slutför migreringen före brytdatumet så att användarna har tillgång till Adobe program och tjänster. Mer information om förfallodatum för ETLA-kontrakt finns i [Automatiska förfallofaser för ETLA-kontrakt](https://helpx.adobe.com/enterprise/using/contract-expiry.html).
* För VIP-kunder kan du köpa licenser före årsdatumet och tilldela licenser innan förnyelseperioden för din nuvarande VIP-period avslutas.
* CLP- eller TLP-kunder kan migrera från serialiserade Acrobat eller Creative Suite till personliga användarlicenser med migreringsinstruktionerna i [Licensiering](https://helpx.adobe.com/enterprise/using/licensing.html).

>[!NOTE]
>
>Om organisationens licenstyp ändras måste slutanvändarna logga ut från alla Adobe-produkter eller -tjänster och logga in igen med samma inloggningsuppgifter.
>
>För datorprodukter som Photoshop, Acrobat och Illustrator använder du alternativen Logga ut och Logga in på Hjälp-menyn. På Adobe.com använder du ikonen i det övre högra hörnet för att logga ut och sedan logga in igen.

## Snabbtilldelning av licenser (VIP till VIP)

Nuvarande VIP-medlemmar som köpt Creative Cloud for enterprise eller Acrobat (for enterprise) via VIP kan snabbt tilldela licenser under förnyelseperioden med hjälp av Snabbtilldelning av licenser. Berättigade kunder uppfyller följande kriterier:

* Produkterna är desamma

   1. Förnyelseperioden är öppen (30 dagar före eller efter brytdatumet för VIP-avtalet).
   2. Enterprise-produkterna i beställningen är nya SKU:er som motsvarar teamversionerna under den pågående perioden.
   3. Antalet beställda enterprise-licenser är större än eller lika med det befintliga antalet team-licenser.

* Produkterna är mer prisvärda

   1. Förnyelseperioden är öppen.
   2. Företagsprodukterna i beställningen är nya SKU:er som är mer prisvärda produkter än teamprodukterna i den pågående perioden.
   3. Antalet beställda enterprise-licenser är större än eller lika med det befintliga antalet team-licenser.

* Snabbtilldelning av licenser är inte tillgängligt när

   * Antalet företagslicenser i beställningen är mindre än antalet befintliga teamlicenser.
   * Ordern avser större företagsprodukter, men den beställda licenskvantiteten är mindre än den befintliga teamlicenskvantiteten.
   * I beställningen blandas team- och företagsprodukter, oavsett kvantitet.
   * Kunden har redan köpt team- och företagsprodukter före förnyelseperioden.
   * förnyelse-SKU:er för företag används för den nya Enterprise-ordern.
   * Företagets produktbeställning avser ett annat avtalsnummer för VIP.
   * Aktuella teamprodukter innehåller objekt som inte har några företagsversioner.

När Adobe har bearbetat din enterprise-inköpsorder får du ett bekräftelsemeddelande via e-post med instruktioner, inklusive den dag du måste överföra användare från team-licenser till enterprise-licenser i Admin Console innan de förlorar åtkomsten.

I Admin Console uppmanas du att tilldela licenser med Snabbtilldelning av licenser:

1. Bekräfta antalet licenser som ska tilldelas.

   ![Överför licenser](assets/migrate-transfer-licenses.png)

2. Bekräfta att de otilldelade teamproduktlicenserna matchar de enterprise-licenser som tilldelas.

3. Du får ett e-postmeddelande när processen är klar.

   ![Licenstilldelningsbekräftelse](assets/migrate-license-assignment.png)

Hämta [resultatrapporten](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) i Admin Console för att bekräfta att alla licenser har tilldelats. Om du är klar före datumet i bekräftelsemeddelandet ska slutanvändarna inte drabbas av några avbrott i tjänsten.

Schemalägg ett :1 introduktionssamtal med en Adobe-introduktionsspecialist (om du inte redan har det) för att lära dig mer om Admin Console, inklusive [administrativa roller](https://helpx.adobe.com/enterprise/using/admin-roles.html) och [identitet](https://helpx.adobe.com/enterprise/using/identity.html).

>[!NOTE]
>
>Snabbtilldelning av licenser migrerar inte användare med väntande inbjudningar i Team Admin Console.

## Grupptilldelning av licenser (VIP till VIP)

Tilldela licenser med en gruppåtgärd med hjälp av en CSV-mall från [!DNL Admin Console]. Använd den här metoden när:

* Du är en VIP-kund som inte uppfyller kraven för Snabbtilldelning av licenser, eller
* Du måste tilldela licenser utanför förnyelseperioden.

1. När du har tillgång till [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) och dina licenser har lagts till går du till **[!UICONTROL Users]** > **[!UICONTROL Users]**.
2. Klicka på ![Fler alternativ-menyn](assets/migrate-more-options.png) i det övre högra hörnet på sidan **[!UICONTROL Users]** och välj sedan **[!UICONTROL Edit User Details by CSV]**.
3. Klicka på **[!UICONTROL Edit Users by CSV]** i dialogrutan **[!UICONTROL Download CSV template]** och välj **[!UICONTROL Current user list]**.

   ![Redigera användare via CSV](assets/migrate-edit-users-by-csv.png)

   Fältbeskrivningar i den hämtade filen finns i [CSV-filformat](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header).
4. Lägg till licenstilldelningar i CSV-filen, dra den uppdaterade filen till dialogrutan **[!UICONTROL Edit Users by CSV]** och klicka på **[!UICONTROL Upload]**. Du får ett e-postmeddelande när åtgärden har slutförts.

   ![Användarredigering slutförd](assets/migrate-user-edit-complete.png)

Hämta [resultatrapporten](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) för att validera tilldelningar. Schemalägg sedan introduktionen med en Adobe-introduktionsspecialist för att få veta mer om [administrativa roller](https://helpx.adobe.com/enterprise/using/admin-roles.html) och [identitet](https://helpx.adobe.com/enterprise/using/identity.html).

## Grupptilldelning av licenser (VIP till ETLA)

Om du har en VIP-prenumeration och flyttar användare till ETLA ska du använda det här bulkflödet:

1. Logga in på [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) och öppna organisationen som innehåller dina VIP-användare.
2. Gå till **[!UICONTROL Users]** > **[!UICONTROL Users]**.
3. Klicka på ![Fler alternativ-menyn](assets/migrate-more-options.png) i det övre högra hörnet och välj sedan **[!UICONTROL Export users list to CSV]**.
4. Öppna den ETLA-organisation där du vill att användarna ska vara.
5. Gå till **[!UICONTROL Users]** > **[!UICONTROL Users]**.
6. Klicka på **[!UICONTROL Add Users by CSV]**.
7. Klicka på **[!UICONTROL Download CSV template]** och lägg sedan till VIP-användare från den CSV-fil som du exporterade i steg 3.
8. Överför den uppdaterade CSV-filen.

Du får ett e-postmeddelande när användare läggs till i ETLA.

![Användare har lagts till efter migrering från VIP till ETLA](assets/migrate-users-added-vip-etla.png)

Hämta [resultatrapporten](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) för att validera tilldelningar. Schemalägg introduktion med en Adobe-introduktionsspecialist för [administrativa roller](https://helpx.adobe.com/enterprise/using/admin-roles.html) och [identitet](https://helpx.adobe.com/enterprise/using/identity.html).

Information om problem med massöverföring finns i [Felsöka massöverföring av användare](https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).

## Grupptilldelning av licenser (ETLA till VIP)

Om du prenumererar på ETLA och flyttar användare till VIP:

1. Logga in på [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) och öppna organisationen som innehåller dina ETLA-användare.
2. Gå till **[!UICONTROL Users]** > **[!UICONTROL Users]**.
3. Klicka på ![Fler alternativ-menyn](assets/migrate-more-options.png) i det övre högra hörnet och välj sedan **[!UICONTROL Export users list to CSV]**.

   ![Menyn Exportera användarlista](assets/migrate-export-user-list.png)

4. Öppna den VIP-organisation där du vill att användarna ska vara.
5. Gå till **[!UICONTROL Users]** > **[!UICONTROL Users]**.
6. Klicka på **[!UICONTROL Add Users by CSV]**.
7. Klicka på **[!UICONTROL Download CSV template]** och lägg sedan till ETLA-användare från den CSV-fil som du exporterade i steg 3.
8. Överför den uppdaterade CSV-filen.

Du får ett e-postmeddelande när användare läggs till i VIP.

![Användare har lagts till efter migrering från ETLA till VIP](assets/migrate-users-added-etla-vip.png)

Hämta [resultatrapporten](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) för att validera tilldelningar. Schemalägg introduktion med en Adobe-introduktionsspecialist för [administrativa roller](https://helpx.adobe.com/enterprise/using/admin-roles.html) och [identitet](https://helpx.adobe.com/enterprise/using/identity.html).

Information om problem med massöverföring finns i [Felsöka massöverföring av användare](https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).


