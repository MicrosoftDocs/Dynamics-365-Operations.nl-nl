---
title: De ER-functie GUIDVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GUIDVALUE.
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746382"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="17572-103">De ER-functie GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="17572-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17572-104">De functie `GUIDVALUE` converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *GUID*.</span><span class="sxs-lookup"><span data-stu-id="17572-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="17572-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="17572-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="17572-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="17572-106">Arguments</span></span>

<span data-ttu-id="17572-107">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="17572-107">`input`: *String*</span></span>

<span data-ttu-id="17572-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="17572-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="17572-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="17572-109">Return values</span></span>

<span data-ttu-id="17572-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="17572-110">*GUID*</span></span>

<span data-ttu-id="17572-111">De resulterende GUID-waarde (Globally Unique Identifier).</span><span class="sxs-lookup"><span data-stu-id="17572-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17572-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="17572-112">Usage notes</span></span>

<span data-ttu-id="17572-113">Als u een conversie in de tegenovergestelde richting wilt uitvoeren (dat wil zeggen: opgegeven invoer van het gegevenstype *GUID* converteren naar een gegevensitem van het gegevenstype *Tekenreeks*), kunt u de functie [TEXT](er-functions-text-text.md) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="17572-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="17572-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="17572-114">Example</span></span>

<span data-ttu-id="17572-115">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="17572-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="17572-116">Een gegevensbron **myID** van het type *Berekend veld* die de expressie `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` bevat</span><span class="sxs-lookup"><span data-stu-id="17572-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="17572-117">Een gegevensbron **Gebruikers** van het type *Tabelrecords* die verwijst naar de tabel UserInfo</span><span class="sxs-lookup"><span data-stu-id="17572-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="17572-118">Vervolgens kunt u een expressie, zoals `FILTER (Users, Users.objectId = myID)`, gebruiken om de tabel UserInfo te filteren op het veld **objectId** van het gegevenstype *GUID*.</span><span class="sxs-lookup"><span data-stu-id="17572-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17572-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="17572-119">Additional resources</span></span>

[<span data-ttu-id="17572-120">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="17572-120">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]