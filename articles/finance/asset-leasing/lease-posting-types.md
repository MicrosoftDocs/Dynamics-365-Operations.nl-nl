---
title: Boekingstypen voor lease
description: In dit onderwerp worden de boekingstypen beschreven die worden gebruikt voor activa-leasingtransacties.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 721463000c05eb1774335ccce1af39468c2aed9f179e5e88d8725f4d265d6870
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718242"
---
# <a name="lease-posting-types"></a>Boekingstypen voor lease

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de boekingstypen beschreven die worden gebruikt voor activa-leasingtransacties.

## <a name="lease-asset"></a>Leaseactivum

De rekening is gekoppeld aan het RoU-activum (activum met gebruiksrecht). Deze rekening wordt gedebiteerd wanneer een lease in eerste instantie wordt toegerekend onder de nieuwe boekhoudstandaarden voor leases, Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16). Voor een gewijzigde lease kan deze rekening worden gedebiteerd of gecrediteerd, afhankelijk van het feit of de leaseverplichtingen door de wijziging worden verhoogd of verlaagd.

**Voorbeeldjournaalposten:** eerste toerekening<br>
**Debet:** leaseactiva XXX<br>
**Credit:** leaseverplichtingen XXX

## <a name="lease-liability"></a>Leaseverplichting

De rekening is gekoppeld aan de leaseverplichtingen die zich voordoen wanneer betalingen worden verdisconteerd onder de nieuwe IFRS 16- en ASC 842-standaarden. Deze rekening wordt gecrediteerd wanneer een lease in eerste instantie wordt toegerekend onder de nieuwe standaarden. Deze wordt gedebiteerd voor leasebetalingen en gecrediteerd voor rentetoerekeningen.

**Voorbeeldjournaalposten:** eerste toerekening<br>
**Debet:** leaseactiva XXX<br>
**Credit:** leaseverplichtingen XXX

**Voorbeeldjournaalposten:** rentetoerekening<br>
**Debet:** rentelasten XXX<br>
**Credit:** leaseverplichtingen XXX

**Voorbeeldjournaalposten:** leasebetaling<br>
**Debet:** leaseverplichtingen XXX<br>
**Credit:** te betalen leverancier/leasebetaling XXX

## <a name="short-term-lease-liability"></a>Kortlopende leaseverplichtingen

De rekening is gekoppeld aan de kortlopende leaseverplichtingen wanneer de herclassificatiejournaalpost voor de kortlopende leaseverplichtingen wordt geboekt. Deze rekening wordt gecrediteerd voor de kortlopende verplichtingen van de aflossingsplanning op de laatste dag van de maand. Hetzelfde bedrag wordt echter op de eerste dag van de volgende maand gedebiteerd.

**Voorbeeldjournaalposten:** herclassificatie kortlopende leaseverplichtingen<br>
**Debet:** leaseverplichtingen XXX<br>
**Credit:** kortlopende leaseverplichtingen XXX<br>
**Debet:** kortlopende leaseverplichtingen XXX<br>
**Credit:** leaseverplichtingen XXX

## <a name="depreciation-expense"></a>Afschrijvingskosten

De rekening is gekoppeld aan de kosten die zijn gerelateerd aan de afschrijving van het RoU-activum onder IFRS 16, ASC 842 en financiële leases overeenkomstig IAS 17 en ASC 840. Deze rekening wordt gedebiteerd wanneer een RoU-activum elke maand wordt afgeschreven.

**Voorbeeldjournaalposten:** afschrijvingstoerekening<br>
**Debet:** afschrijvingskosten XXX<br>
**Credit:** samengevoegde afschrijving XXX

## <a name="gainloss-on-lease-modification"></a>Winst/verlies bij wijziging van lease

De rekening is gekoppeld aan winsten of verliezen die voortvloeien uit leasewijzigingen. Er kan een winst ontstaan tijdens een leasewijziging als de wijziging de leaseverplichtingen vermindert met een bedrag dat hoger is dan de boekwaarde van het RoU-activum.

Een lease heeft bijvoorbeeld een actuele boekwaarde van de leaseverplichtingen van $ 150.000 en een boekwaarde van het RoU-activum van $ 100.000. De lease wordt gewijzigd en deze wijziging produceert een nieuwe huidige waarde van de toekomstige minimale leasebetalingen (PVFMLP) van $ 40.000. Daarom worden de leaseverplichtingen gedebiteerd met $ 110.000 ($ 150.000 – $ 40.000). Omdat het RoU-activum slechts $ 100.000 is, zal de verlaging van $ 110.000 het activum voorbij 0 (nul) verlagen. Daarom wordt in de boekhoudingsrichtlijnen aangegeven dat het restant moet worden geboekt op een winstrekening. In dit geval is de definitieve journaalpost een debet voor de leaseverplichtingen voor $ 110.000, een credit voor het leaseactivum voor $ 100.000 en een credit voor de winstrekening voor $ 10.000.

**Voorbeeldjournaalposten:** leasewijziging<br>
**Debet:** leaseverplichtingen XXX<br>
**Credit:** leaseactivum XXX<br>
**Credit:** winst XXX

## <a name="accumulated-depreciation"></a>Samengevoegde afschrijving

De rekening is gekoppeld aan de contra-activumrekening van het RoU-activum. Deze rekening wordt gecrediteerd wanneer afschrijvingskosten worden geboekt.

**Voorbeeldjournaalposten:** afschrijvingstoerekening<br>
**Debet:** afschrijvingskosten XXX<br>
**Credit:** samengevoegde afschrijving XXX

## <a name="variable-payment"></a>Variabele betaling

De rekening is gekoppeld aan variabele leasebetalingen die worden geproduceerd door een herwaardering van de index onder ASC 842, ASC 840 en IAS 17 leases. In het leasebetalingsschema worden variabele betalingen opgenomen in de kolom **Variabele betaling**. Deze rekening wordt gedebiteerd wanneer er een factuur wordt gemaakt op basis van een betalingsschemaregel die een variabele betaling bevat.

**Voorbeeldjournaalposten:** leasebetaling<br>
**Debet:** leaseverplichtingen XXX<br>
**Debet:** variabele betaling XXX<br>
**Credit:** te betalen leverancier/leasebetaling XXX

## <a name="deferred-rent-asset-liability"></a>Activum uitgestelde gebruiksvergoeding (verplichtingen)

De rekening is gekoppeld aan het activum uitgestelde gebruiksvergoeding of de verplichting die wordt geproduceerd door een lease behandeling uitgestelde gebruiksvergoeding. Deze rekening wordt gedebiteerd wanneer een factuur wordt geboekt voor een lease behandeling uitgestelde gebruiksvergoeding, als het bedrag van de leasebetaling hoger is dan de lineaire gebruiksvergoeding van de periode. Het wordt gecrediteerd als de leasebetaling kleiner is dan de lineaire gebruiksvergoeding van de periode.

**Voorbeeldjournaalposten:** leasebetaling (lease behandeling uitgestelde gebruiksvergoeding)<br>
**Debet:** leasekosten XXX<br>
**Credit:** verplichtingen uitgestelde gebruiksvergoeding XXX<br>
**Credit:** te betalen leverancier/leasebetaling XXX

## <a name="lease-expense"></a>Onkosten van lease

De rekening is gekoppeld aan de leasekosten als de lease wordt geclassificeerd als een lease behandeling uitgestelde gebruiksvergoeding. Deze rekening wordt gedebiteerd wanneer een factuur wordt geboekt voor een lease behandeling uitgestelde gebruiksvergoeding.

**Voorbeeldjournaalposten:** leasebetaling (lease behandeling uitgestelde gebruiksvergoeding)<br>
**Debet:** leasekosten XXX<br>
**Credit:** verplichtingen uitgestelde gebruiksvergoeding XXX<br>
**Credit:** te betalen leverancier/leasebetaling XXX

## <a name="impairment-expense"></a>Waardeverminderingskosten

De rekening wordt tegen geboekt wanneer een lease een waardevermindering heeft ondergaan. Deze rekening wordt gedebiteerd, terwijl de RoU-activumrekening rechtstreeks wordt gecrediteerd.

**Voorbeeldjournaalposten:** leasebetaling<br>
**Debet:** kosten waardevermindering XXX<br>
**Credit:** RoU-activum XXX

## <a name="lease-payment"></a>Leasebetaling

De rekening wordt tegengeboekt als de parameter **Betaling aan leverancier** is uitgeschakeld. Deze rekening wordt gecrediteerd in plaats van de te betalen leverancier als de parameter is uitgeschakeld.

**Voorbeeldjournaalposten:** leasebetaling<br>
**Debet:** leaseverplichtingen XXX<br>
**Credit:** leasebetaling XXX

## <a name="expense-type-postings"></a>Boekingen onkostentypen

De rekening die is geselecteerd voor elk onkostentype wordt gedebiteerd wanneer er een betaling voor dat onkostentype wordt gegenereerd. De rekening die is opgegeven voor het onkostentype **Verzekering** bijvoorbeeld wordt gedebiteerd wanneer er een factuur- of betalingsjournaalpost wordt gemaakt van het schema administratieve kosten voor verzekeringskosten.

**Voorbeeldjournaalposten:** verzekeringsbetaling<br>
**Debet:** rekening onkostentype verzekering XXX<br>
**Credit:** tegenrekening XXX

> [!NOTE]
> De tegenrekening wordt geselecteerd op het leaseniveau op de regels voor het betalingsschema administratieve kosten. Deze tegenrekening kan aan de leverancier of aan een grootboekrekening zijn gekoppeld.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
