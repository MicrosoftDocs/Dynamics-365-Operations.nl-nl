---
title: Bankfaciliteiten en boekingsprofielen voor borgstellingen instellen
description: Deze taak maakt een bankfaciliteit en boekingsprofiel dat nodig is om een borgstelling te verwerken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976261"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="e4cfd-103">Bankfaciliteiten en boekingsprofielen voor borgstellingen instellen</span><span class="sxs-lookup"><span data-stu-id="e4cfd-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4cfd-104">Deze taak maakt een bankfaciliteit en boekingsprofiel dat nodig is om een borgstelling te verwerken.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="e4cfd-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="e4cfd-106">Grootboekparameter</span><span class="sxs-lookup"><span data-stu-id="e4cfd-106">General ledger parameter</span></span>
1. <span data-ttu-id="e4cfd-107">Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="e4cfd-108">Vouw de sectie Bankdocument uit.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="e4cfd-109">Selecteer de optie Borgstelling inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="e4cfd-110">Klik in het veld Transactiejournaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e4cfd-111">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="e4cfd-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e4cfd-113">Klik op het tabblad Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="e4cfd-114">Nummerreekscode definiëren voor verwijzingen naar borgstellingsnummers en borgstellingstransacties</span><span class="sxs-lookup"><span data-stu-id="e4cfd-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="e4cfd-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-115">Click Save.</span></span>
9. <span data-ttu-id="e4cfd-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="e4cfd-117">Bankfaciliteit maken</span><span class="sxs-lookup"><span data-stu-id="e4cfd-117">Create Bank facility</span></span>
1. <span data-ttu-id="e4cfd-118">Ga naar Kas- en bankbeheer > Instellingen > Bankfaciliteiten.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="e4cfd-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-119">Click New.</span></span>
3. <span data-ttu-id="e4cfd-120">Voer in het veld Faciliteitsgroep de naam in van de bankfaciliteitsgroep voor de borgstellingstransactie.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="e4cfd-121">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e4cfd-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-122">Click Save.</span></span>
6. <span data-ttu-id="e4cfd-123">Klik op het tabblad Faciliteitstypen.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="e4cfd-124">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-124">Click New.</span></span>
8. <span data-ttu-id="e4cfd-125">Voer in het veld Faciliteitstype de naam in van het type bankfaciliteit dat is gekoppeld aan de bankfaciliteitsovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="e4cfd-126">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="e4cfd-127">Klik in het veld Faciliteitsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e4cfd-128">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e4cfd-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e4cfd-130">Selecteer een optie in het veld Faciliteitsaard.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="e4cfd-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-131">Click Save.</span></span>
15. <span data-ttu-id="e4cfd-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="e4cfd-133">Boekingsprofiel van bank</span><span class="sxs-lookup"><span data-stu-id="e4cfd-133">Bank posting profile</span></span>
1. <span data-ttu-id="e4cfd-134">Ga naar Kas- en bankbeheer > Instellingen > Boekingsprofiel van bankdocumenten.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="e4cfd-135">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-135">Click New.</span></span>
3. <span data-ttu-id="e4cfd-136">Klik in het veld Rekening/groepsnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e4cfd-137">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e4cfd-138">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e4cfd-139">Selecteer in het veld Rekening vereffenen de hoofdrekening voor vereffening.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="e4cfd-140">Selecteer in het veld Rekening voor toeslagen de rekening voor onkostentransacties.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="e4cfd-141">Selecteer in het veld Margerekening de rekening voor de margetransactie.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="e4cfd-142">Selecteer in het veld Liquidatierekening de liquiditeitsrekening voor de borgstellingstransactie.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="e4cfd-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-143">Click Save.</span></span>
11. <span data-ttu-id="e4cfd-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-144">Close the page.</span></span>

