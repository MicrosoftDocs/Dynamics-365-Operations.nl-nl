---
title: Leveranciers en bankrekeningen voor leveranciers voor ISO20022-kredietoverdrachten instellen
description: Deze procedure laat zien hoe u de leverancier- en leverancierspecifieke bankrekeninggegevens kunt instellen voor het genereren van bestanden voor ISO20022-kredietoverdracht of andere vormen van leveranciersbetalingen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174817"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="b41c7-103">Leveranciers en bankrekeningen voor leveranciers voor ISO20022-kredietoverdrachten instellen</span><span class="sxs-lookup"><span data-stu-id="b41c7-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b41c7-104">Deze procedure laat zien hoe u de leverancier- en leverancierspecifieke bankrekeninggegevens kunt instellen voor het genereren van bestanden voor ISO20022-kredietoverdracht of andere vormen van leveranciersbetalingen.</span><span class="sxs-lookup"><span data-stu-id="b41c7-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="b41c7-105">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.</span><span class="sxs-lookup"><span data-stu-id="b41c7-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="b41c7-106">Dit is de vierde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="b41c7-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="b41c7-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b41c7-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="b41c7-108">Bankgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="b41c7-108">Set up bank details</span></span>
1. <span data-ttu-id="b41c7-109">Ga naar Leveranciers > Leveranciers > Alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="b41c7-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="b41c7-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="b41c7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b41c7-111">Filter bijvoorbeeld op het veld Leveranciersrekening met een waarde van 'DE-001'.</span><span class="sxs-lookup"><span data-stu-id="b41c7-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="b41c7-112">Klik op DE-001 om de leveranciersgegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="b41c7-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="b41c7-113">Klik in het actievenster op Leverancier.</span><span class="sxs-lookup"><span data-stu-id="b41c7-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="b41c7-114">Klik op Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="b41c7-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="b41c7-115">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b41c7-115">Click Edit.</span></span>
    * <span data-ttu-id="b41c7-116">Als er geen bankrekening beschikbaar is, moet u een nieuwe maken.</span><span class="sxs-lookup"><span data-stu-id="b41c7-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="b41c7-117">Typ 'COBADEFFXXX' in het veld SWIFT-code.</span><span class="sxs-lookup"><span data-stu-id="b41c7-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="b41c7-118">Typ 'DE36200400000628808808' in het veld IBAN.</span><span class="sxs-lookup"><span data-stu-id="b41c7-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="b41c7-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b41c7-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="b41c7-120">Een betalingswijze voor de leverancier instellen</span><span class="sxs-lookup"><span data-stu-id="b41c7-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="b41c7-121">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b41c7-121">Click Edit.</span></span>
2. <span data-ttu-id="b41c7-122">Vouw de sectie Betaling uit of samen.</span><span class="sxs-lookup"><span data-stu-id="b41c7-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="b41c7-123">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b41c7-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b41c7-124">Klik in de lijst op de koppeling in de rij SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="b41c7-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="b41c7-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b41c7-125">Click Save.</span></span>

