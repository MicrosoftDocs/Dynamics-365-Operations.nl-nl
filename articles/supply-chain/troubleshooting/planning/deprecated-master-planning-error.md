---
title: Er wordt een foutbericht weergegeven wanneer u de ingebouwde hoofdplanning-engine gebruikt
description: Wanneer u de afgeschafte, ingebouwde hoofdplanning-engine gebruikt, wordt een foutbericht weergegeven.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294048"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="a6171-103">Er wordt een foutbericht weergegeven wanneer u de ingebouwde hoofdplanning-engine gebruikt</span><span class="sxs-lookup"><span data-stu-id="a6171-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="a6171-104">Foutcode: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="a6171-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="a6171-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="a6171-105">Symptoms</span></span>

<span data-ttu-id="a6171-106">Wanneer u voor de hoofdplanning de afgeschafte, ingebouwde hoofdplanning-engine gebruikt, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="a6171-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="a6171-107">Dit foutbericht wordt weergegeven omdat de ingebouwde engine voor hoofdplanning werd gebruikt voor scenario's die worden ondersteund door Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="a6171-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="a6171-108">U moet nu migreren naar Planningsoptimalisatie, omdat de huidige ingebouwde hoofdplanning wordt afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="a6171-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="a6171-109">De uitvoering van deze hoofdplanning is succesvol voltooid.</span><span class="sxs-lookup"><span data-stu-id="a6171-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="a6171-110">Als uw migratie sterke afhankelijkheden heeft van functies die in behandeling zijn, kan een uitzondering voor het gebruik van de ingebouwde hoofdplanningsengine worden aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="a6171-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="a6171-111">Vul de volgende vragenlijst in om aan de slag te gaan en, indien relevant, vraag een uitzondering aan van de migratie naar Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="a6171-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="a6171-112">Plannings- en uitzonderingsvragenlijst voor optimalisatie</span><span class="sxs-lookup"><span data-stu-id="a6171-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="a6171-113">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="a6171-113">Cause</span></span>

<span data-ttu-id="a6171-114">Als u de planning uitvoert zonder productiebeheerfuncties te gebruiken, kunt u overwegen een migratie uit te voeren naar Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="a6171-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="a6171-115">De ingebouwde hoofdplanning-engine wordt afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="a6171-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="a6171-116">Als u deze wilt blijven gebruiken zonder het foutbericht te ontvangen, moet u daarom een uitzondering aanvragen bij Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6171-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="a6171-117">Oplossing</span><span class="sxs-lookup"><span data-stu-id="a6171-117">Resolution</span></span>

<span data-ttu-id="a6171-118">Zie [Migratie naar Planningsoptimalisatie voor hoofdplanning](/dynamics365/supply-chain/master-planning/new-master-planning-engine) voor meer informatie over het migreren naar Planningsoptimalisatie of het toepassen van een uitzondering, zodat u in plaats te migreren de afgeschafte, ingebouwde planning-engine kunt blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a6171-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
