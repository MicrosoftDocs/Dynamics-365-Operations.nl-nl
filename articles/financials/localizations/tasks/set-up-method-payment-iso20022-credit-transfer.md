--- 
title: Betalingsmethode voor ISO20022-kredietoverdracht instellen
description: IN deze procedure ziet u hoe u de betalingsmethode van de leverancier instelt voor ISO20022-kredietoverdracht of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 2c8e858f15047652b9d6561bc1a4ff8e09ea02d5
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="dd67c-103">Betalingsmethode voor ISO20022-kredietoverdracht instellen</span><span class="sxs-lookup"><span data-stu-id="dd67c-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd67c-104">IN deze procedure ziet u hoe u de betalingsmethode van de leverancier instelt voor ISO20022-kredietoverdracht of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.</span><span class="sxs-lookup"><span data-stu-id="dd67c-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="dd67c-105">Voordat u deze taak uitvoert, moet u indelingconfiguraties voor export en betaalrekeningen hebben ingesteld.</span><span class="sxs-lookup"><span data-stu-id="dd67c-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="dd67c-106">Deze taak is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="dd67c-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="dd67c-107">Dit is de derde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="dd67c-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="dd67c-108">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="dd67c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="dd67c-109">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="dd67c-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="dd67c-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="dd67c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dd67c-111">Filter bijvoorbeeld op het veld Betalingsmethode met een waarde van 'SEPA CT'.</span><span class="sxs-lookup"><span data-stu-id="dd67c-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="dd67c-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="dd67c-112">Click Edit.</span></span>
4. <span data-ttu-id="dd67c-113">Selecteer Totaal in het veld Periode.</span><span class="sxs-lookup"><span data-stu-id="dd67c-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="dd67c-114">Selecteer Elektronische betaling in het veld Betalingstype.</span><span class="sxs-lookup"><span data-stu-id="dd67c-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="dd67c-115">Vouw de sectie Bestandsindelingen uit.</span><span class="sxs-lookup"><span data-stu-id="dd67c-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="dd67c-116">Selecteer Ja in het veld Algemene elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="dd67c-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="dd67c-117">Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="dd67c-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="dd67c-118">Selecteer in de lijst de waarde ISO20022 Kredietoverdracht (DE).</span><span class="sxs-lookup"><span data-stu-id="dd67c-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="dd67c-119">Als de lijst leeg is, betekent dit dat er geen configuratie voor de exportindeling voor leveranciersbetalingen is geïmporteerd en geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="dd67c-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="dd67c-120">Selecteer Bank in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="dd67c-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="dd67c-121">Geef de waarden 'DEMF OPER' op in het veld Betalingsrekening.</span><span class="sxs-lookup"><span data-stu-id="dd67c-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="dd67c-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="dd67c-122">Click Save.</span></span>


