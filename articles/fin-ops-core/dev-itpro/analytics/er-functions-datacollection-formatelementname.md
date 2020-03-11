---
title: De ER-functie FORMATELEMENTNAME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FORMATELEMENTNAME.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5f299a4bb697afce152a61ec35fcefab7157f356
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042522"
---
# <span data-ttu-id="5d020-103"><a name="FORMATELEMENTNAME">De ER-functie FORMATELEMENTNAME</a></span><span class="sxs-lookup"><span data-stu-id="5d020-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d020-104">De functie `FORMATELEMENTNAME` retourneert een *tekenreekswaarde* voor de naam van het element van de huidige ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="5d020-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d020-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="5d020-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="5d020-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="5d020-106">Return values</span></span>

<span data-ttu-id="5d020-107">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="5d020-107">*String*</span></span>

<span data-ttu-id="5d020-108">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="5d020-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5d020-109">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="5d020-109">Usage notes</span></span>

<span data-ttu-id="5d020-110">Deze functie kan worden aangeroepen in ER-expressies die zijn geconfigureerd voor de eigenschappen **Sleutelnaam verzamelde gegevens** en **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel uit de groep **Tekst** onder onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5d020-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="5d020-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5d020-111">Example</span></span>

<span data-ttu-id="5d020-112">Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.</span><span class="sxs-lookup"><span data-stu-id="5d020-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d020-113">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5d020-113">Additional resources</span></span>

[<span data-ttu-id="5d020-114">Functies voor gegevensverzameling</span><span class="sxs-lookup"><span data-stu-id="5d020-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
