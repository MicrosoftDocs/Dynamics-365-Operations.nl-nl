---
title: Rapportdefinities in Ontwerper financiële rapporten
description: Dit artikel bevat informatie over rapportdefinities.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755439"
---
# <a name="report-definitions-in-financial-report-designer"></a>Rapportdefinities in Ontwerper financiële rapporten

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over rapportdefinities. Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken. Een rapportdefinitie bevat ook opties en instellingen voor het aanpassen van een rapport. 

Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken. Daarnaast biedt een rapportdefinitie opties en instellingen die u kunt gebruiken voor het aanpassen van een rapport. Nadat u rijdefinities en kolomdefinities hebt gedefinieerd, moet u deze in een rapportdefinitie combineren. Op dit punt definieert u ook andere aspecten van de definities, zoals het detailniveau en de rapportdatum. U kunt vervolgens een rapport opslaan en genereren. Financiële rapportage biedt de volgende detailniveaus:

- Financieel
- Financieel en Rekening
- Financieel, Rekening en Transactie

Afhankelijk van de wijze waarop gegevens worden opgeslagen in het Microsoft Dynamics ERP-systeem, zijn de transactiedetails misschien niet beschikbaar in de rapporten.

## <a name="create-a-report-definition"></a>Een rapportdefinitie maken
1. Klik in Report Designer in het menu **Bestand** op **Nieuw** en selecteer **Rapportdefinitie**.
2. Geef de gewenste informatie op in de tabbladen **Rapport**, **Uitvoer en distributie** **Kop- en voetteksten** en **Instellingen**.

## <a name="contents-of-a-report-definition"></a>Inhoud van een rapportdefinitie
In de volgende tabel worden de tabbladen in een rapportdefinitie beschreven en hoe de gegevens worden gebruikt.

<table>
<thead>
<tr>
<th>Tabblad</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rapport</td>
<td>Maak een rapport, configureer een rapport of wijzig een bestaand rapport.</td>
</tr>
<tr>
<td>Uitvoer en distributie</td>
<td>Wijzig het uitvoertype en de bestemming van het rapport.</td>
</tr>
<tr>
<td>Kop- en voetteksten</td>
<td>Definieer de kop- en voetteksten voor het rapport en maak deze op. U kunt bijvoorbeeld tekst of afbeeldingen aan de kop- of voettekst toevoegen. Financiële rapportage ondersteunt .bmp, .jpg en .png-bestanden voor afbeeldingen. U kunt ook Autotekstcodes toevoegen om andere informatie, zoals een bedrijfsnaam, rapportnaam of paginanummer, in te voegen.</td>
</tr>
<tr>
<td>Instellingen</td>
<td>Geef instellingen voor de rapportdefinitie op, zoals de volgende instellingen:
<ul>
<li>Opmaken en afronden van bedragen</li>
<li>Opmaken van detailrapporten</li>
<li>Opmaken van rapportagestructuren</li>
<li>Genereren van een uitzonderingenrapport</li>
<li>Opgeven van valutaomrekening</li>
<li>Subtotaal en filter van rekeningdetails</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Aanvullende resources

[Financiële rapportage](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]