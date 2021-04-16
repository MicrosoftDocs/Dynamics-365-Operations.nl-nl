---
title: Seedgegevens in nieuwe Commerce-omgevingen initialiseren
description: In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792578"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Seedgegevens in nieuwe Commerce-omgevingen initialiseren

[!include [banner](includes/banner.md)]

In dit artikel worden de gegevens beschreven die zijn gemaakt als onderdeel van het initialisatieproces voor Dynamics 365 Commerce.

Nadat de Commerce-oplossing via Microsoft Dynamics Lifecycle Services (LCS) is geïnstalleerd, moet u de Commerce-configuratie initialiseren om de basisconfiguratiegegevens te maken.

> [!IMPORTANT]
> Voordat u de Commerce-configuratie initialiseert, moet u zorgen dat u een taal en een postadres hebt opgegeven voor elke rechtspersoon waar u detailhandelwinkels wilt instellen. Deze stap moet worden voltooid voor elke rechtspersoon die u voor handel gebruikt.

Om de configuratie te initialiseren, volgt u deze stappen.

1. Start de Commerce-client.
2. Klik op **Retail en commerce** &gt; **Instelling van hoofdkantoor** &gt; **Parameters** &gt; **Commerce-parameters**.
3. Klik op **Initialiseren**.

Initialisatie maakt de volgende standaardconfiguratiegegevens:

- Commerce-planner taken en subtaken
- Handelkanaalschema
- Distributieplanningen Commerce
- Standaardschermindelingen, die knoppenrasters, afbeeldingen en thema's omvatten
- Tijdzonegegevens
- Werking verkooppunten (POS)
- POS-machtigingen
- Afzetkanaalrapporten
- Kenmerkmetagegevens
- Sjablonen voor entiteitvalidatie
- Batchtaak om de Commerce Data Exchange-sessiehistorie op te schonen

Bovendien wordt registratie in verband met de betaalkaartindustrie (PCI) ingeschakeld voor de Commerce-database.

> [!NOTE]
> Er is een optie om de Commerce-planner afzonderlijk te configureren. Met deze optie kunt u de configuratie van de Commerce-planner opnieuw instellen op de standaardwaarden.

Nadat de initialisatie is voltooid, moet u aanvullende Commerce-gegevens configureren. Hieronder volgen een aantal voorbeelden:

- Handelparameters
- Parameters voor handelplanner
- Commerce-kanalen
- Kassa's en apparaten
- Assortimenten


[!INCLUDE[footer-include](../includes/footer-banner.md)]