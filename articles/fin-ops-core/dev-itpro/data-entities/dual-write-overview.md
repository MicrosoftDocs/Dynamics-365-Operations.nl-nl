---
title: Bijna realtime gegevensintegratie met Common Data Service
description: In dit onderwerp wordt een overzicht gegevens van de integratie tussen Finance and Operations en Common Data Service.
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
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853901"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Bijna realtime gegevensintegratie met Common Data Service

[!include [banner](../includes/banner.md)]

In de huidige digitale wereld gebruiken bedrijfsecosystemen de Microsoft Dynamics 365-toepassingen als geheel. Omdat gegevens van mensen, klanten, bewerkingen en IoT-apparaten (Internet of Things) in één bron terechtkomen, ontstaat er een mogelijkheid voor digitale feedbacklussen. Om deze ervaring te bereiken, is integratie tussen Finance and Operations-apps en andere Dynamics 365-toepassingen essentieel. Bepaalde toepassingen zijn gebouwd op Common Data Service. Dankzij de integratie tussen Finance and Operations-apps en Common Data Service kunnen andere toepassingen coherent en vloeiend communiceren met Finance and Operations.

Finance and Operations-apps en Common Data Service bieden voor near realtime gegevenssynchronisatie tussen Finance and Operations en andere Dynamics 365-toepassingen via een famework voor Twee keer wegschrijven. De dekking is breed en beslaat 28 oppervlaktegebieden van de toepassing. Het doel is om een 'Eén Dynamics 365'-gebruikerservaring te bieden via naadloze gegevensstromen die bedrijfsprocessen tussen toepassingen verbinden.

![Overzichtsdiagram van de architectuur](media/dual-write-overview.jpg)

De volgende waardeproposities zijn beschikbaar:

+ [Organisatiehiërarchie in Common Data Service](dual-write-organization.md)
+ [Bedrijfsconcept in Common Data Service](dual-write-company.md)
+ [Geïntegreerd klantmodel](dual-write-customer.md)
+ [Geïntegreerd grootboek](dual-write-ledger.md)
+ [Uniforme productervaring](dual-write-product.md)
+ [Geïntegreerd leveranciersmodel](dual-write-vendor.md)
+ [Geïntegreerde locaties en magazijnen](dual-write-sites-and-warehouses.md)
+ [Geïntegreerde hoofdgegevens voor belasting](dual-write-tax.md)

## <a name="system-requirements"></a>Systeemvereisten

Synchrone, bidirectionele, near realtime gegevensstromen vereisen de volgende versies:

+ Microsoft Dynamics 365 for Finance and Operations versie 10.0.4 (juli 2019) met platformupdate 28 of hoger
+ Microsoft Dynamics 365 for Customer Engagement, platformversie 9.1 (4.2) of hoger

## <a name="setup-instructions"></a>Instructies voor instellingen

Volg deze stappen om de integratie tussen Finance and Operations-apps en Common Data Service in te stellen.
    
1. Voor de installatie van het systeem voor Twee keer wegschrijven raadpleegt u de [stapsgewijze handleiding](https://aka.ms/dualwrite-docs) over het aankondigen van de preview voor Twee keer wegschrijven.
2. Download en installeer de oplossing via de Yammer-groep [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096). Het pakket bevat vijf oplossingen:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Volg de uitvoeringsvolgorde voor [Eerste referentiegegevens synchroniseren](dual-write-initial.md).
4. Als u problemen ondervindt met de synchronisatie voor Twee keer wegschrijven, raadpleegt u de [Probleemoplossingsgids voor gegevensintegratie](dual-write-troubleshooting.md).

> [!IMPORTANT]
> U kunt Twee keer wegschrijven en [Prospect naar contant geld](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) niet naast elkaar uitvoeren. Als u de oplossing Prospect naar contant geld uitvoert, moet u deze verwijderen. U moet ook de klant- en leveranciersjablonen voor Twee keer wegschrijven uitschakelen die deel uitmaken van de oplossing Prospect naar contant geld.
