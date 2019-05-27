---
title: Aanvraagtypen en scoringscriteria maken voor offerteaanvragen
description: Deze handleiding laat zien hoe u een verzoektype kunt maken en dit kunt koppelen aan een scoringsmethode.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14fd7d0bfa17427883f97c5e0a72044016d4965e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552573"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="16abb-103">Aanvraagtypen en scoringscriteria maken voor offerteaanvragen</span><span class="sxs-lookup"><span data-stu-id="16abb-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16abb-104">Deze handleiding laat zien hoe u een verzoektype kunt maken en dit kunt koppelen aan een scoringsmethode.</span><span class="sxs-lookup"><span data-stu-id="16abb-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="16abb-105">Er wordt tevens weergegeven hoe u het verzoektype kunt gebruiken in een offerteaanvraag, waarbij vervolgens de standaardscoringsmethode wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="16abb-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="16abb-106">Deze taken worden meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="16abb-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="16abb-107">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="16abb-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="16abb-108">U moet over een scoringsmethode beschikken voordat u van start gaat.</span><span class="sxs-lookup"><span data-stu-id="16abb-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="16abb-109">Een nieuw verzoektype maken</span><span class="sxs-lookup"><span data-stu-id="16abb-109">Create a solicitation type</span></span>
1. <span data-ttu-id="16abb-110">Ga naar Inkoopbeheer > Instellingen > Offerteaanvraag > Sollicitatietype.</span><span class="sxs-lookup"><span data-stu-id="16abb-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="16abb-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="16abb-111">Click New.</span></span>
3. <span data-ttu-id="16abb-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="16abb-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="16abb-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="16abb-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="16abb-114">Selecteer in het veld Scoringsmethod de scoringsmethode die u wilt gebruiken voor dit verzoektype.</span><span class="sxs-lookup"><span data-stu-id="16abb-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="16abb-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="16abb-115">Click Save.</span></span>
7. <span data-ttu-id="16abb-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="16abb-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="16abb-117">Het verzoektype gebruiken</span><span class="sxs-lookup"><span data-stu-id="16abb-117">Use the solicitation type</span></span>
1. <span data-ttu-id="16abb-118">Ga naar Inkoop en sourcing > Offerteaanvragen > Alle offerteaanvragen.</span><span class="sxs-lookup"><span data-stu-id="16abb-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="16abb-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="16abb-119">Click New.</span></span>
3. <span data-ttu-id="16abb-120">Selecteer in het veld Verzoektype het verzoektype dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="16abb-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="16abb-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="16abb-121">Click OK.</span></span>
5. <span data-ttu-id="16abb-122">Klik op Scoringscriteria.</span><span class="sxs-lookup"><span data-stu-id="16abb-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="16abb-123">De scoringscriteria die worden weergegeven zijn afkomstig van de scoringsmethode die u aan het verzoektype hebt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="16abb-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="16abb-124">U kunt ervoor kiezen criteria toe te voegen of te verwijderen op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="16abb-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="16abb-125">Het is ook mogelijk om nieuwe criteria toe te voegen door deze vanuit andere scoringsmethoden te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="16abb-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="16abb-126">Klik op Criteria kopiëren.</span><span class="sxs-lookup"><span data-stu-id="16abb-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="16abb-127">Typ of selecteer een waarde in het veld Scoringsmethode.</span><span class="sxs-lookup"><span data-stu-id="16abb-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="16abb-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="16abb-128">Click OK.</span></span>
9. <span data-ttu-id="16abb-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="16abb-129">Close the page.</span></span>

