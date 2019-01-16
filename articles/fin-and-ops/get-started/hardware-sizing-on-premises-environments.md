---
title: Vereisten vaststellen voor grootte van de hardware voor on-premises omgevingen
description: Vereisten vaststellen voor grootte van de hardware voor on-premises omgevingen
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: d277bc4c4c815317bade8a04b9111232fb707086
ms.contentlocale: nl-nl
ms.lasthandoff: 12/18/2018

---

# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="29fbc-103">Vereisten vaststellen voor grootte van de hardware voor on-premises omgevingen</span><span class="sxs-lookup"><span data-stu-id="29fbc-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29fbc-104">Voordat u de omvang gaat bepalen van de hardware en de infrastructuur van een on-premises omgeving, dient u vertrouwd zijn met de [Systeemvereisten](system-requirements.md) en [Instructies voor installatie en implementatie](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) om een goed begrip te krijgen van de onderliggende infrastructuur.</span><span class="sxs-lookup"><span data-stu-id="29fbc-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="29fbc-105">Let goed op de aanbevolen procedures voor de systeeminstellingen voor optimale prestaties.</span><span class="sxs-lookup"><span data-stu-id="29fbc-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="29fbc-106">Nadat u de documentatie hebt bekeken, kunt u gaan inschatten hoeveel transactionele en gelijktijdige gebruikers er zijn en welke omvang uw omgeving moet hebben op basis van de gemiddelde coredoorvoer.</span><span class="sxs-lookup"><span data-stu-id="29fbc-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="29fbc-107">Factoren die invloed hebben op de grootte</span><span class="sxs-lookup"><span data-stu-id="29fbc-107">Factors that affect sizing</span></span>

<span data-ttu-id="29fbc-108">Alle factoren in de volgende afbeelding zijn bepalend voor de grootte.</span><span class="sxs-lookup"><span data-stu-id="29fbc-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="29fbc-109">Hoe meer gedetailleerde informatie u verzamelt, hoe preciezer u de grootte kunt bepalen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="29fbc-110">Zonder ondersteunende gegevens kunt u de omvang van de hardware niet inschatten.</span><span class="sxs-lookup"><span data-stu-id="29fbc-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="29fbc-111">De absolute minimumvereiste voor de benodigde gegevens is de piekbelasting voor de transactieregels per uur.</span><span class="sxs-lookup"><span data-stu-id="29fbc-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="29fbc-112">[![Grootte van de hardware voor on-premises omgevingen vaststellen](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="29fbc-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="29fbc-113">Van links naar rechts gezien, is de eerste en de belangrijkste factor voor het nauwkeurig schatten een transactieprofiel of een karakterisering van de transacties.</span><span class="sxs-lookup"><span data-stu-id="29fbc-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="29fbc-114">Het is van groot belang dat u altijd het transactionele piekvolume per uur weet.</span><span class="sxs-lookup"><span data-stu-id="29fbc-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="29fbc-115">Als er meerdere piekuren zijn, moeten deze perioden correct zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="29fbc-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="29fbc-116">Als u weet wat de belasting is van uw infrastructuur, moet u ook meer details weten van deze factoren:</span><span class="sxs-lookup"><span data-stu-id="29fbc-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="29fbc-117">**Transacties**: transacties hebben doorgaans bepaalde pieken in de dag/week.</span><span class="sxs-lookup"><span data-stu-id="29fbc-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="29fbc-118">Dit is meestal afhankelijk van het transactietype.</span><span class="sxs-lookup"><span data-stu-id="29fbc-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="29fbc-119">Tijd- en onkostengegevens hebben meestal eenmaal per week een piek, terwijl verkoopordergegevens vaak in bulk binnenkomen via integratie of binnendruppelen gedurende de dag.</span><span class="sxs-lookup"><span data-stu-id="29fbc-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="29fbc-120">**Aantal gelijktijdige gebruikers**: het aantal gelijktijdige gebruikers is de tweede belangrijkste factor voor de grootte.</span><span class="sxs-lookup"><span data-stu-id="29fbc-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="29fbc-121">U kunt geen betrouwbare ramingen krijgen op basis van het aantal gelijktijdige gebruikers, dus als dit de enige gegevens zijn waarover u beschikt, schat u het aantal bij benadering en past u dit aan als u meer gegevens hebt.</span><span class="sxs-lookup"><span data-stu-id="29fbc-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="29fbc-122">Een nauwkeurige definitie van het aantal gelijktijdige gebruikers houdt in:</span><span class="sxs-lookup"><span data-stu-id="29fbc-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="29fbc-123">Benoemde gebruikers zijn geen gelijktijdige gebruikers.</span><span class="sxs-lookup"><span data-stu-id="29fbc-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="29fbc-124">Gelijktijdige gebruikers zijn altijd een subset van de benoemde gebruikers.</span><span class="sxs-lookup"><span data-stu-id="29fbc-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="29fbc-125">Maximale werkbelasting bepaalt de maximale gelijktijdigheid voor grootte.</span><span class="sxs-lookup"><span data-stu-id="29fbc-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="29fbc-126">Criteria voor gelijktijdige gebruikers zijn dat de gebruiker voldoet aan de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="29fbc-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="29fbc-127">Heeft zich aangemeld.</span><span class="sxs-lookup"><span data-stu-id="29fbc-127">Logged on.</span></span>
    - <span data-ttu-id="29fbc-128">Verwerkt transacties/query's op het moment van de telling.</span><span class="sxs-lookup"><span data-stu-id="29fbc-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="29fbc-129">Is geen niet-actieve sessie.</span><span class="sxs-lookup"><span data-stu-id="29fbc-129">Not an idle session.</span></span>

- <span data-ttu-id="29fbc-130">**Gegevenssamenstelling**: dit betreft vooral hoe uw systeem wordt ingesteld en geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="29fbc-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="29fbc-131">Bijvoorbeeld hoeveel rechtspersonen u hebt, hoeveel artikelen, het aantal stuklijstniveaus en de complexiteit van de beveiligingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="29fbc-132">Elk van deze factoren kan een kleine invloed hebben op prestaties, zodat deze factoren kunnen worden verrekend met behulp van slimme keuzes wanneer het gaat om de infrastructuur.</span><span class="sxs-lookup"><span data-stu-id="29fbc-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="29fbc-133">**Uitbreidingen**: aanpassingen kunnen eenvoudig of complex zijn.</span><span class="sxs-lookup"><span data-stu-id="29fbc-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="29fbc-134">Het aantal aanpassingen en de aard van de complexiteit en het gebruik heeft een uiteenlopende invloed op de omvang van de benodigde infrastructuur.</span><span class="sxs-lookup"><span data-stu-id="29fbc-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="29fbc-135">Voor complexe aanpassingen wordt het aanbevolen om de werking te evalueren om te zorgen dat ze niet alleen worden getest op efficiëntie, maar ook op inzicht in wat nodig is voor de infrastructuur.</span><span class="sxs-lookup"><span data-stu-id="29fbc-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="29fbc-136">Dit is nog belangrijker wanneer de uitbreidingen niet zijn gecodeerd volgens de beste methoden voor prestaties en schaalbaarheid.</span><span class="sxs-lookup"><span data-stu-id="29fbc-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="29fbc-137">**Rapportage en analyse**: hiervoor moeten normaal gesproken zware query's worden uitgevoerd op de verschillende databases in de databasesystemen van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="29fbc-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</span></span> <span data-ttu-id="29fbc-138">Begrip en vermindering van de frequentie voor het uitvoeren van dure rapporten geeft meer inzicht in de gevolgen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="29fbc-139">**Oplossingen van andere leveranciers**: deze oplossingen, zoals ISV's, hebben dezelfde implicaties en aanbevelingen als uitbreidingen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-finance-and-operations-environment"></a><span data-ttu-id="29fbc-140">De omvang van de Finance and Operations-omgeving</span><span class="sxs-lookup"><span data-stu-id="29fbc-140">Sizing your Finance and Operations environment</span></span>

<span data-ttu-id="29fbc-141">Als u inzicht wilt krijgen in welke omvang nodig is, moet u het piekvolume weten van de transacties die moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="29fbc-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="29fbc-142">Aanvullende systemen, zoals Management Reporter of SQL Server Reporting Services, zijn meestal minder bedrijfskritiek.</span><span class="sxs-lookup"><span data-stu-id="29fbc-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="29fbc-143">Daarom richt dit document zich voornamelijk op de AOS en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="29fbc-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="29fbc-144">Gewoonlijk worden de berekeningsniveaus schaalbaar uitgebreid en ingesteld als N+1. Als u dus een schatting maakt voor drie AOS, voegt u een vierde AOS toe.</span><span class="sxs-lookup"><span data-stu-id="29fbc-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="29fbc-145">De databaselaag moet worden ingesteld als maximaal beschikbaar en Always On.</span><span class="sxs-lookup"><span data-stu-id="29fbc-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="29fbc-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="29fbc-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="29fbc-147">Grootte</span><span class="sxs-lookup"><span data-stu-id="29fbc-147">Sizing</span></span>

- <span data-ttu-id="29fbc-148">3K tot 15K transactieregels per uur per core op de databaseserver.</span><span class="sxs-lookup"><span data-stu-id="29fbc-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="29fbc-149">Normale verhouding van AOS-SQL-core 3:1 voor de primaire SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="29fbc-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="29fbc-150">Extra cores zijn vereist op basis van de gekozen configuratie voor hoge beschikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="29fbc-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="29fbc-151">Door zware databasebewerkingen kan dit veranderen in 2:1.</span><span class="sxs-lookup"><span data-stu-id="29fbc-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="29fbc-152">De volgende factoren beïnvloeden variaties:</span><span class="sxs-lookup"><span data-stu-id="29fbc-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="29fbc-153">Gebruikte parameterinstellingen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="29fbc-154">Uitbreidingsniveaus.</span><span class="sxs-lookup"><span data-stu-id="29fbc-154">Levels of extensions.</span></span>
    - <span data-ttu-id="29fbc-155">Gebruik van aanvullende functionaliteit, zoals databaselogboeken en waarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="29fbc-156">Door extreem gebruik van databaselogboeken daalt de doorvoer per uur per core onder 3K regels.</span><span class="sxs-lookup"><span data-stu-id="29fbc-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="29fbc-157">Complexiteit van de gegevenssamenstelling: een eenvoudig rekeningschema versus een gedetailleerd en specifiek rekeningschema heeft gevolgen voor de doorvoer (bijvoorbeeld).</span><span class="sxs-lookup"><span data-stu-id="29fbc-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="29fbc-158">Kenmerken van de transacties.</span><span class="sxs-lookup"><span data-stu-id="29fbc-158">Transaction characterization.</span></span>
    - <span data-ttu-id="29fbc-159">2 GB tot 4 GB geheugen voor elke core.</span><span class="sxs-lookup"><span data-stu-id="29fbc-159">2 GB to 4 GB memory for each core.</span></span>
    - <span data-ttu-id="29fbc-160">Aanvullende databases op een databaseserver zoals Management Reporter en SSRS-databases.</span><span class="sxs-lookup"><span data-stu-id="29fbc-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="29fbc-161">Tijdelijke DB = 15% van de DB-omvang met evenveel bestanden als fysieke processors.</span><span class="sxs-lookup"><span data-stu-id="29fbc-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="29fbc-162">SAN-grootte en doorvoer op basis van het totale gelijktijdige transactievolume/gebruik.</span><span class="sxs-lookup"><span data-stu-id="29fbc-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="29fbc-163">Hoge beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="29fbc-163">High availability</span></span>

<span data-ttu-id="29fbc-164">Wij raden altijd aan om SQL Server te gebruiken voor cluster- of mirror-instellingen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="29fbc-165">Het tweede SQL-knooppunt moet hetzelfde aantal cores hebben als het primaire knooppunt.</span><span class="sxs-lookup"><span data-stu-id="29fbc-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="29fbc-166">Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="29fbc-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="29fbc-167">Voor de omvang van AD FS raadpleegt u [de documentatie over de capaciteit van de AD FS-server](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="29fbc-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="29fbc-168">Er is een [werkblad met de grootte](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) beschikbaar voor het plannen van het aantal exemplaren in uw implementatie.</span><span class="sxs-lookup"><span data-stu-id="29fbc-168">A [sizing spreadsheet](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="29fbc-169">AOS (online en batch)</span><span class="sxs-lookup"><span data-stu-id="29fbc-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="29fbc-170">Grootte</span><span class="sxs-lookup"><span data-stu-id="29fbc-170">Sizing</span></span>

- <span data-ttu-id="29fbc-171">Grootte op transactie volume/gebruik</span><span class="sxs-lookup"><span data-stu-id="29fbc-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="29fbc-172">2K tot 6K regels per core</span><span class="sxs-lookup"><span data-stu-id="29fbc-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="29fbc-173">16 GB per exemplaar</span><span class="sxs-lookup"><span data-stu-id="29fbc-173">16 GB per instance</span></span>
    - <span data-ttu-id="29fbc-174">Standaard: 4 tot 24 cores</span><span class="sxs-lookup"><span data-stu-id="29fbc-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="29fbc-175">10 tot 15 Enterprise-gebruikers per core</span><span class="sxs-lookup"><span data-stu-id="29fbc-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="29fbc-176">15 tot 25 activiteitgebruikers per core</span><span class="sxs-lookup"><span data-stu-id="29fbc-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="29fbc-177">25 tot 50 teamleden per core</span><span class="sxs-lookup"><span data-stu-id="29fbc-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="29fbc-178">Batch</span><span class="sxs-lookup"><span data-stu-id="29fbc-178">Batch</span></span>

    - <span data-ttu-id="29fbc-179">1 tot 4 batchthreads per core</span><span class="sxs-lookup"><span data-stu-id="29fbc-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="29fbc-180">Grootte op basis van de kenmerken van het batchvenster</span><span class="sxs-lookup"><span data-stu-id="29fbc-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="29fbc-181">Houd er rekening mee dat AOS, Gegevensbeheer en Batch dezelfde rol hebben in de Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="29fbc-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="29fbc-182">Gebruik een gecombineerde omvang voor deze drie werkbelastingen en niet afzonderlijk zoals in Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="29fbc-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="29fbc-183">Dezelfde variabele factoren voor SQL Server zijn hier van toepassing.</span><span class="sxs-lookup"><span data-stu-id="29fbc-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="29fbc-184">Hoge beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="29fbc-184">High availability</span></span>

- <span data-ttu-id="29fbc-185">Zorg ervoor dat er minimaal 1 tot 2 meer AOS beschikbaar zijn dan de schatting.</span><span class="sxs-lookup"><span data-stu-id="29fbc-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="29fbc-186">Zorg ervoor dat er ten minste 3 tot 4 virtuele hosts beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="29fbc-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="29fbc-187">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="29fbc-187">Management reporter</span></span>

<span data-ttu-id="29fbc-188">In de meeste gevallen, tenzij bij intensief gebruik, zijn de aanbevolen minimale eisen met twee knooppunten voldoende.</span><span class="sxs-lookup"><span data-stu-id="29fbc-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="29fbc-189">Alleen in gevallen met intensief gebruik moet u meer dan twee knooppunten hebben.</span><span class="sxs-lookup"><span data-stu-id="29fbc-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="29fbc-190">Breid dit naar behoeven uit.</span><span class="sxs-lookup"><span data-stu-id="29fbc-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="29fbc-191">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="29fbc-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="29fbc-192">Voor de algemene beschikbaarheid hoeft slechts één SSRS-knooppunt te worden geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="29fbc-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="29fbc-193">Controleer SSRS-knooppunt bij het testen en verhoog het aantal beschikbare cores voor SSRS op basis van de behoefte.</span><span class="sxs-lookup"><span data-stu-id="29fbc-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="29fbc-194">Zorg ervoor dat er een vooraf geconfigureerd secundair knooppunt beschikbaar is op een virtuele host die verschilt van de SSRS VM.</span><span class="sxs-lookup"><span data-stu-id="29fbc-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="29fbc-195">Dit is belangrijk als er een probleem is met de virtuele machine die als host fungeert voor SSRS of met de virtuele host.</span><span class="sxs-lookup"><span data-stu-id="29fbc-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="29fbc-196">Als dit het geval is, moeten ze worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="29fbc-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="29fbc-197">Orchestrator-omgeving</span><span class="sxs-lookup"><span data-stu-id="29fbc-197">Environment Orchestrator</span></span>

<span data-ttu-id="29fbc-198">De Orchestrator-service beheert uw implementatie en de gerelateerde communicatie met LCS.</span><span class="sxs-lookup"><span data-stu-id="29fbc-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="29fbc-199">Deze service wordt geïmplementeerd als de primaire Service Fabric-service en vereist ten minste drie VM's.</span><span class="sxs-lookup"><span data-stu-id="29fbc-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="29fbc-200">Deze service bevindt zich op dezelfde locatie als de Service Fabric-configuratieservices.</span><span class="sxs-lookup"><span data-stu-id="29fbc-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="29fbc-201">De omvang moet voldoen aan de piekbelasting van het cluster.</span><span class="sxs-lookup"><span data-stu-id="29fbc-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="29fbc-202">Zie voor meer informatie [Overwegingen bij capaciteitsplanning van Service Fabric-cluster](/azure/service-fabric/service-fabric-cluster-capacity).</span><span class="sxs-lookup"><span data-stu-id="29fbc-202">For more information, see [Service Fabric cluster capacity planning considerations](/azure/service-fabric/service-fabric-cluster-capacity).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="29fbc-203">Virtualisering en te veel abonnementen</span><span class="sxs-lookup"><span data-stu-id="29fbc-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="29fbc-204">Bedrijfskritieke services, zoals de AOS, moeten worden gehost op virtuele hosts met eigen resources: cores, geheugen en schijfruimte.</span><span class="sxs-lookup"><span data-stu-id="29fbc-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>

