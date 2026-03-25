---
title: Exportera eller importera organisationsstruktur och produktallokeringar
description: Lär dig hur globala administratörer exporterar och importerar organisationshierarki och produktallokeringsdata i Global Admin Console med JSON, CSV eller XLSX. Gäller Enterprise.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 3220086a-4603-465f-a3e3-194193ca10ba
source-git-commit: 91d79132e11b322fd0ebd77df918be07060595fa
workflow-type: tm+mt
source-wordcount: '4377'
ht-degree: 2%

---

# Exportera eller importera organisationsstruktur och produktallokeringar

**Gäller för:** Enterprise

Läs om hur globala administratörer kan effektivisera organisationen och produkthanteringen med export- och importfunktionerna i Global Admin Console.

Gå till fliken **[!UICONTROL Organizations]** i [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) om du vill exportera eller importera organisationsstrukturen. Gå till fliken **[!UICONTROL Product Allocation]** om du vill se allokeringsdata. Använd ikonen **[!UICONTROL More Options]** **⋮** för att välja export eller import. [Logga in på Global Admin Console](https://global-admin-console.adobe.com).

## Exportera organisationsstrukturen

Som [global administratör](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) kan du exportera organisationshierarkin. Du kan hämta en JSON-, CSV- eller XLSX-representation av hela organisationshierarkin eller en delmängd av den. Du kan sedan använda dessa data för analys eller ändring.

Det exportformat som valts påverkar strukturen för exporterade data:

- CSV-format - Endast en typ av data i taget kan exporteras. När du exporterar produktprofiler i CSV-format kombineras profilerna och resurserna i en tabell. Det finns flera poster för produktprofilen, en för varje resurs.
- XLSX-format - Resultat i varje organisationsdetalj som visas i ett separat blad. Posterna kopplas mellan de olika objekttyperna med hjälp av ett referens-ID. I vissa fall kan det finnas flera rader för ett visst objekt (t.ex. Resursobjekt när det finns en uppsättning värden som är kopplade till en viss resurs).
- JSON-format - det mest flexibla. Det kan dra nytta av strukturella relationer mellan exporterade objekt (t.ex. att produkter i en organisation visas direkt i organisationselementet). Samma fält exporteras i alla tre format, men vissa värden är överflödiga i JSON-format.

### Steg som ska exporteras

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/). På fliken **[!UICONTROL Organizations]** använder du organisationsväljaren för att välja organisationshierarkin där du vill exportera. Data för alla organisationer i hierarkin exporteras.
2. Markera ikonen **[!UICONTROL More Options]** ⋮ och välj **[!UICONTROL Export]**.

   ![Exportera organisationsstruktur](./assets/export-org-structure.png)

3. I dialogrutan **[!UICONTROL Export]** väljer du vad som ska exporteras och ett format som data ska exporteras i.

   ![Admin Console exportdialogruta](./assets/export-12.png)

4. Välj **[!UICONTROL Export]**.  Det kan ta flera minuter att generera exportfilen. När du är klar kan du hämta rapporten genom att gå till **[!UICONTROL Global Admin Console]** > **[!UICONTROL Insights]** > **[!UICONTROL Export Reports]**.

>[!NOTE]
>
>JSON-filer exporteras i zip-format. Du kan öppna dem med ett ZIP-verktyg eller operativsystemets zip-funktioner.

När du har hämtat filen kan du ändra data och sedan importera tillbaka dem. De importerade uppdateringarna visas i Global Admin Console som om du har redigerat data manuellt.

## Importera organisationsstrukturen

Som [global administratör](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) kan du importera potentiellt ändrade data. När nya data överförs jämförs de med aktuella data och eventuella ändringar tillämpas på organisationshierarkin. Alla importåtgärder utförs på den uppdaterade kopian av organisationshierarkin. Om du har väntande ändringar läggs importändringarna till ovanpå de väntande ändringarna i hierarkin.

### Steg som ska importeras

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com). På fliken **[!UICONTROL Organizations]** använder du organisationsväljaren för att välja den organisationshierarki där du vill utföra importen.
2. Markera ikonen **[!UICONTROL More Options]** **⋮** och välj **[!UICONTROL Import]**. Beroende på importfilens storlek och komplexitet kan bearbetningen ta från några sekunder till flera minuter.
3. Välj **[!UICONTROL Select a file]** och välj en JSON-, CSV- eller XLSX-fil som ska överföras. För CSV kan endast en organisationsinformation importeras åt gången och det finns inte stöd för import av produkter. De importerade ändringarna ser ut som om du har redigerat data manuellt.
4. Välj **[!UICONTROL Close]**.
5. Välj **[!UICONTROL Review Pending Changes]**.  Välj sedan **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem. Innan du utför ändringarna visas de väntande åtgärderna på samma sätt som när redigeringar görs manuellt i Global Admin Console.

## Exportera och importera scheman

När du importerar data med en CSV-fil kan fälten visas i vilken ordning som helst, men de måste alltid matcha rubrikraden.

När du importerar data måste du ange en åtgärd för varje element. Åtgärden kan vara något av följande:

- Uppdatera: indikerar en redigering.
- Skapa: innebär att ett nytt objekt skapas (till exempel organisation, användargrupp eller administratör).
- Ta bort: innebär att ett objekt tas bort (till exempel organisation, användargrupp eller administratör).

Indataposter utan operationsfält eller tomma operationsfält ignoreras.

### Organisationer

<table>
  <tr>
    <th>Fältnamn</th>
    <th>Beskrivning</th>
    <th>Anteckningar</th>
  </tr>

<tr>
    <td>id</td>
    <td>
      Organisations-ID.<br><br>
      När du lägger till en ny organisation kan detta vara tomt eller anges som en platshållaridentifierare, till exempel
      new_org_1. Platshållarens identifierare används om andra importerade poster måste referera till
      till den här organisationen. När dokumentet har skapats tilldelas det ett faktiskt organisations-ID och ersätter alla
      använder platshållarens organisations-ID.
    </td>
    <td>Kan anges till ett temporärt värde när operation=create</td>
  </tr>

<tr>
    <td>name</td>
    <td>
      Organisationens enkla namn. Minsta längd 4, max 100.
      Namn kan innehålla UTF-8-tecken på upp till 3 byte,
      4-byte-tecken stöds inte.
    </td>
    <td>
      Kan anges eller uppdateras när operation=create respektive operation=update
    </td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>Landskod</td>
    <td>
      Måste anges när operation=create, kan uppdateras när operation=update
    </td>
  </tr>

<tr>
    <td>type</td>
    <td>Typ av organisation</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      ID för överordnad organisation. Tom för rotorganisation.
      Vid uppdatering gäller avsevärda begränsningar, inklusive att den nya överordnade är i samma hierarki och
      har de produkter som finns i organisationen.
    </td>
    <td>
      Kan anges eller uppdateras när operation=create respektive operation=update
    </td>
  </tr>

<tr>
    <td>adminCount</td>
    <td>Antal administratörer</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>domainCount</td>
    <td>Antal domäner</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Antal användare</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>userGroupCount</td>
    <td>Antal användargrupper</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>administratörer</td>
    <td>Uppsättning administratörsobjekt som representerar administratörer för den här organisationen</td>
    <td rowspan="6">
      Kan saknas om det inte markerats för export. Den visas på en separat flik i XLSX-filer.
    </td>
  </tr>

<tr>
    <td>domäner</td>
    <td>Uppsättning domänobjekt som representerar domäner i den här organisationen</td>
  </tr>

<tr>
    <td>produkter</td>
    <td>Uppsättning produktobjekt som representerar produkter i den här organisationen</td>
  </tr>

<tr>
    <td>productProfiles</td>
    <td>Uppsättning produktprofilsobjekt som representerar produktprofiler i den här organisationen</td>
  </tr>

<tr>
    <td>userGroups</td>
    <td>Uppsättning användargruppsobjekt som representerar användargrupper i organisationen</td>
  </tr>

<tr>
    <td>orgPolicies</td>
    <td>Struktur som representerar policyer och deras värden</td>
  </tr>

<tr>
    <td>operation</td>
    <td>
      Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras.
    </td>
    <td>Alltid tomt vid export.</td>
  </tr>
</table>


**Importkrav:**

- För uppdatering eller borttagning måste orgId referera till en befintlig organisation i din hierarki.
- Om du skapar en ny organisation kan du lämna fältet orgId tomt eller ställa in det på ett unikt ID som du kan skapa (till exempel new-1 eller new-2). Detta ger ett id som kan användas för att referera till den organisation som ska skapas.
- Landskoden ska vara giltig.
- orgId för åtgärden *Update* och *Delete* ska redan finnas i organisationshierarkin.
- orgId markerat som *Delete* ska inte markeras som ett parentOrgId för organisationer med åtgärden *Update* eller *Create*.
- Underordnade organisationer på samma nivå och med samma överordnade ska inte ha samma orgNames.
- Om du skapar en organisation eller uppdaterar ett organisationsnamn får organisationens namn inte matcha namnet på ett befintligt underordnat objekt till samma överordnade.

### Administratörer

<table>
  <tr>
    <th>Fältnamn</th>
    <th>Beskrivning</th>
    <th>Använd</th>
  </tr>

<tr>
    <td>orgId</td>
    <td>Referens till den organisation där administratören finns.</td>
    <td>Används som referens för att hitta objekt som innehåller eller är kopplade till dem.</td>
  </tr>

<tr>
    <td>firstName</td>
    <td>
     Administratörsanvändarens förnamn.
För- och efternamn för Adobe ID-användare kan ersättas med ett användardefinierat värde när användaren accepterar inbjudan.
    </td>
    <td rowspan="4">
      Kan anges eller uppdateras när operation=create respektive operation=update
    </td>
  </tr>

<tr>
    <td>lastName</td>
    <td>Administratörens efternamn</td>
  </tr>

<tr>
    <td>e-post</td>
    <td>Admin - användarens e-postadress. Detta är en primärnyckel för användaren och måste vara unik.</td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>
Landskod där användaren arbetar. Gäller endast för Federated ID och Enterprise ID.
    </td>
  </tr>

<tr>
    <td>userType</td>
    <td>Adobe ID, Enterprise ID eller Federated ID.</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>GLOBAL ADMIN, GLOBAL VIEWER, SYSTEMADMINISTRATÖR, ANVÄNDARGRUPPADMINISTRATÖR, PRODUKTADMINISTRATÖR, PRODUKTPROFILADMINISTRATÖR, DISTRIBUTIONSADMINISTRATÖR OCH STORAGE_ADMIN.</td>
    <td rowspan="5">Kan anges när operation=Skapa</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>Grupp-ID för gruppen som den här användaren är administratör för. Relevant endast för användargrupp- och produktprofiladministratörer.</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>Produktlicens-ID för den produkt som användaren är administratör för. Gäller endast produktadministratörer.</td>

</tr>

<tr>
    <td>domän</td>
    <td>Domännamn för användare om e-postdomän inte används</td>

</tr>

<tr>
    <td>userName</td>
    <td>Användarnamn om inte e-postadress används</td>
  </tr>

<tr>
    <td>operation</td>
    <td>Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras.</td>
    <td></td>
  </tr>
</table>


**Importkrav:**

- orgId, email, adminType och userType måste innehålla giltiga värden.
- countryCode måste vara giltig.
- Om användaren redan finns och uppdateras måste userType matcha användaren.
- Kontrollera om det finns dubbla e-postadresser i organisationen.

### Produktprofiler

Export och import av produktprofiler består av två delar: information om produktprofiler och en uppsättning resurser som är kopplade till produktprofilen. Dessa resurser identifierar tjänster som kan konfigureras, vanligtvis bara för att aktivera eller inaktivera dem.

- Resursobjekten kapslas i produktprofilen i JSON-format.
- När du använder CSV eller XLSX med produktprofiler kombineras profilerna och resurserna i en tabell. Det kommer att finnas flera poster för produktprofilen, en för varje resurs.
- Det valda fältet i resursen kontrollerar om tjänsten är aktiverad.
- När du importerar produktprofiler måste det finnas en Skapa- eller Uppdatera-åtgärd för själva produktprofilen och för alla resursobjekt som ska uppdateras eller skapas.


<table>
  <tr>
    <th>Fältnamn</th>
    <th>Beskrivning</th>
    <th>Använd</th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      Identifierare för produktprofilen
Platshållarvärde kan användas när du skapar så att andra objekt kan referera till den nya profilen.
    </td>
    <td>Kan anges till tillfälligt värde när operation=create</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     Namn på produktprofil. Det kan inte vara en dubblett av andra produktprofiler eller användargrupper i samma organisation.
    </td>
    <td rowspan="2">
   Kan anges eller uppdateras när operation=create respektive operation=update
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>Textbeskrivning av produktprofilen</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>Licens-ID-referens till produkten</td>
    <td rowspan="2"> Används som referens för att hitta innehållande eller associerat objekt
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
Organisation som innehåller användargruppen
    </td>
  </tr>

<tr>
    <td>meddelanden</td>
    <td>Sant eller falskt för att ange om e-postmeddelanden ska skickas till användare när de läggs till eller tas bort från den här produktprofilen</td>
    <td>Kan anges eller uppdateras när operation=create respektive operation=update</td>
  </tr>

<tr>
    <td>resurser</td>
    <td> Array med resurser som är associerade med den här produktprofilen.
Resursfältet finns bara för JSON-formatet. För CSV- och XLSX-format representeras resurserna med följande extrafält: resourceName, resourceId, resourceDescription, icon, selected, quota, resourceType. Mer information om dessa fält finns i avsnittet *Produkter och resurser*.
Om produktprofilen har fler än en resurs finns det flera rader, en för varje resurs. De andra fälten får samma värden för varje resurs. </td>
    <td></td>
  </tr>

<tr>
    <td>operation</td>
    <td>Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras.</td>  
    <td></td>
  </tr>
</table>



**Importkrav:**

- productProfileId, licenseId och orgId måste ha giltiga värden.
- När du skapar en produktprofil måste productProfileName vara ett giltigt namn och får inte duplicera ett annat produktprofilnamn eller användargruppnamn i samma organisation.
- Kvotfältet måste ha ett giltigt värde för enhetstypen. Detta är numeriskt eller obegränsat när resourceType=QUOTA eller annars tomt.
- Meddelandefältet måste vara sant eller falskt.
- För CSV- och XLSX-importer validerar du productProfileId; alla dess poster måste ha samma orgId, licenseId och productProfileName.
- Validera duplicerat productProfileName i indatafilen och i organisationen.
- Profiler som ska uppdateras och tas bort måste finnas i organisationen.
- Resurser som ska uppdateras och tas bort (inaktiveras) måste finnas i profilen.
- Se till att följande gäller för profiler som ska skapas:
   - OrgId ska vara en ny organisation eller en befintlig organisation.
   - licenseId ska vara en ny produkt eller en befintlig produkt.
   - Validera profilens resurser.

### Resurser i produktprofiler

<table>
  <tr>
    <th>Fältnamn</th>
    <th>Beskrivning</th>
    <th>Använd</th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>Resursens namn</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>Identifierare för resursen</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>Textbeskrivning av resursen</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>icon</td>
    <td>URL till bild för resurs</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>markerad</td>
    <td>
      Om funktionen är aktiverad för en konfigurationspost.
      Det här fältet finns endast i JSON.
    </td>
    <td rowspan="2">
      Kan anges eller uppdateras när operation=create respektive operation=update.
    </td>
  </tr>

<tr>
    <td>kvot</td>
    <td>
      Kvantitet av primär resurs som kan ges ut till användare via den här produktprofilen.
      Det här fältet finns endast i JSON.
    </td>
  </tr>


<tr>
    <td>resourceType</td>
    <td>
      Värdet är SERVICE om det finns. Den här resursen representerar en tjänst som kan
      aktiverat eller inaktiverat baserat på värdet för det valda fältet.
      Det här fältet finns endast i JSON.
    </td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>operation</td>
    <td>
      Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras.
    </td>
    <td></td>
  </tr>
</table>


**Importkrav:**

- Åtgärdsfältet på resurser ignoreras när den produktprofil som de tillhör har åtgärder inställda på *Ta bort* eller *Skapa*.
- Ingen resurs ska markeras för borttagning. Det är en ogiltig åtgärd.
- För att produktprofiler ska kunna skapas måste antalet resurser matcha källproduktprofilens antal resurser.
- För resurser med åtgärden *Uppdatera* måste resursen finnas i produktprofilen.

### Användargrupper

<table>
  <tr>
    <th>Fältnamn</th>
    <th>Beskrivning</th>
    <th>Använd</th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
      Identifierare för användargrupp. Platshållarvärde kan användas för att skapa så att
      andra objekt kan referera till den nya användargruppen.
    </td>
    <td>Kan anges till tillfälligt värde när operation=create</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td>Namn på användargrupp</td>
    <td rowspan="2">
      Kan anges eller uppdateras när operation=create respektive operation=update.
    </td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>Textbeskrivning av användargrupp</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Antal användare i användargruppen</td>
    <td>Skrivskyddad</td>
  </tr>

<tr>
    <td>profiler</td>
    <td>
      Array med produktprofil-ID som användargruppen är kopplad till.
      XLSX har en rad per värde med samma värden för andra fält.
    </td>
    <td>
      Kan anges eller uppdateras när operation=create respektive operation=update.
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>Organisation som innehåller användargruppen</td>
    <td>Används som referens för att hitta innehållande eller associerat objekt</td>
  </tr>

<tr>
    <td>operation</td>
    <td>
      Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras.
    </td>
    <td></td>
  </tr>
</table>

**Importkrav:**

- orgId måste referera till en befintlig organisation eller en organisation som skapas i samma import.
- userGroupId måste referera till en befintlig grupp för uppdatering eller borttagning, och kan vara ett id som du definierar för nya användargrupper.
- För uppdatering eller skapande får userGroupName inte vara tomt och får inte duplicera ett annat namn för användargrupp eller produktprofil i samma organisation.
- Kontrollera att userGroupName inte är duplicerat i indatafilen och i organisationen.
- userGroups som ska uppdateras och tas bort måste finnas i organisationen.
- Profil som ska tas bort från användargruppen måste finnas i användargruppen. Uppdateringsåtgärder kan inte utföras på en användargrupps profil.
- För att användargrupper ska kunna skapas måste du kontrollera följande:
   - OrgId ska vara en ny organisation eller en befintlig organisation.
   - LicensId, om tillämpligt, ska vara en ny produkt eller en befintlig produkt.
   - productProfileId ska vara en ny produktprofil eller en befintlig produktprofil.

### Domäner

Domäninformationen ger skrivskyddad information om domäner som är tillgängliga i respektive organisation. Dessa data kan inte redigeras.


| Fältnamn | Beskrivning | Använd |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | Referens till organisationen som den här domänen finns i | Används som referens för att hitta objekt som innehåller eller är kopplade till dem. |
| domainName | Domänens namn (till exempel adobe.com). | Skrivskyddad |
| directoryName | Namnet på den katalog där domänen är listad | Skrivskyddad |
| directoryType | Federated ID eller Enterprise ID. | Skrivskyddad |
| domainStatus | ETT AV AKTIVT, RESERVERAT, OANPASSAT, ANPASSAT, VALIDERAT, ÅTERKALLAT, UPPHÖRT. | Skrivskyddad |


### Produkter och resurser {#products-and-resources}

I XLSX-filer finns det två ark - en för produkter och en för resurserna. I JSON kapslas resursobjekt i produktobjektet.

**Produkter**


| Fältnamn | Beskrivning | Använd |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | ID som identifierar produkten. Varje produkt har ett unikt licens-ID i den organisation där den listas. När du lägger till en ny produkt kan detta vara tomt eller använda en platshållaridentifierare (till exempel new_product_1). När du har skapat en licens-id tilldelas den ett som ersätter all användning av platshållarens licens-id. | Kan anges till tillfälligt värde när operation=create |
| productName | Produktens namn | Skrivskyddad |
| productDescription | Textbeskrivning av produkten | Skrivskyddad |
| allowOverallokation | Booleskt som anger om överallokering av den här produktinstansen är tillåten. Överbeläggning avser möjligheten att tilldela mer kvantitet till en underordnad organisation än vad du har beviljats. | Kan anges eller uppdateras när operation=create respektive operation=update |
| icon | URL för ikon | Skrivskyddad |
| sourceLicenseId | Licens-ID för produktinstansen i organisationen som den här produkten har allokerats från. Värdet är null om den här instansen inte är en tilldelad produkt, utan är en köpt produkt. | Kan anges när operation=Skapa |
| productId | Identifierare för produkten. | Skrivskyddad |
| orgId | Identifierare för organisationen som innehåller den här produktinstansen | Används som referens för att hitta innehållande eller associerat objekt |
| återdistribuerbar | Booleskt som anger om den här produkten har resurser som kan beviljas underordnade organisationer. | Skrivskyddad |
| resurser | Objekt som innehåller en uppsättning resursobjekt som representerar resurserna och inställningarna i den här produkten |                                                                               |
| operation | Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras. |                                                                               |


**Importkrav:**

- För att kunna skapa måste licenseId vara ett unikt ID som du skapar.
- För uppdatering måste licenseId vara ID:t för en befintlig produkt i den angivna organisationen.
- orgId måste referera till en befintlig organisation eller en organisation som skapas i samma importåtgärd.
- För att skapa måste sourceLicenseId referera till en befintlig produkt eller det ID som du definierade för en produkt som skapas i samma importåtgärd.
- licenseId och sourceLicenseId ska inte vara samma för produkter med åtgärden *Create*.
- Validera produktorganisationer. Organisationen ska vara ny eller finnas redan i organisationshierarkin.
- Produkten ska redan finnas i organisationshierarkin för åtgärden *Uppdatera* och *Ta bort*.
- licenseId som har markerats som *Delete* ska inte användas som ett sourceLicenseId för produkter med åtgärden *Create* och *Update*.
- Verifiera att sourceLicenseId ska finnas i den överordnade organisationen för produkter med åtgärden *Create*.

**Resurser för produkter**

Resursobjekt kan visas i produkter och i produktprofiler.


| Fältnamn | Beskrivning | Använd |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | Resursens namn | Skrivskyddad |
| resourceId | Identifierare för resursen | Skrivskyddad |
| resourceDescription | Textbeskrivning av resursen | Skrivskyddad |
| icon | URL till bild för resurs | Skrivskyddad |
| productName | Namnet på produkten som resursen är en del av. | Skrivskyddad |
| licenseId | Licens-ID (produktinstans) för produkten som den här resursen är en del av. | Används som referens för att hitta innehållande eller associerat objekt |
| grantedQuantity | Beviljad kvantitet för den här resursen: mängden resurser som den här organisationen har tillgängligt att använda lokalt eller allokera till underordnade organisationer. | Kan anges eller uppdateras när operation=create respektive operation=update |
| enhet | Namn på enhet för bidragskvantitet. | Skrivskyddad |
| currentQuantity | Aktuell användbar kvantitet i organisationen. Detta är tilldeladKvantitet minus resurser som tilldelats underordnade organisationer. Det här är värdet som visas i Admin Console för den här produkten/resursen. | Skrivskyddad |
| provisionedQuantity | Kvantitet som faktiskt har etablerats: kan vara mindre än grant eller current, kan vara mindre än currentQuantity om en begränsning finns på plats. | Skrivskyddad |
| operation | Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras. |                                                                               |


**Importkrav:**

Åtgärdsfältet på resurser ignoreras när den produkt de tillhör har åtgärder som angetts som *Ta bort* eller *Skapa*.
- Ingen resurs ska markeras för borttagning. Det är en ogiltig åtgärd.
- För produkter som ska skapas måste antalet resurser matcha källproduktens antal resurser.
- För resurser med *Update*-åtgärden måste resursen finnas i produkten.

## Importera och exportera produktallokeringsdata

Som [global administratör](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) kan du exportera produktallokeringsdata som en JSON- eller CSV-fil. Du kan sedan ändra dessa data och överföra dem tillbaka för att importera ändringarna. När data som kan ändras överförs jämförs de med aktuella data och eventuella ändringar tillämpas på produktallokeringsdata. Du kan sedan granska och skicka in väntande ändringar så att de träder i kraft.

## Exportera produktallokeringsmodellen

Så här exporterar du produktallokeringsmodellen:

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/) och gå till fliken **[!UICONTROL Product Allocation]**.
2. Markera ikonen **[!UICONTROL More Options]** ⋮ och välj sedan **[!UICONTROL Export CSV]** eller **[!UICONTROL Export JSON]**. Filen hämtas. [Läs mer](#export-and-import-formats-for-product-allocation) om exportformaten.

## Importera produktallokeringsmodellen

Du kan exportera data, ändra dem och sedan importera den ändrade filen. Så här importerar du produktallokeringsmodellen:

1. Logga in på [Global Admin Console](https://global-admin-console.adobe.com/) och gå till fliken **[!UICONTROL Product Allocation]**.
2. Markera ikonen **[!UICONTROL More Options]** ⋮ och välj **[!UICONTROL Import]**.
3. Välj en JSON- eller CSV-fil som ska överföras.
4. Välj **[!UICONTROL Review Pending Changes]**.  När du har granskat ändringarna väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Exportera och importera format för produkttilldelning

Exportera- och importformaten är desamma. När du importerar i CSV-format kan fälten visas i valfri ordning, men de måste matcha rubrikraden. När du importerar i JSON-format kan fälten visas i valfri ordning.

Du måste ange åtgärden när du importerar produktallokeringsdata. Åtgärden kan vara något av följande:

- Uppdatera: anger en redigering (ändra till grantedQuantity, allowOverAllocation values).
- Skapa: anger att en produktresurs ska läggas till i den angivna organisationen.
- Ta bort: indikerar borttagning av produkten.

Om ingen åtgärd anges sker inga ändringar när data importeras för den raden i CSV eller objektet i JSON.

I den exporterade filen finns det en rad eller post för varje produktresurs. Vissa produkter har mer än en resurs.

Om en produkt har mer än en resurs kan Uppdateringsåtgärder tillämpas på oberoende resurser, en Delete-åtgärd tar bort produkten inklusive alla resurser från en organisation och en Create-åtgärd behöver en post för varje resurs i importfilen så att rätt kvantitet kan anges för var och en av dem. Fältet allowOverAllocation är för hela produkten och det spelar ingen roll i vilken resurs en uppdatering av det här fältet finns.

### Beskrivning av rubriker


| Fältnamn | Beskrivning | Använd |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| productName | Produktens namn. | Skrivskyddad |
| licenseId | ID för en produkt (unikt för en produkt i en organisation). När du lägger till en ny produkt kan detta vara tomt eller anges som en platshållaridentifierare (till exempel new_product_1). Platshållaridentifieraren används om andra importerade poster behöver referera till den här produkten. När du skapat en licens-id tilldelas den och ersätter all användning av platshållarens licens-id. | Kan anges när operation=Skapa |
| sourceLicenseId | ID för överordnad produkt. Det är tomt eller null om det här representerar ett inköp i stället för en allokering. | Kan anges när operation=Skapa |
| productId | ID som identifierar den här produktklassen. Detta ID delas mellan produkter av samma typ och skiljer sig från licenseId som identifierar en instans av den här produkten. | Skrivskyddad |
| resourceName | Namn på den här produktresursen. Exempel: Användarlicenser. | Skrivskyddad |
| resourceId | ID som identifierar denna produktresurs. | Kan anges när operation=Skapa |
| orgPathName | Sökväg till organisationen som produktresursen finns i. Segment avgränsade med &quot;/&quot;. | Skrivskyddad |
| orgName | Enkelt namn på organisationen som innehåller den här produktresursen. Detta är det sista segmentet i orgPathName. | Skrivskyddad |
| orgId | Organisations-ID för organisationen som innehåller den här produktresursen. | Kan anges när operation=Skapa |
| grantedQuantity | Antal enheter av resurskvantitet som den här organisationen har beviljats av dess överordnade eller det belopp som köpts om den här produktresursposten representerar ett inköp. Det här fältet kan uppdateras förutom för köpta produkter eller rotallokeringar som den globala administratören inte har behörighet att ändra. | Kan uppdateras när operation=Uppdatera eller operation=Skapa |
| enhet | Resursenhetens namn. Exempel: Användare. | Skrivskyddad |
| totalAllocations | Summan av bidrag till underordnade organisationer från den här organisationen för den här produktresursen. Detta värde omfattar direkta bidrag till omedelbart tillkommande barn plus överanslag från dessa organisationer. Om den här organisationen t.ex. beviljade ett barn som fyllt 10 och barnet sedan tilldelade sitt barn 25, skulle totalAllocations vara 25: de 10 som beviljats barnet plus en åldersgräns på 15 i det barnet. | Skrivskyddad |
| grantOverage | Belopp med vilket totalAllocations överskrider given kvantitet. Om totalAllocations inte överstiger grantedQuantity är det här värdet null eller noll. | Skrivskyddad |
| localLicensedQuantity | Belopp för den här resursen som har beviljats den här organisationen kvar för användning efter att den kvantitet som tilldelats till barn har dragits av. Detta är det belopp som visas som tillgängligt i Admin Console. Värdet kan vara noll, men är aldrig negativt, även om den här organisationen har överallokerade resurser till sina underordnade. | Skrivskyddad |
| localUsage | Antal enheter för resursen som används i organisationen. Om du till exempel delegerar en användarlicens till en användare räknas det som en användarenhet. | Skrivskyddad |
| totalUsage | Antal enheter av resursen som används av den här organisationen och alla underordnade. Detta visar användningen av den här resursen i den del av organisationshierarkin som den här organisationen har roterat. | Skrivskyddad |
| useOverage | Belopp för den totala användningen jämfört med organisationens beviljande (organisationen och underordnade har använt mer av resursen än vad som är tillgängligt). Detta visar ett värde som inte är noll när totalUsage överskrider localLicensedQuantity. | Skrivskyddad |
| allowOverAllocation | Anger om användaren har rätt att bevilja fler resurser till barn även om det inte finns mer att bevilja (tillåts att bevilja trots att det finns en anslagsmängd). Detta värde gäller alla resurser för den här produkten. Om det görs ett försök att uppdatera allowOverocation för mer än en resurs av samma produkt till olika värden, blir resultatet slumpmässigt. | Kan uppdateras när operation=Update |
| isPurchasedProduct | true om produkten är en inköpsprodukt (inte allokerad av överordnad). Detta motsvarar att sourceLicenseId har ett tomt värde. | Skrivskyddad |
| återdistribuerbar | true om produkten kan tilldelas barn betyder false att produkten endast är tillgänglig i den organisation där den visas och att resurser inte kan tilldelas någon annan organisation. | Skrivskyddad |
| operation | Ett av de tomma alternativen Skapa, Uppdatera eller Ta bort. Åtgärd som ska vidtas när data importeras. |                                                          |


**Importkrav**

**Dataverifiering**

- Åtgärdsfältet måste ha en giltig åtgärd.
- Produktimportdata måste ha egenskaper och värden för obligatoriska fält.
- Produktimportens dataegenskaper måste vara av rätt typ.
- Produktprincipfältet (overAllocation) får inte anges för olika resurser.
- Fältet för beviljad kvantitet:
   - Det går inte att ändra till *obegränsat* om det inte redan är *obegränsat*.
   - Måste vara ett positivt heltal eller strängvärdet *unlimited.*

**Behörighet/hjälpmedelsvalidering**

- Organisationen som är associerad med importdata måste finnas. Om du uppdaterar kontrollerar du att produkten och resursen som är kopplad till importdata verkligen finns.

**Lägg till produktvalidering**

- SourceLicenseId måste finnas.
- Organisationen som är associerad med den nya produkten måste finnas.
- Produkten som skapas får inte finnas (produkt med samma licens-ID).
- Resurserna som är kopplade till en produkt som skapas måste ha ett motsvarande productId som matchar den produkten.
