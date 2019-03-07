---
title: Afgerond bedrag voor afschrijvingsberekeningen
description: In dit artikel wordt het veld Afschrijving afronden besproken uit de pagina's Instellingen voor boeken.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "308409"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="17791-103">Afgerond bedrag voor afschrijvingsberekeningen</span><span class="sxs-lookup"><span data-stu-id="17791-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17791-104">In dit artikel wordt het veld Afschrijving afronden besproken uit de pagina's Instellingen voor boeken.</span><span class="sxs-lookup"><span data-stu-id="17791-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="17791-105">Afgeronde afschrijvingsbedragen worden ingesteld voor elk boek.</span><span class="sxs-lookup"><span data-stu-id="17791-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="17791-106">Afgeronde afschrijvingsbedragen worden gebruikt in het afschrijvingsprofiel voor vaste activa dat de toekomstige afschrijving en waarde van het vaste activum weergeeft, en ook in afschrijvingsvoorstellen.</span><span class="sxs-lookup"><span data-stu-id="17791-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="17791-107">Voer het laagste afschrijvingsbedrag in dat is toegestaan voor het boek.</span><span class="sxs-lookup"><span data-stu-id="17791-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="17791-108">Ongeacht de afronding die is ingesteld, wordt het afschrijvingsbedrag in de laatste afschrijvingsperiode niet afgerond.</span><span class="sxs-lookup"><span data-stu-id="17791-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="17791-109">Aan het einde van de laatste afschrijvingsperiode moet de waarde van het vaste activum 0 (nul) of de restwaarde zijn als de restwaarde wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="17791-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="17791-110">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="17791-110">Example</span></span>

<span data-ttu-id="17791-111">Afschrijving zonder afronding wordt berekend als 2444,44.</span><span class="sxs-lookup"><span data-stu-id="17791-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="17791-112">Zoals te zien in de volgende tabel, variëren de bedragen die worden voorgesteld, afhankelijk van hoe de afronding is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="17791-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="17791-113">Afrondingsmethode</span><span class="sxs-lookup"><span data-stu-id="17791-113">Rounding method</span></span> | <span data-ttu-id="17791-114">Afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="17791-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="17791-115">Afronding van 0,1</span><span class="sxs-lookup"><span data-stu-id="17791-115">Rounding 0.1</span></span>    | <span data-ttu-id="17791-116">2444,40</span><span class="sxs-lookup"><span data-stu-id="17791-116">2,444.40</span></span>            |
| <span data-ttu-id="17791-117">Afronding van 1,00</span><span class="sxs-lookup"><span data-stu-id="17791-117">Rounding 1.00</span></span>   | <span data-ttu-id="17791-118">2444,00</span><span class="sxs-lookup"><span data-stu-id="17791-118">2,444.00</span></span>            |
| <span data-ttu-id="17791-119">Afronding van 10,00</span><span class="sxs-lookup"><span data-stu-id="17791-119">Rounding 10.00</span></span>  | <span data-ttu-id="17791-120">2440,00</span><span class="sxs-lookup"><span data-stu-id="17791-120">2,440.00</span></span>            |
| <span data-ttu-id="17791-121">Afronding van 100,00</span><span class="sxs-lookup"><span data-stu-id="17791-121">Rounding 100.00</span></span> | <span data-ttu-id="17791-122">2400,00</span><span class="sxs-lookup"><span data-stu-id="17791-122">2,400.00</span></span>            |





