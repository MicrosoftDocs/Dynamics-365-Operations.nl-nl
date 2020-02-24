---
title: Tekstafbreking in de positiehiërarchie vermijden en exporteren naar Visio
description: In dit artikel wordt uitgelegd hoe u het probleem oplost dat namen van personen en posities worden afgekapt wanneer klanten de positiehiërarchie weergeven in Microsoft Dynamics 365 Human Resources. Tekstafbreking kan het moeilijk maken om een schermopname te maken of de hiërarchie af te drukken.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39ac850b70974dd15906039293bb6c60492da324
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008636"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="6de34-104">Tekstafbreking in de positiehiërarchie vermijden en exporteren naar Visio</span><span class="sxs-lookup"><span data-stu-id="6de34-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

<span data-ttu-id="6de34-105">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="6de34-105">**Issue**</span></span>

<span data-ttu-id="6de34-106">Als een klant de positiehiërarchie weergeeft in Microsoft Dynamics 365 Human Resources, worden de namen van personen en posities afgebroken.</span><span class="sxs-lookup"><span data-stu-id="6de34-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="6de34-107">Daarom kan het lastig zijn om een schermopname te maken of de hiërarchie af te drukken en te distribueren.</span><span class="sxs-lookup"><span data-stu-id="6de34-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Positiehiërarchie](media/position-h.png)

<span data-ttu-id="6de34-109">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="6de34-109">**Cause**</span></span>

<span data-ttu-id="6de34-110">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="6de34-110">This behavior is by design.</span></span>

<span data-ttu-id="6de34-111">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="6de34-111">**Resolution**</span></span>

<span data-ttu-id="6de34-112">Helaas kunnen gebruikers de grootte van de tekst niet gemakkelijk wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6de34-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="6de34-113">U kunt de positiehiërarchie echter uit Human Resources exporteren en vervolgens importeren in Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6de34-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="6de34-114">Hoewel het volgende artikel is geschreven voor Microsoft Dynamics AX 2012, is het proces ook van toepassing op Human Resources: [Een positiehiërarchie exporteren naar Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="6de34-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="6de34-115">Volg deze stappen om te exporteren naar Visio.</span><span class="sxs-lookup"><span data-stu-id="6de34-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="6de34-116">Open in Human Resources de lijstpagina **Posities**.</span><span class="sxs-lookup"><span data-stu-id="6de34-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="6de34-117">Als u meer informatie in het diagram van de structuur van organisatie wilt opnemen, voegt u velden toe aan de lijst **Posities**, zodat deze beschikbaar zijn wanneer u de wizard verderop in deze procedure gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6de34-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="6de34-118">Selecteer in het actievenster de knop **Openen in Microsoft Office** en selecteer vervolgens onder **Exporteren naar Excel** de optie **Posities**.</span><span class="sxs-lookup"><span data-stu-id="6de34-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="6de34-119">Of druk op Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="6de34-119">Alternatively, press Ctrl+T.</span></span>

    ![De lijstpagina Posities exporteren naar Excel](media/org-admin.png)

3. <span data-ttu-id="6de34-121">Sla het geëxporteerde Excel-bestand op.</span><span class="sxs-lookup"><span data-stu-id="6de34-121">Save the Excel file that is exported.</span></span>

    ![Het dialoogvenster Exporteren naar Excel](media/export-excel.png)

4. <span data-ttu-id="6de34-123">Selecteer in Visio de optie **Visio - Nieuwe maken** en selecteer de sjablooncategorie **Zakelijk**.</span><span class="sxs-lookup"><span data-stu-id="6de34-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Nieuw diagram](media/new.png)

5. <span data-ttu-id="6de34-125">Selecteer **Wizard Organigram** en vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="6de34-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Het dialoogvenster Wizard Organigram](media/orgchart-wizard.png)

6. <span data-ttu-id="6de34-127">Selecteer **Gegevens die al zijn opgeslagen in een bestand of database** en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6de34-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Wizard Organigram 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="6de34-129">Kies **Een tekst-, Org Plus- (\*.txt) of Excel-bestand** en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6de34-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Wizard Organigram 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="6de34-131">Ga naar het geëxporteerde Excel-bestand met de positiehiërarchie en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6de34-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Wizard Organigram 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="6de34-133">Stel het veld **Naam** in op **Positie**, stel het veld **Rapporteert aan** in op **Verantwoording aan positie** en selecteer vervolgens **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6de34-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Wizard Organigram 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="6de34-135">Selecteer de velden die moeten worden weergegeven voor elk knooppunt en selecteer vervolgens **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6de34-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Wizard Organigram 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="6de34-137">Voeg de kolom **Positie** toe aan de lijst **Shapegegevensvelden** en selecteer vervolgens **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6de34-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Wizard Organigram 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="6de34-139">Afbeeldingen zijn momenteel niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="6de34-139">Pictures aren't currently available.</span></span> <span data-ttu-id="6de34-140">Selecteer daarom **Volgende** op de volgende pagina.</span><span class="sxs-lookup"><span data-stu-id="6de34-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="6de34-141">Selecteer **Ik wil dat het organigram automatisch over de pagina's wordt verdeeld**.</span><span class="sxs-lookup"><span data-stu-id="6de34-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Wizard Organigram 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="6de34-143">Selecteer **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="6de34-143">Select **Finish**.</span></span>

    <span data-ttu-id="6de34-144">Als er posities zijn die niet in de structuur zijn opgenomen, wordt u gevraagd om deze op te nemen in het diagram.</span><span class="sxs-lookup"><span data-stu-id="6de34-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="6de34-145">In het diagram dat wordt gegenereerd in Visio wordt elke manager in een afzonderlijk werkblad weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6de34-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="6de34-146">Op basis van de velden die u hebt geselecteerd voor het diagram worden voor elk knooppunt de relevante gegevens weergegeven wanneer het Visio-bestand wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="6de34-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hiërarchiediagram](media/hierarchy.png)

<span data-ttu-id="6de34-148">**Aanvullende optie**</span><span class="sxs-lookup"><span data-stu-id="6de34-148">**Additional option**</span></span>

<span data-ttu-id="6de34-149">In Human Resources kunt u mogelijk ook het werkgebied **Mensen** gebruiken om bepaalde hiërarchiegerelateerde informatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6de34-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
