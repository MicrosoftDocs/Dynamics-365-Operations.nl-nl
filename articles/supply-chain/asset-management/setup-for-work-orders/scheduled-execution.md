---
title: Geplande uitvoering
description: In dit onderwerp wordt geplande uitvoering in Activabeheer uitgelegd.
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
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874665"
---
# <a name="scheduled-execution"></a><span data-ttu-id="d1ad6-103">Geplande uitvoering</span><span class="sxs-lookup"><span data-stu-id="d1ad6-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d1ad6-104">U kunt serviceniveaus van werkorders gebruiken om geplande uitvoering in te stellen.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="d1ad6-105">(Zie [Serviceniveau en omschrijving](service-level-and-description.md)voor meer informatie over service niveaus van werkorders.) Geplande uitvoering biedt flexibiliteit bij werkplanning voor onderhoudsmedewerkers, omdat u meer gedetailleerde of minder gedetailleerde vereisten kunt instellen voor het interval waarin een werkorder moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="d1ad6-106">Een onderhoudsmedewerker die een taak sneller dan verwacht in een productiefaciliteit voltooid, kan bijvoorbeeld naar een andere nabijgelegen taak gaan die gepland is voor de huidige week, maar niet noodzakelijkerwijs voor de huidige dag.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="d1ad6-107">Deze aanpak maakt optimalisatie van werknemersplanning en taakvoltooiing mogelijk.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="d1ad6-108">De instellingen van de geplande uitvoering, die betrekking hebben op werkorders, kunnen algemeen of specifiek zijn.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="d1ad6-109">U kunt algemene regels instellen die niet beperkt zijn tot specifieke typen werkorders, activatypen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="d1ad6-110">U kunt ook geplande uitvoeringsregels maken die van toepassing zijn op een specifiek type werkorder, activatype, type onderhoudstaak, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="d1ad6-111">Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Geplande uitvoering**.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="d1ad6-112">Selecteer **Nieuw** om een geplande uitvoeringsregel te maken.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="d1ad6-113">Selecteer in de **Functionele locatie**, **Type werkorder**, **Activatype**, **Fabrikant**, **Model**, **Categorie type onderhoudstaak**, **Type onderhoudstaak**, **Type onderhoudstaak Variant** en **Handels**-velden. Selecteer waarden als u ze nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="d1ad6-114">Selecteer in het veld **Serviceniveau** een serviceniveau van een werkorder.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="d1ad6-115">Als u dit veld leeg laat, kunt u het meest algemene type geplande uitvoeringsregel maken.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="d1ad6-116">Zie het eerste record in de volgende afbeelding voor een voor beeld van een algemene regel.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="d1ad6-117">Op die regel kunnen alle werkorders waarvoor geen serviceniveau is ingesteld, voor een bepaalde datum en tijd worden gepland.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="d1ad6-118">Selecteer de tijdseenheid in het veld **Geplande uitvoering**.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="d1ad6-119">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d1ad6-119">Select **Save**.</span></span>

![Figuur 1](media/20-setup-for-work-orders.png)
