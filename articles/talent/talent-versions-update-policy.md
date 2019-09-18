---
title: Systeemvereisten en updatebeleid voor Talent
description: In dit onderwerp worden vereisten voor Dynamics 365 for Talent weergegeven. Ook wordt het updatebeleid beschreven.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6c881bf25e7145228ccf7ef73a7ef3637c115a49
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741770"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="dc088-104">Systeemvereisten en updatebeleid voor Talent</span><span class="sxs-lookup"><span data-stu-id="dc088-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc088-105">In dit onderwerp worden de vereisten beschreven voor Microsoft Dynamics 365 for Talent, met inbegrip van Attract, Onboard, en Core HR.</span><span class="sxs-lookup"><span data-stu-id="dc088-105">This topic describes requirements for Microsoft Dynamics 365 for Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="dc088-106">Het bevat ook een overzicht van de landen en regio's waarin Talent beschikbaar is, plus informatie over talen en lokalisatie voor Talent-gegevens.</span><span class="sxs-lookup"><span data-stu-id="dc088-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="dc088-107">In toevoegingen bevat dit onderwerp het updatebeleid voor Talent.</span><span class="sxs-lookup"><span data-stu-id="dc088-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="dc088-108">Ondersteunde webbrowsers</span><span class="sxs-lookup"><span data-stu-id="dc088-108">Supported web browsers</span></span>

<span data-ttu-id="dc088-109">De webtoepassing Microsoft Dynamics 365 for Talent kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:</span><span class="sxs-lookup"><span data-stu-id="dc088-109">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="dc088-110">Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10</span><span class="sxs-lookup"><span data-stu-id="dc088-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="dc088-111">Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7</span><span class="sxs-lookup"><span data-stu-id="dc088-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="dc088-112">Google Chrome (meest recente openbaar beschikbare versie)</span><span class="sxs-lookup"><span data-stu-id="dc088-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="dc088-113">Apple Safari (meest recente openbaar beschikbare versie)</span><span class="sxs-lookup"><span data-stu-id="dc088-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="dc088-114">Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant.</span><span class="sxs-lookup"><span data-stu-id="dc088-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="dc088-115">Om schermopnamen vast te leggen die door Taakrecorder zijn gegenereerd en deze op te nemen in Microsoft Word-documenten, moet u een Chrome-invoegtoepassing hebben geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="dc088-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="dc088-116">De workfloweditor wordt als ClickOnce-toepassing gestart.</span><span class="sxs-lookup"><span data-stu-id="dc088-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="dc088-117">Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="dc088-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="dc088-118">De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.</span><span class="sxs-lookup"><span data-stu-id="dc088-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="dc088-119">Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.</span><span class="sxs-lookup"><span data-stu-id="dc088-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="dc088-120">Netwerkvereisten</span><span class="sxs-lookup"><span data-stu-id="dc088-120">Network requirements</span></span>
> * <span data-ttu-id="dc088-121">Dynamics 365 for Talent is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder.</span><span class="sxs-lookup"><span data-stu-id="dc088-121">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="dc088-122">Dit is de vertragingstijd van een browserclient naar het Microsoft Azure-datacentrum waar Dynamics 365 for Talent wordt gehost.</span><span class="sxs-lookup"><span data-stu-id="dc088-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="dc088-123">Het wordt aangeraden om uw netwerklatentie te testen op [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span><span class="sxs-lookup"><span data-stu-id="dc088-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="dc088-124">Bandbreedtevereisten voor Dynamics 365 for Talent zijn afhankelijk van uw scenario.</span><span class="sxs-lookup"><span data-stu-id="dc088-124">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="dc088-125">De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps).</span><span class="sxs-lookup"><span data-stu-id="dc088-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="dc088-126">Bereken bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten.</span><span class="sxs-lookup"><span data-stu-id="dc088-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="dc088-127">Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen.</span><span class="sxs-lookup"><span data-stu-id="dc088-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="dc088-128">Gebruik voor klanten die zich zorgen maken over de bandbreedtevereisten, een evaluatieversie van Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="dc088-128">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="dc088-129">Ondersteunde Microsoft Office-toepassingen</span><span class="sxs-lookup"><span data-stu-id="dc088-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="dc088-130">Als u de invoegtoepassingen voor Microsoft Excel en Word wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="dc088-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="dc088-131">Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](../dev-itpro/office-integration/office-integration-troubleshooting.md "Probleemoplossing voor Office-integratie").</span><span class="sxs-lookup"><span data-stu-id="dc088-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="dc088-132">Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="dc088-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="dc088-133">Regionale beschikbaarheid, talen en lokalisatie</span><span class="sxs-lookup"><span data-stu-id="dc088-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="dc088-134">U kunt een PDF-bestand downloaden met de landen, regio's en talen die door Talent worden ondersteund in [Internationale beschikbaarheid van Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="dc088-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="dc088-135">Terwijl de gebruikersinterface wordt gelokaliseerd in andere talen, worden alle gebruikersgegevens opgeslagen in de taal waarin deze zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="dc088-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="dc088-136">U kunt e-mails en sjablonen in andere talen maken, maar gegevens zoals planningsgegevens zijn op dit moment alleen in het Engels beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="dc088-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="dc088-137">Zie [Globalisatie](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) als u een ontwikkelaar bent die geïnteresseerd is in het maken van land- of regiospecifieke aanpassingen of in het maken van een oplossing voor een land dat of regio die momenteel niet door Microsoft wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="dc088-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="dc088-138">Updatebeleid</span><span class="sxs-lookup"><span data-stu-id="dc088-138">Update policy</span></span>

<span data-ttu-id="dc088-139">Microsoft Dynamics 365 for Talent wordt aangeboden via de cloud.</span><span class="sxs-lookup"><span data-stu-id="dc088-139">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="dc088-140">Updates voor Dynamics 365 for Talent vinden doorlopend plaats en worden automatisch toegepast door Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc088-140">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="dc088-141">Er worden regelmatig updates uitgebracht en doorgevoerd in alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="dc088-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="dc088-142">Dynamics 365 for Talent wordt ondersteund volgens het [Microsoft Support Lifecycle-beleid](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), dat consistente en voorspelbare richtlijnen bevat voor de beschikbaarheid van productondersteuning.</span><span class="sxs-lookup"><span data-stu-id="dc088-142">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
