---
title: Problemen met magazijnaanvulling oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828077"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="f8975-103">Problemen met magazijnaanvulling oplossen</span><span class="sxs-lookup"><span data-stu-id="f8975-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8975-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f8975-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="f8975-105">Het volgende foutbericht wordt weergegeven: "Werk %1 kan niet ongedaan worden gemaakt omdat het onvoltooid aanvullingswerk bevat."</span><span class="sxs-lookup"><span data-stu-id="f8975-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f8975-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="f8975-106">Issue description</span></span>

<span data-ttu-id="f8975-107">Verzamelwerk wordt geblokkeerd vanwege afhankelijk aanvullingswerk.</span><span class="sxs-lookup"><span data-stu-id="f8975-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f8975-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="f8975-108">Issue resolution</span></span>

<span data-ttu-id="f8975-109">Wanneer u wavevraagaanvulling gebruikt en er een verzamellocatie moet worden aangevuld om aan de bronordervraag te voldoen, worden zowel het aanvullingswerk als het verzamelwerk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f8975-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="f8975-110">Het verzamelproces wordt echter geblokkeerd totdat het aanvullingswerk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f8975-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="f8975-111">Dit gebeurt met opzet, omdat de verzamellocatie onvoldoende voorraad heeft, tenzij het aanvullingswerk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f8975-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="f8975-112">Voltooi het aanvullingswerk en verwerk vervolgens het verzamelwerk.</span><span class="sxs-lookup"><span data-stu-id="f8975-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]