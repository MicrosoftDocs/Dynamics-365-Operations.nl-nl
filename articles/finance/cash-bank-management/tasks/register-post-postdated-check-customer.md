---
title: Een gepostdateerde cheque voor een klant registreren en boeken
description: U kunt gegevens van een gepostdateerde cheque die u van een klant hebt ontvangen, registreren.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f27675a2aa2160619bf78eea33bba2ce0b7bd81
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188091"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="e867d-103">Een gepostdateerde cheque voor een klant registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="e867d-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e867d-104">U kunt gegevens van een gepostdateerde cheque die u van een klant hebt ontvangen, registreren.</span><span class="sxs-lookup"><span data-stu-id="e867d-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="e867d-105">U kunt de gepostdateerde cheque ook boeken en financiële transacties genereren.</span><span class="sxs-lookup"><span data-stu-id="e867d-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="e867d-106">Voer de volgende taken uit voordat u een gepostdateerde cheque die u van een klant hebt ontvangen, registreert en boekt:   • Stel gepostdateerde cheques in op de pagina Contanten en bankbeheer • Stel een betalingsmethode voor gepostdateerde cheques in   De rol voor deze procedure is Penningmeester.</span><span class="sxs-lookup"><span data-stu-id="e867d-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="e867d-107">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e867d-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="e867d-108">Ga naar Klanten > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="e867d-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e867d-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e867d-109">Click New.</span></span>
3. <span data-ttu-id="e867d-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e867d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e867d-111">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="e867d-111">Click Lines.</span></span>
5. <span data-ttu-id="e867d-112">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e867d-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e867d-113">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="e867d-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="e867d-114">Voer een nummer in het veld Credit in.</span><span class="sxs-lookup"><span data-stu-id="e867d-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="e867d-115">Voer het bedrag in dat is opgegeven op de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="e867d-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="e867d-116">Klik op het tabblad Betaling.</span><span class="sxs-lookup"><span data-stu-id="e867d-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="e867d-117">Typ een waarde in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="e867d-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="e867d-118">Selecteer de betalingsmethode voor de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="e867d-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="e867d-119">Klik op het tabblad Gepostdateerde cheques.</span><span class="sxs-lookup"><span data-stu-id="e867d-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="e867d-120">Voer een datum in het veld Vervaldatum in.</span><span class="sxs-lookup"><span data-stu-id="e867d-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="e867d-121">Voer de datum in waarop de gepostdateerde cheque moet worden betaald.</span><span class="sxs-lookup"><span data-stu-id="e867d-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="e867d-122">Typ een waarde in het veld Afdeling van uitgevende bank.</span><span class="sxs-lookup"><span data-stu-id="e867d-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="e867d-123">Voer de bankdetails in van de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="e867d-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="e867d-124">Typ een waarde in het veld Chequenummer.</span><span class="sxs-lookup"><span data-stu-id="e867d-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="e867d-125">Typ een waarde in het veld Naam van uitgevende bank.</span><span class="sxs-lookup"><span data-stu-id="e867d-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="e867d-126">Voer de bankdetails in van de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="e867d-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="e867d-127">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="e867d-127">Click Post.</span></span>
16. <span data-ttu-id="e867d-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e867d-128">Close the page.</span></span>
