---
title: Klantbetalingen storten
description: Stort klantbetalingen.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bf44570a0eaceab94765b100bdd8b4d507a0f54
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822366"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="091ac-103">Klantbetalingen storten</span><span class="sxs-lookup"><span data-stu-id="091ac-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="091ac-104">Stort klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="091ac-104">Deposit customer payments.</span></span> <span data-ttu-id="091ac-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="091ac-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="091ac-106">Ga naar het **Navigatiedeelvenster > Modules > Klanten > Betalingen > Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="091ac-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="091ac-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="091ac-107">Select **New**.</span></span>
3. <span data-ttu-id="091ac-108">Selecteer in het veld **Naam** **CustPay** in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="091ac-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="091ac-109">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="091ac-109">Select **Lines**.</span></span>
5. <span data-ttu-id="091ac-110">Voer in het veld **Rekening** de klant in voor wie u de betaling hebt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="091ac-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="091ac-111">Voer in het veld **Credit** het bedrag van de betaling in.</span><span class="sxs-lookup"><span data-stu-id="091ac-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="091ac-112">U kunt ervoor kiezen het bedrag leeg te laten en dit door het systeem te laten berekenen door de facturen te selecteren die zijn betaald.</span><span class="sxs-lookup"><span data-stu-id="091ac-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="091ac-113">Typ een waarde in het veld **Betalingsverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="091ac-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="091ac-114">De betalingsverwijzing kan het chequenummer zijn voor de betaling die u invoert.</span><span class="sxs-lookup"><span data-stu-id="091ac-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="091ac-115">De betalingsverwijzing is vereist om de betaling op te nemen op een depositostrook.</span><span class="sxs-lookup"><span data-stu-id="091ac-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="091ac-116">Schakel het selectievakje Depositostrook gebruiken in.</span><span class="sxs-lookup"><span data-stu-id="091ac-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="091ac-117">Als de betaling in de storting moet worden opgenomen, wijzigt u deze instelling in Ja.</span><span class="sxs-lookup"><span data-stu-id="091ac-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="091ac-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="091ac-118">Select **New**.</span></span>
10. <span data-ttu-id="091ac-119">Selecteer in het veld **Rekening** de klant voor de volgende betaling.</span><span class="sxs-lookup"><span data-stu-id="091ac-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="091ac-120">Voer in het veld **Credit** het betalingsbedrag in.</span><span class="sxs-lookup"><span data-stu-id="091ac-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="091ac-121">Typ een waarde in het veld **Betalingsverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="091ac-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="091ac-122">Schakel het selectievakje **Depositostrook gebruiken** in.</span><span class="sxs-lookup"><span data-stu-id="091ac-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="091ac-123">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="091ac-123">Select **Post**.</span></span> <span data-ttu-id="091ac-124">Betalingen moeten worden geboekt voordat de depositostrook kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="091ac-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="091ac-125">Dit moet ervoor zorgen dat betalingen niet veranderen nadat de depositostrook is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="091ac-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="091ac-126">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="091ac-126">Select **Functions**.</span></span>
16. <span data-ttu-id="091ac-127">Selecteer **Depositostrook**.</span><span class="sxs-lookup"><span data-stu-id="091ac-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="091ac-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="091ac-128">Select **OK**.</span></span> <span data-ttu-id="091ac-129">De eerste pagina wordt gebruikt om de depositostrook te maken.</span><span class="sxs-lookup"><span data-stu-id="091ac-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="091ac-130">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="091ac-130">Select **OK**.</span></span> <span data-ttu-id="091ac-131">De tweede stap is het afdrukken van de depositostrook, maar deze stap is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="091ac-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]