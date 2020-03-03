---
title: De ER-functie QRCODE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916747"
---
# <span data-ttu-id="f4ceb-103"><a name="QRCODE">De ER-functie QRCODE</a></span><span class="sxs-lookup"><span data-stu-id="f4ceb-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4ceb-104">De functie `QRCODE` retourneert een waarde van het type *Container* die de afbeelding met de QR-code (Quick Response) voor de opgegeven tekenreeks in binaire indeling weergeeft.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ceb-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="f4ceb-105">Syntax</span></span>

```
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="f4ceb-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="f4ceb-106">Arguments</span></span>

<span data-ttu-id="f4ceb-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f4ceb-107">`text`: *String*</span></span>

<span data-ttu-id="f4ceb-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4ceb-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="f4ceb-109">Return values</span></span>

<span data-ttu-id="f4ceb-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="f4ceb-110">*Container*</span></span>

<span data-ttu-id="f4ceb-111">De resulterende binaire stroom.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="f4ceb-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f4ceb-112">Example</span></span>

<span data-ttu-id="f4ceb-113">U een ER-indeling (Elektronische rapportage) configureren om een uitgaand document in Microsoft Office-indeling (Excel-werkmappen of Word-documenten) te genereren op basis van een vooraf gedefinieerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="f4ceb-114">Deze sjabloon kan een object **Afbeelding** (Excel-werkmap) of een **Inhoudsbesturingselement voor afbeeldingen** (Word-document) bevatten als tijdelijke aanduiding voor een afbeelding met een QR-code.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="f4ceb-115">U moet aan de geconfigureerde ER-indeling een element **Cel** toevoegen dat wordt gebruikt om deze tijdelijke aanduiding in te vullen.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="f4ceb-116">Als u wilt opgeven welke gegevens worden opgeslagen in een QR-code, moet u een binding definiëren voor dit element **Cel**.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="f4ceb-117">U een kunt een dergelijke binding bijvoorbeeld configureren met de volgende expressie:</span><span class="sxs-lookup"><span data-stu-id="f4ceb-117">For example, you can configure such binding as containing the following expression:</span></span>

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="f4ceb-118">Wanneer u de geconfigureerde ER-indeling uitvoert, wordt de tekstwaarde van het veld **LabelText** van de gegevensbron **model.ListOfShelfLabels** gebruikt om een afbeelding met een QR-code te genereren.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="f4ceb-119">Deze afbeelding vervangt een tijdelijke plaatsaanduiding voor een afbeelding met een QR-code in de documentsjabloon met behulp waarvan een uitgaand document wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="f4ceb-120">Wanneer deze afbeelding van het gegenereerde document wordt gescand, wordt de tekst geretourneerd die is opgehaald uit het veld **LabelText** van de gegevensbron **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="f4ceb-121">Zie [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f4ceb-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4ceb-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f4ceb-122">Additional resources</span></span>

[<span data-ttu-id="f4ceb-123">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="f4ceb-123">Text functions</span></span>](er-functions-category-text.md)