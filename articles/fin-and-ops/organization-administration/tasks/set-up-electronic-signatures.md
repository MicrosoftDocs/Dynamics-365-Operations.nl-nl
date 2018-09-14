--- 
title: Elektronische handtekeningen instellen
description: Gebruik deze procedure om elektronische handtekeningen in te stellen.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: eb6bf529b1e94d598e219482f182140402f2928a
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="3f809-103">Elektronische handtekeningen instellen</span><span class="sxs-lookup"><span data-stu-id="3f809-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f809-104">Gebruik deze procedure om elektronische handtekeningen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="3f809-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="3f809-105">Met een elektronische handtekening wordt de identiteit bevestigd van een persoon die een computerproces wil starten of goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="3f809-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="3f809-106">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DAT.</span><span class="sxs-lookup"><span data-stu-id="3f809-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="3f809-107">Configuratiesleutel Elektronische handtekening inschakelen</span><span class="sxs-lookup"><span data-stu-id="3f809-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="3f809-108">Ga naar Systeembeheer > Instellingen > Licentieconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="3f809-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="3f809-109">Vouw in de structuur 'Beheer' uit.</span><span class="sxs-lookup"><span data-stu-id="3f809-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="3f809-110">Controleer of het selectievakje Elektronische handtekening is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3f809-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="3f809-111">Als het selectievakje Elektronische handtekening niet is ingeschakeld, moet u de onderhoudsmodus inschakelen.</span><span class="sxs-lookup"><span data-stu-id="3f809-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="3f809-112">De onderhoudsmodus kan in deze omgeving worden ingeschakeld door een onderhoudstaak uit te voeren vanuit Lifecycle Services of door het hulpmiddel Deployment.Setup lokaal te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3f809-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="3f809-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3f809-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="3f809-114">Parameters voor elektronische handtekeningen instellen</span><span class="sxs-lookup"><span data-stu-id="3f809-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="3f809-115">Ga naar Organisatiebeheer > Instellingen > Elektronische handtekening > Parameters voor elektronische handtekening.</span><span class="sxs-lookup"><span data-stu-id="3f809-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="3f809-116">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="3f809-116">Click Edit.</span></span>
3. <span data-ttu-id="3f809-117">Typ een waarde in het veld Mededeling.</span><span class="sxs-lookup"><span data-stu-id="3f809-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="3f809-118">Voer de melding in die ondertekenaars ontvangen wanneer om een handtekening wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="3f809-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="3f809-119">U kunt hier elke gewenste tekst invoeren.</span><span class="sxs-lookup"><span data-stu-id="3f809-119">You can enter any text.</span></span> <span data-ttu-id="3f809-120">Gewoonlijk laat u hiermee de gebruiker weten wat het betekent om een document elektronisch te ondertekenen.</span><span class="sxs-lookup"><span data-stu-id="3f809-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="3f809-121">Als u de meldingstekst in aanvullende talen wilt invoeren, klikt u op de knop Vertalingen.</span><span class="sxs-lookup"><span data-stu-id="3f809-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="3f809-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3f809-122">Click Save.</span></span>
5. <span data-ttu-id="3f809-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3f809-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="3f809-124">Redencodes voor elektronische handtekeningen instellen</span><span class="sxs-lookup"><span data-stu-id="3f809-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="3f809-125">Ga naar Organisatiebeheer > Instellingen > Elektronische handtekening > Redencodes elektronische handtekening.</span><span class="sxs-lookup"><span data-stu-id="3f809-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="3f809-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3f809-126">Click New.</span></span>
    * <span data-ttu-id="3f809-127">U moet redencodes instellen voordat u elektronische handtekeningen kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3f809-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="3f809-128">Een geldige redencode is vereist voor het ondertekenen van een document.</span><span class="sxs-lookup"><span data-stu-id="3f809-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="3f809-129">Een ondertekenaar selecteert een redencode om het doel van een elektronische handtekening aan te geven.</span><span class="sxs-lookup"><span data-stu-id="3f809-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="3f809-130">Een redencode kan bijvoorbeeld worden gebruikt om wettelijke goedkeuring aan te geven.</span><span class="sxs-lookup"><span data-stu-id="3f809-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="3f809-131">Typ een waarde in het veld Redencode.</span><span class="sxs-lookup"><span data-stu-id="3f809-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="3f809-132">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="3f809-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3f809-133">Voer aanvullende redencodes in indien nodig.</span><span class="sxs-lookup"><span data-stu-id="3f809-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="3f809-134">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3f809-134">Click Save.</span></span>
6. <span data-ttu-id="3f809-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3f809-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="3f809-136">Elektronische handtekeningen voor bestaande processen vereisen</span><span class="sxs-lookup"><span data-stu-id="3f809-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="3f809-137">Ga naar Organisatiebeheer > Instellingen > Elektronische handtekening > Vereisten elektronische handtekeningen.</span><span class="sxs-lookup"><span data-stu-id="3f809-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="3f809-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3f809-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f809-139">Selecteer een proces dat elektronische handtekeningen vereist</span><span class="sxs-lookup"><span data-stu-id="3f809-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="3f809-140">Schakel het selectievakje Handtekening vereist desgewenst in of uit.</span><span class="sxs-lookup"><span data-stu-id="3f809-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="3f809-141">Herhaal deze stappen voor elk proces dat elektronische handtekeningen vereist.</span><span class="sxs-lookup"><span data-stu-id="3f809-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="3f809-142">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3f809-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="3f809-143">Een aangepaste vereiste voor elektronische handtekeningen maken</span><span class="sxs-lookup"><span data-stu-id="3f809-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="3f809-144">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3f809-144">Click New.</span></span>
2. <span data-ttu-id="3f809-145">Schakel het selectievakje Handtekening vereist desgewenst in of uit.</span><span class="sxs-lookup"><span data-stu-id="3f809-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="3f809-146">Geef in het veld Naam een naam op voor het proces dat elektronische handtekeningen vereist.</span><span class="sxs-lookup"><span data-stu-id="3f809-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="3f809-147">Klik in het veld Tabelnaam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="3f809-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3f809-148">Zoek en selecteer in de lijst de tabel waarin de gegevens die moeten worden ondertekend, zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="3f809-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="3f809-149">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3f809-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3f809-150">Klik in het veld Veldnaam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="3f809-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3f809-151">Zoek en selecteer in de lijst het veld in de tabel dat u wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="3f809-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="3f809-152">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3f809-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3f809-153">Geef op wanneer een handtekening is vereist.</span><span class="sxs-lookup"><span data-stu-id="3f809-153">Specify when a signature is required.</span></span>     <span data-ttu-id="3f809-154">Selecteer Altijd als een handtekening vereist is wanneer de gegevens in het veld worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="3f809-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="3f809-155">Selecteer Alleen als een handtekening alleen onder bepaalde voorwaarden vereist is.</span><span class="sxs-lookup"><span data-stu-id="3f809-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="3f809-156">Als u Alleen selecteert, moet u een van de volgende opties ook selecteren: Wanneer een record wordt ingevoegd, Wanneer een record wordt bijgewerkt of Wanneer een record wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3f809-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="3f809-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3f809-157">Click Save.</span></span>
11. <span data-ttu-id="3f809-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3f809-158">Close the page.</span></span>


