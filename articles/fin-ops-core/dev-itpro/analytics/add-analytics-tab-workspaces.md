---
title: Analyses aan werkgebieden toevoegen met Power BI Embedded
description: In dit onderwerp wordt beschreven hoe u een Power BI-rapport insluit op het tabblad Analyses van een werkgebied.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: dd88537506521fd37aa170c7e8f43bcf5a106836
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174346"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="9e48c-103">Analyses aan werkgebieden toevoegen met Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="9e48c-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9e48c-104">Deze functie wordt ondersteund in Finance and Operations (versie 7.2 en hoger).</span><span class="sxs-lookup"><span data-stu-id="9e48c-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="9e48c-105">Inleiding</span><span class="sxs-lookup"><span data-stu-id="9e48c-105">Introduction</span></span>
<span data-ttu-id="9e48c-106">In dit onderwerp wordt beschreven hoe u een Microsoft Power BI-rapport insluit op het tabblad **Analyses** van een werkgebied.</span><span class="sxs-lookup"><span data-stu-id="9e48c-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="9e48c-107">In het hier gebruikte voorbeeld wordt het werkgebied **Reserveringenbeheer** in de toepassing Wagenparkbeheer uitgebreid om een analytisch werkgebied in te sluiten in het tabblad **Analyses**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e48c-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="9e48c-108">Prerequisites</span></span>
+ <span data-ttu-id="9e48c-109">Open een ontwikkelaaromgeving waarop Platformupdate 8 of hoger wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9e48c-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="9e48c-110">Een analyserapport (.pbix-bestand) dat is gemaakt met Microsoft Power BI Desktop-bureaublad en dat een gegevensmodel bevat dat de entiteitsopslagdatabase als bron heeft.</span><span class="sxs-lookup"><span data-stu-id="9e48c-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="9e48c-111">Overzicht</span><span class="sxs-lookup"><span data-stu-id="9e48c-111">Overview</span></span>
<span data-ttu-id="9e48c-112">Of u een bestaand werkgebied van de toepassing uitbreidt of een nieuw werkgebied introduceert, u kunt in beide de ingesloten analytische weergaven gebruiken om begrijpelijke en interactieve weergaven van uw zakelijke gegevens te maken.</span><span class="sxs-lookup"><span data-stu-id="9e48c-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="9e48c-113">Het proces voor het toevoegen van een analytisch werkgebiedtabblad bestaat uit vier stappen.</span><span class="sxs-lookup"><span data-stu-id="9e48c-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="9e48c-114">Een .pbix-bestand toevoegen als een Dynamics 365-resource.</span><span class="sxs-lookup"><span data-stu-id="9e48c-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="9e48c-115">Een tabblad voor het analytische werkgebied definiëren.</span><span class="sxs-lookup"><span data-stu-id="9e48c-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="9e48c-116">De .pbix-resource op het werkgebiedtabblad insluiten.</span><span class="sxs-lookup"><span data-stu-id="9e48c-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="9e48c-117">Optioneel: voeg extensies toe om de weergave aan te passen.</span><span class="sxs-lookup"><span data-stu-id="9e48c-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="9e48c-118">Meer informatie over het maken van analytische rapporten vindt u in [Aan de slag met Power BI Desktop-bureaublad](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="9e48c-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="9e48c-119">Deze pagina bevat veel inzichten waarmee u aantrekkelijke analytische rapportoplossingen kunt maken.</span><span class="sxs-lookup"><span data-stu-id="9e48c-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="9e48c-120">Een .pbix-bestand toevoegen als een resource</span><span class="sxs-lookup"><span data-stu-id="9e48c-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="9e48c-121">Voordat u begint, moet u het Power BI-rapport dat u in het werkgebied wilt insluiten, maken of ophalen.</span><span class="sxs-lookup"><span data-stu-id="9e48c-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="9e48c-122">Meer informatie over het maken van analytische rapporten vindt u in [Aan de slag met Power BI Desktop-bureaublad](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="9e48c-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="9e48c-123">Volg deze stappen om een .pbix-bestand toe te voegen als een Visual Studio-projectartefact.</span><span class="sxs-lookup"><span data-stu-id="9e48c-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="9e48c-124">Maak een nieuw project in het juiste model.</span><span class="sxs-lookup"><span data-stu-id="9e48c-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="9e48c-125">Selecteer het project in Solution Explorer, klik met de rechtermuisknop en selecteer **Toevoegen** \> **Nieuw artikel**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="9e48c-126">Selecteer in het dialoogvenster **Nieuw artikel toevoegen** onder **Operations-artefacten** de sjabloon **Resource**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="9e48c-127">Voer een naam in die wordt gebruikt als referentie voor het rapport in X ++-metagegevens en klik vervolgens op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialoogvenster Nieuw artikel toevoegen](media/analytical-workspace-add.png)

5. <span data-ttu-id="9e48c-129">Zoek het .pbix-bestand dat de definitie van het analytische rapport bevat en klik op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Het dialoogvenster met een bronbestand selecteren](media/analytical-workspace-select-resource.png)

<span data-ttu-id="9e48c-131">Nu u het .pbix-bestand hebt toegevoegd als een Dynamics 365-resource, kunt u rapporten insluiten in werkgebieden en rechtstreekse koppelingen toevoegen via menuopties.</span><span class="sxs-lookup"><span data-stu-id="9e48c-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="9e48c-132">Een tabbesturingselement toevoegen aan een toepassingswerkgebied</span><span class="sxs-lookup"><span data-stu-id="9e48c-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="9e48c-133">In dit voorbeeld breiden we het werkgebied **Reserveringsbeheer** in het model Wagenparkbeheer uit door het toevoegen van het tabblad **Analyses** aan de definitie van het formulier **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="9e48c-134">In de volgende afbeelding ziet u hoe het formulier **FMClerkWorkspace** eruit ziet in de ontwerper in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e48c-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Formulier FMClerkWorkspace voor het wijzigen](media/analytical-workspace-definition-before.png)

<span data-ttu-id="9e48c-136">Volg deze stappen om de formulierdefinitie voor het werkgebied **Reserveringsbeheer** uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="9e48c-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="9e48c-137">Open de formulierontwerper om de ontwerpdefinitie uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="9e48c-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="9e48c-138">Selecteer in de ontwerpdefinitie het bovenste element met de naam **Ontwerp | Patroon: Werkgebied Operationeel**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="9e48c-139">Klik met de rechtermuisknop en selecteer vervolgens **Nieuw** \> **Tabblad** om een nieuw besturingselement toe te voegen met de naam **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="9e48c-140">Selecteer **FormTabControl1** in de formulierontwerper.</span><span class="sxs-lookup"><span data-stu-id="9e48c-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="9e48c-141">Klik met de rechtermuisknop en selecteer **Nieuwe tabbladpagina** om een nieuwe tabbladpagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="9e48c-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="9e48c-142">Wijzig de naam van de tabpagina in iets herkenbaars, zoals **Werkgebied**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="9e48c-143">Selecteer **FormTabControl1** in de formulierontwerper.</span><span class="sxs-lookup"><span data-stu-id="9e48c-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="9e48c-144">Klik met de rechtermuisknop en selecteer **Nieuwe tabbladpagina**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="9e48c-145">Wijzig de naam van de tabbladpagina in iets herkenbaars, zoals **Analyses**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="9e48c-146">Selecteer in de formulierontwerper **Analyses (tabbladpagina)**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="9e48c-147">Stel de eigenschap **Bijschrift** in op **Analyses**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="9e48c-148">Klik met de rechtermuisknop en selecteer vervolgens **Nieuw** \> **Groep** om een besturingselement voor een nieuwe formuliergroep toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="9e48c-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="9e48c-149">Wijzig de naam van de formuliergroepin iets herkenbaars, zoals **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="9e48c-150">Selecteer in de formulierontwerper **PanoramaBody (tabblad)** en sleep het besturingselement naar het tabblad **Werkgebied**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="9e48c-151">Selecteer in de ontwerpdefinitie het bovenste element met de naam **Ontwerp | Patroon: Werkgebied Operationeel**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="9e48c-152">Klik met de rechtermuisknop en selecteer **Patroon verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="9e48c-153">Klik nogmaals met de rechtermuisknop en selecteer **Patroon toevoegen** \> **Werkgebied met tabbladen**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="9e48c-154">Voer een build uit om uw wijzigingen te controleren.</span><span class="sxs-lookup"><span data-stu-id="9e48c-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="9e48c-155">In de volgende afbeelding ziet u hoe het ontwerp eruitziet nadat deze wijzigingen zijn toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e48c-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace na wijzigingen](media/analytical-workspace-definition-after.png)

<span data-ttu-id="9e48c-157">U hebt nu de besturingselementen voor het formulier toegevoegd die worden gebruikt voor het insluiten van het werkgebiedrapport. Vervolgens moet u de grootte van het bovenliggende besturingselement definiëren zodat dit geschikt is voor de lay-out.</span><span class="sxs-lookup"><span data-stu-id="9e48c-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="9e48c-158">Standaard zijn de pagina **Filtervenster** en de pagina **Tabblad** zichtbaar in het rapport.</span><span class="sxs-lookup"><span data-stu-id="9e48c-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="9e48c-159">U kunt echter de zichtbaarheid van deze besturingselementen wijzigen afhankelijk van de eindgebruiker van het rapport.</span><span class="sxs-lookup"><span data-stu-id="9e48c-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="9e48c-160">Voor ingesloten werkgebieden kunt u het beste uitbreidingen gebruiken om de pagina's **Filtervenster** en **Tabblad** te verbergen vanwege de consistentie.</span><span class="sxs-lookup"><span data-stu-id="9e48c-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="9e48c-161">U hebt nu de taak voor het uitbreiden van de formulierdefinitie van de toepassing voltooid.</span><span class="sxs-lookup"><span data-stu-id="9e48c-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="9e48c-162">Voor meer informatie over het gebruik van uitbreidingen en aanpassingen zie [Aanpassen met extensies en overlayering](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="9e48c-162">For more information about how to use extensions to do customizations, see [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="9e48c-163">X ++-bedrijfslogica toevoegen om een besturingselement voor weergave in te sluiten</span><span class="sxs-lookup"><span data-stu-id="9e48c-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="9e48c-164">Volg deze stappen om bedrijfslogica toe te voegen voor het initialiseren van het rapportweergave-besturingselement dat is ingesloten in het werkgebied **Reserveringsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="9e48c-165">Open de formulierontwerper **FMClerkWorkspace** om de ontwerpdefinitie uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="9e48c-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="9e48c-166">Druk op F7 om toegang te krijgen tot de code achter de codedefinitie.</span><span class="sxs-lookup"><span data-stu-id="9e48c-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="9e48c-167">Voeg de volgende X++-code toe:</span><span class="sxs-lookup"><span data-stu-id="9e48c-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="9e48c-168">Voer een build uit om uw wijzigingen te controleren.</span><span class="sxs-lookup"><span data-stu-id="9e48c-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="9e48c-169">U hebt nu de taak voltooid voor het toevoegen van bedrijfslogica voor het initialiseren van het ingesloten rapportweergave-besturingselement.</span><span class="sxs-lookup"><span data-stu-id="9e48c-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="9e48c-170">In de volgende afbeelding ziet u hoe het werkgebied eruitziet nadat deze wijzigingen zijn toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e48c-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Rapport ingesloten in het werkgebied](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="9e48c-172">U kunt de bestaande operationele weergave openen met de werkgebiedtabbladen onder de paginatitel.</span><span class="sxs-lookup"><span data-stu-id="9e48c-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="9e48c-173">Verwijzing</span><span class="sxs-lookup"><span data-stu-id="9e48c-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="9e48c-174">Methode PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="9e48c-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="9e48c-175">Deze sectie bevat informatie over de helperklasse die wordt gebruikt om een Power BI-rapport (.pbix-resource) in te sluiten in een besturingselement voor een formuliergroep.</span><span class="sxs-lookup"><span data-stu-id="9e48c-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="9e48c-176">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9e48c-176">Syntax</span></span>
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="9e48c-177">Parameters</span><span class="sxs-lookup"><span data-stu-id="9e48c-177">Parameters</span></span>

| <span data-ttu-id="9e48c-178">Naam</span><span class="sxs-lookup"><span data-stu-id="9e48c-178">Name</span></span>             | <span data-ttu-id="9e48c-179">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="9e48c-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e48c-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="9e48c-180">resourceName</span></span>     | <span data-ttu-id="9e48c-181">De naam van de .pbix-resource.</span><span class="sxs-lookup"><span data-stu-id="9e48c-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="9e48c-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="9e48c-182">formGroupControl</span></span> | <span data-ttu-id="9e48c-183">Het besturingselement van de formuliergroep waarop het Power BI-rapportbesturingselement wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e48c-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="9e48c-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="9e48c-184">defaultPageName</span></span>  | <span data-ttu-id="9e48c-185">De standaardpaginanaam.</span><span class="sxs-lookup"><span data-stu-id="9e48c-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="9e48c-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="9e48c-186">showFilterPane</span></span>   | <span data-ttu-id="9e48c-187">Een Booleaanse waarde die aangeeft of het filtervenster moet worden weergegeven (**true**) of verborgen (**false**).</span><span class="sxs-lookup"><span data-stu-id="9e48c-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="9e48c-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="9e48c-188">showNavPane</span></span>      | <span data-ttu-id="9e48c-189">Een Booleaanse waarde die aangeeft of het navigatievenster moet worden weergegeven (**true**) of verborgen (**false**).</span><span class="sxs-lookup"><span data-stu-id="9e48c-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="9e48c-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="9e48c-190">defaultFilters</span></span>   | <span data-ttu-id="9e48c-191">De standaardfilters voor het Power BI-rapport.</span><span class="sxs-lookup"><span data-stu-id="9e48c-191">The default filters for the Power BI report.</span></span>                                                                 |