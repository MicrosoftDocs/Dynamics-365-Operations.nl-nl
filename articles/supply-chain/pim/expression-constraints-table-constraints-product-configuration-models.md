---
title: Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen
description: Dit onderwerp beschrijft het gebruik van expressiebeperkingen en tabelbeperkingen. U gebruikt beperkingen om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert. U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88d52031f4c916f5ec3e970f38864977e69a9d9a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "356640"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft het gebruik van expressiebeperkingen en tabelbeperkingen. U gebruikt beperkingen om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert. U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken. 

Beperkingen worden gebruikt om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert. U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.

## <a name="what-are-expression-constraints"></a>Wat zijn expressiebeperkingen?
Expressiebeperkingen worden gekenmerkt door een expressie met rekenkundige en Booleaanse operatoren en functies. Een expressiebeperking wordt geschreven voor een bepaald onderdeel in een productconfiguratiemodel. De beperking kan niet worden hergebruikt door of gedeeld met een ander onderdeel. Expressiebeperkingen voor een onderdeel kunnen echter verwijzen naar kenmerken van subonderdelen van het onderdeel.

## <a name="what-are-table-constraints"></a>Wat zijn tabelbeperkingen?
Tabelbeperkingen maken een lijst met de combinaties van waarden die zijn toegestaan voor kenmerken wanneer u een product configureert. De definities van tabelbeperkingen kunnen algemeen worden gebruikt. Wanneer u een tabelbeperking voor een component maakt in een productconfiguratiemodel, selecteert u een definitie voor de tabelbeperking. Om de combinaties te maken die worden toegestaan, voegt u kenmerken van specifieke typen aan de onderdelen toe. Elk kenmerktype heeft een specifieke waarde.

### <a name="example-of-a-table-constraint"></a>Voorbeeld van een tabelbeperking.

Dit voorbeeld toont hoe u de configuratie van een speaker tot specifieke afwerkingen van de behuizingen en voorkanten kunt beperken. De eerste tabel laat de afwerkingen van de behuizingen en voorkanten zien die algemeen beschikbaar zijn voor configuratie. De waarden zijn gedefinieerd voor **Afwerking behuizing** en **Voorgrill**.

| Kenmerktype | Waarden                      |
|----------------|-----------------------------|
| Afwerking behuizing | Zwart, Eiken, Rozenhout, Wit |
| Voorgrill    | Zwart, Metaal, Wit         |

De volgende tabel geeft de combinaties weer die door de tabelbeperking **Kleur en afwerking** zijn gedefinieerd. Door deze tabelbeperking te gebruiken, kunt u een speaker configureren met een eiken afwerking en een zwarte grill, een rozenhouten afwerking en een witte grill, enzovoort.

| Voltooien         | Grill                       |
|----------------|-----------------------------|
| Eiken            | Zwart                       |
| Rozenhout       | Wit                       |
| Wit          | Zwart                       |
| Wit          | Wit                       |
| Zwart          | Zwart                       |
| Zwart          | Metaal                       | 

U kunt door het systeem gedefinieerde en door de gebruiker gedefinieerde tabelbeperkingen maken. Voor meer informatie, zie [Door het systeem gedefinieerde en door gebruiker gedefinieerde tabelbeperkingen](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Welke syntaxis moet worden gebruikt om beperkingen te schrijven?
Gebruik de OML-syntaxis (Optimization Modeling Language) wanneer u beperkingen opstelt. Microsoft Solver Foundation-beperkingsoplosser wordt gebruikt om de beperkingen op te lossen.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Moet ik tabelbeperkingen of expressiebeperkingen gebruiken?
U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken. U maakt een tabelbeperking als matrix, terwijl een expressiebeperking een afzonderlijke statement is. Wanneer u een product configureert, is het niet van belang welk type beperking wordt gebruikt. In het volgende voorbeeld kunt u zien hoe de twee methoden verschillen.  

Wanneer u een product met de volgende beperkingsinstellingen configureert, worden deze combinaties toegestaan:

-   Een product in de kleur Zwart, in grootte 30 of 50
-   Een product in de kleur Rood, in grootte 20

### <a name="table-constraint-setup"></a>Tabelbeperkingsinstelling

| Kleur | Grootte |
|-------|------|
| Zwart | 30   |
| Zwart | 50   |
| Rood   | 20   |

### <a name="expression-constraint-setup"></a>Instelling expressiebeperking

(Kleur == "Zwart" & (afmeting == "30" | afmeting == "50")) | (kleur == "Rood" & afmeting = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Moet ik operators gebruiken of tussenvoegselaantekening gebruiken wanneer ik expressiebeperkingen schrijf?
U kunt een expressiebeperking opstellen met behulp van de beschikbare voorvoegseloperatoren of met tussenvoegselnotatie. Voor de operatoren **Min**, **Max**, en **Abs** kunt u de tussenvoegselnotatie niet gebruiken. Deze operatoren zijn opgenomen als standaardoperatoren in de meeste programmeertalen.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Welke operators en tussenvoegselnotatie kan ik gebruiken wanneer ik expressiebeperkingen schrijf?
In de volgende tabel worden de operatoren en de tussenvoegselnotatie vermeld die u kunt gebruiken voor het schrijven van een expressiebeperking voor een onderdeel van een productconfiguratiemodel. In de voorbeelden in de eerste tabel kunt u zien hoe u een expressie maakt door tussenvoegselnotaties of operators te gebruiken.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operator</th>
<th>Omschrijving</th>
<th>Syntaxis</th>
<th>Voorbeelden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Heeft</td>
<td>Dit is waar als de eerste voorwaarde onwaar is, de tweede voorwaarde waar, of beide.</td>
<td>Heeft[a, b], tussenvoegselaantekening: a -: b</td>
<td><ul>
<li><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</li>
<li><strong>Tussenvoegselnotatie:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>En</td>
<td>Dit is alleen waar als alle voorwaarden waar zijn. Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>Waar</strong>.</td>
<td>And[args], tussenvoegsel: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Operator:</strong> And[x == 2, y &lt;= 2]</li>
<li><strong>Tussenvoegselnotatie:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Of</td>
<td>Dit is waar als een van de voorwaarden waar is. Als het aantal condities 0 is (nul), is het product <strong>Onwaar</strong>.</td>
<td>Or[args], tussenvoegsel: a | b | ... | z</td>
<td><ul>
<li><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Tussenvoegselnotatie:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plus</td>
<td>Dit is de som van de voorwaarden. Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>0</strong>.</td>
<td>Plus[args], tussenvoegsel: a + b + ... + z</td>
<td><ul>
<li><strong>Operator:</strong> Plus[x, y, 2] == z</li>
<li><strong>Tussenvoegselnotatie:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Min</td>
<td>Het argument wordt genegeerd. Het moet precies één voorwaarde hebben.</td>
<td>Minus[expr], tussenvoegselaantekening: -expr</td>
<td><ul>
<li><strong>Operator:</strong> Minus[x] == y</li>
<li><strong>Tussenvoegselnotatie:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Hiervoor is de absolute waarde van de voorwaarde vereist. Het moet precies één voorwaarde hebben.</td>
<td>Abs[expr]</td>
<td><strong>Operator:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Tijden</td>
<td>Hiervoor is het product van de voorwaarden vereist. Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>1</strong>.</td>
<td>Times[args], tussenvoegsel: a * b * ... * z</td>
<td><ul>
<li><strong>Operator:</strong> Times[x, y, 2] == z</li>
<li><strong>Tussenvoegselnotatie:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Vermogen</td>
<td>Hiervoor is een exponentiële waarde vereist. Hiermee wordt machtsverheffen van rechts naar links toegepast. (Dat wil zeggen dat het rechts associatief is) Hierdoor is <strong>Power[a, b, c]</strong> gelijk aan <strong>Power[a, Power[b, c]]</strong>. <strong>Power</strong> kan alleen worden gebruikt als de exponent een positieve constante is.</td>
<td>Power[args], tussenvoegsel: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Operator:</strong> Power[x, 2] == y</li>
<li><strong>Tussenvoegselnotatie:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Max.</td>
<td>Dit levert de grootste voorwaarde. Als het aantal condities 0 is (nul), resulteert dit in <strong>Oneindigheid</strong>.</td>
<td>Max[args]</td>
<td><strong>Operator:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Min.</td>
<td>Dit levert de kleinste voorwaarde. Als het aantal condities 0 is (nul), resulteert dit in <strong>Oneindigheid</strong>.</td>
<td>Min[args]</td>
<td><strong>Operator:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Niet</td>
<td>Dit resulteert in de logische inverse van de voorwaarde. Het moet precies één voorwaarde hebben.</td>
<td>Niet[expr], infix: !expr</td>
<td><ul>
<li><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Tussenvoegselnotatie:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

De voorbeelden in de volgende tabel geven weer hoe een tussenvoegselnotatie moet worden geschreven.


|  Infix-notatie   |                                          Omschrijving                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           Optelling                                            |
|    x \* y \* z    |                                        Vermenigvuldigen                                         |
|       x - y       | Binair aftrekken wordt op dezelfde manier vertaald als binaire optelling waarbij er een genegeerde tweede is. |
|     x ^ y ^ z     |                          Machtsverheffen met associatie naar rechts                          |
|        !x         |                                          Booleaans niet                                          |
|      x -: y       |                                      Booleaanse implicatie                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          Booleaans en                                          |
|    x == y == z    |                                           Gelijkheid                                            |
|    x != y != z    |                                           Afzonderlijk                                            |
|  x &lt; y &lt; z  |                                           Kleiner dan                                           |
|  x &gt; y &gt; z  |                                         Groter dan                                          |
| x &lt;= y &lt;= z |                                     Kleiner dan of gelijk aan                                     |
| x &gt;= y &gt;= z |                                   Groter dan of gelijk aan                                    |
|        (x)        |                           Haakjes overschrijven standaard voorrang.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Waarom worden mijn expressiebeperkingen niet correct gevalideerd?
U kunt geen gereserveerde sleutelwoorden gebruiken als oplossernamen voor kenmerken, onderdelen of subonderdelen in een productconfiguratiemodel. Hierna vindt u een lijst met de gereserveerde woorden die u niet kunt gebruiken:

-   Plafond
-   Element
-   Gelijk
-   Etage
-   Als
-   Kleiner
-   Groter
-   Heeft
-   Logboek
-   Max.
-   Min
-   Min
-   Plus
-   Vermogen
-   Tijden
-   Tijd
-   Model
-   Beslissing
-   Doel


<a name="additional-resources"></a>Aanvullende resources
--------

[Een expressiebeperking maken (taakbegeleider)](tasks/add-expression-constraint-product-configuration-model.md)

[Een berekening toevoegen aan een productconfiguratiemodel (taakbegeleiding)](tasks/add-calculation-product-configuration-model.md)



