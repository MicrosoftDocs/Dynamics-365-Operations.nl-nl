---
title: Regels in de consistentiecontrole voor detailhandeltransacties uitschakelen
description: In dit onderwerp wordt de functionaliteit beschreven voor het uitschakelen van de regels in de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004338"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="c2b44-103">Regels in de consistentiecontrole voor detailhandeltransacties uitschakelen</span><span class="sxs-lookup"><span data-stu-id="c2b44-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c2b44-104">Detailhandelaren kunnen bedrijfsscenario's en processen hebben die uniek zijn.</span><span class="sxs-lookup"><span data-stu-id="c2b44-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="c2b44-105">Daarom zijn niet alle regels die standaard zijn opgenomen in de consistentiecontrole voor handeltransacties van toepassing op alle detailhandelaren.</span><span class="sxs-lookup"><span data-stu-id="c2b44-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="c2b44-106">Om verschillen te kunnen verwerken, biedt Microsoft Dynamics 365 Commerce functionaliteit die kan worden gebruikt om de regels die niet van toepassing zijn, uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c2b44-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="c2b44-107">Voor het weergeven van de lijst met regels die beschikbaar zijn in de consistentiecontrole voor detailhandeltransacties in uw omgeving en om de status van elke regel weer te geven, gaat u naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters** en selecteert u het tabblad **Transactievalidatie**.</span><span class="sxs-lookup"><span data-stu-id="c2b44-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="c2b44-108">Standaard is de status van elke regel ingesteld op **Ingeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="c2b44-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="c2b44-109">Daarom worden alle regels gebruikt om detailhandeltransacties te valideren voordat ze in de handelsoverzichten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c2b44-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="c2b44-110">Als u een regel wilt uitschakelen, wijzigt u de status in **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="c2b44-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="c2b44-111">Uitgeschakelde regels worden niet meegenomen wanneer transacties worden gevalideerd tijdens het berekeningsproces van het overzicht.</span><span class="sxs-lookup"><span data-stu-id="c2b44-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="c2b44-112">Als u het gehele validatieproces wilt overslaan, ongeacht de ingeschakelde regels, gaat u naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters** en stelt u op het tabblad **Transactievalidatie** de optie **Consistentiecontrole voor detailhandeltransacties uitschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c2b44-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="c2b44-113">Als deze optie is ingesteld op **Nee**, kan deze niet worden teruggezet op **Ja** vanuit de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="c2b44-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>