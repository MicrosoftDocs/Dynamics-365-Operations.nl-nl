---
title: Geïntegreerd grootboek
description: In dit onderwerp wordt de integratie van grootboekgegevens tussen Finance and Operations en andere Dynamics 365-toepassingen via Dataverse beschreven.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e5bdef8ef440bd5ef84060b61b4cf1d0088f204c
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416828"
---
# <a name="integrated-ledger"></a>Geïntegreerd grootboek

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In een bedrijfstoepassing definiëren grootboekgegevens de basisinstelling van de manier waarop een bedrijf zaken doet. Zo beschreven grootboekgegevens bijvoorbeeld het fiscaal jaar dat het bedrijf volgt, de valuta's waarin het bedrijf handelt en de rekeningen die worden gebruikt. In dit onderwerp wordt de integratie van deze financiële kerngegevens beschreven.

## <a name="templates"></a>Sjablonen

Grootboekgegevens omvatten een verzameling financiële basistabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

Finance and Operations-apps | Customer Engagement-apps     | Beschrijving
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
