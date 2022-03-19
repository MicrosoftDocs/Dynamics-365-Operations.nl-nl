---
title: Organisatiehiërarchie in Dataverse
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen apps voor financiële en bedrijfsactiviteiten en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9174612743c68595d12dd223f0932ace1857c0fb
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358359"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisatiehiërarchie in Dataverse

[!include [banner](../../includes/banner.md)]



Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie. Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.

Hoewel Dataverse het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst. Als onderdeel van de Dataverse-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Dataverse.

## <a name="data-flow"></a>Gegevensstroom

Een bedrijfsecosysteem dat bestaat uit apps voor financiële en bedrijfsactiviteiten en Dataverse blijft een organisatiehiërarchie houden. Deze organisatiehiërarchie is gebaseerd op apps voor financiële en bedrijfsactiviteiten, maar is in Dataverse beschikbaar voor informatieve en uitbreidbare doeleinden. In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Dataverse worden weergegeven als een eenrichtingsgegevensstroom van apps voor financiële en bedrijfsactiviteiten naar Dataverse.

![Afbeelding van architectuur.](media/dual-write-data-flow.png)

Tabeltoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit apps voor financiële en bedrijfsactiviteiten naar Dataverse.

## <a name="templates"></a>Sjablonen

Een organisatie is een groep mensen die samenwerkt om een bedrijfsproces uit te voeren of een doel te bereiken. Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat. U kunt de volgende typen interne organisaties definiëren: rechtspersonen, operationele eenheden en teams. Zoals de volgende tabel laat zien, wordt een verzameling tabeltoewijzingen gemaakt om rechtspersonen, operationele eenheden en gerelateerde organigramgegevens te synchroniseren.

Apps voor financiële en bedrijfsactiviteiten | Customer Engagement-apps     | Description
-----------------------|--------------------------------|---
[Rechtspersonen](mapping-reference.md#102) | cdm_companies | 
[Rechtspersonen](mapping-reference.md#142) | msdyn_internalorganizations |
[Operationele eenheid](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisatiehiërarchie - gepubliceerd](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Deze sjabloon biedt synchronisatie in één richting van de tabel Gepubliceerde organisatiehiërarchie.
[Organisatiehiërarchiedoelstellingen](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Deze sjabloon biedt synchronisatie in één richting van de tabel Doel van organisatiehiërarchie.
[Type organisatiehiërarchie](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Deze sjabloon biedt synchronisatie in één richting van de tabel Type organisatiehiërarchie.

## <a name="internal-organization"></a>Interne organisatie

Gegevens over de interne organisatie in Dataverse zijn afkomstig van twee tabellen, **Operationele eenheid** en **Rechtspersonen**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
