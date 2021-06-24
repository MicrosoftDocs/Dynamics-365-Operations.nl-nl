---
title: 'Guide: handmatig een vraagprognose wijzigen'
description: Dit onderwerp laat zien hoe u de prognose voor een artikel kunt wijzigen
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224005"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="4b979-103">Guide: handmatig een vraagprognose wijzigen</span><span class="sxs-lookup"><span data-stu-id="4b979-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b979-104">Deze procedure laat zien hoe u de prognose voor een artikel kunt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4b979-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="4b979-105">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="4b979-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="4b979-106">De prognose voor een geselecteerd artikel wijzigen</span><span class="sxs-lookup"><span data-stu-id="4b979-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="4b979-107">De prognose voor een geselecteerd artikel wijzigen:</span><span class="sxs-lookup"><span data-stu-id="4b979-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="4b979-108">Ga naar **Modules \> Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="4b979-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4b979-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4b979-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="4b979-110">Selecteer het artikel waarvoor u de prognose wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4b979-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="4b979-111">Open in het actievenster het tabblad **Plan** en selecteer **Vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="4b979-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="4b979-112">Selecteer een rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4b979-112">In the list, select a row.</span></span> <span data-ttu-id="4b979-113">Als er geen prognoseregels zijn, maakt u een nieuwe regel door **Nieuw** te selecteren in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4b979-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="4b979-114">Voer in het veld **Verkoophoeveelheid** een positief getal in.</span><span class="sxs-lookup"><span data-stu-id="4b979-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="4b979-115">Dit getal geeft de geraamde hoeveelheid voor het artikel aan.</span><span class="sxs-lookup"><span data-stu-id="4b979-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="4b979-116">Als u een negatief getal opgeeft, wordt er een fout weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b979-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="4b979-117">Vul zo nodig de andere velden in.</span><span class="sxs-lookup"><span data-stu-id="4b979-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="4b979-118">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4b979-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="4b979-119">De prognose voor een of meer artikelen wijzigen met Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="4b979-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="4b979-120">Ga als volgt te werk om de prognose voor een of meer artikelen te wijzigen met Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="4b979-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="4b979-121">U kunt een van de volgende dingen doen:</span><span class="sxs-lookup"><span data-stu-id="4b979-121">Do one of the following:</span></span>
    - <span data-ttu-id="4b979-122">Open de **pagina Vraagprognose** voor een artikel (het maakt niet uit welke pagina) zoals wordt beschreven in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="4b979-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="4b979-123">Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Vraagprognoseregels**.</span><span class="sxs-lookup"><span data-stu-id="4b979-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="4b979-124">Selecteer in het actievenster **Openen in Microsoft Office \> Invoer vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="4b979-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="4b979-125">Selecteer een downloadlocatie, sla deze op en open het gedownloade bestand in Excel.</span><span class="sxs-lookup"><span data-stu-id="4b979-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="4b979-126">Als er een waarschuwing wordt gegeven, kiest u **Bewerken inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="4b979-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="4b979-127">Meld u in Excel aan bij Supply Chain Management met het Microsoft Dynamics-taakvenster.</span><span class="sxs-lookup"><span data-stu-id="4b979-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="4b979-128">U moet zich aanmelden via de optie **Aangemeld houden** en u moet de app voor gegevensverbinding vertrouwen.</span><span class="sxs-lookup"><span data-stu-id="4b979-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="4b979-129">In het Excel-werkblad worden nu alle huidige vraagprognoseregels voor uw bedrijf weergeven.</span><span class="sxs-lookup"><span data-stu-id="4b979-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="4b979-130">U kunt naar wens vraagprognoseregels toevoegen, verwijderen en bewerken.</span><span class="sxs-lookup"><span data-stu-id="4b979-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="4b979-131">Selecteer **Publiceren** in het Microsoft Dynamics-taakvenster om de wijzigingen weer naar Supply Chain Management te uploaden.</span><span class="sxs-lookup"><span data-stu-id="4b979-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
