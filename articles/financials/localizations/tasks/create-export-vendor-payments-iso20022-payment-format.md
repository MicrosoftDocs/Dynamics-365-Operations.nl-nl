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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "340540"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="734ac-103">Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling</span><span class="sxs-lookup"><span data-stu-id="734ac-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="734ac-104">In dit onderwerp ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="734ac-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="734ac-105">Dit is de vijfde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="734ac-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="734ac-106">Gebruik de DEMF-demogegevens om dit voorbeeld te voltooien.</span><span class="sxs-lookup"><span data-stu-id="734ac-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="734ac-107">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="734ac-107">Example</span></span>

1.  <span data-ttu-id="734ac-108">Ga naar **Leveranciers > Betalingen > Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="734ac-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="734ac-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="734ac-109">Click **New**.</span></span>
3.  <span data-ttu-id="734ac-110">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="734ac-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="734ac-111">Klik op **Regels > Betalingsvoorstel > Betalingsvoorstel maken**.</span><span class="sxs-lookup"><span data-stu-id="734ac-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="734ac-112">Vouw de sectie **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="734ac-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="734ac-113">Klik op **Filter**.</span><span class="sxs-lookup"><span data-stu-id="734ac-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="734ac-114">Selecteer in de lijst de rij voor de **tabel Leveranciers** en het **veld Leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="734ac-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="734ac-115">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="734ac-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="734ac-116">U kunt willekeurige criteria toepassen om van leverancierstransacties te selecteren; gebruik in dit voorbeeldgebruik DE-001 als leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="734ac-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="734ac-117">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="734ac-117">Click **OK**.</span></span>
13. <span data-ttu-id="734ac-118">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="734ac-118">Click **OK**.</span></span>
14. <span data-ttu-id="734ac-119">Klik op **Betalingen maken**.</span><span class="sxs-lookup"><span data-stu-id="734ac-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="734ac-120">Een ISO20022-betalingsbestand genereren.</span><span class="sxs-lookup"><span data-stu-id="734ac-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="734ac-121">Klik op **Betalingen genereren.**</span><span class="sxs-lookup"><span data-stu-id="734ac-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="734ac-122">Typ of selecteer een waarde in het veld **Betalingsmethode.**</span><span class="sxs-lookup"><span data-stu-id="734ac-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="734ac-123">Typ een waarde in het veld **Bestandsnaam**.</span><span class="sxs-lookup"><span data-stu-id="734ac-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="734ac-124">In dit voorbeeld is vanwege de EUR-betaling het gegenereerde bestand compatibel is met SEPA.</span><span class="sxs-lookup"><span data-stu-id="734ac-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="734ac-125">ISO20022 kredietoverdracht alsmede andere indelingen voor betalingen van leverancier kunnen ook worden gebruikt voor het genereren van betalingen in andere valuta's.</span><span class="sxs-lookup"><span data-stu-id="734ac-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="734ac-126">Typ of selecteer een waarde in het veld **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="734ac-126">In the **Bank account** field, enter or select a value.</span></span>

