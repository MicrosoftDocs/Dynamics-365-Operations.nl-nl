---
title: Uitvaltijd voor onderhoud
description: In dit onderwerp wordt uitvaltijd voor onderhoud in Activabeheer beschreven.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918239"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="23b2d-103">Uitvaltijd voor onderhoud</span><span class="sxs-lookup"><span data-stu-id="23b2d-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="23b2d-104">U kunt registraties voor uitvaltijd voor onderhoud maken voor de geselecteerde activa in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="23b2d-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="23b2d-105">Dit is handig als u de uitvaltijd voor onderhoud voor een of meer machines in het productiegebied wilt registreren.</span><span class="sxs-lookup"><span data-stu-id="23b2d-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="23b2d-106">Eerst maakt u de redencodes voor uitvaltijd voor onderhoud die u wilt gebruiken, bijvoorbeeld storing en geplande beëindiging.</span><span class="sxs-lookup"><span data-stu-id="23b2d-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="23b2d-107">Dit wordt gedaan in **Redencodes voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="23b2d-108">Vervolgens kunt u registraties voor uitvaltijd voor onderhoud maken in **Uitvaltijd voor onderhoud** en de relevante redencodes toevoegen.</span><span class="sxs-lookup"><span data-stu-id="23b2d-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="23b2d-109">Redencodes voor uitvaltijd voor onderhoud maken</span><span class="sxs-lookup"><span data-stu-id="23b2d-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="23b2d-110">Klik op **Activabeheer** > **Instellingen** > **Werkorders** > **Redencodes voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="23b2d-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-111">Click **New**.</span></span>

3. <span data-ttu-id="23b2d-112">Voeg een id in het **Redencode voor uitvaltijd voor onderhoud** in.</span><span class="sxs-lookup"><span data-stu-id="23b2d-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="23b2d-113">Typ een naam voor de redencode in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="23b2d-114">Schakel het selectievakje **Opnemen in KPI** in als de redencode moet worden opgenomen in KPI-berekeningen voor activa.</span><span class="sxs-lookup"><span data-stu-id="23b2d-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="23b2d-115">Doorgaans moeten geplande productieonderbrekingen niet worden opgenomen in KPI-berekeningen, aangezien deze geen invloed hebben op verwachte prestaties.</span><span class="sxs-lookup"><span data-stu-id="23b2d-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="23b2d-116">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-116">Click **Save**.</span></span>

![Figuur 1](media/15-work-orders.png)


<span data-ttu-id="23b2d-118">Wanneer u de redencodes voor uitvaltijd voor onderhoud hebt gemaakt die u wilt gebruiken, kunt u registraties voor uitvaltijd voor onderhoud maken voor werkorders en activa.</span><span class="sxs-lookup"><span data-stu-id="23b2d-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="23b2d-119">Registraties voor uitvaltijd voor onderhoud maken</span><span class="sxs-lookup"><span data-stu-id="23b2d-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="23b2d-120">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="23b2d-121">Selecteer de werkorder en klik op **Uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="23b2d-122">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-122">Click **New**.</span></span>

4. <span data-ttu-id="23b2d-123">Voeg het datum- en tijdinterval voor de registratie van uitvaltijd voor onderhoud in de velden **Van** en **Tot** in.</span><span class="sxs-lookup"><span data-stu-id="23b2d-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="23b2d-124">Wanneer u het veld **Tot** verlaat, wordt de duur in uren automatisch ingevoegd in het veld **Duur**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="23b2d-125">Selecteer een redencode in het veld **Redencode voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="23b2d-126">Herhaal stap 3-6 als u meer registraties wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="23b2d-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="23b2d-127">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-127">Click **Save**.</span></span>


![Figuur 2](media/16-work-orders.png)


<span data-ttu-id="23b2d-129">De kalender die wordt gebruikt voor het berekenen van de registratie van uitvaltijd voor onderhoud is afhankelijk van uw selectie bij het instellen van activa en parameters.</span><span class="sxs-lookup"><span data-stu-id="23b2d-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="23b2d-130">Als een resource wordt geselecteerd voor een activum in **Alle activa** > het sneltabblad **Vaste activa** > het veld **Resource**, wordt de kalender gebruikt die is ingesteld voor de gekoppelde resourcegroep, zoals weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="23b2d-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Figuur 3](media/17-work-orders.png)


<span data-ttu-id="23b2d-132">Als geen resource is geselecteerd voor het activum, wordt de standaardkalender gebruikt die is geselecteerd in het veld **Parameters voor activabeheer**, zoals weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="23b2d-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Figuur 4](media/18-work-orders.png)


<span data-ttu-id="23b2d-134">Klik op **Activabeheer voor bedrijven** > **Query's** > **Uitvaltijd voor onderhoud** voor een overzicht van alle registraties van uitvaltijd voor onderhoud.</span><span class="sxs-lookup"><span data-stu-id="23b2d-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="23b2d-135">Alle kalenders die in de module **Activabeheer** worden gebruikt, worden ingesteld in **Organisatiebeheer** > **Instellingen** > **Kalenders** > **Kalenders**.</span><span class="sxs-lookup"><span data-stu-id="23b2d-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

