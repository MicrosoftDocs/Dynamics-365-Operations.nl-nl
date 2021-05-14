---
title: Onjuiste veldwaarde in TaxTrans
description: Dit onderwerp bevat informatie over het oplossen van problemen met onjuiste veldwaarden in TaxTrans.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947618"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="bd762-103">Onjuiste veldwaarde in TaxTrans</span><span class="sxs-lookup"><span data-stu-id="bd762-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd762-104">Als een veldwaarde in **TaxTrans** onjuist is, gebruikt u de informatie in dit onderwerp om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="bd762-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="bd762-105">Overzicht van waarden</span><span class="sxs-lookup"><span data-stu-id="bd762-105">Overview of values</span></span>
<span data-ttu-id="bd762-106">In de volgende lijst wordt weergegeven dat **TaxTrans**, **TaxUncommitted** en **TmpTaxWorkTrans** gelijksoortige gegevenssets zijn, maar verschillend werken.</span><span class="sxs-lookup"><span data-stu-id="bd762-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="bd762-107">**TaxTrans** is het definitieve geboekte resultaat van een belastingtransactie dat in de database blijft staan.</span><span class="sxs-lookup"><span data-stu-id="bd762-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="bd762-108">**TaxUncommitted** is het tussenliggende berekende belastingresultaat dat in de database blijft staan (indien van toepassing), dat later wordt gebruikt bij het boeken.</span><span class="sxs-lookup"><span data-stu-id="bd762-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="bd762-109">**TmpTaxWorkTrans** is het tijdelijke berekende belastingresultaat in de geheugentabel (Tabeltype = InMemory).</span><span class="sxs-lookup"><span data-stu-id="bd762-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="bd762-110">Als u de hoofdoorzaak van een onjuiste **TaxTrans**-kolom hebt gevonden, hebt u ook de hoofdoorzaak van een onjuiste **TaxUncommitted**- of **TmpTaxWorkTrans**-kolom gevonden.</span><span class="sxs-lookup"><span data-stu-id="bd762-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="bd762-111">Dit komt omdat de drie kolommen van elkaar zijn gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="bd762-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="bd762-112">Normaal gesproken wordt tijdens de belastingberekening **TmpTaxWorkTrans** gegenereerd en vervolgens, indien van toepassing, wordt **TaxUncommitted** gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bd762-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="bd762-113">Tijdens het boeken van belasting wordt **TaxTrans** gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bd762-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="bd762-114">Onderbrekingspunten toevoegen</span><span class="sxs-lookup"><span data-stu-id="bd762-114">Add breakpoints</span></span>
<span data-ttu-id="bd762-115">Voer de volgende stappen uit om onderbrekingspunten toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="bd762-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="bd762-116">Voeg extensies en onderbrekingspunten toe in *insert()* en *update()* in de extensies zoals hieronder weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bd762-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="bd762-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="bd762-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="bd762-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="bd762-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="bd762-119">**TmptaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="bd762-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="bd762-120">U kunt ook direct onderbrekingspunten toevoegen wanneer **TaxUncommitted** niet is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="bd762-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="bd762-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="bd762-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="bd762-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="bd762-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="bd762-123">Reproduceren en fouten opsporen</span><span class="sxs-lookup"><span data-stu-id="bd762-123">Reproduce and debug</span></span>

<span data-ttu-id="bd762-124">Nadat de onderbrekingspunten zijn ingesteld, is elke wijziging van de gegevenspersistentie zichtbaar tijdens foutopsporing.</span><span class="sxs-lookup"><span data-stu-id="bd762-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="bd762-125">Als u de hoofdoorzaak wilt vinden van een onjuiste kolom met **TaxTrans**, **TaxUncommitted** of **TmpTaxWorkTrans**, controleert en noteert u de volgende punten:</span><span class="sxs-lookup"><span data-stu-id="bd762-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="bd762-126">Het laatste onderbrekingspunt waar de kolom juist is.</span><span class="sxs-lookup"><span data-stu-id="bd762-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="bd762-127">Het eerste onderbrekingspunt waar de kolom onjuist is.</span><span class="sxs-lookup"><span data-stu-id="bd762-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="bd762-128">Wat er tussen deze twee punten gebeurt.</span><span class="sxs-lookup"><span data-stu-id="bd762-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="bd762-129">Bekijk of er een aanpassing bestaat</span><span class="sxs-lookup"><span data-stu-id="bd762-129">Determine whether customization exists</span></span>
<span data-ttu-id="bd762-130">Als u de stappen in de vorige secties hebt voltooid, maar het probleem niet hebt kunnen oplossen, bekijkt u of er aanpassing bestaat.</span><span class="sxs-lookup"><span data-stu-id="bd762-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="bd762-131">Neem, als er geen aanpassing bestaat, contact op met Microsoft Ondersteuning voor hulp.</span><span class="sxs-lookup"><span data-stu-id="bd762-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

