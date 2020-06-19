---
title: Geschiktheidsopties voor persoonlijke contactpersonen configureren
description: Configureer geschiktheidsopties voor persoonlijke contactpersonen in Microsoft Dynamics 365 Human Resources. Persoonlijke contactpersonen kunnen begunstigden of gezinsleden zijn.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68364b0cc1c579a3ee9813474c9d3f6e4df1c05d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430757"
---
# <a name="configure-personal-contact-eligibility-options"></a>Geschiktheidsopties voor persoonlijke contactpersonen configureren

In dit artikel wordt beschreven hoe u typen persoonlijke contactpersonen voor vergoedingen kunt configureren in Microsoft Dynamics 365 Human Resources. Persoonlijke contactpersonen kunnen begunstigden of gezinsleden zijn. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsopties van persoonlijke contactpersonen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Geschiktheidsoptie** | Een unieke naam of code van een geschiktheidsoptie om de geschiktheidsoptie te identificeren. |
   | **Beschrijving** | Een korte omschrijving van de geschiktheidsoptie. |
   | **Geschiktheidscode contactpersoon** | De systeemcode die het beste de persoonlijke geschiktheidsoptie beschrijft. U kunt kiezen uit: <ul><li>Relatie</li><li>Student</li><li>Gezinsdekking</li><li>Afhankelijke persoon is te oud en uitgeschakeld</li></ul> |
   | **Status** | De status van de geschiktheidsoptie. Als de status voor een geschiktheidsoptie is ingesteld op inactief, kunt u die geschiktheidsoptie voor persoonlijke contactpersonen niet selecteren voor persoonlijke contactpersonen. |
   | **Relatie** | Geeft de relatie aan tussen de persoonlijke contactpersoon en de werknemer. Dit veld is alleen actief als de geschiktheidscode van de contactpersoon is ingesteld op Relatie. |
   | **Leeftijd** | De maximale leeftijd van een geschikte persoonlijke contactpersoon voor het vergoedingsplan. Dit veld is alleen actief als u een relatie selecteert. Deze leeftijd wordt vergeleken met de berekende leeftijd van de persoonlijke contactpersoon. Berekende leeftijd is: (dekkingsdatum – geboortedatum van persoonlijke contactpersoon/365). Dit aantal is altijd een geheel getal. |

4. Selecteer **Opslaan**. 
