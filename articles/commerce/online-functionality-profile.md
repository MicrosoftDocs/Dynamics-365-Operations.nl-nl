---
title: Een online functionaliteitsprofiel maken
description: In dit onderwerp wordt beschreven hoe u een online functionaliteitsprofiel maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003367"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="c6dd1-103">Een online functionaliteitsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="c6dd1-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c6dd1-104">Dit onderwerp bevat een overzicht van het instellen van een online functionaliteitsprofiel voor Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6dd1-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="c6dd1-105">Overview</span></span>

<span data-ttu-id="c6dd1-106">Het online functionaliteitsprofiel biedt verschillende instellingen voor online kanalen.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="c6dd1-107">In elk online kanaal moet een online functionaliteitsprofiel worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="c6dd1-108">Een online functionaliteitsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="c6dd1-108">Create an online functionality profile</span></span>

<span data-ttu-id="c6dd1-109">In de volgende procedure wordt beschreven hoe u een online functionaliteitsprofiel maakt vanuit de Commerce Headquarters-app.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="c6dd1-110">Ga in het navigatievenster naar **Modules \> Kanaalinstelling \> Onlinewinkel instellen \> Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="c6dd1-111">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c6dd1-112">Voer in het veld **Profiel** een id voor het profiel in.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="c6dd1-113">Voer in het veld **Beschrijving** een waarde in ('Profiel van Adventure Works' in de voorbeeldafbeelding hieronder).</span><span class="sxs-lookup"><span data-stu-id="c6dd1-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="c6dd1-114">Wijzig indien nodig in de sectie **Functies** de instellingen **WINKELWAGEN**, **DETAILHANDELKLANTEN** of **UITCHECKEN**.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="c6dd1-115">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c6dd1-116">In de volgende afbeelding ziet u een voorbeeld van een online functionaliteitsprofiel.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-116">The following image shows an example online functionality profile.</span></span>
  
![Voorbeeld van online functionaliteitprofiel](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="c6dd1-118">Functies</span><span class="sxs-lookup"><span data-stu-id="c6dd1-118">Functions</span></span>

- <span data-ttu-id="c6dd1-119">**Producten samenvoegen**: als deze functie is ingeschakeld, kan de winkelwagen de hoeveelheid bijwerken wanneer hetzelfde artikel meerdere keren wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="c6dd1-120">**Uitchecken zonder betalingen toestaan**: als deze functie is ingeschakeld, wordt het scenario verwerkt waarbij artikelen die aan de winkelwagen zijn toegevoegd een prijs van $ 0,00 hebben.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="c6dd1-121">**Klant maken in asynchrone modus**: dit is een verouderde instelling die van toepassing is op e-Commerce-kanalen van derden en is niet van toepassing op de Dynamics 365 e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="c6dd1-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6dd1-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c6dd1-122">Additional resources</span></span>

[<span data-ttu-id="c6dd1-123">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="c6dd1-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c6dd1-124">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="c6dd1-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c6dd1-125">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="c6dd1-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="c6dd1-126">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="c6dd1-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="c6dd1-127">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="c6dd1-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
