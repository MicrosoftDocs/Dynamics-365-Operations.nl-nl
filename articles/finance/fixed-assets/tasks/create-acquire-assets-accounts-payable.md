---
title: Activa vanuit Leveranciers maken en aanschaffen
description: Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb7c92fcab622109b01590d4acadce0d707d3d2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227083"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="390dd-103">Activa vanuit Leveranciers maken en aanschaffen</span><span class="sxs-lookup"><span data-stu-id="390dd-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="390dd-104">Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.</span><span class="sxs-lookup"><span data-stu-id="390dd-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="390dd-105">Het gebruikt de accountant en Leveranciersmedewerker en het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="390dd-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="390dd-106">Parameters voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="390dd-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="390dd-107">Ga in het **navigatievenster** naar **Modules > Vaste activa > Instellingen > Parameters vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="390dd-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="390dd-108">Vouw het sneltabblad **Inkooporders** uit.</span><span class="sxs-lookup"><span data-stu-id="390dd-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="390dd-109">Schakel het selectievakje **Bijboekingen van activa vanuit Inkoop toestaan** in.</span><span class="sxs-lookup"><span data-stu-id="390dd-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="390dd-110">Schakel het selectievakje **Activum maken tijdens boeken van productontvangstbon of factuur** in.</span><span class="sxs-lookup"><span data-stu-id="390dd-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="390dd-111">Een nieuwe leveranciersfactuur maken</span><span class="sxs-lookup"><span data-stu-id="390dd-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="390dd-112">Ga in het **navigatievenster** naar **Modules > Leveranciers > Werkgebieden > Leveranciersfactuurregistratie**.</span><span class="sxs-lookup"><span data-stu-id="390dd-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="390dd-113">Klik op **Nieuwe leveranciersfactuur**.</span><span class="sxs-lookup"><span data-stu-id="390dd-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="390dd-114">Klik in het veld **Factuurrekening** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="390dd-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="390dd-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="390dd-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="390dd-116">Typ een waarde in het veld **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="390dd-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="390dd-117">Voer in het veld **Boekingsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="390dd-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="390dd-118">Klik op **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="390dd-118">Click **Add line**.</span></span>
8. <span data-ttu-id="390dd-119">Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="390dd-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="390dd-120">Of de niet-opgeslagen artikelen of de inkoopcategorieën kunnen worden gebruikt voor bijboeking van vaste activa.</span><span class="sxs-lookup"><span data-stu-id="390dd-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="390dd-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="390dd-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="390dd-122">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="390dd-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="390dd-123">Eén factuurregel maakt slechts één vast activum, ongeacht de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="390dd-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="390dd-124">De waarde van het veld voor de factuurhoeveelheid wordt overgebracht naar de vaste-activahoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="390dd-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="390dd-125">Voer een nummer in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="390dd-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="390dd-126">Vouw het sneltabblad **Regeldetails** uit.</span><span class="sxs-lookup"><span data-stu-id="390dd-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="390dd-127">Klik op het tabblad **Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="390dd-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="390dd-128">Schakel het selectievakje **Een nieuw vast activum maken** in.</span><span class="sxs-lookup"><span data-stu-id="390dd-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="390dd-129">Klik in het veld **Groep vaste activa** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="390dd-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="390dd-130">Selecteer in de lijst de groep vaste activa die moet worden gebruikt als de nieuwe vaste activa worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="390dd-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="390dd-131">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="390dd-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="390dd-132">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="390dd-132">Click **Post**.</span></span> <span data-ttu-id="390dd-133">Het vaste activum wordt gemaakt en bijgeboekt wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="390dd-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]