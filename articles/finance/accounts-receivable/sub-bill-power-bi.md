---
title: Power BI-inhoud voor facturering van abonnementen
description: In dit artikel wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud voor facturering van abonnementen.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849955"
---
# <a name="subscription-billing-power-bi-content"></a>Power BI-inhoud voor facturering van abonnementen

[!include[banner](../includes/banner.md)]

In dit artikel wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud voor facturering van abonnementen. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld. 

## <a name="overview"></a>Overzicht

De content voor facturering van abonnementen in Power BI is gemaakt voor de medewerkers en managers die betrokken zijn bij facturering van abonnementen. Dit bevat belangrijke statische gegevens voor facturering van abonnementen, zoals de maandelijkse terugkerende opbrengst (Monthly Recurring Revenue, MRR) voor factureringsplanningen en informatie voor het afnemende saldo en waterval voor uitstelplanningen. Het maakt gebruik van de gegevens van de facturerings- en uitstelplanningen om een overzicht te geven van terugkerende inkomsten en opbrengsten.

De Power BI-content bevat de volgende drie tabbladen, die in totaal vier analytische rapporten bieden: 

- **Analyses - MRR:** dit tabblad bevat het rapport **Maandelijks terugkerende facturering** en het rapport **Details van factureringsplanning**.
- **Analyses - Waterval:** Dit tabblad bevat het rapport **Opbrengstwaterval**.
- **Analyses - Afnemend saldo:** Dit tabblad bevat het rapport **Afnemend saldo**.

## <a name="view-data-on-the-analytical-reports"></a>Gegevens in de analytische rapporten weergeven

Voordat u gegevens in de analytische rapporten kunt weergeven, moet u een periodiek proces uitvoeren om de rapportgegevens voor elk rapport te genereren. Deze gegevens die in de rapporten nodig zijn, moeten worden gegenereerd omdat ze niet rechtstreeks in de database kunnen worden opgeslagen. 

1. Ga naar **Facturering van abonnementen \> Terugkerende contractfacturering \> Periodieke taken \> Batchverwerking voor MRR-analyserapport** en volg deze stappen:

    1. Voer een datumbereik van niet meer dan drie jaar in.
    2. Optioneel: stel een terugkerende taak voor batchverwerking in om de gegevens periodiek te vernieuwen.
    3. Selecteer **OK**.

2. Nadat de batchtaak is voltooid, gaat u naar **Systeembeheer \> Instellingen \> Entiteitsopslag** en vernieuwt u de samengevoegde meting **MRR-rapport**. 
3. Ga naar **Facturering van abonnementen \> Uitgestelde opbrengsten en onkosten \> Periodieke taken \> Batchverwerking voor watervalanalyserapport** en volg deze stappen:

    1. Voer een begin- en einddatum in die niet meer dan 26 perioden omvat. 
    2. Als u het prognosebedrag van afgelopen perioden in de huidige periode wilt weergeven, stelt u de optie **Prognose van voorbije bedragen in huidige periode** in op **Ja**.
    3. Optioneel: stel een terugkerende taak voor batchverwerking in om de gegevens periodiek te vernieuwen.
    4. Selecteer **OK**. 

4. Nadat de batchtaak is voltooid, gaat u naar **Systeembeheer \> Instellingen \> Entiteitsopslag** en vernieuwt u de samengevoegde meting **Watervalrapport**.
5. Ga naar **Facturering van abonnementen \> Uitgestelde opbrengsten en onkosten \> Periodieke taken \> Batchverwerking van analyserapport van afnemend saldo** en volg deze stappen:

    1. Voer een begin- en einddatum in die niet meer dan 26 perioden omvat. 
    2. Als u het prognosebedrag van afgelopen perioden in de huidige periode wilt weergeven, stelt u de optie **Prognose van voorbije bedragen in huidige periode** in op **Ja**.
    3. Optioneel: stel een terugkerende taak voor batchverwerking in om de gegevens periodiek te vernieuwen.
    4. Selecteer **OK**.

6. Nadat de batchtaak is voltooid, gaat u naar **Systeembeheer \> Instellingen \> Entiteitsopslag** en vernieuwt u de samengevoegde meting **Rapport over afnemend saldo**.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud

De content voor facturering van abonnementen in Power BI wordt weergegeven in de werkruimte **Facturering van abonnementen**.
