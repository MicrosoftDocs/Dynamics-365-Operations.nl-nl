---
title: Status magazijnlocatie
description: In dit onderwerp vindt u een overzicht van de functie Status magazijnlocatie.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: e343fbd33ca616b0e20efb1f1fd66ed4863a72dd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248614"
---
# <a name="warehouse-location-status"></a>Status magazijnlocatie

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management beschikt over diverse locatievelden waarmee u flexibiliteit krijgt bij het werken met en het onderhouden van locaties. U kunt de status van de locatie in de query van de locatie-instructie opnemen om een betere controle te krijgen over de magazijnstroom.

In de volgende vier velden op de pagina **Locaties** wordt informatie bijgehouden over de huidige status van een locatie. Met behulp van deze velden kunnen magazijnbeheerders een overzicht krijgen van de status van de magazijnlocaties. Ze bieden ook mogelijkheden voor geavanceerde rapportage en filteren.

- **Artikelnummer:** Het artikel dat zich momenteel op de locatie bevindt. Als de locatie meerdere artikelen bevat, is dit veld leeg.
- **Datum en tijd van de laatste activiteit:** De tijdstempel van de laatste magazijntransactie die is uitgevoerd op de locatie.
- **Ouderdomsdatum:** De datum waarop de voorraad op de locatie in het magazijn is binnengebracht. Deze waarde wordt berekend op basis van de ouderdomsdatum van de nummerplaat. Deze waarde is nauwkeurig voor locaties die met een nummerplaat worden gevolgd, maar mogelijk niet juist voor locaties die niet worden gevolgd met een nummerplaat.
- **Locatiestatus:** De status van de locatie. Er zijn vier mogelijke waarden:

    - **Onbepaald:** Het locatieprofiel kan de status niet bijhouden. Daarom is de huidige status onbekend.
    - **Leeg:** Er is momenteel geen voorraad op de locatie.
    - **Orderverzameling:** Uitgaande transacties zijn uitgevoerd op de locatie sinds deze voor het laatst leeg was.
    - **Opslag:** Alleen ingaande transacties zijn uitgevoerd op de locatie sinds deze voor het laatst leeg was.

## <a name="turn-on-the-warehouse-location-status-feature"></a>De functie Status magazijnlocatie inschakelen

Voordat u de functie *Status magazijnlocatie* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Status magazijnlocatie*

## <a name="set-up-warehouse-location-status"></a>De functie Status magazijnlocatie configureren

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>De voorbeeldgegevens voorbereiden die zijn vereist voor het voorbeeldscenario

Voordat u het scenario gaat doorlopen, moet u voorbeeld gegevens activeren en de functie configureren, zoals in deze sectie wordt beschreven. Om het voorbeeld scenario te voltooien, moet u de magazijnapp of de browser-emulator gebruiken. De stappen die hier worden gegeven, maken gebruik van de magazijnapp. De stappen voor de op de browser gebaseerde emulator zijn vergelijkbaar.

#### <a name="use-the-usmf-legal-entity"></a>De rechtspersoon USMF gebruiken

Als u deze het voorbeeldscenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

#### <a name="set-up-location-profiles"></a>Locatieprofielen instellen

Voor het voorbeeldscenario moet u twee locatieprofielen voorbereiden.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Selecteer het profieltype **BULK-06**.
1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Artikel in locatie inschakelen**: Stel deze optie in op _Ja_.
    - **Locatie voor activiteitsdatum en -tijd inschakelen:** Stel deze optie in op _Ja_.
    - **Locatiestatus inschakelen**: Stel deze optie in op _Ja_.

    Met deze opties bepaalt u of de verwijzingsvelden op de locatie actief zijn.

1. Herhaal de stappen 3 tot en met 4 voor het profiel **PICK-06**.

> [!NOTE]
> Wanneer de parameters in het locatieprofiel (**Artikel in locatie inschakelen**, **Locatieactiviteit inschakelen**, **Locatiestatus inschakelen**) op *Ja* zijn ingesteld, worden de relevante locaties onmiddellijk bijgewerkt met taak *Consistentiecontrole status magazijnlocatie*.

### <a name="scenario"></a>Scenario's

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw**.
1. Ga in het dialoogvenster **Inkooporder maken** naar het sneltabblad **Leverancier** en selecteer in het veld **Leveranciersrekening** de waarde *104*.
1. Selecteer op het sneltabblad **Algemeen** magazijn **61** in het veld *Magazijn*.
1. Selecteer **OK**.
1. De nieuwe inkooporder (IO) wordt geopend. Deze bevat een lege rij in het raster **Inkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** _A0002_
    - **Hoeveelheid:** _5_

1. Ga in het actievenster naar het tabblad **Inkoop** en selecteer in de groep **Acties** de optie **Bevestigen** om de inkooporder te bevestigen.
1. Ga op het mobiele apparaat naar **Inkomend \> Inkoop ontvangen**.
1. Selecteer het veld **PONUM**, voer het verkoopordernummer in en bevestig.
1. Selecteer het veld **ARTIKEL**, voer *A0002* in als het artikelnummer en bevestig.
1. Ga naar de pagina **Hoeveelheid** en voer *5* in als de hoeveelheid en bevestig.

    U kunt de hoeveelheid op een van de volgende manieren invoeren:

    - Selecteer de knop met het plusteken (**+**) of het minteken (**–**) om een numerieke waarde te verhogen of te verlagen.
    - Selecteer het lege veld tussen de knoppen met het plusteken (**+**) en het minteken (**–**) om het numerieke toetsenblok te openen.

1. Bevestig de selectie van artikelnummer *A0002* en de hoeveelheid *5*. Onderin de pagina wordt het bericht "Werk voltooid" getoond.
1. Selecteer de menuknop (ook wel de hamburger of hamburgerknop genoemd) in de rechterbovenhoek en selecteer **Annuleren** om **Inkoop ontvangen** af te sluiten en terug te keren naar het menu **Inkomend**.
1. Selecteer op de pagina Inkooporder de optie **Werkdetails** boven het raster **Inkooporderregels**.
1. Merk op dat op het tabblad **Algemeen** waarden zijn aangemaakt in de velden **Werk-id** en de **Doelnummerplaat-id**.
1. In de sectie **Regels** ziet u de **Locatie**-waarden voor de Werktypen *Orderverzamelen* en *Wegzetten*.
1. Ga op het mobiele apparaat naar **Inkomend \> Inkoop wegzetten**.
1. Selecteer het veld **Id**, voer het werk-id in en bevestig.
1. Bevestig nogmaals om de invoer voor *Orderverzamelen* te voltooien.
1. Selecteer de Menu-knop in de rechterbovenhoek en selecteer vervolgens **Gereed** om het *orderverzamelwerk* te voltooien.
1. Noteer de locatie waarop de artikelen zijn weggezet en bevestig. Onderin de pagina wordt het bericht "Werk voltooid" getoond.
1. Selecteer de menuknop in de rechterbovenhoek en selecteer **Annuleren** om **Inkoop wegzetten** af te sluiten en terug te keren naar het menu **Inkomend**.
1. Selecteer **Vorige** om terug te gaan naar het hoofdmenu.
1. Ga in Dynamics 365 Supply Chain Management naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.
1. Filter op **Locatie** en voer de wegzetlocatie van het inkooporderwerk in. De volgende resultaten wordt weergegeven.

    - In de kolom **Locatiestatus** wordt de waarde van *Opslag* weergegeven , omdat de laatste transactie voor deze locatie een wegzetactie is.
    - In de kolom **Artikelnummer** wordt de waarde *A0002* weergegeven , omdat dat artikel is ontvangen en op de locatie is weggezet.
    - In de kolom **Datum en tijd van de laatste activiteit** wordt de tijdstempel weergegeven voor de datum en tijd waarop het werk op de locatie is voltooid.

1. Ga op het mobiele apparaat naar **Kwaliteit \> Mutatie**.
1. Selecteer het veld **Loc/NP** en geef de locatie op die u hebt genoteerd in de vorige stappen.
1. Bevestig de getoonde informatie. Noteer het nummer van de nummerplaat dat wordt gegenereerd.
1. Selecteer in het scherm **Naar-informatie** het veld **Loc/NP** en voer *06A07R2S1B* in als de locatie waar u het artikel naar wilt verplaatsen.
1. Bevestig in het scherm **Naar-informatie** de waarde van de **NP** (de id van de doelnummerplaat) die automatisch wordt gegenereerd. Onderin de pagina wordt het bericht "Werk voltooid" getoond.
1. Selecteer de menuknop in de rechterbovenhoek en selecteer **Annuleren** om **Mutatie** af te sluiten en terug te keren naar het menu **Kwaliteitsbeheer**.
1. Selecteer **Vorige** om terug te gaan naar het hoofdmenu.
1. Ga in Dynamics 365 Supply Chain Management naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.
1. Vernieuw de pagina **Locaties** en bekijk de oorspronkelijke wegzetlocatie opnieuw. U ziet dat het veld **Locatiestatus** nu is ingesteld op *Leeg* en dat de kolom **Artikelnummer** leeg is.
1. Bekijk de record voor locatie *06A07R2S1B* en merk op dat de waarde in **Status** is gewijzigd in *Opslag* en dat de velden **Artikelnummer** en **Datum en tijd van de laatste activiteit** zijn bijgewerkt.
1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde *US-002*.
1. Selecteer **61** in het veld *Magazijn*.
1. Selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Deze bevat een lege rij in het raster **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** _A0002_
    - **Hoeveelheid:** _1_

1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** de waarde **Partij reserveren** om de orderregel te reserveren. Sluit de pagina door te klikken op de **sluitknop** (**X**) in de rechterbovenhoek.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. Selecteer in de sectie **Verkooporderregels** in het menu **Magazijn** de waarde **Werkdetails**.
1. Kopieer de gemaakte **werk-id**.
1. Ga op het mobiele apparaat naar **Uitgaand \> Verkooporder**.
1. Selecteer het veld **Id**, voer de werk-id in die u eerder hebt gekopieerd en bevestig.
1. Op de pagina **Verkooporders: orderverzamelen** wordt met het veld **Loc** de orderverzamellocatie voorgesteld als de wegzetlocatie die eerder is gemaakt. Noteer de locatie.
1. Selecteer het veld **Loc**, voer de locatie in en bevestig.
1. Selecteer het veld **NP**, voer de nummerplaat in die u hebt genoteerd tijdens de activiteit Mutatie en bevestig.
1. Selecteer het veld **Artikel**, voer *A0002* in als het artikelnummer en bevestig.
1. Ga naar de pagina **Hoeveelheid** en voer *1* in als de hoeveelheid en bevestig.

    U kunt de hoeveelheid op een van de volgende manieren invoeren:

    - Selecteer de knop met het plusteken (**+**) of het minteken (**–**) om een numerieke waarde te verhogen of te verlagen.
    - Selecteer het lege veld tussen de knoppen met het plusteken (**+**) en het minteken (**–**) om het numerieke toetsenblok te openen.

1. Selecteer het veld **Doel-NP**, voer een door de gebruiker gedefinieerde doelnummerplaat-id in en bevestig.
1. Bevestig nogmaals om het orderverzamelwerk te voltooien. Onderin de pagina wordt het bericht "Werk voltooid" getoond.
1. Selecteer de menuknop in de rechterbovenhoek en selecteer **Annuleren** om het verzamelwerk af te sluiten en terug te keren naar het menu **Uitgaand**.
1. Ga in Dynamics 365 Supply Chain Management naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.
1. Filter op **Locatie** en voer de verzamellocatie van het verkooporderwerk in.
1. U ziet dat het veld **Locatiestatus** voor de locatie vanwaar de verkooporder is opgehaald, nu is ingesteld op *Orderverzamelen* en dat het veld **Datum en tijd van de laatste activiteit** is bijgewerkt.

> [!NOTE]
> De locatievelden worden alleen bijgewerkt door magazijntransacties. Als u de voorraad verplaatst met behulp van een journaal of andere processen die niet WHS zijn, worden de velden niet bijgewerkt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]