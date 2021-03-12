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
ms.openlocfilehash: da56501f58e9f5755a72419a41ab704739fa65db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002882"
---
# <a name="audit-file-xml-auditfile-financieel-xaf"></a><span data-ttu-id="48bef-103">Auditfile (XML Auditfile Financieel, XAF)</span><span class="sxs-lookup"><span data-stu-id="48bef-103">Audit file (XML Auditfile Financieel, XAF)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48bef-104">Deze functionaliteit is beschikbaar voor rechtspersonen waarvan het primaire adres in Nederland is.</span><span class="sxs-lookup"><span data-stu-id="48bef-104">This functionality is available for legal entities whose primary address is in the Netherlands.</span></span>

<span data-ttu-id="48bef-105">In dit onderwerp wordt uitgelegd hoe u ER-configuraties voor de auditfile importeert en vervolgens de auditfile voor rechtspersonen in Nederland genereert.</span><span class="sxs-lookup"><span data-stu-id="48bef-105">This topic explains how to import Electronic reporting (ER) configurations for the Audit file and then generate the Audit file for legal entities in the Netherlands.</span></span>

## <a name="import-and-set-up-er-configurations"></a><span data-ttu-id="48bef-106">ER-configuraties importeren en instellen</span><span class="sxs-lookup"><span data-stu-id="48bef-106">Import and set up ER configurations</span></span>

<span data-ttu-id="48bef-107">Als u Microsoft Dynamics 365 Finance wilt voorbereiden op het genereren van het auditfile, moet u de volgende ER-configuraties importeren.</span><span class="sxs-lookup"><span data-stu-id="48bef-107">To prepare Microsoft Dynamics 365 Finance to generate the Audit file, you must import the following ER configurations.</span></span>

| <span data-ttu-id="48bef-108">Nummer</span><span class="sxs-lookup"><span data-stu-id="48bef-108">Number</span></span> | <span data-ttu-id="48bef-109">Naam van ER-configuratie</span><span class="sxs-lookup"><span data-stu-id="48bef-109">ER configuration name</span></span>         | <span data-ttu-id="48bef-110">Type</span><span class="sxs-lookup"><span data-stu-id="48bef-110">Type</span></span>                                 | <span data-ttu-id="48bef-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="48bef-111">Description</span></span> |
|--------|-------------------------------|--------------------------------------|-------------|
| <span data-ttu-id="48bef-112">1</span><span class="sxs-lookup"><span data-stu-id="48bef-112">1</span></span>      | <span data-ttu-id="48bef-113">Model van auditfile</span><span class="sxs-lookup"><span data-stu-id="48bef-113">Audit file model</span></span>              | <span data-ttu-id="48bef-114">Model</span><span class="sxs-lookup"><span data-stu-id="48bef-114">Model</span></span>                                | <span data-ttu-id="48bef-115">Een model voor het auditfile voor Nederland.</span><span class="sxs-lookup"><span data-stu-id="48bef-115">A model for the Audit file for Netherlands.</span></span> |
| <span data-ttu-id="48bef-116">2</span><span class="sxs-lookup"><span data-stu-id="48bef-116">2</span></span>      | <span data-ttu-id="48bef-117">Auditfile (NL)</span><span class="sxs-lookup"><span data-stu-id="48bef-117">Audit file (NL)</span></span>               | <span data-ttu-id="48bef-118">Indeling (exporteren)</span><span class="sxs-lookup"><span data-stu-id="48bef-118">Format (exporting)</span></span>                   | <span data-ttu-id="48bef-119">ER-indeling voor XML Auditfile Financieel, XAF.</span><span class="sxs-lookup"><span data-stu-id="48bef-119">ER format for XML Auditfile Financieel, XAF.</span></span> |

## <a name="generate-the-audit-file"></a><span data-ttu-id="48bef-120">Het auditfile genereren</span><span class="sxs-lookup"><span data-stu-id="48bef-120">Generate the Audit file</span></span>

<span data-ttu-id="48bef-121">Met de stappen in deze procedure wordt uitgelegd hoe u de auditfile gebruikt.</span><span class="sxs-lookup"><span data-stu-id="48bef-121">The steps in this procedure walk you through using the Audit file.</span></span>

1. <span data-ttu-id="48bef-122">Ga naar **Grootboek** > **Periodieke taken** > **Auditfile**.</span><span class="sxs-lookup"><span data-stu-id="48bef-122">Go to **General ledger** > **Periodic tasks** > **Audit file**.</span></span>
2. <span data-ttu-id="48bef-123">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="48bef-123">In the **From date** field, enter a date.</span></span> 
3. <span data-ttu-id="48bef-124">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="48bef-124">In the **To date** field, enter a date.</span></span> 
4. <span data-ttu-id="48bef-125">Typ **Auditfile (NL)** in het veld **Indelingstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="48bef-125">In the **Format mapping** field, enter **Audit file (NL)**.</span></span>
5. <span data-ttu-id="48bef-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="48bef-126">Select **OK**.</span></span>
