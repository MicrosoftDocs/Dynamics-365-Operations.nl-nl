---
title: Overzicht van Project Service Automation
description: Dit onderwerp bevat informatie over de oplossing voor integratie van Dynamics 365 Project Service Automation en Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250548"
---
# <a name="project-service-automation-overview"></a>Overzicht van Project Service Automation

[!include[banner](../includes/banner.md)]

De oplossing voor integratie van Project Service Automation en Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Dynamics 365 Finance en Dynamics 365 Project Service Automation via Common Data Service. De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maakt de stroom van projecten, projectcontracten, projectcontractregels, projectcontractregelmijlpalen, projecttaken, onkostentransactiecategorieën, uurramingen en onkostenramingen van Project Service Automation naar Finance mogelijk.

> [!NOTE]
> - Als u versie 7.3.0 gebruikt, moet u KB 4074835 installeren. U kunt dan projecten met vaste prijs integreren.
> - Als u gebruikmaakt van versie 7.3.0 en u bijzondere-kostentransacties overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten op te nemen in de projectfactuur.
> - Als u versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling gebruiken.
> - Als u gebruikmaakt van versie 8.0.1 of later, kunt u werkelijke waarden synchroniseren.

Voordat u Project Service Automation kunt integreren met Finance, moet u de integratieparameters van Project Service Automation configureren. Zie [Integratieparameters van Project Service Automation](PSA-parameters.md) voor meer informatie.

Met deze integratieoplossing is directe synchronisatie mogelijk in de volgende scenario's:

- Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Onderhoud mijlpalen voor projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Onderhoud onkostentransactiecategorieën in Finance en synchroniseer ze rechtstreeks van Finance naar Project Service Automation.
- Maak projectuurramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Maak projectkostenramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance.
- Maak projecttijd, onkosten en bijzondere kosten werkelijke waarden in Project Service Automation en maak projecttransacties in het integratiejournaal van Project Service Automation zodat deze kunnen worden geboekt in Finance.

## <a name="data-synchronization"></a>Gegevenssynchronisatie

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance.

> [!NOTE]
> Niet alle sjablonen zijn momenteel beschikbaar. Sjablonen wordt vrijgegeven zodra ze gereed zijn.

[![Project Service Automation-integratie met Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systeemvereisten voor Finance

Om de integratieoplossing van Project Service Automation naar Finance te gebruiken moet u Enterprise Edition 7.3 met Platformupdate 12 of hoger installeren.

## <a name="system-requirements-for-project-service-automation"></a>Systeemvereisten voor Project Service Automation

Als u de integratieoplossing van Project Service Automation naar Finance wilt gebruiken, moet u de volgende onderdelen installeren:

- Dynamics 365 Project Service Automation versie 9.0.0.0 of hoger
- De oplossing Prospect naar contant geld voor Dynamics 365 Sales, versie 1.14.0.0 (v14) of hoger
- De oplossing Project Service Automation-integratie naar Finance voor Dynamics 365 Project Service Automation versie 1.0.0.0 of hoger

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installeer de integratieoplossing van Project Service Automation naar Finance in uw exemplaar van Project Service Automation

Download de integratieoplossing Project Service Automation naar Finance vanuit het [Microsoft Downloadcentrum](https://www.microsoft.com/download/details.aspx?id=57016) en volg de instructies die zijn meegeleverd met de oplossing.
