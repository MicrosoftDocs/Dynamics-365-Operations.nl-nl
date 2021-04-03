---
title: Elektronische ER-documenten genereren voor betalingen met een indelingsconfiguratie
description: In dit onderwerp wordt beschreven hoe u een nieuwe ER-indelingsconfiguratie (Electronic Reporting) gebruikt om elektronische documenten voor de verwerking van betalingen te genereren.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dd39b3faba90b38b837cd5167b216f9faa31d82
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570211"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="677fe-103">Elektronische ER-documenten genereren voor betalingen met een indelingsconfiguratie</span><span class="sxs-lookup"><span data-stu-id="677fe-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="677fe-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken om elektronische documenten te genereren voor de verwerking van betalingen.</span><span class="sxs-lookup"><span data-stu-id="677fe-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="677fe-105">Deze stappen kunnen in het voorbeeldbedrijf GBSI worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="677fe-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="677fe-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure Een configuratie maken met de indeling van een betalingsdocument voltooien.</span><span class="sxs-lookup"><span data-stu-id="677fe-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="677fe-107">De configuratie van de elektronische betalingsmethode wijzigen</span><span class="sxs-lookup"><span data-stu-id="677fe-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="677fe-108">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="677fe-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="677fe-109">Selecteer indien nodig de sectie Bestandsindeling om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="677fe-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="677fe-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="677fe-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="677fe-111">Filter bijvoorbeeld op het veld Betalingsmethode met de waarde 'Elektronisch'.</span><span class="sxs-lookup"><span data-stu-id="677fe-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="677fe-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="677fe-112">Click Edit.</span></span>
5. <span data-ttu-id="677fe-113">Stel het veld Algemene elektronische rapportage in op Ja.</span><span class="sxs-lookup"><span data-stu-id="677fe-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="677fe-114">Selecteer Ja als u het algemene patroon voor elektronische rapportage wilt gebruiken voor het genereren van betalingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="677fe-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="677fe-115">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="677fe-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="677fe-116">Selecteer de indelingsconfiguratie BACS (UK fictief).</span><span class="sxs-lookup"><span data-stu-id="677fe-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="677fe-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="677fe-117">Click Save.</span></span>
9. <span data-ttu-id="677fe-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="677fe-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="677fe-119">De indeling van gegenereerde betalingsbestanden testen</span><span class="sxs-lookup"><span data-stu-id="677fe-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="677fe-120">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="677fe-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="677fe-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="677fe-121">Click New.</span></span>
3. <span data-ttu-id="677fe-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="677fe-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="677fe-123">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="677fe-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="677fe-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="677fe-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="677fe-125">Selecteer VendPay.</span><span class="sxs-lookup"><span data-stu-id="677fe-125">Select VendPay.</span></span>  
6. <span data-ttu-id="677fe-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="677fe-126">Click Save.</span></span>
7. <span data-ttu-id="677fe-127">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="677fe-127">Click Lines.</span></span>
8. <span data-ttu-id="677fe-128">Typ 'DEMF' in het veld Bedrijf.</span><span class="sxs-lookup"><span data-stu-id="677fe-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="677fe-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="677fe-129">DEMF</span></span>  
9. <span data-ttu-id="677fe-130">Geef in het veld Rekening de waarde 'DE-01001' op.</span><span class="sxs-lookup"><span data-stu-id="677fe-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="677fe-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="677fe-131">DE-01001</span></span>  
10. <span data-ttu-id="677fe-132">Typ 'Betaling' in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="677fe-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="677fe-133">Betaling</span><span class="sxs-lookup"><span data-stu-id="677fe-133">Payment</span></span>  
11. <span data-ttu-id="677fe-134">Voer een nummer in het veld Debet in.</span><span class="sxs-lookup"><span data-stu-id="677fe-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="677fe-135">1000</span><span class="sxs-lookup"><span data-stu-id="677fe-135">1000</span></span>  
12. <span data-ttu-id="677fe-136">Klik op het tabblad Betaling.</span><span class="sxs-lookup"><span data-stu-id="677fe-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="677fe-137">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="677fe-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="677fe-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="677fe-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="677fe-139">Selecteer de waarde Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="677fe-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="677fe-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="677fe-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="677fe-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="677fe-141">Click Save.</span></span>
17. <span data-ttu-id="677fe-142">Klik op Betalingen genereren.</span><span class="sxs-lookup"><span data-stu-id="677fe-142">Click Generate payments.</span></span>
18. <span data-ttu-id="677fe-143">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="677fe-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="677fe-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="677fe-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="677fe-145">Selecteer de waarde Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="677fe-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="677fe-146">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="677fe-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="677fe-147">Selecteer de waarde Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="677fe-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="677fe-148">Typ een waarde in het veld Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="677fe-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="677fe-149">Typ bijvoorbeeld 'betalingen'.</span><span class="sxs-lookup"><span data-stu-id="677fe-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="677fe-150">Klik in het veld Bankrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="677fe-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="677fe-151">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="677fe-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="677fe-152">Selecteer de waarde GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="677fe-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="677fe-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="677fe-153">Click OK.</span></span>
25. <span data-ttu-id="677fe-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="677fe-154">Click OK.</span></span>
    * <span data-ttu-id="677fe-155">Analyseer het gemaakte betalingsbestand in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="677fe-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="677fe-156">Vergelijken het met de ontworpen documentindeling en de gedefinieerde kenmerken van de betalingstransactie.</span><span class="sxs-lookup"><span data-stu-id="677fe-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]