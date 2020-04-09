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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140170"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="da03d-103">Klantbetalingen storten</span><span class="sxs-lookup"><span data-stu-id="da03d-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da03d-104">Stort klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="da03d-104">Deposit customer payments.</span></span> <span data-ttu-id="da03d-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="da03d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="da03d-106">Ga naar het **Navigatiedeelvenster > Modules > Klanten > Betalingen > Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="da03d-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="da03d-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="da03d-107">Select **New**.</span></span>
3. <span data-ttu-id="da03d-108">Selecteer in het veld **Naam** **CustPay** in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="da03d-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="da03d-109">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="da03d-109">Select **Lines**.</span></span>
5. <span data-ttu-id="da03d-110">Voer in het veld **Rekening** de klant in voor wie u de betaling hebt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="da03d-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="da03d-111">Voer in het veld **Credit** het bedrag van de betaling in.</span><span class="sxs-lookup"><span data-stu-id="da03d-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="da03d-112">U kunt ervoor kiezen het bedrag leeg te laten en dit door het systeem te laten berekenen door de facturen te selecteren die zijn betaald.</span><span class="sxs-lookup"><span data-stu-id="da03d-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="da03d-113">Typ een waarde in het veld **Betalingsverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="da03d-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="da03d-114">De betalingsverwijzing kan het chequenummer zijn voor de betaling die u invoert.</span><span class="sxs-lookup"><span data-stu-id="da03d-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="da03d-115">De betalingsverwijzing is vereist om de betaling op te nemen op een depositostrook.</span><span class="sxs-lookup"><span data-stu-id="da03d-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="da03d-116">Schakel het selectievakje Depositostrook gebruiken in.</span><span class="sxs-lookup"><span data-stu-id="da03d-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="da03d-117">Als de betaling in de storting moet worden opgenomen, wijzigt u deze instelling in Ja.</span><span class="sxs-lookup"><span data-stu-id="da03d-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="da03d-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="da03d-118">Select **New**.</span></span>
10. <span data-ttu-id="da03d-119">Selecteer in het veld **Rekening** de klant voor de volgende betaling.</span><span class="sxs-lookup"><span data-stu-id="da03d-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="da03d-120">Voer in het veld **Credit** het betalingsbedrag in.</span><span class="sxs-lookup"><span data-stu-id="da03d-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="da03d-121">Typ een waarde in het veld **Betalingsverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="da03d-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="da03d-122">Schakel het selectievakje **Depositostrook gebruiken** in.</span><span class="sxs-lookup"><span data-stu-id="da03d-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="da03d-123">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="da03d-123">Select **Post**.</span></span> <span data-ttu-id="da03d-124">Betalingen moeten worden geboekt voordat de depositostrook kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="da03d-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="da03d-125">Dit moet ervoor zorgen dat betalingen niet veranderen nadat de depositostrook is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="da03d-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="da03d-126">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="da03d-126">Select **Functions**.</span></span>
16. <span data-ttu-id="da03d-127">Selecteer **Depositostrook**.</span><span class="sxs-lookup"><span data-stu-id="da03d-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="da03d-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="da03d-128">Select **OK**.</span></span> <span data-ttu-id="da03d-129">De eerste pagina wordt gebruikt om de depositostrook te maken.</span><span class="sxs-lookup"><span data-stu-id="da03d-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="da03d-130">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="da03d-130">Select **OK**.</span></span> <span data-ttu-id="da03d-131">De tweede stap is het afdrukken van de depositostrook, maar deze stap is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="da03d-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

