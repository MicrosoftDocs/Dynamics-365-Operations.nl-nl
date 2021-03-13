---
title: Globale bronbelasting instellen
description: Dit onderwerp biedt een overzicht van de stappen voor het instellen van globale bronbelasting voor verkoop en inkoop.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060720"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="12c2d-103">Globale bronbelasting instellen</span><span class="sxs-lookup"><span data-stu-id="12c2d-103">Set up global withholding tax</span></span>

<span data-ttu-id="12c2d-104">Dit onderwerp biedt een overzicht van de stappen voor het instellen van globale bronbelasting voor verkoop en inkoop.</span><span class="sxs-lookup"><span data-stu-id="12c2d-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="12c2d-105">Stel bronbelastinginstanties in op de pagina **Bronbelastinginstanties**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="12c2d-106">Stel vereffeningsperioden voor bronbelasting in op de pagina **Vereffeningsperioden voor bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="12c2d-107">Stel een grootboekboekingsgroep voor bronbelasting in op de pagina **Bronbelasting > Grootboekboekingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="12c2d-108">Een rekening van het type **Bronbelasting** wordt toegewezen aan een hoofdrekening met het **boekingstype** Bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="12c2d-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="12c2d-109">Een rekening van het type **Verrekening bronbelasting** wordt ook toegewezen aan een hoofdrekening met het **boekingstype** Verrekening bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="12c2d-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="12c2d-110">Ga naar **Grootboek > Rekeningschema > Rekeningen > Hoofdrekeningen** en stel **Boekingstype** in het subformulier **Boekingsvalidatie** voor de hoofdrekeningen in.</span><span class="sxs-lookup"><span data-stu-id="12c2d-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="12c2d-111">Stel bronbelastingcodes in op de pagina **Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="12c2d-112">Stel bronbelastinggroepen in op de pagina **Bronbelastinggroepen**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="12c2d-113">Stel opbrengsttypen voor bronbelasting in op de pagina **Opbrengsttypen** **bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="12c2d-114">Stel bronbelastinggroepen in op de pagina **Artikelbronbelastinggroepen** voor een artikel of service.</span><span class="sxs-lookup"><span data-stu-id="12c2d-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="12c2d-115">Stel **Minimaal factuurbedrag** in op de pagina **Grootboekparameters > Bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="12c2d-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>
