---
title: Een preview van een experiment weergeven en een experiment publiceren
description: In dit onderwerp wordt beschreven hoe u een preview van een experiment weergeeft en een experiment publiceert in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930173"
---
# <a name="preview-and-publish-an-experiment"></a>Een preview van een experiment weergeven en een experiment publiceren

In dit onderwerp wordt beschreven hoe u een preview van uw experiment kunt weergeven en uw experiment kunt publiceren in Dynamics 365 Commerce nadat u [uw experiment hebt verbonden en uw variaties hebt bewerkt](experimentation-connect-edit.md). In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke onderwerpen behandeld.

[ ![Traject van gebruiker voor experimenten - preview weergeven en publiceren](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Een preview van uw experimentvariaties weergeven
U kunt een preview van uw variaties weergeven en ze verder bewerken totdat ze er naar wens uitzien.

1. Gebruik in Site Builder het vervolgkeuzemenu voor variaties onder de opdrachtbalk om de inhoud te selecteren die u wilt bekijken. 
1. Selecteer **Preview** op de bovenste balk. Er wordt een preview weergegeven van hoe de inhoud eruit ziet wanneer deze wordt gepubliceerd.
1. Als u een preview van een andere variatie wilt weergeven, selecteert u deze in het vervolgkeuzemenu voor variaties en selecteert u opnieuw **Preview**.

## <a name="publish-your-experiment"></a>Uw experiment publiceren
Als u geen publicatiegroep gebruikt om te plannen wanneer het experiment live gaat en u onmiddellijk wilt publiceren, selecteert u **Publiceren** op de opdrachtbalk. Alle variaties die bij het experiment horen, worden gepubliceerd.
    
> [!IMPORTANT]
> Als de pagina een niet-gepubliceerde URL heeft, moet u de URL eerst publiceren. Anders is deze niet zichtbaar voor de gebruikers van uw website. Zie [Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md) voor meer informatie.
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Publicatiegroepen gebruiken om te plannen wanneer uw experiment live gaat
Variaties die in Site Builder zijn gemaakt, kunnen worden gepland voor publicatie met behulp van een publicatiegroep. Binnen een publicatiegroep kunt u een pagina of een fragment verbinden met uw experiment door naar het tabblad **Experimenten** of het tabblad **Pagina´s** of **Fragmenten** te gaan. Zie het onderwerp [Een experiment verbinden en variaties bewerken](experimentation-connect-edit.md) voor meer informatie. Zie [Werken met publicatiegroepen](publish-groups.md) voor informatie over publicatiegroepen.

Wanneer u publicatiegroepen gebruikt bij experimenten, moet u rekening houden met een aantal belangrijke aandachtspunten.
- Wanneer u een pagina of fragment toevoegt waarop een experiment wordt uitgevoerd naar een publicatiegroep, wordt het experiment verwijderd uit de pagina of het fragment in de publicatiegroep.
- Experimenten die zijn verbonden met pagina's op een live site, zijn niet beschikbaar voor pagina's binnen publicatiegroepen en andersom. Op dezelfde manier zijn pagina's waarop experimenten zijn uitgevoerd op een live site niet beschikbaar voor andere experimenten in publicatiegroepen en andersom.
- Wanneer u een publicatiegroep publiceert of plant, wordt alle inhoud in de publicatiegroep gepubliceerd, ongeacht of er een experiment aan de publicatiegroep is gekoppeld.
- Omdat een publicatiegroep blijft behouden nadat deze naar een live site is gepubliceerd, blijven experimenten in de publicatiegroep ook behouden. Daarom kunt u geen andere experimenten koppelen aan dezelfde pagina of hetzelfde fragment. Om deze beperking te voorkomen moet u alle publicatiegroepen met persistente experimenten verwijderen. Zo geldt ook dat als u een experiment op een live site wilt verwijderen dat ook in een publicatiegroep bestaat, u het eerst moet verwijderen uit de publicatiegroep.

## <a name="previous-step"></a>Vorige stap
[Een experiment verbinden en bewerken](experimentation-connect-edit.md)

## <a name="next-step"></a>Volgende stap
[Een experiment uitvoeren en controleren](experimentation-run-monitor.md)
