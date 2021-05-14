---
title: NMFC-codes (National Motor Freight Classification)
description: In dit onderwerp wordt beschreven hoe u werkt met NMFC-codes (National Motor Freight Classification) in Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941877"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="41c6b-103">NMFC-codes (National Motor Freight Classification)</span><span class="sxs-lookup"><span data-stu-id="41c6b-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41c6b-104">Met NMFC-codes (National Motor Freight Classification) kunt u artikelen classificeren die kunnen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="41c6b-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="41c6b-105">De NMFC-code is een aanduiding die wordt gebruikt om goederen te groeperen.</span><span class="sxs-lookup"><span data-stu-id="41c6b-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="41c6b-106">Transportbedrijven kunnen hiermee goederen beoordelen voor verzending, door artikelen te classificeren op basis van overwegingen zoals hoe ze in de vrachtwagen passen, eventuele problemen bij laden en hanteren en de bederfelijkheid.</span><span class="sxs-lookup"><span data-stu-id="41c6b-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="41c6b-107">Goederen worden geklassificeerd in een van 18 vrachtklassen met een nummer tussen 50 en 500.</span><span class="sxs-lookup"><span data-stu-id="41c6b-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="41c6b-108">De klasse waar een goed in is gegroepeerd, is gebaseerd op een evaluatie van vier transportkenmerken: dichtheid, stapelbaarheid, hanteerbaarheid en aansprakelijkheid.</span><span class="sxs-lookup"><span data-stu-id="41c6b-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="41c6b-109">Deze kenmerken bepalen samen de transporteerbaarheid van het goed.</span><span class="sxs-lookup"><span data-stu-id="41c6b-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="41c6b-110">Aan elk LTL-verzendartikel (Less Than Truckload, 'geen volledige vrachtwagen') wordt een NMFC-code gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="41c6b-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="41c6b-111">Een laptop kan bijvoorbeeld een NMFC van 2.5 worden toegewezen, terwijl aan stroomkabels een NMFC van 65 wordt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="41c6b-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="41c6b-112">Dit kenmerk kan werknemers helpen om NMFC-codes te gebruiken om LTL-verzendartikelen te classificeren.</span><span class="sxs-lookup"><span data-stu-id="41c6b-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="41c6b-113">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="41c6b-113">Here are some examples:</span></span>

- <span data-ttu-id="41c6b-114">Als uw bedrijf een vrachtbeschrijving op de vrachtbrief opneemt, heeft de vervoerder een idee van wat de vracht is.</span><span class="sxs-lookup"><span data-stu-id="41c6b-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="41c6b-115">Vracht is een belangrijke classificatie, omdat veel transportbedrijven hun hele bedrijfsmodel baseren op de typen vracht die ze transporteren.</span><span class="sxs-lookup"><span data-stu-id="41c6b-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="41c6b-116">Deze classificatie kan essentieel zijn voor uw bedrijf, omdat deze wordt gebruikt om de kosten van een bepaalde lading te bepalen.</span><span class="sxs-lookup"><span data-stu-id="41c6b-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="41c6b-117">Uw bedrijf kan de winstgevendheid van een bedrijf dat werkt met LTL-logistiek en transport identificeren.</span><span class="sxs-lookup"><span data-stu-id="41c6b-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="41c6b-118">In dit onderwerp wordt beschreven hoe u werkt met NMFC-codes in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="41c6b-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="41c6b-119">Vereisten</span><span class="sxs-lookup"><span data-stu-id="41c6b-119">Prerequisites</span></span>

<span data-ttu-id="41c6b-120">Voordat u NMFC-codes kunt maken, moet u alle LTL-vrachtklassen instellen die daaraan moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="41c6b-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="41c6b-121">LTL-vrachtklassen staan voor categorieën artikelen, terwijl NMFC-codes zijn gerelateerd aan specifieke goederen in elk van de achttien vrachtklassen.</span><span class="sxs-lookup"><span data-stu-id="41c6b-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="41c6b-122">Meer informatie over het werken met LTL-klassen vindt u in [LTL-klassen (Less than truckload)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="41c6b-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="41c6b-123">Een NMFC-code maken</span><span class="sxs-lookup"><span data-stu-id="41c6b-123">Create an NMFC code</span></span>

<span data-ttu-id="41c6b-124">U maakt als volgt een NMFC-code.</span><span class="sxs-lookup"><span data-stu-id="41c6b-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="41c6b-125">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="41c6b-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="41c6b-126">Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> NMFC-codes**.</span><span class="sxs-lookup"><span data-stu-id="41c6b-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="41c6b-127">Ga naar **Transportbeheer \> Instellingen \> Transportstandaard \> NMFC-codes**.</span><span class="sxs-lookup"><span data-stu-id="41c6b-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="41c6b-128">Selecteer **Nieuw** om een NMFC-code te maken.</span><span class="sxs-lookup"><span data-stu-id="41c6b-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="41c6b-129">Stel daarna de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="41c6b-129">Then set the following fields:</span></span>

    - <span data-ttu-id="41c6b-130">**NMFC-code**: voer de NFMC-code voor het goederentype in.</span><span class="sxs-lookup"><span data-stu-id="41c6b-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="41c6b-131">**Naam**: voer een naam in voor de NMFC-code.</span><span class="sxs-lookup"><span data-stu-id="41c6b-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="41c6b-132">**LTL-klasse**: selecteer de LTL-klasse die aan de NMFC-code is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="41c6b-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="41c6b-133">**Vrachtbriefverwerkingseenheid**: definieer het standaardverwerkingstype voor de zending.</span><span class="sxs-lookup"><span data-stu-id="41c6b-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="41c6b-134">Voorbeeld: NMFC-codes instellen</span><span class="sxs-lookup"><span data-stu-id="41c6b-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="41c6b-135">In het volgende voorbeeld ziet u hoe u twee verschillende NMFC-codes kunt instellen die bij verschillende producten kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41c6b-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="41c6b-136">Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> NMFC-codes**.</span><span class="sxs-lookup"><span data-stu-id="41c6b-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="41c6b-137">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="41c6b-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="41c6b-138">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="41c6b-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="41c6b-139">**NMFC-code:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="41c6b-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="41c6b-140">**Naam**: *Computers*</span><span class="sxs-lookup"><span data-stu-id="41c6b-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="41c6b-141">**LTL-klasse**: *92.5*</span><span class="sxs-lookup"><span data-stu-id="41c6b-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="41c6b-142">**Vrachtbriefverwerkingseenheid**: *Eenheid*</span><span class="sxs-lookup"><span data-stu-id="41c6b-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="41c6b-143">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="41c6b-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="41c6b-144">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="41c6b-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="41c6b-145">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="41c6b-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="41c6b-146">**NMFC-code:** *125*</span><span class="sxs-lookup"><span data-stu-id="41c6b-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="41c6b-147">**Naam**: *Telefoons*</span><span class="sxs-lookup"><span data-stu-id="41c6b-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="41c6b-148">**LTL-klasse**: *125*</span><span class="sxs-lookup"><span data-stu-id="41c6b-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="41c6b-149">**Vrachtbriefverwerkingseenheid**: *Eenheid*</span><span class="sxs-lookup"><span data-stu-id="41c6b-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="41c6b-150">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="41c6b-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41c6b-151">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="41c6b-151">Additional resources</span></span>

- [<span data-ttu-id="41c6b-152">LTL-klassen (Less than truckload)</span><span class="sxs-lookup"><span data-stu-id="41c6b-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="41c6b-153">Een vrachtbrief maken</span><span class="sxs-lookup"><span data-stu-id="41c6b-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
