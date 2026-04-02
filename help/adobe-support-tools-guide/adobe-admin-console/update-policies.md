---
title: Uppdatera organisationsprofiler i Global Admin Console
description: Läs om hur en global administratör kan ange och ändra policyer för en organisation och dess underordnade i Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
source-git-commit: 90807a4e803de702c9e0975df551efefc254030a
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 0%

---

# Uppdatera organisationsprofiler i Global Admin Console

**Gäller för:** Enterprise

Läs om hur en global administratör kan ange och ändra policyer för en organisation och dess underordnade i Global Admin Console.

>[!NOTE]
>
>I [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) väljer du en organisation i hierarkin och navigerar till fliken **Profiler** för att tillåta eller neka, eller låser profiler.
>
> [Logga in på Global Admin Console](https://global-admin-console.adobe.com/)

Principer är kopplade till en organisation och begränsar åtgärder som kan utföras på den organisationen. När ett principvärde anges begränsas eller aktiveras åtgärder från den punkten och framåt.
Om principen **Anspråksdomäner** till exempel är inställd på *inte tillåten* kan inga ytterligare domäner tas i anspråk, men domäner som tagits i anspråk innan principvärdet har ställts in påverkas inte.

## Konfigurera principer

Så här ändrar du en organisations profiler:

1. I Global Admin Console [väljer du en organisation](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) att redigera och går sedan till fliken **[!UICONTROL Policies]**.
1. Välj en växlingsknapp för den aktuella profilen för att tillåta eller neka den. Du kan också låsa en princip så att ingen annan än en global administratör för den [valda organisationen](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) eller dess överordnade organisation kan ändra eller låsa upp den.
1. Om du vill låsa en profil väljer du ikonen **[!UICONTROL Lock]** ![Lås](./assets/lock.png) . När du placerar låset visas namnet på den valda organisationen. Läs mer om [principlås](#policy-locks).
1. Välj **[!UICONTROL Review Pending Changes]** när du är klar med redigeringen av organisationerna. Efter granskning väljer du **[!UICONTROL Submit Changes]** för att [köra](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) dem.

## Principlås {#policy-locks}

När en princip är låst kan dess värde inte ändras förrän principen är olåst. Global Admin Console kommer ihåg att den [valda organisationen](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) i organisationsväljaren är den organisation som principen är låst från. Alla globala administratörer för den valda organisationen eller en organisation som är högre i trädet har behörighet att låsa upp principen. Globala administratörer vars omfång är lägre än den organisationen saknar behörighet att låsa upp och ändra principvärden.

Om du vill skapa en låst miljö anger du önskade principvärden för dina underordnade organisationer och låser dem sedan. Globala administratörer för dessa underordnade organisationer kan inte redigera principvärdena.

### Exempel: Låst ned miljö

Om Elissa, den globala administratören för *Acme Division*, skapar underordnade organ *Marketing* och *Engineering*, lägger sedan till Robert som global administratör för *Marketing* och Sarah som global administratör för *Engineering*. Därefter anger hon flera profiler till *Inte tillåtet* och *låser*. Elissa kan senare låsa upp och ändra principvärdena när hon väljer *Acme Division* som vald organisation, men Robert och Sarah kan inte låsa upp policyer för de organisationer som de är globala administratörer för eftersom policyer är låsta av organisationen *Acme Division*.

## Policyinformation

### Organisationshantering

| Principnamn | Beskrivning |
| --- | --- |
| **Skapa underordnade organisationer** | Tillåter globala administratörer att skapa underordnade organ. Om det är *av* kan inga underordnade organ skapas. |
| **Byt namn på organisation** | Om det tillåts kan en global administratör eller systemadministratör byta namn på organisationen. Det styr också ändringen av land/region för organisationen. Sökvägen för en organisation kan också ändras oberoende av den här principinställningen om namnet på en överordnad organisation ändras eller om organisationen eller en överordnad organisation omnämns. |
| **Ta bort organisationer** | Tillåter globala administratörer att ta bort underordnade organisationer. Detta blir viktigare när organisationer med Enterprise Storage är aktiverade på grund av risken att ta bort användarresurser. |

### Administratörshantering

| Principnamn | Beskrivning |
| --- | --- |
| **Lägg till eller ta bort administratörer** | Tillåter globala administratörer att lägga till nya administratörer i en organisation. Om *är av* kan nya administratörer inte läggas till. |
| **Ärv systemadministratörer från överordnad när underordnad organisation skapas** | När globala administratörer skapar nya underordnade organisationer blir systemadministratörer för den överordnade automatiskt systemadministratörer för den nya organisationen. Den här principen är *av* som standard. |
| **Hantera administratörer** | Tillåter globala administratörer att ändra eller ta bort/redigera administratörsbehörigheter. |

### Användarhantering

| Principnamn | Beskrivning |
| --- | --- |
| **Ärv användare från kataloger som hanteras av den överordnade organisationen** | Den här principen måste växlas *den* och vara aktiv innan den nya underordnade organisationen kan skapas. När en underordnad organisation skapas blir användarna i den överordnade organisationen tillgängliga som användare i den underordnade organisationen. Med andra ord skapar den här principen automatiskt en förtroenderelation mellan det överordnade och det underordnade objektet när det nya underordnade objektet skapas i GAC:n. För befintliga organ kommer eventuella förtroenderelationer innan de läggs till i den allmänna redovisningen att finnas kvar när de väl förts in i den allmänna redovisningen. Om det inte finns några betrodda relationer på plats måste den vanliga processen för att begära förtroende följas. För att den här principen ska lyckas måste den globala administratören som skapar den nya organisationen också vara systemadministratör för den överordnade organisationen med den domän som tagits i anspråk. Annars ärvs inte domänförtroenderelationen till den nyligen skapade organisationen. |
| **Lägg till Adobe ID-användare** | Om detta anges kan organisationen inte lägga till Adobe ID-typanvändare via Admin Console, UMAPI (User Management API) eller synkroniseringsmekanism. |
| **Hantera användargrupper** | Om det är tillåtet kan administratörer för globala grupper, system och användargrupper skapa, redigera och ta bort användargrupper. |

### Krävande av kataloger och domäner

| Principnamn | Beskrivning |
| --- | --- |
| **Anspråksdomäner** | Om detta anges kan systemadministratörer göra anspråk på domäner på Admin Console. |
| **Ändra identitetskonfiguration** | Om detta anges kan systemadministratörer ändra konfigurationen av användaridentitet på Admin Console. |

### Produktallokering

| Principnamn | Beskrivning |
| --- | --- |
| **Hantera produkter** | Tillåter globala administratörer att lägga till eller ta bort produkter och ändra produktresurstilldelningar. |

### Resursdelning

| Principnamn | Beskrivning |
| --- | --- |
| **System- eller lagringsadministratören kan ändra inställningar för resursdelning** | Om det är tillåtet kan lagrings- och systemadministratörer ändra inställningar för resursdelning, inklusive säkerhetskontakter, lösenordsprinciper och lagringsprinciper. |
| **Ärv delningsprincip från en överordnad när en organisation skapas** | Om det är tillåtet ärvs inställningar för resursdelning från den överordnade organisationen när en underordnad organisation skapas. Inställningarna för resursdelning inkluderar säkerhetskontakter, lösenordsprinciper och lagringsprinciper. Detta gäller endast för nyligen skapade organ när de skapas. Den anges för en överordnad och påverkar skapandet av underordnade organ under den överordnade. |
