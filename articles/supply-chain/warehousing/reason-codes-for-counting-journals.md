---
title: Redencodes voor voorraadtelling
description: Dit onderwerp beschrijft hoe u redencodes instelt en toepast voor teltaken.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 95f7ceb39d2afef1871f395ed562632865022b39
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345261"
---
# <a name="reason-codes-for-inventory-counting"></a>Redencodes voor voorraadtelling

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Met redencodes kunt u de resultaten analyseren van een tellingsproces en eventuele verschillen die tijdens dat proces optreden. U kunt de reden voor het uitvoeren van de telling opgeven, zoals een gebroken pallet of een voorraadcorrectie die is gebaseerd op voorraadmonsters. Tegelijkertijd kunt u de functionaliteit voor correctie gebruiken om de waarde van correcties van voorhanden voorraad op de juiste tegenrekening te boeken, op basis van de reden voor elke voorraadcorrectie.

## <a name="recommendation"></a>Aanbeveling

Voordat u het systeem instelt, wordt aangeraden om een strategie voor het werken met redencodes te definiëren. Probeer bijvoorbeeld de volgende vragen te beantwoorden:

- Moeten redencodes verplicht zijn in magazijnen?
- Moeten redencodes verplicht of optioneel zijn voor bepaalde artikelen?
- Hoeveel redencodes hebt u nodig?
- Moet u voor correcties vooraf een beperkte lijst met redencodes selecteren?
- Hoe moeten gebruikers van sstreepjescodescanners redencodes gebruiken? Moeten de redencodes vooraf worden geselecteerd, verplicht zijjn en niet kunnen worden bewerkt?
- Hebben magazijnmedewerkers andere redencodegedrag nodig voor mobiele scanners? Als het antwoord Ja is, kunt u meer menu-items maken en deze toewijzen aan verschillende personen.
- Moeten de redencodes worden gebruikt voor het boeken op financiële tegenrekeningen?

## <a name="turn-on-reason-code-features-in-your-system"></a>Functies voor redencodes in uw systeem inschakelen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Als u in uw systeem niet alle functies ziet die in dit onderwerp worden beschreven, moet u waarschijnlijk de functie *Voorhanden correcties boeken met configureerbare redencodes die zijn gekoppeld aan tegenrekeningen* inschakelen. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Voorhanden correcties boeken met configureerbare redencodes die zijn gekoppeld aan tegenrekeningen*

## <a name="set-up-reason-codes"></a>Redencodes instellen

### <a name="set-up-reason-code-policies"></a>Redencodebeleid instellen

U kunt meerdere beleidsregels voor redencodes maken om te bepalen wanneer en hoe redencodes voor tellingen worden toegepast. Elk beleid voor redencodes kan een van twee typen redencodes voor tellingen hebben: (*Optioneel* of *Verplicht*). Beleidsregels voor redencodes voor tellingen kunnen worden gebruikt op magazijn- of artikelniveau.

Volg deze stappen om redencodebeleid te maken.

1. Ga naar het **Voorraadbeheer** \> **Instellen** \> **Voorraad** \> **Beleid voor redencodes voor tellingen**.
1. Selecteer in het actievenster de optie **Nieuw** om beleid aan het raster toe te voegen.
1. Stel het veld **Naam** voor het nieuwe beleid in.
1. Selecteer in het veld **Type redencode voor telling** de optie *Verplicht* of *Optioneel* in om op te geven of de selectie van een redencode een optionele of verplichte actie moet zijn in een van de volgende voorraadcorrectieprocessen:

    - Cyclustelling (mobiel apparaat)
    - Plaatscyclustelling (mobiel apparaat)
    - Drempeltelling (mobiel apparaat)
    - Correctie-invoer (mobiel apparaat)
    - Correctie-uitvoer (mobiel apparaat)
    - Tellijst (rich client)
    - Hoeveelheidscorrectie/online telling (rich client)

U kunt beleid voor redencodes instellen voor afzonderlijke magazijnen en voor producten. De instellingen voor redencodes voor een product kunnen voorrang hebben op de instellingen voor het magazijn van het product.

> [!NOTE]
> Als voor magazijnen en artikelen het veld **Beleid van redencode voor telling** in ingesteld op *Verplicht*, is kan de tellijst pas worden voltooid en afgesloten als er een redencode wordt opgegeven. Zie het volgende gedeelte voor meer informatie.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Beleid van redencode voor telling toewijzen aan magazijnen

Volg deze stappen om beleid van redencode voor telling aan een magazijn toe te wijzen.

1. Ga naar **Voorraadbeheer** \> **Instellen** \> **Opsplitsing van voorraad** \> **Magazijnen**.
1. Selecteer een magazijn in het lijstvenster.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Instellen** de optie **Beleid van redencode voor telling**. Neem vervolgens een van de volgende stappen in het vervolgkeuzevenster **Beleid van redencode voor telling toewijzen**:

    - Als u de beleidsinstellingen voor elk artikel wilt gebruiken om te bepalen of tellijsten voor het artikel verplicht zijn, voert u geen waarde in (of verwijdert u de bestaande waarde).
    - Als een redencode voor tellijsten voor het magazijn verplicht zijn, selecteert u een redenbeleid waarbij het veld **Type redencode voor telling** is ingesteld op *Verplicht*.
    - Als een redencode voor tellijsten voor het magazijn optioneel zijn, selecteert u een redenbeleid waarbij het veld **Type redencode voor telling** is ingesteld op *Optioneel*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Beleid van redencode voor telling toewijzen aan producten

Volg deze stappen om beleid van redencode voor telling aan een product toe te wijzen.

1. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.
1. Selecteer een product in het raster.
1. Selecteer in het actievenster op het tabblad **Product** in de groep **Instellen** de optie **Beleid van redencode voor telling**. Neem vervolgens een van de volgende stappen in het vervolgkeuzevenster **Beleid van redencode voor telling toewijzen**:

    - Als u de beleidsinstellingen voor het magazijn wilt gebruiken om te bepalen of tellijsten voor het product verplicht zijn, voert u geen waarde in (of verwijdert u de bestaande waarde).
    - Als een redencode voor tellijsten voor het product verplicht zijn, selecteert u een redenbeleid waarbij het veld **Type redencode voor telling** is ingesteld op *Verplicht*. Deze instelling overschrijft de instelling van redencodes op magazijnniveau.
    - Als een redencode voor tellijsten voor het product optioneel zijn, selecteert u een redenbeleid waarbij het veld **Type redencode voor telling** is ingesteld op *Optioneel*. Deze instelling overschrijft de instelling van redencodes op magazijnniveau.

### <a name="set-up-counting-reason-codes"></a>Redencodes voor telling instellen

Ga als volgt te werk om de redencodes voor telling in te stellen.

1. Ga naar **Voorraadbeheer** \> **Instellen** \> **Voorraad** \> **Redencodes voor tellingen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel de velden **Redencode voor telling** en **Beschrijving** voor de nieuwe rij in.
1. Als u een tegenrekening wilt toewijzen, typt of selecteert u een waarde in het veld **Tegenrekening**.

    > [!NOTE]
    > Als een tegenrekening is toegewezen aan een redencode voor telling, wordt bij het boeken van een tellijst met die redencode voor telling, de waarde geboekt op de toegewezen tegenrekening in plaats van op de standaardrekening voor voorraadboeking.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Redencodegroepen voor telling instellen

*Redencodegroepen voor telling* kunnen worden gebruikt als onderdeel van de menu-items *Correctie-invoer* en *Correctie-uitvoer* in de mobiele app Warehouse Management om de lijst met redencodes voor telling te beperken. (Zie voor meer informatie over redencodegroepen voor telling het gedeelte [Menu-items voor mobiele apparaten instellen voor correctie in en correctie uit](#setup-adjustment-in-out) verderop in dit onderwerp.)

1. Ga naar het **Voorraadbeheer** \> **Instellen** \> **Voorraad** \> **Redencodegroepen voor telling**.
1. Selecteer **Nieuw** in het actievenster om een groep toe te voegen.
1. Stel de velden **Redencodegroep** en **Groepsomschrijving** voor de nieuwe groep in.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het gedeelte **Informatie** de optie **Nieuw** op de werkbalk om een rij aan het raster toe te voegen. Stel vervolgens het veld **Redencode voor telling** voor de nieuwe rij in. 
1. Herhaal de vorige stap om indien nodig meer codes toe te wijzen. Als u een code uit de groep moet verwijderen, selecteert u deze code en selecteert u vervolgens **Verwijderen** op de werkbalk.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Redencodes voor menuopties voor mobiele apparaten instellen

U kunt redencodes configureren voor de volgende voorhanden correctietypen:

- Cyclustelling
- Spotcyclustelling
- Drempeltelling
- Correctie-invoer
- Correctie-uitvoer

In de meeste gevallen kunt u de volgende informatie definiëren voor elk relevante menu-item voor mobiele apparaten:

- Of de redencode tijdens de telling wordt weergegeven aan de werknemer met het mobiele apparaat.
- De standaardredencode die wordt weergegeven in een menuoptie op het mobiele apparaat.
- Of de gebruiker de redencode kan bewerken.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Redencodes voor menuopties voor mobiele apparaten instellen voor een telproces

Als u een menuoptie voor een mobiel apparaat wilt instellen voor een telproces, voert u de volgende stappen uit.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.
1. Selecteer het relevante menu-item in het lijstvenster of maak een nieuw menu-item.
1. Selecteer in het actievenster **Cyclustelling**.
1. Stel in het veld **Standaardredencode voor telling** de standaardredencode in die moet worden vastgelegd wanneer het mobiele apparaat voor het tellen wordt gebruikt.
1. Selecteer in het veld **Redencode voor telling weergeven** een van de volgende waarden:

    - *Regel*: geef de redencode weer nadat elke afwijking is vastgelegd.
    - *Verbergen*: geef de redencode niet weer.

1. Stel de **Redencode voor telling bewerken** in op *Ja* als de medewerker de redencode mag bewerken wanneer deze tijdens het tellen wordt weergegeven op het mobiele apparaat. Stel deze optie in op *Nee* als de medewerker de code niet mag bewerken.

> [!NOTE]
> De knop **Cyclustelling** kan worden ingeschakeld voor elke menuoptie op het mobiele apparaat waarmee de telling kan worden uitgevoerd. Dit kunnen menu-items zijn voor plaatscyclustellingen, door de gebruiker uitgevoerd werk of door het systeem uitgevoerd werk.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>De menu-items voor het mobiele apparaat instellen voor Correctie-invoer en Correctie-uitvoer

Als u een menu-item voor een mobiel apparaat wilt instellen voor Correctie-invoer of Correctie-uitvoer, voert u de volgende stappen uit.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.
1. Selecteer in het actievenster **Nieuw** om een menu-item te maken.
1. Stel de velden **Itemnaam mobiel apparaat** en **Titel** voor het nieuwe menu-item in.
1. Stel het veld **Modus** in op *Werk*.
1. Stel de optie **Bestaand werk gebruiken** in op *Nee*.
1. Selecteer in het veld **Procedure voor het maken van werk** de optie *Correctie-invoer* of *Correctie uitvoer*.
1. Stel op het sneltabblad **Algemeen** de volgende velden in. (Al deze velden worden toegevoegd wanneer u *Correctie invoer* of *Correctie uitvoer* in het veld **Procedure voor het maken van werk** selecteert.)

    - **Verwerkingsinstructies gebruiken**: als u een proces voor *Correctie uitvoer* maakt, moet u deze optie instellen op *Ja*. Als u een proces voor *Correctie uitvoer* maakt, is deze optie altijd ingesteld op *Ja*.
    - **Standaardredencode voor telling**: stel de standaardredencode in die moet worden vastgelegd wanneer het menu-item van het mobiele apparaat voor het tellen wordt gebruikt.
    - **Redencode voor telling weergeven**: selecteer een van de volgende waarden:

        - *Regel*: geef de redencode weer nadat elke afwijking is vastgelegd.
        - *Verbergen*: geef de redencode niet weer.

    - **Redencode voor telling bewerken**: stel deze optie in op *Ja* als de medewerker de redencode mag bewerken wanneer deze tijdens het tellen wordt weergegeven op het mobiele apparaat. Stel deze optie in op *Nee* als de medewerker de code niet mag bewerken.
    - **Redencodegroepen voor telling:** selecteer een redencodegroep als u de lijst met opties die aan medewerkers wordt getoond, wilt beperken. Raadpleeg het gedeelte [Redencodegroepen voor telling instellen](#reason-groups) eerder in dit onderwerp voor informatie over het instellen van redencodegroepen. 

> [!NOTE]
> Wanneer u een redencodegroep voor telling toewijst aan de menu-items *Correctie invoer* en *Correctie uitvoer* waarbij de optie **Verwerkingsinstructies gebruiken** is ingesteld op *Ja*, kunt u een beperkte lijst met redencodes voor telling ophalen als onderdeel van de verwerking in de mobiele app Warehouse Management.
>
> Met de optie **Verwerkingsinstructies gebruiken** kunt u ook voorkomen dat zich per ongeluk grote hoeveelheden correcties voordoen. (Een medewerker scant bijvoorbeeld per ongeluk een streepjescode van een artikelnummer in plaats van een hoeveelheidswaarde.) Als u deze functionaliteit wilt instellen, stelt u de optie **Verwerkingsinstructies gebruiken** in op *Ja* voor elke relevante menu-item. Ga vervolgens naar **Magazijnbeheer \> Instellen \> Medewerker** en stel het veld **Limiet correctiehoeveelheid** in voor elke relevante magazijnmedewerker om de maximale correctiehoeveelheid op te geven die de werknemer kan registreren.

## <a name="processing-that-uses-counting-reason-codes"></a>Verwerking waarbij redencodes voor telling worden gebruikt

Wanneer medewerkers de mobiele app Warehouse Management gebruiken, worden de redencodes geregistreerd. Alleen als er een goedkeuringsproces voor telling is gedefinieerd, worden de geregistreerde redencodes onmiddellijk gebruikt als onderdeel van de tellijstboeking die volgt.

### <a name="cycle-count-approvals"></a>Cyclustelling goedkeuren

Voordat een telling wordt goedgekeurd, kan de medewerker de redencode wijzigen die is gekoppeld aan de telling. Als de telling is goedgekeurd, wordt de redencode ingevoerd in de regels van de tellijst.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Redencodes wijzigen voor goedkeuringen van cyclustellingen

Als u een goedkeuring voor een cyclustelling wilt wijzigen, gaat u als volgt te werk.

1. Ga naar **Magazijnbeheer** \> **Cyclustelling** \> **Cyclustellingswerk in afwachting van controle**.
1. Selecteer een cyclustelling in het raster.
1. Selecteer in het actievenster op het tabblad **Werk** de optie **Cyclustelling**. Selecteer vervolgens in het veld **Redencode** een nieuwe redencode.

Redencodes worden toegevoegd aan de regels in tellijsten van het type *tellijst*.

1. Ga naar **Voorraadbeheer** \> **Journaalboekingen** \> **Artikeltelling** \> **Tellen**.
2. Selecteer in de regeldetails van de teljournaal in het veld **Redencode voor telling** de redencode die overeenkomt met uw huidige situatie.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>De redencodes weergeven die in de telhistorie zijn vastgelegd

Volg deze stappen om de redencodes weer te geven die in de telhistorie zijn vastgelegd.

1. Ga naar **Voorraadbeheer** \> **Query's en rapporten** \> **Telhistorie**.
1. Selecteer een artikeltellingsrecord in het lijstvenster.
1. Bekijk in het veld **Redencode voor telling** de telhistorie die is vastgelegd via een redencode.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Redencodes gebruiken voor hoeveelheidscorrectie of online telling

Volg deze stappen om een redencode te gebruiken voor een hoeveelheidscorrectie of online telling.

1. Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.
1. Selecteer in het actievenster de optie **Hoeveelheidscorrectie**.
1. Selecteer **Hoeveelheidscorrectie** en selecteer in het veld **Redencode voor telling** een redencode.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
