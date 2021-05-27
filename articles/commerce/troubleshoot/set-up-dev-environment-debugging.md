---
title: Een ontwikkelomgeving voor e-commerce instellen voor foutopsporing op een virtuele machine van Tier 1 Retail Server
description: In dit onderwerp wordt uitgelegd hoe u een ontwikkelomgeving voor e-commerce kunt instellen voor foutopsporing op een virtuele machine (VM) van Tier 1 Retail Server.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 38a616c418c3b32490c9adaf69a69af0d47d3478
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019441"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="c4153-103">Een ontwikkelomgeving voor e-commerce instellen voor foutopsporing op een virtuele machine van Tier 1 Retail Server</span><span class="sxs-lookup"><span data-stu-id="c4153-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4153-104">In dit onderwerp wordt uitgelegd hoe u een ontwikkelomgeving voor e-commerce kunt instellen voor foutopsporing op een virtuele machine (VM) van Tier 1 Retail Server.</span><span class="sxs-lookup"><span data-stu-id="c4153-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="c4153-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c4153-105">Description</span></span>

<span data-ttu-id="c4153-106">Microsoft Dynamics 365 Commerce Tier 1-omgevingen worden meestal geïmplementeerd voor Commerce runtime (CRT) en POS-uitbreidingsontwikkeling (Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="c4153-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="c4153-107">Dit zijn zelfstandige omgevingen.</span><span class="sxs-lookup"><span data-stu-id="c4153-107">They are standalone environments.</span></span> <span data-ttu-id="c4153-108">Vanwege de SaaS-aard (Software as a Service) van de architectuur, zijn geen e-commerce-onderdelen inbegrepen.</span><span class="sxs-lookup"><span data-stu-id="c4153-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="c4153-109">In sommige scenario's wilt u mogelijk aanroepen voor uitbreidingen in een Tier 1-omgeving testen, zodat u foutopsporing kunt uitvoeren vanuit e-commerce-onderdelen.</span><span class="sxs-lookup"><span data-stu-id="c4153-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="c4153-110">Zie [Foutopsporing voor een Tier 1-ontwikkelomgeving voor Commerce](../e-commerce-extensibility/debug-tier-1.md) voor algemene instructies.</span><span class="sxs-lookup"><span data-stu-id="c4153-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="c4153-111">Wanneer u fouten opspoort in een Tier 1-omgeving, omdat de site nu een andere Retail Server aanroept, kunnen cross-serveroproepen verschillende fouten veroorzaken met betrekking tot het beleid voor inhoudsbeveiliging.</span><span class="sxs-lookup"><span data-stu-id="c4153-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="c4153-112">In de volgende afbeelding ziet u een voorbeeld van een fout die kan optreden wanneer een variant wordt geselecteerd op een productdetailpagina.</span><span class="sxs-lookup"><span data-stu-id="c4153-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Fout bij het selecteren van een variant op een productdetailpagina](media/unhandled-rejection-error.jpg)

<span data-ttu-id="c4153-114">In de volgende afbeelding ziet u een voorbeeld van een vergelijkbare fout in de foutopsporingstools van een browser (F12 Developer Tools).</span><span class="sxs-lookup"><span data-stu-id="c4153-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="c4153-115">In het foutbericht wordt gesproken over overtreding van de richtlijn voor inhoudsbeveiliging.</span><span class="sxs-lookup"><span data-stu-id="c4153-115">The error message mentions violation of the content security policy directive.</span></span>

![Fout in programma's voor foutopsporing](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="c4153-117">Oplossing</span><span class="sxs-lookup"><span data-stu-id="c4153-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="c4153-118">Het beleid voor inhoudsbeveiliging uitschakelen voor de site in Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="c4153-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="c4153-119">Selecteer de site waaraan u werkt.</span><span class="sxs-lookup"><span data-stu-id="c4153-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="c4153-120">Selecteer **Instellingen** en selecteer vervolgens **Uitbreidingen**.</span><span class="sxs-lookup"><span data-stu-id="c4153-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="c4153-121">Selecteer op het tabblad **Beveiligingsbeleid voor inhoud** de optie **Beleid voor inhoudsbeveiliging uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="c4153-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="c4153-122">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="c4153-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="c4153-123">Aanmelden met B2C (Business-to-consumer) werkt niet in een lokale ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="c4153-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="c4153-124">U kunt echter als gast uitchecken gebruiken of dummypagina's bouwen om waar nodig het aanmelden van gebruikers te simuleren.</span><span class="sxs-lookup"><span data-stu-id="c4153-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4153-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c4153-125">Additional resources</span></span>

[<span data-ttu-id="c4153-126">Aan de slag met ontwikkeling van online uitbreiding van e-commerce</span><span class="sxs-lookup"><span data-stu-id="c4153-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="c4153-127">Beleid voor inhoudsbeveiliging (CSP) op de e-commercesite beheren</span><span class="sxs-lookup"><span data-stu-id="c4153-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
