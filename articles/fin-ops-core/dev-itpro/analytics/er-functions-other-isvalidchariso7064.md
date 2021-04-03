---
title: De ER-functie ISVALIDCHARACTERISO7064
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISVALIDCHARACTERISO7064.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563361"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="20b81-103">De ER-functie ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="20b81-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20b81-104">De functie `ISVALIDCHARACTERISO7064` retourneert de *Booleaanse* waarde **TRUE** als de opgegeven tekenreeks staat voor een geldig internationaal bankrekeningnummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="20b81-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="20b81-105">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="20b81-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b81-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="20b81-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="20b81-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="20b81-107">Arguments</span></span>

<span data-ttu-id="20b81-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="20b81-108">`text`: *String*</span></span>

<span data-ttu-id="20b81-109">Een tekstwaarde die een IBAN vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="20b81-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="20b81-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="20b81-110">Return values</span></span>

<span data-ttu-id="20b81-111">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="20b81-111">*String*</span></span>

<span data-ttu-id="20b81-112">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="20b81-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="20b81-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="20b81-113">Example</span></span>

<span data-ttu-id="20b81-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="20b81-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="20b81-115">`ISVALIDCHARACTERISO7064 ("AT61")` retourneert **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="20b81-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20b81-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="20b81-116">Additional resources</span></span>

[<span data-ttu-id="20b81-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="20b81-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]