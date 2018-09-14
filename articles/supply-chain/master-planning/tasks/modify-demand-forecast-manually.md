--- 
title: Handmatig een vraagprognose wijzigen
description: Deze procedure laat zien hoe u de prognose voor een artikel kunt wijzigen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 063554c98b8a6261ebe69073f214a8e45850c623
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="6b0a4-103">Handmatig een vraagprognose wijzigen</span><span class="sxs-lookup"><span data-stu-id="6b0a4-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b0a4-104">Deze procedure laat zien hoe u de prognose voor een artikel kunt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="6b0a4-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6b0a4-106">Deze opname is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="6b0a4-107">De prognose voor een artikel wijzigen</span><span class="sxs-lookup"><span data-stu-id="6b0a4-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="6b0a4-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6b0a4-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b0a4-110">Selecteer het artikel waarvoor u de prognose wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="6b0a4-111">Zo kunt u bijvoorbeeld het artikel D0001 selecteren.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="6b0a4-112">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="6b0a4-113">Klik op Vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="6b0a4-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6b0a4-115">Als er geen prognoseregels zijn, maakt u een nieuwe regel door</span><span class="sxs-lookup"><span data-stu-id="6b0a4-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="6b0a4-116">op Nieuw te klikken op de appbalk.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="6b0a4-117">Voer in het veld Verkoophoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="6b0a4-118">Dit getal geeft de geraamde hoeveelheid voor het artikel aan.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="6b0a4-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="6b0a4-120">De prognose in Excel wijzigen</span><span class="sxs-lookup"><span data-stu-id="6b0a4-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="6b0a4-121">Klik op Openen in Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="6b0a4-122">Klik op Vraagprognose bewerken in Excel.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="6b0a4-123">In Excel kunt u vraagprognoseregels toevoegen, verwijderen en bewerken.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="6b0a4-124">Als u de gegevens niet kunt weergeven in Excel, moet u zich aanmelden bij Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, met de optie 'Aangemeld blijven' ingeschakeld en moet u de app voor gegevensverbinding vertrouwen.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


