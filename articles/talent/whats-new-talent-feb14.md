---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (14 februari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9f3fa269217bc03a15fde6ee0fc9d0c502c17b3e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009117"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (14 februari 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract
Er zijn andere kleine correcties opgenomen in deze release.

## <a name="changes-in-onboarding"></a>Wijzigingen in Onboarding
Er zijn andere kleine correcties opgenomen in deze release.
 
## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR 
**Build 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Met de entiteit Vaste compensatie voor werknemer worden niet alle records geëxporteerd
Met deze wijziging worden nu alle records geëxporteerd met de entiteit **Vaste compensatie voor werknemer**. De entiteit kan worden gebruikt om bestaande records voor vaste compensatie voor werknemers te maken en bij te werken. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Bij Einddatum dienstverband wordt geen rekening gehouden met de voorkeursinstellingen voor tijdzones van werknemers
Bij Einddatum dienstverband wordt nu wel rekening gehouden met voorkeurstijdzone van gebruikers bij het maken of beëindigen van een dienstverband bij een bedrijf.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Adressen in het Verenigd Koninkrijk worden in Analyses weergegeven als adressen in Oost-Zwitserland
In deze release is een wijziging aangebracht om onjuiste uitlijning te corrigeren in adressen in het rapport 'Personeelsbezetting per locatie' in **Personeelsbeheer**.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Ontslagcode wordt niet ingevuld in de record voor werknemerspositietoewijzing wanneer de positie wordt beëindigd
Er is een wijziging aangebracht zodat de code voor 'Ontslagreden' standaard wordt ingesteld wanneer de werknemerspositietoewijzing wordt beëindigd.

### <a name="new-entity-created-for-job-compensation-levels"></a>Er is een nieuwe entiteit gemaakt voor taakcompensatieniveaus
Er is een nieuwe DMF-entiteit (Data Management Framework) gemaakt. Met de entiteit kunnen compensatieniveaus, marktwaarden en onderzoeksinformatie worden gemaakt en bijgewerkt voor elke taak die in het systeem is gedefinieerd.
