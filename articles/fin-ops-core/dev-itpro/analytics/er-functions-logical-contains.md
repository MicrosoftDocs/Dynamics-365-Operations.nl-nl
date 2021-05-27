---
title: ER-functie CONTAINS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONTAINS.
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
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048865"
---
# <a name="contains-er-function"></a><span data-ttu-id="39b2e-103">ER-functie CONTAINS</span><span class="sxs-lookup"><span data-stu-id="39b2e-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39b2e-104">Met de functie `CONTAINS` wordt bepaald of de opgegeven invoer de opgegeven tekst bevat.</span><span class="sxs-lookup"><span data-stu-id="39b2e-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="39b2e-105">Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer de opgegeven tekst bevat.</span><span class="sxs-lookup"><span data-stu-id="39b2e-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="39b2e-106">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="39b2e-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b2e-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="39b2e-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="39b2e-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="39b2e-108">Arguments</span></span>

<span data-ttu-id="39b2e-109">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="39b2e-109">`input`: *String*</span></span>

<span data-ttu-id="39b2e-110">Het geldige pad van een artikel van een gegevensbron van het type *Tekenreeks* of een tekenreeksconstante, waarvan de waarde het tweede argument kan bevatten.</span><span class="sxs-lookup"><span data-stu-id="39b2e-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="39b2e-111">`search text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="39b2e-111">`search text`: *String*</span></span>

<span data-ttu-id="39b2e-112">Het geldige pad van een gegevensbron van het gegevenstype *Tekenreeks* of een tekenreeksconstante, waarvan de waarde mogelijk is opgenomen in het eerste argument.</span><span class="sxs-lookup"><span data-stu-id="39b2e-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="39b2e-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="39b2e-113">Return values</span></span>

<span data-ttu-id="39b2e-114">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="39b2e-114">*Boolean*</span></span>

<span data-ttu-id="39b2e-115">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="39b2e-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="39b2e-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="39b2e-116">Usage notes</span></span>

<span data-ttu-id="39b2e-117">Deze functie kan alleen worden gebruikt om een voorwaarde-expressie van de [FILTER](er-functions-list-filter.md)-functie op te geven wanneer de relevante toewijzing is geconfigureerd in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) voor toegang tot [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="39b2e-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="39b2e-118">Anders moet een uitzondering worden gemaakt tijdens het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="39b2e-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="39b2e-119">In het bericht dat wordt weergegeven, wordt aanbevolen dat u de [WHERE](er-functions-list-where.md)-functie gebruikt in plaats van de `FILTER`-functie om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="39b2e-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="39b2e-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="39b2e-120">Example 1</span></span>

<span data-ttu-id="39b2e-121">De expressie `CONTAINS ("abc", "d")` retourneert **FALSE**, terwijl de expressie `CONTAINS ("abc", "C")` **TRUE** retourneert.</span><span class="sxs-lookup"><span data-stu-id="39b2e-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="39b2e-122">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="39b2e-122">Example 2</span></span>

<span data-ttu-id="39b2e-123">De expressie `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` retourneert **TRUE** als de waarde van het veld **Adres** van de **model** gegevensbron de tekenreeks **DEU** bevat.</span><span class="sxs-lookup"><span data-stu-id="39b2e-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="39b2e-124">Anders wordt **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="39b2e-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39b2e-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="39b2e-125">Additional resources</span></span>

[<span data-ttu-id="39b2e-126">Logische functies</span><span class="sxs-lookup"><span data-stu-id="39b2e-126">Logical functions</span></span>](er-functions-category-logical.md)
