---
title: LTL-klassen (Less than truckload)
description: In dit onderwerp wordt beschreven wat LTL-klassen (Less Than Truckload, 'geen volledige vrachtwagen') zijn en wordt beschreven hoe u deze in instelt in Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941805"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="da43d-103">LTL-klassen (Less than truckload)</span><span class="sxs-lookup"><span data-stu-id="da43d-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da43d-104">Een LTL-klasse (less than truckload, 'geen volledige vrachtwagen') is een vrachtverzendingsklasse die wordt gebruikt om artikelen te classificeren die kunnen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="da43d-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="da43d-105">Over het algemeen heeft elk type product of goed een NMFC-code (National Motor Freight Classification) die overeenkomt met een specifiek vrachtklassenummer voor LTL-zendingen.</span><span class="sxs-lookup"><span data-stu-id="da43d-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="da43d-106">LTL-vrachtklassen staan voor categorieën artikelen, terwijl NMFC-codes zijn gerelateerd aan specifieke goederen in elk van de achttien vrachtklassen.</span><span class="sxs-lookup"><span data-stu-id="da43d-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="da43d-107">Met deze functie kunt in uw systeem de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="da43d-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="da43d-108">De LTL-vrachtklassen definiëren die in uw bedrijf worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="da43d-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="da43d-109">Aan elke LTL-klasse een NMFC-code toewijzen op de pagina **NMFC-codes**.</span><span class="sxs-lookup"><span data-stu-id="da43d-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="da43d-110">Meer informatie over dit onderwerp vindt u in [NMFC-codes (National Motor Freight Classification)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="da43d-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="da43d-111">Een NMFC-code (en daarmee de bijbehorende LTL-code) toewijzen aan elk product op de pagina **Producten**.</span><span class="sxs-lookup"><span data-stu-id="da43d-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="da43d-112">Precies de LTL-klasse beoordelen van elk product waaraan een NMFC-code is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="da43d-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="da43d-113">De verpakkingsvereisten bepalen voor elke LTL-klasse door de internationale LTL-standaarden te bekijken.</span><span class="sxs-lookup"><span data-stu-id="da43d-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="da43d-114">Hiermee borgt u dat uw producten goed beschermd worden en veilig worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="da43d-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="da43d-115">Nauwkeurige schattingen van transportkosten maken, gebaseerd op de LTL-vrachtklasse voor elk product.</span><span class="sxs-lookup"><span data-stu-id="da43d-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="da43d-116">In dit onderwerp wordt beschreven hoe u LTL-klassen maakt in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="da43d-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="da43d-117">Een LTL-klasse maken</span><span class="sxs-lookup"><span data-stu-id="da43d-117">Create an LTL class</span></span>

<span data-ttu-id="da43d-118">U maakt als volgt een LTL-klasse.</span><span class="sxs-lookup"><span data-stu-id="da43d-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="da43d-119">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="da43d-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="da43d-120">Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> LTL-klassen**.</span><span class="sxs-lookup"><span data-stu-id="da43d-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="da43d-121">Ga naar **Transportbeheer \> Instellingen \> Transportstandaard \> LTL-klassen**.</span><span class="sxs-lookup"><span data-stu-id="da43d-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="da43d-122">Selecteer in het actievenster **Nieuw** om een LTL-klasse te maken.</span><span class="sxs-lookup"><span data-stu-id="da43d-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="da43d-123">Stel daarna de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="da43d-123">Then set the following fields:</span></span>

    - <span data-ttu-id="da43d-124">**LTL-klasse**: Voer de interne LTL-klasse-id van uw bedrijf in voor het goederentype.</span><span class="sxs-lookup"><span data-stu-id="da43d-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="da43d-125">De meeste bedrijven gebruiken de internationale standaard.</span><span class="sxs-lookup"><span data-stu-id="da43d-125">Most companies use the international standard.</span></span> <span data-ttu-id="da43d-126">In dat geval komt de waarde van dit veld overeen met de waarde van het veld **Klasse**.</span><span class="sxs-lookup"><span data-stu-id="da43d-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="da43d-127">Als uw bedrijf echter een eigen standaard gebruikt, voert u een code in die aan die standaard voldoet.</span><span class="sxs-lookup"><span data-stu-id="da43d-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="da43d-128">**Naam**: voer een beschrijvende naam in die u en andere gebruikers helpen de juiste LTL-klasse te selecteren voor elke NMFC-code.</span><span class="sxs-lookup"><span data-stu-id="da43d-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="da43d-129">**Klasse**: Voer de internationale standaard-LTL-klasse-id voor het type goederen in.</span><span class="sxs-lookup"><span data-stu-id="da43d-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="da43d-130">De code die u hier invoert, moet voldoen aan de officiële standaard.</span><span class="sxs-lookup"><span data-stu-id="da43d-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="da43d-131">Voorbeeld: LTL-klassen instellen</span><span class="sxs-lookup"><span data-stu-id="da43d-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="da43d-132">In het volgende voorbeeld ziet u hoe u twee verschillende LTL-klassen kunt instellen die u kunt gebruiken bij verschillende typen producten.</span><span class="sxs-lookup"><span data-stu-id="da43d-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="da43d-133">Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> LTL-klassen**.</span><span class="sxs-lookup"><span data-stu-id="da43d-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="da43d-134">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="da43d-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="da43d-135">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="da43d-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="da43d-136">**LTL-klasse**: *92.5*</span><span class="sxs-lookup"><span data-stu-id="da43d-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="da43d-137">**Naam**: *Computers, beeldschermen, koelkasten*</span><span class="sxs-lookup"><span data-stu-id="da43d-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="da43d-138">**Klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="da43d-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="da43d-139">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="da43d-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="da43d-140">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="da43d-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="da43d-141">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="da43d-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="da43d-142">**LTL-klasse**: *125*</span><span class="sxs-lookup"><span data-stu-id="da43d-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="da43d-143">**Naam**: *Kleine huishoudelijke apparaten*</span><span class="sxs-lookup"><span data-stu-id="da43d-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="da43d-144">**Klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="da43d-144">**Class:** *125*</span></span>

1. <span data-ttu-id="da43d-145">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="da43d-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da43d-146">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="da43d-146">Additional resources</span></span>

- [<span data-ttu-id="da43d-147">NMFC-codes (National Motor Freight Classification)</span><span class="sxs-lookup"><span data-stu-id="da43d-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="da43d-148">Een vrachtbrief maken</span><span class="sxs-lookup"><span data-stu-id="da43d-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
