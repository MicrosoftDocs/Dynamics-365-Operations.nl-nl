---
title: Factureringsplanningen beëindigen
description: In dit onderwerp wordt uitgelegd hoe u factureringsplanningen en factureringsplanningsregels beëindigt in facturering van abonnementen.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: df81cc888e893c6a4a127e1a43426a0a0b56f0d1
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470451"
---
# <a name="terminate-billing-schedules"></a>Factureringsplanningen beëindigen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u factureringsplanningen en factureringsplanningsregels beëindigt in facturering van abonnementen. Wanneer u een factureringsplanning beëindigt, moet deze de status **Actief** hebben. De status kan niet **In wachtstand** zijn. Ook moet een factureringsplanningsregel bij beëindiging de status **Actief** hebben. Het koptekstdeel van de factureringsplanning heeft geen invloed op het beëindigen van een factureringsplanningsregel.

Als u een factureringsplanning of factureringsplanningsregel wilt beëindigen, gaat u naar een van de volgende locaties:

- De lijstpagina **Alle/Actieve factureringsplanningen**
- Een specifieke factureringsplanning op de pagina **Alle factureringsplanningen**
- Een specifieke factureringsplanningsregel op de pagina **Alle factureringsplanningen**

> [!NOTE]
> Als u verschillende factureringsplanningen tegelijk wilt beëindigen, gebruikt u de pagina **Massale beëindigingsverwerking**.

## <a name="terminate-a-billing-schedule-or-line"></a>Een factureringsplanning of -regel beëindigen

Als u een factureringsplanning of factureringsplanningsregel wilt beëindigen, volgt u deze stappen.

1. Selecteer een factureringsplanning of een factureringsplanningsregel en selecteer vervolgens **Beëindigen**. 
2. Stel de velden **Beëindigingsdatum**, **Type beëindiging** en **Redencode** in.
3. Stel het veld **Creditoptie** in op **Credit uitgeven**.
4. Selecteer **Beëindigen**.

De status van de factureringsplanning wordt gewijzigd op basis van het geselecteerde type beëindiging. Als u **Resterend factuurbedrag** als het type beëindiging hebt geselecteerd, is de status van alle regels in de factureringsplanning **Laatste facturering**. De status van de factureringsplanning blijft **Actief** totdat de laatste factuur is verwerkt. Nadat de laatste factuur is verwerkt, wordt de status bijgewerkt naar **Beëindigd**. Als u **Planning aanpassen** als het type beëindiging hebt geselecteerd, wordt de status van de factureringsplanning onmiddellijk bijgewerkt naar **Beëindigd**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Een factureringsplanning of -regel beëindigen en een restitutie toepassen

Als u een factureringsplanning of factureringsplanningsregel wilt beëindigen en een restitutie wilt toepassen, volgt u deze stappen.

1. Selecteer een factureringsplanning of een factureringsplanningsregel en selecteer vervolgens **Beëindigen**.
2. Stel de velden **Beëindigingsdatum**, **Type beëindiging**, **Redencode** en **Creditoptie** in.
3. Selecteer **Beëindigen met restitutie**. De pagina **Massale beëindigingsverwerking** wordt weergegeven en gefilterd zodat hier de factureringsplanning wordt weergegeven.
4. Selecteer **Voorbeeld weergeven** om de factureringsplanningsregels weer te geven en selecteer **Verwerken**.

Nadat de creditering is verwerkt, opent u de pagina **Factureringsdetails weergeven** om de creditering te controleren die op de factureringsplanning is toegepast. Als het creditbedrag meer dan 0 (nul) is, worden alle toekomstige niet-gefactureerde regels verwijderd en vervangen door factureringsdetailregels met de negatieve bedragen voor het creditbedrag dat is toegepast op de factureringsplanning.

### <a name="view-example"></a>Voorbeeld weergeven

Een factureringsplanning bevat de volgende informatie:

- De begindatum is 1 januari 2020.
- De einddatum is 31 december 2020.
- Het factureringsperiodebedrag is 100,00 per maand.
- Er zijn facturen gemaakt voor factureringsperioden van januari tot en met juli.
- De beëindigingsdatum van het contract is 15 juni 2020.

Wanneer de kredietcorrectie wordt verwerkt, worden alle toekomstige factureringsperioden (augustus tot en met december) verwijderd van de pagina **Factureringsdetails weergeven**. Na de factureringsperiode van juli wordt er een regel voor kredietcorrectie toegevoegd:

- 16 juni – 31 juli, met een creditbedrag van 150,00

Als de functie voor niet-gefactureerde opbrengsten wordt gebruikt, wordt de pagina **Controle van niet-gefactureerde opbrengstjournaalboeking** bijgewerkt met de beëindigingspost.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Een factureringsplanning of -regel beëindigen zonder een creditering toe te passen

Als u een factureringsplanning of factureringsplanningsregel wilt beëindigen zonder een creditering toe te passen, volgt u deze stappen.

1. Selecteer een factureringsplanning of een factureringsplanningsregel en selecteer vervolgens **Beëindigen**.
2. Stel het veld **Beëindigingsdatum** in.
3. Stel het veld **Beëindigingstype** in op **Geen correctie**. Het veld **Creditoptie** wordt automatisch ingesteld op **Geen creditering**.
3. Stel het veld **Redencode** in.
4. Voer in het veld **Beëindigingsnotities** eventuele notities in die vereist zijn.
5. Selecteer **Beëindigen**. 

Wanneer de beëindiging wordt verwerkt, worden alle factureringsdetailregels na de beëindigingsdatum verwijderd. (Deze regels bevatten de regel met de datum van beëindiging.) Er kunnen geen facturen worden gemaakt voor de regels die zijn beëindigd. Als de beëindiging wordt verwijderd, worden alle regels opnieuw toegevoegd aan de pagina **Factureringsdetails weergeven** en komen deze beschikbaar voor facturering.

## <a name="fields"></a>Velden

De pagina **Factureringsdetails weergeven** bevat de volgende velden.

| Veld | Description |
|-------|-------------| 
| Ontslagdatum | Selecteer de datum waarop u een factureringsplanning of een factureringsplanningsregel wilt beëindigen. |
| Beëindigingstype | <p>Selecteer het beëindigingstype:</p><ul><li>**Planning aanpassen**: sluit de factureringsperioden voor de regel op de beëindigingsdatum af en wijzig de status van de regel in **Laatste facturering**. Als er een uitgestelde planning bestaat voor het regelartikel, wordt dit gecorrigeerd door het bedrag om te keren dat niet langer moet worden herkend. Als de begindatum van de facturering na de beëindigingsdatum valt, worden de resterende factureringsperioden verwijderd.</li><li>**Resterend factuurbedrag**: voeg elk resterend bedrag voor de factureringsperiode toe aan de beëindigingsperiode en wijzig de status van de regel in **Laatste facturering**. Als er een uitgestelde planning bestaat voor het regelartikel, wordt de einddatum voor het uitstel bijgewerkt. Als de begindatum van de facturering na de datum van beëindiging valt, wordt het totaalbedrag van alle resterende factureringsperioden opgeteld bij de factureringsperiode en worden de resterende factureringsperioden verwijderd.</li><li>**Geen correctie**: beëindig de factureringsperioden voor de regel op de opgegeven beëindigingsdatum. Er worden geen correcties aangebracht. Wanneer dit type beëindiging is geselecteerd, wordt het veld **Creditoptie** ingesteld op **Geen creditering** en wordt het veld **Dagelijks verdelen** ingesteld op **Nee**. Beide velden worden dan alleen-lezen en kunnen niet worden gewijzigd.</li></ul> |
| Kredietoptie | <p>Selecteer hoe de creditering wordt toegepast wanneer u een factureringsplanningsregel beëindigt:</p><ul><li>**Creditcorrectie**: maak een creditcorrectie voor een factureringsplanning wanneer een regel wordt beëindigd. De creditcorrectie wordt weergegeven in een toekomstige factureringsperiode voor de factureringsplanning. Met de correctie wordt ook het factuurbedrag voor de volgende factureringsperiode automatisch aangepast, totdat de creditering is toegepast op de factureringsplanning.</li><li>**Credit uitgeven**: stel een creditnota op als een factureringsplanning of een factureringsplanningsregel wordt beëindigd.</li><li>**Geen creditering**: voer geen creditcorrectie uit of stel geen creditnota op als een factureringsplanning of een factureringsplanningsregel wordt beëindigd. Deze optie is alleen beschikbaar wanneer u een beëindiging van het type **Geen correctie** gebruikt om een factureringsplanning te beëindigen.</li></ul><p>De standaardoptie is afkomstig van de pagina **Factureringsparameters voor terugkerende contracten**.</p> |
| Redencode | Selecteer de redencode voor de beëindiging. |
| Beschrijving reden | De beschrijving van de redencode. |
| Beëindigingsnotities | Eventuele notities over de beëindiging invoeren. |

<!--## Additional information-->
