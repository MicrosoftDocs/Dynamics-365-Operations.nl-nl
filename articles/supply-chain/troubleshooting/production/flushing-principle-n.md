---
title: Wisprincipe-instellingen op stuklijstregels worden niet in acht genomen
description: Wisprincipe-instellingen op stuklijstregels worden niet in acht genomen.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026407"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="a6e56-103">Wisprincipe-instellingen op stuklijstregels worden niet in acht genomen</span><span class="sxs-lookup"><span data-stu-id="a6e56-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="a6e56-104">KB-nummer: 4612725</span><span class="sxs-lookup"><span data-stu-id="a6e56-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="a6e56-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="a6e56-105">Symptoms</span></span>

<span data-ttu-id="a6e56-106">Dit probleem treedt op wanneer het veld **Automatisch stuklijstverbruik** op het tabblad **Automatisch bijwerken** van de pagina **Parameters van productiebeheer** is ingesteld op *Wisprincipe*.</span><span class="sxs-lookup"><span data-stu-id="a6e56-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="a6e56-107">Deze instelling geeft aan dat alle stuklijstregels automatisch moeten worden verbruikt wanneer een inkooporder wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="a6e56-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="a6e56-108">Als het veld **Wisprincipe** op stuklijstregels expliciet is ingesteld op *Handmatig*, kunt u verwachten dat de stuklijstregels niet automatisch worden verbruikt.</span><span class="sxs-lookup"><span data-stu-id="a6e56-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="a6e56-109">Wanneer dit probleem zich echter voordoet, worden stuklijstregels waarbij het veld **Wisprincipe** is ingesteld op *Handmatig* toch automatisch verbruikt.</span><span class="sxs-lookup"><span data-stu-id="a6e56-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="a6e56-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="a6e56-110">Resolution</span></span>

<span data-ttu-id="a6e56-111">Als u dit probleem ondervindt, kunt u de parameters voor productiebeheer zo instellen dat de instelling **Wisprincipe** voor stuklijstregels wordt overgenomen.</span><span class="sxs-lookup"><span data-stu-id="a6e56-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="a6e56-112">Controleer op de pagina **Parameters van productiebeheer** op het tabblad **Automatisch bijwerken** de waarde van het veld **Automatisch stuklijstverbruik**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="a6e56-113">Als de waarde is ingesteld op *Altijd*, wordt de instelling van **Wisprincipe** voor alle stuklijstregels genegeerd en worden de regels altijd leeggemaakt.</span><span class="sxs-lookup"><span data-stu-id="a6e56-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="a6e56-114">Als u wilt instellen dat het systeem de instelling van **Wisprincipe** voor stuklijstregels in acht neemt, wijzigt u de waarde van het veld **Automatisch stuklijstverbruik** in *Wisprincipe*.</span><span class="sxs-lookup"><span data-stu-id="a6e56-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
