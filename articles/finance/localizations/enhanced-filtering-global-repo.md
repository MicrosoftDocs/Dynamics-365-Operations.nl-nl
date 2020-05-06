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
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="76d59-103">Verbeterde RCS-filteropties voor het zoeken van configuraties in de RCS/algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="76d59-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76d59-104">In dit onderwerp worden uitgebreide filtermogelijkheden voor de globale opslagplaats van RCS (Regulatory Configuration Services) beschreven, die zijn uitgebreid met de mogelijkheid om met de volgende criteria te filteren:</span><span class="sxs-lookup"><span data-stu-id="76d59-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="76d59-105">**Land/regio**: gebaseerd op ISO-landcodes</span><span class="sxs-lookup"><span data-stu-id="76d59-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="76d59-106">**Label**typen voor:</span><span class="sxs-lookup"><span data-stu-id="76d59-106">**Tags** types for:</span></span>
  - <span data-ttu-id="76d59-107">Functioneel gebied</span><span class="sxs-lookup"><span data-stu-id="76d59-107">Functional area</span></span>
  - <span data-ttu-id="76d59-108">Functiegebied</span><span class="sxs-lookup"><span data-stu-id="76d59-108">Feature area</span></span>
  - <span data-ttu-id="76d59-109">Bedrijfstak</span><span class="sxs-lookup"><span data-stu-id="76d59-109">Industry</span></span> 
  - <span data-ttu-id="76d59-110">Bedrijfsdocument</span><span class="sxs-lookup"><span data-stu-id="76d59-110">Business document</span></span> 

<span data-ttu-id="76d59-111">U kunt filters toepassen, afzonderlijk of in groepen om gemakkelijk specifieke of verwante configuraties te zoeken.</span><span class="sxs-lookup"><span data-stu-id="76d59-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="76d59-112">Als u bijvoorbeeld wilt zoeken naar een enkel type 'Configureerbare bedrijfsdocumenten' die zijn gerelateerd aan leveranciersfacturen, kunt u een filter voor **een bedrijfsdocumenttype** toepassen om dat type document te zoeken.</span><span class="sxs-lookup"><span data-stu-id="76d59-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="76d59-113">[![Filtersectie voor algemene opslagplaats](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="76d59-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="76d59-114">U kunt de zoekopdracht verder verfijnen door documenttype te selecteren, bijvoorbeeld 'leveranciersfactuur' en te klikken op **Filter toepassen**.</span><span class="sxs-lookup"><span data-stu-id="76d59-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="76d59-115">In het volgende voorbeeld wordt het resultaat weergegeven van het filteren op **Type bedrijfsdocument** met het documenttype toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="76d59-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="76d59-116">[![Toegepast filter en importeren voor type bedrijfsdocument](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="76d59-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="76d59-117">Gefilterde resultaten kunnen in een RCS-opslagplaats van een gebruiker of een Dynamics 365 Finance-omgeving worden geïmporteerd, hetzij afzonderlijk, hetzij als een set.</span><span class="sxs-lookup"><span data-stu-id="76d59-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="76d59-118">Hiertoe selecteert u de groep configuraties en klikt u op **Importeren.**</span><span class="sxs-lookup"><span data-stu-id="76d59-118">To do this, select the group of configurations, and click **Import**.</span></span>
