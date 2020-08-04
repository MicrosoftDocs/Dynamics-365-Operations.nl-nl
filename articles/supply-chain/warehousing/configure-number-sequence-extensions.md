---
title: Nummerreeksen voor magazijnstromen configureren
description: In dit onderwerp komt aan de orde welke functies nummerreeksuitbreidingen bieden voor nummerplaat-id's, wavelabel-id's, container-id's en vrachtbrief-id's.
author: GarmMSFT
manager: tfehr
ms.date: 06/10/2020
ms.topic: configure-number-sequence-extensions
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSNumberSequenceExtension
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 3ee74ba108008ccef53fe3b904c71ddf5f51afb7
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546419"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Nummerreeksen voor magazijnstromen configureren

[!include [banner](../includes/banner.md)]

De functie *Nummerreeksuitbreidingen* voegt een nieuwe configuratiepagina toe voor het instellen van nummerreeksen. Hiermee wordt flexibele configuratie van GS1-gereguleerde id's mogelijk, waaronder GS1-voorvoegsels en controlecijfers (modulo 10) en wordt een lengtelimiet voor bestaande nummerreeksen afgedwongen.

Standaard nummerreekssegmenten zijn niet geschikt voor GS1-implementatie omdat er geen controlecijfer wordt berekend en het GS1-voorvoegsel van het bedrijf handmatig moet worden bijgewerkt.

Dit functie voegt de volgende functionaliteit toe:

- Vrachtbrief-id's (BOL) kunnen vooraf worden gegenereerd.
- Een unieke nummerreeks kan worden gegenereerd voor SSCC-nummers (Serial Shipping Container Code).
- Voor vrachtbrief- en SSCC-nummers kunnen GS1-nummerreeksen worden gemaakt. De functie voegt standaardondersteuning toe voor de nummerplaat-id's, container-id's, wavelabel-id's en vrachtbrief-Id's.
- De configuratie van de id-nummers van nummerplaten is flexibel. U kunt bijvoorbeeld kunstmatige intelligentie (AI) opnemen of uitsluiten, zoals voorloopnullen (00).

Deze functionaliteit maakt het efficiënter om labels van dozen te ondersteunen en om nieuwe nummers aan te passen die door het systeem worden gegenereerd.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>De functie voor nummerreeksuitbreidingen inschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Nummerreeksuitbreidingen*

## <a name="set-up-the-feature"></a>De functie configureren

Voer de volgende stappen uit om nummerreeksuitbreidingen in uw systeem in te stellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Ga naar het tabblad **Algemeen** en voer in het veld **GS1-bedrijfsvoorvoegsel** het GS1-voorvoegsel van uw bedrijf in. Deze waarde geldt voor alle nummerreeksen waarbij het GS1-voorvoegsel als een segment wordt opgenomen.
1. Als u vrachtbriefnummers wilt genereren voor wavelabels, schakelt u op het tabblad **Rapporten** het selectievakje **Vrachtbriefnummer genereren bij het afdrukken van wavelabels** in.

    > [!NOTE]
    > Dit selectievakje is alleen beschikbaar als de functionaliteit voor het [afdrukken van wavelabels](configure-wave-label-printing.md) is ingeschakeld.

1. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Nummerreeksuitbreidingen**
1. Selecteer **Standaardinstelling maken** in het actievenster. Een GS1-compatibele nummerreeks voor vrachtbrieven en drie typen SSCC-nummerreeksen worden gemaakt. Al deze nummerreeksen houden rekening met de lengte van het GS1-voorvoegsel van uw bedrijf.

    Zie het volgende gedeelte voor meer informatie over het aanpassen van deze standaard nummerreeksen en/of het toevoegen van nieuwe reeksen. U kunt deze reeksen ook verwijderen als u ze niet nodig hebt.

1. Ga terug naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Selecteer op het tabblad **Nummerreeksen** de relevante nummerreeksuitbreiding die u wilt gebruiken om nummers te genereren voor uw nummerplaat-id's, wavelabel-id's, container-id's (selecteer in dit geval de juiste **SSCC-18** nummerreeks) en/of vrachtbrief-id's (selecteer in dit geval de **vrachtbrief**reeks). Standaard worden nummerreeksuitbreidingen alleen voor deze vier typen id's ondersteund.

De volgende keer dat een nieuw nummer wordt gegenereerd voor een van deze nummerreeksen, wordt de nieuwe logica gebruikt.

> [!NOTE]
> Als u geen nummerreeksuitbreiding selecteert voor de id van de nummerplaat, worden de huidige regels voor het genereren van de nummerplaat-id gebruikt. Anders wordt de geselecteerde nummerreeks gebruikt. De andere id's gebruiken een gewone nummerreeks totdat u hiervoor een nummerreeksuitbreiding toepast.

## <a name="create-and-edit-number-sequences"></a>Nummerreeksen maken en bewerken

In de vorige sectie hebt u een standaardset met nummerreeksen gegenereerd. In deze sectie wordt uitgelegd hoe elke nummerreeks wordt gedefinieerd. Ook wordt uitgelegd hoe u aangepaste reeksen maakt en hoe u de standaard of aangepaste reeksen bewerkt.

Voer de volgende stappen uit om nummerreeksen te maken en te bewerken.

1. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Nummerreeksuitbreidingen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Nummerreeksuitbreiding** een naam voor de nieuwe reeks in. Voer in het veld **Beschrijving** een beschrijving in.
1. Gebruik op het sneltabblad **Segmenten** de knoppen op de werkbalk om de nummeringsindeling samen te stellen door segmenten toe te voegen, te verwijderen en te rangschikken. Wijs in het veld **Segment** voor elke rij een segmenttype toe om het doel en de inhoud van dat segment te definiëren. In de volgende tabel wordt beschreven welke segmenttypen beschikbaar zijn.

    | Segmenttype | Omschrijving |
    |---|---|
    | Constant | Dit segmenttype voegt dezelfde constante tekst toe voor elk gegenereerd nummer in de reeks. Voer in het veld **Waarde** de vereiste tekst in. Het veld **Lengte** wordt automatisch bijgewerkt naar de lengte van de tekst die u in het veld **Waarde** hebt ingevoerd. |
    | Nummerreeks | Voer in het veld **Waarde** een hekje (*\#*) in voor elk teken dat in de gegenereerde reeks moet worden weergegeven. De nummerreeks zelf kan langere getallen genereren, maar alleen de meest rechtse tekens worden weergegeven. Het veld **Lengte** wordt automatisch bijgewerkt naar het aantal hekjes dat u in het veld **Waarde** hebt ingevoerd.<p>Als u wilt voldoen aan GS1-vereisten voor SSCC-18-nummers, moet u ervoor zorgen dat de lengte van dit segment 16 min de lengte van het GS1-voorvoegsel is.</p> |
    | GS1-voorvoegsel | Dit segmenttype voegt de waarde toe die is ingesteld in het veld **GS1-voorvoegsel bedrijf** op de pagina **Parameters voor magazijnbeheer**. In het veld **Waarde** wordt de waarde weergegeven die is ingesteld op de pagina **Parameters voor magazijnbeheer**, en in het veld **Lengte** wordt het aantal tekens in de waarde weergegeven. Zowel het veld **Waarde** als het veld **Lengte** zijn alleen-lezen. |
    | Toepassings-id | Voer in het veld **Waarde** een toepassings-id in die is opgegeven met het relevante GS1-beleid voor dit type nummerreeks. Voer bijvoorbeeld *00* in voor SSCC of *420* voor vrachtbrieven (BOL). Het veld **Lengte** wordt automatisch bijgewerkt naar de lengte van de id die u in het veld **Waarde** hebt ingevoerd. |
    | Verpakkingstype | Voor artikelen die duidelijk kunnen worden geïdentificeerd, wordt met dit segmenttype een veldwaarde uit de relevante eenheidsvolgordegroep (van de pagina **Eenheidvolgordegroepen**) toegevoegd. (Dit komt overeen met de bestaande logica voor de nummerplaat-id's.) Voor nummerplaten met meerdere SKU's (Stock Keeping Units) wordt voor dit segmenttype standaard *0* (nul) toegevoegd. Voor dit segmenttype wordt het veld **Waarde** altijd ingesteld op *P* en wordt het veld **Lengte** altijd ingesteld op *1*.|
    | Controlecijfer | Dit segmenttype voegt een controlecijfer toe. Dit is een modulo 10-berekening. (Dit komt overeen met de bestaande logica voor nummerplaat-id's.) Voor dit segmenttype wordt het veld **Waarde** altijd ingesteld op een caret (*^*) en wordt het veld **Lengte** altijd ingesteld op *1*. |

1. Als u een voorbeeld wilt weergeven van de uiteindelijke getalnotatie, bekijkt u het veld **Indeling** onderaan het sneltabblad **Segmenten**.
