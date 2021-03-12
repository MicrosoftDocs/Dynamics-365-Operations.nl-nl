---
title: Gegevens van de dochtermaatschappij exporteren naar bestanden
description: In dit onderwerp wordt uitgelegd hoe u de exportgegevens van Microsoft Dynamics 365 Finance voorbereidt en deze vervolgens in een geconsolideerde rechtspersoon importeert.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968674"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="b136c-103">Gegevens van de dochtermaatschappij exporteren naar bestanden</span><span class="sxs-lookup"><span data-stu-id="b136c-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b136c-104">U gebruikt te pagina **Exporteren** (**Systeembeheer \> Werkruimten \> Importeren/exporteren**) om gegevens van de dochtermaatschappij to te exporteren naar bestanden die vervolgens kunnen worden geïmporteerd in een geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="b136c-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="b136c-105">Meer informatie over het import- en exportproces vindt u in [Overzicht van gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="b136c-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="b136c-106">Maak een rechtspersoon voor het consolidatieproces.</span><span class="sxs-lookup"><span data-stu-id="b136c-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="b136c-107">Meer informatie over het maken van rechtspersonen vindt u in [Een rechtspersoon maken](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="b136c-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="b136c-108">Meer informatie vindt u in [Een rechtspersoon voorbereiden voor gebruik in het consolidatieproces](prepare-company-for-consolidation.md) en [Een dochtermaatschappij voor consolidatie instellen](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="b136c-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="b136c-109">Ga naar **Consolidaties \> Bedrijfssaldi exporteren**.</span><span class="sxs-lookup"><span data-stu-id="b136c-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="b136c-110">Geef op de pagina **Bedrijfssaldi exporteren** op het tabblad **Criteria** de details van de consolidatie op door de volgende velden in te stellen.</span><span class="sxs-lookup"><span data-stu-id="b136c-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="b136c-111">Veld</span><span class="sxs-lookup"><span data-stu-id="b136c-111">Field</span></span>                             | <span data-ttu-id="b136c-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b136c-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="b136c-113">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="b136c-113">Main account</span></span>                      | <span data-ttu-id="b136c-114">Geef op welke rekeningen moeten worden geconsolideerd.</span><span class="sxs-lookup"><span data-stu-id="b136c-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="b136c-115">Als u alle rekeningen wilt meenemen, laat u dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="b136c-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="b136c-116">Consolidatierekening gebruiken</span><span class="sxs-lookup"><span data-stu-id="b136c-116">Use consolidation account</span></span>         | <span data-ttu-id="b136c-117">Als u consolidatierekeningen hebt opgegeven, stelt u deze optie in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b136c-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="b136c-118">Consolidatierekening selecteren in</span><span class="sxs-lookup"><span data-stu-id="b136c-118">Select consolidation account from</span></span> | <span data-ttu-id="b136c-119">Selecteer **Hoofdrekening** of **Consolidatierekeninggroep**.</span><span class="sxs-lookup"><span data-stu-id="b136c-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="b136c-120">Consolidatierekeninggroep</span><span class="sxs-lookup"><span data-stu-id="b136c-120">Consolidation account group</span></span>       | <span data-ttu-id="b136c-121">Selecteer een groep consolidatierekeningen voor de consolidatierekening die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b136c-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="b136c-122">Consolidatieperiode</span><span class="sxs-lookup"><span data-stu-id="b136c-122">Consolidation period</span></span>              | <span data-ttu-id="b136c-123">Geef datums "van" en "tot" voor de consolidatie op.</span><span class="sxs-lookup"><span data-stu-id="b136c-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="b136c-124">Werkelijke bedragen opnemen</span><span class="sxs-lookup"><span data-stu-id="b136c-124">Include actual amounts</span></span>            | <span data-ttu-id="b136c-125">Stel deze optie in op **Ja** om werkelijke bedragen op te nemen.</span><span class="sxs-lookup"><span data-stu-id="b136c-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="b136c-126">Budgetbedragen opnemen</span><span class="sxs-lookup"><span data-stu-id="b136c-126">Include budget amounts</span></span>            | <span data-ttu-id="b136c-127">Stel deze optie in op **Ja** als u budgetbedragen wilt opnemen in consolidaties.</span><span class="sxs-lookup"><span data-stu-id="b136c-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="b136c-128">Budgetmodellen</span><span class="sxs-lookup"><span data-stu-id="b136c-128">Budget models</span></span>                     | <span data-ttu-id="b136c-129">Geef het budgetmodel op dat u wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="b136c-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="b136c-130">Geef op het tabblad **Financiële dimensies** de details van de consolidatie op:</span><span class="sxs-lookup"><span data-stu-id="b136c-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="b136c-131">Geef de financiële dimensie-informatie op die moet worden overgebracht van de transacties van de dochtermaatschappijrekeningen naar de transacties in de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="b136c-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="b136c-132">Selecteer financiële dimensies in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b136c-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="b136c-133">Bepaal de juiste specificatie voor elke financiële dimensie die wordt geconsolideerd.</span><span class="sxs-lookup"><span data-stu-id="b136c-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="b136c-134">De beschikbare opties zijn **Dimensie**, **Groepdimensie**, **Bedrijfsrekeningen** en **Rekening**.</span><span class="sxs-lookup"><span data-stu-id="b136c-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b136c-135">Met de optie **Groepdimensie** kunt u de dimensiewaarde definiëren die wordt gebruikt door de groep bedrijven die wordt geconsolideerd.</span><span class="sxs-lookup"><span data-stu-id="b136c-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="b136c-136">Geef de segmentvolgorde op waarin moet worden geconsolideerd.</span><span class="sxs-lookup"><span data-stu-id="b136c-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="b136c-137">Volg deze stappen op het tabblad **Rechtspersonen** om de rechtspersoon op te geven die u exporteert:</span><span class="sxs-lookup"><span data-stu-id="b136c-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="b136c-138">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b136c-138">Select **New**.</span></span>
    2. <span data-ttu-id="b136c-139">Voer in het veld **Rechtspersoon bron** de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="b136c-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="b136c-140">Als dezelfde criteria van toepassing zijn op verschillende dochtermaatschappijen in dezelfde database, kunt u gegevens van de dochtermaatschappijen overbrengen om exportbestanden in één bewerking te scheiden:</span><span class="sxs-lookup"><span data-stu-id="b136c-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="b136c-141">Maak een regel voor elke dochtermaatschappij waarvoor de rekeningen moeten worden geëxporteerd naar bestanden.</span><span class="sxs-lookup"><span data-stu-id="b136c-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="b136c-142">Deze bestanden worden later geïmporteerd in de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="b136c-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="b136c-143">Voer voor elke dochtermaatschappij de naam van de dochtermaatschappij en de naam van het exportbestand in die worden gemaakt tijdens de exporttaak.</span><span class="sxs-lookup"><span data-stu-id="b136c-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="b136c-144">Selecteer in het veld **Rekeningtype voor omrekeningsverschillen** de optie **Winst en verlies** of **Balans**.</span><span class="sxs-lookup"><span data-stu-id="b136c-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="b136c-145">Voer een bestandsnaam in voor het exportbestand dat wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b136c-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="b136c-146">Selecteer **OK** om te exporteren.</span><span class="sxs-lookup"><span data-stu-id="b136c-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="b136c-147">Wanneer de export is voltooid, ontvangt u een bericht waarin het aantal records wordt weergegeven dat is opgeslagen in elk bestand.</span><span class="sxs-lookup"><span data-stu-id="b136c-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="b136c-148">U kunt de bestanden vervolgens importeren in de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="b136c-148">You can then import the files into the consolidated legal entity.</span></span>
