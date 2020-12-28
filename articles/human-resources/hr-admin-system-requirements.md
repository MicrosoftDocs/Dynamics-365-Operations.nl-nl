---
title: Systeemvereisten
description: In dit artikel worden de vereisten voor Microsoft Dynamics 365 Human Resources beschreven.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f68b8f642ada1345e7097b5e7220e222b132b1dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418012"
---
# <a name="system-requirements"></a><span data-ttu-id="cbe07-103">Systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="cbe07-103">System requirements</span></span>

<span data-ttu-id="cbe07-104">In dit artikel worden de vereisten voor Microsoft Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="cbe07-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cbe07-105">Het artikel bevat ook een overzicht van de landen en regio's waarin Human Resources beschikbaar is, plus informatie over talen en lokalisatie voor Human Resources-gegevens.</span><span class="sxs-lookup"><span data-stu-id="cbe07-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="cbe07-106">Ondersteunde webbrowsers</span><span class="sxs-lookup"><span data-stu-id="cbe07-106">Supported web browsers</span></span>

<span data-ttu-id="cbe07-107">Human Resources kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:</span><span class="sxs-lookup"><span data-stu-id="cbe07-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="cbe07-108">Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10</span><span class="sxs-lookup"><span data-stu-id="cbe07-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="cbe07-109">Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbe07-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="cbe07-110">Google Chrome (meest recente openbaar beschikbare versie)</span><span class="sxs-lookup"><span data-stu-id="cbe07-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="cbe07-111">Apple Safari (meest recente openbaar beschikbare versie)</span><span class="sxs-lookup"><span data-stu-id="cbe07-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="cbe07-112">Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant.</span><span class="sxs-lookup"><span data-stu-id="cbe07-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="cbe07-113">Om schermopnamen vast te leggen die door Taakrecorder zijn gegenereerd en deze op te nemen in Microsoft Word-documenten, moet u een Chrome-invoegtoepassing hebben geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="cbe07-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="cbe07-114">De workfloweditor wordt als ClickOnce-toepassing gestart.</span><span class="sxs-lookup"><span data-stu-id="cbe07-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="cbe07-115">Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="cbe07-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="cbe07-116">De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.</span><span class="sxs-lookup"><span data-stu-id="cbe07-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="cbe07-117">Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.</span><span class="sxs-lookup"><span data-stu-id="cbe07-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="cbe07-118">Netwerkvereisten</span><span class="sxs-lookup"><span data-stu-id="cbe07-118">Network requirements</span></span>
> * <span data-ttu-id="cbe07-119">Human Resources is ontworpen voor netwerken met een latentie van 250-300 milliseconden (ms) of minder.</span><span class="sxs-lookup"><span data-stu-id="cbe07-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="cbe07-120">Dit is de latentie van een browserclient naar het Microsoft Azure-datacentrum waar Human Resources wordt gehost.</span><span class="sxs-lookup"><span data-stu-id="cbe07-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="cbe07-121">Het wordt aangeraden om uw netwerklatentie te testen op [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span><span class="sxs-lookup"><span data-stu-id="cbe07-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="cbe07-122">Bandbreedtevereisten voor Human Resources zijn afhankelijk van uw scenario.</span><span class="sxs-lookup"><span data-stu-id="cbe07-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="cbe07-123">De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps).</span><span class="sxs-lookup"><span data-stu-id="cbe07-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="cbe07-124">Bereken bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten.</span><span class="sxs-lookup"><span data-stu-id="cbe07-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="cbe07-125">Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen.</span><span class="sxs-lookup"><span data-stu-id="cbe07-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="cbe07-126">Gebruik voor klanten die zich zorgen maken over de bandbreedtevereisten, een evaluatieversie van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cbe07-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="cbe07-127">Ondersteunde Microsoft Office-toepassingen</span><span class="sxs-lookup"><span data-stu-id="cbe07-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="cbe07-128">Als u de invoegtoepassingen voor Microsoft Excel en Word wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="cbe07-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="cbe07-129">Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](../dev-itpro/office-integration/office-integration-troubleshooting.md "Problemen met Office-integratie oplossen").</span><span class="sxs-lookup"><span data-stu-id="cbe07-129">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="cbe07-130">Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="cbe07-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="cbe07-131">Regionale beschikbaarheid, talen en lokalisatie</span><span class="sxs-lookup"><span data-stu-id="cbe07-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="cbe07-132">U kunt een PDF-bestand downloaden met de landen, regio's en talen die door Human Resources worden ondersteund in [Internationale beschikbaarheid van Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="cbe07-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="cbe07-133">Terwijl de gebruikersinterface wordt gelokaliseerd in andere talen, worden alle gebruikersgegevens opgeslagen in de taal waarin deze zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="cbe07-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="cbe07-134">U kunt e-mails en sjablonen in andere talen maken, maar gegevens zoals planningsgegevens zijn op dit moment alleen in het Engels beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="cbe07-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="cbe07-135">Zie [Globalisatie](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) als u een ontwikkelaar bent die geïnteresseerd is in het maken van land- of regiospecifieke aanpassingen of in het maken van een oplossing voor een land dat of regio die momenteel niet door Microsoft wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="cbe07-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>
