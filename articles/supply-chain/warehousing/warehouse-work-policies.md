---
title: Werkbeleidsregels
description: In dit onderwerp wordt uitgelegd u werkbeleidsregels instelt.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 530abffb4c80a2d2f0e58e0c5a34294f7cba0b1a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998448"
---
# <a name="work-policies"></a>Werkbeleidsregels

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u het systeem en de magazijn-app instelt zodat deze werkbeleidsregels ondersteunen. Met deze functie kunt u de voorraad snel registreren zonder wegzetwerk te maken wanneer u inkoop- of transferorders ontvangt of wanneer u productieprocessen voltooit. Dit onderwerp biedt algemene informatie. Zie voor gedetailleerde informatie over de ontvangst van nummerplaten [Nummerplaat ontvangen via de magazijnapp](warehousing-mobile-device-app-license-plate-receiving.md).

Met een werkbeleid wordt bepaald of magazijnwerk wordt gemaakt wanneer een geproduceerd artikel wordt gereedgemeld of wanneer goederen worden ontvangen via de magazijn-app. U stelt elk werkbeleid in door de voorwaarden te definiëren waaronder het beleid van toepassing is: de werkordertypen en -processen, de voorraadlocatie en (optioneel) de producten. Een inkooporder voor product *A0001* moet bijvoorbeeld worden ontvangen op locatie *RECV* in magazijn *24*. Later wordt het product verbruikt in een ander proces op locatie *RECV*. In dat geval kunt u een werkbeleid instellen om te voorkomen dat wegzetwerk wordt gemaakt wanneer een werknemer product *A0001* meldt als ontvangen op de locatie *RECV*.

> [!NOTE]
> - Voor een actief werkbeleid moet u minimaal één locatie definiëren op het sneltabblad **Voorraadlocaties** van de pagina **Werkbeleidsregels**. 
> - U kunt niet dezelfde locatie opgeven voor meerdere werkbeleidsregels.
> - Met de optie **Etiket afdrukken** voor menuopdrachten van mobiele apparaten wordt een nummerplaat afgedrukt tenzij werk is gemaakt.

## <a name="activate-the-features-in-your-system"></a>De functies in uw systeem activeren

Schakel de volgende twee functies in het [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in om alle functies die in dit onderwerp worden beschreven, beschikbaar te maken in uw systeem:

- Verbeteringen voor ontvangen van nummerplaten
- Verbeteringen in werkbeleid voor inkomend werk

## <a name="the-work-policies-page"></a>De pagina Werkbeleidsregels

Als u werkbeleid wilt instellen, gaat u naar **Magazijnbeheer \> Instellen \> Werk \> Werkbeleidsregels**. Stel vervolgens op elk sneltabblad de velden in zoals beschreven in de volgende subsecties.

### <a name="the-work-order-types-fasttab"></a>Het sneltabblad Werkordertypen

Voeg op het sneltabblad **Werkordertypen** alle werkordertypen en de bijbehorende werkprocessen toe waarop het werkbeleid van toepassing is. De volgende typen werkorders en gerelateerde werkprocessen worden ondersteund voor werkbeleidsregels.

| Werkordertype | Werkproces |
|---|---|
| Orderverzameling van grondstoffen| Alle gerelateerde processen |
| Coproducten en bijproducten wegzetten | Alle gerelateerde processen |
| Eindproducten wegzetten | Alle gerelateerde processen |
| Ontvangstbewijs voor overboeking | Nummerplaten ontvangen (en wegzetten) |
| Inkooporders | <ul><li>Nummerplaten ontvangen (en wegzetten)</li><li>Artikelontvangst laden (en wegzetten)</li><li>Inkooporderregels ontvangen (en wegzetten)</li><li>Inkooporderartikelen ontvangen (en wegzetten)</li></ul> |

Als u een werkbeleid zo wilt instellen dat het wordt toegepast op verschillende werkprocessen van hetzelfde type werkorder, voegt u een aparte regel voor elk werkproces toe aan het raster.

Voor elke regel in het raster stelt u het veld **Werkaanmaakmethode** in op een van de volgende waarden:

- **Nooit**: het werkbeleid voorkomt dat magazijnwerk wordt gemaakt voor het geselecteerde type werkorder en gerelateerde werkprocessen.
- **Cross-docken**: het werkbeleid maakt cross-docken mogelijk met behulp van het beleid dat u selecteert in het veld **Naam van beleid voor cross-docken**.

### <a name="the-inventory-locations-fasttab"></a>Het sneltabblad Voorraadlocaties

Voeg op het sneltabblad **Voorraadlocaties** alle locaties toe waarop dit werkbeleid moet worden toegepast. Als er geen locatie aan een werkbeleid is gekoppeld, wordt het werkbeleid niet op enig proces toegepast.

U kunt niet dezelfde locatie opgeven voor meerdere werkbeleidsregels.

U kunt een magazijnlocatie gebruiken die aan een locatieprofiel is toegewezen als de optie **Bijhouden nummerplaat gebruiken** is uitgeschakeld. In dit geval zullen werknemers de voorhanden voorraad rechtstreeks registreren.

### <a name="the-products-fasttab"></a>Het sneltabblad Producten

Stel op het tabblad **Producten** het veld **Productselectie** in om te bepalen voor welke producten het beleid moet gelden:

- **Alles**: het beleid moet van toepassing zijn op alle producten.
- **Geselecteerd**: het beleid moet alleen van toepassing zijn op producten die worden vermeld in het raster. Gebruik de werkbalk op het sneltabblad **Producten** om producten aan het raster toe te voegen of ze uit het raster te verwijderen.

## <a name="default-and-custom-to-locations"></a>Standaard en aangepaste "naar"-locaties

> [!NOTE]
> Om de functionaliteit die in deze sectie wordt beschreven beschikbaar te maken in uw systeem, moet u de functies *Verbeteringen voor nummerplaat ontvangen voor de mobiele magazijnapp* en *Verbeteringen in werkbeleid voor inkomend werk* inschakelen in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Voorheen bood het systeem alleen ondersteuning voor ontvangst op de standaardlocatie die voor elk magazijn is gedefinieerd. In menuopdrachten op mobiele apparaten die de volgende processen voor het maken van werk gebruiken, wordt nu de optie **Standaardgegevens gebruiken** weergegeven. Met deze optie kunt u een aangepaste 'naar'-locatie toewijzen aan een of meer menuopdrachten. (Deze optie was al beschikbaar voor enkele andere typen menuopdrachten.)

- Nummerplaten ontvangen (en wegzetten)
- Artikelontvangst laden (en wegzetten)
- Inkooporderregels ontvangen (en wegzetten)
- Inkooporderartikelen ontvangen (en wegzetten)

De **naar-locatie** voor een menuopdracht heeft voorrang op de standaardontvangstlocatie voor het magazijn, voor alle orders die met die menuoptie worden verwerkt.

Voer de volgende stappen uit om een menuopdracht voor een mobiel apparaat in te stellen voor ondersteuning van ontvangst op een aangepaste locatie.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer of maak een menuopdracht die gebruikmaakt van een van de werkprocessen die eerder in deze sectie zijn vermeld.
1. Stel op het sneltabblad **Algemeen** de optie **Standaardgegevens gebruiken** in op **Ja**.
1. Selecteer in het actiedeelvenster **Standaardgegevens**.
1. Stel op de pagina **Standaardgegevens** de volgende waarden in:

    - **Standaardgegevensveld:** stel dit veld in op *Naar locatie*.
    - **Magazijn:** selecteer het doelmagazijn dat u wilt gebruiken met deze menuopdracht.
    - **Locatie:** dit veld bevat alle locatie-id's die beschikbaar zijn voor het geselecteerde magazijn. De instelling van dit veld heeft echter geen effect. U kunt dit veld daarom leeg laten. U kunt echter de lijst gebruiken om de id te bevestigen die u moet invoeren in het veld **Hardgecodeerde waarde**.
    - **Hardgecodeerde waarde:** hier kunt u de locatie-id invoeren voor de ontvangstlocatie die van toepassing is op deze menuopdracht.

> [!TIP]
> Een werkbeleid kan alleen worden toegepast als alle ontvangstlocaties in de relevante instellingen van het werkbeleid worden vermeld. Deze behoefte geldt ongeacht of u de standaardmagazijnontvangstlocatie of een aangepaste 'naar'-locatie gebruikt.

## <a name="example-scenario-warehouse-receiving"></a>Voorbeeldscenario: magazijnontvangsten

Alle producten die worden ontvangen door het proces *Inkooporderartikelen ontvangen (en wegzetten)* moeten worden geregistreerd op locatie *FL-001* en ze moeten beschikbaar zijn in magazijn *24*. Er moet echter geen werk worden gemaakt. Producten die worden ontvangen door een ander proces (dat wil zeggen via andere menu-items van het mobiele apparaat) moeten worden geregistreerd op de standaardmagazijnontvangstlocatie (*RECV*) en werk moet op de gebruikelijke manier worden gemaakt. (In dit scenario worden de standaardinstellingen voor het ontvangen niet weergegeven.)

Voor dit scenario zijn de volgende elementen vereist:

- Een werkbeleid voor het proces *Inkooporderartikelen ontvangen (en wegzetten)* op locatie *FL-001* voor alle producten
- Een menuopdracht voor een mobiel apparaat die standaardgegevens bevat en waarmee het veld **Naar locatie** wordt ingesteld op *FL-001*

### <a name="prerequisites"></a>Vereisten

Om de functionaliteit die in dit scenario wordt beschreven beschikbaar te maken in uw systeem, moet u de functies *Verbeteringen voor nummerplaat ontvangen voor de mobiele magazijnapp* en *Verbeteringen in werkbeleid voor inkomend werk* inschakelen in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

In dit scenario worden de standaarddemogegevens gebruikt. Als u dit scenario wilt doorlopen met de waarden die hier worden gebruikt, moet u werken op een systeem waarop demogegevens zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren.

### <a name="set-up-a-work-policy"></a>Een werkbeleid instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkbeleidsregels**.
1. Selecteer **Nieuw**.
1. Voer in het veld **Werkbeleidsnaam** *Geen wegzetwerk voor inkoopartikel* in.
1. Selecteer **Opslaan**.
1. Selecteer op het sneltabblad **Werkordertypen** **Toevoegen** om een rij aan het raster toe te voegen en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - **Werkordertype:** *Inkooporders*
    - **Werkproces:** *Inkooporderartikelen ontvangen (en wegzetten)*
    - **Werkaanmaakmethode:** *Nooit*
    - **Naam van beleid voor cross-docken:** laat dit veld leeg.

1. Selecteer op het sneltabblad **Voorraadlocaties** **Toevoegen** om een rij aan het raster toe te voegen en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - **Magazijn:** *24*
    - **Locatie:** *FL-001*

1. Stel op het sneltabblad **Producten** het veld **Productselectie** in op *Alle*.
1. Selecteer **Opslaan**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Een menu-item voor een mobiel apparaat instellen om de locatie van de ontvangst te wijzigen

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer de bestaande menuopdracht **Inkoop ontvangen** in het linkerdeelvenster.
1. Stel op het sneltabblad **Algemeen** de optie **Standaardgegevens gebruiken** in op *Ja*.
1. Selecteer **Opslaan**.
1. Selecteer in het actiedeelvenster **Standaardgegevens**.
1. Selecteer op de pagina **Standaardgegevens** in het actievenster **Nieuw** om een rij aan het raster toe te voegen en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - **Standaardgegevensveld:** *Naar locatie*
    - **Magazijn:** *24*
    - **Locatie:** laat dit veld leeg.
    - **Hardgecodeerde waarde:** *FL-001*

1. Selecteer **Opslaan**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Een inkooporder ontvangen zonder werk te maken

Het voorbeeld in deze sectie laat zien hoe u een inkooporderartikel ontvangt, zonder dat er werk wordt gemaakt op een locatie die verschilt van de standaardlocatie voor ontvangst die voor het magazijn is ingesteld. In dit voorbeeld worden het werkbeleid en de optie voor mobiele apparaten gebruikt die u eerder in dit scenario hebt gemaakt.

#### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw**.
1. Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:

    - **Leveranciersrekening:** *US-101*
    - **Locatie:** *2*
    - **Magazijn:** *24*

1. Selecteer **OK** om het dialoogvenster te sluiten en de nieuwe inkooporder te openen.
1. Stel op het sneltabblad **Inkooporderregels** de volgende waarden in voor de lege rij:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *1*

1. Selecteer **Opslaan**.
1. Noteer het nummer van de inkooporder.

#### <a name="receive-a-purchase-order"></a>Een inkooporder ontvangen

1. Meld u op het mobiele apparaat aan bij magazijn *24* met *24* als de gebruikersnaam en *1* als het wachtwoord.
1. Selecteer **Inkomend**.
1. Selecteer **Inkoop ontvangen**. Het veld **Locatie** moet worden ingesteld op *FL-001*.
1. Voer het inkoopordernummer in voor de inkooporder die u hebt gemaakt in de vorige procedure.
1. Voer in het veld **Artikelnummer** *A0001* in.
1. Selecteer **OK**.
1. Typ **1** in het veld *Hoeveelheid*.
1. Selecteer **OK**.

De inkooporder wordt nu ontvangen, maar er wordt geen werk aan gekoppeld. De voorhanden voorraad is bijgewerkt en een hoeveelheid van *1* van artikel *A0001* is nu beschikbaar op locatie *FL-001*.

## <a name="example-scenario-manufacturing"></a>Voorbeeldscenario: productie

In het volgende voorbeeld zijn er twee productieorders: *PRD-001* en *PRD-002*. Productieorder *PRD-001* heeft een bewerking met de naam *Assembly*, waarbij product *SC1* aan locatie *001* wordt gereedgemeld. Productieorder *PRD-002* heeft een bewerking met de naam *Verven* en verbruikt product *SC1* van locatie *001*. Productieorder *PRD-002* verbruikt ook grondstof *RM1* van locatie *001*. Grondstof *RM1* is opgeslagen in magazijnlocatie *BULK-001* en wordt verzameld op locatie *001* door magazijnwerk voor het verzamelen van grondstoffen. Het verzamelwerk wordt gegenereerd wanneer productie *PRD-002* wordt vrijgegeven.

[![Werkbeleid magazijn](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Wanneer u de configuratie van een werkbeleid voor magazijnen voor dit scenario plant, moet u rekening houden met het volgende:

- Magazijnwerk voor wegzetten van afgewerkte goederen is niet vereist wanneer u product *SC1* van productieorder *PRD-001* gereed meldt voor locatie *001*. De reden is dat de bewerking *Verven* voor productieorder *PRD-002* product *SC1* op dezelfde locatie verbruikt.
- Magazijnwerk voor het verzamelen van grondstoffen is vereist om grondstof *RM* 1 van magazijnlocatie *BULK-001* naar locatie *001* te verplaatsen.

Hier is een voorbeeld van een werkbeleid dat u kunt instellen, op basis van deze overwegingen:

- **Werkbeleidsnaam:** *Geen wegzetwerk*
- **Werkordertypen**: *Afgewerkte goederen wegzetten* en *Coproducten en bijproducten wegzetten*
- **Voorraadlocaties:** magazijn *51* en locatie *001*
- **Producten:** *SC1*

In het volgende voorbeeldscenario vindt u stapsgewijze instructies voor het instellen van het beleid voor magazijnwerk voor dit scenario.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Voorbeeldscenario: gereedmelden naar een locatie die niet wordt beheerd op nummerplaat

Dit scenario toont een voorbeeld waarin een productieorder gereed wordt gemeld naar een locatie die niet wordt beheerd op nummerplaat.

In dit scenario worden de standaarddemogegevens gebruikt. Als u dit scenario wilt doorlopen met de waarden die hier worden gebruikt, moet u werken op een systeem waarop demogegevens zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren.

### <a name="set-up-a-warehouse-work-policy"></a>Een magazijnwerkbeleid instellen

In magazijnprocessen wordt niet altijd magazijnwerk opgenomen. Door een werkbeleid te definiëren kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkbeleidsregels**.
1. Selecteer **Nieuw**.
1. Voer in het veld **Werkbeleidsnaam** *Geen wegzetwerk* in.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Werkordertypen** **Toevoegen** om een rij aan het raster toe te voegen en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - **Werkordertype**: *afgewerkte producten wegzetten*
    - **Werkproces:** *alle gerelateerde werkprocessen*
    - **Werkaanmaakmethode:** *Nooit*
    - **Naam van beleid voor cross-docken:** laat dit veld leeg.

1. Selecteer nogmaals **Toevoegen** om een tweede rij aan het raster toe te voegen en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - **Werkordertype:** *Coproducten en bijproducten wegzetten*
    - **Werkproces:** *alle gerelateerde werkprocessen*
    - **Werkaanmaakmethode:** *Nooit*
    - **Naam van beleid voor cross-docken:** laat dit veld leeg.

1. Selecteer op het sneltabblad **Voorraadlocaties** **Toevoegen** om een rij aan het raster toe te voegen en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - **Magazijn:** *51*
    - **Locatie:** *001*

1. Stel op het sneltabblad **Producten** het veld **Productselectie** in op *Geselecteerd*.
1. Selecteer op het sneltabblad **Producten** de optie **Toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe rij het veld **Artikelnummer** in op *L0101*.
1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-an-output-location"></a>Een uitvoerlocatie instellen

1. Ga naar **Organisatiebeheer \> Resources \> Resourcegroepen**.
1. Selecteer in het linkerdeelvenster resourcegroep **5102**.
1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Uitvoermagazijn:** *51*
    - **Uitvoerlocatie:** *001*

1. Selecteer **Opslaan** in het actievenster.

> [!NOTE]
> Locatie *001* is geen door nummerplaten beheerde locatie. U kunt een uitvoerlocatie die niet door nummerplaten wordt beheerd, alleen instellen als er een toepasselijk werkbeleid voor de locatie bestaat.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Een productieorder maken en gereedmelden

1. Ga naar **Productiebeheer \> Productieorders \> Alle productieorders**.
1. Selecteer **Nieuwe productieorder** in het actievenster.
1. Stel in het dialoogvenster **Productieorder maken** het **artikelnummer** in op *L0101*.
1. Selecteer **Maken** om het dialoogvenster te sluiten en de verkooporder te maken.

    Er wordt een nieuwe productieorder toegevoegd aan het raster op de pagina **Alle productieorders**.

    Houd de nieuwe productieorder geselecteerd.

1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Raming**.
1. Lees de raming in het dialoogvenster **Raming** en selecteer vervolgens **OK** om het dialoogvenster te sluiten.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Start**.
1. Stel in het dialoogvenster **Start** op het tabblad **Algemeen** het veld **Automatisch stuklijstverbruik** in op *Nooit*.
1. Selecteer **OK** om de instelling op te slaan en het dialoogvenster te sluiten.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Rapporteren als gereed**.
1. Stel in het dialoogvenster **Rapporteren als gereed** op het tabblad **Algemeen** de optie **Fout accepteren** in op *Ja*.
1. Selecteer **OK** om de instelling op te slaan en het dialoogvenster te sluiten.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Algemeen** de optie **Werkgegevens**.

Wanneer de productieorder gereedgemeld wordt, wordt er geen werk gegenereerd voor wegzetten. Deze werking komt doordat er een werkbeleid is gedefinieerd waarmee wordt voorkomen dat werk wordt gegenereerd wanneer product *L0101* wordt gereedgemeld bij locatie *001*.

## <a name="more-information"></a>Meer informatie

Zie [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md) voor meer informatie over menuopties voor mobiele apparaten.

Zie voor meer informatie over de ontvangst van nummerplaten en werkbeleid [Nummerplaat ontvangen via de magazijnapp](warehousing-mobile-device-app-license-plate-receiving.md).

Zie [Magazijnverwerking van inkomende ladingen voor inkooporders](inbound-load-handling.md) voor meer informatie over het beheer van inkomende ladingen.
