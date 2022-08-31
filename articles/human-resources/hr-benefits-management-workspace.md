---
title: Werkgebied voor vergoedingenbeheer
description: In dit artikel wordt de werkruimte Vergoedingenbeheer in Dynamics 365 Human Resources beschreven.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 35c38ad25380b940d050b4e498fabca017c35997
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336879"
---
# <a name="benefits-management-workspace"></a>Werkgebied voor vergoedingenbeheer

[!include [preview feature](./includes/preview-feature.md)]

In dit artikel wordt de werkruimte **Vergoedingenbeheer** in Dynamics 365 Human Resources beschreven.

> [!NOTE]
> Om de werkruimte **Vergoedingenbeheer** weer te geven, moet u eerst de functie **(Voorbeeld) Werkruimte Vergoedingenbeheer** in Functiebeheer inschakelen. Meer informatie over het inschakelen van de previewfuncties vindt u in [Functies beheren](hr-admin-manage-features.md).<br><br>![Werkruimte Vergoedingenbeheer inschakelen.](./media/hr-benefits-management-workspace-enable.png)

De werkruimte **Vergoedingenbeheer** geeft u een snel overzicht van vergoedingenitems die uw aandacht vereisen. Op deze pagina ziet u het volgende:

- Totalen voor artikelen die op actie wachten
- Werknemers met niet-bevestigde selecties
- Werknemers die zich onlangs hebben ingeschreven bij vergoedingen
- Werknemers met toekomstige levensgebeurtenissen
- Nieuwe werknemers die niet zijn ingeschreven
- Werknemers met actieve levensgebeurtenissen
- Werknemers met openstaande inschrijvingen die geen plannen hebben gekozen

![Werkgebied voor vergoedingenbeheer.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Actie-items weergeven

U kunt uw actie-items weergeven door een tegel of een tabblad te selecteren. Als u een tabblad selecteert, kunt u werknemers rechtstreeks van de werkruimtepagina weergeven en selecteren.

![Actie-items.](./media/hr-benefits-management-workspace-action-items.png)

Als u een tegel selecteert, gaat u naar de pagina voor dat gebied. Als u een van deze tegels selecteert, wordt bijvoorbeeld de pagina **Vergoedingsplannen voor werknemers** weergegeven. Deze pagina wordt gefilterd op werknemers voor wie u actie moet ondernemen:

- **Niet-bevestigde selecties**
- **Openstaande inschrijvingen zonder uitgecheckte plannen**
- **Ingeschreven voor vergoedingen**
- **Nieuw aangestelde werknemer niet ingeschreven**

![Vergoedingsplannen voor medewerker.](./media/hr-benefits-management-workspace-plans.png)

Als u de tegels **Actieve levensgebeurtenissen** of **Toekomstige levensgebeurtenissen** selecteert, wordt er een lijst met actieve of toekomstige levensgebeurtenissen weergegeven.

![Levensgebeurtenissen.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Wordt verwerkt

Selecteer het juiste item op de navigatiebalk om kwalificatie voor inschrijving, levensgebeurtenissen of tariefwijzigingen te verwerken.

![In verwerking.](./media/hr-benefits-management-workspace-processing.png)

Om de verwerkingsresultaten te bekijken, selecteert u **Procesresultaten** op de pagina.

![Procesresultaten.](./media/hr-benefits-management-workspace-process-results.png)

Voor meer informatie over de verwerking van vergoedingen, zie:

- [Geschiktheid voor inschrijving verwerken](hr-benefits-process-enrollment-eligibility.md)
- [Wijzigingen in levensgebeurtenissen verwerken](hr-benefits-process-life-event-changes.md)
- [Geschiktheid voor levensgebeurtenissen verwerken](hr-benefits-process-life-event-eligibility.md)
- [Levensgebeurtenissen verwerken](hr-benefits-process-life-events.md)
- [Wijzigingen in tarieven verwerken](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Periode wijzigen

Als u een andere vergoedingsperiode wilt bekijken, selecteert u deze in de vervolgkeuzelijst **Periode**.

![Periode wijzigen.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Tabblad Inschrijving openen

U kunt actie-items weergeven door een tegel of een tabblad te selecteren. Als u een tabblad selecteert, kunt u werknemers op de werkruimtepagina weergeven en selecteren.
Het tabblad **Inschrijving openen** biedt belangrijke metrische gegevens voor het openstaande inschrijvingsproces. 

Informatie over openstaande inschrijving wordt 30 dagen voor de **Begindatum inschrijving** weergegeven. Deze datum wordt gedefinieerd in de instelling **Perioden** in **Vergoedingenbeheer** > **Koppelingen** > **Perioden** in het veld **Begindatum inschrijving**.  Als u deze instelling wilt wijzigen, gaat u naar **Gedeelde Human Resources-parameters** > **Vergoedingenbeheer** > **Inschrijvingsopties openen** en werkt u het veld **Aantal** bij.  

Op het tabblad **Inschrijving openen** is de volgende informatie beschikbaar:
 - Werknemers die het proces voor het openen van inschrijving nog niet hebben gestart
 - Werknemers van wie keuzen worden verwerkt
 - Werknemers die het keuzeproces hebben voltooid
 - Niet-bevestigde selecties

**Overzichtstegels**

- **Niet gestart** – Op de tegel **Niet gestart** wordt een aantal werknemers weergegeven die het inschrijvingsproces nog niet hebben gestart. De tegel **Niet gestart** is een gefilterde lijst waarin alleen die werknemers worden weergegeven die geen plannen hebben geselecteerd, zijn kwijtgescholden of zijn uitgecheckt voor de periode voor het openen van het inschrijvingsplan. Verplichte plannen worden genegeerd en niet opgenomen, omdat deze standaard worden geselecteerd voor de werknemer.  U kunt uitzoomen op deze tegel om een lijst weer te geven met werknemers die het proces voor het openen van inschrijving nog niet hebben gestart op de pagina **Vergoedingenplan medewerker**.

  > [!NOTE]
  > Als u het proces van het openen van inschrijving voor een **Plantype** niet wilt bijhouden, kunt u dit uitsluiten door naar **Vergoedingenbeheer** > **Koppelingen** > **Parameters voor werknemerselfservice** > **Tegelinstelling vergoedingsplannen** en het veld **Openstaande inschrijvingsvoortgang bijhouden** bij te werken.  U hebt bijvoorbeeld plannen gemaakt waarbij **Plantype** = **Overig** is. Deze plannen kunnen optionele plannen zijn waarvan u de voortgang van de inschrijvingsproces niet wilt bijhouden. Als u dit plantype niet selecteert, worden plannen van dit type genegeerd wanneer u de voortgang of voltooiing van de inschrijving op het tabblad **Inschrijving openen** volgt. Deze instelling is van toepassing op het plantype dat voor alle perioden en rechtspersonen is geselecteerd.

- **In uitvoering** – Op de tegel **In uitvoering** wordt het aantal werknemers weergegeven van wie keuzen worden verwerkt De tegel **uitvoering** is een gefilterde lijst waarin alleen werknemers worden weergegeven die ten minste één plan hebben dat is kwijtgescholden of geselecteerd. Verplichte plannen worden genegeerd en niet opgenomen, omdat deze standaard worden geselecteerd voor de werknemer. U kunt inzoomen op deze tegel om de geselecteerde en kwijtgescholden plannen weer te geven op de pagina **Bulkupdate van vergoedingsplannen voor medewerkers**.

- **Ingeschreven voor vergoedingen** – Op de tegel **Ingeschreven voor vergoedingen** wordt het aantal werknemers weergegeven dat volledig is ingeschreven voor vergoedingen. De tegel **Ingeschreven voor vergoedingen** is een gefilterde lijst met werknemers van wie alle plannen zijn geselecteerd of kwijtgescholden. Met de query worden plannen uitgesloten die niet worden bijgehouden voor openstaande inschrijving op de pagina **Parameters voor werknemerselfservice**. U kunt uitzoomen op deze tegel om een lijst met werknemers weer te geven op de pagina **Vergoedingsplannen voor medewerker**.

- **Niet-bevestigde selecties** – Op de tegel **Niet-bevestigde selecties** wordt het aantal werknemers weergegeven met plannen die zijn geselecteerd of kwijtgescholden en moeten worden bevestigd. U kunt inzoomen op deze tegel om de pagina **Bulkupdate van vergoedingsplannen voor medewerkers** weer te geven.

**Activiteit**

- **Niet gestart** – Op het tabblad **Niet gestart** wordt een lijst met werknemers weergegeven die het inschrijvingsproces nog niet hebben gestart. De tegel **Niet gestart** is een gefilterde lijst waarin werknemers worden weergegeven die geen plannen hebben geselecteerd, zijn kwijtgescholden of zijn uitgecheckt voor de periode voor het openen van het inschrijvingsplan. Verplichte plannen worden genegeerd en niet opgenomen, omdat deze standaard worden geselecteerd voor de werknemer. U kunt inzoomen op de werknemer om de detailpagina **Vergoedingsplannen voor medewerker** weer te geven.

- **Keuzen in uitvoering** – Op het tabblad **Keuzen in uitvoering** wordt een lijst met werknemers weergegeven van wie keuzen worden verwerkt Het tabblad **Keuzen in uitvoering** is een gefilterde lijst waarin werknemers worden weergegeven die ten minste één plan hebben dat is kwijtgescholden of geselecteerd. Verplichte plannen worden genegeerd en niet opgenomen, omdat deze standaard worden geselecteerd voor de werknemer. U kunt inzoomen op de werknemer om de detailpagina **Vergoedingsplannen voor medewerker** weer te geven.

## <a name="view-more-options"></a>Meer opties weergeven

Als u meer informatie en/of aanvullende acties wilt weergeven, selecteert u **Koppelingen**.

![Koppelingen.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Zie ook

[Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md)
