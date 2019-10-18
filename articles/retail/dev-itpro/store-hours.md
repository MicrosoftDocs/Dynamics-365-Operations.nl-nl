---
title: Openingstijden maken en bijwerken
description: In dit onderwerp wordt beschreven hoe u openingstijden kunt maken en bijwerken in Retail Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 811d499a3eb8133e5ffd29bb4ae6a0c57708accd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023437"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="a754c-103">Openingstijden maken en bijwerken</span><span class="sxs-lookup"><span data-stu-id="a754c-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="a754c-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a754c-104">Overview</span></span>

<span data-ttu-id="a754c-105">Vanaf één locatie kunnen detailhandelaren de openingstijden voor verschillende winkels in verschillende geografische regio's maken, onderhouden en beheren.</span><span class="sxs-lookup"><span data-stu-id="a754c-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="a754c-106">De openingstijden kunnen vervolgens worden weergegeven op POS-terminals (Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="a754c-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="a754c-107">Op deze manier kunnen kassamedewerkers openingstijden delen met klanten en kopers die geïnteresseerd zijn in voorraad in andere winkels beter helpen.</span><span class="sxs-lookup"><span data-stu-id="a754c-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="a754c-108">De openingstijden kunnen ook op betalingsbewijzen worden afgedrukt, voor het geval klanten later nog willen terugkeren naar de winkel.</span><span class="sxs-lookup"><span data-stu-id="a754c-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="a754c-109">U kunt meerdere openingstijden configureren via verschillende kanalen.</span><span class="sxs-lookup"><span data-stu-id="a754c-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="a754c-110">Tot deze kanalen behoren fysieke winkels, callcenters, mobiele apparaten en e-Commerce-sites.</span><span class="sxs-lookup"><span data-stu-id="a754c-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="a754c-111">Als een klant een ophaalorder voor een andere winkel heeft, kan de kassamedewerker datums selecteren wanneer het artikel kan worden opgehaald in die winkel.</span><span class="sxs-lookup"><span data-stu-id="a754c-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="a754c-112">Het zoekresultaat van de winkel bevat een verwijzing naar de datums en openingstijden.</span><span class="sxs-lookup"><span data-stu-id="a754c-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="a754c-113">De kassamedewerker kan een datum en locatie selecteren en tevens een ontvangstbewijs van ophalen afdrukken dat de openingstijden van de winkel bevat.</span><span class="sxs-lookup"><span data-stu-id="a754c-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="a754c-114">Deze functionaliteit is beschikbaar in Microsoft Dynamics 365 Retail 8.1.2 en hoger.</span><span class="sxs-lookup"><span data-stu-id="a754c-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="a754c-115">Openingstijden configureren</span><span class="sxs-lookup"><span data-stu-id="a754c-115">Configure store hours</span></span>

<span data-ttu-id="a754c-116">Volg deze stappen om openingstijden te configureren.</span><span class="sxs-lookup"><span data-stu-id="a754c-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="a754c-117">Ga naar **Detailhandel** \> **Afzetkanaalinstellingen** \> **Openingstijden**.</span><span class="sxs-lookup"><span data-stu-id="a754c-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="a754c-118">Selecteer **Nieuw** om een nieuwe sjabloon voor openingstijden te maken.</span><span class="sxs-lookup"><span data-stu-id="a754c-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="a754c-119">Als u een bestaande sjabloon wilt gebruiken, selecteert u de sjabloon in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="a754c-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="a754c-120">Definieer in het dialoogvenster **Bereik toevoegen** het datumbereik, de openingstijden en en eventuele vereiste vrije dagen.</span><span class="sxs-lookup"><span data-stu-id="a754c-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="a754c-121">Als de openingstijden niet veranderen, selecteert u **Nooit beëindigen** in het veld **Einddatum**.</span><span class="sxs-lookup"><span data-stu-id="a754c-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="a754c-122">Als de openingstijden betrekking hebben op een bepaalde maand, week of dag, stelt u de gewenste datums in de velden **Begindatum** en **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="a754c-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a754c-123">U kunt meerdere sjablonen maken met overlappende begin- en einddatums.</span><span class="sxs-lookup"><span data-stu-id="a754c-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="a754c-124">Daarom kunt u bijvoorbeeld openingstijden voor winkels in verschillende tijdzones definiëren.</span><span class="sxs-lookup"><span data-stu-id="a754c-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="a754c-125">![Het dialoogvenster Bereik toevoegen](../dev-itpro/media/Storehours1.png "Het dialoogvenster Bereik toevoegen")</span><span class="sxs-lookup"><span data-stu-id="a754c-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="a754c-126">Koppel de sjabloon voor openingstijden aan de winkels waar deze wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a754c-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="a754c-127">Selecteer in het dialoogvenster **Organisatieknooppunten kiezen** de winkels, regio's en organisaties waaraan de sjabloon moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a754c-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="a754c-128">U kunt slechts één sjabloon voor openingstijden aan elke winkel koppelen.</span><span class="sxs-lookup"><span data-stu-id="a754c-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="a754c-129">Gebruik de pijlknoppen om winkels, regio's of organisaties te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a754c-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="a754c-130">De kalender is beschikbaar voor de winkels of winkelketens en is ter referentie zichtbaar in het POS.</span><span class="sxs-lookup"><span data-stu-id="a754c-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="a754c-131">![Het dialoogvenster Organisatieknooppunten kiezen](../dev-itpro/media/Storehours2.png "Het dialoogvenster Organisatieknooppunten kiezen")</span><span class="sxs-lookup"><span data-stu-id="a754c-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="a754c-132">Voer op de pagina **Distributieplanning** de taken **1070** en **1090** uit om de openingstijden beschikbaar te maken voor het POS.</span><span class="sxs-lookup"><span data-stu-id="a754c-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="a754c-133">Winkeltijden toevoegen aan afgedrukte ontvangstbewijzen</span><span class="sxs-lookup"><span data-stu-id="a754c-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="a754c-134">Voer de volgende stappen uit om openingstijden toe te voegen aan de afgedrukte POS-ontvangstbewijzen.</span><span class="sxs-lookup"><span data-stu-id="a754c-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="a754c-135">Open de functie voor het ontwerpen van ontvangstbewijzen.</span><span class="sxs-lookup"><span data-stu-id="a754c-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="a754c-136">Selecteer **Voettekst** in de linkerbenedenhoek.</span><span class="sxs-lookup"><span data-stu-id="a754c-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="a754c-137">Sleep het element **Winkeltijden** van het linkerdeelvenster naar de voettekst onder aan de sjabloon voor ontvangstbewijzen.</span><span class="sxs-lookup"><span data-stu-id="a754c-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="a754c-138">U kunt het standaardlabel van het element **Openingstijden** naar wens bewerken.</span><span class="sxs-lookup"><span data-stu-id="a754c-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="a754c-139">Sla het ontvangstbewijs op en sluit de ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="a754c-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="a754c-140">Voer op de pagina **Distributieplanning** de taken **1070** en **1090** uit.</span><span class="sxs-lookup"><span data-stu-id="a754c-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="a754c-141">Meld u aan bij het POS.</span><span class="sxs-lookup"><span data-stu-id="a754c-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="a754c-142">Voltooi een verkoop en kis ervoor om een ontvangstbewijs af te drukken.</span><span class="sxs-lookup"><span data-stu-id="a754c-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="a754c-143">POS-ontvangstbewijzen bevatten nu de openingstijden.</span><span class="sxs-lookup"><span data-stu-id="a754c-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="a754c-144">Als de sjabloon feestdagen bevat, worden deze weergegeven op het ontvangstbewijs.</span><span class="sxs-lookup"><span data-stu-id="a754c-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="a754c-145">![Voorbeeld van ontvangstbewijs](../dev-itpro/media/Storehours3.png "Voorbeeld van ontvangstbewijs")</span><span class="sxs-lookup"><span data-stu-id="a754c-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
