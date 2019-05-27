---
title: Afschrijvingsboeken voor activa instellen (mei 2016)
description: Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566910"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="d0601-103">Afschrijvingsboeken voor activa instellen (mei 2016)</span><span class="sxs-lookup"><span data-stu-id="d0601-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0601-104">Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="d0601-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="d0601-105">Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d0601-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="d0601-106">Maak een afschrijvingsboek</span><span class="sxs-lookup"><span data-stu-id="d0601-106">Create a depreciation book</span></span>
1. <span data-ttu-id="d0601-107">Ga naar Vaste activa > Instellingen > Afschrijvingsboeken.</span><span class="sxs-lookup"><span data-stu-id="d0601-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="d0601-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d0601-108">Click New.</span></span>
3. <span data-ttu-id="d0601-109">Typ een waarde in het veld Afschrijvingsboek.</span><span class="sxs-lookup"><span data-stu-id="d0601-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="d0601-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="d0601-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d0601-111">Schakel het selectievakje Afschrijving berekenen in of uit.</span><span class="sxs-lookup"><span data-stu-id="d0601-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="d0601-112">Klik in het veld Afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d0601-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d0601-113">Zoek en selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d0601-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="d0601-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d0601-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d0601-115">Klik in het veld Alternatief afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d0601-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d0601-116">Selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d0601-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="d0601-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d0601-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d0601-118">Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="d0601-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="d0601-119">U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.</span><span class="sxs-lookup"><span data-stu-id="d0601-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="d0601-120">Schakel het selectievakje Afschrijvingscorrecties met basiscorrecties maken in of uit.</span><span class="sxs-lookup"><span data-stu-id="d0601-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="d0601-121">Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d0601-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d0601-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d0601-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="d0601-123">Afschrijvingsboeken aan vaste-activagroepen koppelen</span><span class="sxs-lookup"><span data-stu-id="d0601-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="d0601-124">Klik op Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="d0601-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="d0601-125">Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d0601-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d0601-126">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d0601-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d0601-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d0601-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d0601-128">Selecteer in het veld Afschrijvingsconventie een optie.</span><span class="sxs-lookup"><span data-stu-id="d0601-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="d0601-129">Voer een getal in het veld Levensduur in.</span><span class="sxs-lookup"><span data-stu-id="d0601-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="d0601-130">Merk op dat de waarde van het veld Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d0601-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

