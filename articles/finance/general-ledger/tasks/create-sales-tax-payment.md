---
title: Een btw-betaling maken
description: De taak Btw vereffenen en boeken vereffent btw-saldi op de btw-rekeningen en tegenboekt ze naar de btw-vereffeningsrekening voor een bepaalde periode.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee69cfee672be1571fd5cc630e33601bb5a48eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186159"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="a4b1d-103">Een btw-betaling maken</span><span class="sxs-lookup"><span data-stu-id="a4b1d-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4b1d-104">De taak Btw vereffenen en boeken vereffent btw-saldi op de btw-rekeningen en tegenboekt ze naar de btw-vereffeningsrekening voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="a4b1d-105">Ga naar Btw > Aangiften > Btw > Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="a4b1d-106">Klik in het veld Vereffeningsperiode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a4b1d-107">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a4b1d-108">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="a4b1d-109">Als de optie Correcties opnemen niet op de pagina Grootboekparameters is geselecteerd, kan de vereffening voor verschillende versies worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="a4b1d-110">Oorspronkelijk is de eerste vereffening voor een periode-interval en kan slechts eenmaal worden verwerkt voor een periode-interval.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="a4b1d-111">Laatste correcties vereffenen btw-transacties die zijn geboekt nadat de oorspronkelijke versie is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="a4b1d-112">Voer in het veld Transactiedatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="a4b1d-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a4b1d-113">Click OK.</span></span>

