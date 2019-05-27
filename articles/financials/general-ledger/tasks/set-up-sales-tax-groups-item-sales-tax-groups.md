---
title: Btw-groepen en artikel-btw-groepen instellen
description: Deze taakregistratie doorloopt de instelling van btw-groepen en btw-groepen voor artikelen.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec5bbe37aa06f18172c417e903538cadc8a6f312
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559406"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="83ba0-103">Btw-groepen en artikel-btw-groepen instellen</span><span class="sxs-lookup"><span data-stu-id="83ba0-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83ba0-104">Deze taakregistratie doorloopt de instelling van btw-groepen en btw-groepen voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="83ba0-105">Btw-groepen zijn groepen met btw-codes die worden gekoppeld klanten en leveranciers.</span><span class="sxs-lookup"><span data-stu-id="83ba0-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="83ba0-106">Deze worden ook gekoppeld aan grootboekrekeningen voor transacties die niet worden geboekt naar een specifieke leverancier of klant.</span><span class="sxs-lookup"><span data-stu-id="83ba0-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="83ba0-107">Btw-groepen voor artikelen zijn groepen met btw-codes die worden gekoppeld aan bronnen zoals producten.</span><span class="sxs-lookup"><span data-stu-id="83ba0-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="83ba0-108">De btw die van toepassing is op een bepaalde transactie, wordt bepaald door de btw-codes die zijn opgenomen in zowel de btw-groep als de btw-groep voor artikel van de transactie.</span><span class="sxs-lookup"><span data-stu-id="83ba0-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="83ba0-109">Btw kan alleen worden berekend als een btw-groep en een btw-groep voor artikelen zijn geselecteerd voor elke transactie waarvoor u de btw wilt berekenen of vastleggen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="83ba0-110">Ga naar Btw > Indirecte belastingen > Btw > Btw-groepen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="83ba0-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="83ba0-111">Click New.</span></span>
3. <span data-ttu-id="83ba0-112">Typ een waarde in het veld Btw-groep.</span><span class="sxs-lookup"><span data-stu-id="83ba0-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="83ba0-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="83ba0-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83ba0-114">Schakel de uitbreiding van de sectie Instelling om.</span><span class="sxs-lookup"><span data-stu-id="83ba0-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="83ba0-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-115">Click Add.</span></span>
7. <span data-ttu-id="83ba0-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="83ba0-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="83ba0-117">Klik in het veld Btw-code op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="83ba0-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="83ba0-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="83ba0-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="83ba0-119">Click Save.</span></span>
11. <span data-ttu-id="83ba0-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="83ba0-120">Close the page.</span></span>
12. <span data-ttu-id="83ba0-121">Ga naar Btw > Indirecte belastingen > Btw > Btw-groepen voor artikel.</span><span class="sxs-lookup"><span data-stu-id="83ba0-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="83ba0-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="83ba0-122">Click New.</span></span>
14. <span data-ttu-id="83ba0-123">Typ een waarde in het veld Btw-groep voor artikel.</span><span class="sxs-lookup"><span data-stu-id="83ba0-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="83ba0-124">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="83ba0-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="83ba0-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-125">Click Add.</span></span>
17. <span data-ttu-id="83ba0-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="83ba0-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="83ba0-127">Klik in het veld Btw-code op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="83ba0-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="83ba0-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="83ba0-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="83ba0-129">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="83ba0-129">Click Save.</span></span>

