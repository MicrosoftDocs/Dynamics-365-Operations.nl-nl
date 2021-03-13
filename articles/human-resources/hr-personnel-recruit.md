---
title: Kandidaten werven
description: In dit onderwerp wordt beschreven hoe u kandidaten werft in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f615584785ba48a140e4e97991a4594047fea8ee
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112001"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="ce68a-103">Kandidaten werven</span><span class="sxs-lookup"><span data-stu-id="ce68a-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ce68a-104">Met Dynamics 365 Human Resources kunt u wervingsaanvragen te beheren.</span><span class="sxs-lookup"><span data-stu-id="ce68a-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="ce68a-105">Ook kunt u met dit programma sollicitanten naadloos omzetten in werknemers.</span><span class="sxs-lookup"><span data-stu-id="ce68a-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="ce68a-106">Als uw organisatie gebruikmaakt van een afzonderlijke wervingsapplicatie, kan uw wervingsproces de volgende stappen bevatten:</span><span class="sxs-lookup"><span data-stu-id="ce68a-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="ce68a-107">Uw wervingsaanvraag invoeren in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce68a-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="ce68a-108">Kandidaat-verwijzingen ontvangen in Human Resources vanuit de wervingsapplicatie.</span><span class="sxs-lookup"><span data-stu-id="ce68a-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="ce68a-109">Het goedkeuringsproces voor kandidaten in voltooien in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce68a-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="ce68a-110">Als u geen afzonderlijke wervingsapplicatie gebruikt, kunt u de kandidaten ook handmatig beheren in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce68a-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="ce68a-111">Zie [Dataverse-integratie configureren](hr-admin-integration-common-data-service.md) en [Virtuele Dataverse-tabellen configureren](hr-admin-integration-common-data-service-virtual-entities.md) als u een beheerder of ontwikkelaar bent en u Human Resources wilt integreren met een wervingsapplicatie van derden.</span><span class="sxs-lookup"><span data-stu-id="ce68a-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="ce68a-112">U kunt ook apps voor wervingsintegratie vinden op [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="ce68a-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="ce68a-113">Zie [Integratie met LinkedIn Talent Hub](hr-admin-integration-linkedin.md) voor informatie over het gebruik van de preview-functie voor integratie met LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="ce68a-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="ce68a-114">Wervingsaanvragen inschakelen</span><span class="sxs-lookup"><span data-stu-id="ce68a-114">Enable recruiting requests</span></span>

<span data-ttu-id="ce68a-115">Als u wervingsaanvragen in Human Resources wilt verzenden, moet u eerst de functionaliteit **Gedeelde Human Resources-parameters** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ce68a-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="ce68a-116">In de werkruimte **Personeelsbeheer** selecteert u **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="ce68a-117">Selecteer onder **Instellen** de optie **Gedeelde Human Resources-parameters**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="ce68a-118">Op het tabblad **Werving** onder **WERVING**, stelt u **Wervingsaanvragen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="ce68a-119">De locatie van een wervingsaanvraag toevoegen</span><span class="sxs-lookup"><span data-stu-id="ce68a-119">Add a recruiting request location</span></span>

<span data-ttu-id="ce68a-120">Als uw organisatie meerdere locaties heeft, kunt u deze toevoegen zodat aanvragers een locatie kunnen selecteren waar de nieuwe werving actief is.</span><span class="sxs-lookup"><span data-stu-id="ce68a-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="ce68a-121">De locatie wordt opgenomen in de vacaturebeschrijving.</span><span class="sxs-lookup"><span data-stu-id="ce68a-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="ce68a-122">Voer in de zoekbalk **Locatie voor wervingsaanvraag** in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="ce68a-123">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-123">Select **New**.</span></span>

3. <span data-ttu-id="ce68a-124">Voer in het veld **Locatie voor wervingsaanvraag** de locatienaam in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![De locatie van een wervingsaanvraag toevoegen](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="ce68a-126">Voer in het veld **Omschrijving** een omschrijving voor de locatie in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="ce68a-127">Selecteer **Locatie** onder **Producten**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="ce68a-128">Als het venster **Nieuw adres** verschijnt, voert u het adres voor de locatie in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Adres invoeren](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="ce68a-130">Voer onder **Contactgegevens** de gegevens in voor de contactpersoon van de locatie.</span><span class="sxs-lookup"><span data-stu-id="ce68a-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="ce68a-131">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="ce68a-132">Een wervingsaanvraag toevoegen</span><span class="sxs-lookup"><span data-stu-id="ce68a-132">Add a recruiting request</span></span>

<span data-ttu-id="ce68a-133">Managers kunnen wervingsverzoeken indienen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce68a-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="ce68a-134">Als u een afzonderlijke wervingsapplicatie gebruikt, zal het uitvoeren van deze stappen een wervingsaanvraag verzenden en het wervingsproces starten in die applicatie.</span><span class="sxs-lookup"><span data-stu-id="ce68a-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="ce68a-135">Voer anders deze procedure uit om de workflow te starten voor uw eigen interne wervingsproces.</span><span class="sxs-lookup"><span data-stu-id="ce68a-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="ce68a-136">Selecteer **Werknemerselfservice**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="ce68a-137">Selecteer het tabblad **Mijn team**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="ce68a-138">Selecteer **Wervingsaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-138">Select  **Request to recruit**.</span></span>

   ![Een wervingsaanvraag starten](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="ce68a-140">Vul de velden **Omschrijving**, **Vacature** en **Geschatte begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![De wervingsaanvraag voltooien](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="ce68a-142">Selecteer **Continue**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-142">Select **Continue**.</span></span> <span data-ttu-id="ce68a-143">De wervingsaanvraag voor uw functie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce68a-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="ce68a-144">Selecteer onder **Algemeen** een werver uit de keuzelijst **Werver** en selecteer een locatie in de **Locatie voor wervingsaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="ce68a-145">Wijzig onder **Vacature** de benodigde informatie en selecteer **Details uit vacature aanmaken**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Details van taak maken](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="ce68a-147">De rest van het wervingsverzoek wordt gevuld met de standaardinformatie over de vacature die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce68a-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="ce68a-148">Voer onder **Externe omschrijving** een externe vacatureomschrijving in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="ce68a-149">Selecteer onder **Functies** de optie **Toevoegen** en selecteer vervolgens een functie voor deze wervingsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="ce68a-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Een functie toevoegen](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="ce68a-151">Selecteer onder **Vaardigheden** **Toevoegen** en selecteer vervolgens een vaardigheid.</span><span class="sxs-lookup"><span data-stu-id="ce68a-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="ce68a-152">Selecteer onder **Opleidingseisen** **Toevoegen** en vervolgens waarden uit de vervolgkeuzelijsten **Opleiding** en **Opleidingsniveau**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Opleidingseisen toevoegen](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="ce68a-154">Voeg onder **Opmerkingen** opmerkingen toe indien nodig.</span><span class="sxs-lookup"><span data-stu-id="ce68a-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="ce68a-155">Selecteer onder **Compensatie** een niveau in de vervolgkeuzelijst **Niveau** en wijzig vervolgens de **Lage drempelwaarde**, het **Controlepunt** en **Hoge drempelwaarde** indien nodig.</span><span class="sxs-lookup"><span data-stu-id="ce68a-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="ce68a-156">Wanneer uw wervingsaanvraag is voltooid en u klaar bent om het wervingsproces te starten, selecteert u **Activeren** in de menubalk.</span><span class="sxs-lookup"><span data-stu-id="ce68a-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Wervingsaanvraag activeren](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="ce68a-158">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="ce68a-159">Uw wervingsaanvragen weergeven en bewerken</span><span class="sxs-lookup"><span data-stu-id="ce68a-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="ce68a-160">Als u manager bent en u uw eigen aanvragen wilt bekijken, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="ce68a-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="ce68a-161">Selecteer **Werknemerselfservice**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="ce68a-162">Selecteer het tabblad **Mijn team**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="ce68a-163">Selecteer onder **Mijn teamgegevens** het tabblad **Wervingsaanvragen**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Selecteer het tabblad Wervingsaanvragen](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="ce68a-165">Als u een wervingsaanvraag wilt weergeven of bewerken, selecteert u deze in het raster.</span><span class="sxs-lookup"><span data-stu-id="ce68a-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="ce68a-166">Als u een HR-professional bent en alle wervingsaanvragen wilt bekijken, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="ce68a-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="ce68a-167">Selecteer **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="ce68a-168">Selecteer **Wervingsaanvragen**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-168">Select **Recruiting requests**.</span></span>

   ![Wervingsaanvragen weergeven in Personeelsbeheer](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="ce68a-170">Als u een wervingsaanvraag wilt weergeven of bewerken, selecteert u deze in het raster.</span><span class="sxs-lookup"><span data-stu-id="ce68a-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="ce68a-171">Een kandidaatprofiel toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="ce68a-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="ce68a-172">Als uw organisatie is geïntegreerd met een andere toepassing om wervingsaanvragen te beheren, worden deze doorgestuurd naar die toepassing.</span><span class="sxs-lookup"><span data-stu-id="ce68a-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="ce68a-173">De wervingstoepassing stuurt vervolgens informatie over kandidaten terug naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce68a-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="ce68a-174">Anders kunt u uw eigen interne wervingsprocessen volgen en handmatig kandidaatgegevens invoeren.</span><span class="sxs-lookup"><span data-stu-id="ce68a-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="ce68a-175">Selecteer **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="ce68a-176">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-176">Select **Links**.</span></span>

3. <span data-ttu-id="ce68a-177">Selecteer onder **Werving** **Kandidaten**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Bekijk de kandidaten](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="ce68a-179">Selecteer **Nieuw** om een kandidaat toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ce68a-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="ce68a-180">Om een bestaande kandidaat te bewerken, selecteert u de kandidaat uit de lijst en vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="ce68a-181">Het kandidaatprofiel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce68a-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="ce68a-182">Voer onder **Kandidaatoverzicht** de kandidaatgegevens van de kandidaat in of bewerk deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="ce68a-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="ce68a-183">Selecteer onder **Wervingsaanvraag** een wervingsaanvraag om de kandidaat aan te koppelen.</span><span class="sxs-lookup"><span data-stu-id="ce68a-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="ce68a-184">Vul vervolgens de **Geschatte begindatum**, **Aanstellend manager**, **Functie**  en **Omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Een wervingsaanvraag koppelen](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="ce68a-186">Vul alle gegevens in de volgende gebieden in die u wilt opnemen in het dossier van de kandidaat:</span><span class="sxs-lookup"><span data-stu-id="ce68a-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="ce68a-187">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="ce68a-187">**Comments**</span></span>
   - <span data-ttu-id="ce68a-188">**Beroepservaring**</span><span class="sxs-lookup"><span data-stu-id="ce68a-188">**Professional experience**</span></span>
   - <span data-ttu-id="ce68a-189">**Gegevens contactpersoon**</span><span class="sxs-lookup"><span data-stu-id="ce68a-189">**Contact information**</span></span>
   - <span data-ttu-id="ce68a-190">**Onderwijs**</span><span class="sxs-lookup"><span data-stu-id="ce68a-190">**Education**</span></span>
   - <span data-ttu-id="ce68a-191">**Vaardigheden**</span><span class="sxs-lookup"><span data-stu-id="ce68a-191">**Skills**</span></span>
   - <span data-ttu-id="ce68a-192">**Getuigschriften**</span><span class="sxs-lookup"><span data-stu-id="ce68a-192">**Certificates**</span></span>
   - <span data-ttu-id="ce68a-193">**Screenings**</span><span class="sxs-lookup"><span data-stu-id="ce68a-193">**Screenings**</span></span>

8. <span data-ttu-id="ce68a-194">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="ce68a-195">Een kandidaat aannemen</span><span class="sxs-lookup"><span data-stu-id="ce68a-195">Hire a candidate</span></span>

<span data-ttu-id="ce68a-196">Wanneer u klaar bent om een kandidaat aan te nemen, volgt u deze procedure om de kandidaat om te zetten in een werknemer.</span><span class="sxs-lookup"><span data-stu-id="ce68a-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="ce68a-197">Selecteer op het kandidaatformulier de optie **Aannemen**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-197">On the candidate form, select **Hire**.</span></span>

   ![Een kandidaat aannemen](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="ce68a-199">Vul in het formulier **Nieuwe werknemers aannemen** onder **Gegevens** alle velden in.</span><span class="sxs-lookup"><span data-stu-id="ce68a-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Gegevens nieuwe werknemer invoeren](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="ce68a-201">Controleer en wijzig onder **Functiegegevens** zo nodig de gegevens.</span><span class="sxs-lookup"><span data-stu-id="ce68a-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="ce68a-202">Selecteer onder **Controlelijsten voor onboarding** de relevante controlelijsten voor deze werknemer.</span><span class="sxs-lookup"><span data-stu-id="ce68a-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="ce68a-203">Selecteer **Doorgaan** om het werknemersdossier te maken.</span><span class="sxs-lookup"><span data-stu-id="ce68a-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="ce68a-204">Afhankelijk van de workflows van uw organisatie kan het kandidaatdossier aanvullende goedkeuringsstappen nodig hebben voordat deze wordt omgezet in een werknemersdossier.</span><span class="sxs-lookup"><span data-stu-id="ce68a-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="ce68a-205">Besluiten om een kandidaat niet aan te nemen</span><span class="sxs-lookup"><span data-stu-id="ce68a-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="ce68a-206">Als u besluit een kandidaat niet aan te nemen, volgt u deze procedure om ze te verwijderen uit het wervingsproces.</span><span class="sxs-lookup"><span data-stu-id="ce68a-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="ce68a-207">Selecteer op het kandidaatformulier de optie **Niet aannemen**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-207">On the candidate form, select **Do not hire**.</span></span>

   ![Een kandidaat niet aannemen](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="ce68a-209">Selecteer een **Redencode** en voeg eventuele opmerkingen toe.</span><span class="sxs-lookup"><span data-stu-id="ce68a-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="ce68a-210">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="ce68a-211">Een kandidaat ontslaan</span><span class="sxs-lookup"><span data-stu-id="ce68a-211">Dismiss a candidate</span></span>

<span data-ttu-id="ce68a-212">U kunt een kandidaat zo nodig ontslaan nadat u deze hebt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="ce68a-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="ce68a-213">Een kandidaat kan bijvoorbeeld uw aanbod afwijzen of op de eerste dag niet komen opdagen.</span><span class="sxs-lookup"><span data-stu-id="ce68a-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="ce68a-214">Selecteer op het kandidaatformulier de optie **Kandidaat ontslaan**.</span><span class="sxs-lookup"><span data-stu-id="ce68a-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Kandidaat negeren](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="ce68a-216">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ce68a-216">See also</span></span>

[<span data-ttu-id="ce68a-217">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="ce68a-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="ce68a-218">Uw personeel organiseren</span><span class="sxs-lookup"><span data-stu-id="ce68a-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="ce68a-219">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="ce68a-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)
