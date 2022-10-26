---
title: Eindproducten fysiek beschikbaar maken vóór boeking naar journalen
description: Wanneer een geproduceerd artikel wordt gereedgemeld, is het geregistreerd als beschikbaar voor verdere fysieke verwerking en worden een of meer journalen geboekt. In dit artikel wordt beschreven hoe u journaalboekingen uitstelt door mogelijk te maken dat ze worden verwerkt door een batchtaak in een berichtenwachtrij.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689335"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Eindproducten fysiek beschikbaar maken vóór boeking naar journalen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Wanneer een medewerker een geproduceerd artikel gereedmeldt, registreert het systeem het artikel als beschikbaar voor verdere fysieke verwerking (zoals verzending of opslag). Tijdens dit proces worden er ook een of meer journalen geboekt (zoals het gereedmeldingsjournaal, orderverzamellijstjournaal en routekaartjournaal). Als u uw artikelen fysiek beschikbaar wilt maken voordat alle boekingen zijn verwerkt, kunt u het systeem instellen om de journaalboekingen uit te stellen. Uitgestelde boekingen worden vervolgens afgehandeld door een batchtaak die de boekingen verwerkt wanneer systeembronnen het toestaan.

In de volgende afbeelding wordt getoond hoe processen voor boekingen van journalen aangeroepen worden met en zonder uitgestelde boeking.

![Het gereedmeldingsproces met en zonder uitgestelde journaalboeking.](media/deferred-posting-flowchart.png "Het gereedmeldingsproces met en zonder uitgestelde journaalboeking")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Uitgestelde journaalboeking voor uw systeem inschakelen

Voordat u uitgestelde journaalboeking kunt gebruiken, moet deze mogelijkheid zijn ingeschakeld in uw systeem. Beheerders kunnen de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Productiebeheer*
- **Functienaam:** *(Preview) Eindproducten fysiek beschikbaar maken vóór boeking naar journalen*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Journaalboekingsopties instellen voor gereedmeldingen

Medewerkers kunnen artikelen gereed melden met een van de volgende clients:

- Webclient
- Mobiele app Warehouse Management
- Uitvoeringsinterface voor de werkvloer

De webclient gebruikt dezelfde boekingsmethodeconfiguratie als de mobiele app Warehouse Management. De boekingsmethode die in de uitvoeringsinterface voor de werkvloer wordt gebruikt, moet echter afzonderlijk worden geconfigureerd.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Boekingsopties voor journalen instellen voor de webclient en de mobiele app Warehouse Management

In de mobiele app melden medwerkers artikelen gereed door een menuopdracht van een mobiel apparaat te openen waarbij de waarde van **Proces van werkaanmaak** is *Gereedmelden* of *Rapporteren als voltooid*. In de webclient melden medewerkers artikelen gereed vanaf de lijstpagina **Alle productieorders** of de pagina **Details van productieorder**. U kunt een standaardmethode voor het hele bedrijf configureren en u kunt ook magazijnspecifieke overschrijvingen instellen als u dat nodig hebt.

Met de volgende procedure kunt u de standaardboekingsmethode voor het hele bedrijf configureren voor het gereedmelden van artikelen vanaf de webclient of de mobiele app Warehouse Management.

1. Ga naar **Productiebeheer \> Instellen \> Parameters van productiebeheer**.
1. Stel op het tabblad **Journalen** in de sectie **Gereedmeldingsjournaal** het veld **Boekingsmethode** in op een van de volgende waarden:

    - *Onmiddellijk*: wanneer een artikel wordt gereedgemeld, worden alle gerelateerde journaalboekingen volledig door het systeem verwerkt voordat het gereedgemelde artikel fysiek beschikbaar is.
    - *Uitgesteld*: wanneer een artikel wordt gereedgemeld, wordt het door het systeem gemarkeerd als fysiek beschikbaar en worden de journaalboekingen toegevoegd aan een berichtenwachtrij. Het systeem wacht niet tot de boekingen volledig zijn verwerkt voordat het gereedgemelde artikel als fysiek beschikbaar wordt gemarkeerd.

Met de volgende procedure kunt u magazijnspecifieke overschrijvingen configureren voor de standaardboekingsmethode die is geconfigureerd op de pagina **Parameters van productiebeheer**.

1. Ga naar **Magazijnbeheer \> Instellen \> Opsplitsing van voorraad \> Magazijnen**.
1. Selecteer het magazijn dat u wilt instellen.
1. Selecteer **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Magazijn** in de sectie **Productieorders** het veld **Boekingsmethode** in op een van de volgende waarden:

    - *Overnemen:* het geselecteerde magazijn neemt de instelling over van de pagina **Parameters van productiebeheer**.
    - *Onmiddellijk*: wanneer een artikel wordt gereedgemeld, worden alle gerelateerde journaalboekingen volledig door het systeem verwerkt voordat het gereedgemelde artikel fysiek beschikbaar is.
    - *Uitgesteld*: wanneer een artikel wordt gereedgemeld, wordt het door het systeem gemarkeerd als fysiek beschikbaar en worden de journaalboekingen toegevoegd aan een berichtenwachtrij. Het systeem wacht niet tot de boekingen volledig zijn verwerkt voordat het gereedgemelde artikel als fysiek beschikbaar wordt gemarkeerd.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Boekingsopties voor journalen instellen voor de uitvoeringsinterface voor de werkvloer

Met de volgende procedure kunt u de boekingsmethode configureren die wordt gebruikt wanneer artikelen worden gereed gemeld vanuit voor de uitvoeringsinterface voor de werkvloer.

1. Ga naar **Productiebeheer \> Instellingen \> Productieregistratie \> Standaardwaarden van productieorder**.
1. Stel op het tabblad **Gereedmelden** in de sectie **Gereedmeldingsjournaal** het veld **Boekingsmethode** in op een van de volgende waarden:

    - *Onmiddellijk*: wanneer een artikel wordt gereedgemeld, worden alle gerelateerde journaalboekingen volledig door het systeem verwerkt voordat het gereedgemelde artikel fysiek beschikbaar is.
    - *Uitgesteld*: wanneer een artikel wordt gereedgemeld, wordt het door het systeem gemarkeerd als fysiek beschikbaar en worden de journaalboekingen toegevoegd aan een berichtenwachtrij. Het systeem wacht niet tot de boekingen volledig zijn verwerkt voordat het gereedgemelde artikel als fysiek beschikbaar wordt gemarkeerd.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>De batchtaak van de berichtenverwerker plannen om uitgestelde boekingen te verwerken

De batchtaak vanuit de berichtenverwerker is verantwoordelijk voor de verwerking van de journaalboekingen nadat deze in de wachtrij zijn geplaatst. Om er zeker van te zijn dat uw journaalboekingen worden verwerkt, moet u deze taak zo configureren dat deze regelmatig wordt uitgevoerd. Met de volgende procedure kunt u de vereiste batchtaak instellen.

1. Ga naar **Systeembeheer \> Berichtenverwerker \> Berichtenverwerker**.
1. Stel op het sneltabblad **Parameters** het veld **Berichtenwachtrij** in op *Productie*.
1. Stel op het sneltabblad **Op de achtergrond uitvoeren** de optie **Batchverwerking** in op *Ja*. Stel vervolgens een terugkerend schema in en configureer waar nodig andere instellingen. De instellingen werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>De voortgang van uitgestelde boekingen bijhouden

Uitgestelde journaalboekingen worden in de wachtrij geplaatst als *berichten voor de berichtenverwerker* die wachten totdat ze worden verwerkt door de *berichtenverwerker*. De berichtenverwerker moet zo worden ingesteld dat deze wordt uitgevoerd als een geplande batchtaak. Als u uitgestelde boekingsberichten wilt weergeven die zijn of worden verwerkt door de berichtenverwerker, gaat u naar **Productiebeheer \> Productieorders \> Uitgestelde productieorderboeking**.

### <a name="message-grid-columns-and-filters"></a>Kolommen en filters in het berichtenraster

Met de velden boven aan de pagina **Uitgestelde productieorderboeking** kunt u alle specifieke berichten vinden die u zoekt.

De volgende filters zijn beschikbaar:

- **Berichttype** – geef het type berichten op dat in het raster wordt weergegeven.
- **Berichtstatus** – geef de status van de berichten op die in het raster worden weergegeven. De volgende statuswaarden bestaan:

    - *In de wachtrij*: het bericht is gereed voor verwerking door de berichtenverwerker.
    - *Verwerkt*: het bericht is verwerkt door de berichtenverwerker.
    - *Geannuleerd* – het bericht kon niet worden verwerkt tijdens de laatste poging en werd vervolgens geannuleerd door de gebruiker.
    - *Mislukt* – het bericht kon niet worden verwerkt tijdens de laatste poging. Er wordt tot drie keer toe geprobeerd om een mislukt bericht te verwerken. Daarna geeft het systeem het op en laat het bericht in de status *Mislukt*. U kunt een bericht pas handmatig annuleren of bewerken na de laatste van deze drie pogingen.

- **Berichtinhoud**: Dit filter biedt de mogelijkheid voor een zoekopdracht in de volledige tekst van de berichtinhoud. (De inhoud van het bericht wordt niet in het raster getoond.) Het filter verwerkt de meeste speciale symbolen (zoals koppeltekens) als spaties en alle spaties als booleaanse OR-operators. Als u bijvoorbeeld zoekt naar een specifieke `journalid`-waarde die gelijk is aan *USMF-123456*, worden alle berichten gevonden die ofwel 'USMF' ofwel '123456' bevatten. In dit geval zal de lijst met resultaten waarschijnlijk lang zijn. Het is daarom beter om slechts *123456* in te voeren, omdat dat meer specifieke resultaten oplevert.

U kunt de lijst ook sorteren en filteren door een van de kolomkoppen te selecteren en criteria in te voeren in het dialoogvenster met vervolgkeuzemenu.

### <a name="view-the-message-log-message-content-and-details"></a>Het berichtenlogboek, de berichtinhoud en details weergeven

U kunt gedetailleerde informatie over een bericht vinden door het te selecteren in het raster en vervolgens het tabblad **Logboek** of **Onbewerkte inhoud** te selecteren onder het berichtenraster, waar alle verwerkingsgebeurtenis worden weergegeven.

De werkbalk op het tabblad **Logboek** bevat de volgende knoppen:

- **Logboek** : selecteer deze knop om de verwerkingsresultaten weer te geven. Deze knop is vooral nuttig wanneer berichten bij **Verwerkingsresultaat** de waarde *Mislukt* hebben en u de redenen hiervoor wilt weten.
- **Bundel**: Meerdere bewerkingen voor berichtverwerking kunnen worden uitgevoerd als onderdeel van hetzelfde batchproces. Selecteer deze knop als u deze gedetailleerde gegevens wilt weergeven. U kunt bijvoorbeeld zien of er afhankelijkheden zijn die vereisen dat bepaalde berichten in een specifieke volgorde worden verwerkt.

### <a name="manually-process-or-cancel-a-message"></a>Een bericht handmatig verwerken of annuleren

U kunt een bericht desgewenst handmatig verwerken of annuleren, afhankelijk van de huidige status. Selecteer het bericht in het raster en selecteer **Verwerken** of **Annuleren** in het actievenster.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Zakelijke gebeurtenissen instellen om waarschuwingen te leveren voor mislukte verwerkingsresultaten

U kunt [zakelijke gebeurtenissen](../../fin-ops-core/dev-itpro/business-events/home-page.md) instellen die u waarschuwen voor mislukte verwerkingsresultaten. Ga naar **Systeembeheer \> Instellingen \> Zakelijke gebeurtenissen \> Catalogus met zakelijke gebeurtenissen** en activeer de zakelijke gebeurtenis met de naam *Bericht van berichtenverwerker verwerkt*.

Als onderdeel van het activeringsproces wordt u gevraagd om op te geven of de gebeurtenis specifiek is voor één rechtspersoon of voor alle rechtspersonen geldt. U wordt ook gevraagd een waarde voor **Eindpuntnaam** op te geven. Deze waarde moet eerst worden gedefinieerd.

> [!NOTE]
> Als het veld **Als zich een zakelijke gebeurtenis voordoet** is ingesteld op *Microsoft Power Automate* (in plaats van bijvoorbeeld *HTTPS*), wordt de waarde voor **Eindpuntnaam** automatisch gemaakt in Supply Chain Management, op basis van de *Microsoft Power Automate*-configuratie.
