---
title: Onderhoudsrondes
description: In dit onderwerp wordt uitgelegd wat onderhoudsronden zijn in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: eca732f245650c8e1f3dc976454536a0ab1ee117
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922017"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="fd0e4-103">Onderhoudsrondes</span><span class="sxs-lookup"><span data-stu-id="fd0e4-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fd0e4-104">In **Activabeheer** kunt u onderhoudsronden maken voor verschillende activa. Daarop kunt u met regelmatige tussenpozen een soortgelijke taak uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="fd0e4-105">Bijvoorbeeld smeertaken of veiligheidsinspectietaken die voor een aantal machines binnen dezelfde intervallen moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="fd0e4-106">De eerste stap bestaat uit het maken van een onderhoudsronde, inclusief activa waarvoor eenzelfde onderhoudstaak moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="fd0e4-107">Vervolgens plant u de onderhoudsronden.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="fd0e4-108">Wanneer u de planning van de onderhoudsronden hebt voltooid, kunt u alle taakrecords voor de ronden bekijken in **Hele onderhoudsschema** en **Openstaande onderhoudsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="fd0e4-109">Op het moment dat een op ronde gebaseerde werkorder wordt gemaakt, kunnen onderhoudsronden ook worden ingesteld voor functionele locaties als deze ronden moeten worden voltooid voor de activa die op de functionele locatie zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="fd0e4-110">Zie [Functionele locaties maken](../functional-locations/create-functional-locations.md) voor meer informatie over het instellen van onderhoudsronden voor functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="fd0e4-111">Een onderhoudsronde instellen</span><span class="sxs-lookup"><span data-stu-id="fd0e4-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="fd0e4-112">Klik op **Activabeheer** > **Instellen** > **Preventief onderhoud** > **Onderhoudsronden**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="fd0e4-113">Klik op **Nieuw** om een nieuwe onderhoudsronde te maken.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="fd0e4-114">Type een id in het veld **Onderhoudsronde** en een naam voor de onderhoudsronde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="fd0e4-115">Selecteer een begindatum voor de ronde in het veld **Begindatum**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="fd0e4-116">In de velden **Voltooien binnen dagen** en **Voltooien binnen uren** kunt u de verwachte einddatum in dagen of uren invoegen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="fd0e4-117">De verwachte einddatum wordt berekend ten opzichte van de begindatum. Deze wordt berekend wanneer de onderhoudsschemaregels worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="fd0e4-118">Zo kunt u 7 in het veld **Voltooien binnen dagen** invoeren als u wilt aangeven dat de betreffende taak binnen een week vanaf de begindatum moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="fd0e4-119">Selecteer Ja op de wisselknop **Automatisch maken** als werkorders automatisch moeten worden gemaakt op basis van onderhoudsschemaregels die op basis van deze onderhoudsronde zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="fd0e4-120">Selecteer in het veld **Werkordertype** het werkordertype dat moet worden gebruikt voor werkorders die zijn gemaakt op basis van deze onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="fd0e4-121">Selecteer in het veld **Serviceniveau** het serviceniveau voor de werkorder dat moet worden gebruikt voor werkorders die zijn gemaakt op basis van deze onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="fd0e4-122">Klik op het sneltabblad **Activaregels** op **Toevoegen** om een activum aan de onderhoudsronde toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="fd0e4-123">In het veld **Regelnummer** wordt automatisch een regelnummer ingevoegd om de volgorde van de activa in de onderhoudsronde aan te geven.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="fd0e4-124">Selecteer het activum in het veld **Activum**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="fd0e4-125">Selecteer het type onderhoudstaak voor het activum in het veld **Type onderhoudstaak**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="fd0e4-126">Selecteer zo nodig **Variant van type onderhoudstaak** en **Handel** voor het type onderhoudstaak.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="fd0e4-127">Selecteer het terugkeerpatroon (dag, week enzovoort) in het veld **Periodetype**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="fd0e4-128">Voer in het veld **Periodefrequentie** het aantal herhalingen voor de onderhoudsronde in.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="fd0e4-129">Voorbeeld: als u in het veld **Periodetype** de optie Dag hebt geselecteerd en u het getal 7 in dit veld opgeeft, worden er eenmaal per week nieuwe onderhoudsronderegels gemaakt tijdens de planning van preventief onderhoud.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="fd0e4-130">Selecteer in het veld **Begindatum** een begindatum voor het activum dat u wilt opnemen in de onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="fd0e4-131">Deze datum kan verschillen van de begindatum die is ingesteld in de onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="fd0e4-132">Herhaal stap 9 tot en met 16 als u meer activa aan de onderhoudsronde wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="fd0e4-133">Klik op het sneltabblad **Regels voor functionele locatie** op **Toevoegen** om een functionele locatie aan de onderhoudsronde toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="fd0e4-134">Zie de beschrijving van de betreffende velden hierboven.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="fd0e4-135">Dezelfde velden zijn beschikbaar voor het maken van een activumregel, maar u kunt indien nodig ook **Fabrikant** en **Model** voor een functionele locatie selecteren.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="fd0e4-136">Als u alleen een functionele locatie op een regel selecteert, maar geen selecties opgeeft in **Activatype**, **Fabrikant**, **Model**, **Type onderhoudstaak**, **Variant van type onderhoudstaak** en **Handel**, worden alle activa voor deze functionele locatie op het moment van de onderhoudsplanning opgenomen in de onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="fd0e4-137">Klik op het sneltabblad **Groepen** op **Toevoegen** om een werkordergroep te selecteren die u wilt opnemen in de onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="fd0e4-138">Verschillende werkordergroepen kunnen worden gekoppeld aan één onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="fd0e4-139">Sla de instellingen op.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="fd0e4-140">In de velden **Activa** en **Regels** in de groep **Details** van het sneltabblad **Koptekst** ziet u het totaal aantal activa en regels voor de geselecteerde onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="fd0e4-141">In de onderstaande afbeelding ziet u een voorbeeld van een onderhoudsronde die drie activa bevat.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Figuur 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="fd0e4-143">Onderhoudsrondes plannen</span><span class="sxs-lookup"><span data-stu-id="fd0e4-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="fd0e4-144">Wanneer u een onderhoudsronde hebt ingesteld, voert u een planningstaak uit om alle taken voor de onderhoudsronde te plannen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="fd0e4-145">Klik op **Activabeheer** > **Periodiek** > **Preventief onderhoud** > **Onderhoudsronden plannen**, of **Activabeheer** > **Algemeen** > **Onderhoudsschema** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen** > selecteer een onderhoudsschemaregel in de lijst > knop **Onderhoudsronden**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="fd0e4-146">Selecteer in het veld **Periode** het periodetype dat u voor de planningstaak wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="fd0e4-147">Voer in het veld **Periodefrequentie** het aantal perioden in dat u in de planningstaak wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="fd0e4-148">De huidige datum is de begindatum van de planning.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="fd0e4-149">Selecteer Ja op de wisselknop **Automatisch maken** als een werkorder automatisch moet worden gemaakt op basis van een onderhoudsronde.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="fd0e4-150">Als deze wisselknop is ingesteld op Ja en de wisselknop **Automatisch maken** voor de onderhoudsronde in het formulier **Onderhoudsronden** ook is ingeschakeld op Ja, worden werkorders gemaakt op basis van de regels in de onderhoudsronde en worden onderhoudsschemaregels met de status 'Werkorder gemaakt' ook gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="fd0e4-151">Als slechts een van de wisselknoppen voor **Automatisch maken** in deze vervolgkeuzelijst of in **Onderhoudsronden** is ingesteld op Ja, worden alleen regels in onderhoudsronden gemaakt die de status Gemaakt hebben.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="fd0e4-152">In dat geval worden er geen werkorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="fd0e4-153">U kunt zo nodig specifieke ronden of een andere begindatum voor de planningstaak selecteren.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="fd0e4-154">Klik op **Filter** en voeg de ronden toe die u wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="fd0e4-155">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-155">Click **OK**.</span></span>

7. <span data-ttu-id="fd0e4-156">Nu kunt u de taken van de onderhoudsronden bekijken in **Activabeheer** > **Algemeen** > **Onderhoudsschema** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="fd0e4-157">Als de geplande ronden zijn gekoppeld aan een werkordergroep, ziet u ook onderhoudsschemaregels in **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="fd0e4-158">Onderhoudsschemaregels op basis van een ronde hebben het verwijzingstype Onderhoudsronden.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="fd0e4-159">In de twee illustraties hieronder ziet u een planningstaak in het dialoogvenster **Onderhoudsronden plannen** en de onderhoudsplanningsregels die op basis van die planningstaak zijn gemaakt in **Alle onderhoudsschema's**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Figuur 2](media/14-preventive-maintenance.png)

![Figuur 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="fd0e4-162">Wanneer werkorders handmatig worden gemaakt voor activa die onder een leveranciersgarantie vallen, wordt er een dialoogvenster weergegeven om de gebruiker te informeren over de garantie.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="fd0e4-163">Het maken van de werkorder kan dan worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="fd0e4-164">De controle op een garantierelatie wordt achterwege gelaten voor werkorders die automatisch worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="fd0e4-165">U kunt een batchtaak instellen op het sneltabblad **Op de achtergrond uitvoeren** als u de ronden met vaste intervallen wilt plannen.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="fd0e4-166">Als een ronde is opgenomen in verschillende werkordergroepen (zie [Werkordergroepen](../work-orders/work-order-pools.md)), wordt één record voor elke groep weergegeven in **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="fd0e4-167">Dit wordt gedaan om de filteropties voor werkordergroepen te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-167">This is done to optimize the filtering options for work order pools.</span></span>

