---
title: Handmatig een vraagprognose wijzigen
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889019"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="67715-103">Handmatig een vraagprognose wijzigen</span><span class="sxs-lookup"><span data-stu-id="67715-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67715-104">Deze procedure laat zien hoe u de prognose voor een artikel kunt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="67715-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="67715-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="67715-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="67715-106">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="67715-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="67715-107">De prognose voor een geselecteerd artikel wijzigen</span><span class="sxs-lookup"><span data-stu-id="67715-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="67715-108">De prognose voor een geselecteerd artikel wijzigen:</span><span class="sxs-lookup"><span data-stu-id="67715-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="67715-109">Ga naar **Modules \> Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="67715-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="67715-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="67715-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="67715-111">Selecteer het artikel waarvoor u de prognose wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="67715-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="67715-112">Open in het actievenster het tabblad **Plan** en selecteer **Vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="67715-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="67715-113">Selecteer een rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="67715-113">In the list, select a row.</span></span> <span data-ttu-id="67715-114">Als er geen prognoseregels zijn, maakt u een nieuwe regel door **Nieuw** te selecteren in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="67715-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="67715-115">Voer in het veld **Verkoophoeveelheid** een positief getal in.</span><span class="sxs-lookup"><span data-stu-id="67715-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="67715-116">Dit getal geeft de geraamde hoeveelheid voor het artikel aan.</span><span class="sxs-lookup"><span data-stu-id="67715-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="67715-117">Als u een negatief getal opgeeft, wordt er een fout weergegeven.</span><span class="sxs-lookup"><span data-stu-id="67715-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="67715-118">Vul zo nodig de andere velden in.</span><span class="sxs-lookup"><span data-stu-id="67715-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="67715-119">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="67715-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="67715-120">De prognose voor een of meer artikelen wijzigen met Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="67715-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="67715-121">De prognose voor een of meer artikelen wijzigen met Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="67715-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="67715-122">U kunt een van de volgende dingen doen:</span><span class="sxs-lookup"><span data-stu-id="67715-122">Do one of the following:</span></span>
    - <span data-ttu-id="67715-123">Open de **pagina Vraagprognose** voor een artikel (het maakt niet uit welke pagina) zoals wordt beschreven in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="67715-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="67715-124">Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Vraagprognoseregels**.</span><span class="sxs-lookup"><span data-stu-id="67715-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="67715-125">Selecteer in het actievenster **Openen in Microsoft Office \> Invoer vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="67715-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="67715-126">Selecteer een downloadlocatie, sla deze op en open het gedownloade bestand in Excel.</span><span class="sxs-lookup"><span data-stu-id="67715-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="67715-127">Als er een waarschuwing wordt gegeven, kiest u **Bewerken inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="67715-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="67715-128">Meld u in Excel aan bij Supply Chain Management met het Microsoft Dynamics-taakvenster.</span><span class="sxs-lookup"><span data-stu-id="67715-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="67715-129">U moet zich aanmelden via de optie **Aangemeld houden** en u moet de app voor gegevensverbinding vertrouwen.</span><span class="sxs-lookup"><span data-stu-id="67715-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="67715-130">In het Excel-werkblad worden nu alle huidige vraagprognoseregels voor uw bedrijf weergeven.</span><span class="sxs-lookup"><span data-stu-id="67715-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="67715-131">U kunt naar wens vraagprognoseregels toevoegen, verwijderen en bewerken.</span><span class="sxs-lookup"><span data-stu-id="67715-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="67715-132">Selecteer **Publiceren** in het Microsoft Dynamics-taakvenster om de wijzigingen weer naar Supply Chain Management te uploaden.</span><span class="sxs-lookup"><span data-stu-id="67715-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
