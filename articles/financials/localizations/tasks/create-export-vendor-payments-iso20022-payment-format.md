--- 
title: Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling
description: In deze procedure ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5787edc4a041e4b571c7ab6f056f4bd0a17cf2d7
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="f135d-103">Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling</span><span class="sxs-lookup"><span data-stu-id="f135d-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f135d-104">In deze procedure ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="f135d-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="f135d-105">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.</span><span class="sxs-lookup"><span data-stu-id="f135d-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="f135d-106">Dit is de vijfde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="f135d-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f135d-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f135d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="f135d-108">Betalingsregels maken</span><span class="sxs-lookup"><span data-stu-id="f135d-108">Create payment lines</span></span>
1. <span data-ttu-id="f135d-109">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="f135d-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f135d-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f135d-110">Click New.</span></span>
3. <span data-ttu-id="f135d-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f135d-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f135d-112">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f135d-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="f135d-113">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="f135d-113">Click Lines.</span></span>
6. <span data-ttu-id="f135d-114">Klik op Betalingsvoorstel.</span><span class="sxs-lookup"><span data-stu-id="f135d-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="f135d-115">Klik op Betalingsvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="f135d-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="f135d-116">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="f135d-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="f135d-117">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="f135d-117">Click Filter.</span></span>
10. <span data-ttu-id="f135d-118">Selecteer in de lijst de rij voor de tabel Leveranciers en het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="f135d-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="f135d-119">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="f135d-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="f135d-120">U kunt willekeurige criteria toepassen om van leverancierstransacties te selecteren; gebruik in dit voorbeeldgebruik DE-001 als leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="f135d-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="f135d-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f135d-121">Click OK.</span></span>
13. <span data-ttu-id="f135d-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f135d-122">Click OK.</span></span>
14. <span data-ttu-id="f135d-123">Klik op Betalingen maken.</span><span class="sxs-lookup"><span data-stu-id="f135d-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="f135d-124">Een ISO20022-betalingsbestand genereren</span><span class="sxs-lookup"><span data-stu-id="f135d-124">Generate an ISO20022 payment file</span></span>


