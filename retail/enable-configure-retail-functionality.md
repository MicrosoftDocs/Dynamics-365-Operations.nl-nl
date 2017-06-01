---
title: Seedgegevens in een nieuwe Retail-omgeving initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 534c9ab0f4d95f42d09f35d3197a2258c8d39526
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Seedgegevens in een nieuwe Retail-omgeving initialiseren

[!include[banner](includes/banner.md)]


In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Operations - Retail.

Nadat de detailhandelsoplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de detailhandelsconfiguratie initialiseren om de basisconfiguratiegegevens te maken. **Belangrijk:** Voordat u de detailhandelsconfiguratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen. Deze stap moet worden voltooid voor elke rechtspersoon die u voor kleinhandel gebruikt. Om de kleinhandelsconfiguratie te initialiseren, volgt u deze stappen.

1.  Start de Dynamics 365 for Operations-client.
2.  Klik op **Detailhandel en commerce** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Detailhandelparameters**.
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

Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Dynamics 365 for Operations-database. **Opmerking:** Er is een optie om de detailhandelplanner afzonderlijk te configureren. Met deze optie kunt u de configuratie van de Detailhandel planner opnieuw instellen op de standaardwaarden. Nadat de initialisatie is voltooid, moet u aanvullende detailhandelsgegevens configureren. Hieronder vindt u enkele voorbeelden:

-   Detailhandelparameters
-   Parameters voor Detailhandel planner
-   Detailhandelafzetkanalen
-   Kassa's en apparaten
-   Assortimenten





