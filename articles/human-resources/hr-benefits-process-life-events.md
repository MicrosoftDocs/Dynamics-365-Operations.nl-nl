---
title: Levensgebeurtenissen verwerken
description: Tijdens de levenscyclus van werknemers in Microsoft Dynamics 365 Human Resources, kan iedere werknemer verschillende levensgebeurteniswijzigingen ondergaan.
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
ms.openlocfilehash: ef160af483f81b8c1e60a274029b77c3cd34f924
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324783"
---
# <a name="process-life-events"></a>Levensgebeurtenissen verwerken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tijdens de levenscyclus van werknemers in Microsoft Dynamics 365 Human Resources, kan iedere werknemer verschillende levensgebeurteniswijzigingen ondergaan. Bijvoorbeeld een huwelijk, verandering van werk of wijziging van gezinsleden of begunstigden. Als u levensgebeurtenissen wilt gebruiken, moet u levensgebeurtenissen inschakelen op de pagina **Parameters voor vergoedingen** en opties voor levensgebeurtenissen instellen voor plantypen.

Voordat u de levensgebeurtenissen kunt verwerken, moet u al minimaal eenmaal een open inschrijving hebben uitgevoerd tijdens een aanstellingstijdvak. In de Verenigde Staten vindt een open inschrijving meestal eenmaal per jaar plaats. Buiten de Verenigde Staten kan de open inschrijving worden uitgevoerd op het moment van de aanstelling. Een medewerker hoeft geen vergoedingsplan te selecteren om te zorgen dat levensgebeurtenissen worden verwerkt, maar de medewerker moeten wel zijn opgenomen in de verwerking van een openstaande inschrijving. 

Gebruik de levensgebeurtenisverwerking wanneer u medewerkers hebt met levensgebeurtenissen die op een toekomstige datum plaatsvinden. Met deze gebeurtenis worden alle levensgebeurtenissen verwerkt die nog niet zijn verwerkt (zoals toekomstige levensgebeurtenissen of levensgebeurtenissen die zijn toegevoegd en die niet specifiek zijn voor een bepaalde medewerker – een voorbeeld is een nieuwe vergoeding). Realtime levensgebeurtenissen zijn verborgen.

Als het bijvoorbeeld vandaag 1 februari is, op 14 februari medewerker Joe Smith volgens de planning rechtspersonen wijzigt u en de levensgebeurtenisverwerking voor 15 februari uitvoert, worden alle gebeurtenissen tot en met 15 februari verwerkt. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Levensgebeurtenissen verwerken**.

2. Geef in het dialoogvenster **Levensgebeurtenisproces uitvoeren** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Inschrijvingsperiode** | De inschrijvingsperiode waarvoor de levensgebeurtenissen moeten worden verwerkt. |
   | **Rechtspersoon** | De rechtspersoon waarvoor levensgebeurtenissen moeten worden verwerkt. |
   | **Datum van levensgebeurtenis** | Het systeem verwerkt alle gebeurtenissen tijdens de inschrijvingsperiode die plaatsvinden tot en met deze datum. |
   | **Medewerker** | De medewerker waarvoor levensgebeurtenissen moeten worden verwerkt. Als u dit veld leeg laat, worden de levensgebeurtenissen voor alle medewerkers verwerkt. |

3. Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Voer gegevens in voor het proces.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het proces wordt uitgevoerd met de parameters die u instelt.

4. Selecteer **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
