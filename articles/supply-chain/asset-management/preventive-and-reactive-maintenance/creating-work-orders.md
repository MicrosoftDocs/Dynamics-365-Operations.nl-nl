---
title: Werkorders maken
description: In dit onderwerp wordt uitgelegd hoe u werkorders maakt in Activabeheer.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131788"
---
# <a name="creating-work-orders"></a><span data-ttu-id="5b379-103">Werkorders maken</span><span class="sxs-lookup"><span data-stu-id="5b379-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b379-104">Nadat u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken.</span><span class="sxs-lookup"><span data-stu-id="5b379-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="5b379-105">U kunt deze stap uitvoeren met een van de onderhoudsschema's.</span><span class="sxs-lookup"><span data-stu-id="5b379-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="5b379-106">De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben, zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="5b379-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="5b379-107">Verwijzingstype</span><span class="sxs-lookup"><span data-stu-id="5b379-107">Reference type</span></span> | <span data-ttu-id="5b379-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5b379-108">Description</span></span> |
|---|---|
| <span data-ttu-id="5b379-109">Onderhoudsplannen</span><span class="sxs-lookup"><span data-stu-id="5b379-109">Maintenance plans</span></span> | <span data-ttu-id="5b379-110">Taken voor preventief onderhoud op basis van de typen onderhoudsplan *Tijd* of *Teller*.</span><span class="sxs-lookup"><span data-stu-id="5b379-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="5b379-111">Onderhoudsrondes</span><span class="sxs-lookup"><span data-stu-id="5b379-111">Maintenance rounds</span></span> | <span data-ttu-id="5b379-112">Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist.</span><span class="sxs-lookup"><span data-stu-id="5b379-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="5b379-113">Onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="5b379-113">Maintenance request</span></span> | <span data-ttu-id="5b379-114">Een handmatig gemaakte aanvraag voor onderhoud of reparatie van een activum.</span><span class="sxs-lookup"><span data-stu-id="5b379-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="5b379-115">Deze aanvraag kan worden geconverteerd naar een werkorder.</span><span class="sxs-lookup"><span data-stu-id="5b379-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="5b379-116">Werkorders maken op basis van uw onderhoudsschema</span><span class="sxs-lookup"><span data-stu-id="5b379-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="5b379-117">Volg deze stappen om werkorders te maken op basis van uw onderhoudsschema.</span><span class="sxs-lookup"><span data-stu-id="5b379-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="5b379-118">Open een van de volgende pagina's, afhankelijk van hoe u schema-artikelen voor uw werkorders wilt selecteren:</span><span class="sxs-lookup"><span data-stu-id="5b379-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="5b379-119">Alle onderhoudsschema's (**Activabeheer \> Beheerschema \> Alle onderhoudsschema's**)</span><span class="sxs-lookup"><span data-stu-id="5b379-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="5b379-120">Open onderhoudsschemaregels (**Activabeheer \> Beheerschema \> Alle onderhoudsschemaregels**)</span><span class="sxs-lookup"><span data-stu-id="5b379-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="5b379-121">Open onderhoudsschemagroepen (**Activabeheer \> Beheerschema \> Onderhoudsschemagroepen openen**)</span><span class="sxs-lookup"><span data-stu-id="5b379-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="5b379-122">Schakel in het raster het selectievakje in voor elke geplande onderhoudstaak waarvoor u een werkorder wilt maken.</span><span class="sxs-lookup"><span data-stu-id="5b379-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="5b379-123">Selecteer vervolgens in het actievenster **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="5b379-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="5b379-124">Het dialoogvenster **Werkorders maken** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5b379-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="5b379-125">Het veld **Prognose voor onderhoudsuren** toont het totaal aantal geraamde uren voor de geselecteerde regels.</span><span class="sxs-lookup"><span data-stu-id="5b379-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Dialoogvenster Werkorders maken](media/18-preventive-maintenance.png)

1. <span data-ttu-id="5b379-127">Geef in de sectie **Parameters** het aantal werkorders op dat u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="5b379-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="5b379-128">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="5b379-128">Select one of the following options:</span></span>

    - <span data-ttu-id="5b379-129">**Eén werkorder per regel** – Eén werkorder per onderhoudsschemaregel maken.</span><span class="sxs-lookup"><span data-stu-id="5b379-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="5b379-130">**Eén werkorder per** – Werkorders maken die gegroepeerd zijn volgens de instellingen van de andere opties die beschikbaar worden wanneer u deze optie selecteert.</span><span class="sxs-lookup"><span data-stu-id="5b379-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="5b379-131">Selecteer in het veld **Werkordertype** het werkordertype dat u wilt gebruiken voor alle werkorders die u maakt.</span><span class="sxs-lookup"><span data-stu-id="5b379-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="5b379-132">Selecteer **OK** om de werkorders volgens uw instellingen te maken.</span><span class="sxs-lookup"><span data-stu-id="5b379-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="5b379-133">Werkorderregels groeperen die automatisch worden gemaakt terwijl een onderhoudsplan wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="5b379-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b379-134">De functionaliteit die in deze sectie wordt beschreven, is beschikbaar als onderdeel van een beperkte previewversie.</span><span class="sxs-lookup"><span data-stu-id="5b379-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="5b379-135">De inhoud en de functies kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="5b379-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="5b379-136">Meer informatie over preview-versies vindt u in [Veelgestelde vragen over updates van service met één versie](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="5b379-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="5b379-137">Met deze functie kunt u regels definiëren voor het groeperen van werkorderregels onder één werkorder wanneer het systeem is ingesteld om automatisch werkorders te genereren op basis van een onderhoudsplan.</span><span class="sxs-lookup"><span data-stu-id="5b379-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="5b379-138">Eerder automatisch gegenereerde werkorders kunnen slechts één regel bevatten.</span><span class="sxs-lookup"><span data-stu-id="5b379-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="5b379-139">U kunt werkorders nu echter wel groeperen op bijvoorbeeld activa, activatype of functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="5b379-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="5b379-140">(Handmatig gegenereerde werkorders konden al op deze manier worden gegroepeerd, zoals wordt beschreven in de vorige sectie van dit onderwerp.)</span><span class="sxs-lookup"><span data-stu-id="5b379-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="5b379-141">Groepering inschakelen voor automatisch gegenereerde werkorders</span><span class="sxs-lookup"><span data-stu-id="5b379-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="5b379-142">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="5b379-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="5b379-143">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5b379-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="5b379-144">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="5b379-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5b379-145">**Module:** *Activabeheer*</span><span class="sxs-lookup"><span data-stu-id="5b379-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="5b379-146">**Functienaam:** *(Preview) Regels toepassen voor het groeperen van werkorders tijdens het uitvoeren van een onderhoudsplan*</span><span class="sxs-lookup"><span data-stu-id="5b379-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="5b379-147">Groepering instellen voor automatisch gegenereerde werkorders</span><span class="sxs-lookup"><span data-stu-id="5b379-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="5b379-148">Volg deze stappen om groepering in te stellen voor automatisch gegenereerde werkorders.</span><span class="sxs-lookup"><span data-stu-id="5b379-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="5b379-149">Ga naar **Activabeheer \> Instellen \> Preventief onderhoud \> Onderhoudsplannen**.</span><span class="sxs-lookup"><span data-stu-id="5b379-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="5b379-150">Volg deze stappen voor elk plan waarin u gegroepeerde werkorders wilt genereren:</span><span class="sxs-lookup"><span data-stu-id="5b379-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="5b379-151">Selecteer het plan in het lijstvenster.</span><span class="sxs-lookup"><span data-stu-id="5b379-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="5b379-152">Controleer op sneltabblad **Regels** of het selectievakje **Automatisch maken** op elke regel is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5b379-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="5b379-153">Ga naar **Activabeheer \> Periodiek \> Preventief onderhoud \> Onderhoudsplannen plannen**.</span><span class="sxs-lookup"><span data-stu-id="5b379-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="5b379-154">Geef in het dialoogvenster **Onderhoudsplannen plannen** in de sectie **Periode** de tijdshorizon op voor het plan (hoe ver vooruit moet worden gekeken bij het zoeken naar geplande onderhoudstaken om werk voor te genereren).</span><span class="sxs-lookup"><span data-stu-id="5b379-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="5b379-155">Stel de optie **Automatisch maken van werkorder vanuit schema** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="5b379-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="5b379-156">Selecteer in het gedeelte **Werkorder** een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="5b379-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="5b379-157">**Eén werkorder per regel** – Eén werkorder per onderhoudsschemaregel maken.</span><span class="sxs-lookup"><span data-stu-id="5b379-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="5b379-158">(Deze optie biedt dezelfde functionaliteit die beschikbaar is wanneer de functie *Regels toepassen voor het groeperen van werkorders tijdens het uitvoeren van een onderhoudsplan* is uitgeschakeld.)</span><span class="sxs-lookup"><span data-stu-id="5b379-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="5b379-159">**Eén werkorder per** – Werkorders maken die gegroepeerd zijn volgens de instellingen van de andere opties die beschikbaar worden wanneer u deze optie selecteert.</span><span class="sxs-lookup"><span data-stu-id="5b379-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="5b379-160">Als u wilt dat de opties worden toegepast wanneer u slechts enkele van uw onderhoudsplannen uitvoert, voegt u op het tabblad **Op te nemen records** desgewenst filters toe, net als voor andere batchtaken in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5b379-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="5b379-161">Stel op het sneltabblad **Uitvoeren op achtergrond** desgewenst batch- en planningsopties in, op dezelfde manier als u doet voor andere batchtaken in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5b379-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="5b379-162">Selecteer **OK** om de geselecteerde onderhoudsplannen uit te voeren en/of te plannen.</span><span class="sxs-lookup"><span data-stu-id="5b379-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
