---
title: Intercompany-onkosten
description: Een werknemer die werkzaam is bij één rechtspersoon in een organisatie, voert mogelijk werk uit voor een andere rechtspersoon in dezelfde organisatie. In deze situatie kunt u de functie IC-kosten gebruiken om de onkosten van voor de werknemer toe te wijzen aan de rechtspersoon voor wie het werk is uitgevoerd.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390879"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="8d811-104">Intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="8d811-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d811-105">Een werknemer die werkzaam is bij één rechtspersoon in een organisatie, voert mogelijk werk uit voor een andere rechtspersoon in dezelfde organisatie.</span><span class="sxs-lookup"><span data-stu-id="8d811-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="8d811-106">In deze situatie kunt u de functie IC-kosten gebruiken om de onkosten van voor de werknemer toe te wijzen aan de rechtspersoon voor wie het werk is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8d811-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="8d811-107">De rechtspersoon waarbij de werknemer in dienst is, wordt de uitlenende rechtspersoon genoemd.</span><span class="sxs-lookup"><span data-stu-id="8d811-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="8d811-108">De juridische entiteit waarvan de werknemer onkosten maakt, heet de ontlenende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="8d811-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="8d811-109">Voordat een werknemer onkosten kan maken en indienen voor werk dat is uitgevoerd voor een andere rechtspersoon, selecteert u voor de uitlenende rechtspersoon op de pagina **Parameters onkostenbeheer** de optie **Intercompany-onkostenregels toestaan**.</span><span class="sxs-lookup"><span data-stu-id="8d811-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="8d811-110">Boeking van btw voor intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="8d811-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d811-111">Als u btw-groepen wilt gebruiken die zijn gekoppeld aan de uitlenende rechtspersoon (bron) in plaats van de lenende rechtspersoon (bestemming) in uw onkostendeclaratie, moet u deze configureren in de btw-instellingen voor het grootboek.</span><span class="sxs-lookup"><span data-stu-id="8d811-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="8d811-112">Wanneer de grootboekparameter **Rechtspersoon voor intercompany-btw-boekingen** is ingesteld op **Bron** en **Belastingregels btw toepassen** is ingesteld op **Nee**, wordt de btw-combinatie voor de uitlenende rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8d811-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="8d811-113">Wanneer dezelfde parameter wordt ingesteld op **Bestemming**, wordt de btw-combinatie voor de lenende rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8d811-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="8d811-114">Voor rechtspersonen in de Verenigde Staten geldt dat als de parameter is ingesteld op **Bron**, het veld **Te ontvangen btw** ook worden geconfigureerd op de nieuwe pagina **Grootboekboekingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="8d811-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="8d811-115">De boekhoudingsengine gebruikt de informatie uit dit veld voor belastinggerelateerde journaalregels.</span><span class="sxs-lookup"><span data-stu-id="8d811-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="8d811-116">Het gedrag is consistent voor onkostenregels die zijn geboekt met of zonder een project.</span><span class="sxs-lookup"><span data-stu-id="8d811-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
