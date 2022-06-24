---
title: Sjabloon voor gesplitste opbrengst in facturering van abonnementen
description: In dit artikel wordt uitgelegd hoe u sjablonen voor het splitsen van opbrengsten kunt instellen voor artikelen die als bundels worden verkocht.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904754"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Sjabloon voor gesplitste opbrengst in facturering van abonnementen

Op de pagina **Sjabloon met gesplitste opbrengst** kunt u sjablonen instellen voor het splitsen van opbrengsten. Opbrengstsplitsing omvat een bovenliggend artikel met onderliggende artikelen. Dit artikeltype wordt vaak als één enkel artikel of bundel aan klanten verkocht.

Een computerartikel kan bijvoorbeeld op de volgende manier worden gemaakt:

- **Bovenliggend artikel:** Abonnement Zilver
- **Regelartikelen (onderliggende artikelen):**

    - Ondersteuning
    - Onderhoud
    - Licentie

Wanneer u een bovenliggend artikel maakt, moet u rekening houden met de volgende beperkingen:

- Een artikel kan slechts één keer als een bovenliggend artikel worden opgegeven.
- Het bovenliggende artikel kan worden geselecteerd als onderliggend artikel in dezelfde sjabloon.
- Voor een geldige sjabloon is minimaal één onderliggend artikel vereist.
- Een artikel kan als onderliggend artikel voor meer dan één bundelartikel worden opgegeven.
- Elke relatie bovenliggend-onderliggend moet uniek zijn.

## <a name="create-a-parent-item-that-has-child-items"></a>Een bovenliggend artikel met onderliggende artikelen maken

Volg de volgende stappen om een bovenliggend artikel met onderliggende artikelen te maken.

1. Selecteer op de pagina **Sjabloon met gesplitste opbrengst** de optie **Nieuw**.
1. Selecteer een bovenliggend artikel in het veld **Bovenliggend artikel**. Het veld **Variantnummer** wordt automatisch bijgewerkt. U kunt deze waarde zo nodig wijzigen.
1. Selecteer een toewijzingsmethode in het veld **Toewijzingsmethode**.
1. Selecteer in de lijst **Onderdeelartikelen** de optie **Toevoegen** om onderliggende artikelen toe te voegen.
1. Als u **Percentage** hebt geselecteerd in het veld **Toewijzingsmethode**, geef dan in het veld **Percentage** een percentage op.

    - Als u in het veld **Toewijzingsmethode** de waarde **Gelijk bedrag** hebt gekozen, wordt het veld **Percentage** automatisch bijgewerkt zodat elk artikel hetzelfde percentage heeft.
    - Als u in het veld **Toewijzingsmethode** de waarde **Variabel bedrag**, **Nulbedrag bovenliggend** of **Nulbedrag** hebt gekozen, blijft de waarde in het veld **Percentage** op **0** (nul) staan en kunt u dit niet wijzigen.

1. Selecteer **Opslaan**.

## <a name="fields"></a>Velden

De pagina **Sjabloon met gesplitste opbrengst** bevat de volgende velden.

| Veld | Description |
|-------|-------------|
| Bovenliggend artikel | Selecteer een artikelnummer. Dit artikel wordt het bovenliggende artikel voor het bundelartikel dat u maakt. |
| Productnaam | De productnaam. |
| Toewijzingsmethode | <p>Selecteer de toewijzingssmethode:</p><ul><li>**Gelijk bedrag**: de toewijzingspercentages worden automatisch berekend en gelijk verdeeld over alle artikelen in de sjabloon.</li><li>**Percentage**: u kunt een percentagebedrag opgeven voor de toewijzing. De som van alle percentages moet gelijk zijn aan 100.</li><li>**Variabel bedrag**: Onderliggende artikelen die worden toegevoegd, hebben een nettobedrag van 0 (nul). De prijs van de onderliggende artikelen moet worden opgegeven op het niveau van de transactie.</li><li>**Nulbedrag**: Het bovenliggende artikel behoudt de eenheidsprijs en het nettobedrag. Alle onderliggende artikelen hebben een nettobedrag van 0 (nul).</li><li>**Nulbedrag bovenliggend**: Het bovenliggende artikel heeft een vast nettobedrag van 0 (nul). Alle onderliggende artikelen worden behandeld als standaardartikelen. Er wordt niet gevalideerd of de som van de bedragen van onderliggende artikelen gelijk is aan het bedrag van het bovenliggende artikel.</li></ul> |
| **Onderdeelartikelen** | |
| Onderdeelartikel | Selecteer een artikelnummer. Dit artikel is een onderliggend artikel. |
| Variantnummer | Selecteer het variantnummer van het artikel. |
| Productnaam | De productnaam. |
| Percentage | <p>Het toewijzingspercentage voor de mijlpaal.</p><ul><li>Als het veld **Toewijzingsmethode** is ingesteld op **Percentage**, kunt u het percentage voor de regel opgeven.</li><li>Als het veld **Toewijzingsmethode** is ingesteld op **Gelijk bedrag**, wordt het percentage automatisch berekend zodat elk artikel in de sjabloon hetzelfde percentage krijgt toegewezen.</li><li>Als het veld **Toewijzingsmethode** is ingesteld op **Variabel bedrag**, **Nulbedrag bovenliggend** of **Nulbedrag**, is het percentage 0 (nul) en kunt u dit niet bewerken.</li></ul><p>De waarde van dit veld kan een positief getal zijn tussen 0 (nul) en 100. De som van alle percentages moet gelijk zijn aan 100.</p> |
| Totaal percentage | <p>De som van waarden in de kolom **Percentage**.</p><ul><li>Als het veld **Toewijzingsmethode** is ingesteld op **Gelijk bedrag** of **Percentage**, moet het totaal van alle percentages gelijk zijn aan 100.</li><li>Als het veld **Toewijzingsmethode** is ingesteld op **Variabel bedrag**, **Nulbedrag bovenliggend** of **Nulbedrag**, is het totale percentage 0 (nul).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Gesplitste opbrengst op een verkooporder

Volg deze stappen om een verkooporder te maken met een artikel dat is ingesteld voor gesplitste opbrengst.

1. Maak op de pagina **Verkooporder** een verkooporder.
2. Schakel het selectievakje **Gesplitste opbrengst** in op de regel voor elk artikel dat is ingesteld voor gesplitste opbrengst. Dat artikel wordt het bovenliggende artikel. Als de sjabloon al is geconfigureerd, worden de onderliggende artikelen automatisch in de lijst weergegeven.
3. Als u meer onderliggende artikelen wilt toevoegen, selecteert u **Onderliggende opbrengstsplitsing toevoegen** en selecteert u het onderliggende artikel dat u wilt toevoegen.
4. Sla de order op.

## <a name="revenue-split-with-billing-schedules"></a>Gesplitste opbrengst met factureringsplanningen

Volg deze stappen om een factureringsplanning te maken met een artikel dat is ingesteld voor gesplitste opbrengst.

1. Maak een factureringsplanning aan op de pagina **Alle/Actieve factureringsplanningen**.
2. Schakel het selectievakje **Gesplitste opbrengst** in op de regel voor elk artikel dat is ingesteld voor gesplitste opbrengst. Dat artikel wordt het bovenliggende artikel. Als de sjabloon al is geconfigureerd, worden de onderliggende artikelen automatisch in de lijst weergegeven.
3. Als u meer onderliggende artikelen wilt toevoegen, selecteert u **Onderliggende opbrengstsplitsing toevoegen** en selecteert u het onderliggende artikel dat u wilt toevoegen.
4. Ga door met de stappen voor het werken met het factureringsplanning.

> [!NOTE]
> Als de optie **Opbrengstsplitsing automatisch maken** is ingesteld op **Ja** op de pagina **Terugkerende contractfactureringsparameters**, worden de volgende acties uitgevoerd:
>
> - Als het regelartikel is ingesteld als het bovenliggende artikel in een sjabloon voor opbrengstsplitsing, wordt het selectievakje **Gesplitste opbrengst** automatisch ingeschakeld.
> - De onderliggende artikelen worden automatisch ingevoerd op de regel van de verkooporder of de factureringsplanning.
>
> Als de optie **Opbrengstsplitsing automatisch maken** splitsen is ingesteld op **Nee**, volgt het gedrag de eerdere uitleg.

## <a name="additional-revenue-split-information"></a>Aanvullende gegevens over opbrengstsplitsing

Wanneer u een artikel toevoegt dat onderdeel is van een opbrengstsplitsing, houd dan rekening met de volgende punten: 

- Het bovenliggende bedrag kan niet worden uitgesteld.
- De waarden voor begindatum, einddatum, hoeveelheid, eenheid, locatie en magazijn van onderliggende artikelen worden gebaseerd op het bovenliggende artikel. Deze waarden kunnen niet worden gewijzigd voor de onderliggende artikelen. Alle wijzigingen moeten in het bovenliggende artikel worden aangebracht. 
- De prijsmethode is **Vast** en kan niet worden gewijzigd.
- Onderliggende artikelen kunnen worden toegevoegd of verwijderd.
- Bovenliggende en onderliggende artikelen moeten dezelfde artikelengroep gebruiken. 
- Onderliggende artikelen kunnen een van de volgende instellingen hebben:

    - De velden **Factureringsfrequentie** en **Factureringsintervallen** worden ingesteld op dezelfde waarde als het bovenliggende artikel. 
    - Het veld **Factureringsfrequentie** wordt ingesteld op **Eenmalig**. In dit geval wordt het veld **Factureringsintervallen** automatisch ingesteld op **1**. 

- De som van de nettobedragen van de onderliggende artikelen is gelijk aan het bovenliggende bedrag. Als de toewijzingsmethode **Nulbedragen** is, zijn de som van de bedragen van de onderliggende artikelen en de som van het bovenliggende bedrag 0 (nul). 

    > [!NOTE]
    > Als de toewijzingsmethode **Nulbedrag bovenliggend** is, is de som (niet-nul) van de onderliggende artikelen niet gelijk aan het bovenliggende bedrag dat 0 (nul) is. Deze toewijzingsmethode wordt gebruikt voor interne doeleinden, zodat werknemers de onderliggende artikelen kunnen zien. Klanten kunnen echter alleen het bovenliggende artikel zien.

- Als het MEA-type (Multiple Element Arrangement) van de verkooporder **Enkel** is, wordt de bijbehorende transactieregel voor opbrengsttoewijzing met meerdere elementen gemaakt wanneer de bovenliggende en onderliggende artikelen worden toegevoegd. 
- Als de toewijzingsmethode voor een opbrengstsplitsing **Gelijke bedragen** is en het bovenliggende bedrag wordt gewijzigd, worden de bedragen opnieuw berekend voor alle onderliggende regels. 
- Voor een opbrengstsplitsing waarbij de toewijzingsmethode **Variabel bedrag** is, gebeurt het volgende:

    - Het nettobedrag van het bovenliggende artikel wordt weergegeven in de kolom **Bovenliggend bedrag**. Deze waarde kan worden bewerkt. De eenheidsprijs, het nettobedrag en de korting zijn echter 0 (nul) en kunnen niet worden bewerkt.
    - De eenheidsprijs van onderliggende artikelen is 0 (nul). U kunt de eenheidsprijs of het nettobedrag bewerken. Wanneer u één waarde bewerkt, wordt de andere waarde automatisch bijgewerkt.

- Voor een opbrengstsplitsing waarbij de toewijzingsmethode **Percentage** is, gebeurt het volgende:

    - Het nettobedrag van het bovenliggende artikel wordt weergegeven in de kolom **Bovenliggend bedrag**. Deze waarde kan worden bewerkt. De eenheidsprijs, het nettobedrag en de korting zijn echter 0 (nul) en kunnen niet worden bewerkt. 
    - Het nettobedrag van onderliggende artikelen wordt berekend als *Percentage* &times; *Bovenliggend bedrag*.

- Voor een opbrengstsplitsing waarbij de toewijzingsmethode **Gelijk bedrag** is, gebeurt het volgende:

    - Het nettobedrag van het bovenliggende artikel wordt weergegeven in de kolom **Bovenliggend bedrag**. Deze waarde kan worden bewerkt. De eenheidsprijs, het nettobedrag en de korting zijn echter 0 (nul) en kunnen niet worden bewerkt. 
    - Het nettobedrag van de onderliggende artikelen wordt berekend door het bovenliggende bedrag gelijkelijk te verdelen over alle onderliggende artikelen. 
    - Als onderliggende artikelen worden verwijderd of toegevoegd, worden het nettobedrag en de eenheidsprijzen opnieuw berekend, zodat alle onderliggende regels gelijke bedragen hebben. 
    - Als het bovenliggende bedrag niet gelijkelijk kan worden verdeeld, kan het nettobedrag en de eenheidsprijs van het laatste onderliggende artikel iets meer of minder zijn dan het nettobedrag en de eenheidsprijs van de andere onderliggende artikelen. 

- Voor een opbrengstsplitsing waarbij de toewijzingsmethode **Nulbedrag** is, gebeurt het volgende:

    - De eenheidsprijs, het nettobedrag en de korting kunnen worden bewerkt. Het bovenliggende bedrag is 0 (nul) en kan niet worden bewerkt. 
    - De waarden voor hoeveelheid, eenheid, locatie en magazijn van onderliggende artikelen worden gebaseerd op het bovenliggende artikel. U kunt deze waarden niet wijzigen voor de onderliggende artikelen. Alle wijzigingen moeten in het bovenliggende artikel worden aangebracht. 
    - De eenheidsprijs en nettoprijs van onderliggende artikelen is 0 (nul) en kan niet worden bewerkt. 

- Voor een opbrengstsplitsing waarbij de toewijzingsmethode **Nulbedrag bovenliggend** is, gebeurt het volgende:

    - De eenheidsprijs, het bovenliggende bedrag en het nettobedrag van het bovenliggende artikel zijn 0 (nul).
    - In een factureringsschema worden de onderliggende regels weergegeven alsof ze handmatig zijn toegevoegd, en worden alle waarden bijgewerkt op basis van de geselecteerde factureringsschemagroep. Deze waarden kunnen worden bewerkt. Voor onderliggende artikelen hebt u toegang tot de opties **Escalatie en korting** en **Geavanceerde prijscalculatie** door de velden **Hoeveelheid ingevoerd**, **Eenheidsprijs**, **Korting** en **Nettobedrag** te gebruiken in **Factureringsdetails weergeven**. 
    - Op een verkooporder hebben de onderliggende regels een korting en kortingspercentage van 0 (nul). 
    - De factureringsfrequentie van de bovenliggende en de onderliggende artikelen kan worden gewijzigd, en elke regel kan een andere frequentie hebben. Het bovenliggende artikel wordt echter automatisch bijgewerkt zodat het de kortste frequentie van de onderliggende regels gebruikt. Een opbrengstsplitsing heeft bijvoorbeeld twee onderliggende artikelen, waarvan er één de **Maandelijkse** factureringsfrequentie gebruikt en de andere de **Jaarlijkse** factureringsfrequentie. In dit geval wordt de factureringsfrequentie van het bovenliggende artikel gewijzigd in **Maandelijks**.
