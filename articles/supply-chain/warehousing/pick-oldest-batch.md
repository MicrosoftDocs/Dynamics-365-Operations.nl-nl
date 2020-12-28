---
title: Oudste batch verzamelen op een mobiel apparaat
description: In dit onderwerp wordt beschreven hoe u de opties voor het verzamelen van de oudste batch kunt instellen en toepassen op een mobiel apparaat.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f235c34d6369c6f0584a7bac1c1be75f3d84c9c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425323"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="4f081-103">Oudste batch verzamelen op een mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="4f081-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f081-104">U hebt toegang tot de configuratie **Oudste batch verzamelen** via het menu van een mobiel apparaat en hiermee kunt u magazijnmedewerkers dwingen of waarschuwen dat zij de oudste batch picken op hun huidige locatie.</span><span class="sxs-lookup"><span data-stu-id="4f081-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="4f081-105">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="4f081-105">Where it applies</span></span>
<span data-ttu-id="4f081-106">Oudste batch verzamelen wordt geconfigureerd in menu-items van mobiel apparaten en beïnvloedt het verzamelen voor de onderste artikelen in de batch.</span><span class="sxs-lookup"><span data-stu-id="4f081-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="4f081-107">De configuratie voor Oudste batch verzamelen instellen</span><span class="sxs-lookup"><span data-stu-id="4f081-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="4f081-108">Voor artikelen die zijn ingesteld op gebruik van bestaand werk kan **Oudste batch verzamelen** worden ingesteld op **Geen**, **Waarschuwen** of **Forceren** in het menu van een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="4f081-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="4f081-109">**Geen**: Werknemers ontvangen geen berichten en ze mogen elke batch in hun locatie verzamelen.</span><span class="sxs-lookup"><span data-stu-id="4f081-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="4f081-110">**Waarschuwing** en **Forceren**: Een lijst van de batch(es) met de oudste vervaldatum verschijnt boven het batchbesturingselement wanneer de werknemer een batch selecteert.</span><span class="sxs-lookup"><span data-stu-id="4f081-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="4f081-111">Als de locatie wordt aangestuurd via nummerplaten, wordt een lijst met nummerplaten die de oudste batch bevatten weergegeven boven het besturingselement nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="4f081-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="4f081-112">**Waarschuwing**: Als een werknemer een nummerplaat of een batch kiest die niet in de weergegeven lijst staat, wordt het besturingselement blanco gemaakt en een waarschuwing getoond dat er een oudere batch is die moet worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4f081-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="4f081-113">Om te kunnen doorgaan met het werk, mag de werknemer dezelfde nummerplaat of batch opnieuw selecteren.</span><span class="sxs-lookup"><span data-stu-id="4f081-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="4f081-114">**Forceren**: Werknemers blijven het bericht ontvangen dat er een oudere batch is, die moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4f081-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>
