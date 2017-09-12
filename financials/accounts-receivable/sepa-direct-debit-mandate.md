---
title: SEPA-mandaat instellen voor automatische afschrijving
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="f4928-102">SEPA-mandaat instellen voor automatische afschrijving</span><span class="sxs-lookup"><span data-stu-id="f4928-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="f4928-103">Een automatische SEPA-overschrijving maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend.</span><span class="sxs-lookup"><span data-stu-id="f4928-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="f4928-104">De klant tekent een mandaat dat de crediteur autoriseert om een betaling te innen en dat de bank van de klant opdraagt om de inning te betalen.</span><span class="sxs-lookup"><span data-stu-id="f4928-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="f4928-105">Dit onderwerp is opgezet om het proces weer te geven voor het instellen van SEPA-mandaten voor automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="f4928-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4928-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="f4928-106">Prerequisites</span></span>
<span data-ttu-id="f4928-107">De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.</span><span class="sxs-lookup"><span data-stu-id="f4928-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="f4928-108">Categorie</span><span class="sxs-lookup"><span data-stu-id="f4928-108">Category</span></span>       | <span data-ttu-id="f4928-109">Vereiste</span><span class="sxs-lookup"><span data-stu-id="f4928-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4928-110">Land/regio</span><span class="sxs-lookup"><span data-stu-id="f4928-110">Country/region</span></span> | <span data-ttu-id="f4928-111">Het primaire adres van de rechtspersoon moet zich in de volgende landen/regio's bevinden: Oostenrijk, België, Duitsland, Spanje, Frankrijk, Italië of Nederland.</span><span class="sxs-lookup"><span data-stu-id="f4928-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="f4928-112">Een nummerreeks instellen voor automatische overschrijvingsmandaten
Elk mandaat voor automatische afschrijving moet een uniek nummer hebben.</span><span class="sxs-lookup"><span data-stu-id="f4928-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="f4928-113">Gebruik het formulier **Nummerreeksen** om een nummerreeks voor automatische overschrijvingsmandaten te maken.</span><span class="sxs-lookup"><span data-stu-id="f4928-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="f4928-114">U wilt deze identificatie gebruiken om de nummerreeks op het automatische overschrijvingsdebetmandaatsysteem op de pagina **Parameters van module Klanten** toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="f4928-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="f4928-115">De leveranciersparameters voor mandaten voor automatische afschrijving in stellen
Op de pagina **Parameters van module Klanten** stelt u de parameters voor mandaten voor automatische afschrijving in.</span><span class="sxs-lookup"><span data-stu-id="f4928-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="f4928-116">Als u de parameters wilt instellen, wijzigt u de standaardparameters op het tabblad **Automatische afschrijving**.</span><span class="sxs-lookup"><span data-stu-id="f4928-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="f4928-117">Werk op het tabblad **Nummerreeksen** het veld **Mandaat-ID voor automatische afschrijving** bij met de eerder ingestelde nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="f4928-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="f4928-118">Een betalingsmethode voor automatische overschrijvingsmandaten instellen
U moet een betalingsmethode voor mandaten voor automatische afschrijving instellen.</span><span class="sxs-lookup"><span data-stu-id="f4928-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="f4928-119">U gebruikt deze betalingsmethode om facturen op te vragen om automatische afschrijvingen voor te genereren.</span><span class="sxs-lookup"><span data-stu-id="f4928-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="f4928-120">Gebruik de pagina **Betalingsmethoden** om de betalingsmethode in te stellen.</span><span class="sxs-lookup"><span data-stu-id="f4928-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="f4928-121">Als u een betalingsmethode voor mandaten voor automatische afschrijving wilt instellen, moet u deze extra stappen voor een betalingsmethode uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="f4928-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="f4928-122">Selecteer **Elektronische betaling** in het veld **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="f4928-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="f4928-123">Optioneel: Als u verwacht dat al uw klanten meerdere mandaten hebben, selecteert u in het veld **Periode** de waarde **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="f4928-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="f4928-124">Hierdoor wordt een afzonderlijke betaling voor elke factuur gemaakt, en elke betaling gebruikt het mandaat dat voor de factuur is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="f4928-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="f4928-125">Selecteer de optie **Mandaat vereisen** om betalingen te maken door mandaten voor automatische afschrijving te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f4928-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="f4928-126">De optie **Mandaat vereisen** is alleen beschikbaar als u **Elektronische betaling** in het veld **Betalingstype** selecteert.</span><span class="sxs-lookup"><span data-stu-id="f4928-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="f4928-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f4928-127">See Also</span></span>

[<span data-ttu-id="f4928-128">Overzicht automatische overschrijvingen</span><span class="sxs-lookup"><span data-stu-id="f4928-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="f4928-129">Een mandaat voor automatische afschrijving maken voor een klant</span><span class="sxs-lookup"><span data-stu-id="f4928-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


