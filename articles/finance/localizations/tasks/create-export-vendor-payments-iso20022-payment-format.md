---
title: Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling
description: In deze procedure ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143119"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="de635-103">Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling</span><span class="sxs-lookup"><span data-stu-id="de635-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de635-104">In dit onderwerp ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="de635-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="de635-105">Dit is de vijfde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="de635-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="de635-106">Gebruik de DEMF-demogegevens om dit voorbeeld te voltooien.</span><span class="sxs-lookup"><span data-stu-id="de635-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="de635-107">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="de635-107">Example</span></span>

1.    <span data-ttu-id="de635-108">Ga naar **Leveranciers > Betalingen > Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="de635-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="de635-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="de635-109">Click **New**.</span></span>
3.    <span data-ttu-id="de635-110">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="de635-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="de635-111">Klik op **Regels > Betalingsvoorstel > Betalingsvoorstel maken**.</span><span class="sxs-lookup"><span data-stu-id="de635-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="de635-112">Vouw de sectie **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="de635-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="de635-113">Klik op **Filter**.</span><span class="sxs-lookup"><span data-stu-id="de635-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="de635-114">Selecteer in de lijst de rij voor de **tabel Leveranciers** en het **veld Leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="de635-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="de635-115">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="de635-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="de635-116">U kunt willekeurige criteria toepassen om van leverancierstransacties te selecteren; gebruik in dit voorbeeldgebruik DE-001 als leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="de635-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="de635-117">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="de635-117">Click **OK**.</span></span>
13.    <span data-ttu-id="de635-118">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="de635-118">Click **OK**.</span></span>
14.    <span data-ttu-id="de635-119">Klik op **Betalingen maken**.</span><span class="sxs-lookup"><span data-stu-id="de635-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="de635-120">Een ISO20022-betalingsbestand genereren.</span><span class="sxs-lookup"><span data-stu-id="de635-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="de635-121">Klik op **Betalingen genereren.**</span><span class="sxs-lookup"><span data-stu-id="de635-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="de635-122">Typ of selecteer een waarde in het veld **Betalingsmethode.**</span><span class="sxs-lookup"><span data-stu-id="de635-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="de635-123">Typ een waarde in het veld **Bestandsnaam**.</span><span class="sxs-lookup"><span data-stu-id="de635-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="de635-124">In dit voorbeeld is vanwege de EUR-betaling het gegenereerde bestand compatibel is met SEPA.</span><span class="sxs-lookup"><span data-stu-id="de635-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="de635-125">ISO20022 kredietoverdracht alsmede andere indelingen voor betalingen van leverancier kunnen ook worden gebruikt voor het genereren van betalingen in andere valuta's.</span><span class="sxs-lookup"><span data-stu-id="de635-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="de635-126">Typ of selecteer een waarde in het veld **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="de635-126">In the **Bank account** field, enter or select a value.</span></span>

