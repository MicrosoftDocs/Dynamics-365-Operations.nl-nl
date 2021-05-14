---
title: Artikelbemonstering voor kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u artikelbemonstering instelt.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956602"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="a6c03-103">Artikelbemonstering voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="a6c03-103">Quality management item sampling</span></span>

<span data-ttu-id="a6c03-104">Artikelbemonstering wordt gebruikt als onderdeel van een kwaliteitskoppeling.</span><span class="sxs-lookup"><span data-stu-id="a6c03-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="a6c03-105">In de artikelbemonstering wordt het bedrag gedefinieerd van de huidige fysieke voorraad die moet worden geïnspecteerd.</span><span class="sxs-lookup"><span data-stu-id="a6c03-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="a6c03-106">Bemonstering kan worden gebaseerd op een vaste hoeveelheid, een percentage of een volledige nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="a6c03-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="a6c03-107">Artikelbemonstering instellen</span><span class="sxs-lookup"><span data-stu-id="a6c03-107">Set up item sampling</span></span>

<span data-ttu-id="a6c03-108">Ga als volgt te werk om artikelbemonstering in te stellen.</span><span class="sxs-lookup"><span data-stu-id="a6c03-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="a6c03-109">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Artikelbemonstering**.</span><span class="sxs-lookup"><span data-stu-id="a6c03-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="a6c03-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a6c03-110">Select **New**.</span></span>
1. <span data-ttu-id="a6c03-111">Voer een waarde in het veld **Artikelbemonstering** in.</span><span class="sxs-lookup"><span data-stu-id="a6c03-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="a6c03-112">Voer een waarde in het veld **Beschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="a6c03-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="a6c03-113">Typ een getal in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="a6c03-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="a6c03-114">Deze waarde heeft betrekking op de waarde voor de hoeveelheidsspecificatie die in het aangrenzende veld is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a6c03-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="a6c03-115">Schakel in de sectie **Proces** het selectievakje **Volledige blokkering** in als de hoeveelheid van de hele partij of de orderregel moet worden geblokkeerd als een test is mislukt.</span><span class="sxs-lookup"><span data-stu-id="a6c03-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="a6c03-116">Als dit selectievakje is uitgeschakeld, worden alleen de artikelen in de kwaliteitsorder geblokkeerd als een test is mislukt.</span><span class="sxs-lookup"><span data-stu-id="a6c03-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="a6c03-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="a6c03-117">Select **Save**.</span></span>
1. <span data-ttu-id="a6c03-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a6c03-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="a6c03-119">Met de functie *Kwaliteitsbeheer voor magazijnprocessen* worden extra voorzieningen voor artikelbemonstering toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="a6c03-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="a6c03-120">Het concept van *artikelbemonsteringsbereik* wordt toegevoegd en u kunt een volledige nummerplaat als hoeveelheidsspecificatie definiëren.</span><span class="sxs-lookup"><span data-stu-id="a6c03-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="a6c03-121">Als u deze functie hebt ingeschakeld, vindt u in [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md) meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a6c03-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
