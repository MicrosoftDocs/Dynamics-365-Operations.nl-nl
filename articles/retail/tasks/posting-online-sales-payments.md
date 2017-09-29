--- 
title: " Online verkopen en betalingen boeken"
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e8c3f861a53a3f5c2de29248523ff4efd5e1d072
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="24ad1-103"> Online verkopen en betalingen boeken</span><span class="sxs-lookup"><span data-stu-id="24ad1-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="24ad1-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="24ad1-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="24ad1-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="24ad1-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="24ad1-106">Ga naar Alle werkruimten > Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="24ad1-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="24ad1-107">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="24ad1-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="24ad1-108">Selecteer in het veld Organisatiehiërarchie 'Detailhandelwinkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="24ad1-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="24ad1-109">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="24ad1-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="24ad1-110">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="24ad1-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="24ad1-111">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="24ad1-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="24ad1-112">Schakel het selectievakje Batchverwerking in of uit.</span><span class="sxs-lookup"><span data-stu-id="24ad1-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="24ad1-113">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="24ad1-113">Click Recurrence.</span></span>
7. <span data-ttu-id="24ad1-114">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="24ad1-114">Select the No end date option.</span></span>
8. <span data-ttu-id="24ad1-115">Voer een getal in het veld Aantal in.</span><span class="sxs-lookup"><span data-stu-id="24ad1-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="24ad1-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="24ad1-116">Click OK.</span></span>
10. <span data-ttu-id="24ad1-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="24ad1-117">Click OK.</span></span>


