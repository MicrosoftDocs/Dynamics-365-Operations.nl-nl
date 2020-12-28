---
title: Activum-KPI's
description: In dit onderwerp worden KPI's in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3ebbb1016bafed8ad9fb998fc76152e215c08c3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425343"
---
# <a name="asset-kpis"></a>Activum-KPI's

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u verschillende KPI's (Key Performance Indicators) berekenen voor activa en activatypen. Met KPI's krijgt u een overzicht van de prestaties van activa in relatie tot, bijvoorbeeld, uptime, downtime, reparatietijd en de gemiddelde tijd tussen fouten.

1. Klik op **Activabeheer** > **Query's** > **Activa** > **KPI's voor activa**.

2. Selecteer in het dialoogvenster **KPI's voor activa berekenen** de **tijdschaal** die moet worden gebruikt in de berekening en geef een periode op in de velden **Begindatum** en **Einddatum**. 

3. Op het sneltabblad **Op te nemen records** kunt u specifieke activa en activatypen selecteren die in de berekening moeten worden opgenomen, indien nodig.

4. Klik op **OK** om de berekening te starten.

5. Op het sneltabblad **Overzicht** worden de resultaten van de berekening weergegeven in de rasterweergave. Elk activum wordt op een aparte regel weergegeven.

6. Op het sneltabblad **KPI's voor geselecteerde regel** ziet u berekeningen voor het activum dat is geselecteerd op het sneltabblad **Overzicht**. De KPI-waarden worden gecategoriseerd op basis van **tijd**, **beschikbaarheid**, **werkorders**, **onderhoud**, **fouten**, **uitvaltijd voor onderhoud** en **kosten**.

In de volgende tabel vindt u een omschrijving van de velden op de pagina **KPI's voor activa**.

| Veld                   | Beschrijving                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Activum                   | Activum-id.                                                                                                                                                                                                                                                                                             |
| Totale tijd              | De totale tijd die is ingesteld in de kalender die wordt gebruikt in de berekening. Als het activum aan een resource is gekoppeld, wordt de gekoppelde resourcekalender gebruikt. Als het activum niet aan een resource is gekoppeld, wordt de kalender gebruikt die is geselecteerd in het veld **Standaardkalender** in **Parameters voor activabeheer**. |
| Bedrijfstijd                  | Totale tijd min uitvaltijd.                                                                                                                                                                                                                                                                            |
| Uitvaltijd                | Registraties van downtime van onderhoud voor het activum in de geselecteerde periode.                                                                                                                                                                                                                              |
| Reparatietijd             | Het totale aantal werkuren dat is verbruikt voor reparatiewerkorders.                                                                                                                                                                                                                                            |
| Beschikbaarheid %          | De uptime gedeeld door de totale tijd en vermenigvuldigd met 100.                                                                                                                                                                                                                                                   |
| Aantal fouten        | Het aantal geregistreerde foutoorzaken voor foutsymptomen voor het activum in de geselecteerde periode.                                                                                                                                                                                                             |
| Gemiddelde tijd tussen fouten                    | De totale tijd gedeeld door het aantal fouten dat is geregistreerd voor het activum in de geselecteerde periode. Als het aantal fouten nul is, wordt de gemiddelde tijd tussen fouten ingesteld op de totale tijd.                                                                                                                   |
| Storingspercentage               | 1 gedeeld door de gemiddelde tijd tussen fouten.                                                                                                                                                                                                                                                                                    |
| Gemiddelde reparatietijd                     | De reparatietijd gedeeld door het aantal fouten dat is geregistreerd voor het activum in de geselecteerde periode. Als het aantal fouten nul is, wordt de gemiddelde reparatietijd ingesteld op de reparatietijd.                                                                                                                           |
| Aantal onderbrekingen         | Het aantal gemaakte registraties van uitvaltijd voor onderhoud voor het activum.                                                                                                                                                                                                                                     |
| Gemiddelde tijd tussen onderbrekingen                    | De totale tijd gedeeld door het aantal registraties van uitvaltijd voor onderhoud. Als het aantal registraties van uitvaltijd voor onderhoud nul is in de geselecteerde periode, wordt de totale tijd ingesteld als waarde voor de gemiddelde tijd tussen onderbrekingen.                                                                                      |
| Preventieve kosten         | Kosten die voor het activum zijn geboekt met betrekking tot het kostentype Preventief in de geselecteerde periode. Er worden kostentypen ingesteld voor werkordertypen.                                                                                                                                                                       |
| Correctiekosten         | Kosten die voor het activum zijn geboekt met betrekking tot het kostentype Corrigerend in de geselecteerde periode. Er worden kostentypen ingesteld voor werkordertypen.                                                                                                                                                                       |
| Vervangingswaarde       | De waarde die voor het activum is gedefinieerd als vervangingskosten.                                                                                                                                                                                                                                                  |
| Activumtype             | Identificatie van het geselecteerde activatype voor het activum.                                                                                                                                                                                                                                             |
| Fabrikant           | Identificatie van de geselecteerde fabrikant voor het activum.                                                                                                                                                                                                                                                 |
| Model                   | Identificatie van de geselecteerde fabrikantmodel voor het activum.                                                                                                                                                                                                                                           |
| Begindatum               | Begindatum van de KPI-berekening. Als het activum is gemaakt na de geselecteerde begindatum voor de berekening, wordt de begindatum van het activum weergegeven in dit veld.                                                                                                                                  |
| Einddatum                 | Einddatum van de KPI-berekening. Als het activum als inactief is geregistreerd vóór de geselecteerde einddatum voor de berekening, wordt in dit veld de datum weergegeven waarop het activum niet langer actief is.                                                                                               |
| Tijdschaal              | Tijdens het berekenen van de KPI's selecteert u de gewenste tijdschaal: Uren, Dagen of Weken.                                                                                                                                                                                                            |
| Beschikbaarheid            | De uptime gedeeld door de totale tijd.                                                                                                                                                                                                                                                                         |
| Werkorders             | Het totale aantal werkorders in de KPI-berekening.                                                                                                                                                                                                                                          |
| Werkordertijd         | Het totale aantal werkuren dat is verbruikt voor de werkorders.                                                                                                                                                                                                                                               |
| Primaire werkorders     | Het aantal primaire werkorders in de KPI-berekening.                                                                                                                                                                                                                                        |
| Secundaire werkorders   | Het aantal secundaire werkorders in de KPI-berekening.                                                                                                                                                                                                                                      |
| Onderhoudswerkorders | Het aantal onderhoudswerkorders in de KPI-berekening. Een onderhoudswerkorder is een werkorder zonder gerelateerde foutoorzaken.                                                                                                                                                             |
| Onderhoudstijd        | Het totale aantal werkuren dat is verbruikt voor onderhoudswerkorders.                                                                                                                                                                                                                                       |
| Reparatiewerkorders      | Het aantal reparatiewerkorders in de KPI-berekening. Een reparatiewerkorder is een werkorder met een gerelateerde foutoorzaak.                                                                                                                                                                        |
| Betrouwbaarheid %           | Berekening op basis van de verwachte exponentiële ontwikkeling in foutregistraties voor een activum, wat betekent dat het activum na verloop van tijd minder betrouwbaar wordt vanwege slijtage. De berekening van deze KPI is gebaseerd op de gemiddelde tijd tussen fouten en de totale tijd.                                                            |
| Gemiddelde tijd van productieonderbrekingen                    | De uitvaltijd voor onderhoud gedeeld door het aantal registraties van uitvaltijd voor onderhoud. Als het aantal registraties van uitvaltijd voor onderhoud nul is in de geselecteerde periode, wordt de waarde voor de gemiddelde tijd tussen onderbrekingen ingesteld op nul.                                                                               |
| Totale kosten              | De totale kosten die voor het activum zijn geboekt in de geselecteerde periode.                                                                                                                                                                                                                                              |
| Investeringskosten         | Kosten die voor het activum zijn geboekt met betrekking tot het kostentype Investering in de geselecteerde periode. Er worden kostentypen ingesteld voor werkordertypen.                                                                                                                                                                       |

De volgende afbeelding toont een schermafbeelding van een KPI-berekening voor vier activa.

![Schermopname van een KPI-berekening voor vier activa](media/11-controlling-and-reporting.png)

- U kunt meerdere activa selecteren in **Alle activa** en op de knop **KPI's voor activa** op het tabblad **Algemeen** klikken. Klik vervolgens op **OK** in het dialoogvenster **KPI's voor activa berekenen** om KPI's te berekenen voor de geselecteerde activa.  
- De resultaten van een KPI-berekening kunnen de [registraties van uitvaltijd voor onderhoud](../work-orders/maintenance-downtime.md) omvatten, afhankelijk van de instellingen en het gebruik van redencodes voor uitvaltijd voor onderhoud. 

