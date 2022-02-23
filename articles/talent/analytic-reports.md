---
title: Analytische rapporten gebruiken in Attract
description: In dit onderwerp worden de analytische rapporten voor inzichten in het aanstellingsproces in Microsoft Dynamics 365 Talent - Attract beschreven
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460835"
---
# <a name="use-analytic-reports-in-attract"></a>Analytische rapporten gebruiken in Attract

[!include [banner](includes/banner.md)]

Analytische rapporten in Microsoft Dynamics 365 Talent: Attract bieden een standaardoplossing voor inzichten in het aanstellingsproces. Tot de beschikbare functies behoren:

- **Functieanalyse**: klik op het tabblad **Analyses** binnen een functie voor metrische gegevens over de sollicitanten naar de functie.
- **Analysehub**: klik op **Analyses** in de linkernavigatiebalk voor samengevoegde meetgegevens over de verschillende functies.
- **Gebruikersspecifieke beveiliging**: toegang tot rapporten wordt beheerd per Attract-[rol](security-attract.md) en functiedeelnemersrol.
- **Kruisfilteren**: klik op visuele elementen in een rapport om andere metrische gegevens weer te geven die door geselecteerde gegevens worden gefilterd.

>[!NOTE] 
>- Deze functie is momenteel in [preview](access-preview-feature.md). Als u deze wilt proberen, hebt u [**Uitgebreide invoegtoepassing voor aanstellingen**](attract-comprehensive-hiring.md) nodig.
>- Alle rapporten in openbare preview worden in het Engels weergegeven.
>- Rapporten worden elke 3 uur vernieuwd. Het tijdstip van de laatste vernieuwing (in de lokale tijdzone) wordt boven aan het rapport weergegeven. De vernieuwingsfrequentie is een benadering en varieert op basis van gegevensvolume en belasting van resources in uw regio.

## <a name="job-analytics"></a>Analyses van functie

Functieanalyse-rapporten vormen een momentopname van het aanstellingsproces van een functie.  Belangrijke metrische gegevens zijn:

- Actieve sollicitanten op fase
- Bron van sollicitant
- Type sollicitant (intern of extern)

## <a name="analytics-hub"></a>Analysehub

Analysehub-rapporten voegen gegevens van verschillende functies samen om trends in het aanstellingsproces naar boven te halen. Attract omvat twee OOTB-rapporten: Pipeline-overzicht en Trechteranalyse.

### <a name="pipeline-summary"></a>Overzicht pipeline

In het rapport Pipeline-overzicht worden gegevens samengevoegd voor openstaande functies. Belangrijke metrische gegevens zijn:

- Sollicitanten in alle functies op fase
- Bron van sollicitant
- Openstaande functies op anciënniteitsniveau

### <a name="funnel-analysis"></a>Trechteranalyse

In het rapport Trechteranalyse worden gegevens samengevoegd voor functies die zijn afgesloten als vervuld. Belangrijke metrische gegevens zijn:

- Wervingstijd
- Metrische gegevens voor conversie (bij aanwijzen)
- Percentage van aanbiedingsacceptatie

Opmerking: voor de meest accurate rapportage van het wervingstijdstip, verdient het aanbeveling om [Aanbiedingsbeheer](offer-setup.md) te gebruiken. Dit is een functie die beschikbaar is als onderdeel van de uitgebreide invoegtoepassing voor aanstellingen.

>[!TIP] 
>Probeer visuele elementen aan te wijzen voor aanvullende informatie. Als u bijvoorbeeld visuele elementen voor **Actieve sollicitanten** aanwijst, wordt het gemiddelde aantal dagen in de fase weergegeven. Het analyseren van deze informatie kan leiden tot belangrijke inzichten die de wervingstijd verkorten en wervers in staat stellen zich te concentreren op manieren om de tijd te beperken die in elke fase wordt besteed.

## <a name="user-specific-security"></a>Gebruikersspecifieke beveiliging

Attract-rapporten zijn toegankelijk voor de [rollen](security-attract.md) Beheer, Alles lezen, Werver en Aanstellend manager. Niet-toegewezen gebruikers hebben geen toegang tot de analytische rapportpagina's (Functieanalyse of Analysehub).

Functieanalyserapporten tonen gegevens voor de geselecteerde functie. In Analysehubrapporten worden gegevens samengevoegd over alle functies die een gebruiker kan weergeven. Gebruikers die zowel Mijn functies als Alle functies op de pagina Functies kunnen weergeven, hebben de beschikking over dezelfde weergaven in de Analysehub.

## <a name="cross-filter"></a>Kruisfilter

Een van de mooie functies van Power BI is de manier waarop alle visuele elementen op een rapportpagina onderling zijn verbonden. Als u een gegevenspunt selecteert in een van de visuele elementen, worden alle andere visuele elementen op de pagina die deze gegevens bevatten gewijzigd op basis van die selectie. Lees meer over deze functie en bekijk een voorbeeld in [Visuele elementen kruisfilteren in een Power BI-rapport](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Exporteren naar Excel

Als u rapportgegevens wilt weergeven in Excel, kunt u op het optiemenu (drie puntjes) in een visueel element klikken en **Onderliggende gegevens exporteren** selecteren. Geëxporteerde gegevens worden als gefilterd geëxporteerd, met inachtneming van de gebruikersmachtigingen in Attract. Zie [Gegevens exporteren vanuit visualisaties](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data) voor meer informatie.
