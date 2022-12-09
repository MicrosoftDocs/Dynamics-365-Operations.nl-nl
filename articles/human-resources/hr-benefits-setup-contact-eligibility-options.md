---
title: Opties voor geschiktheid van persoonlijke contactpersonen configureren
description: In dit artikel wordt uitgelegd hoe u geschiktheidsopties voor persoonlijke contactpersonen in Microsoft Dynamics 365 Human Resources configureert.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803879"
---
# <a name="configure-personal-contact-eligibility-options"></a>Opties voor geschiktheid van persoonlijke contactpersonen configureren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt uitgelegd hoe u de typen persoonlijke contactpersonen die kunnen worden gebruikt in vergoedingen, kunt configureren in Microsoft Dynamics 365 Human Resources. Persoonlijke contactpersonen zijn de personen die onder uw plannen vallen (afhankelijken) of die van uw plannen zullen profiteren (begunstigden). Afhankelijken zijn meestal echtgenoten/echtgenotes of kinderen. Begunstigden kunnen echtgenoten/echtgenotes, kinderen, vertrouwensrelaties of ouders zijn.

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
   | **Leeftijd** |Geeft de maximale leeftijd van een geschikte persoonlijke contactpersoon voor het vergoedingsplan op. Dit veld is alleen actief als u een relatie selecteert. Deze leeftijd wordt vergeleken met de berekende leeftijd van de persoonlijke contactpersoon. Berekende leeftijd is: (dekkingsdatum – geboortedatum van persoonlijke contactpersoon/365). Dit aantal is altijd een geheel getal.
Voor **Dekking geschiktheidsopties voor persoonlijke contactpersonen** is de leeftijd in dit veld de minimumleeftijd. Bijvoorbeeld: als de ouderdom wordt ingesteld op 18 voor de optie **Gezinsdekking**, komen de afhankelijken die zijn gemarkeerd voor gezinsdekking en die 18 of ouder zijn, in aanmerking voor deze optie.  |

4. Selecteer **Opslaan**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
