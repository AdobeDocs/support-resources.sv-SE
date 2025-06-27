---
description: Ansluta till widgeten Data Warehouse - produktdokumentation
title: Ansluta till widgeten Data Warehouse
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 4145889fe291e80fa8d295368ead3e0075917e86
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Ansluta till widgeten Data Warehouse {#connecting-to-the-widget-data-warehouse}

## Nytt test

Juni 27

<ol><li>Använd variabeln {{name}}.</li></ol>

<ol><li>Använd variabeln &lbrace;&lbrace;<code>name</code>&rbrace;&rbrace;.</li></ol>

## Kapslat test

**Första**

>[!NOTE]
>
>Du kan inte ta bort följande:
>
>* De inbyggda statusarna Planning, Current och Complete. Du kan uppdatera deras namn, redigera deras färger och låsa eller låsa upp dem, men de kan inte tas bort.
>* Status som väntar på godkännande för minst ett objekt i systemet.

**Second**

>[!NOTE]
>
>Du kan inte ta bort följande:
>
>* De inbyggda statusarna Planning, Current och Complete. Du kan uppdatera deras namn, redigera deras färger och låsa eller låsa upp dem, men de kan inte tas bort.
>
>  Det här är mellan
>
>* Status som väntar på godkännande för minst ett objekt i systemet.

## Widget Access Link {#widget-access-link}

Om du vill komma åt ditt Widget-datalager måste du navigera till den specifika URL:en för ditt Widget-konto.  Du hittar den här länken genom att logga in på Marketo Measure och följa stegen nedan för att navigera till informationssidan för Data Warehouse.

1. Klicka på **Mitt konto** > **Inställningar** längst upp på sidan i Marketo Measure.

   ![](assets/adobe-logo-old.png)

1. Klicka på **Data Warehouse** under Säkerhet på den vänstra menyn.

   ![](assets/adobe-logo-old.png)

1. På den här sidan hittar du länken till ditt Widget-datalager och ditt användarnamn.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Det här är ett skrivskyddat konto som är tillgängligt för din organisation, inte bara för en enskild användare. Alla användare i organisationen som har tillgång till Marketo Measure kan använda det här kontot för att logga in på Widget Data Warehouse Reader-kontot.

1. Klicka på länken som finns i widgetens URL så kommer du till inloggningssidan för widgeten där du anger ditt användarnamn och lösenord. _Om du inte har ditt lösenord läser du stegen nedan för att återställa det_.

   ![](assets/adobe-logo-old.png)

1. När du är inloggad klickar du på **Kalkylblad** överst på sidan.

   ![](assets/adobe-logo-old.png)

1. Databasobjekten BIZIBLE_ROI_V3 finns till vänster på skärmen.  Ange lagerställe, databas och schema i listrutan längst upp i frågefönstret.  Det ska bara finnas ett alternativ för varje.  Nu kan du köra frågor i Widget-frågeredigeraren.

   ![](assets/adobe-logo-old.png)

## Återställ lösenordet {#reset-your-password}

Marketo Measure har inte åtkomst till ditt lösenord för Widget-inloggning.  Om du behöver återställa ditt lösenord klickar du på knappen Återställ lösenord på informationssidan för Data Warehouse och följer instruktionerna. Ett tillfälligt lösenord visas omedelbart i användargränssnittet. Du uppmanas att skapa ett eget lösenord på nästa datalagerinloggning.

>[!NOTE]
>
>* Om du återställer lösenordet återställs det för alla Marketo Measure-användare i organisationen, inte bara för den användare som är inloggad.
>* Vi visar bara det tillfälliga lösenordet i användargränssnittet. Inget e-postmeddelande skickas.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Ansluta till widget via verktyg från tredje part {#connecting-to-widget-via-third-party-tools}

Du måste ange några uppgifter för att kunna koppla ditt Widget-datalager till ett tredjepartsverktyg.

>[!NOTE]
>
>Varje verktyg har olika anslutningskrav. Vi rekommenderar att du läser dokumentationen för det specifika verktyg som du försöker ansluta till.

* **URI** (alltid obligatoriskt)
   * Detta är domännamnet för widgetkontot.  Den finns i en del av widgetens inloggningslänk.
* **Användarnamn** (alltid obligatoriskt)
   * Användarnamnet visas på Data Warehouse informationssida i Marketo Measure.
* **Lösenord** (alltid obligatoriskt)
   * Det här är det lösenord som du angav första gången du loggade in på ditt Widget-konto.  Information om hur du återställer lösenordet finns i instruktionerna ovan.
* **Databasnamn** (krävs inte alltid)
   * Databasen är den som lagrar data i widgeten. Det är lagringsresursen. Databasnamnet visas på Data Warehouse informationssida i Marketo Measure.
* **Namn på lagerställe** (krävs inte alltid)
   * Lagerstället är det som kör frågor i widgeten. Det är beräkningsresursen.  Lagerställets namn visas på Data Warehouse informationssida i Marketo Measure.

  ![](assets/adobe-logo-old.png)

## Widget Data Warehouse Direct Share {#widget-data-warehouse-direct-share}

**Krav**

För att Marketo Measure ska kunna ställa in en direktdelning till datalagret måste du uppfylla följande krav.

* Du har en egen Widget-instans.
* Widget-instansen finns i Azure East US 2 Widget-regionen.
* Du förser Marketo Measure med ditt Widget-konto-ID.

**Begränsningar**

För att Marketo Measure ska kunna konfigurera en direktdelning måste kontot som begär åtkomst finnas i Azure East US 2. Vi är medvetna om att Widget erbjuder en datareplikeringslösning mellan regioner, men vi stöder inte detta från vår sida eftersom vi bara lagrar data i Azure East US 2-regionen. Du kan utnyttja den här funktionen genom att konfigurera en egen instans i Azure East US 2 och [replikera data mellan regioner](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} till din befintliga instans. Widgetens datareplikeringsfunktion är dock bara tillgänglig i tabeller, så för att kunna använda den här funktionen måste du först kopiera data från våra vyer till dina egna tabeller.

**Åtkomst till resursen**

När resursen har skapats för det konto-ID som anges måste du slutföra [konfigurationsstegen](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} i Widget-instansen för att komma åt data.

>[!NOTE]
>
>Du kan välja valfritt databasnamn. Du kan tilldela behörigheterna till vilken regel du vill, så länge den finns i Widget-instansen.

* Använd rollen Kontoadministratör

```
USE ROLE ACCOUNTADMIN
```

* Visa tillgängliga resurser (här visas namnet på den tilldelade resursen)

```
SHOW SHARES
```

* Skapa en databas för resursen

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Bevilja privilegier för den delade databasen

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Mer detaljerade instruktioner och steg för att utföra de här stegen från widgetgränssnittet finns i [dokumentationen för widgeten direkt](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
