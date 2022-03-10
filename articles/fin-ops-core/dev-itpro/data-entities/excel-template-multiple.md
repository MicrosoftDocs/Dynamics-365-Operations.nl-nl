---
title: Sjablonen met meerdere werkbladen
description: In dit onderwerp wordt beschreven hoe u gegevens importeert met Excel-gegevensentiteitsjablonen in Finance and Operations.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: cf3c423bdf06685a3c4025551927123773ae818a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070056"
---
# <a name="data-templates-with-multiple-worksheets"></a>Sjablonen met meerdere werkbladen

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Gegevensbeheer in de toepassing ondersteunt Microsoft Excel-sjablonen voor gegevensentiteiten. Deze sjablonen kunnen een of meer werkbladen bevatten. Sjablonen met meerdere werkbladen worden vaak gebruikt wanneer het handig is om gegevens in één bestand te beheren en in verschillende gegevensentiteiten te importeren. Een voorbeeld hiervan zijn locaties en magazijnen.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Een bestand eenmaal uploaden en toewijzen aan alle entiteiten
We bekijken hier het voorbeeld van een Excel-bestand met de werkbladen **Locaties** en **Magazijnen**. Om het gegevensimportproject in te stellen, moet u de eerste gegevensentiteit **Locaties** toevoegen en het bestand vervolgens uploaden. U kunt **Locaties** als het werkblad voor deze entiteit selecteren.

Als u de tweede entiteit, **Magazijnen**, toevoegt zonder het formulier **Bestand toevoegen** te verlaten, kunt u het werkblad **Magazijnen** selecteren zonder het bestand opnieuw te hoeven uploaden. Alleen als de gegevens voor **Magazijnen** zich in een ander bestand bevinden, zou een nieuw bestand moeten worden geüpload.

![Meerdere werkbladen.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Toewijzing van werkblad aan entiteit corrigeren

De toewijzing van het werkblad aan een gegevensentiteit in de importtaak kan worden gecorrigeerd vanuit het raster. In de kolom **Werkblad** in het raster worden de werkbladen uit het toegewezen bestand weergegeven. U kunt een ander werkblad kiezen in de vervolgkeuzelijst. Als het gekozen werkblad al aan een entiteit in het gegevensproject is toegewezen, wordt u gevraagd de wijziging te bevestigen. Het is raadzaam om alle toewijzingen te corrigeren in het raster.

![Werkbladtoewijzing bijwerken.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Opnieuw toewijzen aan een nieuw bestand

In gevallen waarin een nieuwe versie van hetzelfde bestand of een volledig nieuw bestand moet worden geüpload voor bestaande entiteiten in een gegevensproject, moet u de ervaring **Bestand toevoegen** toevoegen en de entiteiten opnieuw toevoegen alsof ze voor het eerst worden toegevoegd. U wordt gevraagd of u de bestaande entiteiten in het gegevensproject wilt overschrijven. Entiteiten die niet opnieuw worden toegevoegd (of overschreven) blijven de vorige toewijzingen uit het vorige bestand houden.

## <a name="upload-a-file-using-run-project"></a>Een bestand uploaden met Project uitvoeren

U kunt een Excel-bestand uploaden met de optie **Project uitvoeren** om een importproject uit te voeren. Upload alleen bestanden met dezelfde werkbladen als de bestaande toewijzingen voor de gegevensentiteiten in het gegevensproject. Als een werkblad in het onlangs geüpload bestand niet wordt gevonden, wordt er een fout weergegeven en wordt er gestopt met importeren. Als de toewijzing aan het werkblad moet worden gewijzigd voor een entiteit, moeten de toewijzingen in het gegevensproject vanuit het gegevensproject worden bijgewerkt voordat u het bestand in de ervaring **Project uitvoeren** gebruikt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
