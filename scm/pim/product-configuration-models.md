---
title: Overzicht productconfiguratiemodellen
description: "In dit artikel worden de termen en concepten gedefinieerd die relevant voor productconfiguratiemodellen zijn. Met productconfiguratiemodellen kunt u een generieke productstructuur maken, waarmee u veel productvarianten voor één product kunt configureren."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: yuyus
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 15af90d007d77a490db7cb540ef96b4104dbba7e
ms.lasthandoff: 03/31/2017


---

# <a name="product-configuration-models-overview"></a>Overzicht productconfiguratiemodellen

In dit artikel worden de termen en concepten gedefinieerd die relevant voor productconfiguratiemodellen zijn. Met productconfiguratiemodellen kunt u een generieke productstructuur maken, waarmee u veel productvarianten voor één product kunt configureren.

Productconfiguratiemodellen zijn gemaakt om een generieke productstructuur te vertegenwoordigen. Wanneer u een productconfiguratiemodel hebt ingesteld, kunt u een andere productvariant configureren, met een unieke stuklijst (BOM) en een unieke route. Productconfiguratiemodellen gebruiken zowel declaratieve als imperatieve berekeningen voor de relaties en beperkingen tussen verschillende productvarianten. U kunt artikelen configureren op verkooporders, verkoopoffertes, inkooporders en productieorders. De volgende tabel beschrijft de tabel op beperkingen gebaseerde termen en concepten.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Onderdelen</td>
<td>Onderdelen zijn de belangrijkste bouwstenen van een productconfiguratiemodel. Onderdelen worden weergegeven in een boomstructuur op de pagina <strong>Details van op beperkingen gebaseerd productconfiguratiemodel</strong>. Onderdelen kunnen de volgende elementen bevatten:
<ul>
<li>Kenmerken</li>
<li>Beperkingen</li>
<li>Berekeningen</li>
<li>Subonderdelen</li>
<li>Gebruikersvereisten</li>
<li>Stuklijstregels</li>
<li>Routebewerkingen</li>
</ul></td>
</tr>
<tr class="even">
<td>Kenmerken</td>
<td>Kenmerken beschrijven de functies van het productconfiguratiemodel. U kunt de kenmerken gebruiken om de functies op te geven die kunnen worden geselecteerd als een verschillend product is geconfigureerd. Kenmerken worden gebruikt in de beperkingen en voorwaarden. Als kenmerken worden gemaakt en worden toegevoegd aan een productconfiguratiemodel, wordt er naar de gerelateerde kenmerktypes verwezen. Een standaardwaarde kan worden ingesteld voor een kenmerk. De standaard waarde wordt gebruikt in de configuratie van de gebruikersinterface (UI) wanneer het productconfiguratiemodel is geconfigureerd. U kunt opgeven dat een kenmerk verplicht, alleen-lezen of verborgen is.
<ul>
<li><strong>Verplicht</strong> – Er moet een waarde voor het kenmerk worden ingesteld wanneer het product is geconfigureerd.</li>
<li><strong>Alleen-lezen</strong> – De waarde van het kenmerk wordt weergegeven tijdens een configuratiesessie, maar kan niet worden gewijzigd.</li>
<li><strong>Verborgen</strong> – De kenmerkwaarde is opgenomen in de beperkingen en voorwaarden, maar wordt niet weergegeven tijdens een configuratiesessie.</li>
</ul>
U kunt ook een voorwaarde voor kenmerken opgeven. Als er aan de voorwaarde is voldaan, moet er verplicht een waarde voor het kenmerk worden ingevoerd. Voorwaarden zijn expressies die moeten worden voldaan voor het toevoegen van kenmerken, stuklijstregels en routebewerkingen aan een productconfiguratiemodel. Elk kenmerk waarnaar in een voorwaarde wordt verwezen, wordt verplicht. Wij raden aan dat u kenmerken als verplicht selecteert in het tabblad <strong>Kenmerken</strong>. Hierdoor kunt eenvoudiger verplichte kenmerken identificeren. Waarden zijn een belangrijk onderdeel voor het hergebruik van configuraties. Het systeem gebruikt kenmerkwaarden om te bepalen of een configuratie bestaat die overeenkomt met de selecties die een gebruiker tijdens een configuratiesessie heeft gemaakt.</td>
</tr>
<tr class="odd">
<td>Kenmerktypen</td>
<td>Kenmerktypen bepalen de reeks gegevenstypen voor kenmerken die worden gebruikt in een productconfiguratiemodel. De volgende kenmerktypen worden gebruikt:
<ul>
<li><strong>Geheel getal</strong> met of zonder een bereik</li>
<li><strong>Decimaal</strong></li>
<li><strong>Tekst</strong> met of zonder een vaste lijst</li>
<li><strong>Booleaanse waarde</strong></li>
</ul>
Als het type kenmerk <strong>Booleaans</strong>, <strong>Geheel getal</strong> met een bereik, of <strong>Tekst</strong> met een vaste lijst is, is de set waarden beschikbaar wanneer een productconfiguratiemodel is ingesteld. <strong>Opmerking:</strong> De productconfiguratieoplosser herkent alleen de volgende typen kenmerken: <strong>Booleaans</strong>, <strong>Tekst</strong> met een vaste lijst en <strong>Geheel getal</strong> met een bereik. Daarom kunnen alleen deze kenmerkytypen worden gebruikt in de expressie beperkingen en voorwaarden.</td>
</tr>
<tr class="even">
<td>Beperkingen</td>
<td>Beperkingen beschrijven de beperkingen van het productconfiguratiemodel. Beperkingen worden gebruikt om te garanderen dat alleen geldige waarden zijn geselecteerd wanneer een product wordt geconfigureerd. Er zijn twee typen beperkingen: expressiebeperkingen en tabelbeperkingen:
<ul>
<li>Expressiebeperkingen kunnen alleen worden gebruikt voor het onderdeel waaraan ze gekoppeld zijn. De expressiebeperkingen voor een onderdeel kunnen echter verwijzen naar kenmerken van subonderdelen van het onderdeel. De productconfiguratieoplosser wordt gebruikt voor het oplossen van de beperkingen, en u moet de oplossersyntaxis gebruiken wanneer u de beperkingen schrijft. Zie de wiki-koppeling over expressiebeperkingen en tabelbeperkingen voor meer info.</li>
<li>Tabelbeperkingen moeten worden gedefinieerd voordat ze op een component in een productconfiguratie kunnen worden toegepast. Tabelbeperkingen kunnen door de gebruiker of door het systeem zijn gedefinieerd. Een gebruikergedefinieerde tabelbeperking is een matrix die kan worden gebruikt voor het beschrijven van combinaties voor de waarden die zijn gedefinieerd door het kenmerktypen. Als er bijvoorbeeld speakers worden geproduceerd, heeft de matrix voor een gebruikergedefinieerde tabelbeperking mogelijk kolommen voor de speakerafwerking en speaker grill.</li>
</ul>
<strong>Voorbeeld</strong> De speakers zijn beschikbaar in vier afwerkingen: Zwart, Eiken, Rozenhout en Wit. De speakers kunnen drie voorgrills hebben: Zwart, Metaal of Wit. De zwarte afwerking is beschikbaar voor alle grills, maar de andere afwerkingen zijn beperkt tot specifieke grills. De volgende tabel toont een voorbeeld van de informatie die op het tabblad <strong>Toegestane combinaties</strong> op de pagina <strong>Tabelbeperking bewerken</strong> wordt weergegeven.
<table>
<thead>
<tr class="header">
<th>Afwerking behuizing</th>
<th>Voorgrill</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zwart</td>
<td>Zwart</td>
</tr>
<tr class="even">
<td>Zwart</td>
<td>Metaal</td>
</tr>
<tr class="odd">
<td>Zwart</td>
<td>Wit</td>
</tr>
<tr class="even">
<td>Eiken</td>
<td>Zwart</td>
</tr>
<tr class="odd">
<td>Rozenhout</td>
<td>Wit</td>
</tr>
<tr class="even">
<td>Wit</td>
<td>Zwart</td>
</tr>
<tr class="odd">
<td>Wit</td>
<td>Wit</td>
</tr>
</tbody>
</table>
Een systeemgedefinieerde tabelbeperking vertegenwoordigt een koppeling tussen een kenmerktype en een veld in een Dynamics 365 for Operations-tabel. Een systeemgedefinieerde tabelbeperking koppelt dynamisch het kenmerktype aan het veld. Dankzij deze koppeling kan het kenmerk in een productconfiguratiemodel de gegevens van het veld in de Dynamics 365 for Operations-tabel weergeven.</td>
</tr>
<tr class="odd">
<td>Berekeningen</td>
<td>Berekeningen vertegenwoordigen een aanvulling op beperkingen. U kunt een berekening gebruiken om rekenkundige bewerkingen uit te voeren op kenmerken van de typen <strong>Decimaal</strong> en <strong>Geheel getal</strong>, of logische bewerkingen met kenmerken van de typen <strong>Tekst</strong> met een vaste lijst en <strong>Booleaans</strong>. Een berekening heeft een doelkenmerk dat het resultaat van de berekeningsexpressie bevat. De berekeningsexpressie wordt gebouwd met de expressie-editor.</td>
</tr>
<tr class="even">
<td>Subonderdelen</td>
<td>Subonderdelen weerspiegelen de structuur van het productconfiguratiemodel. U kunt subonderdelen gebruiken om de structuur van het productconfiguratiemodel te bouden. Subonderdelen verwijzen naar bestaande onderdelen. Subonderdelen moedigen daarom het hergebruik van onderdelen in meerdere productconfiguratiemodellen aan. U kunt op de pagina <strong>Regeldetails van stuklijst</strong> voor een subonderdeel een andere waarde voor het subonderdeel selecteren. U kunt ook een kenmerk selecteren waarvoor de waarde is geselecteerd wanneer het productconfiguratiemodel is ingesteld. Om een product als onderdeel of subonderdeel toe te voegen, moet u in de pagina<strong> Product maken</strong> de volgende info opgeven:
<ul>
<li>Selecteer in het veld <strong>Producttype</strong> de optie <strong>Artikel</strong>.</li>
<li>Selecteer in het veld <strong>Subtype van product</strong> de optie <strong>Productmodel</strong>.</li>
<li>Selecteer in het veld <strong>Configuratietechnologie</strong> de optie <strong>Op beperkingen gebaseerde configuratie</strong>.</li>
</ul>
U kunt bekijken of een vrijgegeven product kan worden gebruikt als een onderdeel of subonderdeel op het tabblad <strong>Algemeen</strong> van de pagina <strong>Vrijgegeven productdetails</strong>. Als <strong>Op beperkingen gebaseerde configuratie</strong> in het veld <strong>Configuratietechnologie</strong> is geselecteerd, kan het product als onderdeel of subonderdeel worden gebruikt. U kunt subonderdelen verbergen zodat ze niet voor de gebruiker worden weergegeven tijdens een configuratiesessie. Kenmerken, subonderdelen en gebruikerseisen met betrekking tot het subonderdeel worden ook verborgen.</td>
</tr>
<tr class="odd">
<td>Gebruikersvereisten</td>
<td>Gebruikerseisen vertegenwoordigen een abstractie tussen de gebruikerseisen en bepaalde onderdelen en kenmerken. U kunt een gebruikersvereiste niet toewijzen aan een artikel. Een klant zoekt bijvoorbeeld naar een home-theatersysteem. De verkoopvertegenwoordiger vraagt mogelijk naar de grootte van de kamer waar de klant het systeem wilt installeren, om te bepalen hoeveel watt er nodig is. In dit voorbeeld kan de kamergrootte een gebruikersvereiste zijn die de juiste kenmerkwaarde voor een specifiek onderdeel helpt bepalen. U kunt gebruikersvereisten verbergen zodat ze niet voor de gebruiker tijdens een configuratiesessie worden weergegeven. Kenmerken, subonderdelen en gebruikerseisen met betrekking tot de gebruikerseisen worden ook verborgen. U kunt een voorwaarde schrijven om te bepalen of een gebruikerseis kan worden verborgen. U moet de voorwaarde schrijven met de syntaxis Optimization Modeling Language (OML).</td>
</tr>
<tr class="even">
<td>Stuklijstregels</td>
<td>Stuklijstregels vertegenwoordigen de afzonderlijke materialen van de onderdelen in het productconfiguratiemodel. Op de pagina <strong>Regeldetails van stuklijst</strong> zijn alle artikelen beschikbaar voor selectie. Er kan een voorwaarde worden toegevoegd aan de stuklijstregel, zodat de stuklijstregels die zijn geselecteerd voor een andere productvariant kunnen variëren op basis van de gebruikersselectie als het productconfiguratiemodel wordt ingesteld. Voorwaarden zijn expressies die moeten worden voldaan voor het toevoegen van kenmerken, stuklijstregels en routebewerkingen aan een productconfiguratiemodel. Op de pagina <strong>Regeldetails van stuklijst</strong> kunt u een andere waarde selecteren. U kunt ook een kenmerk toewijzen waarvoor de waarde is geselecteerd wanneer het productconfiguratiemodel is ingesteld.</td>
</tr>
<tr class="odd">
<td>Routebewerkingen</td>
<td>Op de pagina <strong>Routebewerkingsdetails</strong> kunt u een andere waarde selecteren. U kunt ook een kenmerk toewijzen waarvoor de waarde is geselecteerd wanneer het productconfiguratiemodel is ingesteld. Voorwaarden worden geschreven als expressiebeperkingen. Voorwaarden zijn expressies die moeten worden voldaan voor het toevoegen van kenmerken, stuklijstregels en routebewerkingen aan een productconfiguratiemodel.</td>
</tr>
</tbody>
</table>




