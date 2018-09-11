--- 
title: Een vast activum afstoten met een vrije-tekstfactuur
description: In deze procedure ziet u hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: bf449be5f9b79c1e6bf7d9a5dd6d7cdede20eea9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="a80d0-103">Een vast activum afstoten met een vrije-tekstfactuur</span><span class="sxs-lookup"><span data-stu-id="a80d0-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a80d0-104">In deze procedure ziet u hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="a80d0-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="a80d0-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="a80d0-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="a80d0-106">Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="a80d0-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="a80d0-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a80d0-107">Click New.</span></span>
3. <span data-ttu-id="a80d0-108">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a80d0-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a80d0-109">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="a80d0-109">Click Lines.</span></span>
5. <span data-ttu-id="a80d0-110">Klik op Voorstellen.</span><span class="sxs-lookup"><span data-stu-id="a80d0-110">Click Proposals.</span></span>
6. <span data-ttu-id="a80d0-111">Klik op Bijboekingsvoorstel.</span><span class="sxs-lookup"><span data-stu-id="a80d0-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="a80d0-112">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="a80d0-112">Click Filter.</span></span>
8. <span data-ttu-id="a80d0-113">Klik op Opnieuw instellen om waarden te wissen.</span><span class="sxs-lookup"><span data-stu-id="a80d0-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="a80d0-114">Selecteer de rij Vaste-activanummer.</span><span class="sxs-lookup"><span data-stu-id="a80d0-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="a80d0-115">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a80d0-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="a80d0-116">Stel de resterende criteria in voor de vaste activa die u met dit voorstel wilt bijboeken.</span><span class="sxs-lookup"><span data-stu-id="a80d0-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="a80d0-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a80d0-117">Click OK.</span></span>
12. <span data-ttu-id="a80d0-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a80d0-118">Click OK.</span></span>
    * <span data-ttu-id="a80d0-119">Controleer de gemaakte transactieregels.</span><span class="sxs-lookup"><span data-stu-id="a80d0-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="a80d0-120">Alleen vaste activa waarvoor de verwervingsdatum en aanschafprijs zijn ingesteld in het boek worden in het bijboekingsvoorstel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="a80d0-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="a80d0-121">Klik op het tabblad Boeken.</span><span class="sxs-lookup"><span data-stu-id="a80d0-121">Click the Books tab.</span></span>
14. <span data-ttu-id="a80d0-122">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="a80d0-122">Click Post.</span></span>


