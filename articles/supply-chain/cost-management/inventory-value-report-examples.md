---
title: Voorbeelden en logica voorraadwaardenrapporten
description: Dit onderwerp geeft enkele voorbeelden van resultaten die worden gepresenteerd op elk type voorraadwaardenrapport. Voorraadwaardenrapporten geven informatie over de fysieke en financiële hoeveelheden en bedragen in uw voorraad.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d594fc18a104c434a334a5b6d1d249330a6be9a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675314"
---
# <a name="inventory-value-report-examples-and-logic"></a>Voorbeelden en logica voorraadwaardenrapporten

[!include [banner](../includes/banner.md)]

Voorraadwaardenrapporten geven informatie over de fysieke en financiële hoeveelheden en bedragen in uw voorraad. Dit onderwerp geeft enkele voorbeelden van resultaten die worden gepresenteerd op elk type voorraadwaardenrapport.

Zie [Voorraadwaardenrapporten](inventory-value-report-storage.md) voor meer informatie over het genereren en gebruiken van elk type voorraadwaardenrapport.

## <a name="sample-data-that-is-used-in-these-examples"></a>Voorbeeldgegevens die in deze voorbeelden worden gebruikt

De voorbeelden in dit onderwerp zijn gebaseerd op de voorbeeldgegevens voor voorraadtransacties die in deze sectie worden beschreven.

### <a name="storage-dimension-setup"></a>Instellingen opslagdimensiegroep

Het voorbeeldsysteem bevat de volgende instellingen voor opslagdimensies.

| Naam | Actief | Fysieke voorraad | Financiële voorraad |
|---|---|---|---|
| Locatie | Ja | Ja | Ja |
| Magazijn | Ja | Ja | Nee |

### <a name="inventory-model"></a>Voorraadwaarderingsmodel

Voor het voorbeeldsysteem is het voorraadmodel voor de vrijgegeven producten *FIFO* en het veld **Kostprijs** voor het voorraadmodel is ingesteld op *Fysieke waarde opnemen*.

### <a name="inventory-transactions"></a>Voorraadtransacties

Het voorbeeldsysteem bevat de volgende voorraadtransacties voor een vrijgegeven product met artikelnummer *B0001*.

| Verwijzing | Locatie | Magazijn | Ontvangst | Probleem | Fysieke datum | Fin. datum | Hoeveelheid | Kosten | Fysieke kostprijs |
|---|---|---|---|---|---|---|---|---|---|
| Inkooporder | 1 | 11 | Ingekocht | | 15 maart | 15 maart | 10 | 1.000 | 1.000 |
| Inkooporder | 2 | 21 | Ingekocht | | 15 maart | 15 maart | 10 | 2,000 | 2,000 |
| Inkooporder | 1 | 11 | Ontvangen | | 15 april | | 5 | | 375 |
| overboekingsorder | 1 | 11 | | Verkocht | mei 2 | mei 2 | -5 | -458,33 | -458,33 |
| overboekingsorder | 1 | 12 | Ingekocht | | mei 2 | mei 2 | 5 | 458.33 | 458.33 |
| Verkooporder | 1 | 12 | | Verkocht | mei 3 | mei 3 | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Configuratie van voorraadwaardenrapport

Het voorbeeldsysteem bevat een configuratie voor het voorraadwaardenrapport met de volgende instellingen:

- **Bereik:**  *Boekingsdatum*
- **Voorraad:** *Ja*
- **Gemiddelde eenheidskosten berekenen:** *Ja*
- **Totale hoeveelheid en waarde:** *Ja*
- **Locatie, Weergeven:** *Geselecteerd*
- **Resource-id, Weergeven:** *Ja*
- **Niveau:** *Totalen*

## <a name="inventory-value-report-example-1"></a>Voorraadwaardenrapport voorbeeld 1

De volgende tabel en afbeeldingen geven de resultaten weer wanneer u de voorbeeldgegevens en de rapportconfiguratie gebruikt die eerder in dit onderwerp zijn beschreven.

| Resourcetype | Bron | Locatie | Verwijzing | Voorraad: financiële hoeveelheid | Voorraad: financieel bedrag | Voorraad: fysieke geboekte hoeveelheid | Voorraad: fysiek geboekt bedrag | Voorraad: hoeveelheid | Voorraad: bedrag | Gemiddelde kostprijs per eenheid |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiaal | B0001 | 1 | Eindsaldo | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Materiaal | B0001 | 2 | Eindsaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standaard voorraadwaardenrapport voor voorbeeld 1

In de volgende afbeelding ziet u een **Voorraadwaardenrapport** voor voorbeeld 1. (Selecteer de afbeelding om een grotere versie te openen.)

[![Voorraadwaardenrapport voor voorbeeld 1.](media/inventory-value-report-ex1-small.png "Voorraadwaardenrapport voor voorbeeld 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Rapport Opslag voor voorraadwaardenrapport voor voorbeeld 1

In de volgende afbeelding ziet u het rapport **Opslag voorraadwaardenrapport** voor voorbeeld 1. (Selecteer de afbeelding om een grotere versie te openen.)

[![Rapport Opslag voor voorraadwaardenrapport voor voorbeeld 1.](media/inventory-value-report-storage-ex1-small.png "Rapport Opslag voor voorraadwaardenrapport voor voorbeeld 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Voorraadwaardenrapport voorbeeld 2

De volgende tabel en afbeeldingen tonen de resultaten wanneer u de voorbeeldgegevens gebruikt die eerder in dit onderwerp zijn beschreven, maar u de waarde van het veld **Niveau** wijzigt in *Transacties* in de rapportconfiguratie en u het veld **Begindatum** instelt op *15 maart* wanneer u het rapport uitvoert.

| Resourcetype | Bron | Locatie | Datum | Nummer | Verwijzing | Voorraad: financiële hoeveelheid | Voorraad: financieel bedrag | Voorraad: fysieke geboekte hoeveelheid | Voorraad: fysiek geboekt bedrag | Voorraad: hoeveelheid | Voorraad: bedrag |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiaal | B0001 | 1 | 15-03-2021 | 00000126 | Inkooporder | 0,00 | 0,00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| Materiaal | B0001 | 1 | 15-03-2021 | 00000126 | Inkooporder | 10.00 | 1,000.00 | -10.00 | -1.000,00 | **0.00** | **0.00** |
| Materiaal | B0001 | 1 | 15-04-2021 | 00000128 | Inkooporder | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materiaal | B0001 | 1 | 2-5-2021 | 000003 | Zending van transferorder | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Materiaal | B0001 | 1 | 2-5-2021 | 000003 | Transferorder ontvangst | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiaal | B0001 | 1 | 3-5-2021 | 000835 | Verkooporder | 0,00 | 0,00 | -1,00 | -91,67 | **-1.00** | **-91.67** |
| Materiaal | B0001 | 1 | 3-5-2021 | 000835 | Verkooporder | -1,00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Materiaal | B0001 | 2 | 15-03-2021 | 00000127 | Inkooporder | 0,00 | 0,00 | 10.00 | 2,000.00 | **10.00** | **2,000.00** |
| Materiaal | B0001 | 2 | 15-03-2021 | 00000127 | Inkooporder | 10.00 | 2,000.00 | -10.00 | -2000,00 | **0.00** | **0.00** |
| Materiaal | B0001 | 2 | 2-5-2021 | 000003 | Zending van transferorder | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiaal | B0001 | 2 | 2-5-2021 | 000003 | Transferorder ontvangst | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standaard voorraadwaardenrapport voor voorbeeld 2

In de volgende afbeelding ziet u een **Voorraadwaardenrapport** voor voorbeeld 2. (Selecteer de afbeelding om een grotere versie te openen.)

[![Voorraadwaardenrapport voor voorbeeld 2.](media/inventory-value-report-ex2-small.png "Voorraadwaardenrapport voor voorbeeld 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Rapport Opslag voor voorraadwaardenrapport voor voorbeeld 2

In de volgende afbeelding ziet u het rapport **Opslag voorraadwaardenrapport** voor voorbeeld 2. (Selecteer de afbeelding om een grotere versie te openen.)

[![Rapport Opslag voor voorraadwaardenrapport voor voorbeeld 2.](media/inventory-value-report-storage-ex2-small.png "Rapport Opslag voor voorraadwaardenrapport voor voorbeeld 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Voorraadwaardenrapport voorbeeld 3

Het is raadzaam voorraadwaardenrapporten uit te voeren na een herberekening of voorraadafsluiting, zodat u de transacties en bedragen hebt die worden beïnvloed door de herberekening of voorraadafsluiting.

In de volgende subsecties worden de rapporten met voorraadwaarden tonen die worden gegenereerd nadat u de voorraad tot 30 mei hebt gesloten.

### <a name="example-3-when-the-totals-level-is-used"></a>Voorbeeld 3 wanneer het niveau Totalen wordt gebruikt

De volgende tabel geeft de resultaten weer wanneer u de voorbeeldgegevens en de rapportconfiguratie gebruikt die eerder in dit onderwerp zijn beschreven. (In de rapportconfiguratie is het veld **Niveau** ingesteld op *Totalen*.)

| Resourcetype | Bron | Locatie | Verwijzing | Voorraad: financiële hoeveelheid | Voorraad: financieel bedrag | Voorraad: fysieke geboekte hoeveelheid | Voorraad: fysiek geboekt bedrag | Voorraad: hoeveelheid | Voorraad: bedrag | Gemiddelde kostprijs per eenheid |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiaal | B0001 | 1 | Eindsaldo | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Materiaal | B0001 | 2 | Eindsaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Voorbeeld 3 wanneer het niveau Transacties wordt gebruikt

De volgende tabel toont de resultaten wanneer u de voorbeeldgegevens gebruikt die eerder in dit onderwerp zijn beschreven, maar u de waarde van het veld **Niveau** wijzigt in *Transacties* in de rapportconfiguratie.

| Resourcetype | Bron | Locatie | Datum | Nummer | Verwijzing | Voorraad: financiële hoeveelheid | Voorraad: financieel bedrag | Voorraad: fysieke geboekte hoeveelheid | Voorraad: fysiek geboekt bedrag | Voorraad: hoeveelheid | Voorraad: bedrag |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiaal | B0001 | 1 | 15-03-2021 | 00000126 | Inkooporder | 0,00 | 0,00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| Materiaal | B0001 | 1 | 15-03-2021 | 00000126 | Inkooporder | 10.00 | 1,000.00 | -10.00 | -1.000,00 | 0,00 | 0,00 |
| Materiaal | B0001 | 1 | 15-04-2021 | 00000128 | Inkooporder | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materiaal | B0001 | 1 | 2-5-2021 | 000003 | Zending van transferorder | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiaal | B0001 | 1 | 2-5-2021 | 000003 | Transferorder ontvangst | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiaal | B0001 | 1 | 3-5-2021 | 000835 | Verkooporder | 0,00 | 0,00 | -1,00 | -91,67 | -1,00 | -91,67 |
| Materiaal | B0001 | 1 | 3-5-2021 | 000835 | Verkooporder | -1,00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Materiaal | B0001 | 1 | 31-5-2021 | 000835 | Verkooporder | 0,00 | -8,33 | 0,00 | 0,00 | 0,00 | -8,33 |
| Materiaal | B0001 | 1 | 31-5-2021 | 000003 | Zending van transferorder | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Materiaal | B0001 | 1 | 31-5-2021 | 000003 | Transferorder ontvangst | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiaal | B0001 | 2 | 15-03-2021 | 00000127 | Inkooporder | 0,00 | 0,00 | 10.00 | 2,000.00 | 10.00 | 2,000.00 |
| Materiaal | B0001 | 2 | 15-03-2021 | 00000127 | Inkooporder | 10.00 | 2,000.00 | -10.00 | -2000,00 | 0,00 | 0,00 |
| Materiaal | B0001 | 2 | 2-5-2021 | 000003 | Zending van transferorder | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiaal | B0001 | 2 | 2-5-2021 | 000003 | Transferorder ontvangst | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiaal | B0001 | 2 | 31-5-2021 | 000003 | Zending van transferorder | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiaal | B0001 | 2 | 31-5-2021 | 000003 | Transferorder ontvangst | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
