---
title: Gepostdateerde cheques instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442028"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="9df3e-103">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="9df3e-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9df3e-104">In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen.</span><span class="sxs-lookup"><span data-stu-id="9df3e-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="9df3e-105">U kunt tijdelijke rekeningen opgeven voor uitgegeven cheques, ontvangen cheques en bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="9df3e-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="9df3e-106">Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="9df3e-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="9df3e-107">U kunt opgeven of de cheque vóór de vervaldatum in uw boekhoudingsstukken moet worden weerspiegeld.</span><span class="sxs-lookup"><span data-stu-id="9df3e-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="9df3e-108">De rol van deze procedure is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="9df3e-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="9df3e-109">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9df3e-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="9df3e-110">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="9df3e-110">Set up postdated checks</span></span>
1. <span data-ttu-id="9df3e-111">Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.</span><span class="sxs-lookup"><span data-stu-id="9df3e-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="9df3e-112">Klik op het tabblad Gepostdateerde cheques.</span><span class="sxs-lookup"><span data-stu-id="9df3e-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="9df3e-113">Schakel het selectievakje Gepostdateerde cheques inschakelen in of uit.</span><span class="sxs-lookup"><span data-stu-id="9df3e-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="9df3e-114">Schakel het selectievakje Journaalboekingen voor gepostdateerde cheques uitvoeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="9df3e-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="9df3e-115">Geef in het veld Aflossingsrekening voor uitgegeven cheques de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="9df3e-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="9df3e-116">Geef in het veld Aflossingsrekening voor ontvangen cheques de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="9df3e-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="9df3e-117">Typ een waarde in het veld Algemeen journaal voor aflossingstransacties.</span><span class="sxs-lookup"><span data-stu-id="9df3e-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="9df3e-118">Typ een waarde in het veld Gepostdateerde cheques overboeken naar dit leveranciersbetalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="9df3e-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="9df3e-119">Geef de gewenste waarden op in het veld Aflossingsrekening bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="9df3e-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="9df3e-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9df3e-120">Click Save.</span></span>
11. <span data-ttu-id="9df3e-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9df3e-121">Close the page.</span></span>
12. <span data-ttu-id="9df3e-122">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="9df3e-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="9df3e-123">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9df3e-123">Click New.</span></span>
14. <span data-ttu-id="9df3e-124">Typ een waarde in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="9df3e-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="9df3e-125">Selecteer de optie Boeking van aflossing gepostdateerde cheque om aan te geven dat het bedrag van de cheque naar een tijdelijke rekening wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="9df3e-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="9df3e-126">Selecteer Bank in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="9df3e-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="9df3e-127">De tegenrekening van de betalingsmethode zal een bank zijn.</span><span class="sxs-lookup"><span data-stu-id="9df3e-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="9df3e-128">Geef in het veld Betalingsrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="9df3e-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="9df3e-129">Selecteer de bankrekening die wordt gebruikt om het factuurbedrag af te trekken.</span><span class="sxs-lookup"><span data-stu-id="9df3e-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="9df3e-130">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9df3e-130">Click Save.</span></span>
19. <span data-ttu-id="9df3e-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9df3e-131">Close the page.</span></span>

