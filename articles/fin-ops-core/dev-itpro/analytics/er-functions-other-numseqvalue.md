---
title: De ER-functie NUMSEQVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMSEQVALUE.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c3351360d0c1afca9f828ba4fc935096ddfd67f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743998"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="40cd3-103">De ER-functie NUMSEQVALUE</span><span class="sxs-lookup"><span data-stu-id="40cd3-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40cd3-104">De functie `NUMSEQVALUE` retourneert een *tekenreekswaarde* die voor de nieuwe gegenereerde waarde van een nummerreeks staat, op basis van de opgegeven nummerreeks, het bereik en de bereik-id.</span><span class="sxs-lookup"><span data-stu-id="40cd3-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="40cd3-105">De bereik-id is gelijk aan de bedrijfscode die wordt geleverd door de context waarin de ER-indeling (Elektronische rapportage) wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40cd3-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="40cd3-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="40cd3-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="40cd3-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="40cd3-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="40cd3-108">Syntaxis 3</span><span class="sxs-lookup"><span data-stu-id="40cd3-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="40cd3-109">Argumenten</span><span class="sxs-lookup"><span data-stu-id="40cd3-109">Arguments</span></span>

<span data-ttu-id="40cd3-110">`number sequence code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40cd3-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="40cd3-111">Een tekstwaarde die staat voor de code van de nummerreeks waarin een nieuwe waarde vereist is.</span><span class="sxs-lookup"><span data-stu-id="40cd3-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="40cd3-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="40cd3-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="40cd3-113">Een *Int64-waarde* die de record-id vertegenwoordigt van een record in de tabel NumberSequenceTable die de definitie bevat van de nummerreeks waarin een nieuwe waarde vereist is.</span><span class="sxs-lookup"><span data-stu-id="40cd3-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="40cd3-114">`scope type`: *Opsommingswaarde*</span><span class="sxs-lookup"><span data-stu-id="40cd3-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="40cd3-115">Een opsommingswaarde van de opsomming **ERExpressionNumberSequenceScopeType** die het bereik van de nummerreeks definieert waarin een nieuwe waarde vereist is.</span><span class="sxs-lookup"><span data-stu-id="40cd3-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="40cd3-116">De beschikbare bereiktypen zijn **Gedeeld**, **Rechtspersoon** en **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="40cd3-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="40cd3-117">`scope ID`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40cd3-117">`scope ID`: *String*</span></span>

<span data-ttu-id="40cd3-118">Een *tekenreekswaarde* die de scope identificeert op basis van het opgegeven bereiktype.</span><span class="sxs-lookup"><span data-stu-id="40cd3-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="40cd3-119">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="40cd3-119">Return values</span></span>

<span data-ttu-id="40cd3-120">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40cd3-120">*String*</span></span>

<span data-ttu-id="40cd3-121">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="40cd3-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="40cd3-122">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="40cd3-122">Usage notes</span></span>

<span data-ttu-id="40cd3-123">Geef voor het bereiktype **Gedeeld** een lege tekenreeks als de bereik-id op.</span><span class="sxs-lookup"><span data-stu-id="40cd3-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="40cd3-124">Geef voor de bereiktypen **Bedrijf** en **Rechtspersoon** de bedrijfscode op als de bereik-id.</span><span class="sxs-lookup"><span data-stu-id="40cd3-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="40cd3-125">Als u voor deze bereiktypen een lege tekenreeks opgeeft als de bereik-id, wordt de huidige bedrijfscode gebruikt.</span><span class="sxs-lookup"><span data-stu-id="40cd3-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="40cd3-126">Wanneer u syntaxis 1 gebruikt, wordt de nummerreeks aangevraagd voor het bereiktype **Bedrijf** en wordt de bedrijfscode geleverd door de context waarin de ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40cd3-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="40cd3-127">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="40cd3-127">Example 1</span></span>

<span data-ttu-id="40cd3-128">In de ER-indeling definieert u de gegevensbron **AskNumSeq** van het type *Gebruikersinvoerparameter*.</span><span class="sxs-lookup"><span data-stu-id="40cd3-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="40cd3-129">Deze gegevensbron verwijst naar het uitgebreide-gegevenstype **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="40cd3-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="40cd3-130">Vervolgens definieert u de gegevensbron **NumSeq** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="40cd3-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="40cd3-131">Deze gegevensbron bevat de expressie `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="40cd3-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="40cd3-132">Wanneer de gegevensbron **NumSeq** wordt aangeroepen, wordt de nieuwe gegenereerde waarde gegenereerd van de nummerreeks die tijdens runtime was opgegeven,door de code in te voeren in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="40cd3-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="40cd3-133">De nummerreeks wordt aangevraagd voor het bereiktype **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="40cd3-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="40cd3-134">De bedrijfscode wordt geleverd door de context waarin de ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40cd3-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="40cd3-135">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="40cd3-135">Example 2</span></span>

<span data-ttu-id="40cd3-136">De volgende gegevensbronnen worden gedefinieerd in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="40cd3-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="40cd3-137">De gegevensbron **LedgerParms** van het type *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="40cd3-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="40cd3-138">Deze gegevensbron verwijst naar de tabel LedgerParameters.</span><span class="sxs-lookup"><span data-stu-id="40cd3-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="40cd3-139">De gegevensbron **NumSeq** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="40cd3-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="40cd3-140">Deze gegevensbron bevat de expressie `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="40cd3-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="40cd3-141">Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks die is geconfigureerd in de grootboekparameters voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40cd3-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="40cd3-142">Deze getalreeks vormt een unieke identificatie van journalen en fungeert als batchnummer dat de transacties aan elkaar koppelt.</span><span class="sxs-lookup"><span data-stu-id="40cd3-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="40cd3-143">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="40cd3-143">Example 3</span></span>

<span data-ttu-id="40cd3-144">De volgende gegevensbronnen worden gedefinieerd in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="40cd3-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="40cd3-145">De gegevensbron **enumScope** van het Microsoft Dynamics 365 Finance-type *opsomming*.</span><span class="sxs-lookup"><span data-stu-id="40cd3-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="40cd3-146">Deze gegevensbron verwijst naar de opsomming **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="40cd3-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="40cd3-147">De gegevensbron **NumSeq** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="40cd3-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="40cd3-148">Deze gegevensbron bevat de expressie `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="40cd3-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="40cd3-149">Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks **Gene\_1**, die is geconfigureerd voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40cd3-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40cd3-150">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="40cd3-150">Additional resources</span></span>

[<span data-ttu-id="40cd3-151">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="40cd3-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]