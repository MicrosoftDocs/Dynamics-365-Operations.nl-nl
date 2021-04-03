---
title: De ER-functie GETENUMVALUEBYNAME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570585"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="49b30-103">De ER-functie GETENUMVALUEBYNAME</span><span class="sxs-lookup"><span data-stu-id="49b30-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49b30-104">De functie `GETENUMVALUEBYNAME` zoekt naar een specifieke waarde van het type *Opsomming* in de opgegeven gegevensbron voor opsommingen met behulp van de opsommingsnaam die is opgegeven als waarde van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="49b30-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="49b30-105">Als de waarde van het type *Opsomming* wordt gevonden, wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="49b30-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="49b30-106">Anders retourneert de functie de opsommingswaarde **null**.</span><span class="sxs-lookup"><span data-stu-id="49b30-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b30-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="49b30-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="49b30-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="49b30-108">Arguments</span></span>

<span data-ttu-id="49b30-109">`enumeration data source path`: *Opsomming*</span><span class="sxs-lookup"><span data-stu-id="49b30-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="49b30-110">Het geldige verwijzingspad van een gegevensbron van een van de volgende opsommingstypen:</span><span class="sxs-lookup"><span data-stu-id="49b30-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="49b30-111">ER-opsommingsmodel (Elektronische rapportage)</span><span class="sxs-lookup"><span data-stu-id="49b30-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="49b30-112">Opsomming van ER-indelingen</span><span class="sxs-lookup"><span data-stu-id="49b30-112">ER format enumeration</span></span>
- <span data-ttu-id="49b30-113">Microsoft Dynamics 365 Finance-opsomming</span><span class="sxs-lookup"><span data-stu-id="49b30-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="49b30-114">`enumeration value text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="49b30-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="49b30-115">Een tekenreekswaarde die voor de naam van een enkele opsommingswaarde staat.</span><span class="sxs-lookup"><span data-stu-id="49b30-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="49b30-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="49b30-116">Return values</span></span>

<span data-ttu-id="49b30-117">*Opsomming* waarvoor null-waarde is toegestaan</span><span class="sxs-lookup"><span data-stu-id="49b30-117">Nullable *Enum*</span></span>

<span data-ttu-id="49b30-118">De resulterende opsommingswaarde.</span><span class="sxs-lookup"><span data-stu-id="49b30-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="49b30-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="49b30-119">Usage notes</span></span>

<span data-ttu-id="49b30-120">Er wordt geen uitzondering gegenereerd als een *opsommingswaarde* niet wordt gevonden met behulp van de naam van de opsommingswaarde die is opgegeven als een *tekenreekswaarde*.</span><span class="sxs-lookup"><span data-stu-id="49b30-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="49b30-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="49b30-121">Example 1</span></span>

<span data-ttu-id="49b30-122">In het volgende voorbeeld wordt de opsomming **ReportDirection** geïntroduceerd in een gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="49b30-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="49b30-123">Houd er rekening mee dat labels voor de opsommingswaarden worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="49b30-123">Notice that labels are defined for the enumeration values.</span></span>

![Beschikbare waarden voor een gegevensmodelopsomming](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="49b30-125">De volgende afbeelding toont deze details:</span><span class="sxs-lookup"><span data-stu-id="49b30-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="49b30-126">De gegevensbron **$Direction** wordt geconfigureerd in een ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="49b30-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="49b30-127">Deze gegevensbron wordt geconfigureerd op basis van de modelopsomming **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="49b30-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="49b30-128">De expressie `$IsArrivals` is ontworpen om de gegevensbron **$Direction** op basis van modelopsomming als parameter voor deze functie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="49b30-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="49b30-129">De waarde van deze vergelijkingsexpressie is **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="49b30-129">The value of this comparison expression is **TRUE**.</span></span>

![Voorbeeld van gegevensmodelopsomming](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="49b30-131">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="49b30-131">Example 2</span></span>

<span data-ttu-id="49b30-132">Met de functies `GETENUMVALUEBYNAME` en [`LISTOFFIELDS`](er-functions-list-listoffields.md) kunt u waarden en labels van ondersteunde opsommingen ophalen als tekstwaarden.</span><span class="sxs-lookup"><span data-stu-id="49b30-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="49b30-133">(De ondersteunde opsommingen zijn opsommingen van toepassingen, gegevensmodellen en indelingen.)</span><span class="sxs-lookup"><span data-stu-id="49b30-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="49b30-134">In de volgende afbeelding wordt de gegevensbron **TransType** in een modeltoewijzing geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="49b30-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="49b30-135">Deze gegevensbron verwijst naar de toepassingsopsomming **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="49b30-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Gegevensbron van een modeltoewijzing die verwijst naar een toepassingsopsomming](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="49b30-137">In de volgende afbeelding wordt de gegevensbron **TransTypeList** weergegeven die in een modeltoewijzing is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="49b30-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="49b30-138">Deze gegevensbron wordt geconfigureerd op basis van de opsomming **TransType**.</span><span class="sxs-lookup"><span data-stu-id="49b30-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="49b30-139">De functie `LISTOFFIELDS` wordt gebruikt om alle opsommingswaarden te retourneren als een lijst met records die velden bevatten.</span><span class="sxs-lookup"><span data-stu-id="49b30-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="49b30-140">Op deze manier worden de details van elke opsommingswaarde weergegeven.</span><span class="sxs-lookup"><span data-stu-id="49b30-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="49b30-141">Het veld **EnumValue** wordt geconfigureerd voor de gegevensbron **TransTypeList** met de expressie `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="49b30-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="49b30-142">Met dit veld wordt een opsommingswaarde geretourneerd voor elke record in deze lijst.</span><span class="sxs-lookup"><span data-stu-id="49b30-142">This field returns an enumeration value for every record in this list.</span></span>

![Gegevensbron van een modeltoewijzing waarmee alle opsommingswaarden van een geselecteerde opsomming als een lijst met records worden geretourneerd](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="49b30-144">In de volgende afbeelding wordt de gegevensbron **VendTrans** weergegeven die in een modeltoewijzing is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="49b30-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="49b30-145">Met deze gegevensbron worden leverancierstransactierecords geretourneerd uit de toepassingstabel **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="49b30-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="49b30-146">Het grootboektype van elke transactie wordt gedefinieerd door de waarde van het veld **TransType**.</span><span class="sxs-lookup"><span data-stu-id="49b30-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="49b30-147">Het veld **TransTypeTitle** wordt geconfigureerd voor de gegevensbron **VendTrans** met de expressie `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="49b30-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="49b30-148">Met dit veld wordt het label van een opsommingswaarde van de huidige transactie geretourneerd als tekst als deze opsommingswaarde beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="49b30-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="49b30-149">Anders wordt een lege tekenreekswaarde geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="49b30-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="49b30-150">Het veld **TransTypeTitle** is gebonden aan het veld **LedgerType** van een gegevensmodel waarmee deze informatie kan worden gebruikt in elke ER-indeling waarin het gegevensmodel als een bron van gegevens wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="49b30-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Gegevensbron van een modeltoewijzing waarmee leverancierstransacties worden geretourneerd](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="49b30-152">In de volgende afbeelding ziet u hoe u de [foutopsporing voor gegevensbronnen](er-debug-data-sources.md) kunt gebruiken om de geconfigureerde modeltoewijzing te testen.</span><span class="sxs-lookup"><span data-stu-id="49b30-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![De geconfigureerde modeltoewijzing testen met de foutopsporing voor gegevensbronnen](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="49b30-154">Met het veld **LedgerType** van een gegevensmodel worden labels van transactietypen zoals verwacht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="49b30-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="49b30-155">Als u deze methode wilt gebruiken voor een groot aantal transactiegegevens, moet u kijken naar de uitvoeringsprestaties.</span><span class="sxs-lookup"><span data-stu-id="49b30-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="49b30-156">Zie [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="49b30-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49b30-157">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="49b30-157">Additional resources</span></span>

[<span data-ttu-id="49b30-158">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="49b30-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="49b30-159">De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen</span><span class="sxs-lookup"><span data-stu-id="49b30-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="49b30-160">De ER-functie LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="49b30-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="49b30-161">De ER-functie FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="49b30-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="49b30-162">De ER-functie WHERE</span><span class="sxs-lookup"><span data-stu-id="49b30-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]