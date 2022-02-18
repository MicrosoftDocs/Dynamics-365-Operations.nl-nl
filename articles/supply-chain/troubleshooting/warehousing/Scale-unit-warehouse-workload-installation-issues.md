---
title: Verwerkingsproblemen treden op nadat de workload van een magazijn voor een schaaleenheid is geïnstalleerd
description: In dit onderwerp worden problemen beschreven die zich kunnen voordoen nadat de workload van een schaaleenheid voor magazijnen is geïnstalleerd en vindt u advies om deze problemen op te lossen.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071635"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Verwerkingsproblemen treden op nadat de workload van een magazijn voor een schaaleenheid is geïnstalleerd

In dit onderwerp worden problemen beschreven die zich kunnen voordoen nadat de workload van een schaaleenheid voor magazijnen is geïnstalleerd en vindt u advies om deze problemen op te lossen.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Probleem 1: fout nadat een workload is vrijgegeven vanuit een workbench voor ladingplanning

### <a name="symptoms-of-issue-1"></a>Symptomen van probleem 1

Wanneer u een lading vrijgeeft via de pagina **Workbench voor ladingplanning** of **Workbench voor uitgaande ladingplanning**, wordt een foutbericht weergegeven in de volgende vorm:

> Er is een uitzondering opgetreden bij het boeken van de lading%1: de lading kan niet worden vrijgegeven.
> 
> UPDATE WHSSHIPMENTTABLE SET ...
> 
> Kan een record in zendingen niet bewerken (WHSShipmentTable). Zending-id: ...

Hier is een werkelijk voorbeeld met voorbeeldgegevens:

> Er is een uitzondering opgetreden bij het boeken van de lading USMF-000033. De lading kan niet worden vrijgegeven.
session 5133 (Admin)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? WHERE ((RECID=?) AND (RECVERSION=?))  
> [Microsoft][ODBC-stuurprogramma 17 voor SQL Server] [SQL Server] Schaaleenheid @@ heeft geprobeerd records bij te werken die het eigendom zijn van schaaleenheid @A.  
> Object Server Azure:
>
> Kan een record in zendingen niet bewerken (WHSShipmentTable). Zending-id: USMF-000031, USMF-000033. De SQL-database heeft een fout gegenereerd:

### <a name="cause-of-issue-1"></a>Oorzaak van probleem 1

Dit probleem kan optreden als de volgende combinatie van voorwaarden bestaat wanneer u de workload van een schaaleenheid voor magazijnen installeert:

- Het systeem bevat een niet-vrijgegeven lading waarbij meerdere regels aan verschillende orders worden gekoppeld en sommige ladingregels niet aan een zending worden gekoppeld.
- Het systeem is ingesteld op consolidatie van de zending.

In een gedistribueerde implementatie van een hybride topologie wordt elke ladings- en zendingsrecord gemarkeerd als eigendom van een specifieke schaaleenheid of hub. Als u een lading vrijgeeft via de pagina **Workbench voor ladingplanning**, wordt het toegewezen eigendom gewijzigd. Het kan echter zijn dat het systeem vanwege de eerder vermelde voorwaarden het gegevenseigendom niet kan herleiden. Daarom kan de lading niet aan het magazijn worden vrijgegeven.

### <a name="resolution-of-issue-1"></a>Oplossing van probleem 1

De lading opsplitsen in twee kleinere ladingen voordat u deze vrijgeeft aan het magazijn.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Probleem 2: fout tijdens de verwerking van een wave voor een schaaleenheid

### <a name="symptoms-of-issue-2"></a>Symptomen van probleem 2

Wanneer u een wave voor een schaaleenheid verwerkt, ontvangt u een foutmelding in de volgende vorm:

> U kunt ladingregel met ontvangst-id = %1, lading-id= %2 niet wijzigen omdat deze nog steeds in eigendom is van de bedrijfshub. Controleer of de bijbehorende uitgaande lading is vrijgegeven aan een schaaleenheid en dat er daardoor magazijnorderregels zijn gemaakt.

Hier is een werkelijk voorbeeld met voorbeeldgegevens:

> Infologboek voor taak Wave uitvoeren USMF-000000012 (9223377668365210)  
> Infologboek voor taak Wave uitvoeren USMF-000000012 (9223377668370462)  
> U kunt ladingregel met ontvangst-id = 68719478242, lading-id = USMF-000034 niet wijzigen omdat deze nog steeds in eigendom is van de bedrijfshub. Controleer of de bijbehorende uitgaande lading is vrijgegeven aan een schaaleenheid en dat er daardoor magazijnorderregels zijn gemaakt.

### <a name="cause-of-issue-2"></a>Oorzaak van probleem 2

In een gedistribueerde implementatie van een hybride topologie wordt het eigendom van de lading- en zendingsgegevens toegewezen aan een specifieke schaaleenheid of hub. Als onderdeel van de waveverwerking wordt het eigendom van de gegevens naar verwachting toegewezen aan een schaaleenheid.

Als u de workload van een schaaleenheid voor magazijnen installeert als een openstaande zending is gekoppeld aan een lading en een magazijn, kan het eigendom van de gegevens in het systeem niet worden beheerd. Daarom mislukt de waveverwerking voor de schaaleenheid.

### <a name="resolution-of-issue-2"></a>Oplossing van probleem 2

Geef de lading vanuit de hub vrij aan het magazijn.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Problemen oplossen door het eigendom en de bestemming van een record weer te geven

In een gedistribueerde implementatie van een hybride topologie worden veel typen records gemarkeerd als eigendom van een specifieke schaaleenheid of hub. Wanneer u overschakelt naar een gedistribueerde hybride topologie en/of een nieuwe magazijnworkload voor schaaleenheden hebt ingesteld, wordt het eigendom toegewezen aan elke relevante record. Dit proces kan soms tot fouten of onverwachte resultaten leiden. Daarom kunt u met de informatie over het eigendom en het transferdoel problemen oplossen die optreden nadat u deze typen wijzigingen hebt aangebracht.

Voer de volgende stappen uit om het eigendom en transferdoel van een record weer te geven.

1. Open de relevante record.
1. Selecteer in het actievenster op het tabblad **Opties** in de groep **Recordinfo** de optie **Alle velden weergeven**.
1. Op de pagina die verschijnt, worden waarden weergegeven voor alle velden die beschikbaar zijn voor de geselecteerde record. Bekijk de volgende velden:

    - **SYSSCALEUNITID**: in dit veld ziet u de huidige eigenaar van de record.
    - **SYSTARGETSCALEUNITID**: dit veld bevat de schaaleenheids-id van de hub of schaaleenheid waaraan de record wordt overgedragen wanneer de huidige eigenaar er klaar mee is. De waarde van dit veld wordt gebruikt door batchtaken waarmee dit type proces wordt beheerd. Hoewel dit veld niet direct is gerelateerd aan eigendom, kan het eigendom veranderen wanneer de record wordt overgedragen. In sommige gevallen is dit veld leeg.
