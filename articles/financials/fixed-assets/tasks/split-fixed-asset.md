--- 
title: Een vast activum splitsen
description: "Deze taakbegeleiding splitst een percentage van één activumboek op naar een nieuw activumboek."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="0c23b-103">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="0c23b-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c23b-104">Deze taakbegeleiding splitst een percentage van één activumboek op naar een nieuw activumboek.</span><span class="sxs-lookup"><span data-stu-id="0c23b-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="0c23b-105">Het gebruikt de accountantsrol en USMF-demogegevens.</span><span class="sxs-lookup"><span data-stu-id="0c23b-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="0c23b-106">Nieuwe vaste activa maken</span><span class="sxs-lookup"><span data-stu-id="0c23b-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="0c23b-107">Ga naar Vaste activa > Vaste activa > Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="0c23b-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="0c23b-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0c23b-108">Click New.</span></span>
3. <span data-ttu-id="0c23b-109">Typ of selecteer een waarde in het veld Groep vaste activa.</span><span class="sxs-lookup"><span data-stu-id="0c23b-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="0c23b-110">Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0c23b-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="0c23b-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0c23b-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0c23b-112">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="0c23b-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="0c23b-113">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="0c23b-113">Split a fixed asset</span></span>
1. <span data-ttu-id="0c23b-114">Zoek en selecteer in de lijst het vaste activum om te splitsen.</span><span class="sxs-lookup"><span data-stu-id="0c23b-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="0c23b-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0c23b-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0c23b-116">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="0c23b-116">Click Books.</span></span>
    * <span data-ttu-id="0c23b-117">Selecteer het boek dat u wilt opsplitsen naar het nieuwe activum.</span><span class="sxs-lookup"><span data-stu-id="0c23b-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="0c23b-118">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="0c23b-118">Click Functions.</span></span>
5. <span data-ttu-id="0c23b-119">Klik op Vaste activa splitsen.</span><span class="sxs-lookup"><span data-stu-id="0c23b-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="0c23b-120">Typ of selecteer een waarde in het veld Naar vaste activa.</span><span class="sxs-lookup"><span data-stu-id="0c23b-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="0c23b-121">Klik in het veld Boeken op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0c23b-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0c23b-122">Voer in het veld Transactiedatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="0c23b-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="0c23b-123">Voer een getal in het veld Percentage in.</span><span class="sxs-lookup"><span data-stu-id="0c23b-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="0c23b-124">Typ of selecteer een waarde in het veld Journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="0c23b-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="0c23b-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0c23b-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="0c23b-126">De journaaltransactie boeken</span><span class="sxs-lookup"><span data-stu-id="0c23b-126">Post the journal transaction</span></span>
1. <span data-ttu-id="0c23b-127">Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="0c23b-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="0c23b-128">Selecteer in de lijst het journaal dat met het splitsingsproces is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0c23b-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="0c23b-129">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="0c23b-129">Click Lines.</span></span>
    * <span data-ttu-id="0c23b-130">Controleer de gemaakte journaalregels.</span><span class="sxs-lookup"><span data-stu-id="0c23b-130">Verify the journal lines created.</span></span>  <span data-ttu-id="0c23b-131">Een bijboekingscorrectietransactie wordt gemaakt voor het oorspronkelijke activum om de waarde te verlagen door het percentage dat is opgegeven tijdens het opsplitsingsproces.</span><span class="sxs-lookup"><span data-stu-id="0c23b-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="0c23b-132">Een bijboekingstransactie wordt gemaakt voor het nieuwe activum voor hetzelfde bedrag.</span><span class="sxs-lookup"><span data-stu-id="0c23b-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="0c23b-133">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="0c23b-133">Click Post.</span></span>


