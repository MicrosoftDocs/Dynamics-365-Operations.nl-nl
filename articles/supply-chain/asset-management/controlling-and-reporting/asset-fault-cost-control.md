---
title: Kostenbeheer activafout
description: In dit onderwerp wordt kostencontrole voor activafouten in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918298"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="de2db-103">Kostenbeheer activafout</span><span class="sxs-lookup"><span data-stu-id="de2db-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="de2db-104">In Activabeheer kunt u kosten voor activafoutregistraties berekenen om een overzicht te krijgen van de werkelijke kosten ten opzichte van budgetkosten voor fouten.</span><span class="sxs-lookup"><span data-stu-id="de2db-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs on faults.</span></span> <span data-ttu-id="de2db-105">Werkelijke kosten worden gebaseerd op geboekte transacties.</span><span class="sxs-lookup"><span data-stu-id="de2db-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="de2db-106">De datum is de foutdatum waarop het symptoom is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="de2db-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="de2db-107">Klik op **Activabeheer** > **Query's** > **Activafout** > **Kostencontrole activafout**.</span><span class="sxs-lookup"><span data-stu-id="de2db-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="de2db-108">Selecteer in het dialoogvenster **Kostencontrole activafout** een financiële-dimensieset die u wilt opnemen in de berekening, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="de2db-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="de2db-109">Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul kosten.</span><span class="sxs-lookup"><span data-stu-id="de2db-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="de2db-110">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor kostencontrole moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="de2db-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="de2db-111">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle kostencontroleregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="de2db-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="de2db-112">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor kostencontrole voor activafouten weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="de2db-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="de2db-113">Als u de zoekopdracht wilt beperken, kunt u specifieke activa, foutdatums en foutoorzaken selecteren op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="de2db-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="de2db-114">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="de2db-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="de2db-115">Klik in de actievenstergroepen **Groeperen op** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="de2db-115">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="de2db-116">De geselecteerde knoppen in het actievenster zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="de2db-116">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="de2db-117">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="de2db-117">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="de2db-118">In de volgende afbeelding ziet u een voorbeeld van de berekening van de kostencontrole voor activafouten.</span><span class="sxs-lookup"><span data-stu-id="de2db-118">The figure below shows an example of an asset fault cost control calculation.</span></span>

![Figuur 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="de2db-120">Raadpleeg de sectie [Foutbeheer](../setup-for-work-orders/fault-management.md) voor informatie over het instellen van fouten.</span><span class="sxs-lookup"><span data-stu-id="de2db-120">Refer to the [Fault management](../setup-for-work-orders/fault-management.md) section for information on how to set up faults.</span></span>

>[!NOTE]
><span data-ttu-id="de2db-121">In het veld **Oorspronkelijk budget** worden budgetkosten uit de werkorderprognose weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de2db-121">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="de2db-122">In het veld **Werkelijke kosten** worden geboekte kosten voor werkorders weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de2db-122">The **Actual cost** field shows posted costs on work orders.</span></span> <span data-ttu-id="de2db-123">In het veld **Toegezegde kosten** wordt het totale aantal kosten weergegeven dat uw bedrijf heeft toegezegd met betrekking tot werkorders.</span><span class="sxs-lookup"><span data-stu-id="de2db-123">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

