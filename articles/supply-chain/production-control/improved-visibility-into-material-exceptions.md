---
title: Inzicht in materiaaluitzonderingen
description: In dit onderwerp wordt beschreven hoe u meer inzicht in uitzonderingen voor grondstoffen voor productieorders en batchorders kunt krijgen.
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 18c8b5d1d3e83259cf5dafd08bfc779161a4c916
ms.contentlocale: nl-nl
ms.lasthandoff: 12/14/2017

---
# <a name="visibility-into-material-exceptions"></a>Inzicht in materiaaluitzonderingen

[!include[banner](../includes/banner.md)]

In het werkgebied **Productievloerbeheer** bieden drie tegels u meer inzicht in uitzonderingen voor grondstoffen voor productieorders en batchorders:

- Niet-vrijgegeven materiaalregels die aandacht vereisen
- Niet-verwerkte waves die aandacht vereisen
- Openstaand magazijnwerk dat aandacht vereist

Voor alle drie de tegels wordt de grondstoffendatum van de stuklijst- en formuleregels vergeleken met de werkgebieddatum en de filters voor **Productie-eenheid**, **Resourcegroep** en **Resource** die zijn ingesteld in het menu **Mijn werkgebied configureren**. Standaard is de werkgebieddatum ingesteld op de huidige datum, maar u kunt deze wijzigen.

Een niet-vrijgegeven stuklijst- of formuleregel vereist aandacht als de grondstofdatum van de regel op of voor de werkgebieddatum valt en voldoet aan de criteria die zijn gedefinieerd op basis van de filters in het werkgebied.

In de volgende afbeelding staat de blauwe balk voor een productietaak die voor een resource is gepland. De taak is gepland om te beginnen op 1 mei 2017. Dit is de grondstofdatum. Met andere woorden, de materialen die zijn toegewezen aan de taak op de stuklijst- en formuleregels moeten gereed zijn op deze datum. De andere datum in de afbeelding, 6 mei 2017, staat voor de werkgebieddatum. In dit voorbeeld valt de grondstofdatum vóór de werkgebieddatum. De datum waarop het verbruik van grondstoffen had moeten beginnen, is dus verstreken en de stuklijst- en formuleregels voldoen aan de criteria voor het vereisen van aandacht.

![Voorbeeld van een productietaak waarbij de grondstofdatum vóór de werkgebieddatum valt](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Niet-vrijgegeven materiaalregels die aandacht vereisen

Een stuklijst- of formuleregel kan op drie manieren worden vrijgegeven aan het magazijn:

- Als onderdeel van de vrijgave van een productieorder of batchorder
- Als handmatige vrijgave
- Automatisch via een batchtaak

Zie voor meer informatie [Stuklijst- en formuleregels vrijgeven aan het magazijn](releasing-bom-and-formula-lines-to-warehouse.md). 

Als een stuklijst- of formuleregel niet of slechts gedeeltelijk is vrijgegeven en aan de datum- en filtercriteria voor het werkgebied wordt voldaan, wordt de regel opgenomen in de berekening van de waarde die wordt weergegeven op de tegel **Niet-vrijgegeven materiaalregels die aandacht vereisen**.

Wanneer u de tegel selecteert, wordt de pagina **Vrijgave naar magazijn** geopend. Op deze pagina wordt het aantal niet-vrijgegeven stuklijst- en formuleregels weergegeven, dat wordt aangegeven op de tegel. De niet-vrijgegeven regels worden weergegeven in het bovenste raster. In dit raster wordt de hoeveelheid weergegeven die oorspronkelijk was geraamd voor de regel, de hoeveelheid die al is vrijgegeven en de resterende hoeveelheid die nog moet worden vrijgegeven. U kunt regels uit het bovenste raster toevoegen aan het onderste raster. Vanuit het onderste raster kunt u de geselecteerde regels vrijgeven aan het magazijn. Vanuit het onderste raster kunt u ook de hoeveelheid aanpassen die moet worden vrijgegeven, zodat slechts een gedeeltelijke hoeveelheid wordt vrijgegeven.

## <a name="unprocessed-waves-needing-attention"></a>Niet-verwerkte waves die aandacht vereisen

Wanneer een stuklijst- of formuleregel wordt vrijgegeven, wordt deze toegevoegd aan een nieuwe productiewave of een bestaande open wave, afhankelijk van de configuratie van de sjabloon voor de productiewave. Door middel van de configuratie van de wavesjabloon kunt u een wave ook zo instellen dat deze automatisch wordt verwerkt wanneer een stuklijst- of formuleregel wordt vrijgegeven. Wanneer de wave wordt verwerkt, wordt magazijnwerk voor het verzamelen van grondstoffen gegenereerd. Als de wavesjabloon zo is geconfigureerd dat golven ten tijde van de release niet worden verwerkt, behoudt de wave een niet-verwerkte status. Op de tegel **Niet-verwerkte waves die aandacht vereisen** wordt aangegeven hoeveel stuklijst- en formuleregels met een grondstofdatum gelijk aan of vóór de werkgebieddatum in niet-verwerkte waves zijn vrijgegeven aan het magazijn. De regels moeten ook worden gebruikt door een bewerkingsresource die voldoet aan het filter van het werkgebied.

Wanneer de tegel wordt geselecteerd, wordt de pagina **Alle productie-waves** geopend. Deze pagina wordt gefilterd op het aantal open waves dat waveregels bevat uit vrijgegeven stuklijst- en formuleregels die voldoen aan de criteria voor de tegel. Via de pagina **Alle productie-waves** kunt u de wave handmatig verwerken.

## <a name="open-warehouse-work-needing-attention"></a>Openstaand magazijnwerk dat aandacht vereist

Op de tegel **Openstaand magazijnwerk dat aandacht vereist** wordt aangegeven hoeveel stuklijst- en formuleregels met een grondstofdatum gelijk aan of vóór de werkgebieddatum en niet-verwerkt werk zijn vrijgegeven aan het magazijn. De regels moeten ook worden gebruikt door een bewerkingsresource die voldoet aan het filter van het werkgebied.

Wanneer de tegel wordt geselecteerd, wordt de pagina **Alle werk** geopend. Deze pagina wordt gefilterd op het aantal open werkkopteksten dat werkregels bevat uit vrijgegeven stuklijst- en formuleregels die voldoen aan de criteria voor de tegel. Via de pagina **Alle werk** kunt u het werk handmatig verwerken.

