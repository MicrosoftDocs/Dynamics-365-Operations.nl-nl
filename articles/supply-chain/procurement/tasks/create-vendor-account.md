---
title: Een leverancierrekening maken
description: Deze procedure laat zien hoe u een leveranciersrekening maakt en een adres en contactgegevens toevoegt.
author: mkirknel
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba585a9bb1a296bbf7181530e151d737bfa22fc2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149591"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="c4ced-103">Een leverancierrekening maken</span><span class="sxs-lookup"><span data-stu-id="c4ced-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4ced-104">Deze procedure laat zien hoe u een leveranciersrekening maakt en een adres en contactgegevens toevoegt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="c4ced-105">De procedure toont niet hoe u alle velden vult voor inkoop- en financiële doelen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="c4ced-106">Voor meer informatie over deze velden leest u de veldbeschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="c4ced-107">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="c4ced-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c4ced-108">Leveranciersrekeningen worden gewoonlijk gemaakt door een inkoop- of debiteurenmedewerker.</span><span class="sxs-lookup"><span data-stu-id="c4ced-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="c4ced-109">Een leverancierrekening maken</span><span class="sxs-lookup"><span data-stu-id="c4ced-109">Create a vendor account</span></span>
1. <span data-ttu-id="c4ced-110">Ga naar **Navigatievenster > Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c4ced-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-111">Click **New**.</span></span>
3. <span data-ttu-id="c4ced-112">Typ een waarde in het veld **Leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="c4ced-113">De waarde kan automatisch worden ingevuld.</span><span class="sxs-lookup"><span data-stu-id="c4ced-113">The value may be populated automatically.</span></span> <span data-ttu-id="c4ced-114">Zo ja, dan kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="c4ced-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="c4ced-115">U kunt leveranciersrekeningen voor een persoon of een organisatie maken.</span><span class="sxs-lookup"><span data-stu-id="c4ced-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="c4ced-116">Dit zal beïnvloeden welke velden beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="c4ced-116">This will affect which fields are available.</span></span> <span data-ttu-id="c4ced-117">In dit voorbeeld wordt een leveranciersrekening voor een organisatie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="c4ced-118">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="c4ced-119">Als de leverancier reeds een geregistreerde partij in uw systeem is kunt u de vervolgkeuzelijst gebruiken en een item in dit veld selecteren. De nieuwe leveranciersrekening neemt dan het adres en de contactgegevens over die al zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="c4ced-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="c4ced-120">Typ of selecteer een waarde in het veld **Groep**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="c4ced-121">De leveranciersgroep wordt gebruikt om leveranciers te groeperen die een van de volgende parameters gemeenschappelijk hebben: betalingsvoorwaarden, vereffeningsperiode, grootboekrekeningen voor voorraadboeking (met inbegrip van de btw-groep), standaardgrootboekrekeningen, productfiltercodes of aanbodprognoseconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="c4ced-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="c4ced-122">Voer in het veld **Aantal werknemers** een getal in.</span><span class="sxs-lookup"><span data-stu-id="c4ced-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="c4ced-123">Typ een waarde in het veld **Organisatienummer**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="c4ced-124">Een adres toevoegen</span><span class="sxs-lookup"><span data-stu-id="c4ced-124">Add an address</span></span>
1. <span data-ttu-id="c4ced-125">Vouw de sectie **Adressen** uit.</span><span class="sxs-lookup"><span data-stu-id="c4ced-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="c4ced-126">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-126">Click **Add**.</span></span>
3. <span data-ttu-id="c4ced-127">Typ of selecteer een waarde in het veld **Doel**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="c4ced-128">U kunt een of meerdere doelen selecteren.</span><span class="sxs-lookup"><span data-stu-id="c4ced-128">You can select one or more purposes.</span></span> <span data-ttu-id="c4ced-129">Deze worden gebruikt om het juiste adres voor een bepaald doel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="c4ced-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="c4ced-130">Als bijvoorbeeld "Factuur" het doel is, wordt dat adres gebruikt wanneer u facturen verzendt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="c4ced-131">Typ een waarde in het veld **Naam of omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="c4ced-132">Typ of selecteer een waarde in het **veld Land/regio**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="c4ced-133">Voer de adresgegevens in.</span><span class="sxs-lookup"><span data-stu-id="c4ced-133">Enter the address details.</span></span> <span data-ttu-id="c4ced-134">Het land/regio dat u hebt geselecteerd bepaalt welke velden u ziet, corresponderend met de adresindeling voor het land/regio.</span><span class="sxs-lookup"><span data-stu-id="c4ced-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="c4ced-135">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="c4ced-136">Contactgegevens toevoegen</span><span class="sxs-lookup"><span data-stu-id="c4ced-136">Add contact information</span></span>
1. <span data-ttu-id="c4ced-137">Vouw de sectie **Contactgegevens** uit.</span><span class="sxs-lookup"><span data-stu-id="c4ced-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="c4ced-138">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-138">Click **Add**.</span></span>
3. <span data-ttu-id="c4ced-139">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="c4ced-140">Selecteer een optie in het veld **Type**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="c4ced-141">Typ een waarde in het veld **Contactnummer/-adres**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="c4ced-142">U kunt het selectievakje Primair inschakelen als dit de primaire contactpersoon is.</span><span class="sxs-lookup"><span data-stu-id="c4ced-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="c4ced-143">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-143">Click **Save**.</span></span>
7. <span data-ttu-id="c4ced-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c4ced-144">Close the page.</span></span>
8. <span data-ttu-id="c4ced-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c4ced-145">Close the page.</span></span>

