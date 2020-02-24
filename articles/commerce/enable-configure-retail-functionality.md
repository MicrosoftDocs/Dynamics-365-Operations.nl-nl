---
title: Seedgegevens in nieuwe Retail-omgevingen initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Dynamics 365 Commerce.
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
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022171"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="86ebd-103">Seedgegevens in nieuwe Retail-omgevingen initialiseren</span><span class="sxs-lookup"><span data-stu-id="86ebd-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86ebd-104">In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86ebd-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="86ebd-105">Nadat de Commerce-oplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de Commerce-configuratie initialiseren om de basisconfiguratiegegevens te maken.</span><span class="sxs-lookup"><span data-stu-id="86ebd-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86ebd-106">Voordat u de Commerce-configuratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="86ebd-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="86ebd-107">Deze stap moet worden voltooid voor elke rechtspersoon die u voor handel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="86ebd-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="86ebd-108">Om de configuratie te initialiseren, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="86ebd-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="86ebd-109">Start de Commerce-client.</span><span class="sxs-lookup"><span data-stu-id="86ebd-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="86ebd-110">Klik op **Retail en commerce** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Commerce-parameters**.</span><span class="sxs-lookup"><span data-stu-id="86ebd-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="86ebd-111">Klik op **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="86ebd-111">Click **Initialize**.</span></span>

<span data-ttu-id="86ebd-112">Initialisatie maakt de volgende standaardconfiguratiegegevens:</span><span class="sxs-lookup"><span data-stu-id="86ebd-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="86ebd-113">Commerce-planner taken en subtaken</span><span class="sxs-lookup"><span data-stu-id="86ebd-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="86ebd-114">Handelkanaalschema</span><span class="sxs-lookup"><span data-stu-id="86ebd-114">Commerce channel schema</span></span>
- <span data-ttu-id="86ebd-115">Distributieplanningen Commerce</span><span class="sxs-lookup"><span data-stu-id="86ebd-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="86ebd-116">Standaardschermindelingen, die knoppenrasters, afbeeldingen en thema's omvatten</span><span class="sxs-lookup"><span data-stu-id="86ebd-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="86ebd-117">Tijdzonegegevens</span><span class="sxs-lookup"><span data-stu-id="86ebd-117">Time zone information</span></span>
- <span data-ttu-id="86ebd-118">Werking verkooppunten (POS)</span><span class="sxs-lookup"><span data-stu-id="86ebd-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="86ebd-119">POS-machtigingen</span><span class="sxs-lookup"><span data-stu-id="86ebd-119">POS permissions</span></span>
- <span data-ttu-id="86ebd-120">Afzetkanaalrapporten</span><span class="sxs-lookup"><span data-stu-id="86ebd-120">Channel reports</span></span>
- <span data-ttu-id="86ebd-121">Kenmerkmetagegevens</span><span class="sxs-lookup"><span data-stu-id="86ebd-121">Attribute metadata</span></span>
- <span data-ttu-id="86ebd-122">Sjablonen voor entiteitvalidatie</span><span class="sxs-lookup"><span data-stu-id="86ebd-122">Entity validation templates</span></span>
- <span data-ttu-id="86ebd-123">Batchtaak om de Commerce Data Exchange-sessiehistorie op te schonen</span><span class="sxs-lookup"><span data-stu-id="86ebd-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="86ebd-124">Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Commerce-database.</span><span class="sxs-lookup"><span data-stu-id="86ebd-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="86ebd-125">Er is een optie om de Commerce-planner afzonderlijk te configureren.</span><span class="sxs-lookup"><span data-stu-id="86ebd-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="86ebd-126">Met deze optie kunt u de configuratie van de Commerce-planner opnieuw instellen op de standaardwaarden.</span><span class="sxs-lookup"><span data-stu-id="86ebd-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="86ebd-127">Nadat de initialisatie is voltooid, moet u aanvullende Commerce-gegevens configureren.</span><span class="sxs-lookup"><span data-stu-id="86ebd-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="86ebd-128">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="86ebd-128">Here are some examples:</span></span>

- <span data-ttu-id="86ebd-129">Handelparameters</span><span class="sxs-lookup"><span data-stu-id="86ebd-129">Commerce parameters</span></span>
- <span data-ttu-id="86ebd-130">Parameters voor handelplanner</span><span class="sxs-lookup"><span data-stu-id="86ebd-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="86ebd-131">Commerce-kanalen</span><span class="sxs-lookup"><span data-stu-id="86ebd-131">Commerce channels</span></span>
- <span data-ttu-id="86ebd-132">Kassa's en apparaten</span><span class="sxs-lookup"><span data-stu-id="86ebd-132">Registers and devices</span></span>
- <span data-ttu-id="86ebd-133">Assortimenten</span><span class="sxs-lookup"><span data-stu-id="86ebd-133">Assortments</span></span>
