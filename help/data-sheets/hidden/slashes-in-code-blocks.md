---
title: snedstreck i kodblock UGP-11189
description: Slash in code blocks UGP-11189 test
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Snedstreck i kodblock

1. Kör kommandot:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Kör kommandot (escape):

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

Finns inte i kodblocket

vendor/bin/magento-patches -n status |grep &quot;27015\|Status&quot;

Escaped:

vendor/bin/magento-patches -n status |grep &quot;27015&amp;bsol;|Status&quot;

