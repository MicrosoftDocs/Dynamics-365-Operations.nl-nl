---
title: Wave-sjabloongroepering
description: Met de functie Wave-sjabloongroepering kan het systeem wave-sjabloonconfiguraties gebruiken om te bepalen, op basis van criteria die u definieert, hoe vrijgegeven regels moeten worden gesplitst en aan nieuwe of bestaande waves worden toegewezen. Deze functie kan handig zijn in magazijnen waar waves worden gemaakt op basis van specifieke criteria, maar waar managers liever automatisch waves laten maken in plaats van handmatig.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b422eb432e579d4ae914fbc0efa79aaa15f1de27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998373"
---
# <a name="wave-template-grouping"></a>Wave-sjabloongroepering

[!include [banner](../includes/banner.md)]

Met de functie Wave-sjabloongroepering kan het systeem [wave-sjabloon](tasks/configure-wave-processing.md)configuraties gebruiken om te bepalen, op basis van criteria die u definieert, hoe vrijgegeven regels moeten worden gesplitst en aan nieuwe of bestaande waves worden toegewezen. Deze functie kan handig zijn in magazijnen waar waves worden gemaakt op basis van specifieke criteria, maar waar managers liever automatisch waves laten maken in plaats van handmatig. Het systeem kan elke pas vrijgegeven zending toevoegen aan de eerste wave die wordt gevonden met overeenkomende groeperingsveldwaarden. Als geen overeenkomst wordt gevonden, maakt het systeem een nieuwe wave aan voor de nieuwe zending.

> [!IMPORTANT]
> Wave-sjabloongroepering wordt niet ondersteund voor de werktypen *verzamelen van grondstoffen voor produtie* of *kanbanorderverzamelen*. De reden hiervoor is dat de wavegroepering is gebaseerd op zendingen en dat deze werk typen geen zendingen gebruiken.

## <a name="turn-on-the-wave-template-grouping-feature"></a>De functie Wave-sjabloongroepering inschakelen

Voordat u de functie *Wave-sjabloongroepering* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Wave-sjabloongroepering*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Een wave-sjabloon instellen voor gebruik met wave-sjabloongroepering

Voer de volgende stappen uit om uw [wave-sjabloon in te stellen](tasks/configure-wave-processing.md) om wave-sjabloongroepering beschikbaar te maken.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Selecteer in het linkerdeelvenster de wave-sjabloon die u wilt instellen. Als u het scenario later in dit onderwerp wilt doorlopen met behulp van voorbeeldgegevens, selecteert u de sjabloon **62 Shipping default**.
1. Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Het maken van waves automatiseren:** *Ja*
    - **Toewijzen aan open waves:** *Ja*
    - **Wave verwerken bij vrijgave door magazijn:** *Nee*

1. Selecteer in het actievenster de optie **Query bewerken** het query-dialoogvenster te openen.
1. Bekijk in het querydialoogvenster op het tabblad **Sorteren** de sorteercriteria en zorg ervoor dat er een regel is die het veld bevat dat u wilt gebruiken om uw waves te groeperen.

    Als u het scenario wilt doorlopen met behulp van demogegevens, voegt u een rij toe die de volgende waarden bevat:

    - **Tabel:** *Zendingen*
    - **Afgeleide tabel:** *Zendingen*
    - **Veld:** *Vervoerdersservice*

        > [!NOTE]
        > Nadat u deze waarde hebt geselecteerd, kan de volgende melding worden weergegeven: "Vervoerdersservice is geen indexveld. Wilt u hieraan sortering toevoegen?" Selecteer **Ja** om sortering toe te voegen.

    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om de wijzigingen op te slaan en het querydialoogvenster te sluiten.
1. Selecteer in het actievenster de optie **Wave-sjabloongroepering**.
1. Schakel op de pagina **Wave-sjabloongroepering** het selectievakje **Groeperen op** in voor elke rij die u wilt gebruiken om de orderregels in waves te groeperen. Als u het scenario wilt doorlopen met behulp van voorbeeldgegevens, schakelt u het selectievakje **Groeperen op** in voor de rij *Vervoerderservice*.
1. Selecteer **Opslaan**.
1. Sluit de pagina **Wave-sjabloongroepering**.
1. Klik op **Opslaan** om de sjabloon op te slaan.

## <a name="scenario"></a>Scenario's

Deze sectie bespreekt een scenario waarmee u kunt leren wat de functie doet en hoe u ermee kunt werken.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt dit scenario ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt. In dat geval moet u echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.

### <a name="scenario-wave-template-grouping"></a>Scenario: Wave-sjabloongroepering

In dit scenario ziet u hoe u met wave-sjabloongroepering automatisch meerdere waves maakt op basis van groeperingscriteria die zijn gedefinieerd in een wave-sjabloon. In dit scenario wordt de wave-sjabloon geconfigureerd in het systeem om één wave per vervoerdersservice te maken.

Voordat u begint, moet u de wave-sjabloon voorbereiden zoals beschreven in de sectie [Een wave-sjabloon instellen voor gebruik met wave-sjabloongroepering](#set-up-template) eerder in dit onderwerp. Als u voor dit scenario met demogegevens gaat werken, moet u ervoor zorgen dat u de voorbeeldgegevenswaarden gebruikt die in die procedure worden voorgesteld. Met deze configuratie worden de waves gegroepeerd op basis van de vervoerdersservice die voor elke verkooporder is ingesteld.

#### <a name="create-sales-order-1"></a>Verkooporder 1 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-004*.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.

1. Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.
1. De nieuwe verkooporder wordt geopend in de weergave **Regels**. Noteer het nummer van de verkooporder.
1. Schakel over naar de weergave **Koptekst**.
1. Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:

    - **Vervoerder:** *Air Cargo*
    - **Vervoerdersservice:** *Air*

1. Ga terug naar de weergave **Regels**.
1. Selecteer in de sectie **Verkooporderrgels** de optie **Regel toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *2*

1. Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven. Noteer het id-nummer van de wave en de id-nummers van de zendingen.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>De wave weergeven die is gemaakt op basis van verkooporder 1

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave-id die is aangemaakt op basis van de verkooporder.
1. Selecteer de koppeling van de wave-id om de pagina Wave-gegevens te openen.
1. U ziet dat de zending is toegevoegd aan het sneltabblad **Wave-regels**.

#### <a name="create-sales-order-2"></a>Verkooporder 2 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-005*.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.

1. Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.
1. De nieuwe verkooporder wordt geopend in de weergave **Regels**. Noteer het nummer van de verkooporder.
1. Schakel over naar de weergave **Koptekst**.
1. Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:

    - **Vervoerder:** *Flower moving*
    - **Vervoerdersservice:** *Std*

1. Ga terug naar de weergave **Regels**.
1. Selecteer in de sectie **Verkooporderrgels** de optie **Regel toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *1*

1. Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven. Noteer het id-nummer van de wave en de id-nummers van de zendingen. Merk op dat de wave-id anders is dan de wave-id van de eerste verkooporder.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>De wave weergeven die is gemaakt op basis van verkooporder 2

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave-id die is aangemaakt op basis van de tweede verkooporder.
1. Selecteer de koppeling van de wave-id om de pagina Wave-gegevens te openen.
1. U ziet dat de zending is toegevoegd aan het sneltabblad **Wave-regels**.

Een nieuwe wave is gemaakt voor deze zending, omdat deze een andere vervoerdersservice gebruikt dan de eerste verkooporder.

#### <a name="create-sales-order-3"></a>Verkooporder 3 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-006*.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.

1. Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.
1. De nieuwe verkooporder wordt geopend in de weergave **Regels**. Noteer het nummer van de verkooporder.
1. Schakel over naar de weergave **Koptekst**.
1. Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:

    - **Vervoerder:** *Air Cargo*
    - **Vervoerdersservice:** *Air*

1. Ga terug naar de weergave **Regels**.
1. Selecteer in de sectie **Verkooporderrgels** de optie **Regel toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *1*

1. Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven. Noteer het id-nummer van de wave en de id-nummers van de zendingen. De zending is toegewezen aan de bestaande wave van de eerste verkooporder.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>De wave voor verkooporders 1 en 3 weergeven

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave-id die is aangemaakt op basis van de derde verkooporder.
1. Selecteer de koppeling van de wave-id om de pagina Wave-gegevens te openen.
1. U ziet dat de zending is toegevoegd aan het sneltabblad **Wave-regels** , samen met de zending voor de eerste verkooporder.
