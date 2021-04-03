---
title: Wijzigingen van levensgebeurtenissen verwerken
description: U kunt wijzigingen in levensgebeurtenissen verwerken in Microsoft Dynamics 365 Human Resources bij wijzigingen in levensgebeurtenissen.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2726dcb3c847c9af2a431358de04a27341b9e66c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464245"
---
# <a name="process-life-event-changes"></a>Wijzigingen van levensgebeurtenissen verwerken

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