---
title: De ER-functie CONCATENATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONCATENATE
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746476"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="fcc3c-103">De ER-functie CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="fcc3c-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcc3c-104">De functie `CONCATENATE` retourneert alle opgegeven tekenreeksen als een waarde van het type *Tekenreeks* nadat ze zijn samengevoegd in één tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc3c-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="fcc3c-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="fcc3c-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="fcc3c-106">Arguments</span></span>

<span data-ttu-id="fcc3c-107">`text 1`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="fcc3c-107">`text 1`: *String*</span></span>

<span data-ttu-id="fcc3c-108">Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="fcc3c-109">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-109">This argument is required.</span></span>

<span data-ttu-id="fcc3c-110">`text N`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="fcc3c-110">`text N`: *String*</span></span>

<span data-ttu-id="fcc3c-111">Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="fcc3c-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="fcc3c-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="fcc3c-113">Return values</span></span>

<span data-ttu-id="fcc3c-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="fcc3c-114">*String*</span></span>

<span data-ttu-id="fcc3c-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fcc3c-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fcc3c-116">Example</span></span>

<span data-ttu-id="fcc3c-117">`CONCATENATE ("abc", "def")` retourneert **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fcc3c-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="fcc3c-118">Usage notes</span></span>

<span data-ttu-id="fcc3c-119">De expressie `"abc" & "def"` retourneert ook **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcc3c-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fcc3c-120">Additional resources</span></span>

[<span data-ttu-id="fcc3c-121">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="fcc3c-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]