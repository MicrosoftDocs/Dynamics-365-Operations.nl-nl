---
title: Verbeteringen in kasbeheer
description: In dit onderwerp worden de verbeteringen in kasbeheer in POS voor Dynamics 365 for Retail beschreven.
author: anpurush
manager: AnnBe
ms.date: 5/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: ace32148387b2244f4b600597f16dfd7ebc5d108
ms.sourcegitcommit: 23ab3c99d05869ea2c73514754608e8684697d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595202"
---
# <a name="cash-management-improvements"></a>Verbeteringen in kasbeheer

[!include [banner](includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Kasbeheer is een belangrijke functie voor detailhandelaren in fysieke winkels. Detailhandelaren willen in hun winkels beschikken over systemen die volledige traceerbaarheid en verantwoording voor geldstromen tussen de verschillende kassa's en kassamedewerkers in een winkel kunnen bieden. Daarnaast moeten ze verschillen kunnen afstemmen en de verantwoordelijkheid kunnen bepalen.

Microsoft Dynamics 365 for Retail biedt functies voor kasbeheer in de POS-toepassing. In eerdere versies van Retail dan versie 10.0.3 is de functionaliteit voor kasbeheer echter niet robuust genoeg voor een volledige traceerbaarheid van geldverplaatsingen in winkels. Hoewel detailhandelaren het contante geld voor een winkel kunnen afstemmen, kan ze de verantwoordelijkheid bij discrepanties niet nauwkeurig vaststellen.

Microsoft Dynamics 365 for Retail 10.0.3 en hoger bieden detailhandelaren betere traceermogelijkheden voor kasverwerking. Als onderdeel van deze traceerbaarheid kunnen detailhandelaren kluizen definiëren, tweezijdige transacties van contant geld maken en kasbeheertransacties afstemmen.

## <a name="set-up-traceability-and-define-safes"></a>Traceerbaarheid instellen en kluizen definiëren

Als u de nieuwe functionaliteit voor kasbeheer wilt instellen, volgt u deze stappen om het functionaliteitsprofiel voor winkels te configureren.

1. Ga naar **Detailhandel \> Afzetkanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen** en selecteer een functionaliteit die is gekoppeld aan de winkels waarvoor u de kasbeheerverbeteringen beschikbaar wilt maken.
2. Stel op het sneltabblad **Functies** van het functionaliteitsprofiel onder **Geavanceerde kasbeheer** de optie **Traceerbaarheid van contant geld inschakelen** in op **Ja**.
3. Als u kluizen wilt instellen, gaat u naar **Detailhandel \> Kanalen \> Detailhandelwinkels \> Alle detailhandelwinkels** en selecteer een winkel.
4. Selecteer op de pagina **Winkels** in het actievenster op het tabblad **Instellen** in de groep **Instellen** de optie **Kluizen**. Met deze optie kunt u meerdere kluizen voor een winkel definiëren en onderhouden.
4. Voordat de functionaliteit kan worden gebruikt, moet u de distributieschemataak **1070-kanaalconfiguratie** uitvoeren om deze configuraties te synchroniseren met de kanaaldatabase.

## <a name="additional-cash-management-changes"></a>Extra wijzigingen in kasbeheer

In Retail-versie 10.0.3 en hoger zijn ook de volgende functies voor transacties van contant geld beschikbaar:

- Een gebruiker die wordt gevraagd om een beginbedrag te declareren, moet de bron van contant geld invoeren. De gebruiker kan zoeken naar de beschikbare kluizen die in de winkel zijn gedefinieerd en de luis selecteren waaruit het contante geld voor de kassa wordt gehaald.
- Een gebruiker die een bewerking uitvoert om wisselgeld te verwijderen, wordt gevraagd om in een lijst met openstaande wisselgeldinvoertransacties de transactie te selecteren waarop de bewerking wordt uitgevoerd. Als de bijbehorende wisselgeldinvoer niet bestaat in het systeem, kan de gebruiker een niet-gekoppelde transactie voor het verwijderen van wisselgeld maken.
- Een gebruiker die een wisselgeldinvoerbewerking uitvoert, wordt gevraagd om in een lijst met openstaande transacties voor het verwijderen van wisselgeld de transactie te selecteren waarop de wisselgeldinvoerbewerking wordt uitgevoerd. Als de bijbehorende wisselgeldverwijdering niet bestaat in het systeem, kan de gebruiker een niet-gekoppelde transactie voor invoeren van wisselgeld maken.
- Een gebruiker die een kluisstorting doet, wordt gevraagd de kluis te selecteren waarin het geld wordt gestort.
- Voor kluizen die zijn gedefinieerd in een winkel, kunnen gebruikers bewerkingen beheren, zoals het declareren van het beginbedrag, het uitvoeren van wisselgeldinvoer, het verwijderen van wisselgeld en het uitvoeren van een bankstorting.
- Voor gebruikers met de juiste gebruikersbevoegdheden worden in bewerkingen van het type Ploegen beheren de saldi van actieve, onderbroken en blind gesloten ploegen weergegeven.
- Als u de transacties van contant geld binnen een ploeg of tussen ploegen wilt afstemmen, selecteert u de ploeg die u wilt afstemmen en vervolgens **Afstemmen**. In de weergave die wordt geopend, wordt de lijst met afgestemde en niet-afgestemde transacties op afzonderlijke tabbladen weergegeven. Vanuit deze weergave kunnen gebruikers niet-afgestemde transacties selecteren en deze afstemmen of eerder afgestemde transacties selecteren en de afstemming hiervan ongedaan maken.
- Als tijdens het afstemmen de geselecteerde transactie niet in balans is, moet de gebruiker een omschrijving van de reden voor de niet-sluitende afstemming invoeren. Gebruikers kunnen één transactie selecteren en deze afstemmen met de relevante redenomschrijving.
- Gebruikers kunnen transacties blijven afstemmen en afstemmingen ongedaan maken totdat de ploeg is gesloten. Als een ploeg is gesloten, kan de afstemming van transacties niet ongedaan worden gemaakt.
- Wanneer een gebruiker ervoor kiest een ploeg te sluiten, wordt gecontroleerd of er geen niet-afgestemde kasbeheertransacties meer bestaan in de ploeg. Een ploeg kan niet worden gesloten als deze nog niet-afgestemde transacties bevat.
