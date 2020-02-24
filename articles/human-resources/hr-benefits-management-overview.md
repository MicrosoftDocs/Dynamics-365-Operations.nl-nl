---
title: Overzicht van Vergoedingenbeheer
description: Overzicht van de preview-functie Vergoedingenbeheer in Dynamics 365 Human Resources. Bied uw werknemers uitgebreide vergoedingsopties met een gebruiksvriendelijke online ervaring.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029458"
---
# <a name="benefits-management-overview"></a>Overzicht van Vergoedingenbeheer

[!include [banner](includes/preview-feature.md)]

Om concurrerend te blijven, moet u een uitgebreide reeks vergoedingen bieden om goede werknemers aan te trekken en te behouden. Naast standaardvergoedingen, zoals medische en tandheelkundige dekking, kunt u ook uitgebreide services aanbieden, zoals hulp bij adoptie, recreatieprogramma's en kledingtoelagen. De preview-functie Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources biedt u een flexibele oplossing die een breed scala aan vergoedingsopties ondersteunt. Human Resources bevat ook een gebruiksvriendelijke werknemerservaring waarin uw aanbod wordt gepresenteerd.

- De verbeterde functionaliteit voor vergoedingsplannen biedt u de mogelijkheid om unieke vergoedingsplannen te maken en beheren en ondersteunt complexe vergoedingstarieftabellen en geneste niveaus. U kunt eenvoudig vergoedingsprogramma's, bundels en automatische inschrijvingsregels maken voor een gebruiksvriendelijker werknemerservaring.

- Via flex-kredietprogramma's kunt u zorgen voor een evenredige verdeling van kredieten voor ondersteuning bij pensioenering en andere levensgebeurtenissen.

- De uitgebreide regels om te controleren of iemand voor een bepaalde vergoeding in aanmerking komt, zorgen ervoor dat u de juiste vergoedingen voor de juiste werknemers kunt maken.

- U kunt werknemers een gebruiksvriendelijke optie bieden om zich online in te schrijven voor vergoedingen.

- De verwerking van levensgebeurtenissen die recht geven op bepaalde vergoedingen, is geïntegreerd in het werkgebied Werknemerselfservice en biedt ook ondersteuning voor toekomstige levensgebeurtenissen.

Als u toegang wilt tot de demogegevens, moet u de sandbox-omgeving opnieuw implementeren.

U kunt direct feedback geven of problemen melden via: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Bekende problemen met Vergoedingenbeheer

### <a name="eligibility-processing"></a>Geschiktheidsverwerking

Bij het uitvoeren van de geschiktheidsverwerking voor vergoedingen met een dekkingsbedrag van 1-5X het salaris, % van salaris en een vast bedrag, moet de datum bij **Vergoedingsdetails** worden ingesteld op de **Begindatum voor werknemer** in **Historie dienstverband**. U moet ook **Gewerkte uren**, **Betalingsfrequentie** en **Jaarlijks salarisbedrag voor vergoedingen** opnemen. Als de medewerker vaste compensatie heeft, voert u de **Gewerkte uren** en de **Betalingsfrequentie** in. Het jaarlijkse salarisbedrag wordt berekend. Als de werknemer een vast salaris heeft, hoeft u **Gewerkte uren** niet in te voeren. Het is raadzaam eerst de vaste compensatie in te voeren wanneer u nieuwe medewerkers maakt. Als u de record met de vergoedingsdetails wilt bijwerken, gaat u naar **Medewerker > Medewerkershistorie > Dienstverbandgegevens**. Stel de datum in op de begindatum van de medewerker.

### <a name="employee-self-service"></a>Werknemerselfservice

Het bedrag van de werknemer wordt niet berekend wanneer het dekkingsbedrag voor de levensverzekering wordt bijgewerkt. Als aan een werknemer bijvoorbeeld een levensverzekeringsplan wordt aangeboden, kan deze maximaal €50.000 aan dekking selecteren tegen een kostprijs van €0,36 per €1.000 aan dekking.  Wanneer de werknemer het dekkingsbedrag bijwerkt, blijven de gekoppelde kosten van de werknemer nul.

Voor een vergoedingsplan dat slechts één selectie van dat plantype toestaat, krijgt de gebruiker een foutmelding als deze een plan probeert af te wijzen na het selecteren van een plan. Een gebruiker selecteert bijvoorbeeld een medisch plan en plaatst dit in zijn of haar winkelwagen. De gebruiker selecteert vervolgens **Afwijzen** voor een ander medisch plan. De gebruiker krijgt een foutmelding.

## <a name="enable-benefits-management"></a>Vergoedingenbeheer inschakelen

Vergoedingenbeheer is een preview-functie die alleen beschikbaar is in **sandbox**-omgevingen. In deze artikelen wordt beschreven hoe u preview-functies inschakelt in Human Resources. U leest hierin ook welke bestaande functies in Human Resources door Vergoedingenbeheer worden vervangen of worden uitgeschakeld wanneer u Vergoedingenbeheer inschakelt.

- [Functies beheren](hr-admin-manage-features.md)
- [Preview-functie: Vergoedingenbeheer](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Vergoedingenbeheer configureren

Voordat u vergoedingsplannen voor uw werknemers kunt maken, moet u opties voor de plannen configureren.

- [Parameters voor Vergoedingenbeheer instellen](hr-benefits-setup-parameters.md)
- [Geschiktheidsregels en -opties configureren](hr-benefits-setup-eligibility-rules.md)
- [Geschiktheidsopties voor persoonlijke contactpersonen configureren](hr-benefits-setup-contact-eligibility-options.md)
- [Dekkingsopties maken](hr-benefits-setup-coverage-options.md)
- [Betalingsfrequenties instellen](hr-benefits-setup-payment-frequencies.md)
- [Typen levensgebeurtenissen configureren](hr-benefits-setup-life-event-types.md)
- [Plantypen maken](hr-benefits-setup-plan-types.md)
- [Redencodes instellen](hr-benefits-setup-reason-codes.md)
- [Laagcodes instellen](hr-benefits-setup-tier-codes.md)
- [Tarieven configureren](hr-benefits-setup-rates.md)
- [Inhoudingen configureren](hr-benefits-setup-deductions.md)
- [Wachtdagen configureren](hr-benefits-setup-waiting-days.md)
- [Wachtperioden configureren](hr-benefits-setup-waiting-periods.md)
- [Afrondingsregels instellen](hr-benefits-setup-rounding-rules.md)
- [Dienstverbandcategorieën maken](hr-benefits-setup-employment-categories.md)
- [Dienstverbandtypen instellen](hr-benefits-setup-employment-types.md)
- [Werknemerselfservice configureren](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Vergoedingsplannen maken

In de volgende artikelen wordt uitgelegd hoe u vergoedingsplannen, waaronder bundels en flex-kredietprogramma's, kunt maken.

- [Vergoedingsplannen instellen](hr-benefits-plans-setup.md)
- [Vergoedingsplannen voor medewerkers maken](hr-benefits-plans-worker.md)
- [Flex-kredietprogramma's instellen](hr-benefits-plans-flex-credit-programs.md)
- [Toekomstige levensgebeurtenissen configureren](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Vergoedingenplannen verwerken

U moet enkele wijzigingen verwerken om deze actief te maken.

- [Geschiktheid voor inschrijving verwerken](hr-benefits-process-enrollment-eligibility.md)
- [Levensgebeurtenissen verwerken](hr-benefits-process-life-events.md)
- [Wijzigingen in levensgebeurtenissen verwerken](hr-benefits-process-life-event-changes.md)
- [Geschiktheid voor levensgebeurtenis verwerken](hr-benefits-process-life-event-eligibility.md)
- [Tariefwijzigingen verwerken](hr-benefits-process-rate-changes.md)

