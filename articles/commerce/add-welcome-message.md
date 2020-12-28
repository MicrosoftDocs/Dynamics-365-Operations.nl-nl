---
title: Een welkomstbericht toevoegen
description: In dit onderwerp wordt beschreven hoe u een welkomstbericht toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411329"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="80977-103">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="80977-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="80977-104">In dit onderwerp wordt beschreven hoe u een welkomstbericht toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="80977-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="80977-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="80977-105">Overview</span></span>

<span data-ttu-id="80977-106">Een welkomstbericht op uw e-commerce-website kan bezoekers informeren over de lopende verkoop, site-updates of de beschikbaarheid van seizoensgebonden producten.</span><span class="sxs-lookup"><span data-stu-id="80977-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="80977-107">Het welkomstbericht wordt ingesteld via de waarschuwingsmodule.</span><span class="sxs-lookup"><span data-stu-id="80977-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="80977-108">De waarschuwingsmodule moet worden toegevoegd aan het vak **Fout-/informatieve berichten** van het koptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="80977-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="80977-109">In de waarschuwingsmodule kunt u de tekst, de tekstkleur en de uitlijning opgeven.</span><span class="sxs-lookup"><span data-stu-id="80977-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="80977-110">U kunt hier ook opgeven of bezoekers van de site het bericht kunnen sluiten.</span><span class="sxs-lookup"><span data-stu-id="80977-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="80977-111">Wanneer een welkomstbericht wordt toegevoegd aan een gedeeld koptekstfragment, wordt dit weergegeven op elke pagina met de sjabloon waarin het gedeelde koptekstfragment wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="80977-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="80977-112">Voer de volgende stappen uit om een welkomstbericht aan uw site toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="80977-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="80977-113">Ga naar uw site in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="80977-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="80977-114">Selecteer **Fragmenten**.</span><span class="sxs-lookup"><span data-stu-id="80977-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="80977-115">Selecteer het koptekstfragment waaraan u het bericht wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="80977-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="80977-116">Vouw in de overzichtsstructuur **Fout-/informatieve berichten** uit.</span><span class="sxs-lookup"><span data-stu-id="80977-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="80977-117">Selecteer de waarschuwingsmodule en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="80977-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="80977-118">Als er nog geen waarschuwingsmodule bestaat, selecteert u eerst de knop met het weglatingsteken (**...**) naast **Fout-/informatieve berichten** en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="80977-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="80977-119">Selecteer in het eigenschappenvenster aan de rechterkant op het tabblad **Gegevens** de optie **Gegevensbron toevoegen** en selecteer vervolgens **Inhoud**.</span><span class="sxs-lookup"><span data-stu-id="80977-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="80977-120">Voer in het veld **Invoertekst** de tekst van het welkomstbericht in.</span><span class="sxs-lookup"><span data-stu-id="80977-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="80977-121">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het koptekstfragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="80977-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="80977-122">Het welkomstbericht verschijnt nu boven aan elke sitepagina die het geselecteerde koptekstfragment gebruikt.</span><span class="sxs-lookup"><span data-stu-id="80977-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80977-123">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="80977-123">Additional resources</span></span>

[<span data-ttu-id="80977-124">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="80977-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="80977-125">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="80977-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="80977-126">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="80977-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="80977-127">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="80977-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="80977-128">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="80977-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="80977-129">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="80977-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="80977-130">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="80977-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

