---
title: Uitvaltijd voor onderhoud
description: In dit onderwerp wordt uitvaltijd voor onderhoud in Activabeheer beschreven.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad9f1b2a0e63b4fb0d6daceb451c3a1dc1ec7de7
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626143"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="29654-103">Uitvaltijd voor onderhoud</span><span class="sxs-lookup"><span data-stu-id="29654-103">Maintenance downtime</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="29654-104">U kunt registraties voor uitvaltijd voor onderhoud maken voor de geselecteerde activa in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="29654-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="29654-105">Deze functie is handig als u de uitvaltijd voor onderhoud voor een of meer machines in het productiegebied wilt registreren.</span><span class="sxs-lookup"><span data-stu-id="29654-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="29654-106">Eerst maakt u de redencodes voor uitvaltijd voor onderhoud die u wilt gebruiken, bijvoorbeeld **Storing** en **Geplande beëindiging**.</span><span class="sxs-lookup"><span data-stu-id="29654-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="29654-107">Deze stap wordt uitgevoerd op de pagina **Redencodes voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="29654-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="29654-108">Vervolgens kunt u registraties voor uitvaltijd voor onderhoud maken op de pagina **Uitvaltijd voor onderhoud** en de relevante redencodes voor uitvaltijd toevoegen.</span><span class="sxs-lookup"><span data-stu-id="29654-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="29654-109">Redencodes voor uitvaltijd voor onderhoud maken</span><span class="sxs-lookup"><span data-stu-id="29654-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="29654-110">Selecteer **Activabeheer** > **Instellingen** > **Werkorders** > **Redencodes voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="29654-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="29654-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="29654-111">Select **New**.</span></span>

3. <span data-ttu-id="29654-112">Voer in het veld **Redencode voor uitvaltijd voor onderhoud** een id in voor de redencode voor uitvaltijd voor onderhoud.</span><span class="sxs-lookup"><span data-stu-id="29654-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="29654-113">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="29654-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="29654-114">Schakel het selectievakje **KPI opnemen** in als de redencode moet worden opgenomen in berekeningen van KPI's voor de activa.</span><span class="sxs-lookup"><span data-stu-id="29654-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="29654-115">Doorgaans moeten geplande productieonderbrekingen niet worden opgenomen in KPI-berekeningen, omdat deze geen invloed hebben op verwachte prestaties.</span><span class="sxs-lookup"><span data-stu-id="29654-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="29654-116">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="29654-116">Select **Save**.</span></span>

<span data-ttu-id="29654-117">In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Redencodes voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="29654-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Figuur 1](media/15-work-orders.png)

<span data-ttu-id="29654-119">Nadat u de redencodes voor uitvaltijd voor onderhoud hebt gemaakt die u wilt gebruiken, kunt u registraties voor uitvaltijd voor onderhoud maken voor werkorders en activa.</span><span class="sxs-lookup"><span data-stu-id="29654-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="29654-120">Registraties voor uitvaltijd voor onderhoud maken</span><span class="sxs-lookup"><span data-stu-id="29654-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="29654-121">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="29654-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="29654-122">Selecteer de werkorder en selecteer vervolgens op het tabblad **Werkorder** in de groep **Activum** de optie **Uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="29654-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="29654-123">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="29654-123">Select **New**.</span></span>

4. <span data-ttu-id="29654-124">Bepaal het datum- en tijdinterval voor de registratie van uitvaltijd voor onderhoud in de velden **Van** en **Tot**.</span><span class="sxs-lookup"><span data-stu-id="29654-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="29654-125">Wanneer u het veld **Tot** verlaat, wordt de duur in uren automatisch ingevoegd in het veld **Duur**.</span><span class="sxs-lookup"><span data-stu-id="29654-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="29654-126">Selecteer een redencode in het veld **Redencode voor uitvaltijd voor onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="29654-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="29654-127">Herhaal stap 3 en 5 als u nog meer registraties wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="29654-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="29654-128">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="29654-128">Select **Save**.</span></span>

<span data-ttu-id="29654-129">In de onderstaande afbeelding ziet u een voorbeeld van een registratie voor uitvaltijd voor onderhoud.</span><span class="sxs-lookup"><span data-stu-id="29654-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Figuur 2](media/16-work-orders.png)

<span data-ttu-id="29654-131">De kalender die wordt gebruikt voor het berekenen van de registratie van uitvaltijd voor onderhoud is afhankelijk van uw selectie bij het instellen van activa en parameters.</span><span class="sxs-lookup"><span data-stu-id="29654-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="29654-132">Als een resource wordt geselecteerd voor een activum in het veld **Resource** op het het sneltabblad **Vaste activa** van de pagina **Alle activa**, wordt de kalender gebruikt die is ingesteld voor de gekoppelde resourcegroep, zoals weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="29654-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Figuur 3](media/17-work-orders.png)

<span data-ttu-id="29654-134">Als geen resource is geselecteerd voor het activum, wordt de standaardkalender gebruikt die is geselecteerd op de pagina **Parameters voor activabeheer**, zoals weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="29654-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Figuur 4](media/18-work-orders.png)

<span data-ttu-id="29654-136">Klik op **Activabeheer voor bedrijven** > **Query's** > **Uitvaltijd voor onderhoud** voor een overzicht van alle registraties van uitvaltijd voor onderhoud.</span><span class="sxs-lookup"><span data-stu-id="29654-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="29654-137">Alle kalenders die in de module **Activabeheer** worden gebruikt, worden ingesteld in **Organisatiebeheer** > **Instellingen** > **Kalenders** > **Kalenders**.</span><span class="sxs-lookup"><span data-stu-id="29654-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

