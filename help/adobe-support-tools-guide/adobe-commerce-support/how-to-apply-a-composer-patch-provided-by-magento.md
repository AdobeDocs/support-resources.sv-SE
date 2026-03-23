---
title: Använda en kompositkorrigering från Adobe
description: I den här artikeln beskrivs hur du använder en kompositkorrigering för Adobe Commerce lokalt, Adobe Commerce i molninfrastrukturen och Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
source-git-commit: fa46bb7187c55a0c7d75930868c74bf8ba072c41
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Använda en kompositkorrigering från Adobe

I den här artikeln beskrivs hur du använder en kompositkorrigering för Adobe Commerce lokalt, Adobe Commerce i molninfrastrukturen och Magento Open Source.

>[!WARNING]
>
>Vi rekommenderar att du använder och testar korrigeringsfilen i mellanlagrings-/integreringsmiljön innan du använder den i produktionen. Vi rekommenderar även att du nyligen har säkerhetskopierat innan du ändrar något.

## Så här använder du en kompositkorrigering för Adobe Commerce i molninfrastrukturen {#cloud}

1. Om du inte har någon katalog med namnet `m2-hotfixes` i projektroten skapar du en.
1. Kopiera `%patch_name%.composer.patch` fil(er) till katalogen `m2-hotfixes`.
1. Lägg till, implementera och skicka dina kodändringar:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.composer.patch patch"
   ```

   ```git
   git push origin
   ```

Mer information om hur du använder korrigeringsfiler i molnprojekt finns i [Tillämpa korrigeringsfiler](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches) i utvecklardokumentationen.

## Använda en kompositkorrigering för Adobe Commerce lokalt och Magento Open Source {#commerce}

1. Överför patchen till Adobe Commerce lokala katalog eller Magento Open Source rotkatalog.
1. Kör följande SSH-kommando:

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   (Om ovanstående kommando inte fungerar kan du försöka med att använda `-p2` i stället för `-p1` )

1. Uppdatera cacheminnet i administratören under **[!UICONTROL System]** > **[!UICONTROL Cache Management]** för att ändringarna ska återspeglas.