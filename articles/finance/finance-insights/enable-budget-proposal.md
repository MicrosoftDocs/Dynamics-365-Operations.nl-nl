---
title: Budgetvoorstellen inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646200"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="779b6-103">Budgetvoorstellen inschakelen (preview)</span><span class="sxs-lookup"><span data-stu-id="779b6-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="779b6-104">In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="779b6-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="779b6-105">Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving.</span><span class="sxs-lookup"><span data-stu-id="779b6-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="779b6-106">Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="779b6-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="779b6-107">(Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="779b6-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="779b6-108">Als uw implementatie van Microsoft Dynamics 365 Finance een Service Fabric-implementatie is, kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="779b6-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="779b6-109">Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="779b6-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="779b6-110">Als u de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt bij het inschakelen van de functie, verzendt u een e-mail naar het [team voor de preview van de Financiële inzichten-app](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="779b6-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="779b6-111">Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="779b6-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="779b6-112">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="779b6-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="779b6-113">Zoek **Budgetvoorstel** en schakel de functie in.</span><span class="sxs-lookup"><span data-stu-id="779b6-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="779b6-114">Ga naar **Budgettering \> Instellen \> Basisbudgettering \> Budgetvoorstel (preview)** en selecteer **Functie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="779b6-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="779b6-115">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="779b6-115">Privacy notice</span></span>
<span data-ttu-id="779b6-116">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="779b6-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
