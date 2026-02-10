---
title: Så här hämtar och använder du [!UICONTROL security patch]
description: Den här artikeln innehåller anvisningar om hur du hämtar och använder en [!UICONTROL security patch] som har släppts, men det finns inga instruktioner.
source-git-commit: 93ee9bd110930e244befca682fadd3edc24d138a
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Så här hämtar och använder du en [!UICONTROL security patch]

>[!NOTE]
>Om du har en lokal installation och inte använder versionskontrollsystem som [!DNL CVS] eller GitHub för att hantera koden, kan din webbvärd kanske hjälpa dig med att tillämpa korrigeringen. Kontakta dem gärna om du behöver hjälp.

Den här artikeln innehåller anvisningar om hur du hämtar och använder en [!UICONTROL security patch] som har släppts, men det finns inga instruktioner.

## Berörda produkter och versioner

Adobe Commerce lokala infrastruktur och molninfrastruktur - alla versioner som stöds


## Orsak

De flesta [!UICONTROL security patches] släpps utan någon isolerad korrigering eller snabbkorrigering och måste uppgraderas till [!UICONTROL security patch]-versionen.

## Lösning


### Fall I:

* Om en isolerad korrigeringsfil/snabbkorrigering anges i [versionsinformationen](https://experienceleague.adobe.com/sv/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite) hämtar du filen från hämtningsavsnittet på [https://account.magento.com](https://account.magento.com/downloads/view/). Användare med delad åtkomst måste först få hämtningsbehörighet av kontoägaren/licenshavaren.

**Caveats:**

Om du har en äldre version av Adobe Commerce (2.4.4) har du automatiskt fått utökad support. Din version måste vara en av följande versioner som inte stöds för att du ska kunna tillämpa de senaste tillgängliga säkerhetsuppdateringarna:

2.4.4 - 2.4.4-p11

Versioner som inte stöds (2.3.x, 2.4.0 - 2.4.3) har inte rätt till support och du måste först uppgradera till en version som stöds för att kunna utnyttja de senaste säkerhetskorrigeringarna.

Om du inte har Extended Support (Utökad support) kan du begära Support för att dela korrigeringsfilerna med dig, men de kan inte lösa eventuella problem eller fel som du kan stöta på när du tillämpar dem.

### Fall II:

Isolerade korrigeringsfiler tillhandahålls endast i undantagsfall och är inte den rekommenderade formen för implementering av säkerhetskorrigeringar.

Om en isolerad korrigeringsfil/snabbkorrigering inte omnämns i versionsinformationen:

* **Cloud:**

1. Vissa [!UICONTROL security patches] kan ingå/släppas i den senaste versionen av Cloud Tools Suite (ECE-verktyg) under Cloud Patches for Commerce - kontrollera [Versionsinformation](https://experienceleague.adobe.com/sv/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) och om en säkerhetskorrigering nämns i den versionen uppgraderar du paketet till den versionen.
1. Om versionsinformationen inte innehåller någon säkerhetskorrigering kan du fortsätta läsa.

* **Molninfrastruktur eller lokal:**

* Om det inte finns någon isolerad korrigeringsfil/snabbkorrigering kan du [uppgradera Adobe Commerce-versionen i molninfrastrukturen](https://experienceleague.adobe.com/sv/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X till den senaste korrigeringsversionen, 2.4.X-pY.
* Om det inte finns någon isolerad korrigeringsfil/snabbkorrigering kan du [uppgradera Adobe Commerce-versionen On-Premise](https://experienceleague.adobe.com/sv/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X till den senaste korrigeringsversionen, 2.4.X-pY.

## Relaterad läsning

* Se [Versionsinformation om Commerce Cloud Tools Suite](https://experienceleague.adobe.com/sv/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) i *Adobe Commerce on Cloud Infrastructure Guide*.
* Se [Uppgradera Adobe Commerce-versionen](https://experienceleague.adobe.com/sv/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) i *Adobe Commerce on Cloud Infrastructure Guide*.
