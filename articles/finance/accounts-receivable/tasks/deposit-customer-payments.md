---
title: Klantbetalingen storten
description: Stort klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220246"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="0085b-103">Klantbetalingen storten</span><span class="sxs-lookup"><span data-stu-id="0085b-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0085b-104">Stort klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="0085b-104">Deposit customer payments.</span></span> <span data-ttu-id="0085b-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0085b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0085b-106">Ga naar het **Navigatiedeelvenster > Modules > Klanten > Betalingen > Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="0085b-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="0085b-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0085b-107">Select **New**.</span></span>
3. <span data-ttu-id="0085b-108">Selecteer in het veld **Naam** **CustPay** in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="0085b-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="0085b-109">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="0085b-109">Select **Lines**.</span></span>
5. <span data-ttu-id="0085b-110">Voer in het veld **Rekening** de klant in voor wie u de betaling hebt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="0085b-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="0085b-111">Voer in het veld **Credit** het bedrag van de betaling in.</span><span class="sxs-lookup"><span data-stu-id="0085b-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="0085b-112">U kunt ervoor kiezen het bedrag leeg te laten en dit door het systeem te laten berekenen door de facturen te selecteren die zijn betaald.</span><span class="sxs-lookup"><span data-stu-id="0085b-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="0085b-113">Typ een waarde in het veld **Betalingsverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="0085b-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="0085b-114">De betalingsverwijzing kan het chequenummer zijn voor de betaling die u invoert.</span><span class="sxs-lookup"><span data-stu-id="0085b-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="0085b-115">De betalingsverwijzing is vereist om de betaling op te nemen op een depositostrook.</span><span class="sxs-lookup"><span data-stu-id="0085b-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="0085b-116">Schakel het selectievakje Depositostrook gebruiken in.</span><span class="sxs-lookup"><span data-stu-id="0085b-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="0085b-117">Als de betaling in de storting moet worden opgenomen, wijzigt u deze instelling in Ja.</span><span class="sxs-lookup"><span data-stu-id="0085b-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="0085b-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0085b-118">Select **New**.</span></span>
10. <span data-ttu-id="0085b-119">Selecteer in het veld **Rekening** de klant voor de volgende betaling.</span><span class="sxs-lookup"><span data-stu-id="0085b-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="0085b-120">Voer in het veld **Credit** het betalingsbedrag in.</span><span class="sxs-lookup"><span data-stu-id="0085b-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="0085b-121">Typ een waarde in het veld **Betalingsverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="0085b-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="0085b-122">Schakel het selectievakje **Depositostrook gebruiken** in.</span><span class="sxs-lookup"><span data-stu-id="0085b-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="0085b-123">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="0085b-123">Select **Post**.</span></span> <span data-ttu-id="0085b-124">Betalingen moeten worden geboekt voordat de depositostrook kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0085b-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="0085b-125">Dit moet ervoor zorgen dat betalingen niet veranderen nadat de depositostrook is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0085b-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="0085b-126">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="0085b-126">Select **Functions**.</span></span>
16. <span data-ttu-id="0085b-127">Selecteer **Depositostrook**.</span><span class="sxs-lookup"><span data-stu-id="0085b-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="0085b-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0085b-128">Select **OK**.</span></span> <span data-ttu-id="0085b-129">De eerste pagina wordt gebruikt om de depositostrook te maken.</span><span class="sxs-lookup"><span data-stu-id="0085b-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="0085b-130">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0085b-130">Select **OK**.</span></span> <span data-ttu-id="0085b-131">De tweede stap is het afdrukken van de depositostrook, maar deze stap is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="0085b-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]