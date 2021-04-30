---
title: Dynamics 365-globalisatieservices
description: Dit onderwerp bevat een overzicht van Microsoft Dynamics 365-globalisatieservices..
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893043"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="26f82-103">Dynamics 365-globalisatieservices</span><span class="sxs-lookup"><span data-stu-id="26f82-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26f82-104">De volgende globalisatieservices kunnen worden geconfigureerd om de capaciteiten van sommige Microsoft Dynamics 365 online services uit te breiden:</span><span class="sxs-lookup"><span data-stu-id="26f82-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="26f82-105">**Regulatory Configuration Service (RCS)** ondersteunt de configuratie van verschillende typen elektronische documenten en rapporten.</span><span class="sxs-lookup"><span data-stu-id="26f82-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="26f82-106">RCS biedt een verbeterde versie van de ER-ontwerper (Electronic Reporting), waarin de configuratie-opslagplaats een zelfstandige service is.</span><span class="sxs-lookup"><span data-stu-id="26f82-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="26f82-107">Zie [Regulatory Configuration Service](rcs-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="26f82-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="26f82-108">**Elektronische facturering** brengt configureerbare indelingen voor transformaties, digitale handtekeningen en configureerbare integraties samen voor connectiviteit met externe webservices, waaronder certificerings- en antwoordverwerking.</span><span class="sxs-lookup"><span data-stu-id="26f82-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="26f82-109">Zie [Elektronische facturering](e-invoicing-service-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="26f82-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="26f82-110">Met **Belastingberekening** kunt u meer flexibiliteit bieden met ondersteuning voor meerdere belasting-id's, bepalen van belastingcodes, ontwerper van de belastingberekening en een runtime-engine om te voldoen aan complexe belastingregels over de hele wereld.</span><span class="sxs-lookup"><span data-stu-id="26f82-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="26f82-111">Zie voor meer informatie [Belastingberekening](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26f82-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="26f82-112">Deze globalisatieservices bieden out-of-box-integratie met de volgende online services van Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="26f82-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="26f82-113">Online service</span><span class="sxs-lookup"><span data-stu-id="26f82-113">Online service</span></span> | <span data-ttu-id="26f82-114">RCS</span><span class="sxs-lookup"><span data-stu-id="26f82-114">RCS</span></span> | <span data-ttu-id="26f82-115">Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="26f82-115">Electronic Invoicing</span></span> | <span data-ttu-id="26f82-116">Belastingberekening (Preview)</span><span class="sxs-lookup"><span data-stu-id="26f82-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="26f82-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="26f82-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="26f82-118">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-118">Yes</span></span> | <span data-ttu-id="26f82-119">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-119">Yes</span></span> | <span data-ttu-id="26f82-120">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-120">Yes</span></span> | 
| <span data-ttu-id="26f82-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="26f82-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="26f82-122">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-122">Yes</span></span> | <span data-ttu-id="26f82-123">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-123">Yes</span></span> | <span data-ttu-id="26f82-124">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-124">Yes</span></span> | 
| <span data-ttu-id="26f82-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="26f82-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="26f82-126">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-126">Yes</span></span> | <span data-ttu-id="26f82-127">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-127">Yes</span></span> | <span data-ttu-id="26f82-128">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="26f82-128">Not applicable</span></span> | 
| <span data-ttu-id="26f82-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="26f82-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="26f82-130">Ja</span><span class="sxs-lookup"><span data-stu-id="26f82-130">Yes</span></span> | <span data-ttu-id="26f82-131">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="26f82-131">Not applicable</span></span> | <span data-ttu-id="26f82-132">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="26f82-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="26f82-133">Vanwege verschillen in de beschikbaarheid van geografische locaties van Azure (geo) voor RCS, kunnen klantgegevens door de configuratie van deze service worden overgebracht buiten de geografische locatie die is geselecteerd voor de toepasselijke Dynamics 365 online service.</span><span class="sxs-lookup"><span data-stu-id="26f82-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="26f82-134">Zie [Dynamics 365 en Power Platform: beschikbaarheid, gegevenslocatie, taal en lokalisatie](https://aka.ms/rcs/D365Productavailabilityguide) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="26f82-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>