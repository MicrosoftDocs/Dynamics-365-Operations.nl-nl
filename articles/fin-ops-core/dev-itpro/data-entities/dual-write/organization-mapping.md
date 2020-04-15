---
title: Organisatiehiërarchie in Common Data Service
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen Finance and Operations-apps en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173149"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organisatiehiërarchie in Common Data Service

[!include [banner](../../includes/banner.md)]



Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie. Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.

Hoewel Common Data Service het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst. Als onderdeel van de Common Data Service-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Common Data Service.

## <a name="data-flow"></a>Gegevensstroom

Een bedrijfsecosysteem dat bestaat uit Finance and Operations-apps en Common Data Service blijft een organisatiehiërarchie houden. Deze organisatiehiërarchie is gebaseerd op Finance and Operations-apps, maar is in Common Data Service beschikbaar voor informatieve en uitbreidbare doeleinden. In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Common Data Service worden weergegeven als een eenrichtingsgegevensstroom Finance and Operations-apps naar Common Data Service.

![Afbeelding van architectuur](media/dual-write-data-flow.png)

## <a name="templates"></a>Sjablonen

Entiteitstoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations-apps naar Common Data Service.

## <a name="templates"></a>Sjablonen

Productinformatie bevat alle informatie die betrekking heeft op het product en de definitie ervan, zoals de productdimensies of de tracerings- en opslagdimensies. Zoals in de volgende tabel wordt aangegeven, wordt een verzameling entiteitstoewijzingen gemaakt om producten en gerelateerde informatie te synchroniseren.

Finance and Operations-apps | Andere Dynamics 365-apps | Omschrijving
-----------------------|--------------------------------|---
Organisatiehiërarchiedoelstellingen | msdyn_internalorganizationhierarchypurposes | Deze sjabloon biedt synchronisatie in één richting van de entiteit Doel van organisatiehiërarchie.
Type organisatiehiërarchie | msdyn_internalorganizationhierarchytypes | Deze sjabloon biedt synchronisatie in één richting van de entiteit Type organisatiehiërarchie.
Organisatiehiërarchie - gepubliceerd | msdyn_internalorganizationhierarchies | Deze sjabloon biedt synchronisatie in één richting van de entiteit Gepubliceerde organisatiehiërarchie.
Operationele eenheid | msdyn_internalorganizations | 
Rechtspersonen | msdyn_internalorganizations | 
Rechtspersonen | cdm_companies | Biedt bidirectionele synchronisatie van gegevens over rechtspersonen (bedrijven).


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Interne organisatie

Gegevens over de interne organisatie in Common Data Service zijn afkomstig van twee entiteiten, **operationele eenheid** en **rechtspersonen**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

