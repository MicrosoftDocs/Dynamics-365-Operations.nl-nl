---
title: Betalingsmethode voor ISO20022 automatische afschrijving instellen
description: In deze procedure ziet u hoe u de betalingsmethode van de klanten instelt voor ISO20022 automatische incasso of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c6a692553867d7e8679099210dc44b9d9e4d0f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838677"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="237a2-103">Betalingsmethode voor ISO20022 automatische afschrijving instellen</span><span class="sxs-lookup"><span data-stu-id="237a2-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="237a2-104">In deze procedure ziet u hoe u de betalingsmethode van de klanten instelt voor ISO20022 automatische incasso of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.</span><span class="sxs-lookup"><span data-stu-id="237a2-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="237a2-105">Voordat u deze taak uitvoert, moet u indelingconfiguraties voor export en betaalrekeningen hebben ingesteld.</span><span class="sxs-lookup"><span data-stu-id="237a2-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="237a2-106">Deze procedure is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="237a2-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="237a2-107">Dit is de derde van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="237a2-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="237a2-108">Ga naar Klanten > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="237a2-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="237a2-109">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="237a2-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="237a2-110">Filter bijvoorbeeld op het veld Betalingsmethode met een waarde van 'ELECTRONIC'.</span><span class="sxs-lookup"><span data-stu-id="237a2-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="237a2-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="237a2-111">Click Edit.</span></span>
4. <span data-ttu-id="237a2-112">Geef de waarden 'DEMF OPER' op in het veld Betalingsrekening.</span><span class="sxs-lookup"><span data-stu-id="237a2-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="237a2-113">Vouw de sectie Bestandsindelingen uit.</span><span class="sxs-lookup"><span data-stu-id="237a2-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="237a2-114">Selecteer Ja in het veld Algemene elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="237a2-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="237a2-115">Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="237a2-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="237a2-116">Selecteer in de lijst de waarde ISO20022 Automatische incasso (DE).</span><span class="sxs-lookup"><span data-stu-id="237a2-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="237a2-117">Als de lijst leeg is, betekent dit dat er geen configuratie voor de exportindeling voor klantenbetalingen is geïmporteerd en geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="237a2-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="237a2-118">Selecteer Ja in het veld Mandaat vereisen.</span><span class="sxs-lookup"><span data-stu-id="237a2-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="237a2-119">Selecteer de parameter Mandaat vereisen voor klantbetalingsindelingen, die vereist dat mandaatinformatie deel uitmaakt van het betalingbericht, zoals SEPA automatische incasso.</span><span class="sxs-lookup"><span data-stu-id="237a2-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="237a2-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="237a2-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]