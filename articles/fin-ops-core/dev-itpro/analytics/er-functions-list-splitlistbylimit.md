---
title: De ER-functie SPLITLISTBYLIMIT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLITLISTBYLIMIT.
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743420"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="26793-103">De ER-functie SPLITLISTBYLIMIT</span><span class="sxs-lookup"><span data-stu-id="26793-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26793-104">Met de functie `SPLITLISTBYLIMIT` wordt de opgegeven lijst gesplitst in een nieuwe lijst met sublijsten (batches).</span><span class="sxs-lookup"><span data-stu-id="26793-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="26793-105">Het aantal records in elke batch wordt dynamisch berekend.</span><span class="sxs-lookup"><span data-stu-id="26793-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="26793-106">De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat.</span><span class="sxs-lookup"><span data-stu-id="26793-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="26793-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="26793-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="26793-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="26793-108">Arguments</span></span>

<span data-ttu-id="26793-109">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="26793-109">`list`: *Record list*</span></span>

<span data-ttu-id="26793-110">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="26793-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="26793-111">`limit value`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="26793-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="26793-112">De maximumwaarde van de limiet die wordt gebruikt om de oorspronkelijke lijst in batches te splitsen.</span><span class="sxs-lookup"><span data-stu-id="26793-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="26793-113">`limit source`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="26793-113">`limit source`: *Field*</span></span>

<span data-ttu-id="26793-114">Het geldige pad van een veld van het type *Geheel getal* of *Werkelijk* in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="26793-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="26793-115">De waarde van dit veld bepaalt de stap waarvoor de totale som wordt verhoogd.</span><span class="sxs-lookup"><span data-stu-id="26793-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="26793-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="26793-116">Return values</span></span>

<span data-ttu-id="26793-117">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="26793-117">*Record list*</span></span>

<span data-ttu-id="26793-118">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="26793-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26793-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="26793-119">Usage notes</span></span>

<span data-ttu-id="26793-120">De geretourneerde lijst batches bevat de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="26793-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="26793-121">**Waarde**: *Lijst*</span><span class="sxs-lookup"><span data-stu-id="26793-121">**Value**: *List*</span></span>

    <span data-ttu-id="26793-122">De lijst met records die deel uitmaken van de huidige batch.</span><span class="sxs-lookup"><span data-stu-id="26793-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="26793-123">**BatchNumber**: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="26793-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="26793-124">Het nummer van de huidige batch in de geretourneerde lijst.</span><span class="sxs-lookup"><span data-stu-id="26793-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="26793-125">De limiet wordt niet toegepast op één artikel van de oorspronkelijke lijst als de limietbron de gedefinieerde limiet overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="26793-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="26793-126">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="26793-126">Example</span></span>

<span data-ttu-id="26793-127">In de volgende afbeelding ziet u een ER-indeling (Elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="26793-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="26793-128">In de volgende afbeelding ziet u de gegevensbronnen die voor de indeling worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="26793-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="26793-129">In de volgende afbeelding ziet u het resultaat wanneer de indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="26793-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="26793-130">In dit geval is de uitvoer een platte lijst met basisproducten.</span><span class="sxs-lookup"><span data-stu-id="26793-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="26793-131">De volgende voorbeelden laten dezelfde indeling zien die is aangepast om de lijst met basisproducten in batches weer te geven als één batch basisproducten moet omvatten en het totale gewicht niet groter mag zijn dan 9.</span><span class="sxs-lookup"><span data-stu-id="26793-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="26793-132">In de volgende afbeelding ziet u het resultaat wanneer de aangepaste indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="26793-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="26793-133">De limiet wordt niet toegepast op het laatste artikel van de oorspronkelijke lijst omdat de waarde (**11**) van de limietbron (**gewicht**) de gedefinieerde limiet (**9**) overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="26793-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="26793-134">Als u sublijsten wilt negeren tijdens het genereren van rapporten, gebruikt u de functie `WHERE` of de expressie **Ingeschakeld** van het bijbehorende indelingselement.</span><span class="sxs-lookup"><span data-stu-id="26793-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26793-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="26793-135">Additional resources</span></span>

[<span data-ttu-id="26793-136">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="26793-136">List functions</span></span>](er-functions-category-list.md)
