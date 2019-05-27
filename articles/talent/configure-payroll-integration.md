---
title: De integratie van de salarisadministratie tussen Talent en Dayforce configureren
description: In dit onderwerp wordt uitgelegd hoe de integratie tussen Microsoft Dynamics 365 for Talent en Ceridian Dayforce wordt geconfigureerd zodat u een betaling kunt verwerken.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517668"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="d6401-103">De integratie van de salarisadministratie tussen Talent en Dayforce configureren</span><span class="sxs-lookup"><span data-stu-id="d6401-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6401-104">De integratie tussen Microsoft Dynamics 365 for Talent en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen die in dit onderwerp worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="d6401-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="d6401-105">Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Talent als Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d6401-106">Als u een service zoals Dayforce gebruikt voor het uitvoeren van betalingen, moet u de integratie inschakelen in Talent.</span><span class="sxs-lookup"><span data-stu-id="d6401-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="d6401-107">De integratie vereist specifieke gegevens vanuit Talent.</span><span class="sxs-lookup"><span data-stu-id="d6401-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="d6401-108">Daarom moet u controleren of gegevens die zijn toegewezen aan Dayforce zodanig in Talent zijn geconfigureerd dat de integratie wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d6401-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="d6401-109">De integratie maakt gebruik van de volgende brede categorieën gegevens:</span><span class="sxs-lookup"><span data-stu-id="d6401-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d6401-110">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-110">Human resources data</span></span>
- <span data-ttu-id="d6401-111">Compensatiegegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-111">Compensation data</span></span>
- <span data-ttu-id="d6401-112">Salarisgegevens, zoals betalingscycli, salarisperioden en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d6401-113">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-113">Worker data</span></span>

<span data-ttu-id="d6401-114">In dit onderwerp worden de stappen beschreven die u moet volgen om de integratie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d6401-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d6401-115">Ook wordt uitgelegd welke typen gegevens en welke configuratiedetails vereist zijn voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d6401-116">De integratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="d6401-116">Enable the integration</span></span>

<span data-ttu-id="d6401-117">In Talent moet u de integratie inschakelen en de configuratiegegevens invoeren om verbinding te maken met Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d6401-118">Als u wilt dat de grootboektransactie die wordt geproduceerd wordt geïmporteerd in Microsoft Dynamics 365 for Finance and Operations, moet u ook een Microsoft Azure-opslagaccount instellen en de verbindingstekenreeks voor Azure Storage invoeren in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d6401-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="d6401-119">Voer de volgende stappen uit om de integratie in Talent in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d6401-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="d6401-120">Ga naar de pagina **Systeembeheer** en selecteer **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="d6401-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d6401-121">Voer het beveiligde FTP-eindpunt (File Transfer Protocol) en het pad naar de beveiligde FTP-map in.</span><span class="sxs-lookup"><span data-stu-id="d6401-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d6401-122">Voer de gebruikersnaam en het wachtwoord in van de gebruiker die toegang krijgt tot het beveiligde FTP-eindpunt en het mappad.</span><span class="sxs-lookup"><span data-stu-id="d6401-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d6401-123">Test de verbinding, zoals vereist, en stel de optie **Integratie van salarisadministratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d6401-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d6401-124">Wanneer de integratie is ingeschakeld, worden het pakket voor gegevensexport en de bestanden gemaakt en wordt de frequentie ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d6401-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d6401-125">U kunt deze frequentie naar behoefte wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d6401-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="d6401-126">Zie de volgende Azure-onderwerpen voor meer informatie over Azure-opslagaccounts en verbindingstekenreeksen voor Azure Storage:</span><span class="sxs-lookup"><span data-stu-id="d6401-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="d6401-127">Informatie over Azure-opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="d6401-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d6401-128">Verbindingstekenreeks voor Azure Storage configureren</span><span class="sxs-lookup"><span data-stu-id="d6401-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="d6401-129">Uw gegevens configureren</span><span class="sxs-lookup"><span data-stu-id="d6401-129">Configure your data</span></span> 

<span data-ttu-id="d6401-130">Om salarissen te kunnen verwerken, moet u HRM-gegevens configureren in Talent.</span><span class="sxs-lookup"><span data-stu-id="d6401-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="d6401-131">U moet gegevens over de organisatie, zoals taken en functies, instellen samen met informatie over vergoedingen en compensatie.</span><span class="sxs-lookup"><span data-stu-id="d6401-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d6401-132">Deze informatie biedt de informatie over dienstverband, salaris en inhoudingen die vereist is om het salaris van werknemers te genereren.</span><span class="sxs-lookup"><span data-stu-id="d6401-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d6401-133">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d6401-134">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="d6401-134">Benefits</span></span> 

<span data-ttu-id="d6401-135">Human resources biedt hulpmiddelen voor het instellen en onderhouden van de vergoedingen, inhoudingen en compensatieplannen van medewerkers die een organisatie zijn medewerkers biedt.</span><span class="sxs-lookup"><span data-stu-id="d6401-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d6401-136">Wanneer u vergoedingen maakt, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d6401-137">Vergoedingsplannen</span><span class="sxs-lookup"><span data-stu-id="d6401-137">Benefit plans</span></span>

- <span data-ttu-id="d6401-138">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-138">Plan (required)</span></span>
- <span data-ttu-id="d6401-139">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-139">Type (required)</span></span>
- <span data-ttu-id="d6401-140">Gevolgen voor salaris (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-140">Payroll impact (required)</span></span>
- <span data-ttu-id="d6401-141">Achterstallige betalingen herstellen</span><span class="sxs-lookup"><span data-stu-id="d6401-141">Recover arrears</span></span>
- <span data-ttu-id="d6401-142">Inhoudingsmethode</span><span class="sxs-lookup"><span data-stu-id="d6401-142">Deduction method</span></span>
- <span data-ttu-id="d6401-143">Inhoudingsprioriteit</span><span class="sxs-lookup"><span data-stu-id="d6401-143">Deduction priority</span></span>
- <span data-ttu-id="d6401-144">Limietperiode</span><span class="sxs-lookup"><span data-stu-id="d6401-144">Limit period</span></span>
- <span data-ttu-id="d6401-145">Bedrag beperken</span><span class="sxs-lookup"><span data-stu-id="d6401-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d6401-146">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="d6401-146">Benefits</span></span>

- <span data-ttu-id="d6401-147">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-147">Plan (required)</span></span>
- <span data-ttu-id="d6401-148">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-148">Type (required)</span></span>
- <span data-ttu-id="d6401-149">Optie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-149">Option (required)</span></span>
- <span data-ttu-id="d6401-150">Vergoeding-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-150">Benefit ID (required)</span></span>
- <span data-ttu-id="d6401-151">Frequentie</span><span class="sxs-lookup"><span data-stu-id="d6401-151">Frequency</span></span>
- <span data-ttu-id="d6401-152">Basis</span><span class="sxs-lookup"><span data-stu-id="d6401-152">Basis</span></span>
- <span data-ttu-id="d6401-153">Bedrag of tarief</span><span class="sxs-lookup"><span data-stu-id="d6401-153">Amount or rate</span></span>
- <span data-ttu-id="d6401-154">Inkomstencode</span><span class="sxs-lookup"><span data-stu-id="d6401-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d6401-155">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="d6401-155">Supported frequencies</span></span> 

- <span data-ttu-id="d6401-156">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="d6401-156">Weekly</span></span>
- <span data-ttu-id="d6401-157">Tweewekelijks</span><span class="sxs-lookup"><span data-stu-id="d6401-157">Bi-weekly</span></span>
- <span data-ttu-id="d6401-158">Halfmaandelijks</span><span class="sxs-lookup"><span data-stu-id="d6401-158">Semi-monthly</span></span>
- <span data-ttu-id="d6401-159">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="d6401-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d6401-160">Ondersteund bases</span><span class="sxs-lookup"><span data-stu-id="d6401-160">Supported bases</span></span> 

- <span data-ttu-id="d6401-161">Vast bedrag</span><span class="sxs-lookup"><span data-stu-id="d6401-161">Fixed amount</span></span>
- <span data-ttu-id="d6401-162">Percentage van inkomsten</span><span class="sxs-lookup"><span data-stu-id="d6401-162">Percent of earnings</span></span>
- <span data-ttu-id="d6401-163">Productieve uren</span><span class="sxs-lookup"><span data-stu-id="d6401-163">Productive hours</span></span>

<span data-ttu-id="d6401-164">Dayforce maakt de volgende inhoudingen, op basis van de salarisgevolgen die zijn gedefinieerd voor het vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="d6401-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d6401-165">Selectie in Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-165">Selection in Talent</span></span>        | <span data-ttu-id="d6401-166">Resultaat in Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d6401-167">None</span><span class="sxs-lookup"><span data-stu-id="d6401-167">None</span></span>                       | <span data-ttu-id="d6401-168">Er wordt geen inhouding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6401-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="d6401-169">Alleen inhouding</span><span class="sxs-lookup"><span data-stu-id="d6401-169">Deduction only</span></span>             | <span data-ttu-id="d6401-170">Er wordt een inhouding voor de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6401-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d6401-171">Alleen bijdrage</span><span class="sxs-lookup"><span data-stu-id="d6401-171">Contribution only</span></span>          | <span data-ttu-id="d6401-172">Er wordt een inhouding voor de werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6401-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d6401-173">Inhouding en bijdrage</span><span class="sxs-lookup"><span data-stu-id="d6401-173">Deduction and contribution</span></span> | <span data-ttu-id="d6401-174">Er worden inhoudingen voor werknemer en werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6401-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d6401-175">Zie de volgende onderwerpen voor meer informatie over het definiëren en beheren van een vergoedingsprogramma:</span><span class="sxs-lookup"><span data-stu-id="d6401-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="d6401-176">Een vergoedingenprogramma voor werknemers maken</span><span class="sxs-lookup"><span data-stu-id="d6401-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d6401-177">Een nieuwe vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="d6401-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d6401-178">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="d6401-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d6401-179">Vergoedingen inschrijven en verwijderen van medewerkers</span><span class="sxs-lookup"><span data-stu-id="d6401-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d6401-180">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d6401-180">Compensation</span></span> 

<span data-ttu-id="d6401-181">Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren.</span><span class="sxs-lookup"><span data-stu-id="d6401-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d6401-182">Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd.</span><span class="sxs-lookup"><span data-stu-id="d6401-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d6401-183">De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="d6401-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d6401-184">Dayforce gebruikt compensatie-informatie voor het berekenen van het uur- of jaartarief van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d6401-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d6401-185">Er zijn vastecompensatieplannen en conversies van het loontarief vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d6401-186">Werknemers moeten worden gekoppeld aan een vastecompensatieplan.</span><span class="sxs-lookup"><span data-stu-id="d6401-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d6401-187">Zie de volgende onderwerpen voor meer informatie over compensatieplannen:</span><span class="sxs-lookup"><span data-stu-id="d6401-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="d6401-188">Plannen voor vaste compensatie maken</span><span class="sxs-lookup"><span data-stu-id="d6401-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d6401-189">Plannen voor variabele compensatie maken</span><span class="sxs-lookup"><span data-stu-id="d6401-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d6401-190">Salaris-/compensatiestructuur en -plannen ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="d6401-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d6401-191">Compensatie verwerken</span><span class="sxs-lookup"><span data-stu-id="d6401-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d6401-192">Compensatieproces definiëren en resultaten berekenen</span><span class="sxs-lookup"><span data-stu-id="d6401-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d6401-193">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="d6401-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d6401-194">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="d6401-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d6401-195">Taken</span><span class="sxs-lookup"><span data-stu-id="d6401-195">Jobs</span></span> 

<span data-ttu-id="d6401-196">Een functie is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een functie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="d6401-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d6401-197">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d6401-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d6401-198">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="d6401-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d6401-199">Nieuwe taken definiëren</span><span class="sxs-lookup"><span data-stu-id="d6401-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d6401-200">Posities</span><span class="sxs-lookup"><span data-stu-id="d6401-200">Positions</span></span>

<span data-ttu-id="d6401-201">Een positie is een afzonderlijk exemplaar van een taak.</span><span class="sxs-lookup"><span data-stu-id="d6401-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="d6401-202">De positie 'Verkoopmanager (Oost)' is bijvoorbeeld een van de posities die zijn gekoppeld aan de functie 'Verkoopmanager'.</span><span class="sxs-lookup"><span data-stu-id="d6401-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d6401-203">Een positie bestaat op een afdeling.</span><span class="sxs-lookup"><span data-stu-id="d6401-203">A position exists in a department.</span></span> <span data-ttu-id="d6401-204">Aan elke positie kan slechts één medewerker worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d6401-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d6401-205">Let op de volgende gegevens en configuratie bij het instellen van posities:</span><span class="sxs-lookup"><span data-stu-id="d6401-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d6401-206">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-206">Position (required)</span></span>
- <span data-ttu-id="d6401-207">Beschrijving (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-207">Description (required)</span></span>
- <span data-ttu-id="d6401-208">Functie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-208">Job (required)</span></span>
- <span data-ttu-id="d6401-209">Afdeling (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-209">Department (required)</span></span>
- <span data-ttu-id="d6401-210">Positietype (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-210">Position type (required)</span></span>
- <span data-ttu-id="d6401-211">Voltijdse equivalent</span><span class="sxs-lookup"><span data-stu-id="d6401-211">Full-time equivalent</span></span>
- <span data-ttu-id="d6401-212">Jaarlijkse normale uren (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="d6401-213">Betaald door rechtspersoon (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d6401-214">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-214">Pay cycle (required)</span></span>
- <span data-ttu-id="d6401-215">Standaard financiële dimensie: kostenplaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d6401-216">Medewerkertoewijzing: medewerker, toewijzing begin, einde toewijzing, redencode</span><span class="sxs-lookup"><span data-stu-id="d6401-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d6401-217">Als meerdere posities op dezelfde afdeling aan dezelfde functie zijn gekoppeld, worden deze geconsolideerd in een enkele positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d6401-218">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d6401-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d6401-219">Uw werknemers organiseren met afdelingen, taken en posities</span><span class="sxs-lookup"><span data-stu-id="d6401-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d6401-220">Posities instellen</span><span class="sxs-lookup"><span data-stu-id="d6401-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d6401-221">Afdelingen</span><span class="sxs-lookup"><span data-stu-id="d6401-221">Departments</span></span>

<span data-ttu-id="d6401-222">Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt.</span><span class="sxs-lookup"><span data-stu-id="d6401-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d6401-223">Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR.</span><span class="sxs-lookup"><span data-stu-id="d6401-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d6401-224">U kunt afdelingen gebruiken om te rapporteren over functiegebieden.</span><span class="sxs-lookup"><span data-stu-id="d6401-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d6401-225">Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.</span><span class="sxs-lookup"><span data-stu-id="d6401-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d6401-226">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d6401-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d6401-227">Een afdeling maken en koppelen aan de afdelingshiërarchie</span><span class="sxs-lookup"><span data-stu-id="d6401-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d6401-228">Nieuwe afdelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="d6401-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d6401-229">Betalingscycli en salarisperioden</span><span class="sxs-lookup"><span data-stu-id="d6401-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="d6401-230">Een betalingscyclus bepaalt hoe vaak salarissen worden berekend en op welke specifieke dagen medewerkers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="d6401-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d6401-231">Zo kan bijvooorbeeld een betalingscyclus maandelijks zijn en kunnen werknemers worden uitbetaald op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="d6401-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d6401-232">Een betalingscyclus kan ook wekelijks en werknemers kunnen worden uitbetaald op de dinsdag na het einde van de salarisperiode.</span><span class="sxs-lookup"><span data-stu-id="d6401-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d6401-233">Betalingscycli zijn toegewezen aan posities om te bepalen wanneer medewerkers in deze posities worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="d6401-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d6401-234">Nadat u betalingscycli hebt gemaakt, kunt u salarisperioden voor elke cyclus genereren.</span><span class="sxs-lookup"><span data-stu-id="d6401-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d6401-235">Elke salarisperiode bevat een standaard betalingsdatum die is gebaseerd op gegevens die u verstrekt.</span><span class="sxs-lookup"><span data-stu-id="d6401-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d6401-236">U kunt echter de standaard betalingsdatum in een salarisperiode wijzigen om te voorzien in uitzonderingen, bijvoorbeeld wanneer de betalingsdatum op een feestdag valt.</span><span class="sxs-lookup"><span data-stu-id="d6401-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d6401-237">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="d6401-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d6401-238">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-238">Pay cycle (required)</span></span>
- <span data-ttu-id="d6401-239">Frequentie van betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d6401-240">Begindatum van periode (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d6401-241">Standaardbetalingsdatum (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d6401-242">Deze informatie is geïntegreerd met Dayforce als betalingsgroepen en worden gescheiden per land of regio voor elke betalingscyclus.</span><span class="sxs-lookup"><span data-stu-id="d6401-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d6401-243">Vóór integratie moet ten minste één salarisperiode worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d6401-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d6401-244">Dayforce genereert van betalingsgroepkalenders en betalingsdatums, op basis van de begindatum van de eerste salarisperiode en de standaardbetalingsdatum die is ingesteld in Talent.</span><span class="sxs-lookup"><span data-stu-id="d6401-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d6401-245">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-245">Earning codes</span></span>

<span data-ttu-id="d6401-246">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d6401-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d6401-247">De codes hebben verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="d6401-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d6401-248">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="d6401-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d6401-249">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-249">Earning Code (required)</span></span>
- <span data-ttu-id="d6401-250">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-250">Description</span></span>
- <span data-ttu-id="d6401-251">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="d6401-251">Unit of measure</span></span>
- <span data-ttu-id="d6401-252">Productief</span><span class="sxs-lookup"><span data-stu-id="d6401-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d6401-253">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-253">Worker data</span></span>

<span data-ttu-id="d6401-254">Records voor de verschillende soorten medewerkers die u hebt zijn belangrijk voor uw HRM- en salarisadministratiesystemen.</span><span class="sxs-lookup"><span data-stu-id="d6401-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d6401-255">De gegevens die u invoert, kunnen worden gebruikt om medewerkers en persoonlijke gegevens bij te houden.</span><span class="sxs-lookup"><span data-stu-id="d6401-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d6401-256">U kunt de volgende informatie bijhouden voor medewerkers:</span><span class="sxs-lookup"><span data-stu-id="d6401-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d6401-257">**Basis** – Basisinformatie over een medewerker bijhouden, zoals contactgegevens, demografische gegevens, identificatiegegevens, informatie over de familie, status van militaire dienst, expat-informatie en contactpersonen voor noodgevallen.</span><span class="sxs-lookup"><span data-stu-id="d6401-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d6401-258">**Dienstverband** – Informatie bijhouden over werkgelegenheid van een medewerker, zoals een aansluiting met een bedrijf of organisatie, functie, start- en einddatums, arbeidsgeschiktheid, arbeidsvoorwaarden, pensioen, verlof en relocatie-informatie.</span><span class="sxs-lookup"><span data-stu-id="d6401-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d6401-259">**Verlof en verzuim** – Informatie bijhouden over de afwezigheid van een medewerker, zoals werkkalenders, verzuimtransacties en verzuiminstellingen.</span><span class="sxs-lookup"><span data-stu-id="d6401-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d6401-260">**Vergoedingen en salarissen** – Informatie bijhouden over compensatieplannen en salarisgegevens van een medewerker zoals inschrijving op plan, onderscheidingen, commissie, fiscale informatie, pensioen en salarisinhoudingen.</span><span class="sxs-lookup"><span data-stu-id="d6401-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d6401-261">Wanneer u informatie over een werknemer invoert, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d6401-262">Algemene informatie</span><span class="sxs-lookup"><span data-stu-id="d6401-262">General information</span></span>

- <span data-ttu-id="d6401-263">Personeelsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-263">Personnel number (required)</span></span>
- <span data-ttu-id="d6401-264">Voornaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-264">First name (required)</span></span>
- <span data-ttu-id="d6401-265">Achternaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-265">Last name (required)</span></span>
- <span data-ttu-id="d6401-266">Tweede naam</span><span class="sxs-lookup"><span data-stu-id="d6401-266">Middle name</span></span>
- <span data-ttu-id="d6401-267">Anciënniteitsdatum</span><span class="sxs-lookup"><span data-stu-id="d6401-267">Seniority date</span></span>
- <span data-ttu-id="d6401-268">Bekend als</span><span class="sxs-lookup"><span data-stu-id="d6401-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d6401-269">Persoonlijke informatie</span><span class="sxs-lookup"><span data-stu-id="d6401-269">Personal information</span></span>

- <span data-ttu-id="d6401-270">Burgerlijke staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-270">Marital status (required)</span></span>
- <span data-ttu-id="d6401-271">Geboortedatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-271">Birth date (required)</span></span>
- <span data-ttu-id="d6401-272">Geslacht (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-272">Gender (required)</span></span>
- <span data-ttu-id="d6401-273">Persoon met handicap</span><span class="sxs-lookup"><span data-stu-id="d6401-273">Person with disabilities</span></span>
- <span data-ttu-id="d6401-274">Land/regio nationaliteit (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="d6401-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d6401-275">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-275">Address information</span></span>

- <span data-ttu-id="d6401-276">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-276">Primary (required)</span></span>
- <span data-ttu-id="d6401-277">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-277">Country/region (required)</span></span>
- <span data-ttu-id="d6401-278">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-278">Postal code (required)</span></span>
- <span data-ttu-id="d6401-279">Huisnummer (vereist) (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="d6401-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d6401-280">Gebouwtoevoeging (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="d6401-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d6401-281">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-281">City (required)</span></span>
- <span data-ttu-id="d6401-282">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-282">State (required)</span></span>
- <span data-ttu-id="d6401-283">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d6401-284">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="d6401-284">Contact information</span></span> 

- <span data-ttu-id="d6401-285">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-285">Primary (required)</span></span>
- <span data-ttu-id="d6401-286">Contactnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-286">Contact number (required)</span></span>
- <span data-ttu-id="d6401-287">Toestel</span><span class="sxs-lookup"><span data-stu-id="d6401-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d6401-288">Salarisinformatie en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-288">Payroll information and earning codes</span></span>

<span data-ttu-id="d6401-289">Aan werknemers kunnen bepaalde inkomsten met een bepaalde betalingsfrequentie worden toegewezen en zij kunnen een geprefereerde betalingsmethode hebben.</span><span class="sxs-lookup"><span data-stu-id="d6401-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d6401-290">De volgende velden worden gebruikt in Dayforce om te garanderen dat deze voorkeuren en instellingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6401-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d6401-291">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-291">Earning codes</span></span>

- <span data-ttu-id="d6401-292">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-292">Position (required)</span></span>
- <span data-ttu-id="d6401-293">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-293">Earning Code (required)</span></span>
- <span data-ttu-id="d6401-294">Frequentie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-294">Frequency (required)</span></span>
- <span data-ttu-id="d6401-295">Bedrag (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d6401-296">Salarisinformatie</span><span class="sxs-lookup"><span data-stu-id="d6401-296">Payroll information</span></span>

- <span data-ttu-id="d6401-297">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="d6401-297">Payment Method</span></span>
- <span data-ttu-id="d6401-298">Economische regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-298">Economic Region (required)</span></span>
- <span data-ttu-id="d6401-299">Id personeelsvergoedingen</span><span class="sxs-lookup"><span data-stu-id="d6401-299">Employee Benefits ID</span></span>
- <span data-ttu-id="d6401-300">Nationaal id-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-300">National ID Number (required)</span></span>
- <span data-ttu-id="d6401-301">Nummer militaire dienst</span><span class="sxs-lookup"><span data-stu-id="d6401-301">Military Service Number</span></span>
- <span data-ttu-id="d6401-302">Ploeg-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-302">Shift ID (required)</span></span>
- <span data-ttu-id="d6401-303">Btw-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-303">Tax Number (required)</span></span>
- <span data-ttu-id="d6401-304">Vakbond-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-304">Union ID (required)</span></span>
- <span data-ttu-id="d6401-305">Werkdag-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-305">Work Day ID (required)</span></span>
- <span data-ttu-id="d6401-306">Nummer werkvergunning</span><span class="sxs-lookup"><span data-stu-id="d6401-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d6401-307">Voor de betalingsmethode ondersteunt Mexico **Contant geld**, **Cheque** (de fysieke cheque van het bedrijf) en **Elektronische betaling**.</span><span class="sxs-lookup"><span data-stu-id="d6401-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d6401-308">Als geen betalingsmethode is opgegeven, wordt standaard **Cheque** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6401-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d6401-309">Details dienstverband</span><span class="sxs-lookup"><span data-stu-id="d6401-309">Employment details</span></span>

<span data-ttu-id="d6401-310">Historische gegevens over het dienstverband worden gebruikt als belangrijkste informatie voor het opvragen van de statussen voor aanstellen, ontslaan en opnieuw aanstellen van een werknemer in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d6401-311">Dayforce ondersteunt slechts één actieve dienstverbandrecord tegelijk.</span><span class="sxs-lookup"><span data-stu-id="d6401-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d6401-312">Begindatum dienstverband (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-312">Employment start date (required)</span></span>
- <span data-ttu-id="d6401-313">Einddatum dienstverband</span><span class="sxs-lookup"><span data-stu-id="d6401-313">Employment end date</span></span>
- <span data-ttu-id="d6401-314">Begindatum</span><span class="sxs-lookup"><span data-stu-id="d6401-314">Start date</span></span>
- <span data-ttu-id="d6401-315">Aangepaste begindatum</span><span class="sxs-lookup"><span data-stu-id="d6401-315">Adjusted start date</span></span>
- <span data-ttu-id="d6401-316">Ontslagdatum (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="d6401-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d6401-317">Ontslagreden (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="d6401-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d6401-318">De belangrijkste datums van een werknemer worden afgeleid met behulp van de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="d6401-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d6401-319">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-319">Talent</span></span>                | <span data-ttu-id="d6401-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6401-321">Meest recente huurdatum</span><span class="sxs-lookup"><span data-stu-id="d6401-321">Most recent hire date</span></span> | <span data-ttu-id="d6401-322">Begindatum van dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="d6401-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d6401-323">Ontslagdatum</span><span class="sxs-lookup"><span data-stu-id="d6401-323">Termination date</span></span>      | <span data-ttu-id="d6401-324">Ontslagdatum van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="d6401-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d6401-325">Begindatum</span><span class="sxs-lookup"><span data-stu-id="d6401-325">Start date</span></span>            | <span data-ttu-id="d6401-326">Aangepaste begindatum, begindatum of begindatum dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="d6401-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d6401-327">Oorspronkelijke datum indiensttreding</span><span class="sxs-lookup"><span data-stu-id="d6401-327">Original hire date</span></span>    | <span data-ttu-id="d6401-328">Begindatum dienstverband van vroegste historierecord van dienstverband</span><span class="sxs-lookup"><span data-stu-id="d6401-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d6401-329">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d6401-329">Compensation</span></span>

<span data-ttu-id="d6401-330">Een vastecompensatieplan moet worden gekoppeld aan de primaire functie van elke werknemer tijdens de hele duur van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="d6401-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d6401-331">Deze periode begint op de datum waarop de werknemer in dienst is genomen (of de begindatum van het dienstverband) en gaat door totdat aan het ontslag.</span><span class="sxs-lookup"><span data-stu-id="d6401-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d6401-332">Ingangsdatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-332">Effective Date (required)</span></span>
- <span data-ttu-id="d6401-333">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d6401-333">Expiration date</span></span>
- <span data-ttu-id="d6401-334">Loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-334">Pay Rate (required)</span></span>
- <span data-ttu-id="d6401-335">Conversies van loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d6401-336">Jaarlijks equivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="d6401-337">Uurequivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="d6401-338">Als een werknemer met uurtarief meerdere posities heeft, wordt de vaste compensatie van de primaire positie geïmporteerd in Dayforce als het basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="d6401-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d6401-339">Voor niet-primaire posities, wordt het uurtarief opgeslagen bij de overeenkomende positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d6401-340">Als een medewerker met een salaris meerdere posities heeft, worden het cumulatieve uurtarief en het jaarsalaris voor alle actieve posities afgeleid en gebruikt als de basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="d6401-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d6401-341">Identificatienummers</span><span class="sxs-lookup"><span data-stu-id="d6401-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d6401-342">Sociaal-fiscaal nummer</span><span class="sxs-lookup"><span data-stu-id="d6401-342">Social Security identifier</span></span> 

<span data-ttu-id="d6401-343">Elke werknemer moet één primaire id hebben.</span><span class="sxs-lookup"><span data-stu-id="d6401-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d6401-344">Deze id moet van het identificatietype **Sofinummer** zijn.</span><span class="sxs-lookup"><span data-stu-id="d6401-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d6401-345">In Dayforce, wordt dit automatisch afgeleid als het sociaal-fiscaal nummer van de werknemer dat is vereist voor aanstelling.</span><span class="sxs-lookup"><span data-stu-id="d6401-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d6401-346">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-346">Primary (required)</span></span>
- <span data-ttu-id="d6401-347">Identificatietype = 'Sofinummer'</span><span class="sxs-lookup"><span data-stu-id="d6401-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d6401-348">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="d6401-348">Issued Date</span></span>
- <span data-ttu-id="d6401-349">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d6401-349">Expiration Date</span></span>

<span data-ttu-id="d6401-350">Werknemers kunnen meerdere identificatienummers van het identificatietype **Sofinummer** opgeven.</span><span class="sxs-lookup"><span data-stu-id="d6401-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d6401-351">Alleen de record die is gemarkeerd als **Primair** wordt echter opgenomen in Dayforce, ongeacht of het nummer actief of verlopen is.</span><span class="sxs-lookup"><span data-stu-id="d6401-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d6401-352">Bankrekeningen en voorschotten</span><span class="sxs-lookup"><span data-stu-id="d6401-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="d6401-353">Er moet geldige bankrekeninginformatie worden ingevoerd voor elke werknemer die wil worden uitbetaald via bankrekeningoverboekingen.</span><span class="sxs-lookup"><span data-stu-id="d6401-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d6401-354">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-354">Talent</span></span>                         | <span data-ttu-id="d6401-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6401-356">Bankrekeningnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d6401-357">SWIFT-code (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-357">SWIFT code (required)</span></span>          | <span data-ttu-id="d6401-358">Veld **Bank-id** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="d6401-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d6401-359">Vestigingsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d6401-360">Bankrekeningtype (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-360">Bank account type (required)</span></span>   | <span data-ttu-id="d6401-361">Veld **Rekeningtype** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="d6401-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d6401-362">Ondersteunde waarden zijn **Rekening-courant** en **Salaris**.</span><span class="sxs-lookup"><span data-stu-id="d6401-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d6401-363">Werknemers die ervoor kiezen om te worden uitbetaald via bankrekeningoverboekingen moeten een koppeling opgeven naar een restantrekening die zich onder een rechtspersoon bevindt met het primaire adres in Mexico en die is gekoppeld aan een geldige bankrekening van een Mexicaanse bank.</span><span class="sxs-lookup"><span data-stu-id="d6401-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d6401-364">Alle andere niet-restantrekeningen worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="d6401-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d6401-365">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="d6401-365">Address information</span></span>

<span data-ttu-id="d6401-366">Elke werknemer moet één primaire locatie hebben.</span><span class="sxs-lookup"><span data-stu-id="d6401-366">Every employee must have one primary location.</span></span> <span data-ttu-id="d6401-367">In Dayforce wordt deze locatie gebruikt om de primaire woonplaats van de werknemer te bepalen voor belastingdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="d6401-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d6401-368">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-368">Primary (required)</span></span>
- <span data-ttu-id="d6401-369">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-369">Country/region (required)</span></span>
- <span data-ttu-id="d6401-370">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="d6401-371">Straat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-371">Street (required)</span></span>
- <span data-ttu-id="d6401-372">Huisnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-372">Street Number (required)</span></span>
- <span data-ttu-id="d6401-373">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="d6401-373">Building Complement</span></span>
- <span data-ttu-id="d6401-374">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-374">City (required)</span></span>
- <span data-ttu-id="d6401-375">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-375">State (required)</span></span>
- <span data-ttu-id="d6401-376">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d6401-377">Uw gegevens configureren voor het genereren van salarissen in de Verenigde Staten en Canada</span><span class="sxs-lookup"><span data-stu-id="d6401-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d6401-378">Als u salarissen genereert voor werknemers in de Verenigde Staten en Canada, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="d6401-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d6401-379">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="d6401-379">Departments are required on positions.</span></span>
- <span data-ttu-id="d6401-380">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="d6401-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d6401-381">U kunt Talent zo configureren dat wordt vereist dat met posities een afdeling wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="d6401-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="d6401-382">Hiertoe gaat u naar **Gedeelde Human Resources-posities > Posities > Afdelingen voor posities vereisen**.</span><span class="sxs-lookup"><span data-stu-id="d6401-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d6401-383">Het wordt aanbevolen deze instelling af te dwingen voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d6401-384">Functietypen</span><span class="sxs-lookup"><span data-stu-id="d6401-384">Job types</span></span>

<span data-ttu-id="d6401-385">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="d6401-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d6401-386">Functietypen zijn vereist voor het verwerken van salarissen in de Verenigde Staten en Canada.</span><span class="sxs-lookup"><span data-stu-id="d6401-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d6401-387">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="d6401-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d6401-388">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="d6401-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d6401-389">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d6401-390">Functietype</span><span class="sxs-lookup"><span data-stu-id="d6401-390">Job type</span></span>   | <span data-ttu-id="d6401-391">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d6401-392">Per uur</span><span class="sxs-lookup"><span data-stu-id="d6401-392">Hourly</span></span>     | <span data-ttu-id="d6401-393">Per uur</span><span class="sxs-lookup"><span data-stu-id="d6401-393">Hourly</span></span>      |
| <span data-ttu-id="d6401-394">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d6401-394">Salaried</span></span>   | <span data-ttu-id="d6401-395">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d6401-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d6401-396">Positietypen</span><span class="sxs-lookup"><span data-stu-id="d6401-396">Position types</span></span> 

<span data-ttu-id="d6401-397">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="d6401-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d6401-398">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="d6401-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d6401-399">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d6401-400">Positietype</span><span class="sxs-lookup"><span data-stu-id="d6401-400">Position type</span></span>   | <span data-ttu-id="d6401-401">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d6401-402">Voltijd</span><span class="sxs-lookup"><span data-stu-id="d6401-402">Full-time</span></span>       | <span data-ttu-id="d6401-403">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="d6401-403">Full time employee</span></span> |
| <span data-ttu-id="d6401-404">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="d6401-404">Part-time</span></span>       | <span data-ttu-id="d6401-405">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="d6401-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d6401-406">Redencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-406">Reason codes</span></span>

<span data-ttu-id="d6401-407">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d6401-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d6401-408">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="d6401-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d6401-409">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d6401-410">Redencode</span><span class="sxs-lookup"><span data-stu-id="d6401-410">Reason code</span></span>    | <span data-ttu-id="d6401-411">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-411">Description</span></span>      | <span data-ttu-id="d6401-412">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="d6401-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d6401-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d6401-413">RESIGNATION</span></span>    | <span data-ttu-id="d6401-414">Ontslag</span><span class="sxs-lookup"><span data-stu-id="d6401-414">Resignation</span></span>      | <span data-ttu-id="d6401-415">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-415">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d6401-416">TERMINATION</span></span>    | <span data-ttu-id="d6401-417">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="d6401-417">Termination</span></span>      | <span data-ttu-id="d6401-418">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-418">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d6401-419">RETIREMENT</span></span>     | <span data-ttu-id="d6401-420">Pensionering</span><span class="sxs-lookup"><span data-stu-id="d6401-420">Retirement</span></span>       | <span data-ttu-id="d6401-421">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-421">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-422">OTHER</span><span class="sxs-lookup"><span data-stu-id="d6401-422">OTHER</span></span>          | <span data-ttu-id="d6401-423">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="d6401-423">Other Reasons</span></span>    | <span data-ttu-id="d6401-424">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-424">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="d6401-425">DEATH</span></span>          | <span data-ttu-id="d6401-426">Overlijden</span><span class="sxs-lookup"><span data-stu-id="d6401-426">Death</span></span>            | <span data-ttu-id="d6401-427">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-427">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d6401-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d6401-429">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="d6401-429">Leave of Absence</span></span> | <span data-ttu-id="d6401-430">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-430">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d6401-431">CONTRACTEND</span></span>    | <span data-ttu-id="d6401-432">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="d6401-432">End of Contract</span></span>  | <span data-ttu-id="d6401-433">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-433">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d6401-434">SALARYCHANGE</span></span>   | <span data-ttu-id="d6401-435">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="d6401-435">Change of Salary</span></span> | <span data-ttu-id="d6401-436">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d6401-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d6401-437">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="d6401-437">Marital status</span></span>

<span data-ttu-id="d6401-438">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d6401-439">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d6401-440">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-440">Talent</span></span>                 | <span data-ttu-id="d6401-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d6401-442">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d6401-442">Married</span></span>                | <span data-ttu-id="d6401-443">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d6401-443">Married</span></span>              |
| <span data-ttu-id="d6401-444">Eén</span><span class="sxs-lookup"><span data-stu-id="d6401-444">Single</span></span>                 | <span data-ttu-id="d6401-445">Eén</span><span class="sxs-lookup"><span data-stu-id="d6401-445">Single</span></span>               |
| <span data-ttu-id="d6401-446">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d6401-446">Widowed</span></span>                | <span data-ttu-id="d6401-447">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d6401-447">Widowed</span></span>              |
| <span data-ttu-id="d6401-448">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d6401-448">Divorced</span></span>               | <span data-ttu-id="d6401-449">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d6401-449">Divorced</span></span>             |
| <span data-ttu-id="d6401-450">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="d6401-450">Registered Partnership</span></span> | <span data-ttu-id="d6401-451">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="d6401-451">Domestic Partnership</span></span> |
| <span data-ttu-id="d6401-452">None</span><span class="sxs-lookup"><span data-stu-id="d6401-452">None</span></span>                   | <span data-ttu-id="d6401-453">None</span><span class="sxs-lookup"><span data-stu-id="d6401-453">None</span></span>                 |
| <span data-ttu-id="d6401-454">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="d6401-454">Cohabiting</span></span>             | <span data-ttu-id="d6401-455">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="d6401-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d6401-456">Geslacht</span><span class="sxs-lookup"><span data-stu-id="d6401-456">Gender</span></span>

<span data-ttu-id="d6401-457">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d6401-458">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d6401-459">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-459">Talent</span></span>       | <span data-ttu-id="d6401-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d6401-461">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-461">Male</span></span>         | <span data-ttu-id="d6401-462">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-462">Male</span></span>            |
| <span data-ttu-id="d6401-463">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-463">Female</span></span>       | <span data-ttu-id="d6401-464">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-464">Female</span></span>          |
| <span data-ttu-id="d6401-465">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="d6401-465">Non-specific</span></span> | <span data-ttu-id="d6401-466">*Niet ondersteund*</span><span class="sxs-lookup"><span data-stu-id="d6401-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d6401-467">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-467">Earning codes</span></span>

<span data-ttu-id="d6401-468">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d6401-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d6401-469">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="d6401-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d6401-470">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="d6401-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d6401-471">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="d6401-471">Supported frequencies</span></span>

- <span data-ttu-id="d6401-472">Alles</span><span class="sxs-lookup"><span data-stu-id="d6401-472">All</span></span>
- <span data-ttu-id="d6401-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d6401-473">EVERYPAY</span></span>
- <span data-ttu-id="d6401-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d6401-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d6401-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d6401-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d6401-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d6401-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d6401-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-477">1OFMTH</span></span>
- <span data-ttu-id="d6401-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-478">LASTOFMTH</span></span>
- <span data-ttu-id="d6401-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-479">2OFMTH</span></span>
- <span data-ttu-id="d6401-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-480">3OFMTH</span></span>
- <span data-ttu-id="d6401-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-481">4OFMTH</span></span>
- <span data-ttu-id="d6401-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-482">5OFMTH</span></span>
- <span data-ttu-id="d6401-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-483">1N2OFMTH</span></span>
- <span data-ttu-id="d6401-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-484">3N4OFMTH</span></span>
- <span data-ttu-id="d6401-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-485">1N3OFMTH</span></span>
- <span data-ttu-id="d6401-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-486">1N4OFMTH</span></span>
- <span data-ttu-id="d6401-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-487">2N3OFMTH</span></span>
- <span data-ttu-id="d6401-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-488">2N4OFMTH</span></span>
- <span data-ttu-id="d6401-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="d6401-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="d6401-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="d6401-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="d6401-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d6401-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d6401-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d6401-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d6401-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d6401-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d6401-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d6401-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d6401-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d6401-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d6401-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d6401-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d6401-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d6401-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d6401-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d6401-501">Adressen</span><span class="sxs-lookup"><span data-stu-id="d6401-501">Addresses</span></span>

<span data-ttu-id="d6401-502">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="d6401-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d6401-503">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="d6401-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d6401-504">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-504">Talent</span></span>          | <span data-ttu-id="d6401-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d6401-506">Land/regio</span><span class="sxs-lookup"><span data-stu-id="d6401-506">Country/Region</span></span>  | <span data-ttu-id="d6401-507">Landcode</span><span class="sxs-lookup"><span data-stu-id="d6401-507">Country Code</span></span>          |
| <span data-ttu-id="d6401-508">Postcode</span><span class="sxs-lookup"><span data-stu-id="d6401-508">Zip/Postal Code</span></span> | <span data-ttu-id="d6401-509">Postcode</span><span class="sxs-lookup"><span data-stu-id="d6401-509">Postal Code</span></span>           |
| <span data-ttu-id="d6401-510">Provincie</span><span class="sxs-lookup"><span data-stu-id="d6401-510">State</span></span>           | <span data-ttu-id="d6401-511">Staatcode</span><span class="sxs-lookup"><span data-stu-id="d6401-511">State Code</span></span>            |
| <span data-ttu-id="d6401-512">Plaats</span><span class="sxs-lookup"><span data-stu-id="d6401-512">City</span></span>            | <span data-ttu-id="d6401-513">Plaats</span><span class="sxs-lookup"><span data-stu-id="d6401-513">City</span></span>                  |
| <span data-ttu-id="d6401-514">District</span><span class="sxs-lookup"><span data-stu-id="d6401-514">County</span></span>          | <span data-ttu-id="d6401-515">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="d6401-515">County (Municipality)</span></span> |
| <span data-ttu-id="d6401-516">Adres</span><span class="sxs-lookup"><span data-stu-id="d6401-516">Street</span></span>          | <span data-ttu-id="d6401-517">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="d6401-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d6401-518">Belastingregio's</span><span class="sxs-lookup"><span data-stu-id="d6401-518">Tax regions</span></span>

<span data-ttu-id="d6401-519">Belastingregio's worden gebruikt om de juiste belasting te bepalen die moet worden gebruikt bij het genereren van salarissen.</span><span class="sxs-lookup"><span data-stu-id="d6401-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d6401-520">Belastingregio's worden aan Dayforce toegewezen als locatieadressen.</span><span class="sxs-lookup"><span data-stu-id="d6401-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d6401-521">De standaardbelastingregio moet aan de actieve positie van de werknemer worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d6401-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d6401-522">Belastingregio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-522">Tax region (required)</span></span>
- <span data-ttu-id="d6401-523">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-523">Country/Region (required)</span></span>
- <span data-ttu-id="d6401-524">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-524">State (required)</span></span>
- <span data-ttu-id="d6401-525">District</span><span class="sxs-lookup"><span data-stu-id="d6401-525">County</span></span> 
- <span data-ttu-id="d6401-526">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d6401-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d6401-527">Uw gegevens configureren voor het genereren van salarissen in Mexico</span><span class="sxs-lookup"><span data-stu-id="d6401-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d6401-528">Als u salarissen genereert voor werknemers in Mexico, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="d6401-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d6401-529">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="d6401-529">Departments are required on positions.</span></span>
- <span data-ttu-id="d6401-530">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="d6401-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d6401-531">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="d6401-531">Job types</span></span>

<span data-ttu-id="d6401-532">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="d6401-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d6401-533">Functietypen zijn vereist voor het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="d6401-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d6401-534">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="d6401-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d6401-535">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="d6401-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d6401-536">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d6401-537">Functietype</span><span class="sxs-lookup"><span data-stu-id="d6401-537">Job type</span></span>   | <span data-ttu-id="d6401-538">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d6401-539">Per uur</span><span class="sxs-lookup"><span data-stu-id="d6401-539">Hourly</span></span>     | <span data-ttu-id="d6401-540">MX Per uur</span><span class="sxs-lookup"><span data-stu-id="d6401-540">MX Hourly</span></span>   |
| <span data-ttu-id="d6401-541">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d6401-541">Salaried</span></span>   | <span data-ttu-id="d6401-542">MX Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d6401-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d6401-543">Positietypen</span><span class="sxs-lookup"><span data-stu-id="d6401-543">Position types</span></span> 

<span data-ttu-id="d6401-544">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="d6401-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d6401-545">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="d6401-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d6401-546">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d6401-547">Positietype</span><span class="sxs-lookup"><span data-stu-id="d6401-547">Position type</span></span>   | <span data-ttu-id="d6401-548">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d6401-549">Voltijd</span><span class="sxs-lookup"><span data-stu-id="d6401-549">Full-time</span></span>       | <span data-ttu-id="d6401-550">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="d6401-550">Full time employee</span></span> |
| <span data-ttu-id="d6401-551">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="d6401-551">Part-time</span></span>       | <span data-ttu-id="d6401-552">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="d6401-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d6401-553">Redencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-553">Reason codes</span></span>

<span data-ttu-id="d6401-554">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d6401-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d6401-555">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="d6401-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d6401-556">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d6401-557">Redencode</span><span class="sxs-lookup"><span data-stu-id="d6401-557">Reason code</span></span>            | <span data-ttu-id="d6401-558">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-558">Description</span></span>                    | <span data-ttu-id="d6401-559">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="d6401-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d6401-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d6401-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d6401-561">Vertrek voor eerste salaris</span><span class="sxs-lookup"><span data-stu-id="d6401-561">Departure before first payroll</span></span> | <span data-ttu-id="d6401-562">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-562">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d6401-563">RESIGNATION</span></span>            | <span data-ttu-id="d6401-564">Ontslag</span><span class="sxs-lookup"><span data-stu-id="d6401-564">Resignation</span></span>                    | <span data-ttu-id="d6401-565">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-565">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="d6401-566">PENSION</span></span>                | <span data-ttu-id="d6401-567">Pensioen</span><span class="sxs-lookup"><span data-stu-id="d6401-567">Pension</span></span>                        | <span data-ttu-id="d6401-568">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-568">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d6401-569">TERMINATION</span></span>            | <span data-ttu-id="d6401-570">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="d6401-570">Termination</span></span>                    | <span data-ttu-id="d6401-571">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-571">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d6401-572">RETIREMENT</span></span>             | <span data-ttu-id="d6401-573">Pensionering</span><span class="sxs-lookup"><span data-stu-id="d6401-573">Retirement</span></span>                     | <span data-ttu-id="d6401-574">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-574">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d6401-575">ABSENTEE</span></span>               | <span data-ttu-id="d6401-576">Verzuim</span><span class="sxs-lookup"><span data-stu-id="d6401-576">Absentee</span></span>                       | <span data-ttu-id="d6401-577">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-577">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-578">OTHER</span><span class="sxs-lookup"><span data-stu-id="d6401-578">OTHER</span></span>                  | <span data-ttu-id="d6401-579">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="d6401-579">Other Reasons</span></span>                  | <span data-ttu-id="d6401-580">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-580">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="d6401-581">CLOSURE</span></span>                | <span data-ttu-id="d6401-582">Bedrijfssluiting</span><span class="sxs-lookup"><span data-stu-id="d6401-582">Business Closure</span></span>               | <span data-ttu-id="d6401-583">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-583">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="d6401-584">DEATH</span></span>                  | <span data-ttu-id="d6401-585">Overlijden</span><span class="sxs-lookup"><span data-stu-id="d6401-585">Death</span></span>                          | <span data-ttu-id="d6401-586">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-586">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d6401-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d6401-588">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="d6401-588">Leave of Absence</span></span>               | <span data-ttu-id="d6401-589">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-589">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d6401-590">CONTRACTEND</span></span>            | <span data-ttu-id="d6401-591">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="d6401-591">End of Contract</span></span>                | <span data-ttu-id="d6401-592">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d6401-592">Terminate worker</span></span>     |
| <span data-ttu-id="d6401-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d6401-593">SALARYCHANGE</span></span>           | <span data-ttu-id="d6401-594">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="d6401-594">Change of Salary</span></span>               | <span data-ttu-id="d6401-595">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d6401-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d6401-596">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="d6401-596">Terms of employment</span></span>

<span data-ttu-id="d6401-597">Arbeidsvoorwaarden worden gebruikt om categorieën met arbeidsvoorwaarden te maken.</span><span class="sxs-lookup"><span data-stu-id="d6401-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d6401-598">De voorwaarden worden toegewezen aan Dayforce als indicatorwaarden voor het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="d6401-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d6401-599">De volgende arbeidsvoorwaarden en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d6401-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d6401-600">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="d6401-600">Terms of employment</span></span>   | <span data-ttu-id="d6401-601">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d6401-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d6401-602">Normaal</span><span class="sxs-lookup"><span data-stu-id="d6401-602">Regular</span></span>               | <span data-ttu-id="d6401-603">Normaal</span><span class="sxs-lookup"><span data-stu-id="d6401-603">Regular</span></span>     |
| <span data-ttu-id="d6401-604">Direct</span><span class="sxs-lookup"><span data-stu-id="d6401-604">Direct</span></span>                | <span data-ttu-id="d6401-605">Direct</span><span class="sxs-lookup"><span data-stu-id="d6401-605">Direct</span></span>      |
| <span data-ttu-id="d6401-606">Stage</span><span class="sxs-lookup"><span data-stu-id="d6401-606">Internship</span></span>            | <span data-ttu-id="d6401-607">Stage</span><span class="sxs-lookup"><span data-stu-id="d6401-607">Internship</span></span>  |
| <span data-ttu-id="d6401-608">Permanent</span><span class="sxs-lookup"><span data-stu-id="d6401-608">Permanent</span></span>             | <span data-ttu-id="d6401-609">Permanent</span><span class="sxs-lookup"><span data-stu-id="d6401-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d6401-610">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="d6401-610">Marital status</span></span>

<span data-ttu-id="d6401-611">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d6401-612">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d6401-613">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-613">Talent</span></span>                 | <span data-ttu-id="d6401-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d6401-615">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d6401-615">Married</span></span>                | <span data-ttu-id="d6401-616">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d6401-616">Married</span></span>                   |
| <span data-ttu-id="d6401-617">Eén</span><span class="sxs-lookup"><span data-stu-id="d6401-617">Single</span></span>                 | <span data-ttu-id="d6401-618">Eén</span><span class="sxs-lookup"><span data-stu-id="d6401-618">Single</span></span>                    |
| <span data-ttu-id="d6401-619">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d6401-619">Widowed</span></span>                | <span data-ttu-id="d6401-620">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d6401-620">Widowed</span></span>                   |
| <span data-ttu-id="d6401-621">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d6401-621">Divorced</span></span>               | <span data-ttu-id="d6401-622">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d6401-622">Divorced</span></span>                  |
| <span data-ttu-id="d6401-623">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="d6401-623">Registered Partnership</span></span> | <span data-ttu-id="d6401-624">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="d6401-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="d6401-625">None</span><span class="sxs-lookup"><span data-stu-id="d6401-625">None</span></span>                   | <span data-ttu-id="d6401-626">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d6401-627">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="d6401-627">Cohabiting</span></span>             | <span data-ttu-id="d6401-628">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d6401-629">Geslacht</span><span class="sxs-lookup"><span data-stu-id="d6401-629">Gender</span></span>

<span data-ttu-id="d6401-630">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d6401-631">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d6401-632">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-632">Talent</span></span>       | <span data-ttu-id="d6401-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d6401-634">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-634">Male</span></span>         | <span data-ttu-id="d6401-635">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-635">Male</span></span>                      |
| <span data-ttu-id="d6401-636">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-636">Female</span></span>       | <span data-ttu-id="d6401-637">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d6401-637">Female</span></span>                    |
| <span data-ttu-id="d6401-638">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="d6401-638">Non-specific</span></span> | <span data-ttu-id="d6401-639">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d6401-640">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="d6401-640">Payment method</span></span>

<span data-ttu-id="d6401-641">Betalingsmethoden bieden de werknemer en het bedrijf een manier om te beschrijven hoe werknemers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="d6401-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d6401-642">Betalingsmethoden worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d6401-643">In de volgende tabel wordt aangegeven hoe betalingsmethoden worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d6401-644">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-644">Talent</span></span>             | <span data-ttu-id="d6401-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d6401-646">Contant geld</span><span class="sxs-lookup"><span data-stu-id="d6401-646">Cash</span></span>               | <span data-ttu-id="d6401-647">Contant geld</span><span class="sxs-lookup"><span data-stu-id="d6401-647">Cash</span></span>                      |
| <span data-ttu-id="d6401-648">Elektronische betaling</span><span class="sxs-lookup"><span data-stu-id="d6401-648">Electronic Payment</span></span> | <span data-ttu-id="d6401-649">Overboeking</span><span class="sxs-lookup"><span data-stu-id="d6401-649">Transfer</span></span>                  |
| <span data-ttu-id="d6401-650">Controle</span><span class="sxs-lookup"><span data-stu-id="d6401-650">Check</span></span>              | <span data-ttu-id="d6401-651">Cheque</span><span class="sxs-lookup"><span data-stu-id="d6401-651">Cheque</span></span>                    |
| <span data-ttu-id="d6401-652">Bankcheque</span><span class="sxs-lookup"><span data-stu-id="d6401-652">Bank Draft</span></span>         | <span data-ttu-id="d6401-653">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d6401-654">Overig</span><span class="sxs-lookup"><span data-stu-id="d6401-654">Other</span></span>              | <span data-ttu-id="d6401-655">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d6401-656">Bankrekeningtype</span><span class="sxs-lookup"><span data-stu-id="d6401-656">Bank account type</span></span>

<span data-ttu-id="d6401-657">Bankrekeningtypen worden gebruikt voor elektronische betalingen aan werknemers.</span><span class="sxs-lookup"><span data-stu-id="d6401-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d6401-658">Bankrekeningtypen worden toegewezen aan Dayforce als overdrachtrekeninggegevens.</span><span class="sxs-lookup"><span data-stu-id="d6401-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d6401-659">De bankrekeningtypen worden, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d6401-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d6401-660">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-660">Talent</span></span>            | <span data-ttu-id="d6401-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d6401-662">Betaalrekening</span><span class="sxs-lookup"><span data-stu-id="d6401-662">Checking Account</span></span>  | <span data-ttu-id="d6401-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="d6401-663">CheckingAccount</span></span>           |
| <span data-ttu-id="d6401-664">Salarisrekening</span><span class="sxs-lookup"><span data-stu-id="d6401-664">Payroll Account</span></span>   | <span data-ttu-id="d6401-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="d6401-665">PayrollAccount</span></span>            |
| <span data-ttu-id="d6401-666">Spaarrekening</span><span class="sxs-lookup"><span data-stu-id="d6401-666">Savings Account</span></span>   | <span data-ttu-id="d6401-667">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d6401-668">BankGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="d6401-668">BankGirot account</span></span> | <span data-ttu-id="d6401-669">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d6401-670">PlusGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="d6401-670">PlusGirot account</span></span> | <span data-ttu-id="d6401-671">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d6401-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d6401-672">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d6401-672">Earning codes</span></span>

<span data-ttu-id="d6401-673">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d6401-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d6401-674">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="d6401-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d6401-675">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="d6401-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d6401-676">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="d6401-676">Supported frequencies</span></span>

- <span data-ttu-id="d6401-677">Alles</span><span class="sxs-lookup"><span data-stu-id="d6401-677">All</span></span>
- <span data-ttu-id="d6401-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d6401-678">EVERYPAY</span></span>
- <span data-ttu-id="d6401-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d6401-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d6401-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d6401-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d6401-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d6401-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d6401-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-682">1OFMTH</span></span>
- <span data-ttu-id="d6401-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-683">LASTOFMTH</span></span>
- <span data-ttu-id="d6401-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-684">2OFMTH</span></span>
- <span data-ttu-id="d6401-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-685">3OFMTH</span></span>
- <span data-ttu-id="d6401-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-686">4OFMTH</span></span>
- <span data-ttu-id="d6401-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-687">5OFMTH</span></span>
- <span data-ttu-id="d6401-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-688">1N2OFMTH</span></span>
- <span data-ttu-id="d6401-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-689">3N4OFMTH</span></span>
- <span data-ttu-id="d6401-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-690">1N3OFMTH</span></span>
- <span data-ttu-id="d6401-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-691">1N4OFMTH</span></span>
- <span data-ttu-id="d6401-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-692">2N3OFMTH</span></span>
- <span data-ttu-id="d6401-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-693">2N4OFMTH</span></span>
- <span data-ttu-id="d6401-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="d6401-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="d6401-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="d6401-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="d6401-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d6401-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d6401-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d6401-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d6401-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d6401-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d6401-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d6401-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d6401-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d6401-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d6401-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d6401-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d6401-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d6401-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d6401-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d6401-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d6401-706">Adressen</span><span class="sxs-lookup"><span data-stu-id="d6401-706">Addresses</span></span>

<span data-ttu-id="d6401-707">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="d6401-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d6401-708">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="d6401-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d6401-709">Talent</span><span class="sxs-lookup"><span data-stu-id="d6401-709">Talent</span></span>              | <span data-ttu-id="d6401-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d6401-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d6401-711">Land/regio</span><span class="sxs-lookup"><span data-stu-id="d6401-711">Country/Region</span></span>      | <span data-ttu-id="d6401-712">Landcode</span><span class="sxs-lookup"><span data-stu-id="d6401-712">Country Code</span></span>          |
| <span data-ttu-id="d6401-713">Postcode</span><span class="sxs-lookup"><span data-stu-id="d6401-713">Zip/Postal Code</span></span>     | <span data-ttu-id="d6401-714">Postcode</span><span class="sxs-lookup"><span data-stu-id="d6401-714">Postal Code</span></span>           |
| <span data-ttu-id="d6401-715">Provincie</span><span class="sxs-lookup"><span data-stu-id="d6401-715">State</span></span>               | <span data-ttu-id="d6401-716">Staatcode</span><span class="sxs-lookup"><span data-stu-id="d6401-716">State Code</span></span>            |
| <span data-ttu-id="d6401-717">Plaats</span><span class="sxs-lookup"><span data-stu-id="d6401-717">City</span></span>                | <span data-ttu-id="d6401-718">Plaats</span><span class="sxs-lookup"><span data-stu-id="d6401-718">City</span></span>                  |
| <span data-ttu-id="d6401-719">District</span><span class="sxs-lookup"><span data-stu-id="d6401-719">County</span></span>              | <span data-ttu-id="d6401-720">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="d6401-720">County (Municipality)</span></span> |
| <span data-ttu-id="d6401-721">Adres</span><span class="sxs-lookup"><span data-stu-id="d6401-721">Street</span></span>              | <span data-ttu-id="d6401-722">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="d6401-722">Address Line 1</span></span>        |
| <span data-ttu-id="d6401-723">Huisnummer</span><span class="sxs-lookup"><span data-stu-id="d6401-723">Street Number</span></span>       | <span data-ttu-id="d6401-724">Adresregel 2</span><span class="sxs-lookup"><span data-stu-id="d6401-724">Address Line 2</span></span>        |
| <span data-ttu-id="d6401-725">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="d6401-725">Building Complement</span></span> | <span data-ttu-id="d6401-726">Adresregel 5</span><span class="sxs-lookup"><span data-stu-id="d6401-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d6401-727">Paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d6401-727">Passport number</span></span>

<span data-ttu-id="d6401-728">Werknemers kunnen paspoortgegevens opgeven.</span><span class="sxs-lookup"><span data-stu-id="d6401-728">Employees can declare passport information.</span></span> <span data-ttu-id="d6401-729">Deze informatie is van het identificatietype **Paspoort** en wordt in Dayforce geïntegreerd als onderdeel van de Mexico-specifieke informatie van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d6401-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d6401-730">Identificatietype = 'Paspoort'</span><span class="sxs-lookup"><span data-stu-id="d6401-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d6401-731">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="d6401-731">Issued Date</span></span>
- <span data-ttu-id="d6401-732">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d6401-732">Expiration Date</span></span>

<span data-ttu-id="d6401-733">Werknemers kunnen meerdere identificatienummers van het identificatietype **Paspoort** opgeven.</span><span class="sxs-lookup"><span data-stu-id="d6401-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d6401-734">Echter alleen de huidige actieve paspoortvermelding wordt geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d6401-735">Als alle paspoortvermeldingen zijn verlopen, wordt het paspoort dat als laatste is uitgegeven geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d6401-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
