---
title: De ER-functie LISTOFFIELDS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTOFFIELDS.
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
ms.openlocfilehash: c288050fa1f9f1be9c38696e844e782794795471
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745076"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="c660b-103">De ER-functie LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="c660b-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c660b-104">De functie `LISTOFFIELDS` retourneert een *recordlijstwaarde* die wordt gemaakt op basis van de structuur van het opgegeven argument van het type *Opsomming* of *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="c660b-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c660b-105">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="c660b-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="c660b-106">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="c660b-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="c660b-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c660b-107">Arguments</span></span>

<span data-ttu-id="c660b-108">`path`: Gegevensbronverwijzing</span><span class="sxs-lookup"><span data-stu-id="c660b-108">`path`: Data source reference</span></span>

<span data-ttu-id="c660b-109">Het geldige verwijzingspad van een gegevensbron van een van de volgende gegevenstypen:</span><span class="sxs-lookup"><span data-stu-id="c660b-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="c660b-110">Modelopsomming</span><span class="sxs-lookup"><span data-stu-id="c660b-110">Model enumeration</span></span>
- <span data-ttu-id="c660b-111">Opsomming van indelingen</span><span class="sxs-lookup"><span data-stu-id="c660b-111">Format enumeration</span></span>
- <span data-ttu-id="c660b-112">Toepassingsopsomming</span><span class="sxs-lookup"><span data-stu-id="c660b-112">Application enumeration</span></span>
- <span data-ttu-id="c660b-113">Container (record)</span><span class="sxs-lookup"><span data-stu-id="c660b-113">Container (record)</span></span>

<span data-ttu-id="c660b-114">`language`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c660b-114">`language`: *String*</span></span>

<span data-ttu-id="c660b-115">Tekst die een taalcode vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="c660b-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="c660b-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c660b-116">Return values</span></span>

<span data-ttu-id="c660b-117">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="c660b-117">*Record list*</span></span>

<span data-ttu-id="c660b-118">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="c660b-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c660b-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="c660b-119">Usage notes</span></span>

<span data-ttu-id="c660b-120">De lijst die wordt gemaakt bestaat uit records met de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="c660b-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="c660b-121">**Naam** (gegevenstype *Tekenreeks*)</span><span class="sxs-lookup"><span data-stu-id="c660b-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="c660b-122">**Label** (gegevenstype *Tekenreeks*)</span><span class="sxs-lookup"><span data-stu-id="c660b-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="c660b-123">**Beschrijving** (gegevenstype *Tekenreeks*)</span><span class="sxs-lookup"><span data-stu-id="c660b-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="c660b-124">**Istranslated** (gegevenstype *Booleaans*)</span><span class="sxs-lookup"><span data-stu-id="c660b-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="c660b-125">Als het argument `path` verwijst naar een gegevensbron van het type *Container (record)*, wordt voor elk veld van de container record waarnaar wordt verwezen een nieuwe record toegevoegd aan de lijst die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c660b-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="c660b-126">Voor elke record die wordt gemaakt, retourneert het veld **Naam** de naam van het veld van de containerrecord waarnaar wordt verwezen waarvoor de huidige record is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c660b-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="c660b-127">Als het argument `path` verwijst naar een gegevensbron van een van de typen *Opsomming*, wordt voor elke opsommingswaarde van de opsomming waarnaar wordt verwezen een nieuwe record toegevoegd aan de lijst die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c660b-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="c660b-128">Voor elke record die wordt gemaakt, retourneert het veld **Naam** de waarde van de opsomming waarnaar wordt verwezen en waarvoor de huidige record is gemaakt. Het veld **Beschrijving** retourneert de beschrijving van die opsomming en het veld **Label** retourneert het label van die opsomming.</span><span class="sxs-lookup"><span data-stu-id="c660b-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="c660b-129">Wanneer bij uitvoering syntaxis 1 wordt gebruikt, moeten de velden **Label** en **Beschrijving** waarden retourneren die zijn gebaseerd op de taalinstellingen van de ER-indeling (Elektronische rapportage) die wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="c660b-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="c660b-130">Als de labels en beschrijvingen voor de gevraagde taal beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op die taal en retourneert het veld **IsTranslated** de waarde **True**.</span><span class="sxs-lookup"><span data-stu-id="c660b-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="c660b-131">Als de labels en beschrijvingen voor de gevraagde taal niet beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op de standaardtaal **EN-US** en retourneert het veld **IsTranslated** de waarde **False**.</span><span class="sxs-lookup"><span data-stu-id="c660b-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="c660b-132">Wanneer bij uitvoering syntaxis 2 wordt gebruikt, moeten de velden **Label** en **Beschrijving** waarden retourneren die zijn gebaseerd op de taal die is gedefinieerd als het tweede argument van de aangeroepen functie:</span><span class="sxs-lookup"><span data-stu-id="c660b-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="c660b-133">Als de labels en beschrijvingen voor de gevraagde taal beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op die taal en retourneert het veld **IsTranslated** de waarde **True**.</span><span class="sxs-lookup"><span data-stu-id="c660b-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="c660b-134">Als de labels en beschrijvingen voor de gevraagde taal niet beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op de taal **EN-US** en retourneert het veld **IsTranslated** de waarde **False**.</span><span class="sxs-lookup"><span data-stu-id="c660b-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="c660b-135">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="c660b-135">Example 1</span></span>

<span data-ttu-id="c660b-136">In het volgende voorbeeld wordt een opsomming geïntroduceerd in een ER-gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="c660b-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="c660b-137">De volgende afbeelding toont deze details:</span><span class="sxs-lookup"><span data-stu-id="c660b-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="c660b-138">De modelopsomming wordt in een rapport ingevoegd als gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="c660b-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="c660b-139">Een ER-expressie gebruikt de modelopsomming als een parameter van de functie `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="c660b-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="c660b-140">Een gegevensbron van het type *Recordlijst* wordt ingevoegd in een rapport met de gemaakte ER-expressie.</span><span class="sxs-lookup"><span data-stu-id="c660b-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="c660b-141">In het volgende voorbeeld ziet u de elementen van de ER-indeling die gebonden zijn aan de gegevensbron van het type *Recordlijst* die is gemaakt met de functie `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="c660b-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="c660b-142">In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c660b-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="c660b-143">Op basis van de taalinstellingen van de bovenliggende indelingselementen **BESTAND** en **MAP** worden labels en beschrijvingen in de uitvoer van de ER-indeling ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="c660b-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="c660b-144">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="c660b-144">Example 2</span></span>

<span data-ttu-id="c660b-145">U gebruikt het gegevensbrontype *Berekend veld* om de gegevensbronnen **enumType\_de** en **enumType\_deCH** te configureren voor de gegevensmodelopsomming **enumType**:</span><span class="sxs-lookup"><span data-stu-id="c660b-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="c660b-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="c660b-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="c660b-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="c660b-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="c660b-148">In dit geval kunt u de volgende expressie gebruiken om het label van de opsommingswaarde in Zwitsers Duits te krijgen, als deze vertaling beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="c660b-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="c660b-149">Als de Zwitsers Duitse vertaling niet beschikbaar is, is het label in het Duits.</span><span class="sxs-lookup"><span data-stu-id="c660b-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="c660b-150">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c660b-150">Additional resources</span></span>

[<span data-ttu-id="c660b-151">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="c660b-151">List functions</span></span>](er-functions-category-list.md)
