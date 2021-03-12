---
title: Gepostdateerde cheques
description: Dit artikel biedt informatie over ondersteuning voor gepostdateerde cheques in Microsoft Dynamics 365 Finance. Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen. Daarom kan de cheque pas op de opgegeven datum worden geïnd.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f30b8d1061eb2fe709df38628acd798448c8929e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989222"
---
# <a name="postdated-checks"></a><span data-ttu-id="8a665-105">Gepostdateerde cheques</span><span class="sxs-lookup"><span data-stu-id="8a665-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a665-106">Dit artikel biedt informatie over ondersteuning voor gepostdateerde cheques.</span><span class="sxs-lookup"><span data-stu-id="8a665-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="8a665-107">Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="8a665-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="8a665-108">Daarom kan de cheque pas op de opgegeven datum worden geïnd.</span><span class="sxs-lookup"><span data-stu-id="8a665-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="8a665-109">Dynamics 365 Finance ondersteunt de volledige beheercyclus voor gepostdateerde cheques in Klanten en in Leveranciers, zoals u in de volgende tabel ziet.</span><span class="sxs-lookup"><span data-stu-id="8a665-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8a665-110">Scenario</span><span class="sxs-lookup"><span data-stu-id="8a665-110">Scenario</span></span></th>
<th><span data-ttu-id="8a665-111">Details</span><span class="sxs-lookup"><span data-stu-id="8a665-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a665-112">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="8a665-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="8a665-113">U moet een nieuwe betalingsmethode instellen en de betalingsroutine voor speciale rekeningen opgeven voor uitgegeven cheques, ontvangen cheques en bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="8a665-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a665-114">Een gepostdateerde cheque voor een leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="8a665-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="8a665-115">Registreer de details van een gepostdateerde cheque die u aan een leverancier uitschrijft.</span><span class="sxs-lookup"><span data-stu-id="8a665-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="8a665-116">Wanneer de betaling wordt geboekt, wordt de leveranciersaansprakelijkheid erkend, maar wordt de bankrekening nog niet gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="8a665-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="8a665-117">In plaats daarvan wordt hiervoor een speciale rekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8a665-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a665-118">Een gepostdateerde cheque voor een klant registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="8a665-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="8a665-119">Registreer de gegevens van een gepostdateerde cheque die u van een klant ontvangt.</span><span class="sxs-lookup"><span data-stu-id="8a665-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="8a665-120">Wanneer de betaling wordt geboekt, wordt het klanttegoed wel gecrediteerd, maar wordt de bankrekening nog niet gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="8a665-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="8a665-121">In plaats daarvan wordt hiervoor een speciale rekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8a665-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a665-122">Een vervangende gepostdateerde cheque voor een klant of leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="8a665-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="8a665-123">Als uw originele cheque voor een leverancier of klant verloren of beschadigd is geraakt, kunt u een vervangende gepostdateerde cheque uitgeven.</span><span class="sxs-lookup"><span data-stu-id="8a665-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="8a665-124">Wanneer u de gegevens van de cheque registreert, geeft u een referentie naar de originele cheque op en geeft u aan dat de nieuwe cheque de originele cheque vervangt.</span><span class="sxs-lookup"><span data-stu-id="8a665-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="8a665-125">U kunt de vervangende cheque ook boeken.</span><span class="sxs-lookup"><span data-stu-id="8a665-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a665-126">Een gepostdateerde cheque van een klant overboeken naar een leverancier</span><span class="sxs-lookup"><span data-stu-id="8a665-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="8a665-127">Wanneer u een gepostdateerde cheque van een klant ontvangt, kunt u die cheque als betaling naar een leverancier overboeken.</span><span class="sxs-lookup"><span data-stu-id="8a665-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a665-128">Een gepostdateerde cheque voor een klant of leverancier vereffenen</span><span class="sxs-lookup"><span data-stu-id="8a665-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="8a665-129">Vereffen een gepostdateerde cheque die op een overbruggingsrekening voor een klant of leverancier is geboekt wanneer de cheque eindelijk vervalt.</span><span class="sxs-lookup"><span data-stu-id="8a665-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="8a665-130">Als de cheque wordt vereffend, wordt de debitering of creditering eindelijk uitgevoerd voor de speciale rekening die eerder is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8a665-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a665-131">Een gepostdateerde cheque voor een leverancier annuleren</span><span class="sxs-lookup"><span data-stu-id="8a665-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="8a665-132">U kunt een geboekte gepostdateerde cheque in dergelijke situaties annuleren - de cheque wordt geretourneerd door de bank.</span><span class="sxs-lookup"><span data-stu-id="8a665-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="8a665-133">- De cheque is toegepast op een verkeerde factuur.</span><span class="sxs-lookup"><span data-stu-id="8a665-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="8a665-134">- De cheque is contant betaald.</span><span class="sxs-lookup"><span data-stu-id="8a665-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="8a665-135">Betaling voor een gepostdateerde cheque stoppen</span><span class="sxs-lookup"><span data-stu-id="8a665-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="8a665-136">U kunt de betaling stopzetten voor een gepostdateerde cheque die aan een leverancier is uitgeschreven, bijvoorbeeld omdat er sprake is van onvoldoende fondsen, omdat de voorwaarden van de overeenkomst met de leverancier zijn gewijzigd, omdat de leverancier defecte goederen heeft geleverd of omdat er goederen aan de leverancier zijn geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8a665-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="8a665-137">Het is alleen mogelijk om de betaling stop te zetten voor cheques die niet zijn verrekend.</span><span class="sxs-lookup"><span data-stu-id="8a665-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="8a665-138">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="8a665-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="8a665-139">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="8a665-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="8a665-140">Een gepostdateerde cheque voor een klant registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="8a665-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="8a665-141">Een gepostdateerde cheque van een klant vereffenen</span><span class="sxs-lookup"><span data-stu-id="8a665-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="8a665-142">Een gepostdateerde cheque voor een leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="8a665-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="8a665-143">Een gepostdateerde cheque voor een leverancier vereffenen</span><span class="sxs-lookup"><span data-stu-id="8a665-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



