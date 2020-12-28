---
title: Een medewerker configureren
description: Deze procedure laat zien hoe u een medewerker als een vertegenwoordiger kunt configureren die voor provisie op verkopen in POS aanmerking komt.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd437f549ffc1f8879ce3814ace1193040b280e1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411466"
---
# <a name="configure-a-worker"></a><span data-ttu-id="efdcf-103">Een medewerker configureren</span><span class="sxs-lookup"><span data-stu-id="efdcf-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efdcf-104">Deze procedure laat zien hoe u een medewerker als een vertegenwoordiger kunt configureren die voor provisie op verkopen in POS aanmerking komt.</span><span class="sxs-lookup"><span data-stu-id="efdcf-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="efdcf-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="efdcf-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="efdcf-106">Een provisieverkoopgroep voor de medewerker maken</span><span class="sxs-lookup"><span data-stu-id="efdcf-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="efdcf-107">Ga naar Verkoop en marketing > Provisies > Verkoopgroepen.</span><span class="sxs-lookup"><span data-stu-id="efdcf-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="efdcf-108">Werknemers kunnen aan een of meerdere verkoopgroepen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="efdcf-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="efdcf-109">In POS kunt u een willekeurige verkoopgroep kiezen die werknemers bevat uit het adresboek van de opslag.</span><span class="sxs-lookup"><span data-stu-id="efdcf-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="efdcf-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="efdcf-110">Click New.</span></span>
3. <span data-ttu-id="efdcf-111">Typ een waarde in het veld Groep.</span><span class="sxs-lookup"><span data-stu-id="efdcf-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="efdcf-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="efdcf-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="efdcf-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="efdcf-113">Click Save.</span></span>
6. <span data-ttu-id="efdcf-114">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="efdcf-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="efdcf-115">Klik op Vertegenwoordiger.</span><span class="sxs-lookup"><span data-stu-id="efdcf-115">Click Sales rep.</span></span>
    * <span data-ttu-id="efdcf-116">Een verkoopgroep kan meer dan een werknemer bevatten.</span><span class="sxs-lookup"><span data-stu-id="efdcf-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="efdcf-117">Provisies kunnen tussen werknemers worden gesplitst op basis van hoe u het provisieaandeel definieert.</span><span class="sxs-lookup"><span data-stu-id="efdcf-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="efdcf-118">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="efdcf-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="efdcf-119">Typ een getal in het veld Provisieaandeel.</span><span class="sxs-lookup"><span data-stu-id="efdcf-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="efdcf-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="efdcf-120">Click Save.</span></span>
11. <span data-ttu-id="efdcf-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="efdcf-121">Close the page.</span></span>
12. <span data-ttu-id="efdcf-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="efdcf-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="efdcf-123">De standaardverkoopgroep toewijzen aan medewerkers</span><span class="sxs-lookup"><span data-stu-id="efdcf-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="efdcf-124">Ga naar Detailhandel en commerce > Werknemers > Werknemers.</span><span class="sxs-lookup"><span data-stu-id="efdcf-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="efdcf-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="efdcf-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="efdcf-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="efdcf-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="efdcf-127">Klik op het tabblad Commerce.</span><span class="sxs-lookup"><span data-stu-id="efdcf-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="efdcf-128">Een werknemer kan aan een standaardverkoopgroep worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="efdcf-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="efdcf-129">De standaardverkoopgroep wordt automatisch toegevoegd aan verkoopregels in POS als de optie in het functionaliteitprofiel voor de opslag is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="efdcf-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="efdcf-130">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="efdcf-130">Click Edit.</span></span>
6. <span data-ttu-id="efdcf-131">Typ of selecteer een waarde in het veld Standaardgroep.</span><span class="sxs-lookup"><span data-stu-id="efdcf-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="efdcf-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="efdcf-132">Click Save.</span></span>

