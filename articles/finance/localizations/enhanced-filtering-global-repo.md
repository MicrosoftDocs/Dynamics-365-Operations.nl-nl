---
title: Verbeterde filters in de RCS/algemene opslagplaats
description: In dit artikel worden uitgebreide filtermogelijkheden voor de globale opslagplaats van RCS beschreven, die zijn verbeterd en die extra filters bevatten.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274507"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Verbeterde RCS-filteropties voor het zoeken van configuraties in de RCS/algemene opslagplaats

[!include [banner](../includes/banner.md)]

In dit artikel worden uitgebreide filtermogelijkheden voor de globale opslagplaats van RCS (Regulatory Configuration Services) beschreven, die zijn uitgebreid met de mogelijkheid om met de volgende criteria te filteren: 
- **Land/regio**: gebaseerd op ISO-landcodes  
- **Label** typen voor:
  - Functioneel gebied
  - Functiegebied
  - Bedrijfstak 
  - Bedrijfsdocument 

U kunt filters toepassen, afzonderlijk of in groepen om gemakkelijk specifieke of verwante configuraties te zoeken. Als u bijvoorbeeld wilt zoeken naar een enkel type 'Configureerbare bedrijfsdocumenten' die zijn gerelateerd aan leveranciersfacturen, kunt u een filter voor **een bedrijfsdocumenttype** toepassen om dat type document te zoeken. 

[![Filtersectie voor algemene opslagplaats.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

U kunt de zoekopdracht verder verfijnen door documenttype te selecteren, bijvoorbeeld 'leveranciersfactuur' en te klikken op **Filter toepassen**. In het volgende voorbeeld wordt het resultaat weergegeven van het filteren op **Type bedrijfsdocument** met het documenttype toegevoegd. 

[![Toegepast filter en importeren voor type bedrijfsdocument.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Gefilterde resultaten kunnen in een RCS-opslagplaats van een gebruiker of een Dynamics 365 Finance-omgeving worden geïmporteerd, hetzij afzonderlijk, hetzij als een set. Hiertoe selecteert u de groep configuraties en klikt u op **Importeren.**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
