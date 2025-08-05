---
title: Fel vid komprimering av avsnitt
description: Komprimerbara avsnitt i UGP-13446 återges inte, kanske på grund av inbäddade sidflikar
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 6%

---

# Komprimerbara avsnitt

<http://jira.corp.adobe.com/browse/UGP-13446> Komprimerbara avsnitt i UGP-13446 återges inte, kanske på grund av inbäddade sidflikar

## Exempel

Först med sidflikar; andra utan

### Alternativ 2: Med sidflikar

+++ Manuell snabbkorrigering för 6.5.18.0 - 6.5.22.0

**Steg 1: Hämta och extrahera snabbkorrigeringspaketet**

- Hämta [snabbkorrigeringen för 6.5.18.0 - 6.5.22](https://www.adobe.com) från Adobe Software Distribution Portal
- Extrahera lokalt

**Steg 2: Navigera till rätt versionsmapp**

- Gå till den matchande mappen baserat på vilken Service Pack-version som är installerad i din miljö.

  Exempel för Service Pack 20 är:

  ```
  <extracted-hotfix>/SP20/
  ```

**Steg 3: Leta reda på distributionskatalogen**

- På din AEM Forms på JEE-server går du till:

  ```
  [AEM installation directory]/deploy
  ```

  Exempel: `adobe/adobe-experience-manager-forms/deploy`



**Steg 4: Uppdatera och ersätt EAR-filerna**

>[!BEGINTABS]

>[!TAB JBoss]

1. Öppna `adobe-core-jboss.ear` och ersätt `adminui.war` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. I `adobe-core-jboss.ear` går du till mappen `lib/` och ersätter `adobe-uisupport.jar` med:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Spara på EAR. Se till att ändringarna sparas korrekt.


1. Ersätt `adobe-edcserver-jboss.ear` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. Ersätt `adobe-forms-jboss.ear` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. Öppna `adobe-core-weblogic.ear` och ersätt `adminui.war` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. I `adobe-core-weblogic.ear` ersätter du `adobe-uisupport.jar` med:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Spara på EAR. Se till att ändringarna sparas korrekt.


1. Ersätt `adobe-edcserver-weblogic.ear` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. Ersätt `adobe-forms-weblogic.ear` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. Öppna `adobe-core-websphere.ear` och ersätt `adminui.war` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. I `adobe-core-websphere.ear` ersätter du `adobe-uisupport.jar` med:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Spara på EAR. Se till att ändringarna sparas korrekt.


1. Ersätt `adobe-edcserver-websphere.ear` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. Ersätt `adobe-forms-websphere.ear` med

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   Exempel: `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**Steg 5: Uppdatera `adobe-rightsmanagement-<appserver>-dsc.jar`filen med**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Exempel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Steg 6: Ytterligare konfiguration för dokumentsäkerhet i WebSphere och WebLogic**:

Om du använder Dokumentsäkerhet (tidigare Rights Management) anger du följande Java-systemegenskap (JVM-argument) innan du startar AEM Forms-servern:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Steg 7: Kör Configuration Manager igen**

- Starta Configuration Manager för att omdistribuera den uppdaterade EAR-uppdateringen och tillämpa snabbkorrigeringen

+++

### Alternativ 2: Utan sidflikar

+++ Manuell snabbkorrigering för 6.5.18.0 - 6.5.22.0

**Steg 1: Hämta och extrahera snabbkorrigeringspaketet**

- Hämta [snabbkorrigeringen för 6.5.18.0 - 6.5.22](https://www.adobe.com) från Adobe Software Distribution Portal
- Extrahera lokalt

**Steg 2: Navigera till rätt versionsmapp**

- Gå till den matchande mappen baserat på vilken Service Pack-version som är installerad i din miljö.

  Exempel för Service Pack 20 är:

  ```
  <extracted-hotfix>/SP20/
  ```

**Steg 3: Leta reda på distributionskatalogen**

- På din AEM Forms på JEE-server går du till:

  ```
  [AEM installation directory]/deploy
  ```

  Exempel: `adobe/adobe-experience-manager-forms/deploy`



**Steg 4: Uppdatera och ersätt EAR-filerna**

Sidflikar har tagits bort

**Steg 5: Uppdatera `adobe-rightsmanagement-<appserver>-dsc.jar`filen med**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Exempel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Steg 6: Ytterligare konfiguration för dokumentsäkerhet i WebSphere och WebLogic**:

Om du använder Dokumentsäkerhet (tidigare Rights Management) anger du följande Java-systemegenskap (JVM-argument) innan du startar AEM Forms-servern:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Steg 7: Kör Configuration Manager igen**

- Starta Configuration Manager för att omdistribuera den uppdaterade EAR-uppdateringen och tillämpa snabbkorrigeringen

+++

Fin
