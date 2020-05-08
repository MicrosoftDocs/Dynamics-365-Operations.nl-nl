---
title: Verbeterde filters in de RCS/algemene opslagplaats
description: In dit onderwerp worden uitgebreide filtermogelijkheden voor de globale opslagplaats van RCS beschreven, die zijn verbeterd en die extra filters bevatten.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287934"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Verbeterde RCS-filteropties voor het zoeken van configuraties in de RCS/algemene opslagplaats

[!include [banner](../includes/banner.md)]

In dit onderwerp worden uitgebreide filtermogelijkheden voor de globale opslagplaats van RCS (Regulatory Configuration Services) beschreven, die zijn uitgebreid met de mogelijkheid om met de volgende criteria te filteren: 
- **Land/regio**: gebaseerd op ISO-landcodes  
- **Label**typen voor:
  - Functioneel gebied
  - Functiegebied
  - Bedrijfstak 
  - Bedrijfsdocument 

U kunt filters toepassen, afzonderlijk of in groepen om gemakkelijk specifieke of verwante configuraties te zoeken. Als u bijvoorbeeld wilt zoeken naar een enkel type 'Configureerbare bedrijfsdocumenten' die zijn gerelateerd aan leveranciersfacturen, kunt u een filter voor **een bedrijfsdocumenttype** toepassen om dat type document te zoeken. 

[![Filtersectie voor algemene opslagplaats](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

U kunt de zoekopdracht verder verfijnen door documenttype te selecteren, bijvoorbeeld 'leveranciersfactuur' en te klikken op **Filter toepassen**. In het volgende voorbeeld wordt het resultaat weergegeven van het filteren op **Type bedrijfsdocument** met het documenttype toegevoegd. 

[![Toegepast filter en importeren voor type bedrijfsdocument](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Gefilterde resultaten kunnen in een RCS-opslagplaats van een gebruiker of een Dynamics 365 Finance-omgeving worden geïmporteerd, hetzij afzonderlijk, hetzij als een set. Hiertoe selecteert u de groep configuraties en klikt u op **Importeren.**
