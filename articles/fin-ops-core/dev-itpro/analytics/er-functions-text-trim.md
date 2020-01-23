---
title: De ER-functie TRIM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRIM.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915528"
---
# <span data-ttu-id="d87b6-103"><a name="TRIM">De ER-functie TRIM</a></span><span class="sxs-lookup"><span data-stu-id="d87b6-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d87b6-104">De functie `TRIM` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat voorloop- en volgspaties zijn afgekapt en nadat meerdere spaties tussen woorden zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d87b6-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87b6-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="d87b6-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="d87b6-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="d87b6-106">Arguments</span></span>

<span data-ttu-id="d87b6-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="d87b6-107">`text`: *String*</span></span>

<span data-ttu-id="d87b6-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="d87b6-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d87b6-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="d87b6-109">Return values</span></span>

<span data-ttu-id="d87b6-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="d87b6-110">*String*</span></span>

<span data-ttu-id="d87b6-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="d87b6-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d87b6-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d87b6-112">Example</span></span>

<span data-ttu-id="d87b6-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` retourneert **Sample text**.</span><span class="sxs-lookup"><span data-stu-id="d87b6-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d87b6-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d87b6-114">Additional resources</span></span>

[<span data-ttu-id="d87b6-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="d87b6-115">Text functions</span></span>](er-functions-category-text.md)
