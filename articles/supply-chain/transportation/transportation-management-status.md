---
title: Statussen voor Transportbeheer
description: In dit onderwerp wordt uitgelegd hoe u een transportstatus maakt en die status toewijst aan een de status van een vervoerder.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006461"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="2c031-103">Statussen voor Transportbeheer</span><span class="sxs-lookup"><span data-stu-id="2c031-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c031-104">Stel modelcodes voor transportstatussen in om codes te interpreteren die door uw vervoerders worden verstrekt.</span><span class="sxs-lookup"><span data-stu-id="2c031-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="2c031-105">Hiermee kunt u integreren met vervoerders om een status te geven.</span><span class="sxs-lookup"><span data-stu-id="2c031-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="2c031-106">De transportstatus die u voor een transportstatusmodelcode opgeeft, kan u helpen de status van een lading, zending of container te volgen.</span><span class="sxs-lookup"><span data-stu-id="2c031-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="2c031-107">De specifieke transportstatus voor een lading, zending of container kan alleen worden bijgewerkt via gegevensintegratie en niet handmatig via de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="2c031-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="2c031-108">Een transportstatus maken</span><span class="sxs-lookup"><span data-stu-id="2c031-108">Create a transportation status</span></span>

<span data-ttu-id="2c031-109">Volg deze stappen om een transportstatus te maken:</span><span class="sxs-lookup"><span data-stu-id="2c031-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="2c031-110">Ga naar **Transportbeheer \> Instellingen \> Transportstatusmodellen**.</span><span class="sxs-lookup"><span data-stu-id="2c031-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="2c031-111">Selecteer **Nieuw** om een nieuw transportstatusmodel te maken.</span><span class="sxs-lookup"><span data-stu-id="2c031-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="2c031-112">Voer in het veld **Transportstatusmodel** een unieke code voor de transportstatus in.</span><span class="sxs-lookup"><span data-stu-id="2c031-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="2c031-113">Selecteer in het veld **Transporttype** als type transport *Vervoerder* of *Hub*.</span><span class="sxs-lookup"><span data-stu-id="2c031-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="2c031-114">Voer een naam en een transportstatus in.</span><span class="sxs-lookup"><span data-stu-id="2c031-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="2c031-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2c031-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="2c031-116">Een transportstatus toewijzen aan de status van een vervoerder</span><span class="sxs-lookup"><span data-stu-id="2c031-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="2c031-117">Ga als volgt te werk om een transportstatus toe te wijzen aan de status van een vervoerder:</span><span class="sxs-lookup"><span data-stu-id="2c031-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="2c031-118">Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Transportstatus vervoerder**.</span><span class="sxs-lookup"><span data-stu-id="2c031-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="2c031-119">Selecteer **Nieuw** om een code van een vervoerder te koppelen aan een transportstatusmodelcode.</span><span class="sxs-lookup"><span data-stu-id="2c031-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="2c031-120">Selecteer de unieke id voor de vervoerder en de vervoerdersservice.</span><span class="sxs-lookup"><span data-stu-id="2c031-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="2c031-121">Selecteer de transportstatuscode die u wilt koppelen aan de code van de geselecteerde vervoerder.</span><span class="sxs-lookup"><span data-stu-id="2c031-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="2c031-122">Voer de externe code in die door de vervoerder wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2c031-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="2c031-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2c031-123">Close the page.</span></span>
