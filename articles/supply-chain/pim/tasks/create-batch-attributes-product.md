---
title: Batchkenmerken maken voor een product
description: Deze procedure laat zien hoe u een batchkenmerk maakt, standaardwaardebereiken toewijst en het kenmerk opneemt in een groep.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d874b6b6e53164c00d9b4656d27b1060f4e3ba06
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934930"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="20733-103">Batchkenmerken maken voor een product</span><span class="sxs-lookup"><span data-stu-id="20733-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20733-104">Deze procedure laat zien hoe u een batchkenmerk maakt, standaardwaardebereiken toewijst en het kenmerk opneemt in een groep.</span><span class="sxs-lookup"><span data-stu-id="20733-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="20733-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is het bedrijf USP2.</span><span class="sxs-lookup"><span data-stu-id="20733-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="20733-106">Ga naar Voorraadbeheer > Instellingen > Batch > Batchkenmerken.</span><span class="sxs-lookup"><span data-stu-id="20733-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="20733-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="20733-107">Click New.</span></span>
3. <span data-ttu-id="20733-108">Typ een waarde in het veld Kenmerk.</span><span class="sxs-lookup"><span data-stu-id="20733-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="20733-109">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="20733-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="20733-110">Selecteer 'Fractie" in het veld Kenmerktype.</span><span class="sxs-lookup"><span data-stu-id="20733-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="20733-111">Deze procedure gebruikt om het type Fractie om decimale waarden mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="20733-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="20733-112">U kunt ook andere kenmerktypen selecteren.</span><span class="sxs-lookup"><span data-stu-id="20733-112">You can select other attribute types.</span></span> <span data-ttu-id="20733-113">Als u het type Opsomming selecteert, moet u waarden in de opsomminglijst invoeren voordat u een waarde in het veld Doel kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="20733-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="20733-114">Voer een getal in het veld Minimum in.</span><span class="sxs-lookup"><span data-stu-id="20733-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="20733-115">Voer een getal in het veld Maximum in.</span><span class="sxs-lookup"><span data-stu-id="20733-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="20733-116">Voer een getal in het veld Verhoging in.</span><span class="sxs-lookup"><span data-stu-id="20733-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="20733-117">Typ een waarde in het veld Doel.</span><span class="sxs-lookup"><span data-stu-id="20733-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="20733-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="20733-118">Click Save.</span></span>
11. <span data-ttu-id="20733-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="20733-119">Close the page.</span></span>
12. <span data-ttu-id="20733-120">Ga naar Voorraadbeheer > Instellingen > Batch > Batchkenmerkgroepen.</span><span class="sxs-lookup"><span data-stu-id="20733-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="20733-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="20733-121">Click New.</span></span>
14. <span data-ttu-id="20733-122">Typ een waarde in het veld Kenmerkgroep.</span><span class="sxs-lookup"><span data-stu-id="20733-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="20733-123">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="20733-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="20733-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="20733-124">Click Save.</span></span>
17. <span data-ttu-id="20733-125">Klik op Groepkenmerken.</span><span class="sxs-lookup"><span data-stu-id="20733-125">Click Group attributes.</span></span>
18. <span data-ttu-id="20733-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="20733-126">Click New.</span></span>
19. <span data-ttu-id="20733-127">Klik in het veld Kenmerk op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="20733-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="20733-128">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="20733-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="20733-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="20733-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="20733-130">Een kenmerk kan in elk van de groepen worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="20733-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="20733-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="20733-131">Click Save.</span></span>
23. <span data-ttu-id="20733-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="20733-132">Close the page.</span></span>

