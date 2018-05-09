--- 
title: " Financiële dimensies maken voor POS-kassa's en dimensiewaarden configureren voor kassa's"
description: "Deze procedure doorloopt het maken van financiële dimensies voor verkooppuntregisters (POS) en demonstreert hoe u waarden van financiële dimensies voor registers configureert."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 33e0b1da5d16372b8a3c4cd153f451166af6003f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="b1fbe-103"> Financiële dimensies maken voor POS-kassa's en dimensiewaarden configureren voor kassa's</span><span class="sxs-lookup"><span data-stu-id="b1fbe-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b1fbe-104">Deze procedure doorloopt het maken van financiële dimensies voor verkooppuntregisters (POS) en demonstreert hoe u waarden van financiële dimensies voor registers configureert.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="b1fbe-105">Deze procedure omvat geen andere gerelateerde stappen, zoals het maken van dimensiesets en rekeningstructuren.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="b1fbe-106">Die taken vindt u in andere onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="b1fbe-107">Deze registratie gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="b1fbe-108">Ga naar Grootboek > Rekeningschema > Dimenies > Financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="b1fbe-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-109">Click New.</span></span>
3. <span data-ttu-id="b1fbe-110">Selecteer een optie in het veld Waarden gebruiken van.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="b1fbe-111">Typ een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="b1fbe-112">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-112">Click Activate.</span></span>
6. <span data-ttu-id="b1fbe-113">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-113">Click Close.</span></span>
7. <span data-ttu-id="b1fbe-114">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-114">Click Activate.</span></span>
8. <span data-ttu-id="b1fbe-115">Klik op Dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-115">Click Dimension values.</span></span>
9. <span data-ttu-id="b1fbe-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-116">Close the page.</span></span>
10. <span data-ttu-id="b1fbe-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-117">Click Save.</span></span>
11. <span data-ttu-id="b1fbe-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-118">Close the page.</span></span>
12. <span data-ttu-id="b1fbe-119">Ga naar Detailhandel en commerce > Kanaalinstellingen > POS-instellingen > Kassa´s.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="b1fbe-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b1fbe-121">Schakel de uitbreiding van de sectie Financiële dimensies om.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="b1fbe-122">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-122">Click Edit.</span></span>
16. <span data-ttu-id="b1fbe-123">Klik in het veld Terminal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b1fbe-124">Zoek en selecteer in de lijst de dimensiewaarde voor het register dat wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="b1fbe-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b1fbe-125">Click Save.</span></span>


