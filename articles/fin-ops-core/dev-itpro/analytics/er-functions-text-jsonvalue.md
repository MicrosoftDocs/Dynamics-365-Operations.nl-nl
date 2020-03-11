---
title: De ER-functie JSONVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041211"
---
# <span data-ttu-id="f79e1-103"><a name="JSONVALUE">De ER-functie JSONVALUE</a></span><span class="sxs-lookup"><span data-stu-id="f79e1-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f79e1-104">De functie `JSONVALUE` parseert gegevens in de indeling JavaScript Object Notation (JSON), die kan worden geopend op het opgegeven pad, en er wordt een scalaire waarde met de opgegeven id geëxtraheerd.</span><span class="sxs-lookup"><span data-stu-id="f79e1-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="f79e1-105">Vervolgens wordt de geëxtraheerde scalaire waarde als een *tekenreekswaarde* geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f79e1-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79e1-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="f79e1-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="f79e1-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="f79e1-107">Arguments</span></span>

<span data-ttu-id="f79e1-108">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f79e1-108">`input`: *String*</span></span>

<span data-ttu-id="f79e1-109">Het geldige pad van een gegevensbron van het type *Tekenreeks* die JSON-gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="f79e1-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="f79e1-110">`path`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f79e1-110">`path`: *String*</span></span>

<span data-ttu-id="f79e1-111">De id van een scalaire waarde van JSON-gegevens.</span><span class="sxs-lookup"><span data-stu-id="f79e1-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="f79e1-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="f79e1-112">Return values</span></span>

<span data-ttu-id="f79e1-113">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f79e1-113">*String*</span></span>

<span data-ttu-id="f79e1-114">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="f79e1-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f79e1-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f79e1-115">Example</span></span>

<span data-ttu-id="f79e1-116">De gegevensbron **JsonField** bevat de volgende gegevens in JSON-indeling: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="f79e1-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="f79e1-117">In dit geval retourneert de expressie `JSONVALUE (JsonField, "BuildNumber")` de volgende waarde van het gegevenstype *Tekenreeks*: **7.3.1234.1.**</span><span class="sxs-lookup"><span data-stu-id="f79e1-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f79e1-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f79e1-118">Additional resources</span></span>

[<span data-ttu-id="f79e1-119">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="f79e1-119">Text functions</span></span>](er-functions-category-text.md)
