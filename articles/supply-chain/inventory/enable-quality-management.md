---
title: Beheer van kwaliteit en niet-conformeringen inschakelen
description: Dit onderwerp bevat een overzicht van het proces voor het instellen en configureren van de functies voor beheer van kwaliteit en niet-conformeringen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956249"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="25f05-103">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="25f05-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25f05-104">Dit onderwerp bevat een overzicht van het proces voor het instellen en configureren van de functies voor beheer van kwaliteit en niet-conformeringen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25f05-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="25f05-105">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="25f05-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="25f05-106">Volg deze stappen om kwaliteitsbeheer op uw systeem in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="25f05-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="25f05-107">Ga naar **Voorraadbeheer \> Instellen \> Parameters voor voorraad- en magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="25f05-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="25f05-108">Stel op het tabblad **Kwaliteitsbeheer** de optie **Kwaliteitsbeheer gebruiken** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="25f05-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="25f05-109">Voer in het veld **Uurtarief** een uurtarief in de lokale valuta in.</span><span class="sxs-lookup"><span data-stu-id="25f05-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="25f05-110">Het uurtarief wordt gebruikt voor het berekenen van de kosten voor bewerkingen die zijn gerelateerd aan een niet-conformering.</span><span class="sxs-lookup"><span data-stu-id="25f05-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="25f05-111">Het uurtarief en de berekende kosten vormen referentiegegevens voor een niet-conformering.</span><span class="sxs-lookup"><span data-stu-id="25f05-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="25f05-112">Ze worden niet samen met andere functies gebruikt.</span><span class="sxs-lookup"><span data-stu-id="25f05-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="25f05-113">Selecteer **Rapportinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="25f05-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="25f05-114">Voeg nieuwe regels toe voor de verschillende rapporttypen en selecteer het type document dat u voor elk rapport wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="25f05-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="25f05-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="25f05-115">Close the page.</span></span>
1. <span data-ttu-id="25f05-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="25f05-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="25f05-117">Het proces voor configureren van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="25f05-117">Quality management configuration process</span></span>

<span data-ttu-id="25f05-118">Voordat u de functies voor kwaliteitsbeheer kunt gebruiken en kwaliteitsorders kunt genereren, moet u het systeem en de vereisten configureren.</span><span class="sxs-lookup"><span data-stu-id="25f05-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="25f05-119">Hieronder volgt een lijst met de stappen die nodig zijn om kwaliteitsbeheer te configureren.</span><span class="sxs-lookup"><span data-stu-id="25f05-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="25f05-120">[Beheer van kwaliteit en niet-conformeringen inschakelen](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="25f05-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="25f05-121">Optioneel: [Testinstrumenten configureren](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="25f05-122">[Tests configureren](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="25f05-123">[Testvariabelen en resultaten configureren](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="25f05-124">[Testgroepen configureren](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="25f05-125">Optioneel: [Kwaliteitsgroepen configureren en aan producten koppelen](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="25f05-126">Optioneel: [Kwaliteitskoppelingen configureren](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="25f05-127">Nadat het configureren is voltooid, kunt u beginnen met het maken en verwerken van kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="25f05-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="25f05-128">Meer informatie over het maken van en werken met kwaliteitsorders vindt u in [Kwaliteitsorders](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="25f05-129">Het proces voor configureren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="25f05-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="25f05-130">Voordat u de functies voor beheer van niet-conformeringen kunt gebruiken en niet-conformeringen kunt genereren, moet u het systeem en de vereisten configureren.</span><span class="sxs-lookup"><span data-stu-id="25f05-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="25f05-131">Hieronder volgt een lijst met de stappen die nodig zijn om het beheer van niet-conformeringen te configureren.</span><span class="sxs-lookup"><span data-stu-id="25f05-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="25f05-132">[Beheer van kwaliteit en niet-conformeringen inschakelen](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="25f05-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="25f05-133">[Medewerkers configureren die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="25f05-134">[Probleemtypen configureren](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="25f05-135">[Quarantainezones configureren](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="25f05-136">[Diagnosetypen configureren](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="25f05-137">[Bewerkingen configureren](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="25f05-138">Optioneel: [Kwaliteitstoeslagen configureren](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="25f05-139">Nadat het configureren is voltooid, kunt u beginnen met het maken en verwerken van niet-conformeringen.</span><span class="sxs-lookup"><span data-stu-id="25f05-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="25f05-140">Meer informatie over het maken van en werken met niet-conformeringen vindt u in [Niet-conformeringen maken en verwerken](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="25f05-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25f05-141">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="25f05-141">Additional resources</span></span>

- [<span data-ttu-id="25f05-142">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="25f05-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="25f05-143">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="25f05-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="25f05-144">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="25f05-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
