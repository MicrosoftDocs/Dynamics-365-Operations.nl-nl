---
title: Consignatie instellen
description: In dit onderwerp wordt uitgelegd hoe u bewerkingen voor inkomende consignatievoorraad configureert.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 24500ff46cc77ca8fa59c0c16427d9f05f33a87e
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="set-up-consignment"></a><span data-ttu-id="62af2-103">Consignatie instellen</span><span class="sxs-lookup"><span data-stu-id="62af2-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62af2-104">In dit onderwerp wordt uitgelegd hoe u bewerkingen voor inkomende consignatievoorraad configureert.</span><span class="sxs-lookup"><span data-stu-id="62af2-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="62af2-105">De consignatievoorraad is de voorraad die eigendom is van een leverancier, maar die op uw locatie is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="62af2-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="62af2-106">Wanneer u klaar bent om de voorraad te verbruiken of te gebruiken, neemt u het eigendom van de voorraad over.</span><span class="sxs-lookup"><span data-stu-id="62af2-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="62af2-107">In dit onderwerp worden de instellingen beschreven die nodig zijn voor consignatieprocessen.</span><span class="sxs-lookup"><span data-stu-id="62af2-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="62af2-108">Meer informatie over consignatieprocessen vindt u in [Consignatie](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="62af2-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="62af2-109">Voorraadeigenaren</span><span class="sxs-lookup"><span data-stu-id="62af2-109">Inventory owners</span></span>
<span data-ttu-id="62af2-110">Om fysieke binnenkomende consignatievoorraad te kunnen registreren, moet u een leverancier/eigenaar definiëren.</span><span class="sxs-lookup"><span data-stu-id="62af2-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="62af2-111">Dit doet u op de pagina **Voorraadeigenaar**.</span><span class="sxs-lookup"><span data-stu-id="62af2-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="62af2-112">Als u een **Leveranciersaccount** selecteert, worden standaardwaarden gegenereerd voor de velden **Naam** en **Eigenaar**.</span><span class="sxs-lookup"><span data-stu-id="62af2-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="62af2-113">De waarde in het veld **Eigenaar** is zichtbaar voor de leverancier. Het kan nuttig zijn om deze waarde te wijzigen, als de namen van uw leveranciersaccounts niet eenvoudig herkenbaar zijn voor externe partijen.</span><span class="sxs-lookup"><span data-stu-id="62af2-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="62af2-114">U kunt de waarde in het veld **Eigenaar** bewerken, maar alleen tot het moment dat u de **Voorraadeigenaar**-record opslaat.</span><span class="sxs-lookup"><span data-stu-id="62af2-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="62af2-115">In het veld **Naam** wordt de naam ingevuld van de partij waaraan de leveranciersaccount is gekoppeld. Deze waarde kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="62af2-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="62af2-116">[![Voorraadeigenaren](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="62af2-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="62af2-117">Traceringsdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="62af2-117">Tracking dimension group</span></span>
<span data-ttu-id="62af2-118">Artikelen die in consignatieprocessen worden gebruikt, moeten zijn gekoppeld aan een **Traceringsdimensiegroep** waarvoor de dimensie **Eigenaar** is ingesteld op **Actief**.</span><span class="sxs-lookup"><span data-stu-id="62af2-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="62af2-119">Voor de dimensie Eigenaar zijn altijd de opties **Fysieke voorraad** en **Financiële voorraad** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="62af2-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="62af2-120">De optie **In behoefteplan opnemen volgens dimensie** is nooit geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="62af2-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="62af2-121">[![Traceringsdimensiegroep](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="62af2-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="62af2-122">Journaal voor wijzigingen aan voorraadeigendom</span><span class="sxs-lookup"><span data-stu-id="62af2-122">Inventory ownership change journal</span></span>
<span data-ttu-id="62af2-123">In het journaal **Wijziging aan voorraadeigendom** wordt de overdracht van eigendom van de consignatievoorraad geregistreerd van de leverancier naar de rechtspersoon die de voorraad gebruikt.</span><span class="sxs-lookup"><span data-stu-id="62af2-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="62af2-124">Net als bij andere voorraadjournaals moet het worden geïdentificeerd met de naam van een voorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="62af2-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="62af2-125">Deze namen maakt u aan op de pagina **Voorraadjournaalnamen**. Het **Journaaltype** moet worden ingesteld op **Wijziging aan eigendom**.</span><span class="sxs-lookup"><span data-stu-id="62af2-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="62af2-126">[![journaal-wijziging-voorraadeigendom](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="62af2-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="62af2-127">Leverancierssamenwerking in consignatieprocessen</span><span class="sxs-lookup"><span data-stu-id="62af2-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="62af2-128">Als uw leveranciers de interface van de leverancierssamenwerking gebruiken, kunnen ze daarmee het verbruik van voorraad op uw locatie volgen.</span><span class="sxs-lookup"><span data-stu-id="62af2-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="62af2-129">Meer informatie over het configureren van leveranciers voor leverancierssamenwerking vindt u in [Beveiliging configureren voor leverancierssamenwerkingsgebruikers](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="62af2-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

