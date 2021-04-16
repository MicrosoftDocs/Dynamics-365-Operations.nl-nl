---
title: Algemene bronbelasting
description: Dit onderwerp biedt informatie over de functionaliteit voor algemene bronbelasting en over het instellen ervan. De functionaliteit voor algemene bronbelasting is verbeterd voor leveranciers- en klanttransacties, zodat bronbelasting wordt berekend op artikelniveau.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826661"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="351bd-104">Algemene bronbelasting</span><span class="sxs-lookup"><span data-stu-id="351bd-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="351bd-105">Dit onderwerp biedt informatie over de functionaliteit voor algemene bronbelasting en legt uit hoe u deze instelt.</span><span class="sxs-lookup"><span data-stu-id="351bd-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="351bd-106">De nieuwe functionaliteit is beschikbaar in versie 10.0.17 en hoger.</span><span class="sxs-lookup"><span data-stu-id="351bd-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="351bd-107">De functionaliteit voor algemene bronbelasting is verbeterd voor leveranciers- en klanttransacties, zodat bronbelasting wordt berekend op artikelniveau.</span><span class="sxs-lookup"><span data-stu-id="351bd-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="351bd-108">Het saldo op de bronbelastingrekening van inkooptransacties kan worden vereffend door de taak voor bronbelastingbetaling uit te voeren tegen de vereffeningsrekening voor bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="351bd-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="351bd-109">Algemene bronbelasting ondersteunt niet de functie **Toeslagen onderhouden** op de inkooporder-, leveranciersfactuur- en verkooporderpagina's.</span><span class="sxs-lookup"><span data-stu-id="351bd-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="351bd-110">Algemene bronbelasting inschakelen</span><span class="sxs-lookup"><span data-stu-id="351bd-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="351bd-111">Selecteer in de werkruimte **Functiebeheer** de optie **Algemene bronbelasting** en selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="351bd-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="351bd-112">Ga naar **Belasting \> Instellen \> Parameters \> Grootboekparameters** en stel op het tabblad **Bronbelasting** de optie **Algemene bronbelasting** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="351bd-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="351bd-113">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="351bd-113">Select **Save**.</span></span>
4. <span data-ttu-id="351bd-114">Vernieuw de pagina in de webbrowser.</span><span class="sxs-lookup"><span data-stu-id="351bd-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="351bd-115">De functionaliteit voor algemene bronbelasting kan niet worden ingeschakeld voor landen/regio's waar al lokale bronbelastingoplossingen bestaan.</span><span class="sxs-lookup"><span data-stu-id="351bd-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="351bd-116">Deze gebieden zijn onder andere, maar niet uitsluitend India, Brazilië, Thailand, Saudi-Arabië, Ierland, Groot-Brittannië en de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="351bd-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]