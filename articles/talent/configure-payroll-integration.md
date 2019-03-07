---
title: De integratie van de salarisadministratie tussen Talent en Dayforce configureren
description: In dit onderwerp wordt uitgelegd hoe de integratie tussen Microsoft Dynamics 365 for Talent en Ceridian Dayforce wordt geconfigureerd zodat u een betaling kunt verwerken.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303867"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="6564c-103">De integratie van de salarisadministratie tussen Talent en Dayforce configureren</span><span class="sxs-lookup"><span data-stu-id="6564c-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6564c-104">De integratie tussen Microsoft Dynamics 365 for Talent en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen die in dit onderwerp worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="6564c-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="6564c-105">Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Talent als Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="6564c-106">Als u een service zoals Dayforce gebruikt voor het uitvoeren van betalingen, moet u de integratie inschakelen in Talent.</span><span class="sxs-lookup"><span data-stu-id="6564c-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="6564c-107">De integratie vereist specifieke gegevens vanuit Talent.</span><span class="sxs-lookup"><span data-stu-id="6564c-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="6564c-108">Daarom moet u controleren of gegevens die zijn toegewezen aan Dayforce zodanig in Talent zijn geconfigureerd dat de integratie wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="6564c-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="6564c-109">De integratie maakt gebruik van de volgende brede categorieën gegevens:</span><span class="sxs-lookup"><span data-stu-id="6564c-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="6564c-110">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-110">Human resources data</span></span>
- <span data-ttu-id="6564c-111">Compensatiegegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-111">Compensation data</span></span>
- <span data-ttu-id="6564c-112">Salarisgegevens, zoals betalingscycli, salarisperioden en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="6564c-113">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-113">Worker data</span></span>

<span data-ttu-id="6564c-114">In dit onderwerp worden de stappen beschreven die u moet volgen om de integratie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="6564c-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="6564c-115">Ook wordt uitgelegd welke typen gegevens en welke configuratiedetails vereist zijn voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="6564c-116">De integratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="6564c-116">Enable the integration</span></span>

<span data-ttu-id="6564c-117">In Talent moet u de integratie inschakelen en de configuratiegegevens invoeren om verbinding te maken met Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="6564c-118">Als u wilt dat de grootboektransactie die wordt geproduceerd wordt geïmporteerd in Microsoft Dynamics 365 for Finance and Operations, moet u ook een Microsoft Azure-opslagaccount instellen en de verbindingstekenreeks voor Azure Storage invoeren in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6564c-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="6564c-119">Voer de volgende stappen uit om de integratie in Talent in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="6564c-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="6564c-120">Ga naar de pagina **Systeembeheer** en selecteer **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="6564c-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="6564c-121">Voer het beveiligde FTP-eindpunt (File Transfer Protocol) en het pad naar de beveiligde FTP-map in.</span><span class="sxs-lookup"><span data-stu-id="6564c-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="6564c-122">Voer de gebruikersnaam en het wachtwoord in van de gebruiker die toegang krijgt tot het beveiligde FTP-eindpunt en het mappad.</span><span class="sxs-lookup"><span data-stu-id="6564c-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="6564c-123">Test de verbinding, zoals vereist, en stel de optie **Integratie van salarisadministratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6564c-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="6564c-124">Wanneer de integratie is ingeschakeld, worden het pakket voor gegevensexport en de bestanden gemaakt en wordt de frequentie ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6564c-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="6564c-125">U kunt deze frequentie naar behoefte wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6564c-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="6564c-126">Zie de volgende Azure-onderwerpen voor meer informatie over Azure-opslagaccounts en verbindingstekenreeksen voor Azure Storage:</span><span class="sxs-lookup"><span data-stu-id="6564c-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="6564c-127">Informatie over Azure-opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="6564c-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="6564c-128">Verbindingstekenreeks voor Azure Storage configureren</span><span class="sxs-lookup"><span data-stu-id="6564c-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="6564c-129">Uw gegevens configureren</span><span class="sxs-lookup"><span data-stu-id="6564c-129">Configure your data</span></span> 

<span data-ttu-id="6564c-130">Om salarissen te kunnen verwerken, moet u HRM-gegevens configureren in Talent.</span><span class="sxs-lookup"><span data-stu-id="6564c-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="6564c-131">U moet gegevens over de organisatie, zoals taken en functies, instellen samen met informatie over vergoedingen en compensatie.</span><span class="sxs-lookup"><span data-stu-id="6564c-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="6564c-132">Deze informatie biedt de informatie over dienstverband, salaris en inhoudingen die vereist is om het salaris van werknemers te genereren.</span><span class="sxs-lookup"><span data-stu-id="6564c-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="6564c-133">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="6564c-134">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="6564c-134">Benefits</span></span> 

<span data-ttu-id="6564c-135">Human resources biedt hulpmiddelen voor het instellen en onderhouden van de vergoedingen, inhoudingen en compensatieplannen van medewerkers die een organisatie zijn medewerkers biedt.</span><span class="sxs-lookup"><span data-stu-id="6564c-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="6564c-136">Wanneer u vergoedingen maakt, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="6564c-137">Vergoedingsplannen</span><span class="sxs-lookup"><span data-stu-id="6564c-137">Benefit plans</span></span>

- <span data-ttu-id="6564c-138">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-138">Plan (required)</span></span>
- <span data-ttu-id="6564c-139">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-139">Type (required)</span></span>
- <span data-ttu-id="6564c-140">Gevolgen voor salaris (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-140">Payroll impact (required)</span></span>
- <span data-ttu-id="6564c-141">Achterstallige betalingen herstellen</span><span class="sxs-lookup"><span data-stu-id="6564c-141">Recover arrears</span></span>
- <span data-ttu-id="6564c-142">Inhoudingsmethode</span><span class="sxs-lookup"><span data-stu-id="6564c-142">Deduction method</span></span>
- <span data-ttu-id="6564c-143">Inhoudingsprioriteit</span><span class="sxs-lookup"><span data-stu-id="6564c-143">Deduction priority</span></span>
- <span data-ttu-id="6564c-144">Limietperiode</span><span class="sxs-lookup"><span data-stu-id="6564c-144">Limit period</span></span>
- <span data-ttu-id="6564c-145">Bedrag beperken</span><span class="sxs-lookup"><span data-stu-id="6564c-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="6564c-146">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="6564c-146">Benefits</span></span>

- <span data-ttu-id="6564c-147">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-147">Plan (required)</span></span>
- <span data-ttu-id="6564c-148">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-148">Type (required)</span></span>
- <span data-ttu-id="6564c-149">Optie (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-149">Option (required)</span></span>
- <span data-ttu-id="6564c-150">Vergoeding-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-150">Benefit ID (required)</span></span>
- <span data-ttu-id="6564c-151">Frequentie</span><span class="sxs-lookup"><span data-stu-id="6564c-151">Frequency</span></span>
- <span data-ttu-id="6564c-152">Basis</span><span class="sxs-lookup"><span data-stu-id="6564c-152">Basis</span></span>
- <span data-ttu-id="6564c-153">Bedrag of tarief</span><span class="sxs-lookup"><span data-stu-id="6564c-153">Amount or rate</span></span>
- <span data-ttu-id="6564c-154">Inkomstencode</span><span class="sxs-lookup"><span data-stu-id="6564c-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="6564c-155">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="6564c-155">Supported frequencies</span></span> 

- <span data-ttu-id="6564c-156">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="6564c-156">Weekly</span></span>
- <span data-ttu-id="6564c-157">Tweewekelijks</span><span class="sxs-lookup"><span data-stu-id="6564c-157">Bi-weekly</span></span>
- <span data-ttu-id="6564c-158">Halfmaandelijks</span><span class="sxs-lookup"><span data-stu-id="6564c-158">Semi-monthly</span></span>
- <span data-ttu-id="6564c-159">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="6564c-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="6564c-160">Ondersteund bases</span><span class="sxs-lookup"><span data-stu-id="6564c-160">Supported bases</span></span> 

- <span data-ttu-id="6564c-161">Vast bedrag</span><span class="sxs-lookup"><span data-stu-id="6564c-161">Fixed amount</span></span>
- <span data-ttu-id="6564c-162">Percentage van inkomsten</span><span class="sxs-lookup"><span data-stu-id="6564c-162">Percent of earnings</span></span>
- <span data-ttu-id="6564c-163">Productieve uren</span><span class="sxs-lookup"><span data-stu-id="6564c-163">Productive hours</span></span>

<span data-ttu-id="6564c-164">Dayforce maakt de volgende inhoudingen, op basis van de salarisgevolgen die zijn gedefinieerd voor het vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="6564c-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="6564c-165">Selectie in Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-165">Selection in Talent</span></span>        | <span data-ttu-id="6564c-166">Resultaat in Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="6564c-167">None</span><span class="sxs-lookup"><span data-stu-id="6564c-167">None</span></span>                       | <span data-ttu-id="6564c-168">Er wordt geen inhouding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6564c-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="6564c-169">Alleen inhouding</span><span class="sxs-lookup"><span data-stu-id="6564c-169">Deduction only</span></span>             | <span data-ttu-id="6564c-170">Er wordt een inhouding voor de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6564c-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="6564c-171">Alleen bijdrage</span><span class="sxs-lookup"><span data-stu-id="6564c-171">Contribution only</span></span>          | <span data-ttu-id="6564c-172">Er wordt een inhouding voor de werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6564c-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="6564c-173">Inhouding en bijdrage</span><span class="sxs-lookup"><span data-stu-id="6564c-173">Deduction and contribution</span></span> | <span data-ttu-id="6564c-174">Er worden inhoudingen voor werknemer en werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6564c-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="6564c-175">Zie de volgende onderwerpen voor meer informatie over het definiëren en beheren van een vergoedingsprogramma:</span><span class="sxs-lookup"><span data-stu-id="6564c-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="6564c-176">Een vergoedingenprogramma voor werknemers maken</span><span class="sxs-lookup"><span data-stu-id="6564c-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="6564c-177">Een nieuwe vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="6564c-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="6564c-178">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="6564c-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="6564c-179">Vergoedingen inschrijven en verwijderen van medewerkers</span><span class="sxs-lookup"><span data-stu-id="6564c-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="6564c-180">Compensatie</span><span class="sxs-lookup"><span data-stu-id="6564c-180">Compensation</span></span> 

<span data-ttu-id="6564c-181">Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren.</span><span class="sxs-lookup"><span data-stu-id="6564c-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="6564c-182">Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd.</span><span class="sxs-lookup"><span data-stu-id="6564c-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="6564c-183">De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="6564c-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="6564c-184">Dayforce gebruikt compensatie-informatie voor het berekenen van het uur- of jaartarief van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="6564c-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="6564c-185">Er zijn vastecompensatieplannen en conversies van het loontarief vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="6564c-186">Werknemers moeten worden gekoppeld aan een vastecompensatieplan.</span><span class="sxs-lookup"><span data-stu-id="6564c-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="6564c-187">Zie de volgende onderwerpen voor meer informatie over compensatieplannen:</span><span class="sxs-lookup"><span data-stu-id="6564c-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="6564c-188">Plannen voor vaste compensatie maken</span><span class="sxs-lookup"><span data-stu-id="6564c-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="6564c-189">Plannen voor variabele compensatie maken</span><span class="sxs-lookup"><span data-stu-id="6564c-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="6564c-190">Salaris-/compensatiestructuur en -plannen ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="6564c-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="6564c-191">Compensatie verwerken</span><span class="sxs-lookup"><span data-stu-id="6564c-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="6564c-192">Compensatieproces definiëren en resultaten berekenen</span><span class="sxs-lookup"><span data-stu-id="6564c-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="6564c-193">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="6564c-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="6564c-194">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="6564c-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="6564c-195">Taken</span><span class="sxs-lookup"><span data-stu-id="6564c-195">Jobs</span></span> 

<span data-ttu-id="6564c-196">Een functie is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een functie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="6564c-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="6564c-197">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="6564c-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6564c-198">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="6564c-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="6564c-199">Nieuwe taken definiëren</span><span class="sxs-lookup"><span data-stu-id="6564c-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="6564c-200">Posities</span><span class="sxs-lookup"><span data-stu-id="6564c-200">Positions</span></span>

<span data-ttu-id="6564c-201">Een positie is een afzonderlijk exemplaar van een taak.</span><span class="sxs-lookup"><span data-stu-id="6564c-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="6564c-202">De positie 'Verkoopmanager (Oost)' is bijvoorbeeld een van de posities die zijn gekoppeld aan de functie 'Verkoopmanager'.</span><span class="sxs-lookup"><span data-stu-id="6564c-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="6564c-203">Een positie bestaat op een afdeling.</span><span class="sxs-lookup"><span data-stu-id="6564c-203">A position exists in a department.</span></span> <span data-ttu-id="6564c-204">Aan elke positie kan slechts één medewerker worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6564c-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="6564c-205">Let op de volgende gegevens en configuratie bij het instellen van posities:</span><span class="sxs-lookup"><span data-stu-id="6564c-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="6564c-206">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-206">Position (required)</span></span>
- <span data-ttu-id="6564c-207">Beschrijving (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-207">Description (required)</span></span>
- <span data-ttu-id="6564c-208">Functie (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-208">Job (required)</span></span>
- <span data-ttu-id="6564c-209">Afdeling (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-209">Department (required)</span></span>
- <span data-ttu-id="6564c-210">Positietype (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-210">Position type (required)</span></span>
- <span data-ttu-id="6564c-211">Voltijdse equivalent</span><span class="sxs-lookup"><span data-stu-id="6564c-211">Full-time equivalent</span></span>
- <span data-ttu-id="6564c-212">Jaarlijkse normale uren (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="6564c-213">Betaald door rechtspersoon (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="6564c-214">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-214">Pay cycle (required)</span></span>
- <span data-ttu-id="6564c-215">Standaard financiële dimensie: kostenplaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="6564c-216">Medewerkertoewijzing: medewerker, toewijzing begin, einde toewijzing, redencode</span><span class="sxs-lookup"><span data-stu-id="6564c-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="6564c-217">Als meerdere posities op dezelfde afdeling aan dezelfde functie zijn gekoppeld, worden deze geconsolideerd in een enkele positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="6564c-218">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="6564c-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6564c-219">Uw werknemers organiseren met afdelingen, taken en posities</span><span class="sxs-lookup"><span data-stu-id="6564c-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="6564c-220">Posities instellen</span><span class="sxs-lookup"><span data-stu-id="6564c-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="6564c-221">Afdelingen</span><span class="sxs-lookup"><span data-stu-id="6564c-221">Departments</span></span>

<span data-ttu-id="6564c-222">Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt.</span><span class="sxs-lookup"><span data-stu-id="6564c-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="6564c-223">Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR.</span><span class="sxs-lookup"><span data-stu-id="6564c-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="6564c-224">U kunt afdelingen gebruiken om te rapporteren over functiegebieden.</span><span class="sxs-lookup"><span data-stu-id="6564c-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="6564c-225">Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.</span><span class="sxs-lookup"><span data-stu-id="6564c-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="6564c-226">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="6564c-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6564c-227">Een afdeling maken en koppelen aan de afdelingshiërarchie</span><span class="sxs-lookup"><span data-stu-id="6564c-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="6564c-228">Nieuwe afdelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="6564c-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="6564c-229">Betalingscycli en salarisperioden</span><span class="sxs-lookup"><span data-stu-id="6564c-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="6564c-230">Een betalingscyclus bepaalt hoe vaak salarissen worden berekend en op welke specifieke dagen medewerkers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="6564c-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="6564c-231">Zo kan bijvooorbeeld een betalingscyclus maandelijks zijn en kunnen werknemers worden uitbetaald op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="6564c-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="6564c-232">Een betalingscyclus kan ook wekelijks en werknemers kunnen worden uitbetaald op de dinsdag na het einde van de salarisperiode.</span><span class="sxs-lookup"><span data-stu-id="6564c-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="6564c-233">Betalingscycli zijn toegewezen aan posities om te bepalen wanneer medewerkers in deze posities worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="6564c-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="6564c-234">Nadat u betalingscycli hebt gemaakt, kunt u salarisperioden voor elke cyclus genereren.</span><span class="sxs-lookup"><span data-stu-id="6564c-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="6564c-235">Elke salarisperiode bevat een standaard betalingsdatum die is gebaseerd op gegevens die u verstrekt.</span><span class="sxs-lookup"><span data-stu-id="6564c-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="6564c-236">U kunt echter de standaard betalingsdatum in een salarisperiode wijzigen om te voorzien in uitzonderingen, bijvoorbeeld wanneer de betalingsdatum op een feestdag valt.</span><span class="sxs-lookup"><span data-stu-id="6564c-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="6564c-237">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="6564c-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="6564c-238">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-238">Pay cycle (required)</span></span>
- <span data-ttu-id="6564c-239">Frequentie van betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="6564c-240">Begindatum van periode (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="6564c-241">Standaardbetalingsdatum (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="6564c-242">Deze informatie is geïntegreerd met Dayforce als betalingsgroepen en worden gescheiden per land of regio voor elke betalingscyclus.</span><span class="sxs-lookup"><span data-stu-id="6564c-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="6564c-243">Vóór integratie moet ten minste één salarisperiode worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="6564c-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="6564c-244">Dayforce genereert van betalingsgroepkalenders en betalingsdatums, op basis van de begindatum van de eerste salarisperiode en de standaardbetalingsdatum die is ingesteld in Talent.</span><span class="sxs-lookup"><span data-stu-id="6564c-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="6564c-245">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-245">Earning codes</span></span>

<span data-ttu-id="6564c-246">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="6564c-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6564c-247">De codes hebben verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="6564c-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="6564c-248">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="6564c-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="6564c-249">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-249">Earning Code (required)</span></span>
- <span data-ttu-id="6564c-250">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-250">Description</span></span>
- <span data-ttu-id="6564c-251">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="6564c-251">Unit of measure</span></span>
- <span data-ttu-id="6564c-252">Productief</span><span class="sxs-lookup"><span data-stu-id="6564c-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="6564c-253">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-253">Worker data</span></span>

<span data-ttu-id="6564c-254">Records voor de verschillende soorten medewerkers die u hebt zijn belangrijk voor uw HRM- en salarisadministratiesystemen.</span><span class="sxs-lookup"><span data-stu-id="6564c-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="6564c-255">De gegevens die u invoert, kunnen worden gebruikt om medewerkers en persoonlijke gegevens bij te houden.</span><span class="sxs-lookup"><span data-stu-id="6564c-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="6564c-256">U kunt de volgende informatie bijhouden voor medewerkers:</span><span class="sxs-lookup"><span data-stu-id="6564c-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="6564c-257">**Basis** – Basisinformatie over een medewerker bijhouden, zoals contactgegevens, demografische gegevens, identificatiegegevens, informatie over de familie, status van militaire dienst, expat-informatie en contactpersonen voor noodgevallen.</span><span class="sxs-lookup"><span data-stu-id="6564c-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="6564c-258">**Dienstverband** – Informatie bijhouden over werkgelegenheid van een medewerker, zoals een aansluiting met een bedrijf of organisatie, functie, start- en einddatums, arbeidsgeschiktheid, arbeidsvoorwaarden, pensioen, verlof en relocatie-informatie.</span><span class="sxs-lookup"><span data-stu-id="6564c-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="6564c-259">**Verlof en verzuim** – Informatie bijhouden over de afwezigheid van een medewerker, zoals werkkalenders, verzuimtransacties en verzuiminstellingen.</span><span class="sxs-lookup"><span data-stu-id="6564c-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="6564c-260">**Vergoedingen en salarissen** – Informatie bijhouden over compensatieplannen en salarisgegevens van een medewerker zoals inschrijving op plan, onderscheidingen, commissie, fiscale informatie, pensioen en salarisinhoudingen.</span><span class="sxs-lookup"><span data-stu-id="6564c-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="6564c-261">Wanneer u informatie over een werknemer invoert, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="6564c-262">Algemene informatie</span><span class="sxs-lookup"><span data-stu-id="6564c-262">General information</span></span>

- <span data-ttu-id="6564c-263">Personeelsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-263">Personnel number (required)</span></span>
- <span data-ttu-id="6564c-264">Voornaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-264">First name (required)</span></span>
- <span data-ttu-id="6564c-265">Achternaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-265">Last name (required)</span></span>
- <span data-ttu-id="6564c-266">Tweede naam</span><span class="sxs-lookup"><span data-stu-id="6564c-266">Middle name</span></span>
- <span data-ttu-id="6564c-267">Anciënniteitsdatum</span><span class="sxs-lookup"><span data-stu-id="6564c-267">Seniority date</span></span>
- <span data-ttu-id="6564c-268">Bekend als</span><span class="sxs-lookup"><span data-stu-id="6564c-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="6564c-269">Persoonlijke informatie</span><span class="sxs-lookup"><span data-stu-id="6564c-269">Personal information</span></span>

- <span data-ttu-id="6564c-270">Burgerlijke staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-270">Marital status (required)</span></span>
- <span data-ttu-id="6564c-271">Geboortedatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-271">Birth date (required)</span></span>
- <span data-ttu-id="6564c-272">Geslacht (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-272">Gender (required)</span></span>
- <span data-ttu-id="6564c-273">Persoon met handicap</span><span class="sxs-lookup"><span data-stu-id="6564c-273">Person with disabilities</span></span>
- <span data-ttu-id="6564c-274">Land/regio nationaliteit (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="6564c-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="6564c-275">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-275">Address information</span></span>

- <span data-ttu-id="6564c-276">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-276">Primary (required)</span></span>
- <span data-ttu-id="6564c-277">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-277">Country/region (required)</span></span>
- <span data-ttu-id="6564c-278">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-278">Postal code (required)</span></span>
- <span data-ttu-id="6564c-279">Huisnummer (vereist) (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="6564c-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="6564c-280">Gebouwtoevoeging (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="6564c-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="6564c-281">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-281">City (required)</span></span>
- <span data-ttu-id="6564c-282">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-282">State (required)</span></span>
- <span data-ttu-id="6564c-283">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="6564c-284">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="6564c-284">Contact information</span></span> 

- <span data-ttu-id="6564c-285">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-285">Primary (required)</span></span>
- <span data-ttu-id="6564c-286">Contactnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-286">Contact number (required)</span></span>
- <span data-ttu-id="6564c-287">Toestel</span><span class="sxs-lookup"><span data-stu-id="6564c-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="6564c-288">Salarisinformatie en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-288">Payroll information and earning codes</span></span>

<span data-ttu-id="6564c-289">Aan werknemers kunnen bepaalde inkomsten met een bepaalde betalingsfrequentie worden toegewezen en zij kunnen een geprefereerde betalingsmethode hebben.</span><span class="sxs-lookup"><span data-stu-id="6564c-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="6564c-290">De volgende velden worden gebruikt in Dayforce om te garanderen dat deze voorkeuren en instellingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6564c-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="6564c-291">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-291">Earning codes</span></span>

- <span data-ttu-id="6564c-292">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-292">Position (required)</span></span>
- <span data-ttu-id="6564c-293">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-293">Earning Code (required)</span></span>
- <span data-ttu-id="6564c-294">Frequentie (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-294">Frequency (required)</span></span>
- <span data-ttu-id="6564c-295">Bedrag (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="6564c-296">Salarisinformatie</span><span class="sxs-lookup"><span data-stu-id="6564c-296">Payroll information</span></span>

- <span data-ttu-id="6564c-297">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="6564c-297">Payment Method</span></span>
- <span data-ttu-id="6564c-298">Economische regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-298">Economic Region (required)</span></span>
- <span data-ttu-id="6564c-299">Id personeelsvergoedingen</span><span class="sxs-lookup"><span data-stu-id="6564c-299">Employee Benefits ID</span></span>
- <span data-ttu-id="6564c-300">Nationaal id-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-300">National ID Number (required)</span></span>
- <span data-ttu-id="6564c-301">Nummer militaire dienst</span><span class="sxs-lookup"><span data-stu-id="6564c-301">Military Service Number</span></span>
- <span data-ttu-id="6564c-302">Ploeg-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-302">Shift ID (required)</span></span>
- <span data-ttu-id="6564c-303">Btw-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-303">Tax Number (required)</span></span>
- <span data-ttu-id="6564c-304">Vakbond-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-304">Union ID (required)</span></span>
- <span data-ttu-id="6564c-305">Werkdag-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-305">Work Day ID (required)</span></span>
- <span data-ttu-id="6564c-306">Nummer werkvergunning</span><span class="sxs-lookup"><span data-stu-id="6564c-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="6564c-307">Voor de betalingsmethode ondersteunt Mexico **Contant geld**, **Cheque** (de fysieke cheque van het bedrijf) en **Elektronische betaling**.</span><span class="sxs-lookup"><span data-stu-id="6564c-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="6564c-308">Als geen betalingsmethode is opgegeven, wordt standaard **Cheque** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6564c-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="6564c-309">Details dienstverband</span><span class="sxs-lookup"><span data-stu-id="6564c-309">Employment details</span></span>

<span data-ttu-id="6564c-310">Historische gegevens over het dienstverband worden gebruikt als belangrijkste informatie voor het opvragen van de statussen voor aanstellen, ontslaan en opnieuw aanstellen van een werknemer in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="6564c-311">Dayforce ondersteunt slechts één actieve dienstverbandrecord tegelijk.</span><span class="sxs-lookup"><span data-stu-id="6564c-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="6564c-312">Begindatum dienstverband (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-312">Employment start date (required)</span></span>
- <span data-ttu-id="6564c-313">Einddatum dienstverband</span><span class="sxs-lookup"><span data-stu-id="6564c-313">Employment end date</span></span>
- <span data-ttu-id="6564c-314">Begindatum</span><span class="sxs-lookup"><span data-stu-id="6564c-314">Start date</span></span>
- <span data-ttu-id="6564c-315">Aangepaste begindatum</span><span class="sxs-lookup"><span data-stu-id="6564c-315">Adjusted start date</span></span>
- <span data-ttu-id="6564c-316">Ontslagdatum (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="6564c-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="6564c-317">Ontslagreden (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="6564c-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="6564c-318">De belangrijkste datums van een werknemer worden afgeleid met behulp van de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="6564c-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="6564c-319">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-319">Talent</span></span>                | <span data-ttu-id="6564c-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6564c-321">Meest recente huurdatum</span><span class="sxs-lookup"><span data-stu-id="6564c-321">Most recent hire date</span></span> | <span data-ttu-id="6564c-322">Begindatum van dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="6564c-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="6564c-323">Ontslagdatum</span><span class="sxs-lookup"><span data-stu-id="6564c-323">Termination date</span></span>      | <span data-ttu-id="6564c-324">Ontslagdatum van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="6564c-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="6564c-325">Begindatum</span><span class="sxs-lookup"><span data-stu-id="6564c-325">Start date</span></span>            | <span data-ttu-id="6564c-326">Aangepaste begindatum, begindatum of begindatum dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="6564c-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="6564c-327">Oorspronkelijke datum indiensttreding</span><span class="sxs-lookup"><span data-stu-id="6564c-327">Original hire date</span></span>    | <span data-ttu-id="6564c-328">Begindatum dienstverband van vroegste historierecord van dienstverband</span><span class="sxs-lookup"><span data-stu-id="6564c-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="6564c-329">Compensatie</span><span class="sxs-lookup"><span data-stu-id="6564c-329">Compensation</span></span>

<span data-ttu-id="6564c-330">Een vastecompensatieplan moet worden gekoppeld aan de primaire functie van elke werknemer tijdens de hele duur van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="6564c-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="6564c-331">Deze periode begint op de datum waarop de werknemer in dienst is genomen (of de begindatum van het dienstverband) en gaat door totdat aan het ontslag.</span><span class="sxs-lookup"><span data-stu-id="6564c-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="6564c-332">Ingangsdatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-332">Effective Date (required)</span></span>
- <span data-ttu-id="6564c-333">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="6564c-333">Expiration date</span></span>
- <span data-ttu-id="6564c-334">Loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-334">Pay Rate (required)</span></span>
- <span data-ttu-id="6564c-335">Conversies van loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="6564c-336">Jaarlijks equivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="6564c-337">Uurequivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="6564c-338">Als een werknemer met uurtarief meerdere posities heeft, wordt de vaste compensatie van de primaire positie geïmporteerd in Dayforce als het basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="6564c-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="6564c-339">Voor niet-primaire posities, wordt het uurtarief opgeslagen bij de overeenkomende positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="6564c-340">Als een medewerker met een salaris meerdere posities heeft, worden het cumulatieve uurtarief en het jaarsalaris voor alle actieve posities afgeleid en gebruikt als de basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="6564c-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="6564c-341">Identificatienummers</span><span class="sxs-lookup"><span data-stu-id="6564c-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="6564c-342">Sociaal-fiscaal nummer</span><span class="sxs-lookup"><span data-stu-id="6564c-342">Social Security identifier</span></span> 

<span data-ttu-id="6564c-343">Elke werknemer moet één primaire id hebben.</span><span class="sxs-lookup"><span data-stu-id="6564c-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="6564c-344">Deze id moet van het identificatietype **Sofinummer** zijn.</span><span class="sxs-lookup"><span data-stu-id="6564c-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="6564c-345">In Dayforce, wordt dit automatisch afgeleid als het sociaal-fiscaal nummer van de werknemer dat is vereist voor aanstelling.</span><span class="sxs-lookup"><span data-stu-id="6564c-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="6564c-346">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-346">Primary (required)</span></span>
- <span data-ttu-id="6564c-347">Identificatietype = 'Sofinummer'</span><span class="sxs-lookup"><span data-stu-id="6564c-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="6564c-348">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="6564c-348">Issued Date</span></span>
- <span data-ttu-id="6564c-349">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="6564c-349">Expiration Date</span></span>

<span data-ttu-id="6564c-350">Werknemers kunnen meerdere identificatienummers van het identificatietype **Sofinummer** opgeven.</span><span class="sxs-lookup"><span data-stu-id="6564c-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="6564c-351">Alleen de record die is gemarkeerd als **Primair** wordt echter opgenomen in Dayforce, ongeacht of het nummer actief of verlopen is.</span><span class="sxs-lookup"><span data-stu-id="6564c-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="6564c-352">Bankrekeningen en voorschotten</span><span class="sxs-lookup"><span data-stu-id="6564c-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="6564c-353">Er moet geldige bankrekeninginformatie worden ingevoerd voor elke werknemer die wil worden uitbetaald via bankrekeningoverboekingen.</span><span class="sxs-lookup"><span data-stu-id="6564c-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="6564c-354">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-354">Talent</span></span>                         | <span data-ttu-id="6564c-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6564c-356">Bankrekeningnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="6564c-357">SWIFT-code (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-357">SWIFT code (required)</span></span>          | <span data-ttu-id="6564c-358">Veld **Bank-id** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="6564c-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="6564c-359">Vestigingsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="6564c-360">Bankrekeningtype (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-360">Bank account type (required)</span></span>   | <span data-ttu-id="6564c-361">Veld **Rekeningtype** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="6564c-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="6564c-362">Ondersteunde waarden zijn **Rekening-courant** en **Salaris**.</span><span class="sxs-lookup"><span data-stu-id="6564c-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="6564c-363">Werknemers die ervoor kiezen om te worden uitbetaald via bankrekeningoverboekingen moeten een koppeling opgeven naar een restantrekening die zich onder een rechtspersoon bevindt met het primaire adres in Mexico en die is gekoppeld aan een geldige bankrekening van een Mexicaanse bank.</span><span class="sxs-lookup"><span data-stu-id="6564c-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="6564c-364">Alle andere niet-restantrekeningen worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="6564c-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="6564c-365">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="6564c-365">Address information</span></span>

<span data-ttu-id="6564c-366">Elke werknemer moet één primaire locatie hebben.</span><span class="sxs-lookup"><span data-stu-id="6564c-366">Every employee must have one primary location.</span></span> <span data-ttu-id="6564c-367">In Dayforce wordt deze locatie gebruikt om de primaire woonplaats van de werknemer te bepalen voor belastingdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="6564c-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="6564c-368">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-368">Primary (required)</span></span>
- <span data-ttu-id="6564c-369">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-369">Country/region (required)</span></span>
- <span data-ttu-id="6564c-370">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="6564c-371">Straat (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-371">Street (required)</span></span>
- <span data-ttu-id="6564c-372">Huisnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-372">Street Number (required)</span></span>
- <span data-ttu-id="6564c-373">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="6564c-373">Building Complement</span></span>
- <span data-ttu-id="6564c-374">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-374">City (required)</span></span>
- <span data-ttu-id="6564c-375">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-375">State (required)</span></span>
- <span data-ttu-id="6564c-376">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="6564c-377">Uw gegevens configureren voor het genereren van salarissen in de Verenigde Staten en Canada</span><span class="sxs-lookup"><span data-stu-id="6564c-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="6564c-378">Als u salarissen genereert voor werknemers in de Verenigde Staten en Canada, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="6564c-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="6564c-379">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="6564c-379">Departments are required on positions.</span></span>
- <span data-ttu-id="6564c-380">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="6564c-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="6564c-381">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="6564c-381">Job types</span></span>

<span data-ttu-id="6564c-382">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="6564c-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="6564c-383">Functietypen zijn vereist voor het verwerken van salarissen in de Verenigde Staten en Canada.</span><span class="sxs-lookup"><span data-stu-id="6564c-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="6564c-384">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="6564c-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6564c-385">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="6564c-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="6564c-386">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="6564c-387">Functietype</span><span class="sxs-lookup"><span data-stu-id="6564c-387">Job type</span></span>   | <span data-ttu-id="6564c-388">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="6564c-389">Per uur</span><span class="sxs-lookup"><span data-stu-id="6564c-389">Hourly</span></span>     | <span data-ttu-id="6564c-390">Per uur</span><span class="sxs-lookup"><span data-stu-id="6564c-390">Hourly</span></span>      |
| <span data-ttu-id="6564c-391">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="6564c-391">Salaried</span></span>   | <span data-ttu-id="6564c-392">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="6564c-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="6564c-393">Positietypen</span><span class="sxs-lookup"><span data-stu-id="6564c-393">Position types</span></span> 

<span data-ttu-id="6564c-394">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="6564c-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="6564c-395">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="6564c-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="6564c-396">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="6564c-397">Positietype</span><span class="sxs-lookup"><span data-stu-id="6564c-397">Position type</span></span>   | <span data-ttu-id="6564c-398">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="6564c-399">Voltijd</span><span class="sxs-lookup"><span data-stu-id="6564c-399">Full-time</span></span>       | <span data-ttu-id="6564c-400">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="6564c-400">Full time employee</span></span> |
| <span data-ttu-id="6564c-401">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="6564c-401">Part-time</span></span>       | <span data-ttu-id="6564c-402">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="6564c-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="6564c-403">Redencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-403">Reason codes</span></span>

<span data-ttu-id="6564c-404">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="6564c-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="6564c-405">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="6564c-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="6564c-406">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="6564c-407">Redencode</span><span class="sxs-lookup"><span data-stu-id="6564c-407">Reason code</span></span>    | <span data-ttu-id="6564c-408">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-408">Description</span></span>      | <span data-ttu-id="6564c-409">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="6564c-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="6564c-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="6564c-410">RESIGNATION</span></span>    | <span data-ttu-id="6564c-411">Ontslag</span><span class="sxs-lookup"><span data-stu-id="6564c-411">Resignation</span></span>      | <span data-ttu-id="6564c-412">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-412">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="6564c-413">TERMINATION</span></span>    | <span data-ttu-id="6564c-414">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="6564c-414">Termination</span></span>      | <span data-ttu-id="6564c-415">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-415">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="6564c-416">RETIREMENT</span></span>     | <span data-ttu-id="6564c-417">Pensionering</span><span class="sxs-lookup"><span data-stu-id="6564c-417">Retirement</span></span>       | <span data-ttu-id="6564c-418">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-418">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-419">OTHER</span><span class="sxs-lookup"><span data-stu-id="6564c-419">OTHER</span></span>          | <span data-ttu-id="6564c-420">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="6564c-420">Other Reasons</span></span>    | <span data-ttu-id="6564c-421">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-421">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="6564c-422">DEATH</span></span>          | <span data-ttu-id="6564c-423">Overlijden</span><span class="sxs-lookup"><span data-stu-id="6564c-423">Death</span></span>            | <span data-ttu-id="6564c-424">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-424">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="6564c-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="6564c-426">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="6564c-426">Leave of Absence</span></span> | <span data-ttu-id="6564c-427">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-427">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="6564c-428">CONTRACTEND</span></span>    | <span data-ttu-id="6564c-429">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="6564c-429">End of Contract</span></span>  | <span data-ttu-id="6564c-430">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-430">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="6564c-431">SALARYCHANGE</span></span>   | <span data-ttu-id="6564c-432">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="6564c-432">Change of Salary</span></span> | <span data-ttu-id="6564c-433">Compensatie</span><span class="sxs-lookup"><span data-stu-id="6564c-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="6564c-434">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="6564c-434">Marital status</span></span>

<span data-ttu-id="6564c-435">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6564c-436">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="6564c-437">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-437">Talent</span></span>                 | <span data-ttu-id="6564c-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="6564c-439">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="6564c-439">Married</span></span>                | <span data-ttu-id="6564c-440">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="6564c-440">Married</span></span>              |
| <span data-ttu-id="6564c-441">Eén</span><span class="sxs-lookup"><span data-stu-id="6564c-441">Single</span></span>                 | <span data-ttu-id="6564c-442">Eén</span><span class="sxs-lookup"><span data-stu-id="6564c-442">Single</span></span>               |
| <span data-ttu-id="6564c-443">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="6564c-443">Widowed</span></span>                | <span data-ttu-id="6564c-444">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="6564c-444">Widowed</span></span>              |
| <span data-ttu-id="6564c-445">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="6564c-445">Divorced</span></span>               | <span data-ttu-id="6564c-446">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="6564c-446">Divorced</span></span>             |
| <span data-ttu-id="6564c-447">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="6564c-447">Registered Partnership</span></span> | <span data-ttu-id="6564c-448">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="6564c-448">Domestic Partnership</span></span> |
| <span data-ttu-id="6564c-449">None</span><span class="sxs-lookup"><span data-stu-id="6564c-449">None</span></span>                   | <span data-ttu-id="6564c-450">None</span><span class="sxs-lookup"><span data-stu-id="6564c-450">None</span></span>                 |
| <span data-ttu-id="6564c-451">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="6564c-451">Cohabiting</span></span>             | <span data-ttu-id="6564c-452">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="6564c-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="6564c-453">Geslacht</span><span class="sxs-lookup"><span data-stu-id="6564c-453">Gender</span></span>

<span data-ttu-id="6564c-454">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6564c-455">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="6564c-456">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-456">Talent</span></span>       | <span data-ttu-id="6564c-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="6564c-458">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-458">Male</span></span>         | <span data-ttu-id="6564c-459">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-459">Male</span></span>            |
| <span data-ttu-id="6564c-460">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-460">Female</span></span>       | <span data-ttu-id="6564c-461">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-461">Female</span></span>          |
| <span data-ttu-id="6564c-462">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="6564c-462">Non-specific</span></span> | <span data-ttu-id="6564c-463">*Niet ondersteund*</span><span class="sxs-lookup"><span data-stu-id="6564c-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="6564c-464">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-464">Earning codes</span></span>

<span data-ttu-id="6564c-465">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="6564c-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6564c-466">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="6564c-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="6564c-467">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="6564c-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="6564c-468">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="6564c-468">Supported frequencies</span></span>

- <span data-ttu-id="6564c-469">Alles</span><span class="sxs-lookup"><span data-stu-id="6564c-469">All</span></span>
- <span data-ttu-id="6564c-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="6564c-470">EVERYPAY</span></span>
- <span data-ttu-id="6564c-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="6564c-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="6564c-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="6564c-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="6564c-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="6564c-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="6564c-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-474">1OFMTH</span></span>
- <span data-ttu-id="6564c-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-475">LASTOFMTH</span></span>
- <span data-ttu-id="6564c-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-476">2OFMTH</span></span>
- <span data-ttu-id="6564c-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-477">3OFMTH</span></span>
- <span data-ttu-id="6564c-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-478">4OFMTH</span></span>
- <span data-ttu-id="6564c-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-479">5OFMTH</span></span>
- <span data-ttu-id="6564c-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-480">1N2OFMTH</span></span>
- <span data-ttu-id="6564c-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-481">3N4OFMTH</span></span>
- <span data-ttu-id="6564c-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-482">1N3OFMTH</span></span>
- <span data-ttu-id="6564c-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-483">1N4OFMTH</span></span>
- <span data-ttu-id="6564c-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-484">2N3OFMTH</span></span>
- <span data-ttu-id="6564c-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-485">2N4OFMTH</span></span>
- <span data-ttu-id="6564c-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="6564c-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="6564c-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="6564c-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="6564c-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="6564c-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="6564c-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="6564c-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="6564c-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="6564c-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="6564c-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="6564c-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="6564c-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="6564c-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="6564c-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="6564c-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6564c-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="6564c-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6564c-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="6564c-498">Adressen</span><span class="sxs-lookup"><span data-stu-id="6564c-498">Addresses</span></span>

<span data-ttu-id="6564c-499">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="6564c-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="6564c-500">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="6564c-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="6564c-501">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-501">Talent</span></span>          | <span data-ttu-id="6564c-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="6564c-503">Land/regio</span><span class="sxs-lookup"><span data-stu-id="6564c-503">Country/Region</span></span>  | <span data-ttu-id="6564c-504">Landcode</span><span class="sxs-lookup"><span data-stu-id="6564c-504">Country Code</span></span>          |
| <span data-ttu-id="6564c-505">Postcode</span><span class="sxs-lookup"><span data-stu-id="6564c-505">Zip/Postal Code</span></span> | <span data-ttu-id="6564c-506">Postcode</span><span class="sxs-lookup"><span data-stu-id="6564c-506">Postal Code</span></span>           |
| <span data-ttu-id="6564c-507">Provincie</span><span class="sxs-lookup"><span data-stu-id="6564c-507">State</span></span>           | <span data-ttu-id="6564c-508">Staatcode</span><span class="sxs-lookup"><span data-stu-id="6564c-508">State Code</span></span>            |
| <span data-ttu-id="6564c-509">Plaats</span><span class="sxs-lookup"><span data-stu-id="6564c-509">City</span></span>            | <span data-ttu-id="6564c-510">Plaats</span><span class="sxs-lookup"><span data-stu-id="6564c-510">City</span></span>                  |
| <span data-ttu-id="6564c-511">District</span><span class="sxs-lookup"><span data-stu-id="6564c-511">County</span></span>          | <span data-ttu-id="6564c-512">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="6564c-512">County (Municipality)</span></span> |
| <span data-ttu-id="6564c-513">Adres</span><span class="sxs-lookup"><span data-stu-id="6564c-513">Street</span></span>          | <span data-ttu-id="6564c-514">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="6564c-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="6564c-515">Belastingregio's</span><span class="sxs-lookup"><span data-stu-id="6564c-515">Tax regions</span></span>

<span data-ttu-id="6564c-516">Belastingregio's worden gebruikt om de juiste belasting te bepalen die moet worden gebruikt bij het genereren van salarissen.</span><span class="sxs-lookup"><span data-stu-id="6564c-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="6564c-517">Belastingregio's worden aan Dayforce toegewezen als locatieadressen.</span><span class="sxs-lookup"><span data-stu-id="6564c-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="6564c-518">De standaardbelastingregio moet aan de actieve positie van de werknemer worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6564c-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="6564c-519">Belastingregio (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-519">Tax region (required)</span></span>
- <span data-ttu-id="6564c-520">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-520">Country/Region (required)</span></span>
- <span data-ttu-id="6564c-521">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-521">State (required)</span></span>
- <span data-ttu-id="6564c-522">District</span><span class="sxs-lookup"><span data-stu-id="6564c-522">County</span></span> 
- <span data-ttu-id="6564c-523">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="6564c-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="6564c-524">Uw gegevens configureren voor het genereren van salarissen in Mexico</span><span class="sxs-lookup"><span data-stu-id="6564c-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="6564c-525">Als u salarissen genereert voor werknemers in Mexico, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="6564c-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="6564c-526">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="6564c-526">Departments are required on positions.</span></span>
- <span data-ttu-id="6564c-527">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="6564c-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="6564c-528">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="6564c-528">Job types</span></span>

<span data-ttu-id="6564c-529">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="6564c-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="6564c-530">Functietypen zijn vereist voor het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="6564c-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="6564c-531">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="6564c-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6564c-532">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="6564c-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="6564c-533">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="6564c-534">Functietype</span><span class="sxs-lookup"><span data-stu-id="6564c-534">Job type</span></span>   | <span data-ttu-id="6564c-535">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="6564c-536">Per uur</span><span class="sxs-lookup"><span data-stu-id="6564c-536">Hourly</span></span>     | <span data-ttu-id="6564c-537">MX Per uur</span><span class="sxs-lookup"><span data-stu-id="6564c-537">MX Hourly</span></span>   |
| <span data-ttu-id="6564c-538">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="6564c-538">Salaried</span></span>   | <span data-ttu-id="6564c-539">MX Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="6564c-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="6564c-540">Positietypen</span><span class="sxs-lookup"><span data-stu-id="6564c-540">Position types</span></span> 

<span data-ttu-id="6564c-541">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="6564c-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="6564c-542">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="6564c-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="6564c-543">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="6564c-544">Positietype</span><span class="sxs-lookup"><span data-stu-id="6564c-544">Position type</span></span>   | <span data-ttu-id="6564c-545">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="6564c-546">Voltijd</span><span class="sxs-lookup"><span data-stu-id="6564c-546">Full-time</span></span>       | <span data-ttu-id="6564c-547">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="6564c-547">Full time employee</span></span> |
| <span data-ttu-id="6564c-548">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="6564c-548">Part-time</span></span>       | <span data-ttu-id="6564c-549">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="6564c-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="6564c-550">Redencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-550">Reason codes</span></span>

<span data-ttu-id="6564c-551">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="6564c-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="6564c-552">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="6564c-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="6564c-553">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="6564c-554">Redencode</span><span class="sxs-lookup"><span data-stu-id="6564c-554">Reason code</span></span>            | <span data-ttu-id="6564c-555">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-555">Description</span></span>                    | <span data-ttu-id="6564c-556">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="6564c-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="6564c-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="6564c-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="6564c-558">Vertrek voor eerste salaris</span><span class="sxs-lookup"><span data-stu-id="6564c-558">Departure before first payroll</span></span> | <span data-ttu-id="6564c-559">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-559">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="6564c-560">RESIGNATION</span></span>            | <span data-ttu-id="6564c-561">Ontslag</span><span class="sxs-lookup"><span data-stu-id="6564c-561">Resignation</span></span>                    | <span data-ttu-id="6564c-562">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-562">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="6564c-563">PENSION</span></span>                | <span data-ttu-id="6564c-564">Pensioen</span><span class="sxs-lookup"><span data-stu-id="6564c-564">Pension</span></span>                        | <span data-ttu-id="6564c-565">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-565">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="6564c-566">TERMINATION</span></span>            | <span data-ttu-id="6564c-567">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="6564c-567">Termination</span></span>                    | <span data-ttu-id="6564c-568">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-568">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="6564c-569">RETIREMENT</span></span>             | <span data-ttu-id="6564c-570">Pensionering</span><span class="sxs-lookup"><span data-stu-id="6564c-570">Retirement</span></span>                     | <span data-ttu-id="6564c-571">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-571">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="6564c-572">ABSENTEE</span></span>               | <span data-ttu-id="6564c-573">Verzuim</span><span class="sxs-lookup"><span data-stu-id="6564c-573">Absentee</span></span>                       | <span data-ttu-id="6564c-574">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-574">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-575">OTHER</span><span class="sxs-lookup"><span data-stu-id="6564c-575">OTHER</span></span>                  | <span data-ttu-id="6564c-576">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="6564c-576">Other Reasons</span></span>                  | <span data-ttu-id="6564c-577">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-577">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="6564c-578">CLOSURE</span></span>                | <span data-ttu-id="6564c-579">Bedrijfssluiting</span><span class="sxs-lookup"><span data-stu-id="6564c-579">Business Closure</span></span>               | <span data-ttu-id="6564c-580">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-580">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="6564c-581">DEATH</span></span>                  | <span data-ttu-id="6564c-582">Overlijden</span><span class="sxs-lookup"><span data-stu-id="6564c-582">Death</span></span>                          | <span data-ttu-id="6564c-583">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-583">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="6564c-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="6564c-585">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="6564c-585">Leave of Absence</span></span>               | <span data-ttu-id="6564c-586">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-586">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="6564c-587">CONTRACTEND</span></span>            | <span data-ttu-id="6564c-588">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="6564c-588">End of Contract</span></span>                | <span data-ttu-id="6564c-589">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="6564c-589">Terminate worker</span></span>     |
| <span data-ttu-id="6564c-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="6564c-590">SALARYCHANGE</span></span>           | <span data-ttu-id="6564c-591">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="6564c-591">Change of Salary</span></span>               | <span data-ttu-id="6564c-592">Compensatie</span><span class="sxs-lookup"><span data-stu-id="6564c-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="6564c-593">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="6564c-593">Terms of employment</span></span>

<span data-ttu-id="6564c-594">Arbeidsvoorwaarden worden gebruikt om categorieën met arbeidsvoorwaarden te maken.</span><span class="sxs-lookup"><span data-stu-id="6564c-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="6564c-595">De voorwaarden worden toegewezen aan Dayforce als indicatorwaarden voor het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="6564c-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="6564c-596">De volgende arbeidsvoorwaarden en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="6564c-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="6564c-597">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="6564c-597">Terms of employment</span></span>   | <span data-ttu-id="6564c-598">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6564c-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="6564c-599">Normaal</span><span class="sxs-lookup"><span data-stu-id="6564c-599">Regular</span></span>               | <span data-ttu-id="6564c-600">Normaal</span><span class="sxs-lookup"><span data-stu-id="6564c-600">Regular</span></span>     |
| <span data-ttu-id="6564c-601">Direct</span><span class="sxs-lookup"><span data-stu-id="6564c-601">Direct</span></span>                | <span data-ttu-id="6564c-602">Direct</span><span class="sxs-lookup"><span data-stu-id="6564c-602">Direct</span></span>      |
| <span data-ttu-id="6564c-603">Stage</span><span class="sxs-lookup"><span data-stu-id="6564c-603">Internship</span></span>            | <span data-ttu-id="6564c-604">Stage</span><span class="sxs-lookup"><span data-stu-id="6564c-604">Internship</span></span>  |
| <span data-ttu-id="6564c-605">Permanent</span><span class="sxs-lookup"><span data-stu-id="6564c-605">Permanent</span></span>             | <span data-ttu-id="6564c-606">Permanent</span><span class="sxs-lookup"><span data-stu-id="6564c-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="6564c-607">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="6564c-607">Marital status</span></span>

<span data-ttu-id="6564c-608">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6564c-609">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="6564c-610">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-610">Talent</span></span>                 | <span data-ttu-id="6564c-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="6564c-612">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="6564c-612">Married</span></span>                | <span data-ttu-id="6564c-613">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="6564c-613">Married</span></span>                   |
| <span data-ttu-id="6564c-614">Eén</span><span class="sxs-lookup"><span data-stu-id="6564c-614">Single</span></span>                 | <span data-ttu-id="6564c-615">Eén</span><span class="sxs-lookup"><span data-stu-id="6564c-615">Single</span></span>                    |
| <span data-ttu-id="6564c-616">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="6564c-616">Widowed</span></span>                | <span data-ttu-id="6564c-617">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="6564c-617">Widowed</span></span>                   |
| <span data-ttu-id="6564c-618">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="6564c-618">Divorced</span></span>               | <span data-ttu-id="6564c-619">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="6564c-619">Divorced</span></span>                  |
| <span data-ttu-id="6564c-620">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="6564c-620">Registered Partnership</span></span> | <span data-ttu-id="6564c-621">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="6564c-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="6564c-622">None</span><span class="sxs-lookup"><span data-stu-id="6564c-622">None</span></span>                   | <span data-ttu-id="6564c-623">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6564c-624">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="6564c-624">Cohabiting</span></span>             | <span data-ttu-id="6564c-625">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="6564c-626">Geslacht</span><span class="sxs-lookup"><span data-stu-id="6564c-626">Gender</span></span>

<span data-ttu-id="6564c-627">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6564c-628">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="6564c-629">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-629">Talent</span></span>       | <span data-ttu-id="6564c-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="6564c-631">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-631">Male</span></span>         | <span data-ttu-id="6564c-632">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-632">Male</span></span>                      |
| <span data-ttu-id="6564c-633">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-633">Female</span></span>       | <span data-ttu-id="6564c-634">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="6564c-634">Female</span></span>                    |
| <span data-ttu-id="6564c-635">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="6564c-635">Non-specific</span></span> | <span data-ttu-id="6564c-636">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="6564c-637">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="6564c-637">Payment method</span></span>

<span data-ttu-id="6564c-638">Betalingsmethoden bieden de werknemer en het bedrijf een manier om te beschrijven hoe werknemers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="6564c-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="6564c-639">Betalingsmethoden worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6564c-640">In de volgende tabel wordt aangegeven hoe betalingsmethoden worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="6564c-641">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-641">Talent</span></span>             | <span data-ttu-id="6564c-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="6564c-643">Contant geld</span><span class="sxs-lookup"><span data-stu-id="6564c-643">Cash</span></span>               | <span data-ttu-id="6564c-644">Contant geld</span><span class="sxs-lookup"><span data-stu-id="6564c-644">Cash</span></span>                      |
| <span data-ttu-id="6564c-645">Elektronische betaling</span><span class="sxs-lookup"><span data-stu-id="6564c-645">Electronic Payment</span></span> | <span data-ttu-id="6564c-646">Overboeking</span><span class="sxs-lookup"><span data-stu-id="6564c-646">Transfer</span></span>                  |
| <span data-ttu-id="6564c-647">Controle</span><span class="sxs-lookup"><span data-stu-id="6564c-647">Check</span></span>              | <span data-ttu-id="6564c-648">Cheque</span><span class="sxs-lookup"><span data-stu-id="6564c-648">Cheque</span></span>                    |
| <span data-ttu-id="6564c-649">Bankcheque</span><span class="sxs-lookup"><span data-stu-id="6564c-649">Bank Draft</span></span>         | <span data-ttu-id="6564c-650">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6564c-651">Overig</span><span class="sxs-lookup"><span data-stu-id="6564c-651">Other</span></span>              | <span data-ttu-id="6564c-652">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="6564c-653">Bankrekeningtype</span><span class="sxs-lookup"><span data-stu-id="6564c-653">Bank account type</span></span>

<span data-ttu-id="6564c-654">Bankrekeningtypen worden gebruikt voor elektronische betalingen aan werknemers.</span><span class="sxs-lookup"><span data-stu-id="6564c-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="6564c-655">Bankrekeningtypen worden toegewezen aan Dayforce als overdrachtrekeninggegevens.</span><span class="sxs-lookup"><span data-stu-id="6564c-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="6564c-656">De bankrekeningtypen worden, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="6564c-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="6564c-657">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-657">Talent</span></span>            | <span data-ttu-id="6564c-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="6564c-659">Betaalrekening</span><span class="sxs-lookup"><span data-stu-id="6564c-659">Checking Account</span></span>  | <span data-ttu-id="6564c-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="6564c-660">CheckingAccount</span></span>           |
| <span data-ttu-id="6564c-661">Salarisrekening</span><span class="sxs-lookup"><span data-stu-id="6564c-661">Payroll Account</span></span>   | <span data-ttu-id="6564c-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="6564c-662">PayrollAccount</span></span>            |
| <span data-ttu-id="6564c-663">Spaarrekening</span><span class="sxs-lookup"><span data-stu-id="6564c-663">Savings Account</span></span>   | <span data-ttu-id="6564c-664">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6564c-665">BankGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="6564c-665">BankGirot account</span></span> | <span data-ttu-id="6564c-666">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6564c-667">PlusGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="6564c-667">PlusGirot account</span></span> | <span data-ttu-id="6564c-668">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="6564c-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="6564c-669">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="6564c-669">Earning codes</span></span>

<span data-ttu-id="6564c-670">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="6564c-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6564c-671">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="6564c-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="6564c-672">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="6564c-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="6564c-673">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="6564c-673">Supported frequencies</span></span>

- <span data-ttu-id="6564c-674">Alles</span><span class="sxs-lookup"><span data-stu-id="6564c-674">All</span></span>
- <span data-ttu-id="6564c-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="6564c-675">EVERYPAY</span></span>
- <span data-ttu-id="6564c-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="6564c-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="6564c-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="6564c-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="6564c-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="6564c-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="6564c-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-679">1OFMTH</span></span>
- <span data-ttu-id="6564c-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-680">LASTOFMTH</span></span>
- <span data-ttu-id="6564c-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-681">2OFMTH</span></span>
- <span data-ttu-id="6564c-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-682">3OFMTH</span></span>
- <span data-ttu-id="6564c-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-683">4OFMTH</span></span>
- <span data-ttu-id="6564c-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-684">5OFMTH</span></span>
- <span data-ttu-id="6564c-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-685">1N2OFMTH</span></span>
- <span data-ttu-id="6564c-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-686">3N4OFMTH</span></span>
- <span data-ttu-id="6564c-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-687">1N3OFMTH</span></span>
- <span data-ttu-id="6564c-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-688">1N4OFMTH</span></span>
- <span data-ttu-id="6564c-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-689">2N3OFMTH</span></span>
- <span data-ttu-id="6564c-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-690">2N4OFMTH</span></span>
- <span data-ttu-id="6564c-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="6564c-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="6564c-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="6564c-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="6564c-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6564c-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="6564c-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="6564c-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="6564c-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="6564c-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="6564c-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="6564c-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="6564c-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="6564c-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="6564c-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="6564c-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="6564c-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6564c-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="6564c-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6564c-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="6564c-703">Adressen</span><span class="sxs-lookup"><span data-stu-id="6564c-703">Addresses</span></span>

<span data-ttu-id="6564c-704">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="6564c-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="6564c-705">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="6564c-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="6564c-706">Talent</span><span class="sxs-lookup"><span data-stu-id="6564c-706">Talent</span></span>              | <span data-ttu-id="6564c-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6564c-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="6564c-708">Land/regio</span><span class="sxs-lookup"><span data-stu-id="6564c-708">Country/Region</span></span>      | <span data-ttu-id="6564c-709">Landcode</span><span class="sxs-lookup"><span data-stu-id="6564c-709">Country Code</span></span>          |
| <span data-ttu-id="6564c-710">Postcode</span><span class="sxs-lookup"><span data-stu-id="6564c-710">Zip/Postal Code</span></span>     | <span data-ttu-id="6564c-711">Postcode</span><span class="sxs-lookup"><span data-stu-id="6564c-711">Postal Code</span></span>           |
| <span data-ttu-id="6564c-712">Provincie</span><span class="sxs-lookup"><span data-stu-id="6564c-712">State</span></span>               | <span data-ttu-id="6564c-713">Staatcode</span><span class="sxs-lookup"><span data-stu-id="6564c-713">State Code</span></span>            |
| <span data-ttu-id="6564c-714">Plaats</span><span class="sxs-lookup"><span data-stu-id="6564c-714">City</span></span>                | <span data-ttu-id="6564c-715">Plaats</span><span class="sxs-lookup"><span data-stu-id="6564c-715">City</span></span>                  |
| <span data-ttu-id="6564c-716">District</span><span class="sxs-lookup"><span data-stu-id="6564c-716">County</span></span>              | <span data-ttu-id="6564c-717">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="6564c-717">County (Municipality)</span></span> |
| <span data-ttu-id="6564c-718">Adres</span><span class="sxs-lookup"><span data-stu-id="6564c-718">Street</span></span>              | <span data-ttu-id="6564c-719">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="6564c-719">Address Line 1</span></span>        |
| <span data-ttu-id="6564c-720">Huisnummer</span><span class="sxs-lookup"><span data-stu-id="6564c-720">Street Number</span></span>       | <span data-ttu-id="6564c-721">Adresregel 2</span><span class="sxs-lookup"><span data-stu-id="6564c-721">Address Line 2</span></span>        |
| <span data-ttu-id="6564c-722">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="6564c-722">Building Complement</span></span> | <span data-ttu-id="6564c-723">Adresregel 5</span><span class="sxs-lookup"><span data-stu-id="6564c-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="6564c-724">Paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="6564c-724">Passport number</span></span>

<span data-ttu-id="6564c-725">Werknemers kunnen paspoortgegevens opgeven.</span><span class="sxs-lookup"><span data-stu-id="6564c-725">Employees can declare passport information.</span></span> <span data-ttu-id="6564c-726">Deze informatie is van het identificatietype **Paspoort** en wordt in Dayforce geïntegreerd als onderdeel van de Mexico-specifieke informatie van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="6564c-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="6564c-727">Identificatietype = 'Paspoort'</span><span class="sxs-lookup"><span data-stu-id="6564c-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="6564c-728">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="6564c-728">Issued Date</span></span>
- <span data-ttu-id="6564c-729">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="6564c-729">Expiration Date</span></span>

<span data-ttu-id="6564c-730">Werknemers kunnen meerdere identificatienummers van het identificatietype **Paspoort** opgeven.</span><span class="sxs-lookup"><span data-stu-id="6564c-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="6564c-731">Echter alleen de huidige actieve paspoortvermelding wordt geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="6564c-732">Als alle paspoortvermeldingen zijn verlopen, wordt het paspoort dat als laatste is uitgegeven geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6564c-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
