---
title: Leaseboeken instellen
description: In dit onderwerp wordt de informatie beschreven die in leaseboeken wordt bijgehouden. Leaseboeken bevatten de boekhoudbeleidsregels die bepalen hoe een lease wordt verwerkt in het systeem.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442161"
---
# <a name="set-up-lease-books"></a>Leaseboeken instellen

[!include [banner](../includes/banner.md)]

Leaseboeken bevatten de boekhoudbeleidsregels die bepalen hoe een lease wordt verwerkt in het systeem. Behalve boekhouden op basis van contante betaling, ondersteunt Activa leasen de volgende standaarden:

- Algemeen geaccepteerde boekhoudprincipes in de Verenigde Staten (VS GAAP)
- Accounting Standards Codification Topic 842 (ASC 842)
- ASC 840
- International Financial Reporting Standard 16 (IFRS 16)
- International Accounting Standard 17 (IAS 17)

Volg deze stappen om een nieuw leaseboek te maken.

1. Ga naar **Activa leasen \> Instellen \> Leaseboeken**.
2. Selecteer **Nieuw** om een boek toe te voegen.
3. Stel de volgende velden in.

    | Naam                                     | Beschrijving |
    |------------------------------------------|-------------|
    | Boekingslaag                            | Selecteer de boekingslaag die moet worden gebruikt. Elk boek dat aan een lease is gekoppeld, wordt ingesteld voor een bepaalde boekingslaag. Elke boekingslaag heeft verschillende boekingsdoeleinden. |
    | Leasetype                               | Selecteer of de lease automatisch moet worden geclassificeerd of dat deze vooraf moet worden gedefinieerd als een financiële of operationele lease. |
    | Boekhoudraamwerk                     | Selecteer het kader dat is gekoppeld aan het boek. |
    | Leasetermijn/economische levensduur instellen          | De lease wordt door het systeem geclassificeerd als een financiële lease als het leasetype is ingesteld op **Automatisch** en als de leasetermijn voor de economische levensduur van het activum groter is dan of gelijk is aan het percentage dat is ingevoerd in dit veld.  |
    | Huidige waarde/reële waarde van activum instellen   | Voer een geheel getal in om de drempel te definiëren waarmee het leasetype wordt bepaald. Als de huidige waarde van de toekomstige minimale leasebetalingen meer is dan de door de gebruiker gedefinieerde waarde in de boekinstelling, en als de leaseclassificatie van het boek is ingesteld op automatisch, wordt de lease door het systeem geclassificeerd als een financiële lease. |
    | Drempel voor de korte termijn                     | Voer het aantal maanden in dat moet worden gebruikt als drempel voor leases op korte termijn. Als de leaseperiode kleiner is dan of gelijk is aan het aantal maanden dat u hier invoert, wordt de lease door het systeem geclassificeerd als een lease op korte termijn en wordt de behandeling uitgestelde gebruiksvergoeding toegepast. |
    | Drempel voor geringe waarde                      | Voer een bedrag in dat u wilt gebruiken als drempelwaarde voor leases met geringe waarde. Als de reële waarde van het activum kleiner is dan of gelijk is aan de waarde die u hier invoert, wordt de lease door het systeem geclassificeerd als een lease met geringe waarde en wordt de behandeling uitgestelde gebruiksvergoeding toegepast. |
    | Betalen aan leverancier                            | Stel deze optie in op **Ja** als u wilt toestaan dat leasebetalingen als een factuur worden geboekt naar de leveranciersrekening die op elke lease is opgegeven. Wanneer een leasebetaling wordt geboekt, wordt de leveranciersrekening gecrediteerd. Als deze optie is ingesteld op **Nee**, wordt de rekening die is opgegeven voor het boekingstype **Leasebetaling** op de pagina **Leaseboekingsparameters** in plaats daarvan gecrediteerd. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]