---
title: Velden configureren voor de mobiele app Magazijnbeheer
description: In dit onderwerp wordt beschreven hoe u veldnamen en prioriteiten van velden die worden weergegeven in de mobiele app Magazijnbeheer kunt definiëren en configureren.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 31b1d9e26a5c21a6be5fd89992316e1d6e657c183a71d5155d8d76e83362c845
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721146"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Velden configureren voor de mobiele app Magazijnbeheer

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veldnamen en prioriteiten van velden die worden weergegeven in de mobiele app Magazijnbeheer kunt definiëren en configureren.

> [!NOTE]
> Dit onderwerp is van toepassing op functies in Magazijnbeheer. Het geldt niet voor functies in Voorraadbeheer. De mobiele app Magazijnbeheer is een toepassing waarmee u magazijntaken kunt uitvoeren. U kunt de in de app gebruikte veldnamen definiëren en configureren en u kunt ook de prioriteit configureren waaraan de veldnamen moeten worden toegewezen. In dit onderwerp wordt uitgelegd hoe u deze veldnamen en prioriteiten van de mobiele app Magazijnbeheer kunt definiëren en configureren en hoe ze worden gebruikt in Magazijnbeheer.

## <a name="configure-warehouse-app-field-names"></a>Veldnamen van magazijnapp configureren

Wanneer u Magazijnbeheer op uw mobiele apparaat gebruikt, kunt u configureren hoe metagegevens moeten worden weergegeven op uw apparaat op de pagina **Veldnamen magazijnapp**. Selecteer in een nieuw bedrijf **Standaardinstelling maken** om alle veldnamen te genereren die worden gebruikt in de magazijnworkflows van het mobiele apparaat en wijs er vervolgens een gewenste invoermodus en invoertype aan toe. Nadat u alle veldnamen hebt gegenereerd, kunt u de volgende invoeropties selecteren.

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
<td>Met deze optie wordt bepaald of het veld Scannen of een invoerveld voor handmatige invoer moet worden weergegeven voor de geselecteerde veldnaam. Dit is handig om velden te onderscheiden, afhankelijk van de vraag of er streepjescodes voor het veld worden gebruikt. <strong>Opmerking:</strong> voor veldnamen waarvan de gewenste invoermodus is ingesteld op <strong>Scannen</strong>, kunt u gegevens handmatig invoeren als de streepjescode onleesbaar of is beschadigd is.</td>
</tr>
<tr class="even">
<td>Invoertype</td>
<td>Met deze optie wordt bepaald welk invoertype moet worden gebruikt voor de geselecteerde veldnaam. Er zijn vier opties beschikbaar:
<ul>
<li><strong>Selectie</strong> - bevat een lijst met opties waaruit u kunt kiezen. Veldnamen met deze optie kunnen niet worden bewerkt.</li>
<li><strong>Datum</strong> - veldnamen die zijn opgegeven als datum, bevatten een datumnotatie met het label. Aan de hand hiervan kunnen magazijnmedewerkers zien in welke notatie de datum moet worden ingevoerd. Veldnamen met deze optie kunnen niet worden bewerkt.</li>
<li><strong>Alfa</strong> - als deze optie is geselecteerd, wordt het toetsenbord van het apparaat gebruikt bij het handmatig invoeren van gegevens in de app. De toetsenbordervaring kan worden gewijzigd. Dit hangt af van het apparaat dat wordt gebruikt.</li>
<li><strong>Numeriek</strong> - voor veldnamen waarin alleen numerieke invoer wordt gebruikt, kunt u deze optie selecteren om een aangepast numeriek toetsenblok weer te geven met het invoerveld in plaats van het toetsenbord van het apparaat.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Veldprioriteit van magazijnapp configureren

Op de pagina **Veldprioriteit van magazijnapp** kunt u veldnamen in verschillende prioriteitsgroepen plaatsen. Hierdoor kunt u bepalen welke informatie moet worden weergegeven op de hoofdtaakpagina wanneer magazijnmedewerkers taken uitvoeren met de app. Als u op **Standaardinstelling maken** klikt, wordt een standaardset prioriteitsgroepen gegenereerd. Het is mogelijk zoveel prioriteitsgroepen te maken als nodig is, maar slechts drie prioriteitsgroepen worden op de taakpagina weergegeven. Als het systeem metagegevens naar de app verzendt, wordt aan elk veld een relatieve prioriteit toegewezen, afhankelijk van de bijbehorende prioriteitsgroep. In de app worden de eerste prioriteitsgroepen in de metagegevens op de taakpagina weergegeven. De rest van de overlopende metagegevens wordt weergegeven op een secundaire detailpagina. De volgende tabel bevat een voorbeeld van vijf prioriteitsgroepen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioriteitsgroep</th>
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

Als een magazijnmedewerker bijvoorbeeld een taak uitvoert op een mobiel apparaat, als de metagegevens die worden weergegeven in de app uit de volgende velden bestaan:

-   Artikel
-   Hoeveelheid
-   Maateenheid
-   Artikelomschrijving.
-   Grootte en locatie

Op basis van de instellingen van de veldprioriteit van de magazijnapp in de bovenstaande tabel worden de volgende 3 rijen met gegevens weergegeven op de taakpagina:

-   Rij 1: Artikel, Hoeveelheid, Maateenheid
-   Rij 2: Artikelomschrijving
-   Rij 3: Grootte

De resterende metagegevens, bijvoorbeeld Locatie, worden niet weergegeven op de taakpagina, maar worden op een detailpagina weergegeven. Raadpleeg voor meer informatie en voorbeelden van de gebruikersinterface het blogbericht [Finance and Operations - Magazijnbeheer aankondigen](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

## <a name="additional-resources"></a>Aanvullende bronnen

[De mobiele app Magazijnbeheer installeren en verbinden](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]