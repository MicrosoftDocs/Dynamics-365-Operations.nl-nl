---
title: Afschrijvingsboeken instellen
description: In deze procedure doorloopt u het proces voor het maken van een nieuw afschrijvingsboek en leest u hoe u dit koppelt aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd65cb77872b3e2f74402cf8c92c8b8989cea6ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224688"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="ec356-103">Afschrijvingsboeken instellen</span><span class="sxs-lookup"><span data-stu-id="ec356-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec356-104">In deze procedure doorloopt u het proces voor het maken van een nieuw afschrijvingsboek en leest u hoe u dit koppelt aan een vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="ec356-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="ec356-105">Maak een afschrijvingsboek</span><span class="sxs-lookup"><span data-stu-id="ec356-105">Create a depreciation book</span></span>
1. <span data-ttu-id="ec356-106">Ga naar Vaste activa > Instellingen > Afschrijvingsboeken.</span><span class="sxs-lookup"><span data-stu-id="ec356-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="ec356-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ec356-107">Click New.</span></span>
3. <span data-ttu-id="ec356-108">Typ een waarde in het veld Afschrijvingsboek.</span><span class="sxs-lookup"><span data-stu-id="ec356-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="ec356-109">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="ec356-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec356-110">Schakel het selectievakje Afschrijving berekenen in of uit.</span><span class="sxs-lookup"><span data-stu-id="ec356-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="ec356-111">Klik in het veld Afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec356-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ec356-112">Zoek en selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec356-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="ec356-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ec356-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ec356-114">Klik in het veld Alternatief afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec356-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ec356-115">Selecteer het gewenste afschrijvingsprofiel in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec356-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="ec356-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ec356-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ec356-117">Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="ec356-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="ec356-118">U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.</span><span class="sxs-lookup"><span data-stu-id="ec356-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="ec356-119">Schakel het selectievakje Afschrijvingscorrecties met basiscorrecties maken in of uit.</span><span class="sxs-lookup"><span data-stu-id="ec356-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="ec356-120">Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec356-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="ec356-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ec356-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="ec356-122">Afschrijvingsboeken aan vaste-activagroepen koppelen</span><span class="sxs-lookup"><span data-stu-id="ec356-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="ec356-123">Klik op Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="ec356-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="ec356-124">Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec356-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ec356-125">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec356-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ec356-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ec356-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ec356-127">Selecteer in het veld Afschrijvingsconventie een optie.</span><span class="sxs-lookup"><span data-stu-id="ec356-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="ec356-128">Voer een getal in het veld Levensduur in.</span><span class="sxs-lookup"><span data-stu-id="ec356-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="ec356-129">Merk op dat de waarde van het veld Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ec356-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]