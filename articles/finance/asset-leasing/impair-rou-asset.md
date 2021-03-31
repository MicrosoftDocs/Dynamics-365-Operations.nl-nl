---
title: Waarde van activa met gebruiksrecht verminderen
description: In dit onderwerp wordt de functionaliteit beschreven waarmee een waardevermindering wordt vastgelegd en het schema van de activa-afschrijving van een Accounting Standards Codification Topic 842 (ASC 842) operationele lease wordt aangepast.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b648075a681fb01720149aac4f479dccf963489
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229521"
---
# <a name="impair-right-of-use-assets"></a>Waarde van activa met gebruiksrecht verminderen

[!include [banner](../includes/banner.md)]

Als de boekwaarde van een activum met gebruiksrecht (RoU-activum) niet terugvorderbaar is, moet u mogelijk testen of de waarde van het activum is verminderd. Als u vaststelt dat de waarde van het activum is verminderd, kan Activa leasen de waardevermindering vastleggen en het afschrijvingsschema dienovereenkomstig aanpassen. In dit onderwerp wordt de functionaliteit beschreven waarmee de waardevermindering wordt vastgelegd en het afschrijvingsschema van een Accounting Standards Codification Topic 842 (ASC 842) operationele lease wordt aangepast. Dezelfde methode geldt ook voor International Financial Reporting Standard 16 (IFRS 16)-leases.

Het resterende saldo van het RoU-activum wordt lineair afgeschreven voor het aantal perioden dat overblijft, ongeacht of de lease was geclassificeerd als financiële lease onder IFRS 16 of een operationele lease onder ASC 842.

## <a name="impair-an-rou-asset"></a>De waarde van een RoU-activum verminderen

1. Ga naar de lease met de verminderde waarde en selecteer **Boeken**.
2. Selecteer in het actievenster **Waardevermindering**.
3. Voer in het dialoogvenster dat verschijnt in het veld **Bedrag waardevermindering** het bedrag van de waardevermindering in. Als u het RoU-activum wilt verlagen, moet u een positieve waarde invoeren.
4. Voer in het veld **Transactiedatum** de datum in waarop de waardeverminderingspost moet worden geboekt.
5. Voer in het veld **Resterende perioden** het resterende aantal maanden in dat moet worden afgeschreven.
6. Schakel de parameter **Boeken** in als u de boeking van de onkostenjournaalpost voor waardevermindering automatisch door het systeem wilt laten boeken. Als u deze parameter uitgeschakeld laat, maakt het systeem de post maar wordt deze niet geboekt. U kunt de post vervolgens boeken vanuit de pagina **Activaleasejournalen**.
7. Stel de optie **Bekijken alvorens te boeken** in op **Ja** om de voorgestelde post weer te geven voordat deze wordt gemaakt of geboekt.
8. Stel de optie **Boek sluiten** in op **Ja** om het leaseboek te sluiten. Deze actie kan niet ongedaan worden gemaakt. Posten kunnen niet worden geboekt voor gesloten leases en gesloten leases kunnen niet worden gecorrigeerd.
9. Klik op **OK** om de waardeverminderingspost te maken of te boeken.
10. Als u het afschrijvingsschema voor activa met een verminderde waarde wilt weergeven, opent u het schema voor activa-afschrijvingen voor dat leaseboek. Het activum wordt nu op lineaire basis afgeschreven over het aantal maanden dat u hebt ingevoerd in het veld **Resterende perioden**.
11. Als u de journaalpost voor waardeverminderingskosten wilt weergeven, selecteert u **lActivaleasejournalen** in het actievenster van het boek voor leases met de verminderde waarde. Het systeem maakt een journaalpost die de boekingsrekening waardeverminderingsonkosten debiteert en de boekingsrekening voor de leaseactiva crediteert.
12. Als u de nieuwe boekwaarde van het RoU-activum wilt weergeven, selecteert u **Activatransacties** in het actievenster van het leaseboek.

## <a name="example-of-rou-asset-impairment"></a>Voorbeeld van waardevermindering RoU-activum

Voor dit voorbeeld is de lease een niet-gespecialiseerd activum dat geen eigendom overdraagt of de leasenemer de mogelijkheid geeft te kopen.

### <a name="setup"></a>Instelling

In de volgende tabellen ziet u de waarden die zijn ingesteld op de tabbladen **Algemeen** en **Betalingsschemaregels** voor de lease die in dit voorbeeld wordt gebruikt.

**Tabblad Algemeen**

| Veld                      | Waarde            |
|----------------------------|------------------|
| Reële waarde van het activum    | 600,000          |
| Verhoogd leningtarief | 7%               |
| Samenstellingsinterval       | Jaarlijks         |
| Economische levensduur activum (maanden) | 600              |
| Type annuïteit               | Normale annuïteit |
| Begindatum          | 01-01-2019       |

**Tabblad Regels van betalingsschema**

| Veld             | Waarde      |
|-------------------|------------|
| Begindatum        | 01-01-2019   |
| Periode-interval   | Maandelijks    |
| Perioden           | 120        |
| Einddatum          | 31-12-2028 |
| Betalingsfrequentie | Jaarlijks   |
| Betalingsbedrag    | 10,000     |

### <a name="steps"></a>Stappen

1. Nadat u de lease hebt gemaakt zoals eerder in dit onderwerp is beschreven, gaat u naar het leaseboek en bevestigt u het betalingsschema. Boek vervolgens de eerste journaalpost voor toerekening. Het initiële RoU-activum en de leaseverplichtingen moeten $ 70.235,81 zijn. Voor dit voorbeeld is de lease geclassificeerd als operationele lease onder ASC 842.
2. Voer het batchjournaalproces drie keer uit om de doorloop van drie jaar te simuleren voor de leasebetalingen, rentelasten en afschrijvingskosten.
3. Nadat u alle drie de batchtaken hebt uitgevoerd, gaat u terug naar het leaseboek en opent u de tabellen verplichtingen en activumtransacties om de huidige boekwaarde van het RoU-activum en leaseverplichtingen weer te geven. Na drie jaar moet de waarde van de verplichtingen ongeveer € -53.893,00 zijn en de waarde van het activum ongeveer $ 53.893,00. 

    Na drie jaar worden door het bedrijf waardeverminderingstests uitgevoerd en wordt vastgesteld dat het RoU-activum een waardevermindering heeft van $ 35.000. U moet nu deze waardevermindering vastleggen.
    
4. Ga naar het leaseboek en selecteer in het actievenster **Waardevermindering**.
5. Voer op de pagina **Parameter voor waardevermindering** de volgende details in.

    | Veld                  | Waarde    |
    |------------------------|----------|
    | Bedrag van waardevermindering      | 35,000   |
    | Transactiedatum       | 1-1-2022 |
    | Resterende perioden      | 84       |
    | Plaatsen                   | Ja      |
    | Bekijken alvorens te boeken | No       |
    | Boek sluiten             | No       |

6. Een journaalpost met waardeverminderingskosten is gemaakt en geboekt. Als u deze wilt weergeven, gaat u naar het leasingjournaal van het activum in het leaseboek. Het bedrag van de waardevermindering is gedebiteerd op de boekingsrekening onkosten waardevermindering en de boekingsrekening RoU-activum is gecrediteerd.
7. Ga naar de tabellen verplichtingen en activumtransacties om het netto-effect van de waardevermindering te bekijken. De waardeverminderingskosten hebben het RoU-activum verlaagd, maar de boekwaarde van de leaseverplichtingen is niet gewijzigd.

De waardevermindering heeft een ander effect waaraan u aandacht moet schenken. Omdat het bedrag van het RoU-activum nu veel kleiner is dan de leaseverplichtingen, moet het bedrag anders worden afgeschreven dan eerder. Het activum wordt nu op lineaire wijze afgeschreven gedurende de resterende 84 maanden van de lease, te beginnen op de transactiedatum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]