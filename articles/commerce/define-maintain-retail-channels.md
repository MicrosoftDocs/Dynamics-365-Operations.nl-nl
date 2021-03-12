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
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51524ad6918d962d70a8a700f135f96e236f7d34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000870"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="3f993-104">Detailhandelskanalen definiëren en onderhouden</span><span class="sxs-lookup"><span data-stu-id="3f993-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f993-105">Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Dynamics 365 Commerce als winkels wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="3f993-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3f993-106">Het bevat informatie over de taken die u vóór en na het opzetten van een winkel moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3f993-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="3f993-107">Commerce ondersteunt meerdere kanalen, zoals online winkels, callcenters en fysieke winkels.</span><span class="sxs-lookup"><span data-stu-id="3f993-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="3f993-108">Een fysieke winkel wordt een winkel genoemd.</span><span class="sxs-lookup"><span data-stu-id="3f993-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="3f993-109">Iedere winkel kan eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen, en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="3f993-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="3f993-110">U moet al deze elementen voor een winkel instellen voordat u deze maakt.</span><span class="sxs-lookup"><span data-stu-id="3f993-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="3f993-111">Nadat u de winkel hebt gemaakt, wijst u de producten toe die u wilt verkopen.</span><span class="sxs-lookup"><span data-stu-id="3f993-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="3f993-112">U moet ook werknemers, kassa's en klanten aan de winkel toewijzen.</span><span class="sxs-lookup"><span data-stu-id="3f993-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="3f993-113">Tot slot voegt u de nieuwe winkel toe aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="3f993-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="3f993-114">Winkels instellen</span><span class="sxs-lookup"><span data-stu-id="3f993-114">Setting up stores</span></span>

<span data-ttu-id="3f993-115">Voordat u een winkel kunt instellen in Commerce, moet u enkele vereiste taken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3f993-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="3f993-116">U kunt de winkel vervolgens maken en gegevens toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3f993-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3f993-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3f993-117">Prerequisites</span></span>

<span data-ttu-id="3f993-118">Voordat u een winkel kunt instellen, moet u enkele vereiste taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="3f993-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="3f993-119">Configureer uw organisatiestructuur en stel de organisatiehiërarchieën in voor detailhandelsassortimenten, aanvulling en rapportage.</span><span class="sxs-lookup"><span data-stu-id="3f993-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="3f993-120">Een magazijn voor de winkel instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="3f993-121">Nummerreeksen voor winkels, winkeloverzichten en overzichtboekstukken instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="3f993-122">Configureer parameters voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f993-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="3f993-123">De betalingsmethoden instellen die door de winkel worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="3f993-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="3f993-124">Om creditcardtransacties op POS-kassa's te kunnen verwerken, kunt u ook betalingsservices instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="3f993-125">Btw-groepen instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="3f993-126">Stel producten in.</span><span class="sxs-lookup"><span data-stu-id="3f993-126">Set up products.</span></span> <span data-ttu-id="3f993-127">Als onderdeel van deze taak kunt u ook producthiërarchieën instellen, productvarianten en productassortimenten.</span><span class="sxs-lookup"><span data-stu-id="3f993-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="3f993-128">Productprijsgroepen instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-128">Set up product price groups.</span></span>
10. <span data-ttu-id="3f993-129">Stel productprijzen in.</span><span class="sxs-lookup"><span data-stu-id="3f993-129">Set up product pricing.</span></span> <span data-ttu-id="3f993-130">Als onderdeel van deze taak kunt u ook prijscorrecties, kortingen en kortingsperioden instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="3f993-131">Personeelsleden instellen.</span><span class="sxs-lookup"><span data-stu-id="3f993-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f993-132">U moet ook de juiste machtigingen aan werknemers toewijzen, zodat ze zich kunnen aanmelden en taken kunnen uitvoeren met het POS-systeem.</span><span class="sxs-lookup"><span data-stu-id="3f993-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="3f993-133">Configureer de POS-profielen die u aan de winkel wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="3f993-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="3f993-134">Deze taak omvat veel andere taken, zoals het opzetten van kassa´s, het instellen van offlineprofielen en ontvangstbewijsindelingen en -profielen.</span><span class="sxs-lookup"><span data-stu-id="3f993-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="3f993-135">Controleer alle taken die in de vereisten zijn opgenomen en voer alleen alle taken uit die op u van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="3f993-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="3f993-136">Een winkel instellen</span><span class="sxs-lookup"><span data-stu-id="3f993-136">Set up a store</span></span>

<span data-ttu-id="3f993-137">Nadat u de vereiste taken hebt uitgevoerd, voert u deze taken uit voor het instellen van de details voor de winkel:</span><span class="sxs-lookup"><span data-stu-id="3f993-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="3f993-138">Maak een winkel.</span><span class="sxs-lookup"><span data-stu-id="3f993-138">Create a store.</span></span>
2. <span data-ttu-id="3f993-139">Wijs een btw-groep aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="3f993-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="3f993-140">Wijs de geaccepteerde betalingsmethoden aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="3f993-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="3f993-141">Details toevoegen aan de productbeschrijvingen voor producten die u in uw winkels aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="3f993-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="3f993-142">U kunt bijvoorbeeld opgemaakte tekst en afbeeldingen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3f993-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="3f993-143">Deze gegevens worden weergegeven in verschillende contexten, zoals in de POS-kassa of op afgedrukte labels.</span><span class="sxs-lookup"><span data-stu-id="3f993-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="3f993-144">Voeg de winkel toe aan een organisatiehiërarchie die is bestemd voor **Detailhandelsassortiment**, **Detailhandelsaanvulling** of **Detailhandelsrapportage**.</span><span class="sxs-lookup"><span data-stu-id="3f993-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="3f993-145">Na het instellen van een winkel</span><span class="sxs-lookup"><span data-stu-id="3f993-145">After you set up a store</span></span>

<span data-ttu-id="3f993-146">Nadat u de gegevens voor de winkel hebt ingevoerd, voert u deze taken uit om de gegevens van de nieuwe winkel naar POS te verzenden:</span><span class="sxs-lookup"><span data-stu-id="3f993-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="3f993-147">Configureer de POS-kassa's voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="3f993-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="3f993-148">Wijs productassortimenten aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="3f993-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="3f993-149">Verwerk assortimenten om de lijst met producten te genereren die in het assortiment zijn opgenomen en om de producten in de winkel beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="3f993-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="3f993-150">Verzend gegevens als numerreeksen, hardwareprofielen en POS-schermindelingen naar de POS-kassa's.</span><span class="sxs-lookup"><span data-stu-id="3f993-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="3f993-151">Publiceer de winkel om winkelgegevens te verzenden naar POS.</span><span class="sxs-lookup"><span data-stu-id="3f993-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="3f993-152">Voer de taken uit om de winkelgegevens naar POS te verzenden.</span><span class="sxs-lookup"><span data-stu-id="3f993-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="3f993-153">Organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="3f993-153">Organization hierarchies</span></span>

<span data-ttu-id="3f993-154">Commerce gebruikt organisatiehiërarchieën om kanalen structuur te geven.</span><span class="sxs-lookup"><span data-stu-id="3f993-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="3f993-155">Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat.</span><span class="sxs-lookup"><span data-stu-id="3f993-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="3f993-156">Bij het instellen van winkels, kunt u ze toevoegen aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="3f993-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="3f993-157">De winkels delen vervolgens gegevens die wordt gebruikt voor assortimenten, aanvulling en rapportering.</span><span class="sxs-lookup"><span data-stu-id="3f993-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="3f993-158">Als u de verkoopfunctionaliteit voor Commerce wilt gebruiken, moet de configuratiesleutel voor **Meerdere verzendadressen** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3f993-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="3f993-159">Deze configuratiesleutel kunt u vinden in de **handelsconfiguratiesleutels** onder **Systeembeheer**\> **Instellingen** \> **Licentieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="3f993-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="3f993-160">Dit is vereist vanwege verschillende validaties op basis van het afleveradres dat is geconfigureerd op het niveau van de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="3f993-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

