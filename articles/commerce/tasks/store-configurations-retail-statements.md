---
title: Winkelconfiguraties voor detailhandeloverzichten
description: Deze procedure doorloopt winkelconfiguraties die van invloed zijn op hoe Commerce-overzichten worden gemaakt en geboekt.
author: jashanno
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da862af25df241ad42b7e1ade3fdca19f6280278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804108"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="59404-103">Winkelconfiguraties voor detailhandeloverzichten</span><span class="sxs-lookup"><span data-stu-id="59404-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59404-104">Deze procedure doorloopt winkelconfiguraties die van invloed zijn op hoe Commerce-overzichten worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="59404-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="59404-105">Financiële dimensies voor winkels worden in een andere procedure behandeld.</span><span class="sxs-lookup"><span data-stu-id="59404-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="59404-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="59404-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="59404-107">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Kanalen > Winkels > Alle detailhandelwinkels**.</span><span class="sxs-lookup"><span data-stu-id="59404-107">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="59404-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="59404-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="59404-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="59404-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="59404-110">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="59404-110">Click **Edit**.</span></span>
5. <span data-ttu-id="59404-111">De instellingen op het sneltabblad **Overzicht/afsluiting** zijn van invloed op het maken, valideren en boeken van overzichten voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="59404-111">The settings in the **Statement/closing** FastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="59404-112">Vouw het sneltabblad **Overzicht/afsluiting** uit.</span><span class="sxs-lookup"><span data-stu-id="59404-112">Expand the **Statement/closing** FastTab.</span></span>  
6. <span data-ttu-id="59404-113">Selecteer de gewenste methode waarmee u de overzichtsregels wilt groeperen in het veld **Overzichtsmethode**.</span><span class="sxs-lookup"><span data-stu-id="59404-113">In the **Statement method** field, select the method you want to use to group the statement lines by.</span></span>  
7. <span data-ttu-id="59404-114">Selecteer Ja bij **Eén overzicht per dag** als er slechts één overzicht per dag moet worden gemaakt wanneer overzichten worden gemaakt vanuit de batchtaak voor het maken van overzichten.</span><span class="sxs-lookup"><span data-stu-id="59404-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="59404-115">Het veld **Berekening kascontrole** definieert of kascontroles moeten worden opgeteld of dat de laatste moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="59404-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="59404-116">Selecteer in het veld **Afronding** de grootboekrekening om afrondingsverschillen naar te boeken.</span><span class="sxs-lookup"><span data-stu-id="59404-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="59404-117">In het veld **Maximaal afrondingsbedrag** kunt u het maximaal toegestane afrondingsverschil invoeren.</span><span class="sxs-lookup"><span data-stu-id="59404-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="59404-118">In het veld **Boeking** kunt u het maximale boekingsverschil invoeren dat toegestaan is voor een overzicht.</span><span class="sxs-lookup"><span data-stu-id="59404-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="59404-119">In het veld **Ploeg** kunt u het maximaal toegestane totale verschil binnen een ploeg in een overzicht invoeren.</span><span class="sxs-lookup"><span data-stu-id="59404-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="59404-120">In het veld **Transactie** kunt u het maximaal toegestane totale verschil op een overzichtsregel invoeren.</span><span class="sxs-lookup"><span data-stu-id="59404-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="59404-121">In het veld **Afsluitingsmethode** kunt u definiëren of transacties die in een overzicht worden opgenomen, deel moeten uitmaken van een gesloten ploeg of dat het transacties kunnen zijn binnen het gedefinieerde datum/tijd-bereik.</span><span class="sxs-lookup"><span data-stu-id="59404-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="59404-122">In het veld **Einde van werkdag** voert u een tijd in als transacties die na middernacht plaatsvinden op de vorige dag moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="59404-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="59404-123">Selecteer Ja bij **Als werkdag boeken** als transacties die na middernacht plaatsvinden, als onderdeel van de vorige dag moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="59404-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="59404-124">Selecteer Ja bij **Splitsing per overzichtsmethode** om overzichten te laten maken voor elke gedefinieerde overzichtsmethode.</span><span class="sxs-lookup"><span data-stu-id="59404-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="59404-125">Deze actie kan nuttig zijn als de prestaties van de boeking moeten worden verbeterd voor winkels met grote transactievolumes, aangezien er veel kleinere overzichten worden gemaakt die parallel kunnen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="59404-125">This action can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="59404-126">In het veld **Standaardklant** op het sneltabblad **Algemeen** kunt u de klantrekening selecteren die u wilt gebruiken voor verkoop aan inloopklanten.</span><span class="sxs-lookup"><span data-stu-id="59404-126">In the **General** FastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]