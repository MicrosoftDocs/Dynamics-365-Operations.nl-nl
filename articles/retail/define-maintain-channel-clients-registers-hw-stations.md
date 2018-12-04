---
title: Randapparaten aansluiten op het verkooppunt (POS)
description: In dit onderwerp wordt beschreven hoe u randapparatuur aansluit op uw Retail POS.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 9952ece965f467a19c911219382da00dd25a29e7
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Randapparaten aansluiten op het verkooppunt (POS)

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u randapparatuur aansluit op uw Retail POS.

**Opmerking:** raadpleeg voor specifieke installatie-instructies [Configuratie en installatie van Retail Hardware Station](retail-hardware-station-configuration-installation.md) en [Download/installatie van Self-service implementatie van Retail Modern POS en activering van moderne POS- en Cloud POS-apparaten](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Belangrijke onderdelen
Er worden verschillende onderdelen gebruikt voor het definiëren van de relatie tussen een winkel, de POS-kassa's (Point of Sale) of kanalen binnen de winkel en de randapparatuur voor de detailhandel die deze kassa's of kanalen gebruiken om transacties te verwerken. In deze sectie wordt elk onderdeel beschreven en wordt uitgelegd hoe dit moet worden gebruikt in een implementatie van een detailhandelwinkel.

### <a name="pos-registers"></a>POS-kassa's

Navigatie: klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Kassa's**. De POS-kassa is een entiteit waarmee de kenmerken worden gedefinieerd voor een specifiek POS. Deze kenmerken omvatten het hardwareprofiel of de instellingen voor detailhandelrandapparaten die worden gebruikt bij de kassa, de winkel waaraan de kassa is toegewezen en de visuele ervaring voor de gebruiker die zich bij die kassa aanmeldt.

### <a name="devices"></a>Apparaten

Navigatie: klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Apparaten**. Een apparaat is een entiteit die een fysiek exemplaar vertegenwoordigt van een apparaat dat is toegewezen aan een POS-kassa. Bij het maken van een apparaat, wordt het toegewezen aan een POS-kassa. De apparaatentiteit houdt informatie bij over wanneer een POS-kassa wordt geactiveerd, het type client dat wordt gebruikt en het toepassingspakket dat is geïmplementeerd op een specifiek apparaat. Devices can be of two types: **Retail Modern POS** (MPOS) of **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS is een POS-clienttoepassing die is geïnstalleerd op Windows 8.1 of een later pc-besturingssysteem. Als het toepassingstype **Retail Modern POS** wordt toegewezen aan een apparaat, kan het downloadpakket voor een bepaald apparaat worden opgegeven. Het downloadpakket kan worden aangepast zodat het verschillende versies van het installatiepakket bevat. De mogelijkheid om verschillende pakketten te implementeren biedt flexibiliteit in gevallen waarin andere POS-kassa's mogelijk andere integraties vereisen. MPOS wordt geïmplementeerd samen met een ingebouwd hardwarestation.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS is een op een browser gebaseerd POS. Omdat het in de browser wordt uitgevoerd, vereist Cloud POS Windows 8.1 of een later pc-besturingssysteem niet. Als het toepassingstype **Retail CloudPOS** is toegewezen aan een specifiek apparaat in Detailhandel Hoofdkantoor, kan dat apparaat worden gebruikt via de browser zonder dat u een pakket hoeft te downloaden of installeren. Cloud POS vereist een hardwarestation voor gebruik van andere hardware dan een toetsenbord voor het scannen van streepjescode.

### <a name="hardware-profile"></a>Hardwareprofiel

Navigatie: klik op **Commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**. Een hardwareprofiel identificeert de hardware die is verbonden met een POS-kassa of een hardwarestation. Het hardwareprofiel wordt ook gebruikt voor het opgeven van de parameters voor de betalingsverwerker die moeten worden gebruikt tijdens de communicatie met de betaling-SDK (Software Development Kit). (De betaling-SDK wordt geïmplementeerd als onderdeel van de hardwarestation.)

### <a name="hardware-station"></a>Hardwarestation

Navigatie: klik op **Detailhandel** &gt; **Kanalen** &gt; **Detailhandelwinkels** &gt; **Alle detailhandelwinkels**. Selecteer een winkel en klik vervolgens op het sneltabblad **Hardwarestations**. Een hardwarestation is een exemplaar van de bedrijfslogica die POS-randapparatuur aanstuurt. Een hardwarestations wordt automatisch geïnstalleerd samen met MPOS. Ook kan het hardwarestation worden geïnstalleerd als zelfstandig onderdeel en vervolgens door MPOS of Cloud POS worden geopend via een webservice. Het hardwarestation moet worden gedefinieerd op het kanaalniveau.

### <a name="hardware-station-profile"></a>Profiel van hardwarestation

Navigatie: klik op **Commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Profielen van hardwarestation**. Terwijl het hardwarestation zelf is opgegeven op kanaalniveau en exemplaarspecifieke gegevens bevat, zoals de URL van het hardwarestation, bevat het profiel van het hardwarestation informatie die statisch kan zijn of kan worden gedeeld door meerdere hardwarestations. De statische informatie bevat de poort die moet worden gebruikt, het hardwarestationpakket en het hardwareprofiel. De statische informatie bevat ook een beschrijving van het type hardwarestation dat wordt geïmplementeerd, zoals **Uitchecken** of **Retouren**, afhankelijk van de hardware die is vereist voor elk specifiek hardwarestation.

## <a name="scenarios"></a>Scenario's
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS met aangesloten randapparaten

[![Traditioneel, vast verkooppunt](./media/traditional-300x279.png)](./media/traditional.png) 

Als u MPOS wilt verbinden met POS-randapparaten volgens een traditioneel, vast POS-scenario, gaat u eerst naar de kassa zelf en wijst u hieraan een hardwareprofiel toe. U vindt de POS-kassa's onder **Detailhandel** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **Kassa's**. Nadat u het hardwareprofiel hebt toegewezen, synchroniseert u wijzigingen met de kanaaldatabase via de distributieplanning "Kassa's". U vindt de distributieplanningen onder **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanning**. Stel vervolgens een "lokaal" hardwarestation in op het kanaal. Klik op **Detailhandel** &gt; **Kanalen** &gt; **Detailhandelwinkels** &gt; **Alle detailhandelwinkels** en selecteer een winkel. Klik vervolgens op het sneltabblad **Hardwarestations** op **Toevoegen** om een hardwarestation toe te voegen. Voer een beschrijving in, voer **localhost** in als hostnaam en synchroniseer vervolgens de wijzigingen met het kanaal via de distributieplanning "Kanaalconfiguratie". U vindt de distributieplanningen onder **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanning**. Gebruik tot slot, in MPOS, de bewerking **Hardwarestation selecteren** om het hardwarestation **localhost** te selecteren. Stel het hardwarestation in op **Actief**. Het hardwareprofiel dat wordt gebruikt in dit scenario moet afkomstig zijn van de POS-kassa zelf. Een profiel voor een hardwarestation is niet vereist voor dit scenario. **Opmerking:** sommige hardwareprofielwijzigingen, zoals wijzigingen in kassalades, vereisen dat een nieuwe ploeg wordt geopend nadat de wijzigingen zijn gesynchroniseerd met het kanaal. **Opmerking:** Cloud POS moet gebruikmaken van het zelfstandige hardwarestation om te communiceren met randapparaten voor de detailhandel.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS of Cloud POS met een zelfstandig hardwarestation
[![Gedeelde randapparatuur](./media/shared-300x254.png)](./media/shared.png)

In dit scenario wordt een zelfstandig hardwarestation gedeeld door MPOS- en Cloud POS-clients. In dit scenario moet u een profiel voor een hardwarestation maken om het downloadpakket, de poort en het hardwareprofiel op te geven dat het hardwarestation gebruikt. U kunt het profiel voor een hardwarestation vinden onder **Detailhandel** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Profielen van hardwarestation**. Nadat u het profiel van een hardwarestation hebt gemaakt, gaat u naar het specifieke detailhandelskanaal (**Detailhandel** &gt; **Kanalen** &gt; **Detailhandelwinkels** &gt; **Alle detailhandelwinkels**) en voegt u een nieuw hardwarestation toe. Wijs dit nieuwe hardwarestation toe aan het profiel van een hardwarestation dat eerder is gemaakt. Geef vervolgens een beschrijving op die de kassamedewerker helpt bij het identificeren van het hardwarestation. Voer in het veld **Hostnaam** de URL in van de hostcomputer in de volgende indeling: **https://&lt;Computernaam:Poort&gt;/Hardwarestation**. (Vervang **&lt;Computernaam:Poort&gt;** met de werkelijke computernaam van het hardwarestation en de poort die is opgegeven in het profiel voor het hardwarestation.) Voor een zelfstandig hardwarestation moet u ook de terminal-ID voor elektronische betalingen (EFT) opgeven. Deze waarde identificeert de EFT-terminal die is verbonden met het hardwarestation als de betalingsconnector met de betalingsprovider communiceert. Ga vervolgens van de daadwerkelijke machine van het hardwarestation naar het kanaal en selecteer het hardwarestation. Klik vervolgens op **Downloaden** en installeer het hardwarestation. Gebruik vervolgens, vanuit MPOS of Cloud POS wolk, de bewerking **Hardwarestation selecteren** om het hardwarestation te selecteren dat eerder was geïnstalleerd. Selecteer **Koppelen** om een veilige verbinding tot stand te brengen tussen het POS en het hardwarestation. Deze stap moet één keer worden uitgevoerd voor elke combinatie van een POS en een hardwarestation. Nadat het hardwarestation is gekoppeld, wordt dezelfde bewerking gebruikt om het hardwarestation actief te maken terwijl het wordt gebruikt. In dit scenario moet het hardwareprofiel worden toegewezen aan het profiel voor het hardwarestation in plaats van de kassa zelf. Als om de een of andere reden een hardwareprofiel niet rechtstreeks aan een hardwarestation is toegewezen, wordt het hardwareprofiel gebruikt dat is toegewezen aan de kassa.

## <a name="client-maintenance"></a>Clientonderhoud
### <a name="registers"></a>Kassa's

POS-kassa's worden voornamelijk beheerd via de kassa's zelf en tevens via de profielen die zijn toegewezen aan kassa's. Kenmerken die specifiek zijn voor een afzonderlijk register worden beheerd op het kassaniveau. Deze kenmerken omvatten de winkel waar de kassa wordt gebruikt, het kassanummer, de beschrijving en de EFT-terminal-id die specifiek is voor de kassa zelf.

### <a name="pos-profiles"></a>POS-profielen

U vindt de POS-profielen onder **Detailhandel** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen**. Het is handig om vele aspecten van een kassa te beheren via profielen, omdat de profielen kunnen worden gedeeld door vele kassa's. Profielen kunnen worden toegewezen aan een afzonderlijke kassa of, als een profiel geldt voor de hele winkel, aan de detailhandelwinkel. In de volgende secties worden de POS-profielen beschreven en wordt aangegeven hoe ze worden gebruikt.

#### <a name="offline-profile"></a>Offlineprofiel

Het offline profiel wordt ingesteld op het winkelniveau. Het wordt gebruikt om de upload-instellingen op te geven voor transacties die worden uitgevoerd op een POS-kassa, terwijl die kassa niet is verbonden met de kanaaldatabase.

#### <a name="functionality-profile"></a>Functionaliteitsprofiel

Het functionaliteitsprofiel wordt ingesteld op het winkelniveau. Het wordt gebruikt om instellingen voor de hele winkel op te geven met betrekking tot de functies die kunnen worden uitgevoerd op het POS. De volgende mogelijkheden worden beheerd via het functionaliteitsprofiel. Deze mogelijkheden worden geordend per sneltabblad.

-   Sneltabblad **Algemeen**:
    -   International Organization for Standardization (ISO).
    -   Een klant aanmaken in offlinemodus.
    -   Profiel voor e-mail met ontvangstbewijs.
    -   Centrale aanmeldingsverificatie voor werknemers.
-   Sneltabblad **Functies**:
    -   Beheer van aanmelding en uitgebreide aanmelding.
    -   Financiële en aan valuta's gerelateerde aspecten van het POS, zoals de mogelijkheid om prijzen in te voeren en of decimalen zijn vereist voor kleingeld.
    -   Tijdsregistratie inschakelen via het POS.
    -   Hoe producten en betalingen worden weergegeven in het POS en op betalingsbewijzen.
    -   Beheer aan einde van dag.
    -   Parameters voor bewaren van kanaaldatabasetransacties.
    -   Hoe klanten worden opgezocht en gemaakt vanaf het POS.
    -   Hoe kortingen worden berekend.
-   Sneltabblad **Bedrag**:
    -   Maximale en minimale prijzen die zijn toegestaan.
    -   Toepassing en berekenen van korting.
-   Sneltabblad **Informatiecodes**:
    -   Alle aspecten van beheer van informatiecodes op het POS. Zie voor meer informatie [Informatiecodes](info-codes-retail.md).
-   Sneltabblad **Ontvangstbewijsnummering**:
    -   Geef maskers voor ontvangstnummer op. Deze kan segmenten bevatten voor het winkelnummer, het terminalnummer, constanten en of verkopen, retouren, verkooporders en offertes worden afgedrukt in aparte reeksen of allemaal dezelfde reeks volgen.

#### <a name="receipt-profiles"></a>Ontvangstbewijsprofielen

Ontvangstprofielen worden direct aan printers toegewezen binnen het hardwareprofiel. Zij worden gebruikt om de ontvangsttypen die worden afgedrukt op een specifieke printer op te geven. De profielen bevatten instellingen voor de ontvangstbewijsindelingen en instellingen die bepalen of het ontvangstbewijs altijd wordt afgedrukt dan wel of de kassamedewerker wordt gevraagd of het ontvangstbewijs moet worden afgedrukt. Verschillende printers gebruiken tevens mogelijk verschillende ontvangstbewijsprofielen. Zo is bijvoorbeeld printer 1 een standaard thermische printer voor ontvangstbewijzen, die daardoor kleinere ontvangstbewijsindelingen levert. Printer 2 is echter een volwaardige ontvangstbewijsprinter die alleen wordt gebruikt voor het afdrukken van ontvangstbewijzen voor klantorders, die meer ruimte vereisen.

#### <a name="hardware-profiles"></a>Hardwareprofielen

Eerder in dit artikel werd uitgelegd dat hardwareprofielen onderdeel van de clientinstellingen vormen. Hardwareprofielen worden rechtstreeks aan de POS-kassa of naar een profiel van een hardwarestation toegewezen. Zij worden gebruikt om aan te geven welke typen apparaten door een specifieke POS-kassa of hardwarestation worden gebruikt. Hardwareprofielen worden ook gebruikt om de EFT-instellingen op te geven die worden gebruikt om te communiceren met de betaling-SDK.

#### <a name="visual-profiles"></a>Weergaveprofielen

Visuele profielen worden toegewezen op het kassaniveau. Zij worden gebruikt om het thema voor een specifieke kassa op te geven. De profielen omvatten instellingen voor het type toepassing dat wordt gebruikt (MPOS of Cloud POS), de accentkleur en het thema, het lettertypeschema, de aanmeldingsachtergrond en de POS-achtergrond.

### <a name="custom-fields"></a>Aangepaste velden

U kunt aangepaste velden maken om velden toe te voegen die niet standaard aan het POS worden verschaft. Zie voor meer informatie over het gebruik van aangepaste velden het blogbericht [Werken met aangepaste velden](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Tekst taal

U kunt standaardtekenreeksen in het POS overschrijven met behulp van invoer van taalteksten. U kunt een tekenreeks in het POS overschrijven door een nieuwe taaltekstregel toe te voegen. Geef vervolgens een id, de standaardtekenreeks die moet worden overschreven en de tekst die moet worden weergegeven op het POS in plaats van de standaardtekst op.

### <a name="hardware-station-profiles"></a>Profielen van hardwarestation

Profielen van hardwarestation worden eerder in dit artikel beschreven. Zij worden gebruikt voor het toewijzen van niet-exemplaarspecifieke gegevens aan hardwarestations.

### <a name="channel-reports-configuration"></a>Configuratie van afzetkanaalrapporten

U stelt de rapporten die beschikbaar zijn in het detailhandelkanaal in op de pagina **Configuratie van afzetkanaalrapporten van detailhandel**. U kunt nieuwe rapporten maken door de XML-definitie van het rapport op te geven en het rapport toe te wijzen aan een specifieke machtigingsgroep op het POS.

### <a name="devices"></a>Apparaten

Apparaten worden eerder in dit artikel beschreven. Zij worden gebruikt voor het beheren van de activering van een specifieke POS-kassa. Apparaten worden ook gebruikt om de toepassing op te geven die wordt gebruikt voor een specifieke kassa en het installatiepakket dat moet worden gebruikt voor het installeren van de MPOS-client. Hier volgen de statussen voor apparaatactivering:

-   **In behandeling**: het apparaat is klaar om te worden geactiveerd.
-   **Geactiveerd**: het apparaat is geactiveerd.
-   **Gedeactiveerd**: het apparaat is uitgeschakeld in Detailhandel Hoofdkantoor of via het POS.
-   **Uitgeschakeld**: het apparaat is uitgeschakeld.

Meer informatie met betrekking tot activering omvat de werknemer die de activeringsstatus voor het apparaat heeft gewijzigd, een tijdstempel voor de activering en of de apparaatconfiguratie is geverifieerd.

### <a name="client-data-synchronization"></a>Synchronisatie van clientgegevens

Alle wijzigingen in een POS-client, met uitzondering van de wijzigingen in de status van de apparaatactivering, worden pas van kracht na synchronisatie met de kanaaldatabase. Om wijzigingen te synchroniseren met de kanaaldatabase, gaat u naar **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanning** en voert u de vereiste distributieplanning uit. Voor clientwijzigingen moet u de distributieplanningen "Kassa's" en "Kanaalconfiguratie" uitvoeren.




