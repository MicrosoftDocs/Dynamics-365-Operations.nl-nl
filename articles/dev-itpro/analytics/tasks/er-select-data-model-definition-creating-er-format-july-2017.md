---
title: Definities voor gegevensmodel selecteren tijdens het maken van indelingen
description: Als u de stappen in deze procedure wilt uitvoeren, moet u eerst de stappen in de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc357db8acbdb98741a694a8a9d3c0c0625c50e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "334491"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="c27eb-103">Definities voor gegevensmodel selecteren tijdens het maken van indelingen</span><span class="sxs-lookup"><span data-stu-id="c27eb-103">Select data model definitions when you create formats</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c27eb-104">Als u de stappen in deze procedure wilt uitvoeren, moet u eerst de stappen in de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien.</span><span class="sxs-lookup"><span data-stu-id="c27eb-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="c27eb-105">Deze procedure laat zien hoe een basisitem van een model kan worden geselecteerd als een gegevensmodeldefinitie voor het invoegen van een ER-indelingsconfiguratie (Electronic Reporting) die is ontworpen om elektronische documenten te genereren.</span><span class="sxs-lookup"><span data-stu-id="c27eb-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="c27eb-106">In deze procedure voegt u een nieuwe ER-indelingsconfiguratie voor het voorbeeldbedrijf Litware, Inc toe.</span><span class="sxs-lookup"><span data-stu-id="c27eb-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="c27eb-107">Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="c27eb-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="c27eb-108">De stappen kunnen worden voltooid met elke dataset.</span><span class="sxs-lookup"><span data-stu-id="c27eb-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="c27eb-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="c27eb-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c27eb-110">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief.</span><span class="sxs-lookup"><span data-stu-id="c27eb-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c27eb-111">Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure Een configuratieprovider maken en deze als actief markeren.</span><span class="sxs-lookup"><span data-stu-id="c27eb-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="c27eb-112">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="c27eb-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="c27eb-113">Een nieuwe ER-gegevensmodelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="c27eb-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="c27eb-114">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="c27eb-115">We voegen een nieuwe ER-modelconfiguratie toe met een gegevensmodel dat is ontworpen om te worden gebruikt als gegevensbron voor het genereren van ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="c27eb-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="c27eb-116">Typ in het veld Naam 'Betalingsmodel (fictief)'.</span><span class="sxs-lookup"><span data-stu-id="c27eb-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="c27eb-117">Betalingsmodel (fictief)</span><span class="sxs-lookup"><span data-stu-id="c27eb-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="c27eb-118">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="c27eb-118">Click Create configuration.</span></span>
4. <span data-ttu-id="c27eb-119">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="c27eb-119">Click Designer.</span></span>
    * <span data-ttu-id="c27eb-120">Open de ER-ontwerper om de structuur op te geven van een gegevensmodel van deze configuratie.</span><span class="sxs-lookup"><span data-stu-id="c27eb-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="c27eb-121">Stel dat we het gegevensmodel ontwerpen voor betalingenbedrijfsdomein om 2 betalingsmethoden te ondersteunen, kredietoverboeking en automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="c27eb-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="c27eb-122">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="c27eb-123">Typ 'Betalingen - kredietoverboeking' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c27eb-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="c27eb-124">Betaling - kredietoverboeking</span><span class="sxs-lookup"><span data-stu-id="c27eb-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="c27eb-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-125">Click Add.</span></span>
8. <span data-ttu-id="c27eb-126">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="c27eb-127">Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".</span><span class="sxs-lookup"><span data-stu-id="c27eb-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="c27eb-128">Typ 'Betalingen - directe afschrijving' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c27eb-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="c27eb-129">Betalingen - automatische afschrijving</span><span class="sxs-lookup"><span data-stu-id="c27eb-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="c27eb-130">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-130">Click Add.</span></span>
12. <span data-ttu-id="c27eb-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c27eb-131">Click Save.</span></span>
13. <span data-ttu-id="c27eb-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c27eb-132">Close the page.</span></span>
14. <span data-ttu-id="c27eb-133">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-133">Click Change status.</span></span>
    * <span data-ttu-id="c27eb-134">De conceptversie van het model voltooien om het beschikbaar te maken in nieuwe modeltoewijzingen en -indelingen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="c27eb-135">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="c27eb-135">Click Complete.</span></span>
16. <span data-ttu-id="c27eb-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c27eb-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="c27eb-137">Beginnen met het invoeren van een nieuwe ER-indelingsconfiguratie</span><span class="sxs-lookup"><span data-stu-id="c27eb-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="c27eb-138">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="c27eb-139">Voer in het veld Nieuw 'Indeling gebaseerd op gegevensmodel Betalingsmodel (fictief)' in.</span><span class="sxs-lookup"><span data-stu-id="c27eb-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="c27eb-140">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="c27eb-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="c27eb-141">Alle basisitems van het geselecteerde gegevensmodel zijn momenteel beschikbaar voor selectie als een gegevensmodeldefinitie.</span><span class="sxs-lookup"><span data-stu-id="c27eb-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="c27eb-142">U kunt doorgaan met uw indeling te ontwerpen met behulp van een van de vereiste basisitems van het gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="c27eb-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="c27eb-143">Een ontbrekende modeltoewijzing voor het geselecteerde basisitem voorkomt niet dat u doorgaat.</span><span class="sxs-lookup"><span data-stu-id="c27eb-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="c27eb-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c27eb-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="c27eb-145">Een nieuwe ER-modelgegevensmodelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="c27eb-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="c27eb-146">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="c27eb-147">Voer in het veld Nieuw 'Modeltoewijzing gebaseerd op gegevensmodel Betalingsmodel (fictief)' in.</span><span class="sxs-lookup"><span data-stu-id="c27eb-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="c27eb-148">Typ in het veld Naam 'Betalingsmodeltoewijzingen (fictief)'.</span><span class="sxs-lookup"><span data-stu-id="c27eb-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="c27eb-149">Betalingsmodeltoewijzingen (fictief)</span><span class="sxs-lookup"><span data-stu-id="c27eb-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="c27eb-150">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="c27eb-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="c27eb-151">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="c27eb-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="c27eb-152">ER-modeltoewijzingen ontwerpen</span><span class="sxs-lookup"><span data-stu-id="c27eb-152">Design ER model mappings</span></span>
1. <span data-ttu-id="c27eb-153">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="c27eb-153">Click Designer.</span></span>
    * <span data-ttu-id="c27eb-154">Gebruik de ER-ontwerper om de modeltoewijzingen op te geven voor de vereiste basisitems.</span><span class="sxs-lookup"><span data-stu-id="c27eb-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="c27eb-155">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="c27eb-155">Click Designer.</span></span>
    * <span data-ttu-id="c27eb-156">Instelling van geselecteerde modeltoewijzing simuleren voor het geselecteerde basisitem van het model.</span><span class="sxs-lookup"><span data-stu-id="c27eb-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="c27eb-157">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="c27eb-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="c27eb-158">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-158">Click Add root.</span></span>
5. <span data-ttu-id="c27eb-159">Typ 'Grootboek' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c27eb-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="c27eb-160">Typ "LedgerJournalTrans" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="c27eb-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="c27eb-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="c27eb-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="c27eb-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c27eb-162">Click OK.</span></span>
8. <span data-ttu-id="c27eb-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c27eb-163">Click Save.</span></span>
9. <span data-ttu-id="c27eb-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c27eb-164">Close the page.</span></span>
10. <span data-ttu-id="c27eb-165">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c27eb-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="c27eb-166">Beginnen met het invoeren van een andere ER-indelingsconfiguratie</span><span class="sxs-lookup"><span data-stu-id="c27eb-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="c27eb-167">Selecteer 'Betalingsmodel (fictief)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c27eb-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="c27eb-168">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c27eb-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="c27eb-169">Voer in het veld Nieuw 'Indeling gebaseerd op gegevensmodel Betalingsmodel (fictief)' in.</span><span class="sxs-lookup"><span data-stu-id="c27eb-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="c27eb-170">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="c27eb-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="c27eb-171">Houd er rekening mee dat nu slechts één basisitem beschikbaar is voor toewijzing aan de gegevensbronnen van de toepassing.</span><span class="sxs-lookup"><span data-stu-id="c27eb-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="c27eb-172">Wanneer ten minste één modeltoewijzing wordt geïntroduceerd, kunnen alleen de basisitems van het model die aan toepassingsgegevensbronnen zijn toegewezen, als modeldefinitie worden geselecteerd terwijl de ER-indeling wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c27eb-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="c27eb-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c27eb-173">Close the page.</span></span>

