---
title: Overzicht van Nummerreeksen
description: Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben.
author: SunilGarg
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "15461"
- intro-internal
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48e395cc3e3ccd0f93ab9523add455ef16f612ba
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985676"
---
# <a name="number-sequences-overview"></a>Overzicht van Nummerreeksen

[!include [banner](../includes/banner.md)]

Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben. Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een *verwijzing* genoemd.

Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen. Het is raadzaam om de formulieren in **Organisatiebeheer** te gebruiken om nummerreeksen in te stellen. Als er modulespecifieke instellingen zijn vereist, kunt u de parameterpagina in een module gebruiken om nummerreeksen op te geven voor de verwijzingen in die module. In **Klanten** en **Leveranciers** kunt u bijvoorbeeld nummerreeksgroepen instellen om specifieke nummerreeksen toe te wijzen aan specifieke klanten of leveranciers.

Wanneer u een nummerreeks instelt, moet u een bereik opgeven die definieert welke organisatie de nummerreeks gebruikt. De scope kan **Gedeeld**, **Bedrijf**, **Rechtspersoon** of **Operationele eenheid** zijn. De scopes van **rechtspersonen** en **bedrijven** kunnen ook met **Fiscale kalenderperiode** worden gecombineerd om nog specifiekere nummerreeksen te maken.

Nummerreeksnotaties bestaan uit segmenten. Nummerreeksen met een andere scope dan **Gedeeld**, kunnen segmenten bevatten die overeenkomen met de scope. Een nummerreeks met een scope van **Rechtspersoon** kan bijvoorbeeld een segment voor de rechtspersoon bevatten. Door een scopesegmenten in de nummerreeksnotatie op te nemen, kunt u de scope van een specifieke registratie bepalen door naar het nummer te kijken.

Naast de segmenten die overeenkomen met scopes, kunnen nummerreeksnotaties **constante** en **alfanumerieke** segmenten bevatten. Een **constant** segment bevat een reeks letters, cijfers of symbolen die niet verandert. Een **alfanumeriek** segment bevat een reeks letters of cijfers die worden verhoogd telkens als het nummer wordt gebruikt. Gebruik een hekje (\#) om stijgende nummers aan te geven en een en-teken (&) om stijgende letters aan te geven. De indeling \#\#\#\#\#\_2017 maakt bijvoorbeeld de reeks 00001\_2017, 00002\_2017, enzovoort.

## <a name="number-sequence-examples"></a>Voorbeelden van nummerreeksen

De volgende voorbeelden geven aan hoe u segmenten gebruikt om nummerreeksnotaties te maken. De voorbeelden tonen in het bijzonder de effecten van het gebruik van scopesegmenten.

### <a name="expense-report-numbers"></a>Onkostennotanummers

In het volgende voorbeeld worden onkostennotanummer ingesteld voor de rechtspersoon die **CS** heet.

- **Gebied:** Reis- en onkosten
- **Referentie:** Het nummer van de onkostennota
- **Bereik:** Rechtspersoon
- **Rechtspersoon:** CS

| Segmenten  | Segmenttype | Waarde     |
|-----------|--------------|-----------|
| Segment 1 | Rechtspersoon | CS        |
| Segment 2 | Constante     | -ONKOSTEN- |
| Segment 3 | Alfanumeriek | \#\#\#\#  |

**Voorbeeld van een opgemaakt nummer**: CS-EXPENSE-0039

U kunt een soortgelijke nummerreeksnotatie instellen voor andere rechtspersonen. Voor een rechtspersoon die **RW** heeft, is, wanneer u alleen de waarde van de rechtspersoon van het rechtspersoonsegment wijzigt, het opgemaakte nummer RW-EXPENSE-0039. U kunt ook de volledige nummerreeksnotatie wijzigen voor andere rechtspersonen. U kunt bijvoorbeeld het scopesegment van de rechtspersoon weglaten om een opgemaakt nummer zoals Exp-0001 te maken.

### <a name="sales-order-numbers"></a>Verkoopordernummers

In het volgende voorbeeld worden verkoopordernummers ingesteld voor de bedrijfs-id **CEU**.

- **Gebied:** Verkoop
- **Referentie:** Verkooporder
- **Bereik:** Bedrijf
- **Bedrijf:** CEU

| Segmenten  | Segmenttype | Waarde    |
|-----------|--------------|----------|
| Segment 1 | Constante     | SO-      |
| Segment 2 | Alfanumeriek | \#\#\#\# |

**Voorbeeld van een opgemaakt nummer**: SO-0029

Hoewel een scopesegment niet in de notaties is opgenomen, begint de nummering opnieuw voor elke bedrijfs-ID. Als u dezelfde notatie gebruikt voor alle bedrijfs-ID´s, dan worden dezelfde nummers in elk bedrijf gebruikt. Het verkoopordernummer SO-0029 wordt bijvoorbeeld in elk bedrijf gebruikt. U kunt ook de volledige nummerreeksnotatie wijzigen voor andere bedrijfs-ID´s.

### <a name="purchase-requisition-numbers"></a>Nummers van opdrachten tot inkoop

In het volgende voorbeeld zijn de nummers van de opdracht tot inkoop organisatiebreed.

- **Gebied:** Inkoop
- **Referentie:** Opdracht tot inkoop
- **Bereik:** Gedeeld

| Segmenten  | Segmenttype | Waarde    |
|-----------|--------------|----------|
| Segment 1 | Constante     | Behoefte      |
| Segment 2 | Alfanumeriek | \#\#\#\# |

**Voorbeeld van een opgemaakt nummer**: Req0052

Omdat het bereik **Gedeeld** is, wordt de nummerreeksnotatie in de hele organisatie gebruikt. U kunt geen verschillende nummerreeksnotaties instellen voor verschillende delen van de organisatie.

## <a name="performance-considerations-for-number-sequences"></a>Prestatieoverwegingen voor nummerreeksen

Bekijk de volgende gegevens over hoe de configuratie van nummerreeksen de systeemprestaties kan beïnvloeden voordat u nummerreeksen instelt.

### <a name="continuous-and-non-continuous-number-sequences"></a>Doorlopende en niet-doorlopende nummerreeksen

Nummerreeksen kunnen doorlopend of niet-doorlopend zijn. Een doorlopende nummerreeks slaat geen nummers over, maar de nummers mogen niet opeenvolgend worden gebruikt. Nummers van een niet-doorlopende nummerreeks worden opeenvolgend gebruikt, maar de nummerreeks kan nummers overslaan. Als een gebruiker bijvoorbeeld een transactie annuleert, wordt een nummer gegenereerd, maar niet gebruikt. In een doorlopende nummerreeks, wordt dat nummer later opnieuw gebruikt. In een niet-doorlopende nummerreeks, wordt het nummer niet gebruikt.

Doorlopende nummerreeksen zijn normaal gezien vereist voor externe documenten, zoals inkooporders, verkooporders en facturen. Doorlopende nummerreeksen kunnen de reactietijden van het systeem nadelig beïnvloeden, maar het systeem moet een nummer aanvragen bij de database telkens als een nieuw document of registratie wordt gemaakt.

Als u een niet-doorlopende nummerreeks gebruikt, kunt u **Voorafgaande toewijzing** inschakelen op het sneltabblad **Prestaties** op de pagina **Nummerreeksen**. Wanneer u een hoeveelheid nummers opgeeft om vooraf toe te wijzen, selecteert het systeem die nummers en bewaart het ze in het geheugen. Nieuwe nummers worden alleen bij de database opgevraagd nadat de vooraf toegewezen hoeveelheid is gebruikt.

Tenzij er een regelgevende vereiste is die doorlopende nummerreeksen gebruikt, bevelen we u aan om niet-doorlopende nummerreeksen te gebruiken voor betere prestaties.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatische opschoning van nummerreeksen

Bij een stroomuitval, een toepassingsfout of andere onverwachte storting, kan het systeem nummers niet automatisch opnieuw gebruiken voor doorlopende nummerreeksen. U kunt het opschoonproces handmatig of automatisch uitvoeren om de verloren nummers te herstellen.

Overweeg zorgvuldig het servergebruik wanneer u het opschoonproces plant. Het is aan te raden het opschonen als batchtaak uit te voeren tijdens de daluren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
