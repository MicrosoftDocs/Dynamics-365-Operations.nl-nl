---
title: Randapparatuur simulator detailhandel
description: Dit onderwerp beschrijft de randapparatuur simulator tool die wordt geleverd met Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Randapparatuur simulator detailhandel

Dit onderwerp beschrijft de randapparatuur simulator tool die wordt geleverd met Microsoft Dynamics 365 for Operations - Retail.

<a name="overview"></a>Overzicht
--------

De Microsoft Dynamics 365 for Operations - randapparatuur simulator Retail is een hulpprogramma waarmee u instellen kunt, testen en oplossen van randapparatuur die worden gebruikt in omgevingen met retail. U kunt de randapparatuur simulator stroomlijnen het testen van retail randapparatuur en opsporen van problemen die worden veroorzaakt door onjuiste instellingen of stuurprogramma's niet goed functioneert. De simulator randapparatuur bevat elk programma dat functies virtuele versies van apparaten die Dynamics 365 for Operations - Retail ondersteunt. Een sectie voor elk virtueel apparaat ziet u de interactie tussen het apparaat en het punt detailhandel van verkooppunten (POS). Ook kunt u deze gegevens invoeren die geldig is voor verschillende POS-scenario's. De randapparatuur simulator ondersteunt interactie tussen het POS en de volgende virtuele apparaten:

-   **Printer** : de randapparatuur simulator ontvangsten die zijn geconfigureerd voor een POS-printer kunt weergeven.
-   **Weergave-regel** : U kunt een virtuele regelweergave activiteit om op te geven een fysieke regelweergave configureren.
-   **Magneetstriplezer (MSR)** : U kunt gesimuleerde magneetstrip gebeurtenissen naar het POS verzenden vanuit de randapparatuur simulator.
-   **Lade** : U kunt een fysieke kassalade simuleren.
-   **Lade 2** : door een tweede kassalade in de randapparatuur simulator instelt, kunt u scenario's voor een enkele POS-kassa met twee actieve ploegen simuleren.
-   **Scanner** : de virtuele streepjescodescanner die ondersteuning biedt voor de randapparatuur simulator Streepjescode scannen gebeurtenissen kan worden verleend.
-   **Schaal** : een virtuele schaal kunt u de interactie tussen gewogen artikelen en het POS simuleren.
-   **Persoonlijke identificatienummer (PIN) toetsenblok** : U kunt simuleren PIN toetsenblok bewerkingen. **opmerking:** ondersteuning voor een fysieke pinapparaat via de betalingsconnector moet worden geïmplementeerd.
-   **Handtekeningregistratie** : de simulator randapparatuur bevat een virtueel apparaat voor handtekeningregistratie die u wilt worden gevraagd voor handtekeningen die vereist voor offertes, zoals klantbetalingen rekening zijn kunt instellen.

U kunt ook de randapparatuur simulator toetsenbord wig gebeurtenissen die afkomstig van een streepjescodescanner en MSR zijn simuleren. De virtuele randapparatuur simulator ondersteunt specifiek Object Linking and Embedding voor Retail POS (OPOS) apparaten.

## <a name="key-scenarios"></a>Belangrijke scenario 's
### <a name="troubleshooting"></a>Problemen oplossen

U kunt de randapparatuur simulator oplossen apparaat instellen. Als er geen de simulator randapparatuur of een tweede apparaat van dezelfde klasse, kan het lastig zijn om te bepalen waar problemen afkomstig zijn. Echter wanneer u de randapparatuur simulator hebt, kunt u virtuele apparaten instellen en uitvoeren van de codepaden met dezelfde en zakelijke logica die worden gebruikt voor fysieke apparaten. Vanuit het perspectief van de randapparatuur simulator is het belangrijkste verschil tussen de virtuele apparaten en fysieke apparaten het serviceobject of stuurprogramma's. Voor de fysieke apparaten wordt het serviceobject geleverd door de fabrikant van het apparaat. De serviceobjecten worden daarentegen voor de randapparatuur simulator geleverd als onderdeel van de randapparatuur simulator. Wanneer de randapparatuur simulator correct werkt als een apparaat niet goed werkt nadat de apparaatnaam in het hardwareprofiel op de naam van een echt apparaat is gewijzigd, kunt u ervan uitgaat dat er een probleem is met het serviceobject die de fabrikant geleverd.

### <a name="training"></a>Opleiding

U kunt de randapparatuur simulator toevoegen een realistische laag om de kassamedewerker training als een fysieke hardware-instellingen niet beschikbaar. Wanneer de randapparatuur simulator is opgenomen in de training scenario's, kan efficiënter de kassamedewerker interactie met het POS door invoer zoals product code scans en gift kaart swipes en door te bekijken welke ontvangsten worden afgedrukt voor een specifieke transactie.

### <a name="testing"></a>Testen

U kunt de randapparatuur simulator product streepjescodes, ontvangstbewijsindelingen, enzovoort, testen zonder fysieke hardware in een virtuele omgeving implementeren. Omdat de fysieke hardware niet vereist en u geen implementatie van een POS-client op een hardware-station of een fysieke computer, kunt u sneller wijzigingen die zijn aangebracht in de back office testen.

## <a name="set-up-the-peripheral-simulator"></a>De randapparatuur simulator instellen
### <a name="set-up-a-hardware-profile"></a>Een hardwareprofiel instellen

1.  Als u de randapparatuur simulator instellen, gaat u naar **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profielen**&gt;**hardwareprofielen**.
2.  Een nieuw profiel toevoegen, klikt u op **New**.
3.  Voer waarden in de **Profielnummer** en **omschrijving** velden.
4.  Gebruik de volgende tabel om in te stellen van de virtuele apparaten die moeten worden getest. Hier volgt een uitleg van de kolommen in de tabel:
    -   **Apparaat** – deze kolom geeft de naam van het sneltabblad dat u uitbreiden om het apparaat in te stellen.
    -   **Apparaattype** – deze kolom geeft de waarde die u selecteert in het veld dat wordt aangeduid met de naam van het apparaat.
    -   **Apparaatnaam** – deze kolom geeft de exacte waarde die u voor de apparaatnaam invoert. **Belangrijk:** de namen die hier zijn gegeven zijn vereist, omdat het station hardware deze specifieke namen gebruikt om de apparaten. Als u deze specifieke namen niet gebruikt, is het apparaat niet kan worden gebruikt.

    | Apparaat            | Apparaattype | Apparaatnaam              |
    |-------------------|-------------|--------------------------|
    | Printer           | OPOS        | MockOPOSPrinter          |
    | Regelweergave      | OPOS        | MockOPOSLineDisplay      |
    | MSR               | OPOS        | MockOPOSMSR              |
    | Wisseluitschrijver            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Scanner           | OPOS        | MockOPOSScanner          |
    | Schaal             | OPOS        | MockOPOSScale            |
    | Pinapparaat           | OPOS        | MockOPOSPinPad           |
    | Handtekeningregistratie | OPOS        | MockOPOSSignatureCapture |

**opmerking:** geen specifieke instellingen in het hardwareprofiel is vereist voor het simuleren van toetsenbord wig gebeurtenissen van de scanner voor streepjescodes en MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Het hardwareprofiel aan een kassa toewijzen

1.  Nadat het hardwareprofiel is gemaakt, gaat u naar **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**registreert**.
2.  In de **POS-kassa's** lijst, klikt u op de koppeling in de **kassanummer** -veld voor het journaal dat de randapparatuur simulator moet worden gebruikt.
3.  Klik op **Bewerken**.
4.  In de **profielen** gedeelte in de **hardwareprofiel** veld, selecteert u het hardwareprofiel dat u hebt gemaakt voor virtuele randapparatuur.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen in de kanaaldatabase synchroniseren

1.  Ga naar **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributieplanning**.
2.  Selecteer de **1090** distributieplanning.
3.  Klik op **nu uitvoeren** te synchroniseren van wijzigingen in het POS.

Nadat de gegevens zijn gesynchroniseerd, zijn de nieuwe hardwareprofiel en wijzigingen in het register beschikbaar in de kanaaldatabase.

## <a name="install-the-peripheral-simulator"></a>De randapparatuur simulator installeren
1.  Ga naar **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profielen**&gt;**hardwareprofielen**.
2.  Klik op **downloaden**, en klik vervolgens op **PeripheralSimulator**. **opmerking:** moet u pop-upblokkeringsprogramma's uitschakelen voordat u de randapparatuur simulator kunt downloaden.
3.  Nadat het downloaden is voltooid, opent u het **Downloads** map en dubbelklik op **VirtualPeripherals.msi** het installatieprogramma te starten.
4.  De randapparatuur simulator installeren via de standaardinstellingen.

Naast de randapparatuur simulator, moet u de gebruikte control-objecten van Monroe Consulting Services installeren. Anders wordt werkt de randapparatuur simulator niet correct. Als u wilt downloaden van de gebruikte control-objecten, gaat u naar <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Met behulp van de randapparatuur simulator
U start de randapparatuur simulator, klikt u op **starten** op uw computer, typt u **detailhandel randapparatuur simulator**, en selecteer vervolgens de app wanneer deze wordt weergegeven in de zoekresultaten. Nadat u de randapparatuur simulator start, klikt u op een apparaatnaam om te zien van de ondersteunde apparaten. Deze apparaten wordt weergegeven als tabbladen aan de linkerkant van het venster. Klik op het tabblad voor het apparaat een bepaald apparaat.

### <a name="line-display-capabilities"></a>Regel weergavemogelijkheden

De regelweergave is het eerste apparaat dat wordt vermeld in de randapparatuur simulator. Wanneer de virtuele regelweergave wordt geconfigureerd, zien hierin regelartikelen worden gecontroleerd in de POS-transactie. De weergave bevat naast regelartikelen, het totaal dat is verschuldigd als een betaling is geselecteerd op het POS. Het saldo die verwacht wordt ook weergegeven als een betaling wordt ingevoerd, maar nog steeds een saldo is verschuldigd voor de transactie. Wanneer het POS niet wordt gebruikt, kan een bericht weergegeven om aan te geven dat de kassa gesloten is. Moet u het bericht op de **weergave regel** sneltabblad in het hardwareprofiel.

### <a name="cash-drawer-capabilities"></a>Mogelijkheden voor cash-lade

De kassalade wordt het tweede apparaat dat wordt vermeld in de randapparatuur simulator. Wanneer het hardwareprofiel is geconfigureerd voor gebruik van virtuele kassalades, het POS de kassalade voor de actieve ploeg geopend naar aanleiding van ladebewerkingen zoals kascontroles, en zodat de kassamedewerker kunt wijzigen of storting van contant geld tijdens standaard cash-and-carry transacties. De virtuele kassalades hebben de labels **hoofdtabel lade** en **secundaire lade**. Deze labels geven lade en lade 2 in het hardwareprofiel respectievelijk. Wanneer een lade is gesloten, een afbeelding van een gesloten kassalade wordt weergegeven en de knop op de gesloten kassalade heet **lade openen**. Als u op deze knop klikt, wordt de afbeelding vervangen door een afbeelding van een kassalade openen om aan te geven dat de lade nu geopend is. De knop op de kassalade openen heet **sluit lade**. Meerdere bewerkingen op het POS kunnen leiden tot de kassalade te openen. De meeste bewerkingen kunnen niet worden voortgezet terwijl de kassalade geopend wordt. De uitzonderingen zijn sommige procedures voor einde dag. Als de POS-gebruiker een foutbericht waarin wordt gemeld ontvangt dat een bewerking kan niet worden uitgevoerd terwijl de kassalade geopend wordt, moet de gebruiker sluit de virtuele of fysieke kassalade om door te gaan. Als een kassalade is gemarkeerd als **gedeeld** in het hardwareprofiel het systeem niet controleren of de lade vóór een bewerking is gesloten. De bewerking gaat door zoals gebruikelijk, zelfs als de kassalade geopend wordt. Dit gedrag ondersteunt scenario's waarbij kassalades worden gedeeld door verkoopmedewerkers en één koppelen wordt een kassalade gebruikt terwijl een andere partner niet-gerelateerde taken op zijn of haar eigen POS-apparaat uitvoert. Wijzigingen die zijn aangebracht in de kassalade niet duidelijk totdat de huidige ploeg wordt gesloten en een nieuwe ploeg wordt geopend.

### <a name="msr-capabilities"></a>MSR-mogelijkheden

De randapparatuur simulator biedt krachtige ondersteuning voor virtuele MSR bewerkingen door in de OPOS-modus of toetsenbord wig-modus te werken. OPOS-modus is vereist dat de MSR worden geconfigureerd in het hardwareprofiel werken als een OPOS-apparaat. Toetsenbord wig modus stuurt NET toetsenbordgebeurtenissen wig gegevens naar Microsoft Windows. Naast de verschillen in instellingen verschillen OPOS en toetsenbord wig-modus op de volgende manieren:

-   De POS-client kunt OPOS MSR-apparaten voor specifieke scenario's, zoals de scenario's waarmee gegevens van de magneetstrip voor loyale of post van de geschenkbon.
-   In de modus voor toetsenbord wig verzendt de randapparatuur simulator toetsenbord wig gegevens naar het veld dat wordt geactiveerd wanneer de gegevens worden verzonden. Dit probleem lijkt op wat er gebeurt als de gegevens worden ingevoerd met behulp van een toetsenbord. Als u wilt gebruiken de MSR als een toetsenbord wig, moet de gebruiker naar Retail moderne POS (MPOS) om ervoor te zorgen dat gegevens worden ontvangen in het juiste veld overschakelen. U kunt daarom een vertraging configureren zodat de gebruiker tijd om ervoor te zorgen heeft dat de gegevens worden verzonden naar het juiste veld.

#### <a name="testing-gift-and-payment-card-swipes"></a>Cadeau- en betalingsgegevens kaart swipes testen

De virtuele MSR waarmee de randapparatuur simulator ook kunt u specifieke MSR gegevens om te testen van scenario's voor het gift- en betalingsgegevens kaart swipes configureren. Klik op het plusteken (+) om een kaart (**+**) en selecteer het type kaart. Vervolgens geeft u het kaartnummer of bij te houden van gegevens die moeten worden verzonden naar de POS, samen met de vervaldatum maand en jaar voor de kaart die u definieert. De waarde die u selecteert in de **Type kaart** veld is alleen een label die kan worden toegewezen aan een kaart. Dit label gemakkelijker kaarten kunt herkennen wanneer ze via de randapparatuur simulator worden gehaald. U kunt de kaarten die zijn geconfigureerd in de randapparatuur simulator met behulp van de pijl naar links selecteren (**&lt;**) en rechterpijl (**&gt;**) knoppen boven de afbeelding van de kaart. U kunt bewerken en kaarten verwijderen met behulp van de **bewerken** en **verwijderen** knoppen naast het plusteken (**+**) knop.

### <a name="pin-pad"></a>Pinapparaat

U kunt de simulator PIN toetsenblok om te simuleren van een OPOS-pinapparaat configureren. Wanneer een overboekingstransactie van elektronische betaling (EFT) wordt uitgevoerd op het POS en PIN-vermelding vereist, roept de hardware-station het PIN-apparaat voor de invoer van PIN wordt gevraagd. Als u wilt werken, vereist het pinapparaat in de randapparatuur simulator EFT betaling connector ondersteuning.

### <a name="printer"></a>Printer

De virtuele randapparatuur printer wordt nu ontvangsten terwijl deze worden afgedrukt op het POS. Als er een af te drukken bewerking door meerdere ontvangsten, kunt u de ontvangsten doorloopt.

#### <a name="configure-receipt-printing"></a>Configureren van ontvangstbewijzen af te drukken

1.  Ga naar **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profielen**&gt;**hardwareprofielen**.
2.  Selecteer het hardwareprofiel dat u hebt gemaakt voor virtuele randapparatuur.
3.  Op de **Printer** sneltabblad, klikt u op **bewerken**.
4.  In de **id ontvangstbewijsprofiel** veld, selecteert u een ontvangstbewijsprofiel.
5.  Click **Save**.

### <a name="scale"></a>Schaal

Wanneer een product op schaal wordt toegevoegd aan de POS-transactie en een schaal is geconfigureerd, worden het gewicht in het POS opgehaald uit de schaal. Voor zowel de virtuele en fysieke schaal, moet het product of het gewicht worden opgegeven voordat het product wordt toegevoegd aan de transactie. Voordat u het product op schaal aan de transactie toevoegen, gaat u naar de schaal van de randapparatuur simulator en gebruik de plus-teken (**+**) en het minteken (**:**) knoppen aanpassen van het gewicht dat de schaal moet rapporteren. U kunt ook opgeven met de gewenste dikte rechtstreeks in de **huidige waarde** veld. U kunt de eenheden van het gewicht van de schaal aanpassen met behulp van de plus-teken (**+**), **bewerken**, en **verwijderen** knoppen. Op deze manier kunnen eenheden worden opgegeven op basis van de producten die worden gewogen of de landinstelling waar de schaal wordt gebruikt.

#### <a name="configure-a-scale-product"></a>Een product op schaal configureren

1.  Ga naar **detailhandel en****commerce**&gt;**producten en categorieën**&gt;**vrijgegeven producten per categorie**.
2.  Open de productrecord.
3.  Selecteer het product te wegen.
4.  Op de **detailhandel** sneltabblad instellen de **product op schaal** optie uit **Nee** naar **Ja**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen in de kanaaldatabase synchroniseren

1.  Ga naar **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributieplanning**.
2.  Selecteer de **1040** distributieplanning.
3.  Klik op **nu uitvoeren** te synchroniseren van wijzigingen in het POS.

Nadat de gegevens zijn gesynchroniseerd, wanneer een product op schaal wordt toegevoegd aan de POS-transactie, controleert het POS de schaal voor het gewicht.

### <a name="signature-capture"></a>Handtekeningregistratie

Het virtuele apparaat voor handtekeningregistratie vraagt de gebruiker op te geven van een handtekening in het pad virtuele handtekening vastleggen wanneer een handtekening is vereist voor de betalingsmethode die wordt gebruikt. De gebruiker kan de handtekening weergeven op het POS accepteren. De kassamedewerker kan de handtekening vervolgens accepteren. De handtekening wordt vervolgens opgeslagen samen met de betaling en wordt gesynchroniseerd met de BackOffice samen met andere transactiegegevens.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Instellen van een offerte een handtekening vereisen

1.  Ga naar **detailhandel en commerce**&gt;**kanalen**&gt;**detailhandel**&gt;**alle detailhandel**.
2.  Selecteer de winkel.
3.  Klik op **Bewerken**.
4.  Klik op **instellen**, en klik in de **instellen** sectie, klikt u op **betalingsmethoden**.
5.  Klik op **Bewerken**.
6.  Selecteer de betalingsmethode waarvoor een handtekening.
7.  In de **algemeen** gedeelte onder **handtekening vastleggen**, geeft de **apparaat voor handtekeningregistratie gebruik** optie naar **Ja**.
8.  In de **Minimumbedrag handtekeningregistratie** en voer het minimumbedrag waarmee handtekeningregistratie moet worden geactiveerd.

#### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen in de kanaaldatabase synchroniseren

1.  Ga naar **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributieplanning**.
2.  Selecteer de **1070** distributieplanning.
3.  Klik op **nu uitvoeren** te synchroniseren van wijzigingen in het POS.

Nadat de gegevens zijn gesynchroniseerd, wanneer een betaling waarvoor een handtekening wordt gebruikt en het bedrag voldoet aan de drempel handtekening, wordt de gevraagd voor een handtekening op de virtuele handtekeningapparaat.

## <a name="additional-configuration"></a>Aanvullende configuratie
U kunt de randapparatuur simulator configuratiebestand om de scenario's die u beter op te lossen bewerken. U vindt het configuratiebestand op C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Het configuratiebestand definieert de eenheden die beschikbaar zijn voor het testen op de schaal, de kaarttypen die beschikbaar zijn voor het testen en streepjescodetypen. Bijvoorbeeld de tekstwaarden in het configuratiebestand wordt aangepast, kunt u toevoegen een nieuw kaarttype of maateenheid die kan worden geselecteerd tijdens de uitvoering. De nieuwe waarden worden weergegeven nadat de toepassing opnieuw is opgestart.

## <a name="troubleshooting"></a>Problemen oplossen
Activiteiten voor de randapparatuur simulator worden vastgelegd in de randapparatuur simulator. Het logboek is te vinden op C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. De randapparatuur simulator rapporten ook problemen met de Windows-gebeurtenislogboek, waarin u via openen kunt **toepassing Logboeken en Services**&gt;**Microsoft**&gt;**DynamicsAX**. Als wijzigingen die u hebt aangebracht aan het hardwareprofiel of andere gebieden niet duidelijk wanneer u MPOS of de randapparatuur simulator, controleert u plannertaken distributie die u gebruikt om de gegevens naar de kanaaldatabase te synchroniseren. Als de wijzigingen zijn gesynchroniseerd, maar nog steeds niet duidelijk op het POS, moet u de POS-client opnieuw opstarten. Wijzigingen in de geconfigureerde kassalades niet effectief totdat een nieuwe ploeg wordt gemaakt. Als u wijzigingen in de kassalades aanbrengt, let er daarom altijd de bestaande shift om de nieuwe instellingen van de kas-lade testen te sluiten. Soms als het stuurprogramma van de fabrikant is geïnstalleerd na de gebruikte control-objecten van de ondersteuningsdiensten van Monroe, het stuurprogramma kan leiden tot de gebruikte control-objecten niet langer goed werkt. In dit geval moet u de algemene controle objecten opnieuw installeren.

<a name="see-also"></a>Zie ook
--------

[Retail randapparatuur-overzicht](retail-peripherals-overview.md)


