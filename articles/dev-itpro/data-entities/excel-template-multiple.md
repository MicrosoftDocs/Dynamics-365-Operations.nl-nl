---
title: Gegevens importeren vanuit Excel-sjablonen voor gegevensentiteiten die meerdere werkbladen bevatten
description: In dit onderwerp wordt beschreven hoe u gegevens importeert met Excel-gegevensentiteitsjablonen in Microsoft Dynamics 365 for Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551048"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="d4fa1-103">Gegevens importeren vanuit Excel-sjablonen voor gegevensentiteiten die meerdere werkbladen bevatten</span><span class="sxs-lookup"><span data-stu-id="d4fa1-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4fa1-104">Gegevensbeheer in Microsoft Dynamics 365 for Finance and Operations ondersteunt Microsoft Excel-gebaseerde sjablonen voor gegevensentiteiten.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="d4fa1-105">Deze sjablonen kunnen een of meer werkbladen bevatten.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="d4fa1-106">Sjablonen met meerdere werkbladen worden vaak gebruikt wanneer het handig is om gegevens in één bestand te beheren en in verschillende gegevensentiteiten te importeren.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="d4fa1-107">Een voorbeeld hiervan zijn locaties en magazijnen.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="d4fa1-108">Een bestand eenmaal uploaden en toewijzen aan alle entiteiten</span><span class="sxs-lookup"><span data-stu-id="d4fa1-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="d4fa1-109">We bekijken hier het voorbeeld van een Excel-bestand met de werkbladen **Locaties** en **Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="d4fa1-110">Om het gegevensimportproject in te stellen, moet u de eerste gegevensentiteit **Locaties** toevoegen en het bestand vervolgens uploaden.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="d4fa1-111">U kunt **Locaties** als het werkblad voor deze entiteit selecteren.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="d4fa1-112">Als u de tweede entiteit, **Magazijnen**, toevoegt zonder het formulier **Bestand toevoegen** te verlaten, kunt u het werkblad **Magazijnen** selecteren zonder het bestand opnieuw te hoeven uploaden.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="d4fa1-113">Alleen als de gegevens voor **Magazijnen** zich in een ander bestand bevinden, zou een nieuw bestand moeten worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Meerdere werkbladen](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="d4fa1-115">Toewijzing van werkblad aan entiteit corrigeren</span><span class="sxs-lookup"><span data-stu-id="d4fa1-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="d4fa1-116">De toewijzing van het werkblad aan een gegevensentiteit in de importtaak kan worden gecorrigeerd vanuit het raster.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="d4fa1-117">In de kolom **Werkblad** in het raster worden de werkbladen uit het toegewezen bestand weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="d4fa1-118">U kunt een ander werkblad kiezen in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="d4fa1-119">Als het gekozen werkblad al aan een entiteit in het gegevensproject is toegewezen, wordt u gevraagd de wijziging te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="d4fa1-120">Het is raadzaam om alle toewijzingen te corrigeren in het raster.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-120">We recommend that you fix all mappings in the grid.</span></span>

![Werkbladtoewijzing bijwerken](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="d4fa1-122">Opnieuw toewijzen aan een nieuw bestand</span><span class="sxs-lookup"><span data-stu-id="d4fa1-122">Re-map to a new file</span></span>

<span data-ttu-id="d4fa1-123">In gevallen waarin een nieuwe versie van hetzelfde bestand of een volledig nieuw bestand moet worden geüpload voor bestaande entiteiten in een gegevensproject, moet u de ervaring **Bestand toevoegen** toevoegen en de entiteiten opnieuw toevoegen alsof ze voor het eerst worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="d4fa1-124">U wordt gevraagd of u de bestaande entiteiten in het gegevensproject wilt overschrijven.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="d4fa1-125">Entiteiten die niet opnieuw worden toegevoegd (of overschreven) blijven de vorige toewijzingen uit het vorige bestand houden.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="d4fa1-126">Een bestand uploaden met Project uitvoeren</span><span class="sxs-lookup"><span data-stu-id="d4fa1-126">Upload a file using Run project</span></span>

<span data-ttu-id="d4fa1-127">U kunt een Excel-bestand uploaden met de optie **Project uitvoeren** om een importproject uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="d4fa1-128">Upload alleen bestanden met dezelfde werkbladen als de bestaande toewijzingen voor de gegevensentiteiten in het gegevensproject.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="d4fa1-129">Als een werkblad in het onlangs geüpload bestand niet wordt gevonden, wordt er een fout weergegeven en wordt er gestopt met importeren.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="d4fa1-130">Als de toewijzing aan het werkblad moet worden gewijzigd voor een entiteit, moeten de toewijzingen in het gegevensproject vanuit het gegevensproject worden bijgewerkt voordat u het bestand in de ervaring **Project uitvoeren** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d4fa1-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>
