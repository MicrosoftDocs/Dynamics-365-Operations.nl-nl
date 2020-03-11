---
title: De ER-functie CONCATENATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONCATENATE
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
ms.openlocfilehash: 04c7b32e2a9578f8864570a552817ec3ce28fa43
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041150"
---
# <span data-ttu-id="1b96d-103"><a name="CONCATENATE">De ER-functie CONCATENATE</a></span><span class="sxs-lookup"><span data-stu-id="1b96d-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b96d-104">De functie `CONCATENATE` retourneert alle opgegeven tekenreeksen als een waarde van het type *Tekenreeks* nadat ze zijn samengevoegd in één tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="1b96d-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b96d-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="1b96d-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="1b96d-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="1b96d-106">Arguments</span></span>

<span data-ttu-id="1b96d-107">`text 1`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1b96d-107">`text 1`: *String*</span></span>

<span data-ttu-id="1b96d-108">Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="1b96d-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="1b96d-109">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="1b96d-109">This argument is required.</span></span>

<span data-ttu-id="1b96d-110">`text N`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1b96d-110">`text N`: *String*</span></span>

<span data-ttu-id="1b96d-111">Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="1b96d-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="1b96d-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="1b96d-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b96d-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="1b96d-113">Return values</span></span>

<span data-ttu-id="1b96d-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1b96d-114">*String*</span></span>

<span data-ttu-id="1b96d-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="1b96d-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1b96d-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1b96d-116">Example</span></span>

<span data-ttu-id="1b96d-117">`CONCATENATE ("abc", "def")` retourneert **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="1b96d-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1b96d-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="1b96d-118">Usage notes</span></span>

<span data-ttu-id="1b96d-119">De expressie `"abc" & "def"` retourneert ook **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="1b96d-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b96d-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1b96d-120">Additional resources</span></span>

[<span data-ttu-id="1b96d-121">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="1b96d-121">Text functions</span></span>](er-functions-category-text.md)
