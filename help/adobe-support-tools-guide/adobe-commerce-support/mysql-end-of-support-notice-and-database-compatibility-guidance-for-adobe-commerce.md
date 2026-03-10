---
title: Meddelande om supportslut för MySQL och riktlinjer för databaskompatibilitet för Adobe Commerce
description: Den här artikeln innehåller information om tidslinjer för MySQL-support och riktlinjer för databaskompatibilitet för de Adobe Commerce-versioner som stöds.
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Meddelande om supportslut för MySQL och riktlinjer för databaskompatibilitet för Adobe Commerce

Den här artikeln innehåller viktig information om MySQL-stöd (EOS) och databaskompatibilitet för de Adobe Commerce-versioner som stöds.
Adobe rekommenderar starkt att handlarna granskar detta och vidtar åtgärder för att upprätthålla plattformsstabiliteten och även fortsättningsvis uppfylla supportkraven.
Läs mer i [Uppgraderingskrav för MariaDB](https://experienceleague.adobe.com/sv/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) och [Systemkrav](https://experienceleague.adobe.com/sv/docs/commerce-operations/installation-guide/system-requirements).

## MySQL 8.0 End of Support (EOS)

MySQL 8.0 upphör med stödet (EOS) den 30 april 2026.
Efter detta datum kommer följande Adobe Commerce-versioner inte att stödja eller upprätthålla kompatibilitet med MySQL-versioner som släppts efter MySQL 8.0:

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe kommer inte att validera eller ge support för nyare större MySQL-versioner på dessa Adobe Commerce-versioner.

## Nödvändig åtgärd för lokala kunder

Adobe Commerce lokala installationer som kör följande versioner bör migrera sina databasservrar till en kompatibel MariaDB-version:

* 2.4.5
* 2.4.6
* 2.4.7

MariaDB stöds fullt ut i dessa versioner och är den rekommenderade databasplattformen som går framåt.

* 2.4.5
* 2.4.6
* 2.4.7

Vi rekommenderar starkt att du migrerar deras databasservrar till en kompatibel MariaDB-version.
MariaDB stöds fullt ut för dessa Adobe Commerce-versioner och är den rekommenderade databasplattformen.

## MySQL-stöd i Adobe Commerce 2.4.8 och 2.4.9

Adobe Commerce 2.4.8 och 2.4.9 är de sista Adobe Commerce-versionerna som stöder MySQL.

För dessa versioner:
* MySQL 8.4 är den slutliga MySQL-versionen som stöds av Adobe Commerce.
* Inga MySQL-versioner som släpps efter 8.4 kommer att certifieras eller stödjas i Adobe Commerce.

## Framtida riktning: MariaDB som standarddatabasplattform

I framtiden fortsätter Adobe Commerce att stödja MariaDB som standarddatabasplattform och rekommenderad databasplattform.

Adobe rekommenderar starkt att följande kunder börjar planera sin migrering till MariaDB för att bibehålla långsiktig kompatibilitet och stödja justering:
* Alla lokala Adobe Commerce 2.4.8- och 2.4.9-kunder
* Kunder som kör tidigare Adobe Commerce-versioner som stöds
