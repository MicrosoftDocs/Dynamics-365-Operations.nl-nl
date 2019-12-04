---
title: Analytische rapporten gebruiken in Attract
description: In dit onderwerp worden de analytische rapporten voor inzichten in het aanstellingsproces in Microsoft Dynamics 365 Talent - Attract beschreven
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 4ae608bbca111313d8c77e63f6a7a95813f6e5cd
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833226"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="09000-103">Analytische rapporten gebruiken in Attract</span><span class="sxs-lookup"><span data-stu-id="09000-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09000-104">Analytische rapporten in Microsoft Dynamics 365 Talent: Attract bieden een standaardoplossing voor inzichten in het aanstellingsproces.</span><span class="sxs-lookup"><span data-stu-id="09000-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="09000-105">Tot de beschikbare functies behoren:</span><span class="sxs-lookup"><span data-stu-id="09000-105">Availabe features include:</span></span>

- <span data-ttu-id="09000-106">**Functieanalyse**: klik op het tabblad **Analyses** binnen een functie voor metrische gegevens over de sollicitanten naar de functie.</span><span class="sxs-lookup"><span data-stu-id="09000-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="09000-107">**Analysehub**: klik op **Analyses** in de linkernavigatiebalk voor samengevoegde meetgegevens over de verschillende functies.</span><span class="sxs-lookup"><span data-stu-id="09000-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="09000-108">**Gebruikersspecifieke beveiliging**: toegang tot rapporten wordt beheerd per Attract-[rol](security-attract.md) en functiedeelnemersrol.</span><span class="sxs-lookup"><span data-stu-id="09000-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="09000-109">**Kruisfilteren**: klik op visuele elementen in een rapport om andere metrische gegevens weer te geven die door geselecteerde gegevens worden gefilterd.</span><span class="sxs-lookup"><span data-stu-id="09000-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="09000-110">Deze functie is momenteel in [preview](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="09000-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="09000-111">Als u deze wilt proberen, hebt u [**Uitgebreide invoegtoepassing voor aanstellingen**](attract-comprehensive-hiring.md) nodig.</span><span class="sxs-lookup"><span data-stu-id="09000-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="09000-112">Alle rapporten in openbare preview worden in het Engels weergegeven.</span><span class="sxs-lookup"><span data-stu-id="09000-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="09000-113">Rapporten worden elke 3 uur vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="09000-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="09000-114">Het tijdstip van de laatste vernieuwing (in de lokale tijdzone) wordt boven aan het rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="09000-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="09000-115">De vernieuwingsfrequentie is een benadering en varieert op basis van gegevensvolume en belasting van resources in uw regio.</span><span class="sxs-lookup"><span data-stu-id="09000-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="09000-116">Analyses van functie</span><span class="sxs-lookup"><span data-stu-id="09000-116">Job Analytics</span></span>

<span data-ttu-id="09000-117">Functieanalyse-rapporten vormen een momentopname van het aanstellingsproces van een functie.</span><span class="sxs-lookup"><span data-stu-id="09000-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="09000-118">Belangrijke metrische gegevens zijn:</span><span class="sxs-lookup"><span data-stu-id="09000-118">Key metrics include:</span></span>

- <span data-ttu-id="09000-119">Actieve sollicitanten op fase</span><span class="sxs-lookup"><span data-stu-id="09000-119">Active applicants by stage</span></span>
- <span data-ttu-id="09000-120">Bron van sollicitant</span><span class="sxs-lookup"><span data-stu-id="09000-120">Applicant source</span></span>
- <span data-ttu-id="09000-121">Type sollicitant (intern of extern)</span><span class="sxs-lookup"><span data-stu-id="09000-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="09000-122">Analysehub</span><span class="sxs-lookup"><span data-stu-id="09000-122">Analytics Hub</span></span>

<span data-ttu-id="09000-123">Analysehub-rapporten voegen gegevens van verschillende functies samen om trends in het aanstellingsproces naar boven te halen.</span><span class="sxs-lookup"><span data-stu-id="09000-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="09000-124">Attract omvat twee OOTB-rapporten: Pipeline-overzicht en Trechteranalyse.</span><span class="sxs-lookup"><span data-stu-id="09000-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="09000-125">Overzicht pipeline</span><span class="sxs-lookup"><span data-stu-id="09000-125">Pipeline Summary</span></span>

<span data-ttu-id="09000-126">In het rapport Pipeline-overzicht worden gegevens samengevoegd voor openstaande functies.</span><span class="sxs-lookup"><span data-stu-id="09000-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="09000-127">Belangrijke metrische gegevens zijn:</span><span class="sxs-lookup"><span data-stu-id="09000-127">Key metrics include:</span></span>

- <span data-ttu-id="09000-128">Sollicitanten in alle functies op fase</span><span class="sxs-lookup"><span data-stu-id="09000-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="09000-129">Bron van sollicitant</span><span class="sxs-lookup"><span data-stu-id="09000-129">Applicant source</span></span>
- <span data-ttu-id="09000-130">Openstaande functies op anciënniteitsniveau</span><span class="sxs-lookup"><span data-stu-id="09000-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="09000-131">Trechteranalyse</span><span class="sxs-lookup"><span data-stu-id="09000-131">Funnel Analysis</span></span>

<span data-ttu-id="09000-132">In het rapport Trechteranalyse worden gegevens samengevoegd voor functies die zijn afgesloten als vervuld.</span><span class="sxs-lookup"><span data-stu-id="09000-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="09000-133">Belangrijke metrische gegevens zijn:</span><span class="sxs-lookup"><span data-stu-id="09000-133">Key metrics include:</span></span>

- <span data-ttu-id="09000-134">Wervingstijd</span><span class="sxs-lookup"><span data-stu-id="09000-134">Time to hire</span></span>
- <span data-ttu-id="09000-135">Metrische gegevens voor conversie (bij aanwijzen)</span><span class="sxs-lookup"><span data-stu-id="09000-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="09000-136">Percentage van aanbiedingsacceptatie</span><span class="sxs-lookup"><span data-stu-id="09000-136">Offer acceptance rate</span></span>

<span data-ttu-id="09000-137">Opmerking: voor de meest accurate rapportage van het wervingstijdstip, verdient het aanbeveling om [Aanbiedingsbeheer](offer-setup.md) te gebruiken. Dit is een functie die beschikbaar is als onderdeel van de uitgebreide invoegtoepassing voor aanstellingen.</span><span class="sxs-lookup"><span data-stu-id="09000-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="09000-138">Probeer visuele elementen aan te wijzen voor aanvullende informatie.</span><span class="sxs-lookup"><span data-stu-id="09000-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="09000-139">Als u bijvoorbeeld visuele elementen voor **Actieve sollicitanten** aanwijst, wordt het gemiddelde aantal dagen in de fase weergegeven.</span><span class="sxs-lookup"><span data-stu-id="09000-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="09000-140">Het analyseren van deze informatie kan leiden tot belangrijke inzichten die de wervingstijd verkorten en wervers in staat stellen zich te concentreren op manieren om de tijd te beperken die in elke fase wordt besteed.</span><span class="sxs-lookup"><span data-stu-id="09000-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="09000-141">Gebruikersspecifieke beveiliging</span><span class="sxs-lookup"><span data-stu-id="09000-141">User-specific security</span></span>

<span data-ttu-id="09000-142">Attract-rapporten zijn toegankelijk voor de [rollen](security-attract.md) Beheer, Alles lezen, Werver en Aanstellend manager.</span><span class="sxs-lookup"><span data-stu-id="09000-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="09000-143">Niet-toegewezen gebruikers hebben geen toegang tot de analytische rapportpagina's (Functieanalyse of Analysehub).</span><span class="sxs-lookup"><span data-stu-id="09000-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="09000-144">Functieanalyserapporten tonen gegevens voor de geselecteerde functie.</span><span class="sxs-lookup"><span data-stu-id="09000-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="09000-145">In Analysehubrapporten worden gegevens samengevoegd over alle functies die een gebruiker kan weergeven.</span><span class="sxs-lookup"><span data-stu-id="09000-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="09000-146">Gebruikers die zowel Mijn functies als Alle functies op de pagina Functies kunnen weergeven, hebben de beschikking over dezelfde weergaven in de Analysehub.</span><span class="sxs-lookup"><span data-stu-id="09000-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="09000-147">Kruisfilter</span><span class="sxs-lookup"><span data-stu-id="09000-147">Cross-filter</span></span>

<span data-ttu-id="09000-148">Een van de mooie functies van Power BI is de manier waarop alle visuele elementen op een rapportpagina onderling zijn verbonden.</span><span class="sxs-lookup"><span data-stu-id="09000-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="09000-149">Als u een gegevenspunt selecteert in een van de visuele elementen, worden alle andere visuele elementen op de pagina die deze gegevens bevatten gewijzigd op basis van die selectie.</span><span class="sxs-lookup"><span data-stu-id="09000-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="09000-150">Lees meer over deze functie en bekijk een voorbeeld in [Visuele elementen kruisfilteren in een Power BI-rapport](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="09000-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="09000-151">Exporteren naar Excel</span><span class="sxs-lookup"><span data-stu-id="09000-151">Export to Excel</span></span>

<span data-ttu-id="09000-152">Als u rapportgegevens wilt weergeven in Excel, kunt u op het optiemenu (drie puntjes) in een visueel element klikken en **Onderliggende gegevens exporteren** selecteren.</span><span class="sxs-lookup"><span data-stu-id="09000-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="09000-153">Geëxporteerde gegevens worden als gefilterd geëxporteerd, met inachtneming van de gebruikersmachtigingen in Attract.</span><span class="sxs-lookup"><span data-stu-id="09000-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="09000-154">Zie [Gegevens exporteren vanuit visualisaties](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="09000-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
