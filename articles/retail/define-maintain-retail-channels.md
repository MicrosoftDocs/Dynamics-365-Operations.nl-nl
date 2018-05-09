---
title: "Detailhandelskanalen definiëren en onderhouden"
description: "Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Microsoft Dynamics 365 for Retail als detailhandelwinkels wordt verwezen. Het bevat informatie over de taken die u vóór en na het opzetten van een detailhandelwinkel moet uitvoeren."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 321673a4294e705587bbd5c1afcaab67de50bad5
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="9f096-104">Detailhandelskanalen definiëren en onderhouden</span><span class="sxs-lookup"><span data-stu-id="9f096-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f096-105">Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Microsoft Dynamics 365 for Retail als detailhandelwinkels wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="9f096-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="9f096-106">Het bevat informatie over de taken die u vóór en na het opzetten van een detailhandelwinkel moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9f096-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="9f096-107">Dynamics 365 for Retail ondersteunt meerdere retailkanalen, zoals onlinewinkels, fysieke winkels en call centers.</span><span class="sxs-lookup"><span data-stu-id="9f096-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="9f096-108">Een fysieke winkel wordt een detailhandelswinkel genoemd.</span><span class="sxs-lookup"><span data-stu-id="9f096-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="9f096-109">Iedere detailhandelwinkel kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="9f096-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="9f096-110">U moet al deze elementen voor een detailhandel instellen voordat u deze maakt.</span><span class="sxs-lookup"><span data-stu-id="9f096-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="9f096-111">Nadat u de detailhandelswinkel hebt gemaakt, wijst u de producten toe die u wilt verkopen.</span><span class="sxs-lookup"><span data-stu-id="9f096-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="9f096-112">U moet ook werknemers, kassa's en klanten aan de winkel toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9f096-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="9f096-113">Tot slot voegt u de nieuwe winkel toe aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="9f096-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="9f096-114">Detailhandelwinkels instellen</span><span class="sxs-lookup"><span data-stu-id="9f096-114">Setting up retail stores</span></span>
<span data-ttu-id="9f096-115">Voordat u een detailhandelswinkel kunt instellen, moet u in Dynamics 365 for Retail enkele vereiste taken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9f096-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="9f096-116">U kunt de detailhandel vervolgens maken en gegevens toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f096-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9f096-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="9f096-117">Prerequisites</span></span>

<span data-ttu-id="9f096-118">Voordat u een detailhandel kunt instellen, moet u enkele vereiste taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="9f096-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="9f096-119">Configureer uw organisatiestructuur en stel de organisatiehiërarchieën in voor detailhandelsassortimenten, aanvulling en rapportage.</span><span class="sxs-lookup"><span data-stu-id="9f096-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="9f096-120">Een magazijn voor de detailhandel instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="9f096-121">Nummerreeksen voor detailhandelwinkels, winkeloverzichten en overzichtboekstukken instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="9f096-122">Parameters voor detailhandel configureren</span><span class="sxs-lookup"><span data-stu-id="9f096-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="9f096-123">De betalingsmethoden instellen die door de winkel worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="9f096-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="9f096-124">Om creditcardtransacties op de POS-kassa's van de detailhandelswinkel te kunnen verwerken, kunt u ook betalingsservices instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="9f096-125">Btw-groepen instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="9f096-126">Detailhandelproducten instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-126">Set up retail products.</span></span> <span data-ttu-id="9f096-127">Als onderdeel van deze taak kunt u ook detailhandelsproducthiërarchieën instellen, productvarianten en productassortimenten.</span><span class="sxs-lookup"><span data-stu-id="9f096-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="9f096-128">Productprijsgroepen instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-128">Set up product price groups.</span></span>
10. <span data-ttu-id="9f096-129">Prijzen voor detailhandelproducten instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-129">Set up retail product pricing.</span></span> <span data-ttu-id="9f096-130">Als onderdeel van deze taak kunt u ook prijscorrecties, kortingen en kortingsperioden instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="9f096-131">Personeelsleden instellen.</span><span class="sxs-lookup"><span data-stu-id="9f096-131">Set up staff members.</span></span> <span data-ttu-id="9f096-132">**Opmerking:** u moet ook de juiste machtigingen aan werknemers toewijzen, zodat ze zich kunnen aanmelden en taken kunnen uitvoeren met het Retail POS-systeem van Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="9f096-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="9f096-133">Configureer de Retail POS-profielen die u aan de winkel wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9f096-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="9f096-134">Deze taak omvat veel andere taken, zoals het opzetten van kassa´s, het instellen van offlineprofielen en ontvangstbewijsindelingen en -profielen.</span><span class="sxs-lookup"><span data-stu-id="9f096-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="9f096-135">Controleer alle taken die in de vereiste taken zijn opgenomen en voer alleen alle taken uit die op u van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="9f096-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="9f096-136">Een detailhandelwinkel instellen</span><span class="sxs-lookup"><span data-stu-id="9f096-136">Set up a retail store</span></span>

<span data-ttu-id="9f096-137">Nadat u de vereiste taken hebt uitgevoerd, voert u deze taken uit voor het instellen van de details voor de detailhandelswinkel:</span><span class="sxs-lookup"><span data-stu-id="9f096-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="9f096-138">Maak een detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="9f096-138">Create a retail store.</span></span>
2.  <span data-ttu-id="9f096-139">Wijs een btw-groep aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="9f096-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="9f096-140">Wijs de geaccepteerde betalingsmethoden aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="9f096-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="9f096-141">Details toevoegen aan de productbeschrijvingen voor producten die u in uw detailhandels aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="9f096-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="9f096-142">U kunt bijvoorbeeld opgemaakte tekst en afbeeldingen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f096-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="9f096-143">Deze gegevens worden weergegeven in verschillende contexten, zoals in de POS-kassa of op afgedrukte labels.</span><span class="sxs-lookup"><span data-stu-id="9f096-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="9f096-144">Voeg de winkel toe aan een organisatiehiërarchie die is bestemd voor **Detailhandelsassortiment**, **Detailhandelsaanvulling** of **Detailhandelsrapportage**.</span><span class="sxs-lookup"><span data-stu-id="9f096-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="9f096-145">Na het instellen van een detailhandelwinkel</span><span class="sxs-lookup"><span data-stu-id="9f096-145">After you set up a retail store</span></span>

<span data-ttu-id="9f096-146">Nadat u de gegevens voor de detailhandelswinkel hebt ingevoerd, voert u deze taken uit om de gegevens van de nieuwe detailhandelswinkel naar Retail POS te verzenden.</span><span class="sxs-lookup"><span data-stu-id="9f096-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="9f096-147">Configureer de POS-kassa's voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="9f096-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="9f096-148">Wijs productassortimenten aan de winkel toe.</span><span class="sxs-lookup"><span data-stu-id="9f096-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="9f096-149">Verwerk assortimenten om de lijst met producten te genereren die in het assortiment zijn opgenomen en om de producten in de detailhandelwinkel beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="9f096-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="9f096-150">Verzend gegevens zoals numerreeksen, hardwareprofielen en POS-schermindelingen naar de Retail POS-kassa´s.</span><span class="sxs-lookup"><span data-stu-id="9f096-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="9f096-151">Publiceer de detailhandelswinkel om winkelgegevens te verzenden naar Retail POS.</span><span class="sxs-lookup"><span data-stu-id="9f096-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="9f096-152">Voer de taken uit om de winkelgegevens naar Retail POS te verzenden.</span><span class="sxs-lookup"><span data-stu-id="9f096-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="9f096-153">Organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="9f096-153">Organization hierarchies</span></span>
<span data-ttu-id="9f096-154">Retail gebruikt organisatiehiërarchieën om detailhandelkanalen structuur te geven.</span><span class="sxs-lookup"><span data-stu-id="9f096-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="9f096-155">Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat.</span><span class="sxs-lookup"><span data-stu-id="9f096-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="9f096-156">Bij het instellen van winkels, kunt u ze toevoegen aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="9f096-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="9f096-157">De winkels delen vervolgens gegevens die wordt gebruikt voor assortimenten, aanvulling en rapportering.</span><span class="sxs-lookup"><span data-stu-id="9f096-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




