---
title: Gegevens importeren vanuit Excel-sjablonen voor gegevensentiteiten die meerdere werkbladen bevatten
description: In dit onderwerp wordt beschreven hoe u gegevens importeert met Excel-gegevensentiteitsjablonen in Microsoft Dynamics 365 for Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551048"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a>Gegevens importeren vanuit Excel-sjablonen voor gegevensentiteiten die meerdere werkbladen bevatten

[!include [banner](../includes/banner.md)]

Gegevensbeheer in Microsoft Dynamics 365 for Finance and Operations ondersteunt Microsoft Excel-gebaseerde sjablonen voor gegevensentiteiten. Deze sjablonen kunnen een of meer werkbladen bevatten. Sjablonen met meerdere werkbladen worden vaak gebruikt wanneer het handig is om gegevens in één bestand te beheren en in verschillende gegevensentiteiten te importeren. Een voorbeeld hiervan zijn locaties en magazijnen.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Een bestand eenmaal uploaden en toewijzen aan alle entiteiten
We bekijken hier het voorbeeld van een Excel-bestand met de werkbladen **Locaties** en **Magazijnen**. Om het gegevensimportproject in te stellen, moet u de eerste gegevensentiteit **Locaties** toevoegen en het bestand vervolgens uploaden. U kunt **Locaties** als het werkblad voor deze entiteit selecteren.

Als u de tweede entiteit, **Magazijnen**, toevoegt zonder het formulier **Bestand toevoegen** te verlaten, kunt u het werkblad **Magazijnen** selecteren zonder het bestand opnieuw te hoeven uploaden. Alleen als de gegevens voor **Magazijnen** zich in een ander bestand bevinden, zou een nieuw bestand moeten worden geüpload.

![Meerdere werkbladen](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Toewijzing van werkblad aan entiteit corrigeren

De toewijzing van het werkblad aan een gegevensentiteit in de importtaak kan worden gecorrigeerd vanuit het raster. In de kolom **Werkblad** in het raster worden de werkbladen uit het toegewezen bestand weergegeven. U kunt een ander werkblad kiezen in de vervolgkeuzelijst. Als het gekozen werkblad al aan een entiteit in het gegevensproject is toegewezen, wordt u gevraagd de wijziging te bevestigen. Het is raadzaam om alle toewijzingen te corrigeren in het raster.

![Werkbladtoewijzing bijwerken](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Opnieuw toewijzen aan een nieuw bestand

In gevallen waarin een nieuwe versie van hetzelfde bestand of een volledig nieuw bestand moet worden geüpload voor bestaande entiteiten in een gegevensproject, moet u de ervaring **Bestand toevoegen** toevoegen en de entiteiten opnieuw toevoegen alsof ze voor het eerst worden toegevoegd. U wordt gevraagd of u de bestaande entiteiten in het gegevensproject wilt overschrijven. Entiteiten die niet opnieuw worden toegevoegd (of overschreven) blijven de vorige toewijzingen uit het vorige bestand houden.

## <a name="upload-a-file-using-run-project"></a>Een bestand uploaden met Project uitvoeren

U kunt een Excel-bestand uploaden met de optie **Project uitvoeren** om een importproject uit te voeren. Upload alleen bestanden met dezelfde werkbladen als de bestaande toewijzingen voor de gegevensentiteiten in het gegevensproject. Als een werkblad in het onlangs geüpload bestand niet wordt gevonden, wordt er een fout weergegeven en wordt er gestopt met importeren. Als de toewijzing aan het werkblad moet worden gewijzigd voor een entiteit, moeten de toewijzingen in het gegevensproject vanuit het gegevensproject worden bijgewerkt voordat u het bestand in de ervaring **Project uitvoeren** gebruikt.
