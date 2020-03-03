---
title: De ER-functie FORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FORMAT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09efeb6b5d8bd2ea452dbf7a9ddaeec2ab75c92
ms.sourcegitcommit: 0455a024185f79ecb82df61e6d994bd71dee5c10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/20/2020
ms.locfileid: "2974287"
---
# <span data-ttu-id="f5321-103"><a name="FORMAT">De ER-functie FORMAT</a></span><span class="sxs-lookup"><span data-stu-id="f5321-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5321-104">De functie `FORMAT` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze is ingedeeld door elk exemplaar van **%N** te vervangen door het *N*e argument.</span><span class="sxs-lookup"><span data-stu-id="f5321-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5321-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="f5321-105">Syntax</span></span>

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="f5321-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="f5321-106">Arguments</span></span>

<span data-ttu-id="f5321-107">`string`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f5321-107">`string`: *String*</span></span>

<span data-ttu-id="f5321-108">Een verwijzing naar een gegevensbron van het type *Tekenreeks* die moet worden ingedeeld.</span><span class="sxs-lookup"><span data-stu-id="f5321-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="f5321-109">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="f5321-109">This argument is required.</span></span>

<span data-ttu-id="f5321-110">`argument 1`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f5321-110">`argument 1`: *String*</span></span>

<span data-ttu-id="f5321-111">Het eerste argument, dat wordt gebruikt om exemplaren van **%1** te vervangen.</span><span class="sxs-lookup"><span data-stu-id="f5321-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="f5321-112">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="f5321-112">This argument is required.</span></span>

<span data-ttu-id="f5321-113">`argument N`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f5321-113">`argument N`: *String*</span></span>

<span data-ttu-id="f5321-114">Het *N*e argument, dat wordt gebruikt om exemplaren van **%2**, **%3**, enzovoort te vervangen.</span><span class="sxs-lookup"><span data-stu-id="f5321-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="f5321-115">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="f5321-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5321-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="f5321-116">Return values</span></span>

<span data-ttu-id="f5321-117">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f5321-117">*String*</span></span>

<span data-ttu-id="f5321-118">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="f5321-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f5321-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="f5321-119">Usage notes</span></span>

<span data-ttu-id="f5321-120">Als een argument niet voor een parameter wordt verstrekt, wordt de parameter geretourneerd als **"%N"** in de tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="f5321-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="f5321-121">Voor waarden van het type *Werkelijk* wordt de standaard tekenreeksconversie beperkt tot twee decimalen.</span><span class="sxs-lookup"><span data-stu-id="f5321-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="f5321-122">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f5321-122">Example</span></span>

<span data-ttu-id="f5321-123">In de volgende afbeelding retourneert de gegevensbron **PaymentModel** een lijst met klantrecords met behulp van het onderdeel **Klant**.</span><span class="sxs-lookup"><span data-stu-id="f5321-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="f5321-124">De waarde van de verwerkingsdatum wordt geretourneerd met het veld **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="f5321-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="f5321-125">In de ER-indeling (Elektronische rapportage) die is ontworpen om een elektronisch bestand voor geselecteerde klanten te genereren, wordt **PaymentModel** geselecteerd als een gegevensbron en beheert deze de processtroom.</span><span class="sxs-lookup"><span data-stu-id="f5321-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="f5321-126">Er treedt een uitzondering op om de gebruiker te informeren wanneer een geselecteerde klant wordt gestopt voor de datum waarop het rapport wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="f5321-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="f5321-127">De formule die is ontworpen voor dit type verwerkingsbesturingselement kan de volgende bronnen gebruiken:</span><span class="sxs-lookup"><span data-stu-id="f5321-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="f5321-128">Label SYS70894, met de volgende tekst:</span><span class="sxs-lookup"><span data-stu-id="f5321-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="f5321-129">**Voor de taal EN-US:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="f5321-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="f5321-130">**Voor de taal NL:** "Er is niets om af te drukken"</span><span class="sxs-lookup"><span data-stu-id="f5321-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="f5321-131">Label SYS18389, met de volgende tekst:</span><span class="sxs-lookup"><span data-stu-id="f5321-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="f5321-132">**Voor de taal EN-US:** Customer %1 is stopped for %2.</span><span class="sxs-lookup"><span data-stu-id="f5321-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="f5321-133">**Voor de taal DE:** Debitor '%1' wird für %2 gesperrt.</span><span class="sxs-lookup"><span data-stu-id="f5321-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="f5321-134">Hier is de expressie die kan worden ontworpen.</span><span class="sxs-lookup"><span data-stu-id="f5321-134">Here is the expression that can be designed.</span></span>

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="f5321-135">Als een rapport wordt verwerkt voor de klant **Litware Retail** op 17 december 2015 in de cultuur **EN-US** en de taal **EN-US**, retourneert deze formule de volgende tekst, die aan de gebruiker kan worden weergegeven als uitzonderingsbericht:</span><span class="sxs-lookup"><span data-stu-id="f5321-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="f5321-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span><span class="sxs-lookup"><span data-stu-id="f5321-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="f5321-137">Als hetzelfde rapport voor de klant **Litware Retail** wordt verwerkt op 17 december 2015 in de cultuur **DE** en de taal **DE**, retourneert de formule de volgende tekst die een andere datumnotatie gebruikt:</span><span class="sxs-lookup"><span data-stu-id="f5321-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="f5321-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="f5321-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="f5321-139">De volgende syntaxis wordt toegepast in ER-formules voor labels:</span><span class="sxs-lookup"><span data-stu-id="f5321-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="f5321-140">**Voor labels van resources in de Microsoft Dynamics 365 Finance-app:** **\@X**, waarbij **X** de label-id in de Application Object Tree (AOT) is</span><span class="sxs-lookup"><span data-stu-id="f5321-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="f5321-141">**Voor labels die zich in ER-configuraties bevinden:** **@"GER_LABEL:X"**, waarbij **X** de label-id in de ER-configuratie is</span><span class="sxs-lookup"><span data-stu-id="f5321-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5321-142">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f5321-142">Additional resources</span></span>

[<span data-ttu-id="f5321-143">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="f5321-143">Text functions</span></span>](er-functions-category-text.md)