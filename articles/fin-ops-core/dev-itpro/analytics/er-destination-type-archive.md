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
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019708"
---
# <span data-ttu-id="fa95a-103"><a name="ArchiveDestinationType">Archiefbestemming</a></span><span class="sxs-lookup"><span data-stu-id="fa95a-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa95a-104">U kunt een archiefbestemming configureren voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.</span><span class="sxs-lookup"><span data-stu-id="fa95a-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="fa95a-105">Op basis van de doelinstelling wordt een gegenereerd document opgeslagen als een bijlage van een record van de ER-takenlijst.</span><span class="sxs-lookup"><span data-stu-id="fa95a-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="fa95a-106">Met deze optie kunt u het gegenereerde document naar een Microsoft SharePoint-map of naar de Microsoft Azure-opslag verzenden.</span><span class="sxs-lookup"><span data-stu-id="fa95a-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="fa95a-107">Stel **Ingeschakeld** in op **Ja** om uitvoer naar een bestemming te verzenden die is gedefinieerd door het geselecteerde documenttype.</span><span class="sxs-lookup"><span data-stu-id="fa95a-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="fa95a-108">Alleen documenttypen waarvan de groep is ingesteld op **Bestand** zijn beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="fa95a-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="fa95a-109">U definieert document[typen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) onder **Organisatiebeheer** \> **Documentbeheer** \> **Documenttypen**.</span><span class="sxs-lookup"><span data-stu-id="fa95a-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="fa95a-110">De configuratie voor ER-bestemmingen is hetzelfde als de configuratie voor het documentbeheersysteem.</span><span class="sxs-lookup"><span data-stu-id="fa95a-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="fa95a-111">[![Pagina Documenttypen](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="fa95a-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="fa95a-112">De locatie bepaalt waar het bestand wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="fa95a-112">The location determines where the file is saved.</span></span> <span data-ttu-id="fa95a-113">Nadat de bestemming **Archief** is ingeschakeld, kunnen de resultaten worden opgeslagen in het taakarchief.</span><span class="sxs-lookup"><span data-stu-id="fa95a-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="fa95a-114">U kunt de resultaten weergeven via **Organisatiebeheer** \> **Elektronische aangifte** \> **Gearchiveerde taken elektronische aangifte**.</span><span class="sxs-lookup"><span data-stu-id="fa95a-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="fa95a-115">Selecteer een documenttype voor het taakarchief via **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische aangifte** \> **Elektronische rapportparameters**.</span><span class="sxs-lookup"><span data-stu-id="fa95a-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="fa95a-116">Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="fa95a-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="fa95a-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="fa95a-117">SharePoint</span></span>

<span data-ttu-id="fa95a-118">U kunt een bestand opslaan in een aangewezen SharePoint-map.</span><span class="sxs-lookup"><span data-stu-id="fa95a-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="fa95a-119">Als u de standaard-SharePoint-server wilt definiëren, gaat u naar **Organisatiebeheer** \> **Documentbeheer** \> **Parameters voor documentbeheer**.</span><span class="sxs-lookup"><span data-stu-id="fa95a-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="fa95a-120">Configureer op het tabblad **SharePoint** de SharePoint-map.</span><span class="sxs-lookup"><span data-stu-id="fa95a-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="fa95a-121">Vervolgens kunt u deze selecteren als de map waarin de ER-uitvoer wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="fa95a-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="fa95a-122">De **SharePoint**-locatie moet worden geselecteerd in dit documenttype.</span><span class="sxs-lookup"><span data-stu-id="fa95a-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="fa95a-123">[![Een SharePoint-map selecteren](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="fa95a-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="fa95a-124">Azure-opslag</span><span class="sxs-lookup"><span data-stu-id="fa95a-124">Azure Storage</span></span>

<span data-ttu-id="fa95a-125">Als de locatie van het documenttype is ingesteld op **Azure-opslag**, kunt u een bestand opslaan in Azure-opslag.</span><span class="sxs-lookup"><span data-stu-id="fa95a-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa95a-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fa95a-126">Additional resources</span></span>

- [<span data-ttu-id="fa95a-127">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="fa95a-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="fa95a-128">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="fa95a-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="fa95a-129">Documentbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="fa95a-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
