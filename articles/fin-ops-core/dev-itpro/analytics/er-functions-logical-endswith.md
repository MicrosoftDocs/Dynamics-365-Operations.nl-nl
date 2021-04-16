---
title: ER-functie ENDSWITH
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ENDSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: bdd2f364e2d0b80d3df20592ec827dcabf99a06c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745396"
---
# <a name="endswith-er-function"></a><span data-ttu-id="92d88-103">ER-functie ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="92d88-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92d88-104">Met de functie `ENDSWITH` wordt bepaald of de opgegeven invoer eindigt op de opgegeven tekst.</span><span class="sxs-lookup"><span data-stu-id="92d88-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="92d88-105">Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer eindigt op de opgegeven tekst.</span><span class="sxs-lookup"><span data-stu-id="92d88-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="92d88-106">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="92d88-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d88-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="92d88-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="92d88-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="92d88-108">Arguments</span></span>

<span data-ttu-id="92d88-109">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="92d88-109">`input`: *String*</span></span>

<span data-ttu-id="92d88-110">Het geldige pad van een artikel van een gegevensbron van het type *Tekenreeks* of een tekenreeksconstante, waarvan de waarde mogelijk eindigt op het tweede argument.</span><span class="sxs-lookup"><span data-stu-id="92d88-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="92d88-111">`start text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="92d88-111">`start text`: *String*</span></span>

<span data-ttu-id="92d88-112">Het geldige pad van een gegevensbron van het gegevenstype *Tekenreeks* of een tekenreeksconstante, waarvan de waarde zich mogelijk aan het einde van het eerste argument bevindt.</span><span class="sxs-lookup"><span data-stu-id="92d88-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="92d88-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="92d88-113">Return values</span></span>

<span data-ttu-id="92d88-114">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="92d88-114">*Boolean*</span></span>

<span data-ttu-id="92d88-115">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="92d88-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="92d88-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="92d88-116">Usage notes</span></span>

<span data-ttu-id="92d88-117">Deze functie kan alleen worden gebruikt om een voorwaarde-expressie van de [FILTER](er-functions-list-filter.md)-functie op te geven wanneer de relevante toewijzing is geconfigureerd in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) voor toegang tot [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="92d88-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="92d88-118">Anders moet een uitzondering worden gemaakt tijdens het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="92d88-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="92d88-119">In het bericht dat wordt weergegeven, wordt aanbevolen dat u de [WHERE](er-functions-list-where.md)-functie gebruikt in plaats van de `FILTER`-functie om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="92d88-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="92d88-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="92d88-120">Example 1</span></span>

<span data-ttu-id="92d88-121">De expressie `ENDSWITH ("abc", "d")` retourneert **FALSE**, terwijl de expressie `ENDSWITH ("abc", "C")` **TRUE** retourneert.</span><span class="sxs-lookup"><span data-stu-id="92d88-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="92d88-122">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="92d88-122">Example 2</span></span>

<span data-ttu-id="92d88-123">De expressie `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` retourneert **TRUE** als de waarde van het veld **Adres** van de **model** gegevensbron eindigt op de tekenreeks **USA**.</span><span class="sxs-lookup"><span data-stu-id="92d88-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="92d88-124">Anders wordt **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="92d88-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92d88-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="92d88-125">Additional resources</span></span>

[<span data-ttu-id="92d88-126">Logische functies</span><span class="sxs-lookup"><span data-stu-id="92d88-126">Logical functions</span></span>](er-functions-category-logical.md)
