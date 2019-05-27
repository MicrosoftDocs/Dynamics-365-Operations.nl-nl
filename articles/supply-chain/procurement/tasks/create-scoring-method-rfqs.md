---
title: Een scoringsmethode maken voor offerteaanvragen
description: Deze procedure laat zien hoe u een scoringsmethode maakt.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98bcffdf63e20a0a620aa87b44449ce13a5df2fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565272"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="8528f-103">Een scoringsmethode maken voor offerteaanvragen</span><span class="sxs-lookup"><span data-stu-id="8528f-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8528f-104">Deze procedure laat zien hoe u een scoringsmethode maakt.</span><span class="sxs-lookup"><span data-stu-id="8528f-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="8528f-105">Een scoringsmethode is een set van criteria die kan worden gebruikt om biedingen te vergelijken die in antwoord op een offerteaanvraag zijn verzonden.</span><span class="sxs-lookup"><span data-stu-id="8528f-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="8528f-106">Zo kunt u bijvoorbeeld een leverancier beoordelen op vroegere prestaties of beoordelen of het bedrijf milieuvriendelijk is of goed meewerkt, of u kunt biedingen vergelijken op basis van de prijs.</span><span class="sxs-lookup"><span data-stu-id="8528f-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="8528f-107">De scoringsmethode kan als standaardscoringsmethode aan een verzoektype worden gekoppeld voor offerteaanvragen van dat type.</span><span class="sxs-lookup"><span data-stu-id="8528f-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="8528f-108">Deze taken worden meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="8528f-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="8528f-109">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="8528f-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="8528f-110">Ga naar Inkoopbeheer > Instellingen > Offerteaanvraag > Scoringsmethode.</span><span class="sxs-lookup"><span data-stu-id="8528f-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="8528f-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8528f-111">Click New.</span></span>
3. <span data-ttu-id="8528f-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="8528f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8528f-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8528f-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8528f-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8528f-114">Click Save.</span></span>
6. <span data-ttu-id="8528f-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8528f-115">Click New.</span></span>
7. <span data-ttu-id="8528f-116">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="8528f-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="8528f-117">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8528f-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="8528f-118">Deze omschrijving wordt weergegeven samen met de naam van de scoringsmethode wanneer een scoringsmethode is geselecteerd voor een offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="8528f-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="8528f-119">Typ een getal in het veld Bereik van.</span><span class="sxs-lookup"><span data-stu-id="8528f-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="8528f-120">Het bereik beperkt wat de inkoopprofessional als score kan invoeren.</span><span class="sxs-lookup"><span data-stu-id="8528f-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="8528f-121">Wanneer er meerdere scoringscriteria voor een offerteaanvraag zijn, worden de scores die zijn ingevoerd bij elkaar opgeteld en wordt de som beschikbaar gesteld om het vergelijken van biedingen mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="8528f-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="8528f-122">Typ een getal in het veld Bereik tot.</span><span class="sxs-lookup"><span data-stu-id="8528f-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="8528f-123">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8528f-123">Click New.</span></span>
12. <span data-ttu-id="8528f-124">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="8528f-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="8528f-125">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8528f-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="8528f-126">Typ een getal in het veld Bereik van.</span><span class="sxs-lookup"><span data-stu-id="8528f-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="8528f-127">Typ een getal in het veld Bereik tot.</span><span class="sxs-lookup"><span data-stu-id="8528f-127">In the Range to field, enter a number.</span></span>

