---
title: Budgetvoorstellen inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222529"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="27be8-103">Budgetvoorstellen inschakelen (preview)</span><span class="sxs-lookup"><span data-stu-id="27be8-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="27be8-104">In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="27be8-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="27be8-105">Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving.</span><span class="sxs-lookup"><span data-stu-id="27be8-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="27be8-106">Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="27be8-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="27be8-107">(Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="27be8-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="27be8-108">Sla deze stap over als u versie 10.0.20 of hoger gebruikt of als u een Service Fabric-implementatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="27be8-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="27be8-109">Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="27be8-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="27be8-110">Als de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="27be8-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="27be8-111">Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="27be8-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="27be8-112">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="27be8-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="27be8-113">Zoek **Budgetvoorstel** en schakel de functie in.</span><span class="sxs-lookup"><span data-stu-id="27be8-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="27be8-114">Ga naar **Budgettering \> Instellen \> Basisbudgettering \> Budgetvoorstel (preview)** en selecteer **Functie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="27be8-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
