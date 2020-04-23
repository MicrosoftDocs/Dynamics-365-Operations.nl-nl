---
title: Naar ouderdom gerangschikt voorraadrapport
description: In dit onderwerp wordt de functionaliteit beschreven waarmee u een naar ouderdom gerangschikt voorraadrapport kunt uitvoeren en de uitvoer beschikbaar kunt maken als een formulier en een grafiek.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201613"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="1f207-103">Naar ouderdom gerangschikt voorraadrapport</span><span class="sxs-lookup"><span data-stu-id="1f207-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1f207-104">In Microsoft Dynamics 365 Supply Chain Management kunt u een rapport **Naar ouderdom rangschikken van voorraad** uitvoeren en de uitvoer beschikbaar maken als een formulier en een grafiek.</span><span class="sxs-lookup"><span data-stu-id="1f207-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="1f207-105">In het formulier worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="1f207-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="1f207-106">De grafiek biedt een visueel overzicht dat filters ondersteunt en waarmee u op details kunt inzoomen.</span><span class="sxs-lookup"><span data-stu-id="1f207-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="1f207-107">Daarnaast kunt u met de gegevensentiteit met de naam **Naar ouderdom gerangschikt voorraadrapport** de resultaten van een rapport **Naar ouderdom rangschikken van voorraad** uitvoeren naar een indeling zoals een Microsoft Excel-of PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="1f207-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="1f207-108">Deze methode voor het uitvoeren van een rapport **Naar ouderdom rangschikken van voorraad** is handig wanneer de uitvoer veel regels bevat.</span><span class="sxs-lookup"><span data-stu-id="1f207-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="1f207-109">De uitvoer bevat bijvoorbeeld een groot aantal regels als u 50.000 artikelen en 300 winkels hebt die zijn gemaakt als magazijnen en u een naar ouderdom gerangschikte voorraad per artikel, locatie en magazijn aanvraagt.</span><span class="sxs-lookup"><span data-stu-id="1f207-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="1f207-110">Een naar ouderdom gerangschikt voorraadrapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="1f207-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="1f207-111">Ga naar **Kostenbeheer \> Query's en rapporten \> Opslag naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="1f207-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="1f207-112">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="1f207-112">Select **New**.</span></span>
1. <span data-ttu-id="1f207-113">Geef in het veld **Proces-id – Naam** een unieke naam op voor het rapport op.</span><span class="sxs-lookup"><span data-stu-id="1f207-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="1f207-114">Selecteer het rapport **Identificatie-id** en filter het zo nodig.</span><span class="sxs-lookup"><span data-stu-id="1f207-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="1f207-115">De rapportuitvoering wordt altijd uitgevoerd in een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="1f207-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="1f207-116">Nadat de batchtaak is voltooid, wordt de uitvoer weergegeven op de pagina **Opslag naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="1f207-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="1f207-117">Als u de uitvoer wilt weergeven als een formulier met een traditionele rasterindeling, selecteert u **Details weergeven**.</span><span class="sxs-lookup"><span data-stu-id="1f207-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="1f207-118">Als u de uitvoer als een samengevoegde grafiek wilt weergeven, selecteert u **Grafiek weergeven**.</span><span class="sxs-lookup"><span data-stu-id="1f207-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f207-119">In het formulier worden geen subtotalen opgenomen die zijn gedefinieerd in de rapportindeling.</span><span class="sxs-lookup"><span data-stu-id="1f207-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="1f207-120">Met de gegevensentiteit **Naar ouderdom gerangschikt voorraadrapport** kunt u de uitvoer van een rapport **Naar ouderdom rangschikken van voorraad** exporteren door een filter voor het veld **Proces-id – Naam** toe te passen op alle indelingen die door Gegevensbeheer worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="1f207-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
