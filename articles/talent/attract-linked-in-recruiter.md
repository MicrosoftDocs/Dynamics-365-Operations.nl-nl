---
title: Aanstelling met LinkedIn Recruiter
description: Dit onderwerp biedt informatie over het gebruik van machine learning om aanbevelingen voor functies en functiekandidaten te krijgen.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.contentlocale: nl-nl
ms.lasthandoff: 12/07/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="b4a7c-103">Aanstelling met LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="b4a7c-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="b4a7c-104">LinkedIn is 's werelds grootste talentendatabase en vaak het primaire systeem dat wervers gebruiken om kandidaten te zoeken, mee te communiceren en aan te stellen voor de functies die wervers willen opvullen.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="b4a7c-105">LinkedIn Recruiter-integratie met Dynamics 365 for Talent: Attract maakt het eenvoudiger voor gebruikers om personen aan te stellen en de gegevens tussen twee systemen gesynchroniseerd te houden.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="b4a7c-106">U hebt de Uitgebreide invoegtoepassing voor aanstellingen- en LinkedIn Recruiter-seats nodig om LinkedIn Recruiter-integratie met Attract te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="b4a7c-107">LinkedIn Recruiter instellen met Attract</span><span class="sxs-lookup"><span data-stu-id="b4a7c-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="b4a7c-108">Voordat u de mogelijkheden van LinkedIn Recruiter gebruiken kunt, moet u toegang op contract- of bedrijfsniveau configureren met uw Attract-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="b4a7c-109">Als u het configuratieproces wilt voltooien, moet u werken met de gebruiker die een beheerder is in uw LinkedIn Recruiter-contract.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="b4a7c-110">Voer de volgende stappen uit voor het configureren van de LinkedIn Recruiter met Attract.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="b4a7c-111">Meld u aan bij Attract als beheerder en ga naar **Beheerinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="b4a7c-112">Klik in het linkerdeelvenster op het tabblad **LinkedIn-integratie**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="b4a7c-113">[![Attract-beheerweergave om LinkedIn Recruiter-integratie te starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="b4a7c-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="b4a7c-114">Klik op **Verbinden** om de instelling te starten en te worden begeleid door het aanmeldingsproces voor LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="b4a7c-115">Als u seats in meerdere LinkedIn-contracten hebt, selecteert u het contract dat u wilt verbinden met het Attract-systeem.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="b4a7c-116">Als u een seat in slechts één LinkedIn-contract hebt, is deze stap niet nodig.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="b4a7c-117">De LinkedIn-widget wordt nu geladen in uw beheerinstellingen met de lijst van weergegeven integraties.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="b4a7c-118">Klik onder **Verbinding met Recruiter-systeem** op **Aanvragen**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="b4a7c-119">[![Attract-beheerweergave om LinkedIn Recruiter-integratie aan te vragen](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b4a7c-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="b4a7c-120">Nadat de integratie is aangevraagd vanuit Attract, wordt **Partner gereed** weergegeven en kan het worden ingeschakeld vanuit **Recruiter-beheerinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="b4a7c-121">Als u **Partner waarschuwen** op deze pagina ziet, wacht u enkele seconden, klikt u op **Partner waarschuwen** en vernieuwt u de pagina.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="b4a7c-122">Het wordt nu weergegeven als **Partner gereed**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="b4a7c-123">[![Attract-beheerweergave om aan te geven dat de Attract-zijde van aanvragen is voltooid](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b4a7c-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="b4a7c-124">Als u de volgende stap wilt uitvoeren, hebt u een beheerdersbevoegdheid nodig in uw LinkedIn Recruiter-contract.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="b4a7c-125">Meld u bij LinkedIn aan met het beheerdersaccount en ga rechtsboven naar LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="b4a7c-126">Klik in het menu **meer** boven aan het scherm op **Beheerinstellingen** en klik vervolgens op het tabblad **ATS**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="b4a7c-127">Het Attract-systeem wordt weergegeven met een aantal opties die kunnen worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="b4a7c-128">Als u alleen met 1 klik exporteren voor de **In-ATS-indicator** en de **In-ATS-profielwidget** wilt inschakelen, selecteert u **Toegang op bedrijfsniveau**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="b4a7c-129">Als u alle toegangsfuncties op bedrijfsniveau plus InMail-historie, notitiehistorie en de InMail-stub profieltoegang wilt inschakelen, selecteert u **Toegang op contractniveau**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="b4a7c-130">Schakel het gewenste toegangsniveau vanuit uw LinkedIn Recruiter **Admin-ATS**-instellingen in.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="b4a7c-131">[![Attract-integratie inschakelen vanuit LinkedIn Recruiter-beheerweergave](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b4a7c-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="b4a7c-132">Ga terug naar de Attract-beheerinstellingen als AttractAdmin en selecteer het tabblad **LinkedIn integratie**. U moet nu bij laden van de LinkedIn-widget **Ingeschakeld** zien met het geselecteerde toegangsniveau ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="b4a7c-133">[![LinkedIn Recruiter-integratie voltooid](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="b4a7c-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="b4a7c-134">LinkedIn Recruiter-mogelijkheden gebruiken</span><span class="sxs-lookup"><span data-stu-id="b4a7c-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="b4a7c-135">Nadat LinkedIn Recruiter-mogelijkheden zijn ingeschakeld door de Attract-beheerder, is het beschikbaar voor toegang door aanstellend managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="b4a7c-136">Als u deze mogelijkheden wilt gebruiken, verbindt u uw LinkedIn-account onder **Gebruikersinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="b4a7c-137">Diverse mogelijkheden zijn beschikbaar nadat zowel de beheerders als gebruikersinstellingen zijn verbonden.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="b4a7c-138">In-ATS-profielwidget</span><span class="sxs-lookup"><span data-stu-id="b4a7c-138">In-ATS profile widget</span></span>

<span data-ttu-id="b4a7c-139">U kunt het LinkedIn-profiel van de kandidaat in Attract weergeven.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="b4a7c-140">De LinkedIn-widget geeft het kandidaatprofiel weer wanneer de ATS-informatie overeenkomt met de LinkedIn-informatie van de gebruikers.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="b4a7c-141">Als u een profiel wilt weergeven, gaat u naar het kandidaatprofiel vanuit een functie of talentenpool.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="b4a7c-142">Selecteer in het kandidaatprofiel het tabblad **LinkedIn** en de profielwidget wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="b4a7c-143">U kunt vanaf deze pagina ook de kandidaat opslaan in uw LinkedIn Recruiter-projecten.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="b4a7c-144">Als LinkedIn de match heeft gevonden op basis van de e-mail- en lid-id voor LinkedIn (exacte match), wordt het kandidaatprofiel weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="b4a7c-145">De gebruiker heeft nog steeds de optie om het profiel te koppelen of ontkoppelen.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="b4a7c-146">Als de kandidaat niet kan worden gevonden op basis van de e-mail- of lid-id, wordt er een lijst met mogelijke kandidaten weergegeven op basis van de naam van de kandidaat en kan de gebruiker er hiervan één kiezen en het profiel koppelen.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="b4a7c-147">Als er geen kandidaten kunnen worden gevonden op basis van de naam, wordt aangegeven dat er geen match is gevonden.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="b4a7c-148">Met 1 klik exporteren</span><span class="sxs-lookup"><span data-stu-id="b4a7c-148">1-click export</span></span> 

<span data-ttu-id="b4a7c-149">Tijdens het zoeken van kandidaten in LinkedIn, kunt u de kandidaat met 1 klik exporteren naar de functies die u momenteel open hebt.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="b4a7c-150">Volg de volgende stappen voor een export met 1 klik.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="b4a7c-151">Controleer voordat u deze stappen uitvoert of aan u de rol van Aanstellend manager of Werver voor de functie is toegewezen en of de functie de fase **Prospect** heeft.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="b4a7c-152">Maak de functie, wijs de juiste rollen toe en activeer de functie.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="b4a7c-153">Wanneer de functie is geactiveerd, gaat u naar LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="b4a7c-154">Zoek de gewenste kandidaat en ga naar zijn of haar profiel.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="b4a7c-155">Zoek de functie met het functiezoekvak op de contactkaart aan de hand van de titel of de functie-id die is geactiveerd in Attract.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="b4a7c-156">Als u de functie niet kunt vinden, klikt u op **ATS wijzigen** om het juiste Attract-exemplaar te zoeken.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="b4a7c-157">Nadat de functie is geselecteerd, klikt u op **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="b4a7c-158">De kandidaat wordt nu opgehaald door Attract.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="b4a7c-159">Ga naar Attract en open de desbetreffende functie.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="b4a7c-160">U vindt de kandidaat die u zojuist hebt geëxporteerd, in de fase **Prospect** van de functie.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="b4a7c-161">In-ATS-indicator</span><span class="sxs-lookup"><span data-stu-id="b4a7c-161">In-ATS indicator</span></span> 

<span data-ttu-id="b4a7c-162">Met LinkedIn Recruiter kunt u bijhouden of een kandidaat naar andere functies in uw organisatie heeft gesolliciteerd, kijken waar hij of zij zich in verschillende fasen van sollicitaties bevindt en de feedback en opmerkingen vanuit Attract in LinkedIn Recruiter lezen.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="b4a7c-163">Open LinkedIn Recruiter en zoek het kandidaatprofiel dat u zoekt.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="b4a7c-164">Schuif omlaag om de sectie **In-ATS** weer te geven in het profiel van de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="b4a7c-165">U kunt deze widget gebruiken om alle informatie over de kandidaat die in Attract aanwezig is, weer te geven in de LinkedIn Recruiter-weergave.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="b4a7c-166">Selecteer het tabblad **Functies en statussen** om functies te zien waarvan ze deel uitmaken, de laatste status te zien en te zien hoe ze in elke functie zijn gegaan.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="b4a7c-167">Selecteer het tabblad **Feedback sollicitatiegesprek** om feedback te zien die de interviewers in Attract hebben ingediend.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="b4a7c-168">Selecteer het tabblad **Notities** om notities te zien die zijn vastgelegd voor deze sollicitant in Attract.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="b4a7c-169">Kandidaats- en sollicitatiegegevens worden niet gesynchroniseerd met LinkedIn Recruiter als de kandidaat niet voorbij de prospectfase komt.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="b4a7c-170">InMail-historie</span><span class="sxs-lookup"><span data-stu-id="b4a7c-170">InMail history</span></span>

<span data-ttu-id="b4a7c-171">De LinkedIn InMail-historie is beschikbaar met toegang op contractniveau met LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b4a7c-172">Als dit is ingeschakeld, kunt u uw volledige InMail-historie weergeven met de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="b4a7c-173">U kunt ook zien wie er verder in uw organisatie InMail heeft uitgewisseld met de kandidaat, maar u kunt de berichten tussen hen niet weergeven.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="b4a7c-174">Als u InMail-historie wilt weergeven, gaat u naar het profiel van een kandidaat, gaat u naar het tabblad **LinkedIn** en schuift u naar de onderzijde van de pagina om de historie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b4a7c-175">Als u een discussie met de kandidaat hebt gehad, kunt u de InMail-historie bekijken.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="b4a7c-176">De berichten vanuit InMail worden elke paar uur met Attract gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="b4a7c-177">Notitiehistorie</span><span class="sxs-lookup"><span data-stu-id="b4a7c-177">Notes history</span></span> 

<span data-ttu-id="b4a7c-178">De LinkedIn-notitiehistorie is beschikbaar met toegang op contractniveau met LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b4a7c-179">Als het is ingeschakeld, kunt u de notities weergeven die zijn vastgelegd over de kandidaat door verschillende wervers uit uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="b4a7c-180">Als u notitiehistorie wilt weergeven, gaat u naar het profiel van een kandidaat, gaat u naar het tabblad **LinkedIn** en schuift u naar de onderzijde van de pagina om de historie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b4a7c-181">U kunt alle notities over de kandidaat weergeven vanuit LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="b4a7c-182">InMail-stubprofiel</span><span class="sxs-lookup"><span data-stu-id="b4a7c-182">InMail stub profile</span></span>

<span data-ttu-id="b4a7c-183">Het InMail-stubprofiel is beschikbaar met toegang op contractniveau met LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b4a7c-184">Als kandidaten ermee instemmen hun LinkedIn-profiel te delen met een gebruiker in uw organisatie, kunt u de kandidaten in Attract bijhouden en wordt een nieuwe kandidaatrecord voor elke kandidaat gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="b4a7c-185">U kunt het e-mailadres van de kandidaat weergeven als de kandidaat al in het systeem bestaat met een e-mailadres of ervoor heeft gekozen om zijn of haar adres te delen met de werver.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="b4a7c-186">Als u de lijst met kandidaten wilt weergeven, gaat u naar **Talentenpools** om een door het systeem gemaakte LinkedIn-talentenpool te zien.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="b4a7c-187">Deze talentenpool bevat de lijst met kandidaten en hun stubprofielen, zoals ontvangen van LinkedIn, met de voornaam en achternaam van de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="b4a7c-188">De e-mail-id van de kandidaat wordt weergegeven als de kandidaat ervoor heeft gekozen zijn of haar e-mailadres te delen.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

