---
title: Parameters configureren die gevolgen hebben voor detailhandeloverzichten
description: Dit onderwerp demonstreert configuraties voor Commerce-parameters die van invloed zijn op hoe overzichten worden gemaakt en geboekt.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022117"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="1abbf-103">Parameters configureren die gevolgen hebben voor detailhandeloverzichten</span><span class="sxs-lookup"><span data-stu-id="1abbf-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1abbf-104">Dit onderwerp demonstreert configuraties voor Commerce-parameters die van invloed zijn op hoe overzichten worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="1abbf-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="1abbf-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="1abbf-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="1abbf-106">Ga in het navigatievenster naar **Modules > Retail en Commerce > Instelling van hoofdkantoor > Parameters > Commerce-parameters**.</span><span class="sxs-lookup"><span data-stu-id="1abbf-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="1abbf-107">Selecteer het tabblad **Boeking**.</span><span class="sxs-lookup"><span data-stu-id="1abbf-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="1abbf-108">Selecteer **Ja** als u de periodieke kortingsbedragen specifiek wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="1abbf-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="1abbf-109">Selecteer **Standaard** om standaardrekeningen te gebruiken of selecteer **Periodiek** als u wilt definiëren welke rekening moet worden gebruikt voor elke periodieke rekening.</span><span class="sxs-lookup"><span data-stu-id="1abbf-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="1abbf-110">Selecteer **Overzicht** als voorraadregels moeten worden samengevoegd indien mogelijk.</span><span class="sxs-lookup"><span data-stu-id="1abbf-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="1abbf-111">Selecteer **Ja** als facturen en betalingen automatisch moeten worden vereffend als onderdeel van het overzichtsboekingsproces.</span><span class="sxs-lookup"><span data-stu-id="1abbf-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="1abbf-112">Selecteer **Ja** als kluisstortingstransacties moeten worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="1abbf-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="1abbf-113">Selecteer **Ja** als bankstortingstransacties moeten worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="1abbf-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="1abbf-114">Selecteer **Ja** om samenvoeging in te schakelen voor overzichtsboeking.</span><span class="sxs-lookup"><span data-stu-id="1abbf-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="1abbf-115">Selecteer **Ja** om orders parallel te maken en te verwerken wanneer overzichten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="1abbf-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="1abbf-116">Voer de maximale orders in die moeten worden verwerkt in elke batchtaak.</span><span class="sxs-lookup"><span data-stu-id="1abbf-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="1abbf-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1abbf-117">Select **Save**.</span></span>

