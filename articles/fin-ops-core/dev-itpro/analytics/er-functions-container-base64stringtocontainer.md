---
title: ER-functie Base64StringToContainer
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) Base64StringToContainer.
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754369"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="c6f67-103">ER-functie Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="c6f67-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6f67-104">De `BASE64STRINGTOCONTAINER` [functie](er-formula-language.md#functions) converteert de opgegeven invoer van het type *Tekenreeks* naar een gegevensitem van het type *[Container](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="c6f67-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f67-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="c6f67-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="c6f67-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c6f67-106">Arguments</span></span>

<span data-ttu-id="c6f67-107">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c6f67-107">`input`: *String*</span></span>

<span data-ttu-id="c6f67-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="c6f67-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6f67-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c6f67-109">Return values</span></span>

<span data-ttu-id="c6f67-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="c6f67-110">*Container*</span></span>

<span data-ttu-id="c6f67-111">De resulterende binaire waarde in BLOB-indeling (binary large object).</span><span class="sxs-lookup"><span data-stu-id="c6f67-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c6f67-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="c6f67-112">Usage notes</span></span>

<span data-ttu-id="c6f67-113">De uitzondering 'Parameter is niet geldig' wordt gebruikt als de invoertekenreeks geen juiste Base64-groep coderingsschema's voor binair naar tekst levert.</span><span class="sxs-lookup"><span data-stu-id="c6f67-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="c6f67-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c6f67-114">Example</span></span>

<span data-ttu-id="c6f67-115">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="c6f67-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="c6f67-116">De hoofdgegevensbron **DocuTypeGroupEnum** van het type *Dynamics 365 for Operations / Opsomming* dat verwijst naar de **DocuTypeGroup** -toepassingsopsomming</span><span class="sxs-lookup"><span data-stu-id="c6f67-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="c6f67-117">De hoofdgegevensbron **Klant** van het type *Dynamics 365 for Operations / Tabelrecords* dat verwijst naar de **CustTable**-toepassingstabel</span><span class="sxs-lookup"><span data-stu-id="c6f67-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="c6f67-118">De gegevensbron **\#Media** van het type *Berekend veld* dat is geconfigureerd op de volgende manier:</span><span class="sxs-lookup"><span data-stu-id="c6f67-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="c6f67-119">Deze wordt toegevoegd als onderliggende gegevensbron van de **Klant**-gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="c6f67-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="c6f67-120">Deze bevat de expressie `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="c6f67-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="c6f67-121">De gegevensbron **\#MediaAsBase64String** van het type *Berekend veld* dat is geconfigureerd op de volgende manier:</span><span class="sxs-lookup"><span data-stu-id="c6f67-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="c6f67-122">Deze wordt toegevoegd als onderliggende gegevensbron van de **Customer.'\#Media'**-gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="c6f67-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="c6f67-123">Deze bevat de expressie `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="c6f67-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="c6f67-124">De gegevensbron **\#BlobFomBase64** van het type *Berekend veld* dat is geconfigureerd op de volgende manier:</span><span class="sxs-lookup"><span data-stu-id="c6f67-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="c6f67-125">Deze wordt toegevoegd als onderliggende gegevensbron van de **Customer.'\#Media'**-gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="c6f67-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="c6f67-126">Deze bevat de expressie `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="c6f67-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="c6f67-127">In dit voorbeeld codeert de **\#MediaAsBase64String**-gegevensbron de binaire inhoud van de huidige mediabijlage als tekst die staat voor een Base64-groep coderingsschema's voor binair naar tekst.</span><span class="sxs-lookup"><span data-stu-id="c6f67-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="c6f67-128">De **\#BlobFomBase64**-gegevensbron decodeert de Base64-tekenreeks en retourneert een binaire waarde in BLOB-indeling.</span><span class="sxs-lookup"><span data-stu-id="c6f67-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Voorbeeldgegevensbronnen op de modelontwerperpagina ER-model](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="c6f67-130">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c6f67-130">Additional resources</span></span>

[<span data-ttu-id="c6f67-131">Containerfuncties</span><span class="sxs-lookup"><span data-stu-id="c6f67-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]