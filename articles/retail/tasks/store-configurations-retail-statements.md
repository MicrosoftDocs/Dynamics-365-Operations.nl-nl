--- 
title: " Winkelconfiguraties voor detailhandeloverzichten"
description: Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d28e9cd63277a3a0c8dc0bce61177d7f7ae9c1ab
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="15d8f-103"> Winkelconfiguraties voor detailhandeloverzichten</span><span class="sxs-lookup"><span data-stu-id="15d8f-103">Store configurations for Retail statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="15d8f-104">Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="15d8f-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="15d8f-105">Financiële dimensies voor detailhandelwinkels worden in een andere procedure behandeld.</span><span class="sxs-lookup"><span data-stu-id="15d8f-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="15d8f-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="15d8f-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="15d8f-107">Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.</span><span class="sxs-lookup"><span data-stu-id="15d8f-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="15d8f-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="15d8f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="15d8f-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="15d8f-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="15d8f-110">De instellingen in de sectie Overzicht/afsluiting zijn van invloed op het maken, valideren en boeken van overzichten voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="15d8f-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="15d8f-111">Open de sectie Overzicht/afsluiting.</span><span class="sxs-lookup"><span data-stu-id="15d8f-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="15d8f-112">Selecteer de gewenste methode om de overzichtsregels op te groeperen.</span><span class="sxs-lookup"><span data-stu-id="15d8f-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="15d8f-113">Selecteer 'Ja' als er slechts één overzicht per dag moet worden gemaakt wanneer overzichten worden gemaakt vanuit de batchtaak voor het maken van overzichten.</span><span class="sxs-lookup"><span data-stu-id="15d8f-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="15d8f-114">Het veld Berekening kascontrole definieert of kascontroles moeten worden opgeteld of dat de laatste moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="15d8f-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="15d8f-115">Selecteer de grootboekrekening om afrondingsverschillen naar te boeken.</span><span class="sxs-lookup"><span data-stu-id="15d8f-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="15d8f-116">In het veld Maximaal afrondingsbedrag kunt u het maximaal toegestane afrondingsverschil invoeren.</span><span class="sxs-lookup"><span data-stu-id="15d8f-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="15d8f-117">In het veld Boeking kunt u het maximale boekingsverschil invoeren dat toegestaan is voor een overzicht.</span><span class="sxs-lookup"><span data-stu-id="15d8f-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="15d8f-118">In het veld Ploeg kunt u het maximaal toegestane totale verschil binnen een ploeg in een overzicht invoeren.</span><span class="sxs-lookup"><span data-stu-id="15d8f-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="15d8f-119">In het veld Transactie kunt u het maximaal toegestane totale verschil op een overzichtsregel invoeren.</span><span class="sxs-lookup"><span data-stu-id="15d8f-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="15d8f-120">In het veld Afsluitingsmethode kunt u definiëren of transacties die in een overzicht worden opgenomen, deel moeten uitmaken van een gesloten ploeg of dat het transacties kunnen zijn binnen het gedefinieerde datum/tijd-bereik.</span><span class="sxs-lookup"><span data-stu-id="15d8f-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="15d8f-121">In het veld Einde van werkdag kunt u een tijd invoeren als transacties die na middernacht plaatsvinden, op de vorige dag moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="15d8f-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="15d8f-122">Selecteer 'Ja' als transacties die na middernacht plaatsvinden, als onderdeel van de vorige dag moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="15d8f-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="15d8f-123">Selecteer 'Ja' om overzichten te laten maken voor elke gedefinieerde overzichtsmethode.</span><span class="sxs-lookup"><span data-stu-id="15d8f-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="15d8f-124">Dat kan nuttig zijn als de prestaties van de boeking moeten worden verbeterd voor winkels met grote transactievolumes, aangezien er veel kleinere overzichten worden gemaakt die parallel kunnen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="15d8f-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="15d8f-125">In het veld Standaardklant kunt u de klantrekening selecteren om te gebruiken voor verkoop aan inloopklanten.</span><span class="sxs-lookup"><span data-stu-id="15d8f-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


