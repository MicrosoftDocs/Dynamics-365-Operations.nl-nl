---
title: Resourcegroep voor afzonderlijke productie definiëren
description: Een resourcegroep is een set van bronnen voor bedrijfsactiviteiten die meestal corresponderen met de fysieke organisatie van werkcellen, gedefinieerd door gele lijnen op de werkvloer van de productie.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "353236"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="002a0-103">Resourcegroep voor afzonderlijke productie definiëren</span><span class="sxs-lookup"><span data-stu-id="002a0-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="002a0-104">Een resourcegroep is een set van bronnen voor bedrijfsactiviteiten die meestal corresponderen met de fysieke organisatie van werkcellen, gedefinieerd door gele lijnen op de werkvloer van de productie.</span><span class="sxs-lookup"><span data-stu-id="002a0-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="002a0-105">Deze procedure laat zien hoe u een resourcegroep voor gebruik in afzonderlijke productie definieert.</span><span class="sxs-lookup"><span data-stu-id="002a0-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="002a0-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="002a0-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="002a0-107">Ga naar Resourcegroepen.</span><span class="sxs-lookup"><span data-stu-id="002a0-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="002a0-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="002a0-108">Click New.</span></span>
3. <span data-ttu-id="002a0-109">Typ een waarde in het veld Resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="002a0-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="002a0-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="002a0-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="002a0-111">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="002a0-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="002a0-112">Typ of selecteer een waarde in het veld Productie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="002a0-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="002a0-113">Standaard operationele parameters definiëren</span><span class="sxs-lookup"><span data-stu-id="002a0-113">Define default operational parameters</span></span>
1. <span data-ttu-id="002a0-114">Vouw de sectie Bewerking uit.</span><span class="sxs-lookup"><span data-stu-id="002a0-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="002a0-115">Voer in het veld Uitvalpercentage een getal in.</span><span class="sxs-lookup"><span data-stu-id="002a0-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="002a0-116">Typ of selecteer een waarde in het veld Instelcategorie.</span><span class="sxs-lookup"><span data-stu-id="002a0-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="002a0-117">Typ of selecteer een waarde in het veld Uitvoeringstijdcategorie.</span><span class="sxs-lookup"><span data-stu-id="002a0-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="002a0-118">Voer in het veld Percentage bewerkingsplanning een getal in.</span><span class="sxs-lookup"><span data-stu-id="002a0-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="002a0-119">Bewerkingsuren definiëren</span><span class="sxs-lookup"><span data-stu-id="002a0-119">Define operating hours</span></span>
1. <span data-ttu-id="002a0-120">Vouw de sectie Kalenders uit.</span><span class="sxs-lookup"><span data-stu-id="002a0-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="002a0-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="002a0-121">Click Add.</span></span>
3. <span data-ttu-id="002a0-122">Typ of selecteer een waarde in het veld Kalender.</span><span class="sxs-lookup"><span data-stu-id="002a0-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="002a0-123">Bronnen voor bedrijfsactiviteiten toevoegen</span><span class="sxs-lookup"><span data-stu-id="002a0-123">Add operations resources</span></span>
1. <span data-ttu-id="002a0-124">Vouw de sectie Resources uit.</span><span class="sxs-lookup"><span data-stu-id="002a0-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="002a0-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="002a0-125">Click Add.</span></span>
3. <span data-ttu-id="002a0-126">Typ of selecteer een waarde in het veld Bron.</span><span class="sxs-lookup"><span data-stu-id="002a0-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="002a0-127">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="002a0-127">Click Add.</span></span>
5. <span data-ttu-id="002a0-128">Typ of selecteer een waarde in het veld Bron.</span><span class="sxs-lookup"><span data-stu-id="002a0-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="002a0-129">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="002a0-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="002a0-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="002a0-130">In the list, click the link in the selected row.</span></span>

