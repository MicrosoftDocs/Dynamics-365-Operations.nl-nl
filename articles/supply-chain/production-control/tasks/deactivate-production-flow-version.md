---
title: Een productiestroomversie deactiveren
description: Als een actieve productiestroomversie niet meer nodig is, kan deze worden gedeactiveerd.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091cafd02bd568323e586373fc8b0f983afee343
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565249"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="02788-103">Een productiestroomversie deactiveren</span><span class="sxs-lookup"><span data-stu-id="02788-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02788-104">Als een actieve productiestroomversie niet meer nodig is, kan deze worden gedeactiveerd.</span><span class="sxs-lookup"><span data-stu-id="02788-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="02788-105">U kunt deze optie alleen gebruiken als alle kanbanregels en activiteiten zijn beëindigd en niet opnieuw worden geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="02788-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="02788-106">Merk op dat de vervaldatum van alle kanbanregels voor deze productiestroomversie wordt bijgewerkt met de huidige datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="02788-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="02788-107">Als u een actieve productiestroomversie wilt wijzigen, kunt u een vervaldatum instellen voor de actieve versie en een nieuwe versie maken.</span><span class="sxs-lookup"><span data-stu-id="02788-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="02788-108">Hierdoor kunt u uw productiebewerkingen voortzetten tijdens het voorbereiden van de nieuwe versie en gerelateerde kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="02788-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="02788-109">Als u een actieve productiestroomversie wilt laten vervallen, stelt u een vervaldatum in.</span><span class="sxs-lookup"><span data-stu-id="02788-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="02788-110">In dit opzicht is deactivering meer een uitzondering dan een regel.</span><span class="sxs-lookup"><span data-stu-id="02788-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="02788-111">Voor deze procedure hebt u een productiestroom nodig met een versie die kan worden gedeactiveerd.</span><span class="sxs-lookup"><span data-stu-id="02788-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="02788-112">Probeer dit niet in een productieomgeving als u niet 100% zeker weet of de versie volledig verouderd is.</span><span class="sxs-lookup"><span data-stu-id="02788-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="02788-113">Een productiestroomversie deactiveren</span><span class="sxs-lookup"><span data-stu-id="02788-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="02788-114">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="02788-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="02788-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="02788-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="02788-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="02788-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="02788-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="02788-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="02788-118">Klik op Deactiveren.</span><span class="sxs-lookup"><span data-stu-id="02788-118">Click Deactivate.</span></span>
    * <span data-ttu-id="02788-119">Ga niet verder als u niet 100% zeker weet of deze productiestroomversie verouderd is.</span><span class="sxs-lookup"><span data-stu-id="02788-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="02788-120">Als u op OK klikt, verlopen alle actieve kanbanregels en wordt een direct einde gemaakt aan alle productie- en aanvulactiviteiten van deze productiestroomversie.</span><span class="sxs-lookup"><span data-stu-id="02788-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="02788-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="02788-121">Click OK.</span></span>

