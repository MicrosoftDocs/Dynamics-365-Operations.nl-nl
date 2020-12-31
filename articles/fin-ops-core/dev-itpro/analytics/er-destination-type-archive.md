---
title: ER-bestemmingstype voor archief
description: Dit onderwerp bevat informatie over het configureren van een archiefbestemming voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679673"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="09fc8-103">ER-bestemmingstype voor archief</span><span class="sxs-lookup"><span data-stu-id="09fc8-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09fc8-104">U kunt een archiefbestemming configureren voor elk onderdeel **Map** of **Bestand** van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.</span><span class="sxs-lookup"><span data-stu-id="09fc8-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="09fc8-105">Op basis van de doelinstelling wordt een gegenereerd document opgeslagen als een bijlage van een record van de ER-takenlijst.</span><span class="sxs-lookup"><span data-stu-id="09fc8-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="09fc8-106">U kunt de resultaten weergeven door naar **Organisatiebeheer** \> **Elektronische aangifte** \> **Elektronische rapportagetaken** te gaan.</span><span class="sxs-lookup"><span data-stu-id="09fc8-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="09fc8-107">Met deze optie kunt u het gegenereerde document naar een Microsoft SharePoint-map of naar de Microsoft Azure-opslag verzenden.</span><span class="sxs-lookup"><span data-stu-id="09fc8-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="09fc8-108">Stel **Ingeschakeld** in op **Ja** om uitvoer naar een bestemming te verzenden die is gedefinieerd door het geselecteerde documenttype.</span><span class="sxs-lookup"><span data-stu-id="09fc8-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="09fc8-109">Alleen documenttypen waarvan de groep is ingesteld op **Bestand** zijn beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="09fc8-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="09fc8-110">U definieert document [typen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) onder **Organisatiebeheer** \> **Documentbeheer** \> **Documenttypen**.</span><span class="sxs-lookup"><span data-stu-id="09fc8-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="09fc8-111">De configuratie voor ER-bestemmingen is hetzelfde als de configuratie voor het documentbeheersysteem.</span><span class="sxs-lookup"><span data-stu-id="09fc8-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="09fc8-112">[![Pagina Documenttypen](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="09fc8-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="09fc8-113">De locatie bepaalt waar het bestand wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="09fc8-113">The location determines where the file is saved.</span></span> <span data-ttu-id="09fc8-114">Nadat de bestemming **Archief** is ingeschakeld, kunnen de resultaten worden opgeslagen in het taakarchief.</span><span class="sxs-lookup"><span data-stu-id="09fc8-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="09fc8-115">U kunt de resultaten weergeven via **Organisatiebeheer** \> **Elektronische aangifte** \> **Gearchiveerde taken elektronische aangifte**.</span><span class="sxs-lookup"><span data-stu-id="09fc8-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="09fc8-116">Selecteer een documenttype voor het taakarchief via **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische aangifte** \> **Elektronische rapportparameters**.</span><span class="sxs-lookup"><span data-stu-id="09fc8-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="09fc8-117">Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="09fc8-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="09fc8-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="09fc8-118">SharePoint</span></span>

<span data-ttu-id="09fc8-119">U kunt een bestand opslaan in een aangewezen SharePoint-map.</span><span class="sxs-lookup"><span data-stu-id="09fc8-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="09fc8-120">Als u de standaard-SharePoint-server wilt definiëren, gaat u naar **Organisatiebeheer** \> **Documentbeheer** \> **Parameters voor documentbeheer**.</span><span class="sxs-lookup"><span data-stu-id="09fc8-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="09fc8-121">Configureer op het tabblad **SharePoint** de SharePoint-map.</span><span class="sxs-lookup"><span data-stu-id="09fc8-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="09fc8-122">Vervolgens kunt u deze selecteren als de map waarin de ER-uitvoer wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="09fc8-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="09fc8-123">De **SharePoint**-locatie moet worden geselecteerd in dit documenttype.</span><span class="sxs-lookup"><span data-stu-id="09fc8-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="09fc8-124">[![Een SharePoint-map selecteren](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="09fc8-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="09fc8-125">Azure-opslag</span><span class="sxs-lookup"><span data-stu-id="09fc8-125">Azure Storage</span></span>

<span data-ttu-id="09fc8-126">Als de locatie van het documenttype is ingesteld op **Azure-opslag**, kunt u een bestand opslaan in Azure-opslag.</span><span class="sxs-lookup"><span data-stu-id="09fc8-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="09fc8-127">In het huidige ER-raamwerk worden bestanden in de Azure Blob-opslag opgeslagen, in tegenstelling tot het raamwerk voor gegevensbeheer waarin het bewaarbeleid van zeven dagen wordt toegepast voor documenten die moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="09fc8-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="09fc8-128">Zie [API voor ophalen van berichtstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) en [API voor statuscontrole](../data-entities/data-management-api.md#status-check-api) voor meer informatie .</span><span class="sxs-lookup"><span data-stu-id="09fc8-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="09fc8-129">De ER-gerelateerde bestanden worden in de Azure Blob-opslag zo lang als nodig is opgeslagen als bijlagen van toepassingstabelrecords.</span><span class="sxs-lookup"><span data-stu-id="09fc8-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="09fc8-130">Een enkel bestand wordt verwijderd uit de Azure Blob-opslag, samen met de toepassingstabelrecord waaraan dit bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="09fc8-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09fc8-131">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="09fc8-131">Additional resources</span></span>

- [<span data-ttu-id="09fc8-132">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="09fc8-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="09fc8-133">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="09fc8-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="09fc8-134">Documentbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="09fc8-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
