---
title: Organisatiehiërarchie in Common Data Service
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen Finance and Operations en Common Data Service beschreven.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789173"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organisatiehiërarchie in Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Omdat Microsoft Dynamics 365 for Finance and Operations een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie. Bedrijfsfinanciën en -bewerkingen kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.

Hoewel Common Data Service het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst. Als onderdeel van de Common Data Service-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Common Data Service.

## <a name="data-flow"></a>Gegevensstroom

Een bedrijfsecosysteem dat bestaat uit Finance and Operations en Common Data Service blijft een organisatiehiërarchie houden. Deze organisatiehiërarchie is gebaseerd op Finance and Operations, maar is in Common Data Service beschikbaar voor informatieve en uitbreidbare doeleinden. In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Common Data Service worden weergegeven als een eenrichtingsgegevensstroom van Finance and Operations naar Common Data Service.

![Afbeelding van architectuur](media/dual-write-data-flow.png)

## <a name="templates"></a>Sjablonen

Entiteitstoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations naar Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Doel van interne organisatiehiërarchie

Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Doel van organisatiehiërarchie van Finance and Operations naar Dynamics 365 for Customer Engagement.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Type interne organisatiehiërarchie

Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Type organisatiehiërarchie van Finance and Operations naar Customer Engagement.

<!-- ![architecture image](media/dual-write-type.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
NAAM | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Interne organisatiehiërarchie

Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Gepubliceerde organisatiehiërarchie van Finance and Operations naar Customer Engagement.

<!-- ![architecture image](media/dual-write-organization.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Interne organisatie

Gegevens over de interne organisatie in Common Data Service zijn afkomstig van twee Finance and Operations-entiteiten, **operationele eenheid** en **rechtspersonen**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Operationele eenheid

Bronveld | Toewijzingstype | Doelveld
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NAAM | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Rechtspersoon

Bronveld | Toewijzingstype | Doelveld
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NAAM | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
geen | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Bedrijf

Biedt bidirectionele synchronisatie van rechtspersoonsgegevens (bedrijfsgegevens) tussen Finance and Operations en Customer Engagement.

<!-- ![architecture image](media/dual-write-company.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
NAAM | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
