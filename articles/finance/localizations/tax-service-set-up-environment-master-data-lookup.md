---
title: Een omgeving instellen voor het opzoeken van hoofdgegevens
description: In dit onderwerp wordt uitgelegd hoe u uw omgeving instelt om de zoekfunctie voor hoofdgegevens voor Belastingberekening te gebruiken.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869055"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="1617e-103">Een omgeving instellen voor het opzoeken van hoofdgegevens</span><span class="sxs-lookup"><span data-stu-id="1617e-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1617e-104">In dit onderwerp wordt uitgelegd hoe u uw omgeving instelt om de zoekfunctie voor hoofdgegevens voor Belastingberekening te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1617e-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="1617e-105">Integratie van Power Platform instellen in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1617e-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="1617e-106">Zie [Integratie van Microsoft Power Platform - Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1617e-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="1617e-107">Dynamics 365 Finance en Microsoft Dataverse instellen.</span><span class="sxs-lookup"><span data-stu-id="1617e-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="1617e-108">Zie [De oplossing ophalen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) en [Verificatie en autorisatie](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1617e-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="1617e-109">Importeer de *vereiste oplossing voor de virtuele entiteit belastingservice* uit de [Virtuele entiteit voor de belastingservice](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="1617e-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="1617e-110">Dynamics 365 Regulatory Configuration Service (RCS) instellen.</span><span class="sxs-lookup"><span data-stu-id="1617e-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="1617e-111">Maak een serviceaanvraag voor Microsoft om flights met de volgende functies mogelijk te maken:</span><span class="sxs-lookup"><span data-stu-id="1617e-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="1617e-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="1617e-112">ERCdsFeature</span></span>
      - <span data-ttu-id="1617e-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="1617e-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="1617e-114">Schakel in Finance in het werkgebied **Functiebeheer** de volgende functies in:</span><span class="sxs-lookup"><span data-stu-id="1617e-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="1617e-115">(Preview) Ondersteuning voor Dataverse-gegevensbronnen voor elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1617e-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="1617e-116">(Preview) Ondersteuning voor Dataverse-gegevensbronnen van de Belastingdienst</span><span class="sxs-lookup"><span data-stu-id="1617e-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="1617e-117">(Preview) Globalisatiefuncties</span><span class="sxs-lookup"><span data-stu-id="1617e-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="1617e-118">Meld u aan bij RCS met een beheerderaccount voor tenants.</span><span class="sxs-lookup"><span data-stu-id="1617e-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="1617e-119">Ga naar **Elektronische rapportage** > **Gekoppelde toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="1617e-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="1617e-120">Selecteer **Nieuw** om een record toe te voegen en voer de volgende veldgegevens in.</span><span class="sxs-lookup"><span data-stu-id="1617e-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="1617e-121">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="1617e-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="1617e-122">Selecteer **Dataverse** in het veld **Type**.</span><span class="sxs-lookup"><span data-stu-id="1617e-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="1617e-123">Voer in het veld **Toepassing** de Dataverse-URL in.</span><span class="sxs-lookup"><span data-stu-id="1617e-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="1617e-124">Voer in het veld **Tenant** uw tenant in.</span><span class="sxs-lookup"><span data-stu-id="1617e-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="1617e-125">Voer in het veld **Aangepaste URL** uw Dataverse-URL in en voeg deze toe met '/api/data/v9.1'.</span><span class="sxs-lookup"><span data-stu-id="1617e-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="1617e-126">Selecteer **Verbinding controleren** en voltooi het verbindingsproces.</span><span class="sxs-lookup"><span data-stu-id="1617e-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="1617e-127">[![Knop Verbinding controleren](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="1617e-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="1617e-128">Ga naar **Elektronische rapportage** > **Belastingconfiguraties** en importeer belastingconfiguraties vanuit [Belastingconfiguraties](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="1617e-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="1617e-129">[![Pagina Belastingconfiguraties, structuur belastinggegevensmodel](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="1617e-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="1617e-130">Ga naar **Modeltoewijzing belastbaar document** of **Dataverse-modeltoewijzing** als u een Microsoft-configuratie gebruikt en selecteer in het veld **Verbonden toepassing** de record die u in stap 7 hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1617e-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="1617e-131">Stel **Standaard voor modeltoewijzing** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1617e-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="1617e-132">[![Pagina Modeltoewijzingen](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="1617e-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
