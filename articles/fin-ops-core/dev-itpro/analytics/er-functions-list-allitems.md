---
title: De ER-functie ALLITEMS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ALLITEMS.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917437"
---
# <span data-ttu-id="a13f3-103"><a name="ALLITEMS">De ER-functie ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="a13f3-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a13f3-104">De functie `ALLITEMS` wordt uitgevoerd als een selectie in het geheugen en geeft als resultaat een nieuwe afgevlakte *recordlijstwaarde* als een lijst met records voor alle artikelen die overeenkomen met het opgegeven pad.</span><span class="sxs-lookup"><span data-stu-id="a13f3-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="a13f3-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a13f3-105">Syntax</span></span>

```
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="a13f3-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a13f3-106">Arguments</span></span>

<span data-ttu-id="a13f3-107">`path`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="a13f3-107">`path`: *Record list*</span></span>

<span data-ttu-id="a13f3-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="a13f3-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a13f3-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a13f3-109">Return values</span></span>

<span data-ttu-id="a13f3-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="a13f3-110">*Record list*</span></span>

<span data-ttu-id="a13f3-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="a13f3-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a13f3-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="a13f3-112">Usage notes</span></span>

<span data-ttu-id="a13f3-113">Het pad moet worden gedefinieerd als een geldig gegevensbronpad van een gegevensbronelement van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="a13f3-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="a13f3-114">Gegevenselementen zoals de padreeks en datum moeten tijdens het ontwerp tot een fout leiden in ER Expression Builder.</span><span class="sxs-lookup"><span data-stu-id="a13f3-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="a13f3-115">We raden u af deze functie te gebruiken voor transactionele gegevensbronnen die een grote hoeveelheid gegevens kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="a13f3-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="a13f3-116">Overweeg in plaats daarvan de functie [ALLTEMSQUERY](er-functions-list-allitemsquery.md) te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a13f3-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="a13f3-117">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="a13f3-117">Example 1</span></span>

<span data-ttu-id="a13f3-118">Als u `SPLIT("abcdef" , 2)` als gegevensbron **DS** invoert, geeft de expressie `COUNT( ALLITEMS (DS))` als resultaat **3**.</span><span class="sxs-lookup"><span data-stu-id="a13f3-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a13f3-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="a13f3-119">Example 2</span></span>

<span data-ttu-id="a13f3-120">Als u **Leverancier** invoert als de gegevensbron van het gegevenstype van *Recordlijst* die naar de toepassingstabel VendTable verwijst, retourneert de expressie `ALLITEMS (Vend.'<Relations'.ContactPerson)` een afgevlakte lijst met records met de tabelstructuur **ContactPerson** die alle contactpersonen bevat. Deze is toegankelijk via de relatie **ContactPerson.ContactForParty == VendTable.Party** en beschikbaar voor alle leveranciers uit de leverancierstabel waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="a13f3-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a13f3-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a13f3-121">Additional resources</span></span>

[<span data-ttu-id="a13f3-122">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="a13f3-122">List functions</span></span>](er-functions-category-list.md)
