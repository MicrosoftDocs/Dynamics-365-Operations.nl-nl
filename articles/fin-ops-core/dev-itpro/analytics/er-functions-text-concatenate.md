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
ms.openlocfilehash: 1a21140e5636ebd96eca4be90308c915e77510e1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743898"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="df6db-103">De ER-functie CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="df6db-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df6db-104">De functie `CONCATENATE` retourneert alle opgegeven tekenreeksen als een waarde van het type *Tekenreeks* nadat ze zijn samengevoegd in één tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="df6db-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6db-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="df6db-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="df6db-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="df6db-106">Arguments</span></span>

<span data-ttu-id="df6db-107">`text 1`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="df6db-107">`text 1`: *String*</span></span>

<span data-ttu-id="df6db-108">Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="df6db-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="df6db-109">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="df6db-109">This argument is required.</span></span>

<span data-ttu-id="df6db-110">`text N`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="df6db-110">`text N`: *String*</span></span>

<span data-ttu-id="df6db-111">Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="df6db-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="df6db-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="df6db-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="df6db-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="df6db-113">Return values</span></span>

<span data-ttu-id="df6db-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="df6db-114">*String*</span></span>

<span data-ttu-id="df6db-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="df6db-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="df6db-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="df6db-116">Example</span></span>

<span data-ttu-id="df6db-117">`CONCATENATE ("abc", "def")` retourneert **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="df6db-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="df6db-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="df6db-118">Usage notes</span></span>

<span data-ttu-id="df6db-119">De expressie `"abc" & "def"` retourneert ook **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="df6db-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df6db-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="df6db-120">Additional resources</span></span>

[<span data-ttu-id="df6db-121">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="df6db-121">Text functions</span></span>](er-functions-category-text.md)
