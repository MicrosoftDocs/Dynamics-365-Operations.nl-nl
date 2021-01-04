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
ms.search.scope: Core, Finance
ms.search.region: Netherlands
ms.author: elgolu
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99f90740e802cb1c20d9f05629f1decb0a16ad80
ms.sourcegitcommit: 102c1e998a591a295307c588dfe523cfa750d43c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665500"
---
# <a name="audit-file-xml-auditfile-financieel-xaf"></a><span data-ttu-id="2abe2-103">Auditfile (XML Auditfile Financieel, XAF)</span><span class="sxs-lookup"><span data-stu-id="2abe2-103">Audit file (XML Auditfile Financieel, XAF)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2abe2-104">Deze functionaliteit is beschikbaar voor rechtspersonen waarvan het primaire adres in Nederland is.</span><span class="sxs-lookup"><span data-stu-id="2abe2-104">This functionality is available for legal entities whose primary address is in the Netherlands.</span></span>

<span data-ttu-id="2abe2-105">In dit onderwerp wordt uitgelegd hoe u ER-configuraties voor de auditfile importeert en vervolgens de auditfile voor rechtspersonen in Nederland genereert.</span><span class="sxs-lookup"><span data-stu-id="2abe2-105">This topic explains how to import Electronic reporting (ER) configurations for the Audit file and then generate the Audit file for legal entities in the Netherlands.</span></span>

## <a name="import-and-set-up-er-configurations"></a><span data-ttu-id="2abe2-106">ER-configuraties importeren en instellen</span><span class="sxs-lookup"><span data-stu-id="2abe2-106">Import and set up ER configurations</span></span>

<span data-ttu-id="2abe2-107">Als u Microsoft Dynamics 365 Finance wilt voorbereiden op het genereren van het auditfile, moet u de volgende ER-configuraties importeren.</span><span class="sxs-lookup"><span data-stu-id="2abe2-107">To prepare Microsoft Dynamics 365 Finance to generate the Audit file, you must import the following ER configurations.</span></span>

| <span data-ttu-id="2abe2-108">Nummer</span><span class="sxs-lookup"><span data-stu-id="2abe2-108">Number</span></span> | <span data-ttu-id="2abe2-109">Naam van ER-configuratie</span><span class="sxs-lookup"><span data-stu-id="2abe2-109">ER configuration name</span></span>         | <span data-ttu-id="2abe2-110">Type</span><span class="sxs-lookup"><span data-stu-id="2abe2-110">Type</span></span>                                 | <span data-ttu-id="2abe2-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="2abe2-111">Description</span></span> |
|--------|-------------------------------|--------------------------------------|-------------|
| <span data-ttu-id="2abe2-112">1</span><span class="sxs-lookup"><span data-stu-id="2abe2-112">1</span></span>      | <span data-ttu-id="2abe2-113">Model van auditfile</span><span class="sxs-lookup"><span data-stu-id="2abe2-113">Audit file model</span></span>              | <span data-ttu-id="2abe2-114">Model</span><span class="sxs-lookup"><span data-stu-id="2abe2-114">Model</span></span>                                | <span data-ttu-id="2abe2-115">Een model voor het auditfile voor Nederland.</span><span class="sxs-lookup"><span data-stu-id="2abe2-115">A model for the Audit file for Netherlands.</span></span> |
| <span data-ttu-id="2abe2-116">2</span><span class="sxs-lookup"><span data-stu-id="2abe2-116">2</span></span>      | <span data-ttu-id="2abe2-117">Auditfile (NL)</span><span class="sxs-lookup"><span data-stu-id="2abe2-117">Audit file (NL)</span></span>               | <span data-ttu-id="2abe2-118">Indeling (exporteren)</span><span class="sxs-lookup"><span data-stu-id="2abe2-118">Format (exporting)</span></span>                   | <span data-ttu-id="2abe2-119">ER-indeling voor XML Auditfile Financieel, XAF.</span><span class="sxs-lookup"><span data-stu-id="2abe2-119">ER format for XML Auditfile Financieel, XAF.</span></span> |

## <a name="generate-the-audit-file"></a><span data-ttu-id="2abe2-120">Het auditfile genereren</span><span class="sxs-lookup"><span data-stu-id="2abe2-120">Generate the Audit file</span></span>

<span data-ttu-id="2abe2-121">Met de stappen in deze procedure wordt uitgelegd hoe u de auditfile gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2abe2-121">The steps in this procedure walk you through using the Audit file.</span></span>

1. <span data-ttu-id="2abe2-122">Ga naar **Grootboek** > **Periodieke taken** > **Auditfile**.</span><span class="sxs-lookup"><span data-stu-id="2abe2-122">Go to **General ledger** > **Periodic tasks** > **Audit file**.</span></span>
2. <span data-ttu-id="2abe2-123">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="2abe2-123">In the **From date** field, enter a date.</span></span> 
3. <span data-ttu-id="2abe2-124">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="2abe2-124">In the **To date** field, enter a date.</span></span> 
4. <span data-ttu-id="2abe2-125">Typ **Auditfile (NL)** in het veld **Indelingstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="2abe2-125">In the **Format mapping** field, enter **Audit file (NL)**.</span></span>
5. <span data-ttu-id="2abe2-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2abe2-126">Select **OK**.</span></span>
