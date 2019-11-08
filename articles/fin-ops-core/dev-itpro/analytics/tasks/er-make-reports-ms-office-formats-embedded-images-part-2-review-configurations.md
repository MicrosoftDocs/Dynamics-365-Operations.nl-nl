---
title: Configuraties beoordelen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten
description: "Als u deze stappen wilt voltooien, moet u eerst de stappen uitvoeren in de taakbegeleiding 'ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen (deel 1: Parameters instellen)'."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 9d05020c5b83137d977d7260e269cb7d8c219406
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184779"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="6fec0-103">Configuraties beoordelen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten</span><span class="sxs-lookup"><span data-stu-id="6fec0-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6fec0-104">Als u deze stappen wilt voltooien, moet u eerst de stappen uitvoeren in de taakbegeleiding 'ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen (deel 1: parameters instellen)'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="6fec0-105">Deze procedure laat zien hoe u elektronische rapportage (ER)-configuraties ontwerpt voor het genereren van elektronische documenten met ingesloten afbeeldingen in Microsoft Excel en Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="6fec0-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="6fec0-106">In dit voorbeeld controleert u ER-configuraties voor voorbeeldbedrijf Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6fec0-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="6fec0-107">Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="6fec0-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="6fec0-108">De stappen kunnen worden voltooid met de USMF-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="6fec0-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="6fec0-109">Het geïmporteerde gegevensmodel controleren</span><span class="sxs-lookup"><span data-stu-id="6fec0-109">Review the imported data model</span></span>
1. <span data-ttu-id="6fec0-110">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="6fec0-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6fec0-111">Selecteer in de structuur 'Model voor cheques'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="6fec0-112">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6fec0-112">Click Designer.</span></span>
    * <span data-ttu-id="6fec0-113">Dit model is ontworpen om betaalcheques voor te stellen vanuit het bedrijfsoogpunt en de toewijzing van dit model aan de gegevensbronnen van de toepassing.</span><span class="sxs-lookup"><span data-stu-id="6fec0-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="6fec0-114">Controleer dit model door de ER Operations-ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6fec0-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="6fec0-115">Let op de kenmerken van de modelelementen die worden weergegeven: structuur, naam, omschrijving, gegevenstype, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="6fec0-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="6fec0-116">Vouw in de structuur 'basis' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="6fec0-117">Selecteer in de structuur 'basis\cheques'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="6fec0-118">Vouw de structuur 'basis\cheques' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="6fec0-119">Vouw de structuur 'basis\cheques\kenmerken' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="6fec0-120">Vouw de structuur 'basis\betaler' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="6fec0-121">Selecteer in de structuur 'basis\istestrun'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="6fec0-122">Selecteer in de structuur 'basis\indeling'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="6fec0-123">Het indelingselement van dit model vertegenwoordigt de details van de afdrukindeling van het chequeformulier voor de geselecteerde bankrekening.</span><span class="sxs-lookup"><span data-stu-id="6fec0-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="6fec0-124">Het bevat ook twee knooppunten van het gegevenstype Container om afbeeldingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="6fec0-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="6fec0-125">Vouw in de structuur 'basis\indeling' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="6fec0-126">Selecteer in de structuur 'basis\indeling\bedrijfslogo'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="6fec0-127">Vouw in de structuur 'basis\indeling\bedrijfslogo' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="6fec0-128">Selecteer in de structuur 'basis\indeling\bedrijfslogo\afbeelding'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="6fec0-129">Selecteer in de structuur 'basis\indeling\bedrijfslogo\isprinted'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="6fec0-130">Selecteer in de structuur 'basis\indeling\handtekening'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="6fec0-131">Vouw in de structuur 'basis\indeling\handtekening' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="6fec0-132">Selecteer in de structuur 'basis\indeling\handtekening\afbeelding'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="6fec0-133">Selecteer in de structuur 'basis\indeling\handtekening\isprinted'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="6fec0-134">Twee afbeeldingsgegevensmodelelementen zijn gebonden aan de velden van de tabellen die afbeeldingen bevatten van het bedrijfslogo en de handtekening van de bevoegde persoon in binaire indeling.</span><span class="sxs-lookup"><span data-stu-id="6fec0-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="6fec0-135">Vouw in de structuur 'basis\indeling\watermerk' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="6fec0-136">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="6fec0-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="6fec0-137">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6fec0-137">Click Designer.</span></span>
23. <span data-ttu-id="6fec0-138">Vouw in de structuur 'chequesgeselecteerd' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="6fec0-139">Vouw in de structuur 'indeling' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="6fec0-140">Vouw in de structuur 'indeling\bedrijfslogo' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="6fec0-141">Vouw in de structuur 'indeling\handtekening' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="6fec0-142">Vouw in de structuur 'indeling\watermerk' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="6fec0-143">Schakel de optie 'Details weergeven' in.</span><span class="sxs-lookup"><span data-stu-id="6fec0-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="6fec0-144">Het chequegegevensmodelelement is gebonden aan de tabel TmpChequePrintout die tijdens runtime records bevat voor cheques die de gebruiker heeft geselecteerd om af te drukken.</span><span class="sxs-lookup"><span data-stu-id="6fec0-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="6fec0-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6fec0-145">Close the page.</span></span>
30. <span data-ttu-id="6fec0-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6fec0-146">Close the page.</span></span>
31. <span data-ttu-id="6fec0-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6fec0-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="6fec0-148">De geïmporteerde indeling controleren</span><span class="sxs-lookup"><span data-stu-id="6fec0-148">Review the imported format</span></span>
1. <span data-ttu-id="6fec0-149">Vouw in de structuur 'Model voor cheques' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="6fec0-150">Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="6fec0-151">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6fec0-151">Click Designer.</span></span>
4. <span data-ttu-id="6fec0-152">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="6fec0-152">Click Attachments.</span></span>
5. <span data-ttu-id="6fec0-153">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="6fec0-153">Click Open.</span></span>
    * <span data-ttu-id="6fec0-154">De gekoppelde sjabloon van het rapport in Excel openen.</span><span class="sxs-lookup"><span data-stu-id="6fec0-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="6fec0-155">Controleer de gekoppelde Excel-sjabloon van het rapport die wordt gebruikt voor het afdrukken van cheques.</span><span class="sxs-lookup"><span data-stu-id="6fec0-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="6fec0-156">De sjabloon bevat twee cheques per pagina en is ontworpen voor het afdrukken van cheques naar het voorgedrukte formulier.</span><span class="sxs-lookup"><span data-stu-id="6fec0-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="6fec0-157">Er zijn twee lege afbeeldingen ingesloten.</span><span class="sxs-lookup"><span data-stu-id="6fec0-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="6fec0-158">Deze lege afbeeldingen zijn voor het bedrijfslogo en de handtekening van de persoon die een betaling autoriseert.</span><span class="sxs-lookup"><span data-stu-id="6fec0-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="6fec0-159">Controleer of de afbeeldingen de naam CompLogo en SignatureImage, respectievelijk in Excel hebben.</span><span class="sxs-lookup"><span data-stu-id="6fec0-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="6fec0-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6fec0-160">Close the page.</span></span>
7. <span data-ttu-id="6fec0-161">Vouw in de structuur 'Rapport' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="6fec0-162">Vouw in de structuur 'Rapport\Chequeregels' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="6fec0-163">Selecteer in de structuur 'Rapport\Chequeregels\Bedrijfslogo'.</span><span class="sxs-lookup"><span data-stu-id="6fec0-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="6fec0-164">Schakel de optie 'Details weergeven' in.</span><span class="sxs-lookup"><span data-stu-id="6fec0-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="6fec0-165">Het celelement van de indeling 'CompLogo' vertegenwoordigt het Excel-item dat wordt gebruikt om de bedrijfslogoafbeelding te vullen in het rapport.</span><span class="sxs-lookup"><span data-stu-id="6fec0-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="6fec0-166">Dit indelingselement is gebonden aan het afbeeldingsgegevensmodelelement dat tijdens de uitvoering een bedrijfslogoafbeelding bevat in binaire indeling.</span><span class="sxs-lookup"><span data-stu-id="6fec0-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="6fec0-167">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="6fec0-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="6fec0-168">Klik op Bewerken ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6fec0-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="6fec0-169">U kunt het celelement van de indeling 'CompLogo' zo maken dat het niet meer ingeschakeld is.</span><span class="sxs-lookup"><span data-stu-id="6fec0-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="6fec0-170">In dit geval verbergt het bijbehorende Excel-afbeeldingselement een bedrijfslogo in het gegenereerde rapport.</span><span class="sxs-lookup"><span data-stu-id="6fec0-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="6fec0-171">Als de ingeschakelde expressie TRUE retourneert en de gedefinieerde binding geen afbeelding oplevert, toont het Excel-afbeeldingselement een afbeelding die is opgeslagen in de Excel-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="6fec0-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="6fec0-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6fec0-172">Close the page.</span></span>
14. <span data-ttu-id="6fec0-173">Vouw in de structuur 'labels: Container' uit.</span><span class="sxs-lookup"><span data-stu-id="6fec0-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="6fec0-174">Sommige labels die worden weergegeven in het voorgedrukte chequeformulier, worden in het rapport opgenomen wanneer het wordt gemaakt voor testdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="6fec0-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="6fec0-175">Deze labels worden echter niet afgedrukt tijdens het echte afdrukken, omdat het voorgedrukte formulier deze al bevat.</span><span class="sxs-lookup"><span data-stu-id="6fec0-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="6fec0-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6fec0-176">Close the page.</span></span>
