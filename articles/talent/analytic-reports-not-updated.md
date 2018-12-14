---
title: Analytische rapporten worden niet bijgewerkt
description: In dit onderwerp wordt uitgelegd wat u moet doen als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="159a1-103">Analytische rapporten worden niet bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="159a1-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="159a1-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="159a1-104">**Issue**</span></span>

<span data-ttu-id="159a1-105">De gegevenswijzigingen van een klant worden niet op het tabblad **Analyses** van de werkgebieden van de klant weergegeven.</span><span class="sxs-lookup"><span data-stu-id="159a1-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="159a1-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="159a1-106">**Cause**</span></span>

<span data-ttu-id="159a1-107">Standaard worden Microsoft Power BI-rapporten elke vier uur vernieuwd, volgens het schema van de batchtaak Meting implementeren.</span><span class="sxs-lookup"><span data-stu-id="159a1-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="159a1-108">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="159a1-108">**Resolution**</span></span>

<span data-ttu-id="159a1-109">Dit probleem kan ook een kwestie van timing zijn.</span><span class="sxs-lookup"><span data-stu-id="159a1-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="159a1-110">Volg deze stappen om de batchtaak te starten en de werkgebieden voor analyses bij te werken.</span><span class="sxs-lookup"><span data-stu-id="159a1-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="159a1-111">Open de pagina **Batchtaken** via **Systeembeheer \> Koppelingen \> Batchtaken \> Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="159a1-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="159a1-112">U kunt ook Zoeken gebruiken en **Batchtaken** invoeren.</span><span class="sxs-lookup"><span data-stu-id="159a1-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="159a1-113">Zoek de taak **Meting implementeren** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="159a1-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="159a1-114">Selecteer **Bewerken** boven aan de pagina en stel de geplande begindatum/-tijd in waarmee de analyses dichter bij de huidige tijd worden vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="159a1-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchtaken](media/batch-jobs.png)

