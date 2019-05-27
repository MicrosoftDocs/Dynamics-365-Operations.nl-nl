---
title: Rijdefinities in Ontwerper financiële rapporten
description: Een rijdefinitie is een rapportonderdeel, of bouwsteen, waarmee de inhoud van elke rij in een financieel rapport wordt gespecificeerd. Een rijdefinitie kan worden gecombineerd met kolomdefinities, rapportagestructuurdefinities en rapportdefinities om een bouwsteengroep te maken die door meerdere bedrijven kan worden gebruikt.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551596"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="c4123-104">Rijdefinities in Ontwerper financiële rapporten</span><span class="sxs-lookup"><span data-stu-id="c4123-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4123-105">Een rijdefinitie is een rapportonderdeel, of bouwsteen, waarmee de inhoud van elke rij in een financieel rapport wordt gespecificeerd.</span><span class="sxs-lookup"><span data-stu-id="c4123-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="c4123-106">Een rijdefinitie kan worden gecombineerd met kolomdefinities, rapportagestructuurdefinities en rapportdefinities om een bouwsteengroep te maken die door meerdere bedrijven kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c4123-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="c4123-107">Een rijdefinitie maken</span><span class="sxs-lookup"><span data-stu-id="c4123-107">Create a row definition</span></span>

1. <span data-ttu-id="c4123-108">Klik in Report Designer in het navigatievenster op **Rijdefinities**.</span><span class="sxs-lookup"><span data-stu-id="c4123-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="c4123-109">Klik in het menu **Bestand** op **Nieuw** en klik vervolgens op **Rijdefinities**.</span><span class="sxs-lookup"><span data-stu-id="c4123-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="c4123-110">Voor meer informatie over de inhoud van elke cel raadpleegt u [Rijdefinitiecellen wijzigen](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c4123-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="c4123-111">Een rijdefinitie openen</span><span class="sxs-lookup"><span data-stu-id="c4123-111">Open a row definition</span></span>
1. <span data-ttu-id="c4123-112">Klik in Report Designer in het navigatievenster op **Rijdefinities**.</span><span class="sxs-lookup"><span data-stu-id="c4123-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="c4123-113">Dubbelklik op de naam van de rijdefinitie die u wilt openen.</span><span class="sxs-lookup"><span data-stu-id="c4123-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="c4123-114">Als u eventuele bouwstenen wilt weergeven die aan de rijdefinitie zijn gekoppeld, klikt u met de rechtermuisknop op de rijdefinitie en selecteert u vervolgens **Koppelingen**</span><span class="sxs-lookup"><span data-stu-id="c4123-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="c4123-115">Inhoud van een rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="c4123-115">Contents of a row definition</span></span>
<span data-ttu-id="c4123-116">Een rijdefinitie kan maximaal 20.000 financiële dimensierijen bevatten en kan de volgende informatie bevatten:</span><span class="sxs-lookup"><span data-stu-id="c4123-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="c4123-117">Beschrijvende tekst die betekenis geeft aan het rapport door sectiekopteksten, regels en spaties te maken, zoals **Contant geld** of **Totale opbrengst**</span><span class="sxs-lookup"><span data-stu-id="c4123-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="c4123-118">Koppelingen naar financiële gegevens, die dimensiewaarden in Microsoft Dynamics 365 for Finance and Operations kunnen omvatten</span><span class="sxs-lookup"><span data-stu-id="c4123-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4123-119">U kunt een rijdefinitie configureren om elke keer dat het rapport wordt gegenereerd, gegevens op te halen uit het financiële dimensiesysteem.</span><span class="sxs-lookup"><span data-stu-id="c4123-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="c4123-120">Rijtotalen en formules die op de bijbehorende financiële gegevens zijn gebaseerd</span><span class="sxs-lookup"><span data-stu-id="c4123-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="c4123-121">Gewoonlijk bevat elke rij in een rijdefinitie een van de volgende soorten gegevens:</span><span class="sxs-lookup"><span data-stu-id="c4123-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="c4123-122">Verwijzingen naar het financiële dimensiessysteem</span><span class="sxs-lookup"><span data-stu-id="c4123-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="c4123-123">Totalen of berekeningen die zijn gebaseerd op de gegevens</span><span class="sxs-lookup"><span data-stu-id="c4123-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="c4123-124">Opmaak</span><span class="sxs-lookup"><span data-stu-id="c4123-124">Formatting</span></span>

<span data-ttu-id="c4123-125">Er zijn twee methoden voor het invoeren van gegevens in een rijdefinitie:</span><span class="sxs-lookup"><span data-stu-id="c4123-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="c4123-126">Voer handmatig rijgegevens in een nieuwe rijdefinitie in.</span><span class="sxs-lookup"><span data-stu-id="c4123-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="c4123-127">Voor meer informatie raadpleegt u [Rijdefinitiecellen wijzigen](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c4123-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="c4123-128">Gebruik de rapportontwerper om rijgegevens rechtstreeks uit de financiële dimensies op te halen.</span><span class="sxs-lookup"><span data-stu-id="c4123-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="c4123-129">Zie voor meer informatie het gedeelte "Gerelateerde formules/rijen/eenheden" in [Rijddefinitiecellen wijzigen](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c4123-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="c4123-130">Dimensies toevoegen aan een rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="c4123-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="c4123-131">Een dimensie is een snijpunt van gegevens en waarden.</span><span class="sxs-lookup"><span data-stu-id="c4123-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="c4123-132">U kunt gegevens en waarden groeperen in de rapportontwerper.</span><span class="sxs-lookup"><span data-stu-id="c4123-132">You can group data and values in report designer.</span></span> <span data-ttu-id="c4123-133">U kunt vervolgens transacties classificeren en meer in detail analyseren.</span><span class="sxs-lookup"><span data-stu-id="c4123-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="c4123-134">U kunt het dialoogvenster **Rijen invoegen van dimensies** gebruiken om meerdere rijen tegelijkertijd toe te voegen aan een rijdefinitie.</span><span class="sxs-lookup"><span data-stu-id="c4123-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="c4123-135">Het dialoogvenster geeft één kolom voor elke dimensie weer.</span><span class="sxs-lookup"><span data-stu-id="c4123-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="c4123-136">De volgende tabel beschrijft de informatie die u voor elke dimensie kunt opgeven.</span><span class="sxs-lookup"><span data-stu-id="c4123-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="c4123-137">Optie</span><span class="sxs-lookup"><span data-stu-id="c4123-137">Option</span></span>                | <span data-ttu-id="c4123-138">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c4123-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c4123-139">Dimensie</span><span class="sxs-lookup"><span data-stu-id="c4123-139">Dimension</span></span>             | <span data-ttu-id="c4123-140">Het patroon dat de dimensie identificeert die aan de rijdefinitie moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c4123-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="c4123-141">Dit patroon bevat één en-teken (&) of hekje (\#) voor elke positie in de dimensies.</span><span class="sxs-lookup"><span data-stu-id="c4123-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="c4123-142">Gebruik in het algemeen allemaal en-tekens voor de dimensie Hoofdrekening en allemaal hekjes voor andere dimensies.</span><span class="sxs-lookup"><span data-stu-id="c4123-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="c4123-143">Begin dimensiebereik</span><span class="sxs-lookup"><span data-stu-id="c4123-143">Dimension Range Start</span></span> | <span data-ttu-id="c4123-144">De eerste waarde voor de dimensie om aan de rijdefinitie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c4123-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="c4123-145">Einde dimensiebereik</span><span class="sxs-lookup"><span data-stu-id="c4123-145">Dimension Range End</span></span>   | <span data-ttu-id="c4123-146">De laatste waarde voor deze dimensie die aan de rijdefinitie moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c4123-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="c4123-147">Als u dimensies wilt toevoegen aan een rijdefinitie, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="c4123-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="c4123-148">Klik in Report Designer op **Rijdefinities** en open vervolgens de rijdefinitie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="c4123-149">Klik in het menu **Bewerken** op **Rijen invoegen van dimensies**.</span><span class="sxs-lookup"><span data-stu-id="c4123-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="c4123-150">Selecteer in het dialoogvenster **Rijen invoegen van dimensies** in de rij **Dimensies** de cel voor de dimensie die u naar de rijdefinitie wilt overbrengen en klik vervolgens op **Alle &&&**.</span><span class="sxs-lookup"><span data-stu-id="c4123-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="c4123-151">Als u de rijdefinitie tot een bepaald bereik van dimensiewaarden wilt beperken, voert u de begindimensiewaarde in de cel **Begin van dimensiebereik** in en voert u vervolgens de einddimensiewaarde in de cel **Einde dimensiebereik** in. Als u alle waarden voor de geselecteerde dimensie wilt opnemen, laat u deze cellen leeg.</span><span class="sxs-lookup"><span data-stu-id="c4123-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="c4123-152">Als u alle waarden voor de geselecteerde dimensie wilt opnemen, laat u deze cellen leeg.</span><span class="sxs-lookup"><span data-stu-id="c4123-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4123-153">Als u jokertekens (\* of ?) in dimensiebereikwaarden gebruikt, worden mogelijk niet alle gewenste resultaten geretourneerd (afhankelijk van de sortering van gegevens in de ERP-database).</span><span class="sxs-lookup"><span data-stu-id="c4123-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="c4123-154">Geef in het veld **Beginrijcode** de rijcode op voor de eerste dimensiewaarde die aan de rijdefinitie moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c4123-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="c4123-155">Geef in het veld **Elke rij verhogen met** een waarde op om de ruimte tussen opeenvolgende rijcodes te specificeren.</span><span class="sxs-lookup"><span data-stu-id="c4123-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="c4123-156">Als de eerste rijcode bijvoorbeeld 100 is en de verhogingswaarde 30, hebben de eerste nieuwe rijen de codes 100, 130, 160, 190 en 220.</span><span class="sxs-lookup"><span data-stu-id="c4123-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="c4123-157">Gebruik een verhogingswaarde die ruimte biedt voor het invoegen van nieuwe opmaak en formulerijen.</span><span class="sxs-lookup"><span data-stu-id="c4123-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="c4123-158">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4123-158">Click **OK**.</span></span> <span data-ttu-id="c4123-159">Voor elk van de geselecteerde dimensiewaarden wordt één regel toegevoegd aan de rijdefinitie.</span><span class="sxs-lookup"><span data-stu-id="c4123-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="c4123-160">Afronding in een rijdefinitie aanpassen</span><span class="sxs-lookup"><span data-stu-id="c4123-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="c4123-161">Wanneer u een balans hebt waarin de bedragen worden afgerond, zijn de totalen mogelijk niet in evenwicht.</span><span class="sxs-lookup"><span data-stu-id="c4123-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="c4123-162">Dit probleem kan optreden als u bijvoorbeeld de afrondingsoptie gebruikt in een balansrapport en in de rapportdefinitie eveneens afronden is gespecificeerd.</span><span class="sxs-lookup"><span data-stu-id="c4123-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="c4123-163">U kunt de optie **Afrondingscorrectie** gebruiken in de rijdefinitie om de bedragen op de balans in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="c4123-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="c4123-164">U kunt afronding uitschakelen of aanpassen op het tabblad **Instellingen** van de rapportdefinitie.</span><span class="sxs-lookup"><span data-stu-id="c4123-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="c4123-165">In de volgende tabel wordt aangegeven hoe bedragen worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="c4123-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="c4123-166">In deze tabel verschillen de totalen van rijen 100 en 200 wanneer afronding is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c4123-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="c4123-167">Rijcode</span><span class="sxs-lookup"><span data-stu-id="c4123-167">Row code</span></span> | <span data-ttu-id="c4123-168">Bedragen zonder afronding</span><span class="sxs-lookup"><span data-stu-id="c4123-168">Amounts without rounding</span></span> | <span data-ttu-id="c4123-169">Bedrag met afronding naar gehele duizendtallen</span><span class="sxs-lookup"><span data-stu-id="c4123-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="c4123-170">100</span><span class="sxs-lookup"><span data-stu-id="c4123-170">100</span></span>      | <span data-ttu-id="c4123-171">3,600</span><span class="sxs-lookup"><span data-stu-id="c4123-171">3,600</span></span>                    | <span data-ttu-id="c4123-172">4</span><span class="sxs-lookup"><span data-stu-id="c4123-172">4</span></span>                                       |
| <span data-ttu-id="c4123-173">200</span><span class="sxs-lookup"><span data-stu-id="c4123-173">200</span></span>      | <span data-ttu-id="c4123-174">3,700</span><span class="sxs-lookup"><span data-stu-id="c4123-174">3,700</span></span>                    | <span data-ttu-id="c4123-175">4</span><span class="sxs-lookup"><span data-stu-id="c4123-175">4</span></span>                                       |
| <span data-ttu-id="c4123-176">Totaal</span><span class="sxs-lookup"><span data-stu-id="c4123-176">Total</span></span>    | <span data-ttu-id="c4123-177">7,300</span><span class="sxs-lookup"><span data-stu-id="c4123-177">7,300</span></span>                    | <span data-ttu-id="c4123-178">8</span><span class="sxs-lookup"><span data-stu-id="c4123-178">8</span></span>                                       |

<span data-ttu-id="c4123-179">Als u afronding in een balans wilt aanpassen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="c4123-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="c4123-180">Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="c4123-181">Klik in het menu **Bewerken** op **Afrondingscorrectie**.</span><span class="sxs-lookup"><span data-stu-id="c4123-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="c4123-182">Voer in het dialoogvenster **Afrondingscorrecties** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c4123-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="c4123-183">**Rij Afrondingscorrectie** - De rijcode voor de rij die moet worden aangepast om de balans in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="c4123-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="c4123-184">**Rij Totale activa** - de rijcode voor de rij in de balans die de totale activa bevat.</span><span class="sxs-lookup"><span data-stu-id="c4123-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="c4123-185">**Rij Totaal aansprakelijkheden en eigen vermogen** - de rijcode voor de rij in de balans die de totale aansprakelijkheden en eigen vermogen bevat.</span><span class="sxs-lookup"><span data-stu-id="c4123-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="c4123-186">**Limiet van aanpassingsbedrag** - Een positief geheel getal dat de limiet voor automatische correcties aangeeft.</span><span class="sxs-lookup"><span data-stu-id="c4123-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="c4123-187">Dit bedrag wordt vergeleken met de absolute waarde van het werkelijke afrondingsverschil.</span><span class="sxs-lookup"><span data-stu-id="c4123-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4123-188">Deze rijcodes moeten aan uw financiële gegevens zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c4123-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="c4123-189">Met andere woorden, de rij moet een dimensiewaarde bevatten in de cel **Koppeling naar financiële dimensies**.</span><span class="sxs-lookup"><span data-stu-id="c4123-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="c4123-190">Verwijs **niet** naar een omschrijvings- (**DESC**), berekende (**CALC**) of totaalrij (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="c4123-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="c4123-191">De bedragen in uw balans zullen nu in evenwicht zijn wanneer afronding is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c4123-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="c4123-192">De correctielimiet wordt toegepast aan de hand van de optie bij **Afrondingsprecisie** die is opgegeven voor de rapportdefinitie.</span><span class="sxs-lookup"><span data-stu-id="c4123-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="c4123-193">Als u bijvoorbeeld selecteert om uw rapport op duizendtallen af te ronden en **2** invoert in het veld **Limiet van aanpassingsbedrag**, wordt een waarschuwingsbericht weergegeven wanneer de waarde die is opgegeven in het veld **Rij Afrondingscorrectie** met meer dan 2000 verhoogt of verlaagt.</span><span class="sxs-lookup"><span data-stu-id="c4123-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="c4123-194">Opmaakrij en kolomtekst</span><span class="sxs-lookup"><span data-stu-id="c4123-194">Format row and column text</span></span>
<span data-ttu-id="c4123-195">U kunt het uiterlijk van uw rapporten aanpassen door lettertypen te wijzigen en tekst op te maken.</span><span class="sxs-lookup"><span data-stu-id="c4123-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="c4123-196">In de volgende secties wordt beschreven hoe u het uiterlijk van rijen en kolommen in rapporten opmaakt.</span><span class="sxs-lookup"><span data-stu-id="c4123-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="c4123-197">Tekenstijlen beheren</span><span class="sxs-lookup"><span data-stu-id="c4123-197">Manage font styles</span></span>

<span data-ttu-id="c4123-198">U kunt lettertypen maken en wijzigen voor uw rapport.</span><span class="sxs-lookup"><span data-stu-id="c4123-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="c4123-199">U kunt deze stijlen vervolgens toepassen op het document of op een specifieke rij of kolom in een rapport.</span><span class="sxs-lookup"><span data-stu-id="c4123-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="c4123-200"><strong>Een tekenstijl maken</strong></span><span class="sxs-lookup"><span data-stu-id="c4123-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="c4123-201">Klik in Report Designer in het menu <strong>Opmaak</strong> op <strong>Stijlen en opmaak</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4123-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="c4123-202">Klik op <strong>Nieuw</strong> in het dialoogvenster <strong>Stijlen en opmaak</strong> en voer een unieke naam voor de nieuwe stijl in.</span><span class="sxs-lookup"><span data-stu-id="c4123-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="c4123-203">Selecteer de gewenste instellingen voor de tekenstijl en klik op <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4123-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4123-204"><strong>Een tekenstijl wijzigen</strong></span><span class="sxs-lookup"><span data-stu-id="c4123-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="c4123-205">Klik in Report Designer in het menu <strong>Opmaak</strong> op <strong>Stijlen en opmaak</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4123-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="c4123-206">Selecteer in het dialoogvenster <strong>Stijlen en opmaak</strong> de stijl die u wilt wijzigen en klik vervolgens op <strong>Wijzigen</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4123-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="c4123-207">Selecteer de gewenste instellingen voor de tekenstijl en klik op <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4123-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4123-208"><strong>Een tekenstijl toepassen</strong></span><span class="sxs-lookup"><span data-stu-id="c4123-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="c4123-209">Selecteer in Report Designer in een definitie of kolomdefinitie of in kop- en voetteksten een of meer cellen.</span><span class="sxs-lookup"><span data-stu-id="c4123-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="c4123-210">Selecteer een tekenstijl in de lijst <strong>Stijl</strong> op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="c4123-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="c4123-211">Tekst van rij opmaken</span><span class="sxs-lookup"><span data-stu-id="c4123-211">Format row text</span></span>

<span data-ttu-id="c4123-212">De opmaak die in de rijdefinitie is opgegeven negeert de opmaak die in de kolomdefinitie en de rapportdefinitie is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c4123-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="c4123-213">U kunt de tekstopmaak wijzigen met behulp van de besturingselementen op de werkbalk Opmaak.</span><span class="sxs-lookup"><span data-stu-id="c4123-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="c4123-214">Deze besturingselementen zijn standaard Microsoft Windows-besturingselementen.</span><span class="sxs-lookup"><span data-stu-id="c4123-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="c4123-215">Open in Report Designer de rijdefinitie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="c4123-216">Selecteer de cellen die u wilt opmaken.</span><span class="sxs-lookup"><span data-stu-id="c4123-216">Select the cells to format.</span></span> <span data-ttu-id="c4123-217">Als u meerdere cellen wilt selecteren, houdt u Ctrl ingedrukt terwijl u de cellen selecteert.</span><span class="sxs-lookup"><span data-stu-id="c4123-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="c4123-218">Klik in de werkbalk op de knop van de opmaak die u wilt toepassen.</span><span class="sxs-lookup"><span data-stu-id="c4123-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="c4123-219">Als u bijvoorbeeld een rij wilt laten inspringen, selecteert u de rij en klikt u vervolgens op **Inspringing vergroten** ![Inspringing vergroten](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Inspringing vergroten") op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="c4123-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="c4123-220">Kolommen aanpassen terwijl u rapporten ontwerpt</span><span class="sxs-lookup"><span data-stu-id="c4123-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="c4123-221">Om het gemakkelijker te maken om de kolommen waarin u werkt in de rijdefinitie weer te geven, kunt u de breedte van een kolom aanpassen en kunt u tevens kolommen verbergen (minimaliseren) of weergeven in het voorbeeldvenster.</span><span class="sxs-lookup"><span data-stu-id="c4123-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="c4123-222">De wijzigingen die u aanbrengt zijn alleen van invloed op de weergave van de kolommen op het scherm.</span><span class="sxs-lookup"><span data-stu-id="c4123-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="c4123-223">Ze hebben geen invloed op de kolomopmaak in rapporten.</span><span class="sxs-lookup"><span data-stu-id="c4123-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="c4123-224">De breedte van een kolom wijzigen in het voorbeeldvenster</span><span class="sxs-lookup"><span data-stu-id="c4123-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="c4123-225">Open in Report Designer de rijdefinitie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="c4123-226">Selecteer in het menu **Opmaak** **Kolombreedte**.</span><span class="sxs-lookup"><span data-stu-id="c4123-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="c4123-227">Voer in het dialoogvenster **Kolombreedte** in en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4123-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="c4123-228">U ook kunt de rechterbegrenzing van een kolomkopcel verslepen om de breedte van de kolom te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="c4123-229">Kolommen verbergen in het voorbeeldvenster</span><span class="sxs-lookup"><span data-stu-id="c4123-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="c4123-230">Open in Report Designer de rijdefinitie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="c4123-231">Selecteer de kolom of kolommen die u wilt minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="c4123-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="c4123-232">Klik met de rechtermuisknop en klik vervolgens op **Verbergen**.</span><span class="sxs-lookup"><span data-stu-id="c4123-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="c4123-233">Alle verborgen kolommen weergeven in het voorbeeldvenster</span><span class="sxs-lookup"><span data-stu-id="c4123-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="c4123-234">Open in Report Designer de rijdefinitie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4123-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="c4123-235">Klik met de rechtermuisknop op de geminimaliseerde kolom die u wilt weergeven en klik vervolgens op **Zichtbaar maken**.</span><span class="sxs-lookup"><span data-stu-id="c4123-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c4123-236">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c4123-236">Additional resources</span></span>

[<span data-ttu-id="c4123-237">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="c4123-237">Financial reporting</span></span>](financial-reporting-intro.md)
