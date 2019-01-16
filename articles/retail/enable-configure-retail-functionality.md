---
title: Seedgegevens in nieuwe Retail-omgevingen initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.contentlocale: nl-nl
ms.lasthandoff: 01/04/2019

---

# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="458ca-103">Seedgegevens in nieuwe Retail-omgevingen initialiseren</span><span class="sxs-lookup"><span data-stu-id="458ca-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="458ca-104">In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="458ca-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="458ca-105">Nadat de detailhandelsoplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de detailhandelsconfiguratie initialiseren om de basisconfiguratiegegevens te maken.</span><span class="sxs-lookup"><span data-stu-id="458ca-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="458ca-106">Voordat u de detailhandelsconfiguratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="458ca-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="458ca-107">Deze stap moet worden voltooid voor elke rechtspersoon die u voor kleinhandel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="458ca-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="458ca-108">Om de kleinhandelsconfiguratie te initialiseren, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="458ca-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="458ca-109">Start de Dynamics 365 for Retail-client.</span><span class="sxs-lookup"><span data-stu-id="458ca-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="458ca-110">Klik op **Detailhandel** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Detailhandelparameters**.</span><span class="sxs-lookup"><span data-stu-id="458ca-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="458ca-111">Klik op **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="458ca-111">Click **Initialize**.</span></span>

<span data-ttu-id="458ca-112">Initialisatie maakt de volgende standaardconfiguratiegegevens:</span><span class="sxs-lookup"><span data-stu-id="458ca-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="458ca-113">Detailhandelplanner taken en subtaken</span><span class="sxs-lookup"><span data-stu-id="458ca-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="458ca-114">Detailhandelafzetkanaalschema</span><span class="sxs-lookup"><span data-stu-id="458ca-114">Retail channel schema</span></span>
- <span data-ttu-id="458ca-115">Distributieplanningen voor detailhandel</span><span class="sxs-lookup"><span data-stu-id="458ca-115">Retail distribution schedules</span></span>
- <span data-ttu-id="458ca-116">Standaardschermindelingen, die knoppenrasters, afbeeldingen en thema's omvatten</span><span class="sxs-lookup"><span data-stu-id="458ca-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="458ca-117">Tijdzonegegevens</span><span class="sxs-lookup"><span data-stu-id="458ca-117">Time zone information</span></span>
- <span data-ttu-id="458ca-118">Werking verkooppunten (POS)</span><span class="sxs-lookup"><span data-stu-id="458ca-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="458ca-119">POS-machtigingen</span><span class="sxs-lookup"><span data-stu-id="458ca-119">POS permissions</span></span>
- <span data-ttu-id="458ca-120">Afzetkanaalrapporten</span><span class="sxs-lookup"><span data-stu-id="458ca-120">Channel reports</span></span>
- <span data-ttu-id="458ca-121">Kenmerkmetagegevens</span><span class="sxs-lookup"><span data-stu-id="458ca-121">Attribute metadata</span></span>
- <span data-ttu-id="458ca-122">Sjablonen voor entiteitvalidatie</span><span class="sxs-lookup"><span data-stu-id="458ca-122">Entity validation templates</span></span>
- <span data-ttu-id="458ca-123">Batchtaak om de sessiehistorie van Commerce Data Exchange op te schonen</span><span class="sxs-lookup"><span data-stu-id="458ca-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="458ca-124">Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Dynamics 365 for Retail-database.</span><span class="sxs-lookup"><span data-stu-id="458ca-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="458ca-125">Er is een optie om de detailhandelplanner afzonderlijk te configureren.</span><span class="sxs-lookup"><span data-stu-id="458ca-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="458ca-126">Met deze optie kunt u de configuratie van de Detailhandel planner opnieuw instellen op de standaardwaarden.</span><span class="sxs-lookup"><span data-stu-id="458ca-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="458ca-127">Nadat de initialisatie is voltooid, moet u aanvullende detailhandelsgegevens configureren.</span><span class="sxs-lookup"><span data-stu-id="458ca-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="458ca-128">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="458ca-128">Here are some examples:</span></span>

- <span data-ttu-id="458ca-129">Detailhandelparameters</span><span class="sxs-lookup"><span data-stu-id="458ca-129">Retail parameters</span></span>
- <span data-ttu-id="458ca-130">Parameters voor Detailhandel planner</span><span class="sxs-lookup"><span data-stu-id="458ca-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="458ca-131">Detailhandelafzetkanalen</span><span class="sxs-lookup"><span data-stu-id="458ca-131">Retail channels</span></span>
- <span data-ttu-id="458ca-132">Kassa's en apparaten</span><span class="sxs-lookup"><span data-stu-id="458ca-132">Registers and devices</span></span>
- <span data-ttu-id="458ca-133">Assortimenten</span><span class="sxs-lookup"><span data-stu-id="458ca-133">Assortments</span></span>

