---
title: Externe gegevens in cashflowprognoses
description: In dit onderwerp worden de installatiestappen beschreven die u moet voltooien, zodat externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses.
author: rcarlson
ms.date: 12/21/2021
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
ms.openlocfilehash: 8284ccd7ac383c53960f7fd6a1333aeb0e7e6f3c
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969007"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Externe gegevens in cashflowprognoses

[!include [banner](../includes/banner.md)]

Externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses. Dit onderwerp beschrijft de instellingsstappen die specifiek zijn voor het gebruik van externe gegevens en waarmee de externe gegevens in een cashflowprognose kunnen worden opgenomen.

## <a name="external-data-setup"></a>Externe gegevens instellen

Gebruik het tabblad **Externe bron** op de pagina **Instelling van cashflowprognose** (**Contanten en bankbeheer \> Cashflowprognose \> Instelling van cashflowprognose**) om instellingen op te geven die het gebruik van externe gegevens in cashflowprognoses ondersteunen.

Externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses. Voordat externe gegevens worden ingevoerd of geïmporteerd, moeten externe bronnen zijn ingesteld. Stel externe cashflowcategorieën in op het tabblad **Externe bron**. Een categorie kan **Uitgaand** of **Inkomend** zijn. **Liquiditeit** moet als boekingstype worden geselecteerd. Selecteer in het raster met **instellingen van de rechtspersoon** de rechtspersonen en de bijbehorende hoofdrekeningen waar de externe cashflowcategorieën van toepassing zijn.

Zie [Cashflowprognose](../cash-bank-management/cash-flow-forecasting.md) voor meer informatie over het instellen van cashflowprognoses.

## <a name="enter-external-data"></a>Externe gegevens invoeren

Als u externe gegevens wilt invoeren en wijzigen voor cashflowprognoses, kunt u de ervaring **Openen in Excel** gebruiken. Selecteer de knop **Externe gegevens** op de pagina **Instelling van cashflowprognose** en selecteer **Externe gegevens toevoegen** of **Bestaande externe gegevens bewerken**. Wanneer het Microsoft Excel-bestand wordt geopend, kunt u informatie invoeren in de volgende velden:

- **Invoer-id** (uniek)
- **Beschrijving** (optioneel)
- **Naam van externe bron**: selecteer een van de waarden in de lijst die u hebt gedefinieerd bij het instellen van Finance Insights.
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
