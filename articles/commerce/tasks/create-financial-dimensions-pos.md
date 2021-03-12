---
title: " Financiële dimensies maken voor POS-kassa's en dimensiewaarden configureren voor kassa's"
description: Deze procedure doorloopt het maken van financiële dimensies voor verkooppuntregisters (POS) en demonstreert hoe u waarden van financiële dimensies voor registers configureert.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c51c77f4b9f411ae45fb955032aa40cb34738e9a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964765"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="d49d2-103"> Financiële dimensies maken voor POS-kassa's en dimensiewaarden configureren voor kassa's</span><span class="sxs-lookup"><span data-stu-id="d49d2-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d49d2-104">Deze procedure doorloopt het maken van financiële dimensies voor verkooppuntregisters (POS) en demonstreert hoe u waarden van financiële dimensies voor registers configureert.</span><span class="sxs-lookup"><span data-stu-id="d49d2-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="d49d2-105">Deze procedure omvat geen andere gerelateerde stappen, zoals het maken van dimensiesets en rekeningstructuren.</span><span class="sxs-lookup"><span data-stu-id="d49d2-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="d49d2-106">Die taken vindt u in andere onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="d49d2-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="d49d2-107">Deze registratie gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="d49d2-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="d49d2-108">Ga naar Grootboek > Rekeningschema > Dimenies > Financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="d49d2-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="d49d2-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d49d2-109">Click New.</span></span>
3. <span data-ttu-id="d49d2-110">Selecteer een optie in het veld Waarden gebruiken van.</span><span class="sxs-lookup"><span data-stu-id="d49d2-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="d49d2-111">Typ een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="d49d2-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="d49d2-112">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="d49d2-112">Click Activate.</span></span>
6. <span data-ttu-id="d49d2-113">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="d49d2-113">Click Close.</span></span>
7. <span data-ttu-id="d49d2-114">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="d49d2-114">Click Activate.</span></span>
8. <span data-ttu-id="d49d2-115">Klik op Dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="d49d2-115">Click Dimension values.</span></span>
9. <span data-ttu-id="d49d2-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d49d2-116">Close the page.</span></span>
10. <span data-ttu-id="d49d2-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d49d2-117">Click Save.</span></span>
11. <span data-ttu-id="d49d2-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d49d2-118">Close the page.</span></span>
12. <span data-ttu-id="d49d2-119">Ga naar Retail en Commerce > Kanaalinstellingen > POS-instellingen > Kassa's.</span><span class="sxs-lookup"><span data-stu-id="d49d2-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="d49d2-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d49d2-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d49d2-121">Schakel de uitbreiding van de sectie Financiële dimensies om.</span><span class="sxs-lookup"><span data-stu-id="d49d2-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="d49d2-122">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="d49d2-122">Click Edit.</span></span>
16. <span data-ttu-id="d49d2-123">Klik in het veld Terminal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d49d2-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="d49d2-124">Zoek en selecteer in de lijst de dimensiewaarde voor het register dat wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d49d2-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="d49d2-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d49d2-125">Click Save.</span></span>

