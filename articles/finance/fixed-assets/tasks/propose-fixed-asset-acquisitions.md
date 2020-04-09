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
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142726"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="74b76-103">Aanschaf van vaste activa voorstellen</span><span class="sxs-lookup"><span data-stu-id="74b76-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74b76-104">In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="74b76-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="74b76-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="74b76-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="74b76-106">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="74b76-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="74b76-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="74b76-107">Select **New**.</span></span>
3. <span data-ttu-id="74b76-108">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="74b76-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="74b76-109">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="74b76-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="74b76-110">Selecteer **Voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="74b76-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="74b76-111">Selecteer **Verwervingsvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="74b76-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="74b76-112">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="74b76-112">Select **Filter**.</span></span> <span data-ttu-id="74b76-113">Selecteer **Opnieuw instellen** om eerdere waarden te wissen.</span><span class="sxs-lookup"><span data-stu-id="74b76-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="74b76-114">Selecteer de rij **Vaste-activanummer**.</span><span class="sxs-lookup"><span data-stu-id="74b76-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="74b76-115">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="74b76-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="74b76-116">Stel de resterende criteria in voor de vaste activa die u met dit voorstel wilt bijboeken.</span><span class="sxs-lookup"><span data-stu-id="74b76-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="74b76-117">Selecteer tweemaal **OK** om het deelvenster af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="74b76-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="74b76-118">Controleer de gemaakte transactieregels.</span><span class="sxs-lookup"><span data-stu-id="74b76-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="74b76-119">Alleen vaste activa waarvoor de verwervingsdatum en -prijs zijn ingesteld in het boek worden in het verwervingsvoorstel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="74b76-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="74b76-120">Selecteer op de pagina het tabblad **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="74b76-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="74b76-121">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="74b76-121">Select **Post**.</span></span>

