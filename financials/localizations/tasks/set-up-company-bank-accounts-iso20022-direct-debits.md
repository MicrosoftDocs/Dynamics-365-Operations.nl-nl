--- 
title: Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen
description: Deze taak voert u door het instellen van de bedrijfsspeifieke bankrekeninggegevens die zijn vereist voor het genereren van klantenbetalingsbestanden.
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 836433a1a280efde5accba3391519f3c0ce08353
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="cbe91-103">Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen</span><span class="sxs-lookup"><span data-stu-id="cbe91-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbe91-104">Deze taak voert u door het instellen van de bedrijfsspeifieke bankrekeninggegevens die zijn vereist voor het genereren van klantenbetalingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="cbe91-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="cbe91-105">Deze procedure gebruikt als voorbeeld de indeling voor automatische incasso van ISO20022.</span><span class="sxs-lookup"><span data-stu-id="cbe91-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="cbe91-106">Andere indelingen kunnen extra configuratie-informatie vereisen, zoals de bedrijfs-ID of de sorteercode.</span><span class="sxs-lookup"><span data-stu-id="cbe91-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="cbe91-107">Deze taak is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="cbe91-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="cbe91-108">Dit is de tweede van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="cbe91-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="cbe91-109">De IBAN en SWIFT-code instellen</span><span class="sxs-lookup"><span data-stu-id="cbe91-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="cbe91-110">Ga naar Contanten en bankbeheer > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="cbe91-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="cbe91-111">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'DEMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="cbe91-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="cbe91-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cbe91-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe91-113">Bijvoorbeeld: klik op 'DEMF OPER' om de bankrekeninggegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="cbe91-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="cbe91-114">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="cbe91-114">Click Edit.</span></span>
5. <span data-ttu-id="cbe91-115">Vouw de sectie Aanvullende identificatie uit of samen.</span><span class="sxs-lookup"><span data-stu-id="cbe91-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="cbe91-116">Typ een waarde in het veld IBAN.</span><span class="sxs-lookup"><span data-stu-id="cbe91-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="cbe91-117">Voer bijvoorbeeld 'DE89370400440532013000' in.</span><span class="sxs-lookup"><span data-stu-id="cbe91-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="cbe91-118">Typ een waarde in het veld SWIFT-code.</span><span class="sxs-lookup"><span data-stu-id="cbe91-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="cbe91-119">Voer bijvoorbeeld 'DEUTDEFF' in.</span><span class="sxs-lookup"><span data-stu-id="cbe91-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="cbe91-120">Merk op dat SWIFT/BIC niet voor veel betalingsindelingen is vereist. Het wordt echter wel aanbevolen om het te registreren voor een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="cbe91-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="cbe91-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cbe91-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="cbe91-122">Een bankrekening instellen voor de rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="cbe91-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="cbe91-123">Ga naar Organisatiebeheer > Organisaties > Rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="cbe91-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="cbe91-124">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="cbe91-124">Click Edit.</span></span>
3. <span data-ttu-id="cbe91-125">Vouw de sectie Bankrekeninggegevens uit of samen.</span><span class="sxs-lookup"><span data-stu-id="cbe91-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="cbe91-126">Klik in het veld Bankrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cbe91-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cbe91-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cbe91-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe91-128">Selecteer bijvoorbeeld de bankrekening "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="cbe91-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="cbe91-129">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cbe91-129">Click Save.</span></span>


