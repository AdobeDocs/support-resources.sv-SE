---
title: Tabellbrytningar
description: Test av olika tabellbrytningar
hide: true
hidefromtoc: true
source-git-commit: 9ad23090cb13f36d6d015b23122736048fe2230c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 5%

---

# Tabellbrytningar

Inte mycket att se här.

## Standardtabell med markeringar med `<br>`

**FASTSTÄLLD`Green<br>Red<br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br>Röd<br>Blå |
| Maria | 23 | Gul<br>Brun |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br>Röd<br>Blå |
| Maria | 23 | Gul<br>Brun |

{style="table-layout:auto"}

## Markeringstabell med dubbel `<br>`s

**FASTSTÄLLD`Green<br><br>Red<br><br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br><br>Röd<br><br>Blå |
| Maria | 23 | Gul<br><br>Brun |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br><br>Röd<br><br>Blå |
| Maria | 23 | Gul<br><br>Brun |

{style="table-layout:auto"}

## Markeringsregister med `<p>`

**FASTSTÄLLD`Green<p>Red<p>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<p>Röd<p>Blå |
| Maria | 23 | Gul<p>Brun |

{style="table-layout:fixed"}

**AUTO`Green<p>Red<p>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<p>Röd<p>Blå |
| Maria | 23 | Gul<p>Brun |

{style="table-layout:auto"}

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Det här är färgen **grön** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **röd** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **blå** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. |
| Maria | 23 | Gul<p>Brun |

{style="table-layout:fixed"}

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Det här är färgen **grön** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **röd** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **blå** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. |
| Maria | 23 | Gul<p>Brun |

{style="table-layout:auto"}
