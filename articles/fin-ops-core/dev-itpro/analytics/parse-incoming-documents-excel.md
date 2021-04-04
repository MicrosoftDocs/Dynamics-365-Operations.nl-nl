---
title: Inkomende documenten in Excel-indeling parseren
description: Dit onderwerp biedt informatie over het ontwerpen van ER-indelingen (elektronische rapportage) om inhoud van binnenkomende Microsoft Excel-bestanden te parseren.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 847b3309a3e0daf7b341c4ba4a58a8ea0902e61c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564514"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="11f93-103">Inkomende documenten in Excel-indeling parseren</span><span class="sxs-lookup"><span data-stu-id="11f93-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11f93-104">U kunt ER-indelingen ontwerpen om binnenkomende Microsoft Excel-bestanden te parseren die gegevens in Microsoft Excel-werkmappen (bestanden in XLSX-indeling) vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="11f93-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="11f93-105">Vervolgens kunt u de inhoud van deze bestanden gebruiken om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="11f93-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="11f93-106">Dit is handig als u het volgende doet:</span><span class="sxs-lookup"><span data-stu-id="11f93-106">This is useful if you:</span></span>

- <span data-ttu-id="11f93-107">Een nieuw model en indeling ontwerpen en ze willen testen tijdens de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="11f93-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="11f93-108">Excel simuleert in dit geval de feitelijke toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="11f93-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="11f93-109">Gegevens beheren buiten uw toepassing in Excel en deze gegevens vervolgens importeren om een specifiek rapport in te dienen.</span><span class="sxs-lookup"><span data-stu-id="11f93-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="11f93-110">Voor meer informatie over deze functie speelt u de taakbegeleidingen **ER gegevens importeren uit een Microsoft Excel-bestand (deel 1: Ontwerpindeling)** en **ER gegevens importeren uit een Microsoft Excel-bestand (deel 2: Gegevens importeren)** (delen van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af.</span><span class="sxs-lookup"><span data-stu-id="11f93-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="11f93-111">Deze taakbegeleidingen begeleiden u door het parseren van het binnenkomende Excel-bestand met behulp van de ER-indeling om gegevens te importeren uit binnenkomende documenten en toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="11f93-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="11f93-112">U kunt de taakbegeleiding downloaden uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="11f93-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="11f93-113">Download de volgende bestanden om de hierboven genoemde taakbegeleidingen te voltooien:</span><span class="sxs-lookup"><span data-stu-id="11f93-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="11f93-114">Omschrijving inhoud</span><span class="sxs-lookup"><span data-stu-id="11f93-114">Content description</span></span>                         | <span data-ttu-id="11f93-115">Bestand</span><span class="sxs-lookup"><span data-stu-id="11f93-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="11f93-116">Binnenkomend bestand in. XLSX-indeling - sjabloon</span><span class="sxs-lookup"><span data-stu-id="11f93-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="11f93-117">1099import template.xlsx</span><span class="sxs-lookup"><span data-stu-id="11f93-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="11f93-118">Binnenkomend bestand in. XLSX-indeling - voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="11f93-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="11f93-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="11f93-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="11f93-120">Als u de volgende taakbegeleiding [ER vereiste configuraties maken om gegevens te importeren uit een extern bestand](./tasks/er-required-configurations-import-data.md) nog niet hebt afgespeeld in de huidige Finance and Operations-toepassing, downloadt u het volgende bestand.</span><span class="sxs-lookup"><span data-stu-id="11f93-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="11f93-121">Omschrijving inhoud</span><span class="sxs-lookup"><span data-stu-id="11f93-121">Content description</span></span>    | <span data-ttu-id="11f93-122">Bestand</span><span class="sxs-lookup"><span data-stu-id="11f93-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="11f93-123">ER-modelconfiguratie</span><span class="sxs-lookup"><span data-stu-id="11f93-123">ER model configuration</span></span> | [<span data-ttu-id="11f93-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="11f93-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]