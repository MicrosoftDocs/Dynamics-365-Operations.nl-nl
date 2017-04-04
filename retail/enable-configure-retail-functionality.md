---
title: Gegevens in een omgeving met nieuwe detailhandel initialiseren
description: Dit artikel worden de gegevens die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Gegevens in een omgeving met nieuwe detailhandel initialiseren

Dit artikel worden de gegevens die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Operations - Retail.

Nadat de detailhandelsoplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de detailhandelsconfiguratie initialiseren om de basisconfiguratiegegevens te maken. **Belangrijk:** Voordat u de detailhandelsconfiguratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen. Deze stap moet worden voltooid voor elke rechtspersoon die u voor kleinhandel gebruikt. Om de kleinhandelsconfiguratie te initialiseren, volgt u deze stappen.

1.  Start de Dynamics 365 voor client bewerkingen.
2.  Klik op **detailhandel en commerce**&gt;**instellingen Headquarters**&gt;**Parameters**&gt;**parameters detailhandel**.
3.  Klik op **Initialiseren**.

Initialisatie maakt de volgende standaardconfiguratiegegevens:

-   Detailhandelplanner taken en subtaken
-   Detailhandelafzetkanaalschema
-   Distributieplanningen voor detailhandel
-   Standaardschermindelingen, die knoppenrasters, afbeeldingen en thema's omvatten
-   Tijdzonegegevens
-   Werking verkooppunten (POS)
-   POS-machtigingen
-   Afzetkanaalrapporten
-   Kenmerkmetagegevens
-   Sjablonen voor entiteitvalidatie
-   Batchtaak om de sessiehistorie van Commerce Data Exchange op te schonen

Bovendien kunnen registreren die betrekking hebben op de bedrijfstak van de betaling kaart (PCI) is ingeschakeld voor de Dynamics 365 voor bewerkingen-database. **Opmerking:** Er is een optie om de detailhandelplanner afzonderlijk te configureren. Met deze optie kunt u de configuratie van de Detailhandel planner opnieuw instellen op de standaardwaarden. Nadat de initialisatie is voltooid, moet u aanvullende detailhandelsgegevens configureren. Hieronder vindt u enkele voorbeelden:

-   Detailhandelparameters
-   Parameters voor Detailhandel planner
-   Detailhandelafzetkanalen
-   Kassa's en apparaten
-   Assortimenten



