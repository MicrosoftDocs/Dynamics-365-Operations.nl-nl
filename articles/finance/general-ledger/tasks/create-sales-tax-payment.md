---
title: Een btw-betaling maken
description: De procedure voor de taak Btw vereffenen en boeken vereffent btw-saldi op de btw-rekeningen en tegenboekt ze naar de btw-vereffeningsrekening voor een bepaalde periode.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b5e3e26e19bd0a9dbf878626328da267b61964f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968699"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="07701-103">Een btw-betaling maken</span><span class="sxs-lookup"><span data-stu-id="07701-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07701-104">De procedure voor de taak Btw vereffenen en boeken vereffent btw-saldi op de btw-rekeningen en tegenboekt ze naar de btw-vereffeningsrekening voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="07701-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="07701-105">Ga naar **Belasting > Aangiften > Btw > Btw vereffenen en boeken**.</span><span class="sxs-lookup"><span data-stu-id="07701-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="07701-106">Klik in het veld **Vereffeningsperiode** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="07701-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="07701-107">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="07701-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="07701-108">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="07701-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="07701-109">Als u de optie **Correcties opnemen** op de pagina **Grootboekparameters** niet selecteert, kan de vereffening voor verschillende versies worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="07701-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="07701-110">Oorspronkelijk is de eerste vereffening voor een periode-interval en kan deze slechts eenmaal worden verwerkt voor een periode-interval.</span><span class="sxs-lookup"><span data-stu-id="07701-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="07701-111">De laatste correcties vereffenen btw-transacties die zijn geboekt nadat de oorspronkelijke versie is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="07701-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="07701-112">Voer in het veld **Transactiedatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="07701-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="07701-113">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="07701-113">Click **OK**.</span></span>

