---
title: Voorstel voor leasebeëindiging
description: In dit onderwerp wordt uitgelegd hoe u een voorstel voor beëindiging van een lease opstelt.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ff3795f26ab10ac19cc3a0dd00dca65095118f45
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207298"
---
# <a name="propose-a-lease-for-termination"></a>Een lease voordragen voor beëindiging

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Als een lease voortijdig wordt beëindigd, kan bij Activa leasen een journaalboeking voor beëindiging worden gemaakt, zodat de leaseverplichtingen, het activum met gebruiksrecht (RoU-activum) en de geaccumuleerde afschrijving worden afgeschreven en de winst of het verlies wordt geboekt. Met het proces voor voortijdige beëindiging worden een lease en de bijbehorende leaseboeken beëindigd. Hiermee worden geen individuele leaseboeken beëindigd. In dit onderwerp wordt de functionaliteit beschreven waarmee u een lease kunt voordragen voor beëindiging en de vermelding in het lease-beëindigingsjournaal kunt verwerken.

Als een lease niet is geclassificeerd als een lease voor uitgestelde gebruiksvergoeding en niet is gekoppeld aan een vast activum, wordt de volgende journaalinvoer geproduceerd.

| Transactie                           | Debet (Dr.) | Credit (Cr.) |
|---------------------------------------|-------------|--------------|
| Leaseverplichting Dr.                   | X           |              |
| Samengevoegde afschrijving Dr.          | X           |              |
| Winst/verlies bij wijziging van lease Dr. | X           |              |
| Leaseactivum Cr.                       |             | X            |
| Winst/verlies bij wijziging van lease Cr. |             | X            |

Als het leaseboek is geclassificeerd als een boek voor uitgestelde gebruiksvergoeding, wordt het saldo van de uitgestelde gebruiksvergoeding vóór de beëindiging afgeschreven naar de winst- of verliesrekening, zoals hier wordt weergegeven.

| Transactie                           | Debet (Dr.) | Credit (Cr.) | 
|---------------------------------------|-------------|--------------|
| Uitgestelde gebruiksvergoeding Dr.                     | X           |              |
| Winst/verlies bij wijziging van lease Cr. |             | X            |
| Uitgestelde gebruiksvergoeding Cr.                     |             | X            |
| Winst/verlies bij wijziging van lease Dr. | X           |              |

Als het leaseboek aan een vast activum is gekoppeld, wordt het RoU-activum in Vaste activa verantwoord. Deze boekhouding omvat de boekhouding voor voortijdige beëindigingen. Bij het leasen van activa wordt de volgende journaalinvoer geproduceerd om de leaseverplichtingen af te schrijven.

| Transactie                           | Debet (Dr.) | Credit (Cr.) |
|---------------------------------------|-------------|--------------|
| Leaseverplichting Dr.                   | X           |              |
| Winst/verlies bij wijziging van lease Cr. |             | X            |

Informatie over de juiste manier om een RoU-activum af te stoten vindt u in [Buiten gebruik gestelde vaste activa als uitval afstoten](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Een lease voordragen voor beëindiging

1. Ga naar de lease die u wilt beëindigen en selecteer in het actievenster de optie **Beëindigingsvoorstel**.

    > [!NOTE]
    > De knop **Beëindigingsvoorstel** is niet beschikbaar als er niet-geboekte journaalposten zijn voor een van de boeken. Voordat u de lease kunt beëindigen, moet u journaalposten die voor de lease zijn gemaakt, boeken of verwijderen.

2. Stel in het dialoogvenster dat verschijnt de velden **Ingangsdatum** en **Boekingsdatum** voor de journaalboeking voor beëindiging in.
3. Selecteer **Beëindigingsvoorstel** om de lease voor te dragen voor beëindiging.
4. Selecteer **Leasebeëindiging boeken** om automatisch de journaalboeking voor leasebeëindiging te boeken.
5. Selecteer op de pagina **Leasebeëindigingen** de lease-id van de lease die u hebt voorgedragen om de regels voor de beëindiging te bekijken. In de beëindigingsregels ziet u de boekwaarde van het RoU-activum, de leaseverplichtingen, de samengevoegde afschrijving, uitgestelde gebruiksvergoeding (indien van toepassing) en winst of verlies dat moet worden verantwoord bij het beëindiging van de lease.

De lease is nu klaar om te worden beëindigd. De waarde van het veld **Beëindigingsstatus** voor het leaseboek wordt gewijzigd in **Gereed voor beëindiging**. Op dit moment kunt u geen journaalposten meer plaatsen voor de lease of deze aanpassen of de waarde ervan verminderen. 

## <a name="process-leases-that-are-ready-for-termination"></a>Leases verwerken die gereed zijn om te worden beëindiging

Als u leases wilt verwerken die gereed zijn voor beëindiging en de journaalpost voor beëindiging wilt maken, volgt u deze stappen.

1. Selecteer op de pagina **Leasebeëindiging** de lease die u wilt verwerken en selecteer vervolgens **Beëindigen**.
2. Selecteer in het dialoogvenster dat verschijnt **OK**.

De journaalboeking voor het beëindigen wordt geboekt. Het veld **Leasestatus** voor het leaseboek wordt ingesteld op **Beëindigd** en het veld **Status beëindigingsvoorstel** wordt ingesteld op **Voltooid**.

## <a name="reverse-a-lease-termination"></a>Een leasebeëindiging ongedaan maken

Volg deze stap om een journaalboeking voor leasebeëindiging ongedaan te maken en een beëindigde lease te openen.

- Selecteer op de pagina **Leasebeëindiging** de beëindigde lease die u ongedaan wilt maken en selecteer vervolgens **Beëindiging ongedaan maken**.

De journaalboeking voor het beëindigen wordt ongedaan gemaakt. Het veld **Leasestatus** voor het leaseboek wordt ingesteld op **Open**. De lease wordt niet meer weergegeven op de pagina **Leasebeëindigingen** en kan opnieuw worden voorgesteld voor beëindiging.

## <a name="example-of-a-lease-termination"></a>Voorbeeld van het beëindigen van een lease

Voor dit voorbeeld is de lease gekoppeld aan een niet-gespecialiseerd activum en draagt de lease geen eigendom over en geeft de leasenemer niet de mogelijkheid het activum te kopen.

### <a name="setup"></a>Instelling

In de volgende tabellen ziet u de waarden die zijn ingesteld op de tabbladen **Algemeen** en **Betalingsschemaregels** voor de lease die in dit voorbeeld wordt gebruikt.

**Tabblad Algemeen**

| Veld                      | Waarde            |
|----------------------------|------------------|
| Reële waarde van het activum    | 600,000          |
| Valuta                   | USD              |
| Initiële directe kosten       | 1.000            |
| Verhoogd leningtarief | 7%               |
| Samenstellingsinterval       | Jaarlijks         |
| Economische levensduur activum (maanden) | 600              |
| Type annuïteit               | Normale annuïteit |
| Begindatum          | 01-01-2019         |

**Tabblad Regels van betalingsschema**

| Veld             | Waarde      |
|-------------------|------------|
| Begindatum        | 01-01-2019   |
| Periode-interval   | Maandelijks    |
| Perioden           | 120        |
| Einddatum          | 31-12-2028 |
| Betalingsfrequentie | Jaarlijks   |
| Betalingsbedrag    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Stappen voor het beëindigen van de lease

1. Nadat u de lease hebt gemaakt zoals eerder in dit onderwerp is beschreven, gaat u naar het leaseboek en bevestigt u het betalingsschema. Boek vervolgens de eerste journaalpost voor toerekening. Het initiële RoU-activum is $71,235.81 en de leaseverplichtingen moeten $70.235,81 zijn. Voor dit voorbeeld is de lease geclassificeerd als operationele lease onder Accounting Standards Codification Topic 842 (ASC 842).
2. Voer het batchjournaalproces drie keer uit om de doorloop van drie jaar te simuleren voor de leasebetalingen, rentelasten en afschrijvingskosten.
3. Nadat u alle drie de batchtaken hebt uitgevoerd, gaat u terug naar het leaseboek en opent u de tabellen Verplichtingen en Activumtransacties om de huidige boekwaarde van het RoU-activum en leaseverplichtingen weer te geven. Na drie jaar moet de waarde van de verplichtingen ongeveer € -53.893,00 zijn en de waarde van het activum ongeveer $ 54.593,00.

    Nadat deze drie jaar zijn verstreken, gaan het bedrijf en de leaseverstrekker gezamenlijk akkoord om de lease te beëindigen. Daarom moet u de lease nu beëindigen.

4. Ga naar de lease die u wilt beëindigen en selecteer in het actievenster de optie **Beëindigingsvoorstel**. 
5. Voer in het volgende dialoogvenster in het veld **Begindatum** en **Boekingsdatum** **1-1-2021** in.
6. Selecteer **Beëindigingsvoorstel** om de lease voor te dragen voor beëindiging.

    De pagina **Leasebeëindiging** wordt geopend met de lease die u wilt beëindigen.

7. Selecteer de lease-id van de lease die u hebt voorgedragen om de regels voor de beëindiging te bekijken. Op de beëindigingsregels wordt de boekwaarde van de lease vermeld. In de volgende tabel ziet u wat deze waarden in dit voorbeeld moeten zijn. 

    | Veld                                                 | Waarde      |
    |-------------------------------------------------------|------------|
    | Boekwaarde van verplichtingen in de transactievaluta | $53,892.89 |
    | RoU-activum in de transactievaluta            | $71,235.81 |
    | Geaccumuleerde afschrijving in de transactievaluta      | $16,642.92 |
    | Winst (verlies) in de transactievaluta                   | $-700,00   |

8. Om de journaalboeking voor de beëindiging te boeken, selecteert u de lease op de pagina **Leasebeëindiging** en vervolgens **Beëindigen**.
9. Selecteer in het dialoogvenster dat verschijnt **OK**.
10. Als u de journaalboeking voor beëindiging wilt weergeven die is gemaakt en geboekt, gaat u naar het leasejournaal van het activum in het leaseboek. In de volgende tabel ziet u wat deze boeking in dit voorbeeld moeten zijn.

    | Transactie                           | Debet (Dr.) | Credit (Cr.) |
    |---------------------------------------|-------------|--------------|
    | Leaseverplichting Dr.                   | 53,892.89   |              |
    | Samengevoegde afschrijving Dr.          | 16,642.92   |              |
    | Winst/verlies bij wijziging van lease Dr. | 700.00      |              |
    | Leaseactivum Cr.                       |             | 71,235.81    |

11. Als u het nettoeffect wilt bekijken van de beëindiging, waarbij het RoU-activum en de leaseverplichtingen 0 (nul) zijn, opent u de tabellen Verplichtingen en Activumtransacties.

De leasestatus moet nu **Beëindigd** zijn. Er worden geen journaalboekingen meer geboekt op deze lease tenzij, de beëindiging ongedaan wordt gemaakt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]