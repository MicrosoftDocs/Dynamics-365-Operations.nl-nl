---
title: Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken
description: In deze procedure wordt voorgedaan hoe u een recordsjabloon kunt maken, zodat vaak gebruikte veldwaarden niet expliciet moeten worden ingevoerd voor elke nieuwe record.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544247"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="f8a51-103">Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="f8a51-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8a51-104">In deze procedure wordt voorgedaan hoe u een recordsjabloon kunt maken, zodat vaak gebruikte veldwaarden niet expliciet moeten worden ingevoerd voor elke nieuwe record.</span><span class="sxs-lookup"><span data-stu-id="f8a51-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="f8a51-105">In deze procedure maakt u een nieuwe record voor nieuwe laptops die u wilt laten toevoegen aan uw vaste activa.</span><span class="sxs-lookup"><span data-stu-id="f8a51-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="f8a51-106">In deze procedure wordt het voorbeeldbedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f8a51-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="f8a51-107">Ga naar Vaste activa > Vaste activa > Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="f8a51-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="f8a51-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f8a51-108">Click New.</span></span>
3. <span data-ttu-id="f8a51-109">Typ of selecteer een waarde in het veld Groep vaste activa.</span><span class="sxs-lookup"><span data-stu-id="f8a51-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="f8a51-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f8a51-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f8a51-111">Voer bijvoorbeeld 'Corporate lead-laptop' in.</span><span class="sxs-lookup"><span data-stu-id="f8a51-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="f8a51-112">Typ een waarde in het veld Zoeknaam.</span><span class="sxs-lookup"><span data-stu-id="f8a51-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="f8a51-113">Voer bijvoorbeeld 'laptop' in.</span><span class="sxs-lookup"><span data-stu-id="f8a51-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="f8a51-114">Vouw de sectie Technische informatie uit.</span><span class="sxs-lookup"><span data-stu-id="f8a51-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="f8a51-115">Typ een waarde in het veld Merk.</span><span class="sxs-lookup"><span data-stu-id="f8a51-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="f8a51-116">Typ een waarde in het veld Model.</span><span class="sxs-lookup"><span data-stu-id="f8a51-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="f8a51-117">Typ een waarde in het veld Bouwjaar.</span><span class="sxs-lookup"><span data-stu-id="f8a51-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="f8a51-118">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="f8a51-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="f8a51-119">Klik op Recordinfo.</span><span class="sxs-lookup"><span data-stu-id="f8a51-119">Click Record info.</span></span>
12. <span data-ttu-id="f8a51-120">Klik op Gebruikersjabloon.</span><span class="sxs-lookup"><span data-stu-id="f8a51-120">Click User template.</span></span>
13. <span data-ttu-id="f8a51-121">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f8a51-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f8a51-122">Voer bijvoorbeeld 'Corporate laptop' in.</span><span class="sxs-lookup"><span data-stu-id="f8a51-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="f8a51-123">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="f8a51-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f8a51-124">Voer bijvoorbeeld 'Corporate laptop' in.</span><span class="sxs-lookup"><span data-stu-id="f8a51-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="f8a51-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f8a51-125">Click OK.</span></span>
16. <span data-ttu-id="f8a51-126">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="f8a51-126">Click Close.</span></span>

