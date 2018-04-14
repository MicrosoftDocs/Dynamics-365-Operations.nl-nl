--- 
title: 'Afschrijvingsboeken instellen '
description: Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 264e671774a1be03f4529339990d4727d20f6d38
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-depreciation-books"></a><span data-ttu-id="6ae71-103">Afschrijvingsboeken instellen </span><span class="sxs-lookup"><span data-stu-id="6ae71-103">Set up depreciation books</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ae71-104">Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="6ae71-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="6ae71-105">Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="6ae71-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="6ae71-106">Maak een afschrijvingsboek</span><span class="sxs-lookup"><span data-stu-id="6ae71-106">Create a depreciation book</span></span>
1. <span data-ttu-id="6ae71-107">Ga naar Vaste activa > Instellingen > Afschrijvingsboeken.</span><span class="sxs-lookup"><span data-stu-id="6ae71-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="6ae71-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6ae71-108">Click New.</span></span>
3. <span data-ttu-id="6ae71-109">Typ een waarde in het veld Afschrijvingsboek.</span><span class="sxs-lookup"><span data-stu-id="6ae71-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="6ae71-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6ae71-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6ae71-111">Schakel het selectievakje Afschrijving berekenen in of uit.</span><span class="sxs-lookup"><span data-stu-id="6ae71-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="6ae71-112">Klik in het veld Afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6ae71-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6ae71-113">Zoek en selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ae71-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="6ae71-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ae71-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6ae71-115">Klik in het veld Alternatief afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6ae71-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="6ae71-116">Selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ae71-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="6ae71-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ae71-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6ae71-118">Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="6ae71-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="6ae71-119">U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.</span><span class="sxs-lookup"><span data-stu-id="6ae71-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="6ae71-120">Schakel het selectievakje Afschrijvingscorrecties met basiscorrecties maken in of uit.</span><span class="sxs-lookup"><span data-stu-id="6ae71-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="6ae71-121">Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6ae71-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="6ae71-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ae71-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="6ae71-123">Afschrijvingsboeken aan vaste-activagroepen koppelen</span><span class="sxs-lookup"><span data-stu-id="6ae71-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="6ae71-124">Klik op Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="6ae71-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="6ae71-125">Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6ae71-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6ae71-126">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ae71-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6ae71-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ae71-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6ae71-128">Selecteer in het veld Afschrijvingsconventie een optie.</span><span class="sxs-lookup"><span data-stu-id="6ae71-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="6ae71-129">Voer een getal in het veld Levensduur in.</span><span class="sxs-lookup"><span data-stu-id="6ae71-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="6ae71-130">Merk op dat de waarde van het veld Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6ae71-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


