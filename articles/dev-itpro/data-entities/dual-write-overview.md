---
title: Near realtime gegevensintegratie tussen Finance and Operations en Common Data Service
description: In dit onderwerp vindt u een overzicht van de integratie tussen Microsoft Dynamics 365 for Finance and Operations en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797223"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Near realtime gegevensintegratie tussen Finance and Operations en Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

In de huidige digitale wereld gebruiken bedrijfsecosystemen de Microsoft Dynamics 365 Suite als geheel. Omdat gegevens van mensen, klanten, bewerkingen en IoT-apparaten (Internet of Things) in één bron terechtkomen, ontstaat er een mogelijkheid voor digitale feedbacklussen. Om deze ervaring te bereiken, is integratie tussen Dynamics 365 for Finance and Operations en Dynamics 365 for Customer Engagement-toepassingen essentieel. Customer Engagement-toepassingen zijn gebouwd op Common Data Service. Dankzij de integratie tussen Finance and Operations-gegevens en Common Data Service kunnen Customer Engagement-toepassingen coherent en vloeiend communiceren met Finance and Operations.

Finance and Operations en Common Data Service bieden voor near realtime gegevenssynchronisatie tussen Finance and Operations en Customer Engagement-toepassingen via een famework voor Twee keer wegschrijven. De dekking is breed en beslaat 28 oppervlaktegebieden van Finance and Operations. Het doel is om een 'Eén Dynamics 365'-gebruikerservaring te bieden via naadloze gegevensstromen die bedrijfsprocessen tussen toepassingen verbinden.

![Overzichtsdiagram van de architectuur](media/dual-write-overview.jpg)

De volgende waardeproposities zijn beschikbaar voor klanten:

+ [Organisatiehiërarchie in Common Data Service](dual-write-organization.md)
+ [Bedrijfsconcept in Common Data Service](dual-write-company.md)
+ [Geïntegreerd klantmodel](dual-write-customer.md)
+ [Geïntegreerd leveranciersmodel](dual-write-vendor.md)
+ Uniform productmodel

## <a name="system-requirements"></a>Systeemvereisten

Synchrone, bidirectionele, near realtime gegevensstromen vereisen de volgende versies:

+ Microsoft Dynamics 365 for Finance and Operations versie 10.0.4 (juli 2019) met platformupdate 28 of hoger
+ Microsoft Dynamics 365 for Customer Engagement, platformversie 9.1 (4.2) of hoger

## <a name="setup-instructions"></a>Instructies voor instellingen

Volg deze stappen om de integratie tussen Finance and Operations en Common Data Service in te stellen.
    
1. Voor de installatie van het systeem voor Twee keer wegschrijven raadpleegt u de [stapsgewijze handleiding](https://aka.ms/dualwrite-docs) over het aankondigen van de preview voor Twee keer wegschrijven.
2. Download en installeer de oplossing vanuit de groep [Integratie tussen Finance and Operations, Common Data Service en Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer. Het pakket bevat vijf oplossingen:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Volg de uitvoeringsvolgorde voor [Eerste referentiegegevens synchroniseren](dual-write-initial.md).
4. Als u problemen ondervindt met de synchronisatie voor Twee keer wegschrijven, raadpleegt u de [Probleemoplossingsgids voor gegevensintegratie](dual-write-troubleshooting.md).

> [!IMPORTANT]
> U kunt Twee keer wegschrijven en [Prospect naar contant geld](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) niet naast elkaar uitvoeren. Als u de oplossing Prospect naar contant geld uitvoert, moet u deze verwijderen. U moet ook de klant- en leveranciersjablonen voor Twee keer wegschrijven uitschakelen die deel uitmaken van de oplossing Prospect naar contant geld.
