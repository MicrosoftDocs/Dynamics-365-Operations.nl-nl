---
title: Dashboard Gebruiksbeheer
description: In dit onderwerp wordt uitgelegd hoe u het dashboard voor gebruiksbeheer gebruikt om het gebruik van de elektronische factureringsservice te controleren en compatibel te blijven.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130501"
---
# <a name="usage-management-dashboard"></a>Dashboard Gebruiksbeheer

[!include [banner](../includes/banner.md)]

Met het dashboard **Gebruiksbeheer** kunt u het gebruik van de elektronische factureringsservice controleren en daardoor kan uw organisatie conform blijven met betrekking tot het maandelijkse gebruik. Compliance wordt bepaald door het indieningsvolume te berekenen en deze te vergelijken met het aangekochte volume van indieningen om eventuele afwijkingen tussen het aangekochte volume en het gebruikte volume aan te geven.

Het dashboard bevat de volgende indicatoren:

- Een kostenindicator die u kunt gebruiken om het verbruik te controleren voor doeleinden van conformiteit van licenties:

    - Gebruik per maand (export)

- Drie operationele indicatoren die u kunt gebruiken om het gebruik van de elektronische factureringsservice bij te houden voor beheerdoeleinden:

    - Gebruik per functie
    - Gebruik per omgeving
    - Gebruik per maand (import)

## <a name="measurement-scope"></a>Bereik van metingen

- Maateenheid: 

    Met het dashboard **Gebruiksbeheer** wordt de indiening van bedrijfsdocumenten en geïmporteerde elektronische facturen geteld.

- Organisatie: 

    Tellen wordt samengevat door de tenant-id van uw organisatie, ongeacht het aantal exemplaren van Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management of het aantal rechtspersonen waar de elektronische factureringsservice is ingeschakeld.


## <a name="indicator-usage-per-month-export"></a>Indicator: Gebruik per maand (export)

Deze indicator geeft details over de elektronische facturen die uw organisatie tijdens een gedefinieerde periode uitgeeft.

### <a name="scope"></a>Bereik
- Het aantal bedrijfsdocumenten dat via Finance en Supply Chain Management wordt ingediend bij de elektronische factureringsservice, ongeacht het aantal regels dat deze bedrijfsdocumenten bevatten.
- Het aantal ingediende bedrijfsdocumenten dat met succes wordt verwerkt door de elektronische factureringsservice. Een document wordt als succesvol verwerkt beschouwd wanneer de stroom acties die in de functie-instellingen zijn gedefinieerd, is voltooid.

> [!NOTE]
> Wanneer een elektronische factuur wordt ingediend bij een externe webservice, is de telling onafhankelijk van de resultaten van de verwerking van de webservice (geaccepteerd, afgewezen of schemavalidatiefout). Als de webservice de aanvraag van de elektronische factureringsservice heeft ontvangen en beantwoord, wordt de indiening als een geldige telling beschouwd.

- **Uitzondering**: bedrijfsdocumenten worden niet geteld als ze opnieuw vanuit Finance en Supply Chain Management worden ingediend bij de elektronische factureringsservice, zoals in de scenario's waarin een nieuwe inzending van hetzelfde bedrijfsdocument nodig is om de status van de elektronische factuur te wijzigen. Uitgifte van een Braziliaanse elektronische factuur (belastingdocument) wordt bijvoorbeeld geteld als geldig, maar de annuleringsaanvraag voor de factuur wordt niet geteld.


### <a name="calculation"></a>Berekening

De berekening van het saldo wordt als volgt berekend:

Saldo = Gratis + Ingekocht – Gebruikt

Hierin:

- Gratis:
  
    Een gratis volume bedrijfsdocumenten die de klant per maand kan indienen. Het bevat een pakket van 100 bedrijfsdocumenten die bij de elektronische factureringsservice kunnen worden ingediend. Een gratis volume is niet cumulatief en resterende saldi worden niet meegenomen naar de volgende periode.
  
- Ingekocht:
  
    Een pakket van 1.000 bedrijfsdocumenten die bij de elektronische factureringsservice kunnen worden ingediend. Dit pakket moet maandelijks voor uw organisatie worden verworven. Ingekocht volume is niet cumulatief en resterende saldi worden niet meegenomen naar de volgende periode.
  
- Gebruikt: 

    De telling van bedrijfsdocumentindieningen bij de elektronische factureringsservice volgens gedefinieerde criteria.
   
> [!IMPORTANT]
> Als uw organisatie van plan is om het maandelijkse volume van 100 gratis indieningen te overschrijden, koopt u het piekvolume om ervoor te zorgen dat u voldoet aan het Microsoft-licentiebeleid voor de elektronische factureringsservice.
>
> Op dit moment moet het ingekochte volume volgens de verwervingsdatum handmatig worden ingevoerd als meerdere pakketten van 1000 indieningen.

## <a name="indicator-usage-by-feature"></a>Indicator: Gebruik door functie

Deze indicator toont het gebruik van elektronische factureringsfuncties voor de uitgifte van elektronische facturen tijdens een gedefinieerde periode.

- Berekening:
  
    Gebruikt = het aantal keren dat elke elektronische factureringsfunctie is gebruikt tijdens de indiening van bedrijfsdocumenten bij de elektronische factureringsservice.

## <a name="indicator-usage-by-environment"></a>Indicator: Gebruik door omgeving

Deze indicator geeft het gebruik van omgevingen van de elektronische factureringsservice gedurende een gedefinieerde periode aan.

- Berekening:
    
    Gebruikt = het aantal keren dat elke omgeving van de elektronische factureringsfunctie is gebruikt tijdens de indiening van bedrijfsdocumenten bij de elektronische factureringsservice.

## <a name="indicator-usage-per-month-import"></a>Indicator: Gebruik per maand (import)

Deze indicator geeft het volume weer van het importeren van elektronische facturen door de elektronische factureringsservice bij Finance en Supply Chain Management gedurende een gedefinieerde periode.

- Bereik:

    Elektronische facturen die worden geïmporteerd in Finance en Supply Chain Management, ongeacht het aantal regels dat die elektronische facturen bevatten.

- Berekening:

    Ontvangen = de telling van geïmporteerde elektronische facturen in Finance en Supply Chain Management.

## <a name="functions"></a>Functies
### <a name="purchase"></a>Inkoop

Selecteer **Inkoop** op het tabblad **Gebruik per maand (export)** om het bedrag van de verworven indieningen handmatig te registreren.

Voor een bepaalde datum selecteert u **Nieuw** en voert u het aantal **Pakketten** in dat op die datum is verworven.

De **Hoeveelheid** wordt als volgt berekend:

Hoeveelheid = Pakketten * 1000

De berekende **Hoeveelheid** wordt weergegeven in **Ingekocht** van de indicator **Gebruik per maand (export)**.

### <a name="update"></a>Update

Selecteer in het actievenster de optie **Bijwerken** om de berekening te vernieuwen en de gegevens bij te werken die op de pagina en in het diagram worden weergegeven.

### <a name="reset-history-data"></a>Historische gegevens opnieuw instellen

Selecteer in het actievenster de optie **Historiegegevens opnieuw instellen** om de database te vernieuwen op basis van de plaats waar de indicatoren worden berekend.




> [!NOTE]
> Op het dashboard **Gebruiksbeheer** worden geen geldbedragen weergegeven. In plaats daarvan wordt alleen het volume van getelde indieningen en geïmporteerde documenten weergegeven.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
