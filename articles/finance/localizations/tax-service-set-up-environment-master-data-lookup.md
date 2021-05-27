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
# <a name="set-up-an-environment-for-master-data-lookup"></a>Een omgeving instellen voor het opzoeken van hoofdgegevens

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u uw omgeving instelt om de zoekfunctie voor hoofdgegevens voor Belastingberekening te gebruiken.

1. Integratie van Power Platform instellen in Lifecycle Services (LCS). Zie [Integratie van Microsoft Power Platform - Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie.
2. Dynamics 365 Finance en Microsoft Dataverse instellen. Zie [De oplossing ophalen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) en [Verificatie en autorisatie](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization) voor meer informatie.
3. Stel de volgende entiteiten in. Zie [Virtuele entiteiten inschakelen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities) voor meer informatie.
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. Dynamics 365 Regulatory Configuration Service (RCS) instellen. 
5. Maak een serviceaanvraag voor Microsoft om flights met de volgende functies mogelijk te maken:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Ga naar het werkgebied **Functiebeheer** en schakel de volgende functies in:

      - (Preview) Ondersteuning voor Dataverse-gegevensbronnen voor elektronische rapportage
      - (Preview) Ondersteuning voor Dataverse-gegevensbronnen van de Belastingdienst
      - (Preview) Globalisatiefuncties

5. Meld u aan bij RCS met een beheerderaccount voor tenants.
6. Ga naar **Elektronische rapportage** > **Gekoppelde toepassingen**. 
7. Selecteer **Nieuw** om een record toe te voegen en voer de volgende veldgegevens in. 

   - Voer in het veld **Naam** een naam in.
   - Selecteer **Dataverse** in het veld **Type**.
   - Voer in het veld **Toepassing** de Dataverse-URL in.
   - Voer in het veld **Tenant** uw tenant in.
   - Voer in het veld **Aangepaste URL** uw Dataverse-URL in en voeg deze toe met '/api/data/v9.1'.

8. Selecteer **Verbinding controleren** en voltooi het verbindingsproces. 

   [![Knop Verbinding controleren](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Ga naar **Elektronische rapportage** > **Belastingconfiguraties** en importeer belastingconfiguraties vanuit [Belastingconfiguraties](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Pagina Belastingconfiguraties, structuur belastinggegevensmodel](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Ga naar **Modeltoewijzing belastbaar document** of **Dataverse-modeltoewijzing** als u een Microsoft-configuratie gebruikt en selecteer in het veld **Verbonden toepassing** de record die u in stap 7 hebt gemaakt.
11. Stel **Standaard voor modeltoewijzing** in op **Ja**.

   [![Pagina Modeltoewijzingen](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
