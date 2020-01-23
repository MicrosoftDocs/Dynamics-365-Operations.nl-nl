---
title: Bijna realtime gegevensintegratie met Common Data Service
description: In dit onderwerp wordt een overzicht gegevens van de integratie tussen Finance and Operations en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853901"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="1ad3d-103">Bijna realtime gegevensintegratie met Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1ad3d-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ad3d-104">In de huidige digitale wereld gebruiken bedrijfsecosystemen de Microsoft Dynamics 365-toepassingen als geheel.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="1ad3d-105">Omdat gegevens van mensen, klanten, bewerkingen en IoT-apparaten (Internet of Things) in één bron terechtkomen, ontstaat er een mogelijkheid voor digitale feedbacklussen.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="1ad3d-106">Om deze ervaring te bereiken, is integratie tussen Finance and Operations-apps en andere Dynamics 365-toepassingen essentieel.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="1ad3d-107">Bepaalde toepassingen zijn gebouwd op Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="1ad3d-108">Dankzij de integratie tussen Finance and Operations-apps en Common Data Service kunnen andere toepassingen coherent en vloeiend communiceren met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="1ad3d-109">Finance and Operations-apps en Common Data Service bieden voor near realtime gegevenssynchronisatie tussen Finance and Operations en andere Dynamics 365-toepassingen via een famework voor Twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="1ad3d-110">De dekking is breed en beslaat 28 oppervlaktegebieden van de toepassing.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="1ad3d-111">Het doel is om een 'Eén Dynamics 365'-gebruikerservaring te bieden via naadloze gegevensstromen die bedrijfsprocessen tussen toepassingen verbinden.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Overzichtsdiagram van de architectuur](media/dual-write-overview.jpg)

<span data-ttu-id="1ad3d-113">De volgende waardeproposities zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="1ad3d-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="1ad3d-114">Organisatiehiërarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1ad3d-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="1ad3d-115">Bedrijfsconcept in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1ad3d-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="1ad3d-116">Geïntegreerd klantmodel</span><span class="sxs-lookup"><span data-stu-id="1ad3d-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="1ad3d-117">Geïntegreerd grootboek</span><span class="sxs-lookup"><span data-stu-id="1ad3d-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="1ad3d-118">Uniforme productervaring</span><span class="sxs-lookup"><span data-stu-id="1ad3d-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="1ad3d-119">Geïntegreerd leveranciersmodel</span><span class="sxs-lookup"><span data-stu-id="1ad3d-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="1ad3d-120">Geïntegreerde locaties en magazijnen</span><span class="sxs-lookup"><span data-stu-id="1ad3d-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="1ad3d-121">Geïntegreerde hoofdgegevens voor belasting</span><span class="sxs-lookup"><span data-stu-id="1ad3d-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="1ad3d-122">Systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="1ad3d-122">System requirements</span></span>

<span data-ttu-id="1ad3d-123">Synchrone, bidirectionele, near realtime gegevensstromen vereisen de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="1ad3d-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="1ad3d-124">Microsoft Dynamics 365 for Finance and Operations versie 10.0.4 (juli 2019) met platformupdate 28 of hoger</span><span class="sxs-lookup"><span data-stu-id="1ad3d-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="1ad3d-125">Microsoft Dynamics 365 for Customer Engagement, platformversie 9.1 (4.2) of hoger</span><span class="sxs-lookup"><span data-stu-id="1ad3d-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="1ad3d-126">Instructies voor instellingen</span><span class="sxs-lookup"><span data-stu-id="1ad3d-126">Setup instructions</span></span>

<span data-ttu-id="1ad3d-127">Volg deze stappen om de integratie tussen Finance and Operations-apps en Common Data Service in te stellen.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="1ad3d-128">Voor de installatie van het systeem voor Twee keer wegschrijven raadpleegt u de [stapsgewijze handleiding](https://aka.ms/dualwrite-docs) over het aankondigen van de preview voor Twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="1ad3d-129">Download en installeer de oplossing via de Yammer-groep [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096).</span><span class="sxs-lookup"><span data-stu-id="1ad3d-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="1ad3d-130">Het pakket bevat vijf oplossingen:</span><span class="sxs-lookup"><span data-stu-id="1ad3d-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="1ad3d-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="1ad3d-131">Dynamics365Company</span></span>
    + <span data-ttu-id="1ad3d-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="1ad3d-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="1ad3d-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="1ad3d-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="1ad3d-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="1ad3d-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="1ad3d-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="1ad3d-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="1ad3d-136">Volg de uitvoeringsvolgorde voor [Eerste referentiegegevens synchroniseren](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="1ad3d-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="1ad3d-137">Als u problemen ondervindt met de synchronisatie voor Twee keer wegschrijven, raadpleegt u de [Probleemoplossingsgids voor gegevensintegratie](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="1ad3d-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ad3d-138">U kunt Twee keer wegschrijven en [Prospect naar contant geld](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) niet naast elkaar uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="1ad3d-139">Als u de oplossing Prospect naar contant geld uitvoert, moet u deze verwijderen.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="1ad3d-140">U moet ook de klant- en leveranciersjablonen voor Twee keer wegschrijven uitschakelen die deel uitmaken van de oplossing Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
