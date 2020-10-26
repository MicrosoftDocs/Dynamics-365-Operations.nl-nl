---
title: Productvarianten toevoegen aan inkooporder met verschillende gewichten
description: Deze procedure doorloopt de stappen voor het gebruik van variantgewichten om inkooporderregels automatisch te vullen voor elke variant van een product.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c099daf888cb2a1740dda3e860b37f88089c5ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986450"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="8c580-103">Productvarianten toevoegen aan inkooporder met verschillende gewichten</span><span class="sxs-lookup"><span data-stu-id="8c580-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c580-104">Deze procedure doorloopt de stappen voor het gebruik van variantgewichten om inkooporderregels automatisch te vullen voor elke variant van een product.</span><span class="sxs-lookup"><span data-stu-id="8c580-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="8c580-105">Wanneer u de hoeveelheid selecteert van het product dat u wilt aanschaffen, worden inkooporderregels gemaakt voor alle varianten van het product met voorgestelde hoeveelheden op basis van de gewichten die zijn geconfigureerd voor de productvarianten.</span><span class="sxs-lookup"><span data-stu-id="8c580-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="8c580-106">Deze procedure omvat geen stappen voor het configureren van gewichtwaarden voor productdimensies en productvarianten.</span><span class="sxs-lookup"><span data-stu-id="8c580-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="8c580-107">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="8c580-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8c580-108">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="8c580-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8c580-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8c580-109">Click New.</span></span>
3. <span data-ttu-id="8c580-110">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8c580-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8c580-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8c580-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8c580-112">Schakel de uitbreiding van de sectie Algemeen om.</span><span class="sxs-lookup"><span data-stu-id="8c580-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="8c580-113">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8c580-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8c580-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8c580-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8c580-115">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8c580-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8c580-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8c580-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8c580-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8c580-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="8c580-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8c580-118">Click OK.</span></span>
12. <span data-ttu-id="8c580-119">Schakel de uitbreiding van de sectie Regeldetails om.</span><span class="sxs-lookup"><span data-stu-id="8c580-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="8c580-120">Klik op het tabblad Varianten.</span><span class="sxs-lookup"><span data-stu-id="8c580-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="8c580-121">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8c580-121">Click Add line.</span></span>
15. <span data-ttu-id="8c580-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8c580-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="8c580-123">Typ '0140' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="8c580-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="8c580-124">Stel Hoeveelheid in op '1000'.</span><span class="sxs-lookup"><span data-stu-id="8c580-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="8c580-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8c580-125">Click Save.</span></span>

