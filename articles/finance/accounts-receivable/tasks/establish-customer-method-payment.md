---
title: Betalingsmethode van klant vaststellen
description: In dit onderwerp wordt uitgelegd hoe u betalingsmethode kunt maken voor klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188804"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="5a780-103">Betalingsmethode van klant vaststellen</span><span class="sxs-lookup"><span data-stu-id="5a780-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a780-104">In dit onderwerp wordt uitgelegd hoe u betalingsmethode kunt maken voor klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="5a780-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="5a780-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5a780-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="5a780-106">Ga in het navigatievenster naar **Modules > Klanten > Instelling van betalingen > Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="5a780-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="5a780-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5a780-107">Select **New**.</span></span>
3. <span data-ttu-id="5a780-108">Voer in het veld **Betalingsmethode** een id voor de betalingsmethode in.</span><span class="sxs-lookup"><span data-stu-id="5a780-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="5a780-109">De id voor de betalingsmethode wordt weergegeven op facturen en betalingen. Maak deze dus beschrijvend genoeg om te begrijpen welk type betaling wordt geregistreerd en voor welke bankrekening.</span><span class="sxs-lookup"><span data-stu-id="5a780-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="5a780-110">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="5a780-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5a780-111">Selecteer welke betalingsstatus is vereist voor het boeken van betalingen.</span><span class="sxs-lookup"><span data-stu-id="5a780-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="5a780-112">Bij het maken van een klantbetaling kan deze alleen worden geboekt als de betalingsstatus overeenstemt met de betalingsstatus die u hier definieert.</span><span class="sxs-lookup"><span data-stu-id="5a780-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="5a780-113">Selecteer hoe betalingen van klanten voor facturen moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5a780-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="5a780-114">Deze optie wordt alleen gebruikt bij het uitvoeren van een betalingsvoorstel.</span><span class="sxs-lookup"><span data-stu-id="5a780-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="5a780-115">Een betalingsvoorstel kan worden gebruikt voor klantbetalingen bij het doen van automatische afschrijvingen en het afschrijven van de fondsen van de bankrekeningen van klanten.</span><span class="sxs-lookup"><span data-stu-id="5a780-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="5a780-116">Selecteer het type betaling.</span><span class="sxs-lookup"><span data-stu-id="5a780-116">Select the type of payment.</span></span> <span data-ttu-id="5a780-117">Het betalingstype helpt om te bepalen of al dan niet enige validatie zal plaatsvinden voor de betaling.</span><span class="sxs-lookup"><span data-stu-id="5a780-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="5a780-118">Selecteer naar welke betalingen van het rekeningtype zal worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="5a780-118">Select what account type payments will post to.</span></span> <span data-ttu-id="5a780-119">Normaal gesproken moet Bank zijn geselecteerd voor deze optie.</span><span class="sxs-lookup"><span data-stu-id="5a780-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="5a780-120">Selecteer de bankrekening waarop deze betaling worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="5a780-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="5a780-121">Voer het banktransactietype in die het type betaling aangeeft dat door uw bank wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5a780-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="5a780-122">Het banktransactietype wordt gebruikt tijdens het bankafstemmingsproces en kan afstemming eenvoudiger maken.</span><span class="sxs-lookup"><span data-stu-id="5a780-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="5a780-123">Selecteer of deze betaling tijdelijk naar een overbruggingsrekening zal worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="5a780-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="5a780-124">Als u wilt weten hoe lang het duurt voordat een betaling wordt vrijgegeven door de bank, gebruikt u de functionaliteit Overbrugging.</span><span class="sxs-lookup"><span data-stu-id="5a780-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="5a780-125">De betaling wordt tijdelijk naar een grootboekrekening geboekt totdat deze wordt vrijgegeven door de bank. Op dat moment wordt de betaling naar de bankrekening verplaatst die u hier definieert.</span><span class="sxs-lookup"><span data-stu-id="5a780-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="5a780-126">Voer de hoofdrekening in die wordt gebruikt voor de overbruggingsboeking.</span><span class="sxs-lookup"><span data-stu-id="5a780-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="5a780-127">Dit is de hoofdrekening waarnaar de betaling tijdelijk wordt geboekt bij gebruik van overbrugging.</span><span class="sxs-lookup"><span data-stu-id="5a780-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="5a780-128">Gebruik het tabblad **Bestandsindeling** om instelling voor elektronische betalingen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="5a780-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="5a780-129">Gebruik het tabblad **Betalingsbeheer** om velden die verplicht zijn te definiëren.</span><span class="sxs-lookup"><span data-stu-id="5a780-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="5a780-130">Als u bijvoorbeeld vereist dat alle betalingen met deze betalingsmethode worden gestort, kunt u die optie kiezen op dit tabblad.</span><span class="sxs-lookup"><span data-stu-id="5a780-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="5a780-131">Gebruik het tabblad **Betalingskenmerken** om te bepalen welke betalingskenmerken u voor deze betalingsmethode wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5a780-131">Use the **Payment atrributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="5a780-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5a780-132">Select **Save**.</span></span>

