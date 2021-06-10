---
title: Problemen met analytische rapporten oplossen
description: In dit artikel wordt uitgelegd wat u moet doen als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053534"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="81482-103">Problemen met analytische rapporten oplossen</span><span class="sxs-lookup"><span data-stu-id="81482-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="81482-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="81482-104">**Issue**</span></span>

<span data-ttu-id="81482-105">De gegevenswijzigingen van een klant worden niet op het tabblad **Analyses** van de werkgebieden van de klant weergegeven.</span><span class="sxs-lookup"><span data-stu-id="81482-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="81482-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="81482-106">**Cause**</span></span>

<span data-ttu-id="81482-107">Standaard worden Microsoft Power BI-rapporten elke vier uur vernieuwd, volgens het schema van de batchtaak Meting implementeren.</span><span class="sxs-lookup"><span data-stu-id="81482-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="81482-108">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="81482-108">**Resolution**</span></span>

<span data-ttu-id="81482-109">Dit probleem kan ook een kwestie van timing zijn.</span><span class="sxs-lookup"><span data-stu-id="81482-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="81482-110">Volg deze stappen om de batchtaak te starten en de werkgebieden voor analyses bij te werken.</span><span class="sxs-lookup"><span data-stu-id="81482-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="81482-111">Open de pagina **Batchtaken** via **Systeembeheer \> Koppelingen \> Batchtaken \> Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="81482-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="81482-112">U kunt ook Zoeken gebruiken en **Batchtaken** invoeren.</span><span class="sxs-lookup"><span data-stu-id="81482-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="81482-113">Zoek de taak **Meting implementeren** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="81482-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="81482-114">Selecteer **Bewerken** boven aan de pagina en stel de geplande begindatum/-tijd in waarmee de analyses dichter bij de huidige tijd worden vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="81482-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchtaken](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]