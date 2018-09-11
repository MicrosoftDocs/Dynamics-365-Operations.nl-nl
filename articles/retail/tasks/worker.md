--- 
title: " Een medewerker configureren"
description: Deze procedure laat zien hoe u een medewerker detailhandel als een vertegenwoordiger kunt configureren die voor provisie op verkopen in POS aanmerking komt.
author: jblucher
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 51a0809306ebdabbf430350fcdaf1ce6dab1bf4b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="724bd-103"> Een medewerker configureren</span><span class="sxs-lookup"><span data-stu-id="724bd-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="724bd-104">Deze procedure laat zien hoe u een medewerker detailhandel als een vertegenwoordiger kunt configureren die voor provisie op verkopen in POS aanmerking komt.</span><span class="sxs-lookup"><span data-stu-id="724bd-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="724bd-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="724bd-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="724bd-106">Een provisieverkoopgroep voor de medewerker maken</span><span class="sxs-lookup"><span data-stu-id="724bd-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="724bd-107">Ga naar Verkoop en marketing > Provisies > Verkoopgroepen.</span><span class="sxs-lookup"><span data-stu-id="724bd-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="724bd-108">Werknemers kunnen aan een of meerdere verkoopgroepen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="724bd-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="724bd-109">In POS kunt u een willekeurige verkoopgroep kiezen die werknemers bevat uit het adresboek van de opslag.</span><span class="sxs-lookup"><span data-stu-id="724bd-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="724bd-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="724bd-110">Click New.</span></span>
3. <span data-ttu-id="724bd-111">Typ een waarde in het veld Groep.</span><span class="sxs-lookup"><span data-stu-id="724bd-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="724bd-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="724bd-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="724bd-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="724bd-113">Click Save.</span></span>
6. <span data-ttu-id="724bd-114">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="724bd-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="724bd-115">Klik op Vertegenwoordiger.</span><span class="sxs-lookup"><span data-stu-id="724bd-115">Click Sales rep.</span></span>
    * <span data-ttu-id="724bd-116">Een verkoopgroep kan meer dan een werknemer bevatten.</span><span class="sxs-lookup"><span data-stu-id="724bd-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="724bd-117">Provisies kunnen tussen werknemers worden gesplitst op basis van hoe u het provisieaandeel definieert.</span><span class="sxs-lookup"><span data-stu-id="724bd-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="724bd-118">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="724bd-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="724bd-119">Typ een getal in het veld Provisieaandeel.</span><span class="sxs-lookup"><span data-stu-id="724bd-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="724bd-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="724bd-120">Click Save.</span></span>
11. <span data-ttu-id="724bd-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="724bd-121">Close the page.</span></span>
12. <span data-ttu-id="724bd-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="724bd-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="724bd-123">De standaardverkoopgroep toewijzen aan medewerkers</span><span class="sxs-lookup"><span data-stu-id="724bd-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="724bd-124">Ga naar Detailhandel en commerce > Werknemers > Werknemers.</span><span class="sxs-lookup"><span data-stu-id="724bd-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="724bd-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="724bd-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="724bd-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="724bd-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="724bd-127">Klik op het tabblad Detailhandel.</span><span class="sxs-lookup"><span data-stu-id="724bd-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="724bd-128">Een werknemer kan aan een standaardverkoopgroep worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="724bd-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="724bd-129">De standaardverkoopgroep wordt automatisch toegevoegd aan verkoopregels in POS als de optie in het functionaliteitprofiel voor de opslag is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="724bd-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="724bd-130">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="724bd-130">Click Edit.</span></span>
6. <span data-ttu-id="724bd-131">Typ of selecteer een waarde in het veld Standaardgroep.</span><span class="sxs-lookup"><span data-stu-id="724bd-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="724bd-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="724bd-132">Click Save.</span></span>


