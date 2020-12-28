---
title: Werk splitsen
description: Dit onderwerp bevat informatie over de functionaliteit voor gesplitst werk. Met deze functie kunt u grote werkorders splitsen in meerdere kleinere werkorders die u vervolgens aan meerdere magazijnmedewerkers kunt toewijzen. Op deze manier kan het werk tegelijkertijd worden verzameld door verschillende magazijnmedewerkers.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4425917"
---
# <a name="work-split"></a>Werk splitsen

Met functionaliteit voor gesplitst werk kunt u grote werkorder-id's splitsen in meerdere kleinere werkorder-id's die u vervolgens aan meerdere magazijnmedewerkers kunt toewijzen. Op deze manier kan één werkaanmaaknummer tegelijkertijd worden verzameld door verschillende magazijnmedewerkers.

> [!IMPORTANT]
> U kunt alleen werkorders splitsen met de status *Openstaand* of *In uitvoering*.

## <a name="turn-on-the-work-split-functionality"></a>De functionaliteit voor gesplitst werk inschakelen

Voordat u de functionaliteit voor gesplitst werk kunt gebruiken, moet u deze functie en de bijbehorende vereiste functie in uw systeem inschakelen. Beheerders kunnen gebruikmaken van de instellingen van [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en desgewenst in te schakelen.

Schakel eerst de bijbehorende vereiste functie *Werk blokkeren voor de hele organisatie* in als deze nog niet is ingeschakeld. Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Werk blokkeren voor de hele organisatie*

> [!NOTE]
> Wanneer deze functie is geactiveerd, wordt automatisch een gegevensupgrade toegepast nadat de functie is ingeschakeld voor alle rechtspersonen.

Schakel vervolgens de functie *Werk splitsen* in. Deze wordt op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Werk splitsen*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Verbeteringen in de pagina's Werkgegevens en Alle werk

Met de functie *Werk splitsen* worden de volgende twee knoppen toegevoegd aan het tabblad **Werk** in het actievenster van de pagina's **Werkgegevens** en **Alle werk**:

- **Werk splitsen**: splits de huidige werk-id in meerdere kleinere werk-id's die kunnen worden verwerkt door afzonderlijke werknemers.
- **Werksplitsingssessie annuleren**: annuleer de sessie voor werksplitsing en maak het werk beschikbaar voor verwerking.

![De knoppen Werk splitsen en Werksplitsingssessie annuleren](media/Work_split_buttons.png "De knoppen Werk splitsen en Werksplitsingssessie annuleren")

> [!IMPORTANT]
> De knop **Werk splitsen** is niet beschikbaar als aan een van de volgende voorwaarden is voldaan:
>
> - De werkstatus is iets anders dan *Openstaand* of *In uitvoering*.
> - Er is een container-ID gekoppeld aan de werk-ID. (Een container kan niet systematisch worden gesplitst, omdat hiervoor fysieke acties vereist zijn.)
> - Het werk is aan een cluster gekoppeld.
> - Het werkordertype is iets anders dan een van de volgende typen:
>
>    - Verkooporders
>    - Orderverzameling van grondstoffen
>    - Overboekingsuitgifte
>
> - Het werk wordt momenteel gesplitst door een andere gebruiker. Als u de splitsingspagina probeert te openen voor werk dat al wordt gesplitst door een andere gebruiker, wordt het volgende foutbericht weergegeven: "Het werk met id \#\#\#\# wordt momenteel gesplitst. Probeer het over een paar minuten opnieuw. Neem contact op met een supervisor als u dit bericht blijft ontvangen."

Een nieuwe reden voor het blokkeren van werk, *Werk gesplitst*, geeft aan dat de werk-id op dat moment wordt gesplitst. Deze wordt weergegeven op de pagina **Werk splitsen** en in de magazijn-app als een gebruiker het werk probeert uit te voeren. Wanneer er blokkeringsredenen worden gebruikt, wordt de naam van het veld **Geblokkeerde wave** van de werk-id gewijzigd in **Geblokkeerd**.

## <a name="initiate-a-work-split"></a>Een werksplitsing starten

Met deze functie voegt u een nieuwe pagina **Werk splitsen** toe waarmee gebruikers werkregels van de werk-id kunnen splitsen. Wanneer de pagina voor het eerst wordt geopend, worden regels met de werkstatus *Openstaand* weergegeven en kunnen deze worden gesplitst. Selecteer in het actievenster de optie **Werk splitsen** om het geselecteerde werk te verwerken.

Voer de volgende stappen uit om werk te splitsen.

1. Open een van de volgende werkpagina's:

    - **Werkgegevens** (**Magazijnbeheer \> Werk \> Werkgegevens**)
    - **Alle werk** (**Magazijnbeheer \> Werk \> Alle werk**)

1. Selecteer in het raster een werk-id om te splitsen. Het veld **Werkordertype** moet zijn ingesteld op een van de volgende waarden:

    - Verkooporders
    - Orderverzameling van grondstoffen
    - Overboekingsuitgifte

1. Selecteer in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Werk splitsen**.

    De pagina **Werk splitsen** verschijnt en toont de werkregels die openstaan en kunnen worden gesplitst. Standaard worden alleen de beschikbare werkregels weergegeven. Als u alle regels voor de werk-id wilt weergeven (bijvoorbeeld regels met werktype *Wegzetten*), schakelt u het selectievakje **Alle regels weergeven** boven het raster in.

    Het volgende bericht wordt weergegeven: "Gebruikers kunnen geen regels van het werk verwerken totdat u klaar bent met de splitsing en deze pagina hebt gesloten."

    Het veld **Reden voor blokkeren van werk** voor het huidige werk wordt ingesteld op *Gesplitst werk* en het werk wordt geblokkeerd.

    ![Reden voor blokkering](media/Blocking_reason.png "Reden voor blokkering")

1. Selecteer de regels die u wilt verwijderen uit de huidige werk-id en toevoegen aan een nieuwe werk-id. De volgende gebeurtenissen vinden plaats:

    - Wanneer u het werk splitst, worden de geselecteerde regel of regels van de oorspronkelijke werk-id geannuleerd en vervolgens naar een nieuwe werk-id gekopieerd.
    - De bestaande werksjabloonstructuur en de wegzetlocatie (en ook toekomstige combinaties van verzamelen en wegzetten) blijven behouden. De waarden voor de volgende werk-id-velden worden gekopieerd van het oorspronkelijke werk naar het nieuwe werk:

        - Lading-id
        - Zending-id
        - Werkordertype
        - Ordernummer
        - Locatie
        - Magazijn
        - Werkprioriteit
        - Werkgroep-id
        - Wave-id
        - Werkaanmaaknummer

    - De volgende velden worden niet naar de nieuwe werk-id gekopieerd:

        - **Werk-id**: er wordt een nieuwe werk-id gegenereerd op basis van de betreffende nummerreeks.
        - **Werkstatus**: dit veld wordt ingesteld op *Openstaand*.
        - **Vergrendeld door**: dit veld wordt in eerste instantie op leeg ingesteld.
        - **Doelnummerplaat-id**: dit veld wordt niet ingevuld.
        - **Aanmaakdatum en -tijd**: dit veld wordt ingesteld op de huidige datum en tijd.
        - **Wave/werk geblokkeerd**: dit veld wordt opnieuw berekend voor de oorspronkelijke werk-id en de nieuwe werk-id.

1. Selecteer **Werk splitsen** in het actievenster.

Terwijl het werk wordt gesplitst, wordt het volgende bericht weergegeven: "Bezig met verwerken -Werk splitsen". Terwijl dit bericht zichtbaar is, kunt u de bewerking annuleren door **Annuleren** te selecteren in het berichtvenster.

Als het selectievakje **Alle regels weergeven** is uitgeschakeld, wordt de regel die is gesplitst en geannuleerd niet meer weergegeven in het raster. Als het selectievakje is ingeschakeld, ziet u dat de waarde van het veld **Werkstatus** voor die regel is gewijzigd in *Geannuleerd*.

De volgende melding wordt weergegeven om aan te geven dat de nieuwe werk-id is gemaakt: "Werk \#\#\#\# is gemaakt door een splitsing van het oorspronkelijke werk \#\#\#\#."

Andere werkregels van de oorspronkelijke werk-id (zoals *Wegzetten*-regels) worden zo nodig aangepast aan de werkregels die zijn geannuleerd. Als de oorspronkelijke werk-id bijvoorbeeld een *Wegzetten*-regel heeft voor een hoeveelheid van 15 en *Verzamelen*-regels met een totale hoeveelheid van 10 die zijn geannuleerd, is de nieuwe hoeveelheid voor *Wegzetten* op de oorspronkelijke werk-id nu 5.

Het nieuwe werk wordt niet onmiddellijk aan een gebruiker toegewezen. U kunt dit echter zo nodig nu aan een gebruiker toewijzen door de standaardfunctionaliteit van de pagina **Werkgegevens** te gebruiken.

> [!IMPORTANT]
> U kunt alleen werk-id's splitsen die twee of meer beschikbare werkregels bevatten. Als u **Werk splitsen** selecteert wanneer er slechts één werkregel is, wordt het volgende foutbericht weergegeven: "Ten minste één werkregel moet op het oorspronkelijke werk blijven." In dit geval wordt er geen splitsing uitgevoerd.

## <a name="finish-a-work-split"></a>Een werksplitsing voltooien

Als u het splitsen van werk wilt voltooien, moet de blokkeringsreden *Gesplitst werk* worden verwijderd. Deze stap kunt u op twee manieren uitvoeren:

- De gebruiker die de werkzaamheden splitst, sluit de pagina **Werk splitsen** door de knop **Sluiten** (**X**) te selecteren in de rechterbovenhoek. Wanneer de pagina wordt gesloten, wordt de blokkeringsreden *Werk splitsen* verwijderd. De status *Geblokkeerd* van dit werk wordt opnieuw berekend en als er geen resterende blokkeringsredenen zijn voor dit werk, wordt de blokkering van het werk opgeheven.
- Een gebruiker opent de werk-id en selecteert de knop **Werksplitsingssessie annuleren** in het actievenster. De blokkeringsreden *Gesplitst werk* wordt verwijderd en de status *Geblokkeerd* van dit werk wordt opnieuw berekend, zoals bij het sluiten van de pagina **Werk splitsen**.

Nadat de blokkeringsreden *Gesplitst werk* is verwijderd, kan het werk worden uitgevoerd op het mobiele apparaat, mits de status **Geblokkeerd** is ingesteld op *Nee* in de werk-id.

## <a name="user-blocking-on-the-warehouse-app"></a>Gebruikers blokkeren in de magazijn-app

Als u de magazijn-app probeert te gebruiken voor verzamelen van werk voor een werk-ID die al wordt gesplitst, wordt het volgende foutbericht weergegeven: "Het werk met id \#\#\#\# wordt momenteel gesplitst." Als dit foutbericht wordt weergegeven, selecteert u **Annuleren**. Vervolgens kunt u doorgaan met het verwerken van ander werk.

## <a name="other-blocked-operations"></a>Andere geblokkeerde bewerkingen

Bewerkingen waarmee werkregels, werkvoorraadtransacties of aanvullingskoppelingen worden gewijzigd die zijn gerelateerd aan het werk dat wordt gesplitst, zullen mislukken en het volgende foutbericht wordt weergegeven: "Het werk met ID \#\#\#\# wordt momenteel gesplitst."
