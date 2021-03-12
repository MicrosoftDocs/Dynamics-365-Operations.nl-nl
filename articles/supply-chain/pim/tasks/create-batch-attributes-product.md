---
title: Batchkenmerken maken voor een product
description: Deze procedure laat zien hoe u een batchkenmerk maakt, standaardwaardebereiken toewijst en het kenmerk opneemt in een groep.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d51cecc800a827fe91583b6086fd88b10aedc41
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986924"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="a69de-103">Batchkenmerken maken voor een product</span><span class="sxs-lookup"><span data-stu-id="a69de-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a69de-104">Deze procedure laat zien hoe u een batchkenmerk maakt, standaardwaardebereiken toewijst en het kenmerk opneemt in een groep.</span><span class="sxs-lookup"><span data-stu-id="a69de-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="a69de-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is het bedrijf USP2.</span><span class="sxs-lookup"><span data-stu-id="a69de-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="a69de-106">Ga naar Voorraadbeheer > Instellingen > Batch > Batchkenmerken.</span><span class="sxs-lookup"><span data-stu-id="a69de-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="a69de-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a69de-107">Click New.</span></span>
3. <span data-ttu-id="a69de-108">Typ een waarde in het veld Kenmerk.</span><span class="sxs-lookup"><span data-stu-id="a69de-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="a69de-109">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a69de-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a69de-110">Selecteer 'Fractie" in het veld Kenmerktype.</span><span class="sxs-lookup"><span data-stu-id="a69de-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="a69de-111">Deze procedure gebruikt om het type Fractie om decimale waarden mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="a69de-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="a69de-112">U kunt ook andere kenmerktypen selecteren.</span><span class="sxs-lookup"><span data-stu-id="a69de-112">You can select other attribute types.</span></span> <span data-ttu-id="a69de-113">Als u het type Opsomming selecteert, moet u waarden in de opsomminglijst invoeren voordat u een waarde in het veld Doel kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a69de-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="a69de-114">Voer een getal in het veld Minimum in.</span><span class="sxs-lookup"><span data-stu-id="a69de-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="a69de-115">Voer een getal in het veld Maximum in.</span><span class="sxs-lookup"><span data-stu-id="a69de-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="a69de-116">Voer een getal in het veld Verhoging in.</span><span class="sxs-lookup"><span data-stu-id="a69de-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="a69de-117">Typ een waarde in het veld Doel.</span><span class="sxs-lookup"><span data-stu-id="a69de-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="a69de-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a69de-118">Click Save.</span></span>
11. <span data-ttu-id="a69de-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a69de-119">Close the page.</span></span>
12. <span data-ttu-id="a69de-120">Ga naar Voorraadbeheer > Instellingen > Batch > Batchkenmerkgroepen.</span><span class="sxs-lookup"><span data-stu-id="a69de-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="a69de-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a69de-121">Click New.</span></span>
14. <span data-ttu-id="a69de-122">Typ een waarde in het veld Kenmerkgroep.</span><span class="sxs-lookup"><span data-stu-id="a69de-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="a69de-123">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a69de-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="a69de-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a69de-124">Click Save.</span></span>
17. <span data-ttu-id="a69de-125">Klik op Groepkenmerken.</span><span class="sxs-lookup"><span data-stu-id="a69de-125">Click Group attributes.</span></span>
18. <span data-ttu-id="a69de-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a69de-126">Click New.</span></span>
19. <span data-ttu-id="a69de-127">Klik in het veld Kenmerk op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a69de-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="a69de-128">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a69de-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="a69de-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a69de-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a69de-130">Een kenmerk kan in elk van de groepen worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="a69de-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="a69de-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a69de-131">Click Save.</span></span>
23. <span data-ttu-id="a69de-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a69de-132">Close the page.</span></span>

