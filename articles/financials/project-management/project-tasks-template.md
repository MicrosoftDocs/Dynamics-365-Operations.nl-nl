---
title: Projecttaken rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations
description: In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projecttaken rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations, versie 8.0.
> - Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.
> - Integratie van werkelijke waarden is beschikbaar in Microsoft Dynamics 365 for Finance and Operations versie 8.01 of hoger.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gegevensstroom voor Project Service Automation naar Finance and Operations

De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjabloon die beschikbaar is met de functie voor gegevensintegratie maakt de stroom van gegevens over projecttaken van Project Service Automation naar Finance and Operations mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Sjabloon en taak

Selecteer voor toegang tot de sjabloon in het Microsoft PowerApps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projecttaken vanuit Project Service Automation naar Finance and Operations:

- **Naam van de sjabloon in Gegevensintegratie:** Projecttaken (PSA naar Fin and Ops)
- **Naam van de taak in het project:** Projecttaken

Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.

## <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance en Operations              |
|----------------------------|-------------------------------------|
| Projecttaken              | Integratie-entiteit voor projecttaak |

## <a name="entity-flow"></a>Entiteitstroom

Projecttaken worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectactiviteiten.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query voor Excel gebruiken om gegevens te filteren als aan deze voorwaarde wordt voldaan:

- U hebt resourcespecifieke records in een projecttaak.

Als u Power Query moet gebruiken, volgt u deze richtlijn:

- De sjabloon Projecttaken (PSA naar Fin and Ops) heeft een standaardfilter waarbij resourcespecifieke records binnen een projecttaak worden uitgesloten door het filter op **IsLineTask** op **False** te zetten. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)

