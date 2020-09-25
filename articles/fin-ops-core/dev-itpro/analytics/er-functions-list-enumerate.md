---
title: De ER-functie ENUMERATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ENUMERATE.
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
ms.openlocfilehash: e1871ee41267c2c0e8b35007a47c9601079f05d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745244"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="16736-103">De ER-functie ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="16736-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16736-104">De functie `ENUMERATE` retourneert een nieuwe waarde van het type *Recordlijst* die bestaat uit opgesomde records van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="16736-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="16736-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="16736-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="16736-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="16736-106">Arguments</span></span>

<span data-ttu-id="16736-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="16736-107">`list`: *Record list*</span></span>

<span data-ttu-id="16736-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="16736-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="16736-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="16736-109">Return values</span></span>

<span data-ttu-id="16736-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="16736-110">*Record list*</span></span>

<span data-ttu-id="16736-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="16736-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="16736-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="16736-112">Usage notes</span></span>

<span data-ttu-id="16736-113">De geretourneerde lijst opgesomde records bevat de volgende extra elementen:</span><span class="sxs-lookup"><span data-stu-id="16736-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="16736-114">De record van velden (onderdeel **Waarde**)</span><span class="sxs-lookup"><span data-stu-id="16736-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="16736-115">De huidige recordindex (onderdeel **Nummer**)</span><span class="sxs-lookup"><span data-stu-id="16736-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="16736-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="16736-116">Example</span></span>

<span data-ttu-id="16736-117">In het volgende voorbeeld wordt de gegevensbron **Genummerd** gemaakt als een genummerde lijst leveranciersrecords van de gegevensbron **Leveranciers** die verwijst naar de tabel VendTable.</span><span class="sxs-lookup"><span data-stu-id="16736-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="16736-118">In de volgende afbeelding ziet u de ER-indeling (Elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="16736-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="16736-119">In deze indeling worden gegevensbindingen gemaakt om uitvoer in XML-indeling te genereren.</span><span class="sxs-lookup"><span data-stu-id="16736-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="16736-120">Deze uitvoer presenteert afzonderlijke leveranciers als opgesomde knooppunten.</span><span class="sxs-lookup"><span data-stu-id="16736-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="16736-121">In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="16736-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="16736-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="16736-122">Additional resources</span></span>

[<span data-ttu-id="16736-123">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="16736-123">List functions</span></span>](er-functions-category-list.md)
