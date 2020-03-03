---
title: Problemen met analytische rapporten oplossen
description: In dit artikel wordt uitgelegd wat u moet doen als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008567"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="6b249-103">Problemen met analytische rapporten oplossen</span><span class="sxs-lookup"><span data-stu-id="6b249-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="6b249-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="6b249-104">**Issue**</span></span>

<span data-ttu-id="6b249-105">De gegevenswijzigingen van een klant worden niet op het tabblad **Analyses** van de werkgebieden van de klant weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6b249-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="6b249-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="6b249-106">**Cause**</span></span>

<span data-ttu-id="6b249-107">Standaard worden Microsoft Power BI-rapporten elke vier uur vernieuwd, volgens het schema van de batchtaak Meting implementeren.</span><span class="sxs-lookup"><span data-stu-id="6b249-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="6b249-108">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="6b249-108">**Resolution**</span></span>

<span data-ttu-id="6b249-109">Dit probleem kan ook een kwestie van timing zijn.</span><span class="sxs-lookup"><span data-stu-id="6b249-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="6b249-110">Volg deze stappen om de batchtaak te starten en de werkgebieden voor analyses bij te werken.</span><span class="sxs-lookup"><span data-stu-id="6b249-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="6b249-111">Open de pagina **Batchtaken** via **Systeembeheer \> Koppelingen \> Batchtaken \> Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="6b249-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="6b249-112">U kunt ook Zoeken gebruiken en **Batchtaken** invoeren.</span><span class="sxs-lookup"><span data-stu-id="6b249-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="6b249-113">Zoek de taak **Meting implementeren** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6b249-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="6b249-114">Selecteer **Bewerken** boven aan de pagina en stel de geplande begindatum/-tijd in waarmee de analyses dichter bij de huidige tijd worden vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="6b249-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchtaken](media/batch-jobs.png)