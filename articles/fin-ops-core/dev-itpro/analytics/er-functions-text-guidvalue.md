---
title: De ER-functie GUIDVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GUIDVALUE.
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041156"
---
# <span data-ttu-id="fb736-103"><a name="GUIDVALUE">De ER-functie GUIDVALUE</a></span><span class="sxs-lookup"><span data-stu-id="fb736-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb736-104">De functie `GUIDVALUE` converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *GUID*.</span><span class="sxs-lookup"><span data-stu-id="fb736-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb736-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="fb736-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="fb736-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="fb736-106">Arguments</span></span>

<span data-ttu-id="fb736-107">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="fb736-107">`input`: *String*</span></span>

<span data-ttu-id="fb736-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="fb736-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb736-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="fb736-109">Return values</span></span>

<span data-ttu-id="fb736-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="fb736-110">*GUID*</span></span>

<span data-ttu-id="fb736-111">De resulterende GUID-waarde (Globally Unique Identifier).</span><span class="sxs-lookup"><span data-stu-id="fb736-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fb736-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="fb736-112">Usage notes</span></span>

<span data-ttu-id="fb736-113">Als u een conversie in de tegenovergestelde richting wilt uitvoeren (dat wil zeggen: opgegeven invoer van het gegevenstype *GUID* converteren naar een gegevensitem van het gegevenstype *Tekenreeks*), kunt u de functie [TEXT](er-functions-text-text.md) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fb736-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="fb736-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fb736-114">Example</span></span>

<span data-ttu-id="fb736-115">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="fb736-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="fb736-116">Een gegevensbron **myID** van het type *Berekend veld* die de expressie `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` bevat</span><span class="sxs-lookup"><span data-stu-id="fb736-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="fb736-117">Een gegevensbron **Gebruikers** van het type *Tabelrecords* die verwijst naar de tabel UserInfo</span><span class="sxs-lookup"><span data-stu-id="fb736-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="fb736-118">Vervolgens kunt u een expressie, zoals `FILTER (Users, Users.objectId = myID)`, gebruiken om de tabel UserInfo te filteren op het veld **objectId** van het gegevenstype *GUID*.</span><span class="sxs-lookup"><span data-stu-id="fb736-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb736-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fb736-119">Additional resources</span></span>

[<span data-ttu-id="fb736-120">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="fb736-120">Text functions</span></span>](er-functions-category-text.md)
