---
title: Belastingberekeningen importeren en exporteren
description: Dit artikel biedt informatie over de import- en exportfunctionaliteit van de service voor belastingberekening.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 9daee683763d7cb0eb9573497eb4e20cba9b1863
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855168"
---
# <a name="import-and-export-tax-calculations"></a>Belastingberekeningen importeren en exporteren

Dit artikel biedt informatie over de import- en exportfunctionaliteit van de service voor belastingberekening. Deze functionaliteit zorgt voor een flexibele en efficiënte configuratie-ervaring.

## <a name="import-and-export-tax-codes"></a>Belastingcodes importeren en exporteren

### <a name="export-templates"></a>sjablonen exporteren

1. Meld u aan bij [RCS (Regulatory Configuration Service)](https://marketing.configure.global.dynamics.com/).
2. Selecteer in de werkruimte **Globalisatiefuncties** de optie **Functies** en selecteer de tegel **Belastingberekening**.
3. Selecteer een bestaande functie of [maak een nieuwe functie](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Selecteer **Bewerken** in het raster **Versies**.
5. Stel de [configuratieversie](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) in op de functiepagina **Belastingberekening**.
6. Selecteer **Importeren** op het tabblad **Belastingcodes**.
7. Selecteer **Een belastingcodesjabloon exporteren** om het zipbestand **TaxCodesTemplate.zip** te downloaden.
8. Pak **TaxCodesTemplate.zip** uit. De belastingcodesjablonen worden afzonderlijk gecomprimeerd volgens de waarde **Oorsprong van berekening**.
9. Pak **By Net Amount.zip** uit om de volgende CSV-bestanden (Comma Separated Values) op te halen:

    - **TaxCode.csv**: voer de belastingcodes in.
    - **TaxLimit.csv**: voer de belastinglimieten in voor elke belastingcode.
    - **TaxRate.csv**: voer de belastingtarieven in voor elke belastingcode.

> [!NOTE]
> Standaard zijn vermeldingen voor de **voorbeeldbelastingcode** beschikbaar in de sjablonen. Als de **voorbeeldbelastingcode** niet uit de CSV-bestanden wordt verwijderd, wordt deze in de functie geïmporteerd.

### <a name="import-tax-codes"></a>Belastingcodes importeren

Volg deze stappen om de **voorbeeldbelastingcode** in de sjabloon te importeren in de functie voor belastingberekening.

1. Selecteer **Importeren** op het tabblad **Belastingcodes** van de functiepagina **Belastingberekening** in RCS.
2. Selecteer **Bladeren**, zoek en selecteer het bestand **TaxCode.csv** en selecteer vervolgens **Belastingcode** in het veld **Doeltabel**.
3. Selecteer **OK** om de belastingcode te importeren.
4. Zoek en selecteer het bestand **TaxRate.csv** en selecteer vervolgens **Belastingtarief** in het veld **Doeltabel**.
5. Selecteer **OK** om het belastingtarief te importeren.
6. Zoek en selecteer het bestand **TaxLimit.csv** en selecteer vervolgens **Belastinglimiet** in het veld **Doeltabel**.
7. Selecteer **OK** om de belastinglimiet te importeren.

U kunt ook direct het zipbestand met alle drie de CSV-bestanden importeren. Op deze manier kunt u het importeren snel en eenvoudig voltooien.

1. Selecteer **Importeren** op het tabblad **Belastingcodes** van de functiepagina **Belastingberekening** in RCS.
2. Selecteer **Bladeren**, zoek en selecteer het zipbestand **By Net Amount.zip** en selecteer **OK**.

### <a name="export-tax-codes"></a>Belastingcodes exporteren

1. Selecteer **Exporteren** op het tabblad **Belastingcodes** van de functiepagina **Belastingberekening** in RCS.

    De knop **Exporteren** is beschikbaar als er minimaal één belastingcode is in het raster **Belastingcodes**.

2. Selecteer **OK** om alle belastingcodes van de functie in een zipbestand te exporteren.

> [!NOTE]
> Gebruik het geëxporteerde bestand als een sjabloon om belastingcodes in de bijbehorende functie te importeren.

## <a name="import-and-export-applicability-rules"></a>Toepasbaarheidsregels importeren en exporteren

### <a name="export-applicability-rules"></a>Toepasbaarheidsregels exporteren

1. Meld u aan bij [RCS](https://marketing.configure.global.dynamics.com/).
2. Selecteer in de werkruimte **Globalisatiefuncties** de optie **Functies** en selecteer de tegel **Belastingberekening**.
3. Selecteer een bestaande functie of [maak een nieuwe functie](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Selecteer **Bewerken** in het raster **Versies**.
5. Stel de [configuratieversie](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) in op de functiepagina **Belastingberekening**.
6. Selecteer op het tabblad **Toepasbaarheid belastinggroep** de rijen in het raster **Toepasbaarheid belastinggroep instellen**.
7. Selecteer de knop **Openen in Microsoft Office** en selecteer vervolgens **Dynamische toepasbaarheidsmatrix voor belastingservice**.

    [![Toepasbaarheidsregels exporteren naar Microsoft Excel op de functiepagina Belastingberekening.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Selecteer **Downloaden** om de geselecteerde rijen naar een Microsoft Excel-werkblad te exporteren.

### <a name="import-applicability-rules"></a>Toepasbaarheidsregels importeren

Het Excel-werkblad dat u hebt gedownload, bevat de structuur van het raster **Toepasbaarheid belastinggroep instellen**. U kunt nieuwe regels direct aan het werkblad toevoegen. Wanneer u klaar bent, volgt u deze stappen om de nieuwe regels weer te importeren in het raster **Toepasbaarheid belastinggroep instellen**.

1. Selecteer in het Excel-werkblad de rijen die u wilt importeren en kopieer deze.
2. In RCS selecteert u op de functiepagina **Belastingberekening** op het tabblad **Toepasbaarheid belastinggroep** de optie **Toevoegen** om een lege record onder aan het raster **Toepasbaarheid belastinggroep instellen** in te voegen.
3. Selecteer **Ctrl+V** om de gekopieerde rijen in het raster te plakken.
4. Selecteer **Opslaan**.
