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
# <a name="set-up-an-environment-for-master-data-lookup"></a>Een omgeving instellen voor het opzoeken van hoofdgegevens

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u uw omgeving instelt om de zoekfunctie voor hoofdgegevens voor Belastingberekening te gebruiken.

1. Integratie van Power Platform instellen in Lifecycle Services (LCS). Zie [Integratie van Microsoft Power Platform - Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie.
2. Dynamics 365 Finance en Microsoft Dataverse instellen. Zie [De oplossing ophalen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) en [Verificatie en autorisatie](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization) voor meer informatie.
3. Importeer de *vereiste oplossing voor de virtuele entiteit belastingservice* uit de [Virtuele entiteit voor de belastingservice](https://go.microsoft.com/fwlink/?linkid=2158160).
4. Dynamics 365 Regulatory Configuration Service (RCS) instellen. 
5. Maak een serviceaanvraag voor Microsoft om flights met de volgende functies mogelijk te maken:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Schakel in Finance in het werkgebied **Functiebeheer** de volgende functies in:

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
