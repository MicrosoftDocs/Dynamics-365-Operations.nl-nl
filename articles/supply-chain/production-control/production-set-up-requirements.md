---
title: Behoeften voor productie-instellingen
description: Dit artikel informatie over installatievereisten voordat u met Productiebeheer kunt werken.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b5df3c6c776a8dafdcfb3be7e2f273e01d70bcae
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="production-setup-requirements"></a><span data-ttu-id="84418-103">Behoeften voor productie-instellingen</span><span class="sxs-lookup"><span data-stu-id="84418-103">Production setup requirements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="84418-104">Dit artikel informatie over installatievereisten voordat u met Productiebeheer kunt werken.</span><span class="sxs-lookup"><span data-stu-id="84418-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="84418-105">Productiebeheer is geïntegreerd met functies in andere modules.</span><span class="sxs-lookup"><span data-stu-id="84418-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="84418-106">Dankzij deze interconnectiviteit kunt u productieorders wijzigen en ervoor zorgen dat deze automatisch worden bijgewerkt in alle andere betrokken processen en berekeningen in het systeem.</span><span class="sxs-lookup"><span data-stu-id="84418-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="84418-107">De volgende instellingsprocessen zijn vermeld in de volgorde waarin deze horen plaats te vinden.</span><span class="sxs-lookup"><span data-stu-id="84418-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="84418-108">Vereiste basisinstelling in andere modules</span><span class="sxs-lookup"><span data-stu-id="84418-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="84418-109">Voordat u met de module Productiebeheer gaat werken, moet eerst de informatie in de andere modules worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="84418-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="84418-110">Deze instelling bevat de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="84418-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="84418-111">Algemene bedrijfsgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="84418-111">Set up general company information.</span></span>
-   <span data-ttu-id="84418-112">Het grootboek instellen</span><span class="sxs-lookup"><span data-stu-id="84418-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="84418-113">Artikelgroepen definiëren</span><span class="sxs-lookup"><span data-stu-id="84418-113">Define item groups.</span></span>
-   <span data-ttu-id="84418-114">Grootboekrekeningen voor artikelgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="84418-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="84418-115">Stel de voorraadartikeltabel in Voorraadbeheer in.</span><span class="sxs-lookup"><span data-stu-id="84418-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="84418-116">Maak stuklijsten (BOM's) en BOM-versies in Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="84418-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="84418-117">Vereist agenda en broninstelling</span><span class="sxs-lookup"><span data-stu-id="84418-117">Required calendar and resource setup</span></span>
<span data-ttu-id="84418-118">Voordat u Productiebeheer gaat gebruiken, opent u eerst Organisatiebeheer en maakt en definieert u in de volgende volgorde de kalender en bronnen voor bedrijfsactiviteiten:</span><span class="sxs-lookup"><span data-stu-id="84418-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="84418-119">**Werktijdsjablonen** – stel werktijdsjablonen in voor het definiëren van de tijden die beschikbaar zijn voor de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="84418-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="84418-120">**Kalenders** – Instellen van werktijdkalenders voor het definiëren van de dagen van het jaar die beschikbaar zijn voor productieplanning.</span><span class="sxs-lookup"><span data-stu-id="84418-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="84418-121">**Resourcegroepen** – Instellen van resourcegroepen voor het groeperen van de bronnen voor bedrijfsactiviteiten om een overzicht te krijgen van de vrije capaciteit wanneer u de planning uitvoert.</span><span class="sxs-lookup"><span data-stu-id="84418-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="84418-122">U hoeft geen resourcegroepen in te stellen voordat u de bronnen voor bedrijfsactiviteiten instelt.</span><span class="sxs-lookup"><span data-stu-id="84418-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="84418-123">Wij raden u echter aan dat u begrijpt hoe bronnen gegroepeerd worden wanneer u Productiebeheer instelt.</span><span class="sxs-lookup"><span data-stu-id="84418-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="84418-124">**Bronnen** – Instellen van bronnen voor bedrijfsactiviteiten om de bronnen te definiëren die gebruikt worden om het productieproces en capaciteitsplanning te voltooien.</span><span class="sxs-lookup"><span data-stu-id="84418-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="84418-125">Vereiste instelling van productieparameters</span><span class="sxs-lookup"><span data-stu-id="84418-125">Required production parameters setup</span></span>
<span data-ttu-id="84418-126">**Parameters van productiecontrole**– Instellen van de parameters voor de basisproductie om te definiëren hoe het systeem productieorders afhandelt en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="84418-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="84418-127">Definiëren hoe productieorders worden gemaakt, geraamd, gepland en verbruikt.</span><span class="sxs-lookup"><span data-stu-id="84418-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="84418-128">U kunt ook selecteren welke feedback u wilt en hoe de kostprijsboekhouding wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="84418-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="84418-129">Vereiste identificatie van journaalnaam</span><span class="sxs-lookup"><span data-stu-id="84418-129">Required journal name identification</span></span>
<span data-ttu-id="84418-130">**Productiejournaalnamen** – Geef de productiejournaalnamen op die worden gebruikt om transacties te registreren en te boeken.</span><span class="sxs-lookup"><span data-stu-id="84418-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="84418-131">Instelling als u bewerkingen gebruikt</span><span class="sxs-lookup"><span data-stu-id="84418-131">Setup if you use operations</span></span>
<span data-ttu-id="84418-132">Bewerkingen zijn de specifieke activiteiten die nodig zijn om een product te fabriceren.</span><span class="sxs-lookup"><span data-stu-id="84418-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="84418-133">**Notitie:** U moet de typen activiteiten kennen die zijn vereist om het artikel te produceren, en de volgorde en prioriteiten van deze activiteiten.</span><span class="sxs-lookup"><span data-stu-id="84418-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="84418-134">Ook moet u weten welke resources betrokken zijn, en hoeveel.</span><span class="sxs-lookup"><span data-stu-id="84418-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="84418-135">**Bewerkingen** – Stel bewerkingen in voor de taken die moeten worden voltooid om het voltooide artikel te produceren.</span><span class="sxs-lookup"><span data-stu-id="84418-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="84418-136">**Relaties** – Bewerkingsrelaties instellen om de gedetailleerde eigenschappen vast te stellen.</span><span class="sxs-lookup"><span data-stu-id="84418-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="84418-137">Om bewerkingsrelaties te definiëren, klikt u op **Relaties** op de pagina **Bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="84418-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="84418-138">Instelling als u routes gebruikt</span><span class="sxs-lookup"><span data-stu-id="84418-138">Setup if you use routes</span></span>
<span data-ttu-id="84418-139">Als u met routes werkt, moet u bewerkingen definiëren voor elke productieroute die u instelt.</span><span class="sxs-lookup"><span data-stu-id="84418-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="84418-140">De route is het pad dat het artikel van bewerking naar bewerking volgt, van het begin van het productieproces tot aan het einde van het productieproces.</span><span class="sxs-lookup"><span data-stu-id="84418-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="84418-141">**Kostencategorieën**- Stel kostencategorieën in voor het definiëren van de kosten per uur van de opgegeven processen en insteltijden.</span><span class="sxs-lookup"><span data-stu-id="84418-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="84418-142">**Kostengroepen** – Stel kostengroepen in voor het maken en muteren van de verschillende typen kostprijsberekeningen.</span><span class="sxs-lookup"><span data-stu-id="84418-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="84418-143">**Routegroepen**– Stel routegroepen in voor het definiëren van parameters die betrekking op groepen routes hebben.</span><span class="sxs-lookup"><span data-stu-id="84418-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="84418-144">U moet routegroepen instellen vóór het maken van productieroutes.</span><span class="sxs-lookup"><span data-stu-id="84418-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="84418-145">**Routes** - Stel productieroutes in en definieer standaardinstellingen voor het beheer van de planning, kostprijsberekening en prijzen van routebewerkingen en voor het beheer van voortgangsrapportage.</span><span class="sxs-lookup"><span data-stu-id="84418-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="84418-146">**Routes**– Instellen van routeversies voor het inschakelen van artikelvariaties in de productie.</span><span class="sxs-lookup"><span data-stu-id="84418-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="84418-147">Optionele, geavanceerde instellingen</span><span class="sxs-lookup"><span data-stu-id="84418-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="84418-148">**Productiegroepen** – Instellen van productiegroepen voor de totstandbrenging van relaties tussen de productieorder en grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="84418-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="84418-149">De grootboekrekeningen worden gebruikt om orders voor rapportage te boeken of te groeperen.</span><span class="sxs-lookup"><span data-stu-id="84418-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="84418-150">**Productiepools** - Maak productiepools voor het groeperen van productieorders zodat u dringende productieorders kunt verwerken of groepen orders kunt verwijderen en boeken.</span><span class="sxs-lookup"><span data-stu-id="84418-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="84418-151">**Eigenschappen**– Definieer eigenschappen om speciale kenmerken te maken die u aan bronnen kunt toewijzen voor het beheer van de productievolgorde.</span><span class="sxs-lookup"><span data-stu-id="84418-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="84418-152">Deze kenmerken zijn verbonden met het werktijdsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84418-152">These attributes are connected to the working time template.</span></span>





