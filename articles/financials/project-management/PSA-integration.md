---
title: Project Service Automation
description: Dit onderwerp biedt informatie over de integratieoplossing voor Project Service Automatisering met Finance and Operations. Deze integratieoplossing gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

De integratieoplossing voor Project Service Automation met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via Common Data Service. De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maakt de stroom van projecten, projectcontracten, projectcontractregels, projectcontractregelmijlpalen, projecttaken, onkostentransactiecategorieën, uurramingen en onkostenramingen van Project Service Automation naar Finance and Operations mogelijk.

> [!NOTE]
> - Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.
> - Als u Finance and Operations 7.3.0 gebruikt, moet u KB 4074835 installeren. U kunt dan projecten met vaste prijs integreren.
> - Als u gebruikmaakt van Finance and Operations 7.3.0 en u bijzondere-kostentransacties overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten op te nemen in de projectfactuur.
> - Als u Microsoft Dynamics 365 for Finance and Operations versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling gebruiken.
> - Als u Microsoft Dynamics 365 for Finance and Operations 8.0.1 of hoger gebruikt, kunt u werkelijke waarden synchroniseren.

Voordat u Project Service Automation kunt integreren met Finance and Operations, moet u de integratieparameters van Project Service Automation configureren. Zie [Integratieparameters van Project Service Automation](PSA-parameters.md) voor meer informatie.

Met deze integratieoplossing is directe synchronisatie mogelijk in de volgende scenario's:

- Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud projectcontractregelmijlpalen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud onkostentransactiecategorieën in Finance and Operations en synchroniseer ze rechtstreeks van Finance and Operations naar Project Service Automation.
- Maak projectuurramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Maak projectkostenramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Maak projecttijd, onkosten en bijzondere kosten werkelijke waarden in Project Service Automation en maak projecttransacties in het integratiejournaal van Project Service Automation zodat deze kunnen worden geboekt in Finance and Operations.

## <a name="data-synchronization"></a>Gegevenssynchronisatie

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance and Operations.

> [!NOTE]
> Niet alle sjablonen zijn momenteel beschikbaar. Sjablonen wordt vrijgegeven zodra ze gereed zijn.

[![Integratie van Project Service Automation met Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations

Om de integratieoplossing van Project Service Automation naar Finance and Operations te gebruiken moet u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 met platformupdate 12 of hoger installeren.

## <a name="system-requirements-for-project-service-automation"></a>Systeemvereisten voor Project Service Automation

Als u de integratieoplossing van Project Service Automation naar Finance and Operations wilt gebruiken, moet u de volgende onderdelen installeren:

- Microsoft Dynamics 365 for Project Service Automation versie 9.0.0.0 of hoger
- De oplossing Prospect naar contant geld voor Microsoft Dynamics 365 for Sales, versie 1.14.0.0 (v14) of hoger
- Oplossing Project Service Automation naar Finance and Operations voor Microsoft Dynamics 365 for Project Service Automation versie 1.0.0.0 of hoger

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>De integratieoplossing van Project Service Automation naar Finance and Operations installeren in uw exemplaar van Project Service Automation

Download de integratieoplossing Project Service Automation naar Finance and Operations vanuit het [Microsoft Downloadcentrum](https://www.microsoft.com/en-us/download/details.aspx?id=57016) en volg de instructies die zijn meegeleverd met de oplossing.

