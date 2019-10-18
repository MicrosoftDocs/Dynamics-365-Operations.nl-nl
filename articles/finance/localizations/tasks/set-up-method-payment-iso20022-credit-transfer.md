---
title: Betalingsmethode voor ISO20022-kredietoverdracht instellen
description: IN deze procedure ziet u hoe u de betalingsmethode van de leverancier instelt voor ISO20022-kredietoverdracht of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174819"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="ea473-103">Betalingsmethode voor ISO20022-kredietoverdracht instellen</span><span class="sxs-lookup"><span data-stu-id="ea473-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea473-104">IN deze procedure ziet u hoe u de betalingsmethode van de leverancier instelt voor ISO20022-kredietoverdracht of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.</span><span class="sxs-lookup"><span data-stu-id="ea473-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="ea473-105">Voordat u deze taak uitvoert, moet u indelingconfiguraties voor export en betaalrekeningen hebben ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ea473-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="ea473-106">Deze taak is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="ea473-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="ea473-107">Dit is de derde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="ea473-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ea473-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="ea473-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="ea473-109">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="ea473-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="ea473-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ea473-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea473-111">Filter bijvoorbeeld op het veld Betalingsmethode met een waarde van 'SEPA CT'.</span><span class="sxs-lookup"><span data-stu-id="ea473-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="ea473-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="ea473-112">Click Edit.</span></span>
4. <span data-ttu-id="ea473-113">Selecteer Totaal in het veld Periode.</span><span class="sxs-lookup"><span data-stu-id="ea473-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="ea473-114">Selecteer Elektronische betaling in het veld Betalingstype.</span><span class="sxs-lookup"><span data-stu-id="ea473-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="ea473-115">Vouw de sectie Bestandsindelingen uit.</span><span class="sxs-lookup"><span data-stu-id="ea473-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="ea473-116">Selecteer Ja in het veld Algemene elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="ea473-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="ea473-117">Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="ea473-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="ea473-118">Selecteer in de lijst de waarde ISO20022 Kredietoverdracht (DE).</span><span class="sxs-lookup"><span data-stu-id="ea473-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="ea473-119">Als de lijst leeg is, betekent dit dat er geen configuratie voor de exportindeling voor leveranciersbetalingen is geïmporteerd en geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="ea473-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="ea473-120">Selecteer Bank in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="ea473-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="ea473-121">Geef de waarden 'DEMF OPER' op in het veld Betalingsrekening.</span><span class="sxs-lookup"><span data-stu-id="ea473-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="ea473-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ea473-122">Click Save.</span></span>

