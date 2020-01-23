---
title: De integratie van de salarisadministratie tussen Talent en Dayforce configureren
description: In dit onderwerp wordt uitgelegd hoe de integratie tussen Microsoft Dynamics 365 Talent en Ceridian Dayforce wordt geconfigureerd zodat u een betaling kunt verwerken.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898524"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="f2099-103">De integratie van de salarisadministratie tussen Talent en Dayforce configureren</span><span class="sxs-lookup"><span data-stu-id="f2099-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="f2099-104">De integratie tussen Microsoft Dynamics 365 Talent en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen die in dit onderwerp worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="f2099-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="f2099-105">Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Talent als Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="f2099-106">Als u een service zoals Dayforce gebruikt voor het uitvoeren van betalingen, moet u de integratie inschakelen in Talent.</span><span class="sxs-lookup"><span data-stu-id="f2099-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="f2099-107">De integratie vereist specifieke gegevens vanuit Talent.</span><span class="sxs-lookup"><span data-stu-id="f2099-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="f2099-108">Daarom moet u controleren of gegevens die zijn toegewezen aan Dayforce zodanig in Talent zijn geconfigureerd dat de integratie wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f2099-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="f2099-109">De integratie maakt gebruik van de volgende brede categorieën gegevens:</span><span class="sxs-lookup"><span data-stu-id="f2099-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="f2099-110">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-110">Human resources data</span></span>
- <span data-ttu-id="f2099-111">Compensatiegegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-111">Compensation data</span></span>
- <span data-ttu-id="f2099-112">Salarisgegevens, zoals betalingscycli, salarisperioden en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="f2099-113">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-113">Worker data</span></span>

<span data-ttu-id="f2099-114">In dit onderwerp worden de stappen beschreven die u moet volgen om de integratie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="f2099-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="f2099-115">Ook wordt uitgelegd welke typen gegevens en welke configuratiedetails vereist zijn voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="f2099-116">De integratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="f2099-116">Enable the integration</span></span>

<span data-ttu-id="f2099-117">In Talent moet u de integratie inschakelen en de configuratiegegevens invoeren om verbinding te maken met Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="f2099-118">Als u wilt dat de grootboektransactie die wordt geproduceerd wordt geïmporteerd in Microsoft Dynamics 365 Finance, moet u ook een Microsoft Azure-opslagaccount instellen en de verbindingstekenreeks voor Azure Storage invoeren in Finance.</span><span class="sxs-lookup"><span data-stu-id="f2099-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="f2099-119">Voer de volgende stappen uit om de integratie in Talent in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="f2099-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="f2099-120">Ga naar de pagina **Systeembeheer** en selecteer **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="f2099-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="f2099-121">Voer het beveiligde FTP-eindpunt (File Transfer Protocol) en het pad naar de beveiligde FTP-map in.</span><span class="sxs-lookup"><span data-stu-id="f2099-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="f2099-122">Voer de gebruikersnaam en het wachtwoord in van de gebruiker die toegang krijgt tot het beveiligde FTP-eindpunt en het mappad.</span><span class="sxs-lookup"><span data-stu-id="f2099-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="f2099-123">Test de verbinding, zoals vereist, en stel de optie **Integratie van salarisadministratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f2099-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="f2099-124">Wanneer de integratie is ingeschakeld, worden het pakket voor gegevensexport en de bestanden gemaakt en wordt de frequentie ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f2099-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="f2099-125">U kunt deze frequentie naar behoefte wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f2099-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="f2099-126">Zie de volgende Azure-onderwerpen voor meer informatie over Azure-opslagaccounts en verbindingstekenreeksen voor Azure Storage:</span><span class="sxs-lookup"><span data-stu-id="f2099-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="f2099-127">Informatie over Azure-opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="f2099-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="f2099-128">Verbindingstekenreeks voor Azure Storage configureren</span><span class="sxs-lookup"><span data-stu-id="f2099-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="f2099-129">Technische details wanneer integratie van salarisadministratie is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="f2099-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="f2099-130">Het inschakelen van de integratie van de salarisadministratie heeft twee belangrijke effecten:</span><span class="sxs-lookup"><span data-stu-id="f2099-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="f2099-131">Er wordt een gegevensexportproject met de naam Export van integratie van salarisadministratie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f2099-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="f2099-132">Dit project bevat de entiteiten en velden die nodig zijn voor de integratie van de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="f2099-133">Als u het project wilt onderzoeken, gaat u naar **Systeembeheer**, selecteert u de tegel **Gegevensbeheer** en opent u het gegevensproject in de lijst met projecten.</span><span class="sxs-lookup"><span data-stu-id="f2099-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="f2099-134">Met deze batchtaak wordt het gegevensexportproject uitgevoerd, wordt het resulterende gegevenspakket gecodeerd en wordt het gegevenspakketbestand overgebracht naar het SFTP-eindpunt dat is geconfigureerd in het scherm **Configuratie van integratie**.</span><span class="sxs-lookup"><span data-stu-id="f2099-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="f2099-135">Het gegevenspakket dat naar het SFTP-eind punt wordt overgebracht, is gecodeerd met een sleutel die uniek is voor het pakket.</span><span class="sxs-lookup"><span data-stu-id="f2099-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="f2099-136">De sleutel bevindt zich in een Azure-sleutelkluis die alleen toegankelijk is via Ceridian.</span><span class="sxs-lookup"><span data-stu-id="f2099-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="f2099-137">Het is niet mogelijk om de inhoud van het gegevenspakket te decoderen en te onderzoeken.</span><span class="sxs-lookup"><span data-stu-id="f2099-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="f2099-138">Als u de inhoud van het gegevenspakket wilt controleren, moet u het gegevensproject Export van integratie van salarisadministratie handmatig exporteren, downloaden en vervolgens openen.</span><span class="sxs-lookup"><span data-stu-id="f2099-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="f2099-139">Bij een handmatige export wordt er geen codering toegepast of wordt het pakket niet overgedragen.</span><span class="sxs-lookup"><span data-stu-id="f2099-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="f2099-140">Uw gegevens configureren</span><span class="sxs-lookup"><span data-stu-id="f2099-140">Configure your data</span></span> 

<span data-ttu-id="f2099-141">Om salarissen te kunnen verwerken, moet u HRM-gegevens configureren in Talent.</span><span class="sxs-lookup"><span data-stu-id="f2099-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="f2099-142">U moet gegevens over de organisatie, zoals taken en functies, instellen samen met informatie over vergoedingen en compensatie.</span><span class="sxs-lookup"><span data-stu-id="f2099-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="f2099-143">Deze informatie biedt de informatie over dienstverband, salaris en inhoudingen die vereist is om het salaris van werknemers te genereren.</span><span class="sxs-lookup"><span data-stu-id="f2099-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="f2099-144">HRM-gegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="f2099-145">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="f2099-145">Benefits</span></span> 

<span data-ttu-id="f2099-146">Human resources biedt hulpmiddelen voor het instellen en onderhouden van de vergoedingen, inhoudingen en compensatieplannen van medewerkers die een organisatie zijn medewerkers biedt.</span><span class="sxs-lookup"><span data-stu-id="f2099-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="f2099-147">Wanneer u vergoedingen maakt, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="f2099-148">Vergoedingsplannen</span><span class="sxs-lookup"><span data-stu-id="f2099-148">Benefit plans</span></span>

- <span data-ttu-id="f2099-149">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-149">Plan (required)</span></span>
- <span data-ttu-id="f2099-150">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-150">Type (required)</span></span>
- <span data-ttu-id="f2099-151">Gevolgen voor salaris (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-151">Payroll impact (required)</span></span>
- <span data-ttu-id="f2099-152">Achterstallige betalingen herstellen</span><span class="sxs-lookup"><span data-stu-id="f2099-152">Recover arrears</span></span>
- <span data-ttu-id="f2099-153">Inhoudingsmethode</span><span class="sxs-lookup"><span data-stu-id="f2099-153">Deduction method</span></span>
- <span data-ttu-id="f2099-154">Inhoudingsprioriteit</span><span class="sxs-lookup"><span data-stu-id="f2099-154">Deduction priority</span></span>
- <span data-ttu-id="f2099-155">Limietperiode</span><span class="sxs-lookup"><span data-stu-id="f2099-155">Limit period</span></span>
- <span data-ttu-id="f2099-156">Bedrag beperken</span><span class="sxs-lookup"><span data-stu-id="f2099-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="f2099-157">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="f2099-157">Benefits</span></span>

- <span data-ttu-id="f2099-158">Plan (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-158">Plan (required)</span></span>
- <span data-ttu-id="f2099-159">Type (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-159">Type (required)</span></span>
- <span data-ttu-id="f2099-160">Optie (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-160">Option (required)</span></span>
- <span data-ttu-id="f2099-161">Vergoeding-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-161">Benefit ID (required)</span></span>
- <span data-ttu-id="f2099-162">Frequentie</span><span class="sxs-lookup"><span data-stu-id="f2099-162">Frequency</span></span>
- <span data-ttu-id="f2099-163">Basis</span><span class="sxs-lookup"><span data-stu-id="f2099-163">Basis</span></span>
- <span data-ttu-id="f2099-164">Bedrag of tarief</span><span class="sxs-lookup"><span data-stu-id="f2099-164">Amount or rate</span></span>
- <span data-ttu-id="f2099-165">Inkomstencode</span><span class="sxs-lookup"><span data-stu-id="f2099-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="f2099-166">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="f2099-166">Supported frequencies</span></span> 

- <span data-ttu-id="f2099-167">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="f2099-167">Weekly</span></span>
- <span data-ttu-id="f2099-168">Tweewekelijks</span><span class="sxs-lookup"><span data-stu-id="f2099-168">Bi-weekly</span></span>
- <span data-ttu-id="f2099-169">Halfmaandelijks</span><span class="sxs-lookup"><span data-stu-id="f2099-169">Semi-monthly</span></span>
- <span data-ttu-id="f2099-170">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="f2099-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="f2099-171">Ondersteund bases</span><span class="sxs-lookup"><span data-stu-id="f2099-171">Supported bases</span></span> 

- <span data-ttu-id="f2099-172">Vast bedrag</span><span class="sxs-lookup"><span data-stu-id="f2099-172">Fixed amount</span></span>
- <span data-ttu-id="f2099-173">Percentage van inkomsten</span><span class="sxs-lookup"><span data-stu-id="f2099-173">Percent of earnings</span></span>
- <span data-ttu-id="f2099-174">Productieve uren</span><span class="sxs-lookup"><span data-stu-id="f2099-174">Productive hours</span></span>

<span data-ttu-id="f2099-175">Dayforce maakt de volgende inhoudingen, op basis van de salarisgevolgen die zijn gedefinieerd voor het vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="f2099-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="f2099-176">Selectie in Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-176">Selection in Talent</span></span>        | <span data-ttu-id="f2099-177">Resultaat in Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f2099-178">None</span><span class="sxs-lookup"><span data-stu-id="f2099-178">None</span></span>                       | <span data-ttu-id="f2099-179">Er wordt geen inhouding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f2099-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="f2099-180">Alleen inhouding</span><span class="sxs-lookup"><span data-stu-id="f2099-180">Deduction only</span></span>             | <span data-ttu-id="f2099-181">Er wordt een inhouding voor de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f2099-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="f2099-182">Alleen bijdrage</span><span class="sxs-lookup"><span data-stu-id="f2099-182">Contribution only</span></span>          | <span data-ttu-id="f2099-183">Er wordt een inhouding voor de werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f2099-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="f2099-184">Inhouding en bijdrage</span><span class="sxs-lookup"><span data-stu-id="f2099-184">Deduction and contribution</span></span> | <span data-ttu-id="f2099-185">Er worden inhoudingen voor werknemer en werkgever gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f2099-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="f2099-186">Zie de volgende onderwerpen voor meer informatie over het definiëren en beheren van een vergoedingsprogramma:</span><span class="sxs-lookup"><span data-stu-id="f2099-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="f2099-187">Een vergoedingenprogramma voor werknemers maken</span><span class="sxs-lookup"><span data-stu-id="f2099-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="f2099-188">Een nieuwe vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="f2099-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="f2099-189">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="f2099-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="f2099-190">Vergoedingen inschrijven en verwijderen van medewerkers</span><span class="sxs-lookup"><span data-stu-id="f2099-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="f2099-191">Compensatie</span><span class="sxs-lookup"><span data-stu-id="f2099-191">Compensation</span></span> 

<span data-ttu-id="f2099-192">Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren.</span><span class="sxs-lookup"><span data-stu-id="f2099-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="f2099-193">Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd.</span><span class="sxs-lookup"><span data-stu-id="f2099-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="f2099-194">De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="f2099-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="f2099-195">Dayforce gebruikt compensatie-informatie voor het berekenen van het uur- of jaartarief van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="f2099-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="f2099-196">Er zijn vastecompensatieplannen en conversies van het loontarief vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="f2099-197">Werknemers moeten worden gekoppeld aan een vastecompensatieplan.</span><span class="sxs-lookup"><span data-stu-id="f2099-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="f2099-198">Zie de volgende onderwerpen voor meer informatie over compensatieplannen:</span><span class="sxs-lookup"><span data-stu-id="f2099-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="f2099-199">Plannen voor vaste compensatie maken</span><span class="sxs-lookup"><span data-stu-id="f2099-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="f2099-200">Plannen voor variabele compensatie maken</span><span class="sxs-lookup"><span data-stu-id="f2099-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="f2099-201">Salaris-/compensatiestructuur en -plannen ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="f2099-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="f2099-202">Compensatie verwerken</span><span class="sxs-lookup"><span data-stu-id="f2099-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="f2099-203">Compensatieproces definiëren en resultaten berekenen</span><span class="sxs-lookup"><span data-stu-id="f2099-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="f2099-204">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="f2099-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="f2099-205">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="f2099-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="f2099-206">Taken</span><span class="sxs-lookup"><span data-stu-id="f2099-206">Jobs</span></span> 

<span data-ttu-id="f2099-207">Een functie is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een functie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="f2099-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f2099-208">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="f2099-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2099-209">De onderdelen van een taak instellen</span><span class="sxs-lookup"><span data-stu-id="f2099-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="f2099-210">Nieuwe taken definiëren</span><span class="sxs-lookup"><span data-stu-id="f2099-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="f2099-211">Posities</span><span class="sxs-lookup"><span data-stu-id="f2099-211">Positions</span></span>

<span data-ttu-id="f2099-212">Een positie is een afzonderlijk exemplaar van een taak.</span><span class="sxs-lookup"><span data-stu-id="f2099-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="f2099-213">De positie 'Verkoopmanager (Oost)' is bijvoorbeeld een van de posities die zijn gekoppeld aan de functie 'Verkoopmanager'.</span><span class="sxs-lookup"><span data-stu-id="f2099-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="f2099-214">Een positie bestaat op een afdeling.</span><span class="sxs-lookup"><span data-stu-id="f2099-214">A position exists in a department.</span></span> <span data-ttu-id="f2099-215">Aan elke positie kan slechts één medewerker worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f2099-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="f2099-216">Let op de volgende gegevens en configuratie bij het instellen van posities:</span><span class="sxs-lookup"><span data-stu-id="f2099-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="f2099-217">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-217">Position (required)</span></span>
- <span data-ttu-id="f2099-218">Beschrijving (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-218">Description (required)</span></span>
- <span data-ttu-id="f2099-219">Functie (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-219">Job (required)</span></span>
- <span data-ttu-id="f2099-220">Afdeling (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-220">Department (required)</span></span>
- <span data-ttu-id="f2099-221">Positietype (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-221">Position type (required)</span></span>
- <span data-ttu-id="f2099-222">Voltijdse equivalent</span><span class="sxs-lookup"><span data-stu-id="f2099-222">Full-time equivalent</span></span>
- <span data-ttu-id="f2099-223">Jaarlijkse normale uren (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="f2099-224">Betaald door rechtspersoon (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="f2099-225">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-225">Pay cycle (required)</span></span>
- <span data-ttu-id="f2099-226">Standaard financiële dimensie: kostenplaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="f2099-227">Medewerkertoewijzing: medewerker, toewijzing begin, einde toewijzing, redencode</span><span class="sxs-lookup"><span data-stu-id="f2099-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="f2099-228">Als meerdere posities op dezelfde afdeling aan dezelfde functie zijn gekoppeld, worden deze geconsolideerd in een enkele positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="f2099-229">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="f2099-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2099-230">Uw werknemers organiseren met afdelingen, taken en posities</span><span class="sxs-lookup"><span data-stu-id="f2099-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="f2099-231">Posities instellen</span><span class="sxs-lookup"><span data-stu-id="f2099-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="f2099-232">Afdelingen</span><span class="sxs-lookup"><span data-stu-id="f2099-232">Departments</span></span>

<span data-ttu-id="f2099-233">Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt.</span><span class="sxs-lookup"><span data-stu-id="f2099-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="f2099-234">Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR.</span><span class="sxs-lookup"><span data-stu-id="f2099-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="f2099-235">U kunt afdelingen gebruiken om te rapporteren over functiegebieden.</span><span class="sxs-lookup"><span data-stu-id="f2099-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="f2099-236">Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.</span><span class="sxs-lookup"><span data-stu-id="f2099-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="f2099-237">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="f2099-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2099-238">Een afdeling maken en koppelen aan de afdelingshiërarchie</span><span class="sxs-lookup"><span data-stu-id="f2099-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="f2099-239">Nieuwe afdelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="f2099-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="f2099-240">Betalingscycli en salarisperioden</span><span class="sxs-lookup"><span data-stu-id="f2099-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="f2099-241">Een betalingscyclus bepaalt hoe vaak salarissen worden berekend en op welke specifieke dagen medewerkers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="f2099-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="f2099-242">Zo kan bijvooorbeeld een betalingscyclus maandelijks zijn en kunnen werknemers worden uitbetaald op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="f2099-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="f2099-243">Een betalingscyclus kan ook wekelijks en werknemers kunnen worden uitbetaald op de dinsdag na het einde van de salarisperiode.</span><span class="sxs-lookup"><span data-stu-id="f2099-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="f2099-244">Betalingscycli zijn toegewezen aan posities om te bepalen wanneer medewerkers in deze posities worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="f2099-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="f2099-245">Nadat u betalingscycli hebt gemaakt, kunt u salarisperioden voor elke cyclus genereren.</span><span class="sxs-lookup"><span data-stu-id="f2099-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="f2099-246">Elke salarisperiode bevat een standaard betalingsdatum die is gebaseerd op gegevens die u verstrekt.</span><span class="sxs-lookup"><span data-stu-id="f2099-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="f2099-247">U kunt echter de standaard betalingsdatum in een salarisperiode wijzigen om te voorzien in uitzonderingen, bijvoorbeeld wanneer de betalingsdatum op een feestdag valt.</span><span class="sxs-lookup"><span data-stu-id="f2099-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="f2099-248">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f2099-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f2099-249">Betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-249">Pay cycle (required)</span></span>
- <span data-ttu-id="f2099-250">Frequentie van betalingscyclus (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="f2099-251">Begindatum van periode (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="f2099-252">Standaardbetalingsdatum (eerste salarisperiode vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="f2099-253">Deze informatie is geïntegreerd met Dayforce als betalingsgroepen en worden gescheiden per land of regio voor elke betalingscyclus.</span><span class="sxs-lookup"><span data-stu-id="f2099-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="f2099-254">Vóór integratie moet ten minste één salarisperiode worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="f2099-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="f2099-255">Dayforce genereert van betalingsgroepkalenders en betalingsdatums, op basis van de begindatum van de eerste salarisperiode en de standaardbetalingsdatum die is ingesteld in Talent.</span><span class="sxs-lookup"><span data-stu-id="f2099-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="f2099-256">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-256">Earning codes</span></span>

<span data-ttu-id="f2099-257">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="f2099-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2099-258">De codes hebben verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="f2099-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="f2099-259">De volgende informatie wordt gebruikt in Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f2099-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f2099-260">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-260">Earning Code (required)</span></span>
- <span data-ttu-id="f2099-261">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-261">Description</span></span>
- <span data-ttu-id="f2099-262">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="f2099-262">Unit of measure</span></span>
- <span data-ttu-id="f2099-263">Productief</span><span class="sxs-lookup"><span data-stu-id="f2099-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="f2099-264">Medewerkergegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-264">Worker data</span></span>

<span data-ttu-id="f2099-265">Records voor de verschillende soorten medewerkers die u hebt zijn belangrijk voor uw HRM- en salarisadministratiesystemen.</span><span class="sxs-lookup"><span data-stu-id="f2099-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="f2099-266">De gegevens die u invoert, kunnen worden gebruikt om medewerkers en persoonlijke gegevens bij te houden.</span><span class="sxs-lookup"><span data-stu-id="f2099-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="f2099-267">U kunt de volgende informatie bijhouden voor medewerkers:</span><span class="sxs-lookup"><span data-stu-id="f2099-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="f2099-268">**Basis** – Basisinformatie over een medewerker bijhouden, zoals contactgegevens, demografische gegevens, identificatiegegevens, informatie over de familie, status van militaire dienst, expat-informatie en contactpersonen voor noodgevallen.</span><span class="sxs-lookup"><span data-stu-id="f2099-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="f2099-269">**Dienstverband** – Informatie bijhouden over werkgelegenheid van een medewerker, zoals een aansluiting met een bedrijf of organisatie, functie, start- en einddatums, arbeidsgeschiktheid, arbeidsvoorwaarden, pensioen, verlof en relocatie-informatie.</span><span class="sxs-lookup"><span data-stu-id="f2099-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="f2099-270">**Verlof en verzuim** – Informatie bijhouden over de afwezigheid van een medewerker, zoals werkkalenders, verzuimtransacties en verzuiminstellingen.</span><span class="sxs-lookup"><span data-stu-id="f2099-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="f2099-271">**Vergoedingen en salarissen** – Informatie bijhouden over compensatieplannen en salarisgegevens van een medewerker zoals inschrijving op plan, onderscheidingen, commissie, fiscale informatie, pensioen en salarisinhoudingen.</span><span class="sxs-lookup"><span data-stu-id="f2099-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="f2099-272">Wanneer u informatie over een werknemer invoert, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="f2099-273">Algemene informatie</span><span class="sxs-lookup"><span data-stu-id="f2099-273">General information</span></span>

- <span data-ttu-id="f2099-274">Personeelsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-274">Personnel number (required)</span></span>
- <span data-ttu-id="f2099-275">Voornaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-275">First name (required)</span></span>
- <span data-ttu-id="f2099-276">Achternaam (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-276">Last name (required)</span></span>
- <span data-ttu-id="f2099-277">Tweede naam</span><span class="sxs-lookup"><span data-stu-id="f2099-277">Middle name</span></span>
- <span data-ttu-id="f2099-278">Anciënniteitsdatum</span><span class="sxs-lookup"><span data-stu-id="f2099-278">Seniority date</span></span>
- <span data-ttu-id="f2099-279">Bekend als</span><span class="sxs-lookup"><span data-stu-id="f2099-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="f2099-280">Persoonlijke informatie</span><span class="sxs-lookup"><span data-stu-id="f2099-280">Personal information</span></span>

- <span data-ttu-id="f2099-281">Burgerlijke staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-281">Marital status (required)</span></span>
- <span data-ttu-id="f2099-282">Geboortedatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-282">Birth date (required)</span></span>
- <span data-ttu-id="f2099-283">Geslacht (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-283">Gender (required)</span></span>
- <span data-ttu-id="f2099-284">Persoon met handicap</span><span class="sxs-lookup"><span data-stu-id="f2099-284">Person with disabilities</span></span>
- <span data-ttu-id="f2099-285">Land/regio nationaliteit (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="f2099-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="f2099-286">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-286">Address information</span></span>

- <span data-ttu-id="f2099-287">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-287">Primary (required)</span></span>
- <span data-ttu-id="f2099-288">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-288">Country/region (required)</span></span>
- <span data-ttu-id="f2099-289">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-289">Postal code (required)</span></span>
- <span data-ttu-id="f2099-290">Huisnummer (vereist) (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="f2099-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="f2099-291">Gebouwtoevoeging (alleen voor Mexico)</span><span class="sxs-lookup"><span data-stu-id="f2099-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="f2099-292">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-292">City (required)</span></span>
- <span data-ttu-id="f2099-293">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-293">State (required)</span></span>
- <span data-ttu-id="f2099-294">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="f2099-295">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="f2099-295">Contact information</span></span> 

- <span data-ttu-id="f2099-296">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-296">Primary (required)</span></span>
- <span data-ttu-id="f2099-297">Contactnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-297">Contact number (required)</span></span>
- <span data-ttu-id="f2099-298">Toestel</span><span class="sxs-lookup"><span data-stu-id="f2099-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="f2099-299">Salarisinformatie en inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-299">Payroll information and earning codes</span></span>

<span data-ttu-id="f2099-300">Aan werknemers kunnen bepaalde inkomsten met een bepaalde betalingsfrequentie worden toegewezen en zij kunnen een geprefereerde betalingsmethode hebben.</span><span class="sxs-lookup"><span data-stu-id="f2099-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="f2099-301">De volgende velden worden gebruikt in Dayforce om te garanderen dat deze voorkeuren en instellingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f2099-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="f2099-302">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-302">Earning codes</span></span>

- <span data-ttu-id="f2099-303">Positie (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-303">Position (required)</span></span>
- <span data-ttu-id="f2099-304">Inkomstencode (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-304">Earning Code (required)</span></span>
- <span data-ttu-id="f2099-305">Frequentie (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-305">Frequency (required)</span></span>
- <span data-ttu-id="f2099-306">Bedrag (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="f2099-307">Salarisinformatie</span><span class="sxs-lookup"><span data-stu-id="f2099-307">Payroll information</span></span>

- <span data-ttu-id="f2099-308">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="f2099-308">Payment Method</span></span>
- <span data-ttu-id="f2099-309">Economische regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-309">Economic Region (required)</span></span>
- <span data-ttu-id="f2099-310">Id personeelsvergoedingen</span><span class="sxs-lookup"><span data-stu-id="f2099-310">Employee Benefits ID</span></span>
- <span data-ttu-id="f2099-311">Nationaal id-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-311">National ID Number (required)</span></span>
- <span data-ttu-id="f2099-312">Nummer militaire dienst</span><span class="sxs-lookup"><span data-stu-id="f2099-312">Military Service Number</span></span>
- <span data-ttu-id="f2099-313">Ploeg-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-313">Shift ID (required)</span></span>
- <span data-ttu-id="f2099-314">Btw-nummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-314">Tax Number (required)</span></span>
- <span data-ttu-id="f2099-315">Vakbond-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-315">Union ID (required)</span></span>
- <span data-ttu-id="f2099-316">Werkdag-id (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-316">Work Day ID (required)</span></span>
- <span data-ttu-id="f2099-317">Nummer werkvergunning</span><span class="sxs-lookup"><span data-stu-id="f2099-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="f2099-318">Voor de betalingsmethode ondersteunt Mexico **Contant geld**, **Cheque** (de fysieke cheque van het bedrijf) en **Elektronische betaling**.</span><span class="sxs-lookup"><span data-stu-id="f2099-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="f2099-319">Als geen betalingsmethode is opgegeven, wordt standaard **Cheque** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f2099-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="f2099-320">Details dienstverband</span><span class="sxs-lookup"><span data-stu-id="f2099-320">Employment details</span></span>

<span data-ttu-id="f2099-321">Historische gegevens over het dienstverband worden gebruikt als belangrijkste informatie voor het opvragen van de statussen voor aanstellen, ontslaan en opnieuw aanstellen van een werknemer in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="f2099-322">Dayforce ondersteunt slechts één actieve dienstverbandrecord tegelijk.</span><span class="sxs-lookup"><span data-stu-id="f2099-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="f2099-323">Begindatum dienstverband (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-323">Employment start date (required)</span></span>
- <span data-ttu-id="f2099-324">Einddatum dienstverband</span><span class="sxs-lookup"><span data-stu-id="f2099-324">Employment end date</span></span>
- <span data-ttu-id="f2099-325">Begindatum</span><span class="sxs-lookup"><span data-stu-id="f2099-325">Start date</span></span>
- <span data-ttu-id="f2099-326">Aangepaste begindatum</span><span class="sxs-lookup"><span data-stu-id="f2099-326">Adjusted start date</span></span>
- <span data-ttu-id="f2099-327">Ontslagdatum (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="f2099-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="f2099-328">Ontslagreden (vereist bij ontslag)</span><span class="sxs-lookup"><span data-stu-id="f2099-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="f2099-329">De belangrijkste datums van een werknemer worden afgeleid met behulp van de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="f2099-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="f2099-330">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-330">Talent</span></span>                | <span data-ttu-id="f2099-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2099-332">Meest recente huurdatum</span><span class="sxs-lookup"><span data-stu-id="f2099-332">Most recent hire date</span></span> | <span data-ttu-id="f2099-333">Begindatum van dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="f2099-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f2099-334">Ontslagdatum</span><span class="sxs-lookup"><span data-stu-id="f2099-334">Termination date</span></span>      | <span data-ttu-id="f2099-335">Ontslagdatum van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="f2099-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f2099-336">Begindatum</span><span class="sxs-lookup"><span data-stu-id="f2099-336">Start date</span></span>            | <span data-ttu-id="f2099-337">Aangepaste begindatum, begindatum of begindatum dienstverband van historierecord van huidig niet-beëindigd dienstverband</span><span class="sxs-lookup"><span data-stu-id="f2099-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="f2099-338">Oorspronkelijke datum indiensttreding</span><span class="sxs-lookup"><span data-stu-id="f2099-338">Original hire date</span></span>    | <span data-ttu-id="f2099-339">Begindatum dienstverband van vroegste historierecord van dienstverband</span><span class="sxs-lookup"><span data-stu-id="f2099-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="f2099-340">Compensatie</span><span class="sxs-lookup"><span data-stu-id="f2099-340">Compensation</span></span>

<span data-ttu-id="f2099-341">Een vastecompensatieplan moet worden gekoppeld aan de primaire functie van elke werknemer tijdens de hele duur van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="f2099-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="f2099-342">Deze periode begint op de datum waarop de werknemer in dienst is genomen (of de begindatum van het dienstverband) en gaat door totdat aan het ontslag.</span><span class="sxs-lookup"><span data-stu-id="f2099-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="f2099-343">Ingangsdatum (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-343">Effective Date (required)</span></span>
- <span data-ttu-id="f2099-344">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f2099-344">Expiration date</span></span>
- <span data-ttu-id="f2099-345">Loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-345">Pay Rate (required)</span></span>
- <span data-ttu-id="f2099-346">Conversies van loontarief (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="f2099-347">Jaarlijks equivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="f2099-348">Uurequivalent (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="f2099-349">Als een werknemer met uurtarief meerdere posities heeft, wordt de vaste compensatie van de primaire positie geïmporteerd in Dayforce als het basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="f2099-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="f2099-350">Voor niet-primaire posities, wordt het uurtarief opgeslagen bij de overeenkomende positie in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="f2099-351">Als een medewerker met een salaris meerdere posities heeft, worden het cumulatieve uurtarief en het jaarsalaris voor alle actieve posities afgeleid en gebruikt als de basistarief/-salaris op werknemerniveau.</span><span class="sxs-lookup"><span data-stu-id="f2099-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="f2099-352">Identificatienummers</span><span class="sxs-lookup"><span data-stu-id="f2099-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="f2099-353">Sociaal-fiscaal nummer</span><span class="sxs-lookup"><span data-stu-id="f2099-353">Social Security identifier</span></span> 

<span data-ttu-id="f2099-354">Elke werknemer moet één primaire id hebben.</span><span class="sxs-lookup"><span data-stu-id="f2099-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="f2099-355">Deze id moet van het identificatietype **Sofinummer** zijn.</span><span class="sxs-lookup"><span data-stu-id="f2099-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="f2099-356">In Dayforce, wordt dit automatisch afgeleid als het sociaal-fiscaal nummer van de werknemer dat is vereist voor aanstelling.</span><span class="sxs-lookup"><span data-stu-id="f2099-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="f2099-357">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-357">Primary (required)</span></span>
- <span data-ttu-id="f2099-358">Identificatietype = 'Sofinummer'</span><span class="sxs-lookup"><span data-stu-id="f2099-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="f2099-359">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="f2099-359">Issued Date</span></span>
- <span data-ttu-id="f2099-360">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f2099-360">Expiration Date</span></span>

<span data-ttu-id="f2099-361">Werknemers kunnen meerdere identificatienummers van het identificatietype **Sofinummer** opgeven.</span><span class="sxs-lookup"><span data-stu-id="f2099-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="f2099-362">Alleen de record die is gemarkeerd als **Primair** wordt echter opgenomen in Dayforce, ongeacht of het nummer actief of verlopen is.</span><span class="sxs-lookup"><span data-stu-id="f2099-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="f2099-363">Bankrekeningen en voorschotten</span><span class="sxs-lookup"><span data-stu-id="f2099-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="f2099-364">Er moet geldige bankrekeninginformatie worden ingevoerd voor elke werknemer die wil worden uitbetaald via bankrekeningoverboekingen.</span><span class="sxs-lookup"><span data-stu-id="f2099-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="f2099-365">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-365">Talent</span></span>                         | <span data-ttu-id="f2099-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2099-367">Bankrekeningnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="f2099-368">SWIFT-code (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-368">SWIFT code (required)</span></span>          | <span data-ttu-id="f2099-369">Veld **Bank-id** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="f2099-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="f2099-370">Vestigingsnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="f2099-371">Bankrekeningtype (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-371">Bank account type (required)</span></span>   | <span data-ttu-id="f2099-372">Veld **Rekeningtype** dat wordt gebruikt bij het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="f2099-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="f2099-373">Ondersteunde waarden zijn **Rekening-courant** en **Salaris**.</span><span class="sxs-lookup"><span data-stu-id="f2099-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="f2099-374">Werknemers die ervoor kiezen om te worden uitbetaald via bankrekeningoverboekingen moeten een koppeling opgeven naar een restantrekening die zich onder een rechtspersoon bevindt met het primaire adres in Mexico en die is gekoppeld aan een geldige bankrekening van een Mexicaanse bank.</span><span class="sxs-lookup"><span data-stu-id="f2099-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="f2099-375">Alle andere niet-restantrekeningen worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="f2099-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="f2099-376">Adresgegevens</span><span class="sxs-lookup"><span data-stu-id="f2099-376">Address information</span></span>

<span data-ttu-id="f2099-377">Elke werknemer moet één primaire locatie hebben.</span><span class="sxs-lookup"><span data-stu-id="f2099-377">Every employee must have one primary location.</span></span> <span data-ttu-id="f2099-378">In Dayforce wordt deze locatie gebruikt om de primaire woonplaats van de werknemer te bepalen voor belastingdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="f2099-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="f2099-379">Primair (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-379">Primary (required)</span></span>
- <span data-ttu-id="f2099-380">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-380">Country/region (required)</span></span>
- <span data-ttu-id="f2099-381">Postcode (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="f2099-382">Straat (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-382">Street (required)</span></span>
- <span data-ttu-id="f2099-383">Huisnummer (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-383">Street Number (required)</span></span>
- <span data-ttu-id="f2099-384">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="f2099-384">Building Complement</span></span>
- <span data-ttu-id="f2099-385">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-385">City (required)</span></span>
- <span data-ttu-id="f2099-386">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-386">State (required)</span></span>
- <span data-ttu-id="f2099-387">District (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="f2099-388">Uw gegevens configureren voor het genereren van salarissen in de Verenigde Staten en Canada</span><span class="sxs-lookup"><span data-stu-id="f2099-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="f2099-389">Als u salarissen genereert voor werknemers in de Verenigde Staten en Canada, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="f2099-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="f2099-390">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="f2099-390">Departments are required on positions.</span></span>
- <span data-ttu-id="f2099-391">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="f2099-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="f2099-392">U kunt Talent zo configureren dat wordt vereist dat met posities een afdeling wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="f2099-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="f2099-393">Hiertoe gaat u naar **Gedeelde Human Resources-posities > Posities > Afdelingen voor posities vereisen**.</span><span class="sxs-lookup"><span data-stu-id="f2099-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="f2099-394">Het wordt aanbevolen deze instelling af te dwingen voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="f2099-395">Functietypen</span><span class="sxs-lookup"><span data-stu-id="f2099-395">Job types</span></span>

<span data-ttu-id="f2099-396">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="f2099-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f2099-397">Functietypen zijn vereist voor het verwerken van salarissen in de Verenigde Staten en Canada.</span><span class="sxs-lookup"><span data-stu-id="f2099-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="f2099-398">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="f2099-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f2099-399">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="f2099-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f2099-400">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f2099-401">Functietype</span><span class="sxs-lookup"><span data-stu-id="f2099-401">Job type</span></span>   | <span data-ttu-id="f2099-402">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f2099-403">Per uur</span><span class="sxs-lookup"><span data-stu-id="f2099-403">Hourly</span></span>     | <span data-ttu-id="f2099-404">Per uur</span><span class="sxs-lookup"><span data-stu-id="f2099-404">Hourly</span></span>      |
| <span data-ttu-id="f2099-405">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="f2099-405">Salaried</span></span>   | <span data-ttu-id="f2099-406">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="f2099-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="f2099-407">Positietypen</span><span class="sxs-lookup"><span data-stu-id="f2099-407">Position types</span></span> 

<span data-ttu-id="f2099-408">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="f2099-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f2099-409">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="f2099-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f2099-410">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f2099-411">Positietype</span><span class="sxs-lookup"><span data-stu-id="f2099-411">Position type</span></span>   | <span data-ttu-id="f2099-412">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f2099-413">Voltijd</span><span class="sxs-lookup"><span data-stu-id="f2099-413">Full-time</span></span>       | <span data-ttu-id="f2099-414">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="f2099-414">Full time employee</span></span> |
| <span data-ttu-id="f2099-415">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="f2099-415">Part-time</span></span>       | <span data-ttu-id="f2099-416">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="f2099-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f2099-417">Redencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-417">Reason codes</span></span>

<span data-ttu-id="f2099-418">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="f2099-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f2099-419">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="f2099-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f2099-420">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f2099-421">Redencode</span><span class="sxs-lookup"><span data-stu-id="f2099-421">Reason code</span></span>    | <span data-ttu-id="f2099-422">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-422">Description</span></span>      | <span data-ttu-id="f2099-423">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="f2099-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="f2099-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f2099-424">RESIGNATION</span></span>    | <span data-ttu-id="f2099-425">Ontslag</span><span class="sxs-lookup"><span data-stu-id="f2099-425">Resignation</span></span>      | <span data-ttu-id="f2099-426">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-426">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f2099-427">TERMINATION</span></span>    | <span data-ttu-id="f2099-428">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="f2099-428">Termination</span></span>      | <span data-ttu-id="f2099-429">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-429">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f2099-430">RETIREMENT</span></span>     | <span data-ttu-id="f2099-431">Pensionering</span><span class="sxs-lookup"><span data-stu-id="f2099-431">Retirement</span></span>       | <span data-ttu-id="f2099-432">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-432">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-433">OTHER</span><span class="sxs-lookup"><span data-stu-id="f2099-433">OTHER</span></span>          | <span data-ttu-id="f2099-434">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="f2099-434">Other Reasons</span></span>    | <span data-ttu-id="f2099-435">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-435">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="f2099-436">DEATH</span></span>          | <span data-ttu-id="f2099-437">Overlijden</span><span class="sxs-lookup"><span data-stu-id="f2099-437">Death</span></span>            | <span data-ttu-id="f2099-438">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-438">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f2099-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="f2099-440">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="f2099-440">Leave of Absence</span></span> | <span data-ttu-id="f2099-441">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-441">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f2099-442">CONTRACTEND</span></span>    | <span data-ttu-id="f2099-443">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="f2099-443">End of Contract</span></span>  | <span data-ttu-id="f2099-444">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-444">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2099-445">SALARYCHANGE</span></span>   | <span data-ttu-id="f2099-446">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="f2099-446">Change of Salary</span></span> | <span data-ttu-id="f2099-447">Compensatie</span><span class="sxs-lookup"><span data-stu-id="f2099-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="f2099-448">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="f2099-448">Marital status</span></span>

<span data-ttu-id="f2099-449">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2099-450">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2099-451">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-451">Talent</span></span>                 | <span data-ttu-id="f2099-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="f2099-453">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="f2099-453">Married</span></span>                | <span data-ttu-id="f2099-454">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="f2099-454">Married</span></span>              |
| <span data-ttu-id="f2099-455">Eén</span><span class="sxs-lookup"><span data-stu-id="f2099-455">Single</span></span>                 | <span data-ttu-id="f2099-456">Eén</span><span class="sxs-lookup"><span data-stu-id="f2099-456">Single</span></span>               |
| <span data-ttu-id="f2099-457">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="f2099-457">Widowed</span></span>                | <span data-ttu-id="f2099-458">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="f2099-458">Widowed</span></span>              |
| <span data-ttu-id="f2099-459">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="f2099-459">Divorced</span></span>               | <span data-ttu-id="f2099-460">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="f2099-460">Divorced</span></span>             |
| <span data-ttu-id="f2099-461">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="f2099-461">Registered Partnership</span></span> | <span data-ttu-id="f2099-462">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="f2099-462">Domestic Partnership</span></span> |
| <span data-ttu-id="f2099-463">None</span><span class="sxs-lookup"><span data-stu-id="f2099-463">None</span></span>                   | <span data-ttu-id="f2099-464">None</span><span class="sxs-lookup"><span data-stu-id="f2099-464">None</span></span>                 |
| <span data-ttu-id="f2099-465">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="f2099-465">Cohabiting</span></span>             | <span data-ttu-id="f2099-466">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="f2099-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="f2099-467">Geslacht</span><span class="sxs-lookup"><span data-stu-id="f2099-467">Gender</span></span>

<span data-ttu-id="f2099-468">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2099-469">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2099-470">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-470">Talent</span></span>       | <span data-ttu-id="f2099-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="f2099-472">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-472">Male</span></span>         | <span data-ttu-id="f2099-473">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-473">Male</span></span>            |
| <span data-ttu-id="f2099-474">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-474">Female</span></span>       | <span data-ttu-id="f2099-475">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-475">Female</span></span>          |
| <span data-ttu-id="f2099-476">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="f2099-476">Non-specific</span></span> | <span data-ttu-id="f2099-477">*Niet ondersteund*</span><span class="sxs-lookup"><span data-stu-id="f2099-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f2099-478">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-478">Earning codes</span></span>

<span data-ttu-id="f2099-479">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="f2099-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2099-480">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="f2099-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f2099-481">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="f2099-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f2099-482">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="f2099-482">Supported frequencies</span></span>

- <span data-ttu-id="f2099-483">Alles</span><span class="sxs-lookup"><span data-stu-id="f2099-483">All</span></span>
- <span data-ttu-id="f2099-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f2099-484">EVERYPAY</span></span>
- <span data-ttu-id="f2099-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f2099-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f2099-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f2099-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f2099-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f2099-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f2099-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-488">1OFMTH</span></span>
- <span data-ttu-id="f2099-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-489">LASTOFMTH</span></span>
- <span data-ttu-id="f2099-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-490">2OFMTH</span></span>
- <span data-ttu-id="f2099-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-491">3OFMTH</span></span>
- <span data-ttu-id="f2099-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-492">4OFMTH</span></span>
- <span data-ttu-id="f2099-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-493">5OFMTH</span></span>
- <span data-ttu-id="f2099-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-494">1N2OFMTH</span></span>
- <span data-ttu-id="f2099-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-495">3N4OFMTH</span></span>
- <span data-ttu-id="f2099-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-496">1N3OFMTH</span></span>
- <span data-ttu-id="f2099-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-497">1N4OFMTH</span></span>
- <span data-ttu-id="f2099-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-498">2N3OFMTH</span></span>
- <span data-ttu-id="f2099-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-499">2N4OFMTH</span></span>
- <span data-ttu-id="f2099-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="f2099-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="f2099-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="f2099-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="f2099-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f2099-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f2099-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f2099-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f2099-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f2099-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2099-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f2099-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2099-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f2099-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2099-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f2099-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2099-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f2099-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2099-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f2099-512">Adressen</span><span class="sxs-lookup"><span data-stu-id="f2099-512">Addresses</span></span>

<span data-ttu-id="f2099-513">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="f2099-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f2099-514">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="f2099-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f2099-515">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-515">Talent</span></span>          | <span data-ttu-id="f2099-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="f2099-517">Land/regio</span><span class="sxs-lookup"><span data-stu-id="f2099-517">Country/Region</span></span>  | <span data-ttu-id="f2099-518">Landcode</span><span class="sxs-lookup"><span data-stu-id="f2099-518">Country Code</span></span>          |
| <span data-ttu-id="f2099-519">Postcode</span><span class="sxs-lookup"><span data-stu-id="f2099-519">Zip/Postal Code</span></span> | <span data-ttu-id="f2099-520">Postcode</span><span class="sxs-lookup"><span data-stu-id="f2099-520">Postal Code</span></span>           |
| <span data-ttu-id="f2099-521">Provincie</span><span class="sxs-lookup"><span data-stu-id="f2099-521">State</span></span>           | <span data-ttu-id="f2099-522">Staatcode</span><span class="sxs-lookup"><span data-stu-id="f2099-522">State Code</span></span>            |
| <span data-ttu-id="f2099-523">Plaats</span><span class="sxs-lookup"><span data-stu-id="f2099-523">City</span></span>            | <span data-ttu-id="f2099-524">Plaats</span><span class="sxs-lookup"><span data-stu-id="f2099-524">City</span></span>                  |
| <span data-ttu-id="f2099-525">District</span><span class="sxs-lookup"><span data-stu-id="f2099-525">County</span></span>          | <span data-ttu-id="f2099-526">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="f2099-526">County (Municipality)</span></span> |
| <span data-ttu-id="f2099-527">Adres</span><span class="sxs-lookup"><span data-stu-id="f2099-527">Street</span></span>          | <span data-ttu-id="f2099-528">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="f2099-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="f2099-529">Belastingregio's</span><span class="sxs-lookup"><span data-stu-id="f2099-529">Tax regions</span></span>

<span data-ttu-id="f2099-530">Belastingregio's worden gebruikt om de juiste belasting te bepalen die moet worden gebruikt bij het genereren van salarissen.</span><span class="sxs-lookup"><span data-stu-id="f2099-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="f2099-531">Belastingregio's worden aan Dayforce toegewezen als locatieadressen.</span><span class="sxs-lookup"><span data-stu-id="f2099-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="f2099-532">De standaardbelastingregio moet aan de actieve positie van de werknemer worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f2099-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="f2099-533">Belastingregio (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-533">Tax region (required)</span></span>
- <span data-ttu-id="f2099-534">Land/regio (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-534">Country/Region (required)</span></span>
- <span data-ttu-id="f2099-535">Staat (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-535">State (required)</span></span>
- <span data-ttu-id="f2099-536">District</span><span class="sxs-lookup"><span data-stu-id="f2099-536">County</span></span> 
- <span data-ttu-id="f2099-537">Plaats (vereist)</span><span class="sxs-lookup"><span data-stu-id="f2099-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="f2099-538">Uw gegevens configureren voor het genereren van salarissen in Mexico</span><span class="sxs-lookup"><span data-stu-id="f2099-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="f2099-539">Als u salarissen genereert voor werknemers in Mexico, moeten de volgende elementen worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="f2099-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="f2099-540">Afdelingen zijn vereist voor posities.</span><span class="sxs-lookup"><span data-stu-id="f2099-540">Departments are required on positions.</span></span>
- <span data-ttu-id="f2099-541">Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.</span><span class="sxs-lookup"><span data-stu-id="f2099-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="f2099-542">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="f2099-542">Job types</span></span>

<span data-ttu-id="f2099-543">Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen.</span><span class="sxs-lookup"><span data-stu-id="f2099-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f2099-544">Functietypen zijn vereist voor het verwerken van salarissen in Mexico.</span><span class="sxs-lookup"><span data-stu-id="f2099-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="f2099-545">Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief.</span><span class="sxs-lookup"><span data-stu-id="f2099-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f2099-546">Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.</span><span class="sxs-lookup"><span data-stu-id="f2099-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f2099-547">De volgende functietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f2099-548">Functietype</span><span class="sxs-lookup"><span data-stu-id="f2099-548">Job type</span></span>   | <span data-ttu-id="f2099-549">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f2099-550">Per uur</span><span class="sxs-lookup"><span data-stu-id="f2099-550">Hourly</span></span>     | <span data-ttu-id="f2099-551">MX Per uur</span><span class="sxs-lookup"><span data-stu-id="f2099-551">MX Hourly</span></span>   |
| <span data-ttu-id="f2099-552">Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="f2099-552">Salaried</span></span>   | <span data-ttu-id="f2099-553">MX Bezoldigd</span><span class="sxs-lookup"><span data-stu-id="f2099-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="f2099-554">Positietypen</span><span class="sxs-lookup"><span data-stu-id="f2099-554">Position types</span></span> 

<span data-ttu-id="f2099-555">U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is.</span><span class="sxs-lookup"><span data-stu-id="f2099-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f2099-556">Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.</span><span class="sxs-lookup"><span data-stu-id="f2099-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f2099-557">De volgende positietypen en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f2099-558">Positietype</span><span class="sxs-lookup"><span data-stu-id="f2099-558">Position type</span></span>   | <span data-ttu-id="f2099-559">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f2099-560">Voltijd</span><span class="sxs-lookup"><span data-stu-id="f2099-560">Full-time</span></span>       | <span data-ttu-id="f2099-561">Voltijdse werknemer</span><span class="sxs-lookup"><span data-stu-id="f2099-561">Full time employee</span></span> |
| <span data-ttu-id="f2099-562">Deeltijd</span><span class="sxs-lookup"><span data-stu-id="f2099-562">Part-time</span></span>       | <span data-ttu-id="f2099-563">Werknemer in deeltijd</span><span class="sxs-lookup"><span data-stu-id="f2099-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f2099-564">Redencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-564">Reason codes</span></span>

<span data-ttu-id="f2099-565">Redencodes bieden informatie over de status van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="f2099-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f2099-566">Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.</span><span class="sxs-lookup"><span data-stu-id="f2099-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f2099-567">De volgende redencodes en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f2099-568">Redencode</span><span class="sxs-lookup"><span data-stu-id="f2099-568">Reason code</span></span>            | <span data-ttu-id="f2099-569">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-569">Description</span></span>                    | <span data-ttu-id="f2099-570">Toepasselijke scenario's</span><span class="sxs-lookup"><span data-stu-id="f2099-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="f2099-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="f2099-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="f2099-572">Vertrek voor eerste salaris</span><span class="sxs-lookup"><span data-stu-id="f2099-572">Departure before first payroll</span></span> | <span data-ttu-id="f2099-573">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-573">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f2099-574">RESIGNATION</span></span>            | <span data-ttu-id="f2099-575">Ontslag</span><span class="sxs-lookup"><span data-stu-id="f2099-575">Resignation</span></span>                    | <span data-ttu-id="f2099-576">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-576">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="f2099-577">PENSION</span></span>                | <span data-ttu-id="f2099-578">Pensioen</span><span class="sxs-lookup"><span data-stu-id="f2099-578">Pension</span></span>                        | <span data-ttu-id="f2099-579">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-579">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f2099-580">TERMINATION</span></span>            | <span data-ttu-id="f2099-581">Beëindiging</span><span class="sxs-lookup"><span data-stu-id="f2099-581">Termination</span></span>                    | <span data-ttu-id="f2099-582">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-582">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f2099-583">RETIREMENT</span></span>             | <span data-ttu-id="f2099-584">Pensionering</span><span class="sxs-lookup"><span data-stu-id="f2099-584">Retirement</span></span>                     | <span data-ttu-id="f2099-585">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-585">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="f2099-586">ABSENTEE</span></span>               | <span data-ttu-id="f2099-587">Verzuim</span><span class="sxs-lookup"><span data-stu-id="f2099-587">Absentee</span></span>                       | <span data-ttu-id="f2099-588">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-588">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-589">OTHER</span><span class="sxs-lookup"><span data-stu-id="f2099-589">OTHER</span></span>                  | <span data-ttu-id="f2099-590">Andere redenen</span><span class="sxs-lookup"><span data-stu-id="f2099-590">Other Reasons</span></span>                  | <span data-ttu-id="f2099-591">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-591">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="f2099-592">CLOSURE</span></span>                | <span data-ttu-id="f2099-593">Bedrijfssluiting</span><span class="sxs-lookup"><span data-stu-id="f2099-593">Business Closure</span></span>               | <span data-ttu-id="f2099-594">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-594">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="f2099-595">DEATH</span></span>                  | <span data-ttu-id="f2099-596">Overlijden</span><span class="sxs-lookup"><span data-stu-id="f2099-596">Death</span></span>                          | <span data-ttu-id="f2099-597">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-597">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f2099-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="f2099-599">Verlof of verzuim</span><span class="sxs-lookup"><span data-stu-id="f2099-599">Leave of Absence</span></span>               | <span data-ttu-id="f2099-600">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-600">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f2099-601">CONTRACTEND</span></span>            | <span data-ttu-id="f2099-602">Einde van contract</span><span class="sxs-lookup"><span data-stu-id="f2099-602">End of Contract</span></span>                | <span data-ttu-id="f2099-603">Medewerker ontslaan</span><span class="sxs-lookup"><span data-stu-id="f2099-603">Terminate worker</span></span>     |
| <span data-ttu-id="f2099-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2099-604">SALARYCHANGE</span></span>           | <span data-ttu-id="f2099-605">Salariswijziging</span><span class="sxs-lookup"><span data-stu-id="f2099-605">Change of Salary</span></span>               | <span data-ttu-id="f2099-606">Compensatie</span><span class="sxs-lookup"><span data-stu-id="f2099-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="f2099-607">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="f2099-607">Terms of employment</span></span>

<span data-ttu-id="f2099-608">Arbeidsvoorwaarden worden gebruikt om categorieën met arbeidsvoorwaarden te maken.</span><span class="sxs-lookup"><span data-stu-id="f2099-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="f2099-609">De voorwaarden worden toegewezen aan Dayforce als indicatorwaarden voor het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="f2099-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="f2099-610">De volgende arbeidsvoorwaarden en omschrijvingen zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="f2099-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="f2099-611">Arbeidsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="f2099-611">Terms of employment</span></span>   | <span data-ttu-id="f2099-612">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f2099-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f2099-613">Normaal</span><span class="sxs-lookup"><span data-stu-id="f2099-613">Regular</span></span>               | <span data-ttu-id="f2099-614">Normaal</span><span class="sxs-lookup"><span data-stu-id="f2099-614">Regular</span></span>     |
| <span data-ttu-id="f2099-615">Direct</span><span class="sxs-lookup"><span data-stu-id="f2099-615">Direct</span></span>                | <span data-ttu-id="f2099-616">Direct</span><span class="sxs-lookup"><span data-stu-id="f2099-616">Direct</span></span>      |
| <span data-ttu-id="f2099-617">Stage</span><span class="sxs-lookup"><span data-stu-id="f2099-617">Internship</span></span>            | <span data-ttu-id="f2099-618">Stage</span><span class="sxs-lookup"><span data-stu-id="f2099-618">Internship</span></span>  |
| <span data-ttu-id="f2099-619">Permanent</span><span class="sxs-lookup"><span data-stu-id="f2099-619">Permanent</span></span>             | <span data-ttu-id="f2099-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="f2099-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="f2099-621">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="f2099-621">Marital status</span></span>

<span data-ttu-id="f2099-622">De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2099-623">In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2099-624">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-624">Talent</span></span>                 | <span data-ttu-id="f2099-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="f2099-626">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="f2099-626">Married</span></span>                | <span data-ttu-id="f2099-627">Gehuwd</span><span class="sxs-lookup"><span data-stu-id="f2099-627">Married</span></span>                   |
| <span data-ttu-id="f2099-628">Eén</span><span class="sxs-lookup"><span data-stu-id="f2099-628">Single</span></span>                 | <span data-ttu-id="f2099-629">Eén</span><span class="sxs-lookup"><span data-stu-id="f2099-629">Single</span></span>                    |
| <span data-ttu-id="f2099-630">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="f2099-630">Widowed</span></span>                | <span data-ttu-id="f2099-631">Weduwe/weduwnaar</span><span class="sxs-lookup"><span data-stu-id="f2099-631">Widowed</span></span>                   |
| <span data-ttu-id="f2099-632">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="f2099-632">Divorced</span></span>               | <span data-ttu-id="f2099-633">Gescheiden</span><span class="sxs-lookup"><span data-stu-id="f2099-633">Divorced</span></span>                  |
| <span data-ttu-id="f2099-634">Geregistreerd partnerschap</span><span class="sxs-lookup"><span data-stu-id="f2099-634">Registered Partnership</span></span> | <span data-ttu-id="f2099-635">Binnenlands partnerschap</span><span class="sxs-lookup"><span data-stu-id="f2099-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="f2099-636">None</span><span class="sxs-lookup"><span data-stu-id="f2099-636">None</span></span>                   | <span data-ttu-id="f2099-637">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2099-638">Samenwonend</span><span class="sxs-lookup"><span data-stu-id="f2099-638">Cohabiting</span></span>             | <span data-ttu-id="f2099-639">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="f2099-640">Geslacht</span><span class="sxs-lookup"><span data-stu-id="f2099-640">Gender</span></span>

<span data-ttu-id="f2099-641">Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2099-642">In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2099-643">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-643">Talent</span></span>       | <span data-ttu-id="f2099-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="f2099-645">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-645">Male</span></span>         | <span data-ttu-id="f2099-646">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-646">Male</span></span>                      |
| <span data-ttu-id="f2099-647">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-647">Female</span></span>       | <span data-ttu-id="f2099-648">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="f2099-648">Female</span></span>                    |
| <span data-ttu-id="f2099-649">Niet-specifiek</span><span class="sxs-lookup"><span data-stu-id="f2099-649">Non-specific</span></span> | <span data-ttu-id="f2099-650">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="f2099-651">Betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="f2099-651">Payment method</span></span>

<span data-ttu-id="f2099-652">Betalingsmethoden bieden de werknemer en het bedrijf een manier om te beschrijven hoe werknemers worden uitbetaald.</span><span class="sxs-lookup"><span data-stu-id="f2099-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="f2099-653">Betalingsmethoden worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2099-654">In de volgende tabel wordt aangegeven hoe betalingsmethoden worden toegewezen aan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2099-655">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-655">Talent</span></span>             | <span data-ttu-id="f2099-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="f2099-657">Contant geld</span><span class="sxs-lookup"><span data-stu-id="f2099-657">Cash</span></span>               | <span data-ttu-id="f2099-658">Contant geld</span><span class="sxs-lookup"><span data-stu-id="f2099-658">Cash</span></span>                      |
| <span data-ttu-id="f2099-659">Elektronische betaling</span><span class="sxs-lookup"><span data-stu-id="f2099-659">Electronic Payment</span></span> | <span data-ttu-id="f2099-660">Overboeking</span><span class="sxs-lookup"><span data-stu-id="f2099-660">Transfer</span></span>                  |
| <span data-ttu-id="f2099-661">Controle</span><span class="sxs-lookup"><span data-stu-id="f2099-661">Check</span></span>              | <span data-ttu-id="f2099-662">Cheque</span><span class="sxs-lookup"><span data-stu-id="f2099-662">Cheque</span></span>                    |
| <span data-ttu-id="f2099-663">Bankcheque</span><span class="sxs-lookup"><span data-stu-id="f2099-663">Bank Draft</span></span>         | <span data-ttu-id="f2099-664">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2099-665">Overig</span><span class="sxs-lookup"><span data-stu-id="f2099-665">Other</span></span>              | <span data-ttu-id="f2099-666">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="f2099-667">Bankrekeningtype</span><span class="sxs-lookup"><span data-stu-id="f2099-667">Bank account type</span></span>

<span data-ttu-id="f2099-668">Bankrekeningtypen worden gebruikt voor elektronische betalingen aan werknemers.</span><span class="sxs-lookup"><span data-stu-id="f2099-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="f2099-669">Bankrekeningtypen worden toegewezen aan Dayforce als overdrachtrekeninggegevens.</span><span class="sxs-lookup"><span data-stu-id="f2099-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="f2099-670">De bankrekeningtypen worden, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.</span><span class="sxs-lookup"><span data-stu-id="f2099-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="f2099-671">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-671">Talent</span></span>            | <span data-ttu-id="f2099-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="f2099-673">Betaalrekening</span><span class="sxs-lookup"><span data-stu-id="f2099-673">Checking Account</span></span>  | <span data-ttu-id="f2099-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="f2099-674">CheckingAccount</span></span>           |
| <span data-ttu-id="f2099-675">Salarisrekening</span><span class="sxs-lookup"><span data-stu-id="f2099-675">Payroll Account</span></span>   | <span data-ttu-id="f2099-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="f2099-676">PayrollAccount</span></span>            |
| <span data-ttu-id="f2099-677">Spaarrekening</span><span class="sxs-lookup"><span data-stu-id="f2099-677">Savings Account</span></span>   | <span data-ttu-id="f2099-678">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2099-679">BankGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="f2099-679">BankGirot account</span></span> | <span data-ttu-id="f2099-680">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2099-681">PlusGirot-rekening</span><span class="sxs-lookup"><span data-stu-id="f2099-681">PlusGirot account</span></span> | <span data-ttu-id="f2099-682">*Niet ondersteund door Mexico*</span><span class="sxs-lookup"><span data-stu-id="f2099-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f2099-683">Inkomstencodes</span><span class="sxs-lookup"><span data-stu-id="f2099-683">Earning codes</span></span>

<span data-ttu-id="f2099-684">Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen.</span><span class="sxs-lookup"><span data-stu-id="f2099-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2099-685">De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.</span><span class="sxs-lookup"><span data-stu-id="f2099-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f2099-686">Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="f2099-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f2099-687">Ondersteunde frequenties</span><span class="sxs-lookup"><span data-stu-id="f2099-687">Supported frequencies</span></span>

- <span data-ttu-id="f2099-688">Alles</span><span class="sxs-lookup"><span data-stu-id="f2099-688">All</span></span>
- <span data-ttu-id="f2099-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f2099-689">EVERYPAY</span></span>
- <span data-ttu-id="f2099-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f2099-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f2099-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f2099-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f2099-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f2099-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f2099-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-693">1OFMTH</span></span>
- <span data-ttu-id="f2099-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-694">LASTOFMTH</span></span>
- <span data-ttu-id="f2099-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-695">2OFMTH</span></span>
- <span data-ttu-id="f2099-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-696">3OFMTH</span></span>
- <span data-ttu-id="f2099-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-697">4OFMTH</span></span>
- <span data-ttu-id="f2099-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-698">5OFMTH</span></span>
- <span data-ttu-id="f2099-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-699">1N2OFMTH</span></span>
- <span data-ttu-id="f2099-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-700">3N4OFMTH</span></span>
- <span data-ttu-id="f2099-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-701">1N3OFMTH</span></span>
- <span data-ttu-id="f2099-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-702">1N4OFMTH</span></span>
- <span data-ttu-id="f2099-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-703">2N3OFMTH</span></span>
- <span data-ttu-id="f2099-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-704">2N4OFMTH</span></span>
- <span data-ttu-id="f2099-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="f2099-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="f2099-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="f2099-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="f2099-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2099-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f2099-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f2099-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f2099-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f2099-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f2099-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2099-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f2099-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2099-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f2099-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2099-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f2099-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2099-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f2099-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2099-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f2099-717">Adressen</span><span class="sxs-lookup"><span data-stu-id="f2099-717">Addresses</span></span>

<span data-ttu-id="f2099-718">De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend.</span><span class="sxs-lookup"><span data-stu-id="f2099-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f2099-719">Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.</span><span class="sxs-lookup"><span data-stu-id="f2099-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f2099-720">Talent</span><span class="sxs-lookup"><span data-stu-id="f2099-720">Talent</span></span>              | <span data-ttu-id="f2099-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2099-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="f2099-722">Land/regio</span><span class="sxs-lookup"><span data-stu-id="f2099-722">Country/Region</span></span>      | <span data-ttu-id="f2099-723">Landcode</span><span class="sxs-lookup"><span data-stu-id="f2099-723">Country Code</span></span>          |
| <span data-ttu-id="f2099-724">Postcode</span><span class="sxs-lookup"><span data-stu-id="f2099-724">Zip/Postal Code</span></span>     | <span data-ttu-id="f2099-725">Postcode</span><span class="sxs-lookup"><span data-stu-id="f2099-725">Postal Code</span></span>           |
| <span data-ttu-id="f2099-726">Provincie</span><span class="sxs-lookup"><span data-stu-id="f2099-726">State</span></span>               | <span data-ttu-id="f2099-727">Staatcode</span><span class="sxs-lookup"><span data-stu-id="f2099-727">State Code</span></span>            |
| <span data-ttu-id="f2099-728">Plaats</span><span class="sxs-lookup"><span data-stu-id="f2099-728">City</span></span>                | <span data-ttu-id="f2099-729">Plaats</span><span class="sxs-lookup"><span data-stu-id="f2099-729">City</span></span>                  |
| <span data-ttu-id="f2099-730">District</span><span class="sxs-lookup"><span data-stu-id="f2099-730">County</span></span>              | <span data-ttu-id="f2099-731">District (gemeente)</span><span class="sxs-lookup"><span data-stu-id="f2099-731">County (Municipality)</span></span> |
| <span data-ttu-id="f2099-732">Adres</span><span class="sxs-lookup"><span data-stu-id="f2099-732">Street</span></span>              | <span data-ttu-id="f2099-733">Adresregel 1</span><span class="sxs-lookup"><span data-stu-id="f2099-733">Address Line 1</span></span>        |
| <span data-ttu-id="f2099-734">Huisnummer</span><span class="sxs-lookup"><span data-stu-id="f2099-734">Street Number</span></span>       | <span data-ttu-id="f2099-735">Adresregel 2</span><span class="sxs-lookup"><span data-stu-id="f2099-735">Address Line 2</span></span>        |
| <span data-ttu-id="f2099-736">Gebouwtoevoeging</span><span class="sxs-lookup"><span data-stu-id="f2099-736">Building Complement</span></span> | <span data-ttu-id="f2099-737">Adresregel 5</span><span class="sxs-lookup"><span data-stu-id="f2099-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="f2099-738">Paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="f2099-738">Passport number</span></span>

<span data-ttu-id="f2099-739">Werknemers kunnen paspoortgegevens opgeven.</span><span class="sxs-lookup"><span data-stu-id="f2099-739">Employees can declare passport information.</span></span> <span data-ttu-id="f2099-740">Deze informatie is van het identificatietype **Paspoort** en wordt in Dayforce geïntegreerd als onderdeel van de Mexico-specifieke informatie van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="f2099-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="f2099-741">Identificatietype = 'Paspoort'</span><span class="sxs-lookup"><span data-stu-id="f2099-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="f2099-742">Uitgiftedatum</span><span class="sxs-lookup"><span data-stu-id="f2099-742">Issued Date</span></span>
- <span data-ttu-id="f2099-743">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f2099-743">Expiration Date</span></span>

<span data-ttu-id="f2099-744">Werknemers kunnen meerdere identificatienummers van het identificatietype **Paspoort** opgeven.</span><span class="sxs-lookup"><span data-stu-id="f2099-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="f2099-745">Echter alleen de huidige actieve paspoortvermelding wordt geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="f2099-746">Als alle paspoortvermeldingen zijn verlopen, wordt het paspoort dat als laatste is uitgegeven geïntegreerd in Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2099-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
