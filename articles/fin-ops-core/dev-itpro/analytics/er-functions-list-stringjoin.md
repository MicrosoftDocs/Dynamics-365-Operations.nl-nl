---
title: De ER-functie STRINGJOIN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) STRINGJOIN.
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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041786"
---
# <span data-ttu-id="87ec0-103"><a name="STRINGJOIN">De ER-functie STRINGJOIN</a></span><span class="sxs-lookup"><span data-stu-id="87ec0-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87ec0-104">De functie `STRINGJOIN` retourneert een *tekenreekswaarde* die bestaat uit samengevoegde waarden van het opgegeven veld uit de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="87ec0-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="87ec0-105">De waarden kunnen worden gescheiden door het opgegeven scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="87ec0-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ec0-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="87ec0-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="87ec0-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="87ec0-107">Arguments</span></span>

<span data-ttu-id="87ec0-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="87ec0-108">`list`: *Record list*</span></span>

<span data-ttu-id="87ec0-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="87ec0-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="87ec0-110">`field`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="87ec0-110">`field`: *Field*</span></span>

<span data-ttu-id="87ec0-111">Het geldige pad van een veld van het type *Tekenreeks* in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="87ec0-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="87ec0-112">`delimiter`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="87ec0-112">`delimiter`: *String*</span></span>

<span data-ttu-id="87ec0-113">Een scheidingsteken dat wordt gebruikt om subtekenreeksen te scheiden.</span><span class="sxs-lookup"><span data-stu-id="87ec0-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="87ec0-114">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="87ec0-114">Return values</span></span>

<span data-ttu-id="87ec0-115">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="87ec0-115">*String*</span></span>

<span data-ttu-id="87ec0-116">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="87ec0-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="87ec0-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="87ec0-117">Example</span></span>

<span data-ttu-id="87ec0-118">Als u `SPLIT("abc" , 1)` als gegevensbron **DS** invoert, geeft de expressie `STRINGJOIN (DS, DS.Value, "-")` als resultaat **a-b-c**.</span><span class="sxs-lookup"><span data-stu-id="87ec0-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87ec0-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="87ec0-119">Additional resources</span></span>

[<span data-ttu-id="87ec0-120">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="87ec0-120">List functions</span></span>](er-functions-category-list.md)
