---
title: Tabeller
description: Arbeta med markeringstabeller och HTML-tabeller.
hide: true
hidefromtoc: true
exl-id: 5ce746fc-6835-4bee-85c5-5ad5176baca0
source-git-commit: 6893d1e41c3899c3ab6a9b02b305161eb3f7e049
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%

---

# Tabeller

Matt var här om och om igen -

EDS

Standard Markdown stöder endast enkla tabeller. För AdobeDocs Markdown finns följande alternativ:

* Grundläggande markeringstabeller
* HTML tabeller
* Markeringstabeller med begränsad HTML-syntax för styckebrytningar (`<p>`), radbrytningar (`<br>`) och grundläggande listor (`<ul>`, `<ol>`).

## Konvertera tabeller från HTML till markeringstabeller

I vissa fall vill du konvertera en HTML-tabell till en markeringstabell eller till markeringstext. Kanske behöver du förbättra utseendet, åtgärda ett valideringsfel eller göra det enklare att redigera i framtiden.

Tyvärr har vi inte lyckats hitta ett enda verktyg som kan konvertera HTML-tabeller på ett bra sätt. Vi brukar använda en kombination av verktyg för att snickra samman en hyfsad markeringstabell.

| Verktyg | Vad det gör |
|--- |--- |
| [Generator för markeringstabeller](https://www.tablesgenerator.com/markdown_tables) | Bra för att skapa markeringsregister från början. |
| [Avancerad tabellkonverterare](https://tableconvert.com/html-to-markdown) | Konvertera tabeller från alla format till alla format. <p>**Obs!** Länkar och bilder förenklas när de konverteras. |
| [Grundläggande tabell-html > markeringskonverterare](https://jmalarcon.github.io/markdowntables/) | Enkel konverterare för HTML <p>**Obs!** Länkar och bilder förenklas när de konverteras. |
| [Icke-tabellbar HTML > Markeringskonverterare](https://codebeautify.org/html-to-markdown) | Konverterar tabeller från HTML till syntax som inte kan tabellmarkeras. Använd i kombination med ovanstående verktyg för att kopiera länkar, bilder och andra förenklade objekt. |

## Grundläggande markeringstabeller

* Se till att du lägger till minst tre bindestreck på den andra raden som bestämmer tabellegenskaperna. Exempel: `|--- |--- |--- |` för en tabell med tre kolumner.
* Markeringstabeller måste ha minst en rubrikrad och en innehållsrad. Du kan inte skapa en enradig eller encellig markeringstabell (använd HTML istället).
* Se till att varje rad har samma antal lodstreck (&vert; ). Om du behöver inkludera ett lodstreck i en tabellcell kan du undvika det genom att föregå det med ett omvänt snedstreck (`\|`) eller använda enhetskoden HTML (`&vert;`).
* Var försiktig med att använda kodblock i tabeller. Textbundna kodblock kan orsaka oproportionella kolumnbredder.
* Du kan ändra hur tabellen återges genom att ange Auto eller Fast. Se [Ändra hur tabeller återges](#table-rendering).

## Skapa markeringstabeller med bonusen HTML

För att underlätta migreringen har vi utökat markeringstabeller med stöd för styckebrytningar i HTML (`<p>`), radbrytningar (`<br>`) och grundläggande HTML-listor (`<ul>` och `<ol>`) i markeringstabeller.

**Markeringstabell med radbrytningar och listor**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**Exempel**

| Rubrik 1 | Rubrik 2 | Rubrik 3 |
|--- |--- |--- |
| Normal rad | rad 1 kolumn 2 | rad 1 kolumn 3 |
| Radbrytning | första raden i cell<br>andra raden i cell | rad 1 kolumn 3 |
| Punktlista | Punktlista:<ul><li>Objekt 1</li><li>Objekt 2</li><li>Objekt 3</li></ul> | rad 2 kolumn 3 |
| Punktlista med radbrytning | Punktlista:<ul><li>Objekt 1</li><li>Objekt 2</li><li>Objekt 3</li></ul><br>Det här är en ny rad efter punktlistan | rad 2 kolumn 3 |

>[!IMPORTANT]
>
>Om du bestämmer dig för att använda HTML i inbyggda tabeller måste du använda rätt HTML-syntax. Felaktiga HTML-syntaxer resulterar i valideringsfel som är svåra att förstå. Dubbelkontrollera ditt arbete.

## Arbeta med tabeller i HTML

Migreringsverktyget försökte bevara så mycket formatering som möjligt från den ursprungliga tabellen. Den mesta HTML-syntaxen ignoreras, medan en del av syntaxen ger upphov till valideringsfel.

**Exempel på migrerad HTML-tabell**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**Återgiven**

<table> 
 <tbody>
  <tr>
   <th>Egenskap</th> 
   <th>Typ</th> 
   <th>Värdebeskrivning</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>Sträng[]</td> 
   <td><p><i>(Obligatoriskt)</i> En sträng med flera värden av badge-bilder upp till antalet badgingLevels. Sökvägarna för taggbilder måste beställas så att den första tilldelas den högsta experten. Om det finns färre emblem än vad som anges av badgingLevels fyller det sista märket i arrayen ut resten av arrayen. Exempelpost:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Lång</td> 
   <td><p><i>(Valfritt)</i> Anger vilka kunskapsnivåer som ska tilldelas. Om det till exempel ska finnas en <code>expert </code> och en <code>almost expert</code> (två emblem), ska värdet anges till 2. badgingLevel ska motsvara antalet expertrelaterade badge-bilder som anges för egenskapen badgingPath. Standardvärdet är 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>Sträng</td> 
   <td><p><i>(Obligatoriskt)</i> Identifierar bedömningsmotorn som antingen grundläggande eller avancerad. Ange som "avancerat", annars är standardvärdet "grundläggande".</p></td> 
  </tr>
 </tbody>
</table>

**När HTML-tabeller ska användas**

* Balansera kolumner.
* Om du vill utesluta tabellrubriker (markeringstabeller måste ha en rubrikrad).
* Om du vill ta bort kanten för en enradig tabell (`<tr style="border: 0;">`).
* Lägga till kolumn- eller radintervall.
* Justera text i en tabellcell.

**Anteckningar för arbete med HTML-tabeller**

* Använd inte Markdown-syntax i HTML-tabeller. Om du t.ex. lägger till `[!NOTE]` i en HTML-tabell återges den som den är (`[!NOTE]`). Använd i stället HTML-syntax för exempelvis anteckningar och bilder.

  Loc-taggar är ett undantag till den här regeln eftersom UICONTROL- och DNL-taggar tas bort innan sidorna återges.

* Alla HTML-syntax stöds inte i tabeller. Bredd, höjd, färg och andra HTML-syntaxelement ignoreras när de återges i EXL. Du kan lämna dessa värden i om de inte resulterar i valideringsfel.
* Om du vill justera text använder du `align: "left|center|right"` i HTML. Om du till exempel vill centrera innehållet i en tabellcell använder du `<td align="center">`.
* HTML-tabeller kan inte innehålla kapslade tabeller.

>[!TIP]
>
>Om du vill stänga av kantlinjen för en HTML-tabell med en rad använder du den här syntaxen:
>
>```
><table>
><tr style="border: 0;">
>```

## Ange hur tabeller ska återges {#table-rendering}

Vi kan återge tabeller på två sätt:

* **Fast** (för närvarande standard) - Innehåller anpassade regler för återgivning av tabeller, inklusive HTML-tabeller med bilder. Tabeller återges som helbreddstecken utan bläddring, vilket ibland orsakar överlappande text.
* **Auto** - Liknar Git-smaksatt markering (GFM). Tabeller kan rullas, så texten överlappar inte.

I de flesta fall återges tabellerna med samma utseende. Om tabellen innehåller överlappande text bör du dock använda taggen `auto`. Eller om tabellen HTML med bildkort inte återges korrekt kanske du vill använda taggen `fixed`.

Vi överväger att ändra standardvärdet från `fixed` till `auto`.

## Redigera markeringstabeller

Om du vill ange hur en intern markeringstabell ska återges lägger du till en av dessa syntaxrader EFTER tabellen, med tomma rader före och efter:

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![table-rendering](assets/table-render.png)

### Redigera HTML-tabeller

Om du vill ange hur en HTML-tabell ska återges använder du någon av dessa syntaxrader på den första raden i tabellen:

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### Använd Auto eller Fixed

**Överlappande text**

Använd `auto` för tabeller med långa kodblock eller text som orsakar överlappande text när `fixed` (standard) är markerat.

*Fast (standard)*

| Insikter - mått | Beskrivning | ID-frågeparameter |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Totalt antal ogiltiga typmeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.range.count** | Totalt antal ogiltiga intervallmeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.format.count** | Totalt antal ogiltiga formatmeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.pattern.count** | Totalt antal ogiltiga mönstermeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.presence.count** | Totalt antal ogiltiga närvaromeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.enum.count** | Totalt antal ogiltiga enum-meddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |

{style="table-layout:fixed"}

*Auto*

| Insikter - mått | Beskrivning | ID-frågeparameter |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Totalt antal ogiltiga typmeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.range.count** | Totalt antal ogiltiga intervallmeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.format.count** | Totalt antal ogiltiga formatmeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.pattern.count** | Totalt antal ogiltiga mönstermeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.presence.count** | Totalt antal ogiltiga närvaromeddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |
| **timeseries.data.collection.validation.category.enum.count** | Totalt antal ogiltiga enum-meddelanden för en datauppsättning eller för alla datauppsättningar. | Datauppsättnings-ID |

{style="table-layout:auto"}

**HTML-tabeller med balanserade bilder**

Använd `fixed` för HTML-tabeller som kräver balanserade bilder som blir obalanserade när `auto` väljs. I det här exemplet har bilderna identiska storlekar, men det finns mer text i den mellersta kolumnen.

*Auto*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Arbetsflöde för Adobe leads</strong></a>
    </div>
    <em>Huvudarbetsflöde för redigering för leadskrivare.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Sällan" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Arbetsflöde för användare med låg frekvens</strong></a>
    </div>
    <em>Inte en huvudskrivare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig det enklaste sättet att göra bidrag.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validering" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validering</strong></a>
    </div>
    <em>Lär dig att lösa valideringsfel.</em>
    <br>
  </td>
</tr>
</table>

*Fast (på fler sätt än ett)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Arbetsflöde för Adobe leads</strong></a>
    </div>
    <em>Huvudarbetsflöde för redigering för leadskrivare.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Sällan" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Arbetsflöde för användare med låg frekvens</strong></a>
    </div>
    <em>Inte en huvudskrivare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig de enklaste sätten att bidra. Inte en ledande författare? Lär dig det enklaste sättet att göra bidrag.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validering" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validering</strong></a>
    </div>
    <em>Lär dig att lösa valideringsfel.</em>
    <br>
  </td>
</tr>
</table>
