---
title: De ER-functie TABLENAME2ID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TABLENAME2ID.
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563265"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="663c9-103">De ER-functie TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="663c9-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="663c9-104">De functie `TABLENAME2ID` retourneert een numerieke weergave van de tabel-id voor de opgegeven tabelnaam als een *geheel getal*.</span><span class="sxs-lookup"><span data-stu-id="663c9-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="663c9-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="663c9-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="663c9-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="663c9-106">Arguments</span></span>

<span data-ttu-id="663c9-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="663c9-107">`text`: *String*</span></span>

<span data-ttu-id="663c9-108">Een tekstwaarde die voor een geldige tabelnaam staat.</span><span class="sxs-lookup"><span data-stu-id="663c9-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="663c9-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="663c9-109">Return values</span></span>

<span data-ttu-id="663c9-110">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="663c9-110">*Integer*</span></span>

<span data-ttu-id="663c9-111">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="663c9-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="663c9-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="663c9-112">Usage notes</span></span>

<span data-ttu-id="663c9-113">De uitvoering van deze functie kan verschillende resultaten in verschillende exemplaren van Microsoft Dynamics 365 Finance opleveren, zelfs als dezelfde bedrijfsnaam wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="663c9-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="663c9-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="663c9-114">Example</span></span>

<span data-ttu-id="663c9-115">`TABLENAME2ID ("Intrastat")` retourneert **1510**.</span><span class="sxs-lookup"><span data-stu-id="663c9-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="663c9-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="663c9-116">Additional resources</span></span>

[<span data-ttu-id="663c9-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="663c9-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]