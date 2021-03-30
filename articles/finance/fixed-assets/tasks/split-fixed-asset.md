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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db601be192b57fbec220193d3c9fde1a4f50c085
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213503"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="e0aa4-103">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="e0aa4-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0aa4-104">In dit onderwerp wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="e0aa4-105">Het gebruikt de accountantsrol en USMF-demogegevens.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="e0aa4-106">Nieuwe vaste activa maken</span><span class="sxs-lookup"><span data-stu-id="e0aa4-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="e0aa4-107">Ga in het navigatievenster naar **Modules \> Vaste activa \> Vaste activa \> Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="e0aa4-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-108">Select **New**.</span></span>
3. <span data-ttu-id="e0aa4-109">Typ of selecteer een waarde in het veld **Groep vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="e0aa4-110">Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="e0aa4-111">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="e0aa4-112">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="e0aa4-113">Een vast activum splitsen</span><span class="sxs-lookup"><span data-stu-id="e0aa4-113">Split a fixed asset</span></span>

<span data-ttu-id="e0aa4-114">Voordat een volledig afgeschreven activum wordt gesplitst, moet de status van het activaboek handmatig worden gewijzigd van **Afgesloten** in **Openstaand**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="e0aa4-115">Deze stap is vereist omdat de status van het boek **Openstaand** moet zijn als u transacties voor het activum moet boeken (bijvoorbeeld voor een afboekingsverkoop).</span><span class="sxs-lookup"><span data-stu-id="e0aa4-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="e0aa4-116">U moet ook de parameter **Meerdere transacties binnen één boekstuk toestaan** inschakelen op het tabblad **Algemeen** van de pagina **Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="e0aa4-117">Nadat de boekingsstatus van het activum is gewijzigd en er meerdere transacties binnen één boekstuk zijn toegestaan, voert u de volgende stappen uit om het activum te splitsen.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="e0aa4-118">Zoek en selecteer in de lijst de koppeling naar het vaste activum om te splitsen.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="e0aa4-119">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-119">Select **Books**.</span></span> <span data-ttu-id="e0aa4-120">Selecteer het boek dat u wilt opsplitsen naar het nieuwe activum.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="e0aa4-121">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-121">Select **Functions**.</span></span>
4. <span data-ttu-id="e0aa4-122">Selecteer **Vast activum splitsen**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="e0aa4-123">Typ of selecteer een waarde in het veld **Naar vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="e0aa4-124">Selecteer in het veld **Boeken** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e0aa4-125">Voer in het veld **Transactiedatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="e0aa4-126">Voer een getal in het veld **Percentage** in.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="e0aa4-127">Typ of selecteer een waarde in het veld **Journaalnaam**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="e0aa4-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="e0aa4-129">De journaaltransactie boeken</span><span class="sxs-lookup"><span data-stu-id="e0aa4-129">Post the journal transaction</span></span>

1. <span data-ttu-id="e0aa4-130">Ga in het navigatievenster naar **Modules \> Vaste activa \> Journaalboekingen \> Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="e0aa4-131">Selecteer in de lijst het journaal dat met het splitsingsproces is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="e0aa4-132">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="e0aa4-132">Select **Lines**.</span></span>

    - <span data-ttu-id="e0aa4-133">Controleer de gemaakte journaalregels.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="e0aa4-134">Een bijboekingscorrectietransactie wordt gemaakt voor het oorspronkelijke activum om de waarde te verlagen door het percentage dat is opgegeven tijdens het opsplitsingsproces.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="e0aa4-135">Een bijboekingstransactie wordt gemaakt voor het nieuwe activum voor hetzelfde bedrag.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="e0aa4-136">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]