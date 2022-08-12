---
title: Geïntegreerd grootboek
description: In dit artikel wordt de integratie van grootboekgegevens tussen apps voor financiën en bedrijfsactiviteiten en andere Dynamics 365-toepassingen via Dataverse beschreven.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e5598295a25e31b33cd8b4d7ce3250a982ab4e87
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112235"
---
# <a name="integrated-ledger"></a>Geïntegreerd grootboek

[!include [banner](../../includes/banner.md)]



In een bedrijfstoepassing definiëren grootboekgegevens de basisinstelling van de manier waarop een bedrijf zaken doet. Zo beschreven grootboekgegevens bijvoorbeeld het fiscaal jaar dat het bedrijf volgt, de valuta's waarin het bedrijf handelt en de rekeningen die worden gebruikt. In dit artikel wordt de integratie van deze financiële kerngegevens beschreven.

## <a name="templates"></a>Sjablonen

Grootboekgegevens omvatten een verzameling financiële basistabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

Apps voor financiën en bedrijfsactiviteiten | Customer Engagement-apps     | Beschrijving
---------------------------------|----------------------------------|------------
[Wisselkoersen CDS](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Rekeningschema](mapping-reference.md#121) | msdyn_chartofaccountses |
[Valuta's](mapping-reference.md#218) | transactioncurrencies |
[Valutapaar wisselkoers](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Wisselkoerstype](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Indeling van financiële dimensie](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Financiële dimensies](mapping-reference.md#128) | msdyn_dimensionattributes |
[Integratie entiteit fiscale kalender](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Fiscale kalenderperiode](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Integratie entiteit fiscaal kalenderjaar](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Hoofdrekening](mapping-reference.md#152) | msdyn_mainaccounts |
[Categorieën van hoofdrekening](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

