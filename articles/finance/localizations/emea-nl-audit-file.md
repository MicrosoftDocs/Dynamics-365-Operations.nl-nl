---
title: Auditfile (XML Auditfile Financieel, XAF)
description: In dit onderwerp wordt uitgelegd hoe u de auditfile voor rechtspersonen in Nederland kunt instellen en genereren.
author: liza-golub
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxEvatParameters_NL
audience: Application User
ms.reviewer: kfend
ms.search.region: Netherlands
ms.author: elgolu
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b97247b4f9c849361c069b115658a05cbdb4dca7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208443"
---
# <a name="audit-file-xml-auditfile-financieel-xaf"></a><span data-ttu-id="8b51e-103">Auditfile (XML Auditfile Financieel, XAF)</span><span class="sxs-lookup"><span data-stu-id="8b51e-103">Audit file (XML Auditfile Financieel, XAF)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b51e-104">Deze functionaliteit is beschikbaar voor rechtspersonen waarvan het primaire adres in Nederland is.</span><span class="sxs-lookup"><span data-stu-id="8b51e-104">This functionality is available for legal entities whose primary address is in the Netherlands.</span></span>

<span data-ttu-id="8b51e-105">In dit onderwerp wordt uitgelegd hoe u ER-configuraties voor de auditfile importeert en vervolgens de auditfile voor rechtspersonen in Nederland genereert.</span><span class="sxs-lookup"><span data-stu-id="8b51e-105">This topic explains how to import Electronic reporting (ER) configurations for the Audit file and then generate the Audit file for legal entities in the Netherlands.</span></span>

## <a name="import-and-set-up-er-configurations"></a><span data-ttu-id="8b51e-106">ER-configuraties importeren en instellen</span><span class="sxs-lookup"><span data-stu-id="8b51e-106">Import and set up ER configurations</span></span>

<span data-ttu-id="8b51e-107">Als u Microsoft Dynamics 365 Finance wilt voorbereiden op het genereren van het auditfile, moet u de volgende ER-configuraties importeren.</span><span class="sxs-lookup"><span data-stu-id="8b51e-107">To prepare Microsoft Dynamics 365 Finance to generate the Audit file, you must import the following ER configurations.</span></span>

| <span data-ttu-id="8b51e-108">Nummer</span><span class="sxs-lookup"><span data-stu-id="8b51e-108">Number</span></span> | <span data-ttu-id="8b51e-109">Naam van ER-configuratie</span><span class="sxs-lookup"><span data-stu-id="8b51e-109">ER configuration name</span></span>         | <span data-ttu-id="8b51e-110">Type</span><span class="sxs-lookup"><span data-stu-id="8b51e-110">Type</span></span>                                 | <span data-ttu-id="8b51e-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="8b51e-111">Description</span></span> |
|--------|-------------------------------|--------------------------------------|-------------|
| <span data-ttu-id="8b51e-112">1</span><span class="sxs-lookup"><span data-stu-id="8b51e-112">1</span></span>      | <span data-ttu-id="8b51e-113">Model van auditfile</span><span class="sxs-lookup"><span data-stu-id="8b51e-113">Audit file model</span></span>              | <span data-ttu-id="8b51e-114">Model</span><span class="sxs-lookup"><span data-stu-id="8b51e-114">Model</span></span>                                | <span data-ttu-id="8b51e-115">Een model voor het auditfile voor Nederland.</span><span class="sxs-lookup"><span data-stu-id="8b51e-115">A model for the Audit file for Netherlands.</span></span> |
| <span data-ttu-id="8b51e-116">2</span><span class="sxs-lookup"><span data-stu-id="8b51e-116">2</span></span>      | <span data-ttu-id="8b51e-117">Auditfile (NL)</span><span class="sxs-lookup"><span data-stu-id="8b51e-117">Audit file (NL)</span></span>               | <span data-ttu-id="8b51e-118">Indeling (exporteren)</span><span class="sxs-lookup"><span data-stu-id="8b51e-118">Format (exporting)</span></span>                   | <span data-ttu-id="8b51e-119">ER-indeling voor XML Auditfile Financieel, XAF.</span><span class="sxs-lookup"><span data-stu-id="8b51e-119">ER format for XML Auditfile Financieel, XAF.</span></span> |

## <a name="generate-the-audit-file"></a><span data-ttu-id="8b51e-120">Het auditfile genereren</span><span class="sxs-lookup"><span data-stu-id="8b51e-120">Generate the Audit file</span></span>

<span data-ttu-id="8b51e-121">Met de stappen in deze procedure wordt uitgelegd hoe u de auditfile gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8b51e-121">The steps in this procedure walk you through using the Audit file.</span></span>

1. <span data-ttu-id="8b51e-122">Ga naar **Grootboek** > **Periodieke taken** > **Auditfile**.</span><span class="sxs-lookup"><span data-stu-id="8b51e-122">Go to **General ledger** > **Periodic tasks** > **Audit file**.</span></span>
2. <span data-ttu-id="8b51e-123">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="8b51e-123">In the **From date** field, enter a date.</span></span> 
3. <span data-ttu-id="8b51e-124">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="8b51e-124">In the **To date** field, enter a date.</span></span> 
4. <span data-ttu-id="8b51e-125">Typ **Auditfile (NL)** in het veld **Indelingstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="8b51e-125">In the **Format mapping** field, enter **Audit file (NL)**.</span></span>
5. <span data-ttu-id="8b51e-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b51e-126">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]