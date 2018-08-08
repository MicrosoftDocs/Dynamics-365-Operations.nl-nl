--- 
title: Bankfaciliteiten en boekingsprofielen voor kredietbrief instellen
description: Deze procedure doorloopt het maken van een bankfaciliteit en boekingsprofiel dat vereist is om borgstellingen te verwerken.
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1a4f63f11c0295cd451c6d5d5eb5842217c6e0a6
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="941e0-103">Bankfaciliteiten en boekingsprofielen voor kredietbrief instellen</span><span class="sxs-lookup"><span data-stu-id="941e0-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="941e0-104">Deze procedure doorloopt het maken van een bankfaciliteit en boekingsprofiel dat vereist is om borgstellingen te verwerken.</span><span class="sxs-lookup"><span data-stu-id="941e0-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="941e0-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="941e0-105">This task uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="941e0-106">Grootboekparameter</span><span class="sxs-lookup"><span data-stu-id="941e0-106">General ledger parameter</span></span>
1. <span data-ttu-id="941e0-107">Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.</span><span class="sxs-lookup"><span data-stu-id="941e0-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="941e0-108">Vouw de sectie Bankdocument uit.</span><span class="sxs-lookup"><span data-stu-id="941e0-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="941e0-109">Schakel de optie Importkredietbrief inschakelen in.</span><span class="sxs-lookup"><span data-stu-id="941e0-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="941e0-110">Schakel de optie Exportkredietbrief inschakelen in.</span><span class="sxs-lookup"><span data-stu-id="941e0-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="941e0-111">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="941e0-111">Click Save.</span></span>
6. <span data-ttu-id="941e0-112">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="941e0-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="941e0-113">Bankfaciliteit maken</span><span class="sxs-lookup"><span data-stu-id="941e0-113">Create Bank facility</span></span>
1. <span data-ttu-id="941e0-114">Ga naar Kas- en bankbeheer > Instellingen > Bankfaciliteiten.</span><span class="sxs-lookup"><span data-stu-id="941e0-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="941e0-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="941e0-115">Click New.</span></span>
3. <span data-ttu-id="941e0-116">Voer in het veld Faciliteitsgroep de groepsnaam van de bankfaciliteiten in.</span><span class="sxs-lookup"><span data-stu-id="941e0-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="941e0-117">Voer in het veld Beschrijving de beschrijving in van de bankfaciliteitsgroep.</span><span class="sxs-lookup"><span data-stu-id="941e0-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="941e0-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="941e0-118">Click Save.</span></span>
6. <span data-ttu-id="941e0-119">Klik op het tabblad Faciliteitstypen.</span><span class="sxs-lookup"><span data-stu-id="941e0-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="941e0-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="941e0-120">Click New.</span></span>
8. <span data-ttu-id="941e0-121">Voer in het veld Faciliteittype een unieke code in.</span><span class="sxs-lookup"><span data-stu-id="941e0-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="941e0-122">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="941e0-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="941e0-123">Klik in het veld Faciliteitsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="941e0-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="941e0-124">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="941e0-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="941e0-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="941e0-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="941e0-126">Selecteer in het veld Faciliteitsaard de aard van de bankfaciliteit.</span><span class="sxs-lookup"><span data-stu-id="941e0-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="941e0-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="941e0-127">Click Save.</span></span>
15. <span data-ttu-id="941e0-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="941e0-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="941e0-129">Boekingsprofiel van bank</span><span class="sxs-lookup"><span data-stu-id="941e0-129">Bank posting profile</span></span>
1. <span data-ttu-id="941e0-130">Ga naar Kas- en bankbeheer > Instellingen > Boekingsprofiel van bankdocumenten.</span><span class="sxs-lookup"><span data-stu-id="941e0-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="941e0-131">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="941e0-131">Click New.</span></span>
3. <span data-ttu-id="941e0-132">Klik in het veld Rekening/groepsnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="941e0-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="941e0-133">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="941e0-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="941e0-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="941e0-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="941e0-135">Selecteer de hoofdrekening voor vereffening.</span><span class="sxs-lookup"><span data-stu-id="941e0-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="941e0-136">Deze rekening wordt gebruikt bij de berekening van de cashflowprognose.</span><span class="sxs-lookup"><span data-stu-id="941e0-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="941e0-137">Selecteer in het veld Rekening voor toeslagen de rekening voor onkostentransacties.</span><span class="sxs-lookup"><span data-stu-id="941e0-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="941e0-138">Selecteer in het veld Margerekening de rekening voor margetransacties.</span><span class="sxs-lookup"><span data-stu-id="941e0-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="941e0-139">Deze rekening wordt gedebiteerd wanneer de openingsmarge wordt geboekt en gecrediteerd wanneer de betaling wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="941e0-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="941e0-140">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="941e0-140">Click Save.</span></span>


