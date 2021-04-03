---
title: Een nieuwe leveranciersbankrekening maken
description: Deze procedure laat u zien hoe u een bankrekening maakt voor een leverancier.
author: RichardLuan
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 425cce178c96097c8aa0a28345d4a9094b7970d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262184"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="abe9a-103">Een nieuwe leveranciersbankrekening maken</span><span class="sxs-lookup"><span data-stu-id="abe9a-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abe9a-104">Deze procedure laat u zien hoe u een bankrekening maakt voor een leverancier.</span><span class="sxs-lookup"><span data-stu-id="abe9a-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="abe9a-105">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="abe9a-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="abe9a-106">Ga naar **Navigatievenster > Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="abe9a-107">Selecteer de leverancier waarvoor u een bankrekening wilt maken en klik vervolgens op de koppeling van de **id van de leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="abe9a-108">Klik in het **actievenster** op **Leverancier**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="abe9a-109">Klik op **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="abe9a-110">Klik in het **actievenster** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="abe9a-111">Typ een waarde in het veld **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="abe9a-112">Deze id wordt gebruikt om de bankrekening in de leverancierrecord te identificeren.</span><span class="sxs-lookup"><span data-stu-id="abe9a-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="abe9a-113">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="abe9a-114">Typ of selecteer een waarde in het veld **Bankgroepen**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="abe9a-115">Selecteer een optie in het veld **Routenummertype**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="abe9a-116">Dit is het type routenummer dat wordt gebruikt voor internationale betalingen.</span><span class="sxs-lookup"><span data-stu-id="abe9a-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="abe9a-117">Typ een waarde in het veld **Bankrekeningnummer**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="abe9a-118">Typ een waarde in het veld **SWIFT-code**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="abe9a-119">Typ een waarde in het veld **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="abe9a-120">Het IBAN-nummer moet de juiste indeling hebben.</span><span class="sxs-lookup"><span data-stu-id="abe9a-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="abe9a-121">U kunt bijvoorbeeld DE89370400440532013000 gebruiken.</span><span class="sxs-lookup"><span data-stu-id="abe9a-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="abe9a-122">De status van de bankrekening is Actief als de begindatum is bereikt en de vervaldatum niet is overschreden.</span><span class="sxs-lookup"><span data-stu-id="abe9a-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="abe9a-123">De bankrekening is tevens actief als zowel het veld Begindatum als het veld Vervaldatum leeg is gelaten.</span><span class="sxs-lookup"><span data-stu-id="abe9a-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="abe9a-124">Als de datums in de velden Begindatum en Vervaldatum beide in de toekomst liggen, zijn er geen elektronische betalingen beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="abe9a-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="abe9a-125">Andere betalingstypen zijn wel beschikbaar en de bankrekening is actief.</span><span class="sxs-lookup"><span data-stu-id="abe9a-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="abe9a-126">Vouw de sectie **Instellingen** uit.</span><span class="sxs-lookup"><span data-stu-id="abe9a-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="abe9a-127">Typ een waarde in het veld **Tekstcode**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="abe9a-128">Dit veld bevat een code die op het bankafschrift van de ontvanger wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="abe9a-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="abe9a-129">Typ een waarde in het veld **Bericht aan bank**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="abe9a-130">Typ een waarde in het veld **Verwijzing uitwisseling**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="abe9a-131">Dit is het verwijzingsnummer voor een eventuele termijnkoers of vaste wisselkoers</span><span class="sxs-lookup"><span data-stu-id="abe9a-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="abe9a-132">Typ of selecteer een waarde in het veld **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="abe9a-133">Wanneer voorafmeldingen worden afgegeven, bevat deze sectie een overzicht van hun status (in behandeling of goedgekeurd).</span><span class="sxs-lookup"><span data-stu-id="abe9a-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="abe9a-134">Vouw de sectie **Adres** uit.</span><span class="sxs-lookup"><span data-stu-id="abe9a-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="abe9a-135">Vouw de sectie **Voorafmeldingen** uit.</span><span class="sxs-lookup"><span data-stu-id="abe9a-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="abe9a-136">Vouw de sectie **Contactgegevens** uit.</span><span class="sxs-lookup"><span data-stu-id="abe9a-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="abe9a-137">Typ een waarde in het veld **Telefoon**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="abe9a-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="abe9a-138">Close the page.</span></span>
23. <span data-ttu-id="abe9a-139">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-139">Click **Edit**.</span></span>
24. <span data-ttu-id="abe9a-140">Vouw de sectie **Betaling** uit.</span><span class="sxs-lookup"><span data-stu-id="abe9a-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="abe9a-141">Selecteer in het veld **Bankrekening** de rekening die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="abe9a-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="abe9a-142">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="abe9a-142">Click **Save**.</span></span> <span data-ttu-id="abe9a-143">Het adres kan worden overgenomen vanuit de bankgroep, als deze is opgegeven, of u kunt het hier toevoegen.</span><span class="sxs-lookup"><span data-stu-id="abe9a-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]