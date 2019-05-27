---
title: Inkomende documenten in Excel-indeling parseren
description: Dit onderwerp biedt informatie over het ontwerpen van ER-indelingen (elektronische rapportage) om inhoud van binnenkomende Microsoft Excel-bestanden te parseren.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545048"
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

Als u de volgende taakbegeleiding [ER vereiste configuraties maken om gegevens te importeren uit een extern bestand](./tasks/er-required-configurations-import-data.md) nog niet hebt afgespeeld in de huidige Dynamics 365 for Finance and Operation-toepassing, downloadt u het volgende bestand.

| Omschrijving inhoud    | Bestand                                                            |
|------------------------|-----------------------------------------------------------------|
| ER-modelconfiguratie | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
