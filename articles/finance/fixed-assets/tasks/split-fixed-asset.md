---
title: Een vast activum splitsen
description: In dit onderwerp wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138110"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="6b881-103">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="6b881-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b881-104">In dit onderwerp wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek.</span><span class="sxs-lookup"><span data-stu-id="6b881-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="6b881-105">Het gebruikt de accountantsrol en USMF-demogegevens.</span><span class="sxs-lookup"><span data-stu-id="6b881-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="6b881-106">Nieuwe vaste activa maken</span><span class="sxs-lookup"><span data-stu-id="6b881-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="6b881-107">Ga in het navigatievenster naar **Modules > Vaste activa > Vaste activa > Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="6b881-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="6b881-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6b881-108">Select **New**.</span></span>
3. <span data-ttu-id="6b881-109">Typ of selecteer een waarde in het veld **Groep vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="6b881-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="6b881-110">Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6b881-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="6b881-111">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="6b881-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="6b881-112">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="6b881-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="6b881-113">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="6b881-113">Split a fixed asset</span></span>
1. <span data-ttu-id="6b881-114">Zoek en selecteer in de lijst de koppeling naar het vaste activum om te splitsen.</span><span class="sxs-lookup"><span data-stu-id="6b881-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="6b881-115">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="6b881-115">Select **Books**.</span></span> <span data-ttu-id="6b881-116">Selecteer het boek dat u wilt opsplitsen naar het nieuwe activum.</span><span class="sxs-lookup"><span data-stu-id="6b881-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="6b881-117">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="6b881-117">Select **Functions**.</span></span>
4. <span data-ttu-id="6b881-118">Selecteer **Vast activum splitsen**.</span><span class="sxs-lookup"><span data-stu-id="6b881-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="6b881-119">Typ of selecteer een waarde in het veld **Naar vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="6b881-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="6b881-120">Selecteer in het veld **Boeken** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6b881-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6b881-121">Voer in het veld **Transactiedatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="6b881-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="6b881-122">Voer een getal in het veld **Percentage** in.</span><span class="sxs-lookup"><span data-stu-id="6b881-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="6b881-123">Typ of selecteer een waarde in het veld **Journaalnaam**.</span><span class="sxs-lookup"><span data-stu-id="6b881-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="6b881-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b881-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="6b881-125">De journaaltransactie boeken</span><span class="sxs-lookup"><span data-stu-id="6b881-125">Post the journal transaction</span></span>
1. <span data-ttu-id="6b881-126">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="6b881-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="6b881-127">Selecteer in de lijst het journaal dat met het splitsingsproces is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6b881-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="6b881-128">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="6b881-128">Select **Lines**.</span></span>

    - <span data-ttu-id="6b881-129">Controleer de gemaakte journaalregels.</span><span class="sxs-lookup"><span data-stu-id="6b881-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="6b881-130">Een bijboekingscorrectietransactie wordt gemaakt voor het oorspronkelijke activum om de waarde te verlagen door het percentage dat is opgegeven tijdens het opsplitsingsproces.</span><span class="sxs-lookup"><span data-stu-id="6b881-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="6b881-131">Een bijboekingstransactie wordt gemaakt voor het nieuwe activum voor hetzelfde bedrag.</span><span class="sxs-lookup"><span data-stu-id="6b881-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="6b881-132">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="6b881-132">Select **Post**.</span></span>

