---
title: Inkomende documenten in Excel-indeling parseren
description: Dit onderwerp biedt informatie over het ontwerpen van ER-indelingen (elektronische rapportage) om inhoud van binnenkomende Microsoft Excel-bestanden te parseren.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755175"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Inkomende documenten in Excel-indeling parseren

[!include[banner](../includes/banner.md)]

U kunt ER-indelingen ontwerpen om binnenkomende Microsoft Excel-bestanden te parseren die gegevens in Microsoft Excel-werkmappen (bestanden in XLSX-indeling) vertegenwoordigen. Vervolgens kunt u de inhoud van deze bestanden gebruiken om toepassingsgegevens bij te werken. Dit is handig als u het volgende doet:

- Een nieuw model en indeling ontwerpen en ze willen testen tijdens de uitvoering. Excel simuleert in dit geval de feitelijke toepassingsgegevens.
- Gegevens beheren buiten uw toepassing in Excel en deze gegevens vervolgens importeren om een specifiek rapport in te dienen.

Voor meer informatie over deze functie speelt u de taakbegeleidingen **ER gegevens importeren uit een Microsoft Excel-bestand (deel 1: Ontwerpindeling)** en **ER gegevens importeren uit een Microsoft Excel-bestand (deel 2: Gegevens importeren)** (delen van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af. Deze taakbegeleidingen begeleiden u door het parseren van het binnenkomende Excel-bestand met behulp van de ER-indeling om gegevens te importeren uit binnenkomende documenten en toepassingsgegevens bij te werken. U kunt de taakbegeleiding downloaden uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684).

Download de volgende bestanden om de hierboven genoemde taakbegeleidingen te voltooien:

| Omschrijving inhoud                         | Bestand                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Binnenkomend bestand in. XLSX-indeling - sjabloon    | [1099import template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Binnenkomend bestand in. XLSX-indeling - voorbeeldgegevens | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Als u de volgende taakbegeleiding [ER vereiste configuraties maken om gegevens te importeren uit een extern bestand](./tasks/er-required-configurations-import-data.md) nog niet hebt afgespeeld in de huidige Finance and Operations-toepassing, downloadt u het volgende bestand.

| Omschrijving inhoud    | Bestand                                                            |
|------------------------|-----------------------------------------------------------------|
| ER-modelconfiguratie | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]