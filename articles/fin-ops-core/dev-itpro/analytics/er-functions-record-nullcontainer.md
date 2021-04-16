---
title: De ER-functie NULLCONTAINER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLCONTAINER.
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746502"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="3c40e-103">De ER-functie NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="3c40e-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c40e-104">De functie `NULLCONTAINER` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.</span><span class="sxs-lookup"><span data-stu-id="3c40e-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c40e-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="3c40e-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="3c40e-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3c40e-106">Arguments</span></span>

<span data-ttu-id="3c40e-107">`list`: *Recordlijst* of *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="3c40e-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="3c40e-108">Het geldige pad van een gegevensbron van het type *Recordlijst* of *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="3c40e-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c40e-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3c40e-109">Return values</span></span>

<span data-ttu-id="3c40e-110">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="3c40e-110">*Container (record)*</span></span>

<span data-ttu-id="3c40e-111">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="3c40e-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3c40e-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="3c40e-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="3c40e-113">Deze functie is verouderd.</span><span class="sxs-lookup"><span data-stu-id="3c40e-113">This function is obsolete.</span></span> <span data-ttu-id="3c40e-114">Gebruik in plaats daarvan de functie `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="3c40e-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="3c40e-115">Zie voor meer informatie [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="3c40e-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="3c40e-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3c40e-116">Example</span></span>

<span data-ttu-id="3c40e-117">`NULLCONTAINER (SPLIT ("abc", 1))` retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="3c40e-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="3c40e-118">Zie voor meer informatie [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="3c40e-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c40e-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3c40e-119">Additional resources</span></span>

[<span data-ttu-id="3c40e-120">Registratiefuncties</span><span class="sxs-lookup"><span data-stu-id="3c40e-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]