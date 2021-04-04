---
title: De ER-functie CHAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CHAR.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563193"
---
# <a name="char-er-function"></a><span data-ttu-id="c5169-103">De ER-functie CHAR</span><span class="sxs-lookup"><span data-stu-id="c5169-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5169-104">De functie `CHAR` retourneert een waarde van het type *Tekenreeks* van één teken waarnaar wordt verwezen door het opgegeven Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="c5169-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5169-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="c5169-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="c5169-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c5169-106">Arguments</span></span>

<span data-ttu-id="c5169-107">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="c5169-107">`number`: *Integer*</span></span>

<span data-ttu-id="c5169-108">Een getal dat overeenkomt met een verwacht enkel teken.</span><span class="sxs-lookup"><span data-stu-id="c5169-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="c5169-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c5169-109">Return values</span></span>

<span data-ttu-id="c5169-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c5169-110">*String*</span></span>

<span data-ttu-id="c5169-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="c5169-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c5169-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="c5169-112">Usage notes</span></span>

<span data-ttu-id="c5169-113">De door deze functie geretourneerde tekenreeks is afhankelijk van de codering die in het bovenliggende indelingselement **FILE** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c5169-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="c5169-114">Zie voor een overzicht van ondersteunde coderingen [Coderingsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="c5169-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="c5169-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c5169-115">Example</span></span>

<span data-ttu-id="c5169-116">`CHAR (255)` retourneert **ÿ**.</span><span class="sxs-lookup"><span data-stu-id="c5169-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5169-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c5169-117">Additional resources</span></span>

[<span data-ttu-id="c5169-118">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="c5169-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]