---
title: Lijst met ER-functies in de gegevensverzamelingscategorie
description: Dit onderwerp biedt informatie over de gegevensverzamelingsfuncties die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686288"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="2b239-103">Lijst met ER-functies in de gegevensverzamelingscategorie</span><span class="sxs-lookup"><span data-stu-id="2b239-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b239-104">Functies voor het verzamelen van gegevens in ER (Elektronische rapportage) worden gebruikt voor het tellen en optellen van een ER-indeling die wordt uitgevoerd, op basis van gegevens van de uitvoer die al is gegenereerd in **tekst-** of **XML**-indeling.</span><span class="sxs-lookup"><span data-stu-id="2b239-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="2b239-105">Deze benadering wordt gebruikt om de prestaties te verbeteren van een ER-indeling die wordt uitgevoerd, om waarden in te voeren van lopende totalen in gegenereerde documenten en voor andere doeleinden.</span><span class="sxs-lookup"><span data-stu-id="2b239-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="2b239-106">In dit onderwerp vindt u een overzicht van deze functies.</span><span class="sxs-lookup"><span data-stu-id="2b239-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="2b239-107">Lijst met ondersteunde functies</span><span class="sxs-lookup"><span data-stu-id="2b239-107">List of supported functions</span></span>

| <span data-ttu-id="2b239-108">Functie</span><span class="sxs-lookup"><span data-stu-id="2b239-108">Function</span></span> | <span data-ttu-id="2b239-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2b239-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2b239-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="2b239-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="2b239-111">Deze functie retourneert een waarde van het type *Recordlijst* die de lijst met waarden bevat die zijn geretourneerd door de eigenschap **Sleutelwaarde verzamelde gegevens** van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="2b239-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="2b239-112">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="2b239-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="2b239-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="2b239-114">Deze functie retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="2b239-115">De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="2b239-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="2b239-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="2b239-117">Deze functie retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="2b239-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="2b239-118">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="2b239-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="2b239-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="2b239-120">Deze functie retourneert een *tekenreekswaarde* voor de naam van het element van de huidige ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="2b239-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="2b239-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="2b239-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="2b239-122">Deze functie retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en die voldoen aan de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="2b239-123">De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="2b239-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="2b239-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="2b239-125">Deze functie retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="2b239-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="2b239-126">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="2b239-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2b239-127">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2b239-127">Additional resources</span></span>

[<span data-ttu-id="2b239-128">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="2b239-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2b239-129">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="2b239-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="2b239-130">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="2b239-130">Electronic reporting formula language</span></span>](er-formula-language.md)
