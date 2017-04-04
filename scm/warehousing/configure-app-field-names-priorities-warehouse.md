---
title: App veldnamen in magazijnbeheer app configureren
description: In dit onderwerp wordt beschreven hoe definieer en configureer magazijn app veldnamen en prioriteiten in Dynamics 365 voor bewerkingen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>App veldnamen in magazijnbeheer app configureren

In dit onderwerp wordt beschreven hoe definieer en configureer magazijn app veldnamen en prioriteiten in Dynamics 365 voor bewerkingen. 

**opmerking:** in dit onderwerp geldt voor de functies in magazijnbeheer. Dit geldt niet voor functies in Voorraadbeheer. Dynamics 365 for Operations - opslag is een toepassing waarmee u kunt magazijn-taken uit te voeren. U kunt definiëren en configureren van de veldnamen die worden gebruikt in de app, alsmede configureren van de prioriteit waarmee de veldnamen moeten worden toegewezen. In dit onderwerp wordt uitgelegd hoe definieer en configureer deze magazijn app veldnamen en prioriteiten, en hoe ze worden gebruikt in Dynamics 365 for Operations - magazijnbeheer. Raadpleeg voor gedetailleerde informatie over het configureren van de verbinding met Dynamics 365 for Operations - magazijnen, de zelfstudie [installeren en configureren van Dynamics 365 for Operations - magazijnbeheer](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Magazijn app veldnamen configureren
===================================

Wanneer u Dynamics 365 voor bewerkingen gebruiken: Magazijnbeheer op het mobiele apparaat kunt u configureren hoe metagegevens moet worden weergegeven op het apparaat op de **magazijn app veldnamen** pagina. Selecteer in een nieuw bedrijf in Dynamics 365 for Operations **standaardinstellingen maken** voor het genereren van alle veldnamen die wordt gebruikt in het magazijn mobiel apparaat workflows en vervolgens een voorkeur invoermodus en invoertype toe te wijzen. Nadat u alle veldnamen hebt gegenereerd, kunt u de volgende opties voor invoer selecteren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optie</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Geprefereerde invoermethode</td>
<td>Deze optie bepaalt of een veld scannen of een invoerveld voor handmatige invoer moet worden weergegeven voor de geselecteerde veldnaam. Dit is handig om te onderscheiden van velden, afhankelijk van als streepjescodes worden gebruikt voor het veld. <strong>opmerking:</strong> voor veldnamen met voorkeur invoermodus is ingesteld op <strong>scannen</strong>, kunt u gegevens handmatig invoeren als de streepjescode onleesbaar of is beschadigd is.</td>
</tr>
<tr class="even">
<td>Invoertype</td>
<td>Deze optie bepaalt welk type ingang moet worden gebruikt voor de geselecteerde veldnaam. Er zijn vier opties beschikbaar:
<ul>
<li><strong>Selectie</strong> - bevat een lijst met opties waaruit u kunt kiezen. Veldnamen met deze optie kunnen niet worden bewerkt.</li>
<li><strong>Datum</strong> - veldnamen opgegeven datum een datumnotatie met het label wordt weergegeven. Dit helpt magazijnmedewerkers zien welke indeling voor de datum invoeren. Veldnamen met deze optie kunnen niet worden bewerkt.</li>
<li><strong>Alpha</strong> - als hebt geselecteerd, het toetsenbord apparaat wordt gebruikt wanneer u gegevens handmatig invoert in de toepassing. De ervaring toetsenbord kan worden gewijzigd, afhankelijk apparaat wordt gebruikt.</li>
<li><strong>Numerieke</strong> - voor die gebruik numerieke invoer alleen veldnamen kunt u deze optie om weer te geven van een aangepaste numeriek toetsenblok met het invoerveld in plaats van het toetsenbord apparaat.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Magazijn app veld prioriteit configureren
======================================

Op de **magazijn app veld prioriteit** pagina kunt u de veldnamen in andere prioriteitsvolgorde groepen plaatsen. Hierdoor kunt u bepalen welke informatie moet worden weergegeven op de pagina hoofdtaak wanneer magazijnmedewerkers uitvoeren met behulp van de toepassing. Als u op **standaardinstellingen maken**, een standaardset prioriteitsvolgorde groepen wordt gegenereerd. Het is mogelijk te maken van zoveel prioriteitsvolgorde groepen zo nodig, maar slechts drie prioriteitsvolgorde groepen worden weergegeven op de taakpagina. Dynamics 365 for Operations metagegevens naar de app verzendt, wordt deze elk veld een relatieve prioriteit, afhankelijk van de groep prioriteit toewijzen als de toepassing wordt de eerste drie prioriteit groepen in de metagegevens op de taakpagina weergegeven. De rest van de overlopende metagegevens wordt weergegeven op een secundaire detailpagina. De volgende tabel toont een voorbeeld van vijf groepen van prioriteit.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>De groep prioriteit</th>
<th>Toegewezen velden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Prioriteit 10</td>
<td><ul>
<li>Artikel</li>
<li>Hoeveelheid</li>
<li>Maateenheid</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteit 20</td>
<td><ul>
<li>Clusterpositie</li>
<li>Cluster</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioriteit 30</td>
<td><ul>
<li>Artikelomschrijving.</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteit 40</td>
<td><ul>
<li>Configuratie</li>
<li>Kleur</li>
<li>Grootte</li>
<li>Opmaakmodel</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioriteit 50</td>
<td><ul>
<li>Locatie</li>
<li>Nummerplaat</li>
</ul></td>
</tr>
</tbody>
</table>

Bijvoorbeeld wanneer een magazijnmedewerker een taak uitvoert op een mobiel apparaat als de metagegevens die worden weergegeven in de toepassing uit de volgende velden bestaat:

-   Artikel
-   Hoeveelheid
-   Maateenheid
-   Artikelomschrijving.
-   Grootte en locatie

Op basis van het magazijn app veld prioriteit instellen in de bovenstaande tabel, worden de volgende 3 rijen met gegevens weergegeven op de taakpagina:

-   Rij 1: Artikel, hoeveelheid, eenheid
-   Rij 2: De artikelomschrijving
-   Rij 3: grootte

De resterende metagegevens, bijvoorbeeld, de locatie wordt niet weergegeven op de taakpagina, maar op een detailpagina worden weergegeven. Raadpleeg voor meer informatie en voorbeelden bekijken van de gebruikersinterface, naar het blogbericht [aankondiging Dynamics 365 for Operations - magazijnbeheer](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Zie ook
--------

[Installeren en configureren van Microsoft Dynamics 365 voor bewerkingen: Magazijnbeheer](install-configure-warehousing-app.md)


