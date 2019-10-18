---
title: Aanbiedingsbeheer instellen
description: In dit onderwerp wordt beschreven hoe u aanbiedingen instelt in Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 706766ba5133af03d00df99dba1c2a7b0405cd86
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010839"
---
# <a name="set-up-offer-management"></a><span data-ttu-id="08c6b-103">Aanbiedingsbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="08c6b-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="08c6b-104">Wanneer een kandidaat wordt verplaatst naar de aanbiedingsfase in Dynamics 365 Talent: Attract, moet u ervoor zorgen dat de aanbiedingen snel kunnen worden gemaakt voor de kandidaat, goedgekeurd indien nodig en naar de kandidaat verzonden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="08c6b-105">Aangezien de meeste aanbiedingen standaard zijn, kunnen ze door herbruikbare sjablonen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="08c6b-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="08c6b-106">In Attract worden alle aanbiedingen in één aanbiedingspakket gecombineerd. Dat is een verzameling van een of meer aanbiedingsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="08c6b-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="08c6b-107">In dit onderwerp vindt u alle stappen die een Attract-beheerder zou volgen om verschillende aanbiedingspakketsjablonen in te stellen als onderdeel van het aanbiedingsbeheer in Attract.</span><span class="sxs-lookup"><span data-stu-id="08c6b-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="08c6b-108">Gebruikers met niet-beheerdersrollen hebben geen toegang tot deze mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="08c6b-109">Mogelijkheden voor aanbiedingsbeheer zijn beschikbaar als onderdeel van de Uitgebreide invoegtoepassing voor aanstellingen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="08c6b-110">Gegevens van aanbieding</span><span class="sxs-lookup"><span data-stu-id="08c6b-110">Offer data</span></span> 

<span data-ttu-id="08c6b-111">Aanbiedingsgegevens zijn de kleinste eenheid in de aanbiedingspakketsjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="08c6b-112">Een veel voorkomend aanbod bestaat uit standaardtekst en een set waarden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="08c6b-113">De sets waarden zijn de enige onderdelen die tussen de aanbiedingen kunnen veranderen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="08c6b-114">Tijdens het maken van de aanbieding is het belangrijkste aspect waar de maker van de aanbieding op kan focussen, de lijst met tijdelijke aanduidingen voor aanbiedingsgegevens in een aanbiedingspakketsjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="08c6b-115">Ga als volgt te werk als u aanbiedingsgegevens wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="08c6b-116">Ga naar **Aanbiedingsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="08c6b-117">Vouw de sectie **Bibliotheek** in het linkernavigatievenster uit en ga naar **Gegevens van aanbieding**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="08c6b-118">De pagina **Gegevens van aanbieding** bevat de secties **Details van kandidaat** en **Functiedetails**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="08c6b-119">Attract biedt standaard enkele tijdelijke aanduidingen voor aanbiedingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="08c6b-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="08c6b-120">Er zijn secties op de pagina waarmee u verschillende tijdelijke aanduidingen voor aanbiedingsgegevens in logische groepen kunt ordenen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="08c6b-121">Deze secties kunnen helpen bij het onderhoud van aanbiedingsgegevens en het invullen van gegevens tijdens het maken van aanbiedingen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="08c6b-122">Als u een nieuwe sectie voor aanbiedingsgegevens wilt maken, klikt u op **Een sectie toevoegen** en voert u een unieke naam voor de sectie in.</span><span class="sxs-lookup"><span data-stu-id="08c6b-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="08c6b-123">Als u tijdelijke aanduidingen voor aanbiedingsgegevens aan een sectie wilt toevoegen, klikt u op **Gegevens van aanbieding toevoegen** en voert u een unieke naam voor de tijdelijke aanduiding in.</span><span class="sxs-lookup"><span data-stu-id="08c6b-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="08c6b-124">Als u de naam van een sectie wilt bewerken, plaatst u de aanwijzer boven de sectienaam en werkt u de naam bij.</span><span class="sxs-lookup"><span data-stu-id="08c6b-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="08c6b-125">Als u de naam van een bestaande tijdelijke aanduiding voor aanbiedingsgegevens wilt bewerken, zorgt u eerst dat de tijdelijke aanduiding niet al deel uitmaakt van een sjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="08c6b-126">Vervolgens plaatst u de muisaanwijzer op de naam van de tijdelijke aanduiding voor aanbiedingsgegevens en werkt u de naam indien nodig bij.</span><span class="sxs-lookup"><span data-stu-id="08c6b-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="08c6b-127">Als u een bestaande tijdelijke aanduiding voor aanbiedingsgegevens wilt verwijderen, zorgt u eerst dat de tijdelijke aanduiding geen deel uitmaakt van een andere sjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="08c6b-128">Plaats vervolgens de muisaanwijzer op de tijdelijke aanduiding en wanneer het prullenbakpictogram wordt weergegeven, klikt u op de prullenbak om de tijdelijke aanduiding voor aanbiedingsgegevens te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="08c6b-129">U kunt zien van hoeveel sjablonen een tijdelijke aanduiding voor aanbiedingsgegevens deel uitmaakt door de getalindicator naast alle aanbiedingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="08c6b-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="08c6b-130">Als u een sectie wilt verwijderen, plaatst u de muisaanwijzer op de naam.</span><span class="sxs-lookup"><span data-stu-id="08c6b-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="08c6b-131">Als geen van de tijdelijke aanduidingen voor aanbiedingsgegevens in de sectie worden weergegeven in een sjabloon, kunt u klikken op het prullenbakpictogram om de sectie te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="08c6b-132">Als u de sectie verwijdert, verwijdert u ook alle tijdelijke aanduidingen voor aanbiedingsgegevens in die sectie.</span><span class="sxs-lookup"><span data-stu-id="08c6b-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="08c6b-133">Nadat de tijdelijke aanduidingen voor aanbiedingsgegevens zijn ingesteld, kunt u ze in elke documentsjabloon gebruiken.</span><span class="sxs-lookup"><span data-stu-id="08c6b-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="08c6b-134">Tijdelijke aanduidingen voor aanbiedingsgegevens zijn niet beperkt tot een specifieke sjabloon. Dezelfde set kan worden gebruikt in alle sjablonen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="08c6b-135">Regels aanbiedingsgegevens</span><span class="sxs-lookup"><span data-stu-id="08c6b-135">Offer data rules</span></span>

<span data-ttu-id="08c6b-136">De meeste organisaties hebben regels voor hoe aanbiedingen moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="08c6b-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="08c6b-137">Een organisatie wil bijvoorbeeld vereisen dat de maximale aanbieding voor jaarsalaris voor een bepaalde combinatie van vestiging en anciënniteitsniveau ligt in een bepaald bereik, of dat er slechts enkele waarden mogelijk zijn voor het aanbiedingsniveau van de nieuwe aanstelling.</span><span class="sxs-lookup"><span data-stu-id="08c6b-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="08c6b-138">Attract ondersteunt momenteel al dergelijke gegevens met behulp van een CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="08c6b-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="08c6b-139">Ga als volgt te werk om het CSV-bestand met gegevensregels voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="08c6b-140">Bepaal de tijdelijke aanduiding voor aanbiedingsgegevens voor de regelset.</span><span class="sxs-lookup"><span data-stu-id="08c6b-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="08c6b-141">Bijvoorbeeld **Jaarsalaris**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="08c6b-142">Bepaal de afhankelijke waarden voor de tijdelijke aanduiding voor aanbiedingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="08c6b-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="08c6b-143">Bijvoorbeeld **Functielocatie** en **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="08c6b-144">Geef kolommen 1 en 2 op als **Functielocatie** en **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="08c6b-145">Als u een bereikwaarde wilt uploaden, maakt u van kolom 3 en 4 **Jaarsalaris**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="08c6b-146">Als u een specifieke waarde wilt uploaden in plaats van een bereik, maakt u alleen van kolom 3 **Jaarsalaris**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="08c6b-147">Vul het Microsoft Excel-bestand in op basis van uw vereiste rollen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="08c6b-148">Zorg ervoor dat elke rij een unieke combinatie van de gezamenlijke waarden is.</span><span class="sxs-lookup"><span data-stu-id="08c6b-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="08c6b-149">Sla het bestand op in CSV-indeling.</span><span class="sxs-lookup"><span data-stu-id="08c6b-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="08c6b-150">Ga als volgt te werk om het bestand met gegevensregels te uploaden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="08c6b-151">Ga naar **Aanbiedingsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="08c6b-152">Vouw de sectie **Bibliotheek** in het linkernavigatievenster uit en ga naar **Regels aanbiedingsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="08c6b-153">Klik op **Nieuwe gegevensset** om het dialoogvenster **Uploaden** te openen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="08c6b-154">Geef een unieke naam voor de regelset op en upload vervolgens het opgeslagen CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="08c6b-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="08c6b-155">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-155">Click **Add**.</span></span>
    <span data-ttu-id="08c6b-156">De regelset wordt verwerkt op de achtergrond en u wordt in de app en per e-mail geïnformeerd zodra het is voltooid.</span><span class="sxs-lookup"><span data-stu-id="08c6b-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="08c6b-157">U wordt gewaarschuwd als er fouten zijn opgetreden tijdens het uploaden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="08c6b-158">U kunt vervolgens het foutenlogboek downloaden, het bestand herstellen en opnieuw uploaden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="08c6b-159">Gebruik de knop met weglatingstekens (**...**) als u de regelset wilt downloaden en de set waarden wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="08c6b-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="08c6b-160">Nadat u hebt bijgewerkt, kunt u het bestand opnieuw uploaden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="08c6b-161">U kunt een bestaande regelsetupload verwijderen als de tijdelijke aanduiding die wordt gedefinieerd, niet wordt gebruikt in een andere documentsjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="08c6b-162">Elke tijdelijke aanduiding kan slechts één unieke set kolommen hebben waarvan deze afhankelijk is.</span><span class="sxs-lookup"><span data-stu-id="08c6b-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="08c6b-163">Bijvoorbeeld als **Jaarsalaris** afhankelijk is van **Functielocatie** en **Niveau**, kunt u geen andere regelset uploaden waarin **Jaarsalaris** afhankelijk is van een andere set kolommen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="08c6b-164">U kunt gegevenssets met voorbeeldaanbiedingsgegevens downloaden op het tabblad **Voorbeelden** op de pagina **Regels aanbiedingsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="08c6b-165">Wanneer de maker van een aanbieding de waarden overschrijft die worden aanbevolen door de aanbiedingsgegevensregels, wordt de aanbieding gemarkeerd als niet-standaard en is een werkstroom voor aanbiedingsgoedkeuring verplicht.</span><span class="sxs-lookup"><span data-stu-id="08c6b-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="08c6b-166">Documentsjablonen</span><span class="sxs-lookup"><span data-stu-id="08c6b-166">Document templates</span></span>

<span data-ttu-id="08c6b-167">Een aanbiedingsdocumentsjabloon kan beheerders helpen aanbiedingsbrieven te maken.</span><span class="sxs-lookup"><span data-stu-id="08c6b-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="08c6b-168">De aanbiedingsdocumentsjabloon is een combinatie van de tekst die deel van de aanbieding uitmaakt, en de gedefinieerde tijdelijke aanduidingen voor aanbiedingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="08c6b-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="08c6b-169">Ga als volgt te werk voor het maken van een aanbiedingsdocumentsjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="08c6b-170">Ga naar **Aanbiedingsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="08c6b-171">Vouw de sectie **Bibliotheek** in het linkernavigatievenster uit en ga naar **Sjablonen**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="08c6b-172">De pagina **Sjablonen** bevat een lijst met documentsjablonen die al zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="08c6b-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="08c6b-173">Als u een nieuwe documentsjabloon wilt maken, klikt u op **Nieuwe sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="08c6b-174">Voer een unieke naam voor de sjabloon in en klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="08c6b-175">Gebruik de RTF-editor om de inhoud van het aanbiedingsdocument in te voegen of te bewerken.</span><span class="sxs-lookup"><span data-stu-id="08c6b-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="08c6b-176">U kunt tabellen, afbeeldingen en hyperlinks invoegen met de beschikbare opties boven in de teksteditor.</span><span class="sxs-lookup"><span data-stu-id="08c6b-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="08c6b-177">U kunt tijdelijke aanduidingen voor aanbiedingsgegevens in het aanbiedingssjabloondocument invoegen door:</span><span class="sxs-lookup"><span data-stu-id="08c6b-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="08c6b-178">Slepen en neerzetten vanuit het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="08c6b-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="08c6b-179">De tijdelijke aanduiding voor aanbiedingsgegevens op de positie hashtaggen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="08c6b-180">Typ **\#** en begin de naam van de tijdelijke aanduiding voor aanbiedingsgegevens te typen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="08c6b-181">Opties worden weergegeven in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="08c6b-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="08c6b-182">Klik of druk op **Enter** om de tijdelijke aanduiding voor aanbiedingsgegevens in te voegen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="08c6b-183">Als u een tijdelijke aanduiding voor aanbiedingsgegevens aan de documentsjabloon wilt koppelen zonder de waarde ervan aan de kandidaat te tonen, plaatst u de muisaanwijzer op de tijdelijke aanduiding voor aanbiedingsgegevens en klikt u op het pictogram **Vastmaken**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="08c6b-184">Hiermee wordt de tijdelijke aanduiding vastgemaakt aan de sectie **Vastgemaakte aanbiedingsgegevens** van de aanbiedingsdocumentsjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="08c6b-185">Als u de tijdelijke aanduiding wilt losmaken, volgt u dezelfde stappen maar klikt u op **Losmaken** in de lijst met tijdelijke aanduidingen voor aanbiedingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="08c6b-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="08c6b-186">Als u de lijst met actieve tijdelijke aanduidingen voor aanbiedingsgegevens wilt weergeven, schakelt u over op het tabblad **Actief** in het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="08c6b-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="08c6b-187">Als u een tijdelijke aanduiding invoegt die wordt aangestuurd door een regelset voor aanbiedingsgegevens, ziet u de afhankelijkheid van die tijdelijke aanduiding voor aanbiedingsgegevens van andere waarden.</span><span class="sxs-lookup"><span data-stu-id="08c6b-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="08c6b-188">U kunt ook de inhoud uit een .docx-bestand op uw lokale computer **importeren** en indien nodig bewerken.</span><span class="sxs-lookup"><span data-stu-id="08c6b-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="08c6b-189">Op die manier hoeft u niet alle content te typen in de editor.</span><span class="sxs-lookup"><span data-stu-id="08c6b-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="08c6b-190">Als u een voorbeeld van het document wilt bekijken, gebruikt u de optie **Voorbeeld** boven aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="08c6b-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="08c6b-191">Als u wilt bepalen of de maker van een aanbieding de inhoud van het aanbiedingsdocument kan bewerken, gebruikt u de optie **Machtiging beheren** boven aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="08c6b-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="08c6b-192">Als u wilt dat de maker van de aanbieding alleen waarden van tijdelijke aanduidingen kan invoegen en geen tekst kan bewerken, stelt u de machtigingswaarde in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="08c6b-193">Klik op **Opslaan** om uw voortgang op te slaan.</span><span class="sxs-lookup"><span data-stu-id="08c6b-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="08c6b-194">De sjabloon wordt opgeslagen in een conceptstaat.</span><span class="sxs-lookup"><span data-stu-id="08c6b-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="08c6b-195">Als u het document wilt voltooien en wilt markeren als gepubliceerd, klikt u op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="08c6b-196">Op de landingspagina van de documentsjabloonbibliotheek kunt u zien welke documentsjablonen momenteel actief zijn, zich in de conceptmodus bevinden en zijn gearchiveerd en niet langer in gebruik zijn.</span><span class="sxs-lookup"><span data-stu-id="08c6b-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="08c6b-197">U kunt elke aanbiedingsdocumentsjabloon verwijderen die geen deel uitmaakt van een bestaande aanbiedingspakketsjabloon.</span><span class="sxs-lookup"><span data-stu-id="08c6b-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="08c6b-198">Pakketsjablonen aanbieden</span><span class="sxs-lookup"><span data-stu-id="08c6b-198">Offer package templates</span></span>

<span data-ttu-id="08c6b-199">Aanbiedingspakketten zijn de aanbiedingsartefacten die worden gedeeld met de kandidaat en bestaan uit een combinatie van een of meer aanbiedingsdocumentsjablonen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="08c6b-200">Ga als volgt te werk voor het maken van een aanbiedingspakket.</span><span class="sxs-lookup"><span data-stu-id="08c6b-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="08c6b-201">Ga naar **Aanbiedingsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="08c6b-202">Ga naar **Pakketten** in het linkernavigatievenster.</span><span class="sxs-lookup"><span data-stu-id="08c6b-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="08c6b-203">Een lijst met actieve pakketsjablonen die beschikbaar zijn voor makers van aanbiedingen, wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="08c6b-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="08c6b-204">Als u een nieuw aanbiedingspakket wilt maken, klikt u op **Nieuw pakket**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="08c6b-205">Voer een unieke naam in en klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="08c6b-206">Klik op **Sjabloon toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="08c6b-207">U kunt een nieuwe sjabloon te maken of een bestaande kiezen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="08c6b-208">Als u een bestaande sjabloon toevoegt, moet u zorgen dat de aanbiedingsdocumentsjabloon is opgeslagen, is voltooid, en als actief is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="08c6b-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="08c6b-209">U kunt zoveel documentsjablonen kiezen als u wilt.</span><span class="sxs-lookup"><span data-stu-id="08c6b-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="08c6b-210">Klik op **Gereed** om terug te keren naar **Pakketbeheer**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="08c6b-211">U kunt de volgorde van de documenten configureren en ook markeren of het specifieke aanbiedingsdocument tijdens het maken van de aanbieding vereist is.</span><span class="sxs-lookup"><span data-stu-id="08c6b-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="08c6b-212">De maker van de aanbieding heeft de optie de documenten te verwijderen die zijn gemarkeerd als **Niet verplicht**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="08c6b-213">Als u de aanbiedingspakketsjabloon wilt opslaan, zodat deze bruikbaar is voor alle makers van aanbiedingen, klikt u op **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="08c6b-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="08c6b-214">Als u concepten van aanbiedingspakketsjablonen wilt zien, gaat u naar het tabblad **Concepten**. Als een wijziging wordt aangebracht in de aanbiedingspakketsjabloon, moet deze worden opgeslagen er opnieuw worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="08c6b-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="08c6b-215">Een aanbiedingsproces configureren</span><span class="sxs-lookup"><span data-stu-id="08c6b-215">Configure an offer process</span></span>

<span data-ttu-id="08c6b-216">Er zijn verschillende onderdelen van het proces voor het maken van een aanbieding die kunnen worden geconfigureerd door de beheerder van Attract.</span><span class="sxs-lookup"><span data-stu-id="08c6b-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="08c6b-217">**Aanbiedingsgoedkeuringen**: kies of aanbiedingsgoedkeuringen vereist zijn voordat de aanbieding kan worden verzonden naar de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="08c6b-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="08c6b-218">Als beheerder kunt u ook besluiten of alle aanbiedingsgoedkeuringen sequentieel plaatsvinden of in een parallelle goedkeuringswerkstroom.</span><span class="sxs-lookup"><span data-stu-id="08c6b-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="08c6b-219">U kunt ook vereisen dat goedkeurders van aanbiedingen een opmerking toevoegen met hun goedkeuring van de aanbieding.</span><span class="sxs-lookup"><span data-stu-id="08c6b-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="08c6b-220">Goedkeuringen van aanbiedingen zijn verplicht voor alle niet-standaard aanbiedingen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="08c6b-221">**Aanbieding van kandidaat**: als beheerder kunt u kiezen of alle aanbiedingen een verloopdatum hebben en zo ja, wat de standaard voor de vervaldatum moet zijn.</span><span class="sxs-lookup"><span data-stu-id="08c6b-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="08c6b-222">U kunt ook configureren of kandidaten een aanbieding kunnen afwijzen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="08c6b-223">**Elektronische handtekeningen**: als beheerder kunt u de methode kiezen waarmee kandidaten aanbiedingen kunnen ondertekenen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="08c6b-224">Adobe Sign: alle aanbiedingspakketten worden verzonden en ondertekend via Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="08c6b-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="08c6b-225">Alle makers van aanbiedingen die de aanbieding willen publiceren, moeten hun Adobe Sign-account hebben verbonden met Attract.</span><span class="sxs-lookup"><span data-stu-id="08c6b-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="08c6b-226">Ga voor Adobe Sign-licenties en een gratis proefversie deze [koppeling](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="08c6b-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="08c6b-227">DocuSign: alle aanbiedingspakketten worden verzonden en ondertekend via DocuSign.</span><span class="sxs-lookup"><span data-stu-id="08c6b-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="08c6b-228">Alle makers van aanbiedingen die de aanbieding willen publiceren, moeten hun DocuSign-account hebben verbonden met Attract.</span><span class="sxs-lookup"><span data-stu-id="08c6b-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="08c6b-229">ESign: dit is de standaardoptie, die kant en klaar wordt geleverd, waarmee de gebruiker een aanbod kan ondertekenen door zijn/haar naam en initialen te typen.</span><span class="sxs-lookup"><span data-stu-id="08c6b-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="08c6b-230">Als u meer wilt weten over het maken van aanbiedingen, raadpleegt u [Aanbiedingen maken, goedkeuren en ondertekenen](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="08c6b-230">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
