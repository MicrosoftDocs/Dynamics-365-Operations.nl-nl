---
title: De ER-functie WHERE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) WHERE.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041826"
---
# <span data-ttu-id="05942-103"><a name="WHERE">De ER-functie WHERE</a></span><span class="sxs-lookup"><span data-stu-id="05942-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05942-104">De functie `WHERE` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gefilterd op basis van de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="05942-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="05942-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="05942-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="05942-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="05942-106">Arguments</span></span>

<span data-ttu-id="05942-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="05942-107">`list`: *Record list*</span></span>

<span data-ttu-id="05942-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="05942-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="05942-109">`condition`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="05942-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="05942-110">Een geldige voorwaardelijke expressie die wordt gebruikt om records van de opgegeven lijst te filteren.</span><span class="sxs-lookup"><span data-stu-id="05942-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="05942-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="05942-111">Return values</span></span>

<span data-ttu-id="05942-112">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="05942-112">*Record list*</span></span>

<span data-ttu-id="05942-113">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="05942-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="05942-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="05942-114">Usage notes</span></span>

<span data-ttu-id="05942-115">Deze functie verschilt van de functie [FILTER](er-functions-list-filter.md) omdat de opgegeven voorwaarde wordt toegepast op een ER-gegevensbron (Elektronische rapportage) van het type *Recordlijst* die aanwezig is in het geheugen.</span><span class="sxs-lookup"><span data-stu-id="05942-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="05942-116">Als de argumenten die zijn geconfigureerd voor deze functie (`list` en `condition`) toestaan dat deze aanvraag wordt omgezet in de directe SQL-aanroep, wordt een waarschuwingsbericht gegenereerd tijdens het ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="05942-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="05942-117">Dit bericht informeert de gebruiker dat de prestaties kunnen worden verbeterd als de functie [FILTER](er-functions-list-filter.md) wordt gebruikt in plaats van `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="05942-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="05942-118">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="05942-118">Example 1</span></span>

<span data-ttu-id="05942-119">Als **Leverancier** als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, wordt met `WHERE (Vendors, Vendors.VendGroup = "40")` de lijst met leveranciers geretourneerd die behoren tot de leveranciersgroep 40.</span><span class="sxs-lookup"><span data-stu-id="05942-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="05942-120">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="05942-120">Example 2</span></span>

<span data-ttu-id="05942-121">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `WHERE( DS, DS.Value = "B")` een lijst met slechts één record die de tekst **B** in het veld **Waarde** bevat.</span><span class="sxs-lookup"><span data-stu-id="05942-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05942-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="05942-122">Additional resources</span></span>

[<span data-ttu-id="05942-123">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="05942-123">List functions</span></span>](er-functions-category-list.md)
