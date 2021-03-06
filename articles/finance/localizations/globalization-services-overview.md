---
title: Dynamics 365-globalisatieservices
description: Dit onderwerp bevat een overzicht van Microsoft Dynamics 365-globalisatieservices..
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018802"
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