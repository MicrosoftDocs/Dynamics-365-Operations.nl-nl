---
title: Werkgroep voor werk wijzigen
description: In dit onderwerp wordt uitgelegd hoe u de knop Werkpool wijzigen kunt gebruiken voor werkitems om de werkpool van bestaande werkzaamheden te wijzigen.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 513d74af52c9b3581827b653d58c95d7d1f2f78a75bea03296495fed0ea85de7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771126"
---
# <a name="change-work-pool-on-work"></a>Werkgroep voor werk wijzigen

[!include [banner](../includes/banner.md)]

U kunt werkpools gebruiken om werk in groepen te organiseren. U kunt bijvoorbeeld, een werkpool maken om werk te classificeren dat zich in een specifieke magazijnlocatie voordoet.

Met de functie *Werkpool voor werk wijzigen* wordt een knop **Werkpool wijzigen** toegevoegd aan het actievenster voor werkitems. Daarom kunnen magazijnmanagers de werkpool van bestaand werk eenvoudig wijzigen. Met deze functie reageert de manager snel op wijzigingen op de werkvloer in het magazijn en kunnen ze beter aanpassen aan veranderende situaties en de noodzaak om werk over te brengen naar een andere werkpool.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Schakel de functie Werkpool voor werk wijzigen in

Voordat u deze functie gaat instellen of gebruiken, moet u controleren of deze beschikbaar is in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Werkpool voor werk wijzigen*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>De functie Werkpool voor werk wijzigen instellen

Als u deze functie wilt gebruiken, moeten sommige werkpools zijn ingesteld. U kunt ook uw werksjablonen instellen zodat deze automatisch een pool toewijzen. Als u het voorbeeldscenario wilt doorlopen dat verderop in dit onderwerp wordt beschreven, stelt u uw systeem in zoals in deze sectie wordt beschreven.

### <a name="set-up-work-pools"></a>Werkpools instellen

Met werk pools kunt u werkitems op type ordenen. Als u wilt werken met de functie *Werkpool voor werk wijzigen*, moeten er minimaal twee werkpools beschikbaar zijn. Voer de volgende stappen uit om werkpools weer te geven en toe te voegen.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkpools**.
1. Als u werkt met demogegevens uit het **USMF**-bedrijf en het voorbeeldscenario verderop in dit onderwerp doorloopt, voegt u twee werkpools toe met de volgende instellingen:

    - Werkpool 1:

        - **Werkpool-id:** *Webshop*
        - **Omschrijving:** *Webshop*

    - Werkpool 2:

        - **Werkpool-id:** *CallCenter*
        - **Omschrijving:** *Callcenter*

1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-work-templates"></a>Werksjablonen instellen

Voor elk van uw werksjablonen kunt u een standaard werkpool instellen. Voor elke relevante sjabloon wijst u een werkpool toe in de kolom **Werkpool-id**. In dit geval nemen alle werkitems die met behulp van een bepaalde sjabloon worden gegenereerd, automatisch de toegewezen werkpool over. Als u werkt met de demogegevens uit het **USMF**-bedrijf en het voorbeeldscenario verderop in dit onderwerp doorloopt, volgt u deze stappen.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer in het actievenster de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. U bewerkt de sjabloon door de volgende waarden in te stellen:

    - **Werksjabloon:** *62 Orderverzamelen voor inpakken*
    - **Werkpool-id:** *Webshop*

1. Selecteer **Opslaan**.

## <a name="example-scenario"></a>Voorbeeldscenario

In dit scenario ziet u hoe u de verwerkingsstroom van een bestaand werk item kunt wijzigen door de werkpool te wijzigen. Het gebruikt demogegevens uit het **USMF**-bedrijf en de instellingen die eerder in dit onderwerp zijn voorgesteld.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Een verkooporder maken en vrijgeven naar het magazijn

1. Controleer of er voldoende voorhanden voorraad is voor artikelen *A0001* en *A0002* in magazijn *62*. Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden lijst** en bewerk de filters zoals hier wordt weergegeven:

    - De waarde **Magazijn** begint met *62*.
    - De waarde **Artikelnummer** is *A001* of *A002*.

    De voorbeeldgegevens moeten een hoeveelheid van 10 voor elk bevatten.

    Vervolgens moet u een verkooporder maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-007*
    - **Magazijn:** *62*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *2*

1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.
1. Sluit de pagina.
1. Selecteer op het sneltabblad **Verkooporderregels** de optie **Regel toevoegen** om nog een regel toe te voegen aan uw verkooporder. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *2*

1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.
1. Sluit de pagina.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.
1. U ontvangt een informatieve melding waarin de wave-id en zendings-id worden vermeld die zijn gemaakt door het vrijgeven. Noteer de wave-id.

### <a name="review-the-outbound-wave"></a>De uitgaande wave controleren

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Zoek in het raster naar de wave-id die is gemaakt op basis van de vrijgegeven verkooporder.
1. Selecteer de wave-id om de details weer te geven.
1. Controleer op het sneltabblad **Waveregels** of er een zending-id voor de verkooporder wordt weergegeven.

    > [!TIP]
    > Als de optie **Wave verwerken bij vrijgave door magazijn** is ingesteld op *Nee* in de instellingen voor de wavesjabloon van de zending, moet u de wave handmatig verwerken door **Verwerken** te selecteren op het tabblad **Wave** in het actievenster om werk te maken.

1. Controleer of de wave is verwerkt. Met deze verwerking wordt het vereiste werk gemaakt.

### <a name="view-work-details-and-change-the-work-pool"></a>Gegevens van werk weergeven en de werkpool wijzigen

U kunt de pagina **Werkdetails** gebruiken om het werk weer te geven dat is gemaakt en om de werkpool te beheren.

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Selecteer de rij voor het werk dat u zojuist hebt gemaakt. In de kolom **Ordernummer** wordt het verkoopordernummer weergegeven.

    Het veld **Werkpool-id** wordt ingesteld op de werkpool-id die is ingesteld in de werksjabloon.

    > [!TIP]
    > Als u het veld **Werkpool-id** niet ziet, voegt u de kolom toe aan het raster en vernieuwt u de pagina.

1. Als u de werkpool wilt wijzigen die aan de werk-id is gekoppeld, selecteert u in het actievenster op het tabblad **Werk** de optie **Werkpool-id wijzigen**.
1. Selecteer in het dialoogvenster **Werkpool wijzigen** de op het sneltabblad **Parameters** in het veld **Werkpool-id** de optie *Callcenter*.
1. Selecteer **OK** om de wijziging toe te passen.
1. U ziet dat de waarde van het veld **Werkpool-id** nu is gewijzigd in *Callcenter*.

> [!IMPORTANT]
> Wanneer het dialoogvenster **Werkpool wijzigen** wordt weergegeven, is het veld **Werkpool-id** standaard leeg. Als het veld leeg is wanneer u **OK** selecteert om wijzigingen toe te passen, wordt de werkpool volledig uit het werk verwijderd.
>
> Naast het schakelen tussen werkpools kunt u deze procedure gebruiken om een werkpool toe te voegen aan een werkitem dat geen werkpools heeft of om een werkpool te verwijderen uit een werkitem dat wel een werkpool heeft.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]