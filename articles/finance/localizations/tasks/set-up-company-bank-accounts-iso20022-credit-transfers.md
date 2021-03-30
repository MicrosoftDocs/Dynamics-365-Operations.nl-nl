---
title: Bankrekeningen voor ISO20022-kredietoverdrachten voor een bank instellen
description: In deze procedure ziet u hoe u de bedrijfsspecifieke bankrekeninggegevens instelt die vereist zijn voor het genereren van SEPA-betalingsbestanden.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ad1ebbea9bca41f43f3f4098114116e32f8517b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205465"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="47223-103">Bankrekeningen voor ISO20022-kredietoverdrachten voor een bank instellen</span><span class="sxs-lookup"><span data-stu-id="47223-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47223-104">In deze procedure ziet u hoe u de bedrijfsspecifieke bankrekeninggegevens instelt die vereist zijn voor het genereren van SEPA-betalingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="47223-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="47223-105">U configureert informatie die nodig is om de indeling voor de ISO20022-kredietoverdracht te genereren. Maar afhankelijk van de indeling kan ook andere informatie nodig zijn, zoals de bedrijfs-ID of de sorteercode.</span><span class="sxs-lookup"><span data-stu-id="47223-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="47223-106">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.</span><span class="sxs-lookup"><span data-stu-id="47223-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="47223-107">Dit is de tweede van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="47223-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="47223-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="47223-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="47223-109">IBAN en SWIFT-code instellen</span><span class="sxs-lookup"><span data-stu-id="47223-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="47223-110">Ga naar Contanten en bankbeheer > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="47223-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="47223-111">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'DEMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="47223-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="47223-112">Klik op DEMF OPER om bankrekeninggegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="47223-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="47223-113">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="47223-113">Click Edit.</span></span>
5. <span data-ttu-id="47223-114">Vouw de sectie Aanvullende identificatie uit.</span><span class="sxs-lookup"><span data-stu-id="47223-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="47223-115">Typ 'DE89370400440532013000' in het veld IBAN.</span><span class="sxs-lookup"><span data-stu-id="47223-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="47223-116">Typ 'DEUTDEFF' in het veld SWIFT-code.</span><span class="sxs-lookup"><span data-stu-id="47223-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="47223-117">Merk op dat SWIFT/BIC niet voor veel betalingsindelingen is vereist. Het wordt echter wel aanbevolen om het te registreren voor een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="47223-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="47223-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="47223-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="47223-119">Bankrekening instellen voor de rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="47223-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="47223-120">Ga naar Organisatiebeheer > Organisaties > Rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="47223-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="47223-121">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="47223-121">Click Edit.</span></span>
3. <span data-ttu-id="47223-122">Vouw de sectie Bankrekeninggegevens uit.</span><span class="sxs-lookup"><span data-stu-id="47223-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="47223-123">Typ of selecteer een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="47223-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="47223-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="47223-124">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]