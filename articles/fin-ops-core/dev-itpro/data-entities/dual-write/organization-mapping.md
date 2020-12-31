---
title: Organisatiehiërarchie in Dataverse
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen Finance and Operations-apps en Dataverse beschreven.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680067"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisatiehiërarchie in Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie. Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.

Hoewel Dataverse het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst. Als onderdeel van de Dataverse-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Dataverse.

## <a name="data-flow"></a>Gegevensstroom

Een bedrijfsecosysteem dat bestaat uit Finance and Operations-apps en Dataverse blijft een organisatiehiërarchie houden. Deze organisatiehiërarchie is gebaseerd op Finance and Operations-apps, maar is in Dataverse beschikbaar voor informatieve en uitbreidbare doeleinden. In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Dataverse worden weergegeven als een eenrichtingsgegevensstroom Finance and Operations-apps naar Dataverse.

![Afbeelding van architectuur](media/dual-write-data-flow.png)

Tabeltoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations-apps naar Dataverse.

## <a name="templates"></a>Sjablonen

Productinformatie bevat alle informatie die betrekking heeft op het product en de definitie ervan, zoals de productdimensies of de tracerings- en opslagdimensies. Zoals in de volgende tabel wordt aangegeven, wordt een verzameling tabeltoewijzingen gemaakt om producten en gerelateerde informatie te synchroniseren.

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

Gegevens over de interne organisatie in Dataverse zijn afkomstig van twee tabellen, **operationele eenheid** en **rechtspersonen**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
