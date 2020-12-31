---
title: Werkgebied Controlelijst voor gegevensvalidatie
description: Met het werkgebied Controlelijst voor gegevensvalidatie kunt u processen voor validatie van gegevens over bedrijven, gebieden en mensen volgen. De controlelijst kan worden gebruikt tijdens een nieuwe implementatie, na een upgrade of na een migratie.
author: bking
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DataValidationWorkspace
audience: Application User
ms.reviewer: rhaertle
ms.assetid: ''
ms.search.region: Global
ms.author: bking
ms.openlocfilehash: a3ac338670fdc9fc7cb526cdcdc1e7199904da8f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687570"
---
# <a name="data-validation-checklist-workspace"></a>Werkgebied Controlelijst voor gegevensvalidatie

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van het werkgebied **Controlelijst voor gegevensvalidatie** en de bijbehorende configuratie.

Met het werkgebied **Controlelijst voor gegevensvalidatie** kunt u processen voor validatie van gegevens over bedrijven, gebieden en mensen volgen. De controlelijst kan worden gebruikt tijdens een nieuwe implementatie, na een upgrade of na een migratie. Afhankelijk van uw weergave van het werkgebied **Controlelijst voor gegevensvalidatie** ziet u alle taken en statussen voor een gegevensvalidatieproject, of alleen de taken die aan u zijn toegewezen.

U moet eerst een gegevensvalidatieproject boven in het werkgebied selecteren. Alle gegevens die worden weergegeven in het werkgebied, worden vervolgens gefilterd op het geselecteerde gegevensvalidatieproject.

## <a name="summary-tiles"></a>Overzichtstegels

De tegels **Overzicht** bieden een overzicht van het proces en bevatten indicatoren die u helpen het gegevensvalidatieproces te volgen. U ziet alle resterende taken, voltooide taken, taken in uitvoering en niet-gestarte taken voor het proces. Deze informatie is bestemd voor alle bedrijven die zijn opgenomen in het geselecteerde gegevensvalidatieproject.

## <a name="tasks-and-status-section"></a>Sectie Taken en status

In de sectie **Taken en status** wordt de status van het algehele gegevensvalidatieproject weergegeven op verschillende manieren: status per rechtspersoon, per gebied en per takenlijst. U kunt het filter selecteren om de status voor een specifiek bedrijf weer te geven. Elk statustabblad bevat een specificatie op basis van het percentage dat is voltooid en het aantal taken dat resteert.

Het laatste tabblad is voor de gedetailleerde takenlijst. Deze lijst bevat de volledige takenlijst.
U kunt de lijst met taken op verschillende manieren filteren. Klik op **Taak bewerken** om de status van een taak te wijzigen of een taak toe te wijzen. Klik op **Bijlagen** om bijlagen voor een taak te bekijken.

De naam van de taak is een hyperlink naar de pagina waar de gebruiker naartoe moet gaan om het werk te voltooien. U kunt deze hyperlink vervolgens instellen met behulp van het veld **Naam menuopdracht** wanneer u een taak bewerkt of maakt via het formulier **Gegevensvalidatieproject configureren**.

U kunt bestanden, notities, afbeeldingen en URL's aan een taak koppelen met behulp van de actie **Bijlagen**. U kunt bijvoorbeeld een rapportbestand bijvoegen dat is afgedrukt voor een taak. Er verschijnt een pictogram in de kolom **Bijlage** voor de taak als er een bijlage aanwezig is.

De optie **Ingevuld door** wordt automatisch nadat de taak is voltooid, ingevuld met de naam van de medewerker die de taak heeft voltooid. Als een taak wordt gemarkeerd als voltooid, wordt het veld **Datum van voltooiing** automatisch bijgewerkt in de huidige datum en tijd.

## <a name="configure-data-validation-project-page"></a>Pagina Gegevensvalidatieproject configureren

Voordat u het werkgebied **Controlelijst voor gegevensvalidatie** kunt gebruiken, moet u het proces met behulp van de **Gegevensvalidatieproject configureren** configureren. (Klik op **Werkgebieden** \> **Controlelijst voor gegevensvalidatie** \> **Gegevensvalidatieproject configureren**.)

## <a name="task-areas"></a>Taakgebieden

U gebruikt taakgebieden om gegevensvalidatietaken te groeperen in logische gebieden van eigendom in uw organisatie. Leveranciers, Klanten of Grootboek kunnen bijvoorbeeld als taakgebieden worden gebruikt.

De optie **Naam menuopdracht** wordt gekoppeld aan de taakwerkinzet en kan worden gebruikt om rechtstreeks naar de gekoppelde pagina te gaan via de taakkoppeling in het werkgebied. Bijvoorbeeld een gegevensvalidatietaak om het rapport **Ouderdom van leveranciers** voor leveranciers uit te voeren, kan worden gekoppeld aan de **Rapport Ouderdom van leveranciers**.
