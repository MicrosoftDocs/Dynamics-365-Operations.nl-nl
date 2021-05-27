---
title: Een omgeving instellen voor het opzoeken van hoofdgegevens
description: In dit onderwerp wordt uitgelegd hoe u uw omgeving instelt om de zoekfunctie voor hoofdgegevens voor Belastingberekening te gebruiken.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021339"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="1e2bf-103">Een omgeving instellen voor het opzoeken van hoofdgegevens</span><span class="sxs-lookup"><span data-stu-id="1e2bf-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e2bf-104">In dit onderwerp wordt uitgelegd hoe u uw omgeving instelt om de zoekfunctie voor hoofdgegevens voor Belastingberekening te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="1e2bf-105">Integratie van Power Platform instellen in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1e2bf-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="1e2bf-106">Zie [Integratie van Microsoft Power Platform - Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="1e2bf-107">Dynamics 365 Finance en Microsoft Dataverse instellen.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="1e2bf-108">Zie [De oplossing ophalen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) en [Verificatie en autorisatie](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="1e2bf-109">Stel de volgende entiteiten in.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-109">Set up the following entities.</span></span> <span data-ttu-id="1e2bf-110">Zie [Virtuele entiteiten inschakelen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="1e2bf-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="1e2bf-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-112">CurrencyEntity</span></span>
      - <span data-ttu-id="1e2bf-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="1e2bf-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="1e2bf-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="1e2bf-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="1e2bf-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="1e2bf-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="1e2bf-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="1e2bf-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="1e2bf-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="1e2bf-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="1e2bf-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="1e2bf-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="1e2bf-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="1e2bf-125">Dynamics 365 Regulatory Configuration Service (RCS) instellen.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="1e2bf-126">Maak een serviceaanvraag voor Microsoft om flights met de volgende functies mogelijk te maken:</span><span class="sxs-lookup"><span data-stu-id="1e2bf-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="1e2bf-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="1e2bf-127">ERCdsFeature</span></span>
      - <span data-ttu-id="1e2bf-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="1e2bf-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="1e2bf-129">Ga naar het werkgebied **Functiebeheer** en schakel de volgende functies in:</span><span class="sxs-lookup"><span data-stu-id="1e2bf-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="1e2bf-130">(Preview) Ondersteuning voor Dataverse-gegevensbronnen voor elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1e2bf-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="1e2bf-131">(Preview) Ondersteuning voor Dataverse-gegevensbronnen van de Belastingdienst</span><span class="sxs-lookup"><span data-stu-id="1e2bf-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="1e2bf-132">(Preview) Globalisatiefuncties</span><span class="sxs-lookup"><span data-stu-id="1e2bf-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="1e2bf-133">Meld u aan bij RCS met een beheerderaccount voor tenants.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="1e2bf-134">Ga naar **Elektronische rapportage** > **Gekoppelde toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="1e2bf-135">Selecteer **Nieuw** om een record toe te voegen en voer de volgende veldgegevens in.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="1e2bf-136">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="1e2bf-137">Selecteer **Dataverse** in het veld **Type**.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="1e2bf-138">Voer in het veld **Toepassing** de Dataverse-URL in.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="1e2bf-139">Voer in het veld **Tenant** uw tenant in.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="1e2bf-140">Voer in het veld **Aangepaste URL** uw Dataverse-URL in en voeg deze toe met '/api/data/v9.1'.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="1e2bf-141">Selecteer **Verbinding controleren** en voltooi het verbindingsproces.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="1e2bf-142">[![Knop Verbinding controleren](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="1e2bf-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="1e2bf-143">Ga naar **Elektronische rapportage** > **Belastingconfiguraties** en importeer belastingconfiguraties vanuit [Belastingconfiguraties](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="1e2bf-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="1e2bf-144">[![Pagina Belastingconfiguraties, structuur belastinggegevensmodel](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="1e2bf-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="1e2bf-145">Ga naar **Modeltoewijzing belastbaar document** of **Dataverse-modeltoewijzing** als u een Microsoft-configuratie gebruikt en selecteer in het veld **Verbonden toepassing** de record die u in stap 7 hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="1e2bf-146">Stel **Standaard voor modeltoewijzing** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="1e2bf-147">[![Pagina Modeltoewijzingen](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="1e2bf-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
