---
title: Clusterpositie vol
description: Dit onderwerp bevat informatie over de functie Clusterpositie vol. Deze functie biedt een alternatief voor strengere handhaving van regels voor werkonderbrekingen wanneer clusterverzameling wordt gebruikt omdat hierdoor een grotere foutmarge mogelijk is in de volumetrische beperkingen van containers of totes.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2da0421bdb1496d51c807e51a26a980238886a42dfec167dac95611cc3df97bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730029"
---
# <a name="cluster-position-full"></a>Clusterpositie vol

[!include [banner](../includes/banner.md)]

De functie *Clusterpositie vol* biedt een alternatief voor strengere handhaving van regels voor werkonderbrekingen wanneer clusterverzameling wordt gebruikt omdat hierdoor een grotere foutmarge mogelijk is in de volumetrische beperkingen van containers of totes. In een algemeen scenario passen niet alle items in een werkorder in een geselecteerde container. Magazijnmedewerkers die een clusterverzameling maken, hebben niet veel opties in dit scenario: ze moeten een grotere containergrootte kiezen of met hun supervisor samenwerken om tot een andere oplossing te komen.

Deze functie introduceert de mogelijkheid om knop **Vol** uit te voeren voor een van de werkeenheden in een cluster. In oudere versies was deze optie alleen beschikbaar voor reguliere orderverzameling, niet voor clusterverzamelingen. Deze functie verschilt echter van de standaardknop **Vol** omdat het resterende werk wordt geannuleerd. Er wordt niet voorgesteld dat de gebruiker nog een bak aan hetzelfde cluster toevoegt en er wordt niet automatisch nieuw werk gemaakt.

## <a name="turn-on-the-cluster-position-full-feature"></a>De functie Clusterpositie vol inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Clusterpositie vol*

## <a name="setup"></a>Instelling

Deze sectie bevat richtlijnen en een voorbeeld waarin wordt aangegeven hoe u de functie *Clusterpositie vol* instelt en gebruikt.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u het [voorbeeldscenario](#example-scenario) wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt het voorbeeldscenario ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt. In dat geval moet u echter uw eigen waarden opgeven voor de instellingen die hier worden beschreven.

### <a name="cluster-profiles"></a>Clusterprofielen

U moet opgeven of cluster-Id's automatisch worden gegenereerd, hoeveel posities er worden gebruikt wanneer clusters worden uitgesplitst en hoe het orderverzamelingswerk wordt geordend en gecontroleerd.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Clusterprofielen**.
1. Selecteer in het lijstvenster de record **Cluster maken**.
1. Verifieer op het sneltabblad **Algemeen** de volgende waarden:

    - **Cluster-id maken**: *Ja*
    - **Posities activeren:** *Ja*
    - **Aantal posities:** *2*
    - **Positienaam:** *Numeriek*
    - **Cluster opsplitsen bij**: *Wegzetten*
    - **Verificatietype sorteren:** *Positie scannen*

1. Op het sneltabblad **Cluster sorteren**. Het raster moet leeg zijn (geen regels bevatten).

### <a name="work-templates"></a>Werksjablonen

U moet opgeven hoe het verzamelwerk voor clusterverzameling wordt gemaakt.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Stel boven aan de pagina het veld **Werkordertype** in op *Verkooporders*.
1. Controleer of de volgende werksjablonen uit de voorbeeldgegevens worden weergegeven. Als deze niet beschikbaar zijn, kunt u het scenario niet voltooien.

    - 61 SO Stage
    - 61 SO Cluster pick

### <a name="location-directives"></a>Locatie-instructies

U moet opgeven waar artikelen worden verzameld en waar deze worden geplaatst.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatie-instructies**.
1. Stel in de lijstkoptekst het veld **Werkordertype** in op *Verkooporders*.
1. Controleer of de volgende verkooporderinstructies uit de voorbeeldgegevens worden weergegeven. Als deze niet beschikbaar zijn, kunt u het scenario niet voltooien.

    - 61 Cluster pick
    - 61 SO Pick order

### <a name="mobile-device-menu-items"></a>Menuopties voor mobiel apparaat

Configureer een menu-item voor een mobiel apparaat om bestaand werk te gebruiken dat wordt geleid door clusterverzameling. U moet de parameter **Splitsing van werk toestaan** in het menu-item voor mobiele apparaten inschakelen en de werkklasse *VO verzamelen* moet worden toegevoegd.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het lijstvenster de record **Clusterverzameling maken**.
1. Selecteer **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Gestuurd door:** *Clusterverzameling*
    - **Nummerplaat maken:** *Ja*
    - **Splitsing van werk toestaan:** *Ja*
    - **Profiel-id van cluster:** *Cluster maken*

    Accepteer de standaardwaarden voor alle overige velden.

1. Voeg indien nodig de volgende twee regels toe op het sneltabblad **Werkklassen**:

    - Regel 1 (gewoonlijk aanwezig in voorbeeldgegevens):

        - **Werkklasse-id**: *Verkoop* 
        - **Werkordertype:** *Verkooporders*

    - Regel 2 (waarschijnlijk niet aanwezig in voorbeeldgegevens):

        - **Werkklasse-id:** *VO verzamelen*
        - **Werkordertype:** *Verkooporders*

1. Ga naar **Werkbevestigingsinstellingen** in het actievenster.
1. Selecteer **Bewerken**.
1. Voer de volgende waarden op de regel in het raster in.
    - **Werktype** - *Orderverzamelen*
    - **Productbevestiging** - *Het selectievakje inschakelen*

1. Selecteer **Opslaan** in het actievenster en sluit de pagina.

## <a name="create-picking-work"></a>Orderverzamelingswerk maken

Voordat u kunt beginnen met clusterverzamelingen, moet u uitgaand werk maken. Met het clusterprofiel dat u eerder hebt gemaakt, worden twee clusterposities opgegeven. Daarom moet u minimaal twee werk-id's maken voor het orderverzamelen van verkooporders. Voor dit scenario vinden transacties plaats in magazijn *61* en worden de artikelen *L0101* en *T0100* gebruikt. De voorbeeldgegevens moeten voldoende voorhanden voorraad van deze artikelen hebben. Controleer of u voldoende voorraad hebt om de transacties te voltooien.

### <a name="create-sales-order-1"></a>Verkooporder 1 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om verkooporder 1 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-010*
    - **Magazijn:** *61*

1. Selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Voeg op het sneltabblad **Verkooporderregels** een regel toe met de volgende instellingen:

    - **Artikelnummer:** *T0100*
    - **Hoeveelheid:** *5*

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.
1. Voeg op het sneltabblad **Verkooporderregels** een tweede regel toe met de volgende instellingen:

    - **Artikelnummer:** *L0101*
    - **Hoeveelheid:** *20*

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.
1. Volg voor elke regel die u zojuist hebt toegevoegd de volgende stappen om voorraad te reserveren:

    1. Selecteer de regel die u wilt reserveren.
    2. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
    3. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.
    4. Sluit de pagina **Reservering**.

1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    Als de vrijgave is voltooid, ontvangt u een informatieve melding waarin de wave- en ladings-id's worden vermeld die zijn gemaakt.

### <a name="create-sales-order-2"></a>Verkooporder 2 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om verkooporder 2 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-011*
    - **Magazijn:** *61*

1. Selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Voeg op het sneltabblad **Verkooporderregels** een regel toe met de volgende instellingen:

    - **Artikelnummer:** *L0101*
    - **Hoeveelheid:** *20*

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.
1. Voeg op het sneltabblad **Verkooporderregels** een tweede regel toe met de volgende instellingen:

    - **Artikelnummer:** *T0100*
    - **Hoeveelheid:** *2*

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.
1. Volg voor elke regel die u zojuist hebt toegevoegd de volgende stappen om voorraad te reserveren:

    1. Selecteer de regel die u wilt reserveren.
    2. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
    3. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.
    4. Sluit de pagina **Reservering**.

1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    Als de vrijgave is voltooid, ontvangt u een informatieve melding waarin de wave- en ladings-id's worden vermeld die zijn gemaakt.

### <a name="get-work-ids-and-license-plate-numbers"></a>Werk-id's en nummerplaatnummers ophalen

Er moeten twee werk-id's met elk twee pickregels zijn gemaakt. Voer de volgende stappen uit om de toewijzingen van werk-id's en nummerplaten te vinden.

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Zoek in raster **Overzicht** de kolom **Ordernummer** voor de twee verkooporders die u zojuist hebt gemaakt. Noteer voor elke verkooporder de bijbehorende werk-id.
1. Selecteer de rij voor elke verkooporder om gerelateerde informatie weer te geven in het raster **Regels**. Noteer de locatie waar elk artikel wordt verzameld.
1. Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.
1. Selecteer in het actievenster de optie **Dimensies** om het dialoogvenster **Weergave van dimensies** te openen.
1. Controleer of de selectievakjes **Nummerplaat**, **Magazijn** en **Artikelnummer** zijn ingeschakeld en selecteer **OK**.
1. Stel in het deelvenster **Filter** de volgende filters in:

    - **Artikelnummer** – **is één van** – *L0101* en *T100*
    - **Magazijn** – **begint met** – *61*

1. Noteer de weergegeven waarden voor **Nummerplaat**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Voorbeeldscenario

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Uitvoering van stroom op mobiele apparaten - Werkbevestigingsinstellingen voor het product

1. Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker in magazijn *61*.
1. Ga naar **Uitgaand \> Clusterverzameling maken**.

    De pagina **TAAK: werk toewijzen aan cluster** wordt weergegeven.

1. Voer de werk-id voor verkooporder 1 in om deze toe te wijzen aan clusterpositie 1.
1. Selecteer **OK** (symbool voor vinkje).
1. Voer de werk-id voor verkooporder 2 in om deze toe te wijzen aan clusterpositie 2.
1. Selecteer **OK** (symbool voor vinkje).

    De pagina **TAAK: Clusterverzameling maken: Orderverzamelen** wordt weergegeven en bevat *Artikel L0101 2 PL*.

Omdat het clusterprofiel het aantal posities instelt op 2, leidt het systeem u automatisch naar de eerste consolidatieverzameling: twee pallets (PL) van artikel *L0101*.

Tijdens de volgende stappen kunt u op elk gewenst moment het tabblad **Details** selecteren om aanvullende informatie over de taak weer te geven, zoals de orderverzamellocatie.

1. Stel het veld **ARTIKEL** in op *L0101*. Hiermee wordt het artikelnummer bevestigd dat vereist is voor deze menuopdracht (u hebt dit eerder geconfigureerd door **Werkbevestigingsinstellingen** te selecteren op de pagina **Menuopties voor mobiel apparaat** toen u deze menuopdracht maakte).
1. Voer het nummerplaatnummer dat is gekoppeld aan het artikel op de locatie dat wordt verzameld. U verzamelt twee pallets.
1. Stel het veld **LP** in op *LP\_PICK\_01*.
1. Selecteer **OK** (symbool voor vinkje).

    De pagina **TAAK: Sorteren: Clusterverzameling maken** wordt weergegeven. Hier kunt u de twee verzamelde pallets in een orderverzamelingspositie sorteren. Deze positie kan een tote of container zijn die wordt gebruikt om de verzamelde voorraad te scheiden op verkooporder.

1. Bekijk de details die worden weergegeven voor het artikel (*L0101*) en aantal (*20* ea) dat wordt gesorteerd op positie 1 (voor verkooporder 1).
1. Stel het veld **POSITIE NA** in op *1*.
1. Selecteer **OK** (symbool voor vinkje).
1. Bekijk de details die worden weergegeven voor het artikel (*L0101*) en aantal (*20* ea) dat wordt gesorteerd op positie 2 (voor verkooporder 2).
1. Stel het veld **POSITIE NA** in op *2*.
1. Selecteer **OK** (symbool voor vinkje).

    De pagina **TAAK: Clusterverzameling maken: Orderverzamelen** wordt weergegeven en bevat *Artikel L0100 7 ea*.

In dit scenario kan positie 1 niet de volledige hoeveelheid artikelen accepteren die moeten worden verzameld om verkooporder 1 af te handelen. Een positie moet als volledig worden gemarkeerd. In dit scenario verzamelt u het tweede artikel gedeeltelijk. Het tweede artikel wordt gedeeltelijk verzameld voor positie 1 en er wordt nieuwe werk gemaakt om de resterende hoeveelheid te verzamelen om de order af te handelen.

1. Selecteer de menuknop boven aan de pagina (ook wel aangeduid als de hamburger of de hamburgerknop) en selecteer **Positie vol**.
1. Geef de positie aan die vol is en selecteer *1*.
1. Selecteer **OK** (symbool voor vinkje).
1. Voer de orderverzamelhoeveelheid die nog kan worden verzameld in positie 1 in. Het systeem kan bepalen welk artikelnummer wordt verzameld.
1. Voer *2* in.
1. Selecteer **OK** (symbool voor vinkje).
1. Bevestig het artikelnummer om de verzameling van het resterende artikel op positie 2 te voltooien.
1. Stel het veld **ARTIKEL** in op *T0100*.
1. Selecteer **OK** (symbool voor vinkje).
1. Voer de nummerplaat in waarvan het artikel wordt verzameld door het veld **LP** in te stellen op *LPREPL04*.
1. Selecteer **OK** (symbool voor vinkje).
1. Bekijk de details die worden weergegeven voor het artikel (*T0100*) en aantal (*2* ea) dat wordt gesorteerd op positie 2 (voor verkooporder 2).
1. Stel het veld **POSITIE NA** in op *2*.
1. Selecteer **OK** (symbool voor vinkje).
1. Bekijk de details die worden weergegeven voor het artikel (*T0100*) en aantal (*2* ea) dat wordt gesorteerd op positie 1 (voor verkooporder 1).
1. Stel het veld **POSITIE NA** in op *1*.
1. Selecteer **OK** (symbool voor vinkje).

    De pagina **TAAK: Clusterverzameling maken: Wegzetten** wordt weergegeven.

In dit scenario is de clusterverzameling voltooid en wordt de gebruiker geïnstrueerd om de verzamelde artikelen van positie 1 en positie 2 weg te zetten op de faseringslocatie *STAGE01*.

1. Bekijk de gegevens op de pagina. Er wordt aangegeven dat het totale aantal van *44* wordt weggezet op de faseringslocatie.
1. Selecteer **OK** (symbool voor vinkje).

    U ontvangt het bericht Cluster voltooid.

U kunt nu de menuoptie **Orderverzamelen** gebruiken om het resterende aantal te verzamelen. Vervolgens kunt u met de menuopdracht **Verkoop laden** de artikelen van de faseringslocatie naar het laaddok verplaatsen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]