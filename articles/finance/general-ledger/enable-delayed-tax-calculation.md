---
title: Vertraagde belastingberekening inschakelen in journalen
description: In dit onderwerp wordt uitgelegd hoe u de functie Vertraagde belastingberekening inschakelt om de belastingberekening te helpen verbeteren als het aantal journaalregels zeer groot is.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d4ce0343ac766b30d532be0866a381dc520fd462
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977138"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="9e6f0-103">Vertraagde belastingberekening inschakelen in journalen</span><span class="sxs-lookup"><span data-stu-id="9e6f0-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="9e6f0-104">In dit onderwerp wordt uitgelegd hoe u btw-berekening in journalen kunt vertragen.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="9e6f0-105">Deze mogelijkheid helpt de prestaties van belastingberekeningen te verbeteren wanneer er veel journaalregels zijn.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="9e6f0-106">Standaard worden btw-bedragen op journaalregels berekend telkens wanneer btw-gerelateerde velden worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="9e6f0-107">Deze velden bevatten de velden voor btw-groepen en btw-groepen voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="9e6f0-108">Eventuele wijzigingen in een journaalregel leiden ertoe dat belastingbedragen opnieuw worden berekend voor alle journaalregels.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="9e6f0-109">Hoewel gebruikers hiermee belastingbedragen kunnen zien die in realtime zijn berekend, kan dit ook invloed hebben op de prestaties als het aantal journaalregels erg groot is.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="9e6f0-110">Met de functie Vertraagde belastingberekening kunt u de btw-berekening in journalen vertragen en zodoende prestatieproblemen oplossen.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="9e6f0-111">Als deze functie is ingeschakeld, worden btw-bedragen alleen berekend wanneer een gebruiker **Btw** selecteert of het journaal boekt.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="9e6f0-112">U kunt de berekening van de btw op drie niveaus vertragen:</span><span class="sxs-lookup"><span data-stu-id="9e6f0-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="9e6f0-113">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="9e6f0-113">Legal entity</span></span>
- <span data-ttu-id="9e6f0-114">Journaalnaam</span><span class="sxs-lookup"><span data-stu-id="9e6f0-114">Journal name</span></span>
- <span data-ttu-id="9e6f0-115">Journaalkoptekst</span><span class="sxs-lookup"><span data-stu-id="9e6f0-115">Journal header</span></span>

<span data-ttu-id="9e6f0-116">Het systeem geeft prioriteit aan de instelling voor de journaalkoptekst.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="9e6f0-117">Standaard wordt deze instelling overgenomen van de journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="9e6f0-118">De instelling voor de journaalnaam wordt standaard overgenomen van de instelling op de pagina **Grootboekparameters** wanneer de journaalnaam wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="9e6f0-119">In de volgende secties wordt uitgelegd hoe u vertraagde belastingberekening inschakelt voor rechtspersonen, journaalnamen en journaalkopteksten.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="9e6f0-120">Vertraagde btw-berekening inschakelen op het niveau van de rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="9e6f0-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="9e6f0-121">Ga naar **Grootboek \> Grootboek instellen \> Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="9e6f0-122">Stel op het tabblad **Btw** op het sneltabblad **Algemeen** de optie **Vertraagde belastingberekening** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Afbeelding van grootboekparameters](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="9e6f0-124">Vertraagde btw-berekening inschakelen op het niveau van de journaalnaam</span><span class="sxs-lookup"><span data-stu-id="9e6f0-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="9e6f0-125">Ga naar **Grootboek \> Journaalinstellingen \> Journaalnamen**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="9e6f0-126">Stel in de sectie **Btw** op het sneltabblad **Algemeen** de optie **Vertraagde belastingberekening** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Afbeelding van journaalnamen](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="9e6f0-128">Vertraagde btw-berekening inschakelen op het niveau van de journaalkoptekst</span><span class="sxs-lookup"><span data-stu-id="9e6f0-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="9e6f0-129">Ga naar **Grootboek \> Journaalboekingen \> Algemene journalen**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="9e6f0-130">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-130">Select **New**.</span></span>
3. <span data-ttu-id="9e6f0-131">Selecteer een journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-131">Select a journal name.</span></span>
4. <span data-ttu-id="9e6f0-132">Stel op het tabblad **Instellingen** de optie **Vertraagde belastingberekening** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9e6f0-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Afbeelding van grootboekpagina](media/delayed-tax-calculation-journal-header.png)
