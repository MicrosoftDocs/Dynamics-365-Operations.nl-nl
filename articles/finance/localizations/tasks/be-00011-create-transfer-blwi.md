---
title: Transacties maken en overboeken naar het BLWI (België)
description: Deze procedure begeleidt u bij het maken van een BLWI-rapport voor België.
author: v-oloski
manager: AnnBe
ms.date: 07/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Belgium
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14669854a5ef73ea1f0a96ac5997dca69454ff5b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183817"
---
# <a name="create-and-transfer-transactions-to-the-blwi-belgium"></a><span data-ttu-id="4e80a-103">Transacties maken en overboeken naar het BLWI (België)</span><span class="sxs-lookup"><span data-stu-id="4e80a-103">Create and transfer transactions to the BLWI (Belgium)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e80a-104">Deze procedure begeleidt u bij het maken van een BLWI-rapport voor België.</span><span class="sxs-lookup"><span data-stu-id="4e80a-104">This procedure walks you through creating BLWI report for the Belgium.</span></span> <span data-ttu-id="4e80a-105">Deze procedure is gemaakt met het demogegevensbedrijf USSI.</span><span class="sxs-lookup"><span data-stu-id="4e80a-105">This procedure was created using the demo data company USSI.</span></span> <span data-ttu-id="4e80a-106">Deze functionaliteit is beschikbaar voor rechtspersonen die hun primaire adres in België hebben.</span><span class="sxs-lookup"><span data-stu-id="4e80a-106">This functionality is available for legal entities whose primary address is in the Belgium.</span></span> <span data-ttu-id="4e80a-107">Ook is het nodig om een registratie-id voor België in te stellen en het registratienummer in te vullen, om een BLWI-aangifte te maken.</span><span class="sxs-lookup"><span data-stu-id="4e80a-107">Also it is necessary to set up Registration ID for Belgium and fill in Registration number in order to create BLWI declaration.</span></span>

<span data-ttu-id="4e80a-108">Als u een transactie naar BLWI wilt maken, moet eerder BLWI-informatie (Belgisch Luxemburgs Wissel Instituut) zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="4e80a-108">To create and transfer transaction to the BLWI it is necessary previously to set up Belgisch Luxemburgs Wissel Instituut (BLWI) information.</span></span>

<span data-ttu-id="4e80a-109">Klant- of leverancierstransacties gemarkeerd met een van de gekozen betalingsdoelcodes waarvan het primaire klant-/leveranciersadres in een ander land ligt dan het land van de rechtspersoon, worden opgenomen in het BLWI-rapport.</span><span class="sxs-lookup"><span data-stu-id="4e80a-109">Customer/vendor transactions marked with one of the chosen payment purpose codes with customer/vendor primary address is in the country different from the country of legal entity are included in BLWI report.</span></span>

1. <span data-ttu-id="4e80a-110">Ga naar Belasting > Aangiften > Buitenlandse handel > BLWI.</span><span class="sxs-lookup"><span data-stu-id="4e80a-110">Go to Tax > Declarations > Foreign trade > BLWI.</span></span>
2. <span data-ttu-id="4e80a-111">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="4e80a-111">Click Transfer.</span></span>
3. <span data-ttu-id="4e80a-112">Typ of selecteer een waarde in het veld Onderzoekscode.</span><span class="sxs-lookup"><span data-stu-id="4e80a-112">In the Survey code field, enter or select a value.</span></span>
4. <span data-ttu-id="4e80a-113">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="4e80a-113">In the Date field, enter a date.</span></span>
5. <span data-ttu-id="4e80a-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4e80a-114">Click OK.</span></span>
6. <span data-ttu-id="4e80a-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4e80a-115">Click New.</span></span>
7. <span data-ttu-id="4e80a-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4e80a-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4e80a-117">Selecteer een optie in het veld BLWI-transactie.</span><span class="sxs-lookup"><span data-stu-id="4e80a-117">In the BLWI transaction field, select an option.</span></span>
9. <span data-ttu-id="4e80a-118">Typ of selecteer een waarde in het veld Rekeningnummer.</span><span class="sxs-lookup"><span data-stu-id="4e80a-118">In the Account number field, enter or select a value.</span></span>
10. <span data-ttu-id="4e80a-119">Typ een getal in het veld Bedrag in transactievaluta.</span><span class="sxs-lookup"><span data-stu-id="4e80a-119">In the Amount in transaction currency field, enter a number.</span></span>
11. <span data-ttu-id="4e80a-120">Typ of selecteer een waarde in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="4e80a-120">In the Country/region field, enter or select a value.</span></span>
12. <span data-ttu-id="4e80a-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4e80a-121">Click Save.</span></span>
13. <span data-ttu-id="4e80a-122">Klik op XML-bestand maken.</span><span class="sxs-lookup"><span data-stu-id="4e80a-122">Click Create XML file.</span></span>
14. <span data-ttu-id="4e80a-123">Typ of selecteer een waarde in het veld Onderzoekscode.</span><span class="sxs-lookup"><span data-stu-id="4e80a-123">In the Survey code field, enter or select a value.</span></span>
15. <span data-ttu-id="4e80a-124">Typ een waarde in het veld Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="4e80a-124">In the File name field, type a value.</span></span>
16. <span data-ttu-id="4e80a-125">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="4e80a-125">In the Date field, enter a date.</span></span>
17. <span data-ttu-id="4e80a-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4e80a-126">Click OK.</span></span>
18. <span data-ttu-id="4e80a-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4e80a-127">Close the page.</span></span>
