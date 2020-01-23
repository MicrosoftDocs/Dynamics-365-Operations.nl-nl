---
title: De ER-functie VALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUE.
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917621"
---
# <span data-ttu-id="2e20f-103"><a name="VALUE">De ER-functie VALUE</a></span><span class="sxs-lookup"><span data-stu-id="2e20f-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e20f-104">De functie `VALUE` retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="2e20f-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e20f-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="2e20f-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="2e20f-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="2e20f-106">Arguments</span></span>

<span data-ttu-id="2e20f-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="2e20f-107">`text`: *String*</span></span>

<span data-ttu-id="2e20f-108">Een tekenreekswaarde die moet worden geconverteerd naar een numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="2e20f-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e20f-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="2e20f-109">Return values</span></span>

<span data-ttu-id="2e20f-110">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="2e20f-110">*Real*</span></span>

<span data-ttu-id="2e20f-111">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="2e20f-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2e20f-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="2e20f-112">Usage notes</span></span>

<span data-ttu-id="2e20f-113">De komma's en punttekens (.) worden beschouwd als decimale scheidingstekens en er wordt een koppelteken (-) vooraan gebruikt als minteken.</span><span class="sxs-lookup"><span data-stu-id="2e20f-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="2e20f-114">Tijdens runtime treedt een uitzondering op als andere niet-numerieke tekens worden aangetroffen in de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="2e20f-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="2e20f-115">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="2e20f-115">Example 1</span></span>

<span data-ttu-id="2e20f-116">`VALUE ("1 234,56")` leidt tot een uitzondering.</span><span class="sxs-lookup"><span data-stu-id="2e20f-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="2e20f-117">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="2e20f-117">Example 2</span></span>

<span data-ttu-id="2e20f-118">`VALUE ("1234,56")` retourneert **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="2e20f-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e20f-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2e20f-119">Additional resources</span></span>

[<span data-ttu-id="2e20f-120">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="2e20f-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
