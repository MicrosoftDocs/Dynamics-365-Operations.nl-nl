---
title: Productdimensies op locaties combineren
description: Dit onderwerp biedt informatie over het combineren van productdimensies op locaties. Deze functionaliteit voor locatieprofielen helpt het locatiebeheer te verbeteren wanneer productvarianten of producten met dimensies worden gebruikt, zoals in de kledingsector. Hiermee kunt u bepalen of configuraties, kleuren, stijlen en formaat kunnen worden gecombineerd voor een bepaald locatieprofiel, of dat een van deze dimensies of een combinatie van deze dimensies op dezelfde locatie kan worden geplaatst.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425766"
---
# <a name="location-product-dimension-mixing"></a>Productdimensies op locaties combineren

[!include [banner](../includes/banner.md)]

Productdimensies op locaties combineren is functionaliteit voor locatieprofielen die helpt het locatiebeheer te verbeteren wanneer productvarianten of producten met dimensies worden gebruikt, zoals in de kledingsector. Hiermee kunt u bepalen of configuraties, kleuren, stijlen en formaat kunnen worden gecombineerd voor een bepaald locatieprofiel, of dat een van deze dimensies of een combinatie van deze dimensies op dezelfde locatie kan worden geplaatst.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>De functie voor het combineren van productdimensies op locaties inschakelen

Voordat u de functie Combineren van productdimensies op locaties kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Combineren van productdimensies op locaties*

## <a name="setup"></a>Instellen

Aan elke locatie in het magazijn moet een locatieprofiel zijn gekoppeld, dat de eigenschappen beschrijft van de locatie. Dit betekent dat alle locaties die hetzelfde locatieprofiel gebruiken, de productdimensie kunnen combineren nadat deze is ingesteld.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Locatieprofielen configureren om combinaties van productdimensies toe te staan

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer in de lijst met locatieprofielen de waarde **BULK**.
1. Selecteer **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Algemeen** de optie **Productdimensie-specifiek combineren op locatie inschakelen** in op *Ja*.

    > [!NOTE]
    > U kunt deze optie alleen op *Ja* instellen als de optie **Gemengde artikelen toestaan** is ingesteld op *Nee*.

1. Stel op het sneltabblad **Toegestane productdimensiecombinaties** de optie **Formaat** in op *Ja*. In het scenario dat in dit onderwerp wordt beschreven, kan combineren alleen worden uitgevoerd voor producten met een verschillende dimensies voor **Formaat**. Er zijn echter ook andere opties beschikbaar.
1. Selecteer **Opslaan**.

### <a name="create-a-new-product-master-and-product-variants"></a>Een nieuw productmodel en productvarianten maken

1. Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**.
1. Selecteer in het actievenster **Nieuw** om een productmodel te maken.
1. Stel in het dialoogvenster **Nieuw product** de volgende waarden in:

    - **Producttype:** *Artikel*
    - **Subtype van product:** *Productmodel*
    - **Productnummer:** *B0001*
    - **Productnaam:** *B0001 Formaat*
    - **Productdimensiegroep:** *Formaat*
    - **Configuratietechnologie:** *Vooraf gedefinieerde variant*

1. Selecteer **OK**.
1. Stel op de pagina **Productgegevens** op het sneltabblad **Algemeen** de volgende waarden in:

    - **Varianten automatisch genereren:** *Ja*
    - **Formaatgroep:** *CASUALDHIR*

1. Als u de vooraf gedefinieerde varianten wilt weergeven, selecteert u in het actievenster **Productvarianten**.

    De pagina **Productvarianten** wordt geopend met een lijst met varianten uit de configuratie van de groep Formaat.

### <a name="release-products-to-the-usmf-company"></a>Producten vrijgeven aan het bedrijf USMF

1. Selecteer in het actievenster **Producten vrijgeven**.
1. Controleer op de pagina **Producten voor vrijgave selecteren** of het productnummer *B0001* in de lijst staat en selecteer **Volgende**.
1. Selecteer **Volgende** om de productvarianten te bevestigen die u wilt vrijgeven.
1. Selecteer op de pagina **Bedrijven selecteren waarnaar wordt vrijgegeven** de optie *USMF* en selecteer **Volgende** om de selectie te bevestigen.
1. Selecteer op de pagina **Selectie bevestigen** de optie **Voltooien** om de release te voltooien.

    De melding "Bewerking voltooid" wordt getoond.

### <a name="update-a-released-product-in-the-usmf-company"></a>Een vrijgegeven product in het bedrijf USMF bijwerken

1. Zorg ervoor dat u bent aangemeld bij het bedrijf **USMF**.
1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten** om het aanmaken van het vrijgegeven product af te ronden.
1. Zoek en selecteer het artikelnummer *B0001* om de pagina **Details van vrijgegeven product** te openen.
1. Selecteer **Bewerken** in het actievenster.
1. Controleer op het sneltabblad **Algemeen** of het veld **Artikelmodelgroep** is ingesteld op *FIFO*.
1. Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Dimensiegroepen**.
1. Stel de volgende waarden in:

    - **Opslagdimensiegroep:** *Artikelen*
    - **Traceringsdimensiegroep:** *Geen*

1. Selecteer **OK**.
1. Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Reserveringshiërarchie**.
1. Stel het veld **Reserveringshiërarchie** in op *Standaard* en selecteer **OK**.
1. Op het sneltabblad **Algemeen** in de sectie **Beheer** ziet u dat de selecties zijn bijgewerkt.
1. Ga naar het sneltabblad **Inkopen** en voer in het veld **Prijs** de waarde *10* in.
1. Voer op het sneltabblad **Kosten beheren** in het veld **Artikelgroep** de waarde *Audio* in.
1. Ga naar het sneltabblad **Inkopen** en voer in het veld **Prijs** de waarde *10* in.
1. Geef op het sneltabblad **Magazijn** in het veld **Eenheidvolgordegroep-id** de waarde *ea* op.
1. Selecteer **Opslaan**.

### <a name="create-a-location-directive"></a>Maak een locatie-richtlijn.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Selecteer in het linkerdeelvenster in het veld **Werkordertype** de waarde *Inkooporders*.
1. Selecteer in de lijst de locatie-instructie met de naam *24 PO Direct*.
1. Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Volgnummer:** *1*

        De nieuwe regel moet vóór de eerder bestaande regel staan. Om de posities te wijzigen, gebruikt u de knoppen **Omhoog** en **Omlaag** op de werk balk, of u wijzigt de waarde van het **volgnummer** van de bestaande regel in *2*.

    - **Naam:** *Locatieprofiel wegzetten naar BULK*
    - **Gebruik vaste locaties:** *Vaste en niet-vaste locaties*
    - **Negatieve voorraad toestaan:** *Schakel dit selectievakje uit (= Nee)*
    - **Batch ingeschakeld:** *Schakel dit selectievakje uit (= Nee)*
    - **Strategie:** *Geen*

1. Selecteer de optie **Query bewerken** boven het raster terwijl de nieuwe regel nog steeds is geselecteerd.
1. Selecteer in het querydialoogvenster op het tabblad **Bereik** de optie **Toevoegen** om een regel aan het raster toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Afgeleide tabel:** *Locaties*
    - **Veld:** *Locatieprofiel-id*
    - **Criteria:** *BULK*

1. Selecteer **OK**.
1. Selecteer in het actievenster op de pagina **Locatie-instructies** **Opslaan**.

> [!NOTE]
> Ga naar het sneltabblad **Locatie-instructieactie**. Als u in het veld **Strategie** de locatiestrategie *Samenvoegen* gebruikt, wordt de configuratie van het snelttabblad **Toegestane productdimensiecombinaties** in de **Locatieprofielen** overschreven. Artikelen worden dan weggezet op dezelfde locatie, ook als dit gedrag niet is toegestaan volgens de configuratie.

### <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het actievenster de optie **Nieuw** om een menuoptie te maken dat u wilt gebruiken voor sorteren.
1. Stel in de koptekst de volgende waarden in:

    - **Menuoptie:** *IO-regel ontvangst*
    - **Titel:** *IO-regel ontvangst*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Nee*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Proces van werkaanmaak:** *Ontvangen en wegzetten van inkooporderregel*
    - **Nummerplaat maken:** *Ja*

1. Selecteer **Opslaan**.

### <a name="configure-the-mobile-device-menu"></a>Het menu voor het mobiele apparaat configureren

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer in de lijst met menu's de waarde **Inkomend**.
1. Selecteer **Bewerken** in het actievenster.
1. Zoek en selecteer in de lijst **Beschikbare menu's en menuopdrachten** de menuopdracht **IO-regel ontvangst**.
1. Selecteer de knop pijl-rechts om de menu opdracht **IO-regel ontvangst** te verplaatsen naar de **lijst Menustructuur**. Op deze manier voegt u de nieuwe menuopdracht toe aan het geselecteerde menu.
1. Selecteer **Opslaan**.

## <a name="scenario"></a>Scenario's

In dit demoscenario wordt weergegeven hoe twee verschillende productvarianten op dezelfde locatie kunnen worden geplaatst, wanneer het locatieprofiel gecombineerde artikelen niet toestaat, maar de functie *Productdimensies op locaties combineren* is ingeschakeld. In dit geval gebruikt u de variant **Formaat** als criterium.

Voordat u begint, moet u controleren of er lege locaties in magazijn *24* zijn die gebruikmaken van het locatieprofiel *BULK*.

### <a name="create-a-purchase-order"></a>Inkooporder maken

U maakt een inkoop order met drie regels: twee regels voor hetzelfde productnummer , maar met verschillende varianten voor **Formaat** en een derde regel voor een ander product zonder varianten.

1. Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:

    - **Leverancieraccount:** *1001*
    - **Magazijn:** *24*

1. Selecteer **OK**.
1. De inkooporder wordt gemaakt en er wordt een nieuwe regel toegevoegd op het sneltabblad **Inkooporderregels**. Noteer het nummer van de inkooporder.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Artikelnummer:** *B0001*
    - **Formaat:** *L*
    - **Hoeveelheid:** *2*

1. Selecteer **Regel toevoegen** boven het raster om een tweede inkooporderregel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *B0001*
    - **Formaat:** *XL*
    - **Hoeveelheid:** *2*

1. Selecteer **Regel toevoegen** boven het raster om een derde inkooporderregel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *1*

9. Selecteer **Opslaan**.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Inkooporderregels ontvangen in de magazijnapp

1. Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *24*.
1. Selecteer het menu **Inkomend**.
1. Selecteer **IO-regel ontvangst**.
1. Selecteer het veld **PONUM** en voer vervolgens het inkoopordernummer in.
1. Bevestig uw invoer door te tikken op de knop Bevestigen (✔) onderaan de pagina.
1. Voer het regelnummer in van de inkooporder die u ontvangt. Selecteer het veld **LINENUM** en voer vervolgens *1* in door middel van het cijfertoetsenblok.
1. Bevestig uw invoer.
1. Voer de hoeveelheid in die u ontvangt. Selecteer de knop met het plusteken (**+**) twee keer om de waarde in het veld **Hoeveelheid** te verhogen naar *2*.
1. Registreer uw invoer door te tikken de knop (✔) onderaan de pagina en bevestig de invoer door opnieuw op de knop (✔) te tikken.
1. Bekijk de informatie op de pagina **Inkooporders: wegzetten**. Op deze pagina wordt het werk weergegeven dat is gemaakt voor het wegzetten (Werk 1).

    De locatie waar het ontvangen artikel wordt opgeslagen, de nummerplaat, het artikel, het formaat en de hoeveelheid van de taak **IO-order ontvangst** die u zojuist hebt voltooid, worden weergegeven.

1. Bevestig het wegzetwerk.
1. Herhaal stappen 4 tot en met 11 voor inkooporderregel 2. Geef echter in stap 8 als hoeveelheid *1* op.

    Nieuw wegzetwerk (Werk 2) wordt gemaakt voor dezelfde locatie als Werk 1.

1. Herhaal stappen 4 tot en met 11 opnieuw voor inkooporderregel 2. Geef echter in stap 8 als resterende hoeveelheid *1* op.

    Nieuw wegzetwerk (Werk 3) wordt gemaakt voor dezelfde locatie als Werk 1 en Werk 2. Dit gedrag treedt op omdat de locatie-instructiestrategie *Samenvoegen* wordt gebruikt en het sneltabblad **Toegestane productdimensiecombinaties** in de instellingen van de *Bulk*-**locatieprofielen** toestaat dat de variant **Formaat** op een locatie wordt gecombineerd.

1. Herhaal stappen 4 tot en met 11 voor inkooporderregel 3. Geef in stap 8 als hoeveelheid *1* op voor artikel nummer *A0001*.

    Nieuw wegzetwerk (Werk 4) worden gemaakt voor een andere locatie dan de locatie die wordt gebruikt voor inkooporderregels 1 en 2. Dit gedrag treedt op omdat het locatieprofiel niet toestaat dat producten worden gecombineerd, maar wel toestaat dat verschillende dimensies van hetzelfde productmodel worden gecombineerd.

1. Tik op de menuknop boven aan de pagina (ook wel aangeduid als de hamburger of de hamburgerknop) en selecteer **Annuleren** om **IO-regel ontvangst** af te sluiten.

> [!TIP]
> U kunt dit scenario herhalen. Stel deze keer **Formaat** - *Nee* in op het sneltabblad **Toegestane productdimensiecombinaties** op de *BULK*-**locatieprofielen**, zodat geen van de productdimensies kunnen worden gecombineerd. Wanneer u de inkooporder ontvangt, wordt in dit geval elke productvariant op een nieuwe locatie geplaatst.