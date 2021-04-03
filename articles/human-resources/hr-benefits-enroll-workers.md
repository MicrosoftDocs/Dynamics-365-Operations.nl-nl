---
title: Vergoedingen inschrijven en verwijderen van werknemers
description: Deze procedure toont hoe één medewerker in een of meerdere vergoedingen kan worden geregistreerd en hoe meerdere medewerkers in een vergoeding kunnen worden geregistreerd.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cb56d11cb3acd1e8e39765284269234fc632f17f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465097"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="cac6d-103">Vergoedingen inschrijven en verwijderen van werknemers</span><span class="sxs-lookup"><span data-stu-id="cac6d-103">Enroll and remove benefits from workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="cac6d-104">Deze procedure toont hoe één medewerker in een of meerdere vergoedingen kan worden geregistreerd en hoe meerdere medewerkers in een vergoeding kunnen worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="cac6d-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="cac6d-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="cac6d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="cac6d-106">Eén medewerker voor vergoedingen inschrijven</span><span class="sxs-lookup"><span data-stu-id="cac6d-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="cac6d-107">Ga naar Human resources > Medewerkers > Werknemers.</span><span class="sxs-lookup"><span data-stu-id="cac6d-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="cac6d-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cac6d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cac6d-109">Klik op Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="cac6d-109">Click Benefits.</span></span>
4. <span data-ttu-id="cac6d-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cac6d-110">Click New.</span></span>
5. <span data-ttu-id="cac6d-111">Typ of selecteer een waarde in het veld Vergoeding.</span><span class="sxs-lookup"><span data-stu-id="cac6d-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="cac6d-112">Typ een datum en tijd in het veld Begindatum dekking.</span><span class="sxs-lookup"><span data-stu-id="cac6d-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="cac6d-113">Typ een datum en tijd in het veld Einddatum dekking.</span><span class="sxs-lookup"><span data-stu-id="cac6d-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="cac6d-114">Vouw de sectie Begunstigden uit als u begunstigden moet toevoegen aan de vergoeding.</span><span class="sxs-lookup"><span data-stu-id="cac6d-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="cac6d-115">U kunt ook afhankelijken van deze pagina toevoegen aan de vergoeding, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="cac6d-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="cac6d-116">Op deze pagina kunt u ook de details van een vergoedingsinschrijving bewerken of een inschrijving verwijderen.</span><span class="sxs-lookup"><span data-stu-id="cac6d-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="cac6d-117">Wanneer u klaar bent met wijzigingen aanbrengen aan de inschrijving op vergoedingen, sluit u de pagina.</span><span class="sxs-lookup"><span data-stu-id="cac6d-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="cac6d-118">Meerdere medewerkers voor een vergoeding inschrijven</span><span class="sxs-lookup"><span data-stu-id="cac6d-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="cac6d-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cac6d-119">Close the page.</span></span>
2. <span data-ttu-id="cac6d-120">Ga naar Human resources > Medewerkers > Werknemers.</span><span class="sxs-lookup"><span data-stu-id="cac6d-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="cac6d-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cac6d-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cac6d-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cac6d-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cac6d-123">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cac6d-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="cac6d-124">Klik op Inschrijven voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="cac6d-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="cac6d-125">Typ of selecteer een waarde in het veld Vergoeding.</span><span class="sxs-lookup"><span data-stu-id="cac6d-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="cac6d-126">Typ een datum en tijd in het veld Begindatum dekking.</span><span class="sxs-lookup"><span data-stu-id="cac6d-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="cac6d-127">Typ een datum en tijd in het veld Einddatum dekking.</span><span class="sxs-lookup"><span data-stu-id="cac6d-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="cac6d-128">Klik op Inschrijven.</span><span class="sxs-lookup"><span data-stu-id="cac6d-128">Click Enroll.</span></span>
11. <span data-ttu-id="cac6d-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cac6d-129">Close the page.</span></span>
12. <span data-ttu-id="cac6d-130">Ga naar Human Resources > Vergoedingen > Inschrijving > Resultaten inschrijving op vergoedingen</span><span class="sxs-lookup"><span data-stu-id="cac6d-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="cac6d-131">Zoek de record met resultaten van vergoeding die u zoekt.</span><span class="sxs-lookup"><span data-stu-id="cac6d-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="cac6d-132">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cac6d-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="cac6d-133">Met deze pagina kunt u weergeven welke werknemers in de vergoeding zijn geregistreerd en welke werknemers niet zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="cac6d-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]