---
title: De stuklijstversie bepalen
description: Als voor een artikel tijdens een vraagexplosie een standaardordertype is ingesteld op Productie, wordt een geldige stuklijstversie gezocht op basis van de locatie.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833612"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="be430-103">De stuklijstversie bepalen</span><span class="sxs-lookup"><span data-stu-id="be430-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be430-104">Als voor een artikel tijdens een vraagexplosie een standaardordertype is ingesteld op Productie, wordt een geldige stuklijstversie gezocht op basis van de locatie.</span><span class="sxs-lookup"><span data-stu-id="be430-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="be430-105">De locatiedimensie is altijd bekend en wordt vermeld op de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="be430-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="be430-106">Het bepalen van de te gebruiken stuklijstversie gaat als volgt in zijn werk:</span><span class="sxs-lookup"><span data-stu-id="be430-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="be430-107">Als voor het artikel een stuklijstversie is gedefinieerd op de vraaglocatie, wordt deze locatiespecifieke stuklijst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="be430-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="be430-108">Als voor een artikel op de vraaglocatie geen locatiespecifieke stuklijstversie is gedefinieerd, wordt een algemene stuklijst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="be430-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="be430-109">Op een algemene stuklijst wordt geen locatie vermeld, want deze is geldig voor meerdere locaties.</span><span class="sxs-lookup"><span data-stu-id="be430-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="be430-110">Als er een algemene stuklijst bestaat, wordt deze gebruikt.</span><span class="sxs-lookup"><span data-stu-id="be430-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="be430-111">Als er geen algemene stuklijstversie bestaat, wordt de vraagexplosie op dit moment gestopt.</span><span class="sxs-lookup"><span data-stu-id="be430-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="be430-112">Een geldige stuklijstversie, of deze nu locatiespecifiek of algemeen is, moet voldoen aan de vereiste criteria voor datum en hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="be430-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]