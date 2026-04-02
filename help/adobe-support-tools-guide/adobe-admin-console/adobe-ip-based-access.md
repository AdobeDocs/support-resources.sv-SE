---
title: Begränsa produktåtkomst via IP-adresser
description: Använd IP-baserad åtkomst för att styra användarnas åtkomst till Adobe-produkter och begränsa användningen till godkända offentliga IP-intervall.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---


# Begränsa produktåtkomst via IP-adresser

Gäller företag.

Använd IP-baserad åtkomst för att styra användarnas åtkomst till Adobe-produkter och förhindra obehörig användning från olistade offentliga IP-adresser.

Gå till [Admin Console](https://adminconsole.adobe.com/settings/identity) om du vill lägga till betrodda offentliga IP-adresser i tillåtelselista **IP-baserad åtkomst** för skyddad användning av Adobe program och tjänster.

## Fördelar med IP-baserad åtkomst

IP-baserad åtkomstkontroll använder en IP-adress tillåtelselista för att begränsa användningen av Adobe-produkter från slumpmässiga offentliga IP-adresser. IP-baserad åtkomst gäller för alla kataloger och tillhörande produkter i din Adobe Admin Console.

Du kan lägga till betrodda offentliga IP-adresser i listan **Tillåtna IP-adresser** om du vill hindra användare från att:

- Åtkomst till produkter från offentliga IP-adresser som ligger utanför de tillåtna IP-intervallen
- Logga in på Adobe [användarprofiler](https://helpx.adobe.com/se/enterprise/using/manage-adobe-profiles.html) från offentliga IP:n utanför de tillåtna IP-intervallen
- Växla användarprofiler i webbprogram utanför de tillåtna IP-intervallen

  ![Exportera organisationsstruktur](./assets/ip-based-access.avif)

## Aktivera IP-baserad åtkomst

### Viktiga överväganden

>[ !IViktiga överväganden]
>
>- Administratörer måste börja med att lägga till sin egen offentliga IP-adress och bara sedan lägga till andra IP-intervall. Annars kan du råka ut för ett fel.
>- IP-baserad åtkomst gäller inte för privata IP-adresser.

Du kan lägga till upp till 150 olika publika IP-intervall endast i CIDR-format.

Så här aktiverar du IP-baserad åtkomst i din Adobe Admin Console:

1. Gå till avsnittet **[[!UICONTROL Adobe Admin Console Settings]](https://adminconsole.adobe.com/settings/identity)**.
2. Markera och expandera **[!UICONTROL Privacy and security]** på markeringsmenyn och välj sedan **[!UICONTROL Authentication settings]**.
3. Markera knappen **[!UICONTROL IP-based access]** i avsnittet **[!UICONTROL Add IP address]**.
4. I fönstret **[!UICONTROL Add IP address]**:
   - Ange de offentliga IP-adresserna eller CIDR-blocket som ska läggas till i tillåtelselista.
   - Använd kommatecken för att avgränsa flera IP-adresser.
   - Välj **[!UICONTROL Save]**.

   Vi stöder för närvarande bara IPv4-formatet. Här är några exempel:
   - IP v4-adress: 1.3.4.6
   - IP v4-undernätsadress: 1.2.0.0/24

Dina IP-adresser läggs till inom några minuter. Associerade användare ser begränsningen nästa gång de försöker logga in eller växla profiler utanför de tillåtna offentliga IP-adresserna. Vi rekommenderar att du informerar dina användare innan den här ändringen görs.

Du kan redigera eller ta bort alla angivna IP-adresser genom att markera redigerings- eller borttagningsalternativen bredvid varje post.

>[!NOTE]
>
>- När IP-baserad åtkomst är aktiverad, **sker ingen tvingad utloggning**. Användare påverkas bara när de försöker välja den begränsade profilen när de loggar in eller byter profil på webben.
>- Om du använder en skyddad webbgateway måste du se till att all trafik dirigeras genom den. Visa [listan över domäner som ska tillåtas](https://helpx.adobe.com/se/enterprise/kb/network-endpoints.html) för att Adobe program och tjänster ska fungera korrekt.
>- Om du har låst dig utanför Admin Console eftersom du angav en ogiltig IP-adress kontaktar du [Adobe kundtjänst](https://helpx.adobe.com/se/enterprise/using/support-for-enterprise.html).

## Delta i konversationen

Om du vill samarbeta, ställa frågor och chatta med andra administratörer går du till vår [Enterprise and Teams Community](https://www.adobe.com/go/entcom_se).
