---
title: Configuraties ontwerpen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten
description: Dit onderwerp laat zien hoe u configuraties ontwerpt voor het genereren van elektronische documenten in Excel- en Word-indeling met ingesloten afbeeldingen.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944552"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="acf89-103">Configuraties ontwerpen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten</span><span class="sxs-lookup"><span data-stu-id="acf89-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acf89-104">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure "ER Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="acf89-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="acf89-105">Deze procedure laat zien hoe u elektronische rapportage (ER)-configuraties ontwerpt voor het genereren van een elektronisch Microsoft Excel- of Word-document met ingesloten afbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="acf89-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="acf89-106">In deze procedure maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Deze stappen kunnen worden uitgevoerd met behulp van de dataset USMF.</span><span class="sxs-lookup"><span data-stu-id="acf89-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="acf89-107">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="acf89-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="acf89-108">Voordat u begint, moet u de volgende bestanden downloaden en opslaan:</span><span class="sxs-lookup"><span data-stu-id="acf89-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="acf89-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="acf89-109">Description</span></span>                                          | <span data-ttu-id="acf89-110">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="acf89-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="acf89-111">Configuratie van model voor ER-gegevens</span><span class="sxs-lookup"><span data-stu-id="acf89-111">ER data model configuration</span></span>                          | [<span data-ttu-id="acf89-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="acf89-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="acf89-113">ER-indelingsconfiguratie</span><span class="sxs-lookup"><span data-stu-id="acf89-113">ER format configuration</span></span>                              | [<span data-ttu-id="acf89-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="acf89-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="acf89-115">Afbeelding met bedrijfslogo</span><span class="sxs-lookup"><span data-stu-id="acf89-115">Company logo image</span></span>                                   | [<span data-ttu-id="acf89-116">png-bestand met bedrijfslogo</span><span class="sxs-lookup"><span data-stu-id="acf89-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="acf89-117">Afbeelding met handtekening</span><span class="sxs-lookup"><span data-stu-id="acf89-117">Signature image</span></span>                                      | [<span data-ttu-id="acf89-118">png-bestand met afbeelding met handtekening</span><span class="sxs-lookup"><span data-stu-id="acf89-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="acf89-119">Afbeelding met alternatieve handtekening</span><span class="sxs-lookup"><span data-stu-id="acf89-119">Alternative signature image</span></span>                          | [<span data-ttu-id="acf89-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="acf89-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="acf89-121">Microsoft Word-sjabloon voor het afdrukken van betalingscheques</span><span class="sxs-lookup"><span data-stu-id="acf89-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="acf89-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="acf89-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="acf89-123">Vereisten controleren</span><span class="sxs-lookup"><span data-stu-id="acf89-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="acf89-124">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="acf89-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="acf89-125">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief.</span><span class="sxs-lookup"><span data-stu-id="acf89-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="acf89-126">Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure "Een configuratieprovider maken en deze als actief markeren".</span><span class="sxs-lookup"><span data-stu-id="acf89-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="acf89-127">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="acf89-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="acf89-128">Een nieuwe ER-modelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="acf89-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="acf89-129">In plaats van een nieuw model te maken kunt u het ER-modelconfiguratiebestand (Model voor cheques.xml) laden dat u eerder hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="acf89-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="acf89-130">Dit bestand bevat het voorbeeldgegevensmodel voor betaalcheques en de toewijzing van het gegevensmodel aan de gegevensonderdelen van de toepassing Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="acf89-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="acf89-131">Klik op het sneltabblad Versies op Uitwisselen.</span><span class="sxs-lookup"><span data-stu-id="acf89-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="acf89-132">Klik op Laden uit XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="acf89-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="acf89-133">Klik op Bladeren en selecteer vervolgens Model voor cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="acf89-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="acf89-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="acf89-134">Click OK.</span></span>  
 6. <span data-ttu-id="acf89-135">Het geladen model wordt gebruikt als een gegevensbron met informatie voor het genereren van documenten met afbeeldingen in Excel en Word.</span><span class="sxs-lookup"><span data-stu-id="acf89-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="acf89-136">Een nieuwe ER-indelingsconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="acf89-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="acf89-137">In plaats van een nieuwe indeling te maken kunt u het ER-indelingsconfiguratiebestand (Afdrukindeling van cheques.xml) laden dat u eerder hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="acf89-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="acf89-138">Dit bestand bevat de voorbeeldindeling voor het afdrukken van cheques met behulp van het voorgedrukte formulier en de toewijzing van deze indeling voor het gegevensmodel 'Model voor cheques'.</span><span class="sxs-lookup"><span data-stu-id="acf89-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="acf89-139">Klik op Uitwisselen.</span><span class="sxs-lookup"><span data-stu-id="acf89-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="acf89-140">Klik op Laden uit XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="acf89-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="acf89-141">Klik op Bladeren en selecteer het bestand Afdrukindeling van cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="acf89-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="acf89-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="acf89-142">Click OK.</span></span>  
 6. <span data-ttu-id="acf89-143">Vouw in de structuur 'Model voor cheques' uit.</span><span class="sxs-lookup"><span data-stu-id="acf89-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="acf89-144">Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="acf89-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="acf89-145">De geladen indeling wordt gebruikt voor het genereren van documenten met afbeeldingen in Excel en Word.</span><span class="sxs-lookup"><span data-stu-id="acf89-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="acf89-146">ER-gebruikersparameters configureren</span><span class="sxs-lookup"><span data-stu-id="acf89-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="acf89-147">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="acf89-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="acf89-148">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="acf89-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="acf89-149">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="acf89-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="acf89-150">Schakel de markering 'Concept uitvoeren' in om de conceptversie van de geselecteerde indeling te starten in plaats van de voltooide.</span><span class="sxs-lookup"><span data-stu-id="acf89-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="acf89-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="acf89-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="acf89-152">Parameters voor cash- en bankbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="acf89-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="acf89-153">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="acf89-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="acf89-154">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="acf89-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="acf89-155">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="acf89-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="acf89-156">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="acf89-156">Click Check.</span></span>  
 5. <span data-ttu-id="acf89-157">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="acf89-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="acf89-158">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="acf89-158">Click Edit.</span></span>  
 7. <span data-ttu-id="acf89-159">Selecteer Ja in het veld Bedrijfslogo.</span><span class="sxs-lookup"><span data-stu-id="acf89-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="acf89-160">Klik op Bedrijfslogo.</span><span class="sxs-lookup"><span data-stu-id="acf89-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="acf89-161">Klik op Wijzigen.</span><span class="sxs-lookup"><span data-stu-id="acf89-161">Click Change.</span></span>  
 10. <span data-ttu-id="acf89-162">Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Bedrijfslogo.png.</span><span class="sxs-lookup"><span data-stu-id="acf89-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="acf89-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="acf89-163">Click Save.</span></span>  
 12. <span data-ttu-id="acf89-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="acf89-164">Close the page.</span></span>  
 13. <span data-ttu-id="acf89-165">Vouw de sectie Handtekening uit.</span><span class="sxs-lookup"><span data-stu-id="acf89-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="acf89-166">Selecteer Ja in het veld Eerste handtekening afdrukken.</span><span class="sxs-lookup"><span data-stu-id="acf89-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="acf89-167">Klik op Wijzigen.</span><span class="sxs-lookup"><span data-stu-id="acf89-167">Click Change.</span></span>  
 16. <span data-ttu-id="acf89-168">Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Afbeelding handtekening.png.</span><span class="sxs-lookup"><span data-stu-id="acf89-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="acf89-169">Vouw de sectie Aantal exemplaren uit.</span><span class="sxs-lookup"><span data-stu-id="acf89-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="acf89-170">Selecteer een optie in het veld Watermerk.</span><span class="sxs-lookup"><span data-stu-id="acf89-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="acf89-171">Selecteer Ja in het veld Algemene elektronische exportindeling.</span><span class="sxs-lookup"><span data-stu-id="acf89-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="acf89-172">Selecteer Configuratie 'afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="acf89-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="acf89-173">Nu wordt de geselecteerde ER-indeling gebruikt voor het afdrukken van cheques.</span><span class="sxs-lookup"><span data-stu-id="acf89-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="acf89-174">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="acf89-174">Click Attach.</span></span>  
 23. <span data-ttu-id="acf89-175">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="acf89-175">Click New.</span></span>  
 24. <span data-ttu-id="acf89-176">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="acf89-176">Click File.</span></span>  
 25. <span data-ttu-id="acf89-177">Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="acf89-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="acf89-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="acf89-178">Close the page.</span></span>  
 27. <span data-ttu-id="acf89-179">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="acf89-179">Close the page.</span></span>  
 28. <span data-ttu-id="acf89-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="acf89-180">Close the page.</span></span>  
 29. <span data-ttu-id="acf89-181">Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.</span><span class="sxs-lookup"><span data-stu-id="acf89-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="acf89-182">Selecteer Ja in het veld Voorafmelding maken toestaan voor inactieve bankrekeningen:.</span><span class="sxs-lookup"><span data-stu-id="acf89-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="acf89-183">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="acf89-183">Click Save.</span></span>  
 32. <span data-ttu-id="acf89-184">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="acf89-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
