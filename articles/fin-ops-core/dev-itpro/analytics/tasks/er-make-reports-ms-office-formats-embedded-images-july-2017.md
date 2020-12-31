---
title: Configuraties ontwerpen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten
description: De stappen in dit onderwerp geven informatie over hoe u elektronische rapportage (ER)-configuraties ontwerpt die elektronische documenten in Microsoft Office-indelingen (Excel en Word) genereren die ingesloten afbeeldingen bevatten.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0145565ba060308162620f29a42499b0bffe6496
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684397"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c519d-103">Configuraties ontwerpen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten</span><span class="sxs-lookup"><span data-stu-id="c519d-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c519d-104">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure "ER Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="c519d-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="c519d-105">Deze procedure laat zien hoe u elektronische rapportage (ER)-configuraties ontwerpt voor het genereren van een elektronisch Microsoft Excel- of Word-document met ingesloten afbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="c519d-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c519d-106">In deze procedure maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Deze stappen kunnen worden uitgevoerd met behulp van de dataset USMF.</span><span class="sxs-lookup"><span data-stu-id="c519d-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c519d-107">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="c519d-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c519d-108">Voordat u begint, downloadt u de bestanden vermeld in het Help-onderwerp [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](../electronic-reporting-embed-images-shapes.md) en slaat u ze op.</span><span class="sxs-lookup"><span data-stu-id="c519d-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="c519d-109">De bestanden zijn: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png en Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="c519d-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="c519d-110">Vereisten controleren</span><span class="sxs-lookup"><span data-stu-id="c519d-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c519d-111">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="c519d-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c519d-112">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief.</span><span class="sxs-lookup"><span data-stu-id="c519d-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c519d-113">Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure "Een configuratieprovider maken en deze als actief markeren".</span><span class="sxs-lookup"><span data-stu-id="c519d-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="c519d-114">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="c519d-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c519d-115">Een nieuwe ER-modelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="c519d-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c519d-116">In plaats van een nieuw model te maken kunt u het ER-modelconfiguratiebestand (Model voor cheques.xml) laden dat u eerder hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="c519d-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c519d-117">Dit bestand bevat het voorbeeldgegevensmodel voor betaalcheques en de toewijzing van het gegevensmodel aan de gegevensonderdelen van de toepassing Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="c519d-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c519d-118">Klik op het sneltabblad Versies op Uitwisselen.</span><span class="sxs-lookup"><span data-stu-id="c519d-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c519d-119">Klik op Laden uit XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="c519d-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c519d-120">Klik op Bladeren en selecteer vervolgens Model voor cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c519d-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c519d-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c519d-121">Click OK.</span></span>  
 6. <span data-ttu-id="c519d-122">Het geladen model wordt gebruikt als een gegevensbron met informatie voor het genereren van documenten met afbeeldingen in Excel en Word.</span><span class="sxs-lookup"><span data-stu-id="c519d-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c519d-123">Een nieuwe ER-indelingsconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="c519d-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c519d-124">In plaats van een nieuwe indeling te maken kunt u het ER-indelingsconfiguratiebestand (Afdrukindeling van cheques.xml) laden dat u eerder hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="c519d-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c519d-125">Dit bestand bevat de voorbeeldindeling voor het afdrukken van cheques met behulp van het voorgedrukte formulier en de toewijzing van deze indeling voor het gegevensmodel 'Model voor cheques'.</span><span class="sxs-lookup"><span data-stu-id="c519d-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="c519d-126">Klik op Uitwisselen.</span><span class="sxs-lookup"><span data-stu-id="c519d-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="c519d-127">Klik op Laden uit XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="c519d-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c519d-128">Klik op Bladeren en selecteer het bestand Afdrukindeling van cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c519d-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c519d-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c519d-129">Click OK.</span></span>  
 6. <span data-ttu-id="c519d-130">Vouw in de structuur 'Model voor cheques' uit.</span><span class="sxs-lookup"><span data-stu-id="c519d-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c519d-131">Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="c519d-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c519d-132">De geladen indeling wordt gebruikt voor het genereren van documenten met afbeeldingen in Excel en Word.</span><span class="sxs-lookup"><span data-stu-id="c519d-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c519d-133">ER-gebruikersparameters configureren</span><span class="sxs-lookup"><span data-stu-id="c519d-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c519d-134">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="c519d-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c519d-135">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="c519d-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="c519d-136">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c519d-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c519d-137">Schakel de markering 'Concept uitvoeren' in om de conceptversie van de geselecteerde indeling te starten in plaats van de voltooide.</span><span class="sxs-lookup"><span data-stu-id="c519d-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c519d-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c519d-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c519d-139">Parameters voor cash- en bankbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="c519d-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c519d-140">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="c519d-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c519d-141">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="c519d-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c519d-142">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="c519d-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c519d-143">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="c519d-143">Click Check.</span></span>  
 5. <span data-ttu-id="c519d-144">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="c519d-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c519d-145">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="c519d-145">Click Edit.</span></span>  
 7. <span data-ttu-id="c519d-146">Selecteer Ja in het veld Bedrijfslogo.</span><span class="sxs-lookup"><span data-stu-id="c519d-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c519d-147">Klik op Bedrijfslogo.</span><span class="sxs-lookup"><span data-stu-id="c519d-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="c519d-148">Klik op Wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c519d-148">Click Change.</span></span>  
 10. <span data-ttu-id="c519d-149">Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Bedrijfslogo.png.</span><span class="sxs-lookup"><span data-stu-id="c519d-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c519d-150">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c519d-150">Click Save.</span></span>  
 12. <span data-ttu-id="c519d-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c519d-151">Close the page.</span></span>  
 13. <span data-ttu-id="c519d-152">Vouw de sectie Handtekening uit.</span><span class="sxs-lookup"><span data-stu-id="c519d-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c519d-153">Selecteer Ja in het veld Eerste handtekening afdrukken.</span><span class="sxs-lookup"><span data-stu-id="c519d-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c519d-154">Klik op Wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c519d-154">Click Change.</span></span>  
 16. <span data-ttu-id="c519d-155">Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Afbeelding handtekening.png.</span><span class="sxs-lookup"><span data-stu-id="c519d-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c519d-156">Vouw de sectie Aantal exemplaren uit.</span><span class="sxs-lookup"><span data-stu-id="c519d-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c519d-157">Selecteer een optie in het veld Watermerk.</span><span class="sxs-lookup"><span data-stu-id="c519d-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c519d-158">Selecteer Ja in het veld Algemene elektronische exportindeling.</span><span class="sxs-lookup"><span data-stu-id="c519d-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c519d-159">Selecteer Configuratie 'afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="c519d-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c519d-160">Nu wordt de geselecteerde ER-indeling gebruikt voor het afdrukken van cheques.</span><span class="sxs-lookup"><span data-stu-id="c519d-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c519d-161">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="c519d-161">Click Attach.</span></span>  
 23. <span data-ttu-id="c519d-162">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c519d-162">Click New.</span></span>  
 24. <span data-ttu-id="c519d-163">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="c519d-163">Click File.</span></span>  
 25. <span data-ttu-id="c519d-164">Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Afbeelding handtekening 2.png.</span><span class="sxs-lookup"><span data-stu-id="c519d-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c519d-165">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c519d-165">Close the page.</span></span>  
 27. <span data-ttu-id="c519d-166">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c519d-166">Close the page.</span></span>  
 28. <span data-ttu-id="c519d-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c519d-167">Close the page.</span></span>  
 29. <span data-ttu-id="c519d-168">Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.</span><span class="sxs-lookup"><span data-stu-id="c519d-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c519d-169">Selecteer Ja in het veld Voorafmelding maken toestaan voor inactieve bankrekeningen:.</span><span class="sxs-lookup"><span data-stu-id="c519d-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c519d-170">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c519d-170">Click Save.</span></span>  
 32. <span data-ttu-id="c519d-171">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c519d-171">Close the page.</span></span>  
