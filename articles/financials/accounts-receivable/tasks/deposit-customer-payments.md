---
title: Klantbetalingen storten
description: Stort klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "313377"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="dfefc-103">Klantbetalingen storten</span><span class="sxs-lookup"><span data-stu-id="dfefc-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfefc-104">Stort klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="dfefc-104">Deposit customer payments.</span></span> <span data-ttu-id="dfefc-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="dfefc-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="dfefc-106">Ga naar Klanten > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="dfefc-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="dfefc-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="dfefc-107">Click New.</span></span>
3. <span data-ttu-id="dfefc-108">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="dfefc-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dfefc-109">Selecteer het betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="dfefc-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="dfefc-110">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="dfefc-110">Click Lines.</span></span>
6. <span data-ttu-id="dfefc-111">Voer in het veld Rekening de klant in voor wie u de betaling hebt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="dfefc-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="dfefc-112">Voer in het veld Credit het bedrag van de betaling in.</span><span class="sxs-lookup"><span data-stu-id="dfefc-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="dfefc-113">U kunt ervoor kiezen het bedrag leeg te laten en dit door het systeem te laten berekenen door de facturen te selecteren die zijn betaald.</span><span class="sxs-lookup"><span data-stu-id="dfefc-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="dfefc-114">Typ een waarde in het veld Betalingsverwijzing.</span><span class="sxs-lookup"><span data-stu-id="dfefc-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="dfefc-115">De betalingsverwijzing kan het chequenummer zijn voor de betaling die u invoert.</span><span class="sxs-lookup"><span data-stu-id="dfefc-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="dfefc-116">De betalingsverwijzing is vereist om de betaling op te nemen op een depositostrook.</span><span class="sxs-lookup"><span data-stu-id="dfefc-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="dfefc-117">Schakel het selectievakje Depositostrook gebruiken in.</span><span class="sxs-lookup"><span data-stu-id="dfefc-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="dfefc-118">Als de betaling in de storting moet worden opgenomen, wijzigt u deze instelling in Ja.</span><span class="sxs-lookup"><span data-stu-id="dfefc-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="dfefc-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="dfefc-119">Click New.</span></span>
11. <span data-ttu-id="dfefc-120">Selecteer in het veld Rekening de klant voor de volgende betaling.</span><span class="sxs-lookup"><span data-stu-id="dfefc-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="dfefc-121">Voer in het veld Credit het betalingsbedrag in.</span><span class="sxs-lookup"><span data-stu-id="dfefc-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="dfefc-122">Typ een waarde in het veld Betalingsverwijzing.</span><span class="sxs-lookup"><span data-stu-id="dfefc-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="dfefc-123">Schakel het selectievakje Depositostrook gebruiken in.</span><span class="sxs-lookup"><span data-stu-id="dfefc-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="dfefc-124">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="dfefc-124">Click Post.</span></span>
    * <span data-ttu-id="dfefc-125">Betalingen moeten worden geboekt voordat de depositostrook kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="dfefc-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="dfefc-126">Dit moet ervoor zorgen dat betalingen niet veranderen nadat de depositostrook is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="dfefc-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="dfefc-127">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="dfefc-127">Click Functions.</span></span>
17. <span data-ttu-id="dfefc-128">Klik op Depositostrook.</span><span class="sxs-lookup"><span data-stu-id="dfefc-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="dfefc-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="dfefc-129">Click OK.</span></span>
    * <span data-ttu-id="dfefc-130">De eerste pagina wordt gebruikt om de depositostrook te maken.</span><span class="sxs-lookup"><span data-stu-id="dfefc-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="dfefc-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="dfefc-131">Click OK.</span></span>
    * <span data-ttu-id="dfefc-132">De tweede stap is het afdrukken van de depositostrook, maar deze stap is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="dfefc-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

