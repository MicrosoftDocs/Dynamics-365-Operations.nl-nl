---
title: Een welkomstbericht toevoegen
description: In dit onderwerp wordt beschreven hoe u een welkomstbericht toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001249"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="a5c63-103">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="a5c63-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a5c63-104">In dit onderwerp wordt beschreven hoe u een welkomstbericht toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="a5c63-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="a5c63-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a5c63-105">Overview</span></span>

<span data-ttu-id="a5c63-106">Een welkomstbericht op uw e-commerce-website kan bezoekers informeren over de lopende verkoop, site-updates of de beschikbaarheid van seizoensgebonden producten.</span><span class="sxs-lookup"><span data-stu-id="a5c63-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="a5c63-107">Het welkomstbericht wordt ingesteld via de waarschuwingsmodule.</span><span class="sxs-lookup"><span data-stu-id="a5c63-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="a5c63-108">De waarschuwingsmodule moet worden toegevoegd aan het vak **Fout-/informatieve berichten** van het koptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="a5c63-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="a5c63-109">In de waarschuwingsmodule kunt u de tekst, de tekstkleur en de uitlijning opgeven.</span><span class="sxs-lookup"><span data-stu-id="a5c63-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="a5c63-110">U kunt hier ook opgeven of bezoekers van de site het bericht kunnen sluiten.</span><span class="sxs-lookup"><span data-stu-id="a5c63-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="a5c63-111">Wanneer een welkomstbericht wordt toegevoegd aan een gedeeld koptekstfragment, wordt dit weergegeven op elke pagina met de sjabloon waarin het gedeelde koptekstfragment wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a5c63-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="a5c63-112">Voer de volgende stappen uit om een welkomstbericht aan uw site toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a5c63-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="a5c63-113">Ga in Dynamics 365 Commerce naar uw site.</span><span class="sxs-lookup"><span data-stu-id="a5c63-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="a5c63-114">Selecteer **Fragmenten**.</span><span class="sxs-lookup"><span data-stu-id="a5c63-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="a5c63-115">Selecteer het koptekstfragment waaraan u het bericht wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a5c63-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="a5c63-116">Vouw in de overzichtsstructuur **Fout-/informatieve berichten**uit.</span><span class="sxs-lookup"><span data-stu-id="a5c63-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="a5c63-117">Selecteer de waarschuwingsmodule.</span><span class="sxs-lookup"><span data-stu-id="a5c63-117">Select the alert module.</span></span>

    <span data-ttu-id="a5c63-118">Als er nog geen waarschuwingsmodule bestaat, selecteert u de knop met hetweglatingsteken (**...**) naast **Fout-/informatieve berichten** en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a5c63-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="a5c63-119">Selecteer de waarschuwingsmodule en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5c63-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="a5c63-120">Selecteer in het eigenschappenvenster aan de rechterkant op het tabblad **Gegevens** de optie **Gegevensbron toevoegen** en selecteer vervolgens **Inhoud**.</span><span class="sxs-lookup"><span data-stu-id="a5c63-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="a5c63-121">Voer in het veld **Invoertekst** de tekst van het welkomstbericht in.</span><span class="sxs-lookup"><span data-stu-id="a5c63-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="a5c63-122">Sla het koptekstfragment op, check het in en publiceer het.</span><span class="sxs-lookup"><span data-stu-id="a5c63-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="a5c63-123">Het welkomstbericht verschijnt nu boven aan elke sitepagina die het geselecteerde koptekstfragment gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a5c63-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5c63-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a5c63-124">Additional resources</span></span>

[<span data-ttu-id="a5c63-125">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="a5c63-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="a5c63-126">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="a5c63-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="a5c63-127">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="a5c63-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="a5c63-128">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="a5c63-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="a5c63-129">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="a5c63-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="a5c63-130">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="a5c63-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="a5c63-131">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="a5c63-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

