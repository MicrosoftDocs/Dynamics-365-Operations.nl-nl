---
title: Productieorders als voltooid melden
description: Gereedmelden is een productiefase. In deze fase wordt een eindproduct gemeld en van de productieorder verplaatst naar de voorraad.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fa40733e3f1310869ead8b0ac774bb621637e250
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="ec908-104">Productieorders als voltooid melden</span><span class="sxs-lookup"><span data-stu-id="ec908-104">Report production orders as finished</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ec908-105">Gereedmelden is een productiefase.</span><span class="sxs-lookup"><span data-stu-id="ec908-105">Report as finished is a production stage.</span></span> <span data-ttu-id="ec908-106">In deze fase wordt een eindproduct gemeld en van de productieorder verplaatst naar de voorraad.</span><span class="sxs-lookup"><span data-stu-id="ec908-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="ec908-107">Wanneer een hoeveelheid van de eindproducten wordt gereedgemeld op een productieorder, wordt dit in de voorraad bijgewerkt als voorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec908-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="ec908-108">Gedeeltelijke hoeveelheden van de oorspronkelijk geplande orderhoeveelheid kunnen worden gereedgemeld.</span><span class="sxs-lookup"><span data-stu-id="ec908-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="ec908-109">Het is ook mogelijk om fouthoeveelheden met een bijbehorende foutreden te rapporteren bij het gereedmelden van hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="ec908-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="ec908-110">Wanneer de productieorder de fase Gereedgemeld bereikt, geeft deze aan dat er geen hoeveelheid meer zal worden gerapporteerd op de productieorder.</span><span class="sxs-lookup"><span data-stu-id="ec908-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="ec908-111">De volgende kenmerken worden ook gekoppeld aan het proces **Gereedmelden**:</span><span class="sxs-lookup"><span data-stu-id="ec908-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="ec908-112">Het is mogelijk om verbruik van grondstoffen en tijd in te stellen die in verhouding zijn met de gerapporteerde hoeveelheid (wisprincipe)</span><span class="sxs-lookup"><span data-stu-id="ec908-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="ec908-113">Weggezet werk kan worden gegenereerd voor artikelen die voor magazijnprocessen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ec908-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="ec908-114">U kunt instellen dat de geplande of standaard kostprijs van de afgewerkte goederen moet worden gerapporteerd op grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="ec908-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="ec908-115">U kunt een kwaliteitsorder maken voor de gerapporteerde hoeveelheid op basis van de instellingen van een kwaliteitskoppeling.</span><span class="sxs-lookup"><span data-stu-id="ec908-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="ec908-116">De hoeveelheid wordt gerapporteerd aan de uitvoerlocatie.</span><span class="sxs-lookup"><span data-stu-id="ec908-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="ec908-117">Magazijnwerk wordt dan gegenereerd om de hoeveelheid van de uitvoerlocatie te verplaatsen naar de definitieve bestemming die is gedefinieerd door de locatierichtlijn voor het weggezette werk.</span><span class="sxs-lookup"><span data-stu-id="ec908-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="ec908-118">U kunt een kwaliteitsorder maken wanneer een productieorder wordt gereedgemeld als een kwaliteitskoppeling is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ec908-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="ec908-119">Een productieorder instellen op Gereedgemeld</span><span class="sxs-lookup"><span data-stu-id="ec908-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="ec908-120">U kunt een productieorder instellen op **Gereedgemeld** via de standaardfunctie voor het bijwerken van productieorders of via de route- en taakkaartjournalen of via het journaal **Gereedmelden**.</span><span class="sxs-lookup"><span data-stu-id="ec908-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="ec908-121">U kunt de fase ook bijwerken naar **Gereedgemeld** via de pagina's Taakkaartterminal en Apparaat voor taakkaarten, wanneer u over de laatste taak van de productieorder rapporteert.</span><span class="sxs-lookup"><span data-stu-id="ec908-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="ec908-122">Tenslotte kunt u de optie **Gereedmelden** inschakelen als een proces voor de oplossing met handbediende magazijnapparaten.</span><span class="sxs-lookup"><span data-stu-id="ec908-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




