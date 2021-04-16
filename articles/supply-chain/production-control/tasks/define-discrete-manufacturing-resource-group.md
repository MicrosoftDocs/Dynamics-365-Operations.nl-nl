---
title: Resourcegroep voor afzonderlijke productie definiëren
description: Een resourcegroep is een set van bronnen voor bedrijfsactiviteiten die meestal corresponderen met de fysieke organisatie van werkcellen, gedefinieerd door gele lijnen op de werkvloer van de productie.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a8e1c6daa78250118a8a16010ef4cc1b1ae693
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811529"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="31834-103">Resourcegroep voor afzonderlijke productie definiëren</span><span class="sxs-lookup"><span data-stu-id="31834-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31834-104">Een resourcegroep is een set van bronnen voor bedrijfsactiviteiten die meestal corresponderen met de fysieke organisatie van werkcellen, gedefinieerd door gele lijnen op de werkvloer van de productie.</span><span class="sxs-lookup"><span data-stu-id="31834-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="31834-105">Deze procedure laat zien hoe u een resourcegroep voor gebruik in afzonderlijke productie definieert.</span><span class="sxs-lookup"><span data-stu-id="31834-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="31834-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="31834-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="31834-107">Ga naar Resourcegroepen.</span><span class="sxs-lookup"><span data-stu-id="31834-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="31834-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="31834-108">Click New.</span></span>
3. <span data-ttu-id="31834-109">Typ een waarde in het veld Resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="31834-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="31834-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="31834-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31834-111">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="31834-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="31834-112">Typ of selecteer een waarde in het veld Productie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="31834-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="31834-113">Standaard operationele parameters definiëren</span><span class="sxs-lookup"><span data-stu-id="31834-113">Define default operational parameters</span></span>
1. <span data-ttu-id="31834-114">Vouw de sectie Bewerking uit.</span><span class="sxs-lookup"><span data-stu-id="31834-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="31834-115">Voer in het veld Uitvalpercentage een getal in.</span><span class="sxs-lookup"><span data-stu-id="31834-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="31834-116">Typ of selecteer een waarde in het veld Instelcategorie.</span><span class="sxs-lookup"><span data-stu-id="31834-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="31834-117">Typ of selecteer een waarde in het veld Uitvoeringstijdcategorie.</span><span class="sxs-lookup"><span data-stu-id="31834-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="31834-118">Voer in het veld Percentage bewerkingsplanning een getal in.</span><span class="sxs-lookup"><span data-stu-id="31834-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="31834-119">Bewerkingsuren definiëren</span><span class="sxs-lookup"><span data-stu-id="31834-119">Define operating hours</span></span>
1. <span data-ttu-id="31834-120">Vouw de sectie Kalenders uit.</span><span class="sxs-lookup"><span data-stu-id="31834-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="31834-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="31834-121">Click Add.</span></span>
3. <span data-ttu-id="31834-122">Typ of selecteer een waarde in het veld Kalender.</span><span class="sxs-lookup"><span data-stu-id="31834-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="31834-123">Bronnen voor bedrijfsactiviteiten toevoegen</span><span class="sxs-lookup"><span data-stu-id="31834-123">Add operations resources</span></span>
1. <span data-ttu-id="31834-124">Vouw de sectie Resources uit.</span><span class="sxs-lookup"><span data-stu-id="31834-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="31834-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="31834-125">Click Add.</span></span>
3. <span data-ttu-id="31834-126">Typ of selecteer een waarde in het veld Bron.</span><span class="sxs-lookup"><span data-stu-id="31834-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="31834-127">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="31834-127">Click Add.</span></span>
5. <span data-ttu-id="31834-128">Typ of selecteer een waarde in het veld Bron.</span><span class="sxs-lookup"><span data-stu-id="31834-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="31834-129">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31834-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="31834-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31834-130">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]