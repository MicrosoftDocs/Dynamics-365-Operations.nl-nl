---
title: Importindeling voor consolidatie
description: Dit onderwerp bevat gedetailleerde informatie over de importindeling die wordt gebruikt wanneer u financiële gegevens van meerdere rechtspersonen consolideert.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 714c34dfcd109a442a4ecd741409dea5c4aade20
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216801"
---
# <a name="import-format-for-consolidation"></a>Importindeling voor consolidatie

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat gedetailleerde informatie over de importindeling die wordt gebruikt wanneer u financiële gegevens van meerdere rechtspersonen consolideert. De importindeling moet als tekstbestand (.txt) worden opgeslagen.

## <a name="import-format"></a>Importindeling

In de volgende tabel wordt de importindeling vermeld die u moet gebruiken bij het consolideren tijdens het importeren.

| Recordtabel | Format | Opmerkingen |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>De recordtabel</li><li>De id van de hoofdrekening van de bron</li><li>De hoofdrekeningsregel</li><li>Het hoofdrekeningtype</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>De hoofdrekening-id</li><li>De transactiedatum</li><li>Het type boekperiode (**0** = Openen, **1** = Operationeel en **2** = Afsluiting)</li><li>De transactievaluta</li><li>Debet of credit (**0** = Debet en **1** = Credit)</li><li>De boekingslaag</li><li>Transactiebedragen</li><li>Hoeveelheid</li><li>De lokale RecID (dubbelzinnige, unieke int64-waarde voor de transactie)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Het invoernummer (transactienummer van budgetkoptekst)</li><li>De standaarddatum van de budgetkoptekst</li><li>De budgetmodel-id</li><li>Budgettype (**1** - Oorspronkelijk budget, **2** - Overboeking, **3** - Revisie, **4** - Vordering, **5** - Voorvordering, **6** - Overgeboekt budget, **7** - Project, **8** - Vaste activa, **9** - Vraagprognose, **10** - Aanbodprognose, **11** - Toewijzingen, **12** - Voorlopig budget.)</li><li>De datum van de regel</li><li>De hoofdrekening-id voor de regel</li><li>De valutacode voor de regel</li><li>Het bedrag voor de regel, in de transactievaluta</li><li>De waarde (geheel getal) van de opsomming voor het budgettype voor de regel (onkosten of opbrengst)</li></ul> |
| 4            | DEMF | RecordCompany is de rechtspersoon Bron. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Hoofdrekening-ID</li><li>Transactiedatum</li><li>Het type boekperiode (0 Openen, 1 Operationeel en 2 Afsluiting)</li><li>Transactievaluta</li><li>Debet of credit (0 voor Debet en 1 voor Credit)</li><li>Boekingslaag</li><li>Transactiebedrag</li><li>Hoeveelheid</li><li>De lokale RecID (dubbelzinnige, unieke int64-waarde voor de transactie)</li></ul>  |
| 6            | Bedrijfseenheid, 1 Afdeling, 2 | De kenmerken van financiële dimensies die in de segmentvolgorde zijn gedefinieerd.<p>U kunt de pagina **Exporteren** gebruiken om te controleren hoe de kenmerken zijn gedefinieerd.</p> |
| 7            | 002,1,658 | <ul><li>De waarde van financiële dimensie</li><li>De financiële dimensie, als de index die wordt geleverd in RecordDimensions</li><li>Een dubbelzinnige, unieke record-id die gekoppeld is aan de unieke record-id van RecordTrans of RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensiewaarden die aan de transactie zijn gekoppeld vanuit Recordbudget</li><li>De financiële dimensie, als de index die wordt geleverd in RecordDimensions</li><li>Een dubbelzinnige regelrecord-ID die is afgestemd op de volgorde van de transactieregels in het bestand</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
