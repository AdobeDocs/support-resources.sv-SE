---
title: Felkorrigeringar (dolda)
description: Testsida för intern testning
hide: true
hidefromtoc: true
source-git-commit: 0279a8985376d587b470bf81fbe8958a5679afb5
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 1%

---

# Felkorrigeringar

## UGP-10560 - emblem i fällningar som kan komprimeras

+++ Tidigare versioner

### Version V1.16

_13 feb 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Produktvideor stöds nu av katalogtjänstens API.
![Korrigera](assets/package.png) Stöd finns nu för paketprodukter med fasta priser.
![Korrigera](assets/package.png) Alternativ utanför lagret visas nu i PDP-widgeten.

#### Kända begränsningar

Dessa funktioner stöds ännu inte:

* Maximal storlek för nyttolasten för dynamiska attribut är 9 MB.
* Gruppproduktpris. Kan beräknas med enkla produktpriser.
* I en bildarray innehåller endast den första bilden roller.

Följande begränsningar kan åtgärdas med API Mesh och Core GraphQL API:

* Lägsta kampanjpris
* [Nivåpriser](https://www.adobe.com)

### Version V1.13

_12 oktober 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Katalogtjänsten stöder `inStock` för produktvarianter.
![Nytt](assets/package.png) `urlKey` och `externalId` har lagts till i GraphQL schema.
![Nytt](assets/package.png) Nu finns det stöd för nedladdningsbara produkter och presentkort.

### Version V1.12

_19 september 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](https://www.adobe.com).
![Korrigera](assets/package.png) Den här versionen innehåller felkorrigeringar och förbättringar på tjänstsidan.

### Version V1.11

_18 juli 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Katalogtjänsten har nu stöd för [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL query for Product Recommendations.

### Version V1.10

_27 juni 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Katalogtjänstens API har nu stöd för&quot;relaterade produkter&quot;.

### Version V1.7

_12 april 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Katalogtjänsten rensar nu borttagna produktvarianter.
![Korrigera](assets/package.png) Infrastrukturskalbarhet och prestandaförbättringar.

### Version V1.6

_28 mars 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Lagt till färgrutor i [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) fråga.
![Nytt](https://www.adobe.com).

### Version V1.5

_6 mars 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Tillagd [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL funktionalitet.
![Korrigera](assets/package.png) Förbättrade prestanda och API-skalbarhet.

### Version V1.4

_7 februari 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Publicerat katalogtjänstpaket för att förenkla installationen.
![Korrigera](assets/package.png) API-skalbarhet och prestandaförbättringar.

### Version V1.3

_17 januari 2023_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Förenklad och förbättrad startupplevelse.
![Nytt](assets/package.png) Nya slutpunkter för kundsandlådor finns tillgängliga för testning före produktion.
![Nytt](assets/package.png) Stöd tillagt för virtuella produkter.
![Korrigera](assets/package.png) API-skalbarhet och prestandaförbättringar.

### Version V1.1

_18 november 2022_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Katalogtjänsten har nu stöd för Adobe [API-nät](https://developer.adobe.com/graphql-mesh-gateway/).
![Korrigera](assets/package.png) Förbättrad API-skalbarhet och övergripande prestanda.

### Version V1.0

_4 oktober 2022_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Nu support för paketerade och grupperade produkter.
![Nytt](assets/package.png) B2B-synlighetsåsidosättningar har lagts till. Produkterna är nu sökbara och kan läggas till i kundvagnen för specifika kundgrupper.
![Korrigera](assets/package.png) Tjänsten är nu stabilare och har förbättrat prestandan.

### 0.3-versionen - Beta+

_12 september 2022_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) Bilder för variantstöd: produktbilder returneras baserat på de valda alternativen
![Nytt](assets/package.png) Roller för prissupport: endast medlemmar i specifika kundgrupper kan se priset på produkter
![Korrigera](assets/package.png) Förbättrad stabilitet och prestanda för tjänsten
![Nytt](assets/package.png) Uppdateringar tas emot när produkter tas bort från katalogen

### Betaversion

_9 augusti 2022_

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](assets/package.png) The `products` och `refineProduct` frågor returnerar följande data:

* Fördefinierade produktattribut (system).
* Dynamiska produktattribut och filtrera dem efter roll (produktvisningssida/produktlistsida).
* Produktalternativ.
* Produktbilder och filtrera dem efter roll (PDP/PLP).
* Ett specifikt pris för enkla produkter och prisintervall för konfigurerbara produkter.
* Kundgruppspriser och prisintervall. De returnerar ett standardgrundpris för kunderna utan någon kundgrupp.
* Produkttyper där B2B-kundspecifika priser används.

+++

## UGP-10565 - Textmarkering

Text före `<div class="preview">`

<div class="preview">

### Lägg till inbyggda Workfront-fält

Du kan lägga till inbyggda Workfront-fält i dina anpassade formulär. När det anpassade formuläret bifogas till ett objekt fylls fältet i från objektdata. Fältet Beskrivning i ett anpassat formulär som är kopplat till ett projekt hämtas till exempel i projektbeskrivningen. (Fältet kan visa &quot;Ej tillämpligt&quot; om inga data är tillgängliga.)

1. På skärmens vänstra sida finns **Ursprungligt fält** och dra den till ett avsnitt på arbetsytan.
1. Konfigurera alternativen för det anpassade fältet till höger på skärmen:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Etikett</td> 
      <td> <p>(Obligatoriskt) Skriv en beskrivande etikett som ska visas ovanför fältet. Du kan när som helst ändra etiketten.</p> <p><b>VIKTIGT</b>: Använd inte specialtecken i den här etiketten. De visas inte korrekt i rapporter.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Namn</td> 
      <td> <p>(Obligatoriskt) Det här namnet är det som identifierar fältet.</p><p> När du konfigurerar fältet för första gången och skriver etiketten fylls fältet Namn automatiskt i så att det matchar det. Men fälten Etikett och Namn är inte synkroniserade, vilket ger dig frihet att ändra etiketten som användarna ser utan att behöva ändra namnet som systemet ser.</p>
      <p><b>VIKTIGT</b>:
      <ul> 
      <li>Även om det går att göra det rekommenderar vi att du inte ändrar det här namnet efter att du eller andra användare har börjat använda det anpassade formuläret i Workfront. Om du gör det kommer systemet inte längre att känna igen fältet där det nu kan refereras i andra områden av Workfront.</p> </li>
      <li> <p>Varje fältnamn måste vara unikt i din organisations Workfront-instans. På så sätt kan du återanvända ett som redan har skapats för ett annat anpassat formulär.</p> </li>
      <li><p>Vi rekommenderar att du inte använder punkt-/punkttecken i det anpassade fältnamnet för att förhindra fel när du använder fältet i olika områden av Workfront.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Instruktioner</td> 
      <td> <p>Ange eventuell ytterligare information om fältet. När användarna fyller i det anpassade formuläret kan de föra musen över frågeteckenikonen för att visa ett verktygstips som innehåller den information du skriver här.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Referensfält</td> 
      <td><p>(Obligatoriskt) Välj ett internt Workfront-fält.<p><p>Endast inbyggda fält för formulärets objekt är tillgängliga. Om t.ex. listan Objekttyper längst upp i formulärdesignern visar Projekt, kan du välja inbyggda fält för projekt, men inte fält som är specifika för uppgifter.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Storlek</td> 
      <td>(Valfritt) Ändra fältets visningsstorlek efter behov.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicka på **Använd** och gå vidare till ett annat avsnitt för att fortsätta skapa formuläret.

   eller

   Klicka **Spara och stäng**.

</div>

Text efter markering

## UGP-10566 - Länktexten är mindre än vanlig text i HTML-tabeller

Se även UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>Indata till</td>
<td>Beskrivning</td>
<td>Finns för </td>
</tr>
<tr> 
    <td role="rowheader">Etikett</td> 
    <td> <p>(Obligatoriskt) Skriv en beskrivande etikett som ska visas ovanför det anpassade fältet. Du kan när som helst ändra etiketten. Mer information finns i <a href="https://www.adobe.com" class="MCXref xref">Lägga till ett anpassat fält i ett anpassat formulär</a> i den här artikeln.</p> <p><b>VIKTIGT</b>: Använd inte specialtecken i den här etiketten. De visas inte korrekt i rapporter.</p> </td> 
    <td>
    <ul>
    <li>Alternativknappar. Mer information finns i <a href="https://www.adobe.com">Lägga till ett anpassat fält i ett anpassat formulär</a> i den här artikeln. (Ingen klass)</li>
    <li>Kryssrutegrupp</li>
    <li>Listruta</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Gammalt fel

&quot;span&quot;-taggen fungerar inte så bra i en NOTE (och list)

Information om vilka funktioner som är tillgängliga i den nya kommentarsfunktionen och för vilka objekt finns i [Ny kommentarsfunktion](note-test.md).

1. Gå till det objekt som du vill lägga till ett svar på.
1. Klicka **Uppdateringar** och klickar sedan på **Kommentar** -fliken för objektet och hitta den kommentar eller det svar som du vill svara på

   eller

   <span class="preview">Klicka på **Alla** tabbtangenten och klicka sedan på **Svara i kommentarer** för att öppna kommentaren på fliken Kommentarer och svara på den. Du kan inte svara på fliken Alla.</span>

1. (Valfritt) Om du vill ta med text från en tidigare uppdatering i ditt svar klickar du på **Mer** i det övre högra hörnet av kommentaren som du vill svara på och klicka sedan på **Offertsvar**. Texten från föregående uppdatering visas i indataområdet, markerat med en lodrät grå linje.
1. Klicka **Svara**.

   ![](assets/package.png)

   Du kan se de användare som aktivt deltar i konversationen längst ned i **Lägg till svar...** och du kan lägga till fler eller ta bort de som inte längre är relevanta. Dessa användare, tillsammans med alla användare som prenumererar på objektet, får ett meddelande varje gång en uppdatering eller ett svar görs för objektet. Du kan också tagga fler användare så att de inkluderas i ditt svar.  Om du vill tagga fler användare läser du [Tagga andra för uppdateringar](note-test.md).

   >[!TIP]
   >
   >   Om du vill lägga till fler svar i ett befintligt svar kan du börja skriva i **Lägg till svar ...** eller klicka **Svara** på den ursprungliga kommentaren. Svaret läggs till i slutet av tråden.

1. Börja skriva ditt svar och använd eventuella ytterligare alternativ från verktygsfältet RTF. Mer information om hur du använder RTF eller andra uppdateringsfunktioner finns i [Uppdatera arbete](note-test.md).

1. Klicka **Skicka** för att spara svaret.

1. (Valfritt) Klicka på **Mer** i det övre högra hörnet av kommentaren som du vill svara på om du vill ha fler alternativ för att hantera svaret. Mer information finns i [Uppdatera arbete](note-test.md).
