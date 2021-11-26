---
title: Zoeken van hoofdgegevens voor btw-berekeningsconfiguratie inschakelen
description: In dit onderwerp wordt uitgelegd hoe u de zoekfunctie voor hoofdgegevens voor belastingberekening kunt instellen en inschakelen.
author: kai-cloud
ms.date: 11/03/2021
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
ms.openlocfilehash: dafeac01aaff62cbbd5ce6ecb0af0ef111f513b2
ms.sourcegitcommit: 76fe020f9c5f4e5cc2e93f5ccb3b040f12b0363e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2021
ms.locfileid: "7749505"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Zoeken van hoofdgegevens voor btw-berekeningsconfiguratie inschakelen 

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de zoekfunctie voor hoofdgegevens voor belastingberekening kunt instellen en inschakelen. Er is een vervolgkeuzelijst beschikbaar voor het selecteren van waarden in de belastingberekeningsconfiguratie voor velden, zoals **Leveranciersrekening**, **Artikelcode** en **Leveringstermijn**. Deze waarden zijn afkomstig uit de verbonden Microsoft Dynamics 365 Finance-omgeving met de Microsoft Dataverse-gegevensbron.

1. De Microsoft Power Platform integratie instellen in Microsoft Dynamics Lifecycle Services (LCS). Zie [Integratie van Microsoft Power Platform - Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie. Nadat u deze stap hebt voltooid, wordt de naam van een Microsoft Power Platform-omgeving weergegeven in de sectie **Power Platform integratie**.
2. Ga naar het [Microsoft Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) en selecteer de omgevingsnaam. De omgevings-URL wordt geleverd.
3. Dynamics 365 Finance en Dataverse instellen. Zie [De oplossing van de virtuele entiteit ophalen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) en [Verificatie en autorisatie](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization) voor meer informatie.
4. Stel de volgende entiteiten in. Zie [Virtuele Microsoft Dataverse-entiteiten inschakelen](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md) voor meer informatie.

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

5. Stel Regulatory Configuration Service (RCS) in. Open het werkgebied **Functiebeheer** en schakel de volgende functies in:

    - Ondersteuning voor Dataverse-gegevensbronnen voor elektronische rapportage
    - Ondersteuning voor Dataverse-gegevensbronnen van de Belastingdienst
    - Globalisatiefuncties

6. Meld u aan bij RCS met een beheerderaccount voor tenants.
7. Ga naar **Elektronische rapportage** > **Gekoppelde toepassingen**. 
8. Selecteer **Nieuw** om een record toe te voegen en voer de volgende veldgegevens in. 

    - Voer in het veld **Naam** een naam in.
    - Selecteer **Dataverse** in het veld **Type**.
    - Voer in het veld **Toepassing** de Dataverse-URL in.
    - Voer in het veld **Tenant** uw tenant in.
    - Voer in het veld **Aangepaste URL** uw Dataverse-URL in en voeg deze toe met '/api/data/v9.1'.

9. Selecteer **Verbinding controleren** en voltooi het verbindingsproces. 

    [![Knop Verbinding controleren.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Ga naar **Elektronische rapportage** > **Belastingconfiguraties** en importeer belastingconfiguraties vanuit [Belastingconfiguraties](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Pagina Belastingconfiguraties, structuur belastinggegevensmodel.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Ga naar **Modeltoewijzing belastbaar document** of **Dataverse-modeltoewijzing** als u een Microsoft-configuratie gebruikt en selecteer in het veld **Verbonden toepassing** de record die u in stap 7 hebt gemaakt.
12. Stel **Standaard voor modeltoewijzing** in op **Ja**.

    [![Pagina Modeltoewijzingen.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
