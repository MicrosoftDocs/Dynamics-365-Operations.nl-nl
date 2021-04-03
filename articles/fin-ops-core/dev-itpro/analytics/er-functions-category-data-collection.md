---
title: Lijst met ER-functies in de gegevensverzamelingscategorie
description: Dit onderwerp biedt informatie over de gegevensverzamelingsfuncties die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba3a1f031a4a98592081b04a4128450aeb8218ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561729"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="1c052-103">Lijst met ER-functies in de gegevensverzamelingscategorie</span><span class="sxs-lookup"><span data-stu-id="1c052-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c052-104">Functies voor het verzamelen van gegevens in ER (Elektronische rapportage) worden gebruikt voor het tellen en optellen van een ER-indeling die wordt uitgevoerd, op basis van gegevens van de uitvoer die al is gegenereerd in **tekst-** of **XML**-indeling.</span><span class="sxs-lookup"><span data-stu-id="1c052-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="1c052-105">Deze benadering wordt gebruikt om de prestaties te verbeteren van een ER-indeling die wordt uitgevoerd, om waarden in te voeren van lopende totalen in gegenereerde documenten en voor andere doeleinden.</span><span class="sxs-lookup"><span data-stu-id="1c052-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="1c052-106">In dit onderwerp vindt u een overzicht van deze functies.</span><span class="sxs-lookup"><span data-stu-id="1c052-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="1c052-107">Lijst met ondersteunde functies</span><span class="sxs-lookup"><span data-stu-id="1c052-107">List of supported functions</span></span>

| <span data-ttu-id="1c052-108">Functie</span><span class="sxs-lookup"><span data-stu-id="1c052-108">Function</span></span> | <span data-ttu-id="1c052-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1c052-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="1c052-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="1c052-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="1c052-111">Deze functie retourneert een waarde van het type *Recordlijst* die de lijst met waarden bevat die zijn geretourneerd door de eigenschap **Sleutelwaarde verzamelde gegevens** van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="1c052-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="1c052-112">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="1c052-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="1c052-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="1c052-114">Deze functie retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="1c052-115">De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="1c052-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="1c052-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="1c052-117">Deze functie retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="1c052-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="1c052-118">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="1c052-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="1c052-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="1c052-120">Deze functie retourneert een *tekenreekswaarde* voor de naam van het element van de huidige ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="1c052-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="1c052-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="1c052-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="1c052-122">Deze functie retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en die voldoen aan de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="1c052-123">De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="1c052-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="1c052-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="1c052-125">Deze functie retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="1c052-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="1c052-126">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="1c052-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="1c052-127">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1c052-127">Additional resources</span></span>

[<span data-ttu-id="1c052-128">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1c052-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="1c052-129">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="1c052-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="1c052-130">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1c052-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]