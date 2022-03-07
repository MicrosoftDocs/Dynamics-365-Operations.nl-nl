---
title: Inkomende documenten in JSON-indeling parseren
description: In dit onderwerp wordt uitgelegd hoe u ER-indelingen (elektronische rapportage) kunt instellen om binnenkomende documenten in JSON-indeling (JavaScript Object Notation) te parseren.
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba30b06cc0c4af230113d532a932594278e13b29a87e6252849483c9dfcbc198
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713913"
---
# <a name="parse-incoming-documents-in-json-format"></a>Inkomende documenten in JSON-indeling parseren

[!include[banner](../includes/banner.md)]

U kunt ER-indelingen ontwerpen voor het parseren van inkomende elektronische documenten die gegevens in een tekstindeling vertegenwoordigen die is gebaseerd op Javascript (met andere woorden, bestanden in de \[JSON\]-indeling).

Als u meer wilt weten over deze functie, downloadt u de bestanden in de volgende tabel en speelt u de taakbegeleider ER Een indelingsconfiguratie maken om gegevens uit een extern JSON-bestand te importeren af. In deze taakbegeleider wordt weergegeven hoe een ER-indeling kan worden gebruikt om een binnenkomend JSON-bestand te parseren om toepassingsgegevens bij te werken.

| Titel                                  | Bestandsnaam |
|----------------------------------------|-----------|
| ER-indelingsconfiguratie                | [Indeling voor het importeren van trans_JSON. XML van leveranciers](https://go.microsoft.com/fwlink/?linkid=874111) |
| Voorbeeld van binnenkomend bestand in CSV-indeling | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Behoeften

Voordat u de taakbegeleider ER Een indelingsconfiguratie maken om gegevens uit een extern JSON-bestand te importeren voltooit, moet aan de volgende vereiste zijn voldaan:

- Bovenliggende elementen in het JSON-bestand kunnen alleen objectelementen zijn.
- Geneste elementen voor een object moeten eigenschapselementen zijn, zodat een geldige JSON-structuur wordt gemaakt.
- JSON-matrices kunnen alleen geneste elementen zijn van de eigenschapselementen van een object.
- JSON-matrices kunnen alleen JSON-objecten bevatten. Ze kunnen geen directe tekenreeks/numerieke waarden en geneste matrices bevatten. Elementen in deze matrices worden geparseerd in de volgorde waarin ze in de indeling zijn opgegeven. Voor elk JSON-object wordt rekening gehouden met instellingen voor multipliciteit.

Bovendien moet u de taakbegeleider [ER Vereiste configuraties maken om gegevens te importeren uit een extern bestand](tasks/er-required-configurations-import-data.md) uitvoeren als u dit nog niet hebt gedaan. Download het volgende bestand om de taakbegeleiding te voltooien.

| Titel                  | Bestandsnaam |
|------------------------|-----------|
| ER-modelconfiguratie | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]