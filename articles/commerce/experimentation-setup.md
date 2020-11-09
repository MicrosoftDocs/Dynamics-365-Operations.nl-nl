---
title: Een experiment instellen
description: In dit onderwerp wordt beschreven hoe u een experiment in een service van derden instelt.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097042"
---
# <a name="set-up-an-experiment"></a>Een experiment instellen

Nadat u [een hypothese hebt gedefinieerd en hebt bepaald welke metrische gegevens voor succes u wilt gebruiken](experimentation-identify.md), moet u uw experiment instellen in de service van derden. In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke onderwerpen behandeld.

[ ![Traject van gebruiker voor experimenten - instellen](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Uw experiment in de service van derden instellen
U moet een service van derden hebben gekozen om uw experiment uit te voeren en te controleren en om de experimentconnector in te stellen. Deze voorwaarden worden vermeld in [Experimenten in Dynamics 365 Commerce](experimentation-overview.md).

Voer de stappen uit die nodig zijn om uw experiment te maken in de service van derden. Als de connector juist is geconfigureerd, wordt de volledige lijst met experimenten die u in de service van derden hebt ingesteld, binnen ongeveer 5 minuten in Commerce Site Builder weergegeven.

## <a name="set-up-your-success-metrics"></a>Uw metrische gegevens voor succes instellen
Voor elk experiment zijn metrische gegevens nodig om de impact van de variaties te meten en de hypothese te valideren. Voer de volgende stappen uit om de berekening van metrische gegevens in de service van derden via live telemetrie-gebeurtenissen in te schakelen in Dynamics 365 Commerce.

Voer de volgende stappen uit om uw metrische gegevens voor succes in te stellen.

1. Selecteer in Commerce Site Builder **Pagina's** in het linkernavigatievenster en selecteer vervolgens de pagina waarvoor u metrische gegevens wilt verzamelen. 
1. Ga naar de sectie **Bij te houden gebeurtenis-ID´s** in het eigenschappenvenster aan de rechterzijde van de pagina of module die u wilt bijhouden.
1. Selecteer **Weergeven**. Er wordt een lijst weergegeven met alle gebeurtenis-ID's. Kopieer de gebeurtenis die u wilt bijhouden en plak de gebeurtenissleutel op de opgegeven locatie in de service van derden. Als u meer dan één gebeurtenis nodig hebt, kopieert u de sleutels een voor een. 
    - Voor meer informatie over het weergeven van alle beschikbare gebeurtenissen en kenmerken, waaronder paginaweergaven en opbrengstentracering, raadpleegt u [Commerce-onderdeelgebeurtenissen voor diagnose en probleemoplossing](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Voer eventuele andere stappen uit voor het bijhouden van metrische gegevens zoals in de service van derden is vereist.

## <a name="previous-step"></a>Vorige stap
[Een hypothese opstellen en metrische gegevens bepalen voor een experiment](experimentation-identify.md) 


## <a name="next-step"></a>Volgende stap
[Een experiment verbinden en bewerken](experimentation-connect-edit.md)
