---
title: Serviceniveau en -beschrijving
description: In dit onderwerp worden serviceniveau en -beschrijving in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874642"
---
# <a name="service-level-and-description"></a><span data-ttu-id="4e1bd-103">Serviceniveau en -beschrijving</span><span class="sxs-lookup"><span data-stu-id="4e1bd-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4e1bd-104">Wanneer u een werkorder maakt, kunt u de serviceniveaus hiervoor definiëren en er een algemene omschrijving aan toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="4e1bd-105">U kunt serviceniveaus voor werkorders maken op de pagina **Serviceniveaus voor werkorders** en omschrijvingen op de pagina **Omschrijvingen voor werkorders**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="4e1bd-106">Een serviceniveau maken</span><span class="sxs-lookup"><span data-stu-id="4e1bd-106">Create a service level</span></span>

1. <span data-ttu-id="4e1bd-107">Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="4e1bd-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-108">Select **New**.</span></span>
3. <span data-ttu-id="4e1bd-109">Voer in het veld **Serviceniveau** het serviceniveau in (bijvoorbeeld een nummer).</span><span class="sxs-lookup"><span data-stu-id="4e1bd-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="4e1bd-110">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="4e1bd-111">Op het Sneltabblad **Werkorders** kunt u de verwachte begin- en einddatums en -tijden definiëren.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="4e1bd-112">De velden op dit Sneltabblad definiëren de periode waarin werkorders moeten worden gestart en beëindigd.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="4e1bd-113">Deze worden gebruikt voor werkorders die handmatig worden gemaakt en werkorders die worden gemaakt op basis van onderhoudsaanvragen.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="4e1bd-114">Voer in het veld **Begindatum** een aantal dagen in om de periode te definiëren waarin de werkorder moet beginnen.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="4e1bd-115">Het aantal dagen wordt berekend vanaf de aanmaakdatum van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="4e1bd-116">Als de werkorder bijvoorbeeld moet beginnen wanneer deze wordt gemaakt, voert u **0** in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="4e1bd-117">Als de werkorder bijvoorbeeld een week nadat deze is gemaakt moet beginnen, voert u **7** in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="4e1bd-118">Als u een begintijd voor de werkorder wilt instellen, moet u behalve de begindatum ook de optie **Begintijd instellen** op **Ja** instellen.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="4e1bd-119">Voer vervolgens de begintijd in het veld **Begintijd** in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="4e1bd-120">Als u de optie op **Nee** instelt, wordt de huidige tijd van de dag gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="4e1bd-121">Voer in het veld **Einddatum** een aantal dagen in om de periode te definiëren waarin de werkorder moet eindigen.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="4e1bd-122">Het aantal dagen wordt berekend vanaf de begindatum van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="4e1bd-123">Als de werkorder bijvoorbeeld binnen één week na de begindatum moet eindigen, voert u **7**in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="4e1bd-124">Als u een eindtijd voor de werkorder wilt instellen, moet u behalve de einddatum ook de optie **Eindtijd instellen** op **Ja** instellen.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="4e1bd-125">Voer vervolgens de eindtijd in het veld **Eindtijd** in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="4e1bd-126">Als u de optie op **Nee** instelt, wordt de huidige tijd van de dag gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="4e1bd-127">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-127">Select **Save**.</span></span>

![Figuur 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="4e1bd-129">Een omschrijving maken</span><span class="sxs-lookup"><span data-stu-id="4e1bd-129">Create a description</span></span>

1. <span data-ttu-id="4e1bd-130">Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Omschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="4e1bd-131">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-131">Select **New**.</span></span>
3. <span data-ttu-id="4e1bd-132">Voer in het veld **Omschrijving** een omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="4e1bd-133">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-133">Select **Save**.</span></span>
