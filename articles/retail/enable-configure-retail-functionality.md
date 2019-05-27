---
title: Seedgegevens in nieuwe Retail-omgevingen initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556893"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="0acd9-103">Seedgegevens in nieuwe Retail-omgevingen initialiseren</span><span class="sxs-lookup"><span data-stu-id="0acd9-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0acd9-104">In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0acd9-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="0acd9-105">Nadat de detailhandelsoplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de detailhandelsconfiguratie initialiseren om de basisconfiguratiegegevens te maken.</span><span class="sxs-lookup"><span data-stu-id="0acd9-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0acd9-106">Voordat u de detailhandelsconfiguratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="0acd9-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="0acd9-107">Deze stap moet worden voltooid voor elke rechtspersoon die u voor kleinhandel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0acd9-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="0acd9-108">Om de kleinhandelsconfiguratie te initialiseren, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="0acd9-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="0acd9-109">Start de Dynamics 365 for Retail-client.</span><span class="sxs-lookup"><span data-stu-id="0acd9-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="0acd9-110">Klik op **Detailhandel** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Detailhandelparameters**.</span><span class="sxs-lookup"><span data-stu-id="0acd9-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="0acd9-111">Klik op **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="0acd9-111">Click **Initialize**.</span></span>

<span data-ttu-id="0acd9-112">Initialisatie maakt de volgende standaardconfiguratiegegevens:</span><span class="sxs-lookup"><span data-stu-id="0acd9-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="0acd9-113">Detailhandelplanner taken en subtaken</span><span class="sxs-lookup"><span data-stu-id="0acd9-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="0acd9-114">Detailhandelafzetkanaalschema</span><span class="sxs-lookup"><span data-stu-id="0acd9-114">Retail channel schema</span></span>
- <span data-ttu-id="0acd9-115">Distributieplanningen voor detailhandel</span><span class="sxs-lookup"><span data-stu-id="0acd9-115">Retail distribution schedules</span></span>
- <span data-ttu-id="0acd9-116">Standaardschermindelingen, die knoppenrasters, afbeeldingen en thema's omvatten</span><span class="sxs-lookup"><span data-stu-id="0acd9-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="0acd9-117">Tijdzonegegevens</span><span class="sxs-lookup"><span data-stu-id="0acd9-117">Time zone information</span></span>
- <span data-ttu-id="0acd9-118">Werking verkooppunten (POS)</span><span class="sxs-lookup"><span data-stu-id="0acd9-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="0acd9-119">POS-machtigingen</span><span class="sxs-lookup"><span data-stu-id="0acd9-119">POS permissions</span></span>
- <span data-ttu-id="0acd9-120">Afzetkanaalrapporten</span><span class="sxs-lookup"><span data-stu-id="0acd9-120">Channel reports</span></span>
- <span data-ttu-id="0acd9-121">Kenmerkmetagegevens</span><span class="sxs-lookup"><span data-stu-id="0acd9-121">Attribute metadata</span></span>
- <span data-ttu-id="0acd9-122">Sjablonen voor entiteitvalidatie</span><span class="sxs-lookup"><span data-stu-id="0acd9-122">Entity validation templates</span></span>
- <span data-ttu-id="0acd9-123">Batchtaak om de Commerce Data Exchange-sessiehistorie op te schonen</span><span class="sxs-lookup"><span data-stu-id="0acd9-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="0acd9-124">Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Dynamics 365 for Retail-database.</span><span class="sxs-lookup"><span data-stu-id="0acd9-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="0acd9-125">Er is een optie om de detailhandelplanner afzonderlijk te configureren.</span><span class="sxs-lookup"><span data-stu-id="0acd9-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="0acd9-126">Met deze optie kunt u de configuratie van de Detailhandel planner opnieuw instellen op de standaardwaarden.</span><span class="sxs-lookup"><span data-stu-id="0acd9-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="0acd9-127">Nadat de initialisatie is voltooid, moet u aanvullende detailhandelsgegevens configureren.</span><span class="sxs-lookup"><span data-stu-id="0acd9-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="0acd9-128">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="0acd9-128">Here are some examples:</span></span>

- <span data-ttu-id="0acd9-129">Detailhandelparameters</span><span class="sxs-lookup"><span data-stu-id="0acd9-129">Retail parameters</span></span>
- <span data-ttu-id="0acd9-130">Parameters voor Detailhandel planner</span><span class="sxs-lookup"><span data-stu-id="0acd9-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="0acd9-131">Detailhandelafzetkanalen</span><span class="sxs-lookup"><span data-stu-id="0acd9-131">Retail channels</span></span>
- <span data-ttu-id="0acd9-132">Kassa's en apparaten</span><span class="sxs-lookup"><span data-stu-id="0acd9-132">Registers and devices</span></span>
- <span data-ttu-id="0acd9-133">Assortimenten</span><span class="sxs-lookup"><span data-stu-id="0acd9-133">Assortments</span></span>
