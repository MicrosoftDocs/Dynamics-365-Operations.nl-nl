--- 
title: Elektronische documenten genereren voor betalingen met een indelingsconfiguratie voor elektronische aangifte (taakbegeleiding) (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken om elektronische documenten te genereren voor de verwerking van betalingen.
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 98c25b884deb82f9d0655dde7790dfb57d7c13f6
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="05d53-103">Elektronische documenten genereren voor betalingen met een indelingsconfiguratie voor elektronische aangifte (taakbegeleiding) (ER)</span><span class="sxs-lookup"><span data-stu-id="05d53-103">Generate electronic documents for payments using a format configuration for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05d53-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken om elektronische documenten te genereren voor de verwerking van betalingen.</span><span class="sxs-lookup"><span data-stu-id="05d53-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="05d53-105">Deze stappen kunnen in het voorbeeldbedrijf GBSI worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="05d53-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="05d53-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratie maken met de indeling van een betalingsdocument" voltooien.</span><span class="sxs-lookup"><span data-stu-id="05d53-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="05d53-107">De configuratie van de elektronische betalingsmethode wijzigen</span><span class="sxs-lookup"><span data-stu-id="05d53-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="05d53-108">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="05d53-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="05d53-109">Selecteer indien nodig de sectie Bestandsindeling om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="05d53-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="05d53-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="05d53-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="05d53-111">Filter bijvoorbeeld op het veld Betalingsmethode met de waarde 'Elektronisch'.</span><span class="sxs-lookup"><span data-stu-id="05d53-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="05d53-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="05d53-112">Click Edit.</span></span>
5. <span data-ttu-id="05d53-113">Stel het veld Algemene elektronische rapportage in op Ja.</span><span class="sxs-lookup"><span data-stu-id="05d53-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="05d53-114">Selecteer Ja als u het algemene patroon voor elektronische rapportage wilt gebruiken voor het genereren van betalingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="05d53-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="05d53-115">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="05d53-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="05d53-116">Selecteer de indelingsconfiguratie BACS (UK fictief).</span><span class="sxs-lookup"><span data-stu-id="05d53-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="05d53-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="05d53-117">Click Save.</span></span>
9. <span data-ttu-id="05d53-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="05d53-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="05d53-119">De indeling van gegenereerde betalingsbestanden testen</span><span class="sxs-lookup"><span data-stu-id="05d53-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="05d53-120">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="05d53-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="05d53-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="05d53-121">Click New.</span></span>
3. <span data-ttu-id="05d53-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="05d53-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="05d53-123">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="05d53-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="05d53-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="05d53-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05d53-125">Selecteer VendPay.</span><span class="sxs-lookup"><span data-stu-id="05d53-125">Select VendPay.</span></span>  
6. <span data-ttu-id="05d53-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="05d53-126">Click Save.</span></span>
7. <span data-ttu-id="05d53-127">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="05d53-127">Click Lines.</span></span>
8. <span data-ttu-id="05d53-128">Typ 'DEMF' in het veld Bedrijf.</span><span class="sxs-lookup"><span data-stu-id="05d53-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="05d53-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="05d53-129">DEMF</span></span>  
9. <span data-ttu-id="05d53-130">Geef in het veld Rekening de waarde 'DE-01001' op.</span><span class="sxs-lookup"><span data-stu-id="05d53-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="05d53-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="05d53-131">DE-01001</span></span>  
10. <span data-ttu-id="05d53-132">Typ 'Betaling' in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="05d53-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="05d53-133">Betaling</span><span class="sxs-lookup"><span data-stu-id="05d53-133">Payment</span></span>  
11. <span data-ttu-id="05d53-134">Voer een nummer in het veld Debet in.</span><span class="sxs-lookup"><span data-stu-id="05d53-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="05d53-135">1000</span><span class="sxs-lookup"><span data-stu-id="05d53-135">1000</span></span>  
12. <span data-ttu-id="05d53-136">Klik op het tabblad Betaling.</span><span class="sxs-lookup"><span data-stu-id="05d53-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="05d53-137">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="05d53-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="05d53-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="05d53-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="05d53-139">Selecteer de waarde Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="05d53-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="05d53-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="05d53-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="05d53-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="05d53-141">Click Save.</span></span>
17. <span data-ttu-id="05d53-142">Klik op Betalingen genereren.</span><span class="sxs-lookup"><span data-stu-id="05d53-142">Click Generate payments.</span></span>
18. <span data-ttu-id="05d53-143">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="05d53-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="05d53-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="05d53-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="05d53-145">Selecteer de waarde Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="05d53-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="05d53-146">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="05d53-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05d53-147">Selecteer de waarde Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="05d53-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="05d53-148">Typ een waarde in het veld Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="05d53-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="05d53-149">Typ bijvoorbeeld 'betalingen'.</span><span class="sxs-lookup"><span data-stu-id="05d53-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="05d53-150">Klik in het veld Bankrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="05d53-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="05d53-151">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="05d53-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05d53-152">Selecteer de waarde GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="05d53-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="05d53-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="05d53-153">Click OK.</span></span>
25. <span data-ttu-id="05d53-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="05d53-154">Click OK.</span></span>
    * <span data-ttu-id="05d53-155">Analyseer het gemaakte betalingsbestand in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="05d53-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="05d53-156">Vergelijken het met de ontworpen documentindeling en de gedefinieerde kenmerken van de betalingstransactie.</span><span class="sxs-lookup"><span data-stu-id="05d53-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


