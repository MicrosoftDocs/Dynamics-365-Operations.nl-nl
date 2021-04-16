---
title: Geïntegreerde nummerreeks voor taak-id's
description: Deze functie biedt één uniforme nummerreeks die taak-id's genereert voor de modules Productiebeheer, Productie-uitvoering en Tijd en aanwezigheid.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824936"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="f1142-103">Geïntegreerde nummerreeks voor taak-id's</span><span class="sxs-lookup"><span data-stu-id="f1142-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1142-104">Deze functie biedt één uniforme nummerreeks die taak-id's genereert voor de modules Productiebeheer, Productie-uitvoering en Tijd en aanwezigheid.</span><span class="sxs-lookup"><span data-stu-id="f1142-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="f1142-105">Voorheen kon u voor elk van deze modules een andere nummerreeks kiezen, wat kon leiden tot conflicterende taak-id's als twee of meer van deze reeksen een identieke indeling gebruikten.</span><span class="sxs-lookup"><span data-stu-id="f1142-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="f1142-106">Een dergelijk conflict kan leiden tot gegevensbeschadiging.</span><span class="sxs-lookup"><span data-stu-id="f1142-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="f1142-107">Deze functie inschakelen voor uw systeem</span><span class="sxs-lookup"><span data-stu-id="f1142-107">Turn on this feature for your system</span></span>

<span data-ttu-id="f1142-108">Als de functie die in dit onderwerp wordt beschreven, nog niet in het systeem aanwezig is, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Geïntegreerde nummerreeks voor taak-id's* in.</span><span class="sxs-lookup"><span data-stu-id="f1142-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="f1142-109">De geïntegreerde nummerreeks voor taak-id's instellen</span><span class="sxs-lookup"><span data-stu-id="f1142-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="f1142-110">Nadat u deze functie hebt ingeschakeld, worden de bestaande instellingen voor de nummerreeks van **Taakidentificatie** op de parameterpagina's voor de modules Productiebeheer, Productie-uitvoering en Tijd en aanwezigheid afgeschaft en wordt een nieuw veld **Geïntegreerde taak-id** toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f1142-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="f1142-111">De waarde **Geïntegreerde taak-id** wordt gedeeld door alle drie de modules, zodat alle modules naar dezelfde nummerreeks verwijzen.</span><span class="sxs-lookup"><span data-stu-id="f1142-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="f1142-112">Taak-id's zullen daarom uniek zijn in alle drie de modules en er zal nooit een conflict optreden.</span><span class="sxs-lookup"><span data-stu-id="f1142-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="f1142-113">De geïntegreerde nummerreeks voor taak-id's instellen:</span><span class="sxs-lookup"><span data-stu-id="f1142-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="f1142-114">Schakel de functie in zoals beschreven in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="f1142-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="f1142-115">Identificeer de nummerreeks die u wilt gebruiken voor uw geïntegreerde taak-id's of maak een nieuwe.</span><span class="sxs-lookup"><span data-stu-id="f1142-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="f1142-116">Zie [Overzicht van nummerreeksen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f1142-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="f1142-117">Ga naar de pagina **Parameters van productiebeheer**, **Parameters van Productie-uitvoering** of **Parameters in Tijd en aanwezigheid**.</span><span class="sxs-lookup"><span data-stu-id="f1142-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="f1142-118">Het maakt niet uit welke u kiest, want wanneer u deze instelling op een van deze pagina's maakt, worden alle andere pagina's automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f1142-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="f1142-119">Open het tabblad **Nummerreeksen** op uw geselecteerde pagina met parameters.</span><span class="sxs-lookup"><span data-stu-id="f1142-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="f1142-120">Wijs de **nummerreekscode** die u eerder hebt geïdentificeerd toe aan de rij **Geïntegreerde taak-id's** van het raster.</span><span class="sxs-lookup"><span data-stu-id="f1142-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
