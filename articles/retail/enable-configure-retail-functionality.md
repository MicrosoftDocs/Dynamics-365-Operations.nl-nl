---
title: Seedgegevens in een nieuwe Retail-omgeving initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ac4f651cd7e5df912ea2535eafd5e54c11377253
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Seedgegevens in een nieuwe Retail-omgeving initialiseren

[!include[banner](includes/banner.md)]


In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Microsoft Dynamics 365 for Retail.

Nadat de detailhandelsoplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de detailhandelsconfiguratie initialiseren om de basisconfiguratiegegevens te maken. **Belangrijk:** Voordat u de detailhandelsconfiguratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen. Deze stap moet worden voltooid voor elke rechtspersoon die u voor kleinhandel gebruikt. Om de kleinhandelsconfiguratie te initialiseren, volgt u deze stappen.

1.  Start de Dynamics 365 for Retail-client.
2.  Klik op **Detailhandel** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Detailhandelparameters**.
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

Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Dynamics 365 for Retail-database. **Opmerking:** Er is een optie om de detailhandelplanner afzonderlijk te configureren. Met deze optie kunt u de configuratie van de Detailhandel planner opnieuw instellen op de standaardwaarden. Nadat de initialisatie is voltooid, moet u aanvullende detailhandelsgegevens configureren. Hieronder vindt u enkele voorbeelden:

-   Detailhandelparameters
-   Parameters voor Detailhandel planner
-   Detailhandelafzetkanalen
-   Kassa's en apparaten
-   Assortimenten





