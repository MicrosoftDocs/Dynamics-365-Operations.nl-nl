---
title: De verbinding met de Talent-klant wordt verbroken
description: In dit onderwerp wordt uitgelegd wat u moet doen als de klant geen verbinding meer heeft met zijn of haar omgeving en niet weet waarom.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d174a8acac3863fb6d9f9431c6bc777cb717470
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008170"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="1cc02-103">De verbinding met de Talent-klant wordt verbroken</span><span class="sxs-lookup"><span data-stu-id="1cc02-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1cc02-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="1cc02-104">**Environment details**</span></span> 

<span data-ttu-id="1cc02-105">Dit probleem kan optreden in alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="1cc02-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="1cc02-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="1cc02-106">**Symptom**</span></span> 

<span data-ttu-id="1cc02-107">De klant heeft geen verbinding meer met zijn of haar omgeving en weet niet waarom.</span><span class="sxs-lookup"><span data-stu-id="1cc02-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="1cc02-108">Een van de volgende foutberichten wordt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="1cc02-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="1cc02-109">De verbinding is verbroken.</span><span class="sxs-lookup"><span data-stu-id="1cc02-109">We've lost your connection.</span></span> <span data-ttu-id="1cc02-110">Klik op Sluiten om verder te gaan met werken.</span><span class="sxs-lookup"><span data-stu-id="1cc02-110">Click Close to continue working.</span></span>
- <span data-ttu-id="1cc02-111">Het lijkt erop dat de netwerkverbinding is verbroken. Klik op Opnieuw proberen om het opnieuw te proberen.</span><span class="sxs-lookup"><span data-stu-id="1cc02-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="1cc02-112">**Rode vlag**</span><span class="sxs-lookup"><span data-stu-id="1cc02-112">**Red flag**</span></span>

<span data-ttu-id="1cc02-113">Dit gebeurt vaak als gebruikers zich in de implementatiefase bevinden, gegevens tussen productie- en testomgevingen vergelijken en vergeten dat ze tussen sessies overschakelen.</span><span class="sxs-lookup"><span data-stu-id="1cc02-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="1cc02-114">Gebruikers ondervinden dit probleem waarschijnlijk als ze zich in deze fase bevinden.</span><span class="sxs-lookup"><span data-stu-id="1cc02-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="1cc02-115">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="1cc02-115">**Issue**</span></span> 

<span data-ttu-id="1cc02-116">**Browsertypen:** Google Chrome Internet Explorer en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1cc02-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="1cc02-117">Microsoft Dynamics 365 Talent verbreekt de verbinding met gebruikers wanneer twee verschillende sessies tegelijkertijd geopend zijn voor dezelfde gebruiker en hetzelfde browsertype.</span><span class="sxs-lookup"><span data-stu-id="1cc02-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="1cc02-118">(bijvoorbeeld wanneer gebruiker A zowel omgeving 1 als omgeving 2 bekijkt in Chrome). Het maakt niet uit of de gebruikers verschillende browservensters of -tabbladen openen.</span><span class="sxs-lookup"><span data-stu-id="1cc02-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="1cc02-119">Als dezelfde gebruikersreferenties worden gebruikt voor de gelijktijdige aanmelding bij omgeving 1 en 2 in hetzelfde browsertype, wordt de verbinding met een van de sessies verbroken.</span><span class="sxs-lookup"><span data-stu-id="1cc02-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="1cc02-120">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="1cc02-120">**Solution**</span></span>

<span data-ttu-id="1cc02-121">Zorg dat altijd slechts één omgeving tegelijk is geopend voor een bepaald browsertype.</span><span class="sxs-lookup"><span data-stu-id="1cc02-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="1cc02-122">Gebruikers kunnen meerdere sessies naar dezelfde omgeving openen (meerdere tabbladen in dezelfde browser).</span><span class="sxs-lookup"><span data-stu-id="1cc02-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="1cc02-123">Gebruikers die tegelijkertijd tussen twee omgevingen willen schakelen, moeten deze omgevingen in verschillende browsertypen openen.</span><span class="sxs-lookup"><span data-stu-id="1cc02-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="1cc02-124">(Gebruiker A kan omgeving 1 bijvoorbeeld in Chrome en omgeving 2 in Microsoft Edge openen.)</span><span class="sxs-lookup"><span data-stu-id="1cc02-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
