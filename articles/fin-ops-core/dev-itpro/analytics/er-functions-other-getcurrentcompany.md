---
title: De ER-functie GETCURRENTCOMPANY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETCURRENTCOMPANY.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 3e14c6a8aaff0a32a115117938d0e853bb34bb14
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684854"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="198d8-103">De ER-functie GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="198d8-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="198d8-104">De functie `GETCURRENTCOMPANY` retourneert een *tekenreekswaarde* voor de code van de rechtspersoon (bedrijf) waarbij een gebruiker momenteel is aangemeld.</span><span class="sxs-lookup"><span data-stu-id="198d8-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="198d8-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="198d8-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="198d8-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="198d8-106">Return values</span></span>

<span data-ttu-id="198d8-107">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="198d8-107">*String*</span></span>

<span data-ttu-id="198d8-108">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="198d8-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="198d8-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="198d8-109">Example</span></span>

<span data-ttu-id="198d8-110">`GETCURRENTCOMPANY ()` retourneert **USMF** voor een gebruiker die zich heeft aangemeld bij het bedrijf **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="198d8-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="198d8-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="198d8-111">Additional resources</span></span>

[<span data-ttu-id="198d8-112">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="198d8-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
