---
title: Boeking voor standaardkostenafwijking
description: Dit onderwerp bevat informatie over het instellen van boekingsprofielen voor standaardkostprijsberekening.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804602"
---
# <a name="standard-cost-variance-posting"></a>Boeking voor standaardkostenafwijking

Wanneer u standaardkostprijsberekening gebruikt voor een of meer producten in uw organisatie, moet u de [vereisten voor standaardkostprijsberekening](/supply-chain/cost-management/prerequisites-standard-costs.md) configureren. In dit onderwerp worden de boekingsrekeningen uitgelegd die nodig zijn voor stap 3 van de vereisten: "Grootboekrekeningen toewijzen aan artikelboekingen die zijn gerelateerd aan standaardkostenafwijkingen".

Er kunnen verschillende typen afwijkingen voorkomen voor inkopen en productieorders. Zie [Veelvoorkomende bronnen van productieafwijkingen](/supply-chain/cost-management/common-sources-of-production-variances.md) voor voorbeelden van productieafwijkingen. Prijsafwijkingen in inkooporders treden op wanneer u de standaardkosten voor een ingekocht artikel gebruikt en er een verschil is tussen de standaardkosten van het product en het gefactureerde bedrag op de inkooporder.

## <a name="sample-posting-profile-configuration"></a>Voorbeeldconfiguratie van boekingsprofiel

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen. De tabel bevat voorbeeldhoofdrekeningen en omschrijvingen.

- De kolom Debet/Credit? geeft aan of de transactie meestal een debet- of credittransactie betreft. In sommige gevallen kan de transactie debet- of credittransacties boeken.
- De kolom "Vereffeningsrekening" geeft aan of het boekingstype een vereffeningsrekening is. Met andere woorden: het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt.
- De kolom "P/F" geeft het type boeking aan. "P" staat voor fysieke boeking en "F" staat voor financiële boeking.
- De kolom "Volgen" geeft aan of de hoofdrekening voor het boekingstype gewoonlijk hetzelfde is als de hoofdrekening voor een ander boekingstype. Met name wordt het boekingstype aangegeven dat doorgaans wordt gebruikt.

> [!NOTE]
> De hoofdrekeningen en hoofdrekeningnamen in de tabel zijn suggesties. Het is raadzaam om samen met uw accountant te bepalen wat de beste configuratie is voor uw bedrijfsbehoeften.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Afwijking inkoopprijs | 510310 | Afwijking inkoopprijs | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt wanneer er een afwijking is tussen de inkoopprijs en de standaardkosten op een inkooporder. |
| Herwaardering voorraadkosten | 510330 | Herwaardering voorraadkosten | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt wanneer een nieuwe kostprijsberekeningsversie is geactiveerd voor een standaardkostenartikel om de voorhanden voorraad te herwaarderen. |
| Afwijking kostenwijziging | 510320 | Afwijking kostenwijziging | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt als er een verschil is in standaardkosten tussen sites of wanneer een artikel wordt geretourneerd en er een wijziging is tussen de oorspronkelijke standaardkosten en de huidige standaardkosten voor een product. |
| Afwijking productiepartijgrootte | 510370 | Afwijking productiepartijgrootte | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt als er verschillen zijn tussen de berekeningsbasis van de stuklijst en de werkelijke hoeveelheid voor de kostenberekening van de productieorder. |
| Productieprijsafwijking | 510340 | Productieprijsafwijking | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt als er prijsverschillen zijn tussen de kostenraming en de werkelijke kosten voor een productieorder. |
| Afwijking productiehoeveelheid | 510350 | Afwijking productiehoeveelheid | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt als er hoeveelheidsverschillen zijn tussen de kostenraming en de werkelijke kosten voor een productieorder. |
| Afwijking productievervanging | 510360 | Afwijking productievervanging | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt wanneer er onverwacht verbruik is voor een productieorder. |
| Afrondingsafwijking | 618160 | Afrondingsverschil | Onkosten | Of | Nr. | Vr | Niet van toepassing | Deze rekening wordt gebruikt wanneer er een afrondingsverschil is wanneer de productiekosten worden berekend op basis van de standaardkosten. |
