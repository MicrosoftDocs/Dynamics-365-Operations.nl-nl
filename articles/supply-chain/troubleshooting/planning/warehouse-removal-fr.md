---
title: U kunt de dimensie voor magazijnvraagprognose niet verwijderen uit prognoseregels
description: U kunt de dimensie voor magazijnvraagprognose niet verwijderen uit prognoseregels.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026408"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="dde16-103">U kunt de dimensie voor magazijnvraagprognose niet verwijderen uit prognoseregels</span><span class="sxs-lookup"><span data-stu-id="dde16-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="dde16-104">KB-nummer: 4614408</span><span class="sxs-lookup"><span data-stu-id="dde16-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="dde16-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="dde16-105">Symptoms</span></span>

<span data-ttu-id="dde16-106">Dit probleem treedt op wanneer de dimensie **Magazijn** niet is toegewezen op het tabblad **Prognosedimensies** van de pagina **Vraagprognoseparameter**.</span><span class="sxs-lookup"><span data-stu-id="dde16-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="dde16-107">De kolom **Magazijn** wordt echter weergegeven op de pagina **Vraagprognose** (**Hoofdplanning \> Prognose \> Handmatige prognose-entiteit \> Vraagprognoseregels**).</span><span class="sxs-lookup"><span data-stu-id="dde16-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="dde16-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="dde16-108">Resolution</span></span>

<span data-ttu-id="dde16-109">De instellingen op het tabblad **Prognosedimenssie** van de pagina **Vraagprognoseparameter** hebben geen invloed op de pagina **Vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="dde16-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="dde16-110">Ze bepalen de basislijnprognose die wordt gegenereerd en weergegeven in de gecorrigeerde vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="dde16-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="dde16-111">Ze hebben echter geen controle over de dimensies die vereist zijn voor de 'echte' vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="dde16-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="dde16-112">Door de records toe te staan die worden weergegeven op de pagina **Gecorrigeerde vraagprognose**, kunt u ze converteren naar 'echte' prognosegegevens voor een prognosemodel.</span><span class="sxs-lookup"><span data-stu-id="dde16-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="dde16-113">Dat model kan vervolgens worden gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="dde16-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="dde16-114">Op de pagina **Vraagprognose** maken de dimensies voor de 'echte' prognose die wordt weergegeven op de vraagprognoseregels deel uit van de voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="dde16-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="dde16-115">(Dit gedrag lijkt op het gedrag van verkooporderregels.) Als uw systeem niet is ingesteld om **Magazijn** te gebruiken als verplichte voorraaddimensie, kunt u de pagina aanpassen om de kolom te verbergen.</span><span class="sxs-lookup"><span data-stu-id="dde16-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
