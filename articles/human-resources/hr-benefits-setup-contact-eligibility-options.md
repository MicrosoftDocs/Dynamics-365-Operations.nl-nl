---
title: Geschiktheidsopties voor persoonlijke contactpersonen configureren
description: Configureer geschiktheidsopties voor persoonlijke contactpersonen in Microsoft Dynamics 365 Human Resources. Persoonlijke contactpersonen kunnen begunstigden of gezinsleden zijn.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d85677973f67f0c68de6c5ede62c142524939833
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054399"
---
# <a name="configure-personal-contact-eligibility-options"></a>Geschiktheidsopties voor persoonlijke contactpersonen configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]