---
title: Opties voor geschiktheid van persoonlijke contactpersonen configureren
description: In dit artikel wordt uitgelegd hoe u geschiktheidsopties voor persoonlijke contactpersonen in Microsoft Dynamics 365 Human Resources configureert.
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: 82bb7c037b4e0ab9950ce4c314c03a0f2d713bbd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895926"
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
   | **Leeftijd** | De maximale leeftijd van een geschikte persoonlijke contactpersoon voor het vergoedingsplan. Dit veld is alleen actief als u een relatie selecteert. Deze leeftijd wordt vergeleken met de berekende leeftijd van de persoonlijke contactpersoon. Berekende leeftijd is: (dekkingsdatum – geboortedatum van persoonlijke contactpersoon/365). Dit aantal is altijd een geheel getal. |

4. Selecteer **Opslaan**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
