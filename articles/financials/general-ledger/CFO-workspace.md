---
title: Financiële dimensies toevoegen aan het CFO-werkgebied
description: In dit onderwerp wordt uitgelegd hoe u financiële dimensies toevoegt aan het werkgebied CFO zodat ze kunnen worden gebruikt voor grootboek- en budgetrapporten.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a15414eff99751d4e77e5b3bf315a556efb7ad5d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566809"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="c2e37-103">Financiële dimensies toevoegen aan het CFO-werkgebied</span><span class="sxs-lookup"><span data-stu-id="c2e37-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2e37-104">In dit onderwerp wordt uitgelegd hoe u financiële dimensies toevoegt aan het werkgebied CFO (Chief Financial Officer) zodat ze kunnen worden gebruikt voor grootboek- en budgetrapporten.</span><span class="sxs-lookup"><span data-stu-id="c2e37-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="c2e37-105">Het CFO-werkgebied omvat een tabblad **Overzicht** en een tabblad **Financieel**. De rapporten op deze twee tabbladen worden ondersteund door twee maateenheden: LedgerActivityMeasure en BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="c2e37-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="c2e37-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), is er een relatie tussen deze twee afmetingen en de DimensionCombinationEntity-entiteit.</span><span class="sxs-lookup"><span data-stu-id="c2e37-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="c2e37-107">Daarom kunt u alle dimensies selecteren.</span><span class="sxs-lookup"><span data-stu-id="c2e37-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="c2e37-108">Werk in Finance and Operations op de pagina **Entiteitopslag** de maateenheden **LedgerActivityMeasure** en **BudgetActivityMeasure** bij.</span><span class="sxs-lookup"><span data-stu-id="c2e37-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="c2e37-109">Open Toepassingsverkenner in Microsoft Visual Studio en zoek naar **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="c2e37-110">Open onder **Resources** **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="c2e37-111">Wanneer de resource wordt geopend in Microsoft Power BI-bureaublad, selecteert u **Gegevens ophalen**, **SQL Server-database** en vervolgens **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="c2e37-112">Voer de servernaam in en **AxDW** als de gedatabase.</span><span class="sxs-lookup"><span data-stu-id="c2e37-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="c2e37-113">Selecteer **DirectQuery** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="c2e37-114">Zoek en selecteer **LedgerActivityMeasure\_DimensionCombination**, en selecteer vervolgens **laden**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="c2e37-115">In de lijst **Velden** wijzigt u de naam van de tabel **Financiële dimensies**, zodat deze gemakkelijk kan worden herkend.</span><span class="sxs-lookup"><span data-stu-id="c2e37-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="c2e37-116">Selecteer **Relaties beheren** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="c2e37-117">Selecteer in het eerste veld **Grootboekactiviteiten** en selecteer vervolgens **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="c2e37-118">Selecteer in het tweede veld **LedgerActivityMeasure\_DimensionCombination** (of **Financiële dimensies** als u de naam van de tabel hebt gewijzigd).</span><span class="sxs-lookup"><span data-stu-id="c2e37-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="c2e37-119">Selecteer de koptekst **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="c2e37-120">Selecteer in het veld **Kardinaliteit** **Veel-op-één**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="c2e37-121">Wijzig de waarde **Cross-filter richting** in **Eén**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="c2e37-122">Selecteer **Deze relatie actief maken** en **Uitgaan van referentiële integriteit**, selecteer **OK** en vervolgens **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="c2e37-123">[![Een relatie maken](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="c2e37-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="c2e37-124">In de lijst **Velden** ziet u de tabel en de beschikbare financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="c2e37-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="c2e37-125">Sleep de gewenste financiële dimensies naar de filters voor het rapportniveau.</span><span class="sxs-lookup"><span data-stu-id="c2e37-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="c2e37-126">Sla de wijzigingen op.</span><span class="sxs-lookup"><span data-stu-id="c2e37-126">Save your changes.</span></span>
15. <span data-ttu-id="c2e37-127">Klik in de Application Object Tree (AOT) met de rechtermuisknop op het project en selecteer **Synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="c2e37-128">Stel het project samen en open vervolgens de toepassing om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c2e37-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="c2e37-129">[![Voltooid werkgebied](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="c2e37-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
