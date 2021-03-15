---
title: Tariefwijzigingen verwerken
description: Verwerk wijzigingen in het vergoedingstarief in Microsoft Dynamics 365 Human Resources wanneer er een wijziging is aangebracht in de instellingen van geschiktheidsregels in een nieuw of bestaand vergoedingsplan.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f326957d5f33607e434f99563cfeb528c05f258d
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112076"
---
# <a name="process-rate-changes"></a>Tariefwijzigingen verwerken

Verwerk wijzigingen in het vergoedingstarief in Microsoft Dynamics 365 Human Resources wanneer er een wijziging is aangebracht in de instellingen van geschiktheidsregels in een nieuw of bestaand vergoedingsplan. Als er een nieuwe geschiktheidsregel wordt gemaakt en aan het plan wordt toegewezen, wordt u door het systeem gevraagd om de geschiktheidscontrole van medewerkers opnieuw uit te voeren om te controleren of medewerkers nu mogelijk in aanmerking komen voor het plan op basis van nieuwe geschiktheidsopties. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Updateverwerking voor tariefwijziging**.

2. Geef in het dialoogvenster **Updateproces voor vergoedingstarief uitvoeren** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Inschrijvingsperiode** | De inschrijvingsperiode waarvoor de tariefwijzigingen moeten worden verwerkt. |

3. Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Voer gegevens in voor het proces.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het proces wordt uitgevoerd met de parameters die u instelt.

4. Selecteer **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]