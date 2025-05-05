---
title: snedstreck i kodblock UGP-11189
description: Slash in code blocks UGP-11189 test
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 0%

---

# Snedstreck i kodblock

1. Kör kommandot:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Nästa steg

Finns inte i kodblocket

vendor/bin/magento-patches -n status |grep &quot;27015\|Status&quot;

Backslash med Escaped:

vendor/bin/magento-patches -n status |grep &quot;27015&bsol;|Status&quot;
