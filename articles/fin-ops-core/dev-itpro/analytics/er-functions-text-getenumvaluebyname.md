---
title: De ER-functie GETENUMVALUEBYNAME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETENUMVALUEBYNAME.
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
ms.openlocfilehash: 87613978c149b5d41aefc58f9896424229819626
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041160"
---
# <span data-ttu-id="ec1c4-103"><a name="GETENUMVALUEBYNAME">De ER-functie GETENUMVALUEBYNAME</a></span><span class="sxs-lookup"><span data-stu-id="ec1c4-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec1c4-104">De functie `GETENUMVALUEBYNAME` zoekt naar een specifieke waarde van het type *Opsomming* in de opgegeven gegevensbron voor opsommingen met behulp van de opsommingsnaam die is opgegeven als waarde van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="ec1c4-105">Als de waarde van het type *Opsomming* wordt gevonden, wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="ec1c4-106">Anders retourneert de functie de opsommingswaarde **null**.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1c4-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="ec1c4-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="ec1c4-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="ec1c4-108">Arguments</span></span>

<span data-ttu-id="ec1c4-109">`enumeration data source path`: *Opsomming*</span><span class="sxs-lookup"><span data-stu-id="ec1c4-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="ec1c4-110">Het geldige verwijzingspad van een gegevensbron van een van de volgende opsommingstypen:</span><span class="sxs-lookup"><span data-stu-id="ec1c4-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="ec1c4-111">ER-opsommingsmodel (Elektronische rapportage)</span><span class="sxs-lookup"><span data-stu-id="ec1c4-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="ec1c4-112">Opsomming van ER-indelingen</span><span class="sxs-lookup"><span data-stu-id="ec1c4-112">ER format enumeration</span></span>
- <span data-ttu-id="ec1c4-113">Microsoft Dynamics 365 Finance-opsomming</span><span class="sxs-lookup"><span data-stu-id="ec1c4-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="ec1c4-114">`enumeration value text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ec1c4-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="ec1c4-115">Een tekenreekswaarde die voor de naam van een enkele opsommingswaarde staat.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec1c4-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="ec1c4-116">Return values</span></span>

<span data-ttu-id="ec1c4-117">*Opsomming* waarvoor null-waarde is toegestaan</span><span class="sxs-lookup"><span data-stu-id="ec1c4-117">Nullable *Enum*</span></span>

<span data-ttu-id="ec1c4-118">De resulterende opsommingswaarde.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec1c4-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="ec1c4-119">Usage notes</span></span>

<span data-ttu-id="ec1c4-120">Er wordt geen uitzondering gegenereerd als een *opsommingswaarde* niet wordt gevonden met behulp van de naam van de opsommingswaarde die is opgegeven als een *tekenreekswaarde*.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="ec1c4-121">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ec1c4-121">Example</span></span>

<span data-ttu-id="ec1c4-122">In het volgende voorbeeld wordt de opsomming **ReportDirection** geïntroduceerd in een gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="ec1c4-123">Houd er rekening mee dat labels voor de opsommingswaarden worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="ec1c4-124">De volgende afbeelding toont deze details:</span><span class="sxs-lookup"><span data-stu-id="ec1c4-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="ec1c4-125">De gegevensbron **$Direction** wordt geconfigureerd in een ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="ec1c4-126">Deze gegevensbron wordt geconfigureerd op basis van de modelopsomming **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="ec1c4-127">De expressie `$IsArrivals` is ontworpen om de gegevensbron **$Direction** op basis van modelopsomming als parameter voor deze functie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="ec1c4-128">De waarde van deze vergelijkingsexpressie is **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="ec1c4-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ec1c4-129">Additional resources</span></span>

[<span data-ttu-id="ec1c4-130">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="ec1c4-130">Text functions</span></span>](er-functions-category-text.md)
