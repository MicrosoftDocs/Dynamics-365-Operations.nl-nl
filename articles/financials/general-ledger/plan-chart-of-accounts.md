---
title: Uw rekeningschema plannen
description: Dit onderwerp bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93d5ef19a4b1cb2885c611c8675ac06fd841ac56
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "337573"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="d80eb-103">Uw rekeningschema plannen</span><span class="sxs-lookup"><span data-stu-id="d80eb-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d80eb-104">Dit onderwerp bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.</span><span class="sxs-lookup"><span data-stu-id="d80eb-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="d80eb-105">Als u financiële gegevens in een organisatie wilt bijhouden en onderhouden, kunt u een rekeningschema instellen.</span><span class="sxs-lookup"><span data-stu-id="d80eb-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="d80eb-106">Een rekeningschema is een verzameling van rekeningen waarmee een financieel raamwerk wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d80eb-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="d80eb-107">Als u de transacties in deze rekeningen wilt bijhouden, kunt u segmenten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d80eb-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="d80eb-108">Deze segmenten worden financiële dimensies genoemd.</span><span class="sxs-lookup"><span data-stu-id="d80eb-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="d80eb-109">Een onkostenrekening kan bijvoorbeeld financiële dimensies bevatten met de naam Afdeling, Kostenplaats en Doel.</span><span class="sxs-lookup"><span data-stu-id="d80eb-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="d80eb-110">Met door de gebruiker gedefinieerde regels wordt bepaald hoe financiële dimensies worden gekoppeld aan de hoofdrekeningen en andere financiële dimensies, en ook hoe transacties worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="d80eb-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="d80eb-111">Deze door de gebruiker gedefinieerde regels worden rekeningstructuren en geavanceerde regels genoemd.</span><span class="sxs-lookup"><span data-stu-id="d80eb-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="d80eb-112">Het rekeningschema is een gestructureerde lijst van de grootboekrekeningen van een rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d80eb-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="d80eb-113">De lijst wordt gebruikt om financiële rapporten voor te bereiden voor autoriteiten en eigenaren.</span><span class="sxs-lookup"><span data-stu-id="d80eb-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="d80eb-114">De rekeningen worden eerst gegroepeerd in typen rekeningen en worden verder in grotere categorieën samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="d80eb-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="d80eb-115">Op het meest algemene niveau zijn de rekeningen gegroepeerd als opbrengsten en kosten (exploitatierekeningen) en activa en passiva (balansrekeningen).</span><span class="sxs-lookup"><span data-stu-id="d80eb-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="d80eb-116">Een rekeningschema kan door elke rechtspersoon in een organisatie worden gedeeld en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d80eb-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="d80eb-117">Het rekeningschema dat door een rechtspersoon wordt gebruikt, wordt gedefinieerd op de pagina **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="d80eb-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="d80eb-118">Hierna vindt u een aantal factoren waarmee u rekening dient te houden wanneer u de structuur van het rekeningschema voor uw organisatie plant:</span><span class="sxs-lookup"><span data-stu-id="d80eb-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="d80eb-119">De rapportagevereisten van het land of de regio waarin uw organisatie zich bevindt</span><span class="sxs-lookup"><span data-stu-id="d80eb-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="d80eb-120">De rapportage-eisen van uw rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="d80eb-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="d80eb-121">De mate van specificatie die nodig is, zowel voor externe instanties als voor uw organisatie</span><span class="sxs-lookup"><span data-stu-id="d80eb-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="d80eb-122">U maakt het rekeningschema op de pagina **Rekeningschema**.</span><span class="sxs-lookup"><span data-stu-id="d80eb-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="d80eb-123">U kunt hoofdrekeningen maken op de pagina **Rekeningschema** of de pagina **Hoofdrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="d80eb-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="d80eb-124">Voor uw hoofdrekeningen mogen geen speciale tekens worden gebruikt die als scheidingstekens voor het rekeningschema worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d80eb-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="d80eb-125">Anders wordt het systeem instabiel of moet u altijd wellicht zoekopdrachten of het dialoogvenster gebruiken wanneer u combinaties van rekeningen en dimensies opgeeft.</span><span class="sxs-lookup"><span data-stu-id="d80eb-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="d80eb-126">Zie [Een hoofdrekening maken](tasks/create-main-account.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d80eb-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d80eb-127">In Microsoft Dynamics for Finance and Operations versie 8.0 (april 2018) kunt u het scheidingsteken uit het rekeningschema van de pagina **Grootboekparameters** wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d80eb-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="d80eb-128">Het is daarom raadzaam de hoofdrekeningen te koppelen aan hoofdrekeningcategorieën, zodat u kunt profiteren van de financiële standaardrapporten zonder dat u wijzigingen hoeft aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="d80eb-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="d80eb-129">Zo kunt u rapporten sneller en eenvoudig ontwerpen en onderhouden.</span><span class="sxs-lookup"><span data-stu-id="d80eb-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="d80eb-130">U kunt rekeningstructuren maken op de pagina **Rekeningstructuren configureren**.</span><span class="sxs-lookup"><span data-stu-id="d80eb-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="d80eb-131">Met rekeningstructuren worden geldige combinaties gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d80eb-131">Account structures define valid combinations.</span></span> <span data-ttu-id="d80eb-132">Deze combinaties vormen, samen met de hoofdrekeningen, een rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="d80eb-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="d80eb-133">Zie [Rekeningstructuren maken](tasks/create-account-structures.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d80eb-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="d80eb-134">**Overschrijvingen rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="d80eb-134">**Legal entity overrides**</span></span>

<span data-ttu-id="d80eb-135">Niet alle hoofdrekeningen zijn geldig voor alle rechtspersonen en sommige hoofdrekeningen zijn mogelijk alleen relevant voor een specifiek tijdsbestek.</span><span class="sxs-lookup"><span data-stu-id="d80eb-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="d80eb-136">In dit scenario kunt u de sectie **Overschrijvingen rechtspersoon** gebruiken om de bedrijven te identificeren waarvoor de hoofdrekening moet worden opgeschort, wie de eigenaar is en gedurende welke periode de dimensie actief is.</span><span class="sxs-lookup"><span data-stu-id="d80eb-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="d80eb-137">De overschrijvingen op het gedeelde niveau kunnen niet beperkender zijn dan de overschrijvingen op rechtspersoonniveau.</span><span class="sxs-lookup"><span data-stu-id="d80eb-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="d80eb-138">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d80eb-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d80eb-139">Financiële dimensies</span><span class="sxs-lookup"><span data-stu-id="d80eb-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="d80eb-140">Geavanceerde regelstructuren maken en toewijzen</span><span class="sxs-lookup"><span data-stu-id="d80eb-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
