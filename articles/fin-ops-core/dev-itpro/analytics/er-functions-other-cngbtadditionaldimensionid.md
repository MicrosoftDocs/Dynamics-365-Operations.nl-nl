---
title: De ER-functie CN_GBT_ADDITIONALDIMENSIONID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CN_GBT_ADDITIONALDIMENSIONID.
author: NickSelin
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744386"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="4ddd8-103">De ER-functie CN_GBT_ADDITIONALDIMENSIONID</span><span class="sxs-lookup"><span data-stu-id="4ddd8-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ddd8-104">De functie `CN_GBT_ADDITIONALDIMENSIONID` retourneert een waarde van het type *Tekenreeks* voor één financiële dimensie-id die uit de opgegeven tekenreeks wordt gehaald.</span><span class="sxs-lookup"><span data-stu-id="4ddd8-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="4ddd8-105">De opgegeven tekenreeks presenteert alle dimensies als een door komma's gescheiden lijst met id's.</span><span class="sxs-lookup"><span data-stu-id="4ddd8-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddd8-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="4ddd8-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="4ddd8-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="4ddd8-107">Arguments</span></span>

<span data-ttu-id="4ddd8-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="4ddd8-108">`text`: *String*</span></span>

<span data-ttu-id="4ddd8-109">Een *tekenreekswaarde* die alle dimensies als een door komma's gescheiden lijst met id's presenteert.</span><span class="sxs-lookup"><span data-stu-id="4ddd8-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="4ddd8-110">`number`: Geheel getal</span><span class="sxs-lookup"><span data-stu-id="4ddd8-110">`number`: Integer</span></span>

<span data-ttu-id="4ddd8-111">Een *geheel getal* dat de volgordecode van de gevraagde dimensie in de opgegeven tekenreeks definieert.</span><span class="sxs-lookup"><span data-stu-id="4ddd8-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ddd8-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="4ddd8-112">Return values</span></span>

<span data-ttu-id="4ddd8-113">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="4ddd8-113">*String*</span></span>

<span data-ttu-id="4ddd8-114">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="4ddd8-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4ddd8-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4ddd8-115">Example</span></span>

<span data-ttu-id="4ddd8-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` retourneert **CC**.</span><span class="sxs-lookup"><span data-stu-id="4ddd8-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ddd8-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4ddd8-117">Additional resources</span></span>

[<span data-ttu-id="4ddd8-118">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="4ddd8-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]