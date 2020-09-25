---
title: Prestaties van projectresourceplanning
description: Dit onderwerp bevat informatie over het verbeteren van de prestaties van de resourceplanning voor een groot aantal projecten.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760519"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="05b98-103">Prestaties van projectresourceplanning</span><span class="sxs-lookup"><span data-stu-id="05b98-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="05b98-104">Prestatieproblemen met betrekking tot resourceplanning kunnen zich voordoen wanneer het aantal projecten in de duizenden loopt.</span><span class="sxs-lookup"><span data-stu-id="05b98-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="05b98-105">Als u de prestaties van de resourceplanning wilt verbeteren, is er een functie beschikbaar waarmee gebruikers de tijd kunnen beperken die nodig is om het formulier voor resourcebeschikbaarheid te starten.</span><span class="sxs-lookup"><span data-stu-id="05b98-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="05b98-106">Hiermee verwijdert u het synchronisatieproces voor de vergaarde resourcecapaciteit en u gebruikt de tabel **ResProjectResource** om het opzoeken van resources te versnellen.</span><span class="sxs-lookup"><span data-stu-id="05b98-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="05b98-107">De tabel **ResRollup** wordt niet meer gebruikt.</span><span class="sxs-lookup"><span data-stu-id="05b98-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05b98-108">Als er een afhankelijkheid van het synchronisatieproces voor de vergaarde resourcecapaciteit of de tabel **ResprojectResource** bestaat, gebruikt u deze functie niet.</span><span class="sxs-lookup"><span data-stu-id="05b98-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="05b98-109">Prestatieverbetering voor resourceplanning inschakelen</span><span class="sxs-lookup"><span data-stu-id="05b98-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="05b98-110">Voer de volgende stappen uit om de prestatieverbetering voor resourceplanning in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="05b98-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="05b98-111">Ga naar **Functiebeheer** > **Alle** en zoek in de lijst met functies naar **Functie voor verbetering van prestaties van projectresourceplanning inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="05b98-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="05b98-112">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="05b98-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="05b98-113">Als u de functie niet kunt vinden in de lijst, selecteert u **Controleren op updates** om de lijst te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="05b98-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="05b98-114">Vernieuw de browser en ga vervolgens naar **Projectbeheer en boekhouding** > **Periodiek** > **Projectresources** > **Capaciteit van resourcekalenders synchroniseren voor alle bedrijven**.</span><span class="sxs-lookup"><span data-stu-id="05b98-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="05b98-115">Stel **Bestaande capaciteitsrecords verwijderen** in op **Ja** als u eerdere gegevens wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="05b98-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="05b98-116">Als u incrementele gegevens wilt genereren, stelt u deze optie in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="05b98-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="05b98-117">Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="05b98-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="05b98-118">Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.</span><span class="sxs-lookup"><span data-stu-id="05b98-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="05b98-119">Als u het veld **Periodecode** leeg laat, selecteert u specifieke begin- en einddatums om gegevens te genereren.</span><span class="sxs-lookup"><span data-stu-id="05b98-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="05b98-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05b98-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="05b98-121">Er worden nu algemene gegevens naar de tabel **ResCalendarCapacity** gedistribueerd voor alle bedrijven in uw omgeving, zodat de batchtaak alleen in één rechtspersoon hoeft te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="05b98-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="05b98-122">De gegevens in deze batchtaak zijn nodig om de resourcecapaciteit te berekenen via de bijbehorende kalender.</span><span class="sxs-lookup"><span data-stu-id="05b98-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="05b98-123">Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Projectresources** > **Projectresources invullen voor alle bedrijven** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05b98-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="05b98-124">Dit is het script voor gegevensupgrades voor algemene gegevens in de tabellen **ResProjectResource**, **ResCalendarDateTimeRange** en **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="05b98-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="05b98-125">Waarden voor het veld **PSAPRojSchedRole.RootActivity** worden ook bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="05b98-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="05b98-126">Als deze bewerking niet wordt uitgevoerd, wordt een waarschuwing weergegeven wanneer u probeert om resourceplanningsbewerkingen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="05b98-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="05b98-127">Prestatieverbetering voor resourceplanning uitschakelen</span><span class="sxs-lookup"><span data-stu-id="05b98-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="05b98-128">Ga naar **Functiebeheer** > **Alle** en zoek naar **Functie voor verbetering van prestaties van projectresourceplanning inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="05b98-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="05b98-129">Selecteer de functie en de knop **Uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="05b98-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="05b98-130">Vernieuw de browser.</span><span class="sxs-lookup"><span data-stu-id="05b98-130">Refresh your browser.</span></span>
4. <span data-ttu-id="05b98-131">Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Capaciteitsynchronisatie** > **Vergaarde resourcecapaciteit synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="05b98-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="05b98-132">Stel op de pagina **Synchronisatie van vergaarde capaciteit** de optie **Bestaande capaciteitsrecords verwijderen** in op **Ja** om eerdere gegevens te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="05b98-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="05b98-133">Als u incrementele gegevens wilt genereren, stelt u deze optie in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="05b98-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="05b98-134">Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="05b98-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="05b98-135">Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.</span><span class="sxs-lookup"><span data-stu-id="05b98-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="05b98-136">Als u het veld **Periodecode** leeg laat, selecteert u specifieke begin- en einddatums om gegevens te genereren.</span><span class="sxs-lookup"><span data-stu-id="05b98-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="05b98-137">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05b98-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="05b98-138">Er worden nu algemene gegevens naar de tabel **ResRollup** gedistribueerd voor alle bedrijven in uw omgeving, zodat de batchtaak alleen in één rechtspersoon hoeft te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="05b98-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="05b98-139">Deze batchtaak is nodig voor alle weergaven **Beschikbaarheid van resource**.</span><span class="sxs-lookup"><span data-stu-id="05b98-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="05b98-140">Als deze batchtaak niet wordt uitgevoerd, worden de gegevens in **ResRollup** al doende gegenereerd. Dit kan tijd kosten.</span><span class="sxs-lookup"><span data-stu-id="05b98-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
