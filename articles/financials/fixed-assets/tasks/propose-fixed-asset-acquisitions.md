---
title: Aanschaf van vaste activa voorstellen
description: In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839900"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="f1ba1-103">Aanschaf van vaste activa voorstellen</span><span class="sxs-lookup"><span data-stu-id="f1ba1-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1ba1-104">In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="f1ba1-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f1ba1-106">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="f1ba1-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-107">Select **New**.</span></span>
3. <span data-ttu-id="f1ba1-108">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="f1ba1-109">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="f1ba1-110">Selecteer **Voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="f1ba1-111">Selecteer **Verwervingsvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="f1ba1-112">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-112">Select **Filter**.</span></span> <span data-ttu-id="f1ba1-113">Selecteer **Opnieuw instellen** om eerdere waarden te wissen.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="f1ba1-114">Selecteer de rij **Vaste-activanummer**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="f1ba1-115">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="f1ba1-116">Stel de resterende criteria in voor de vaste activa die u met dit voorstel wilt bijboeken.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="f1ba1-117">Selecteer tweemaal **OK** om het deelvenster af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="f1ba1-118">Controleer de gemaakte transactieregels.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="f1ba1-119">Alleen vaste activa waarvoor de verwervingsdatum en -prijs zijn ingesteld in het boek worden in het verwervingsvoorstel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="f1ba1-120">Selecteer op de pagina het tabblad **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="f1ba1-121">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-121">Select **Post**.</span></span>

