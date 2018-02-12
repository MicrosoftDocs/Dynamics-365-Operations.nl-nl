---
title: "Rapportdefinities in Ontwerper financiële rapporten"
description: Dit artikel bevat informatie over rapportdefinities. Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken. Een rapportdefinitie bevat ook opties en instellingen voor het aanpassen van een rapport.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58030df8db467f754ec93ecc3f41585b20f03893
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="report-definitions-in-financial-report-designer"></a>Rapportdefinities in Ontwerper financiële rapporten

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over rapportdefinities. Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken. Een rapportdefinitie bevat ook opties en instellingen voor het aanpassen van een rapport. 

Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken. Daarnaast biedt een rapportdefinitie opties en instellingen die u kunt gebruiken voor het aanpassen van een rapport. Nadat u rijdefinities en kolomdefinities hebt gedefinieerd, moet u deze in een rapportdefinitie combineren. Op dit punt definieert u ook andere aspecten van de definities, zoals het detailniveau en de rapportdatum. U kunt vervolgens een rapport opslaan en genereren. Financiële rapportage biedt de volgende detailniveaus:

-   Financieel
-   Financieel en Rekening
-   Financieel, Rekening en Transactie

Afhankelijk van hoe de gegevens in het Microsoft Dynamics ERP-systeem worden opgeslagen, zijn transactiedetails mogelijk niet beschikbaar in rapporten.

## <a name="create-a-report-definition"></a>Een rapportdefinitie maken
1.  Klik in Report Designer in het menu **Bestand** op **Nieuw** en selecteer **Rapportdefinitie**.
2.  Geef de gewenste informatie op in de tabbladen **Rapport**, **Uitvoer en distributie** **Kop- en voetteksten** en **Instellingen**.

## <a name="contents-of-a-report-definition"></a>Inhoud van een rapportdefinitie
In de volgende tabel worden de tabbladen in een rapportdefinitie beschreven en hoe de gegevens worden gebruikt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tabblad</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rapport</td>
<td>Maak een rapport, configureer een rapport of wijzig een bestaand rapport.</td>
</tr>
<tr class="even">
<td>Uitvoer en distributie</td>
<td>Wijzig het uitvoertype en de bestemming van het rapport.</td>
</tr>
<tr class="odd">
<td>Kop- en voetteksten</td>
<td>Definieer de kop- en voetteksten voor het rapport en maak deze op. U kunt bijvoorbeeld tekst of afbeeldingen aan de kop- of voettekst toevoegen. Financiële rapportage ondersteunt .bmp, .jpg en .png-bestanden voor afbeeldingen. U kunt ook Autotekstcodes toevoegen om andere informatie, zoals een bedrijfsnaam, rapportnaam of paginanummer, in te voegen.</td>
</tr>
<tr class="even">
<td>Instellingen</td>
<td>Geef instellingen voor de rapportdefinitie op, zoals de volgende instellingen:
<ul>
<li>Opmaken en afronden van bedragen</li>
<li>Opmaken van detailrapporten</li>
<li>Opmaken van rapportagestructuren</li>
<li>Genereren van een uitzonderingenrapport</li>
<li>Opgeven van valutaomrekening</li>
<li>Subtotaal en filter van rekeningdetails</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Zie ook
--------

[Financiële rapportage](financial-reporting-intro.md)




