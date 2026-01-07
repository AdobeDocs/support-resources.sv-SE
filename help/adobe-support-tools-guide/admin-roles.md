---
title: Administrativa roller
description: Med Adobe Admin Console kan man definiera en flexibel administrativ hierarki som detaljerat kan hantera åtkomst och användning av Adobe-produkter.
solution: Admin Console
source-git-commit: a96f8be10d63d4f1f40738d533147c22de9b5482
workflow-type: tm+mt
source-wordcount: '1593'
ht-degree: 0%

---

# Administrativa roller

Med Adobe Admin Console kan man definiera en flexibel administrativ hierarki som detaljerat kan hantera åtkomst och användning av Adobe-produkter. En eller flera systemadministratörer, som etablerats under företagets introduktionsprocess, är högst upp i hierarkin. Dessa systemadministratörer kan delegera ansvar till andra administratörer, men behåller den övergripande kontrollen.

Administrativa roller ger följande viktiga fördelar för företag:

* Kontrollerad decentralisering av det administrativa ansvaret
* Snabböversikt över produkttilldelningar - per användare och produkt
* Funktioner för att tilldela kvoter till produktadministratörer

## Administrativ hierarki

Gäller för: Adobe företagskunder.

Den administrativa hierarkin kan användas för att passa företagets unika behov. Ett företag kan till exempel utse olika administratörer för att hantera berättiganden för Adobe Creative Cloud- och Adobe Marketing Cloud-erbjudanden. Ett företag kan också ha olika administratörer för att hantera berättiganden för användare som tillhör olika affärsenheter.

>[!NOTE]
>
>Den administrativa hierarkin gäller inte för teamkunder. Teamkunder har en enda **systemadministratörsroll**. Kontraktsägaren (_som tidigare kallats **primär administratör**&#x200B;_) är systemadministratören med tillgång till avtalsinformationen och faktureringshistoriken. Om du är den nuvarande avtalsägaren kan du utse en befintlig systemadministratör (_ som tidigare kallats **sekundär administratör**&#x200B;_) som avtalsägare.

![administratörsbild](assets/storage_admin.png)

_Hierarki för administratörsroller_

| Roll | Beskrivning |
|--- |--- |
| **Systemadministratör** | Superanvändare för organisationen; kan utföra alla administrativa uppgifter i Admin Console.<br>Har även behörighet att delegera följande administrativa funktioner till andra användare: produktadministratör, produktprofiladministratör, administratör för användargrupp, distributionsadministratör och supportadministratör. |
| **Produktadministratör** | Administrerar de produkter som kopplats till den aktuella administratören och alla tillhörande administrativa funktioner, som omfattar:<ul><li>Skapa produktprofiler</li><li>Lägga till användare och användargrupper i organisationen men inte ta bort dessa</li><li>Lägga till eller ta bort användare och användargrupper från produktprofiler</li><li>Lägga till eller ta bort produktprofiladministratörer från produktprofiler</li><li>Lägga till eller ta bort andra produktadministratörer från produkten</li><li>Lägga till eller ta bort gruppadministratörer från grupper</li></ul> |
| **Produktprofiladministratör** | Administrerar beskrivningar av produktprofiler som tilldelats den aktuella administratören och alla tillhörande administrativa funktioner, som omfattar:<ul><li>Lägga till användare och användargrupper i organisationen men inte ta bort dessa</li><li>Lägga till eller ta bort användare och användargrupper från produktprofiler</li><li>Tilldela eller återkalla produktbehörigheter till användare och användargrupper från produktprofiler</li><li>Hantera produktroller för användare och användargrupper för produktprofiler |
| **Administratör för användargrupp** | Administrerar de användargruppsbeskrivningar som kopplats till den aktuella administratören och alla tillhörande administrativa funktioner, som omfattar:<ul><li>Lägga till eller ta bort användare från grupper</li><li>Lägga till eller ta bort administratörer för användargrupper från grupper |
| **Distributionsadministratör** | Skapar, hanterar och distribuerar programvarupaket och uppdateringar till slutanvändare. |
| **Support Admin** | Icke-administrativ roll som har tillgång till supportrelaterad information, t.ex. kundrapporterade problemrapporter. |
| **Lagringsadministratör** | Hanterar organisationens lagringsadministration. Administratören kan visa lagringsförbrukningen för både aktiva och inaktiva användare och överföra innehåll till andra mottagare. |

En detaljerad lista över behörigheter för varje administratörsroll finns i [Behörigheter](#enterprise-admins-permissions-matrix).

## Lägg till en företagsadministratörsroll {#add-enterprise-role}

Gäller för: Adobe företagskunder.

Som administratör kan du tilldela en administratörsroll till andra användare och ge dem samma behörigheter som du har, eller behörigheter för en roll under din administratörsroll i hierarkin enligt beskrivningen [ovan](#administrative-hierarchy). Som produktadministratör kan du till exempel ge en användare administratörsbehörighet för produkt eller produktprofil, men inte distributionsadministratörsbehörighet. Behörigheterna för Admin Console finns i [Behörighetsmatrisen](#enterprise-admins-permissions-matrix).

Så här lägger du till eller bjuder in en administratör:

1. I **[[!UICONTROL Adobe Admin Console]](https://adminconsole.adobe.com/)** väljer du **[!UICONTROL Users]** > **[!UICONTROL Administrators]**.

   Du kan också gå till den relevanta produkten, produktprofilen eller användargruppen och gå till fliken **[!UICONTROL Admins]**.

1. Klicka på **[!UICONTROL Add Admin]**.
1. Ange namn eller e-postadress. Du kan söka efter befintliga användare eller lägga till en ny användare genom att ange en giltig e-postadress och fylla i informationen på skärmen.
1. Klicka på **[!UICONTROL Next]**. En lista med administratörsroller visas.

   >[!NOTE]
   >
   >* Vilka alternativ som visas på den här skärmen beror på ditt konto och din administratörsroll. Du kan antingen ge samma behörigheter som du har eller behörigheter för en roll som finns under din i hierarkin.
   >* Som systemadministratör för ett team kan du bara tilldela en administratörsroll: Systemadministratör.

1. Välj en eller flera administratörsroller.
1. För Admin-typer som produktadministratör, produktprofiladministratör och administratör för användargrupp väljer du de specifika produkterna, profilerna och grupperna.

   >[!NOTE]
   >
   >För en produktprofiladministratör kan du inkludera profiler för mer än en produkt.

   ![lägg till administratör](assets/add-admin.png)

1. Granska de administratörsroller som tilldelats användaren och klicka på **Spara**.

Användaren får en e-postinbjudan om de nya administratörsbehörigheterna från `message@adobe.com`.

Användarna måste klicka på **[!UICONTROL Get started]** i e-postmeddelandet för att gå med i organisationen. Om nya administratörer inte använder länken **[!UICONTROL Get started]** i e-postinbjudan kan de inte logga in på Admin Console.

Som en del av inloggningsprocessen kan användare uppmanas att konfigurera en Adobe-profil om de inte redan har en. Om flera profiler är associerade med användarens e-postadress måste användarna välja&quot;Gå med i team&quot; (om de uppmanas till det) och sedan välja den profil som är associerad med den nya organisationen.

![administratörsrättighetsbild](assets/admin-get-started-email.png)

## Lägg till en teamadministratör {#add-admin-teams}

Gäller för: Adobe teamkunder.

Som administratör kan du tilldela systemadministratörsrollen till andra användare och ge dem samma behörigheter som du har.

Så här lägger du till eller bjuder in en systemadministratör:

1. I **[!UICONTROL Adobe Admin Console]** väljer du **[!UICONTROL Users]** > **[!UICONTROL Administrators]**.

   En lista över befintliga administratörer visas.

1. Klicka på **[!UICONTROL Add Admin]**.

   Skärmen **[!UICONTROL Add an Administrator]** visas.

1. Ange namn eller e-postadress. Du kan söka efter befintliga användare eller lägga till en ny användare genom att ange en giltig e-postadress och fylla i informationen på skärmen.

   Som standard är Systemadministratör valt.

1. Klicka på **[!UICONTROL Save]**.

![Teamadministratörsbild](assets/teams-admin.png)

Eftersom alla användare i en teamorganisation är Business ID-användare får de en e-postinbjudan om de nya administratörsbehörigheterna från `message@adobe.com`.
Användarna måste klicka på Kom igång i e-postmeddelandet för att gå med i organisationen.

Som en del av inloggningsprocessen kan användare uppmanas att konfigurera en Adobe-profil om de inte redan har en. Om flera profiler är associerade med användarens e-postadress måste användarna välja&quot;Gå med i team&quot; (om de uppmanas till det) och sedan välja den profil som är associerad med den nya organisationen.

![administratörsrättighetsbild](assets/admin-get-started-email.png)

## Redigera företagsadministratörsroll

Gäller för: Adobe företagskunder.

Som administratör kan du redigera administratörsrollen till andra administratörer som finns nedanför dig i den administrativa hierarkin. Du kan till exempel ta bort administratörsbehörighet för andra administratörer.

Så här redigerar du administratörsroller:

1. I **[!UICONTROL Adobe Admin Console]** väljer du **[!UICONTROL Users]** > **[!UICONTROL Administrators]**. Listan över befintliga administratörer visas.

   Du kan också gå till den relevanta produkten, produktprofilen eller användargruppen och gå till fliken **[!UICONTROL Admins]**.

1. Klicka på namnet på den administratör som ska redigeras.
1. I **[!UICONTROL User Details]** klickar du på ![icon](assets/one-console-ellipses.png) för avsnittet **Administrativa rättigheter** och väljer **[!UICONTROL Edit admin rights]**.

   ![redigera administratörsrättigheter](assets/admin-rights-section.png)

1. Redigera de administrativa rättigheterna och spara ändringarna.

## Redigera teamadministratörsroll

Gäller för: Adobe teamkunder.

Som teamsystemadministratör kan du ta bort systemadministratörsbehörighet för andra administratörer.

Så här återkallar du systemadministratörsbehörighet:

1. I **[!UICONTROL Adobe Admin Console]** väljer du **[!UICONTROL Users]** > **[!UICONTROL Administrators]**.

   Listan över befintliga administratörer visas.

1. I **[!UICONTROL User Details]** klickar du på ![icon](assets/one-console-ellipses.png) till höger om avsnittet **[!UICONTROL Administrative Rights]** och väljer **[!UICONTROL Edit admin rights]**.

   ![redigera administratörsrättigheter](assets/admin-rights-section.png)

1. Redigera de administrativa rättigheterna och spara ändringarna.

## Ta bort en administratör

Gäller för: Adobe teams företagskunder.

Om du vill återkalla administratörsbehörigheter markerar du en användare och klickar sedan på **[!UICONTROL Remove Admin]**.

![ta bort administratörsbild](assets/remove-admin.png)

>[!NOTE]
>
>När du tar bort en administratör tas inte användaren bort från Admin Console, utan endast de behörigheter som är kopplade till administratörsrollen tas bort.

## Behörighetsmatris för företagsadministratörer

Gäller för: Adobe företagskunder.

I följande tabell visas alla behörigheter för de olika typerna av administratörer, indelade efter följande funktionsområden:

### Identitetshantering

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Lägg till domän (begära/göra anspråk på en domän) | ✔ | |
| Visa domän- och domänlista | ✔ | |
| Hantera domänkrypteringsnycklar | ✔ | |
| Hantera standardlösenordsprincip för organisation | ✔ | |
| Visa standardlösenordsprincip för organisation | ✔ | |

### Användarhantering

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Lägg till användare i organisation | ✔ | |
| Ta bort användare från organisation | ✔ | |
| Visa användarinformation och lista | ✔ | |
| Redigera användarprofil | ✔ | |
| Lägg till produktprofil för användare eller grupp | ✔ | |
| Ta bort produktprofil för användare eller grupp | ✔ | |
| Lägg till produktprofil för flera användare | ✔ | |
| Visa produktprofiler för en användare | ✔ | |
| Visa produktanvändarlista | ✔ | |
| Lägg till användare i organisationen gruppvis | ✔ | |

### Administratörshantering

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Bevilja organisationsadministratör för en användare | ✔ | |
| Återkalla organisationsadministratör för en användare | ✔ | |
| Bevilja produktlicensadministratör för en användare | ✔ | |
| Återkalla produktlicensadministratör för en användare | ✔ | |
| Bevilja distributionsadministratör för en användare | ✔ | |
| Återkalla distributionsadministratör för en användare | ✔ | |
| Bevilja användargruppadministratör för en användare | ✔ | |
| Återkalla administratör för användargrupp från en användare | ✔ | |
| Bevilja produktägaradministratör för en användare | ✔ | |
| Återkalla produktägaradministratör för en användare | ✔ | |

### Konfigurationshantering för produktlicenser

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Bevilja produktberättigande för organisation | | |
| Ta bort produktberättigande från organisation | | |
| Visa totalt antal licenser som ägs av organisationen | ✔ | |
| Visa tillgängliga produkter och produktfamiljer | ✔ | |
| Redigera produktlicensbeskrivningar/data | ✔ | |
| Tillhandahålla produktlicens för en användare | ✔ | |
| Ta bort produktlicens från en användare | ✔ | |
| Lägg till ny produktlicenskonfiguration | ✔ | |
| Redigera tjänstkonfiguration för produktlicens | ✔ | |
| Ta bort tjänstkonfiguration för produktlicens | ✔ | |
| Ta bort produktåtkomst från en användare (ta bort från alla konfigurationer) | ✔ | |

### Lagringshantering

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Visa aktiva och inaktiva användarmappar | ✔ | |
| Ta bort inaktiva användarmappar och överför innehåll | ✔ | |

### Distribution

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Visa/använd fliken Paket | ✔ | |

### Support

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Visa supportfliken | ✔ | |
| Hantera supportärenden | ✔ | ✔ |

### Hantering av användargrupper

| Behörighet | Systemadministratör | Supportadministratör |
|--- |--- |--- |
| Skapa användargrupp | ✔ | |
| Ta bort användargrupp | ✔ | |
| Lägg till användare i användargrupp | ✔ | |
| Ta bort användare från användargrupp | ✔ | |
| Tilldela användargrupp till produktlicens | ✔ | |
| Ta bort användargrupp från produktlicens | ✔ | |
| Visa medlem i användargrupp | ✔ | ✔ |
| Visa lista med användargrupper | ✔ | ✔ |