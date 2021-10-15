---
title: Visualisatie van uitgaande workload
description: Dit onderwerp biedt informatie over visualisatie van uitgaande workloads. Met deze functionaliteit kunnen magazijnbeheerders en supervisors aangepaste workloaddiagrammen maken die kunnen worden gebruikt om de voortgang van het huidige werk en de resterende hoeveelheid te controleren. Magazijnbeheerders kunnen meerdere weergaven maken en zo nodig automatisch vernieuwen instellen.
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8416d43fe2b8b08e4d66434a1d95daa4b01a0fa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576155"
---
# <a name="outbound-workload-visualization"></a>Visualisatie van uitgaande workload

[!include [banner](../includes/banner.md)]

Geavanceerde instellingsmogelijkheden die toegankelijk zijn via de pagina **Visualisatie van uitgaande workload** laten magazijnbeheerders en supervisors aangepaste workloaddiagrammen maken die kunnen worden gebruikt om de voortgang van het huidige werk en de resterende hoeveelheid te controleren. Magazijnbeheerders kunnen meerdere weergaven maken en zo nodig automatisch vernieuwen instellen. De visualisaties van uitgaande workloads zijn geschikt voor weergave op pagina's met magazijnprestaties.

Deze functie kan worden gebruikt om de voortgang van het orderverzamelen bij te houden. De functie is geïntegreerd met arbeidsbeheer, en als arbeidsbeheer is ingesteld, kunnen visualisaties van uitgaande workloads een berekening weergeven van het aantal uren dat resteert voor het orderverzamelen dat wordt weergegeven (gefilterd).

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>De functie Visualisatie van uitgaande workload inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-instellingen om de status van de functie te controleren en deze in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Visualisatie van uitgaande workload*

## <a name="set-up-outbound-workload-visualizations"></a>Visualisaties van uitgaande workloads instellen

Als u visualisaties wilt instellen, maakt u een verzameling filters (weergaven) en ontwerpt u elk filter zo dat er een ander type analyse wordt weergegeven. U gebruikt de pagina **Filters configureren** om de filters te ontwerpen.

Voer de volgende stappen uit om een visualisatie voor een uitgaande workload in te stellen.

1. Ga naar **Magazijnbeheer \> Rapporten van magazijnbewaking \> Visualisatie van uitgaande workload**.

    De pagina **Visualisatie van uitgaande workload** wordt weergegeven. Nadat u een aantal filters hebt gemaakt, wordt op deze pagina uw visualisatie weergegeven. U kunt zoveel filters maken als u wilt. Alle filters die u maakt, worden opgeslagen onder uw gebruikersaccount, zodat u ze later kunt gebruiken. Met andere woorden, elke gebruiker heeft een eigen set filters die ze hebben gemaakt. Deze filters worden niet gedeeld met andere gebruikers.

1. Selecteer op de pagina **Visualisatie van uitgaande workload** in het actievenster op het tabblad **Filters** de optie **Filters configureren**.
1. Selecteer op de pagina **Filters configureren** in het actievenster **Nieuw** om een filter toe te voegen en stel vervolgens de volgende velden in:

    - **Tabel groeperen X-as**: selecteer de tabel die het veld bevat dat moet worden gebruikt voor het groeperen van de waarden van de X-as.
    - **Veld groeperen X-as**: selecteer uit de velden van de tabel die u hebt geselecteerd in het veld **Tabel groeperen X-as** het veld dat moet worden gebruikt voor het groeperen van de waarden van de X-as.
    - **Tabel voor X-aswaarden**: selecteer de tabel die het veld bevat dat moet worden gebruikt voor het verder analyseren van de groepen.
    - **Veld voor X-aswaarden**: selecteer uit de velden van de tabel die u hebt geselecteerd in het veld **Tabel voor X-aswaarden** het veld dat de waarden levert die voor elke groep moeten worden geanalyseerd.
    - **Automatisch vernieuwen**: selecteer of de visualisatie automatisch moet worden vernieuwd.
    - **Vernieuwingsinterval (minuten)**: geef het aantal minuten op tussen automatisch vernieuwingen.
    - **Weergaveniveau**: selecteer of u in het diagram aantallen van openstaande regels of openstaande kopteksten wilt weergeven.
    - **Type orderverzameling**: als u het veld **Weergaveniveau** instelt op het _Open regels_, geeft u aan of het aantal openstaande werkregels in het diagram de eerste, klaargezette of zowel eerste als klaargezette orderverzamelingen moet bevatten.
    - **Site**: selecteer de site waarvoor u het diagram wilt laden.
    - **Magazijn**: selecteer het magazijn waarvoor u het diagram wilt laden.
    - **Op te nemen dagen**: geef het aantal dagen op in het verleden waarvoor het diagram moet worden gegenereerd.
    - **Werkordertype**: selecteer de typen uitgaande werkorder waarop u wilt filteren.

    ![Pagina Filters configureren.](media/work-viz-filters-1.png "Pagina Filters configureren")

1. Sluit de pagina **Filters configureren** om terug te keren naar de pagina **Visualisaties van uitgaande workload**.

    Op de pagina **Visualisaties van uitgaande workload** worden nu gegevens weergegeven op basis van de nieuwe filterinstellingen. Het nieuwe filter is nu beschikbaar en wordt geselecteerd in het veld **Filter**. De volgende velden zijn beschikbaar boven aan het diagram:

    - **Filter**: dit veld bevat alle filters die u tot dusverre hebt gemaakt. Selecteer een filter om de gegevens in het diagram weer te geven.
    - **Laatst vernieuwd**: dit veld bevat de datum en tijd waarop de gegevens in het diagram voor het laatst zijn bijgewerkt.
    - **Geschatte/werkelijke tijd**: als arbeidsstandaarden in het systeem zijn ingesteld, stelt u deze optie in op *Ja* om de geaccumuleerde geraamde verzameltijden boven aan elke kolom in het diagram weer te geven. Als u geen arbeidsstandaarden gebruikt, is deze optie niet beschikbaar.

    ![Voorbeeld visualisatie.](media/work-viz-chart.png "Voorbeeld visualisatie")

1. Selecteer een willekeurige staaf in het diagram om de bijbehorende werkregeldetails weer te geven.

    ![Details werkregel.](media/work-viz-work-details.png "Details werkregel")

## <a name="example-outbound-workload-visualization-for-zones"></a>Voorbeeld: Visualisatie van uitgaande workload voor zones

Voor dit voorbeeld wilt u een visualisatie instellen die werkregels weergeeft voor elke zone en de status van elke werkregel (_Open_, _Gesloten_ of _Geannuleerd_). In dat geval kunt u een filter instellen met de volgende instellingen:

- **Filternaam**: geef een naam op voor dit filter (bijvoorbeeld _Zone versus werkstatus_).
- **Beschrijving**: geef een korte beschrijving op voor dit filter (bijvoorbeeld _Zone versus werkstatus_).
- **Tabel groeperen X-as**: selecteer _Locaties._
- **X-asgroep**: selecteer _Zone-id_.
- **Tabel voor X-aswaarden**: selecteer _Werk_, omdat u het werk per zone wilt weergeven.
- **Veld voor X-aswaarden**: selecteer _Werkstatus_, omdat u de werkstatus wilt weergeven.
- **Automatisch vernieuwen**: selecteer of de visualisatie automatisch moet worden vernieuwd.
- **Type orderverzameling**: selecteer _Eerste verzamelingen en klaargezette verzamelingen_, omdat u de eerste verzamelingen en de verzamelingen uit faseringslocaties wilt opnemen. Met andere woorden, u wilt in wezen alle verzamelwerkregels opnemen.
- **Weergaveniveau**: selecteer _Open regels_, omdat u de informatie per regel wilt weergeven, niet per werkkoptekst.

In de volgende afbeelding ziet u een voorbeeld van het resulterende diagram.

![Visualisatie van zone vs. werkstatus.](media/work-viz-chart.png "Visualisatie van zone vs. werkstatus")

Dit diagram toont twee zones met de naam **VERDIEPING** en **BULK**, plus een zone met de naam **Leeg**. De **lege** zone vertegenwoordigt alle werkregels die geen deel uitmaken van een zone. In het diagram worden altijd alle niet-gerelateerde gefilterde gegevens als **Leeg** weergegeven, zodat u zo veel mogelijk inzicht krijgt. In de **VERDIEPING**-zone worden in het diagram drie afgesloten regels en vier openstaande regels weergegeven. In de **BULK**-zone worden in het diagram vier afgesloten regels, één openstaande regel en 24 geannuleerde regels weergegeven. Tot slot worden in het diagram acht afgesloten regels weergegeven die geen deel uitmaken van een zone en die dus **leeg** zijn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]