---
title: Detailhandelskanalen definiëren en onderhouden
description: Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Dynamics 365 Commerce als winkels wordt verwezen. Het bevat informatie over de taken die u vóór en na het opzetten van een winkel moet uitvoeren.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411294"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="8a8bc-104">Detailhandelskanalen definiëren en onderhouden</span><span class="sxs-lookup"><span data-stu-id="8a8bc-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a8bc-105">Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Dynamics 365 Commerce als winkels wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8a8bc-106">Het bevat informatie over de taken die u vóór en na het opzetten van een winkel moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="8a8bc-107">Commerce ondersteunt meerdere kanalen, zoals online winkels, callcenters en fysieke winkels.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="8a8bc-108">Een fysieke winkel wordt een winkel genoemd.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="8a8bc-109">Iedere winkel kan eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen, en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="8a8bc-110">U moet al deze elementen voor een winkel instellen voordat u deze maakt.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="8a8bc-111">Nadat u de winkel hebt gemaakt, wijst u de producten toe die u wilt verkopen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="8a8bc-112">U moet ook werknemers, kassa's en klanten aan de winkel toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="8a8bc-113">Tot slot voegt u de nieuwe winkel toe aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="8a8bc-114">Winkels instellen</span><span class="sxs-lookup"><span data-stu-id="8a8bc-114">Setting up stores</span></span>

<span data-ttu-id="8a8bc-115">Voordat u een winkel kunt instellen in Commerce, moet u enkele vereiste taken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="8a8bc-116">U kunt de winkel vervolgens maken en gegevens toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8a8bc-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="8a8bc-117">Prerequisites</span></span>

<span data-ttu-id="8a8bc-118">Voordat u een winkel kunt instellen, moet u enkele vereiste taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="8a8bc-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="8a8bc-119">Configureer uw organisatiestructuur en stel de organisatiehiërarchieën in voor detailhandelsassortimenten, aanvulling en rapportage.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="8a8bc-120">Een magazijn voor de winkel instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="8a8bc-121">Nummerreeksen voor winkels, winkeloverzichten en overzichtboekstukken instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="8a8bc-122">Configureer parameters voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="8a8bc-123">De betalingsmethoden instellen die door de winkel worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="8a8bc-124">Om creditcardtransacties op POS-kassa's te kunnen verwerken, kunt u ook betalingsservices instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="8a8bc-125">Btw-groepen instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="8a8bc-126">Stel producten in.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-126">Set up products.</span></span> <span data-ttu-id="8a8bc-127">Als onderdeel van deze taak kunt u ook producthiërarchieën instellen, productvarianten en productassortimenten.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="8a8bc-128">Productprijsgroepen instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-128">Set up product price groups.</span></span>
10. <span data-ttu-id="8a8bc-129">Stel productprijzen in.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-129">Set up product pricing.</span></span> <span data-ttu-id="8a8bc-130">Als onderdeel van deze taak kunt u ook prijscorrecties, kortingen en kortingsperioden instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="8a8bc-131">Personeelsleden instellen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a8bc-132">U moet ook de juiste machtigingen aan werknemers toewijzen, zodat ze zich kunnen aanmelden en taken kunnen uitvoeren met het POS-systeem.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="8a8bc-133">Configureer de POS-profielen die u aan de winkel wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="8a8bc-134">Deze taak omvat veel andere taken, zoals het opzetten van kassa´s, het instellen van offlineprofielen en ontvangstbewijsindelingen en -profielen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="8a8bc-135">Controleer alle taken die in de vereisten zijn opgenomen en voer alleen alle taken uit die op u van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="8a8bc-136">Een winkel instellen</span><span class="sxs-lookup"><span data-stu-id="8a8bc-136">Set up a store</span></span>

<span data-ttu-id="8a8bc-137">Nadat u de vereiste taken hebt uitgevoerd, voert u deze taken uit voor het instellen van de details voor de winkel:</span><span class="sxs-lookup"><span data-stu-id="8a8bc-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="8a8bc-138">Maak een winkel.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-138">Create a store.</span></span>
2. <span data-ttu-id="8a8bc-139">Wijs een btw-groep aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="8a8bc-140">Wijs de geaccepteerde betalingsmethoden aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="8a8bc-141">Details toevoegen aan de productbeschrijvingen voor producten die u in uw winkels aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="8a8bc-142">U kunt bijvoorbeeld opgemaakte tekst en afbeeldingen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="8a8bc-143">Deze gegevens worden weergegeven in verschillende contexten, zoals in de POS-kassa of op afgedrukte labels.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="8a8bc-144">Voeg de winkel toe aan een organisatiehiërarchie die is bestemd voor **Detailhandelsassortiment**, **Detailhandelsaanvulling** of **Detailhandelsrapportage**.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="8a8bc-145">Na het instellen van een winkel</span><span class="sxs-lookup"><span data-stu-id="8a8bc-145">After you set up a store</span></span>

<span data-ttu-id="8a8bc-146">Nadat u de gegevens voor de winkel hebt ingevoerd, voert u deze taken uit om de gegevens van de nieuwe winkel naar POS te verzenden:</span><span class="sxs-lookup"><span data-stu-id="8a8bc-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="8a8bc-147">Configureer de POS-kassa's voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="8a8bc-148">Wijs productassortimenten aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="8a8bc-149">Verwerk assortimenten om de lijst met producten te genereren die in het assortiment zijn opgenomen en om de producten in de winkel beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="8a8bc-150">Verzend gegevens als numerreeksen, hardwareprofielen en POS-schermindelingen naar de POS-kassa's.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="8a8bc-151">Publiceer de winkel om winkelgegevens te verzenden naar POS.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="8a8bc-152">Voer de taken uit om de winkelgegevens naar POS te verzenden.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="8a8bc-153">Organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="8a8bc-153">Organization hierarchies</span></span>

<span data-ttu-id="8a8bc-154">Commerce gebruikt organisatiehiërarchieën om kanalen structuur te geven.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="8a8bc-155">Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="8a8bc-156">Bij het instellen van winkels, kunt u ze toevoegen aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="8a8bc-157">De winkels delen vervolgens gegevens die wordt gebruikt voor assortimenten, aanvulling en rapportering.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="8a8bc-158">Als u de verkoopfunctionaliteit voor Commerce wilt gebruiken, moet de configuratiesleutel voor **Meerdere verzendadressen** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="8a8bc-159">Deze configuratiesleutel kunt u vinden in de **handelsconfiguratiesleutels** onder **Systeembeheer**\> **Instellingen** \> **Licentieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="8a8bc-160">Dit is vereist vanwege verschillende validaties op basis van het afleveradres dat is geconfigureerd op het niveau van de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="8a8bc-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

