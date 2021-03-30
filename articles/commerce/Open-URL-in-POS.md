---
title: URL openen in POS
description: Dit onderwerp biedt een overzicht van verbeteringen die zijn aangebracht in de functies voor het zoeken van producten en klanten in Dynamics 365 Commerce.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 91d10ac383ed860a69d2d62f4a246c5ca8690b3c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206794"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="c5079-103">URL openen in POS</span><span class="sxs-lookup"><span data-stu-id="c5079-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5079-104">In dit onderwerp wordt beschreven hoe u een knop in Retail POS kunt configureren zodat hiermee een URL wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c5079-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="c5079-105">Hiervoor hoeft geen code te worden aangepast en dit kan worden geconfigureerd door iemand die geen ontwikkelaar is.</span><span class="sxs-lookup"><span data-stu-id="c5079-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="c5079-106">Met deze functie kan een knop in POS zo worden geconfigureerd dat via de ontwerpfunctie van het knoppenraster een URL wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c5079-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="c5079-107">Dit wordt op dit moment ondersteund in de volgende configuraties:</span><span class="sxs-lookup"><span data-stu-id="c5079-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="c5079-108">Openen in nieuw venster.</span><span class="sxs-lookup"><span data-stu-id="c5079-108">Open in new window.</span></span>
- <span data-ttu-id="c5079-109">Openen in POS.</span><span class="sxs-lookup"><span data-stu-id="c5079-109">Open within POS.</span></span>
- <span data-ttu-id="c5079-110">Een native app openen.</span><span class="sxs-lookup"><span data-stu-id="c5079-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="c5079-111">Openen in nieuw venster</span><span class="sxs-lookup"><span data-stu-id="c5079-111">Open in new window</span></span>

<span data-ttu-id="c5079-112">Deze configuratie bepaalt of de URL in een nieuw venster of in de app wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c5079-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="c5079-113">Als de knop is geconfigureerd om een web-URL in de app te openen, zijn het navigatievenster aan de zijkant en de bovenste balk van POS zichtbaar en beschikbaar voor gebruikersinteractie.</span><span class="sxs-lookup"><span data-stu-id="c5079-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="c5079-114">Is de knop geconfigureerd om in een nieuw venster te worden geopend, dan wordt de URL geopend in een nieuw app-venster in Modern POS voor Windows en in een nieuw browsertabblad in alle andere POS-clients.</span><span class="sxs-lookup"><span data-stu-id="c5079-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="c5079-115">Om dit mogelijk te maken, moet u de optie **Openen in nieuw venster** selecteren als u de URL configureert.</span><span class="sxs-lookup"><span data-stu-id="c5079-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="c5079-116">Openen in POS</span><span class="sxs-lookup"><span data-stu-id="c5079-116">Open within POS</span></span>

<span data-ttu-id="c5079-117">Het openen van een web-URL in POS wordt momenteel alleen ondersteund voor Modern POS in Windows.</span><span class="sxs-lookup"><span data-stu-id="c5079-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="c5079-118">In andere clients wordt hieraan gewerkt en is dit in toekomstige updates wel mogelijk.</span><span class="sxs-lookup"><span data-stu-id="c5079-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="c5079-119">Om dit mogelijk te maken, moet u de optie **Openen in nieuw venster** niet selecteren als u de URL configureert.</span><span class="sxs-lookup"><span data-stu-id="c5079-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="c5079-120">Een native app openen</span><span class="sxs-lookup"><span data-stu-id="c5079-120">Open a native app</span></span>

<span data-ttu-id="c5079-121">Met deze functie kunt u niet-web-URL's opgeven om een native app te openen.</span><span class="sxs-lookup"><span data-stu-id="c5079-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="c5079-122">U kunt bijvoorbeeld URL-protocollen, zoals MailTo, SIP, IM of MSTEAMS, opgeven. Deze kunnen vervolgens worden verwerkt door respectievelijke native apps op het hostapparaat.</span><span class="sxs-lookup"><span data-stu-id="c5079-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="c5079-123">Om dit mogelijk te maken, moet u de optie **Openen in nieuw venster** selecteren als u de URL configureert.</span><span class="sxs-lookup"><span data-stu-id="c5079-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="c5079-124">Raadpleeg voor Windows-computers [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) om de standaardprotocolkoppelingen in te stellen als u uw computer instelt met Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="c5079-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="c5079-125">Als u MDM, bijvoorbeeld Intune, gebruikt voor het beheren van uw Windows-computers, raadpleegt u [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="c5079-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="c5079-126">Als u als ontwikkelaar een aangepaste website bouwt, raadpleegt u [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="c5079-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="c5079-127">Naadloos een native app openen</span><span class="sxs-lookup"><span data-stu-id="c5079-127">Open a native app seamlessly</span></span>

<span data-ttu-id="c5079-128">Windows, iOS en Android bieden ook ondersteuning voor een vloeiendere methode voor het openen van apps, op basis van de koppeling van app-protocollen.</span><span class="sxs-lookup"><span data-stu-id="c5079-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="c5079-129">Als uw app nog niet is geconfigureerd om vanuit een webbrowser te worden geopend, moet u hiervoor mogelijk de hulp van een ontwikkelaar inroepen.</span><span class="sxs-lookup"><span data-stu-id="c5079-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="c5079-130">Raadpleeg voor Windows [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="c5079-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="c5079-131">Raadpleeg voor iOS [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="c5079-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="c5079-132">Raadpleeg voor Android [Handling Android App Links](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="c5079-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="c5079-133">Klant</span><span class="sxs-lookup"><span data-stu-id="c5079-133">Client</span></span>                | <span data-ttu-id="c5079-134">Openen in nieuw venster</span><span class="sxs-lookup"><span data-stu-id="c5079-134">Open in new window</span></span> | <span data-ttu-id="c5079-135">Native app openen</span><span class="sxs-lookup"><span data-stu-id="c5079-135">Open native app</span></span> | <span data-ttu-id="c5079-136">Openen in POS</span><span class="sxs-lookup"><span data-stu-id="c5079-136">Open within POS</span></span> | <span data-ttu-id="c5079-137">Details</span><span class="sxs-lookup"><span data-stu-id="c5079-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="c5079-138">Modern POS in Windows</span><span class="sxs-lookup"><span data-stu-id="c5079-138">Modern POS on Windows</span></span> | <span data-ttu-id="c5079-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="c5079-139">✓\*</span></span>                | <span data-ttu-id="c5079-140">✓</span><span class="sxs-lookup"><span data-stu-id="c5079-140">✓</span></span>               | <span data-ttu-id="c5079-141">✓</span><span class="sxs-lookup"><span data-stu-id="c5079-141">✓</span></span>              | <span data-ttu-id="c5079-142">\* Wordt geopend in nieuw Modern POS-venster</span><span class="sxs-lookup"><span data-stu-id="c5079-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="c5079-143">Cloud-POS</span><span class="sxs-lookup"><span data-stu-id="c5079-143">Cloud POS</span></span>             | <span data-ttu-id="c5079-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="c5079-144">✓\*</span></span>                | <span data-ttu-id="c5079-145">✓</span><span class="sxs-lookup"><span data-stu-id="c5079-145">✓</span></span>               | <span data-ttu-id="c5079-146">X</span><span class="sxs-lookup"><span data-stu-id="c5079-146">X</span></span>              | <span data-ttu-id="c5079-147">\* Wordt geopend op nieuw browsertabblad</span><span class="sxs-lookup"><span data-stu-id="c5079-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="c5079-148">Modern POS in iOS</span><span class="sxs-lookup"><span data-stu-id="c5079-148">Modern POS on iOS</span></span>     | <span data-ttu-id="c5079-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="c5079-149">✓\*</span></span>                | <span data-ttu-id="c5079-150">✓</span><span class="sxs-lookup"><span data-stu-id="c5079-150">✓</span></span>               | <span data-ttu-id="c5079-151">X</span><span class="sxs-lookup"><span data-stu-id="c5079-151">X</span></span>              | <span data-ttu-id="c5079-152">\* Wordt geopend op nieuw browsertabblad</span><span class="sxs-lookup"><span data-stu-id="c5079-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="c5079-153">Modern POS in Android</span><span class="sxs-lookup"><span data-stu-id="c5079-153">Modern POS on Android</span></span> | <span data-ttu-id="c5079-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="c5079-154">✓\*</span></span>                | <span data-ttu-id="c5079-155">✓</span><span class="sxs-lookup"><span data-stu-id="c5079-155">✓</span></span>               | <span data-ttu-id="c5079-156">X</span><span class="sxs-lookup"><span data-stu-id="c5079-156">X</span></span>              | <span data-ttu-id="c5079-157">\* Wordt geopend op nieuw browsertabblad</span><span class="sxs-lookup"><span data-stu-id="c5079-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="c5079-158">Voordat u begint</span><span class="sxs-lookup"><span data-stu-id="c5079-158">Before you begin</span></span>

<span data-ttu-id="c5079-159">Controleer voordat u begint hoe u [schermindelingen voor het verkooppunt (POS)](pos-screen-layouts.md) configureert.</span><span class="sxs-lookup"><span data-stu-id="c5079-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="c5079-160">URL openen in POS</span><span class="sxs-lookup"><span data-stu-id="c5079-160">Open URL in POS</span></span>

<span data-ttu-id="c5079-161">Als u een URL wilt configureren om in POS te worden geopend, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="c5079-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="c5079-162">Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS \> Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="c5079-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="c5079-163">Selecteer **Knoppenrasters \> Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="c5079-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="c5079-164">Maak een nieuwe knop.</span><span class="sxs-lookup"><span data-stu-id="c5079-164">Create a new button.</span></span>
4. <span data-ttu-id="c5079-165">Selecteer **Knopeigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="c5079-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="c5079-166">Selecteer **URL openen** als de actie.</span><span class="sxs-lookup"><span data-stu-id="c5079-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="c5079-167">Voer de URL in die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5079-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="c5079-168">Configureer of de URL in een nieuw venster wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c5079-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]