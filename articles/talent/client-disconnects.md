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
ms.openlocfilehash: 02df31b56c0e960a16ec2aadd8b1e817e0b6ec65
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898452"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="cb8df-103">De verbinding met de Talent-klant wordt verbroken</span><span class="sxs-lookup"><span data-stu-id="cb8df-103">Talent client disconnects</span></span>

<span data-ttu-id="cb8df-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="cb8df-104">**Environment details**</span></span> 

<span data-ttu-id="cb8df-105">Dit probleem kan optreden in alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="cb8df-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="cb8df-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="cb8df-106">**Symptom**</span></span> 

<span data-ttu-id="cb8df-107">De klant heeft geen verbinding meer met zijn of haar omgeving en weet niet waarom.</span><span class="sxs-lookup"><span data-stu-id="cb8df-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="cb8df-108">Een van de volgende foutberichten wordt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="cb8df-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="cb8df-109">De verbinding is verbroken.</span><span class="sxs-lookup"><span data-stu-id="cb8df-109">We've lost your connection.</span></span> <span data-ttu-id="cb8df-110">Klik op Sluiten om verder te gaan met werken.</span><span class="sxs-lookup"><span data-stu-id="cb8df-110">Click Close to continue working.</span></span>
- <span data-ttu-id="cb8df-111">Het lijkt erop dat de netwerkverbinding is verbroken. Klik op Opnieuw proberen om het opnieuw te proberen.</span><span class="sxs-lookup"><span data-stu-id="cb8df-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="cb8df-112">**Rode vlag**</span><span class="sxs-lookup"><span data-stu-id="cb8df-112">**Red flag**</span></span>

<span data-ttu-id="cb8df-113">Dit gebeurt vaak als gebruikers zich in de implementatiefase bevinden, gegevens tussen productie- en testomgevingen vergelijken en vergeten dat ze tussen sessies overschakelen.</span><span class="sxs-lookup"><span data-stu-id="cb8df-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="cb8df-114">Gebruikers ondervinden dit probleem waarschijnlijk als ze zich in deze fase bevinden.</span><span class="sxs-lookup"><span data-stu-id="cb8df-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="cb8df-115">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="cb8df-115">**Issue**</span></span> 

<span data-ttu-id="cb8df-116">**Browsertypen:** Google Chrome Internet Explorer en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cb8df-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="cb8df-117">Microsoft Dynamics 365 Talent verbreekt de verbinding met gebruikers wanneer twee verschillende sessies tegelijkertijd geopend zijn voor dezelfde gebruiker en hetzelfde browsertype.</span><span class="sxs-lookup"><span data-stu-id="cb8df-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="cb8df-118">(bijvoorbeeld wanneer gebruiker A zowel omgeving 1 als omgeving 2 bekijkt in Chrome). Het maakt niet uit of de gebruikers verschillende browservensters of -tabbladen openen.</span><span class="sxs-lookup"><span data-stu-id="cb8df-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="cb8df-119">Als dezelfde gebruikersreferenties worden gebruikt voor de gelijktijdige aanmelding bij omgeving 1 en 2 in hetzelfde browsertype, wordt de verbinding met een van de sessies verbroken.</span><span class="sxs-lookup"><span data-stu-id="cb8df-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="cb8df-120">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="cb8df-120">**Solution**</span></span>

<span data-ttu-id="cb8df-121">Zorg dat altijd slechts één omgeving tegelijk is geopend voor een bepaald browsertype.</span><span class="sxs-lookup"><span data-stu-id="cb8df-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="cb8df-122">Gebruikers kunnen meerdere sessies naar dezelfde omgeving openen (meerdere tabbladen in dezelfde browser).</span><span class="sxs-lookup"><span data-stu-id="cb8df-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="cb8df-123">Gebruikers die tegelijkertijd tussen twee omgevingen willen schakelen, moeten deze omgevingen in verschillende browsertypen openen.</span><span class="sxs-lookup"><span data-stu-id="cb8df-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="cb8df-124">(Gebruiker A kan omgeving 1 bijvoorbeeld in Chrome en omgeving 2 in Microsoft Edge openen.)</span><span class="sxs-lookup"><span data-stu-id="cb8df-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
