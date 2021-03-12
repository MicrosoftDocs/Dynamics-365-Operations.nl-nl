---
title: Opslag naar ouderdom gerangschikt voorraadrapport
description: In dit onderwerp wordt de functionaliteit beschreven waarmee u een naar ouderdom gerangschikt voorraadrapport kunt uitvoeren en de uitvoer beschikbaar kunt maken als een formulier en een grafiek.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a292bd7a7ccbb09af1955e1e253b45e230c1009
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005422"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="5462a-103">Opslag naar ouderdom gerangschikt voorraadrapport</span><span class="sxs-lookup"><span data-stu-id="5462a-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5462a-104">In Microsoft Dynamics 365 Supply Chain Management kunt u een rapport **Opslag naar ouderdom gerangschikt voorraadrapport** uitvoeren en de uitvoer beschikbaar maken als een formulier en een grafiek.</span><span class="sxs-lookup"><span data-stu-id="5462a-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="5462a-105">In het formulier worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="5462a-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="5462a-106">De grafiek biedt een visueel overzicht dat filters ondersteunt en waarmee u op details kunt inzoomen.</span><span class="sxs-lookup"><span data-stu-id="5462a-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="5462a-107">Daarnaast kunt u met de gegevensentiteit met de naam **Naar ouderdom gerangschikt voorraadrapport** de resultaten van een rapport **Opslag naar ouderdom gerangschikt voorraadrapport** uitvoeren naar een indeling zoals een Microsoft Excel-of PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="5462a-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="5462a-108">Deze methode voor het uitvoeren van een rapport **Opslag naar ouderdom gerangschikt voorraadrapport** is handig wanneer de uitvoer veel regels bevat.</span><span class="sxs-lookup"><span data-stu-id="5462a-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="5462a-109">De uitvoer bevat bijvoorbeeld een groot aantal regels als u 50.000 artikelen en 300 winkels hebt die zijn gemaakt als magazijnen en u een naar ouderdom gerangschikte voorraad per artikel, locatie en magazijn aanvraagt.</span><span class="sxs-lookup"><span data-stu-id="5462a-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="5462a-110">De functie Opslag naar ouderdom gerangschikt voorraadrapport inschakelen</span><span class="sxs-lookup"><span data-stu-id="5462a-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="5462a-111">Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem.</span><span class="sxs-lookup"><span data-stu-id="5462a-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="5462a-112">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5462a-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="5462a-113">Hier ziet u de functie als:</span><span class="sxs-lookup"><span data-stu-id="5462a-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="5462a-114">**Module** - Kostenbeheer</span><span class="sxs-lookup"><span data-stu-id="5462a-114">**Module** - Cost management</span></span>
- <span data-ttu-id="5462a-115">**Functienaam**: Opslag naar ouderdom gerangschikt voorraadrapport</span><span class="sxs-lookup"><span data-stu-id="5462a-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="5462a-116">Opslag naar ouderdom gerangschikt voorraadrapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="5462a-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="5462a-117">Ga naar **Kostenbeheer \> Query's en rapporten \> Opslag naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="5462a-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="5462a-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5462a-118">Select **New**.</span></span>
1. <span data-ttu-id="5462a-119">Geef in het veld **Proces-id – Naam** een unieke naam op voor het rapport op.</span><span class="sxs-lookup"><span data-stu-id="5462a-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="5462a-120">Selecteer het rapport **Identificatie-id** en filter het zo nodig.</span><span class="sxs-lookup"><span data-stu-id="5462a-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="5462a-121">De rapportuitvoering wordt altijd uitgevoerd in een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="5462a-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="5462a-122">Nadat de batchtaak is voltooid, wordt de uitvoer weergegeven op de pagina **Opslag naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="5462a-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="5462a-123">Als u de uitvoer wilt weergeven als een formulier met een traditionele rasterindeling, selecteert u **Details weergeven**.</span><span class="sxs-lookup"><span data-stu-id="5462a-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="5462a-124">Als u de uitvoer als een samengevoegde grafiek wilt weergeven, selecteert u **Grafiek weergeven**.</span><span class="sxs-lookup"><span data-stu-id="5462a-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5462a-125">In het formulier worden geen subtotalen opgenomen die zijn gedefinieerd in de rapportindeling.</span><span class="sxs-lookup"><span data-stu-id="5462a-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="5462a-126">Met de gegevensentiteit **Naar ouderdom gerangschikt voorraadrapport** kunt u de uitvoer van een **Opslag naar ouderdom gerangschikt voorraadrapport** exporteren door een filter voor het veld **Proces-id – Naam** toe te passen op alle indelingen die door Gegevensbeheer worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="5462a-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
