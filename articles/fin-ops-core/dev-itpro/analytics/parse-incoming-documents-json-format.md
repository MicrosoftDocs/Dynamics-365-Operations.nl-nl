---
title: Inkomende documenten in JSON-indeling parseren
description: In dit onderwerp wordt uitgelegd hoe u ER-indelingen (elektronische rapportage) kunt instellen om binnenkomende documenten in JSON-indeling (JavaScript Object Notation) te parseren.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185262"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="127d0-103">Inkomende documenten in JSON-indeling parseren</span><span class="sxs-lookup"><span data-stu-id="127d0-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="127d0-104">U kunt ER-indelingen ontwerpen voor het parseren van inkomende elektronische documenten die gegevens in een tekstindeling vertegenwoordigen die is gebaseerd op Javascript (met andere woorden, bestanden in de \[JSON\]-indeling).</span><span class="sxs-lookup"><span data-stu-id="127d0-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="127d0-105">Als u meer wilt weten over deze functie, downloadt u de bestanden in de volgende tabel en speelt u de taakbegeleider ER Een indelingsconfiguratie maken om gegevens uit een extern JSON-bestand te importeren af.</span><span class="sxs-lookup"><span data-stu-id="127d0-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="127d0-106">In deze taakbegeleider wordt weergegeven hoe een ER-indeling kan worden gebruikt om een binnenkomend JSON-bestand te parseren om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="127d0-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="127d0-107">Titel</span><span class="sxs-lookup"><span data-stu-id="127d0-107">Title</span></span>                                  | <span data-ttu-id="127d0-108">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="127d0-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="127d0-109">ER-indelingsconfiguratie</span><span class="sxs-lookup"><span data-stu-id="127d0-109">ER format configuration</span></span>                | [<span data-ttu-id="127d0-110">Indeling voor het importeren van trans_JSON. XML van leveranciers</span><span class="sxs-lookup"><span data-stu-id="127d0-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="127d0-111">Voorbeeld van binnenkomend bestand in CSV-indeling</span><span class="sxs-lookup"><span data-stu-id="127d0-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="127d0-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="127d0-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="127d0-113">Behoeften</span><span class="sxs-lookup"><span data-stu-id="127d0-113">Requirements</span></span>

<span data-ttu-id="127d0-114">Voordat u de taakbegeleider ER Een indelingsconfiguratie maken om gegevens uit een extern JSON-bestand te importeren voltooit, moet aan de volgende vereiste zijn voldaan:</span><span class="sxs-lookup"><span data-stu-id="127d0-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="127d0-115">Bovenliggende elementen in het JSON-bestand kunnen alleen objectelementen zijn.</span><span class="sxs-lookup"><span data-stu-id="127d0-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="127d0-116">Geneste elementen voor een object moeten eigenschapselementen zijn, zodat een geldige JSON-structuur wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="127d0-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="127d0-117">JSON-matrices kunnen alleen geneste elementen zijn van de eigenschapselementen van een object.</span><span class="sxs-lookup"><span data-stu-id="127d0-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="127d0-118">JSON-matrices kunnen alleen JSON-objecten bevatten.</span><span class="sxs-lookup"><span data-stu-id="127d0-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="127d0-119">Ze kunnen geen directe tekenreeks/numerieke waarden en geneste matrices bevatten.</span><span class="sxs-lookup"><span data-stu-id="127d0-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="127d0-120">Elementen in deze matrices worden geparseerd in de volgorde waarin ze in de indeling zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="127d0-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="127d0-121">Voor elk JSON-object wordt rekening gehouden met instellingen voor multipliciteit.</span><span class="sxs-lookup"><span data-stu-id="127d0-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="127d0-122">Bovendien moet u de taakbegeleider [ER Vereiste configuraties maken om gegevens te importeren uit een extern bestand voor elektronische rapportage](tasks/er-required-configurations-import-data.md) uitvoeren als u dit nog niet hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="127d0-122">Additionally, you must complete the [ER Create required configurations to import data from an external file for electronic reporting](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="127d0-123">Download het volgende bestand om de taakbegeleiding te voltooien.</span><span class="sxs-lookup"><span data-stu-id="127d0-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="127d0-124">Titel</span><span class="sxs-lookup"><span data-stu-id="127d0-124">Title</span></span>                  | <span data-ttu-id="127d0-125">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="127d0-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="127d0-126">ER-modelconfiguratie</span><span class="sxs-lookup"><span data-stu-id="127d0-126">ER model configuration</span></span> | [<span data-ttu-id="127d0-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="127d0-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |