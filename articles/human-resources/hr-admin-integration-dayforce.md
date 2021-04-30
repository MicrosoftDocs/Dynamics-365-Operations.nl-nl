---
title: Integratie met Dayforce configureren
description: De integratie tussen Microsoft Dynamics 365 Human Resources en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen, die in dit artikel worden beschreven. Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Human Resources als Dayforce.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889999"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="d4e8c-104">Integratie met Dayforce configureren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d4e8c-105">De integratie tussen Microsoft Dynamics 365 Human Resources en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen, die in dit artikel worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="d4e8c-106">Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Human Resources als Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d4e8c-107">Als u een service zoals Dayforce gebruikt voor het uitvoeren van betalingen, moet u de integratie inschakelen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="d4e8c-108">De integratie vereist specifieke gegevens vanuit Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="d4e8c-109">Daarom moet u controleren of gegevens die zijn toegewezen aan Dayforce, zodanig in Human Resources zijn geconfigureerd dat de integratie wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="d4e8c-110">De integratie maakt gebruik van de volgende brede categorieën gegevens:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d4e8c-111">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-111">Human resources data</span></span>
- <span data-ttu-id="d4e8c-112">Compensatiegegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-112">Compensation data</span></span>
- <span data-ttu-id="d4e8c-113">Salarisgegevens, zoals betalingscycli, salarisperioden en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d4e8c-114">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-114">Worker data</span></span>

<span data-ttu-id="d4e8c-115">In dit artikel worden de stappen beschreven die u moet volgen om de integratie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d4e8c-116">Ook wordt uitgelegd welke typen gegevens en welke configuratiedetails vereist zijn voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d4e8c-117">De integratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-117">Enable the integration</span></span>

<span data-ttu-id="d4e8c-118">In Human Resources moet u de integratie inschakelen en de configuratiegegevens invoeren om verbinding te maken met Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d4e8c-119">Als u wilt dat de grootboektransactie die wordt geproduceerd wordt geïmporteerd in Microsoft Dynamics 365 Finance, moet u ook een Microsoft Azure-opslagaccount instellen en de verbindingstekenreeks voor Azure Storage invoeren in Finance.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="d4e8c-120">Voer de volgende stappen uit om de integratie in Human Resources in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="d4e8c-121">Ga naar de pagina **Systeembeheer** en selecteer **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d4e8c-122">Voer het beveiligde FTP-eindpunt (File Transfer Protocol) en het pad naar de beveiligde FTP-map in.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d4e8c-123">Voer de gebruikersnaam en het wachtwoord in van de gebruiker die toegang krijgt tot het beveiligde FTP-eindpunt en het mappad.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d4e8c-124">Test de verbinding, zoals vereist, en stel de optie **Integratie van salarisadministratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d4e8c-125">Wanneer de integratie is ingeschakeld, worden het pakket voor gegevensexport en de bestanden gemaakt en wordt de frequentie ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d4e8c-126">U kunt deze frequentie naar behoefte wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="d4e8c-127">Zie de volgende Azure-artikelen voor meer informatie over Azure Storage-accounts en Azure Storage-verbindingstekenreeksen:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="d4e8c-128">Informatie over Azure-opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="d4e8c-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d4e8c-129">Verbindingstekenreeks voor Azure Storage configureren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d4e8c-130">Technische details wanneer integratie van salarisadministratie is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="d4e8c-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d4e8c-131">Het inschakelen van de integratie van de salarisadministratie heeft twee belangrijke effecten:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d4e8c-132">Er wordt een gegevensexportproject met de naam Export van integratie van salarisadministratie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d4e8c-133">Dit project bevat de entiteiten en velden die nodig zijn voor de integratie van de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d4e8c-134">Als u het project wilt onderzoeken, gaat u naar **Systeembeheer**, selecteert u de tegel **Gegevensbeheer** en opent u het gegevensproject in de lijst met projecten.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d4e8c-135">Met deze batchtaak wordt het gegevensexportproject uitgevoerd, wordt het resulterende gegevenspakket gecodeerd en wordt het gegevenspakketbestand overgebracht naar het SFTP-eindpunt dat is geconfigureerd in het scherm **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d4e8c-136">Het gegevenspakket dat naar het SFTP-eind punt wordt overgebracht, is gecodeerd met een sleutel die uniek is voor het pakket.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d4e8c-137">De sleutel bevindt zich in een Azure-sleutelkluis die alleen toegankelijk is via Ceridian.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d4e8c-138">Het is niet mogelijk om de inhoud van het gegevenspakket te decoderen en te onderzoeken.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d4e8c-139">Als u de inhoud van het gegevenspakket wilt controleren, moet u het gegevensproject Export van integratie van salarisadministratie handmatig exporteren, downloaden en vervolgens openen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d4e8c-140">Bij een handmatige export wordt er geen codering toegepast of wordt het pakket niet overgedragen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="d4e8c-141">Wanneer de integratiebestanden bijvoorbeeld worden verzonden vanuit een UAT- of sandboxomgeving in Dynamics 365 Human Resources naar een Ceridian Dayforce Test-omgeving, kunt u de volgende Key Vault-URL gebruiken: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d4e8c-142">Uw gegevens configureren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-142">Configure your data</span></span> 

<span data-ttu-id="d4e8c-143">Om salarissen te kunnen verwerken, moet u resourcegegevens configureren in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="d4e8c-144">U moet gegevens over de organisatie, zoals taken en functies, instellen samen met informatie over vergoedingen en compensatie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d4e8c-145">Deze informatie biedt de informatie over dienstverband, salaris en inhoudingen die vereist is om het salaris van werknemers te genereren.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d4e8c-146">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d4e8c-147">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-147">Benefits</span></span> 

<span data-ttu-id="d4e8c-148">Human resources biedt hulpmiddelen voor het instellen en onderhouden van de vergoedingen, inhoudingen en compensatieplannen van medewerkers die een organisatie zijn medewerkers biedt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d4e8c-149">Wanneer u vergoedingen maakt, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d4e8c-150">Vergoedingsplannen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-150">Benefit plans</span></span>

- <span data-ttu-id="d4e8c-151">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-151">Plan (required)</span></span>
- <span data-ttu-id="d4e8c-152">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-152">Type (required)</span></span>
- <span data-ttu-id="d4e8c-153">Gevolgen voor salaris (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-153">Payroll impact (required)</span></span>
- <span data-ttu-id="d4e8c-154">Achterstallige betalingen herstellen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-154">Recover arrears</span></span>
- <span data-ttu-id="d4e8c-155">Inhoudingsmethode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-155">Deduction method</span></span>
- <span data-ttu-id="d4e8c-156">Inhoudingsprioriteit</span><span class="sxs-lookup"><span data-stu-id="d4e8c-156">Deduction priority</span></span>
- <span data-ttu-id="d4e8c-157">Limietperiode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-157">Limit period</span></span>
- <span data-ttu-id="d4e8c-158">Bedrag beperken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d4e8c-159">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-159">Benefits</span></span>

- <span data-ttu-id="d4e8c-160">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-160">Plan (required)</span></span>
- <span data-ttu-id="d4e8c-161">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-161">Type (required)</span></span>
- <span data-ttu-id="d4e8c-162">Optie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-162">Option (required)</span></span>
- <span data-ttu-id="d4e8c-163">Vergoeding-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-163">Benefit ID (required)</span></span>
- <span data-ttu-id="d4e8c-164">Frequentie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-164">Frequency</span></span>
- <span data-ttu-id="d4e8c-165">Basis</span><span class="sxs-lookup"><span data-stu-id="d4e8c-165">Basis</span></span>
- <span data-ttu-id="d4e8c-166">Bedrag of tarief</span><span class="sxs-lookup"><span data-stu-id="d4e8c-166">Amount or rate</span></span>
- <span data-ttu-id="d4e8c-167">Inkomstencode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d4e8c-168">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="d4e8c-168">Supported frequencies</span></span> 

- <span data-ttu-id="d4e8c-169">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="d4e8c-169">Weekly</span></span>
- <span data-ttu-id="d4e8c-170">Tweewekelijks</span><span class="sxs-lookup"><span data-stu-id="d4e8c-170">Bi-weekly</span></span>
- <span data-ttu-id="d4e8c-171">Halfmaandelijks</span><span class="sxs-lookup"><span data-stu-id="d4e8c-171">Semi-monthly</span></span>
- <span data-ttu-id="d4e8c-172">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="d4e8c-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d4e8c-173">Ondersteund bases</span><span class="sxs-lookup"><span data-stu-id="d4e8c-173">Supported bases</span></span> 

- <span data-ttu-id="d4e8c-174">Vast bedrag</span><span class="sxs-lookup"><span data-stu-id="d4e8c-174">Fixed amount</span></span>
- <span data-ttu-id="d4e8c-175">Percentage van inkomsten</span><span class="sxs-lookup"><span data-stu-id="d4e8c-175">Percent of earnings</span></span>
- <span data-ttu-id="d4e8c-176">Productieve uren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-176">Productive hours</span></span>

<span data-ttu-id="d4e8c-177">Dayforce maakt de volgende inhoudingen, op basis van de salarisgevolgen die zijn gedefinieerd voor het vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d4e8c-178">Selectie in Human Resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-178">Selection in Human Resources</span></span>        | <span data-ttu-id="d4e8c-179">Resultaat in Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d4e8c-180">Geen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-180">None</span></span>                       | <span data-ttu-id="d4e8c-181">Er wordt geen inhouding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="d4e8c-182">Alleen inhouding</span><span class="sxs-lookup"><span data-stu-id="d4e8c-182">Deduction only</span></span>             | <span data-ttu-id="d4e8c-183">Er wordt een inhouding voor de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d4e8c-184">Alleen bijdrage</span><span class="sxs-lookup"><span data-stu-id="d4e8c-184">Contribution only</span></span>          | <span data-ttu-id="d4e8c-185">Er wordt een inhouding voor de werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d4e8c-186">Inhouding en bijdrage</span><span class="sxs-lookup"><span data-stu-id="d4e8c-186">Deduction and contribution</span></span> | <span data-ttu-id="d4e8c-187">Er worden inhoudingen voor werknemer en werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d4e8c-188">Zie de volgende artikelen voor meer informatie over het definiëren en beheren van een vergoedingsprogramma:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="d4e8c-189">Een vergoedingenprogramma voor werknemers maken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d4e8c-190">Een nieuwe vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d4e8c-191">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d4e8c-192">Vergoedingen inschrijven en verwijderen van medewerkers</span><span class="sxs-lookup"><span data-stu-id="d4e8c-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d4e8c-193">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-193">Compensation</span></span> 

<span data-ttu-id="d4e8c-194">Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d4e8c-195">Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d4e8c-196">De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d4e8c-197">Dayforce gebruikt compensatie-informatie voor het berekenen van het uur- of jaartarief van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d4e8c-198">Er zijn vastecompensatieplannen en conversies van het loontarief vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d4e8c-199">Werknemers moeten worden gekoppeld aan een vastecompensatieplan.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d4e8c-200">Zie de volgende artikelen voor meer informatie over compensatieplannen:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="d4e8c-201">Plannen voor vaste compensatie maken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d4e8c-202">Plannen voor variabele compensatie maken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d4e8c-203">Salaris-/compensatiestructuur en -plannen ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d4e8c-204">Compensatie verwerken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d4e8c-205">Compensatieproces definiëren en resultaten berekenen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d4e8c-206">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="d4e8c-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d4e8c-207">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="d4e8c-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d4e8c-208">Taken</span><span class="sxs-lookup"><span data-stu-id="d4e8c-208">Jobs</span></span> 

<span data-ttu-id="d4e8c-209">Een functie is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een functie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d4e8c-210">Zie de volgende artikelen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d4e8c-211">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d4e8c-212">Nieuwe taken definiëren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d4e8c-213">Posities</span><span class="sxs-lookup"><span data-stu-id="d4e8c-213">Positions</span></span>

<span data-ttu-id="d4e8c-214">Een positie is een afzonderlijk exemplaar van een taak.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="d4e8c-215">De positie 'Verkoopmanager (Oost)' is bijvoorbeeld een van de posities die zijn gekoppeld aan de functie 'Verkoopmanager'.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d4e8c-216">Een positie bestaat op een afdeling.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-216">A position exists in a department.</span></span> <span data-ttu-id="d4e8c-217">Aan elke positie kan slechts één medewerker worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d4e8c-218">Let op de volgende gegevens en configuratie bij het instellen van posities:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d4e8c-219">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-219">Position (required)</span></span>
- <span data-ttu-id="d4e8c-220">Beschrijving (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-220">Description (required)</span></span>
- <span data-ttu-id="d4e8c-221">Functie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-221">Job (required)</span></span>
- <span data-ttu-id="d4e8c-222">Afdeling (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-222">Department (required)</span></span>
- <span data-ttu-id="d4e8c-223">Positietype (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-223">Position type (required)</span></span>
- <span data-ttu-id="d4e8c-224">Voltijdse equivalent</span><span class="sxs-lookup"><span data-stu-id="d4e8c-224">Full-time equivalent</span></span>
- <span data-ttu-id="d4e8c-225">Jaarlijkse normale uren (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="d4e8c-226">Betaald door rechtspersoon (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d4e8c-227">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-227">Pay cycle (required)</span></span>
- <span data-ttu-id="d4e8c-228">Standaard financiële dimensie: kostenplaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d4e8c-229">Medewerkertoewijzing: medewerker, toewijzing begin, einde toewijzing, redencode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d4e8c-230">Als meerdere posities op dezelfde afdeling aan dezelfde functie zijn gekoppeld, worden deze geconsolideerd in een enkele positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d4e8c-231">Zie de volgende artikelen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d4e8c-232">Uw werknemers organiseren met afdelingen, taken en posities</span><span class="sxs-lookup"><span data-stu-id="d4e8c-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d4e8c-233">Posities instellen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d4e8c-234">Afdelingen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-234">Departments</span></span>

<span data-ttu-id="d4e8c-235">Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d4e8c-236">Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d4e8c-237">U kunt afdelingen gebruiken om te rapporteren over functiegebieden.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d4e8c-238">Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d4e8c-239">Zie de volgende artikelen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d4e8c-240">Een afdeling maken en koppelen aan de afdelingshiërarchie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d4e8c-241">Nieuwe afdelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d4e8c-242">Betalingscycli en salarisperioden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="d4e8c-243">Een betalingscyclus bepaalt hoe vaak salarissen worden berekend en op welke specifieke dagen medewerkers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d4e8c-244">Zo kan bijvooorbeeld een betalingscyclus maandelijks zijn en kunnen werknemers worden uitbetaald op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d4e8c-245">Een betalingscyclus kan ook wekelijks en werknemers kunnen worden uitbetaald op de dinsdag na het einde van de salarisperiode.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d4e8c-246">Betalingscycli zijn toegewezen aan posities om te bepalen wanneer medewerkers in deze posities worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d4e8c-247">Nadat u betalingscycli hebt gemaakt, kunt u salarisperioden voor elke cyclus genereren.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d4e8c-248">Elke salarisperiode bevat een standaard betalingsdatum die is gebaseerd op gegevens die u verstrekt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d4e8c-249">U kunt echter de standaard betalingsdatum in een salarisperiode wijzigen om te voorzien in uitzonderingen, bijvoorbeeld wanneer de betalingsdatum op een feestdag valt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d4e8c-250">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d4e8c-251">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-251">Pay cycle (required)</span></span>
- <span data-ttu-id="d4e8c-252">Frequentie van betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d4e8c-253">Begindatum van periode (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d4e8c-254">Standaardbetalingsdatum (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d4e8c-255">Deze informatie is geïntegreerd met Dayforce als betalingsgroepen en worden gescheiden per land of regio voor elke betalingscyclus.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d4e8c-256">Vóór integratie moet ten minste één salarisperiode worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d4e8c-257">Dayforce genereert van betalingsgroepkalenders en betalingsdatums, op basis van de begindatum van de eerste salarisperiode en de standaardbetalingsdatum die is ingesteld in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d4e8c-258">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-258">Earning codes</span></span>

<span data-ttu-id="d4e8c-259">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d4e8c-260">De codes hebben verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d4e8c-261">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d4e8c-262">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-262">Earning Code (required)</span></span>
- <span data-ttu-id="d4e8c-263">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-263">Description</span></span>
- <span data-ttu-id="d4e8c-264">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="d4e8c-264">Unit of measure</span></span>
- <span data-ttu-id="d4e8c-265">Productief</span><span class="sxs-lookup"><span data-stu-id="d4e8c-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d4e8c-266">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-266">Worker data</span></span>

<span data-ttu-id="d4e8c-267">Records voor de verschillende soorten medewerkers die u hebt zijn belangrijk voor uw HRM- en salarisadministratiesystemen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d4e8c-268">De gegevens die u invoert, kunnen worden gebruikt om medewerkers en persoonlijke gegevens bij te houden.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d4e8c-269">U kunt de volgende informatie bijhouden voor medewerkers:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d4e8c-270">**Basis** – Basisinformatie over een medewerker bijhouden, zoals contactgegevens, demografische gegevens, identificatiegegevens, informatie over de familie, status van militaire dienst, expat-informatie en contactpersonen voor noodgevallen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d4e8c-271">**Dienstverband** – Informatie bijhouden over werkgelegenheid van een medewerker, zoals een aansluiting met een bedrijf of organisatie, functie, start- en einddatums, arbeidsgeschiktheid, arbeidsvoorwaarden, pensioen, verlof en relocatie-informatie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d4e8c-272">**Verlof en verzuim** – Informatie bijhouden over de afwezigheid van een medewerker, zoals werkkalenders, verzuimtransacties en verzuiminstellingen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d4e8c-273">**Vergoedingen en salarissen** – Informatie bijhouden over compensatieplannen en salarisgegevens van een medewerker zoals inschrijving op plan, onderscheidingen, commissie, fiscale informatie, pensioen en salarisinhoudingen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d4e8c-274">Wanneer u informatie over een werknemer invoert, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d4e8c-275">Algemene informatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-275">General information</span></span>

- <span data-ttu-id="d4e8c-276">Personeelsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-276">Personnel number (required)</span></span>
- <span data-ttu-id="d4e8c-277">Voornaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-277">First name (required)</span></span>
- <span data-ttu-id="d4e8c-278">Achternaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-278">Last name (required)</span></span>
- <span data-ttu-id="d4e8c-279">Tweede naam</span><span class="sxs-lookup"><span data-stu-id="d4e8c-279">Middle name</span></span>
- <span data-ttu-id="d4e8c-280">Anciënniteitsdatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-280">Seniority date</span></span>
- <span data-ttu-id="d4e8c-281">Bekend als</span><span class="sxs-lookup"><span data-stu-id="d4e8c-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d4e8c-282">Persoonlijke informatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-282">Personal information</span></span>

- <span data-ttu-id="d4e8c-283">Burgerlijke staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-283">Marital status (required)</span></span>
- <span data-ttu-id="d4e8c-284">Geboortedatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-284">Birth date (required)</span></span>
- <span data-ttu-id="d4e8c-285">Geslacht (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-285">Gender (required)</span></span>
- <span data-ttu-id="d4e8c-286">Persoon met handicap</span><span class="sxs-lookup"><span data-stu-id="d4e8c-286">Person with disabilities</span></span>
- <span data-ttu-id="d4e8c-287">Land/regio nationaliteit (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d4e8c-288">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-288">Address information</span></span>

- <span data-ttu-id="d4e8c-289">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-289">Primary (required)</span></span>
- <span data-ttu-id="d4e8c-290">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-290">Country/region (required)</span></span>
- <span data-ttu-id="d4e8c-291">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-291">Postal code (required)</span></span>
- <span data-ttu-id="d4e8c-292">Huisnummer (vereist) (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d4e8c-293">Gebouwtoevoeging (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d4e8c-294">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-294">City (required)</span></span>
- <span data-ttu-id="d4e8c-295">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-295">State (required)</span></span>
- <span data-ttu-id="d4e8c-296">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d4e8c-297">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="d4e8c-297">Contact information</span></span> 

- <span data-ttu-id="d4e8c-298">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-298">Primary (required)</span></span>
- <span data-ttu-id="d4e8c-299">Contactnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-299">Contact number (required)</span></span>
- <span data-ttu-id="d4e8c-300">Toestel</span><span class="sxs-lookup"><span data-stu-id="d4e8c-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d4e8c-301">Salarisinformatie en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-301">Payroll information and earning codes</span></span>

<span data-ttu-id="d4e8c-302">Aan werknemers kunnen bepaalde inkomsten met een bepaalde betalingsfrequentie worden toegewezen en zij kunnen een geprefereerde betalingsmethode hebben.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d4e8c-303">De volgende velden worden gebruikt in Dayforce om te garanderen dat deze voorkeuren en instellingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d4e8c-304">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-304">Earning codes</span></span>

- <span data-ttu-id="d4e8c-305">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-305">Position (required)</span></span>
- <span data-ttu-id="d4e8c-306">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-306">Earning Code (required)</span></span>
- <span data-ttu-id="d4e8c-307">Frequentie (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-307">Frequency (required)</span></span>
- <span data-ttu-id="d4e8c-308">Bedrag (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d4e8c-309">Salarisinformatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-309">Payroll information</span></span>

- <span data-ttu-id="d4e8c-310">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-310">Payment Method</span></span>
- <span data-ttu-id="d4e8c-311">Economische regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-311">Economic Region (required)</span></span>
- <span data-ttu-id="d4e8c-312">Id personeelsvergoedingen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-312">Employee Benefits ID</span></span>
- <span data-ttu-id="d4e8c-313">Nationaal id-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-313">National ID Number (required)</span></span>
- <span data-ttu-id="d4e8c-314">Nummer militaire dienst</span><span class="sxs-lookup"><span data-stu-id="d4e8c-314">Military Service Number</span></span>
- <span data-ttu-id="d4e8c-315">Ploeg-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-315">Shift ID (required)</span></span>
- <span data-ttu-id="d4e8c-316">Btw-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-316">Tax Number (required)</span></span>
- <span data-ttu-id="d4e8c-317">Vakbond-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-317">Union ID (required)</span></span>
- <span data-ttu-id="d4e8c-318">Werkdag-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-318">Work Day ID (required)</span></span>
- <span data-ttu-id="d4e8c-319">Nummer werkvergunning</span><span class="sxs-lookup"><span data-stu-id="d4e8c-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d4e8c-320">Voor de betalingsmethode ondersteunt Mexico **Contant geld**, **Cheque** (de fysieke cheque van het bedrijf) en **Elektronische betaling**.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d4e8c-321">Als geen betalingsmethode is opgegeven, wordt standaard **Cheque** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d4e8c-322">Details dienstverband</span><span class="sxs-lookup"><span data-stu-id="d4e8c-322">Employment details</span></span>

<span data-ttu-id="d4e8c-323">Historische gegevens over het dienstverband worden gebruikt als belangrijkste informatie voor het opvragen van de statussen voor aanstellen, ontslaan en opnieuw aanstellen van een werknemer in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d4e8c-324">Dayforce ondersteunt slechts één actieve dienstverbandrecord tegelijk.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d4e8c-325">Begindatum dienstverband (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-325">Employment start date (required)</span></span>
- <span data-ttu-id="d4e8c-326">Einddatum dienstverband</span><span class="sxs-lookup"><span data-stu-id="d4e8c-326">Employment end date</span></span>
- <span data-ttu-id="d4e8c-327">Begindatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-327">Start date</span></span>
- <span data-ttu-id="d4e8c-328">Aangepaste begindatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-328">Adjusted start date</span></span>
- <span data-ttu-id="d4e8c-329">Ontslagdatum (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d4e8c-330">Ontslagreden (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d4e8c-331">De belangrijkste datums van een werknemer worden afgeleid met behulp van de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d4e8c-332">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-332">Human Resources</span></span>                | <span data-ttu-id="d4e8c-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e8c-334">Meest recente huurdatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-334">Most recent hire date</span></span> | <span data-ttu-id="d4e8c-335">Begindatum van dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="d4e8c-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d4e8c-336">Ontslagdatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-336">Termination date</span></span>      | <span data-ttu-id="d4e8c-337">Ontslagdatum van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="d4e8c-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d4e8c-338">Begindatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-338">Start date</span></span>            | <span data-ttu-id="d4e8c-339">Aangepaste begindatum, begindatum of begindatum dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="d4e8c-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d4e8c-340">Oorspronkelijke datum indiensttreding</span><span class="sxs-lookup"><span data-stu-id="d4e8c-340">Original hire date</span></span>    | <span data-ttu-id="d4e8c-341">Begindatum dienstverband van vroegste historierecord van dienstverband</span><span class="sxs-lookup"><span data-stu-id="d4e8c-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d4e8c-342">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-342">Compensation</span></span>

<span data-ttu-id="d4e8c-343">Een vastecompensatieplan moet worden gekoppeld aan de primaire functie van elke werknemer tijdens de hele duur van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d4e8c-344">Deze periode begint op de datum waarop de werknemer in dienst is genomen (of de begindatum van het dienstverband) en gaat door totdat aan het ontslag.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d4e8c-345">Ingangsdatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-345">Effective Date (required)</span></span>
- <span data-ttu-id="d4e8c-346">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-346">Expiration date</span></span>
- <span data-ttu-id="d4e8c-347">Loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-347">Pay Rate (required)</span></span>
- <span data-ttu-id="d4e8c-348">Conversies van loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d4e8c-349">Jaarlijks equivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="d4e8c-350">Uurequivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="d4e8c-351">Als een werknemer met uurtarief meerdere posities heeft, wordt de vaste compensatie van de primaire positie geïmporteerd in Dayforce als het basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d4e8c-352">Voor niet-primaire posities, wordt het uurtarief opgeslagen bij de overeenkomende positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d4e8c-353">Als een medewerker met een salaris meerdere posities heeft, worden het cumulatieve uurtarief en het jaarsalaris voor alle actieve posities afgeleid en gebruikt als de basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d4e8c-354">Identificatienummers</span><span class="sxs-lookup"><span data-stu-id="d4e8c-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d4e8c-355">Sociaal-fiscaal nummer</span><span class="sxs-lookup"><span data-stu-id="d4e8c-355">Social Security identifier</span></span> 

<span data-ttu-id="d4e8c-356">Elke werknemer moet één primaire id hebben.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d4e8c-357">Deze id moet van het identificatietype **Sofinummer** zijn.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d4e8c-358">In Dayforce, wordt dit automatisch afgeleid als het sociaal-fiscaal nummer van de werknemer dat is vereist voor aanstelling.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d4e8c-359">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-359">Primary (required)</span></span>
- <span data-ttu-id="d4e8c-360">Identificatietype = 'Sofinummer'</span><span class="sxs-lookup"><span data-stu-id="d4e8c-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d4e8c-361">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-361">Issued Date</span></span>
- <span data-ttu-id="d4e8c-362">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-362">Expiration Date</span></span>

<span data-ttu-id="d4e8c-363">Werknemers kunnen meerdere identificatienummers van het identificatietype **Sofinummer** opgeven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d4e8c-364">Alleen de record die is gemarkeerd als **Primair** wordt echter opgenomen in Dayforce, ongeacht of het nummer actief of verlopen is.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d4e8c-365">Bankrekeningen en voorschotten</span><span class="sxs-lookup"><span data-stu-id="d4e8c-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="d4e8c-366">Er moet geldige bankrekeninginformatie worden ingevoerd voor elke werknemer die wil worden uitbetaald via bankrekeningoverboekingen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d4e8c-367">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-367">Human Resources</span></span>                         | <span data-ttu-id="d4e8c-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e8c-369">Bankrekeningnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d4e8c-370">SWIFT-code (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-370">SWIFT code (required)</span></span>          | <span data-ttu-id="d4e8c-371">Veld **Bank-id** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d4e8c-372">Vestigingsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d4e8c-373">Bankrekeningtype (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-373">Bank account type (required)</span></span>   | <span data-ttu-id="d4e8c-374">Veld **Rekeningtype** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d4e8c-375">Ondersteunde waarden zijn **Rekening-courant** en **Salaris**.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d4e8c-376">Werknemers die ervoor kiezen om te worden uitbetaald via bankrekeningoverboekingen moeten een koppeling opgeven naar een restantrekening die zich onder een rechtspersoon bevindt met het primaire adres in Mexico en die is gekoppeld aan een geldige bankrekening van een Mexicaanse bank.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d4e8c-377">Alle andere niet-restantrekeningen worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d4e8c-378">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="d4e8c-378">Address information</span></span>

<span data-ttu-id="d4e8c-379">Elke werknemer moet één primaire locatie hebben.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-379">Every employee must have one primary location.</span></span> <span data-ttu-id="d4e8c-380">In Dayforce wordt deze locatie gebruikt om de primaire woonplaats van de werknemer te bepalen voor belastingdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d4e8c-381">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-381">Primary (required)</span></span>
- <span data-ttu-id="d4e8c-382">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-382">Country/region (required)</span></span>
- <span data-ttu-id="d4e8c-383">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="d4e8c-384">Straat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-384">Street (required)</span></span>
- <span data-ttu-id="d4e8c-385">Huisnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-385">Street Number (required)</span></span>
- <span data-ttu-id="d4e8c-386">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="d4e8c-386">Building Complement</span></span>
- <span data-ttu-id="d4e8c-387">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-387">City (required)</span></span>
- <span data-ttu-id="d4e8c-388">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-388">State (required)</span></span>
- <span data-ttu-id="d4e8c-389">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d4e8c-390">Uw gegevens configureren voor het genereren van salarissen in de Verenigde Staten en Canada</span><span class="sxs-lookup"><span data-stu-id="d4e8c-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d4e8c-391">Als u salarissen genereert voor werknemers in de Verenigde Staten en Canada, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d4e8c-392">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-392">Departments are required on positions.</span></span>
- <span data-ttu-id="d4e8c-393">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d4e8c-394">U kunt Human Resources zo configureren dat wordt vereist dat met posities een afdeling wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="d4e8c-395">Hiertoe gaat u naar **Gedeelde Human Resources-posities > Posities > Afdelingen voor posities vereisen**.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d4e8c-396">Het wordt aanbevolen deze instelling af te dwingen voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d4e8c-397">Functietypen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-397">Job types</span></span>

<span data-ttu-id="d4e8c-398">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d4e8c-399">Functietypen zijn vereist voor het verwerken van salarissen in de Verenigde Staten en Canada.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d4e8c-400">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d4e8c-401">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d4e8c-402">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-403">Functietype</span><span class="sxs-lookup"><span data-stu-id="d4e8c-403">Job type</span></span>   | <span data-ttu-id="d4e8c-404">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d4e8c-405">Per uur</span><span class="sxs-lookup"><span data-stu-id="d4e8c-405">Hourly</span></span>     | <span data-ttu-id="d4e8c-406">Per uur</span><span class="sxs-lookup"><span data-stu-id="d4e8c-406">Hourly</span></span>      |
| <span data-ttu-id="d4e8c-407">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-407">Salaried</span></span>   | <span data-ttu-id="d4e8c-408">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d4e8c-409">Positietypen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-409">Position types</span></span> 

<span data-ttu-id="d4e8c-410">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d4e8c-411">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d4e8c-412">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-413">Positietype</span><span class="sxs-lookup"><span data-stu-id="d4e8c-413">Position type</span></span>   | <span data-ttu-id="d4e8c-414">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d4e8c-415">Voltijd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-415">Full-time</span></span>       | <span data-ttu-id="d4e8c-416">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="d4e8c-416">Full time employee</span></span> |
| <span data-ttu-id="d4e8c-417">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-417">Part-time</span></span>       | <span data-ttu-id="d4e8c-418">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d4e8c-419">Redencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-419">Reason codes</span></span>

<span data-ttu-id="d4e8c-420">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d4e8c-421">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d4e8c-422">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-423">Redencode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-423">Reason code</span></span>    | <span data-ttu-id="d4e8c-424">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-424">Description</span></span>      | <span data-ttu-id="d4e8c-425">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="d4e8c-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d4e8c-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d4e8c-426">RESIGNATION</span></span>    | <span data-ttu-id="d4e8c-427">Ontslag</span><span class="sxs-lookup"><span data-stu-id="d4e8c-427">Resignation</span></span>      | <span data-ttu-id="d4e8c-428">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-428">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d4e8c-429">TERMINATION</span></span>    | <span data-ttu-id="d4e8c-430">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="d4e8c-430">Termination</span></span>      | <span data-ttu-id="d4e8c-431">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-431">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d4e8c-432">RETIREMENT</span></span>     | <span data-ttu-id="d4e8c-433">Pensionering</span><span class="sxs-lookup"><span data-stu-id="d4e8c-433">Retirement</span></span>       | <span data-ttu-id="d4e8c-434">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-434">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-435">OTHER</span><span class="sxs-lookup"><span data-stu-id="d4e8c-435">OTHER</span></span>          | <span data-ttu-id="d4e8c-436">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-436">Other Reasons</span></span>    | <span data-ttu-id="d4e8c-437">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-437">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-438">DEATH</span></span>          | <span data-ttu-id="d4e8c-439">Overlijden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-439">Death</span></span>            | <span data-ttu-id="d4e8c-440">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-440">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d4e8c-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d4e8c-442">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="d4e8c-442">Leave of Absence</span></span> | <span data-ttu-id="d4e8c-443">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-443">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d4e8c-444">CONTRACTEND</span></span>    | <span data-ttu-id="d4e8c-445">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="d4e8c-445">End of Contract</span></span>  | <span data-ttu-id="d4e8c-446">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-446">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d4e8c-447">SALARYCHANGE</span></span>   | <span data-ttu-id="d4e8c-448">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="d4e8c-448">Change of Salary</span></span> | <span data-ttu-id="d4e8c-449">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d4e8c-450">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="d4e8c-450">Marital status</span></span>

<span data-ttu-id="d4e8c-451">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4e8c-452">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4e8c-453">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-453">Human Resources</span></span>                 | <span data-ttu-id="d4e8c-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d4e8c-455">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-455">Married</span></span>                | <span data-ttu-id="d4e8c-456">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-456">Married</span></span>              |
| <span data-ttu-id="d4e8c-457">Eén</span><span class="sxs-lookup"><span data-stu-id="d4e8c-457">Single</span></span>                 | <span data-ttu-id="d4e8c-458">Eén</span><span class="sxs-lookup"><span data-stu-id="d4e8c-458">Single</span></span>               |
| <span data-ttu-id="d4e8c-459">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d4e8c-459">Widowed</span></span>                | <span data-ttu-id="d4e8c-460">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d4e8c-460">Widowed</span></span>              |
| <span data-ttu-id="d4e8c-461">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-461">Divorced</span></span>               | <span data-ttu-id="d4e8c-462">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-462">Divorced</span></span>             |
| <span data-ttu-id="d4e8c-463">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="d4e8c-463">Registered Partnership</span></span> | <span data-ttu-id="d4e8c-464">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="d4e8c-464">Domestic Partnership</span></span> |
| <span data-ttu-id="d4e8c-465">None</span><span class="sxs-lookup"><span data-stu-id="d4e8c-465">None</span></span>                   | <span data-ttu-id="d4e8c-466">None</span><span class="sxs-lookup"><span data-stu-id="d4e8c-466">None</span></span>                 |
| <span data-ttu-id="d4e8c-467">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="d4e8c-467">Cohabiting</span></span>             | <span data-ttu-id="d4e8c-468">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="d4e8c-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d4e8c-469">Geslacht</span><span class="sxs-lookup"><span data-stu-id="d4e8c-469">Gender</span></span>

<span data-ttu-id="d4e8c-470">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4e8c-471">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4e8c-472">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-472">Human Resources</span></span>       | <span data-ttu-id="d4e8c-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d4e8c-474">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-474">Male</span></span>         | <span data-ttu-id="d4e8c-475">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-475">Male</span></span>            |
| <span data-ttu-id="d4e8c-476">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-476">Female</span></span>       | <span data-ttu-id="d4e8c-477">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-477">Female</span></span>          |
| <span data-ttu-id="d4e8c-478">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="d4e8c-478">Non-specific</span></span> | <span data-ttu-id="d4e8c-479">*Niet ondersteund*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d4e8c-480">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-480">Earning codes</span></span>

<span data-ttu-id="d4e8c-481">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d4e8c-482">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d4e8c-483">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d4e8c-484">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="d4e8c-484">Supported frequencies</span></span>

- <span data-ttu-id="d4e8c-485">Alles</span><span class="sxs-lookup"><span data-stu-id="d4e8c-485">All</span></span>
- <span data-ttu-id="d4e8c-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d4e8c-486">EVERYPAY</span></span>
- <span data-ttu-id="d4e8c-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d4e8c-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d4e8c-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d4e8c-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d4e8c-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d4e8c-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d4e8c-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-490">1OFMTH</span></span>
- <span data-ttu-id="d4e8c-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-491">LASTOFMTH</span></span>
- <span data-ttu-id="d4e8c-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-492">2OFMTH</span></span>
- <span data-ttu-id="d4e8c-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-493">3OFMTH</span></span>
- <span data-ttu-id="d4e8c-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-494">4OFMTH</span></span>
- <span data-ttu-id="d4e8c-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-495">5OFMTH</span></span>
- <span data-ttu-id="d4e8c-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-496">1N2OFMTH</span></span>
- <span data-ttu-id="d4e8c-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-497">3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-498">1N3OFMTH</span></span>
- <span data-ttu-id="d4e8c-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-499">1N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-500">2N3OFMTH</span></span>
- <span data-ttu-id="d4e8c-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-501">2N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="d4e8c-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d4e8c-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d4e8c-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d4e8c-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d4e8c-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d4e8c-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d4e8c-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d4e8c-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d4e8c-514">Adressen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-514">Addresses</span></span>

<span data-ttu-id="d4e8c-515">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d4e8c-516">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d4e8c-517">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-517">Human Resources</span></span>          | <span data-ttu-id="d4e8c-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d4e8c-519">Land/regio</span><span class="sxs-lookup"><span data-stu-id="d4e8c-519">Country/Region</span></span>  | <span data-ttu-id="d4e8c-520">Landcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-520">Country Code</span></span>          |
| <span data-ttu-id="d4e8c-521">Postcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-521">Zip/Postal Code</span></span> | <span data-ttu-id="d4e8c-522">Postcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-522">Postal Code</span></span>           |
| <span data-ttu-id="d4e8c-523">Provincie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-523">State</span></span>           | <span data-ttu-id="d4e8c-524">Staatcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-524">State Code</span></span>            |
| <span data-ttu-id="d4e8c-525">Plaats</span><span class="sxs-lookup"><span data-stu-id="d4e8c-525">City</span></span>            | <span data-ttu-id="d4e8c-526">Plaats</span><span class="sxs-lookup"><span data-stu-id="d4e8c-526">City</span></span>                  |
| <span data-ttu-id="d4e8c-527">District</span><span class="sxs-lookup"><span data-stu-id="d4e8c-527">County</span></span>          | <span data-ttu-id="d4e8c-528">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-528">County (Municipality)</span></span> |
| <span data-ttu-id="d4e8c-529">Adres</span><span class="sxs-lookup"><span data-stu-id="d4e8c-529">Street</span></span>          | <span data-ttu-id="d4e8c-530">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="d4e8c-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d4e8c-531">Belastingregio's</span><span class="sxs-lookup"><span data-stu-id="d4e8c-531">Tax regions</span></span>

<span data-ttu-id="d4e8c-532">Belastingregio's worden gebruikt om de juiste belasting te bepalen die moet worden gebruikt bij het genereren van salarissen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d4e8c-533">Belastingregio's worden aan Dayforce toegewezen als locatieadressen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d4e8c-534">De standaardbelastingregio moet aan de actieve positie van de werknemer worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d4e8c-535">Belastingregio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-535">Tax region (required)</span></span>
- <span data-ttu-id="d4e8c-536">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-536">Country/Region (required)</span></span>
- <span data-ttu-id="d4e8c-537">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-537">State (required)</span></span>
- <span data-ttu-id="d4e8c-538">District</span><span class="sxs-lookup"><span data-stu-id="d4e8c-538">County</span></span> 
- <span data-ttu-id="d4e8c-539">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d4e8c-540">Uw gegevens configureren voor het genereren van salarissen in Mexico</span><span class="sxs-lookup"><span data-stu-id="d4e8c-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d4e8c-541">Als u salarissen genereert voor werknemers in Mexico, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="d4e8c-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d4e8c-542">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-542">Departments are required on positions.</span></span>
- <span data-ttu-id="d4e8c-543">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d4e8c-544">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-544">Job types</span></span>

<span data-ttu-id="d4e8c-545">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d4e8c-546">Functietypen zijn vereist voor het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d4e8c-547">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d4e8c-548">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d4e8c-549">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-550">Functietype</span><span class="sxs-lookup"><span data-stu-id="d4e8c-550">Job type</span></span>   | <span data-ttu-id="d4e8c-551">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d4e8c-552">Per uur</span><span class="sxs-lookup"><span data-stu-id="d4e8c-552">Hourly</span></span>     | <span data-ttu-id="d4e8c-553">MX Per uur</span><span class="sxs-lookup"><span data-stu-id="d4e8c-553">MX Hourly</span></span>   |
| <span data-ttu-id="d4e8c-554">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-554">Salaried</span></span>   | <span data-ttu-id="d4e8c-555">MX Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d4e8c-556">Positietypen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-556">Position types</span></span> 

<span data-ttu-id="d4e8c-557">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d4e8c-558">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d4e8c-559">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-560">Positietype</span><span class="sxs-lookup"><span data-stu-id="d4e8c-560">Position type</span></span>   | <span data-ttu-id="d4e8c-561">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d4e8c-562">Voltijd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-562">Full-time</span></span>       | <span data-ttu-id="d4e8c-563">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="d4e8c-563">Full time employee</span></span> |
| <span data-ttu-id="d4e8c-564">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-564">Part-time</span></span>       | <span data-ttu-id="d4e8c-565">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d4e8c-566">Redencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-566">Reason codes</span></span>

<span data-ttu-id="d4e8c-567">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d4e8c-568">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d4e8c-569">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-570">Redencode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-570">Reason code</span></span>            | <span data-ttu-id="d4e8c-571">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-571">Description</span></span>                    | <span data-ttu-id="d4e8c-572">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="d4e8c-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d4e8c-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d4e8c-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d4e8c-574">Vertrek voor eerste salaris</span><span class="sxs-lookup"><span data-stu-id="d4e8c-574">Departure before first payroll</span></span> | <span data-ttu-id="d4e8c-575">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-575">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d4e8c-576">RESIGNATION</span></span>            | <span data-ttu-id="d4e8c-577">Ontslag</span><span class="sxs-lookup"><span data-stu-id="d4e8c-577">Resignation</span></span>                    | <span data-ttu-id="d4e8c-578">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-578">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="d4e8c-579">PENSION</span></span>                | <span data-ttu-id="d4e8c-580">Pensioen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-580">Pension</span></span>                        | <span data-ttu-id="d4e8c-581">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-581">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d4e8c-582">TERMINATION</span></span>            | <span data-ttu-id="d4e8c-583">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="d4e8c-583">Termination</span></span>                    | <span data-ttu-id="d4e8c-584">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-584">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d4e8c-585">RETIREMENT</span></span>             | <span data-ttu-id="d4e8c-586">Pensionering</span><span class="sxs-lookup"><span data-stu-id="d4e8c-586">Retirement</span></span>                     | <span data-ttu-id="d4e8c-587">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-587">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d4e8c-588">ABSENTEE</span></span>               | <span data-ttu-id="d4e8c-589">Verzuim</span><span class="sxs-lookup"><span data-stu-id="d4e8c-589">Absentee</span></span>                       | <span data-ttu-id="d4e8c-590">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-590">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-591">OTHER</span><span class="sxs-lookup"><span data-stu-id="d4e8c-591">OTHER</span></span>                  | <span data-ttu-id="d4e8c-592">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-592">Other Reasons</span></span>                  | <span data-ttu-id="d4e8c-593">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-593">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="d4e8c-594">CLOSURE</span></span>                | <span data-ttu-id="d4e8c-595">Bedrijfssluiting</span><span class="sxs-lookup"><span data-stu-id="d4e8c-595">Business Closure</span></span>               | <span data-ttu-id="d4e8c-596">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-596">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-597">DEATH</span></span>                  | <span data-ttu-id="d4e8c-598">Overlijden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-598">Death</span></span>                          | <span data-ttu-id="d4e8c-599">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-599">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d4e8c-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d4e8c-601">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="d4e8c-601">Leave of Absence</span></span>               | <span data-ttu-id="d4e8c-602">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-602">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d4e8c-603">CONTRACTEND</span></span>            | <span data-ttu-id="d4e8c-604">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="d4e8c-604">End of Contract</span></span>                | <span data-ttu-id="d4e8c-605">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="d4e8c-605">Terminate worker</span></span>     |
| <span data-ttu-id="d4e8c-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d4e8c-606">SALARYCHANGE</span></span>           | <span data-ttu-id="d4e8c-607">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="d4e8c-607">Change of Salary</span></span>               | <span data-ttu-id="d4e8c-608">Compensatie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d4e8c-609">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-609">Terms of employment</span></span>

<span data-ttu-id="d4e8c-610">Arbeidsvoorwaarden worden gebruikt om categorieën met arbeidsvoorwaarden te maken.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d4e8c-611">De voorwaarden worden toegewezen aan Dayforce als indicatorwaarden voor het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d4e8c-612">De volgende arbeidsvoorwaarden en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d4e8c-613">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-613">Terms of employment</span></span>   | <span data-ttu-id="d4e8c-614">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d4e8c-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d4e8c-615">Normaal</span><span class="sxs-lookup"><span data-stu-id="d4e8c-615">Regular</span></span>               | <span data-ttu-id="d4e8c-616">Normaal</span><span class="sxs-lookup"><span data-stu-id="d4e8c-616">Regular</span></span>     |
| <span data-ttu-id="d4e8c-617">Direct</span><span class="sxs-lookup"><span data-stu-id="d4e8c-617">Direct</span></span>                | <span data-ttu-id="d4e8c-618">Direct</span><span class="sxs-lookup"><span data-stu-id="d4e8c-618">Direct</span></span>      |
| <span data-ttu-id="d4e8c-619">Stage</span><span class="sxs-lookup"><span data-stu-id="d4e8c-619">Internship</span></span>            | <span data-ttu-id="d4e8c-620">Stage</span><span class="sxs-lookup"><span data-stu-id="d4e8c-620">Internship</span></span>  |
| <span data-ttu-id="d4e8c-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="d4e8c-621">Permanent</span></span>             | <span data-ttu-id="d4e8c-622">Permanent</span><span class="sxs-lookup"><span data-stu-id="d4e8c-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d4e8c-623">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="d4e8c-623">Marital status</span></span>

<span data-ttu-id="d4e8c-624">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4e8c-625">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4e8c-626">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-626">Human Resources</span></span>                 | <span data-ttu-id="d4e8c-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d4e8c-628">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-628">Married</span></span>                | <span data-ttu-id="d4e8c-629">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="d4e8c-629">Married</span></span>                   |
| <span data-ttu-id="d4e8c-630">Eén</span><span class="sxs-lookup"><span data-stu-id="d4e8c-630">Single</span></span>                 | <span data-ttu-id="d4e8c-631">Eén</span><span class="sxs-lookup"><span data-stu-id="d4e8c-631">Single</span></span>                    |
| <span data-ttu-id="d4e8c-632">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d4e8c-632">Widowed</span></span>                | <span data-ttu-id="d4e8c-633">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="d4e8c-633">Widowed</span></span>                   |
| <span data-ttu-id="d4e8c-634">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-634">Divorced</span></span>               | <span data-ttu-id="d4e8c-635">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="d4e8c-635">Divorced</span></span>                  |
| <span data-ttu-id="d4e8c-636">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="d4e8c-636">Registered Partnership</span></span> | <span data-ttu-id="d4e8c-637">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="d4e8c-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="d4e8c-638">None</span><span class="sxs-lookup"><span data-stu-id="d4e8c-638">None</span></span>                   | <span data-ttu-id="d4e8c-639">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4e8c-640">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="d4e8c-640">Cohabiting</span></span>             | <span data-ttu-id="d4e8c-641">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d4e8c-642">Geslacht</span><span class="sxs-lookup"><span data-stu-id="d4e8c-642">Gender</span></span>

<span data-ttu-id="d4e8c-643">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4e8c-644">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4e8c-645">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-645">Human Resources</span></span>       | <span data-ttu-id="d4e8c-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d4e8c-647">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-647">Male</span></span>         | <span data-ttu-id="d4e8c-648">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-648">Male</span></span>                      |
| <span data-ttu-id="d4e8c-649">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-649">Female</span></span>       | <span data-ttu-id="d4e8c-650">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="d4e8c-650">Female</span></span>                    |
| <span data-ttu-id="d4e8c-651">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="d4e8c-651">Non-specific</span></span> | <span data-ttu-id="d4e8c-652">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d4e8c-653">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-653">Payment method</span></span>

<span data-ttu-id="d4e8c-654">Betalingsmethoden bieden de werknemer en het bedrijf een manier om te beschrijven hoe werknemers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d4e8c-655">Betalingsmethoden worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4e8c-656">In de volgende tabel wordt aangegeven hoe betalingsmethoden worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4e8c-657">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-657">Human Resources</span></span>             | <span data-ttu-id="d4e8c-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d4e8c-659">Contant geld</span><span class="sxs-lookup"><span data-stu-id="d4e8c-659">Cash</span></span>               | <span data-ttu-id="d4e8c-660">Contant geld</span><span class="sxs-lookup"><span data-stu-id="d4e8c-660">Cash</span></span>                      |
| <span data-ttu-id="d4e8c-661">Elektronische betaling</span><span class="sxs-lookup"><span data-stu-id="d4e8c-661">Electronic Payment</span></span> | <span data-ttu-id="d4e8c-662">Overboeking</span><span class="sxs-lookup"><span data-stu-id="d4e8c-662">Transfer</span></span>                  |
| <span data-ttu-id="d4e8c-663">Controleren</span><span class="sxs-lookup"><span data-stu-id="d4e8c-663">Check</span></span>              | <span data-ttu-id="d4e8c-664">Cheque</span><span class="sxs-lookup"><span data-stu-id="d4e8c-664">Cheque</span></span>                    |
| <span data-ttu-id="d4e8c-665">Bankcheque</span><span class="sxs-lookup"><span data-stu-id="d4e8c-665">Bank Draft</span></span>         | <span data-ttu-id="d4e8c-666">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4e8c-667">Overig</span><span class="sxs-lookup"><span data-stu-id="d4e8c-667">Other</span></span>              | <span data-ttu-id="d4e8c-668">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d4e8c-669">Bankrekeningtype</span><span class="sxs-lookup"><span data-stu-id="d4e8c-669">Bank account type</span></span>

<span data-ttu-id="d4e8c-670">Bankrekeningtypen worden gebruikt voor elektronische betalingen aan werknemers.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d4e8c-671">Bankrekeningtypen worden toegewezen aan Dayforce als overdrachtrekeninggegevens.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d4e8c-672">De bankrekeningtypen worden, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d4e8c-673">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-673">Human Resources</span></span>            | <span data-ttu-id="d4e8c-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d4e8c-675">Betaalrekening</span><span class="sxs-lookup"><span data-stu-id="d4e8c-675">Checking Account</span></span>  | <span data-ttu-id="d4e8c-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="d4e8c-676">CheckingAccount</span></span>           |
| <span data-ttu-id="d4e8c-677">Salarisrekening</span><span class="sxs-lookup"><span data-stu-id="d4e8c-677">Payroll Account</span></span>   | <span data-ttu-id="d4e8c-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="d4e8c-678">PayrollAccount</span></span>            |
| <span data-ttu-id="d4e8c-679">Spaarrekening</span><span class="sxs-lookup"><span data-stu-id="d4e8c-679">Savings Account</span></span>   | <span data-ttu-id="d4e8c-680">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4e8c-681">BankGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="d4e8c-681">BankGirot account</span></span> | <span data-ttu-id="d4e8c-682">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4e8c-683">PlusGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="d4e8c-683">PlusGirot account</span></span> | <span data-ttu-id="d4e8c-684">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="d4e8c-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d4e8c-685">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="d4e8c-685">Earning codes</span></span>

<span data-ttu-id="d4e8c-686">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d4e8c-687">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d4e8c-688">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d4e8c-689">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="d4e8c-689">Supported frequencies</span></span>

- <span data-ttu-id="d4e8c-690">Alles</span><span class="sxs-lookup"><span data-stu-id="d4e8c-690">All</span></span>
- <span data-ttu-id="d4e8c-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d4e8c-691">EVERYPAY</span></span>
- <span data-ttu-id="d4e8c-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d4e8c-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d4e8c-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d4e8c-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d4e8c-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d4e8c-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d4e8c-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-695">1OFMTH</span></span>
- <span data-ttu-id="d4e8c-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-696">LASTOFMTH</span></span>
- <span data-ttu-id="d4e8c-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-697">2OFMTH</span></span>
- <span data-ttu-id="d4e8c-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-698">3OFMTH</span></span>
- <span data-ttu-id="d4e8c-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-699">4OFMTH</span></span>
- <span data-ttu-id="d4e8c-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-700">5OFMTH</span></span>
- <span data-ttu-id="d4e8c-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-701">1N2OFMTH</span></span>
- <span data-ttu-id="d4e8c-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-702">3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-703">1N3OFMTH</span></span>
- <span data-ttu-id="d4e8c-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-704">1N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-705">2N3OFMTH</span></span>
- <span data-ttu-id="d4e8c-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-706">2N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="d4e8c-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4e8c-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d4e8c-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d4e8c-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d4e8c-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d4e8c-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d4e8c-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d4e8c-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d4e8c-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d4e8c-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4e8c-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d4e8c-719">Adressen</span><span class="sxs-lookup"><span data-stu-id="d4e8c-719">Addresses</span></span>

<span data-ttu-id="d4e8c-720">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d4e8c-721">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d4e8c-722">Human resources</span><span class="sxs-lookup"><span data-stu-id="d4e8c-722">Human Resources</span></span>              | <span data-ttu-id="d4e8c-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4e8c-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d4e8c-724">Land/regio</span><span class="sxs-lookup"><span data-stu-id="d4e8c-724">Country/Region</span></span>      | <span data-ttu-id="d4e8c-725">Landcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-725">Country Code</span></span>          |
| <span data-ttu-id="d4e8c-726">Postcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-726">Zip/Postal Code</span></span>     | <span data-ttu-id="d4e8c-727">Postcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-727">Postal Code</span></span>           |
| <span data-ttu-id="d4e8c-728">Provincie</span><span class="sxs-lookup"><span data-stu-id="d4e8c-728">State</span></span>               | <span data-ttu-id="d4e8c-729">Staatcode</span><span class="sxs-lookup"><span data-stu-id="d4e8c-729">State Code</span></span>            |
| <span data-ttu-id="d4e8c-730">Plaats</span><span class="sxs-lookup"><span data-stu-id="d4e8c-730">City</span></span>                | <span data-ttu-id="d4e8c-731">Plaats</span><span class="sxs-lookup"><span data-stu-id="d4e8c-731">City</span></span>                  |
| <span data-ttu-id="d4e8c-732">District</span><span class="sxs-lookup"><span data-stu-id="d4e8c-732">County</span></span>              | <span data-ttu-id="d4e8c-733">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="d4e8c-733">County (Municipality)</span></span> |
| <span data-ttu-id="d4e8c-734">Adres</span><span class="sxs-lookup"><span data-stu-id="d4e8c-734">Street</span></span>              | <span data-ttu-id="d4e8c-735">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="d4e8c-735">Address Line 1</span></span>        |
| <span data-ttu-id="d4e8c-736">Huisnummer</span><span class="sxs-lookup"><span data-stu-id="d4e8c-736">Street Number</span></span>       | <span data-ttu-id="d4e8c-737">Adresregel 2</span><span class="sxs-lookup"><span data-stu-id="d4e8c-737">Address Line 2</span></span>        |
| <span data-ttu-id="d4e8c-738">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="d4e8c-738">Building Complement</span></span> | <span data-ttu-id="d4e8c-739">Adresregel 5</span><span class="sxs-lookup"><span data-stu-id="d4e8c-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d4e8c-740">Paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d4e8c-740">Passport number</span></span>

<span data-ttu-id="d4e8c-741">Werknemers kunnen paspoortgegevens opgeven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-741">Employees can declare passport information.</span></span> <span data-ttu-id="d4e8c-742">Deze informatie is van het identificatietype **Paspoort** en wordt in Dayforce geïntegreerd als onderdeel van de Mexico-specifieke informatie van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d4e8c-743">Identificatietype = 'Paspoort'</span><span class="sxs-lookup"><span data-stu-id="d4e8c-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d4e8c-744">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-744">Issued Date</span></span>
- <span data-ttu-id="d4e8c-745">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d4e8c-745">Expiration Date</span></span>

<span data-ttu-id="d4e8c-746">Werknemers kunnen meerdere identificatienummers van het identificatietype **Paspoort** opgeven.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d4e8c-747">Echter alleen de huidige actieve paspoortvermelding wordt geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d4e8c-748">Als alle paspoortvermeldingen zijn verlopen, wordt het paspoort dat als laatste is uitgegeven geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d4e8c-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]