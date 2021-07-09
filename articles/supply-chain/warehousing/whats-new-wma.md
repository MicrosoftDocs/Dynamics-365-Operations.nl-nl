---
title: Nieuwe of gewijzigde functies in de mobiele app Warehouse Management
description: In dit onderwerp worden de nieuwe en gewijzigde functies genoemd voor elke vrijgegeven versie van de mobiele app Warehouse Management voor Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261770"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="5a10f-103">Nieuwe of gewijzigde functies in de mobiele app Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="5a10f-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a10f-104">In dit onderwerp worden de nieuwe functies, oplossingen, verbeteringen en bekende problemen genoemd voor elke vrijgegeven versie van de mobiele app Warehouse Management voor Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a10f-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="5a10f-105">Versie 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="5a10f-106">Nieuwe functies, oplossingen en verbeteringen in 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="5a10f-107">Deze versie bevat de volgende nieuwe functies, verbeteringen en oplossingen voor fouten:</span><span class="sxs-lookup"><span data-stu-id="5a10f-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="5a10f-108">In de demonstratiemodus worden nu alle labels in de apparaattaal vermeld.</span><span class="sxs-lookup"><span data-stu-id="5a10f-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="5a10f-109">Het is minder waarschijnlijk dat u het volgende foutbericht ontvangt: 'Kan geen geschikte weergave vinden voor de opgegeven grootte'.</span><span class="sxs-lookup"><span data-stu-id="5a10f-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="5a10f-110">De minimumhoogte voor werkkaarten is toegenomen (voor gevallen waarin er drie of minder velden zijn geconfigureerd voor de werklijst).</span><span class="sxs-lookup"><span data-stu-id="5a10f-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="5a10f-111">De marges (wegvallen) onderaan de detailkaarten zijn verbeterd.</span><span class="sxs-lookup"><span data-stu-id="5a10f-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="5a10f-112">Ongeldige symbolen in XML-bestanden die met de server worden uitgewisseld, worden nu op de een of andere manier verwerkt.</span><span class="sxs-lookup"><span data-stu-id="5a10f-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="5a10f-113">(Niet-afdrukbare tekens worden nu op een andere manier verwerkt en zijn er niet langer de oorzaak van dat de app niet meer reageert.)</span><span class="sxs-lookup"><span data-stu-id="5a10f-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="5a10f-114">HTTP-fouten (zoals 'fout 503') wanneer een serveraanvraag wordt ingediend, worden nu op een andere manier verwerkt.</span><span class="sxs-lookup"><span data-stu-id="5a10f-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="5a10f-115">Als er een fout wordt weergegeven, wordt de lijst met opties niet meer automatisch weergegeven voor de besturingselementen van keuzelijsten met invoervak.</span><span class="sxs-lookup"><span data-stu-id="5a10f-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="5a10f-116">De weergavestand die in de gebruikersinstellingen is geselecteerd, veroorzaakt niet meer dat de app stopt met reageren.</span><span class="sxs-lookup"><span data-stu-id="5a10f-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="5a10f-117">Productafbeeldingen worden nu weergegeven in selfserviceomgevingen.</span><span class="sxs-lookup"><span data-stu-id="5a10f-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="5a10f-118">(Deze wijziging is alleen van toepassing op versies met een lage resolutie.</span><span class="sxs-lookup"><span data-stu-id="5a10f-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="5a10f-119">De bestandsbeheerservice ondersteunt geen afbeeldingen in een volledige grootte in selfserviceomgevingen.)</span><span class="sxs-lookup"><span data-stu-id="5a10f-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="5a10f-120">Een probleem met een nulhoeveelheid voor korte verzamelingen is opgelost.</span><span class="sxs-lookup"><span data-stu-id="5a10f-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="5a10f-121">Als een detailkaart meerdere identieke velden bevat, veroorzaakt dit niet meer dat de app stopt met reageren.</span><span class="sxs-lookup"><span data-stu-id="5a10f-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="5a10f-122">Bekende problemen in 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="5a10f-123">De volgende bekende problemen komen in deze versie voor:</span><span class="sxs-lookup"><span data-stu-id="5a10f-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="5a10f-124">De app (met name de werklijst) wordt na verloop van tijd langzamer.</span><span class="sxs-lookup"><span data-stu-id="5a10f-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="5a10f-125">**Windows-versie**: wanneer onder Windows een USB-scanner wordt gebruikt om te scannen, veroorzaken inconsistente resultaten dat gescande symbolen door elkaar raken.</span><span class="sxs-lookup"><span data-stu-id="5a10f-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="5a10f-126">Versie 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-126">Version 2.0.5.0</span></span>

<span data-ttu-id="5a10f-127">Deze versie bevat de volgende nieuwe functies, verbeteringen en oplossingen voor fouten:</span><span class="sxs-lookup"><span data-stu-id="5a10f-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="5a10f-128">Het clientgeheim wordt niet meer verborgen in de configuratie van de verbindingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="5a10f-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="5a10f-129">U kunt nu elke tekst lang indrukken om deze volledig weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5a10f-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="5a10f-130">Het foutbericht wanneer er opslagmachtigingen ontbreken, is verbeterd.</span><span class="sxs-lookup"><span data-stu-id="5a10f-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="5a10f-131">Er zijn nieuwe besturingsreeksen toegevoegd voor bepaalde stromen.</span><span class="sxs-lookup"><span data-stu-id="5a10f-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="5a10f-132">De verzendknop wordt niet langer ten onrechte beschikbaar gesteld vanwege de venstergrootte.</span><span class="sxs-lookup"><span data-stu-id="5a10f-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="5a10f-133">Schuifregelaars kunnen nu doorgaan op kleinere schermen wanneer grotere knoppengrootten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5a10f-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="5a10f-134">De overlay met vier knoppen wordt niet meer afgesneden.</span><span class="sxs-lookup"><span data-stu-id="5a10f-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="5a10f-135">De knop Verwijderen wordt nu ondersteund op het toetsenbord.</span><span class="sxs-lookup"><span data-stu-id="5a10f-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="5a10f-136">Een probleem met de helderheid is verholpen dat zich kon voordoen wanneer op het toetsenbord werd gedrukt.</span><span class="sxs-lookup"><span data-stu-id="5a10f-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="5a10f-137">Er zijn verschillende problemen met demogegevens opgelost.</span><span class="sxs-lookup"><span data-stu-id="5a10f-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="5a10f-138">Er is een probleem verholpen dat gevolgen had voor numerieke velden op de detailpagina.</span><span class="sxs-lookup"><span data-stu-id="5a10f-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="5a10f-139">Het toetsenbord verdwijnt niet meer af en toe op bepaalde apparaten.</span><span class="sxs-lookup"><span data-stu-id="5a10f-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="5a10f-140">Er zijn diverse fouten met de gebruikersinterface (UI) verholpen, zoals fouten die van invloed waren op de kleur en positionering van de achtergrond.</span><span class="sxs-lookup"><span data-stu-id="5a10f-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="5a10f-141">De Russische gebruikersinterface is verbeterd.</span><span class="sxs-lookup"><span data-stu-id="5a10f-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="5a10f-142">Verschillende problemen waardoor het systeem niet meer reageerde, zijn opgelost.</span><span class="sxs-lookup"><span data-stu-id="5a10f-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="5a10f-143">Een probleem in verband met het heropenen van de rekenmachine is opgelost.</span><span class="sxs-lookup"><span data-stu-id="5a10f-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="5a10f-144">**Android-versie**: er is een probleem verholpen waardoor Android 4.4 niet meer reageerde bij het opstarten.</span><span class="sxs-lookup"><span data-stu-id="5a10f-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="5a10f-145">**Android versie:** minimum voor schalen is verlaagd tot 50 procent.</span><span class="sxs-lookup"><span data-stu-id="5a10f-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="5a10f-146">Versie 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-146">Version 2.0.4.0</span></span>

<span data-ttu-id="5a10f-147">Versie 2.0.4.0 was de eerste algemeen beschikbare versie van de mobiele app Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="5a10f-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="5a10f-148">Nieuwe functies, oplossingen en verbeteringen in 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="5a10f-149">Deze versie bevat de volgende nieuwe functies, correcties en verbeteringen die niet beschikbaar waren in de preview-versie:</span><span class="sxs-lookup"><span data-stu-id="5a10f-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="5a10f-150">Als een detailkaart twee labels bevat met identieke gegevens, wordt één van de labels verborgen.</span><span class="sxs-lookup"><span data-stu-id="5a10f-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="5a10f-151">Speciale tekens worden nu standaard weergegeven en de optie om ze te verbergen is uit de gebruikersinstellingen verwijderd.</span><span class="sxs-lookup"><span data-stu-id="5a10f-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="5a10f-152">Uitgeschakelde verzendknoppen worden nu als niet beschikbaar weergegeven in de compacte weergave op de arm.</span><span class="sxs-lookup"><span data-stu-id="5a10f-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="5a10f-153">Met een wijziging in de reekslogica voor besturingselementen verandert de schaal op verschillende apparaten gelijkmatiger.</span><span class="sxs-lookup"><span data-stu-id="5a10f-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="5a10f-154">U hoeft de schaal van lettertypen of knoppen daarom niet zo sterk aan te passen.</span><span class="sxs-lookup"><span data-stu-id="5a10f-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="5a10f-155">Het standaardkleurenthema is gewijzigd in *Donker*.</span><span class="sxs-lookup"><span data-stu-id="5a10f-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="5a10f-156">Het ontbrekende pictogram voor de uitgeschakelde verzendknop is toegevoegd in de weergave in het lint.</span><span class="sxs-lookup"><span data-stu-id="5a10f-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="5a10f-157">Bij time-out-uitzonderingen gaat u nu naar de verbindingspagina in plaats van dat een inlinefout wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5a10f-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="5a10f-158">Als er geen verzendactie beschikbaar is (zoals **OK**, **Ja**, **Accepteren**, **Gereed** of **Voltooid**), wordt de verzendknop uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5a10f-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="5a10f-159">De app-stabiliteit is verbeterd.</span><span class="sxs-lookup"><span data-stu-id="5a10f-159">App stability has been improved.</span></span>
- <span data-ttu-id="5a10f-160">Er is een oplossing voor beveiligingsprobleem [CVE-2021-26701. ](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701)</span><span class="sxs-lookup"><span data-stu-id="5a10f-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="5a10f-161">**Windows-versie:** er is een probleem opgelost in Windows, waarbij menu's niet reageerden nadat het formaat van het venster was gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="5a10f-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="5a10f-162">Bekend probleem in versie 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="5a10f-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="5a10f-163">Het volgende bekende probleem komt in deze versie voor:</span><span class="sxs-lookup"><span data-stu-id="5a10f-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="5a10f-164">Deze versie heeft een probleem met apparaten die Android 4.4 gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5a10f-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="5a10f-165">U kunt problemen ondervinden wanneer u de app met deze versie van Android gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5a10f-165">You might experience issues when you use the app on this Android version.</span></span>
