---
title: Toerekenen van abonnementen
description: Met serviceabonnementen boekt u de transitorische opbrengst handmatig in de perioden die volgen op de datum waarop u een tarieftransactie hebt gefactureerd.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a183e17749c04b407eb17155ecb1363e96ade18a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546635"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="7e51a-103">Toerekenen van abonnementen</span><span class="sxs-lookup"><span data-stu-id="7e51a-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7e51a-104">Met serviceabonnementen boekt u de transitorische opbrengst handmatig in de perioden die volgen op de datum waarop u een tarieftransactie hebt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="7e51a-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="7e51a-105">Perioden voor transitorische opbrengsten worden gemaakt voor de factuurperiode die u voor de abonnementskosten hebt gedefinieerd en worden gebaseerd op de periodecode van het abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e51a-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="7e51a-106">U kunt de transitorische opbrengst boeken en terugboeken.</span><span class="sxs-lookup"><span data-stu-id="7e51a-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="7e51a-107">Transitorische creditbedragen terugboeken</span><span class="sxs-lookup"><span data-stu-id="7e51a-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="7e51a-108">Bij het crediteren van gefactureerde abonnementsbedragen kunt u twee verschillende methoden gebruiken om de transitorische bedragen terug te boeken:</span><span class="sxs-lookup"><span data-stu-id="7e51a-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="7e51a-109">u kunt elke transitorische opbrengsttransactie afzonderlijk terugboeken voordat u een creditnotavoorstel maakt voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="7e51a-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="7e51a-110">Dit is de handmatige methode.</span><span class="sxs-lookup"><span data-stu-id="7e51a-110">This is the manual method.</span></span> <span data-ttu-id="7e51a-111">(handmatig)</span><span class="sxs-lookup"><span data-stu-id="7e51a-111">(manual)</span></span>

  - <span data-ttu-id="7e51a-112">u kunt de transitorische bedragen laten terugboeken op de boekingsdatum van de creditnota of op de oorspronkelijke boekingsdatum van de toerekening.</span><span class="sxs-lookup"><span data-stu-id="7e51a-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="7e51a-113">Zie [Parameters voor abonnement (formulier)](https://technet.microsoft.com/en-us/library/aa619615.aspx) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7e51a-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/en-us/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="7e51a-114">Vereisten instellen</span><span class="sxs-lookup"><span data-stu-id="7e51a-114">Setup requirements</span></span>

<span data-ttu-id="7e51a-115">Controleer of wordt voldaan aan de volgende gegevensvereisten als u transitorische opbrengst wilt boeken:</span><span class="sxs-lookup"><span data-stu-id="7e51a-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="7e51a-116">Rekeninginstelling</span><span class="sxs-lookup"><span data-stu-id="7e51a-116">Account setup</span></span>

<span data-ttu-id="7e51a-117">De rekeningen **OHW - abonnement** en **Transitorische opbrengsten - abonnement** moeten worden ingesteld in de module **Project**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="7e51a-118">Wanneer u transitorische opbrengsten boekt, wordt de rekening **OHW - abonnement** gedebiteerd met het transitorische bedrag. Dit bedrag wordt gecrediteerd aan de rekening **Transitorische opbrengsten - abonnement**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="7e51a-119">Rekeningen instellen voor het boeken van transitorische opbrengsten van abonnementen</span><span class="sxs-lookup"><span data-stu-id="7e51a-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="7e51a-120">Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Boeking** \> **Instellingen boeking in grootboek**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="7e51a-121">Klik op het tabblad **Opbrengstrekeningen** en selecteer **OHW - abonnement** of **Transitorische opbrengsten - abonnement** om de rekeningen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="7e51a-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="7e51a-122">Abonnementsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="7e51a-122">Subscription group setup</span></span>

<span data-ttu-id="7e51a-123">U moet het selectievakje **Opbrengst samenvoegen** inschakelen om transitorische opbrengst voor abonnementen te kunnen boeken.</span><span class="sxs-lookup"><span data-stu-id="7e51a-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="7e51a-124">U vindt dit selectievakje in het formulier **Abonnementsgroepen** voor de groep die aan het abonnement is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7e51a-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="7e51a-125">Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="7e51a-126">Transitorische opbrengst voor een abonnementsgroep inschakelen</span><span class="sxs-lookup"><span data-stu-id="7e51a-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="7e51a-127">Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="7e51a-128">Perioden</span><span class="sxs-lookup"><span data-stu-id="7e51a-128">Periods</span></span>

<span data-ttu-id="7e51a-129">U moet een factureringsperiodecode definiëren.</span><span class="sxs-lookup"><span data-stu-id="7e51a-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="7e51a-130">Als u niet wilt dat transitorische opbrengst wordt geboekt in dezelfde tijdsintervallen die u voor facturering gebruikt, moet u ook een transitorische periode definiëren.</span><span class="sxs-lookup"><span data-stu-id="7e51a-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="7e51a-131">In de volgende tabel vindt u een overzicht van de transitorische perioden die u voor elke factureringsperiode kunt definiëren:</span><span class="sxs-lookup"><span data-stu-id="7e51a-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e51a-132">Factureringsperiode</span><span class="sxs-lookup"><span data-stu-id="7e51a-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="7e51a-133">Transitorische periode</span><span class="sxs-lookup"><span data-stu-id="7e51a-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e51a-134"><strong>Jaren</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7e51a-135"><strong>Jaren</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="7e51a-136"><strong>Kwartaal</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="7e51a-137"><strong>Maand</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="7e51a-138"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e51a-139"><strong>Kwartaal</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7e51a-140"><strong>Kwartaal</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="7e51a-141"><strong>Maand</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="7e51a-142"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e51a-143"><strong>Maand</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7e51a-144"><strong>Maand</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="7e51a-145"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e51a-146"><strong>Week</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7e51a-147"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e51a-148"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7e51a-149"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="7e51a-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7e51a-150">Het instellen van een factureringsperiode is een verplicht onderdeel voor het instellen van een abonnementsgroep.</span><span class="sxs-lookup"><span data-stu-id="7e51a-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="7e51a-151">U kunt zelf bepalen of u ook een transitorische periode voor de abonnementsgroep wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="7e51a-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="7e51a-152">Als u een transitorische periode voor de abonnementsgroep instelt, wordt deze periode voorgesteld in het veld **Periodecode**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="7e51a-153">U vindt dit veld in het formulier **Abonnementsopbrengsten samenvoegen** wanneer u de transitorische opbrengst van abonnementen boekt.</span><span class="sxs-lookup"><span data-stu-id="7e51a-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="7e51a-154">De transitorische periode is echter optionele informatie over de abonnementsgroep.</span><span class="sxs-lookup"><span data-stu-id="7e51a-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7e51a-155">Gebruik het volgende pad om het formulier <STRONG>Abonnementopbrengsten samenvoegen</STRONG> te openen.</span><span class="sxs-lookup"><span data-stu-id="7e51a-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="7e51a-156">Klik op <STRONG>Servicebeheer</STRONG> &gt; <STRONG>Periodiek</STRONG> &gt; <STRONG>Serviceabonnementen</STRONG> &gt; <STRONG>Abonnementsopbrengsten samenvoegen</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7e51a-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="7e51a-157">Transacties</span><span class="sxs-lookup"><span data-stu-id="7e51a-157">Transactions</span></span>

<span data-ttu-id="7e51a-158">U kunt het aantal grootboektransacties beperken dat wordt gemaakt wanneer u transitorische opbrengsten boekt.</span><span class="sxs-lookup"><span data-stu-id="7e51a-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="7e51a-159">Geef voor abonnementen op of de grootboektransacties als een totaal of per regel moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7e51a-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="7e51a-160">Opgeven welk niveau van boekingsdetails moet worden weergegeven voor transitorische transacties</span><span class="sxs-lookup"><span data-stu-id="7e51a-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="7e51a-161">Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Projectbeheer- en boekhoudingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="7e51a-162">Selecteer op het tabblad **Financieel** in het veld **Factuur** **Totaal** of **Regel**.</span><span class="sxs-lookup"><span data-stu-id="7e51a-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="7e51a-163">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7e51a-163">See also</span></span>

[<span data-ttu-id="7e51a-164">Abonnementsopbrengsten samenvoegen</span><span class="sxs-lookup"><span data-stu-id="7e51a-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


