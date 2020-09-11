---
title: Overzicht van gevaarlijke stoffen
description: Dit onderwerp biedt een overzicht van functies die zijn gerelateerd aan het afhandelen en documenteren van gevaarlijke stoffen tijdens productgegevensbeheer en magazijnbeheer.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 227111f4703d9dc381270382dcb796874d7de937
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699601"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="15279-103">Overzicht van gevaarlijke stoffen</span><span class="sxs-lookup"><span data-stu-id="15279-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15279-104">Om te voldoen aan de verzend- en transportregels, moeten organisaties die materialen verzenden die zijn geclassificeerd als gevaarlijke goederen, aanvullende documenten opnemen in de zending.</span><span class="sxs-lookup"><span data-stu-id="15279-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="15279-105">Met de functie voor gevaarlijke goederen kunnen klanten gegevens opslaan die betrekking hebben op vrijgegeven artikelen.</span><span class="sxs-lookup"><span data-stu-id="15279-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="15279-106">Deze informatie kan vervolgens worden gebruikt om verzenddocumentatie voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="15279-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="15279-107">Een organisatie die gevaarlijke goederen verzendt, moet zijn eigen processen en procedures hebben voor het beheer van het verzendproces.</span><span class="sxs-lookup"><span data-stu-id="15279-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="15279-108">Microsoft Dynamics 365 Supply Chain Management is slechts een hulpmiddel waarmee u de vereiste documenten kunt genereren.</span><span class="sxs-lookup"><span data-stu-id="15279-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="15279-109">Het volgende diagram illustreert de stappen die nodig zijn voor het instellen en gebruiken van de functie voor gevaarlijke goederen.</span><span class="sxs-lookup"><span data-stu-id="15279-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="15279-110">![De functie voor gevaarlijke goederen instellen en gebruiken](media/hazmat-overview.png "De functie voor gevaarlijke goederen instellen en gebruiken")</span><span class="sxs-lookup"><span data-stu-id="15279-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="15279-111">De functie voor gevaarlijke goederen wordt ingesteld in Productgegevensbeheer en biedt documenten die kunnen worden afgedrukt via Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="15279-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="15279-112">Daarom zijn deze gebieden in principe de belangrijkste twee gebieden waar u de functionaliteit van deze functie kunt controleert, instelt en gebruikt:</span><span class="sxs-lookup"><span data-stu-id="15279-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="15279-113">**Productgegevensbeheer**: stel de codes in die kunnen worden toegepast op een vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="15279-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="15279-114">**Magazijnbeheer** : werk met aanvullende vervoersdocumenten die voor zendingen worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="15279-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15279-115">De functies voor gevaarlijke goederen in Supply Chain Management bevatten een verzameling nuttige productgegevensvelden en gerelateerde functionaliteit die u kunnen helpen bij het registreren van en verwijzen naar informatie met betrekking tot uw gevaarlijke producten.</span><span class="sxs-lookup"><span data-stu-id="15279-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="15279-116">Deze functies kunnen u ook helpen bij het ontwerpen en afdrukken van vervoersdocumenten met dezelfde informatie over gevaarlijke stoffen die u verzendt.</span><span class="sxs-lookup"><span data-stu-id="15279-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="15279-117">Het gebruik van dit systeem betekent echter niet dat u automatisch voldoet aan alle toepasselijke voorschriften uw land of regio.</span><span class="sxs-lookup"><span data-stu-id="15279-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="15279-118">Hoewel deze hulpmiddelen zijn bedoeld om u te helpen te voldoen aan algemene regelgeving, zijn ze niet voldoende en geven ze geen garanties.</span><span class="sxs-lookup"><span data-stu-id="15279-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="15279-119">Uw organisatie is moet er zelf voor zorgen dat men op de hoogte is van alle toepasselijke regelgeving en dat alle nodige maatregelen worden genomen om daaraan te voldoen.</span><span class="sxs-lookup"><span data-stu-id="15279-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="15279-120">Productgegevensbeheer</span><span class="sxs-lookup"><span data-stu-id="15279-120">Product information management</span></span>

<span data-ttu-id="15279-121">Productgegevensbeheer bevat een reeks instellingstabellen waarin u referentiegegevens kunt toevoegen voor de diverse lijsten met gevaarlijke goederen voor transport over land, lucht en zee.</span><span class="sxs-lookup"><span data-stu-id="15279-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="15279-122">Bij het ontwikkelen van deze functie wordt verwezen naar de volgende algemene regelgevingen:</span><span class="sxs-lookup"><span data-stu-id="15279-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="15279-123">**ADR**: verordeningen met betrekking tot het internationale vervoer van gevaarlijke goederen over de weg</span><span class="sxs-lookup"><span data-stu-id="15279-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="15279-124">**CFR 49**: reglementering in de Verenigde Staten voor het vervoer van gevaarlijke goederen</span><span class="sxs-lookup"><span data-stu-id="15279-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="15279-125">**IMDG**: de internationale code voor internationale gevaarlijke goederen over zee (IMDG)</span><span class="sxs-lookup"><span data-stu-id="15279-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="15279-126">**IATA**: de IATA-bepalingen (International Air Trans Port Association) inzake gevaarlijke goederen</span><span class="sxs-lookup"><span data-stu-id="15279-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="15279-127">Elke reeks regelgevingen voorziet in gestandaardiseerde lijsten van gevaarlijke goederen en referentiecodes.</span><span class="sxs-lookup"><span data-stu-id="15279-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="15279-128">Daarin verstrekt Supply Chain Management een referentietabel voor de algemene codes in die lijsten.</span><span class="sxs-lookup"><span data-stu-id="15279-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="15279-129">Elke lijst heeft ook een aantal unieke codes die u kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="15279-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="15279-130">Zie de volgende onderwerpen voor meer informatie over het instellen van regels en waarden voor gevaarlijke goederen en over het toewijzen van de waarden aan relevante producten:</span><span class="sxs-lookup"><span data-stu-id="15279-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="15279-131">Gevaarlijke goederen instellen</span><span class="sxs-lookup"><span data-stu-id="15279-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="15279-132">Gevaarlijke goederen in producten, orders, zendingen en ladingen</span><span class="sxs-lookup"><span data-stu-id="15279-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="15279-133">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="15279-133">Warehouse management</span></span>

<span data-ttu-id="15279-134">Wanneer u een zending voorbereidt in Magazijnbeheer, kunt u verschillende nieuwe rapporten afdrukken waarin de informatie wordt gebruikt die u hebt ingesteld in Productgegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="15279-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="15279-135">Meer informatie over de beschikbare rapporten en hoe u deze kunt gebruiken vindt u in [Informatie en rapporten voor gevaarlijke stoffen](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="15279-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
