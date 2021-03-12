---
title: Een rentecode met een bereik maken
description: U kunt rentecodes instellen om verschillende rentebedragen te berekenen op basis van een waardebereik.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f063e24e2c332889191638b4f6ffcb2c08500d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990987"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="219b3-103">Een rentecode met een bereik maken</span><span class="sxs-lookup"><span data-stu-id="219b3-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="219b3-104">U kunt rentecodes instellen om verschillende rentebedragen te berekenen op basis van een waardebereik.</span><span class="sxs-lookup"><span data-stu-id="219b3-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="219b3-105">Deze procedure toont hoe u een rentecode toevoegt en er een bereik aan toevoegt.</span><span class="sxs-lookup"><span data-stu-id="219b3-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="219b3-106">Ga naar Crediteringen en aanmaningen > Rente > Rentecodes instellen.</span><span class="sxs-lookup"><span data-stu-id="219b3-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="219b3-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="219b3-107">Click New.</span></span>
3. <span data-ttu-id="219b3-108">Voer in het veld Rentecode de naam van de rentecode in.</span><span class="sxs-lookup"><span data-stu-id="219b3-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="219b3-109">Type in het veld Omschrijving een omschrijving voor de rentecode.</span><span class="sxs-lookup"><span data-stu-id="219b3-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="219b3-110">Selecteer Maand.</span><span class="sxs-lookup"><span data-stu-id="219b3-110">Select Month.</span></span>
6. <span data-ttu-id="219b3-111">Vouw de sectie Inkomsten uit.</span><span class="sxs-lookup"><span data-stu-id="219b3-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="219b3-112">Vouw de sectie Inkomsten per valuta uit.</span><span class="sxs-lookup"><span data-stu-id="219b3-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="219b3-113">Geef in het veld Grootboekboekingsrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="219b3-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="219b3-114">Selecteer 'Maanden' in het veld Rente per bereik.</span><span class="sxs-lookup"><span data-stu-id="219b3-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="219b3-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="219b3-115">Click Add.</span></span>
11. <span data-ttu-id="219b3-116">Voer in het veld Omschrijving een omschrijving van deze valuta en dit bereik in.</span><span class="sxs-lookup"><span data-stu-id="219b3-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="219b3-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="219b3-117">Click Save.</span></span>
13. <span data-ttu-id="219b3-118">Klik op Bereiken.</span><span class="sxs-lookup"><span data-stu-id="219b3-118">Click Ranges.</span></span>
14. <span data-ttu-id="219b3-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="219b3-119">Click New.</span></span>
15. <span data-ttu-id="219b3-120">Voer 0 in als Vanaf waarde en voer vervolgens het rentepercentage per maand in dat wordt gebruikt om de rente te berekenen.</span><span class="sxs-lookup"><span data-stu-id="219b3-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="219b3-121">In ons voorbeeld is dit 1,5.</span><span class="sxs-lookup"><span data-stu-id="219b3-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="219b3-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="219b3-122">Click New.</span></span>
17. <span data-ttu-id="219b3-123">Voer 4 in voor de volgende Vanaf waarde. Dit is de eerste maand waarin u een nieuw rentebedrag berekent.</span><span class="sxs-lookup"><span data-stu-id="219b3-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="219b3-124">Voer het rentepercentage per maand in dat wordt gebruikt om de rente te berekenen vanaf maand 4.</span><span class="sxs-lookup"><span data-stu-id="219b3-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="219b3-125">In dit voorbeeld is dit 2,0.</span><span class="sxs-lookup"><span data-stu-id="219b3-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="219b3-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="219b3-126">Click New.</span></span>
20. <span data-ttu-id="219b3-127">Voer 7 in voor de volgende Vanaf waarde. Dit is de volgende maand waarin u een nieuw rentebedrag berekent.</span><span class="sxs-lookup"><span data-stu-id="219b3-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="219b3-128">Voer het rentepercentage per maand in dat wordt gebruikt om de rente te berekenen vanaf maand 7.</span><span class="sxs-lookup"><span data-stu-id="219b3-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="219b3-129">In dit voorbeeld is dit 2,5.</span><span class="sxs-lookup"><span data-stu-id="219b3-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="219b3-130">Klik op Sluiten om de instelling te beëindigen.</span><span class="sxs-lookup"><span data-stu-id="219b3-130">Click Close to complete the setup.</span></span>

