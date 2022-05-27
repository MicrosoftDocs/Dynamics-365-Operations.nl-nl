---
title: Wijzigingen in levensgebeurtenissen verwerken
description: In dit onderwerp wordt uitgelegd hoe u wijzigingen in de levensgebeurtenissen in Microsoft Dynamics 365 Human Resources verwerkt.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f43ee914bb57b14969b6d729218accbd1009d67a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691773"
---
# <a name="process-life-event-changes"></a>Wijzigingen in levensgebeurtenissen verwerken


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt wijzigingen in levensgebeurtenissen verwerken in Microsoft Dynamics 365 Human Resources voor twee levensgebeurtenissen:

- Verjaardagswijzigingen
- Wijzigingen in de vervaldatum voor het negeren van een geschiktheidsregel 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Wijziging in levensgebeurtenis verwerken**.

2. Geef in het dialoogvenster **Wijzigingsproces voor levensgebeurtenissen uitvoeren** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Inschrijvingsperiode | De inschrijvingsperiode waarvoor de wijzigingen in de levensgebeurtenis moeten worden verwerkt. |
   | Rechtspersoon | De rechtspersoon waarvoor de wijzigingen in de levensgebeurtenis moeten worden verwerkt. |

3. Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Voer gegevens in voor het proces.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het proces wordt uitgevoerd met de parameters die u instelt.

4. Selecteer **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
