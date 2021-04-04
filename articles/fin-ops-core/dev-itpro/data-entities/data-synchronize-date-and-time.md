---
title: Datum en tijd in importtaken synchroniseren
description: Gebruik UTC-tijdzones in importtaken om problemen met tijdzoneconversies te voorkomen.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570474"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="8999b-103">Datum en tijd in importtaken synchroniseren</span><span class="sxs-lookup"><span data-stu-id="8999b-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8999b-104">Het is belangrijk om de tijdzone voor uw importtaak in te stellen op UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="8999b-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8999b-105">Er worden mogelijk onverwachte datums en tijden voor uw geïmporteerde gegevens weergegeven als u een andere instelling gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8999b-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="8999b-106">Zonder de juiste instelling converteert het importproces de UTC-datum naar de lokale indeling, waarna deze opnieuw wordt geconverteerd via de systeeminstellingen.</span><span class="sxs-lookup"><span data-stu-id="8999b-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="8999b-107">Door deze dubbele conversie veranderen de datums tussen toepassingen.</span><span class="sxs-lookup"><span data-stu-id="8999b-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="8999b-108">Bij de dubbele conversie kan bijvoorbeeld de begindatum van een werknemer verschillen tussen Dynamics 365 Human Resources en Dynamics 365 Finance door verschillen in lokale tijdzones.</span><span class="sxs-lookup"><span data-stu-id="8999b-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="8999b-109">Als u de importtaak instelt op UTC, wordt dit probleem verholpen.</span><span class="sxs-lookup"><span data-stu-id="8999b-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="8999b-110">Selecteer in Dynamics 365 Finance and Operations **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="8999b-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="8999b-111">Selecteer **Projecten importeren** en dan het project.</span><span class="sxs-lookup"><span data-stu-id="8999b-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="8999b-112">Selecteer onder **Brondatumnotatie** de optie **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="8999b-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="8999b-113">[![De brondatumnotatie wijzigen in UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="8999b-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="8999b-114">Wijzig **de tijdzone** in **Coordinated Universal Timezone** en wijzig **Taal** in **En-US**.</span><span class="sxs-lookup"><span data-stu-id="8999b-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]