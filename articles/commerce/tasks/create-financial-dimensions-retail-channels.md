---
title: Financiële dimensies maken voor detailhandelskanalen en dimensiewaarden configureren voor winkels
description: Deze procedure doorloopt het maken van een financiële dimensie voor een Commerce-kanaal met dimensiewaarden en stappen om waarden van financiële dimensies voor winkels te configureren.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79abb6875e2f5b101410ca004b525c4b881621a2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022132"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="f8c0b-103">Financiële dimensies maken voor detailhandelskanalen en dimensiewaarden configureren voor winkels</span><span class="sxs-lookup"><span data-stu-id="f8c0b-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f8c0b-104">Deze procedure doorloopt het maken van een financiële dimensie voor een Commerce-kanaal met dimensiewaarden en stappen om waarden van financiële dimensies voor winkels te configureren.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="f8c0b-105">Het onderwerp omvat geen andere gerelateerde stappen, zoals het maken van dimensiesets en rekeningstructuren.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="f8c0b-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f8c0b-107">Ga naar Grootboek > Rekeningschema > Dimenies > Financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="f8c0b-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-108">Click New.</span></span>
3. <span data-ttu-id="f8c0b-109">Selecteer 'Commerce-kanalen' in het veld Waarden gebruiken van.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="f8c0b-110">Typ een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="f8c0b-111">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-111">Click Activate.</span></span>
6. <span data-ttu-id="f8c0b-112">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-112">Click Close.</span></span>
7. <span data-ttu-id="f8c0b-113">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-113">Click Activate.</span></span>
8. <span data-ttu-id="f8c0b-114">Klik op Dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-114">Click Dimension values.</span></span>
9. <span data-ttu-id="f8c0b-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-115">Close the page.</span></span>
10. <span data-ttu-id="f8c0b-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-116">Click Save.</span></span>
11. <span data-ttu-id="f8c0b-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-117">Close the page.</span></span>
12. <span data-ttu-id="f8c0b-118">Ga naar Retail en Commerce > Kanalen > Winkels > Alle winkels.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="f8c0b-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f8c0b-120">Schakel de uitbreiding van de sectie Financiële dimensies om.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="f8c0b-121">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-121">Click Edit.</span></span>
16. <span data-ttu-id="f8c0b-122">Klik in het veld Commerce-kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="f8c0b-123">Zoek en selecteer in de lijst de dimensiewaarde voor de winkel die wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="f8c0b-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="f8c0b-125">Klik in het veld Kostenplaats op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="f8c0b-126">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="f8c0b-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="f8c0b-128">Klik in het veld Afdeling op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="f8c0b-129">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="f8c0b-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="f8c0b-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f8c0b-131">Click Save.</span></span>

