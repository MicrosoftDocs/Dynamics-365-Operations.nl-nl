---
title: Rapportage voor betalingssaldo instellen (België)
description: Gebruik deze procedure om BLWI-informatie (Belgisch Luxemburgs Wissel Instituut) in te stellen voor België.
author: v-oloski
manager: AnnBe
ms.date: 07/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Belgium
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed5e463f23bd2e2bde7d34a0e5b59d416f6fb84
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175160"
---
# <a name="set-up-payment-balance-reporting-belgium"></a><span data-ttu-id="82c31-103">Rapportage voor betalingssaldo instellen (België)</span><span class="sxs-lookup"><span data-stu-id="82c31-103">Set up payment balance reporting (Belgium)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82c31-104">Gebruik deze procedure om BLWI-informatie (Belgisch Luxemburgs Wissel Instituut) in te stellen voor België.</span><span class="sxs-lookup"><span data-stu-id="82c31-104">Use this procedure to set up Belgisch Luxemburgs Wissel Instituut (BLWI) information for Belgium.</span></span> <span data-ttu-id="82c31-105">Deze procedure is gemaakt met het demogegevensbedrijf USSI.</span><span class="sxs-lookup"><span data-stu-id="82c31-105">This procedure was created by using the USSI demo data company.</span></span>

<span data-ttu-id="82c31-106">Deze functionaliteit is beschikbaar voor rechtspersonen die hun primaire adres in België hebben.</span><span class="sxs-lookup"><span data-stu-id="82c31-106">This functionality is available for legal entities that have their primary address in Belgium.</span></span> <span data-ttu-id="82c31-107">Voordat u deze procedure voltooien kunt, moet u de registratie-id instellen voor België en het registratienummer invoeren dat moet worden gebruikt om de BLWI-aangifte te maken.</span><span class="sxs-lookup"><span data-stu-id="82c31-107">Before you can complete this procedure, you must set up the registration ID for Belgium and enter the registration number that should be used to create the BLWI declaration.</span></span>


## <a name="set-up-a-blwi-countryregion-group"></a><span data-ttu-id="82c31-108">Een BLWI-land-/regiogroep instellen</span><span class="sxs-lookup"><span data-stu-id="82c31-108">Set up a BLWI country/region group</span></span>
1. <span data-ttu-id="82c31-109">Ga naar Btw > Instellingen > Buitenlandse handel > Landen-/regiogroepen BLWI.</span><span class="sxs-lookup"><span data-stu-id="82c31-109">Go to Tax > Setup > Foreign trade > BLWI country/region groups.</span></span>
2. <span data-ttu-id="82c31-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="82c31-110">Click New.</span></span>
3. <span data-ttu-id="82c31-111">Typ een waarde in het veld Groep-id.</span><span class="sxs-lookup"><span data-stu-id="82c31-111">In the Group ID field, type a value.</span></span>
4. <span data-ttu-id="82c31-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="82c31-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82c31-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="82c31-113">Click Add.</span></span>
6. <span data-ttu-id="82c31-114">Typ of selecteer een waarde in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="82c31-114">In the Country/region field, enter or select a value.</span></span>
7. <span data-ttu-id="82c31-115">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="82c31-115">In the Description field, type a value.</span></span>
8. <span data-ttu-id="82c31-116">Klik op Vertalingen.</span><span class="sxs-lookup"><span data-stu-id="82c31-116">Click Translations.</span></span>
9. <span data-ttu-id="82c31-117">Typ of selecteer een waarde in het veld Waarde.</span><span class="sxs-lookup"><span data-stu-id="82c31-117">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="82c31-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="82c31-118">Close the page.</span></span>

## <a name="set-up-blwi-currencies"></a><span data-ttu-id="82c31-119">BLWI-valuta's instellen</span><span class="sxs-lookup"><span data-stu-id="82c31-119">Set up BLWI currencies</span></span>
1. <span data-ttu-id="82c31-120">Ga naar Btw > Instellingen > Buitenlandse handel > BLWI-valuta's.</span><span class="sxs-lookup"><span data-stu-id="82c31-120">Go to Tax > Setup > Foreign trade > BLWI currencies.</span></span>
2. <span data-ttu-id="82c31-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="82c31-121">Click New.</span></span>
3. <span data-ttu-id="82c31-122">Typ of selecteer een waarde in het veld Valuta.</span><span class="sxs-lookup"><span data-stu-id="82c31-122">In the Currency field, enter or select a value.</span></span>
4. <span data-ttu-id="82c31-123">Schakel het selectievakje Rapporteren in deze valuta in.</span><span class="sxs-lookup"><span data-stu-id="82c31-123">Select the Report in this currency check box.</span></span>
5. <span data-ttu-id="82c31-124">Voer in het veld Kolomnummer een getal in.</span><span class="sxs-lookup"><span data-stu-id="82c31-124">In the Column number field, enter a number.</span></span>

## <a name="set-up-blwi-parameters"></a><span data-ttu-id="82c31-125">BLWI-parameters instellen</span><span class="sxs-lookup"><span data-stu-id="82c31-125">Set up BLWI parameters</span></span>
1. <span data-ttu-id="82c31-126">Ga naar Btw > Instellingen > Buitenlandse handel > BLWI-parameters.</span><span class="sxs-lookup"><span data-stu-id="82c31-126">Go to Tax > Setup > Foreign trade > BLWI parameters.</span></span>
2. <span data-ttu-id="82c31-127">Selecteer Ja in het veld BLWI.</span><span class="sxs-lookup"><span data-stu-id="82c31-127">Select Yes in the BLWI field.</span></span>
    * <span data-ttu-id="82c31-128">Deze parameter moet worden geactiveerd voordat u klant/leveranciertransacties boekt, zodat de transacties worden overgeboekt naar het betalingssaldo.</span><span class="sxs-lookup"><span data-stu-id="82c31-128">This parameter should be activated before you post customer/vendor transactions, so that the transactions are transferred to the payment balance.</span></span>  
3. <span data-ttu-id="82c31-129">Typ een waarde in het veld E-mailadres.</span><span class="sxs-lookup"><span data-stu-id="82c31-129">In the Email field, type a value.</span></span>
4. <span data-ttu-id="82c31-130">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="82c31-130">In the Name field, type a value.</span></span>
5. <span data-ttu-id="82c31-131">Typ een waarde in het veld Telefoon.</span><span class="sxs-lookup"><span data-stu-id="82c31-131">In the Telephone field, type a value.</span></span>
6. <span data-ttu-id="82c31-132">Typ een waarde in het veld Fax.</span><span class="sxs-lookup"><span data-stu-id="82c31-132">In the Fax field, type a value.</span></span>
7. <span data-ttu-id="82c31-133">Selecteer een optie in het veld BLWI-code in journalen controleren.</span><span class="sxs-lookup"><span data-stu-id="82c31-133">In the Check BLWI code on journals field, select an option.</span></span>
    * <span data-ttu-id="82c31-134">Selecteer de regel voor het controleren of een betalingsdoelcode in documenten is opgegeven in het veld BLWI-code controleren.</span><span class="sxs-lookup"><span data-stu-id="82c31-134">In the Check BLWI code field, select the rule for checking that a payment purpose code is specified in documents.</span></span> <span data-ttu-id="82c31-135">De beschikbare opties zijn Geen, Waarschuwing en Fout.</span><span class="sxs-lookup"><span data-stu-id="82c31-135">The available options are None, Warning, and Error.</span></span> <span data-ttu-id="82c31-136">Als een transactie een klant/leverancier heeft die zich in een vreemd land/regio bevindt (dat wil zeggen het land/regio van de klant/leverancier verschilt van het land/regio van de rechtspersoon), de transactie geen toegewezen betalingsdoelcode heeft en de cheque is ingesteld op waarschuwing of fout, wordt een waarschuwing of foutbericht weergegeven tijdens de boeking.</span><span class="sxs-lookup"><span data-stu-id="82c31-136">If a transaction has a customer/vendor that is located in a foreign country/region (that is, the country/region of the customer/vendor differs from the country/region of the legal entity), the transaction doesn’t have an assigned payment purpose code, and the check is set to Warning or Error, either a warning or error message will be shown during posting.</span></span> <span data-ttu-id="82c31-137">Deze validatie wordt toegepast op alle klant/leverancierstransacties, behalve betalingstransacties.</span><span class="sxs-lookup"><span data-stu-id="82c31-137">This validation is applied for all customer/vendor transactions except payment transactions.</span></span>  
8. <span data-ttu-id="82c31-138">Typ of selecteer een waarde in het veld Indelingstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="82c31-138">In the Format mapping field, enter or select a value.</span></span>
    * <span data-ttu-id="82c31-139">Vereiste: u moet de configuratie van de BLWI-indeling (BE) voor elektronische rapportage (ER) uploaden vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="82c31-139">Prerequisite: You should upload the BLWI format (BE) configuration for Electronic reporting (ER) from Microsoft Dynamics Lifecycle Services (LCS).</span></span>  

## <a name="set-up-payment-survey-codes"></a><span data-ttu-id="82c31-140">Betalingsonderzoekscodes instellen</span><span class="sxs-lookup"><span data-stu-id="82c31-140">Set up payment survey codes</span></span>
1. <span data-ttu-id="82c31-141">Ga naar Btw > Instellingen > Buitenlandse handel > Betalingsonderzoekscodes.</span><span class="sxs-lookup"><span data-stu-id="82c31-141">Go to Tax > Setup > Foreign trade > Payment survey codes.</span></span>
2. <span data-ttu-id="82c31-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="82c31-142">Click New.</span></span>
3. <span data-ttu-id="82c31-143">Typ een waarde in het veld Onderzoekscode.</span><span class="sxs-lookup"><span data-stu-id="82c31-143">In the Survey code field, type a value.</span></span>
4. <span data-ttu-id="82c31-144">Selecteer een optie in het veld Maand/kwartaal.</span><span class="sxs-lookup"><span data-stu-id="82c31-144">In the Month/Quarter field, select an option.</span></span>
5. <span data-ttu-id="82c31-145">Selecteer een optie in het veld Berekening.</span><span class="sxs-lookup"><span data-stu-id="82c31-145">In the Calculation type field, select an option.</span></span>
    * <span data-ttu-id="82c31-146">Als u Omzet selecteert in het veld Berekeningstype, worden de klant/leverancierstransacties die worden geboekt tijdens de rapportperiode overgebracht naar het betalingssaldo en is het bedrag dat wordt gerapporteerd het totale bedrag van de geboekte transactie.</span><span class="sxs-lookup"><span data-stu-id="82c31-146">If you select Turnover in the Calculation type field, the customer/vendor transactions that are posted during the reporting period are transferred to the payment balance, and the amount that is reported is the total amount of the posted transaction.</span></span>  <span data-ttu-id="82c31-147">Als u Saldo selecteert, worden de klant/leverancierstransacties die openstaan (niet volledig vereffend of gesloten) aan het einde van de rapportageperiode, overgebracht naar het betalingssaldo en is het bedrag dat wordt gerapporteerd het openstaande (niet-vereffende) bedrag van de geboekte transactie aan het einde van de rapportageperiode.</span><span class="sxs-lookup"><span data-stu-id="82c31-147">If you select Balance, the customer/vendor transactions that are open (not fully settled/closed) at the end of the reporting period are transferred to the payment balance, and the amount that is reported is the open (unsettled) amount of the posted transaction as of the end of the reporting period.</span></span>  
6. <span data-ttu-id="82c31-148">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="82c31-148">In the Description field, type a value.</span></span>
7. <span data-ttu-id="82c31-149">Typ een waarde in het veld Overzicht land/regio.</span><span class="sxs-lookup"><span data-stu-id="82c31-149">In the Summary country/region field, type a value.</span></span>
8. <span data-ttu-id="82c31-150">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="82c31-150">Click Add.</span></span>
9. <span data-ttu-id="82c31-151">Typ of selecteer een waarde in het veld Doelcode centrale bank.</span><span class="sxs-lookup"><span data-stu-id="82c31-151">In the Central bank purpose code field, enter or select a value.</span></span>
10. <span data-ttu-id="82c31-152">Schakel het selectievakje Betaling opnemen in.</span><span class="sxs-lookup"><span data-stu-id="82c31-152">Select the Include payment check box.</span></span>
    * <span data-ttu-id="82c31-153">Houd er rekening mee dat betalingstransacties standaard niet worden overgeboekt naar het betalingssaldo.</span><span class="sxs-lookup"><span data-stu-id="82c31-153">Note that payment transactions won't be transferred to the payment balance survey by default.</span></span> <span data-ttu-id="82c31-154">De gebruiker moet het veld Betaling opnemen activeren voor doelcodes.</span><span class="sxs-lookup"><span data-stu-id="82c31-154">The user must activate the Include payment field for purpose codes.</span></span>  
