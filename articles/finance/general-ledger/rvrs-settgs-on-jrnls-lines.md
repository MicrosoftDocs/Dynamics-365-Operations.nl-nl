---
title: Terugboekingsinstellingen voor journalen en regels
description: In dit onderwerp wordt aangegeven waarom een ingevoerde stornopost in een journaal mogelijk niet wordt opgenomen in de geboekte transactie.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028556"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="ed523-103">Terugboekingsinstellingen voor journalen en regels</span><span class="sxs-lookup"><span data-stu-id="ed523-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed523-104">In dit onderwerp wordt aangegeven waarom een ingevoerde stornopost in een journaal mogelijk niet wordt opgenomen in de geboekte transactie.</span><span class="sxs-lookup"><span data-stu-id="ed523-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="ed523-105">Symptoom</span><span class="sxs-lookup"><span data-stu-id="ed523-105">Symptom</span></span>

<span data-ttu-id="ed523-106">Een journaal bevat een stornopost en -datum.</span><span class="sxs-lookup"><span data-stu-id="ed523-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="ed523-107">Wanneer u het journaal boekt, wordt geen van de boekstukken teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="ed523-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="ed523-108">Waarom gebeurt dit?</span><span class="sxs-lookup"><span data-stu-id="ed523-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="ed523-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ed523-109">Resolution</span></span>

<span data-ttu-id="ed523-110">Wanneer het journaal wordt geboekt, wordt in het terugboekingsproces alleen gekeken naar de instellingen **Stornopost** en **Stornodatum** in de sectie **Regels** van het boekstuk.</span><span class="sxs-lookup"><span data-stu-id="ed523-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="ed523-111">Bij deze aanpak kan een journaal enkele boekstukken bevatten die zijn gemarkeerd voor terugboeken en andere boekstukken waarvoor dit niet geldt.</span><span class="sxs-lookup"><span data-stu-id="ed523-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="ed523-112">De waarden uit het journaal worden alleen als standaardinstellingen gebruikt bij het toevoegen van *nieuwe* regels.</span><span class="sxs-lookup"><span data-stu-id="ed523-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="ed523-113">Als u de waarden in het journaal wijzigt, heeft dit geen invloed op bestaande regels.</span><span class="sxs-lookup"><span data-stu-id="ed523-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="ed523-114">In dit voorbeeld zijn de boekstukregels eerst ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="ed523-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="ed523-115">Wanneer u de regeldetails invoert voordat u het journaal aanduidt als stornojournaal, wordt de aanduiding als stornopost en stornodatum niet toegepast op bestaande regels.</span><span class="sxs-lookup"><span data-stu-id="ed523-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="ed523-116">Als u de stornopost of -datum op een bestaande regel wijzigt, worden die wijzigingen doorgegeven aan andere regels in hetzelfde boekstuk.</span><span class="sxs-lookup"><span data-stu-id="ed523-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="ed523-117">Om de prestaties te optimaliseren, wordt het raster niet vernieuwd nadat wijzigingen zijn doorgegeven aan andere regels.</span><span class="sxs-lookup"><span data-stu-id="ed523-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="ed523-118">U kunt de bijgewerkte waarden weergeven door het raster te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="ed523-118">You can display the updated values by refreshing the grid.</span></span>


