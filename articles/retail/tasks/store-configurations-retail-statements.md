---
title: " Winkelconfiguraties voor detailhandeloverzichten"
description: Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "354708"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="f73a7-103"> Winkelconfiguraties voor detailhandeloverzichten</span><span class="sxs-lookup"><span data-stu-id="f73a7-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f73a7-104">Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="f73a7-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="f73a7-105">Financiële dimensies voor detailhandelwinkels worden in een andere procedure behandeld.</span><span class="sxs-lookup"><span data-stu-id="f73a7-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="f73a7-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="f73a7-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="f73a7-107">Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.</span><span class="sxs-lookup"><span data-stu-id="f73a7-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="f73a7-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f73a7-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f73a7-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f73a7-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f73a7-110">De instellingen in de sectie Overzicht/afsluiting zijn van invloed op het maken, valideren en boeken van overzichten voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="f73a7-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="f73a7-111">Open de sectie Overzicht/afsluiting.</span><span class="sxs-lookup"><span data-stu-id="f73a7-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="f73a7-112">Selecteer de gewenste methode om de overzichtsregels op te groeperen.</span><span class="sxs-lookup"><span data-stu-id="f73a7-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="f73a7-113">Selecteer 'Ja' als er slechts één overzicht per dag moet worden gemaakt wanneer overzichten worden gemaakt vanuit de batchtaak voor het maken van overzichten.</span><span class="sxs-lookup"><span data-stu-id="f73a7-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="f73a7-114">Het veld Berekening kascontrole definieert of kascontroles moeten worden opgeteld of dat de laatste moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f73a7-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="f73a7-115">Selecteer de grootboekrekening om afrondingsverschillen naar te boeken.</span><span class="sxs-lookup"><span data-stu-id="f73a7-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="f73a7-116">In het veld Maximaal afrondingsbedrag kunt u het maximaal toegestane afrondingsverschil invoeren.</span><span class="sxs-lookup"><span data-stu-id="f73a7-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="f73a7-117">In het veld Boeking kunt u het maximale boekingsverschil invoeren dat toegestaan is voor een overzicht.</span><span class="sxs-lookup"><span data-stu-id="f73a7-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="f73a7-118">In het veld Ploeg kunt u het maximaal toegestane totale verschil binnen een ploeg in een overzicht invoeren.</span><span class="sxs-lookup"><span data-stu-id="f73a7-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="f73a7-119">In het veld Transactie kunt u het maximaal toegestane totale verschil op een overzichtsregel invoeren.</span><span class="sxs-lookup"><span data-stu-id="f73a7-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="f73a7-120">In het veld Afsluitingsmethode kunt u definiëren of transacties die in een overzicht worden opgenomen, deel moeten uitmaken van een gesloten ploeg of dat het transacties kunnen zijn binnen het gedefinieerde datum/tijd-bereik.</span><span class="sxs-lookup"><span data-stu-id="f73a7-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="f73a7-121">In het veld Einde van werkdag kunt u een tijd invoeren als transacties die na middernacht plaatsvinden, op de vorige dag moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="f73a7-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="f73a7-122">Selecteer 'Ja' als transacties die na middernacht plaatsvinden, als onderdeel van de vorige dag moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="f73a7-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="f73a7-123">Selecteer 'Ja' om overzichten te laten maken voor elke gedefinieerde overzichtsmethode.</span><span class="sxs-lookup"><span data-stu-id="f73a7-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="f73a7-124">Dat kan nuttig zijn als de prestaties van de boeking moeten worden verbeterd voor winkels met grote transactievolumes, aangezien er veel kleinere overzichten worden gemaakt die parallel kunnen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="f73a7-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="f73a7-125">In het veld Standaardklant kunt u de klantrekening selecteren om te gebruiken voor verkoop aan inloopklanten.</span><span class="sxs-lookup"><span data-stu-id="f73a7-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  

