---
title: Dynamics 365-globalisatieservices
description: Dit artikel bevat een overzicht van Microsoft Dynamics 365-globalisatieservices..
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278227"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365-globalisatieservices

[!include [banner](../includes/banner.md)]

De volgende globalisatieservices kunnen worden geconfigureerd om de capaciteiten van sommige Microsoft Dynamics 365 online services uit te breiden:

- **Regulatory Configuration Service (RCS)** ondersteunt de configuratie van verschillende typen elektronische documenten en rapporten. RCS biedt een verbeterde versie van de ER-ontwerper (Electronic Reporting), waarin de configuratie-opslagplaats een zelfstandige service is. Zie [Regulatory Configuration Service](rcs-overview.md) voor meer informatie.
- **Elektronische facturering** brengt configureerbare indelingen voor transformaties, digitale handtekeningen en configureerbare integraties samen voor connectiviteit met externe webservices, waaronder certificerings- en antwoordverwerking. Zie [Elektronische facturering](e-invoicing-service-overview.md) voor meer informatie.
- Met **Belastingberekening** kunt u meer flexibiliteit bieden met ondersteuning voor meerdere belasting-id's, bepalen van belastingcodes, ontwerper van de belastingberekening en een runtime-engine om te voldoen aan complexe belastingregels over de hele wereld. Zie voor meer informatie [Belastingberekening](global-tax-calcuation-service-overview.md).

Deze globalisatieservices bieden out-of-box-integratie met de volgende online services van Dynamics 365.

| Online service | RCS | Elektronische facturering | Belastingberekening (Preview) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Ja | Ja | Ja | 
| Dynamics 365 Supply Chain Management | Ja | Ja | Ja | 
| Dynamics 365 Project Operations | Ja | Ja | Niet van toepassing | 
| Dynamics 365 Commerce | Ja | Niet van toepassing | Niet van toepassing | 

> [!NOTE]
> Vanwege verschillen in de beschikbaarheid van geografische locaties van Azure (geo) voor RCS, kunnen klantgegevens door de configuratie van deze service worden overgebracht buiten de geografische locatie die is geselecteerd voor de toepasselijke Dynamics 365 online service. Zie [Dynamics 365 en Power Platform: beschikbaarheid, gegevenslocatie, taal en lokalisatie](https://aka.ms/rcs/D365Productavailabilityguide) voor meer informatie.
