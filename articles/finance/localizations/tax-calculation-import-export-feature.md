---
title: Belastingberekeningen importeren en exporteren
description: Dit artikel biedt informatie over de import- en exportfunctionaliteit van de service voor belastingberekening.
author: Kai-Cloud
ms.date: 10/17/2022
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
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690228"
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

## <a name="import-feature-demo-data"></a>Demonstratiegegevens voor functie importeren

Volg deze stappen om demonstratiegegevens voor functies te importeren.

1. Meld u aan bij [RCS](https://marketing.configure.global.dynamics.com/).
2. Selecteer in de werkruimte **Globalisatiefuncties** de optie **Functies** en selecteer de tegel **Belastingberekening**.
3. Selecteer **Importeren** en selecteer vervolgens op de pagina **Functie importeren uit algemene opslagplaats** de optie **Synchroniseren**. 
4. Selecteer in de tabel de functie **tax-calculation-feature-demo-data** en selecteer vervolgens **Importeren**.
5. Selecteer **Weergeven** om de btw-codes, -groepen en -regels te controleren die in de geïmporteerde functie zijn gedefinieerd.
6. Ga in Finance naar de rechtspersoon **DEMF** en vervolgens naar **Belastingen** \> **Instellingen** \> **Belastingconfiguratie** \> **Parameters voor belastingberekening**.
7. Selecteer **Service voor belastingberekening inschakelen** op het tabblad **Algemeen**.
8. Selecteer **tax-calculation-feature-demo-data** in het veld **Naam van functie-instellingen**.
9. Selecteer een **vereffeningsperiode** en een **grootboekboekingsgroep** voor de nieuwe belastingcodes voor demonstraties en selecteer vervolgens **Bevestigen**.
10. Selecteer **Opslaan**.

> [!NOTE]
> De demonstratiefunctie **tax-calculation-feature-demo-data** is gebaseerd op functieversie **40.54.234** en is ontworpen voor de rechtspersoon **DEMF** voor demonstraties. Zorg ervoor dat Finance en RCS worden bijgewerkt naar versie 10.0.26 of hoger.
