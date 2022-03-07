---
title: Externe gegevens in cashflowprognoses gebruiken
description: In dit onderwerp worden de installatiestappen beschreven die u moet voltooien zodat externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 855f428ae8ce79f2b7ce9a6f3347cd454bad9566
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386457"
---
# <a name="use-external-data-in-cash-flow-forecasts"></a>Externe gegevens in cashflowprognoses gebruiken

[!include [banner](../includes/banner.md)]

Externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses. Dit onderwerp beschrijft de instellingsstappen die specifiek zijn voor het gebruik van externe gegevens en waarmee de externe gegevens in een cashflowprognose kunnen worden opgenomen.

## <a name="external-data-setup"></a>Externe gegevens instellen

Gebruik het tabblad **Externe bron** op de pagina **Instelling van cashflowprognose** (**Contanten en bankbeheer \> Cashflowprognose**) om instellingen op te geven die het gebruik van externe gegevens in cashflowprognoses ondersteunen.

Zie voor meer informatie over het instellen [Cashflowprognose](../cash-bank-management/cash-flow-forecasting.md).

Als u externe gegevens wilt invoeren voor cashflowprognoses, kunt u de ervaring Openen in Excel gebruiken voor het invoeren en wijzigen van externe gegevens. Selecteer de knop **Externe gegevens** en selecteer vervolgens **Externe gegevens toevoegen** of **Bestaande externe gegevens bewerken**. Wanneer het Microsoft Excel-bestand wordt geopend, kunt u informatie invoeren in de volgende velden:

- **Invoer-ID**
- **Beschrijving** (optioneel)
- **Naam van externe bron**: selecteer een van de waarden in de lijst die u hebt gedefinieerd bij het instellen van Financiële inzichten.
- **Rechtspersoon**
- **Datum**
- **Bedrag in transactievaluta**
- **Valutacode**
- **Standaarddimensie** (optioneel)
- **Documentnummer** (optioneel)
- **Rekeningnummer** (optioneel)
- **Rekeningnaam** (optioneel)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Externe gegevens importeren met behulp van het Gegevensbeheer-framework

U kunt externe gegevens importeren voor cashflowprognoses met behulp van het werkgebied **Gegevensbeheer** en de entiteit met de naam **Invoer externe bron cashflowprognose**.

Bovendien, als u instellingsgegevens van de ene omgeving naar de andere moet verplaatsen, zijn de volgende entiteiten beschikbaar voor de vereiste instellingstabellen:

- Externe bron voor cashflowprognose instellen
- Rechtspersoon van externe bron voor cashflowprognose instellen

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
