---
title: Contantkortingen
description: Contantkortingen worden ingesteld en gedeeld voor Leveranciers en Klanten.  De beschikbare contantkorting kan op de klant- of leveranciersfactuur worden gedefinieerd en deze wordt toegepast als de factuur wordt betaald binnen de datum voor de contantkorting.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d4f6d5bdf4f2fdc4529d9f51515ed2ac4b5b3b5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985307"
---
# <a name="cash-discounts"></a>Contantkortingen

[!include [banner](../includes/banner.md)]

Contantkortingen worden ingesteld en gedeeld voor Leveranciers en Klanten.  De beschikbare contantkorting kan op de klant- of leveranciersfactuur worden gedefinieerd en deze wordt toegepast als de factuur wordt betaald binnen de datum voor de contantkorting. 

## <a name="cash-discounts"></a>Contantkortingen

Contantkortingen voor zowel klanten als leveranciers kunnen op de pagina Contantkortingen worden gemaakt. Ook kunt u met behulp van het veld Volgende kortingscode een reeks contantkortingen maken die elkaar opvolgen, telkens wanneer de datum van de vorige contantkorting verloopt. Zie “Voorbeeld: reeks contantkortingen” verderop in dit onderwerp voor meer informatie. Als de factuur, credittransactie (een betaling of creditnota) of beide worden ingevoerd in een andere valuta dan de valuta voor boekhouding van de rechtspersoon, wordt de contantkorting berekend aan de hand van de wisselkoers op basis van de datum van de betaling of de creditnota. Als de factuur en het creditdocument worden ingevoerd in verschillende rechtspersonen en de valuta's voor boekhouding van de rechtspersonen verschillend zijn, wordt de wisselkoers gebruikt van de rechtspersoon van de factuur op de datum van het creditdocument. Zie “Voorbeeld: wisselkoersen voor contantkortingen” verderop in dit onderwerp voor meer informatie.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Standaardvolgorde van de hoofdrekening voor contantkortingen

Als een factuur wordt vereffend binnen de tijd waarin een contactkorting kan worden gegeven, wordt de contantkorting automatisch geboekt volgens de volgende standaardprioriteit naar een grootboekrekening voor contantkortingen:
1.  De hoofdrekening die is opgegeven in het veld Alternatieve contantkortingsrekening van de pagina Openstaande transacties vereffenen van de klant of de pagina Openstaande transacties vereffenen van de leverancier.
2.  De hoofdrekening die is opgegeven in het veld Contantkorting van de klant of het veld Contantkorting van leverancier van de grootboekboekingsgroep die is toegewezen aan de btw-code van de factuur. Configureer grootboekboekingsgroepen op de pagina Grootboekboekingsgroepen en wijs deze toe aan btw-codes op de pagina Btw-codes.
3.  De hoofdrekening voor boeking op de pagina Contantkortingen in het veld Hoofdrekening voor klantkortingen of het veld Hoofdrekening voor leverancierskortingen voor de contantkortingscode van de klant of leverancier op de vereffende factuur.
4.  De hoofdrekening voor contantkortingen, zoals gedefinieerd op de pagina Rekeningen voor automatische transacties.

## <a name="example-series-of-cash-discounts"></a>Voorbeeld: reeksen contantkortingen
Stel als volgt drie contantkortingscodes in:
-   Code 5D10%: er wordt een contantkorting van 10% gegeven als de factuur binnen 5 dagen wordt betaald.
-   Code 10D5%: er wordt een contantkorting van 5% gegeven als de factuur binnen 10 dagen wordt betaald.
-   Code 14D2%: er wordt een contantkorting van 2% gegeven als de factuur binnen 14 dagen wordt betaald.

In het veld Volgende kortingscode:
-   10D5% voor de code 5D10%.
-   14D2% voor de code 10D5%.
-   Voor de code 14D2% laat u het veld Volgende kortingscode leeg.

De drie contantkortingen volgen elkaar op wanneer de betaaldatum de vorige contantkortingsdatum op de factuur overschrijdt. Slechts één contantkorting wordt toegekend wanneer de factuur wordt betaald, afhankelijk van welke contantkorting aan bod is in de reeks kortingen.

## <a name="example-exchange-rates-for-cash-discounts"></a>Voorbeeld: wisselkoersen voor contantkortingen
De valuta voor boekhouding van de rechtspersoon is EUR en de volgende wisselkoersen zijn opgegeven voor USD:
-   1 februari = 110
-   1 maart = 80

Op 15 februari wordt een factuur geboekt voor 1000 USD met contantkortingsvoorwaarden van 20D2%. Het factuurbedrag in de valuta voor boekhouding is 1100 EUR. Een betaling van 980 USD wordt vereffend met de factuur op 1 maart. Het bedrag van de contantkorting is 20 USD. Het bedrag van de betaling in de valuta voor boekhouding is 784 EUR. Het bedrag van de contantkorting in de valuta voor boekhouding wordt berekend op basis van de wisselkoers op 1 maart: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> Als de optie Contantkortingen berekenen voor gedeeltelijke betalingen is geselecteerd op de pagina's Parameters van module Klanten of Parameters van module Leveranciers, wordt de wisselkoers gebruikt die geldt op de datum van elke deelbetaling. 

