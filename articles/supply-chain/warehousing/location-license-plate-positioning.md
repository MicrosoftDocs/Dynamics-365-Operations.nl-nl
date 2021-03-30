---
title: Positionering van locatie nummerplaat
description: Met positionering van de nummerplaatlocatie kunt u zien waar een nummerplaat zich bevindt in een locatie met meerdere pallets, zoals een locatie waar pallets dubbeldiep worden weggezet.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cfab8c36adb08f799305a153589926bfc1ae31fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217096"
---
# <a name="location-license-plate-positioning"></a>Positionering van locatie nummerplaat

[!include [banner](../includes/banner.md)]

Met positionering van de nummerplaatlocatie kunt u zien waar een nummerplaat zich bevindt in een locatie met meerdere pallets, zoals een locatie waar pallets dubbeldiep worden weggezet.

De functie voegt een volgnummer toe aan elke nummerplaat die op een opslaglocatie wordt geplaatst. Dit volgnummer wordt gebruikt om de nummerplaten op de opslaglocatie te bestellen. De functie ondersteunt daarom op intelligente wijze scenario's waarin klanten een doorrolstelling gebruiken en die voor het verzamelen van producten moeten weten welke nummerplaat zich vooraan bevindt.

Dit onderwerp bespreekt een scenario waarin wordt uitgelegd hoe u de functie instelt en gebruikt.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>De functie Positionering van locatie nummerplaat inschakelen

Voordat u de functie Positionering van locatie nummerplaat kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Positionering van locatie nummerplaat*

## <a name="example-scenario"></a>Voorbeeldscenario

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Om dit scenario te doorlopen met de waarden die hier worden voorgesteld, moet u werken op een systeem waarop voorbeeldgegevens zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="set-up-the-feature-for-this-scenario"></a>De functie instellen voor dit scenario

Voer de volgende procedures uit om de functie *Positionering van locatie nummerplaat* in te stellen voor het scenario dat in dit onderwerp wordt besproken.

#### <a name="location-profiles"></a>Locatieprofielen

De functie moet worden ingeschakeld in het locatieprofiel voor elke locatie waar de functie wordt gebruikt.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer in de lijst met locatieprofielen in het linkerdeel venster de optie **BULK-06**.
1. Op het sneltabblad **Algemeen** zijn twee nieuwe opties toegevoegd door de functie. Stel de volgende waarden in:

    - **Positie van kentekenplaat inschakelen:** *Ja*

        Als deze optie is ingesteld op *Ja*, wordt de positie van de nummerplaat vastgehouden voor nummerplaten op deze locatie.

    - **Positie nummerplaat tonen op mobiel apparaat:** *Ja*

        Wanneer deze optie is ingesteld op *Ja*, wordt de positie van de nummerplaat getoond aan gebruikers van mobiele apparaten tijdens corrigeren en tellen. U kunt de instelling van deze optie alleen wijzigen als de functie is ingeschakeld.

1. Selecteer **Opslaan**.

#### <a name="location-directives"></a>Locatie-instructies

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Controleer in het linkerdeel venster of het veld **Werkordertype** is ingesteld op *Verkooporders*.
1. Selecteer in de lijst met locatie-instructies **61 VO Orderverzamelingsorder**.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer op het sneltabblad **Regels** de regel met het **volgnummer** *2*.
1. Selecteer op het sneltabblad **Locatie-instructieacties** de regel met de **Naam**-waarde *Verzamelen voor minder dan pallet* (dit moet de enige regel zijn) en wijzig de waarde van het **Volgnummer** in *2*.
1. Selecteer **Nieuw** boven het raster om een regel voor een nieuwe locatie-instructieactie toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Volgnummer:** *1*
    - **Naam:** *Pickpositie 1*

1. Selecteer de optie **Query bewerken** boven het raster terwijl de nieuwe regel nog steeds is geselecteerd.
1. Selecteer in de query-editor het tabblad **Joins**.
1. Vouw de tabeljoin **Locaties** uit om de join met de tabel **Voorraaddimensies** weer te geven.
1. Vouw de tabeljoin **Voorraaddimensies** uit om de join met de tabel **Voorhanden voorraad** weer te geven.
1. Selecteer **Voorraaddimensies** en selecteer vervolgens **Tabeljoin toevoegen**.
1. Selecteer in de lijst met tabellen die wordt geopend in de kolom **Relatie** de waarde **Nummerplaat (nummerplaat)**. Selecteer vervolgens **Selecteren** om **Nummerplaat** toe te voegen aan de tabeljoin **Voorraaddimensies**.
1. Terwijl **Nummerplaat** nog is geselecteerd, selecteert u **Tabeljoin toevoegen**.
1. Selecteer in de lijst met tabellen die wordt geopend in de kolom **Relatie** de waarde **Positionering van locatie nummerplaat (nummerplaat)**. Selecteer vervolgens **Selecteren** om **Positionering van locatie nummerplaat** toe te voegen aan de tabeljoin **Voorraaddimensies**.

    ![Tabeljoins](media/LpTableJoin.png "Tabeljoins")

1. Klik op **OK** om de bijgewerkte gekoppelde tabellen te bevestigen en de query-editor te sluiten.
1. Selecteer op het sneltabblad **Locatie-instructieacties** opnieuw de optie **Query bewerken** om de query-editor te openen.
1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Positionering van locatie nummerplaat*
    - **Afgeleide tabel:** *Positionering van locatie nummerplaat*
    - **Veld:** *Positie NP*
    - **Criteria:** *1*

    ![Nieuw bereik](media/LpPositionCriteria.png "Nieuw bereik")

1. Selecteer **OK** om de wijzigingen te bevestigen en de query-editor te sluiten.

### <a name="set-up-sample-data-for-this-scenario"></a>Voorbeeldgegevens instellen voor dit scenario

Voor dit scenario moet de gebruiker zich aanmelden bij de mobiele magazijnapp door een werknemer te gebruiken die is ingesteld om werk uit te voeren in magazijn *61*. De gebruiker moet ook transacties uitvoeren.

Omdat de functie *Positionering van locatie nummerplaat* een nieuwe id toevoegt voor posities van de nummerplaat op een locatie, moet u eerst enkele gegevens aanmaken om het scenario te ondersteunen.

#### <a name="spot-count-the-first-location"></a>Plaatscyclustelling uitvoeren op de eerste locatie

1. Start de mobiele magazijnapp en meld u aan bij magazijn *61*.
1. Ga naar **Voorraad \> Plaatscyclustelling**.
1. Stel op de pagina **Plaatscyclustelling** het veld **Locatie** in op *01A01R1S1B*.
1. Selecteer **OK**.

    Op de pagina wordt de locatie getoond die u hebt ingevoerd. Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"

1. Selecteer **Vernieuwen** om een telling toe te voegen aan de locatie.
1. Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **Artikel** en voert u de waarde *A0001* in.
1. Selecteer **OK**.
1. Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **NP** en voert u de waarde *LP1001* in (of een ander nummerplaatnummer van uw keuze).

    Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** wordt **Nummerplaatpositie 1** weergegeven.

1. Selecteer **OK**.

    U moet nu de hoeveelheid opgeven van het artikel dat op de nummerplaat wordt geteld.

1. Stel het veld **Hoeveelheid** in op *10*.
1. Selecteer **OK**.

    Op de pagina wordt de locatie getoond die u hebt ingevoerd. Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"

1. Selecteer **Vernieuwen** om nog een telling toe te voegen aan de locatie.
1. Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **Artikel** en voert u de waarde *A0002* in.
1. Selecteer **OK**.
1. Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **NP** en voert u de waarde *LP1002* in (of een ander nummerplaatnummer van uw keuze, mits deze verschilt van het nummerplaatnummer dat u eerder hebt opgegeven).
1. Wijzig de positie van de nummerplaat door het veld **Positie NP** in te stellen op *2*.
1. Selecteer **OK**.
1. Geef de hoeveelheid van het artikel op dat wordt geteld bij de nummerplaat door het veld **Hoeveelheid** in te stellen op *10*.
1. Selecteer **OK**.

    Op de pagina wordt de locatie getoond die u hebt ingevoerd. Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"

1. Selecteer **OK**.

Het werk is nu voltooid.

#### <a name="spot-count-the-second-location"></a>Plaatscyclustelling uitvoeren op de tweede locatie

1. Stel op de pagina **Plaatscyclustelling** het veld **Locatie** in op *01A01R1S2B*.
1. Selecteer **OK**.

    Op de pagina wordt de locatie getoond die u hebt ingevoerd. Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"

1. Selecteer **Vernieuwen** om een telling toe te voegen aan de locatie.
1. Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **Artikel** en voert u de waarde *A0002* in.
1. Selecteer **OK**.
1. Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **NP** en voert u de waarde *LP1003* in (of een ander nummerplaatnummer van uw keuze, mits deze verschilt van de beide nummerplaatnummers die u hebt opgegeven in de vorige procedure).

    Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** wordt **Nummerplaatpositie 1** weergegeven.

1. Selecteer **OK**.
1. Geef de hoeveelheid van het artikel op dat wordt geteld bij de nummerplaat door het veld **Hoeveelheid** in te stellen op *10*.
1. Selecteer **OK**.

    Op de pagina wordt de locatie getoond die u hebt ingevoerd. Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"

1. Selecteer **OK**.

Het werk is nu voltooid.

#### <a name="work-details"></a>Werkgegevens

> [!NOTE]
> Plaatscyclustellingen vanuit de mobiele app maken cyclustellingswerk aan in Microsoft Dynamics 365. Voor het werk moeten de tellingen worden geaccepteerd voordat ze naar de voorraad worden geboekt.

1. Meld u aan bij Dynamics 365 Supply Chain Management.
1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Zoek op het tabblad **Overzicht** naar de regels met de volgende waarden:

    - **Werkordertype:** *Cyclustelling*
    - **Magazijn:** *61*
    - **Werkstatus:** *In afwachting van controle*

    Voor deze regels moeten twee werk-id's zijn gemaakt. De telling voor beide werk-id's moet worden geaccepteerd.

1. Selecteer in het raster de eerste werk-id voor het werkordertype *Cyclustelling*.
1. Selecteer in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Cyclustelling**.

    Er worden twee regels weergegeven: één voor elk artikel met nummerplaat. De waarden in de **velden Getelde hoeveelheid**, **Locatie**, **Nummerplaat** en **Artikel** moeten overeenkomen met de waarden van de tellingen die u op het mobiele apparaat hebt gemaakt. Als een of meer van deze velden niet zichtbaar zijn, selecteert u in het actievenster de optie **Dimensies weergeven** om ze aan het raster toe te voegen.

1. Selecteer beide regels.
1. Selecteer in het actievenster **Telling accepteren**.
1. U ziet de melding "Boeken - journaal". Selecteer **Berichtdetails** om het geboekte journaalnummer weer te geven.
1. Sluit de berichtdetails.
1. Vernieuw de pagina **Werk**.

    De eerste werk-id is gesloten en wordt niet meer weergegeven.

    > [!TIP]
    > U kunt het afgesloten werk weergeven door het selectievakje **Gesloten weergeven** boven het raster in te schakelen.

    U accepteert nu het werk voor de nummerplaat op de locatie *01A01R1S2B*.

1. Selecteer op het tabblad **Overzicht** de tweede werk-id voor het werkordertype *Cyclustelling*.
1. Selecteer in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Cyclustelling**.

    Er wordt één regel weergegeven voor het artikel en de nummerplaat. De waarden in de **velden Getelde hoeveelheid**, **Locatie**, **Nummerplaat** en **Artikel** moeten overeenkomen met de waarden van de tellingen die u op het mobiele apparaat hebt gemaakt.

1. Selecteer de regel.
1. Selecteer in het actievenster **Telling accepteren**.
1. U ziet de melding "Boeken - journaal". Selecteer **Berichtdetails** om het geboekte journaalnummer weer te geven.
1. Sluit de berichtdetails.
1. Vernieuw de pagina **Werk**.

    De tweede werk-id is gesloten en wordt niet meer weergegeven.

    > [!TIP]
    > U kunt het afgesloten werk weergeven door het selectievakje **Gesloten weergeven** boven het raster in te schakelen.

#### <a name="on-hand-by-location"></a>Voorhanden voorraad per locatie

1. Ga naar **Magazijnbeheer \> Query's en rapporten \> Voorhanden voorraad per locatie**.
1. Stel de volgende waarden in:

    - **Locatie:** *6*
    - **Magazijn:** *61*
    - **Vernieuwen op locaties:** *Ja*

1. Merk op dat de locatie *01A01R1S1B* twee nummerplaten heeft:

    - **A0001**, waarbij het veld **Positie NP** is ingesteld op *1*
    - **A0002**, waarbij het veld **Positie NP** is ingesteld op *2*

1. Merk op dat de locatie *01A01R1S2B* één nummerplaat heeft:

    - **A0002**, waarbij het veld **Positie NP** is ingesteld op *1*

### <a name="sales-order-scenario"></a>Scenario met verkooporder

Nu de functie *Positionering van locatie nummerplaat* is ingesteld en de voorraad is klaargezet, moet u een verkooporder maken om werk voor orderverzamelen te genereren. De magazijnwerknemer moet dan artikel *A0002* ophalen bij de voorraadlocatie waarop de pallet-id zich bevindt in positie *1*.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-004*
    - **Magazijn:** *61*

1. Selecteer **OK**.
1. Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *1*

1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren voor de orderregel.
1. Sluit de pagina **Reservering**.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.

    U ontvangt een informatieve melding waarin de wave-id en zendings-id worden vermeld die zijn aangemaakt voor de order.

1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** boven het raster de waarde **Werkdetails**.
1. De pagina **Werk** wordt weergegeven en toont het werk dat voor de verkoopregel is gemaakt. Noteer de werk-id die wordt getoond.

### <a name="sales-picking-scenario"></a>Scenario met orderverzamelen voor verkoop

1. Start de mobiele app en meld u aan bij magazijn *61*.
1. Ga naar **Uitgaand \> Orderverzamelen**.
1. Selecteer op de pagina **Een werk-id/nummerplaat-id scannen** het veld **Id** en voer vervolgens de werk-id van de verkoopregel in.
1. U ziet dat het verzamelwerk u artikel *A0002* laat ophalen vanuit locatie *01A01R1S2B*. U ontvangt deze instructie omdat artikel *A0002* op een nummerplaat staat die zich bevindt op positie *1* op die locatie.

    ![Locatie positie 1](media/LocationLicensePlatePositioning.png "Locatie positie 1")

1. Voer de nummerplaat-id in die u voor de locatie hebt gemaakt en volg de aanwijzingen om de verkooporder te verzamelen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]