---
title: Regels in de consistentiecontrole voor detailhandeltransacties uitschakelen
description: In dit onderwerp wordt de functionaliteit voor het uitschakelen van de regels in de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586292"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="feaa2-103">Regels in de consistentiecontrole voor detailhandeltransacties uitschakelen</span><span class="sxs-lookup"><span data-stu-id="feaa2-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="feaa2-104">Detailhandelaren kunnen bedrijfsscenario's en processen hebben die uniek zijn.</span><span class="sxs-lookup"><span data-stu-id="feaa2-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="feaa2-105">Daarom zijn niet alle regels die standaard zijn opgenomen in de consistentiecontrole voor detailhandeltransacties van toepassing op alle detailhandelaren.</span><span class="sxs-lookup"><span data-stu-id="feaa2-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="feaa2-106">Om verschillen te kunnen verwerken biedt Microsoft Dynamics 365 Retail functionaliteit die kan worden gebruikt om de regels die niet van toepassing zijn, uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="feaa2-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="feaa2-107">Voor het weergeven van de lijst met regels die beschikbaar zijn in de consistentiecontrole voor detailhandeltransacties in uw omgeving en om de status van elke regel weer te geven, gaat u naar **Detailhandel \> Instelling van hoofdkantoor \> Parameters \> Detailhandelparameters** en selecteert u het tabblad **Transactievalidatie**.</span><span class="sxs-lookup"><span data-stu-id="feaa2-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="feaa2-108">Standaard is de status van elke regel ingesteld op **Ingeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="feaa2-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="feaa2-109">Daarom worden alle regels gebruikt om detailhandeltransacties te valideren voordat ze in de detailhandeloverzichten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="feaa2-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="feaa2-110">Als u een regel wilt uitschakelen, wijzigt u de status in **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="feaa2-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="feaa2-111">Uitgeschakelde regels worden niet meegenomen wanneer detailhandeltransacties worden gevalideerd tijdens het berekeningsproces van het overzicht.</span><span class="sxs-lookup"><span data-stu-id="feaa2-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="feaa2-112">Als u het gehele validatieproces wilt overslaan, ongeacht de ingeschakelde regels, gaat u naar **Detailhandel \> Instelling van hoofdkantoor \> Parameters \> Detailhandelparameters** en stelt u op het tabblad **Transactievalidatie** de optie **Consistentiecontrole voor detailhandeltransacties uitschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="feaa2-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="feaa2-113">Als deze optie is ingesteld op **Nee**, kan deze niet worden teruggezet op **Ja** vanuit de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="feaa2-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
