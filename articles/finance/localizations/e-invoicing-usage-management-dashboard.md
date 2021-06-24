---
title: Dashboard Gebruiksbeheer
description: In dit onderwerp wordt uitgelegd hoe u het dashboard voor gebruiksbeheer gebruikt om het gebruik van de elektronische factureringsservice te controleren en compatibel te blijven.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130501"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="0c958-103">Dashboard Gebruiksbeheer</span><span class="sxs-lookup"><span data-stu-id="0c958-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c958-104">Met het dashboard **Gebruiksbeheer** kunt u het gebruik van de elektronische factureringsservice controleren en daardoor kan uw organisatie conform blijven met betrekking tot het maandelijkse gebruik.</span><span class="sxs-lookup"><span data-stu-id="0c958-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="0c958-105">Compliance wordt bepaald door het indieningsvolume te berekenen en deze te vergelijken met het aangekochte volume van indieningen om eventuele afwijkingen tussen het aangekochte volume en het gebruikte volume aan te geven.</span><span class="sxs-lookup"><span data-stu-id="0c958-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="0c958-106">Het dashboard bevat de volgende indicatoren:</span><span class="sxs-lookup"><span data-stu-id="0c958-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="0c958-107">Een kostenindicator die u kunt gebruiken om het verbruik te controleren voor doeleinden van conformiteit van licenties:</span><span class="sxs-lookup"><span data-stu-id="0c958-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="0c958-108">Gebruik per maand (export)</span><span class="sxs-lookup"><span data-stu-id="0c958-108">Usage per month (export)</span></span>

- <span data-ttu-id="0c958-109">Drie operationele indicatoren die u kunt gebruiken om het gebruik van de elektronische factureringsservice bij te houden voor beheerdoeleinden:</span><span class="sxs-lookup"><span data-stu-id="0c958-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="0c958-110">Gebruik per functie</span><span class="sxs-lookup"><span data-stu-id="0c958-110">Usage by feature</span></span>
    - <span data-ttu-id="0c958-111">Gebruik per omgeving</span><span class="sxs-lookup"><span data-stu-id="0c958-111">Usage by environment</span></span>
    - <span data-ttu-id="0c958-112">Gebruik per maand (import)</span><span class="sxs-lookup"><span data-stu-id="0c958-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="0c958-113">Bereik van metingen</span><span class="sxs-lookup"><span data-stu-id="0c958-113">Measurement scope</span></span>

- <span data-ttu-id="0c958-114">Maateenheid:</span><span class="sxs-lookup"><span data-stu-id="0c958-114">Unit of measure:</span></span> 

    <span data-ttu-id="0c958-115">Met het dashboard **Gebruiksbeheer** wordt de indiening van bedrijfsdocumenten en geïmporteerde elektronische facturen geteld.</span><span class="sxs-lookup"><span data-stu-id="0c958-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="0c958-116">Organisatie:</span><span class="sxs-lookup"><span data-stu-id="0c958-116">Organization:</span></span> 

    <span data-ttu-id="0c958-117">Tellen wordt samengevat door de tenant-id van uw organisatie, ongeacht het aantal exemplaren van Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management of het aantal rechtspersonen waar de elektronische factureringsservice is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0c958-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="0c958-118">Indicator: Gebruik per maand (export)</span><span class="sxs-lookup"><span data-stu-id="0c958-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="0c958-119">Deze indicator geeft details over de elektronische facturen die uw organisatie tijdens een gedefinieerde periode uitgeeft.</span><span class="sxs-lookup"><span data-stu-id="0c958-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="0c958-120">Bereik</span><span class="sxs-lookup"><span data-stu-id="0c958-120">Scope</span></span>
- <span data-ttu-id="0c958-121">Het aantal bedrijfsdocumenten dat via Finance en Supply Chain Management wordt ingediend bij de elektronische factureringsservice, ongeacht het aantal regels dat deze bedrijfsdocumenten bevatten.</span><span class="sxs-lookup"><span data-stu-id="0c958-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="0c958-122">Het aantal ingediende bedrijfsdocumenten dat met succes wordt verwerkt door de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="0c958-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="0c958-123">Een document wordt als succesvol verwerkt beschouwd wanneer de stroom acties die in de functie-instellingen zijn gedefinieerd, is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0c958-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="0c958-124">Wanneer een elektronische factuur wordt ingediend bij een externe webservice, is de telling onafhankelijk van de resultaten van de verwerking van de webservice (geaccepteerd, afgewezen of schemavalidatiefout).</span><span class="sxs-lookup"><span data-stu-id="0c958-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="0c958-125">Als de webservice de aanvraag van de elektronische factureringsservice heeft ontvangen en beantwoord, wordt de indiening als een geldige telling beschouwd.</span><span class="sxs-lookup"><span data-stu-id="0c958-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="0c958-126">**Uitzondering**: bedrijfsdocumenten worden niet geteld als ze opnieuw vanuit Finance en Supply Chain Management worden ingediend bij de elektronische factureringsservice, zoals in de scenario's waarin een nieuwe inzending van hetzelfde bedrijfsdocument nodig is om de status van de elektronische factuur te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0c958-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="0c958-127">Uitgifte van een Braziliaanse elektronische factuur (belastingdocument) wordt bijvoorbeeld geteld als geldig, maar de annuleringsaanvraag voor de factuur wordt niet geteld.</span><span class="sxs-lookup"><span data-stu-id="0c958-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="0c958-128">Berekening</span><span class="sxs-lookup"><span data-stu-id="0c958-128">Calculation</span></span>

<span data-ttu-id="0c958-129">De berekening van het saldo wordt als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="0c958-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="0c958-130">Saldo = Gratis + Ingekocht – Gebruikt</span><span class="sxs-lookup"><span data-stu-id="0c958-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="0c958-131">Hierin:</span><span class="sxs-lookup"><span data-stu-id="0c958-131">Where:</span></span>

- <span data-ttu-id="0c958-132">Gratis:</span><span class="sxs-lookup"><span data-stu-id="0c958-132">Free:</span></span>
  
    <span data-ttu-id="0c958-133">Een gratis volume bedrijfsdocumenten die de klant per maand kan indienen.</span><span class="sxs-lookup"><span data-stu-id="0c958-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="0c958-134">Het bevat een pakket van 100 bedrijfsdocumenten die bij de elektronische factureringsservice kunnen worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="0c958-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="0c958-135">Een gratis volume is niet cumulatief en resterende saldi worden niet meegenomen naar de volgende periode.</span><span class="sxs-lookup"><span data-stu-id="0c958-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="0c958-136">Ingekocht:</span><span class="sxs-lookup"><span data-stu-id="0c958-136">Purchased:</span></span>
  
    <span data-ttu-id="0c958-137">Een pakket van 1.000 bedrijfsdocumenten die bij de elektronische factureringsservice kunnen worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="0c958-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="0c958-138">Dit pakket moet maandelijks voor uw organisatie worden verworven.</span><span class="sxs-lookup"><span data-stu-id="0c958-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="0c958-139">Ingekocht volume is niet cumulatief en resterende saldi worden niet meegenomen naar de volgende periode.</span><span class="sxs-lookup"><span data-stu-id="0c958-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="0c958-140">Gebruikt:</span><span class="sxs-lookup"><span data-stu-id="0c958-140">Used:</span></span> 

    <span data-ttu-id="0c958-141">De telling van bedrijfsdocumentindieningen bij de elektronische factureringsservice volgens gedefinieerde criteria.</span><span class="sxs-lookup"><span data-stu-id="0c958-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="0c958-142">Als uw organisatie van plan is om het maandelijkse volume van 100 gratis indieningen te overschrijden, koopt u het piekvolume om ervoor te zorgen dat u voldoet aan het Microsoft-licentiebeleid voor de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="0c958-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="0c958-143">Op dit moment moet het ingekochte volume volgens de verwervingsdatum handmatig worden ingevoerd als meerdere pakketten van 1000 indieningen.</span><span class="sxs-lookup"><span data-stu-id="0c958-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="0c958-144">Indicator: Gebruik door functie</span><span class="sxs-lookup"><span data-stu-id="0c958-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="0c958-145">Deze indicator toont het gebruik van elektronische factureringsfuncties voor de uitgifte van elektronische facturen tijdens een gedefinieerde periode.</span><span class="sxs-lookup"><span data-stu-id="0c958-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="0c958-146">Berekening:</span><span class="sxs-lookup"><span data-stu-id="0c958-146">Calculation:</span></span>
  
    <span data-ttu-id="0c958-147">Gebruikt = het aantal keren dat elke elektronische factureringsfunctie is gebruikt tijdens de indiening van bedrijfsdocumenten bij de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="0c958-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="0c958-148">Indicator: Gebruik door omgeving</span><span class="sxs-lookup"><span data-stu-id="0c958-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="0c958-149">Deze indicator geeft het gebruik van omgevingen van de elektronische factureringsservice gedurende een gedefinieerde periode aan.</span><span class="sxs-lookup"><span data-stu-id="0c958-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="0c958-150">Berekening:</span><span class="sxs-lookup"><span data-stu-id="0c958-150">Calculation:</span></span>
    
    <span data-ttu-id="0c958-151">Gebruikt = het aantal keren dat elke omgeving van de elektronische factureringsfunctie is gebruikt tijdens de indiening van bedrijfsdocumenten bij de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="0c958-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="0c958-152">Indicator: Gebruik per maand (import)</span><span class="sxs-lookup"><span data-stu-id="0c958-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="0c958-153">Deze indicator geeft het volume weer van het importeren van elektronische facturen door de elektronische factureringsservice bij Finance en Supply Chain Management gedurende een gedefinieerde periode.</span><span class="sxs-lookup"><span data-stu-id="0c958-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="0c958-154">Bereik:</span><span class="sxs-lookup"><span data-stu-id="0c958-154">Scope:</span></span>

    <span data-ttu-id="0c958-155">Elektronische facturen die worden geïmporteerd in Finance en Supply Chain Management, ongeacht het aantal regels dat die elektronische facturen bevatten.</span><span class="sxs-lookup"><span data-stu-id="0c958-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="0c958-156">Berekening:</span><span class="sxs-lookup"><span data-stu-id="0c958-156">Calculation:</span></span>

    <span data-ttu-id="0c958-157">Ontvangen = de telling van geïmporteerde elektronische facturen in Finance en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c958-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="0c958-158">Functies</span><span class="sxs-lookup"><span data-stu-id="0c958-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="0c958-159">Inkoop</span><span class="sxs-lookup"><span data-stu-id="0c958-159">Purchase</span></span>

<span data-ttu-id="0c958-160">Selecteer **Inkoop** op het tabblad **Gebruik per maand (export)** om het bedrag van de verworven indieningen handmatig te registreren.</span><span class="sxs-lookup"><span data-stu-id="0c958-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="0c958-161">Voor een bepaalde datum selecteert u **Nieuw** en voert u het aantal **Pakketten** in dat op die datum is verworven.</span><span class="sxs-lookup"><span data-stu-id="0c958-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="0c958-162">De **Hoeveelheid** wordt als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="0c958-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="0c958-163">Hoeveelheid = Pakketten \* 1000</span><span class="sxs-lookup"><span data-stu-id="0c958-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="0c958-164">De berekende **Hoeveelheid** wordt weergegeven in **Ingekocht** van de indicator **Gebruik per maand (export)**.</span><span class="sxs-lookup"><span data-stu-id="0c958-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="0c958-165">Update</span><span class="sxs-lookup"><span data-stu-id="0c958-165">Update</span></span>

<span data-ttu-id="0c958-166">Selecteer in het actievenster de optie **Bijwerken** om de berekening te vernieuwen en de gegevens bij te werken die op de pagina en in het diagram worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0c958-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="0c958-167">Historische gegevens opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="0c958-167">Reset history data</span></span>

<span data-ttu-id="0c958-168">Selecteer in het actievenster de optie **Historiegegevens opnieuw instellen** om de database te vernieuwen op basis van de plaats waar de indicatoren worden berekend.</span><span class="sxs-lookup"><span data-stu-id="0c958-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="0c958-169">Op het dashboard **Gebruiksbeheer** worden geen geldbedragen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0c958-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="0c958-170">In plaats daarvan wordt alleen het volume van getelde indieningen en geïmporteerde documenten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0c958-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
