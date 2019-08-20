---
title: Rentepercentages instellen voor een rentecode
description: Rentecodes bevatten instellingen die bepalen wanneer kosten voor de rente geheven worden en hoe deze berekend wordt op achterstallige rekeningen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843164"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="31bb3-103">Rentepercentages instellen voor een rentecode</span><span class="sxs-lookup"><span data-stu-id="31bb3-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31bb3-104">Rentecodes bevatten instellingen die bepalen wanneer kosten voor de rente geheven worden en hoe deze berekend wordt op achterstallige rekeningen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="31bb3-105">U kunt een enkele rentecode instellen en deze toepassen op meerdere klantboekingsprofielen, factureringscodes of op specifieke factuurregels.</span><span class="sxs-lookup"><span data-stu-id="31bb3-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="31bb3-106">Als de details van de rentecode veranderen, zullen alle functies die de code gebruiken de wijzigingen automatisch toepassen op nieuwe transacties.</span><span class="sxs-lookup"><span data-stu-id="31bb3-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="31bb3-107">U kunt twee typen tarieven instellen voor elke rentecode:</span><span class="sxs-lookup"><span data-stu-id="31bb3-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="31bb3-108">Tarieven voor rente-inkomsten - Dit zijn inkomsten die worden gehaald door het aanrekenen van rente op facturen of rentenota's.</span><span class="sxs-lookup"><span data-stu-id="31bb3-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="31bb3-109">Tarieven voor rentebetalingen - Deze vormen kosten die betaald worden voor de rente op creditnota's.</span><span class="sxs-lookup"><span data-stu-id="31bb3-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="31bb3-110">Beide tarieftypes kunnen tegelijkertijd en in dezelfde rentecode bestaan.</span><span class="sxs-lookup"><span data-stu-id="31bb3-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="31bb3-111">Rentetarieven kunnen worden gebaseerd op drie berekeningstypen:</span><span class="sxs-lookup"><span data-stu-id="31bb3-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="31bb3-112">Rente volgens percentage.</span><span class="sxs-lookup"><span data-stu-id="31bb3-112">Interest by percentage.</span></span>
-   <span data-ttu-id="31bb3-113">Rente volgens bedrag.</span><span class="sxs-lookup"><span data-stu-id="31bb3-113">Interest by amount.</span></span>
-   <span data-ttu-id="31bb3-114">Rente volgens bereik, wat leidt tot een enkel percentage of bedrag.</span><span class="sxs-lookup"><span data-stu-id="31bb3-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="31bb3-115">Wanneer een rentecode wordt gebruikt om rente te berekenen, wordt een afzonderlijke rentecode gemaakt voor elke rentevoet die van toepassing is gedurende de periode dat de betaling de vervaldatum van de transactie heeft overschreden.</span><span class="sxs-lookup"><span data-stu-id="31bb3-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="31bb3-116">U gebruikt het tabblad **Inkomsten** op de pagina **Rentecode** om rentepercentages in te stellen voor rente die u verdient door rente aan te rekenen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="31bb3-117">Gebruik het tabblad **Betalingen** voor het instellen van rentetarieven voor de rente die u betaalt.</span><span class="sxs-lookup"><span data-stu-id="31bb3-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="31bb3-118">Rentevoeten op basis van een percentage</span><span class="sxs-lookup"><span data-stu-id="31bb3-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="31bb3-119">U kunt de rentevoeten instellen die een opgegeven percentage berekenen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="31bb3-120">Rentebedrag is van toepassing op alle valuta's.</span><span class="sxs-lookup"><span data-stu-id="31bb3-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="31bb3-121">Optionele limieten voor het rentebedrag kunnen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="31bb3-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="31bb3-122"><strong>Percentage</strong> is geselecteerd\*\* <strong>in het veld \*\*Rente berekenen op basis van</strong> op de pagina <strong>Rentecodes instellen</strong>.</span><span class="sxs-lookup"><span data-stu-id="31bb3-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="31bb3-123">Als u bijvoorbeeld een rentecode wilt instellen die 5 procent rente aanrekent voor elke twee maanden dat de factuurbetaling voorbij de vervaldatum is, voert u 2 in het veld **Bereken rente elke** in en selecteert u **Maand**.</span><span class="sxs-lookup"><span data-stu-id="31bb3-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="31bb3-124">Rentevoeten op basis van bedragen</span><span class="sxs-lookup"><span data-stu-id="31bb3-124">Interest rates based on amounts</span></span>
<span data-ttu-id="31bb3-125">U kunt de rentevoeten instellen die een opgegeven bedrag berekenen per valuta.</span><span class="sxs-lookup"><span data-stu-id="31bb3-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="31bb3-126">Een rentebedrag wordt opgegeven voor elke valuta in de rentecode.</span><span class="sxs-lookup"><span data-stu-id="31bb3-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="31bb3-127">Optionele limieten voor het rentebedrag kunnen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="31bb3-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="31bb3-128">**Bedrag** is geselecteerd in het veld **Rente berekenen op basis van** op de pagina **Rentecodes instellen**.</span><span class="sxs-lookup"><span data-stu-id="31bb3-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="31bb3-129">Als u bijvoorbeeld een rentecode wilt instellen die 25,00 rente aanrekent voor elke 20 dagen dat de factuurbetaling voorbij de vervaldatum is, voert u 20 in het veld **Bereken rente elke in** en selecteert u **Dag**.</span><span class="sxs-lookup"><span data-stu-id="31bb3-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="31bb3-130">Rentevoeten op basis van bereiken</span><span class="sxs-lookup"><span data-stu-id="31bb3-130">Interest rates based on ranges</span></span>
<span data-ttu-id="31bb3-131">U kunt rentevoeten instellen die variëren afhankelijk van het openstaande bedrag, het aantal dagen dat het bedrag vervallen is of het aantal maanden dat het bedrag vervallen is.</span><span class="sxs-lookup"><span data-stu-id="31bb3-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="31bb3-132">U kunt het tabblad **Inkomsten per valuta** gebruiken om specifieke rente-instellingen voor elke valuta te definiëren.</span><span class="sxs-lookup"><span data-stu-id="31bb3-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="31bb3-133">Hier definieert u ook het bereik.</span><span class="sxs-lookup"><span data-stu-id="31bb3-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="31bb3-134">Met de knop **Bereiken** kunt u regels toevoegen voor de bereiken die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="31bb3-135">De waarde bij **Van** staat voor het begin van het bereik en de waarde bij **Rentewaarde** staat voor een percentage of bedrag, afhankelijk van de selectie bij **Rente berekenen op basis van** op de pagina **Rentecodes** instellen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="31bb3-136">Voorbeeld 1: Rente volgens bereik = bedrag</span><span class="sxs-lookup"><span data-stu-id="31bb3-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="31bb3-137">U stelt een rentecode in die één keer rente aanrekent voor elke drie maanden dat de factuur voorbij de vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="31bb3-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="31bb3-138">Wilt u de berekening baseren op een percentage rentewaarde, volgens getrapte bedragintervallen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="31bb3-139">De rentewaarde zal 1 procent zijn voor factuurbedragen tot 1000,00, 2 procent voor bedragen van 1001,00 tot 5000,00 en 3 procent voor bedragen hoger dan 5000,00.</span><span class="sxs-lookup"><span data-stu-id="31bb3-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="31bb3-140">U stelt het rentecodeveld als volgt in.</span><span class="sxs-lookup"><span data-stu-id="31bb3-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="31bb3-141">**Veldnaam**</span><span class="sxs-lookup"><span data-stu-id="31bb3-141">**Field name**</span></span>                  | <span data-ttu-id="31bb3-142">**Veldwaarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="31bb3-143">**Rentecode**</span><span class="sxs-lookup"><span data-stu-id="31bb3-143">**Interest code**</span></span>               | <span data-ttu-id="31bb3-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="31bb3-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="31bb3-145">**Bereken rente elke**</span><span class="sxs-lookup"><span data-stu-id="31bb3-145">**Calculate interest every**</span></span>    | <span data-ttu-id="31bb3-146">3/maand</span><span class="sxs-lookup"><span data-stu-id="31bb3-146">3/Month</span></span>         |
| <span data-ttu-id="31bb3-147">**Rente per bereik**</span><span class="sxs-lookup"><span data-stu-id="31bb3-147">**Interest by range**</span></span>           | <span data-ttu-id="31bb3-148">Bedrag</span><span class="sxs-lookup"><span data-stu-id="31bb3-148">Amount</span></span>          |
| <span data-ttu-id="31bb3-149">**Rente berekenen op basis van**</span><span class="sxs-lookup"><span data-stu-id="31bb3-149">**Calculate interest based on**</span></span> | <span data-ttu-id="31bb3-150">Percentage</span><span class="sxs-lookup"><span data-stu-id="31bb3-150">Percentage</span></span>      |

<span data-ttu-id="31bb3-151">U stelt de bereikinformatie als volgt in.</span><span class="sxs-lookup"><span data-stu-id="31bb3-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="31bb3-152">**Vanaf waarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-152">**From value**</span></span> | <span data-ttu-id="31bb3-153">**Rentewaarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="31bb3-154">0</span><span class="sxs-lookup"><span data-stu-id="31bb3-154">0</span></span>              | <span data-ttu-id="31bb3-155">1</span><span class="sxs-lookup"><span data-stu-id="31bb3-155">1</span></span>                  |
| <span data-ttu-id="31bb3-156">1,001</span><span class="sxs-lookup"><span data-stu-id="31bb3-156">1,001</span></span>          | <span data-ttu-id="31bb3-157">2</span><span class="sxs-lookup"><span data-stu-id="31bb3-157">2</span></span>                  |
| <span data-ttu-id="31bb3-158">5,001</span><span class="sxs-lookup"><span data-stu-id="31bb3-158">5,001</span></span>          | <span data-ttu-id="31bb3-159">3</span><span class="sxs-lookup"><span data-stu-id="31bb3-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="31bb3-160">Voorbeeld 2: Rente volgens bereik = Dagen</span><span class="sxs-lookup"><span data-stu-id="31bb3-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="31bb3-161">U stelt een rentecode in die één keer rente aanrekent voor elke 15 dagen dat de factuur voorbij de vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="31bb3-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="31bb3-162">U wilt de berekening baseren op een rentewaarde van een bepaald bedrag, volgens getrapte dagintervallen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="31bb3-163">De waarde van de rente worden 10,00 per 15 dagen gedurende de eerste 60 dagen 15,00 per 15 dagen van dagen 61-90 en 20,00 per 15 dagen vanaf dag 91 en later.</span><span class="sxs-lookup"><span data-stu-id="31bb3-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="31bb3-164">U stelt het rentecodeveld als volgt in.</span><span class="sxs-lookup"><span data-stu-id="31bb3-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="31bb3-165">**Veldnaam**</span><span class="sxs-lookup"><span data-stu-id="31bb3-165">**Field name**</span></span>                  | <span data-ttu-id="31bb3-166">**Veldwaarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="31bb3-167">**Rentecode**</span><span class="sxs-lookup"><span data-stu-id="31bb3-167">**Interest code**</span></span>               | <span data-ttu-id="31bb3-168">\*15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="31bb3-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="31bb3-169">**Bereken rente elke**</span><span class="sxs-lookup"><span data-stu-id="31bb3-169">**Calculate interest every**</span></span>    | <span data-ttu-id="31bb3-170">15/dag</span><span class="sxs-lookup"><span data-stu-id="31bb3-170">15/Day</span></span>          |
| <span data-ttu-id="31bb3-171">**Rente per bereik**</span><span class="sxs-lookup"><span data-stu-id="31bb3-171">**Interest by range**</span></span>           | <span data-ttu-id="31bb3-172">Dagen</span><span class="sxs-lookup"><span data-stu-id="31bb3-172">Days</span></span>            |
| <span data-ttu-id="31bb3-173">**Rente berekenen op basis van**</span><span class="sxs-lookup"><span data-stu-id="31bb3-173">**Calculate interest based on**</span></span> | <span data-ttu-id="31bb3-174">Bedrag</span><span class="sxs-lookup"><span data-stu-id="31bb3-174">Amount</span></span>          |

<span data-ttu-id="31bb3-175">U stelt de bereikinformatie als volgt in.</span><span class="sxs-lookup"><span data-stu-id="31bb3-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="31bb3-176">**Vanaf waarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-176">**From value**</span></span> | <span data-ttu-id="31bb3-177">**Rentewaarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="31bb3-178">0</span><span class="sxs-lookup"><span data-stu-id="31bb3-178">0</span></span>              | <span data-ttu-id="31bb3-179">10</span><span class="sxs-lookup"><span data-stu-id="31bb3-179">10</span></span>                 |
| <span data-ttu-id="31bb3-180">61</span><span class="sxs-lookup"><span data-stu-id="31bb3-180">61</span></span>             | <span data-ttu-id="31bb3-181">15</span><span class="sxs-lookup"><span data-stu-id="31bb3-181">15</span></span>                 |
| <span data-ttu-id="31bb3-182">91</span><span class="sxs-lookup"><span data-stu-id="31bb3-182">91</span></span>             | <span data-ttu-id="31bb3-183">20</span><span class="sxs-lookup"><span data-stu-id="31bb3-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="31bb3-184">Voorbeeld 3: Rente volgens bereik = Maanden</span><span class="sxs-lookup"><span data-stu-id="31bb3-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="31bb3-185">U stelt een rentecode in die één keer rente aanrekent voor elke maand dat de factuur voorbij de vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="31bb3-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="31bb3-186">U wilt de berekening baseren op een percentage rentewaarde, volgens getrapte maandintervallen.</span><span class="sxs-lookup"><span data-stu-id="31bb3-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="31bb3-187">De waarde van de rente is 1,5 procent per maand voor de eerste drie maanden achterstal, 2,0 procent per maand voor de tweede drie maanden en 2,5 procent per maand voor elke maand voorbij de eerste zes maanden.</span><span class="sxs-lookup"><span data-stu-id="31bb3-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="31bb3-188">U stelt het rentecodeveld als volgt in.</span><span class="sxs-lookup"><span data-stu-id="31bb3-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="31bb3-189">**Veldnaam**</span><span class="sxs-lookup"><span data-stu-id="31bb3-189">**Field name**</span></span>                  | <span data-ttu-id="31bb3-190">**Veldwaarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="31bb3-191">**Rentecode**</span><span class="sxs-lookup"><span data-stu-id="31bb3-191">**Interest code**</span></span>               | <span data-ttu-id="31bb3-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="31bb3-192">1M%ByMth</span></span>        |
| <span data-ttu-id="31bb3-193">**Bereken rente elke**</span><span class="sxs-lookup"><span data-stu-id="31bb3-193">**Calculate interest every**</span></span>    | <span data-ttu-id="31bb3-194">1/Maand</span><span class="sxs-lookup"><span data-stu-id="31bb3-194">1/Month</span></span>         |
| <span data-ttu-id="31bb3-195">**Rente per bereik**</span><span class="sxs-lookup"><span data-stu-id="31bb3-195">**Interest by range**</span></span>           | <span data-ttu-id="31bb3-196">Maanden</span><span class="sxs-lookup"><span data-stu-id="31bb3-196">Months</span></span>          |
| <span data-ttu-id="31bb3-197">**Rente berekenen op basis van**</span><span class="sxs-lookup"><span data-stu-id="31bb3-197">**Calculate interest based on**</span></span> | <span data-ttu-id="31bb3-198">Percentage</span><span class="sxs-lookup"><span data-stu-id="31bb3-198">Percentage</span></span>      |

<span data-ttu-id="31bb3-199">U stelt de bereikinformatie als volgt in.</span><span class="sxs-lookup"><span data-stu-id="31bb3-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="31bb3-200">**Vanaf waarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-200">**From value**</span></span> | <span data-ttu-id="31bb3-201">**Rentewaarde**</span><span class="sxs-lookup"><span data-stu-id="31bb3-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="31bb3-202">0</span><span class="sxs-lookup"><span data-stu-id="31bb3-202">0</span></span>              | <span data-ttu-id="31bb3-203">1.5</span><span class="sxs-lookup"><span data-stu-id="31bb3-203">1.5</span></span>                |
| <span data-ttu-id="31bb3-204">4</span><span class="sxs-lookup"><span data-stu-id="31bb3-204">4</span></span>              | <span data-ttu-id="31bb3-205">2</span><span class="sxs-lookup"><span data-stu-id="31bb3-205">2</span></span>                  |
| <span data-ttu-id="31bb3-206">7</span><span class="sxs-lookup"><span data-stu-id="31bb3-206">7</span></span>              | <span data-ttu-id="31bb3-207">2.5</span><span class="sxs-lookup"><span data-stu-id="31bb3-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="31bb3-208">Nieuwe versies</span><span class="sxs-lookup"><span data-stu-id="31bb3-208">New versions</span></span>
<span data-ttu-id="31bb3-209">Rentecodes zijn geldig op bepaalde datums.</span><span class="sxs-lookup"><span data-stu-id="31bb3-209">Interest codes are date effective.</span></span> <span data-ttu-id="31bb3-210">Als u de rentevoet wilt wijzigen, kunt u een **nieuwe versie** maken die vanaf een toekomstige datum geldig is.</span><span class="sxs-lookup"><span data-stu-id="31bb3-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="31bb3-211">Als u verschillende versies wilt bekijken, kunt u de menukeuze **Begindatum** gebruiken om de afsluitdatum te selecteren.</span><span class="sxs-lookup"><span data-stu-id="31bb3-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="31bb3-212">U kunt ook **Alle records weergeven** selecteren om alle rentecodes op de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="31bb3-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



