---
title: Streepjescodetypen onderhouden
description: Deze procedure toont hoe u een nieuwe definitie van streepjescodes instelt die u vervolgens kunt gebruiken als onderdeel van het rapport van orderverzamellijst.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71bbc090d928cb80d19db33655ec9c9cc8e654bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011492"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="313c4-103">Streepjescodetypen onderhouden</span><span class="sxs-lookup"><span data-stu-id="313c4-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="313c4-104">Deze procedure toont hoe u een nieuwe definitie van streepjescodes instelt die u vervolgens kunt gebruiken als onderdeel van het rapport van orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="313c4-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="313c4-105">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="313c4-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="313c4-106">Als u USMF gebruikt, kunt u de voorbeeldwaarden gebruiken die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="313c4-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="313c4-107">Deze taken worden meestal uitgevoerd door een magazijnmanager.</span><span class="sxs-lookup"><span data-stu-id="313c4-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="313c4-108">Ga naar Streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="313c4-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="313c4-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="313c4-109">Click New.</span></span>
3. <span data-ttu-id="313c4-110">Typ een waarde in het veld Instelling van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="313c4-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="313c4-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="313c4-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="313c4-112">Selecteer een optie in het veld Streepjescodetype.</span><span class="sxs-lookup"><span data-stu-id="313c4-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="313c4-113">Als u USMF gebruikt, kunt u 'Code 39' selecteren.</span><span class="sxs-lookup"><span data-stu-id="313c4-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="313c4-114">Voer in het veld Grootte een nummer in.</span><span class="sxs-lookup"><span data-stu-id="313c4-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="313c4-115">Voer in het veld Maximumlengte een getal in.</span><span class="sxs-lookup"><span data-stu-id="313c4-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="313c4-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="313c4-116">Click Save.</span></span>
9. <span data-ttu-id="313c4-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="313c4-117">Close the page.</span></span>
10. <span data-ttu-id="313c4-118">Ga naar Parameters voor voorraad- en magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="313c4-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="313c4-119">Typ of selecteer een waarde in het veld Instelling van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="313c4-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="313c4-120">Selecteer de instelling van streepjescodes die u eerder hebt gemaakt, maar houd er rekening mee dat de indeling van streepjescodes moet overeenkomen met de indeling van de unieke identificatie van het registratietype die in het proces wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="313c4-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="313c4-121">Voor orderverzamelroutes moet de indeling van streepjescodes bijvoorbeeld overeenkomen met de indeling van de verwijzing van de orderverzamelroute, die meestal een nummerreeks is.</span><span class="sxs-lookup"><span data-stu-id="313c4-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="313c4-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="313c4-122">Click Save.</span></span>
13. <span data-ttu-id="313c4-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="313c4-123">Close the page.</span></span>

