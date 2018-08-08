---
title: Rentepercentages instellen voor een rentecode
description: Rentecodes bevatten instellingen die bepalen wanneer kosten voor de rente geheven worden en hoe deze berekend wordt op achterstallige rekeningen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Interest
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 665c58fd29fb986bf51e10f5814c4793940c0a47
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="cdede-103">Rentepercentages instellen voor een rentecode</span><span class="sxs-lookup"><span data-stu-id="cdede-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdede-104">Rentecodes bevatten instellingen die bepalen wanneer kosten voor de rente geheven worden en hoe deze berekend wordt op achterstallige rekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdede-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="cdede-105">U kunt een enkele rentecode instellen en deze toepassen op meerdere klantboekingsprofielen, factureringscodes of op specifieke factuurregels.</span><span class="sxs-lookup"><span data-stu-id="cdede-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="cdede-106">Als de details van de rentecode veranderen, zullen alle functies die de code gebruiken de wijzigingen automatisch toepassen op nieuwe transacties.</span><span class="sxs-lookup"><span data-stu-id="cdede-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="cdede-107">U kunt twee typen tarieven instellen voor elke rentecode:</span><span class="sxs-lookup"><span data-stu-id="cdede-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="cdede-108">Tarieven voor rente-inkomsten - Dit zijn inkomsten die worden gehaald door het aanrekenen van rente op facturen of rentenota's.</span><span class="sxs-lookup"><span data-stu-id="cdede-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="cdede-109">Tarieven voor rentebetalingen - Deze vormen kosten die betaald worden voor de rente op creditnota's.</span><span class="sxs-lookup"><span data-stu-id="cdede-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="cdede-110">Beide tarieftypes kunnen tegelijkertijd en in dezelfde rentecode bestaan.</span><span class="sxs-lookup"><span data-stu-id="cdede-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="cdede-111">Rentetarieven kunnen worden gebaseerd op drie berekeningstypen:</span><span class="sxs-lookup"><span data-stu-id="cdede-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="cdede-112">Rente volgens percentage.</span><span class="sxs-lookup"><span data-stu-id="cdede-112">Interest by percentage.</span></span>
-   <span data-ttu-id="cdede-113">Rente volgens bedrag.</span><span class="sxs-lookup"><span data-stu-id="cdede-113">Interest by amount.</span></span>
-   <span data-ttu-id="cdede-114">Rente volgens bereik, wat leidt tot een enkel percentage of bedrag.</span><span class="sxs-lookup"><span data-stu-id="cdede-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="cdede-115">Wanneer een rentecode wordt gebruikt om rente te berekenen, wordt een afzonderlijke rentecode gemaakt voor elke rentevoet die van toepassing is gedurende de periode dat de betaling de vervaldatum van de transactie heeft overschreden.</span><span class="sxs-lookup"><span data-stu-id="cdede-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="cdede-116">U gebruikt het tabblad **Inkomsten** op de pagina **Rentecode** om rentepercentages in te stellen voor rente die u verdient door rente aan te rekenen.</span><span class="sxs-lookup"><span data-stu-id="cdede-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="cdede-117">Gebruik het tabblad **Betalingen** voor het instellen van rentetarieven voor de rente die u betaalt.</span><span class="sxs-lookup"><span data-stu-id="cdede-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="cdede-118">Rentevoeten op basis van een percentage</span><span class="sxs-lookup"><span data-stu-id="cdede-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="cdede-119">U kunt de rentevoeten instellen die een opgegeven percentage berekenen.</span><span class="sxs-lookup"><span data-stu-id="cdede-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="cdede-120">Rentebedrag is van toepassing op alle valuta's.</span><span class="sxs-lookup"><span data-stu-id="cdede-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="cdede-121">Optionele limieten voor het rentebedrag kunnen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="cdede-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="cdede-122"><strong>Percentage</strong> is geselecteerd** <strong>in het veld **Rente berekenen op basis van</strong> op de pagina <strong>Rentecodes instellen</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdede-122"><strong>Percentage</strong> is selected** <strong>in the **Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="cdede-123">Als u bijvoorbeeld een rentecode wilt instellen die 5 procent rente aanrekent voor elke twee maanden dat de factuurbetaling voorbij de vervaldatum is, voert u 2 in het veld **Bereken rente elke** in en selecteert u **Maand**.</span><span class="sxs-lookup"><span data-stu-id="cdede-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="cdede-124">Rentevoeten op basis van bedragen</span><span class="sxs-lookup"><span data-stu-id="cdede-124">Interest rates based on amounts</span></span>
<span data-ttu-id="cdede-125">U kunt de rentevoeten instellen die een opgegeven bedrag berekenen per valuta.</span><span class="sxs-lookup"><span data-stu-id="cdede-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="cdede-126">Een rentebedrag wordt opgegeven voor elke valuta in de rentecode.</span><span class="sxs-lookup"><span data-stu-id="cdede-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="cdede-127">Optionele limieten voor het rentebedrag kunnen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="cdede-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="cdede-128">**Bedrag** is geselecteerd in het veld **Rente berekenen op basis van** op de pagina **Rentecodes instellen**.</span><span class="sxs-lookup"><span data-stu-id="cdede-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="cdede-129">Als u bijvoorbeeld een rentecode wilt instellen die 25,00 rente aanrekent voor elke 20 dagen dat de factuurbetaling voorbij de vervaldatum is, voert u 20 in het veld **Bereken rente elke in** en selecteert u **Dag**.</span><span class="sxs-lookup"><span data-stu-id="cdede-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="cdede-130">Rentevoeten op basis van bereiken</span><span class="sxs-lookup"><span data-stu-id="cdede-130">Interest rates based on ranges</span></span>
<span data-ttu-id="cdede-131">U kunt rentevoeten instellen die variëren afhankelijk van het openstaande bedrag, het aantal dagen dat het bedrag vervallen is of het aantal maanden dat het bedrag vervallen is.</span><span class="sxs-lookup"><span data-stu-id="cdede-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="cdede-132">U kunt het tabblad **Inkomsten per valuta** gebruiken om specifieke rente-instellingen voor elke valuta te definiëren.</span><span class="sxs-lookup"><span data-stu-id="cdede-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="cdede-133">Hier definieert u ook het bereik.</span><span class="sxs-lookup"><span data-stu-id="cdede-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="cdede-134">Met de knop **Bereiken** kunt u regels toevoegen voor de bereiken die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="cdede-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="cdede-135">De waarde bij **Van** staat voor het begin van het bereik en de waarde bij **Rentewaarde** staat voor een percentage of bedrag, afhankelijk van de selectie bij **Rente berekenen op basis van** op de pagina **Rentecodes** instellen.</span><span class="sxs-lookup"><span data-stu-id="cdede-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="cdede-136">Voorbeeld 1: Rente volgens bereik = bedrag</span><span class="sxs-lookup"><span data-stu-id="cdede-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="cdede-137">U stelt een rentecode in die één keer rente aanrekent voor elke drie maanden dat de factuur voorbij de vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="cdede-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="cdede-138">Wilt u de berekening baseren op een percentage rentewaarde, volgens getrapte bedragintervallen.</span><span class="sxs-lookup"><span data-stu-id="cdede-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="cdede-139">De rentewaarde zal 1 procent zijn voor factuurbedragen tot 1000,00, 2 procent voor bedragen van 1001,00 tot 5000,00 en 3 procent voor bedragen hoger dan 5000,00.</span><span class="sxs-lookup"><span data-stu-id="cdede-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="cdede-140">U stelt het rentecodeveld als volgt in.</span><span class="sxs-lookup"><span data-stu-id="cdede-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="cdede-141">**Veldnaam**</span><span class="sxs-lookup"><span data-stu-id="cdede-141">**Field name**</span></span>                  | <span data-ttu-id="cdede-142">**Veldwaarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="cdede-143">**Rentecode**</span><span class="sxs-lookup"><span data-stu-id="cdede-143">**Interest code**</span></span>               | <span data-ttu-id="cdede-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="cdede-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="cdede-145">**Bereken rente elke**</span><span class="sxs-lookup"><span data-stu-id="cdede-145">**Calculate interest every**</span></span>    | <span data-ttu-id="cdede-146">3/maand</span><span class="sxs-lookup"><span data-stu-id="cdede-146">3/Month</span></span>         |
| <span data-ttu-id="cdede-147">**Rente per bereik**</span><span class="sxs-lookup"><span data-stu-id="cdede-147">**Interest by range**</span></span>           | <span data-ttu-id="cdede-148">Bedrag</span><span class="sxs-lookup"><span data-stu-id="cdede-148">Amount</span></span>          |
| <span data-ttu-id="cdede-149">**Rente berekenen op basis van**</span><span class="sxs-lookup"><span data-stu-id="cdede-149">**Calculate interest based on**</span></span> | <span data-ttu-id="cdede-150">Percentage</span><span class="sxs-lookup"><span data-stu-id="cdede-150">Percentage</span></span>      |

<span data-ttu-id="cdede-151">U stelt de bereikinformatie als volgt in.</span><span class="sxs-lookup"><span data-stu-id="cdede-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="cdede-152">**Vanaf waarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-152">**From value**</span></span> | <span data-ttu-id="cdede-153">**Rentewaarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="cdede-154">0</span><span class="sxs-lookup"><span data-stu-id="cdede-154">0</span></span>              | <span data-ttu-id="cdede-155">1</span><span class="sxs-lookup"><span data-stu-id="cdede-155">1</span></span>                  |
| <span data-ttu-id="cdede-156">1,001</span><span class="sxs-lookup"><span data-stu-id="cdede-156">1,001</span></span>          | <span data-ttu-id="cdede-157">2</span><span class="sxs-lookup"><span data-stu-id="cdede-157">2</span></span>                  |
| <span data-ttu-id="cdede-158">5,001</span><span class="sxs-lookup"><span data-stu-id="cdede-158">5,001</span></span>          | <span data-ttu-id="cdede-159">3</span><span class="sxs-lookup"><span data-stu-id="cdede-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="cdede-160">Voorbeeld 2: Rente volgens bereik = Dagen</span><span class="sxs-lookup"><span data-stu-id="cdede-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="cdede-161">U stelt een rentecode in die één keer rente aanrekent voor elke 15 dagen dat de factuur voorbij de vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="cdede-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="cdede-162">U wilt de berekening baseren op een rentewaarde van een bepaald bedrag, volgens getrapte dagintervallen.</span><span class="sxs-lookup"><span data-stu-id="cdede-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="cdede-163">De waarde van de rente worden 10,00 per 15 dagen gedurende de eerste 60 dagen 15,00 per 15 dagen van dagen 61-90 en 20,00 per 15 dagen vanaf dag 91 en later.</span><span class="sxs-lookup"><span data-stu-id="cdede-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="cdede-164">U stelt het rentecodeveld als volgt in.</span><span class="sxs-lookup"><span data-stu-id="cdede-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="cdede-165">**Veldnaam**</span><span class="sxs-lookup"><span data-stu-id="cdede-165">**Field name**</span></span>                  | <span data-ttu-id="cdede-166">**Veldwaarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="cdede-167">**Rentecode**</span><span class="sxs-lookup"><span data-stu-id="cdede-167">**Interest code**</span></span>               | <span data-ttu-id="cdede-168">\*15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="cdede-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="cdede-169">**Bereken rente elke**</span><span class="sxs-lookup"><span data-stu-id="cdede-169">**Calculate interest every**</span></span>    | <span data-ttu-id="cdede-170">15/dag</span><span class="sxs-lookup"><span data-stu-id="cdede-170">15/Day</span></span>          |
| <span data-ttu-id="cdede-171">**Rente per bereik**</span><span class="sxs-lookup"><span data-stu-id="cdede-171">**Interest by range**</span></span>           | <span data-ttu-id="cdede-172">Dagen</span><span class="sxs-lookup"><span data-stu-id="cdede-172">Days</span></span>            |
| <span data-ttu-id="cdede-173">**Rente berekenen op basis van**</span><span class="sxs-lookup"><span data-stu-id="cdede-173">**Calculate interest based on**</span></span> | <span data-ttu-id="cdede-174">Bedrag</span><span class="sxs-lookup"><span data-stu-id="cdede-174">Amount</span></span>          |

<span data-ttu-id="cdede-175">U stelt de bereikinformatie als volgt in.</span><span class="sxs-lookup"><span data-stu-id="cdede-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="cdede-176">**Vanaf waarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-176">**From value**</span></span> | <span data-ttu-id="cdede-177">**Rentewaarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="cdede-178">0</span><span class="sxs-lookup"><span data-stu-id="cdede-178">0</span></span>              | <span data-ttu-id="cdede-179">10</span><span class="sxs-lookup"><span data-stu-id="cdede-179">10</span></span>                 |
| <span data-ttu-id="cdede-180">61</span><span class="sxs-lookup"><span data-stu-id="cdede-180">61</span></span>             | <span data-ttu-id="cdede-181">15</span><span class="sxs-lookup"><span data-stu-id="cdede-181">15</span></span>                 |
| <span data-ttu-id="cdede-182">91</span><span class="sxs-lookup"><span data-stu-id="cdede-182">91</span></span>             | <span data-ttu-id="cdede-183">20</span><span class="sxs-lookup"><span data-stu-id="cdede-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="cdede-184">Voorbeeld 3: Rente volgens bereik = Maanden</span><span class="sxs-lookup"><span data-stu-id="cdede-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="cdede-185">U stelt een rentecode in die één keer rente aanrekent voor elke maand dat de factuur voorbij de vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="cdede-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="cdede-186">U wilt de berekening baseren op een percentage rentewaarde, volgens getrapte maandintervallen.</span><span class="sxs-lookup"><span data-stu-id="cdede-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="cdede-187">De waarde van de rente is 1,5 procent per maand voor de eerste drie maanden achterstal, 2,0 procent per maand voor de tweede drie maanden en 2,5 procent per maand voor elke maand voorbij de eerste zes maanden.</span><span class="sxs-lookup"><span data-stu-id="cdede-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="cdede-188">U stelt het rentecodeveld als volgt in.</span><span class="sxs-lookup"><span data-stu-id="cdede-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="cdede-189">**Veldnaam**</span><span class="sxs-lookup"><span data-stu-id="cdede-189">**Field name**</span></span>                  | <span data-ttu-id="cdede-190">**Veldwaarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="cdede-191">**Rentecode**</span><span class="sxs-lookup"><span data-stu-id="cdede-191">**Interest code**</span></span>               | <span data-ttu-id="cdede-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="cdede-192">1M%ByMth</span></span>        |
| <span data-ttu-id="cdede-193">**Bereken rente elke**</span><span class="sxs-lookup"><span data-stu-id="cdede-193">**Calculate interest every**</span></span>    | <span data-ttu-id="cdede-194">1/Maand</span><span class="sxs-lookup"><span data-stu-id="cdede-194">1/Month</span></span>         |
| <span data-ttu-id="cdede-195">**Rente per bereik**</span><span class="sxs-lookup"><span data-stu-id="cdede-195">**Interest by range**</span></span>           | <span data-ttu-id="cdede-196">Maanden</span><span class="sxs-lookup"><span data-stu-id="cdede-196">Months</span></span>          |
| <span data-ttu-id="cdede-197">**Rente berekenen op basis van**</span><span class="sxs-lookup"><span data-stu-id="cdede-197">**Calculate interest based on**</span></span> | <span data-ttu-id="cdede-198">Percentage</span><span class="sxs-lookup"><span data-stu-id="cdede-198">Percentage</span></span>      |

<span data-ttu-id="cdede-199">U stelt de bereikinformatie als volgt in.</span><span class="sxs-lookup"><span data-stu-id="cdede-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="cdede-200">**Vanaf waarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-200">**From value**</span></span> | <span data-ttu-id="cdede-201">**Rentewaarde**</span><span class="sxs-lookup"><span data-stu-id="cdede-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="cdede-202">0</span><span class="sxs-lookup"><span data-stu-id="cdede-202">0</span></span>              | <span data-ttu-id="cdede-203">1.5</span><span class="sxs-lookup"><span data-stu-id="cdede-203">1.5</span></span>                |
| <span data-ttu-id="cdede-204">4</span><span class="sxs-lookup"><span data-stu-id="cdede-204">4</span></span>              | <span data-ttu-id="cdede-205">2</span><span class="sxs-lookup"><span data-stu-id="cdede-205">2</span></span>                  |
| <span data-ttu-id="cdede-206">7</span><span class="sxs-lookup"><span data-stu-id="cdede-206">7</span></span>              | <span data-ttu-id="cdede-207">2.5</span><span class="sxs-lookup"><span data-stu-id="cdede-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="cdede-208">Nieuwe versies</span><span class="sxs-lookup"><span data-stu-id="cdede-208">New versions</span></span>
<span data-ttu-id="cdede-209">Rentecodes zijn geldig op bepaalde datums.</span><span class="sxs-lookup"><span data-stu-id="cdede-209">Interest codes are date effective.</span></span> <span data-ttu-id="cdede-210">Als u de rentevoet wilt wijzigen, kunt u een **nieuwe versie** maken die vanaf een toekomstige datum geldig is.</span><span class="sxs-lookup"><span data-stu-id="cdede-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="cdede-211">Als u verschillende versies wilt bekijken, kunt u de menukeuze **Begindatum** gebruiken om de afsluitdatum te selecteren.</span><span class="sxs-lookup"><span data-stu-id="cdede-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="cdede-212">U kunt ook **Alle records weergeven** selecteren om alle rentecodes op de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cdede-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




