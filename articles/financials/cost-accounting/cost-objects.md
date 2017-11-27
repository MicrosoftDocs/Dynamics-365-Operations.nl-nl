---
title: Dimensies van kostenobject
description: Wanneer u kosten analyseert, gebruikt u elementendimensies om te bepalen waarheen de kosten stromen. U gebruikt kostenobjectdimensies om te bepalen waaraan u kosten moet toewijzen. Dit onderwerp biedt informatie over kostenobjectdimensies.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8195b776e5d46485172c9f5550ab4ed6d8623dfc
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="40f19-105">Dimensies van kostenobject</span><span class="sxs-lookup"><span data-stu-id="40f19-105">Cost object dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="40f19-106">Wanneer u kosten analyseert, gebruikt u elementendimensies om te bepalen waarheen de kosten stromen.</span><span class="sxs-lookup"><span data-stu-id="40f19-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="40f19-107">U gebruikt kostenobjectdimensies om te bepalen waaraan u kosten moet toewijzen.</span><span class="sxs-lookup"><span data-stu-id="40f19-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="40f19-108">Dit onderwerp biedt informatie over kostenobjectdimensies.</span><span class="sxs-lookup"><span data-stu-id="40f19-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="40f19-109">Een kostenobject kan elk type object zijn dat u wilt ramen, waaraan u kosten wilt toewijzen of dat u rechtstreeks wilt meten.</span><span class="sxs-lookup"><span data-stu-id="40f19-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="40f19-110">Veel gebruikte kostenobjecten zijn bijvoorbeeld producten, projecten, bronnen, afdelingen, kostenplaatsen en geografische regio's.</span><span class="sxs-lookup"><span data-stu-id="40f19-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="40f19-111">Met kostenobjecten kan het management kosten kwantificeren en ook winstgevendheidsanalyses uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="40f19-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="40f19-112">Kostenobjectdimensies en leden van kostenobjectdimensies</span><span class="sxs-lookup"><span data-stu-id="40f19-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="40f19-113">Kostenobjecten worden ook wel *kostenobjectdimensies* genoemd.</span><span class="sxs-lookup"><span data-stu-id="40f19-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="40f19-114">Nadat u hebt bepaald naar welke entiteit de kostenobjectdimensie moet verwijzen, moet u de afzonderlijke dimensiewaarden opgeven of deze in Kostprijsboekhouding importeren vanuit andere bronsystemen.</span><span class="sxs-lookup"><span data-stu-id="40f19-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="40f19-115">Deze individuele dimensiewaarden staan bekend als *kostenobjectdimensieleden*.</span><span class="sxs-lookup"><span data-stu-id="40f19-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="40f19-116">Stel dat u de financiële dimensie met de naam Kostenplaats gebruiken als de kostenobjectdimensie.</span><span class="sxs-lookup"><span data-stu-id="40f19-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="40f19-117">Om te zien hoe kosten naar de individuele kostenplaatsen doorstromen, moet u de leden van de kostenobjectdimensie importeren.</span><span class="sxs-lookup"><span data-stu-id="40f19-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="40f19-118">In dit geval zijn de leden van de kostenobjectdimensie de daadwerkelijke kostenplaatsen, zoals Verkoop, Productie, Administratie en Geografische locaties.</span><span class="sxs-lookup"><span data-stu-id="40f19-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="40f19-119">In de onderstaande schermopname ziet u een voorbeeld van Kostenplaatsen als de kostenobjectdimensie met de werkelijke kostenplaatsen als kostenobjectdimensieleden.</span><span class="sxs-lookup"><span data-stu-id="40f19-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="40f19-120">[![dimensies-kostenobject](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="40f19-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="40f19-121">Kostenobjectdimensieleden importeren door middel van gegevensconnectors</span><span class="sxs-lookup"><span data-stu-id="40f19-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="40f19-122">Om het importeren van kostenobjectdimensieleden eenvoudiger te maken, gebruikt u gegevensconnectors om de waarden op te halen uit de entiteiten die u wilt gebruiken als kostenobjectdimensies.</span><span class="sxs-lookup"><span data-stu-id="40f19-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="40f19-123">U kunt de vooraf aangemaakte gegevensconnectors gebruiken, of aangepaste gegevensconnectors die u zelf samenstelt.</span><span class="sxs-lookup"><span data-stu-id="40f19-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>




