---
title: Streepjescodetypen onderhouden
description: Deze procedure toont hoe u een nieuwe definitie van streepjescodes instelt die u vervolgens kunt gebruiken als onderdeel van het rapport van orderverzamellijst.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7834745923bf5ec05018ff5829ddaa0b75df5db7
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145558"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="bce89-103">Streepjescodetypen onderhouden</span><span class="sxs-lookup"><span data-stu-id="bce89-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bce89-104">Deze procedure toont hoe u een nieuwe definitie van streepjescodes instelt die u vervolgens kunt gebruiken als onderdeel van het rapport van orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="bce89-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="bce89-105">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="bce89-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="bce89-106">Als u USMF gebruikt, kunt u de voorbeeldwaarden gebruiken die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bce89-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="bce89-107">Deze taken worden meestal uitgevoerd door een magazijnmanager.</span><span class="sxs-lookup"><span data-stu-id="bce89-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="bce89-108">Ga naar Streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="bce89-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="bce89-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="bce89-109">Click New.</span></span>
3. <span data-ttu-id="bce89-110">Typ een waarde in het veld Instelling van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="bce89-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="bce89-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="bce89-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bce89-112">Selecteer een optie in het veld Streepjescodetype.</span><span class="sxs-lookup"><span data-stu-id="bce89-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="bce89-113">Als u USMF gebruikt, kunt u 'Code 39' selecteren.</span><span class="sxs-lookup"><span data-stu-id="bce89-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="bce89-114">Voer in het veld Grootte een nummer in.</span><span class="sxs-lookup"><span data-stu-id="bce89-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="bce89-115">Voer in het veld Maximumlengte een getal in.</span><span class="sxs-lookup"><span data-stu-id="bce89-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="bce89-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="bce89-116">Click Save.</span></span>
9. <span data-ttu-id="bce89-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bce89-117">Close the page.</span></span>
10. <span data-ttu-id="bce89-118">Ga naar Parameters voor voorraad- en magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="bce89-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="bce89-119">Typ of selecteer een waarde in het veld Instelling van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="bce89-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="bce89-120">Selecteer de instelling van streepjescodes die u eerder hebt gemaakt, maar houd er rekening mee dat de indeling van streepjescodes moet overeenkomen met de indeling van de unieke identificatie van het registratietype die in het proces wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bce89-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="bce89-121">Voor orderverzamelroutes moet de indeling van streepjescodes bijvoorbeeld overeenkomen met de indeling van de verwijzing van de orderverzamelroute, die meestal een nummerreeks is.</span><span class="sxs-lookup"><span data-stu-id="bce89-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="bce89-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="bce89-122">Click Save.</span></span>
13. <span data-ttu-id="bce89-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bce89-123">Close the page.</span></span>

