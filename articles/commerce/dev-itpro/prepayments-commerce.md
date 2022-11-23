---
title: Vooruitbetalingen in Dynamics 365 Commerce
description: Dit artikel biedt een overzicht van de verwerking van vooruitbetalingstransacties in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780353"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Vooruitbetalingen in Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Dit artikel biedt een overzicht van de verwerking van vooruitbetalingstransacties in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce verwerkt vooruitbetalingstransacties voor de volgende betalingstypen die worden gebruikt in Klanten of Commerce:

- **Depositobetaling voor klantrekening**: een klant doet een aanbetaling bij het verkooppunt (POS). Commerce verwerkt de depositobetaling als een vooruitbetalingstransactie. Wanneer u de transactie boekt, wordt een betalingsjournaal gemaakt en geboekt op de **boekstukpagina** van het journaal in Commerce headquarters. Het selectievakje **Journaalboekstuk van vooruitbetaling** op het tabblad **Betaling** wordt automatisch ingeschakeld voor het betalingsjournaal. Zie [Globalisatieresources - Land-/regiospecifieke Help-inhoud](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content) voor meer informatie over vooruitbetaling en belastingsspecifieke informatie die relevant is voor de doelregio.
- **Klantorder met deposito:** een klant maakt een klantorder op het POS. De klant kan een deposito voor de order betalen op basis van het standaard depositopercentage dat is geconfigureerd op de pagina **Klantorders** in Commerce headquarters (**Handelparameters \> Klantorders**). Commerce verwerkt de depositobetaling voor de klantorder als een vooruitbetalingstransactie. Wanneer u de transactie boekt, wordt een betalingsjournaal gemaakt en geboekt op de pagina **Journaalboekstuk**. Het selectievakje **Journaalboekstuk van vooruitbetaling** op het tabblad **Betaling** wordt automatisch ingeschakeld voor het betalingsjournaal. De betaling wordt vereffend en de klantfactuur wordt automatisch uitgegeven wanneer de order wordt opgehaald of geleverd.
- **Verkooporder callcenter**: een medewerker van de klantenservice van een callcenter maakt een verkooporder namens een klant en het **vooruitbetalingskenmerk** wordt tijdens het vastleggen van de betaling ingesteld op **Ja**.

Commerce voert de volgende taken uit om een vooruitbetaling te verwerken:

- **Een depositobetaling van een klantrekening verwerken**: een depositobetaling van een klant wordt overgeboekt naar Commerce met behulp van een service die gegevens synchroniseert. Commerce maakt een detailhandelbetalingstransactie. Wanneer u de detailhandeltransactie boekt, wordt een kasjournaal of klantbetalingsjournaal geboekt. Het selectievakje **Journaalboekstuk van vooruitbetaling** op het tabblad **Betaling** van de pagina **Journaalboekstuk** in Commerce headquarters wordt automatisch voor het betalingsjournaal ingeschakeld. Vooruitbetalingen kunnen niet worden verwerkt als het betalingsbedrag negatief is.
- **Een klant- of verkooporder met een deposito verwerken**: een klant doet een vereiste aanbetaling voor een klantorder via Commerce Data Exchange: Real-time Service. Commerce maakt een klantbetalingsjournaal of een kasjournaal, afhankelijk van de betalingsmethode die de klant gebruikt. Het selectievakje **Journaalboekstuk van vooruitbetaling** op het tabblad **Betaling** van de pagina **Journaalboekstuk** in Commerce headquarters wordt automatisch voor het journaal ingeschakeld. Als een klant meerdere betalingsmethoden gebruikt voor gedeeltelijke betalingen, verwerkt Commerce elke gedeeltelijke betaling op basis van de gebruikte betalingsmethode.

Voor creditcards en digitale wallets die onderliggende creditcardbetalingsmethoden hebben, verzendt Commerce een aanvraag om gegevens vast te leggen na een geslaagde autorisatie. (Het bedrag wordt vastgelegd voordat de verkooporder wordt gefactureerd.)

Als u een klantorder annuleert, wordt het vooruitbetalingsbedrag gerestitueerd en wordt een restitutiebetalingsjournaal geboekt voor het depositobedrag. Het restitutiebedrag wordt berekend en geboekt op basis van de betalingsmethode die u hebt opgegeven toen u de restitutiebetaling boekte. Commerce kan annuleringskosten toepassen op basis van het percentage dat u op de pagina **Handelparameters** in Commerce headquarters hebt ingesteld.

Als u een klantorder retourneert, worden een retourorder en een betalingsjournaal voor restitutie gemaakt. Wanneer u de retourorder maakt, wordt in Commerce een klantbetalingsjournaal of een kasjournaal gemaakt, afhankelijk van de betalingsmethode die de klant heeft gebruikt voor de oorspronkelijke transactie.
