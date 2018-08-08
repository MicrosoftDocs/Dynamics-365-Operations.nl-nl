---
title: Overzicht van geavanceerde bankafstemming
description: In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5c6cec76ebc8328f221ecb6c30ae93716bd9bfe9
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="2726e-104">Overzicht van geavanceerde bankafstemming</span><span class="sxs-lookup"><span data-stu-id="2726e-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2726e-105">In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven.</span><span class="sxs-lookup"><span data-stu-id="2726e-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="2726e-106">Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.</span><span class="sxs-lookup"><span data-stu-id="2726e-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="2726e-107">Met de functie voor geavanceerde bankafstemming kunt u bankafschriften importeren.</span><span class="sxs-lookup"><span data-stu-id="2726e-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="2726e-108">Het geïmporteerde bankafschrift kan vervolgens automatisch in banktransacties worden afgestemd.</span><span class="sxs-lookup"><span data-stu-id="2726e-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="2726e-109">Hier vindt u de stappen in de geavanceerde bankafstemmingsstroom.</span><span class="sxs-lookup"><span data-stu-id="2726e-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="2726e-110">Stel de import van een bankafschrift in.</span><span class="sxs-lookup"><span data-stu-id="2726e-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="2726e-111">Importeer bankafschriften via het gegevensentiteitsraamwerk.</span><span class="sxs-lookup"><span data-stu-id="2726e-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="2726e-112">Drie typische bankafschriftindelingen zijn ingebouwd: ISO20022, BAI2 en MT940.</span><span class="sxs-lookup"><span data-stu-id="2726e-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="2726e-113">De functionaliteit kan naar iedere indeling worden uitgebreid.</span><span class="sxs-lookup"><span data-stu-id="2726e-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="2726e-114">Stel een nummerreeks in die moet worden gebruikt voor geavanceerde bankafstemming en definieer de afstemmingsregels voor bankafstemming.</span><span class="sxs-lookup"><span data-stu-id="2726e-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="2726e-115">Een afstemmingsregel is een reeks criteria die worden gebruikt om regels van bankafschriften en banktransactieregels van Microsoft Dynamics 365 for Finance and Operations te filteren tijdens het afstemmingsproces.</span><span class="sxs-lookup"><span data-stu-id="2726e-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="2726e-116">Afhankelijk van uw bedrijfspraktijk kunt u meerdere afstemmingsregels instellen om uw afstemmingsproces te automatiseren en te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="2726e-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="2726e-117">Stem bankafschriften af met de banktransacties van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2726e-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="2726e-118">Voer automatische afstemming en het maken van afstemmingsjournalen uit.</span><span class="sxs-lookup"><span data-stu-id="2726e-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="2726e-119">Geef bankafschriften en banktransacties van Finance and Operations naast elkaar weer.</span><span class="sxs-lookup"><span data-stu-id="2726e-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="2726e-120">Boek banktransacties van Finance and Operations automatisch als deze op een bankafschrift worden weergegeven, maar niet in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2726e-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="2726e-121">Genereer een afstemmingsafschrift.</span><span class="sxs-lookup"><span data-stu-id="2726e-121">Generate a reconciliation statement.</span></span>






