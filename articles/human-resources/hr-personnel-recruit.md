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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669161"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="879e7-103">Kandidaten werven</span><span class="sxs-lookup"><span data-stu-id="879e7-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="879e7-104">Met Dynamics 365 Human Resources kunt u wervingsaanvragen te beheren.</span><span class="sxs-lookup"><span data-stu-id="879e7-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="879e7-105">Ook kunt u met dit programma sollicitanten naadloos omzetten in werknemers.</span><span class="sxs-lookup"><span data-stu-id="879e7-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="879e7-106">Als uw organisatie gebruikmaakt van een afzonderlijke wervingsapplicatie, kan uw wervingsproces de volgende stappen bevatten:</span><span class="sxs-lookup"><span data-stu-id="879e7-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="879e7-107">Uw wervingsaanvraag invoeren in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="879e7-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="879e7-108">Kandidaat-verwijzingen ontvangen in Human Resources vanuit de wervingsapplicatie.</span><span class="sxs-lookup"><span data-stu-id="879e7-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="879e7-109">Het goedkeuringsproces voor kandidaten in voltooien in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="879e7-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="879e7-110">Als u geen afzonderlijke wervingsapplicatie gebruikt, kunt u de kandidaten ook handmatig beheren in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="879e7-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="879e7-111">Zie [Common Data Service-integratie configureren](hr-admin-integration-common-data-service.md) en [Common Data Service-virtuele entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md) als u een beheerder of ontwikkelaar bent en u Human Resources wilt integreren met een wervingsapplicatie van derden.</span><span class="sxs-lookup"><span data-stu-id="879e7-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="879e7-112">U kunt ook apps voor wervingsintegratie vinden op [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="879e7-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="879e7-113">Zie [Integratie met LinkedIn Talent Hub](hr-admin-integration-linkedin.md) voor informatie over het gebruik van de preview-functie voor integratie met LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="879e7-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="879e7-114">Wervingsaanvragen inschakelen</span><span class="sxs-lookup"><span data-stu-id="879e7-114">Enable recruiting requests</span></span>

<span data-ttu-id="879e7-115">Als u wervingsaanvragen in Human Resources wilt verzenden, moet u eerst de functionaliteit **Human Resources-parameters** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="879e7-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="879e7-116">In de werkruimte **Personeelsbeheer** selecteert u **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="879e7-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="879e7-117">Selecteer onder **Instellen** de optie **Human resources-parameters**.</span><span class="sxs-lookup"><span data-stu-id="879e7-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="879e7-118">Op het tabblad **Algemeen** onder **WERVING**, stelt u **Wervingsaanvragen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="879e7-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Wervingsaanvragen inschakelen](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="879e7-120">De locatie van een wervingsaanvraag toevoegen</span><span class="sxs-lookup"><span data-stu-id="879e7-120">Add a recruiting request location</span></span>

<span data-ttu-id="879e7-121">Als uw organisatie meerdere locaties heeft, kunt u deze toevoegen zodat aanvragers een locatie kunnen selecteren waar de nieuwe werving actief is.</span><span class="sxs-lookup"><span data-stu-id="879e7-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="879e7-122">De locatie wordt opgenomen in de vacaturebeschrijving.</span><span class="sxs-lookup"><span data-stu-id="879e7-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="879e7-123">Voer in de zoekbalk **Locatie voor wervingsaanvraag** in.</span><span class="sxs-lookup"><span data-stu-id="879e7-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="879e7-124">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="879e7-124">Select **New**.</span></span>

3. <span data-ttu-id="879e7-125">Voer in het veld **Locatie voor wervingsaanvraag** de locatienaam in.</span><span class="sxs-lookup"><span data-stu-id="879e7-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![De locatie van een wervingsaanvraag toevoegen](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="879e7-127">Voer in het veld **Omschrijving** een omschrijving voor de locatie in.</span><span class="sxs-lookup"><span data-stu-id="879e7-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="879e7-128">Selecteer **Locatie** onder **Producten**.</span><span class="sxs-lookup"><span data-stu-id="879e7-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="879e7-129">Als het venster **Nieuw adres** verschijnt, voert u het adres voor de locatie in.</span><span class="sxs-lookup"><span data-stu-id="879e7-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Adres invoeren](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="879e7-131">Voer onder **Contactgegevens** de gegevens in voor de contactpersoon van de locatie.</span><span class="sxs-lookup"><span data-stu-id="879e7-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="879e7-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="879e7-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="879e7-133">Een wervingsaanvraag toevoegen</span><span class="sxs-lookup"><span data-stu-id="879e7-133">Add a recruiting request</span></span>

<span data-ttu-id="879e7-134">Managers kunnen wervingsverzoeken indienen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="879e7-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="879e7-135">Als u een afzonderlijke wervingsapplicatie gebruikt, zal het uitvoeren van deze stappen een wervingsaanvraag verzenden en het wervingsproces starten in die applicatie.</span><span class="sxs-lookup"><span data-stu-id="879e7-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="879e7-136">Voer anders deze procedure uit om de workflow te starten voor uw eigen interne wervingsproces.</span><span class="sxs-lookup"><span data-stu-id="879e7-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="879e7-137">Selecteer **Werknemerselfservice**.</span><span class="sxs-lookup"><span data-stu-id="879e7-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="879e7-138">Selecteer het tabblad **Mijn team**.</span><span class="sxs-lookup"><span data-stu-id="879e7-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="879e7-139">Selecteer **Wervingsaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="879e7-139">Select  **Request to recruit**.</span></span>

   ![Een wervingsaanvraag starten](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="879e7-141">Vul de velden **Omschrijving**, **Vacature** en **Geschatte begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="879e7-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![De wervingsaanvraag voltooien](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="879e7-143">Selecteer **Continue**.</span><span class="sxs-lookup"><span data-stu-id="879e7-143">Select **Continue**.</span></span> <span data-ttu-id="879e7-144">De wervingsaanvraag voor uw functie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="879e7-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="879e7-145">Selecteer onder **Algemeen** een werver uit de keuzelijst **Werver** en selecteer een locatie in de **Locatie voor wervingsaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="879e7-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="879e7-146">Wijzig onder **Vacature** de benodigde informatie en selecteer **Details uit vacature aanmaken**.</span><span class="sxs-lookup"><span data-stu-id="879e7-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Details van taak maken](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="879e7-148">De rest van het wervingsverzoek wordt gevuld met de standaardinformatie over de vacature die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="879e7-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="879e7-149">Voer onder **Externe omschrijving** een externe vacatureomschrijving in.</span><span class="sxs-lookup"><span data-stu-id="879e7-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="879e7-150">Selecteer onder **Functies** de optie **Toevoegen** en selecteer vervolgens een functie voor deze wervingsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="879e7-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Een functie toevoegen](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="879e7-152">Selecteer onder **Vaardigheden** **Toevoegen** en selecteer vervolgens een vaardigheid.</span><span class="sxs-lookup"><span data-stu-id="879e7-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="879e7-153">Selecteer onder **Opleidingseisen** **Toevoegen** en vervolgens waarden uit de vervolgkeuzelijsten **Opleiding** en **Opleidingsniveau**.</span><span class="sxs-lookup"><span data-stu-id="879e7-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Opleidingseisen toevoegen](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="879e7-155">Voeg onder **Opmerkingen** opmerkingen toe indien nodig.</span><span class="sxs-lookup"><span data-stu-id="879e7-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="879e7-156">Selecteer onder **Compensatie** een niveau in de vervolgkeuzelijst **Niveau** en wijzig vervolgens de **Lage drempelwaarde**, het **Controlepunt** en **Hoge drempelwaarde** indien nodig.</span><span class="sxs-lookup"><span data-stu-id="879e7-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="879e7-157">Wanneer uw wervingsaanvraag is voltooid en u klaar bent om het wervingsproces te starten, selecteert u **Activeren** in de menubalk.</span><span class="sxs-lookup"><span data-stu-id="879e7-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Wervingsaanvraag activeren](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="879e7-159">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="879e7-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="879e7-160">Uw wervingsaanvragen weergeven en bewerken</span><span class="sxs-lookup"><span data-stu-id="879e7-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="879e7-161">Als u manager bent en u uw eigen aanvragen wilt bekijken, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="879e7-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="879e7-162">Selecteer **Werknemerselfservice**.</span><span class="sxs-lookup"><span data-stu-id="879e7-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="879e7-163">Selecteer het tabblad **Mijn team**.</span><span class="sxs-lookup"><span data-stu-id="879e7-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="879e7-164">Selecteer onder **Mijn teamgegevens** het tabblad **Wervingsaanvragen**.</span><span class="sxs-lookup"><span data-stu-id="879e7-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Selecteer het tabblad Wervingsaanvragen](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="879e7-166">Als u een wervingsaanvraag wilt weergeven of bewerken, selecteert u deze in het raster.</span><span class="sxs-lookup"><span data-stu-id="879e7-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="879e7-167">Als u een HR-professional bent en alle wervingsaanvragen wilt bekijken, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="879e7-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="879e7-168">Selecteer **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="879e7-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="879e7-169">Selecteer **Wervingsaanvragen**.</span><span class="sxs-lookup"><span data-stu-id="879e7-169">Select **Recruiting requests**.</span></span>

   ![Wervingsaanvragen weergeven in Personeelsbeheer](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="879e7-171">Als u een wervingsaanvraag wilt weergeven of bewerken, selecteert u deze in het raster.</span><span class="sxs-lookup"><span data-stu-id="879e7-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="879e7-172">Een kandidaatprofiel toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="879e7-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="879e7-173">Als uw organisatie is geïntegreerd met een andere toepassing om wervingsaanvragen te beheren, worden deze doorgestuurd naar die toepassing.</span><span class="sxs-lookup"><span data-stu-id="879e7-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="879e7-174">De wervingstoepassing stuurt vervolgens informatie over kandidaten terug naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="879e7-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="879e7-175">Anders kunt u uw eigen interne wervingsprocessen volgen en handmatig kandidaatgegevens invoeren.</span><span class="sxs-lookup"><span data-stu-id="879e7-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="879e7-176">Selecteer **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="879e7-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="879e7-177">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="879e7-177">Select **Links**.</span></span>

3. <span data-ttu-id="879e7-178">Selecteer onder **Werving** **Kandidaten**.</span><span class="sxs-lookup"><span data-stu-id="879e7-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Bekijk de kandidaten](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="879e7-180">Selecteer **Nieuw** om een kandidaat toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="879e7-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="879e7-181">Om een bestaande kandidaat te bewerken, selecteert u de kandidaat uit de lijst en vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="879e7-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="879e7-182">Het kandidaatprofiel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="879e7-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="879e7-183">Voer onder **Kandidaatoverzicht** de kandidaatgegevens van de kandidaat in of bewerk deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="879e7-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="879e7-184">Selecteer onder **Wervingsaanvraag** een wervingsaanvraag om de kandidaat aan te koppelen.</span><span class="sxs-lookup"><span data-stu-id="879e7-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="879e7-185">Vul vervolgens de **Geschatte begindatum**, **Aanstellend manager**, **Functie**  en **Omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="879e7-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Een wervingsaanvraag koppelen](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="879e7-187">Vul alle gegevens in de volgende gebieden in die u wilt opnemen in het dossier van de kandidaat:</span><span class="sxs-lookup"><span data-stu-id="879e7-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="879e7-188">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="879e7-188">**Comments**</span></span>
   - <span data-ttu-id="879e7-189">**Beroepservaring**</span><span class="sxs-lookup"><span data-stu-id="879e7-189">**Professional experience**</span></span>
   - <span data-ttu-id="879e7-190">**Gegevens contactpersoon**</span><span class="sxs-lookup"><span data-stu-id="879e7-190">**Contact information**</span></span>
   - <span data-ttu-id="879e7-191">**Onderwijs**</span><span class="sxs-lookup"><span data-stu-id="879e7-191">**Education**</span></span>
   - <span data-ttu-id="879e7-192">**Vaardigheden**</span><span class="sxs-lookup"><span data-stu-id="879e7-192">**Skills**</span></span>
   - <span data-ttu-id="879e7-193">**Getuigschriften**</span><span class="sxs-lookup"><span data-stu-id="879e7-193">**Certificates**</span></span>
   - <span data-ttu-id="879e7-194">**Screenings**</span><span class="sxs-lookup"><span data-stu-id="879e7-194">**Screenings**</span></span>

8. <span data-ttu-id="879e7-195">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="879e7-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="879e7-196">Een kandidaat aannemen</span><span class="sxs-lookup"><span data-stu-id="879e7-196">Hire a candidate</span></span>

<span data-ttu-id="879e7-197">Wanneer u klaar bent om een kandidaat aan te nemen, volgt u deze procedure om de kandidaat om te zetten in een werknemer.</span><span class="sxs-lookup"><span data-stu-id="879e7-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="879e7-198">Selecteer op het kandidaatformulier de optie **Aannemen**.</span><span class="sxs-lookup"><span data-stu-id="879e7-198">On the candidate form, select **Hire**.</span></span>

   ![Een kandidaat aannemen](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="879e7-200">Vul in het formulier **Nieuwe werknemers aannemen** onder **Gegevens** alle velden in.</span><span class="sxs-lookup"><span data-stu-id="879e7-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Gegevens nieuwe werknemer invoeren](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="879e7-202">Controleer en wijzig onder **Functiegegevens** zo nodig de gegevens.</span><span class="sxs-lookup"><span data-stu-id="879e7-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="879e7-203">Selecteer onder **Controlelijsten voor onboarding** de relevante controlelijsten voor deze werknemer.</span><span class="sxs-lookup"><span data-stu-id="879e7-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="879e7-204">Selecteer **Doorgaan** om het werknemersdossier te maken.</span><span class="sxs-lookup"><span data-stu-id="879e7-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="879e7-205">Afhankelijk van de workflows van uw organisatie kan het kandidaatdossier aanvullende goedkeuringsstappen nodig hebben voordat deze wordt omgezet in een werknemersdossier.</span><span class="sxs-lookup"><span data-stu-id="879e7-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="879e7-206">Besluiten om een kandidaat niet aan te nemen</span><span class="sxs-lookup"><span data-stu-id="879e7-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="879e7-207">Als u besluit een kandidaat niet aan te nemen, volgt u deze procedure om ze te verwijderen uit het wervingsproces.</span><span class="sxs-lookup"><span data-stu-id="879e7-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="879e7-208">Selecteer op het kandidaatformulier de optie **Niet aannemen**.</span><span class="sxs-lookup"><span data-stu-id="879e7-208">On the candidate form, select **Do not hire**.</span></span>

   ![Een kandidaat niet aannemen](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="879e7-210">Selecteer een **Redencode** en voeg eventuele opmerkingen toe.</span><span class="sxs-lookup"><span data-stu-id="879e7-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="879e7-211">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="879e7-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="879e7-212">Een kandidaat ontslaan</span><span class="sxs-lookup"><span data-stu-id="879e7-212">Dismiss a candidate</span></span>

<span data-ttu-id="879e7-213">U kunt een kandidaat zo nodig ontslaan nadat u deze hebt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="879e7-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="879e7-214">Een kandidaat kan bijvoorbeeld uw aanbod afwijzen of op de eerste dag niet komen opdagen.</span><span class="sxs-lookup"><span data-stu-id="879e7-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="879e7-215">Selecteer op het kandidaatformulier de optie **Kandidaat ontslaan**.</span><span class="sxs-lookup"><span data-stu-id="879e7-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Kandidaat negeren](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="879e7-217">Zie ook</span><span class="sxs-lookup"><span data-stu-id="879e7-217">See also</span></span>

[<span data-ttu-id="879e7-218">Virtuele entiteiten van Common Data Service configureren</span><span class="sxs-lookup"><span data-stu-id="879e7-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="879e7-219">Uw personeel organiseren</span><span class="sxs-lookup"><span data-stu-id="879e7-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="879e7-220">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="879e7-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)