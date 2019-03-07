---
title: Een toevoeging aan een vast activum invoeren
description: Deze procedure laat zien hoe u een toevoeging aan een bestaand vast activum toevoegt.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "324417"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="76ffd-103">Een toevoeging aan een vast activum invoeren</span><span class="sxs-lookup"><span data-stu-id="76ffd-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76ffd-104">Deze procedure laat zien hoe u een toevoeging aan een bestaand vast activum toevoegt.</span><span class="sxs-lookup"><span data-stu-id="76ffd-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="76ffd-105">Het doel van vaste-activatoevoegingen is artikeltoevoegingen, onderhoud, of verbeteringen voor een activum bij te houden, en is alleen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="76ffd-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="76ffd-106">Eventuele wijzigingen in de waarde van de vaste activa of levensduur moeten afzonderlijk worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76ffd-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="76ffd-107">De procedure gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="76ffd-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="76ffd-108">Ga naar Vaste activa > Vaste activa > Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="76ffd-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="76ffd-109">Zoek en selecteer in de lijst het vaste activum voor de toevoeging.</span><span class="sxs-lookup"><span data-stu-id="76ffd-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="76ffd-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76ffd-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="76ffd-111">Klik in het actievenster op Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="76ffd-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="76ffd-112">Klik op Toevoegingen van vaste activa.</span><span class="sxs-lookup"><span data-stu-id="76ffd-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="76ffd-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76ffd-113">Click New.</span></span>
7. <span data-ttu-id="76ffd-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="76ffd-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="76ffd-115">Stel de datum van de toevoegingsaankoop of -service in.</span><span class="sxs-lookup"><span data-stu-id="76ffd-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="76ffd-116">Voer de kosten van het artikel, het onderhoud of andere verbeteringen voor het activum in.</span><span class="sxs-lookup"><span data-stu-id="76ffd-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="76ffd-117">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="76ffd-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="76ffd-118">De totale kosten hebben geen gevolg voor de waarde van vaste activa en zijn voor tracering en ter informatie.</span><span class="sxs-lookup"><span data-stu-id="76ffd-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="76ffd-119">Als de kosten worden gekapitaliseerd, moet een opwaarderingscorrectietransactie apart worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="76ffd-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="76ffd-120">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="76ffd-120">Click the General tab.</span></span>
    * <span data-ttu-id="76ffd-121">Stel Hiermee wordt de levensduur verlengd in als de levensduur van de vaste activa toeneemt door de toevoeging.</span><span class="sxs-lookup"><span data-stu-id="76ffd-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="76ffd-122">Dit veld is alleen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="76ffd-122">This field is informational only.</span></span> <span data-ttu-id="76ffd-123">Als u de levensduur wilt verlengen, wijzigt u de levensduur in de waardemodellen en/of afschrijvingsboeken voor het activum.</span><span class="sxs-lookup"><span data-stu-id="76ffd-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

