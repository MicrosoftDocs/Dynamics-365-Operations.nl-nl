--- 
title: Een aanmaningsreeks maken
description: Gebruik deze taakhandleiding om een aanmaningsreeks te maken.
author: mikefalkner
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 63f28194065821f898cc73678a9868ec9ee2c64b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="1d7cc-103">Een aanmaningsreeks maken</span><span class="sxs-lookup"><span data-stu-id="1d7cc-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d7cc-104">Gebruik deze taakhandleiding om een aanmaningsreeks te maken.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="1d7cc-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1d7cc-106">Ga naar Crediteren en aanmaningen > Instellingen > Aanmaningsreeks instellen.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="1d7cc-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-107">Click New.</span></span>
3. <span data-ttu-id="1d7cc-108">Voer in het veld Aanmaningsreeks een volgordeid in die de volgorde zal aangeven.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="1d7cc-109">Deze wordt gebruikt bij het instellen van een boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="1d7cc-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1d7cc-111">De betalingsvoorwaarden zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-111">The terms of payment is optional.</span></span> <span data-ttu-id="1d7cc-112">Als u hier een waarde invoert, gebruikt de factuur voor de aanmaningskosten deze betalingsvoorwaarden in plaats van de betalingsvoorwaarden die zijn opgeslagen met de klant.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="1d7cc-113">Selecteer in het veld van de aanmaningscode de code voor de eerste aanmaning die u wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="1d7cc-114">De eerste aanmaning wordt gemaakt aan de hand van de vervaldatum op de factuur, die waarde die u invoert voor de respijtperiode in het veld Dagen op deze regel en andere gegevens die u in deze regel invoert.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="1d7cc-115">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1d7cc-116">De valuta voor de bijzondere kosten is standaard in de valuta van de klant.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="1d7cc-117">Deze valutacode kan verschillen van de factuurvaluta.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="1d7cc-118">Klik op Toevoegen om de volgende aanmaning toe te voegen die in de reeks wordt verzonden</span><span class="sxs-lookup"><span data-stu-id="1d7cc-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="1d7cc-119">In veel gevallen is de eerste aanmaning enkel een waarschuwing.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="1d7cc-120">U kunt indien nodig bijzondere kosten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="1d7cc-121">Selecteer in het veld van de aanmaningscode de volgende aanmaning die wordt verzonden in de reeks.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="1d7cc-122">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="1d7cc-123">Selecteer in het hoofdrekeningveld de opbrengstrekening die voor bijzondere kosten wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="1d7cc-124">Voer de kosten in die worden doorberekend bij het maken van deze aanmaning.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="1d7cc-125">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="1d7cc-126">Selecteer een btw-groep voor artikel als btw op de kosten moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="1d7cc-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1d7cc-128">Voer het minimale achterstallige saldo dat is vereist voordat een aanmaning wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="1d7cc-129">Voer het aantal respijtdagen in dat u zult toestaan.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="1d7cc-130">Dit is het aantal dagen na de vervaldatum waarop een aanmaning kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="1d7cc-131">De vervaldatum die voor de berekening wordt gebruikt, is afhankelijk van de positie van de aanmaning in de aanmaningsreeks: ⦁ de respijtperiode voor aanmaning 1 is gerelateerd aan de vervaldatum van de factuur.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="1d7cc-132">⦁ De respijtperiode voor aanmaning 2 en hoger is gerelateerd aan de datum waarop de vorige aanmaning is geboekt of afgedrukt, afhankelijk van de selectie in het veld Aanmaningscode bijwerken op de pagina Parameters van de module Klanten.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="1d7cc-133">Klik op Toevoegen om de laatste aanmaning in de reeks toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="1d7cc-134">U kunt tot vijf aanmaningscodes toevoegen voor een aanmaningsreeks.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="1d7cc-135">Selecteer in het veld van de aanmaningscode de volgende aanmaning die wordt verzonden in de reeks.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="1d7cc-136">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="1d7cc-137">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="1d7cc-138">Voer in het veld Bijzondere kosten in valuta een getal in.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="1d7cc-139">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="1d7cc-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="1d7cc-141">Voer in het veld Minimum achterstallig saldo een getal in.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="1d7cc-142">Voer een getal in het veld Dagen in.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="1d7cc-143">Schakel dit selectievakje in om ervoor te zorgen dat de klant geen leveringen en facturen meer ontvangt.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="1d7cc-144">Als u de rekening wilt deblokkeren, selecteert u Nee in het veld Geblokkeerde facturering en levering op de pagina Klanten.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="1d7cc-145">Vouw het sneltabblad Notitie uit.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="1d7cc-146">Voer de tekst in die op de aanmaning moet worden weergegeven voor de geselecteerde aanmaningscode.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="1d7cc-147">Deze tekst kunt u in meerdere talen vertalen via het menu Vertalingen boven het notitievakje.</span><span class="sxs-lookup"><span data-stu-id="1d7cc-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


