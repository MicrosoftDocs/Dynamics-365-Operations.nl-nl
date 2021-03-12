---
title: Problemen met magazijnaanvulling oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993864"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="deae0-103">Problemen met magazijnaanvulling oplossen</span><span class="sxs-lookup"><span data-stu-id="deae0-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="deae0-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="deae0-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="deae0-105">Het volgende foutbericht wordt weergegeven: "Werk %1 kan niet ongedaan worden gemaakt omdat het onvoltooid aanvullingswerk bevat."</span><span class="sxs-lookup"><span data-stu-id="deae0-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="deae0-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="deae0-106">Issue description</span></span>

<span data-ttu-id="deae0-107">Verzamelwerk wordt geblokkeerd vanwege afhankelijk aanvullingswerk.</span><span class="sxs-lookup"><span data-stu-id="deae0-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="deae0-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="deae0-108">Issue resolution</span></span>

<span data-ttu-id="deae0-109">Wanneer u wavevraagaanvulling gebruikt en er een verzamellocatie moet worden aangevuld om aan de bronordervraag te voldoen, worden zowel het aanvullingswerk als het verzamelwerk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="deae0-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="deae0-110">Het verzamelproces wordt echter geblokkeerd totdat het aanvullingswerk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="deae0-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="deae0-111">Dit gebeurt met opzet, omdat de verzamellocatie onvoldoende voorraad heeft, tenzij het aanvullingswerk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="deae0-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="deae0-112">Voltooi het aanvullingswerk en verwerk vervolgens het verzamelwerk.</span><span class="sxs-lookup"><span data-stu-id="deae0-112">Complete the replenishment work, and then process the picking work.</span></span>
