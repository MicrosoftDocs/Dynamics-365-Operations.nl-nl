---
title: Aanschaf van vaste activa voorstellen
description: In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205023"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="fbf3c-103">Aanschaf van vaste activa voorstellen</span><span class="sxs-lookup"><span data-stu-id="fbf3c-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbf3c-104">In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="fbf3c-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="fbf3c-106">Als u een vast activum via een voorsteljournaal voor vaste activa wilt verkrijgen, moet u eerst de record voor de vaste activa maken en vervolgens de aanschafprijs definiëren in het activaboek.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="fbf3c-107">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="fbf3c-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-108">Select **New**.</span></span>
3. <span data-ttu-id="fbf3c-109">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="fbf3c-110">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="fbf3c-111">Selecteer **Voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="fbf3c-112">Selecteer **Verwervingsvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="fbf3c-113">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-113">Select **Filter**.</span></span> <span data-ttu-id="fbf3c-114">Selecteer **Opnieuw instellen** om eerdere waarden te wissen.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="fbf3c-115">Selecteer de rij **Vaste-activanummer**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="fbf3c-116">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="fbf3c-117">Stel de resterende criteria in voor de vaste activa die u met dit voorstel wilt bijboeken.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="fbf3c-118">Selecteer tweemaal **OK** om het deelvenster af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="fbf3c-119">Controleer de gemaakte transactieregels.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="fbf3c-120">Alleen vaste activa waarvoor de verwervingsdatum en -prijs zijn ingesteld in het boek worden in het verwervingsvoorstel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="fbf3c-121">Selecteer op de pagina het tabblad **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="fbf3c-122">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]