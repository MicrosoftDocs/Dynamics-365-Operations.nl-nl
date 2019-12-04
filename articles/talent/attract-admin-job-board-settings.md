---
title: Broadbean-integratie inschakelen in Attract
description: In dit onderwerp wordt uitgelegd hoe u Microsoft Dynamics 365 Talent - Attract kunt configureren om vacatures te plaatsen op externe banensites zoals Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 10b612711e81b2b368ed23fdd95ab6a66451f0ca
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833203"
---
# <a name="enable-broadbean-integration-in-attract"></a><span data-ttu-id="598e2-103">Broadbean-integratie inschakelen in Attract</span><span class="sxs-lookup"><span data-stu-id="598e2-103">Enable Broadbean integration in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="598e2-104">U wilt uw openstaande posities aan zoveel mogelijk kandidaten voorleggen.</span><span class="sxs-lookup"><span data-stu-id="598e2-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="598e2-105">Wervingssites, zoals Broadbean, helpen u bij het realiseren van dit doel.</span><span class="sxs-lookup"><span data-stu-id="598e2-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="598e2-106">Met Microsoft Dynamics 365 Talent: Attract kunt u nu functies publiceren naar Broadbean en Microsoft biedt voortdurend nieuwe aanbiedingen in dit gebied.</span><span class="sxs-lookup"><span data-stu-id="598e2-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="598e2-107">Als u functies naar externe sites wilt publiceren, moet u over de [Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) beschikken.</span><span class="sxs-lookup"><span data-stu-id="598e2-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="598e2-108">Als u functies naar Broadbean wilt publiceren via Attract, moet u beschikken over een Broadbean-abonnement.</span><span class="sxs-lookup"><span data-stu-id="598e2-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="598e2-109">Van deze functie kan momenteel een voorbeeld worden bekeken.</span><span class="sxs-lookup"><span data-stu-id="598e2-109">This feature is currently in preview.</span></span> <span data-ttu-id="598e2-110">Als u de functie wilt proberen, moet u [deze inschakelen in de beheerinstellingen van Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="598e2-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="598e2-111">Broadbean-integratie configureren</span><span class="sxs-lookup"><span data-stu-id="598e2-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="598e2-112">Meld u aan bij Attract als beheerder.</span><span class="sxs-lookup"><span data-stu-id="598e2-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="598e2-113">Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek van de pagina en selecteer vervolgens **Beheercentrum**.</span><span class="sxs-lookup"><span data-stu-id="598e2-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="598e2-114">Neem contact op met Broadbean en voer uw gegevens in **Gebruikersnaam**, **Client-ID** en **Coderingstoken** in.</span><span class="sxs-lookup"><span data-stu-id="598e2-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="598e2-115">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="598e2-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="598e2-116">Uw Broadbean-referenties zijn gevoelig en vertrouwelijk.</span><span class="sxs-lookup"><span data-stu-id="598e2-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="598e2-117">Bewaar deze daarom zorgvuldig en deel ze op verantwoorde wijze.</span><span class="sxs-lookup"><span data-stu-id="598e2-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="598e2-118">Iedereen met een beheerdersrol in Attract kan deze referenties weergeven.</span><span class="sxs-lookup"><span data-stu-id="598e2-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="598e2-119">Microsoft en Attract zijn niet betrokken bij het maken en onderhouden van deze waarden.</span><span class="sxs-lookup"><span data-stu-id="598e2-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="598e2-120">Het is uw verantwoordelijkheid ze om up-to-date te houden in Attract en te werken met Broadbean om eventuele problemen op te lossen die betrekking hebben op uw referenties.</span><span class="sxs-lookup"><span data-stu-id="598e2-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
