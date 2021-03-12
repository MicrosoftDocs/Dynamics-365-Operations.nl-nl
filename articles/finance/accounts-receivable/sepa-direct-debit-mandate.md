---
title: Mandaag voor automatische afschrijving instellen voor SEPA
description: Een automatische SEPA-overschrijving maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6ee3861e967246e79b072aaa69f2be02db9231b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995488"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="c7966-103">Mandaag voor automatische afschrijving instellen voor SEPA</span><span class="sxs-lookup"><span data-stu-id="c7966-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7966-104">Een automatische SEPA-overschrijving maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend.</span><span class="sxs-lookup"><span data-stu-id="c7966-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="c7966-105">De klant tekent een mandaat dat de crediteur autoriseert om een betaling te innen en dat de bank van de klant opdraagt om de inning te betalen.</span><span class="sxs-lookup"><span data-stu-id="c7966-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="c7966-106">Dit onderwerp is opgezet om het proces weer te geven voor het instellen van SEPA-mandaten voor automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="c7966-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7966-107">Vereisten</span><span class="sxs-lookup"><span data-stu-id="c7966-107">Prerequisites</span></span>
<span data-ttu-id="c7966-108">De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.</span><span class="sxs-lookup"><span data-stu-id="c7966-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="c7966-109">Categorie</span><span class="sxs-lookup"><span data-stu-id="c7966-109">Category</span></span>       | <span data-ttu-id="c7966-110">Vereiste</span><span class="sxs-lookup"><span data-stu-id="c7966-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7966-111">Land/regio</span><span class="sxs-lookup"><span data-stu-id="c7966-111">Country/region</span></span> | <span data-ttu-id="c7966-112">Het primaire adres van de rechtspersoon moet zich in de volgende landen/regio's bevinden: Oostenrijk, België, Duitsland, Spanje, Frankrijk, Italië of Nederland.</span><span class="sxs-lookup"><span data-stu-id="c7966-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="c7966-113">Een nummerreeks instellen voor automatische overschrijvingsmandaten Elk mandaat voor automatische afschrijving moet een uniek nummer hebben.</span><span class="sxs-lookup"><span data-stu-id="c7966-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="c7966-114">Gebruik het formulier **Nummerreeksen** om een nummerreeks voor automatische overschrijvingsmandaten te maken.</span><span class="sxs-lookup"><span data-stu-id="c7966-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="c7966-115">U wilt deze identificatie gebruiken om de nummerreeks op het automatische overschrijvingsdebetmandaatsysteem op de pagina **Parameters van module Klanten** toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="c7966-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="c7966-116">De leveranciersparameters voor mandaten voor automatische afschrijving in stellen Op de pagina **Parameters van module Klanten** stelt u de parameters voor mandaten voor automatische afschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c7966-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="c7966-117">Als u de parameters wilt instellen, wijzigt u de standaardparameters op het tabblad **Automatische afschrijving**.</span><span class="sxs-lookup"><span data-stu-id="c7966-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="c7966-118">Werk op het tabblad **Nummerreeksen** het veld **Mandaat-ID voor automatische afschrijving** bij met de eerder ingestelde nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="c7966-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="c7966-119">Een betalingsmethode voor automatische overschrijvingsmandaten instellen U moet een betalingsmethode voor mandaten voor automatische afschrijving instellen.</span><span class="sxs-lookup"><span data-stu-id="c7966-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="c7966-120">U gebruikt deze betalingsmethode om facturen op te vragen om automatische afschrijvingen voor te genereren.</span><span class="sxs-lookup"><span data-stu-id="c7966-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="c7966-121">Gebruik de pagina **Betalingsmethoden** om de betalingsmethode in te stellen.</span><span class="sxs-lookup"><span data-stu-id="c7966-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="c7966-122">Als u een betalingsmethode voor mandaten voor automatische afschrijving wilt instellen, moet u deze extra stappen voor een betalingsmethode uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="c7966-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="c7966-123">Selecteer **Elektronische betaling** in het veld **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="c7966-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="c7966-124">Optioneel: Als u verwacht dat al uw klanten meerdere mandaten hebben, selecteert u in het veld **Periode** de waarde **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="c7966-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="c7966-125">Hierdoor wordt een afzonderlijke betaling voor elke factuur gemaakt, en elke betaling gebruikt het mandaat dat voor de factuur is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c7966-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="c7966-126">Selecteer de optie **Mandaat vereisen** om betalingen te maken door mandaten voor automatische afschrijving te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c7966-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="c7966-127">De optie **Mandaat vereisen** is alleen beschikbaar als u **Elektronische betaling** in het veld **Betalingstype** selecteert.</span><span class="sxs-lookup"><span data-stu-id="c7966-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="c7966-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c7966-128">Additional resources</span></span>

[<span data-ttu-id="c7966-129">Overzicht SEPA-incasso</span><span class="sxs-lookup"><span data-stu-id="c7966-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="c7966-130">Een mandaat voor automatische afschrijving maken voor een klant</span><span class="sxs-lookup"><span data-stu-id="c7966-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

