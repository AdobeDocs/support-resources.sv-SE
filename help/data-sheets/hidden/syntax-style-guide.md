---
title: Handbok för syntax och formatering för självbetjäning i samarbete med experter
description: En grundläggande introduktion till Markdown-format
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Guide för markeringssyntaxformat

På den här sidan visas markeringskomponenten för redigering av digital Experience Technical Documentation med hjälp av markeringsformatet (.md). Den här sidan innehåller information om anställda i Adobe.

EDS

Se här: [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>Titta på den här [AdobeDocs Markdown-videon](https://video.tv.adobe.com/v/26165).

För det mesta följer vi den standardiserade GIF-syntaxen (GIF) för textformatering. Vissa syntaxer (till exempel horisontella linjer) stöds inte och vi har utökat Markdown på flera sätt för att passa vår dokumentationsbehov.

## Grundläggande textformatering

Ett stycke kräver ingen speciell syntax i Markdown. Lägg till en tom rad mellan varje stycke.

Om du vill formatera text som **fet** omsluter du den med två asterisker:

```
This text is **bold**.
```

Om du vill formatera text som *kursiv* omsluter du den med en asterisk:

```
This text is *italic*.
```

Om du vill formatera text som både ***fet och kursiv*** omsluter du den med tre asterisker:

```
This is text is both ***bold and italic***.
```

Om du vill ignorera markeringsformateringstecken använder du `\` före tecknet:

`This is not \*italicized\* type.`

Återgiven: Detta är inte av typen \*kursiv\*.

## Märken

Pågår. Väntar på Loc.

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## Blockcitattecken

I vårt redigeringssystem används blockquotes-syntax (`>` i början av raderna) för att identifiera anpassade markeringstillägg för tips, anteckningar och videor. Du kan skapa riktiga blockcitattecken genom att lägga till ett `>`-tecken framför ett stycke.

>Det här är en blockoffert.

```
>This is a blockquote quotation.
```

## Kodblock (i rad){#code-block}

**När ska jag använda**

Används för att återge en del kod textbundet i en mening. Idealiskt att anropa ett cookie-namn, filnamn, värde eller kommando som inte kräver ett fullständigt kodsblock.

Innehåll i kodblock återges som de är och inte lokaliseras. (Det enda undantaget till den här regeln är `` och ``-syntax, som tas bort vid paketering för publicering.)

Använd även kodblock för exempel-URL:er som inte ska verifieras: `https://www.example.com`

**Syntax**

I ett kodblock används en enda bakterie för att omsluta det kodelement som du vill markera.

```
This is `inline code` within a paragraph of text.
```

**Exempel**

Detta är `inline code` i ett textstycke.

>[!TIP]
>
>Du kan också radbryta text i tre bakåtrutor (&grave;&grave;&grave;) för att skapa ett inline-kodblock. Detta är särskilt användbart när du behöver referera till ett bakåtskalstreck i ett textbundet kodblock. Exempel:
>
>&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;&grave;

## Kodblock (fäst)

**När ska jag använda**

Använd ett kodblock för att visa kodsyntax. I ett avgränsat kodblock används trippelbakterier för att omsluta det kodelement som du vill markera. Lägg till tomma rader ovanför och under det avgränsade kodblocket.

Observera att kodblock inte är lokaliserade.

>[!TIP]
>
>Ange ett språk när du skapar ett avgränsat kodblock. Om du anger ett språk kan syntaxmarkering bara användas för det språket och en **Kopiera**-knapp visas för användarna. Du kan också visa radnummer om du anger ett språk.

**Syntax**

Använd tre bakåtmarkeringar ( &grave;&grave;&grave; ) före och efter kodraderna. Se till att de öppna och avslutande rutorna är indragna med samma antal mellanslag. För optimal återgivning anger du ett kodspråk.

&grave;&grave;&grave;`javascript`

**Exempel**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### Syntaxmarkering för kodblock

Experience League har stöd för syntaxmarkering för kodblock. Se till att du anger ett språk som `java` efter den första uppsättningen bakåtmarkeringar för att säkerställa att syntaxen är korrekt markerad. En lista över giltiga språk finns på [https://prismjs.com](https://prismjs.com/#supported-languages). Om något språk saknas, logga ett jira-ärende.

### Radnumrering i kodblock

Lägg till `{line-numbers="true"}` efter språket för att aktivera radnumrering.

Exempel med radnummer (&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Börja numrering på rad _**

Lägg till `start-number="n"` efter radnummer-syntax för att starta numreringen på ett annat nummer än 1.

Exempel på ny startlinje (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Markering av rader i kodblock

Lägg till `highlight="n"` efter radnummer syntax för att markera rader inom ett kodblock. Om du anger `11-13, 16` markeras rad 11 till 13 och 16.

Exempel med radmarkering (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Variabel formatering i kodblock

Variabelsyntax som `<i>italic</i>` stöds inte i kodblock. Ett alternativ för att ange variabeltext är att använda vinkelparenteser `< >`.

## Komprimerbara avsnitt

Du kan skapa ett infällbart avsnitt (kallas ibland **dragspelspanel**) som är dolt som standard. Användaren kan klicka på titeln för att expandera eller komprimera avsnittet.

Komprimerbar text kan användas för att förenkla komplext innehåll, t.ex. effektivisera en sida med vanliga frågor och svar eller för att rensa en komplex procedur med kapslade listor. I stället för att visa en uppsättning delsteg kan du komprimera delstegen till ett&quot;Visa detaljer&quot;-avsnitt.

**Syntax**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**Exempel**

+++Se information
Det här är text i ett fällt avsnitt.

* Punkt ett
* Punkt två
* Punkt tre

+++

**Anteckningar**

+++* Kapsla inte infällbara avsnitt inuti fällbara sektioner. Kapslade komprimerbara avsnitt återges inte korrekt. De orsakar dock inte att valideringen misslyckas, så användarna ser syntaxen `` för det kapslade avsnittet.
* Se till att du lägger till tomma rader ovanför och nedanför objekt som punktlistor och kodblock inuti det komprimerbara avsnittet, annars får du ett valideringsfel.
* Du kan lägga till rubriker inuti fällbara avsnitt, men det rekommenderas inte.
* [Dragspel är inte alltid svaret på komplext innehåll på datorer](https://www.nngroup.com/articles/accordions-complex-content/)
* En historisk nackdel med komprimerbara avsnitt är att **Sök på sida** (Ctrl/Cmd+F) ignorerar komprimerad text. Det är fortfarande sant i Safari, men det är inte längre sant i Chrome; Find in Page identifierar dold text i Chrome.
* Exempel på en sida med [underhållsuppdateringar](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=sv-SE) med infällbara avsnitt.

## Kommentarer och kommentarer

Kommentarerna visas inte i det renderade hjälpsystemet. Använd kommentarer för att lämna anteckningar till dig själv eller andra skribenter. Du kan också använda kommentarer för textutkast.

När det gäller kommentarer bör du tänka på att även om de inte återges i hjälpsystemet så är de synliga för användare som redigerar markeringsfiler på GitHub.com. Ta inte med konfidentiell information i kommentarerna.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

Du bör inte kunna se text nedanför detta (&quot;Du kan inte se mig&quot;) om du inte redigerar dokumentet.

<!--
You can't see me (unless you're editing in Git).
-->

**Påminnelse:** Kommentarer (kommentarer) visas inte i de offentliga hjälpartiklarna. Kommentarer visas emellertid i de offentliga Markdown-filerna som användarna kan visa och redigera.

>[!IMPORTANT]
>
>Undvik att lägga till kommentarer i blockkomponenter som punktlistor, särskilt kapslade punktlistor. Kommentaren kan ändra hur punktlistan återges.
>
>Kommentera inte rader i mitten av innehållsförteckningslistan i filen TOC.md. Detta kan göra att innehållsförteckningslistan delas upp och orsaka valideringsfel. Flytta i stället kommentarerna i innehållsförteckningen till slutet av filen.

## CONTEXTUALHELP

Författare kan arbeta med produktteam för att lägga till hjälppuffar i användargränssnittet för Experience Cloud eller Experience Platform. Exempel:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## Definitionslistor

För definitionslistor har vi ännu inte stöd för standardsyntaxen Markdown. Använd i stället manuell formatering så här:

```
**Frog** - An amphibious green creature. Likes flies.
```

Återgiven:

**Groda** - en grov grön varelse. Som flugor.

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## Hämta filer

Ladda upp ZIP-filen eller någon annan hämtningsbar fil till katalogen assets och länka sedan till den. Om det är en ZIP-fil laddas filen ned om du klickar på länken. Om det är en filtyp, till exempel PDF eller PNG, som kan öppnas i en webbläsare, öppnas en ny flik när du klickar på länken. För sådana filer bör du överväga att zippa upp dem eller ge instruktioner om hur du högerklickar på länken och hämtar dem.

`Download` &lbrack;`download-test.zip`&rbrack;`(assets/download-test.zip)`

Återgiven:

Hämta [test-zip](assets/download-test.zip)

>[!NOTE]
>
>Den maximala filstorleken för nedladdningsfiler och bilder är 100 MB. Det är gränsen för github.com. git.corp.adobe.com är högre (250 MB), men vi måste kunna kopiera filer till github.com.

## Rubriker {#headings}

I Markering använder du nummertecken (`#`) för att identifiera rubriknivåer. Den första nivån (`#`) är artikelrubriken, som också anges i metadatahuvudet. Behåll dessa värden. Den andra nivån (`##`) representerar de huvudrubriker på sidan som ska inkluderas i miniinnehållsförteckningen. Om du är van vid att skriva i AEM (chl-author) mappas rubriknivå 2 (`##`) till komponenten &quot;Heading 1&quot; i AEM.

Högsta antal tecken för rubriker: 69 tecken (engelska) / 120 tecken (LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**Bästa praxis för rubriker**

* Kontrollera att en rubrik på nivå 1 (`#`) följer en tom rad efter metadata i varje artikel.
* Hoppa inte över nivåer, till exempel hoppa från nivå 2 (`##`) till nivå 4 (`####`).
* Inkludera en tom rad *före* och *efter* för varje rubrik.
* Om en rubrik innehåller siffror anger du ett explicit rubrik-ID som inte börjar med en siffra, till exempel `## Release notes for 2016 {#release-notes-2016}`.
* Vi rekommenderar endast tre rubriknivåer. Nivåer 4 och senare återges för närvarande inte korrekt.
* Rubriker visas i den högra navigeringen så att användarna kan klicka för att gå till ett avsnitt. Som standard visas två rubriknivåer i den högra navigeringen. Om du vill ändra antalet nivåer använder du `mini-toc-levels`-metadata, till exempel `mini-toc-levels: 3`.

**Rubrik-ID**

Rubrik-ID (kallas även *ankar-ID*) används för att skapa anpassade djuplänkar till avsnitt i artiklar. Använd det här formatet om du vill ange ett rubrik-ID:

```
## Creating processing rules {#processing-rules}
```

Rubrik-ID:n ska vara gemener och avstavade.

Om du inte anger ett rubrik-ID för en rubrik är standardrubrikens ID &quot;instruerad&quot; (gemener och avstavade) rubrik. Rubriken `## Creating widgets and Such` får till exempel ett `#creating-widgets-and-such`-ankare.

## HTML syntax {#html}

Av olika anledningar, bland annat för säkerhet och tillgänglighet, begränsar vi HTML-syntaxen som kan användas för markeringar. I följande lista visas vilken HTML-syntax som stöds. Alla HTML-syntaxer som inte finns med i den här listan resulterar i ett valideringsfel.

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

Om du vill lägga till HTML-syntax i listan loggar du en biljett eller kontaktar SSE-teamet.

## Bilder {#images}

Använd syntaxen `![]()` för bilder. Hakparenteserna `[ ]` innehåller alternativ text, och parenteserna `( )` innehåller bildens plats och valfri hovringstext (verktygstips). Exklamationsmärket skiljer en bild från en länk.

```
![alt text](assets/logo.png "Hover text")
```

![Alt-text](assets/logo.png "Hovringstext")

För delade bilder kan du placera bilderna i en rotresursmapp och sedan använda en rotlänk som fungerar från vilken fil som helst i ett svar:

```
/help/assets/imagename.png
```

### Ändra storlek på och justera bilder

**Bildegenskaper (med högerjusterad bild)** ![Alt-text](assets/premium.png "Premium-hover-text"){align="right"}

Använd syntax som följande om du vill ändra bildens standardbredd eller mittpunkt eller högerjustera bilden i sidvyn eller tabellcellen.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

Återgiven:

Bob - Bredd = 300 pixlar under

![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}

* För stora bilder rekommenderar vi att du skapar bilder som är tillräckligt stora för att skalas ned för att få plats inom sidbredden - minst 640 pixlar breda. Rekommenderad bredd är 1 500 pixlar. Du behöver inte skapa bilder som är större än 2 500 pixlar eller 5 000 kilobyte. Den största filstorleken för bilder är 100 MB.
* För små bilder skapar du bilder med önskad bredd i pixlar eller använder breddparametern, till exempel `{width="250"}` (pixlar) eller `{width="50%"}` (procentandel av visningsområdet, inte den ursprungliga bildstorleken). Bilder skalas proportionellt. Observera att bilder kan skalas upp eller ned, så var försiktig med pixelering.
* I vissa fall kommer bilder från samma gränssnitt att se oproportionella ut på sidan eftersom bredare bilder (t.ex. ett verktygsfält) skalas ned medan smala bilder (t.ex. en panel) inte skalas ned. I sådana fall bör du överväga att skala ned de bredare bilderna för att få bättre visuell enhetlighet.
* Du kan ändra justeringen för en bild i visningsområdet. Använd antingen `{align="center"}` eller `{align="right"}`. Parametern `valign` stöds inte.

>[!NOTE]
>
>Den största filstorleken för bilder är 100 MB. Det är gränsen för github.com. git.corp.adobe.com är högre (250 MB), men vi måste kunna kopiera filer till github.com.

### Bildlänkar

Använd det här formatet om du vill tillåta användare att klicka på en bild för att hoppa till en annan sida.

**Syntax**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**Exempel**

Klicka på den här bilden för att gå till webbplatsen Adobe.

[![bild](assets/core-services_96.png)](https://www.adobe.com)

### Klicka för att zooma bilder

Använd parametern `zoomable` om du vill tillåta användare att klicka på en bild för att visa en förstorad version av bilden. När användaren för musen över en zoombar bild blir pekaren ett förstoringsglas. När du klickar på bilden utökas den till webbläsarens hela bredd. Den kan stängas med en stängningsknapp.

**Exempel**

![Skapar en bild](/help/data-sheets/hidden/assets/maui-dive.jpg "Skapas i Maui"){width="100" zoomable="yes"}

**Syntax**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## Länkar och korsreferenser {#links-and-cross-references}

Externa länkar är raka framåt och kan återges som en länkad bildtext eller en ren URL-adress.

```
[Adobe](https://www.adobe.com)
```

Återgiven:

[Adobe](https://www.adobe.com)

Om du lägger till en URL-adress direkt i texten konverteras den inte automatiskt till en länk. Om du vill att en URL ska visas som en länk lägger du till syntaxen `< >`. Exempel:

```
https://www.adobe.com

<https://www.adobe.com>
```

Återgiven:

https://www.adobe.com

<https://www.adobe.com>

Länkar till artiklar (korsreferenser) kan vara lite mer komplicerade.

**Alternativ 1: Standardrelativ länk**

Så här ser en relativ länk ut:

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

Sökvägen måste ta hänsyn till både källfilens och målfilens plats. Du kan använda alla relativa länkoperander, till exempel `./` (aktuell katalog), `../` (bakåt en katalog) och `../../` (bakåt två kataloger).

**Alternativ 2: Rotrelativ länk**

Fördelen med den här typen av länk är att den bara behöver ta hänsyn till målfilen. Den fungerar från alla källfiler i rapporten, oavsett var källfilen finns.

```
/help/using/docile-rules/introduction.md
```

**Djuplänkning**

Om du vill länka till en rubrik i en artikel måste målrubriken ha ett explicit rubrik-ID (kallas även för ett ankar-ID). Exempel:

`## Creating audience segments {#creating-audience-segments}`

Om du vill länka till den här rubriken på samma sida använder du rubrik-ID som länk:

`See [Creating audience segments](#creating-audience-segments)`

Om du vill länka till den här rubriken från en annan artikel i svaret lägger du till suffixet för rubrik-ID i slutet av länken:

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**Öppna i ny flik**

Om du vill att en länk ska öppna en ny flik, till exempel när du går till en annan stödlinje, använder du egenskapen `{target="_blank"}` i länken.

Exempel:

`[See What's new](whats-new.md){target="_blank"}`

## Metadata

Lägg till metadata högst upp i markeringsfilen. Nästa rad efter metadataraden (och tom rad) MÅSTE vara artikelrubriken (# Title).

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## Lokaliseringstaggar: UICONTROL, DNL och DONOTLOCALIZE

Allt vårt Markdown-hjälpinnehåll lokaliseras till att börja med med med maskinöversättning. Om hjälpen aldrig har lokaliserats behåller vi maskinöversättningen. Om hjälpinnehållet tidigare har lokaliserats fungerar maskinöversatt innehåll som platshållare medan innehållet håller på att översättas av människor.

## Mer som detta

Använd komponenten &quot;Mer som den här&quot; för att visa relaterade länkar i slutet av en artikel. Komponenten MORELIKETHIS återges som&quot;Related Articles&quot; (och lokaliseras på andra språk) när den återges.

**Syntax**

![Mer som den här syntaxen](assets/morelikethis.png)

**Exempel**

>[!MORELIKETHIS]
>
>* [Artikel 1](https://helpx.adobe.com/se/support/analytics.html)
>* [Artikel 2](https://helpx.adobe.com/se/support/audience-manager.html)

## Anteckningar/tillägg

Vi har utökat Markdown för att formatera olika typer av anteckningar: Obs!, Tips, Viktigt och Varning.

**Syntax**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**Exempel**

>[!NOTE]
>
>Det här är ett vanligt anteckningsblock.

**Syntax**

```
>[!TIP]
>
>This is a standard tip.
```

**Exempel**

>[!TIP]
>
>Det här är ett standardtips.

**Syntax**

```
>[!WARNING]
>
>This is a standard warning block.
```

**Exempel**

>[!WARNING]
>
>Detta är ett standardvarningsblock.

**Syntax**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**Exempel**

>[!IMPORTANT]
>
>Detta är ett viktigt standardblock.

**Syntax**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**Exempel**

>[!NOTE]
>
>Det här är ett vanligt anteckningsblock.
>
>Det innehåller flera stycken.

Nya anteckningstyper som stöds:

>[!ADMIN]
>
>Det här är en administratörsanteckning. Endast EXL.

>[!AVAILABILITY]
>
>Det här är en tillgänglighetsanteckning. Endast EXL.

>[!PREREQUISITES]
>
>Detta är en kravanteckning. Endast EXL.

>[!INFO]
>
>Det här är en informationsanteckning. Endast EXL.

>[!ERROR]
>
>Det här är en felanteckning. Endast EXL.

>[!SUCCESS]
>
>Detta är en framgångsanteckning. Endast EXL.

## Numrerade listor och punktlistor {#lists}

Om du vill skapa numrerade listor börjar du en rad med `1.` eller `1)`, men väljer en metod och använder den konsekvent i artikeln. Du behöver inte ange siffrorna. GitHub gör det åt dig.

Använd numret `1` för varje steg i den numrerade listan.

Lägg till tomma rader före och efter listor.

**Syntax**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**Exempel**

1. Detta är steg 1.

   1. Delsteg

   1. Delsteg

1. Detta är nästa steg.

1. Detta är ännu ett steg, det tredje.

Om du vill skapa punktlistor börjar du en rad med `*`, `-` eller `+`, men väljer en metod och använder den konsekvent i artikeln. (Om du blandar formaten, till exempel `*` och `+`, visas ett markeringsvalideringsfel när du checkar in filen.)

**Bästa praxis:** Använd `*` för punkter. I Visual Studio Code används asterisken för punktlistor, så det är enklare att hålla dig med asterisker för att automatisera skapandet av en osorterad lista. (Du kanske har märkt att filen TOC.md använder plustecken `+` för listor. Det är en hållplats från migrationen. Alla giltiga punkter fungerar så länge de är konsekventa i artikeln.)

**Syntax**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**Exempel**

* Första objektet i en osorterad lista.
* Ett annat objekt.
* Här är vi igen.

Du kan även bädda in listor i listor och lägga till innehåll mellan listobjekt. Dra in innehåll mellan listobjekt för att undvika att starta en ny lista. Objekt mellan steg bör dras in till början av texten: 3 blanksteg för numrerade listor och 2 blanksteg för punktlistor.

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**Exempel**

1. Skapa tabeller och kodblock.
1. Utför det här steget.

   ![skärm](assets/core-services_96.png)

1. Se till att tabellen ser ut så här:

   | Hej | World |
   |---|---|
   | Hur | Är du? |

1. Detta är det fjärde steget.

   >[!NOTE]
   >
   >Det här är anteckningstext.

1. Gör ett steg till.

   Det här är en indragen linje.

Obs! Om du drar in för långt, till exempel 6 blanksteg i stället för 3, behandlas innehållet på den raden som ett kodblock.

## Skuggningsrutor

Skuggrutor är användbara när du vill ställa in ett avsnitt av innehållet från resten av sidan. Workfront-teamet vill till exempel lägga till exempelrutor som innehåller text, bilder och kodexempel för att uppnå ett visst syfte. En skuggningsruta kan också vara användbar för avsnitten&quot;På egen hand&quot; eller&quot;Använd skiftläge&quot;, eller för utökade anteckningar eller tips.

Om du vill skapa en skuggruta lägger du till `>[!BEGINSHADEBOX]` i början av avsnittet och `>[!ENDSHADEBOX]` i slutet. Allt innehåll mellan dessa start- och sluttaggar har en grå bakgrund. Att lägga till en etikett till `BEGINSHADEBOX` (till exempel `>[!BEGINSHADEBOX "Use Case]`) är ett valfritt sätt att skapa en textruta med fet ton. Du kan också lägga till fet text eller en rubrik på nästa rad.

Exempel:

>[!BEGINSHADEBOX]

**Tar bort kantlinjen i en HTML-tabell**

I vissa fall använder du en HTML-tabell för att skapa en balanserad design, men du vill inte att innehållet ska se ut som en tabell. Om du vill inaktivera kantlinjen för en HTML-tabell med en rad använder du följande syntax:

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
>Överdriv inte. För vanliga tabeller vill vi ha en enhetlig design för hela innehållet.

![tabelltips](assets/table-no-border.png)

I en tabell med tre kolumner kan du också lägga till `<td align="center">` och `<td align="right">` för att fördela cellinnehållet jämnt över visningsområdet. Om det inte vore så, skulle jag ha sagt det till dig.

Det här är den sista raden i skuggrutan.

>[!ENDSHADEBOX]

## Fragment och inkluderar

Om du vill dela text mellan artiklar i ett svar skapar du en `_includes`-mapp i mappen `help`. Den här `_includes`-mappen kan ha .md-filer som kan refereras (inkluderas) från andra filer i svaret. Dessutom kan en `snippets.md`-fil i den här rapporten innehålla Head2-ankarpunkter som kan refereras från vilken fil som helst i svaret.

Referens till H2 i filen snippets.md: `{{id-name}}`

Referens till inkluderingsfil: `{{$include /help/_includes/filename.md}}`

## Tabeller

Tabeller kan vara problematiska i kod. När tabeller migreras från det tidigare redigeringssystemet formateras enkla tabeller (en rad per cell) som interna markeringstabeller (standard). Mer avancerade tabeller formateras som HTML.

>[!TIP]
>
>Titta på videon [Markup Tables](https://video.tv.adobe.com/v/26220)

Inbyggda tabeller ser ofta bättre ut i Markdown. Kolumnernas storlek beror på deras innehåll. HTML-tabeller återges med kolumner med samma bredd.

Markering stöder som standard inte flera rader eller listor i celler. Vi har emellertid utökat Markdown-tabeller så att flera rader tillåts i celler (med `<p>` eller `<br>`) eller grundläggande listor (med `<ul><li>` etc.).

>[!IMPORTANT]
>
>Var försiktig när du lägger till de här HTML-koderna i markeringstabeller. Om syntaxen är felaktig får du ett förvirrande valideringsfel som inte korrekt beskriver problemet. Kontrollera HTML-syntaxen för att se till att den är korrekt formaterad.

Inte tillåtet i någon tabell: iframes, cellintervall eller inbäddade tabeller.

Inte tillåtet i ursprunglig markeringstabell: kapslade eller komplexa listor.

Se [Tabeller](tables.md)

**Syntax**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**Exempel**

| Sidhuvud | En annan rubrik | Ännu en rubrik |
|--- |--- |--- |
| rad 1 | rad 1 kolumn 2 | rad 1 kolumn 3 |
| rad 2 | rad 2 kolumn 2 | rad 2 kolumn 3 |

Enkla tabeller fungerar korrekt i Markdown. Tabeller som innehåller flera stycken eller listor i en cell är emellertid svåra att arbeta med. För sådant innehåll rekommenderar vi att du använder ett annat format, t.ex. rubriker och text.

**Markeringstabell med styckebrytningar och listor**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**Exempel**

| Sidhuvud | En annan rubrik | Ännu en rubrik |
|------------|----------|----------------|
| rad 1 | första stycket i cellen<p>andra stycket i cell(`<p>`)<br>radbrytning (`br`) | rad 1 kolumn 3 |
| rad 2 | punktlista<ul><li>objekt 1</li><li>objekt 2</li><li>objekt 3</li></ul> | rad 2 kolumn 3 |

**Markeringsregister med radbrytningar och falsk lista**

Tillfällig lösning med manuella punkter.

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**Exempel**

| Färg | Saker att göra |
|--- |--- |
| Röd | * Läs <br> * Skriv <br> * Studie |
| Blå | * Swim <br> * Kör <br> * Lyft <br> **Obs!**: Kom ihåg att träna smart. |


## Tabbar

En flik är ett klickbart område högst upp i ett avsnitt som visar olika innehåll. När du klickar på en tabb visas flikens innehåll och innehållet på andra flikar döljs.

Om du vill skapa en flikuppsättning lägger du till `>[!BEGINTABS]` i början av flikuppsättningen och `>[!ENDTABS]` efter den sista fliken. Lägg till `>[!TAB <tab title>]` taggar för varje flikavsnitt och lägg till innehållet för varje flik under det.

**Fliksyntax**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**Återgiven**

>[!BEGINTABS]

>[!TAB iOS]

Innehållet visas på fliken iOS.

>[!TAB Android]

Innehållet visas på fliken Android.

>[!TAB Windows]

Det här innehållet visas på fliken Windows.

>[!TAB MacOS]

Innehållet visas på fliken MacOS.

>[!TAB Linux]

Det här innehållet visas på fliken Linux.

>[!ENDTABS]

**Flikanteckningar**

* Användare kan inte använda sidsökning (Ctrl+F/Cmd+F) för att hitta innehåll på flikar som inte visas.
* Om tabbtitlarna sträcker sig utanför sidvyns bredd i användarens webbläsare visas en vågrät rullningslist.
* Du kan inte formatera tabbtitlarna. Alla syntaxer som du lägger till skickas som en del av titeln. `>[!TAB **iOS**]` visas till exempel som `**iOS**`.
* Du kan skapa flera tabbuppsättningar på en sida, men du kan inte kapsla in en tabbuppsättning i en annan tabbuppsättning.
* En skuggad bakgrund används på tabbuppsättningen så att användarna kan se skillnad på tabbinnehållet och annat innehåll.

## Textmarkering

Workfront-teamet bad om att kunna använda gul markering för att indikera förhandsgranskning av kommande funktioner. Så fungerar det

Exempel:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Återgiven:

Hela stycket ska INTE markeras. <span class="preview"> Det här ordet är **fetstil** inuti en markerad mening.</span> Och det här är bara den sista meningen.

Som allmän regel bör du använda `<span class="preview">` för att markera ett stycke eller en text i ett stycke och sedan använda `<div class="preview">` för flera stycken och komponenter.

>[!NOTE]
>
>Vi arbetar fortfarande med att förbättra färgmarkeringen för vissa sidelement som anteckningar och tabeller. Du kan logga JIRA-fel om du ser felaktig återgivning. Pågår.
>
>VSC-förhandsgranskning stöder ännu inte markering.

## Video

Videor återges inte internt i Markdown. Om du vill visa en textbunden video använder du komponentindikatorn `[!VIDEO]` och sedan webbadressen.

**Syntax**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**Exempel**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## Ytterligare syntaxinformation för markering

### Utökade markeringskomponenter

Vi måste utöka Markdown för att kunna hantera objekt som inte ingår i den gemensamma markeringen.

Specialkomponenter deklareras i ett innehållande blockcitat med hakparenteser och ett utropstecken plus referensen för den typ av block det är. Så här deklarerar du en anteckning:

```
>[!NOTE]
>
>This is a note.
```

* Anteckningar (tillägg), inklusive Anteckningar, Viktigt, Tips, Varning och Varningar
* Inbäddad video
* Mer som detta (relaterade artiklar)
* Olika gränssnittstaggar för lokalisering
* Komponentegenskaper för rubriker, bilder och kodblock
* Komprimerbara avsnitt
* Textmarkering
* Sidflikar

Använd markeringsblockcitattecknet ( `>`) i början av varje rad för att koppla samman en styckebaserad komponent, till exempel en anteckning. Om du vill förbättra förhandsgranskningen lägger du till en rad omedelbart efter början av avsnittet som bara har en blockcitattecken (`>`). Lägg till en tom rad för att avsluta avsnittet.

Om du behöver använda underkomponenter i komponenter lägger du till en extra nivå med blockcitattecken (`>  >`) för det underkomponentavsnittet. En NOTE i ett DONOTLOCALIZE-avsnitt ska till exempel börja med `>  >`.

I vissa fall måste vi ha stöd för särskilda inställningar för markeringselement som rubriker. Om du behöver ändra standardinställningarna lägger du till parametrarna inom klammerparenteser `{# }` efter komponenten.

### Tomma rader

Du kan lägga till lite andningsrum till textväggar med tomma linjer. Använd `<br>&nbsp;` som en tillfällig lösning om du vill lägga till en tom rad.

Exempel: Detta är en första mening i vad som kan vara en väldigt lång text. Låt mig infoga en tom rad mellan det här stycket och nästa.

<br> 

Det här kanske inte verkar särskilt imponerande här, men prova med tomma rader när du tycker att sidorna är för fyllda.

### Tecken som ska&quot;escape&quot; {#characters-to-escape}

Flera tecken (`# { } [ ] < > * + - . !`) har en speciell innebörd i Markdown eller HTML för att skapa rubriker, bilder, listor och andra komponenter. När du använder dessa tecken tror återgivningsmotorn att du lägger till kod. I vissa fall vill du dock visa dessa tecken i texten. Om du vill göra det måste du&quot;fly&quot; från karaktärerna. Den enklaste escape-metoden är att lägga ett omvänt snedstreck (`\`) före tecknet. Om du till exempel vill starta en rad med ett `#`-tecken så att det inte tolkas som en rubrik skriver du `\#`:

`\# This is not a heading`

**Återgiven:**

\# Det här är inte en rubrik

Det omvända snedstrecket fungerar bara med följande tecken: `# { } [ ] * + - . !`. Om du behöver undvika tecken som vinkelparenteser (till exempel `<yourname>`) kan du antingen omsluta texten i bakåttickningar för att använda ett textbundet kodblock, eller använda enhetskoden HTML i stället för tecknet. Exempel på vanliga HTML-koder:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

En fullständig lista över HTML-entiteter finns på webbplatsen [FreeFormatter](https://www.freeformatter.com/html-entities.html). Då kan du slå upp alla specialtecken.

>[!NOTE]
>
>För kedjesteg som &quot;Välj Arkiv > Spara som&quot; behöver du inte kringgå tecknet `>` eftersom det inte finns bredvid andra tecken. För variabler som `<filename>` vill du undvika vinkelparenteserna med kodblocket `backticks` eller teckenkoderna (`&lt;filename&gt;`).

Om du använder HTML-enheter i kodblock konverteras inte enhetstexten till specialtecknet. `&gt;` visas till exempel i ett kodblock som `&gt;` i stället för >.

Om du vill undvika bakåtfästingar (&grave; ) använder du `&grave;` eller infogar bakstrecket inom tre bakåtfästingar som omsluter ett textbundet kodblock.

### Objekt som inte stöds

Det finns några Git-smaksatta Markdown-objekt som vi inte tänker stödja. Förhandsvisningsverktyget som du använder kan aktivera vissa av de här funktionerna, men lita inte på det.

**Uppgiftslista**

Stöds inte

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**Emoji**

Stöds inte

```
:bowtie:
```

**Vågrät linje**

Stöds inte

```
***
```

**Blockcitattecken**

Vi använder blockcitattecken (`>` i början av en rad) för att indikera utökad markeringssyntax, som anteckningar och videoklipp, som beskrivs nedan. Men du kan också använda syntaxen `>` för att skapa ett avsnitt med blockcitattecken.

>[!NOTE]
>
>Om du drar in för långt, till exempel sex blanksteg i stället för tre, återges innehållet som en blockcitat. Använd rätt mängd indrag för att undvika att innehållet återges felaktigt som ett blockcitat.
