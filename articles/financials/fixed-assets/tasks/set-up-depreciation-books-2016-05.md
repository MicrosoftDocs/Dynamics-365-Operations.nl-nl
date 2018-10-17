--- 
title: Afschrijvingsboeken voor activa instellen (mei 2016)
description: Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="c8921-103">Afschrijvingsboeken voor activa instellen (mei 2016)</span><span class="sxs-lookup"><span data-stu-id="c8921-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8921-104">Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="c8921-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="c8921-105">Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="c8921-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="c8921-106">Maak een afschrijvingsboek</span><span class="sxs-lookup"><span data-stu-id="c8921-106">Create a depreciation book</span></span>
1. <span data-ttu-id="c8921-107">Ga naar Vaste activa > Instellingen > Afschrijvingsboeken.</span><span class="sxs-lookup"><span data-stu-id="c8921-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="c8921-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c8921-108">Click New.</span></span>
3. <span data-ttu-id="c8921-109">Typ een waarde in het veld Afschrijvingsboek.</span><span class="sxs-lookup"><span data-stu-id="c8921-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="c8921-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c8921-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c8921-111">Schakel het selectievakje Afschrijving berekenen in of uit.</span><span class="sxs-lookup"><span data-stu-id="c8921-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="c8921-112">Klik in het veld Afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8921-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c8921-113">Zoek en selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8921-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="c8921-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8921-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c8921-115">Klik in het veld Alternatief afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8921-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c8921-116">Selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8921-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="c8921-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8921-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c8921-118">Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="c8921-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="c8921-119">U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.</span><span class="sxs-lookup"><span data-stu-id="c8921-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="c8921-120">Schakel het selectievakje Afschrijvingscorrecties met basiscorrecties maken in of uit.</span><span class="sxs-lookup"><span data-stu-id="c8921-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="c8921-121">Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8921-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c8921-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8921-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="c8921-123">Afschrijvingsboeken aan vaste-activagroepen koppelen</span><span class="sxs-lookup"><span data-stu-id="c8921-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="c8921-124">Klik op Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="c8921-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="c8921-125">Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8921-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c8921-126">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8921-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c8921-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8921-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c8921-128">Selecteer in het veld Afschrijvingsconventie een optie.</span><span class="sxs-lookup"><span data-stu-id="c8921-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="c8921-129">Voer een getal in het veld Levensduur in.</span><span class="sxs-lookup"><span data-stu-id="c8921-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="c8921-130">Merk op dat de waarde van het veld Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="c8921-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


