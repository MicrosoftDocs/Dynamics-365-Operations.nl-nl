---
title: De verbinding met de client wordt verbroken
description: In dit artikel wordt uitgelegd wat u moet doen als de klant geen verbinding meer heeft met zijn of haar omgeving en niet weet waarom.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e9ec43ad0a7d121eb247d81d4b506556a0fa2214
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794896"
---
# <a name="client-disconnects"></a><span data-ttu-id="17d66-103">De verbinding met de client wordt verbroken</span><span class="sxs-lookup"><span data-stu-id="17d66-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="17d66-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="17d66-104">**Environment details**</span></span> 

<span data-ttu-id="17d66-105">Dit probleem kan optreden in alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="17d66-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="17d66-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="17d66-106">**Symptom**</span></span> 

<span data-ttu-id="17d66-107">De klant heeft geen verbinding meer met zijn of haar omgeving en weet niet waarom.</span><span class="sxs-lookup"><span data-stu-id="17d66-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="17d66-108">Een van de volgende foutberichten wordt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="17d66-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="17d66-109">De verbinding is verbroken.</span><span class="sxs-lookup"><span data-stu-id="17d66-109">We've lost your connection.</span></span> <span data-ttu-id="17d66-110">Klik op Sluiten om verder te gaan met werken.</span><span class="sxs-lookup"><span data-stu-id="17d66-110">Click Close to continue working.</span></span>
- <span data-ttu-id="17d66-111">Het lijkt erop dat de netwerkverbinding is verbroken. Klik op Opnieuw proberen om het opnieuw te proberen.</span><span class="sxs-lookup"><span data-stu-id="17d66-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="17d66-112">**Rode vlag**</span><span class="sxs-lookup"><span data-stu-id="17d66-112">**Red flag**</span></span>

<span data-ttu-id="17d66-113">Dit gebeurt vaak als gebruikers zich in de implementatiefase bevinden, gegevens tussen productie- en testomgevingen vergelijken en vergeten dat ze tussen sessies overschakelen.</span><span class="sxs-lookup"><span data-stu-id="17d66-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="17d66-114">Gebruikers ondervinden dit probleem waarschijnlijk als ze zich in deze fase bevinden.</span><span class="sxs-lookup"><span data-stu-id="17d66-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="17d66-115">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="17d66-115">**Issue**</span></span> 

<span data-ttu-id="17d66-116">**Browsertypen:** Google Chrome Internet Explorer en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="17d66-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="17d66-117">Microsoft Dynamics 365 Human Resources verbreekt de verbinding met gebruikers wanneer twee verschillende sessies tegelijkertijd geopend zijn voor dezelfde gebruiker en hetzelfde browsertype.</span><span class="sxs-lookup"><span data-stu-id="17d66-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="17d66-118">(bijvoorbeeld wanneer gebruiker A zowel omgeving 1 als omgeving 2 bekijkt in Chrome). Het maakt niet uit of de gebruikers verschillende browservensters of -tabbladen openen.</span><span class="sxs-lookup"><span data-stu-id="17d66-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="17d66-119">Als dezelfde gebruikersreferenties worden gebruikt voor de gelijktijdige aanmelding bij omgeving 1 en 2 in hetzelfde browsertype, wordt in Human Resources de verbinding met een van de sessies verbroken.</span><span class="sxs-lookup"><span data-stu-id="17d66-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="17d66-120">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="17d66-120">**Solution**</span></span>

<span data-ttu-id="17d66-121">Zorg dat altijd slechts één omgeving tegelijk is geopend voor een bepaald browsertype.</span><span class="sxs-lookup"><span data-stu-id="17d66-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="17d66-122">Gebruikers kunnen meerdere sessies naar dezelfde omgeving openen (meerdere tabbladen in dezelfde browser).</span><span class="sxs-lookup"><span data-stu-id="17d66-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="17d66-123">Gebruikers die tegelijkertijd tussen twee omgevingen willen schakelen, moeten deze omgevingen in verschillende browsertypen openen.</span><span class="sxs-lookup"><span data-stu-id="17d66-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="17d66-124">(Gebruiker A kan omgeving 1 bijvoorbeeld in Chrome en omgeving 2 in Microsoft Edge openen.)</span><span class="sxs-lookup"><span data-stu-id="17d66-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]