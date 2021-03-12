---
title: Een vervaldatum voor een productiestroomversie definiëren
description: Om de geldigheid en de verwerking van een productiestroomversie te voltooien op een bepaalde datum of een actieve versie door een nieuwe versie te vervangen, moet u een vervaldatum op de versieregel instellen.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a595ca4ff9f6753631303b656d56735320a22a69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975080"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="a0a54-103">Een vervaldatum voor een productiestroomversie definiëren</span><span class="sxs-lookup"><span data-stu-id="a0a54-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0a54-104">Om de geldigheid en de verwerking van een productiestroomversie te voltooien op een bepaalde datum of een actieve versie door een nieuwe versie te vervangen, moet u een vervaldatum op de versieregel instellen.</span><span class="sxs-lookup"><span data-stu-id="a0a54-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="a0a54-105">Het is niet nodig om de versie te deactiveren.</span><span class="sxs-lookup"><span data-stu-id="a0a54-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="a0a54-106">Stel een vervaldatum in om een productiestroomversie te beëindigen</span><span class="sxs-lookup"><span data-stu-id="a0a54-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="a0a54-107">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="a0a54-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="a0a54-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a0a54-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a0a54-109">Selecteer een productiestroom met een versie die al is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="a0a54-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="a0a54-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a0a54-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a0a54-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="a0a54-111">Click Edit.</span></span>
5. <span data-ttu-id="a0a54-112">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a0a54-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="a0a54-113">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="a0a54-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="a0a54-114">Een nieuwe versie wordt niet gestart of geactiveerd voor de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="a0a54-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="a0a54-115">Het is ook niet meer mogelijk om taken voor deze productiestroom te maken of te starten.</span><span class="sxs-lookup"><span data-stu-id="a0a54-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="a0a54-116">U kunt gestarte taken na de vervaldatum nog uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a0a54-116">You can still complete started jobs after the expiration date.</span></span>  

