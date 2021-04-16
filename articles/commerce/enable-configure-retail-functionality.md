---
title: Seedgegevens in nieuwe Commerce-omgevingen initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792578"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="b3d26-103">Seedgegevens in nieuwe Commerce-omgevingen initialiseren</span><span class="sxs-lookup"><span data-stu-id="b3d26-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3d26-104">In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3d26-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b3d26-105">Nadat de Commerce-oplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de Commerce-configuratie initialiseren om de basisconfiguratiegegevens te maken.</span><span class="sxs-lookup"><span data-stu-id="b3d26-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3d26-106">Voordat u de Commerce-configuratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="b3d26-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="b3d26-107">Deze stap moet worden voltooid voor elke rechtspersoon die u voor handel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3d26-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="b3d26-108">Om de configuratie te initialiseren, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="b3d26-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="b3d26-109">Start de Commerce-client.</span><span class="sxs-lookup"><span data-stu-id="b3d26-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="b3d26-110">Klik op **Retail en commerce** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Commerce-parameters**.</span><span class="sxs-lookup"><span data-stu-id="b3d26-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="b3d26-111">Klik op **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="b3d26-111">Click **Initialize**.</span></span>

<span data-ttu-id="b3d26-112">Initialisatie maakt de volgende standaardconfiguratiegegevens:</span><span class="sxs-lookup"><span data-stu-id="b3d26-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="b3d26-113">Commerce-planner taken en subtaken</span><span class="sxs-lookup"><span data-stu-id="b3d26-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="b3d26-114">Handelkanaalschema</span><span class="sxs-lookup"><span data-stu-id="b3d26-114">Commerce channel schema</span></span>
- <span data-ttu-id="b3d26-115">Distributieplanningen Commerce</span><span class="sxs-lookup"><span data-stu-id="b3d26-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="b3d26-116">Standaardschermindelingen, die knoppenrasters, afbeeldingen en thema's omvatten</span><span class="sxs-lookup"><span data-stu-id="b3d26-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="b3d26-117">Tijdzonegegevens</span><span class="sxs-lookup"><span data-stu-id="b3d26-117">Time zone information</span></span>
- <span data-ttu-id="b3d26-118">Werking verkooppunten (POS)</span><span class="sxs-lookup"><span data-stu-id="b3d26-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="b3d26-119">POS-machtigingen</span><span class="sxs-lookup"><span data-stu-id="b3d26-119">POS permissions</span></span>
- <span data-ttu-id="b3d26-120">Afzetkanaalrapporten</span><span class="sxs-lookup"><span data-stu-id="b3d26-120">Channel reports</span></span>
- <span data-ttu-id="b3d26-121">Kenmerkmetagegevens</span><span class="sxs-lookup"><span data-stu-id="b3d26-121">Attribute metadata</span></span>
- <span data-ttu-id="b3d26-122">Sjablonen voor entiteitvalidatie</span><span class="sxs-lookup"><span data-stu-id="b3d26-122">Entity validation templates</span></span>
- <span data-ttu-id="b3d26-123">Batchtaak om de Commerce Data Exchange-sessiehistorie op te schonen</span><span class="sxs-lookup"><span data-stu-id="b3d26-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="b3d26-124">Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Commerce-database.</span><span class="sxs-lookup"><span data-stu-id="b3d26-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="b3d26-125">Er is een optie om de Commerce-planner afzonderlijk te configureren.</span><span class="sxs-lookup"><span data-stu-id="b3d26-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="b3d26-126">Met deze optie kunt u de configuratie van de Commerce-planner opnieuw instellen op de standaardwaarden.</span><span class="sxs-lookup"><span data-stu-id="b3d26-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="b3d26-127">Nadat de initialisatie is voltooid, moet u aanvullende Commerce-gegevens configureren.</span><span class="sxs-lookup"><span data-stu-id="b3d26-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="b3d26-128">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="b3d26-128">Here are some examples:</span></span>

- <span data-ttu-id="b3d26-129">Handelparameters</span><span class="sxs-lookup"><span data-stu-id="b3d26-129">Commerce parameters</span></span>
- <span data-ttu-id="b3d26-130">Parameters voor handelplanner</span><span class="sxs-lookup"><span data-stu-id="b3d26-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="b3d26-131">Commerce-kanalen</span><span class="sxs-lookup"><span data-stu-id="b3d26-131">Commerce channels</span></span>
- <span data-ttu-id="b3d26-132">Kassa's en apparaten</span><span class="sxs-lookup"><span data-stu-id="b3d26-132">Registers and devices</span></span>
- <span data-ttu-id="b3d26-133">Assortimenten</span><span class="sxs-lookup"><span data-stu-id="b3d26-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]