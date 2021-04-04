---
title: Een functionaliteitsprofiel voor detailhandel maken
description: In dit onderwerp wordt beschreven hoe u een nieuw functionaliteitsprofiel maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478303"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="fd1a4-103">Een functionaliteitsprofiel voor detailhandel maken</span><span class="sxs-lookup"><span data-stu-id="fd1a4-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd1a4-104">In dit onderwerp wordt beschreven hoe u een nieuw functionaliteitsprofiel maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fd1a4-105">Het functionaliteitsprofiel voor commerce biedt verschillende instellingen voor online kanalen.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="fd1a4-106">In elk kanaal moet een functionaliteitsprofiel worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="fd1a4-107">Een functionaliteitsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="fd1a4-107">Create a functionality profile</span></span>

<span data-ttu-id="fd1a4-108">Volg deze stappen om een functionaliteitsprofiel te maken.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="fd1a4-109">Ga in het navigatievenster naar **Modules \> Kanaalinstelling \> POS-profielen \> Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="fd1a4-110">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fd1a4-111">Voer in het veld **Profiel** een id in voor het profiel ('FN006' in de voorbeeldafbeelding hieronder).</span><span class="sxs-lookup"><span data-stu-id="fd1a4-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="fd1a4-112">Voer in het veld **Beschrijving** een waarde in ('Profiel van Adventure Works' in de voorbeeldafbeelding hieronder).</span><span class="sxs-lookup"><span data-stu-id="fd1a4-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="fd1a4-113">Selecteer in de sectie **Algemeen** een land voor de landinstelling **ISO**.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="fd1a4-114">Pas in de sectie **Algemeen** zo nodig de overige instellingen aan.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="fd1a4-115">Selecteer in de sectie **Algemeen** een **id ontvangstbewijsprofiel** voor ontvangstbewijzen per e-mail.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="fd1a4-116">Pas in de sectie **Functies** zo nodig instellingen aan.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="fd1a4-117">Pas in de sectie **Bedrag** zo nodig instellingen aan.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="fd1a4-118">Pas in de sectie **Infocodes** zo nodig instellingen aan.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="fd1a4-119">Pas in de sectie **Ontvangstbewijsnummering** zo nodig de overige instellingen aan.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="fd1a4-120">In de volgende afbeelding ziet u een voorbeeld van een functionaliteitsprofiel.</span><span class="sxs-lookup"><span data-stu-id="fd1a4-120">The following image shows an example functionality profile.</span></span>
  
![Voorbeeld van functionaliteitprofiel](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="fd1a4-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fd1a4-122">Additional resources</span></span>

[<span data-ttu-id="fd1a4-123">Informatiecodes en informatiecodegroepen</span><span class="sxs-lookup"><span data-stu-id="fd1a4-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="fd1a4-124">Nieuw adresboek maken</span><span class="sxs-lookup"><span data-stu-id="fd1a4-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="fd1a4-125">Overzicht van schermindeling</span><span class="sxs-lookup"><span data-stu-id="fd1a4-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="fd1a4-126">Retail Hardware Station configureren en installeren</span><span class="sxs-lookup"><span data-stu-id="fd1a4-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
