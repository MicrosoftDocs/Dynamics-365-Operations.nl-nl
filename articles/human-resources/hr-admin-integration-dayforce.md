---
title: Integratie met Dayforce configureren
description: De integratie tussen Microsoft Dynamics 365 Human Resources en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen, die in dit artikel worden beschreven. Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Human Resources als Dayforce.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d5f65672960716bee3f58c98ccce249fdbf8697
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467140"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="921c2-104">Integratie met Dayforce configureren</span><span class="sxs-lookup"><span data-stu-id="921c2-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="921c2-105">De integratie tussen Microsoft Dynamics 365 Human Resources en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen, die in dit artikel worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="921c2-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="921c2-106">Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Human Resources als Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="921c2-107">Als u een service zoals Dayforce gebruikt voor het uitvoeren van betalingen, moet u de integratie inschakelen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="921c2-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="921c2-108">De integratie vereist specifieke gegevens vanuit Human Resources.</span><span class="sxs-lookup"><span data-stu-id="921c2-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="921c2-109">Daarom moet u controleren of gegevens die zijn toegewezen aan Dayforce, zodanig in Human Resources zijn geconfigureerd dat de integratie wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="921c2-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="921c2-110">De integratie maakt gebruik van de volgende brede categorieën gegevens:</span><span class="sxs-lookup"><span data-stu-id="921c2-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="921c2-111">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-111">Human resources data</span></span>
- <span data-ttu-id="921c2-112">Compensatiegegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-112">Compensation data</span></span>
- <span data-ttu-id="921c2-113">Salarisgegevens, zoals betalingscycli, salarisperioden en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="921c2-114">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-114">Worker data</span></span>

<span data-ttu-id="921c2-115">In dit artikel worden de stappen beschreven die u moet volgen om de integratie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="921c2-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="921c2-116">Ook wordt uitgelegd welke typen gegevens en welke configuratiedetails vereist zijn voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="921c2-117">De integratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="921c2-117">Enable the integration</span></span>

<span data-ttu-id="921c2-118">In Human Resources moet u de integratie inschakelen en de configuratiegegevens invoeren om verbinding te maken met Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="921c2-119">Als u wilt dat de grootboektransactie die wordt geproduceerd wordt geïmporteerd in Microsoft Dynamics 365 Finance, moet u ook een Microsoft Azure-opslagaccount instellen en de verbindingstekenreeks voor Azure Storage invoeren in Finance.</span><span class="sxs-lookup"><span data-stu-id="921c2-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="921c2-120">Voer de volgende stappen uit om de integratie in Human Resources in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="921c2-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="921c2-121">Ga naar de pagina **Systeembeheer** en selecteer **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="921c2-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="921c2-122">Voer het beveiligde FTP-eindpunt (File Transfer Protocol) en het pad naar de beveiligde FTP-map in.</span><span class="sxs-lookup"><span data-stu-id="921c2-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="921c2-123">Voer de gebruikersnaam en het wachtwoord in van de gebruiker die toegang krijgt tot het beveiligde FTP-eindpunt en het mappad.</span><span class="sxs-lookup"><span data-stu-id="921c2-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="921c2-124">Test de verbinding, zoals vereist, en stel de optie **Integratie van salarisadministratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="921c2-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="921c2-125">Wanneer de integratie is ingeschakeld, worden het pakket voor gegevensexport en de bestanden gemaakt en wordt de frequentie ingesteld.</span><span class="sxs-lookup"><span data-stu-id="921c2-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="921c2-126">U kunt deze frequentie naar behoefte wijzigen.</span><span class="sxs-lookup"><span data-stu-id="921c2-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="921c2-127">Zie de volgende Azure-artikelen voor meer informatie over Azure Storage-accounts en Azure Storage-verbindingstekenreeksen:</span><span class="sxs-lookup"><span data-stu-id="921c2-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="921c2-128">Informatie over Azure-opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="921c2-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="921c2-129">Verbindingstekenreeks voor Azure Storage configureren</span><span class="sxs-lookup"><span data-stu-id="921c2-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="921c2-130">Technische details wanneer integratie van salarisadministratie is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="921c2-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="921c2-131">Het inschakelen van de integratie van de salarisadministratie heeft twee belangrijke effecten:</span><span class="sxs-lookup"><span data-stu-id="921c2-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="921c2-132">Er wordt een gegevensexportproject met de naam Export van integratie van salarisadministratie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="921c2-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="921c2-133">Dit project bevat de entiteiten en velden die nodig zijn voor de integratie van de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="921c2-134">Als u het project wilt onderzoeken, gaat u naar **Systeembeheer**, selecteert u de tegel **Gegevensbeheer** en opent u het gegevensproject in de lijst met projecten.</span><span class="sxs-lookup"><span data-stu-id="921c2-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="921c2-135">Met deze batchtaak wordt het gegevensexportproject uitgevoerd, wordt het resulterende gegevenspakket gecodeerd en wordt het gegevenspakketbestand overgebracht naar het SFTP-eindpunt dat is geconfigureerd in het scherm **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="921c2-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="921c2-136">Het gegevenspakket dat naar het SFTP-eind punt wordt overgebracht, is gecodeerd met een sleutel die uniek is voor het pakket.</span><span class="sxs-lookup"><span data-stu-id="921c2-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="921c2-137">De sleutel bevindt zich in een Azure-sleutelkluis die alleen toegankelijk is via Ceridian.</span><span class="sxs-lookup"><span data-stu-id="921c2-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="921c2-138">Het is niet mogelijk om de inhoud van het gegevenspakket te decoderen en te onderzoeken.</span><span class="sxs-lookup"><span data-stu-id="921c2-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="921c2-139">Als u de inhoud van het gegevenspakket wilt controleren, moet u het gegevensproject Export van integratie van salarisadministratie handmatig exporteren, downloaden en vervolgens openen.</span><span class="sxs-lookup"><span data-stu-id="921c2-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="921c2-140">Bij een handmatige export wordt er geen codering toegepast of wordt het pakket niet overgedragen.</span><span class="sxs-lookup"><span data-stu-id="921c2-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="921c2-141">Uw gegevens configureren</span><span class="sxs-lookup"><span data-stu-id="921c2-141">Configure your data</span></span> 

<span data-ttu-id="921c2-142">Om salarissen te kunnen verwerken, moet u resourcegegevens configureren in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="921c2-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="921c2-143">U moet gegevens over de organisatie, zoals taken en functies, instellen samen met informatie over vergoedingen en compensatie.</span><span class="sxs-lookup"><span data-stu-id="921c2-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="921c2-144">Deze informatie biedt de informatie over dienstverband, salaris en inhoudingen die vereist is om het salaris van werknemers te genereren.</span><span class="sxs-lookup"><span data-stu-id="921c2-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="921c2-145">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="921c2-146">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="921c2-146">Benefits</span></span> 

<span data-ttu-id="921c2-147">Human resources biedt hulpmiddelen voor het instellen en onderhouden van de vergoedingen, inhoudingen en compensatieplannen van medewerkers die een organisatie zijn medewerkers biedt.</span><span class="sxs-lookup"><span data-stu-id="921c2-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="921c2-148">Wanneer u vergoedingen maakt, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="921c2-149">Vergoedingsplannen</span><span class="sxs-lookup"><span data-stu-id="921c2-149">Benefit plans</span></span>

- <span data-ttu-id="921c2-150">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-150">Plan (required)</span></span>
- <span data-ttu-id="921c2-151">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-151">Type (required)</span></span>
- <span data-ttu-id="921c2-152">Gevolgen voor salaris (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-152">Payroll impact (required)</span></span>
- <span data-ttu-id="921c2-153">Achterstallige betalingen herstellen</span><span class="sxs-lookup"><span data-stu-id="921c2-153">Recover arrears</span></span>
- <span data-ttu-id="921c2-154">Inhoudingsmethode</span><span class="sxs-lookup"><span data-stu-id="921c2-154">Deduction method</span></span>
- <span data-ttu-id="921c2-155">Inhoudingsprioriteit</span><span class="sxs-lookup"><span data-stu-id="921c2-155">Deduction priority</span></span>
- <span data-ttu-id="921c2-156">Limietperiode</span><span class="sxs-lookup"><span data-stu-id="921c2-156">Limit period</span></span>
- <span data-ttu-id="921c2-157">Bedrag beperken</span><span class="sxs-lookup"><span data-stu-id="921c2-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="921c2-158">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="921c2-158">Benefits</span></span>

- <span data-ttu-id="921c2-159">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-159">Plan (required)</span></span>
- <span data-ttu-id="921c2-160">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-160">Type (required)</span></span>
- <span data-ttu-id="921c2-161">Optie (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-161">Option (required)</span></span>
- <span data-ttu-id="921c2-162">Vergoeding-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-162">Benefit ID (required)</span></span>
- <span data-ttu-id="921c2-163">Frequentie</span><span class="sxs-lookup"><span data-stu-id="921c2-163">Frequency</span></span>
- <span data-ttu-id="921c2-164">Basis</span><span class="sxs-lookup"><span data-stu-id="921c2-164">Basis</span></span>
- <span data-ttu-id="921c2-165">Bedrag of tarief</span><span class="sxs-lookup"><span data-stu-id="921c2-165">Amount or rate</span></span>
- <span data-ttu-id="921c2-166">Inkomstencode</span><span class="sxs-lookup"><span data-stu-id="921c2-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="921c2-167">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="921c2-167">Supported frequencies</span></span> 

- <span data-ttu-id="921c2-168">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="921c2-168">Weekly</span></span>
- <span data-ttu-id="921c2-169">Tweewekelijks</span><span class="sxs-lookup"><span data-stu-id="921c2-169">Bi-weekly</span></span>
- <span data-ttu-id="921c2-170">Halfmaandelijks</span><span class="sxs-lookup"><span data-stu-id="921c2-170">Semi-monthly</span></span>
- <span data-ttu-id="921c2-171">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="921c2-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="921c2-172">Ondersteund bases</span><span class="sxs-lookup"><span data-stu-id="921c2-172">Supported bases</span></span> 

- <span data-ttu-id="921c2-173">Vast bedrag</span><span class="sxs-lookup"><span data-stu-id="921c2-173">Fixed amount</span></span>
- <span data-ttu-id="921c2-174">Percentage van inkomsten</span><span class="sxs-lookup"><span data-stu-id="921c2-174">Percent of earnings</span></span>
- <span data-ttu-id="921c2-175">Productieve uren</span><span class="sxs-lookup"><span data-stu-id="921c2-175">Productive hours</span></span>

<span data-ttu-id="921c2-176">Dayforce maakt de volgende inhoudingen, op basis van de salarisgevolgen die zijn gedefinieerd voor het vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="921c2-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="921c2-177">Selectie in Human Resources</span><span class="sxs-lookup"><span data-stu-id="921c2-177">Selection in Human Resources</span></span>        | <span data-ttu-id="921c2-178">Resultaat in Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="921c2-179">Geen</span><span class="sxs-lookup"><span data-stu-id="921c2-179">None</span></span>                       | <span data-ttu-id="921c2-180">Er wordt geen inhouding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="921c2-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="921c2-181">Alleen inhouding</span><span class="sxs-lookup"><span data-stu-id="921c2-181">Deduction only</span></span>             | <span data-ttu-id="921c2-182">Er wordt een inhouding voor de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="921c2-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="921c2-183">Alleen bijdrage</span><span class="sxs-lookup"><span data-stu-id="921c2-183">Contribution only</span></span>          | <span data-ttu-id="921c2-184">Er wordt een inhouding voor de werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="921c2-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="921c2-185">Inhouding en bijdrage</span><span class="sxs-lookup"><span data-stu-id="921c2-185">Deduction and contribution</span></span> | <span data-ttu-id="921c2-186">Er worden inhoudingen voor werknemer en werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="921c2-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="921c2-187">Zie de volgende artikelen voor meer informatie over het definiëren en beheren van een vergoedingsprogramma:</span><span class="sxs-lookup"><span data-stu-id="921c2-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="921c2-188">Een vergoedingenprogramma voor werknemers maken</span><span class="sxs-lookup"><span data-stu-id="921c2-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="921c2-189">Een nieuwe vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="921c2-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="921c2-190">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="921c2-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="921c2-191">Vergoedingen inschrijven en verwijderen van medewerkers</span><span class="sxs-lookup"><span data-stu-id="921c2-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="921c2-192">Compensatie</span><span class="sxs-lookup"><span data-stu-id="921c2-192">Compensation</span></span> 

<span data-ttu-id="921c2-193">Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren.</span><span class="sxs-lookup"><span data-stu-id="921c2-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="921c2-194">Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd.</span><span class="sxs-lookup"><span data-stu-id="921c2-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="921c2-195">De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="921c2-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="921c2-196">Dayforce gebruikt compensatie-informatie voor het berekenen van het uur- of jaartarief van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="921c2-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="921c2-197">Er zijn vastecompensatieplannen en conversies van het loontarief vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="921c2-198">Werknemers moeten worden gekoppeld aan een vastecompensatieplan.</span><span class="sxs-lookup"><span data-stu-id="921c2-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="921c2-199">Zie de volgende artikelen voor meer informatie over compensatieplannen:</span><span class="sxs-lookup"><span data-stu-id="921c2-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="921c2-200">Plannen voor vaste compensatie maken</span><span class="sxs-lookup"><span data-stu-id="921c2-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="921c2-201">Plannen voor variabele compensatie maken</span><span class="sxs-lookup"><span data-stu-id="921c2-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="921c2-202">Salaris-/compensatiestructuur en -plannen ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="921c2-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="921c2-203">Compensatie verwerken</span><span class="sxs-lookup"><span data-stu-id="921c2-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="921c2-204">Compensatieproces definiëren en resultaten berekenen</span><span class="sxs-lookup"><span data-stu-id="921c2-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="921c2-205">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="921c2-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="921c2-206">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="921c2-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="921c2-207">Taken</span><span class="sxs-lookup"><span data-stu-id="921c2-207">Jobs</span></span> 

<span data-ttu-id="921c2-208">Een functie is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een functie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="921c2-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="921c2-209">Zie de volgende artikelen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="921c2-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="921c2-210">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="921c2-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="921c2-211">Nieuwe taken definiëren</span><span class="sxs-lookup"><span data-stu-id="921c2-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="921c2-212">Posities</span><span class="sxs-lookup"><span data-stu-id="921c2-212">Positions</span></span>

<span data-ttu-id="921c2-213">Een positie is een afzonderlijk exemplaar van een taak.</span><span class="sxs-lookup"><span data-stu-id="921c2-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="921c2-214">De positie 'Verkoopmanager (Oost)' is bijvoorbeeld een van de posities die zijn gekoppeld aan de functie 'Verkoopmanager'.</span><span class="sxs-lookup"><span data-stu-id="921c2-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="921c2-215">Een positie bestaat op een afdeling.</span><span class="sxs-lookup"><span data-stu-id="921c2-215">A position exists in a department.</span></span> <span data-ttu-id="921c2-216">Aan elke positie kan slechts één medewerker worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="921c2-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="921c2-217">Let op de volgende gegevens en configuratie bij het instellen van posities:</span><span class="sxs-lookup"><span data-stu-id="921c2-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="921c2-218">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-218">Position (required)</span></span>
- <span data-ttu-id="921c2-219">Beschrijving (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-219">Description (required)</span></span>
- <span data-ttu-id="921c2-220">Functie (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-220">Job (required)</span></span>
- <span data-ttu-id="921c2-221">Afdeling (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-221">Department (required)</span></span>
- <span data-ttu-id="921c2-222">Positietype (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-222">Position type (required)</span></span>
- <span data-ttu-id="921c2-223">Voltijdse equivalent</span><span class="sxs-lookup"><span data-stu-id="921c2-223">Full-time equivalent</span></span>
- <span data-ttu-id="921c2-224">Jaarlijkse normale uren (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="921c2-225">Betaald door rechtspersoon (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="921c2-226">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-226">Pay cycle (required)</span></span>
- <span data-ttu-id="921c2-227">Standaard financiële dimensie: kostenplaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="921c2-228">Medewerkertoewijzing: medewerker, toewijzing begin, einde toewijzing, redencode</span><span class="sxs-lookup"><span data-stu-id="921c2-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="921c2-229">Als meerdere posities op dezelfde afdeling aan dezelfde functie zijn gekoppeld, worden deze geconsolideerd in een enkele positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="921c2-230">Zie de volgende artikelen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="921c2-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="921c2-231">Uw werknemers organiseren met afdelingen, taken en posities</span><span class="sxs-lookup"><span data-stu-id="921c2-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="921c2-232">Posities instellen</span><span class="sxs-lookup"><span data-stu-id="921c2-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="921c2-233">Afdelingen</span><span class="sxs-lookup"><span data-stu-id="921c2-233">Departments</span></span>

<span data-ttu-id="921c2-234">Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt.</span><span class="sxs-lookup"><span data-stu-id="921c2-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="921c2-235">Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR.</span><span class="sxs-lookup"><span data-stu-id="921c2-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="921c2-236">U kunt afdelingen gebruiken om te rapporteren over functiegebieden.</span><span class="sxs-lookup"><span data-stu-id="921c2-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="921c2-237">Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.</span><span class="sxs-lookup"><span data-stu-id="921c2-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="921c2-238">Zie de volgende artikelen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="921c2-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="921c2-239">Een afdeling maken en koppelen aan de afdelingshiërarchie</span><span class="sxs-lookup"><span data-stu-id="921c2-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="921c2-240">Nieuwe afdelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="921c2-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="921c2-241">Betalingscycli en salarisperioden</span><span class="sxs-lookup"><span data-stu-id="921c2-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="921c2-242">Een betalingscyclus bepaalt hoe vaak salarissen worden berekend en op welke specifieke dagen medewerkers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="921c2-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="921c2-243">Zo kan bijvooorbeeld een betalingscyclus maandelijks zijn en kunnen werknemers worden uitbetaald op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="921c2-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="921c2-244">Een betalingscyclus kan ook wekelijks en werknemers kunnen worden uitbetaald op de dinsdag na het einde van de salarisperiode.</span><span class="sxs-lookup"><span data-stu-id="921c2-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="921c2-245">Betalingscycli zijn toegewezen aan posities om te bepalen wanneer medewerkers in deze posities worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="921c2-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="921c2-246">Nadat u betalingscycli hebt gemaakt, kunt u salarisperioden voor elke cyclus genereren.</span><span class="sxs-lookup"><span data-stu-id="921c2-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="921c2-247">Elke salarisperiode bevat een standaard betalingsdatum die is gebaseerd op gegevens die u verstrekt.</span><span class="sxs-lookup"><span data-stu-id="921c2-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="921c2-248">U kunt echter de standaard betalingsdatum in een salarisperiode wijzigen om te voorzien in uitzonderingen, bijvoorbeeld wanneer de betalingsdatum op een feestdag valt.</span><span class="sxs-lookup"><span data-stu-id="921c2-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="921c2-249">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="921c2-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="921c2-250">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-250">Pay cycle (required)</span></span>
- <span data-ttu-id="921c2-251">Frequentie van betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="921c2-252">Begindatum van periode (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="921c2-253">Standaardbetalingsdatum (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="921c2-254">Deze informatie is geïntegreerd met Dayforce als betalingsgroepen en worden gescheiden per land of regio voor elke betalingscyclus.</span><span class="sxs-lookup"><span data-stu-id="921c2-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="921c2-255">Vóór integratie moet ten minste één salarisperiode worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="921c2-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="921c2-256">Dayforce genereert van betalingsgroepkalenders en betalingsdatums, op basis van de begindatum van de eerste salarisperiode en de standaardbetalingsdatum die is ingesteld in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="921c2-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="921c2-257">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-257">Earning codes</span></span>

<span data-ttu-id="921c2-258">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="921c2-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="921c2-259">De codes hebben verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="921c2-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="921c2-260">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="921c2-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="921c2-261">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-261">Earning Code (required)</span></span>
- <span data-ttu-id="921c2-262">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-262">Description</span></span>
- <span data-ttu-id="921c2-263">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="921c2-263">Unit of measure</span></span>
- <span data-ttu-id="921c2-264">Productief</span><span class="sxs-lookup"><span data-stu-id="921c2-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="921c2-265">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-265">Worker data</span></span>

<span data-ttu-id="921c2-266">Records voor de verschillende soorten medewerkers die u hebt zijn belangrijk voor uw HRM- en salarisadministratiesystemen.</span><span class="sxs-lookup"><span data-stu-id="921c2-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="921c2-267">De gegevens die u invoert, kunnen worden gebruikt om medewerkers en persoonlijke gegevens bij te houden.</span><span class="sxs-lookup"><span data-stu-id="921c2-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="921c2-268">U kunt de volgende informatie bijhouden voor medewerkers:</span><span class="sxs-lookup"><span data-stu-id="921c2-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="921c2-269">**Basis** – Basisinformatie over een medewerker bijhouden, zoals contactgegevens, demografische gegevens, identificatiegegevens, informatie over de familie, status van militaire dienst, expat-informatie en contactpersonen voor noodgevallen.</span><span class="sxs-lookup"><span data-stu-id="921c2-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="921c2-270">**Dienstverband** – Informatie bijhouden over werkgelegenheid van een medewerker, zoals een aansluiting met een bedrijf of organisatie, functie, start- en einddatums, arbeidsgeschiktheid, arbeidsvoorwaarden, pensioen, verlof en relocatie-informatie.</span><span class="sxs-lookup"><span data-stu-id="921c2-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="921c2-271">**Verlof en verzuim** – Informatie bijhouden over de afwezigheid van een medewerker, zoals werkkalenders, verzuimtransacties en verzuiminstellingen.</span><span class="sxs-lookup"><span data-stu-id="921c2-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="921c2-272">**Vergoedingen en salarissen** – Informatie bijhouden over compensatieplannen en salarisgegevens van een medewerker zoals inschrijving op plan, onderscheidingen, commissie, fiscale informatie, pensioen en salarisinhoudingen.</span><span class="sxs-lookup"><span data-stu-id="921c2-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="921c2-273">Wanneer u informatie over een werknemer invoert, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="921c2-274">Algemene informatie</span><span class="sxs-lookup"><span data-stu-id="921c2-274">General information</span></span>

- <span data-ttu-id="921c2-275">Personeelsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-275">Personnel number (required)</span></span>
- <span data-ttu-id="921c2-276">Voornaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-276">First name (required)</span></span>
- <span data-ttu-id="921c2-277">Achternaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-277">Last name (required)</span></span>
- <span data-ttu-id="921c2-278">Tweede naam</span><span class="sxs-lookup"><span data-stu-id="921c2-278">Middle name</span></span>
- <span data-ttu-id="921c2-279">Anciënniteitsdatum</span><span class="sxs-lookup"><span data-stu-id="921c2-279">Seniority date</span></span>
- <span data-ttu-id="921c2-280">Bekend als</span><span class="sxs-lookup"><span data-stu-id="921c2-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="921c2-281">Persoonlijke informatie</span><span class="sxs-lookup"><span data-stu-id="921c2-281">Personal information</span></span>

- <span data-ttu-id="921c2-282">Burgerlijke staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-282">Marital status (required)</span></span>
- <span data-ttu-id="921c2-283">Geboortedatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-283">Birth date (required)</span></span>
- <span data-ttu-id="921c2-284">Geslacht (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-284">Gender (required)</span></span>
- <span data-ttu-id="921c2-285">Persoon met handicap</span><span class="sxs-lookup"><span data-stu-id="921c2-285">Person with disabilities</span></span>
- <span data-ttu-id="921c2-286">Land/regio nationaliteit (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="921c2-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="921c2-287">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-287">Address information</span></span>

- <span data-ttu-id="921c2-288">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-288">Primary (required)</span></span>
- <span data-ttu-id="921c2-289">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-289">Country/region (required)</span></span>
- <span data-ttu-id="921c2-290">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-290">Postal code (required)</span></span>
- <span data-ttu-id="921c2-291">Huisnummer (vereist) (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="921c2-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="921c2-292">Gebouwtoevoeging (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="921c2-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="921c2-293">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-293">City (required)</span></span>
- <span data-ttu-id="921c2-294">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-294">State (required)</span></span>
- <span data-ttu-id="921c2-295">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="921c2-296">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="921c2-296">Contact information</span></span> 

- <span data-ttu-id="921c2-297">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-297">Primary (required)</span></span>
- <span data-ttu-id="921c2-298">Contactnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-298">Contact number (required)</span></span>
- <span data-ttu-id="921c2-299">Toestel</span><span class="sxs-lookup"><span data-stu-id="921c2-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="921c2-300">Salarisinformatie en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-300">Payroll information and earning codes</span></span>

<span data-ttu-id="921c2-301">Aan werknemers kunnen bepaalde inkomsten met een bepaalde betalingsfrequentie worden toegewezen en zij kunnen een geprefereerde betalingsmethode hebben.</span><span class="sxs-lookup"><span data-stu-id="921c2-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="921c2-302">De volgende velden worden gebruikt in Dayforce om te garanderen dat deze voorkeuren en instellingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="921c2-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="921c2-303">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-303">Earning codes</span></span>

- <span data-ttu-id="921c2-304">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-304">Position (required)</span></span>
- <span data-ttu-id="921c2-305">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-305">Earning Code (required)</span></span>
- <span data-ttu-id="921c2-306">Frequentie (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-306">Frequency (required)</span></span>
- <span data-ttu-id="921c2-307">Bedrag (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="921c2-308">Salarisinformatie</span><span class="sxs-lookup"><span data-stu-id="921c2-308">Payroll information</span></span>

- <span data-ttu-id="921c2-309">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="921c2-309">Payment Method</span></span>
- <span data-ttu-id="921c2-310">Economische regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-310">Economic Region (required)</span></span>
- <span data-ttu-id="921c2-311">Id personeelsvergoedingen</span><span class="sxs-lookup"><span data-stu-id="921c2-311">Employee Benefits ID</span></span>
- <span data-ttu-id="921c2-312">Nationaal id-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-312">National ID Number (required)</span></span>
- <span data-ttu-id="921c2-313">Nummer militaire dienst</span><span class="sxs-lookup"><span data-stu-id="921c2-313">Military Service Number</span></span>
- <span data-ttu-id="921c2-314">Ploeg-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-314">Shift ID (required)</span></span>
- <span data-ttu-id="921c2-315">Btw-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-315">Tax Number (required)</span></span>
- <span data-ttu-id="921c2-316">Vakbond-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-316">Union ID (required)</span></span>
- <span data-ttu-id="921c2-317">Werkdag-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-317">Work Day ID (required)</span></span>
- <span data-ttu-id="921c2-318">Nummer werkvergunning</span><span class="sxs-lookup"><span data-stu-id="921c2-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="921c2-319">Voor de betalingsmethode ondersteunt Mexico **Contant geld**, **Cheque** (de fysieke cheque van het bedrijf) en **Elektronische betaling**.</span><span class="sxs-lookup"><span data-stu-id="921c2-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="921c2-320">Als geen betalingsmethode is opgegeven, wordt standaard **Cheque** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="921c2-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="921c2-321">Details dienstverband</span><span class="sxs-lookup"><span data-stu-id="921c2-321">Employment details</span></span>

<span data-ttu-id="921c2-322">Historische gegevens over het dienstverband worden gebruikt als belangrijkste informatie voor het opvragen van de statussen voor aanstellen, ontslaan en opnieuw aanstellen van een werknemer in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="921c2-323">Dayforce ondersteunt slechts één actieve dienstverbandrecord tegelijk.</span><span class="sxs-lookup"><span data-stu-id="921c2-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="921c2-324">Begindatum dienstverband (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-324">Employment start date (required)</span></span>
- <span data-ttu-id="921c2-325">Einddatum dienstverband</span><span class="sxs-lookup"><span data-stu-id="921c2-325">Employment end date</span></span>
- <span data-ttu-id="921c2-326">Begindatum</span><span class="sxs-lookup"><span data-stu-id="921c2-326">Start date</span></span>
- <span data-ttu-id="921c2-327">Aangepaste begindatum</span><span class="sxs-lookup"><span data-stu-id="921c2-327">Adjusted start date</span></span>
- <span data-ttu-id="921c2-328">Ontslagdatum (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="921c2-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="921c2-329">Ontslagreden (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="921c2-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="921c2-330">De belangrijkste datums van een werknemer worden afgeleid met behulp van de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="921c2-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="921c2-331">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-331">Human Resources</span></span>                | <span data-ttu-id="921c2-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921c2-333">Meest recente huurdatum</span><span class="sxs-lookup"><span data-stu-id="921c2-333">Most recent hire date</span></span> | <span data-ttu-id="921c2-334">Begindatum van dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="921c2-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="921c2-335">Ontslagdatum</span><span class="sxs-lookup"><span data-stu-id="921c2-335">Termination date</span></span>      | <span data-ttu-id="921c2-336">Ontslagdatum van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="921c2-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="921c2-337">Begindatum</span><span class="sxs-lookup"><span data-stu-id="921c2-337">Start date</span></span>            | <span data-ttu-id="921c2-338">Aangepaste begindatum, begindatum of begindatum dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="921c2-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="921c2-339">Oorspronkelijke datum indiensttreding</span><span class="sxs-lookup"><span data-stu-id="921c2-339">Original hire date</span></span>    | <span data-ttu-id="921c2-340">Begindatum dienstverband van vroegste historierecord van dienstverband</span><span class="sxs-lookup"><span data-stu-id="921c2-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="921c2-341">Compensatie</span><span class="sxs-lookup"><span data-stu-id="921c2-341">Compensation</span></span>

<span data-ttu-id="921c2-342">Een vastecompensatieplan moet worden gekoppeld aan de primaire functie van elke werknemer tijdens de hele duur van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="921c2-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="921c2-343">Deze periode begint op de datum waarop de werknemer in dienst is genomen (of de begindatum van het dienstverband) en gaat door totdat aan het ontslag.</span><span class="sxs-lookup"><span data-stu-id="921c2-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="921c2-344">Ingangsdatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-344">Effective Date (required)</span></span>
- <span data-ttu-id="921c2-345">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="921c2-345">Expiration date</span></span>
- <span data-ttu-id="921c2-346">Loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-346">Pay Rate (required)</span></span>
- <span data-ttu-id="921c2-347">Conversies van loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="921c2-348">Jaarlijks equivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="921c2-349">Uurequivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="921c2-350">Als een werknemer met uurtarief meerdere posities heeft, wordt de vaste compensatie van de primaire positie geïmporteerd in Dayforce als het basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="921c2-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="921c2-351">Voor niet-primaire posities, wordt het uurtarief opgeslagen bij de overeenkomende positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="921c2-352">Als een medewerker met een salaris meerdere posities heeft, worden het cumulatieve uurtarief en het jaarsalaris voor alle actieve posities afgeleid en gebruikt als de basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="921c2-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="921c2-353">Identificatienummers</span><span class="sxs-lookup"><span data-stu-id="921c2-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="921c2-354">Sociaal-fiscaal nummer</span><span class="sxs-lookup"><span data-stu-id="921c2-354">Social Security identifier</span></span> 

<span data-ttu-id="921c2-355">Elke werknemer moet één primaire id hebben.</span><span class="sxs-lookup"><span data-stu-id="921c2-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="921c2-356">Deze id moet van het identificatietype **Sofinummer** zijn.</span><span class="sxs-lookup"><span data-stu-id="921c2-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="921c2-357">In Dayforce, wordt dit automatisch afgeleid als het sociaal-fiscaal nummer van de werknemer dat is vereist voor aanstelling.</span><span class="sxs-lookup"><span data-stu-id="921c2-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="921c2-358">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-358">Primary (required)</span></span>
- <span data-ttu-id="921c2-359">Identificatietype = 'Sofinummer'</span><span class="sxs-lookup"><span data-stu-id="921c2-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="921c2-360">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="921c2-360">Issued Date</span></span>
- <span data-ttu-id="921c2-361">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="921c2-361">Expiration Date</span></span>

<span data-ttu-id="921c2-362">Werknemers kunnen meerdere identificatienummers van het identificatietype **Sofinummer** opgeven.</span><span class="sxs-lookup"><span data-stu-id="921c2-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="921c2-363">Alleen de record die is gemarkeerd als **Primair** wordt echter opgenomen in Dayforce, ongeacht of het nummer actief of verlopen is.</span><span class="sxs-lookup"><span data-stu-id="921c2-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="921c2-364">Bankrekeningen en voorschotten</span><span class="sxs-lookup"><span data-stu-id="921c2-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="921c2-365">Er moet geldige bankrekeninginformatie worden ingevoerd voor elke werknemer die wil worden uitbetaald via bankrekeningoverboekingen.</span><span class="sxs-lookup"><span data-stu-id="921c2-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="921c2-366">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-366">Human Resources</span></span>                         | <span data-ttu-id="921c2-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921c2-368">Bankrekeningnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="921c2-369">SWIFT-code (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-369">SWIFT code (required)</span></span>          | <span data-ttu-id="921c2-370">Veld **Bank-id** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="921c2-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="921c2-371">Vestigingsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="921c2-372">Bankrekeningtype (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-372">Bank account type (required)</span></span>   | <span data-ttu-id="921c2-373">Veld **Rekeningtype** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="921c2-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="921c2-374">Ondersteunde waarden zijn **Rekening-courant** en **Salaris**.</span><span class="sxs-lookup"><span data-stu-id="921c2-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="921c2-375">Werknemers die ervoor kiezen om te worden uitbetaald via bankrekeningoverboekingen moeten een koppeling opgeven naar een restantrekening die zich onder een rechtspersoon bevindt met het primaire adres in Mexico en die is gekoppeld aan een geldige bankrekening van een Mexicaanse bank.</span><span class="sxs-lookup"><span data-stu-id="921c2-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="921c2-376">Alle andere niet-restantrekeningen worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="921c2-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="921c2-377">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="921c2-377">Address information</span></span>

<span data-ttu-id="921c2-378">Elke werknemer moet één primaire locatie hebben.</span><span class="sxs-lookup"><span data-stu-id="921c2-378">Every employee must have one primary location.</span></span> <span data-ttu-id="921c2-379">In Dayforce wordt deze locatie gebruikt om de primaire woonplaats van de werknemer te bepalen voor belastingdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="921c2-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="921c2-380">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-380">Primary (required)</span></span>
- <span data-ttu-id="921c2-381">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-381">Country/region (required)</span></span>
- <span data-ttu-id="921c2-382">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="921c2-383">Straat (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-383">Street (required)</span></span>
- <span data-ttu-id="921c2-384">Huisnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-384">Street Number (required)</span></span>
- <span data-ttu-id="921c2-385">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="921c2-385">Building Complement</span></span>
- <span data-ttu-id="921c2-386">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-386">City (required)</span></span>
- <span data-ttu-id="921c2-387">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-387">State (required)</span></span>
- <span data-ttu-id="921c2-388">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="921c2-389">Uw gegevens configureren voor het genereren van salarissen in de Verenigde Staten en Canada</span><span class="sxs-lookup"><span data-stu-id="921c2-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="921c2-390">Als u salarissen genereert voor werknemers in de Verenigde Staten en Canada, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="921c2-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="921c2-391">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="921c2-391">Departments are required on positions.</span></span>
- <span data-ttu-id="921c2-392">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="921c2-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="921c2-393">U kunt Human Resources zo configureren dat wordt vereist dat met posities een afdeling wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="921c2-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="921c2-394">Hiertoe gaat u naar **Gedeelde Human Resources-posities > Posities > Afdelingen voor posities vereisen**.</span><span class="sxs-lookup"><span data-stu-id="921c2-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="921c2-395">Het wordt aanbevolen deze instelling af te dwingen voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="921c2-396">Functietypen</span><span class="sxs-lookup"><span data-stu-id="921c2-396">Job types</span></span>

<span data-ttu-id="921c2-397">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="921c2-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="921c2-398">Functietypen zijn vereist voor het verwerken van salarissen in de Verenigde Staten en Canada.</span><span class="sxs-lookup"><span data-stu-id="921c2-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="921c2-399">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="921c2-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="921c2-400">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="921c2-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="921c2-401">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="921c2-402">Functietype</span><span class="sxs-lookup"><span data-stu-id="921c2-402">Job type</span></span>   | <span data-ttu-id="921c2-403">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="921c2-404">Per uur</span><span class="sxs-lookup"><span data-stu-id="921c2-404">Hourly</span></span>     | <span data-ttu-id="921c2-405">Per uur</span><span class="sxs-lookup"><span data-stu-id="921c2-405">Hourly</span></span>      |
| <span data-ttu-id="921c2-406">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="921c2-406">Salaried</span></span>   | <span data-ttu-id="921c2-407">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="921c2-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="921c2-408">Positietypen</span><span class="sxs-lookup"><span data-stu-id="921c2-408">Position types</span></span> 

<span data-ttu-id="921c2-409">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="921c2-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="921c2-410">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="921c2-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="921c2-411">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="921c2-412">Positietype</span><span class="sxs-lookup"><span data-stu-id="921c2-412">Position type</span></span>   | <span data-ttu-id="921c2-413">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="921c2-414">Voltijd</span><span class="sxs-lookup"><span data-stu-id="921c2-414">Full-time</span></span>       | <span data-ttu-id="921c2-415">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="921c2-415">Full time employee</span></span> |
| <span data-ttu-id="921c2-416">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="921c2-416">Part-time</span></span>       | <span data-ttu-id="921c2-417">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="921c2-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="921c2-418">Redencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-418">Reason codes</span></span>

<span data-ttu-id="921c2-419">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="921c2-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="921c2-420">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="921c2-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="921c2-421">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="921c2-422">Redencode</span><span class="sxs-lookup"><span data-stu-id="921c2-422">Reason code</span></span>    | <span data-ttu-id="921c2-423">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-423">Description</span></span>      | <span data-ttu-id="921c2-424">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="921c2-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="921c2-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="921c2-425">RESIGNATION</span></span>    | <span data-ttu-id="921c2-426">Ontslag</span><span class="sxs-lookup"><span data-stu-id="921c2-426">Resignation</span></span>      | <span data-ttu-id="921c2-427">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-427">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="921c2-428">TERMINATION</span></span>    | <span data-ttu-id="921c2-429">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="921c2-429">Termination</span></span>      | <span data-ttu-id="921c2-430">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-430">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="921c2-431">RETIREMENT</span></span>     | <span data-ttu-id="921c2-432">Pensionering</span><span class="sxs-lookup"><span data-stu-id="921c2-432">Retirement</span></span>       | <span data-ttu-id="921c2-433">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-433">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-434">OTHER</span><span class="sxs-lookup"><span data-stu-id="921c2-434">OTHER</span></span>          | <span data-ttu-id="921c2-435">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="921c2-435">Other Reasons</span></span>    | <span data-ttu-id="921c2-436">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-436">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="921c2-437">DEATH</span></span>          | <span data-ttu-id="921c2-438">Overlijden</span><span class="sxs-lookup"><span data-stu-id="921c2-438">Death</span></span>            | <span data-ttu-id="921c2-439">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-439">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="921c2-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="921c2-441">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="921c2-441">Leave of Absence</span></span> | <span data-ttu-id="921c2-442">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-442">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="921c2-443">CONTRACTEND</span></span>    | <span data-ttu-id="921c2-444">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="921c2-444">End of Contract</span></span>  | <span data-ttu-id="921c2-445">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-445">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="921c2-446">SALARYCHANGE</span></span>   | <span data-ttu-id="921c2-447">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="921c2-447">Change of Salary</span></span> | <span data-ttu-id="921c2-448">Compensatie</span><span class="sxs-lookup"><span data-stu-id="921c2-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="921c2-449">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="921c2-449">Marital status</span></span>

<span data-ttu-id="921c2-450">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="921c2-451">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="921c2-452">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-452">Human Resources</span></span>                 | <span data-ttu-id="921c2-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="921c2-454">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="921c2-454">Married</span></span>                | <span data-ttu-id="921c2-455">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="921c2-455">Married</span></span>              |
| <span data-ttu-id="921c2-456">Eén</span><span class="sxs-lookup"><span data-stu-id="921c2-456">Single</span></span>                 | <span data-ttu-id="921c2-457">Eén</span><span class="sxs-lookup"><span data-stu-id="921c2-457">Single</span></span>               |
| <span data-ttu-id="921c2-458">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="921c2-458">Widowed</span></span>                | <span data-ttu-id="921c2-459">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="921c2-459">Widowed</span></span>              |
| <span data-ttu-id="921c2-460">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="921c2-460">Divorced</span></span>               | <span data-ttu-id="921c2-461">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="921c2-461">Divorced</span></span>             |
| <span data-ttu-id="921c2-462">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="921c2-462">Registered Partnership</span></span> | <span data-ttu-id="921c2-463">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="921c2-463">Domestic Partnership</span></span> |
| <span data-ttu-id="921c2-464">None</span><span class="sxs-lookup"><span data-stu-id="921c2-464">None</span></span>                   | <span data-ttu-id="921c2-465">None</span><span class="sxs-lookup"><span data-stu-id="921c2-465">None</span></span>                 |
| <span data-ttu-id="921c2-466">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="921c2-466">Cohabiting</span></span>             | <span data-ttu-id="921c2-467">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="921c2-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="921c2-468">Geslacht</span><span class="sxs-lookup"><span data-stu-id="921c2-468">Gender</span></span>

<span data-ttu-id="921c2-469">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="921c2-470">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="921c2-471">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-471">Human Resources</span></span>       | <span data-ttu-id="921c2-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="921c2-473">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-473">Male</span></span>         | <span data-ttu-id="921c2-474">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-474">Male</span></span>            |
| <span data-ttu-id="921c2-475">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-475">Female</span></span>       | <span data-ttu-id="921c2-476">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-476">Female</span></span>          |
| <span data-ttu-id="921c2-477">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="921c2-477">Non-specific</span></span> | <span data-ttu-id="921c2-478">*Niet ondersteund*</span><span class="sxs-lookup"><span data-stu-id="921c2-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="921c2-479">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-479">Earning codes</span></span>

<span data-ttu-id="921c2-480">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="921c2-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="921c2-481">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="921c2-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="921c2-482">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="921c2-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="921c2-483">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="921c2-483">Supported frequencies</span></span>

- <span data-ttu-id="921c2-484">Alles</span><span class="sxs-lookup"><span data-stu-id="921c2-484">All</span></span>
- <span data-ttu-id="921c2-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="921c2-485">EVERYPAY</span></span>
- <span data-ttu-id="921c2-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="921c2-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="921c2-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="921c2-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="921c2-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="921c2-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="921c2-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-489">1OFMTH</span></span>
- <span data-ttu-id="921c2-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-490">LASTOFMTH</span></span>
- <span data-ttu-id="921c2-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-491">2OFMTH</span></span>
- <span data-ttu-id="921c2-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-492">3OFMTH</span></span>
- <span data-ttu-id="921c2-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-493">4OFMTH</span></span>
- <span data-ttu-id="921c2-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-494">5OFMTH</span></span>
- <span data-ttu-id="921c2-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-495">1N2OFMTH</span></span>
- <span data-ttu-id="921c2-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-496">3N4OFMTH</span></span>
- <span data-ttu-id="921c2-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-497">1N3OFMTH</span></span>
- <span data-ttu-id="921c2-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-498">1N4OFMTH</span></span>
- <span data-ttu-id="921c2-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-499">2N3OFMTH</span></span>
- <span data-ttu-id="921c2-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-500">2N4OFMTH</span></span>
- <span data-ttu-id="921c2-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="921c2-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="921c2-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="921c2-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="921c2-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="921c2-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="921c2-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="921c2-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="921c2-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="921c2-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="921c2-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="921c2-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="921c2-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="921c2-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="921c2-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="921c2-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="921c2-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="921c2-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="921c2-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="921c2-513">Adressen</span><span class="sxs-lookup"><span data-stu-id="921c2-513">Addresses</span></span>

<span data-ttu-id="921c2-514">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="921c2-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="921c2-515">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="921c2-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="921c2-516">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-516">Human Resources</span></span>          | <span data-ttu-id="921c2-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="921c2-518">Land/regio</span><span class="sxs-lookup"><span data-stu-id="921c2-518">Country/Region</span></span>  | <span data-ttu-id="921c2-519">Landcode</span><span class="sxs-lookup"><span data-stu-id="921c2-519">Country Code</span></span>          |
| <span data-ttu-id="921c2-520">Postcode</span><span class="sxs-lookup"><span data-stu-id="921c2-520">Zip/Postal Code</span></span> | <span data-ttu-id="921c2-521">Postcode</span><span class="sxs-lookup"><span data-stu-id="921c2-521">Postal Code</span></span>           |
| <span data-ttu-id="921c2-522">Provincie</span><span class="sxs-lookup"><span data-stu-id="921c2-522">State</span></span>           | <span data-ttu-id="921c2-523">Staatcode</span><span class="sxs-lookup"><span data-stu-id="921c2-523">State Code</span></span>            |
| <span data-ttu-id="921c2-524">Plaats</span><span class="sxs-lookup"><span data-stu-id="921c2-524">City</span></span>            | <span data-ttu-id="921c2-525">Plaats</span><span class="sxs-lookup"><span data-stu-id="921c2-525">City</span></span>                  |
| <span data-ttu-id="921c2-526">District</span><span class="sxs-lookup"><span data-stu-id="921c2-526">County</span></span>          | <span data-ttu-id="921c2-527">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="921c2-527">County (Municipality)</span></span> |
| <span data-ttu-id="921c2-528">Adres</span><span class="sxs-lookup"><span data-stu-id="921c2-528">Street</span></span>          | <span data-ttu-id="921c2-529">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="921c2-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="921c2-530">Belastingregio's</span><span class="sxs-lookup"><span data-stu-id="921c2-530">Tax regions</span></span>

<span data-ttu-id="921c2-531">Belastingregio's worden gebruikt om de juiste belasting te bepalen die moet worden gebruikt bij het genereren van salarissen.</span><span class="sxs-lookup"><span data-stu-id="921c2-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="921c2-532">Belastingregio's worden aan Dayforce toegewezen als locatieadressen.</span><span class="sxs-lookup"><span data-stu-id="921c2-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="921c2-533">De standaardbelastingregio moet aan de actieve positie van de werknemer worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="921c2-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="921c2-534">Belastingregio (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-534">Tax region (required)</span></span>
- <span data-ttu-id="921c2-535">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-535">Country/Region (required)</span></span>
- <span data-ttu-id="921c2-536">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-536">State (required)</span></span>
- <span data-ttu-id="921c2-537">District</span><span class="sxs-lookup"><span data-stu-id="921c2-537">County</span></span> 
- <span data-ttu-id="921c2-538">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="921c2-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="921c2-539">Uw gegevens configureren voor het genereren van salarissen in Mexico</span><span class="sxs-lookup"><span data-stu-id="921c2-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="921c2-540">Als u salarissen genereert voor werknemers in Mexico, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="921c2-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="921c2-541">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="921c2-541">Departments are required on positions.</span></span>
- <span data-ttu-id="921c2-542">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="921c2-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="921c2-543">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="921c2-543">Job types</span></span>

<span data-ttu-id="921c2-544">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="921c2-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="921c2-545">Functietypen zijn vereist voor het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="921c2-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="921c2-546">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="921c2-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="921c2-547">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="921c2-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="921c2-548">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="921c2-549">Functietype</span><span class="sxs-lookup"><span data-stu-id="921c2-549">Job type</span></span>   | <span data-ttu-id="921c2-550">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="921c2-551">Per uur</span><span class="sxs-lookup"><span data-stu-id="921c2-551">Hourly</span></span>     | <span data-ttu-id="921c2-552">MX Per uur</span><span class="sxs-lookup"><span data-stu-id="921c2-552">MX Hourly</span></span>   |
| <span data-ttu-id="921c2-553">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="921c2-553">Salaried</span></span>   | <span data-ttu-id="921c2-554">MX Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="921c2-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="921c2-555">Positietypen</span><span class="sxs-lookup"><span data-stu-id="921c2-555">Position types</span></span> 

<span data-ttu-id="921c2-556">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="921c2-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="921c2-557">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="921c2-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="921c2-558">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="921c2-559">Positietype</span><span class="sxs-lookup"><span data-stu-id="921c2-559">Position type</span></span>   | <span data-ttu-id="921c2-560">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="921c2-561">Voltijd</span><span class="sxs-lookup"><span data-stu-id="921c2-561">Full-time</span></span>       | <span data-ttu-id="921c2-562">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="921c2-562">Full time employee</span></span> |
| <span data-ttu-id="921c2-563">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="921c2-563">Part-time</span></span>       | <span data-ttu-id="921c2-564">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="921c2-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="921c2-565">Redencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-565">Reason codes</span></span>

<span data-ttu-id="921c2-566">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="921c2-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="921c2-567">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="921c2-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="921c2-568">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="921c2-569">Redencode</span><span class="sxs-lookup"><span data-stu-id="921c2-569">Reason code</span></span>            | <span data-ttu-id="921c2-570">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-570">Description</span></span>                    | <span data-ttu-id="921c2-571">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="921c2-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="921c2-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="921c2-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="921c2-573">Vertrek voor eerste salaris</span><span class="sxs-lookup"><span data-stu-id="921c2-573">Departure before first payroll</span></span> | <span data-ttu-id="921c2-574">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-574">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="921c2-575">RESIGNATION</span></span>            | <span data-ttu-id="921c2-576">Ontslag</span><span class="sxs-lookup"><span data-stu-id="921c2-576">Resignation</span></span>                    | <span data-ttu-id="921c2-577">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-577">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="921c2-578">PENSION</span></span>                | <span data-ttu-id="921c2-579">Pensioen</span><span class="sxs-lookup"><span data-stu-id="921c2-579">Pension</span></span>                        | <span data-ttu-id="921c2-580">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-580">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="921c2-581">TERMINATION</span></span>            | <span data-ttu-id="921c2-582">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="921c2-582">Termination</span></span>                    | <span data-ttu-id="921c2-583">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-583">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="921c2-584">RETIREMENT</span></span>             | <span data-ttu-id="921c2-585">Pensionering</span><span class="sxs-lookup"><span data-stu-id="921c2-585">Retirement</span></span>                     | <span data-ttu-id="921c2-586">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-586">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="921c2-587">ABSENTEE</span></span>               | <span data-ttu-id="921c2-588">Verzuim</span><span class="sxs-lookup"><span data-stu-id="921c2-588">Absentee</span></span>                       | <span data-ttu-id="921c2-589">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-589">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-590">OTHER</span><span class="sxs-lookup"><span data-stu-id="921c2-590">OTHER</span></span>                  | <span data-ttu-id="921c2-591">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="921c2-591">Other Reasons</span></span>                  | <span data-ttu-id="921c2-592">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-592">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="921c2-593">CLOSURE</span></span>                | <span data-ttu-id="921c2-594">Bedrijfssluiting</span><span class="sxs-lookup"><span data-stu-id="921c2-594">Business Closure</span></span>               | <span data-ttu-id="921c2-595">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-595">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="921c2-596">DEATH</span></span>                  | <span data-ttu-id="921c2-597">Overlijden</span><span class="sxs-lookup"><span data-stu-id="921c2-597">Death</span></span>                          | <span data-ttu-id="921c2-598">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-598">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="921c2-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="921c2-600">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="921c2-600">Leave of Absence</span></span>               | <span data-ttu-id="921c2-601">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-601">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="921c2-602">CONTRACTEND</span></span>            | <span data-ttu-id="921c2-603">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="921c2-603">End of Contract</span></span>                | <span data-ttu-id="921c2-604">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="921c2-604">Terminate worker</span></span>     |
| <span data-ttu-id="921c2-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="921c2-605">SALARYCHANGE</span></span>           | <span data-ttu-id="921c2-606">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="921c2-606">Change of Salary</span></span>               | <span data-ttu-id="921c2-607">Compensatie</span><span class="sxs-lookup"><span data-stu-id="921c2-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="921c2-608">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="921c2-608">Terms of employment</span></span>

<span data-ttu-id="921c2-609">Arbeidsvoorwaarden worden gebruikt om categorieën met arbeidsvoorwaarden te maken.</span><span class="sxs-lookup"><span data-stu-id="921c2-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="921c2-610">De voorwaarden worden toegewezen aan Dayforce als indicatorwaarden voor het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="921c2-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="921c2-611">De volgende arbeidsvoorwaarden en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="921c2-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="921c2-612">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="921c2-612">Terms of employment</span></span>   | <span data-ttu-id="921c2-613">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="921c2-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="921c2-614">Normaal</span><span class="sxs-lookup"><span data-stu-id="921c2-614">Regular</span></span>               | <span data-ttu-id="921c2-615">Normaal</span><span class="sxs-lookup"><span data-stu-id="921c2-615">Regular</span></span>     |
| <span data-ttu-id="921c2-616">Direct</span><span class="sxs-lookup"><span data-stu-id="921c2-616">Direct</span></span>                | <span data-ttu-id="921c2-617">Direct</span><span class="sxs-lookup"><span data-stu-id="921c2-617">Direct</span></span>      |
| <span data-ttu-id="921c2-618">Stage</span><span class="sxs-lookup"><span data-stu-id="921c2-618">Internship</span></span>            | <span data-ttu-id="921c2-619">Stage</span><span class="sxs-lookup"><span data-stu-id="921c2-619">Internship</span></span>  |
| <span data-ttu-id="921c2-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="921c2-620">Permanent</span></span>             | <span data-ttu-id="921c2-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="921c2-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="921c2-622">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="921c2-622">Marital status</span></span>

<span data-ttu-id="921c2-623">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="921c2-624">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="921c2-625">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-625">Human Resources</span></span>                 | <span data-ttu-id="921c2-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="921c2-627">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="921c2-627">Married</span></span>                | <span data-ttu-id="921c2-628">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="921c2-628">Married</span></span>                   |
| <span data-ttu-id="921c2-629">Eén</span><span class="sxs-lookup"><span data-stu-id="921c2-629">Single</span></span>                 | <span data-ttu-id="921c2-630">Eén</span><span class="sxs-lookup"><span data-stu-id="921c2-630">Single</span></span>                    |
| <span data-ttu-id="921c2-631">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="921c2-631">Widowed</span></span>                | <span data-ttu-id="921c2-632">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="921c2-632">Widowed</span></span>                   |
| <span data-ttu-id="921c2-633">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="921c2-633">Divorced</span></span>               | <span data-ttu-id="921c2-634">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="921c2-634">Divorced</span></span>                  |
| <span data-ttu-id="921c2-635">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="921c2-635">Registered Partnership</span></span> | <span data-ttu-id="921c2-636">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="921c2-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="921c2-637">None</span><span class="sxs-lookup"><span data-stu-id="921c2-637">None</span></span>                   | <span data-ttu-id="921c2-638">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="921c2-639">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="921c2-639">Cohabiting</span></span>             | <span data-ttu-id="921c2-640">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="921c2-641">Geslacht</span><span class="sxs-lookup"><span data-stu-id="921c2-641">Gender</span></span>

<span data-ttu-id="921c2-642">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="921c2-643">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="921c2-644">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-644">Human Resources</span></span>       | <span data-ttu-id="921c2-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="921c2-646">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-646">Male</span></span>         | <span data-ttu-id="921c2-647">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-647">Male</span></span>                      |
| <span data-ttu-id="921c2-648">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-648">Female</span></span>       | <span data-ttu-id="921c2-649">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="921c2-649">Female</span></span>                    |
| <span data-ttu-id="921c2-650">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="921c2-650">Non-specific</span></span> | <span data-ttu-id="921c2-651">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="921c2-652">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="921c2-652">Payment method</span></span>

<span data-ttu-id="921c2-653">Betalingsmethoden bieden de werknemer en het bedrijf een manier om te beschrijven hoe werknemers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="921c2-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="921c2-654">Betalingsmethoden worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="921c2-655">In de volgende tabel wordt aangegeven hoe betalingsmethoden worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="921c2-656">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-656">Human Resources</span></span>             | <span data-ttu-id="921c2-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="921c2-658">Contant geld</span><span class="sxs-lookup"><span data-stu-id="921c2-658">Cash</span></span>               | <span data-ttu-id="921c2-659">Contant geld</span><span class="sxs-lookup"><span data-stu-id="921c2-659">Cash</span></span>                      |
| <span data-ttu-id="921c2-660">Elektronische betaling</span><span class="sxs-lookup"><span data-stu-id="921c2-660">Electronic Payment</span></span> | <span data-ttu-id="921c2-661">Overboeking</span><span class="sxs-lookup"><span data-stu-id="921c2-661">Transfer</span></span>                  |
| <span data-ttu-id="921c2-662">Controleren</span><span class="sxs-lookup"><span data-stu-id="921c2-662">Check</span></span>              | <span data-ttu-id="921c2-663">Cheque</span><span class="sxs-lookup"><span data-stu-id="921c2-663">Cheque</span></span>                    |
| <span data-ttu-id="921c2-664">Bankcheque</span><span class="sxs-lookup"><span data-stu-id="921c2-664">Bank Draft</span></span>         | <span data-ttu-id="921c2-665">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="921c2-666">Overig</span><span class="sxs-lookup"><span data-stu-id="921c2-666">Other</span></span>              | <span data-ttu-id="921c2-667">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="921c2-668">Bankrekeningtype</span><span class="sxs-lookup"><span data-stu-id="921c2-668">Bank account type</span></span>

<span data-ttu-id="921c2-669">Bankrekeningtypen worden gebruikt voor elektronische betalingen aan werknemers.</span><span class="sxs-lookup"><span data-stu-id="921c2-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="921c2-670">Bankrekeningtypen worden toegewezen aan Dayforce als overdrachtrekeninggegevens.</span><span class="sxs-lookup"><span data-stu-id="921c2-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="921c2-671">De bankrekeningtypen worden, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="921c2-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="921c2-672">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-672">Human Resources</span></span>            | <span data-ttu-id="921c2-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="921c2-674">Betaalrekening</span><span class="sxs-lookup"><span data-stu-id="921c2-674">Checking Account</span></span>  | <span data-ttu-id="921c2-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="921c2-675">CheckingAccount</span></span>           |
| <span data-ttu-id="921c2-676">Salarisrekening</span><span class="sxs-lookup"><span data-stu-id="921c2-676">Payroll Account</span></span>   | <span data-ttu-id="921c2-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="921c2-677">PayrollAccount</span></span>            |
| <span data-ttu-id="921c2-678">Spaarrekening</span><span class="sxs-lookup"><span data-stu-id="921c2-678">Savings Account</span></span>   | <span data-ttu-id="921c2-679">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="921c2-680">BankGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="921c2-680">BankGirot account</span></span> | <span data-ttu-id="921c2-681">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="921c2-682">PlusGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="921c2-682">PlusGirot account</span></span> | <span data-ttu-id="921c2-683">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="921c2-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="921c2-684">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="921c2-684">Earning codes</span></span>

<span data-ttu-id="921c2-685">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="921c2-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="921c2-686">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="921c2-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="921c2-687">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="921c2-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="921c2-688">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="921c2-688">Supported frequencies</span></span>

- <span data-ttu-id="921c2-689">Alles</span><span class="sxs-lookup"><span data-stu-id="921c2-689">All</span></span>
- <span data-ttu-id="921c2-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="921c2-690">EVERYPAY</span></span>
- <span data-ttu-id="921c2-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="921c2-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="921c2-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="921c2-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="921c2-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="921c2-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="921c2-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-694">1OFMTH</span></span>
- <span data-ttu-id="921c2-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-695">LASTOFMTH</span></span>
- <span data-ttu-id="921c2-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-696">2OFMTH</span></span>
- <span data-ttu-id="921c2-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-697">3OFMTH</span></span>
- <span data-ttu-id="921c2-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-698">4OFMTH</span></span>
- <span data-ttu-id="921c2-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-699">5OFMTH</span></span>
- <span data-ttu-id="921c2-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-700">1N2OFMTH</span></span>
- <span data-ttu-id="921c2-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-701">3N4OFMTH</span></span>
- <span data-ttu-id="921c2-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-702">1N3OFMTH</span></span>
- <span data-ttu-id="921c2-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-703">1N4OFMTH</span></span>
- <span data-ttu-id="921c2-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-704">2N3OFMTH</span></span>
- <span data-ttu-id="921c2-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-705">2N4OFMTH</span></span>
- <span data-ttu-id="921c2-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="921c2-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="921c2-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="921c2-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="921c2-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="921c2-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="921c2-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="921c2-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="921c2-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="921c2-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="921c2-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="921c2-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="921c2-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="921c2-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="921c2-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="921c2-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="921c2-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="921c2-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="921c2-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="921c2-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="921c2-718">Adressen</span><span class="sxs-lookup"><span data-stu-id="921c2-718">Addresses</span></span>

<span data-ttu-id="921c2-719">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="921c2-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="921c2-720">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="921c2-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="921c2-721">Human resources</span><span class="sxs-lookup"><span data-stu-id="921c2-721">Human Resources</span></span>              | <span data-ttu-id="921c2-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="921c2-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="921c2-723">Land/regio</span><span class="sxs-lookup"><span data-stu-id="921c2-723">Country/Region</span></span>      | <span data-ttu-id="921c2-724">Landcode</span><span class="sxs-lookup"><span data-stu-id="921c2-724">Country Code</span></span>          |
| <span data-ttu-id="921c2-725">Postcode</span><span class="sxs-lookup"><span data-stu-id="921c2-725">Zip/Postal Code</span></span>     | <span data-ttu-id="921c2-726">Postcode</span><span class="sxs-lookup"><span data-stu-id="921c2-726">Postal Code</span></span>           |
| <span data-ttu-id="921c2-727">Provincie</span><span class="sxs-lookup"><span data-stu-id="921c2-727">State</span></span>               | <span data-ttu-id="921c2-728">Staatcode</span><span class="sxs-lookup"><span data-stu-id="921c2-728">State Code</span></span>            |
| <span data-ttu-id="921c2-729">Plaats</span><span class="sxs-lookup"><span data-stu-id="921c2-729">City</span></span>                | <span data-ttu-id="921c2-730">Plaats</span><span class="sxs-lookup"><span data-stu-id="921c2-730">City</span></span>                  |
| <span data-ttu-id="921c2-731">District</span><span class="sxs-lookup"><span data-stu-id="921c2-731">County</span></span>              | <span data-ttu-id="921c2-732">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="921c2-732">County (Municipality)</span></span> |
| <span data-ttu-id="921c2-733">Adres</span><span class="sxs-lookup"><span data-stu-id="921c2-733">Street</span></span>              | <span data-ttu-id="921c2-734">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="921c2-734">Address Line 1</span></span>        |
| <span data-ttu-id="921c2-735">Huisnummer</span><span class="sxs-lookup"><span data-stu-id="921c2-735">Street Number</span></span>       | <span data-ttu-id="921c2-736">Adresregel 2</span><span class="sxs-lookup"><span data-stu-id="921c2-736">Address Line 2</span></span>        |
| <span data-ttu-id="921c2-737">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="921c2-737">Building Complement</span></span> | <span data-ttu-id="921c2-738">Adresregel 5</span><span class="sxs-lookup"><span data-stu-id="921c2-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="921c2-739">Paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="921c2-739">Passport number</span></span>

<span data-ttu-id="921c2-740">Werknemers kunnen paspoortgegevens opgeven.</span><span class="sxs-lookup"><span data-stu-id="921c2-740">Employees can declare passport information.</span></span> <span data-ttu-id="921c2-741">Deze informatie is van het identificatietype **Paspoort** en wordt in Dayforce geïntegreerd als onderdeel van de Mexico-specifieke informatie van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="921c2-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="921c2-742">Identificatietype = 'Paspoort'</span><span class="sxs-lookup"><span data-stu-id="921c2-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="921c2-743">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="921c2-743">Issued Date</span></span>
- <span data-ttu-id="921c2-744">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="921c2-744">Expiration Date</span></span>

<span data-ttu-id="921c2-745">Werknemers kunnen meerdere identificatienummers van het identificatietype **Paspoort** opgeven.</span><span class="sxs-lookup"><span data-stu-id="921c2-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="921c2-746">Echter alleen de huidige actieve paspoortvermelding wordt geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="921c2-747">Als alle paspoortvermeldingen zijn verlopen, wordt het paspoort dat als laatste is uitgegeven geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="921c2-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]