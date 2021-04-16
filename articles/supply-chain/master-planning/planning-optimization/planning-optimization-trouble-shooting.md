---
title: Problemen met Planningsoptimalisatie oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met Planningsoptimalisatie.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812878"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="79fa4-103">Problemen met Planningsoptimalisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="79fa4-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79fa4-104">In dit onderwerp wordt beschreven hoe u algemene problemen kunt oplossen die kunnen optreden tijdens het werken met Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="79fa4-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="79fa4-105">De installatie van de invoegtoepassing Planningsoptimalisatie wordt niet voltooid</span><span class="sxs-lookup"><span data-stu-id="79fa4-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="79fa4-106">Voor Planningsoptimalisatie is een omgeving met grote beschikbaarheid die Lifecycle Services (LCS) ondersteunt, tier 2 of hoger (geen OneBox-omgeving), met Dynamics 365 Supply Chain Management versie 10.0.7 of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="79fa4-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="79fa4-107">Als u de invoegtoepassing in een OneBox-omgeving probeert te installeren, wordt de installatie niet voltooid.</span><span class="sxs-lookup"><span data-stu-id="79fa4-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="79fa4-108">**Oplossing**: annuleer de installatie en gebruik een omgeving met hoge beschikbaarheid, tier 2 of hoger (geen Onebox-omgeving).</span><span class="sxs-lookup"><span data-stu-id="79fa4-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="79fa4-109">Het plannen van batchtaken mislukt wanneer de Planningsoptimalisatie is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="79fa4-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="79fa4-110">Wanneer u Planningsoptimalisatie inschakelt, wordt de ingebouwde engine voor hoofdplanningen automatisch uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="79fa4-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="79fa4-111">Als bestaande batchtaken voor hoofdplanningen die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine mislukken als zij worden geactiveerd terwijl de optie Planningsoptimalisatie gebruiken is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="79fa4-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="79fa4-112">Er kan een fout bericht worden weergegeven, zoals *Met deze bewerking wordt een hoofdplanning geactiveerd die niet wordt ondersteund wanneer Planningsoptimalisatie is ingeschakeld*.</span><span class="sxs-lookup"><span data-stu-id="79fa4-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="79fa4-113">**Oplossing**: annuleer alle batchtaken voor hoofdplanningen die zijn gemaakt voor de ingebouwde planningsengine van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79fa4-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="79fa4-114">Resultaten van Planningsoptimalisatie verschillen van eerdere resultaten</span><span class="sxs-lookup"><span data-stu-id="79fa4-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="79fa4-115">Planningsoptimalisatie wijkt op bepaalde gebieden af van het ingebouwde hoofdplanningsontwerp.</span><span class="sxs-lookup"><span data-stu-id="79fa4-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="79fa4-116">Dit kan ook worden veroorzaakt door functies die in behandeling zijn.</span><span class="sxs-lookup"><span data-stu-id="79fa4-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="79fa4-117">**Oplossing**: voer Analyse aanpassen aan Planningsoptimalisatie uit en analyseer vervolgens de resultaten terwijl u de bijbehorende documentatie raadpleegt om de gevolgen te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="79fa4-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="79fa4-118">Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="79fa4-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="79fa4-119">Kan Planningsoptimalisatie niet inschakelen</span><span class="sxs-lookup"><span data-stu-id="79fa4-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="79fa4-120">De **verbindingsstatus** moet **Verbonden** zijn voordat u **Planningsoptimalisatie gebruiken** kunt instellen op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="79fa4-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="79fa4-121">Zie [Aan de slag met Planningsoptimalisatie](get-started.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="79fa4-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="79fa4-122">**Oplossing**: zorg ervoor dat de invoegtoepassing Planningsoptimalisatie correct is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="79fa4-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="79fa4-123">Foutbericht wordt weergegeven tijdens CTP</span><span class="sxs-lookup"><span data-stu-id="79fa4-123">Error message is shown during CTP</span></span>

<span data-ttu-id="79fa4-124">Als u CTP (Capable to Promise) probeert uit te voeren vanuit een verkooporder wanneer Planningsoptimalisatie is ingeschakeld, wordt het volgende foutbericht weergegeven: *Met deze bewerking wordt een hoofdplanning geactiveerd die niet wordt ondersteund wanneer Planningsoptimalisatie is ingeschakeld*.</span><span class="sxs-lookup"><span data-stu-id="79fa4-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="79fa4-125">Dit houdt verband met een functie die in behandeling is en die wordt gepland als onderdeel van de ondersteuning voor productieorders.</span><span class="sxs-lookup"><span data-stu-id="79fa4-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="79fa4-126">**Oplossing:** vermijd CTP-berekeningen wanneer Planningsoptimalisatie is ingeschakeld totdat CTP-ondersteuning beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="79fa4-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79fa4-127">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="79fa4-127">Additional resources</span></span>

[<span data-ttu-id="79fa4-128">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="79fa4-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="79fa4-129">Analyse aanpassen aan Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="79fa4-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]