---
title: Een hypothese opstellen en metrische gegevens bepalen voor een experiment
description: In dit onderwerp wordt beschreven hoe u de hypothese en metrische gegevens voor succes kunt identificeren voor een experiment dat u uitvoert op een e-Commerce-website in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91614cda804cae4574fce4c9cfb31c63d876f19b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238625"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Een hypothese opstellen en metrische gegevens voor succes bepalen voor een experiment
De eerste fase in de levenscyclus van het experiment omvat de identificatie van de hypothese voor het experiment en het bepalen van de metrische gegevens die u zult volgen om succes te beoordelen. In het volgende diagram ziet u alle stappen voor het [instellen en uitvoeren van een experiment](experimentation-overview.md) op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke onderwerpen behandeld. 

[ ![Traject van gebruiker voor experimenten - identificeren](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Een hypothese is een verklaring waarin u het resultaat van het experiment voorspelt. Veel factoren zijn aan de orde bij het definiëren van een hypothese, bijvoorbeeld bij onderzoek naar gebruikersgedrag en websitegegevens die u hebt verzameld. Met de hypothese definieert u de veronderstelling of theorie die u met uw experiment wilt valideren. Een voorbeeld van een hypothese voor uw experiment is: "*tijdens de zomermaanden zorgt een afbeelding van een wit t-shirt op mijn startpagina voor een hogere doorkliksnelheid dan een blauwe sweater, omdat mensen in de zomer iets met een licht gewicht en lichte kleur willen dragen.*" In dat geval maakt u variaties die een wit t-shirt en een blauwe sweater bevatten en publiceert u beide tegelijkertijd.

Om een hypothese te valideren moet het slagen of mislukken van een experiment rechtstreeks aan de acties van gebruikers zijn gekoppeld. Bijvoorbeeld als de gebruiker van de website op een koppeling of knop klikt. Deze acties moeten overeenkomen met gebeurtenissen die worden gerapporteerd aan de service van derden waarmee het experiment wordt gevolgd. Na verloop van tijd wordt het percentage gebruikers dat de actie uitvoert, geregistreerd als een metrisch gegeven dat u kunt gebruiken om rapporten te genereren en analyses uit te voeren. Raadpleeg het onderwerp [Commerce-onderdeelgebeurtenissen voor diagnose en probleemoplossing](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) als u alle beschikbare gebeurtenissen en kenmerken wilt controleren.

## <a name="previous-step"></a>Vorige stap
[Experimenten in Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Volgende stap
[Een experiment opzetten](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]