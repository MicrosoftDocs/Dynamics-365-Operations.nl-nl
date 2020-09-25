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
ms.openlocfilehash: 54e5dca38b31c9310d44bdda5f5af14ca1515541
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802696"
---
# <a name="hazardous-materials"></a><span data-ttu-id="cad12-103">Gevaarlijke materialen</span><span class="sxs-lookup"><span data-stu-id="cad12-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cad12-104">Informatie over gevaarlijke materialen wordt ingesteld in Productgegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="cad12-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="cad12-105">Deze module biedt ook documenten die kunnen worden afgedrukt via magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="cad12-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="cad12-106">Wanneer u materialen verzendt die zijn geclassificeerd als gevaarlijke goederen, moeten extra documenten bij de zendingen worden gevoegd.</span><span class="sxs-lookup"><span data-stu-id="cad12-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="cad12-107">Met de functionaliteit voor gevaarlijke materialen kunnen klanten classificatiegegevens opslaan en deze relateren aan vrijgaveartikelen.</span><span class="sxs-lookup"><span data-stu-id="cad12-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="cad12-108">Deze informatie kan vervolgens worden gebruikt om verzenddocumentatie voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="cad12-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cad12-109">De functies voor gevaarlijke stoffen in Microsoft Dynamics 365 Supply Chain Management bevatten een verzameling nuttige productgegevensvelden en gerelateerde functies die u kunnen helpen bij het registreren van en verwijzen naar informatie met betrekking tot uw gevaarlijke producten.</span><span class="sxs-lookup"><span data-stu-id="cad12-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="cad12-110">Deze functies kunnen u ook helpen bij het ontwerpen en afdrukken van vervoersdocumenten met dezelfde informatie over gevaarlijke stoffen die u verzendt.</span><span class="sxs-lookup"><span data-stu-id="cad12-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="cad12-111">Het gebruik van dit systeem betekent echter niet dat u automatisch voldoet aan alle toepasselijke voorschriften uw land of regio.</span><span class="sxs-lookup"><span data-stu-id="cad12-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="cad12-112">Hoewel deze hulpmiddelen zijn bedoeld om u te helpen te voldoen aan algemene regelgeving, zijn ze niet voldoende en geven ze geen garanties.</span><span class="sxs-lookup"><span data-stu-id="cad12-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="cad12-113">Uw organisatie is moet er zelf voor zorgen dat men op de hoogte is van alle toepasselijke regelgeving en dat alle nodige maatregelen worden genomen om daaraan te voldoen.</span><span class="sxs-lookup"><span data-stu-id="cad12-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="cad12-114">Voordat u deze functionaliteit kunt gebruiken, moet u de volgende instellingen opgeven:</span><span class="sxs-lookup"><span data-stu-id="cad12-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="cad12-115">**Productgegevensbeheer**: stel codes in die kunnen worden toegepast op vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="cad12-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="cad12-116">**Magazijnbeheer:** gebruik extra verzenddocumenten om verzendgegevens af te drukken.</span><span class="sxs-lookup"><span data-stu-id="cad12-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="cad12-117">Productgegevensbeheer</span><span class="sxs-lookup"><span data-stu-id="cad12-117">Product information management</span></span>

<span data-ttu-id="cad12-118">In Productgegevensbeheer is er een reeks instellingstabellen waarin u de referentiegegevens kunt toevoegen die worden vermeld in de lijsten met gevaarlijke goederen voor de vracht-, lucht- en zeevracht.</span><span class="sxs-lookup"><span data-stu-id="cad12-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="cad12-119">Dit zijn enkele van de reguleringen waarnaar vaak wordt verwezen:</span><span class="sxs-lookup"><span data-stu-id="cad12-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="cad12-120">**ADR**: verordeningen met betrekking tot het internationale vervoer van gevaarlijke goederen over de weg</span><span class="sxs-lookup"><span data-stu-id="cad12-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="cad12-121">**CFR 49**: reglementering in de Verenigde Staten voor het vervoer van gevaarlijke goederen</span><span class="sxs-lookup"><span data-stu-id="cad12-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="cad12-122">**IMDG**: de internationale code voor internationale gevaarlijke goederen over zee (IMDG)</span><span class="sxs-lookup"><span data-stu-id="cad12-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="cad12-123">**IATA**: de IATA-bepalingen (International Air Trans Port Association) inzake gevaarlijke goederen</span><span class="sxs-lookup"><span data-stu-id="cad12-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="cad12-124">Elk van deze verordeningen heeft een lijst met gevaarlijke goederen waarin referentiecodes zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="cad12-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="cad12-125">De lijsten voor elk type transport worden gecombineerd in gedeelde internationale classificaties.</span><span class="sxs-lookup"><span data-stu-id="cad12-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="cad12-126">Supply Chain Management biedt een referentietabel voor de gedeelde codes in die lijsten.</span><span class="sxs-lookup"><span data-stu-id="cad12-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="cad12-127">Elke lijst heeft ook een aantal unieke codes die kunnen worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="cad12-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="cad12-128">Als u deze gegevens wilt configureren, maakt u een verordening die u kunt gebruiken om de initiële parameters te configureren.</span><span class="sxs-lookup"><span data-stu-id="cad12-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="cad12-129">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="cad12-129">Warehouse management</span></span>

<span data-ttu-id="cad12-130">Wanneer een zending wordt voorbereid, kunnen verschillende nieuwe rapporten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="cad12-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="cad12-131">Deze rapporten gebruiken de informatie die u hebt ingesteld in Productgegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="cad12-131">These reports use the information that you set up in Product information management.</span></span>
