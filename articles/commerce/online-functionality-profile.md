---
title: Een online functionaliteitsprofiel maken
description: In dit onderwerp wordt beschreven hoe u een online functionaliteitsprofiel maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: be78b92858979b8bb009a4699eff96379ef7cef3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791097"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="18404-103">Een online functionaliteitsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="18404-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18404-104">Dit onderwerp bevat een overzicht van het instellen van een online functionaliteitsprofiel voor Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18404-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="18404-105">Het online functionaliteitsprofiel biedt verschillende instellingen voor online kanalen.</span><span class="sxs-lookup"><span data-stu-id="18404-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="18404-106">In elk online kanaal moet een online functionaliteitsprofiel worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="18404-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="18404-107">Een online functionaliteitsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="18404-107">Create an online functionality profile</span></span>

<span data-ttu-id="18404-108">In de volgende procedure wordt beschreven hoe u een online functionaliteitsprofiel maakt vanuit de Commerce Headquarters-app.</span><span class="sxs-lookup"><span data-stu-id="18404-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="18404-109">Ga in het navigatievenster naar **Modules \> Kanaalinstelling \> Onlinewinkel instellen \> Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="18404-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="18404-110">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="18404-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="18404-111">Voer in het veld **Profiel** een id voor het profiel in.</span><span class="sxs-lookup"><span data-stu-id="18404-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="18404-112">Voer in het veld **Beschrijving** een waarde in ('Profiel van Adventure Works' in de voorbeeldafbeelding hieronder).</span><span class="sxs-lookup"><span data-stu-id="18404-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="18404-113">Wijzig indien nodig in de sectie **Functies** de instellingen **WINKELWAGEN**, **DETAILHANDELKLANTEN** of **UITCHECKEN**.</span><span class="sxs-lookup"><span data-stu-id="18404-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="18404-114">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="18404-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="18404-115">In de volgende afbeelding ziet u een voorbeeld van een online functionaliteitsprofiel.</span><span class="sxs-lookup"><span data-stu-id="18404-115">The following image shows an example online functionality profile.</span></span>
  
![Voorbeeld van online functionaliteitprofiel](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="18404-117">Functies</span><span class="sxs-lookup"><span data-stu-id="18404-117">Functions</span></span>

- <span data-ttu-id="18404-118">**Producten samenvoegen**: als deze functie is ingeschakeld, kan de winkelwagen de hoeveelheid bijwerken wanneer hetzelfde artikel meerdere keren wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="18404-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="18404-119">**Uitchecken zonder betalingen toestaan**: als deze functie is ingeschakeld, wordt het scenario verwerkt waarbij artikelen die aan de winkelwagen zijn toegevoegd een prijs van $ 0,00 hebben.</span><span class="sxs-lookup"><span data-stu-id="18404-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="18404-120">**Klant maken in asynchrone modus**: dit is een verouderde instelling die van toepassing is op e-Commerce-kanalen van derden en is niet van toepassing op de Dynamics 365 e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="18404-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18404-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="18404-121">Additional resources</span></span>

[<span data-ttu-id="18404-122">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="18404-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="18404-123">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="18404-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="18404-124">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="18404-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="18404-125">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="18404-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="18404-126">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="18404-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
