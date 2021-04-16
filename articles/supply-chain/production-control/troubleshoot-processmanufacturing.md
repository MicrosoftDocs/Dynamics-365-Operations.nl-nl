---
title: Problemen met procesproductie oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met procesproductie.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 938820b6cd2bb470b440fea7b70124efc0faf7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824985"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="b77b9-103">Problemen met procesproductie oplossen</span><span class="sxs-lookup"><span data-stu-id="b77b9-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="b77b9-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met procesproductie.</span><span class="sxs-lookup"><span data-stu-id="b77b9-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="b77b9-105">Wanneer ik het taakkaartapparaat gebruik om een gedeeltelijke hoeveelheid te rapporteren voor de laatste taak in een productieorder, worden alle eerdere taken op die order met de status In uitvoering automatisch beëindigd.</span><span class="sxs-lookup"><span data-stu-id="b77b9-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="b77b9-106">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="b77b9-106">This behavior is by design.</span></span> <span data-ttu-id="b77b9-107">Op de pagina **Standaardwaarden productieorder**, op het tabblad **Rapporteren als gereed** is een optie met de naam **Eindmarkering van route**.</span><span class="sxs-lookup"><span data-stu-id="b77b9-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="b77b9-108">Als dit onderwerp is ingesteld op *Ja*, wordt een routekaartjournaal geboekt wanneer een werknemer taakkaartapparaat of taakkaartterminal gebruikt om de laatste bewerking te melden.</span><span class="sxs-lookup"><span data-stu-id="b77b9-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="b77b9-109">In dit journaal worden alle bewerkingen gemarkeerd als voltooid en worden alle productietaken beëindigd.</span><span class="sxs-lookup"><span data-stu-id="b77b9-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="b77b9-110">Wanneer de optie **Eindmarkering van route** is ingesteld op *Ja*, houdt het systeem geen rekening met de taakstatus die de werknemer heeft geselecteerd bij het melden van de laatste bewerking.</span><span class="sxs-lookup"><span data-stu-id="b77b9-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="b77b9-111">Het systeem houdt er ook geen rekening mee of de werk nemer een volledige of gedeeltelijke hoeveelheid rapporteert.</span><span class="sxs-lookup"><span data-stu-id="b77b9-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="b77b9-112">Wanneer ik een voorraadafsluiting probeer, wordt het volgende waarschuwingsbericht weergegeven: "Geen uitvoering van kostprijsberekening via terugwaarts afboeken geregistreerd met datum %1 overeenkomend met een einde-periode."</span><span class="sxs-lookup"><span data-stu-id="b77b9-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="b77b9-113">Als u in releases vóór release 10.0.13 de kostenstroom voor de lean-productie niet gebruikt, wordt tijdens de voorraadafsluiting het volgende onjuiste waarschuwingsbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="b77b9-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="b77b9-114">U staat op het punt een voorraadafsluiting uit te voeren met datum %1.</span><span class="sxs-lookup"><span data-stu-id="b77b9-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="b77b9-115">Geen uitvoering van kostprijsberekening via terugwaarts afboeken geregistreerd met datum %1 overeenkomend met een periode-einde.</span><span class="sxs-lookup"><span data-stu-id="b77b9-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="b77b9-116">Vergeet niet een kostprijsberekening via terugwaarts afboeken uit te voeren met datum %1 overeenkomend met een periode-einde.</span><span class="sxs-lookup"><span data-stu-id="b77b9-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="b77b9-117">De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b77b9-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="b77b9-118">Dit probleem is opgelost in release 10.0.13 en hoger.</span><span class="sxs-lookup"><span data-stu-id="b77b9-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="b77b9-119">Zie voor meer informatie [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="b77b9-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]