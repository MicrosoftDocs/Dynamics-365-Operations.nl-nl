---
title: Werkbelastingcapaciteit magazijn
description: In dit onderwerp wordt uitgelegd hoe u de werkbelastingcapaciteit voor werknemers in een magazijn of voor een geheel magazijn kunt instellen en plannen.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4eac4838a4df8f1f5863f1ce1895e7aded5fb08b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239273"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="865ac-103">Werkbelastingcapaciteit plannen</span><span class="sxs-lookup"><span data-stu-id="865ac-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="865ac-104">U kunt de werkbelastingcapaciteit voor magazijnen plannen, en tevens kunt u de huidige en toekomstige werkbelasting voor de werknemers in individuele magazijnen voorstellen.</span><span class="sxs-lookup"><span data-stu-id="865ac-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="865ac-105">U kunt de werkbelasting voor het hele magazijn opstellen of u kunt de werkbelasting apart voor inkomende en uitgaande werkbelasting opstellen.</span><span class="sxs-lookup"><span data-stu-id="865ac-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="865ac-106">Om de werkbelastingsuitvoer voor geselecteerde magazijnen te voorspellen, moeten de hoofdplanningsgegevens beschikbaar zijn voor die magazijnen.</span><span class="sxs-lookup"><span data-stu-id="865ac-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="865ac-107">Zie voor meer informatie [Overzicht van Hoofdplannen](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="865ac-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="865ac-108">Planning en weergave werklast voor een magazijn</span><span class="sxs-lookup"><span data-stu-id="865ac-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="865ac-109">Voor het plannen van de werkbelastingscapaciteit voor een magazijn, kunt u een werkbelasting instellen voor een of meerdere magazijnen en de werkbelastingsinstelling koppelen aan een hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="865ac-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="865ac-110">In de werkbelastingcapaciteitsinstellingen kunt u beperkingen definiëren voor het gewicht of volume voor inkomende en uitgaande transacties.</span><span class="sxs-lookup"><span data-stu-id="865ac-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="865ac-111">U kunt ook meerdere instellingen voor elk magazijn maken en de instelling vervolgens koppelen aan afzonderlijke hoofplanningen.</span><span class="sxs-lookup"><span data-stu-id="865ac-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="865ac-112">U kunt deze aanpak bijvoorbeeld gebruiken om te voldoen aan seizoensgebonden wijzigingen in het personeelsbestand.</span><span class="sxs-lookup"><span data-stu-id="865ac-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="865ac-113">Als de werknemers voor een magazijn werken met transacties voor zowel inkomende als uitgaande werkbelasting, kunt u de instellingen voor de magazijncapaciteit zo configureren dat de werkbelasting in een gecombineerde weergave wordt voorspeld.</span><span class="sxs-lookup"><span data-stu-id="865ac-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="865ac-114">Als u werkbelasting voor magazijnen wilt plannen en bekijken, moet u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="865ac-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="865ac-115">Instellingen voor werkbelastingscapaciteit maken en de beperkingen van de werkbelastingscapaciteit voor een of meerdere magazijnen opgeven.</span><span class="sxs-lookup"><span data-stu-id="865ac-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="865ac-116">Koppel de instellingen voor de werkbelastingcapaciteit aan een hoofdplan om werkbelastingvoorspellingen te maken en aan te geven hoe lang de voorspellingen van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="865ac-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="865ac-117">Instellingen werkbelastingscapaciteit voor een magazijn maken</span><span class="sxs-lookup"><span data-stu-id="865ac-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="865ac-118">Selecteer **Voorraadbeheer** \> **Instellen** \> **Magazijnbewaking** \> **Werkbelastingcapaciteit**.</span><span class="sxs-lookup"><span data-stu-id="865ac-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="865ac-119">Selecteer in het actievenster **Nieuw** om instellingen voor werkbelastingcapaciteit te maken.</span><span class="sxs-lookup"><span data-stu-id="865ac-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="865ac-120">Selecteer op het sneltabblad **Magazijnen** de optie **Nieuw** en voer waarden op de regel in om een magazijn te koppelen aan de instellingen voor werkbelastingcapaciteit.</span><span class="sxs-lookup"><span data-stu-id="865ac-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="865ac-121">Schakel het selectievakje **Gecombineerde inkomende en uitgaande werkbelasting** in als in het rapport **Werkbelastingcapaciteit** de totale werkbelasting voor inkomende en uitgaande transacties in één weergave moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="865ac-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="865ac-122">Selecteer op het sneltabblad **Transactietypen** de typen inkomende en uitgaande transacties waarop de werkbelastingslimieten van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="865ac-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="865ac-123">U moet ten minste één transactietype voor zowel de inkomende als uitgaande werkbelasting selecteren.</span><span class="sxs-lookup"><span data-stu-id="865ac-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="865ac-124">Limieten voor volume of gewicht definiëren</span><span class="sxs-lookup"><span data-stu-id="865ac-124">Define limits for volume or weight</span></span>

<span data-ttu-id="865ac-125">U kunt limieten voor volume of gewicht instellen, afhankelijk van de beperking die relevant is voor het personeel van het magazijn.</span><span class="sxs-lookup"><span data-stu-id="865ac-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="865ac-126">De limieten die u opgeeft, worden opgenomen in de voorspelling van de werkbelastingcapaciteit die u kunt bekijken in het rapport **Werkbelastingcapaciteit**.</span><span class="sxs-lookup"><span data-stu-id="865ac-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="865ac-127">Om informatie over volume en gewicht voor artikelen te voorspellen, moet het standaardvolume van één vooraadartikel en het gewicht van één vooraadartikel worden opgegeven voor alle producten.</span><span class="sxs-lookup"><span data-stu-id="865ac-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="865ac-128">De velden die vereist, zijn beschikbaar in de volgende veldgroepen op het sneltabblad **Voorraad beheren** van de pagina **Vrijgegeven productdetails**:</span><span class="sxs-lookup"><span data-stu-id="865ac-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="865ac-129">Verwerking</span><span class="sxs-lookup"><span data-stu-id="865ac-129">Handling</span></span>
- <span data-ttu-id="865ac-130">Fysieke afmetingen</span><span class="sxs-lookup"><span data-stu-id="865ac-130">Physical dimensions</span></span>
- <span data-ttu-id="865ac-131">Gewichtsmaten</span><span class="sxs-lookup"><span data-stu-id="865ac-131">Weight measurements</span></span>

<span data-ttu-id="865ac-132">Als deze informatie niet correct wordt opgegeven, ontvangt u een bericht als u het rapport **Werkbelastingcapaciteit** genereert.</span><span class="sxs-lookup"><span data-stu-id="865ac-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="865ac-133">Vanuit het rapport kunt u vervolgens inzoomen om de ontbrekende informatie te identificeren die is vereist om de toekomstige werkbelasting te voorspellen.</span><span class="sxs-lookup"><span data-stu-id="865ac-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="865ac-134">Instelling werkbelastingscapaciteit aan een hoofdplan koppelen</span><span class="sxs-lookup"><span data-stu-id="865ac-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="865ac-135">Selecteer **Voorraadbeheer** \> **Periodiek** \> **Werkbelasting plannen**.</span><span class="sxs-lookup"><span data-stu-id="865ac-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="865ac-136">Selecteer in het veld **Hoofdplan** het hoofdplan dat moet worden gebruikt voor werkbelastingvoorspellingen.</span><span class="sxs-lookup"><span data-stu-id="865ac-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="865ac-137">Geef in het veld **Aantal dagen** het aantal dagen op waarop de werkbelastingvoorspelling betrekking heeft.</span><span class="sxs-lookup"><span data-stu-id="865ac-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="865ac-138">Selecteer in het veld **Werkbelasting** de werkbelastingsinstelling die moet worden gekoppeld aan het hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="865ac-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="865ac-139">Werkbelastingscapaciteit bekijken</span><span class="sxs-lookup"><span data-stu-id="865ac-139">View workload capacity</span></span>

1. <span data-ttu-id="865ac-140">Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Fysieke-voorraadrapporten** \> **Werkbelastingcapaciteit**.</span><span class="sxs-lookup"><span data-stu-id="865ac-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="865ac-141">Geef in het veld **Aantal kolommen** het aantal kolommen op dat moet worden weergegeven in het rapport.</span><span class="sxs-lookup"><span data-stu-id="865ac-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="865ac-142">Selecteer in het veld **Ordertype** **Gepland en bevestigd**, **Gepland** of **Bevestigd** om het type orders aan te geven dat moet worden voorspeld in het rapport.</span><span class="sxs-lookup"><span data-stu-id="865ac-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="865ac-143">Selecteer in het veld **Type lading** een ladingtype om op te geven of de werkbelastingcapaciteit moet worden voorspeld voor volume of gewicht.</span><span class="sxs-lookup"><span data-stu-id="865ac-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="865ac-144">Selecteer in het veld **Werkbelastingcapaciteit** een instelling voor werkbelastingcapaciteit.</span><span class="sxs-lookup"><span data-stu-id="865ac-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]