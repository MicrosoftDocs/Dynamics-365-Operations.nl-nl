--- 
title: De kwaliteit van goederen inspecteren
description: Deze procedure laat zien hoe u een kwaliteitsorder verwerkt.
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c2313ba26eac8abf6e603f0230f06103802536c4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="6d4c5-103">De kwaliteit van goederen inspecteren</span><span class="sxs-lookup"><span data-stu-id="6d4c5-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d4c5-104">Deze procedure laat zien hoe u een kwaliteitsorder verwerkt.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="6d4c5-105">U kunt deze handleiding uitvoeren in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="6d4c5-106">Voordat u deze voorbeeldprocedure start, moet u aankooporder "000016" bevestigen en een productontvangst boeken.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="6d4c5-107">Hiermee wordt automatisch een kwaliteitsorder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-107">This will automatically create a quality order.</span></span> <span data-ttu-id="6d4c5-108">Kwaliteitscontroles worden gewoonlijk uitgevoerd door een kwaliteitsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="6d4c5-109">Een kwaliteitsorder selecteren</span><span class="sxs-lookup"><span data-stu-id="6d4c5-109">Select a quality order</span></span>
1. <span data-ttu-id="6d4c5-110">Ga naar Voorraadbeheer > Periodieke taken > Kwaliteitsbeheer > Kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="6d4c5-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6d4c5-112">Selecteer de kwaliteitsorder die is gemaakt voordat u deze procedure hebt gestart.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="6d4c5-113">Testresultaten vastleggen</span><span class="sxs-lookup"><span data-stu-id="6d4c5-113">Record test results</span></span>
1. <span data-ttu-id="6d4c5-114">Klik op Resultaten.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-114">Click Results.</span></span>
2. <span data-ttu-id="6d4c5-115">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-115">Click Edit.</span></span>
3. <span data-ttu-id="6d4c5-116">Voer in het veld Resultaathoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="6d4c5-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="6d4c5-118">Klik in het veld Resultaat op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6d4c5-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6d4c5-120">In dit voorbeeld is het resultaat gebaseerd op een vooraf gedefinieerd resultaat.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="6d4c5-121">Normaliter registreert u een specifieker testresultaat, bijvoorbeeld een formaat of andere dimensie.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="6d4c5-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6d4c5-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-123">Click Save.</span></span>
9. <span data-ttu-id="6d4c5-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="6d4c5-125">De kwaliteitsorder valideren</span><span class="sxs-lookup"><span data-stu-id="6d4c5-125">Validate the quality order</span></span>
1. <span data-ttu-id="6d4c5-126">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-126">Click Validate.</span></span>
2. <span data-ttu-id="6d4c5-127">Klik in het veld Gevalideerd door op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6d4c5-128">Selecteer de gebruiker die de inspectie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="6d4c5-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6d4c5-130">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-130">Click Select.</span></span>
5. <span data-ttu-id="6d4c5-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-131">Click OK.</span></span>
6. <span data-ttu-id="6d4c5-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6d4c5-132">Close the page.</span></span>


