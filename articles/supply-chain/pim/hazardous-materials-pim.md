---
title: Gevaarlijke materialen
description: Dit onderwerp biedt informatie over gevaarlijke materiaal-documenten en informatie die is opgeslagen in uw omgeving.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208453"
---
# <a name="hazardous-materials"></a><span data-ttu-id="f4f15-103">Gevaarlijke materialen</span><span class="sxs-lookup"><span data-stu-id="f4f15-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4f15-104">Informatie over gevaarlijke materialen wordt ingesteld in Productgegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="f4f15-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="f4f15-105">Deze module biedt ook documenten die kunnen worden afgedrukt via magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="f4f15-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="f4f15-106">Wanneer u materialen verzendt die zijn geclassificeerd als gevaarlijke goederen, moeten extra documenten bij de zendingen worden gevoegd.</span><span class="sxs-lookup"><span data-stu-id="f4f15-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="f4f15-107">Met de functionaliteit voor gevaarlijke materialen kunnen klanten classificatiegegevens opslaan en deze relateren aan vrijgaveartikelen.</span><span class="sxs-lookup"><span data-stu-id="f4f15-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="f4f15-108">Deze informatie kan vervolgens worden gebruikt om verzenddocumentatie voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="f4f15-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4f15-109">Voor het beheren van zendingen van gevaarlijke goederen kunt u met Microsoft Dynamics 365 Supply Chain Management aanvullende verwijzingsgegevens instellen die betrekking hebben op producten.</span><span class="sxs-lookup"><span data-stu-id="f4f15-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="f4f15-110">U kunt ook extra verzendingsdocumenten instellen.</span><span class="sxs-lookup"><span data-stu-id="f4f15-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="f4f15-111">Het systeem voldoet echter niet automatisch aan de voorschriften van uw land of regio.</span><span class="sxs-lookup"><span data-stu-id="f4f15-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="f4f15-112">In plaats daarvan is het een hulpprogramma dat uw algehele programma kan ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f4f15-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="f4f15-113">Voordat u deze functionaliteit kunt gebruiken, moet u de volgende instellingen opgeven:</span><span class="sxs-lookup"><span data-stu-id="f4f15-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="f4f15-114">**Productgegevensbeheer**: stel codes in die kunnen worden toegepast op vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="f4f15-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="f4f15-115">**Magazijnbeheer:** gebruik extra verzenddocumenten om verzendgegevens af te drukken.</span><span class="sxs-lookup"><span data-stu-id="f4f15-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="f4f15-116">Productgegevensbeheer</span><span class="sxs-lookup"><span data-stu-id="f4f15-116">Product information management</span></span>

<span data-ttu-id="f4f15-117">In Productgegevensbeheer is er een reeks instellingstabellen waarin u de referentiegegevens kunt toevoegen die worden vermeld in de lijsten met gevaarlijke goederen voor de vracht-, lucht- en zeevracht.</span><span class="sxs-lookup"><span data-stu-id="f4f15-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="f4f15-118">Dit zijn enkele van de reguleringen waarnaar vaak wordt verwezen:</span><span class="sxs-lookup"><span data-stu-id="f4f15-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="f4f15-119">**ADR**: verordeningen met betrekking tot het internationale vervoer van gevaarlijke goederen over de weg</span><span class="sxs-lookup"><span data-stu-id="f4f15-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="f4f15-120">**CFR 49**: reglementering in de Verenigde Staten voor het vervoer van gevaarlijke goederen</span><span class="sxs-lookup"><span data-stu-id="f4f15-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="f4f15-121">**IMDG**: de internationale code voor internationale gevaarlijke goederen over zee (IMDG)</span><span class="sxs-lookup"><span data-stu-id="f4f15-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="f4f15-122">**IATA**: de IATA-bepalingen (International Air Trans Port Association) inzake gevaarlijke goederen</span><span class="sxs-lookup"><span data-stu-id="f4f15-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="f4f15-123">Elk van deze verordeningen heeft een lijst met gevaarlijke goederen waarin referentiecodes zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f4f15-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="f4f15-124">De lijsten voor elk type transport worden gecombineerd in gedeelde internationale classificaties.</span><span class="sxs-lookup"><span data-stu-id="f4f15-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="f4f15-125">Supply Chain Management biedt een referentietabel voor de gedeelde codes in die lijsten.</span><span class="sxs-lookup"><span data-stu-id="f4f15-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="f4f15-126">Elke lijst heeft ook een aantal unieke codes die kunnen worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="f4f15-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="f4f15-127">Als u deze gegevens wilt configureren, maakt u een verordening die u kunt gebruiken om de initiële parameters te configureren.</span><span class="sxs-lookup"><span data-stu-id="f4f15-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="f4f15-128">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="f4f15-128">Warehouse management</span></span>

<span data-ttu-id="f4f15-129">Wanneer een zending wordt voorbereid, kunnen verschillende nieuwe rapporten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="f4f15-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="f4f15-130">Deze rapporten gebruiken de informatie die u hebt ingesteld in Productgegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="f4f15-130">These reports use the information that you set up in Product information management.</span></span>
