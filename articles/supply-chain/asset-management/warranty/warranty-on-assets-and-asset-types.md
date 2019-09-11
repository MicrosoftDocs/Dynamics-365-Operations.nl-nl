---
title: Garanties op activa en activatypen
description: In dit onderwerp wordt uitgelegd hoe u garanties op activa en activatypen kunt instellen in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874596"
---
# <a name="warranty-on-assets-and-asset-types"></a><span data-ttu-id="8137e-103">Garantie op activa en activatypen</span><span class="sxs-lookup"><span data-stu-id="8137e-103">Warranty on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="8137e-104">In dit onderwerp wordt uitgelegd hoe u garanties op activa en activatypen kunt instellen in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="8137e-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="8137e-105">Garantie voor activatypen instellen</span><span class="sxs-lookup"><span data-stu-id="8137e-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="8137e-106">Selecteer **Activabeheer** \> **Instellingen** \> **Activatypen** \> **Activatypen**.</span><span class="sxs-lookup"><span data-stu-id="8137e-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="8137e-107">Selecteer in het linkerdeelvenster het activatype waaraan u een leveranciersgarantieovereenkomst wilt koppelen en selecteer vervolgens **Standaardwaarden van activatype**.</span><span class="sxs-lookup"><span data-stu-id="8137e-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="8137e-108">Selecteer de overeenkomst in het veld **Leveranciersgarantie** van het sneltabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="8137e-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="8137e-109">Garantie voor een activum instellen</span><span class="sxs-lookup"><span data-stu-id="8137e-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="8137e-110">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="8137e-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="8137e-111">Selecteer het activum en selecteer vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="8137e-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="8137e-112">Selecteer de garantieovereenkomst in de sectie **Leveranciersgarantie** van het sneltabblad **Leverancier** in het veld **Garantie**.</span><span class="sxs-lookup"><span data-stu-id="8137e-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="8137e-113">Selecteer in de velden **Begindatum garantie** en **Einddatum garantie** de begin- en einddatums.</span><span class="sxs-lookup"><span data-stu-id="8137e-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8137e-114">Als een datum is geselecteerd in het veld **Begindatum garantie** voor een werkorder, wordt de garantie geldig voor de werkorder op die datum.</span><span class="sxs-lookup"><span data-stu-id="8137e-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="8137e-115">Wanneer u een werkorder maakt, wordt het veld **Begindatum garantie** automatisch ingesteld op de datum van aanmaak.</span><span class="sxs-lookup"><span data-stu-id="8137e-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="8137e-116">U kunt de datum echter wijzigen, zodat deze overeenkomt met bijvoorbeeld de begindatum van een garantieovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="8137e-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Figuur 1](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="8137e-118">Wanneer u een werkorder maakt voor een activum dat wordt gedekt door een garantie van een leverancier, ontvangt u een melding over de garantieovereenkomst als de werkorder een verwachte begindatum heeft gedurende de garantieperiode.</span><span class="sxs-lookup"><span data-stu-id="8137e-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="8137e-119">U kunt de werkorder vervolgens desgewenst annuleren.</span><span class="sxs-lookup"><span data-stu-id="8137e-119">You can then cancel the work order, as you require.</span></span>
