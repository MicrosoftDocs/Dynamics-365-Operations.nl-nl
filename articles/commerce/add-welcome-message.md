---
title: Een welkomstbericht toevoegen
description: In dit onderwerp wordt beschreven hoe u een welkomstbericht toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797378"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="6d075-103">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="6d075-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6d075-104">In dit onderwerp wordt beschreven hoe u een welkomstbericht toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6d075-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="6d075-105">Een welkomstbericht op uw e-commerce-website kan bezoekers informeren over de lopende verkoop, site-updates of de beschikbaarheid van seizoensgebonden producten.</span><span class="sxs-lookup"><span data-stu-id="6d075-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="6d075-106">Het welkomstbericht wordt ingesteld via de waarschuwingsmodule.</span><span class="sxs-lookup"><span data-stu-id="6d075-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="6d075-107">De waarschuwingsmodule moet worden toegevoegd aan het vak **Fout-/informatieve berichten** van het koptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="6d075-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="6d075-108">In de waarschuwingsmodule kunt u de tekst, de tekstkleur en de uitlijning opgeven.</span><span class="sxs-lookup"><span data-stu-id="6d075-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="6d075-109">U kunt hier ook opgeven of bezoekers van de site het bericht kunnen sluiten.</span><span class="sxs-lookup"><span data-stu-id="6d075-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="6d075-110">Wanneer een welkomstbericht wordt toegevoegd aan een gedeeld koptekstfragment, wordt dit weergegeven op elke pagina met de sjabloon waarin het gedeelde koptekstfragment wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6d075-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="6d075-111">Voer de volgende stappen uit om een welkomstbericht aan uw site toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="6d075-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="6d075-112">Ga naar uw site in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="6d075-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="6d075-113">Selecteer **Fragmenten**.</span><span class="sxs-lookup"><span data-stu-id="6d075-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="6d075-114">Selecteer het koptekstfragment waaraan u het bericht wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6d075-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="6d075-115">Vouw in de overzichtsstructuur **Fout-/informatieve berichten** uit.</span><span class="sxs-lookup"><span data-stu-id="6d075-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="6d075-116">Selecteer de waarschuwingsmodule en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d075-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="6d075-117">Als er nog geen waarschuwingsmodule bestaat, selecteert u eerst de knop met het weglatingsteken (**...**) naast **Fout-/informatieve berichten** en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6d075-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="6d075-118">Selecteer in het eigenschappenvenster aan de rechterkant op het tabblad **Gegevens** de optie **Gegevensbron toevoegen** en selecteer vervolgens **Inhoud**.</span><span class="sxs-lookup"><span data-stu-id="6d075-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="6d075-119">Voer in het veld **Invoertekst** de tekst van het welkomstbericht in.</span><span class="sxs-lookup"><span data-stu-id="6d075-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="6d075-120">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het koptekstfragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="6d075-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="6d075-121">Het welkomstbericht verschijnt nu boven aan elke sitepagina die het geselecteerde koptekstfragment gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6d075-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d075-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6d075-122">Additional resources</span></span>

[<span data-ttu-id="6d075-123">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="6d075-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6d075-124">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="6d075-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="6d075-125">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="6d075-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6d075-126">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="6d075-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6d075-127">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="6d075-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="6d075-128">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="6d075-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6d075-129">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="6d075-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
