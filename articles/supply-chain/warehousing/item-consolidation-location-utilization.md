---
title: Locatiegebruik bij artikelconsolidatie
description: Dit onderwerp bevat informatie over de functionaliteit waarmee magazijnbeheerders het volumetrische gebruik van locaties in het magazijn kunnen weergeven en filteren. Managers kunnen locaties selecteren en voorraadmutaties uitvoeren, rechtstreeks vanaf de pagina Artikelconsolidatie om artikelen te consolideren en zodoende de magazijnruimte beter te gebruiken.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3b20b41d27e5faeac7ea88940c086ae33390dc29
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217000"
---
# <a name="item-consolidation---location-utilization"></a>Locatiegebruik bij artikelconsolidatie

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over de functionaliteit waarmee magazijnbeheerders het volumetrische gebruik van locaties in het magazijn kunnen weergeven en filteren. Managers kunnen locaties selecteren en voorraadmutaties uitvoeren, rechtstreeks vanaf de pagina **Artikelconsolidatie** om artikelen te consolideren en zodoende de magazijnruimte beter te gebruiken.

## <a name="turn-on-the-features"></a>De functies inschakelen

Voordat u de in dit onderwerp beschreven functies kunt gebruiken, moet u deze in het systeem inschakelen. Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en deze zo nodig in te schakelen. Schakel de beide volgende functies in in de volgorde waarin ze worden vermeld. (Beide functies zijn voor de module **Magazijnbeheer**.)

1. Status magazijnlocatie
2. Locatiegebruik artikelconsolidatie

## <a name="warehouse-location-status"></a>Status magazijnlocatie

Met de functie *Status magazijnlocatie* kunt u vier nieuwe velden toevoegen aan de pagina **Locaties** om extra informatie over de huidige staat van de locatie bij te houden:

- **Artikelnummer:** Het artikel dat zich momenteel op de locatie bevindt. Als de locatie meerdere artikelen bevat, is dit veld leeg.
- **Datum en tijd van de laatste activiteit:** De tijdstempel van de laatste magazijntransactie die is uitgevoerd op de locatie.
- **Ouderdomsdatum:** De datum waarop de voorraad op de locatie in het magazijn is binnengebracht. Deze datum wordt berekend op basis van de ouderdomsdatum van de nummerplaat. Deze waarde is nauwkeurig voor locaties die met een nummerplaat worden gevolgd, maar mogelijk niet juist voor locaties die niet worden gevolgd met een nummerplaat.
- **Locatiestatus:** De status van de locatie. Er zijn vier waarden beschikbaar:

    - **Onbepaald:** het locatieprofiel kan de status niet bijhouden. Daarom is de huidige status onbekend.
    - **Leeg:** er is momenteel geen voorraad op de locatie.
    - **Orderverzameling:** uitgaande transacties zijn uitgevoerd op de locatie nadat deze voor het laatst leeg was.
    - **Opslag:** alleen ingaande transacties zijn uitgevoerd sinds de locatie voor het laatst leeg was.

Met behulp van deze velden kunnen magazijnbeheerders een beter overzicht krijgen van de status van de magazijnlocaties. Ze bieden ook meer mogelijkheden voor geavanceerde rapportage en filteren.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Artikelconsolidatie en locatiegebruik instellen

In deze sectie wordt beschreven hoe u uw systeem voorbereidt op het gebruik van artikelconsolidatie en locatiegebruik. In de procedures worden voorbeeldwaarden uit de standaard demogegevens gebruikt. Als u het voorbeeldscenario dat verderop in dit onderwerp wordt beschreven wilt doorlopen, selecteert u de rechtspersoon **USMF** (die de standaard demogegevens bevat) en maakt u elke record die in deze sectie wordt beschreven. Als u het voorbeeldscenario niet wilt doorlopen, kunt u de waarden die hier worden opgegeven, beschouwen als voorbeelden van de typen instellingen die u moet voltooien om de functies te kunnen gebruiken.

### <a name="released-product"></a>Vrijgegeven product

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer **M9201** in het veld *Artikelnummer* en open de pagina Details.
1. Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Fysieke afmetingen**.
1. Selecteer op de pagina **Fysieke afmetingen** in het actievenster de optie **Nieuw**.

    Er wordt een nieuwe regel aan het raster toegevoegd. Het veld **Artikelnummer** is vooraf ingesteld.

1. Selecteer **ea** in het veld *Eenheid*. De resterende velden op de regel worden automatisch ingesteld.
1. Selecteer **Opslaan** en sluit de pagina.

### <a name="location-profile"></a>Locatieprofiel

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer in de lijst met locatieprofielen de waarde **FLOOR-05**.
1. Selecteer **Bewerken** in het actievenster.
1. Controleer op het sneltabblad **Algemeen** of beide volgende opties zijn ingesteld op *Ja*:

    - Artikel in locatie inschakelen
    - Locatiestatus inschakelen

1. Selecteer **Opslaan**.

    > [!IMPORTANT]
    > Als de opties **Artikel in locatie inschakelen** en **Locatiestatus inschakelen** al zijn ingesteld op *Ja*, gaat u verder met de instructies voor het instellen van het sneltabblad **Dimensies** in stap 10. Als de opties nog niet zijn ingesteld op *Ja*, moet u een consistentiecontrole uitvoeren voor de module **Magazijnbeheer**, nadat u deze handmatig hebt ingesteld. Ga in dat geval verder met de volgende stap.

1. Als u de consistentiecontrole wilt uitvoeren, gaat u naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole**.
1. Stel in het dialoogvenster **Consistentiecontrole** de volgende waarden in:

    - **Module:** *Magazijnbeheer*
    - **Controleren/corrigeren:** *Controleren*
    - **Begindatum:** laat dit veld leeg.
    - **Consistentiecontrole status magazijnlocatie:** schakel dit selectievakje in.

1. Selecteer **OK**.

    > [!TIP]
    > U ontvangt een melding wanneer de consistentiecontrole is voltooid. Open het [Actiecentrum](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) om het bericht weer te geven. Selecteer **Berichtdetails** om de details weer te geven.
    >
    > Als het bericht voor de consistentiecontrole als volgt luidt: 'Onjuiste locatiestatus gevonden voor locatie XXXX in magazijn XX', moet u de consistentiecontrole opnieuw uitvoeren. Stel het veld **Controleren/corrigeren** nu in op *Fout oplossen*. Geef de berichten weer om er zeker van te zijn dat er geen fouten zijn gevonden.

1. U moet nu het instellen van het locatieprofiel voltooien. Ga terug naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatieprofielen**, selecteer locatieprofiel **FLOOR-05** en selecteer vervolgens **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Dimensies** de volgende waarden in:

    - **Volumegebruikspercentage:** *100*
    - **Volumetrische methode gebruikt voor voorraadlocatie:** *Locatievolume gebruiken*
    - **Werkelijke locatiehoogte:** *10*
    - **Werkelijke locatiebreedte:** *10*
    - **Werkelijke locatiediepte:** *10*
    - **Maximumgewicht:** *100*

1. Selecteer **Opslaan**.

### <a name="mobile-device-menu-items"></a>Menuopties voor mobiel apparaat

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het actievenster de optie **Nieuw** om een menuoptie te maken voor sorteren.
1. Stel in de header de volgende waarden in:

    - **Naam menuopdracht:** *Correctie in*
    - **Titel:** *Correctie in*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Nee*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Procedure voor het maken van werk:** *Correctie in*
    - **Voorraadcorrectietypen:** *Correctie in*

1. Selecteer **Opslaan**.

### <a name="mobile-device-menu"></a>Menu voor mobiel apparaat

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer in de lijst met menu's de waarde **Voorraad**.
1. Selecteer **Bewerken** in het actievenster.
1. Zoek en selecteer in de lijst **Beschikbare menu's en menuopdrachten** de menuopdracht **Correctie in**.
1. Selecteer de knop pijl-rechts om **Correctie in** naar de lijst **Menustructuur** te verplaatsen. Op deze manier voegt u de nieuwe menuopdracht toe aan het geselecteerde menu.
1. Selecteer **Opslaan**.

### <a name="movement-types"></a>Mutatietypen

1. Ga naar **Magazijnbeheer \> Instellingen \> Voorraad \> Mutatietypen**.
1. Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:

    - **Code mutatietype:** *CONSOLIDEREN*
    - **Omschrijving:** *Locaties consolideren*
    - **Werkklasse-id:** *InvMov*

1. Selecteer **Opslaan**.

## <a name="example-scenario"></a>Voorbeeldscenario

In het volgende scenario wordt de magazijnapp op een mobiel apparaat gebruikt om een *aanpassing in* voor de voorraad in te stellen op twee locaties in het magazijn.

### <a name="add-inventory-to-locations"></a>Voorraad toevoegen aan locaties

1. Meld u aan bij het mobiele apparaat als een gebruiker met instellingen voor magazijn *51*.
1. Ga naar **Voorraad \> Correctie in**.

    U gaat nu de eerste locatiecorrectie invoeren.

1. Selecteer in de taak **Correctie in** de locatie waarvoor u de voorraadcorrectie wilt uitvoeren. Selecteer **LP-001** in het veld *LOC*.
1. Bevestig de locatie.
1. Maak een nummerplaat-id voor het artikel dat aan de locatie wordt toegevoegd. Voer in het veld **LP** de waarde *LP00101* in.
1. Bevestig de nummerplaat.
1. Voer het artikel in dat aan de nummerplaat wordt toegevoegd. Voer in het veld **ITEM** de waarde *M9201* in.
1. Bevestig het artikel.
1. Voer de hoeveelheid in van het artikel dat wordt toegevoegd. Typ **10** in het veld *Hoeveelheid*.
1. Bevestig de hoeveelheid.

    U ontvangt de melding Werk voltooid. U gaat nu de tweede locatiecorrectie invoeren.

1. Selecteer in de taak **Correctie in** de locatie waarvoor u de voorraadcorrectie wilt uitvoeren. Selecteer **LP-002** in het veld *LOC*.
1. Bevestig de locatie.
1. Maak een nummerplaat-id voor het artikel dat aan de locatie wordt toegevoegd. Voer in het veld **LP** de waarde *LP00201* in.
1. Bevestig de nummerplaat.
1. Voer het artikel in dat aan de nummerplaat wordt toegevoegd. Voer in het veld **ITEM** de waarde *M9201* in.
1. Bevestig het artikel.
1. Voer de hoeveelheid in van het artikel dat wordt toegevoegd. Voer **15** in in het veld *Hoeveelheid*.
1. Bevestig de hoeveelheid.

    U ontvangt de melding Werk voltooid.

1. Tik op de menuknop boven aan de pagina (ook wel aangeduid als de hamburger of de hamburgerknop) en selecteer **Annuleren** om de taak **Correctie in** af te sluiten.

### <a name="consolidate-locations"></a>Locaties consolideren

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Artikelconsolidatie**.
1. Selecteer in de header een magazijn waarvoor u de consolidatie wilt uitvoeren. Typ **51** in het veld *Magazijn*.

    Er wordt een record weergegeven voor elke locatie waar artikel *M9201* is gecorrigeerd. In de kolom **Gebruikspercentage** wordt de volumetrische capaciteit van elke locatie weergegeven.

1. Als u de voorraad wilt consolideren, selecteert u alle locaties die moeten worden geconsolideerd en vervolgens selecteert u in het actievenster **Voorraad consolideren**.
1. Geef in het dialoogvenster **Voorraad consolideren** de locatie en het mutatietype op die moeten worden gebruikt om het werk voor de voorraadmutatie te maken. Stel de volgende waarden in:

    - **Locatie:** *LP-001*
    - **Code mutatietype:** *CONSOLIDEREN*

1. Selecteer **OK**.
1. U ontvangt een informatieve melding de het mutatiewerk is gemaakt. Noteer de werk-id van de mutatie.

### <a name="view-movement-work"></a>Mutatiewerk weergeven

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Geef het werk weer dat is gemaakt. Gebruik de id van het mutatiewerk van de voorraadconsolidatie om het werkraster te filteren of te doorzoeken.

    In dit scenario wordt een bestaande locatie met voorraad gebruikt als de voorraadconsolidatielocatie. Er is daarom slechts één werk-id gemaakt.

    > [!NOTE]
   > Het systeem maakt voor elke verplaatsing één werk-id die moet worden voltooid. Als u een locatie opgeeft die al een voorraad bevat, wordt er slechts één werk-id gemaakt. Als u een nieuwe locatie opgeeft, worden er twee werk-Id's gemaakt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]