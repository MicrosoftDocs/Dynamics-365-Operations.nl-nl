---
title: Project Service Automation
description: Deze oplossing gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via de Common Data Service (CDS).
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

De oplossing Project Service Automation-integratie gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via de Common Data Service (CDS). De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maakt de stroom van projecten, projectcontracten, projectcontractregels, projectcontractregelmijlpalen, projecttaken, onkostentransactiecategorieën, uurramingen en onkostenramingen van Project Service Automation naar Finance and Operations mogelijk.

> [!NOTE] 
> Als u werkt met Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0, moet u KB 4074835 installeren. Hierdoor kunt u vaste-prijsprojecten integreren.
>
> Als u Dynamics 365 for Finance and Operations versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling gebruiken.
>
> Als u Dynamics 365 for Finance and Operations 8.0.1 gebruikt, kunt u werkelijke waarden synchroniseren.
>
> Als u Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.

Voordat u Project Service Automation kunt integreren met Finance and Operations, moet u de integratieparameters van Project Service Automation configureren. Zie Integratieparameters van Project Service Automation voor meer informatie.

Met deze integratieoplossing is directe synchronisatie mogelijk in de volgende scenario's:

- Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud projectcontractregelmijlpalen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Onderhoud onkostentransactiecategorieën in Finance and Operations en synchroniseer ze rechtstreeks van Finance and Operations naar Project Service Automation.
- Maak projectuurramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.
- Maak projectkostenramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.

## <a name="data-synchronization"></a>Gegevenssynchronisatie
De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance and Operations.

> [!NOTE]
> Niet alle sjablonen zijn momenteel beschikbaar. Sjablonen wordt vrijgegeven zodra ze gereed zijn.

[![Integratie van Project Service Automation met Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations

Om de integratieoplossing van Project Service Automation naar Finance and Operations te gebruiken moet u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 met platformupdate 12 of hoger installeren.

## <a name="system-requirements-for-project-service-automation"></a>Systeemvereisten voor Project Service Automation

Als u de integratieoplossing van Project Service Automation naar Finance and Operations wilt gebruiken, moet u de volgende onderdelen installeren:

- Microsoft Dynamics 365 for Project Service Automation versie 9.0.0.0 of hoger.
- De oplossing Prospect naar contant geld voor Dynamics 365 for Sales, versie 1.14.0.0 (v14) of hoger.
- Oplossing Project Service Automation naar Operations voor Dynamics 365 for Project Service Automation versie 1.0.0.0 of hoger.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>De integratieoplossing van Project Service Automation naar Finance and Operations installeren in uw exemplaar van Project Service Automation



