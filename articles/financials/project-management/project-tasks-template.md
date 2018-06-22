---
title: Projecttaken vanuit Project Service Automation synchroniseren
description: In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Projecttaken vanuit Project Service Automation rechtstreeks synchroniseren met projectactiviteiten in Finance and Operations

In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in Dynamics 365 for Finance and Operations, versie 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gegevensstroom voor Project Service Automation naar Finance and Operations

De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjabloon die beschikbaar is met de functie voor gegevensintegratie maakt de stroom van gegevens over projecttaken van Project Service Automation naar Finance and Operations mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Sjabloon en taak

Selecteer voor toegang tot de sjabloon in het Microsoft PowerApps Beheercentrum **Projecten** en selecteer vervolgens in de rechterbovenhoek **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taak wordt gebruikt voor het synchroniseren van projecttaken vanuit Project Service Automation naar Finance and Operations:

-**Naam van de sjabloon in gegevensintegratie:** Projecttaken (PSA naar Fin and Ops) -**Naam van de taak in het project:** Projecttaken

Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.

## <a name="entity-set"></a>Entiteitset

|Project Service Automation               | Finance en Operations                |
|-----------------------------------------|---------------------------------------|
| Projecttaken                           | Integratie-entiteit voor projecttaak.   |

## <a name="entity-flow"></a>Entiteitstroom

Projecttaken worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectactiviteiten.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query gebruiken om gegevens te filteren als aan deze voorwaarden wordt voldaan:

- U hebt resourcespecifieke records binnen een projecttaak.

Als u Power Query moet gebruiken, volgt u deze richtlijnen:

- De sjabloon Projecttaken (PSA naar Fin and Ops) heeft een standaardfilter voor het uitsluiten van resourcespecifieke records binnen een projecttaak door het filter op de **IsLineTask** op **False** te zetten. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


