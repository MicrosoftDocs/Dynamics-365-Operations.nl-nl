---
title: Wijzigingen in tarieven verwerken
description: In dit onderwerp wordt uitgelegd hoe u wijzigingen in het vergoedingstarief in Microsoft Dynamics 365 Human Resources verwerkt.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa94584749e72cab7aa3466814ed8ea9d59665da
ms.sourcegitcommit: 4f9c889e5cf72f34dd9746a322f8c0d6b983037b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/25/2021
ms.locfileid: "7417443"
---
# <a name="process-rate-changes"></a>Wijzigingen in tarieven verwerken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt beschreven hoe u wijzigingen in het vergoedingstarief in Microsoft Dynamics 365 Human Resources verwerkt wanneer er een wijziging is aangebracht in de instellingen van geschiktheidsregels in een nieuw of bestaand vergoedingsplan. Als er een nieuwe geschiktheidsregel wordt gemaakt en aan het plan wordt toegewezen, wordt u door het systeem gevraagd om de geschiktheidscontrole van medewerkers opnieuw uit te voeren om te controleren of medewerkers nu mogelijk in aanmerking komen voor het plan op basis van nieuwe geschiktheidsopties. 

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
