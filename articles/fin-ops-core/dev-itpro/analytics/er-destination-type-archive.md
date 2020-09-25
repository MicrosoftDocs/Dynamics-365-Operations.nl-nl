---
title: ER-bestemmingstype voor archief
description: Dit onderwerp bevat informatie over het configureren van een archiefbestemming voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745580"
---
# <a name="archive-destination"></a><span data-ttu-id="f6349-103">Archiefbestemming</span><span class="sxs-lookup"><span data-stu-id="f6349-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6349-104">U kunt een archiefbestemming configureren voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.</span><span class="sxs-lookup"><span data-stu-id="f6349-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="f6349-105">Op basis van de doelinstelling wordt een gegenereerd document opgeslagen als een bijlage van een record van de ER-takenlijst.</span><span class="sxs-lookup"><span data-stu-id="f6349-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="f6349-106">Met deze optie kunt u het gegenereerde document naar een Microsoft SharePoint-map of naar de Microsoft Azure-opslag verzenden.</span><span class="sxs-lookup"><span data-stu-id="f6349-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="f6349-107">Stel **Ingeschakeld** in op **Ja** om uitvoer naar een bestemming te verzenden die is gedefinieerd door het geselecteerde documenttype.</span><span class="sxs-lookup"><span data-stu-id="f6349-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="f6349-108">Alleen documenttypen waarvan de groep is ingesteld op **Bestand** zijn beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="f6349-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="f6349-109">U definieert document[typen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) onder **Organisatiebeheer** \> **Documentbeheer** \> **Documenttypen**.</span><span class="sxs-lookup"><span data-stu-id="f6349-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="f6349-110">De configuratie voor ER-bestemmingen is hetzelfde als de configuratie voor het documentbeheersysteem.</span><span class="sxs-lookup"><span data-stu-id="f6349-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="f6349-111">[![Pagina Documenttypen](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="f6349-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="f6349-112">De locatie bepaalt waar het bestand wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="f6349-112">The location determines where the file is saved.</span></span> <span data-ttu-id="f6349-113">Nadat de bestemming **Archief** is ingeschakeld, kunnen de resultaten worden opgeslagen in het taakarchief.</span><span class="sxs-lookup"><span data-stu-id="f6349-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="f6349-114">U kunt de resultaten weergeven via **Organisatiebeheer** \> **Elektronische aangifte** \> **Gearchiveerde taken elektronische aangifte**.</span><span class="sxs-lookup"><span data-stu-id="f6349-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="f6349-115">Selecteer een documenttype voor het taakarchief via **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische aangifte** \> **Elektronische rapportparameters**.</span><span class="sxs-lookup"><span data-stu-id="f6349-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="f6349-116">Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f6349-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="f6349-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="f6349-117">SharePoint</span></span>

<span data-ttu-id="f6349-118">U kunt een bestand opslaan in een aangewezen SharePoint-map.</span><span class="sxs-lookup"><span data-stu-id="f6349-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="f6349-119">Als u de standaard-SharePoint-server wilt definiëren, gaat u naar **Organisatiebeheer** \> **Documentbeheer** \> **Parameters voor documentbeheer**.</span><span class="sxs-lookup"><span data-stu-id="f6349-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="f6349-120">Configureer op het tabblad **SharePoint** de SharePoint-map.</span><span class="sxs-lookup"><span data-stu-id="f6349-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="f6349-121">Vervolgens kunt u deze selecteren als de map waarin de ER-uitvoer wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="f6349-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="f6349-122">De **SharePoint**-locatie moet worden geselecteerd in dit documenttype.</span><span class="sxs-lookup"><span data-stu-id="f6349-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="f6349-123">[![Een SharePoint-map selecteren](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="f6349-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="f6349-124">Azure-opslag</span><span class="sxs-lookup"><span data-stu-id="f6349-124">Azure Storage</span></span>

<span data-ttu-id="f6349-125">Als de locatie van het documenttype is ingesteld op **Azure-opslag**, kunt u een bestand opslaan in Azure-opslag.</span><span class="sxs-lookup"><span data-stu-id="f6349-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6349-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f6349-126">Additional resources</span></span>

- [<span data-ttu-id="f6349-127">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="f6349-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f6349-128">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="f6349-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="f6349-129">Documentbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="f6349-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
