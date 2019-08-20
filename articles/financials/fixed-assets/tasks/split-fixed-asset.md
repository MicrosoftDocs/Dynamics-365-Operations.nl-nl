---
title: Een vast activum splitsen
description: Deze taakbegeleiding splitst een percentage van één activumboek op naar een nieuw activumboek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5fdc8a7b326daca1fc0f0962c69bb8fb1ff64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839708"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="68746-103">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="68746-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68746-104">Deze taakbegeleiding splitst een percentage van één activumboek op naar een nieuw activumboek.</span><span class="sxs-lookup"><span data-stu-id="68746-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="68746-105">Het gebruikt de accountantsrol en USMF-demogegevens.</span><span class="sxs-lookup"><span data-stu-id="68746-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="68746-106">Nieuwe vaste activa maken</span><span class="sxs-lookup"><span data-stu-id="68746-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="68746-107">Ga naar Vaste activa > Vaste activa > Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="68746-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="68746-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="68746-108">Click New.</span></span>
3. <span data-ttu-id="68746-109">Typ of selecteer een waarde in het veld Groep vaste activa.</span><span class="sxs-lookup"><span data-stu-id="68746-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="68746-110">Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="68746-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="68746-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68746-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="68746-112">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="68746-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="68746-113">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="68746-113">Split a fixed asset</span></span>
1. <span data-ttu-id="68746-114">Zoek en selecteer in de lijst het vaste activum om te splitsen.</span><span class="sxs-lookup"><span data-stu-id="68746-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="68746-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="68746-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="68746-116">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="68746-116">Click Books.</span></span>
    * <span data-ttu-id="68746-117">Selecteer het boek dat u wilt opsplitsen naar het nieuwe activum.</span><span class="sxs-lookup"><span data-stu-id="68746-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="68746-118">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="68746-118">Click Functions.</span></span>
5. <span data-ttu-id="68746-119">Klik op Vaste activa splitsen.</span><span class="sxs-lookup"><span data-stu-id="68746-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="68746-120">Typ of selecteer een waarde in het veld Naar vaste activa.</span><span class="sxs-lookup"><span data-stu-id="68746-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="68746-121">Klik in het veld Boeken op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="68746-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="68746-122">Voer in het veld Transactiedatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="68746-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="68746-123">Voer een getal in het veld Percentage in.</span><span class="sxs-lookup"><span data-stu-id="68746-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="68746-124">Typ of selecteer een waarde in het veld Journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="68746-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="68746-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="68746-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="68746-126">De journaaltransactie boeken</span><span class="sxs-lookup"><span data-stu-id="68746-126">Post the journal transaction</span></span>
1. <span data-ttu-id="68746-127">Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="68746-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="68746-128">Selecteer in de lijst het journaal dat met het splitsingsproces is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="68746-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="68746-129">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="68746-129">Click Lines.</span></span>
    * <span data-ttu-id="68746-130">Controleer de gemaakte journaalregels.</span><span class="sxs-lookup"><span data-stu-id="68746-130">Verify the journal lines created.</span></span>  <span data-ttu-id="68746-131">Een bijboekingscorrectietransactie wordt gemaakt voor het oorspronkelijke activum om de waarde te verlagen door het percentage dat is opgegeven tijdens het opsplitsingsproces.</span><span class="sxs-lookup"><span data-stu-id="68746-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="68746-132">Een bijboekingstransactie wordt gemaakt voor het nieuwe activum voor hetzelfde bedrag.</span><span class="sxs-lookup"><span data-stu-id="68746-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="68746-133">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="68746-133">Click Post.</span></span>

