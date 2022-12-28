---
title: Grootboekvereffeningsonderzoek
description: Dit artikel beschrijft het queryvenster voor grootboekvereffening
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853124"
---
# <a name="ledger-settlement-inquiry"></a>Grootboekvereffeningsonderzoek

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft het venster **Grootboekvereffeningsonderzoek** dat kan worden gebruikt om grootboektransacties voor een boekperiode weer te geven die zijn vereffend en/of waarvan de vereffening ongedaan is gemaakt.

## <a name="view-ledger-settlement-transactions"></a>Grootboekvereffeningstransacties weergeven
1.  Ga naar **Grootboek > Query´s en rapporten > Grootboekvereffeningsonderzoek**.
2.  Gebruik de velden **Begindatum** en **Einddatum** of **Datuminterval** om een datumbereik op te geven. Bij de proefbalans moet het datumbereik binnen één fiscaal jaar vallen.
3.  Selecteer in het veld **Hoofdrekeningen** een of meer hoofdrekeningen om de grootboektransacties voor te bekijken. In de vervolgkeuzelijst worden alleen hoofdrekeningen weergegeven die zijn ingesteld voor grootboekvereffening op de pagina **Grootboekparameters**.
4.  Gebruik het veld **Financiële dimensieset** om de financiële dimensies weer te geven in het raster. Omdat de hoofdrekening vereist is, wordt de waarde van het veld **Hoofdrekening** altijd als de eerste kolom weergegeven, zelfs als u een financiële dimensiegroep selecteert die de hoofdrekening niet bevat.
5.  Selecteer in het veld **Status**:
-   **Alle** om zowel vereffende als niet-vereffende transacties weer te geven
-   **Niet vereffend** om alleen niet-vereffende transacties weer te geven 
-   **Vereffend** om alleen vereffende transacties weer te geven
6.  Selecteer **Transacties weergeven**. Grootboektransacties worden weergegeven in het raster op basis van de criteria die u hebt ingevoerd. U kunt de resultaten van de query exporteren naar Microsoft Excel voor verdere analyse. Selecteer en houd ingedrukt (of klik met de rechtermuisknop) in het raster.

### <a name="column-details"></a>Kolomgegevens
Het raster op de pagina **Grootboekvereffeningsonderzoek** bevat de volgende kolommen:
-   **Hoofdrekening**: dit veld is verplicht en wordt altijd weergegeven.
-   **Financiële dimensies**: financiële dimensies worden weergegeven op basis van de geselecteerde financiële-dimensieset.
-   **Transactiedatum**: de boekingsdatum van de grootboektransactie.
-   **Oorspronkelijke transactiedatum**: als de jaarafsluiting is uitgevoerd en de grootboekvereffening zo is ingesteld dat deze details voor een hoofdrekening bijhoudt, worden de niet-vereffende transacties tot in detail overgebracht als openingssaldo. De oorspronkelijke boekingsdatum van de grootboektransactie wordt aangehouden in het veld **Oorspronkelijke transactiedatum**.
-   **Ouderdom van transactie**: de waarde is 0 (nul) voor alle vereffende transacties. Voor niet-vereffende transacties wordt de waarde berekend als het aantal dagen vanaf de oorspronkelijke transactiedatum of de transactiedatum tot aan de datum waarop de query wordt uitgevoerd.
Een grootboektransactie heeft bijvoorbeeld de transactiedatum 1 januari 2022 (1-1-2022) en de oorspronkelijke transactiedatum 30 december 2021 (30-12-2021). Als de aanvraag wordt uitgevoerd op 2 januari 2022 (1-2-2022) voor het boekjaar 2022, is de waarde voor de **Ouderdom van transactie** 4. Deze waarde wordt berekend als het aantal dagen tussen de oorspronkelijke transactiedatum (30-12-2021) en 2-1-2-2022.

Als er geen oorspronkelijke transactiedatum is, wordt in plaats daarvan de transactiedatum gebruikt.
-   **(Overige transactiegegevens)**: aanvullende kolommen bevatten informatie, zoals het boekstuknummer, de omschrijving en debet- en creditbedragen in alle drie de valuta's (van transactie, boekhouding en aangifte).
-   **Status**: deze waarde is **Vereffend** of **Niet vereffend**.
-   **Vereffenings-id**: de id die aan de vereffende transacties is toegewezen.

[![Pagina Grootboekvereffeningsonderzoek](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Totalen kunnen onder het raster worden weergegeven.
1.  Selecteer de puntjes (…) rechts van het raster en selecteer vervolgens **Voettekst tonen**.
2.  Selecteer elke bedragskolom en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens **Groeperen op deze kolom** om de totalen weer te geven. De totalen worden weergegeven in de voettekst. Als de query is gefilterd zodat alleen niet-vereffende transacties worden gevonden, kunt u de totalen gebruiken om de bedragen af te stemmen op de proefbalans.







