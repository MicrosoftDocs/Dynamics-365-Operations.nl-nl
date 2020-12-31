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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 908da840ffcb94f4a60bb41ce041f5f263c921eb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688360"
---
# <a name="trim-er-function"></a><span data-ttu-id="790f8-103">De ER-functie TRIM</span><span class="sxs-lookup"><span data-stu-id="790f8-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="790f8-104">De functie `TRIM` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat voorloop- en volgspaties zijn afgekapt en nadat meerdere spaties tussen woorden zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="790f8-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="790f8-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="790f8-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="790f8-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="790f8-106">Arguments</span></span>

<span data-ttu-id="790f8-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="790f8-107">`text`: *String*</span></span>

<span data-ttu-id="790f8-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="790f8-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="790f8-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="790f8-109">Return values</span></span>

<span data-ttu-id="790f8-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="790f8-110">*String*</span></span>

<span data-ttu-id="790f8-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="790f8-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="790f8-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="790f8-112">Example</span></span>

<span data-ttu-id="790f8-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` retourneert **Sample text**.</span><span class="sxs-lookup"><span data-stu-id="790f8-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="790f8-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="790f8-114">Additional resources</span></span>

[<span data-ttu-id="790f8-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="790f8-115">Text functions</span></span>](er-functions-category-text.md)
