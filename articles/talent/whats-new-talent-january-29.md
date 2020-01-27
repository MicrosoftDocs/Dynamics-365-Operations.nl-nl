---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (31 januari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899100"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (31 januari 2019)

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Talent.

**Build 8.1.2128**

## <a name="core-hr-changes"></a>Core HR-wijzigingen

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Bij verlof dat wordt opgenomen op de verlofkaart wordt geen rekening gehouden met verlofplandatums
Voor personen die verlofplannen hebben die niet in een kalenderjaar vallen, wordt op de kaart **Gebruikt** nu verlof weergegeven dat is opgenomen in het in het plan gedefinieerde verlofjaar. Als het verlofjaar van een organisatie bijvoorbeeld van1 juni tot en met 30 mei loopt en een werknemer 3 dagen verlof heeft opgenomen in december, wordt op de kaart **Gebruikt** op 15 januari 3 dagen weergegeven. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Toerekeningsbedragen die niet overeenkomen met de laagdatumbasis
Nieuwe opties zijn toegevoegd aan verlof en afwezigheid (**Human resources**-parameters) waarmee klanten kunnen bepalen wanneer de dienstmaanden van werknemers geldig zijn. Voor sommige organisaties is de datum het einde van de maand, maar voor andere organisaties kan de datum het begin van de volgende maand zijn. Een bepaalde organisatie kan bijvoorbeeld verlof geven op 31 december, terwijl een andere organsatie verlof op 1 januari geeft. Met deze optie kunt u bepalen wanneer de toekenning moet plaatsvinden. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Aanstellingsacties van werknemers kunnen vastzitten in de status Workflows voltooid.
Er zijn wijzigingen aangebracht om een probleem op te lossen waarbij een klein aantal workflows vastzat in de status Workflows voltooid. Nieuwe workflows krijgen nu de status 'Voltooid' als de workflow is voltooid. Alle workflows met de status Workflow voltooid krijgen de status Fout zodat zo nodig wijziging of verwijdering mogelijk is. 
