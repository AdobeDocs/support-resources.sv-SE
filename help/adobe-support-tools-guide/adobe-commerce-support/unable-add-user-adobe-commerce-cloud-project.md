---
title: Det går inte att lägga till användare i Adobe Commerce molnprojekt
description: Den här artikeln innehåller en lösning för när du inte kan lägga till en användare i ett Adobe Commerce-molnprojekt.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
source-git-commit: dfb3e7ea8638755cdff16b0765125403f429ef2e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---

# Det går inte att lägga till användare i Adobe Commerce molnprojekt

Den här artikeln innehåller en lösning för när du försöker lägga till en användare i ett molnprojekt, men den misslyckas med ett fel: *Användare XXX finns inte*.

## Berörda produkter och versioner

* Adobe Commerce i molninfrastruktur, [alla versioner som stöds](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problem

Den här artikeln innehåller en lösning för när du inte kan lägga till en användare i ett Adobe Commerce-molnprojekt.

## Orsak

Användarens konto måste först skapas på [https://accounts.magento.cloud](https://accounts.magento.cloud) och länkas till deras Adobe SSO innan de kan läggas till som användare i projektet. Om användaren har ett Adobe-konto men inte ett Commerce-konto (magento.com) måste han/hon först skapa ett.

## Lösning

1. Be användaren logga in på [https://accounts.magento.cloud](https://accounts.magento.cloud). Användaren måste redan vara registrerad hos Adobe med samma e-postadress.
   > **OBS!**\
   > Att skapa eller ha ett konto på [https://account.adobe.com](https://account.adobe.com) innebär inte automatiskt att användaren har ett konto på [https://accounts.magento.cloud](https://accounts.magento.cloud). Användaren måste först [skapa sitt Commerce-konto](https://experienceleague.adobe.com/sv/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Om användaren redan har ett Adobe-konto men inte kan logga in ber du användaren att skicka en [supportförfrågan](https://experienceleague.adobe.com/home?lang=sv-SE#support) med [!UICONTROL Issue Reason] inställd på *Användarhantering*.

1. När användaren har loggat in på [https://accounts.magento.cloud](https://accounts.magento.cloud) kan du lägga till användaren i projektet. Detaljerade steg finns i [Lägga till användare och hantera åtkomst](https://experienceleague.adobe.com/sv/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) i infrastrukturguiden för Commerce i molnet.

## Relaterad läsning:

* [Hantera användaråtkomst](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=sv-SE) i vår Commerce on Cloud Infrastructure Guide.
* [Det går inte att logga in på Adobe Commerce support eller molnkontot](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=sv-SE)