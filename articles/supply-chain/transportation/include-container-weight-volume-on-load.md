---
title: Containergewicht en -volume in lading opnemen
description: In dit onderwerp wordt beschreven hoe u functionaliteit instelt en toepast om containergewicht en -volume in ladingen op te nemen.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e6b29bf2e42ea2df3d36f39fa577078009aa584
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206283"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="c5699-103">Containergewicht en -volume in lading opnemen</span><span class="sxs-lookup"><span data-stu-id="c5699-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5699-104">De functionaliteit voor het opnemen van het containergewicht en -volume in een lading geeft een duidelijk beeld van het totale gewicht en volume van containers en artikelen in een lading.</span><span class="sxs-lookup"><span data-stu-id="c5699-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="c5699-105">Een lading bevat een enkele zending of meerdere zendingen en deze zendingen bevatten bepaalde artikelen die tot één verkooporder of meerdere verkooporders behoren.</span><span class="sxs-lookup"><span data-stu-id="c5699-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="c5699-106">De artikelen zijn opgeslagen in een container en containers worden in een lading geladen.</span><span class="sxs-lookup"><span data-stu-id="c5699-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="c5699-107">Artikelen buiten een container kunnen ook deel uitmaken van een lading.</span><span class="sxs-lookup"><span data-stu-id="c5699-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="c5699-108">Op basis van deze voorwaarden berekent het systeem waarden voor het gewicht en volume van de lading door rekening te houden met het gewicht en volume van de containers en artikelen.</span><span class="sxs-lookup"><span data-stu-id="c5699-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="c5699-109">Als de berekende waarden niet nauwkeurig zijn, kunt u deze aanpassen door de werkelijke waarden voor het gewicht en volume in de lading in te voeren.</span><span class="sxs-lookup"><span data-stu-id="c5699-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="c5699-110">De waarden voor het gewicht en volume worden gebruikt in transportbeheerprocessen.</span><span class="sxs-lookup"><span data-stu-id="c5699-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="c5699-111">De waarden worden bijvoorbeeld gebruikt in de tariefroute-workbench, waar ze helpen bij het definiëren van het tarief en de route voor ladingen. Daarnaast worden ze gebruikt voor transportbetalingsmethoden en het inchecken van de chauffeur.</span><span class="sxs-lookup"><span data-stu-id="c5699-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c5699-112">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="c5699-112">Where it applies</span></span>

<span data-ttu-id="c5699-113">De functionaliteit voor het opnemen van het containergewicht en -volume in een lading wordt toegepast in transportbeheerprocessen, zoals de tariefroute-workbench, transportbetalingsmethoden en het inchecken van de chauffeur.</span><span class="sxs-lookup"><span data-stu-id="c5699-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="c5699-114">De instelling</span><span class="sxs-lookup"><span data-stu-id="c5699-114">How it is set up</span></span>

<span data-ttu-id="c5699-115">Het aantal containers voor een lading wordt berekend op basis van het gewicht en volume van de container en het percentage van de container dat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c5699-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="c5699-116">Als u het gewicht en volume voor een container wilt instellen, klikt u op **Magazijnbeheer** \> **Instellingen** \> **Containers** \> **Containertypen**.</span><span class="sxs-lookup"><span data-stu-id="c5699-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="c5699-117">U stelt het containergebruikspercentage in door te klikken op **Magazijnbeheer** \> **Instellingen** \> **Containers** \> **Containergroepen** en een waarde in te voeren in het veld **Containergebruikspercentage**.</span><span class="sxs-lookup"><span data-stu-id="c5699-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
