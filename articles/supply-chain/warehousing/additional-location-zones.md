---
title: Extra locatiezones
description: Dit onderwerp biedt een overzicht van de nieuwe locatiezones die zijn toegevoegd aan Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9727187ad555f9e3d09beed3f3447a22c29ed22a
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530162"
---
# <a name="additional-location-zones"></a><span data-ttu-id="f7ce0-103">Extra locatiezones</span><span class="sxs-lookup"><span data-stu-id="f7ce0-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7ce0-104">Er zijn drie nieuwe zonevelden beschikbaar in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f7ce0-105">Magazijnbeheerders kunnen deze gebruiken om aanvullende magazijnorganisaties of -indelingen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="f7ce0-106">De nieuwe zonevelden kunnen handmatig of met de **wizard voor locatie-instelling** worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="f7ce0-107">Deze kunnen worden gebruikt in query's of filters waarin de tabel Locaties wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="f7ce0-108">Er is geen aanvullende configuratie nodig om de zonevelden te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="f7ce0-109">De functie Extra locatiezone inschakelen</span><span class="sxs-lookup"><span data-stu-id="f7ce0-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="f7ce0-110">Voordat u de functie *Extra locatiezone* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="f7ce0-111">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f7ce0-112">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="f7ce0-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f7ce0-113">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="f7ce0-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f7ce0-114">**Functienaam:** *Extra locatiezone*</span><span class="sxs-lookup"><span data-stu-id="f7ce0-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="f7ce0-115">Locatiezones gebruiken</span><span class="sxs-lookup"><span data-stu-id="f7ce0-115">Use location zones</span></span>

1. <span data-ttu-id="f7ce0-116">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Wizard voor locatie-instelling**.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="f7ce0-117">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="f7ce0-117">Set the following values:</span></span>

    - <span data-ttu-id="f7ce0-118">Selecteer **62** in het veld _Magazijn_.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="f7ce0-119">Selecteer in het veld **Zone-id** de waarde _VERDIEPING_.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="f7ce0-120">Selecteer in het veld **Extra zone 1** de waarde _PICKZONE_.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="f7ce0-121">Selecteer in het veld **Extra zone 2** de waarde _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="f7ce0-122">Selecteer in het veld **Locatieprofiel-ID** de waarde _VERDIEPING_.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="f7ce0-123">Selecteer de regel **Verdieping**.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="f7ce0-124">Voer in het veld **Vanaf nummer** de waarde _1_ in.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="f7ce0-125">Voer in het veld **Tot nummer** de waarde _3_ in.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="f7ce0-126">Selecteer de regel **Aisle**.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="f7ce0-127">Voer in het veld **Vanaf nummer** de waarde _1_ in.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="f7ce0-128">Voer in het veld **Tot nummer** de waarde _5_ in.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="f7ce0-129">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-129">Select **Create**.</span></span>
8. <span data-ttu-id="f7ce0-130">U ontvangt berichten waarin wordt vermeld dat nieuwe locaties zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="f7ce0-131">Klik op de knop **Berichten weergeven** om de berichten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="f7ce0-132">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.</span><span class="sxs-lookup"><span data-stu-id="f7ce0-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="f7ce0-133">De nieuwe locaties worden weergegeven in de lijst en alle zonevelden zijn beschikbaar (dat wil zeggen: het bestaande zoneveld en de nieuwe extra zonevelden).</span><span class="sxs-lookup"><span data-stu-id="f7ce0-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>