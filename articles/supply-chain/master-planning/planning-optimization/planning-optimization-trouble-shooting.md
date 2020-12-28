---
title: Problemen met Planningsoptimalisatie oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425223"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="9cfb5-103">Problemen met Planningsoptimalisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="9cfb5-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cfb5-104">In dit onderwerp wordt beschreven hoe u algemene problemen kunt oplossen die kunnen optreden tijdens het werken met Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="9cfb5-105">De installatie van de invoegtoepassing Planningsoptimalisatie wordt niet voltooid</span><span class="sxs-lookup"><span data-stu-id="9cfb5-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="9cfb5-106">Voor Planningsoptimalisatie is een omgeving met grote beschikbaarheid die Lifecycle Services (LCS) ondersteunt, tier 2 of hoger (geen OneBox-omgeving), met Dynamics 365 Supply Chain Management versie 10.0.7 of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="9cfb5-107">Als u de invoegtoepassing in een OneBox-omgeving probeert te installeren, wordt de installatie niet voltooid.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="9cfb5-108">**Oplossing**: annuleer de installatie en gebruik een omgeving met hoge beschikbaarheid, tier 2 of hoger (geen Onebox-omgeving).</span><span class="sxs-lookup"><span data-stu-id="9cfb5-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="9cfb5-109">Het plannen van batchtaken mislukt wanneer de Planningsoptimalisatie is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="9cfb5-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="9cfb5-110">Wanneer u Planningsoptimalisatie inschakelt, wordt de ingebouwde engine voor hoofdplanningen automatisch uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="9cfb5-111">Als bestaande batchtaken voor hoofdplanningen die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine mislukken als zij worden geactiveerd terwijl de optie Planningsoptimalisatie gebruiken is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="9cfb5-112">Er kan een fout bericht worden weergegeven, zoals *Met deze bewerking wordt een hoofdplanning geactiveerd die niet wordt ondersteund wanneer Planningsoptimalisatie is ingeschakeld*.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="9cfb5-113">**Oplossing**: annuleer alle batchtaken voor hoofdplanningen die zijn gemaakt voor de ingebouwde planningsengine van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="9cfb5-114">Resultaten van Planningsoptimalisatie verschillen van eerdere resultaten</span><span class="sxs-lookup"><span data-stu-id="9cfb5-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="9cfb5-115">Planningsoptimalisatie wijkt op bepaalde gebieden af van het ingebouwde hoofdplanningsontwerp.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="9cfb5-116">Dit kan ook worden veroorzaakt door functies die in behandeling zijn.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="9cfb5-117">**Oplossing**: voer Analyse aanpassen aan Planningsoptimalisatie uit en analyseer vervolgens de resultaten terwijl u de bijbehorende documentatie raadpleegt om de gevolgen te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="9cfb5-118">Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="9cfb5-119">Hoofdplanning respecteert de time fence voor behoefteplanning niet</span><span class="sxs-lookup"><span data-stu-id="9cfb5-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="9cfb5-120">Dit wordt veroorzaakt door een functie die in behandeling is voor Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="9cfb5-121">**Oplossing**: totdat de functie in behandeling beschikbaar is, kunt u geplande orders filteren of verwijderen om voorstellen buiten de time fence voor behoefteplanning te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="9cfb5-122">Kan Planningsoptimalisatie niet inschakelen</span><span class="sxs-lookup"><span data-stu-id="9cfb5-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="9cfb5-123">De **verbindingsstatus** moet **Verbonden** zijn voordat u **Planningsoptimalisatie gebruiken** kunt instellen op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="9cfb5-124">Zie [Aan de slag met Planningsoptimalisatie](get-started.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="9cfb5-125">**Oplossing**: zorg ervoor dat de invoegtoepassing Planningsoptimalisatie correct is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="9cfb5-126">Foutbericht wordt weergegeven tijdens CTP</span><span class="sxs-lookup"><span data-stu-id="9cfb5-126">Error message is shown during CTP</span></span>

<span data-ttu-id="9cfb5-127">Als u CTP (Capable to Promise) probeert uit te voeren vanuit een verkooporder wanneer Planningsoptimalisatie is ingeschakeld, wordt het volgende foutbericht weergegeven: *Met deze bewerking wordt een hoofdplanning geactiveerd die niet wordt ondersteund wanneer Planningsoptimalisatie is ingeschakeld*.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="9cfb5-128">Dit houdt verband met een functie die in behandeling is en die wordt gepland als onderdeel van de ondersteuning voor productieorders.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="9cfb5-129">**Oplossing:** vermijd CTP-berekeningen wanneer Planningsoptimalisatie is ingeschakeld totdat CTP-ondersteuning beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="9cfb5-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cfb5-130">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="9cfb5-130">Additional resources</span></span>

[<span data-ttu-id="9cfb5-131">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="9cfb5-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9cfb5-132">Analyse aanpassen aan Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="9cfb5-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
