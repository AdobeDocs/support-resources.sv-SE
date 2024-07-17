---
title: Tabellbrytningar
description: Test av olika tabellbrytningar
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 5%

---

# Tabellbrytningar

Inte mycket att se här.

## Standardmarkeringstabell med `<br>`

**KORRIGERAD`Green<br>Red<br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br>röd<br>blå |
| Maria | 23 | Gul<br>brun |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br>röd<br>blå |
| Maria | 23 | Gul<br>brun |

{style="table-layout:auto"}

## Markeringstabell med dubbla `<br>`

**KORRIGERAD`Green<br><br>Red<br><br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br><br>röd<br><br>blå |
| Maria | 23 | Gul<br><br>brun |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Grön<br><br>röd<br><br>blå |
| Maria | 23 | Gul<br><br>brun |

{style="table-layout:auto"}

## Markeringstabell med `<p>`

**KORRIGERAD`Green<p>Red<p>Blue`**

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
| Juanya | 17 | Det här är färgen **green** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **red** och är avsett att brytas till en annan rad som en fråga och för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **blue** och är avsett att brytas till en annan rad som en fråga och/eller som ett sätt att testa föregående styckebrytningar. |
| Maria | 23 | Gul<p>Brun |

{style="table-layout:fixed"}

|  | Nummer | Färger |
|---|---|---|
| Juanya | 17 | Det här är färgen **green** och är avsett att brytas till en annan rad som en fråga och/eller metod för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **red** och är avsett att brytas till en annan rad som en fråga och för att testa tidigare nämnda styckebrytningar. <p>Det här är färgen **blue** och är avsett att brytas till en annan rad som en fråga och/eller som ett sätt att testa föregående styckebrytningar. |
| Maria | 23 | Gul<p>Brun |

{style="table-layout:auto"}
