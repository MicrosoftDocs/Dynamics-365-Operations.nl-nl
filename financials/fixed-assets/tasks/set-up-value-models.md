--- 
title: Boeken instellen
description: In deze procedure ziet u hoe u een nieuw vaste-activaboek maakt en deze koppelt aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a29cae6cdcd03903359a3a468243c6ad03c7adc6
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-books"></a><span data-ttu-id="9dc70-103">Boeken instellen</span><span class="sxs-lookup"><span data-stu-id="9dc70-103">Set up books</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9dc70-104">In deze procedure ziet u hoe u een nieuw vaste-activaboek maakt en deze koppelt aan een vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="9dc70-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="9dc70-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="9dc70-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="9dc70-106">Een boek maken</span><span class="sxs-lookup"><span data-stu-id="9dc70-106">Create a book</span></span>
1. <span data-ttu-id="9dc70-107">Ga naar Vaste activa > Instellen > Boeken.</span><span class="sxs-lookup"><span data-stu-id="9dc70-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="9dc70-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9dc70-108">Click New.</span></span>
3. <span data-ttu-id="9dc70-109">Typ een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="9dc70-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="9dc70-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9dc70-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9dc70-111">Als Afschrijving berekenen is geselecteerd, wordt het gekoppelde activumboek in afschrijvingsvoorstellen opgenomen.</span><span class="sxs-lookup"><span data-stu-id="9dc70-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="9dc70-112">Als dit niet is geselecteerd, wordt het activumboek niet automatisch afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="9dc70-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="9dc70-113">Selecteer Ja in het veld Afschrijving berekenen.</span><span class="sxs-lookup"><span data-stu-id="9dc70-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="9dc70-114">Typ of selecteer een waarde in het veld Afschrijvingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="9dc70-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="9dc70-115">Een alternatief afschrijvingsprofiel is ook bekend als overschakelingsmethode voor afschrijving.</span><span class="sxs-lookup"><span data-stu-id="9dc70-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="9dc70-116">Het afschrijvingsvoorstel schakelt over op dit profiel wanneer het alternatieve profiel een afschrijvingsbedrag berekent dat groter of gelijk is als het standaardafschrijvingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="9dc70-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="9dc70-117">Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="9dc70-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="9dc70-118">U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.</span><span class="sxs-lookup"><span data-stu-id="9dc70-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="9dc70-119">Wanneer Afschrijvingscorrecties met basiscorrecties maken is geselecteerd, worden afschrijvingscorrecties automatisch gemaakt wanneer de waarde van het activum wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="9dc70-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="9dc70-120">Als het niet is geselecteerd, beïnvloedt de bijgewerkte activumwaarde alleen nieuwe afschrijvingsberekeningen.</span><span class="sxs-lookup"><span data-stu-id="9dc70-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="9dc70-121">Selecteer in het veld Afschrijvingscorrecties met basiscorrecties maken de waarde Ja.</span><span class="sxs-lookup"><span data-stu-id="9dc70-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="9dc70-122">Standaard worden transacties in het vaste-activaboek naar het grootboek geboekt.</span><span class="sxs-lookup"><span data-stu-id="9dc70-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="9dc70-123">U kunt het boeken naar het algemene grootboek voor het boek uitschakelen door het veld Boeken naar grootboek in te stellen op nee.</span><span class="sxs-lookup"><span data-stu-id="9dc70-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="9dc70-124">De boeken die niet naar het grootboek boeken, worden doorgaans gebruikt voor belastingaangiftes.</span><span class="sxs-lookup"><span data-stu-id="9dc70-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="9dc70-125">Dit geeft u meer flexibiliteit om historische transacties voor het activumboek te verwijderen, omdat ze niet in het grootboek zijn bevestigd.</span><span class="sxs-lookup"><span data-stu-id="9dc70-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="9dc70-126">De Boekingslaag heeft standaard de waarde Huidige laag, als het boek in het algemene grootboek boekt, en de waarde Geen als het boek niet naar het grootboek boekt.</span><span class="sxs-lookup"><span data-stu-id="9dc70-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="9dc70-127">Werk de Boekingslaag bij als u transacties voor dit boek naar een andere laag wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="9dc70-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="9dc70-128">Typ of selecteer een waarde in het veld Kalender.</span><span class="sxs-lookup"><span data-stu-id="9dc70-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="9dc70-129">Aafgeleide boeken boeken transacties naar verschillende boeken tegelijk.</span><span class="sxs-lookup"><span data-stu-id="9dc70-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="9dc70-130">U maakt de transacties met het primaire boek. Tijdens het boeken wordt een exacte kopie van de transactie geboekt naar het afgeleide boek.</span><span class="sxs-lookup"><span data-stu-id="9dc70-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="9dc70-131">Omdat er geen herberekening met afgeleide boektransacties is, moet deze niet voor afschrijvingstransacties moeten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9dc70-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="9dc70-132">Het boek aan een vaste-activagroep koppelen</span><span class="sxs-lookup"><span data-stu-id="9dc70-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="9dc70-133">Klik op Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="9dc70-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="9dc70-134">Typ of selecteer een waarde in het veld Groep vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9dc70-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="9dc70-135">Voer een getal in het veld Levensduur in.</span><span class="sxs-lookup"><span data-stu-id="9dc70-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="9dc70-136">Merk op dat de waarde in Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9dc70-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="9dc70-137">U kunt de afschrijvingsconventie instellen al naar gelang de belastingvereisten.</span><span class="sxs-lookup"><span data-stu-id="9dc70-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


