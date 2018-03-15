---
title: Tijdvensters
description: U kunt tijdvensters gebruiken voor het optimaliseren van de planning van serviceorderregels.
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: b7268870aa9065e4e52d936e819107094bad3663
ms.contentlocale: nl-nl
ms.lasthandoff: 02/20/2018

---

# <a name="time-windows"></a><span data-ttu-id="a7a8e-103">Tijdvensters</span><span class="sxs-lookup"><span data-stu-id="a7a8e-103">Time windows</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a7a8e-104">U kunt tijdvensters gebruiken voor het optimaliseren van de planning van serviceorderregels.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="a7a8e-105">U kunt het systeem zo instellen dat het automatisch serviceorders maakt.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="a7a8e-106">Op basis van de criteria die door een tijdvenster zijn opgegeven, kunt u zoveel mogelijk serviceorderregels verbinden aan zo weinig mogelijk serviceorders.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="a7a8e-107">Door tijdvensters wordt opgegeven in hoeverre een serviceorderregel ten opzichte van de berekende datum kan worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="a7a8e-108">De berekende datum is de datum waarop de serviceorderregel is gepland.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="a7a8e-109">De datum is gebaseerd op de instelling van het interval en de serviceperiode die u hebt gedefinieerd op de pagina **Serviceorders maken**.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="a7a8e-110">U definieert een tijdvenster door de waarden uit de volgende tabel te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="a7a8e-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="a7a8e-111">methode</span><span class="sxs-lookup"><span data-stu-id="a7a8e-111">Method</span></span> | <span data-ttu-id="a7a8e-112">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="a7a8e-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a8e-113">Week</span><span class="sxs-lookup"><span data-stu-id="a7a8e-113">Week</span></span>   | <span data-ttu-id="a7a8e-114">De datum waarop de serviceorderregel kan worden verplaatst naar een willekeurige open dag in dezelfde week als de oorspronkelijk berekende datum.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="a7a8e-115">Maand</span><span class="sxs-lookup"><span data-stu-id="a7a8e-115">Month</span></span>  | <span data-ttu-id="a7a8e-116">De datum waarop de serviceorderregel kan worden verplaatst naar een willekeurige open dag in dezelfde maand als de oorspronkelijk berekende datum.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="a7a8e-117">Stel dat de berekende datum voor een serviceorderregel 15 februari 2017 is.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="a7a8e-118">In dat geval kan de serviceorderregel worden gepland voor elke willekeurige werkdag tussen 1 februari en 28 februari 2017.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="a7a8e-119">Handmatig</span><span class="sxs-lookup"><span data-stu-id="a7a8e-119">Manual</span></span> | <span data-ttu-id="a7a8e-120">U definieert het maximum aantal dagen voor of na de oorspronkelijk berekende datum waarop de serviceorderregel verplaatst kan worden.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="a7a8e-121">Indien u geen tijdvenster opgeeft voor een serviceovereenkomstregel, moet de serviceorderregel die is afgeleid van de serviceovereenkomst op de precieze datum plaatsvinden waarop deze oorspronkelijk was gepland.</span><span class="sxs-lookup"><span data-stu-id="a7a8e-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7a8e-122">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="a7a8e-122">Related topics</span></span>

[<span data-ttu-id="a7a8e-123">Tijdvensters maken</span><span class="sxs-lookup"><span data-stu-id="a7a8e-123">Create time windows</span></span>](create-time-windows.md)


