---
title: ER-functie STARTSWITH
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) STARTSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048837"
---
# <a name="startswith-er-function"></a><span data-ttu-id="35879-103">ER-functie STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="35879-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35879-104">Met de functie `STARTSWITH` wordt bepaald of de opgegeven invoer begint met de opgegeven tekst.</span><span class="sxs-lookup"><span data-stu-id="35879-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="35879-105">Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer begint met de opgegeven tekst.</span><span class="sxs-lookup"><span data-stu-id="35879-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="35879-106">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="35879-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="35879-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="35879-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="35879-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="35879-108">Arguments</span></span>

<span data-ttu-id="35879-109">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="35879-109">`input`: *String*</span></span>

<span data-ttu-id="35879-110">Het geldige pad van een artikel van een gegevensbron van het type *Tekenreeks* of een tekenreeksconstante, waarvan de waarde mogelijk begint met het tweede argument.</span><span class="sxs-lookup"><span data-stu-id="35879-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="35879-111">`start text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="35879-111">`start text`: *String*</span></span>

<span data-ttu-id="35879-112">Het geldige pad van een gegevensbron van het gegevenstype *Tekenreeks* of een tekenreeksconstante, waarvan de waarde zich mogelijk aan het begin van het eerste argument bevindt.</span><span class="sxs-lookup"><span data-stu-id="35879-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="35879-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="35879-113">Return values</span></span>

<span data-ttu-id="35879-114">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="35879-114">*Boolean*</span></span>

<span data-ttu-id="35879-115">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="35879-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="35879-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="35879-116">Usage notes</span></span>

<span data-ttu-id="35879-117">Deze functie kan alleen worden gebruikt om een voorwaarde-expressie van de [FILTER](er-functions-list-filter.md)-functie op te geven wanneer de relevante toewijzing is geconfigureerd in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) voor toegang tot [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="35879-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="35879-118">Anders moet een uitzondering worden gemaakt tijdens het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="35879-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="35879-119">In het bericht dat wordt weergegeven, wordt aanbevolen dat u de [WHERE](er-functions-list-where.md)-functie gebruikt in plaats van de `FILTER`-functie om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="35879-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="35879-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="35879-120">Example 1</span></span>

<span data-ttu-id="35879-121">De expressie `STARTSWITH ("abc", "d")` retourneert **FALSE**, terwijl de expressie `STARTSWITH ("abc", "A")` **TRUE** retourneert.</span><span class="sxs-lookup"><span data-stu-id="35879-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="35879-122">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="35879-122">Example 2</span></span>

<span data-ttu-id="35879-123">De expressie `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` retourneert **TRUE** als de waarde van het veld **Adres** van de **model** gegevensbron begint met de tekenreeks **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="35879-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="35879-124">Anders wordt **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="35879-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35879-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="35879-125">Additional resources</span></span>

[<span data-ttu-id="35879-126">Logische functies</span><span class="sxs-lookup"><span data-stu-id="35879-126">Logical functions</span></span>](er-functions-category-logical.md)
