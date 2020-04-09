---
title: " Betalingsconfiguraties voor detailhandeloverzichten"
description: Deze procedure demonstreert configuraties voor betalingsmethoden voor Commerce-winkels die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 390ccdfde3f9bb93770d456af7532a42e81955a1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140802"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="37bd3-103"> Betalingsconfiguraties voor detailhandeloverzichten</span><span class="sxs-lookup"><span data-stu-id="37bd3-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37bd3-104">Deze procedure demonstreert configuraties voor betalingsmethoden voor Commerce-winkels die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="37bd3-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="37bd3-105">Deze registratie gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="37bd3-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="37bd3-106">Ga naar Retail en Commerce > Kanalen > Winkels > Alle winkels.</span><span class="sxs-lookup"><span data-stu-id="37bd3-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="37bd3-107">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="37bd3-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37bd3-108">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="37bd3-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="37bd3-109">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="37bd3-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="37bd3-110">Klik op Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="37bd3-110">Click Payment methods.</span></span>
6. <span data-ttu-id="37bd3-111">Vouw de sectie Boeking uit of samen.</span><span class="sxs-lookup"><span data-stu-id="37bd3-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="37bd3-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="37bd3-112">Click Edit.</span></span>
    * <span data-ttu-id="37bd3-113">Selecteer of de ontvangen hoeveelheden voor deze betalingsmethode moeten worden geboekt naar een grootboekrekening of een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="37bd3-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="37bd3-114">Selecteer de rekening waarnaar ontvangen bedragen voor deze betalingsmethode moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="37bd3-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="37bd3-115">Selecteer een rekening om mogelijke verschillen naar te boeken tussen het totale ontvangen transactiebedrag en het getelde bedrag voor deze betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="37bd3-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="37bd3-116">In dit veld kunt u een bedrag invoeren om te bepalen wanneer het verschilbedrag moet worden geboekt naar een andere verschilrekening.</span><span class="sxs-lookup"><span data-stu-id="37bd3-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="37bd3-117">U kunt dit gebruiken om grote verschillen bij te houden.</span><span class="sxs-lookup"><span data-stu-id="37bd3-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="37bd3-118">Selecteer een rekening om mogelijke verschillen naar te boeken tussen het totale ontvangen transactiebedrag en het getelde bedrag, wanneer het de waarde overschrijdt die is gedefinieerd in het veld 'Maximumbedrag verschil'.</span><span class="sxs-lookup"><span data-stu-id="37bd3-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="37bd3-119">Selecteer 'Ja' om bankstortingsbedragen naar een aparte rekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="37bd3-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="37bd3-120">In dit veld kunt u selecteren of bankstortingsbedragen moeten worden geboekt naar een grootboekrekening of een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="37bd3-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="37bd3-121">Selecteer de rekening om bankstortingsbedragen naar te boeken.</span><span class="sxs-lookup"><span data-stu-id="37bd3-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="37bd3-122">Selecteer het type banktransactie dat moet worden gebruikt om bankstortingsbedragen te boeken naar de bankrekening.</span><span class="sxs-lookup"><span data-stu-id="37bd3-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="37bd3-123">Selecteer 'Ja' om kluisstortingsbedragen naar een aparte rekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="37bd3-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="37bd3-124">Selecteer of kluisstortingsbedragen moeten worden geboekt naar de grootboekrekening of de bankrekening.</span><span class="sxs-lookup"><span data-stu-id="37bd3-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="37bd3-125">Selecteer de rekening om kluisstortingsbedragen naar te boeken.</span><span class="sxs-lookup"><span data-stu-id="37bd3-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="37bd3-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="37bd3-126">Click Save.</span></span>

