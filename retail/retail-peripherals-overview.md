---
title: Retail randapparatuur-overzicht
description: Dit onderwerp worden de concepten die zijn gerelateerd aan retail randapparatuur. Hierin worden de verschillende manieren randapparatuur kunnen worden aangesloten op het punt van verkoop (POS) en de onderdelen die verantwoordelijk zijn voor het beheren van de verbinding met het POS.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Retail randapparatuur-overzicht

Dit onderwerp worden de concepten die zijn gerelateerd aan retail randapparatuur. Hierin worden de verschillende manieren randapparatuur kunnen worden aangesloten op het punt van verkoop (POS) en de onderdelen die verantwoordelijk zijn voor het beheren van de verbinding met het POS.

<a name="concepts"></a>Concepten
--------

### <a name="pos-registers"></a>POS-kassa's

Navigatie: Klik op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**registreert**. Het punt van de kassa verkooppunten (POS) is een entiteit die wordt gebruikt voor het definiëren van de kenmerken van een specifiek exemplaar van het POS. Deze kenmerken omvatten het hardwareprofiel of instellingen voor retail randapparatuur die wordt gebruikt bij de kassa en de winkel die het journaal is toegewezen aan de visuele ervaring voor de gebruiker die zich bij die kassa aanmeldt.

### <a name="devices"></a>Apparaten

Navigatie: Klik op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**apparaten**. Een apparaat is een entiteit die een fysiek exemplaar vertegenwoordigt van een apparaat dat is toegewezen aan een POS-kassa. Wanneer een apparaat wordt gemaakt, toegewezen aan een POS kassa. De apparaatentiteit houdt informatie bij over wanneer een POS-kassa wordt geactiveerd, het type client dat wordt gebruikt en het toepassingspakket dat is geïmplementeerd op een specifiek apparaat. Apparaten kunnen worden toegewezen aan de volgende toepassingstypen: Retail POS op moderne, Cloud-POS detailhandel Retail moderne POS – Windows Phone, moderne detailhandel-POS-Android en moderne POS detailhandel: iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Moderne POS is het POS-programma voor Microsoft Windows. Deze kan worden geïmplementeerd op de besturingssystemen Windows 10 (OSs).

### <a name="cloud-pos"></a>Cloud POS

Cloud POS is een browser gebaseerde versie van het programma moderne POS die kan worden geopend in een webbrowser.

### <a name="modern-pos-for-ios"></a>Moderne POS voor iOS

Moderne POS voor iOS is een iOS-versie van het moderne POS-programma dat kan worden geïmplementeerd op iOS-apparaten.

### <a name="modern-pos-for-android"></a>Moderne POS voor Android

Moderne POS voor Android is een Android-versie van het moderne POS-programma dat kan worden geïmplementeerd op Android apparaten.

### <a name="pos-peripherals"></a>POS-randapparatuur

POS-randapparatuur zijn apparaten die expliciet worden ondersteund voor POS-functies. Deze randapparatuur worden meestal onderverdeeld in specifieke klassen. Zie de sectie 'Apparaatklassen' van dit onderwerp voor meer informatie over deze klassen.

### <a name="hardware-station"></a>Hardwarestation

Navigatie: Klik op **detailhandel en commerce**&gt;**kanalen**&gt;**detailhandel**&gt;**alle detailhandel**. Selecteer een winkel en klik vervolgens op het sneltabblad **Hardwarestations**. De **Hardware station** instelling is een kanaal-niveau-instelling die wordt gebruikt voor het definiëren van gevallen waarin de retail-randapparatuur logica wordt geïmplementeerd. Deze instelling op het niveau van het kanaal wordt gebruikt om te bepalen van de kenmerken van de hardware-station. Dit wordt ook gebruikt voor lijst hardware stations die beschikbaar voor een moderne POS-instantie in een bepaald archief zijn. Het station hardware is ingebouwd in de moderne POS-programma voor Windows. De hardware-station kan ook onafhankelijk van elkaar worden geïmplementeerd als een zelfstandig programma van Microsoft Internet Information Services (IIS). In dit geval wordt het toegankelijk via een netwerk.

### <a name="hardware-profile"></a>Hardwareprofiel

Navigatie: Klik op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profielen**&gt;**hardwareprofielen**. Het hardwareprofiel is een lijst met apparaten die zijn geconfigureerd voor een POS-kassa of een hardware-station. Het hardwareprofiel kan worden toegewezen rechtstreeks aan een POS-kassa of een hardware-station.

## <a name="devices-classes"></a>Klassen van apparaten
POS-randapparatuur zijn meestal verdeeld in klassen. Deze sectie wordt beschreven en vindt u een overzicht van de apparaten die ondersteuning biedt voor moderne POS.

### <a name="printer"></a>Printer

Printers omvatten die traditioneel POS-printers voor ontvangstbewijzen en volledige pagina printers. Printer worden ondersteund via OLE voor interfaces van Retail POS (OPOS) en Microsoft Windows-stuurprogramma. Tegelijkertijd kunnen maximaal twee printers worden gebruikt. Deze mogelijkheid ondersteunt scenario's waarin cash-and-carry Klantontvangstbewijzen worden afgedrukt op printers voor ontvangstbewijzen, terwijl de klantorders, die meer informatie bevatten, worden afgedrukt op een volledige pagina printer. Printers voor ontvangstbewijzen kunnen worden aangesloten rechtstreeks op een computer via USB, met een netwerk verbonden via Ethernet, of via Bluetooth.

### <a name="scanner"></a>Scanner

Maximaal twee streepjescode kunnen scanners tegelijkertijd worden gebruikt. Deze functionaliteit ondersteunt scenario's waarin een scanner die is meer mobiele vereist voor het scannen van grote of zware artikelen, is terwijl een vaste ingesloten scanner wordt gebruikt voor de meeste Standaardformaatapparaat artikelen sneller uitchecktijden. Scanners worden ondersteund via OPOS, universele Windows-Platform (UWP) of toetsenbord wig interfaces. USB- of Bluetooth-kan worden gebruikt om verbinding maken met een scanner met een computer.

### <a name="msr"></a>MSR

Een USB-Magneetstriplezer (MSR), kunt u instellen met behulp van de OPOS-stuurprogramma's. Als u een zelfstandige MSR voor betalingstransacties van elektronische betalingen transfer (EFT) gebruiken wilt, moet de MSR worden beheerd door een betalingsconnector. Zelfstandige MSRs kunnen worden gebruikt voor loyale klantenpost werknemer aanmelden en post van de geschenkbon, onafhankelijk van de betalingsconnector.

### <a name="cash-drawer"></a>Kassalade

Twee kassalades worden ondersteund per hardwareprofiel. Hierdoor kan twee actieve ploegen per kassa beschikbaar wilt stellen op hetzelfde moment. In het geval van een gedeelde ploegendienst of een kassalade die wordt gebruikt door meerdere mobiele POS-apparaten tegelijk, is per hardwareprofiel kassalade slechts één toegestaan. Kassalades kunnen worden rechtstreeks aangesloten op een computer via USB, verbonden met een netwerk of verbonden met een printer voor ontvangstbewijzen via een RJ12-interface. In sommige gevallen kunnen kassalades ook worden gekoppeld via Bluetooth.

### <a name="line-display"></a>Regelweergave

Weergegeven worden gebruikt voor producten, prognosetransactiesaldi en andere nuttige informatie aan de klant tijdens een transactie weergeven. Regelweergave met één kan worden gekoppeld aan de computer via USB via OPOS-stuurprogramma's.

### <a name="signature-capture"></a>Handtekeningregistratie

Handtekeningapparaten kunnen rechtstreeks op een computer via USB via OPOS-stuurprogramma's worden gekoppeld. Bij het vastleggen van de handtekening is geconfigureerd, wordt de klant gevraagd aan te melden op het apparaat. Nadat de handtekening is opgegeven, ziet u de kassamedewerker acceptatie.

### <a name="scale"></a>Schaal

Tarieven kunnen worden gekoppeld aan de computer via USP via OPOS-stuurprogramma's. Wanneer een product dat is gemarkeerd als 'Weighed' product wordt toegevoegd aan een transactie, het POS leest het gewicht van de schaal het product aan de transactie toegevoegd en wordt de hoeveelheid die de schaal wordt gebruikt.

### <a name="pin-pad"></a>Pinapparaat

Persoonlijke identificatienummer (PIN) cijfertoetsen worden ondersteund via OPOS, maar ze moeten worden beheerd via een betalingsconnector.

### <a name="secondary-display"></a>Secundaire weergave

Wanneer een secundair beeldscherm is geconfigureerd, wordt het getal 2 Windows display gebruikt voor algemene informatie weergeven. Het doel van de secundaire weergave is ter ondersteuning van independent software vendor (ISV) verlenging omdat uit de verpakking, de secundaire weergave niet geconfigureerd is en beperkte inhoud geeft.

### <a name="payment-device"></a>Betalingsapparaat

Ondersteuning voor betaling-apparaat is geïmplementeerd via de betalingsconnector. Betaling apparaten kunnen uitvoeren voor een of meer van de functies die andere apparaatklassen bevatten. Bijvoorbeeld kan een betalingsapparaat functioneren als een MSR/kaartlezer, regelweergave, apparaat voor handtekeningregistratie of pinapparaat. Ondersteuning voor betaling apparaten onafhankelijk van de ondersteuning voor zelfstandige apparaten die wordt geleverd voor andere apparaten die zijn opgenomen in het hardwareprofiel is geïmplementeerd.

## <a name="supported-interfaces"></a>Ondersteunde interface
### <a name="opos"></a>OPOS

Om te garanderen dat het grootste aantal apparaten kan worden gebruikt met Microsoft Dynamics 365 for Operations - detailhandel, de OLE voor POS industriestandaard is de primaire retail randapparaat platform dat wordt ondersteund in Microsoft Dynamics 365 for Operations - Retail. De OLE voor POS-standaard is geproduceerd door de nationale Retail Federation (NRF), waaruit blijkt dat industriestandaard communicatieprotocollen voor randapparatuur retail. OPOS is een verbreide implementatie van de OLE voor POS-standaard. Deze is ontwikkeld in het midden-jaren 1990 en verschillende keren sinds die tijd is bijgewerkt. OPOS geeft een apparaat-stuurprogramma-architectuur waarmee eenvoudige integratie van POS-hardwareprofiel met Windows-gebaseerde POS-systemen. OPOS ingang communicatie tussen hardware en de POS-software controleert. Een OPOS-besturingselement bestaat uit twee onderdelen:

-   **Control-object** : het control-object voor een apparaatklasse (zoals weergegeven) biedt de interface voor het programma. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) biedt een gestandaardiseerde reeks OPOS control-objecten die bekend staan als de gebruikte control-objecten (CCOs). De CCOs worden gebruikt voor het testen van de POS-component van Microsoft Dynamics 365 voor bewerkingen: Retail. Daarom zorgt het testen ervoor dat, als u Microsoft Dynamics 365 for Operations - Retail ondersteunt een apparaatklasse via OPOS, typen veel apparaten worden ondersteund, opgeeft dat de fabrikant een serviceobject dat is gebouwd voor OPOS biedt. U hebt geen expliciet elk apparaattype te testen.
-   **serviceobject** : het serviceobject zorgt voor communicatie tussen het control-object (CCO) en het apparaat. Het serviceobject voor een apparaat wordt normaal gesproken geleverd door de fabrikant van het apparaat. Echter, in sommige gevallen moet u wellicht het serviceobject downloaden vanaf de website van de fabrikant. Een meer recente serviceobject worden beschikbaar. Het adres van de website van de fabrikant, Zie de documentatie bij uw hardware.

[![Object en serviceobject](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) ondersteuning voor de OPOS-implementatie van OLE voor POS zorgt u ervoor dat, als de apparaatfabrikanten en uitgevers POS worden de standaard correct geïmplementeerd, POS-systemen en ondersteunde apparaten samenwerken kunnen, zelfs als ze eerder samen zijn niet getest. **opmerking:** OPOS-support garandeert niet ondersteuning voor alle apparaten die OPOS-stuurprogramma's hebben. Microsoft Dynamics 365 for Operations - Retail moet eerst ondersteuning voor dat apparaattype of klasse via OPOS. Bovendien serviceobjecten altijd mogelijk niet up-to-date met de meest recente versie van de CCOs. Ook moet u er rekening mee houden dat, in het algemeen de kwaliteit van serviceobjecten varieert.

### <a name="windows"></a>Windows

Ontvangstbewijzen af te drukken op het POS is geoptimaliseerd voor OPOS. OPOS vaak veel sneller dan afdrukken via Windows. Daarom is het een goed idee OPOS, vooral in retail omgevingen waar ontvangstbewijzen 40 kolommen worden afgedrukt en transactie tijden snel moet gebruiken. Voor de meeste apparaten u OPOS-besturingselementen gebruikt. Sommige OPOS-ontvangst-printers ondersteunen echter ook Windows-stuurprogramma's. Met behulp van een Windows-stuurprogramma, kunt u toegang tot de meest recente lettertypen en netwerk één printer voor meerdere kassa's. Er zijn echter te Windows-stuurprogramma's. Hier volgen enkele voorbeelden van deze nadelen:

-   Wanneer Windows-stuurprogramma's worden gebruikt, worden de afbeeldingen weergegeven waarna wordt afgedrukt. Daarom vaak afdrukken trager dan op printers die gebruikmaken van OPOS-besturingselementen.
-   Apparaten die zijn verbonden via de printer ('ringnetwerk') werkt mogelijk niet correct wanneer Windows-stuurprogramma's worden gebruikt. Bijvoorbeeld mogelijk niet de kassalade wordt geopend of de printer slip kan niet in word zoals u verwacht.
-   OPOS ondersteunt ook een uitgebreidere reeks variabelen die specifiek voor printers ontvangst detailhandel, zoals papier snijden of pakbon afdrukken zijn.

Als de OPOS-besturingselementen beschikbaar zijn voor de Windows-printer die u gebruikt, wordt de printer moet nog steeds goed werkt met Microsoft Dynamics 365 for Operations - Retail.

### <a name="universal-windows-platform"></a>Universele Windows-Platform

UWP, in het geval van de retail-randapparatuur is gerelateerd aan Windows-ondersteuning voor Plug en Play-apparaten. Wanneer u een Plug en Play-apparaat is verbonden met een versie van het Windows-besturingssysteem die ondersteuning biedt voor dat type apparaat, is er geen stuurprogramma is vereist voor het apparaat moet worden gebruikt als de bedoeling. Bijvoorbeeld: als een luidspreker Bluetooth-apparaat wordt gedetecteerd, het besturingssysteem weet dat het apparaat heeft de **luidspreker** type klasse. Daarom en dat apparaat worden behandeld als een luidspreker. Er is geen aanvullende instellingen vereist. Veel USB-apparaten kunnen worden aangesloten geval van POS-apparaten en Windows u herkent als HID-apparaten (HIDs). Echter, het niet mogelijk om te bepalen van de mogelijkheden die het apparaat geeft, omdat het apparaat niet voor de klasse of het type apparaat opgeven. In Windows 10 zijn apparaatklassen voor streepjescodescanners en MSRs toegevoegd. Dus als een apparaat zelf als een apparaat van een van deze klassen tot en met 10 voor Windows verklaart, luistert Windows naar gebeurtenissen van het apparaat op de gewenste tijd. Moderne POS ondersteunt UWP MSRs en scanners. Wanneer deze gereed voor de invoer van een van deze apparaten is en een apparaat dat bij een van deze klassen hoort is verbonden, kunnen het apparaat dus kan worden gebruikt. Bijvoorbeeld: als een UWP streepjescodescanner is aangesloten op een computer met Windows 10 en -teken in de streepjescode voor moderne POS is geconfigureerd, de streepjescodescanner wordt actief op het scherm aanmelden. Er is geen aanvullende instellingen vereist. Aanvullende klassen van punt van de service UWP apparaten worden toegevoegd aan Windows. Deze klassen bevatten klassen voor kassalades en printers voor ontvangstbewijzen. Ondersteuning voor deze nieuwe apparaatklassen in moderne POS is in behandeling.

### <a name="keyboard-wedge"></a>Toetsenbord wig

Toetsenbord wig apparaten verzenden gegevens naar de computer alsof deze gegevens zijn ingevoerd op een toetsenbord. Standaard krijgen het veld dat actief is op het POS dus de gegevens die worden gescand of gehaald. In sommige gevallen kan dit gedrag kan leiden tot het verkeerde type gegevens moet worden gezocht naar het verkeerde veld. Een streepjescode kan bijvoorbeeld naar een veld dat is bedoeld voor het vastleggen van creditcard-gegevens worden gescand. In veel gevallen is logica op het POS waarmee wordt bepaald of de gegevens die worden gescand of kaart een streepjescode of -kaart. De gegevens worden daarom correct verwerkt. Wanneer apparaten zijn ingesteld als OPOS in plaats van toetsenbord wig apparaten, is er echter meer controle over hoe de gegevens van deze apparaten kunnen worden verbruikt, omdat meer 'bekend' over het apparaat dat de gegevens zijn afkomstig uit. Bijvoorbeeld gegevens uit een streepjescodescanner wordt automatisch herkend als een streepjescode en de bijbehorende record in de database gemakkelijker en sneller dan als een algemene tekenreeks zoeken hebt geaccepteerd,.Net als bij toetsenbord wig apparaten wordt gevonden.

### <a name="native-printer"></a>Eigen printer

Native (of 'Apparaat' als het type met de naam in het hardwareprofiel) printers kunnen worden geconfigureerd voor de gebruiker gevraagd om een printer die is geconfigureerd voor de computer selecteren. Wanneer een printer van de **apparaat** type is geconfigureerd, als moderne POS een opdracht print detecteert, de gebruiker wordt gevraagd een printer in een lijst selecteren. Dit gedrag verschilt van het gedrag van Windows-stuurprogramma's, omdat de **Windows** printertype het hardwareprofiel, een lijst met printers wordt niet weergegeven. In plaats daarvan deze moet u een benoemde printers de **apparaatnaam** veld.

### <a name="windows"></a>Windows

De **Windows** apparaattype wordt gebruikt voor alleen printers. Wanneer een Windows-printer in het hardwareprofiel is geconfigureerd, kan de naam van de specifieke printer moet worden opgegeven. Wanneer moderne POS afdrukken gebeurtenissen tegenkomt als een Windows-printer is geconfigureerd, wordt de gebeurtenis wordt doorgegeven aan de opgegeven Windows-printer. De gebruiker niet gevraagd om een printer te selecteren.

### <a name="network"></a>Netwerk

Netwerk adresseerbare kassalades printers voor ontvangstbewijzen en terminals betaling kunnen worden gebruikt via een netwerk, rechtstreeks via de hardware-station van Interprocess communicatie (Ipc) die van de moderne POS voor Windows-toepassing uitmaakt deel of via de IIS-hardware-station voor andere clients moderne POS.

## <a name="hardware-station-deployment-options"></a>Opties voor distributie van hardware-station
### <a name="ipc-built-in"></a>Indirecte productiekosten (ingebouwd)

Het station van de hardware Interprocess communicatie (Ipc) deel uitmaakt van de moderne POS voor Windows-toepassing. Als u wilt gebruiken in het station Ipc-hardware, moet u een hardwareprofiel toewijzen aan een kassa met de moderne POS voor Windows-toepassing. Maak vervolgens een hardware-station van de **speciaal** type voor de winkel waar de kassa wordt gebruikt. Wanneer u een moderne POS start, het station van de hardware Ipc actief zal zijn en de POS-randapparatuur die zijn geconfigureerd zijn klaar voor gebruik. Als u niet de lokale hardware tijdelijk voor een of andere reden vereist, gebruikt de **hardware stations beheren** bewerking de hardwaremogelijkheden station uitschakelen. Moderne POS kunt ook het station van de hardware Ipc directe communicatie met randapparatuur netwerk gebruiken.

### <a name="iis"></a>IIS

U kunt de IIS- of zelfstandige versie van het station hardware op twee manieren gebruiken. De beschrijving 'IIS' betekent dat de POS-toepassing maakt verbinding met het station hardware via Microsoft Internet Information Services. De POS-toepassing maakt verbinding met het IIS hardware station via webservices die worden uitgevoerd op een computer waarop de apparaten zijn aangesloten. Wanneer IIS wordt gebruikt, de retail-randapparatuur die zijn verbonden met een hardware-station kunnen worden gebruikt door een POS-kassa die zich op hetzelfde netwerk als de IIS-hardware-station. Omdat alleen moderne POS voor Windows ingebouwde ondersteuning voor randapparatuur van de detailhandel, moeten alle andere toepassingen van moderne POS de hardware-station van IIS gebruiken om te communiceren met POS-randapparatuur die zijn geconfigureerd in het hardwareprofiel. Daarom vereist elke instantie van de IIS-hardware-station een computer waarop de webservice wordt uitgevoerd en de toepassing die met de apparaten communiceert. Het station van de hardware IIS is vereist voor alle niet - Windows moderne POS-toepassingen.

#### <a name="dedicated"></a>Specifiek

Moderne POS werkt met hardware-stations van de **speciaal** type om te detecteren dat randapparatuur rechtstreeks verbonden zijn met de computer waarop de toepassing wordt gebruikt. Echter, de **speciaal** type kan ook worden gebruikt voor IIS hardware stations. In een traditioneel, vaste POS-scenario dat Cloud-POS als de POS-toepassing gebruikt, de **speciaal** hardwaretype-station wordt gebruikt voor IIS hardware stations die zijn geïmplementeerd op dezelfde computer waarop de Cloud-POS. Het toegewezen station van de IIS-hardware is vanuit het oogpunt van een randapparatuur retail beter detailhandel ondersteuning voor randapparatuur voor traditionele, vaste POS-scenario's. Specifieke hardware-stations ondersteunen alle randapparatuur die worden ondersteund in het hardwareprofiel.

#### <a name="shared"></a>Gedeeld

Gedeelde stations zijn bedoeld voor gebruik door meerdere POS-apparaten in de loop van de dag hardware. Gedeelde stations zijn geoptimaliseerd ondersteuning alleen kassalades printers voor ontvangstbewijzen en betaling terminals hardware. U kunt geen zelfstandige streepjescodescanners, MSRs, weergegeven, schalen of andere apparaten rechtstreeks verbinding maken. Anders wordt conflicten optreden wanneer meerdere POS-apparaten die randapparatuur aanspraak op hetzelfde moment. Hier ziet u hoe conflicten voor ondersteunde apparaten worden beheerd:

-   **Kassalade** : de kassalade wordt geopend via een gebeurtenis die wordt verzonden naar het apparaat. Het enige probleem dat optreden kan wanneer een kassalade heet treedt op als de kassalade nog is geopend. In het geval van gedeelde hardware stations, de kassalade moet worden ingesteld op **gedeeld** in het hardwareprofiel. Deze instelling voorkomt dat het POS controleren of de kassalade al geopend is bij het verzenden van opdrachten openen.
-   **Kassabonprinter** : als twee ontvangstbewijs afdrukken tegelijkertijd, een van de opdrachten worden verzonden naar het station hardware verloren gaan, afhankelijk van het apparaat worden kan. Sommige apparaten hebben interne geheugen of groeperen die dit probleem kunt voorkomen. Als een opdracht print niet lukt, wordt de kassamedewerker ontvangt een foutbericht weergegeven en opnieuw de opdracht print op het POS.
-   **Betaling terminal** : als een kassamedewerker-pogingen tot inschrijving van een transactie op een terminal betaling die al wordt gebruikt, een bericht informeert de kassamedewerker dat de terminal wordt gebruikt en vraagt de kassamedewerker later weer kunnen proberen. Meestal ziet kassiers dat een terminal al gebruikt wordt en wacht totdat de andere transactie is voltooid voordat ze inschrijving opnieuw proberen.

Validatie is gepland voor een toekomstige versie, om te detecteren of niet-ondersteunde apparaten zijn ingesteld voor een hardwareprofiel die is toegewezen aan een gedeelde hardware-station. Als u alle niet-ondersteunde apparaten worden gedetecteerd, ontvangt de gebruiker een bericht waarin wordt gemeld dat de apparaten worden niet ondersteund voor gedeelde hardware stations. In het geval van gedeelde hardware stations, de **selecteren bij aanbesteding** optie is ingesteld op **Ja** op het niveau van de kassa. De POS-gebruiker wordt vervolgens gevraagd een hardware-station selecteren wanneer een offerte wordt geselecteerd voor een transactie op het POS. Wanneer de hardware-station alleen op het moment van de inschrijving is ingeschakeld, wordt de selectie van de station hardware rechtstreeks naar de POS-werkstroom voor mobiele scenario's toegevoegd. De regel wordt weergegeven op de terminal betaling wordt niet als een extra voordeel voor gedeelde scenario's gebruikt. Als de betaling terminal wordt gebruikt als de regelweergave van een, mogelijk andere gebruikers worden geblokkeerd met behulp van deze terminal totdat de transactie is voltooid. In mobiele scenario's, kunnen de regels worden toegevoegd aan een transactie in een langere periode. Daarom de **selecteren bij aanbesteding** optie is vereist voor het apparaat voor optimale beschikbaarheid te garanderen.

### <a name="network-peripherals"></a>Netwerk-randapparatuur

De aanduiding van het netwerk voor apparaten in het hardwareprofiel kunt kassalades printers voor ontvangstbewijzen en betaling terminals zijn verbonden via een netwerkverbinding.

#### <a name="modern-pos-for-windows"></a>Moderne POS voor Windows

IP-adressen voor randapparatuur met een netwerk kunt u opgeven op twee plaatsen. Als de moderne POS-Windows-client één set randapparatuur netwerk gebruikt, moet u de IP-adressen voor die apparaten instellen met behulp van de **IP-configuratie** optie in het actievenster voor het journaal zelf. In het geval van apparaten die worden gedeeld tussen de POS-kassa's, een hardwareprofiel dat toegewezen aan deze apparaten is rechtstreeks naar een gedeelde hardware-station kan worden toegewezen. IP-adressen toewijzen, selecteert u dat station hardware op de **detailhandel** pagina en gebruik vervolgens de **IP-configuratie** optie de **Hardware stations** sectie om op te geven van de apparaten die zijn toegewezen aan dit station hardware. Voor hardware-werkstations waarop alleen netwerkapparaten hebt, hebt u geen implementatie van de hardware-station zelf. In dit geval wordt is de hardware-station vereist alleen conceptueel netwerk adresseerbare apparaten volgens hun locatie in de winkel te groeperen.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Cloud POS, moderne POS voor iOS en moderne POS voor Android

De logica die fysiek verbonden en netwerk adresseerbare randapparatuur schijven bevindt zich in de hardware-station. Daarom voor alle POS-clients met uitzondering van moderne POS voor Windows moet een IIS-hardware-station zijn geïmplementeerd en actieve opdat het POS om te communiceren met randapparatuur, ongeacht of deze randapparatuur fysiek zijn verbonden met een hardware-station of beantwoord via het netwerk.

## <a name="setup-and-configuration"></a>Instellingen en configuratie
### <a name="hardware-station-installation"></a>Installatie van de hardware-station

Zie voor meer informatie, [detailhandel station hardwareconfiguratie en de installatie](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Moderne POS voor Windows-installatie en configuratie

Zie voor meer informatie, [Retail POS op moderne configuratie en installatie](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS-apparaat instellen en configureren

Zie de sectie 'Ondersteunde interfaces' van dit document voor meer informatie over OPOS-onderdelen. OPOS-stuurprogramma's worden gewoonlijk geleverd door de fabrikant van het apparaat. Wanneer een OPOS-stuurprogramma is geïnstalleerd, wordt een sleutel toegevoegd aan het Windows-register op een van de volgende locaties:

-   **32-bits systeem:** HKEY\_lokale\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bits systeem:** HKEY\_lokale\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Binnen de locatie van het register ServiceOPOS worden volgens de OPOS-apparaatklasse geconfigureerde apparaten ingedeeld. Meerdere stuurprogramma's worden opgeslagen.

## <a name="supported-scenarios-by-hardware-station-type"></a>Ondersteunde scenario's op hardwaretype station
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Ondersteuning voor clients: Ipc hardware station versus IIS hardware station

De volgende tabel ziet u alle topologieën en deployment-scenario's die worden ondersteund.

| Klant      | Indirecte productiekosten hardware station | IIS hardware station |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nee                   | Ja                  |
| Android     | Nee                   | Ja                  |
| iOS         | Nee                   | Ja                  |

### <a name="network-peripherals"></a>Netwerk-randapparatuur

Netwerk randapparatuur kunnen rechtstreeks via de hardware-station dat van de moderne POS voor Windows-toepassing uitmaakt deel worden ondersteund. U moet een station van de hardware IIS implementeren voor alle andere clients.

| Klant      | Indirecte productiekosten hardware station | IIS hardware station |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nee                   | Ja                  |
| Android     | Nee                   | Ja                  |
| iOS         | Nee                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Ondersteunde apparaattypen type hardware-station
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS voor Windows met een hardware-station van indirecte productiekosten (ingebouwd)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ondersteunde apparaatklasse</th>
<th>Ondersteunde interface</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows-stuurprogramma</li>
<li>Apparaat</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-stuurprogramma</li>
<li>Apparaat</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Regelweergave</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Twee schermen</td>
<td>Windows-stuurprogramma</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Er is geen instelling is vereist.)</li>
<li>Toetsenbord wig (Er is geen instelling is vereist.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Wisseluitschrijver</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk <strong>opmerking:</strong> slechts één lade kunt instellen als <strong>gebruik shift gedeelde</strong> is geconfigureerd op de lade.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk <strong>opmerking:</strong> slechts één lade kunt instellen als <strong>gebruik shift gedeelde</strong> is geconfigureerd op de lade.</li>
</ul></td>
</tr>
<tr class="even">
<td>Scanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Er is geen instelling is vereist.)</li>
<li>Toetsenbord wig (Er is geen instelling is vereist.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Er is geen instelling is vereist.)</li>
<li>Toetsenbord wig (Er is geen instelling is vereist.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Schaal</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Pinapparaat</td>
<td>OPOS (ondersteuning is beschikbaar via de aanpassing van de betalingsconnector.)</td>
</tr>
<tr class="even">
<td>Handtekeningregistratie</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Ondersteuning voor aangepaste apparaten</li>
<li>Netwerk (Zie de documentatie van de betaling connector voor meer informatie.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle moderne POS-clients met een toegewezen station van de IIS-hardware

**opmerking:** wanneer de IIS-hardware-station 'gereserveerd' is, is een een-relatie tussen de POS-client en de hardware-station.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ondersteunde apparaatklasse</th>
<th>Ondersteunde interface</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows-stuurprogramma <strong>opmerking:</strong> voor Windows-printers in een netwerk, de gebruiker van het station hardware moet gemachtigd zijn toegang tot de printer.</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-stuurprogramma</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Regelweergave</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Wisseluitschrijver</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk <strong>opmerking:</strong> slechts één lade per hardwareprofiel kunt instellen als <strong>gebruik shift gedeelde</strong> is geconfigureerd op de lade.</li>
</ul></td>
</tr>
<tr class="even">
<td>Lade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Scanner 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Schaal</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Pinapparaat</td>
<td>OPOS (ondersteuning is beschikbaar via de aanpassing van de betalingsconnector.)</td>
</tr>
<tr class="odd">
<td>SIG. registreren</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Betalingsterminal </td>
<td><ul>
<li>Ondersteuning voor aangepaste apparaten</li>
<li>Netwerk (Zie de documentatie van de betaling connector voor meer informatie.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle moderne POS-clients met een gedeelde station van de IIS-hardware

**opmerking:** wanneer het station IIS hardware 'gedeeld' is, meerdere apparaten het hardware-station tegelijk kunnen gebruiken. In dit scenario moet u alleen de apparaten die worden vermeld in de volgende tabel. Als u probeert te delen apparaten die niet worden hier vermeld, zoals streepjescodescanners en MSRs, zich fouten voordoen wanneer meerdere apparaten wilt aanspraak maken op de dezelfde randapparatuur. In de toekomst een dergelijke configuratie expliciet geen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ondersteunde apparaatklasse</th>
<th>Ondersteunde interface</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows-stuurprogramma <strong>opmerking:</strong> voor Windows-printers in een netwerk, de gebruiker van het station hardware moet gemachtigd zijn toegang tot de printer.</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-stuurprogramma</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Wisseluitschrijver</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk <strong>opmerking:</strong> slechts één lade per hardwareprofiel kunt instellen als <strong>gebruik shift gedeelde</strong> is geconfigureerd op de lade.</li>
</ul></td>
</tr>
<tr class="even">
<td>Lade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Ondersteuning voor aangepaste apparaten</li>
<li>Netwerk (Zie de documentatie van de betaling connector voor meer informatie.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>De configuratie van ondersteunde scenario 's
Zie voor meer informatie over het maken van hardwareprofielen [definiëren en onderhouden van kanaal-clients, waaronder kassa's en hardware stations](define-maintain-channel-clients-registers-hw-stations.md). **opmerking:** voor Microsoft Dynamics 365 voor bewerkingen versie 1611, wordt het hardwareprofiel station niet meer gebruikt. Kenmerken die u hebt ingesteld in het station hardwareprofiel maken nu deel uit van het station hardware zelf.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS voor Windows met een hardware-station van indirecte productiekosten (ingebouwd)

Deze configuratie is de meestgebruikte configuratie voor traditionele, vaste POS-kassa's. In dit scenario wordt de informatie over hardware-profiel toegewezen rechtstreeks naar het journaal zelf. Het EFT-terminalnummer moet ook worden ingesteld op het journaal zelf. U kunt deze configuratie instellen door de volgende stappen uit.

1.  Maak een hardwareprofiel waarin de vereiste randapparatuur zijn geconfigureerd.
2.  Het hardwareprofiel toewijzen aan de POS-kassa.
3.  Maken van een hardware-station van de **speciaal** type voor de winkel waar de POS-kassa wordt gebruikt. Een omschrijving is optioneel. **opmerking:** u hebt geen tot andere eigenschappen instellen voor de hardware-station. Alle andere vereiste informatie, zoals het hardwareprofiel worden afkomstig uit het journaal zelf.
4.  Klik op **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributieplanning**.
5.  Selecteer de **1090** distributieplanning te synchroniseren van het nieuwe hardwareprofiel aan de winkel. Klik op **nu uitvoeren** voor synchronisatie van wijzigingen aan het POS.
6.  Selecteer de **1040** distributieplanning te synchroniseren van de nieuwe hardware-station naar de winkel. Klik op **nu uitvoeren** voor synchronisatie van wijzigingen aan het POS.
7.  Installeren en activeren van moderne POS voor Windows.
8.  Moderne POS voor Windows start en begint te gebruiken van de aangesloten randapparatuur.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle moderne POS-clients met een toegewezen station van de IIS-hardware

Deze configuratie kan worden gebruikt voor alle moderne POS-clients met een hardware-station dat wordt gebruikt uitsluitend door één POS registreren. U kunt deze configuratie instellen door de volgende stappen uit.

1.  Maak een hardwareprofiel waarin de vereiste randapparatuur zijn geconfigureerd.
2.  Maken van een hardware-station van de **speciaal** type voor de winkel waar de POS-kassa wordt gebruikt.
3.  Stel op het station specifieke hardware de volgende eigenschappen:
    -   **Hostnaam** : de naam van de computer waar het hardware-station wordt uitgevoerd. **opmerking:** Cloud POS kunt oplossen **localhost** om te bepalen van de lokale computer waarop de Cloud-POS wordt uitgevoerd. Het certificaat dat is vereist voor de Cloud-POS koppelen met de hardware-station moet ook wel 'Localhost' als de naam van de computer. Om problemen te voorkomen, is het raadzaam weer te geven die een exemplaar van elk station specifieke hardware voor de winkel, zoals vereist. Voor elk station hardware de hostnaam worden de specifieke computernaam gebruikt waarin de hardware-station wordt geïmplementeerd.
    -   **Poort** : de poort wilt gebruiken voor het station hardware om te communiceren met de moderne POS-client.
    -   **Hardwareprofiel** : als het hardwareprofiel niet is opgegeven op het station van de hardware zelf, het hardwareprofiel dat is toegewezen aan de kassa wordt gebruikt.
    -   **EFT POS-nummer** : de EFT-terminal-ID moet worden gebruikt bij de EFT-autorisatie worden verzonden. Deze ID wordt geleverd door de creditcardverwerker.
    -   **De pakketnaam** : het pakket hardware station moet worden gebruikt bij de hardware-station wordt geïmplementeerd.

4.  Klik op **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributieplanning**.
5.  Selecteer de **1090** distributieplanning te synchroniseren van het nieuwe hardwareprofiel aan de winkel. Klik op **nu uitvoeren** voor synchronisatie van wijzigingen aan het POS.
6.  Selecteer de **1040** distributieplanning te synchroniseren van de nieuwe hardware-station naar de winkel. Klik op **nu uitvoeren** voor synchronisatie van wijzigingen aan het POS.
7.  Installeer de hardware-station. Zie voor meer informatie over het installeren van de hardware-station, [detailhandel station hardwareconfiguratie en de installatie](retail-hardware-station-configuration-installation.md).
8.  Installeren en activeren van moderne POS. Zie voor meer informatie over het installeren van moderne POS [Retail POS op moderne configuratie en installatie](retail-modern-pos-device-activation.md).
9.  Aanmelden bij moderne POS en selecteer **niet-ladebewerkingen uitvoeren**.
10. Start de **hardware stations beheren** bewerking.
11. Klik op **beheren**.
12. Stel de optie om te schakelen op het station hardware op de pagina hardware station management.
13. Selecteer het station hardware wilt gebruiken en klik op **paar**.
14. Nadat het hardware-station is gekoppeld, klikt u op **sluit**.
15. Klik op de pagina hardware station selecteren op het laatst geselecteerde hardware-station om deze te activeren.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle moderne POS-clients met een gedeelde station van de IIS-hardware

Deze configuratie kan worden gebruikt voor alle moderne POS-clients die hardware stations met andere apparaten delen. U kunt deze configuratie instellen door de volgende stappen uit.

1.  Maak een hardwareprofiel waarin de vereiste randapparatuur zijn geconfigureerd.
2.  Maken van een hardware-station van de **gedeeld** type voor de winkel waar de POS-kassa wordt gebruikt.
3.  Stel op het station gedeelde hardware de volgende eigenschappen:
    -   **Hostnaam** : de naam van de computer waar het hardware-station wordt uitgevoerd.
    -   **Beschrijving** : tekst op die helpt het station hardware, zoals identificeren **retourneert** of **Front van winkel**.
    -   **Poort** : de poort wilt gebruiken voor het station hardware om te communiceren met de moderne POS-client.
    -   **Hardwareprofiel** : voor gedeelde hardware stations, elk hardware-station een hardwareprofiel moet hebben. Hardwareprofielen kunnen worden gedeeld tussen hardware stations, maar ze moeten worden toegewezen aan elk hardware-station. Bovendien is het raadzaam om gebruik te maken van gedeelde ploegen als meerdere apparaten maken gebruik van het station met dezelfde gedeelde hardware. Als u een gedeelde ploeg instellen, klikt u op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profielen**&gt;**hardwareprofielen**. Voor elke gedeelde hardwareprofiel, selecteer de kassalade en stel de **Shared shift lade** optie naar **Ja**.
    -   **EFT POS-nummer** : de EFT-terminal-ID moet worden gebruikt bij de EFT-autorisatie worden verzonden. Deze ID wordt geleverd door de creditcardverwerker.
    -   **De pakketnaam** : het pakket hardware station moet worden gebruikt bij de hardware-station wordt geïmplementeerd.

4.  Herhaal stap 2 en 3 voor elk station extra hardware die is vereist in de winkel.
5.  Klik op **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributieplanning**.
6.  Selecteer de **1090** distributieplanning te synchroniseren van het nieuwe hardwareprofiel aan de winkel. Klik op **nu uitvoeren** voor synchronisatie van wijzigingen aan het POS.
7.  Selecteer de **1040** distributieplanning te synchroniseren van de nieuwe hardware-station naar de winkel. Klik op **nu uitvoeren** voor synchronisatie van wijzigingen aan het POS.
8.  Installeer het station hardware op elke hostcomputer die u in stap 2 en 3. Zie voor meer informatie over het installeren van de hardware-station, [detailhandel station hardwareconfiguratie en de installatie](retail-hardware-station-configuration-installation.md).
9.  Installeren en activeren van moderne POS. Zie voor meer informatie over het installeren van moderne POS [Retail POS op moderne configuratie en installatie](retail-modern-pos-device-activation.md).
10. Aanmelden bij moderne POS en selecteer **niet-ladebewerkingen uitvoeren**.
11. Start de **hardware stations beheren** bewerking.

12. Klik op **beheren**.
13. Stel de optie om te schakelen op het station hardware op de pagina hardware station management.
14. Selecteer het station hardware wilt gebruiken en klik op **paar**.
15. Herhaal stap 14 voor elk station hardware die moderne POS wilt gebruiken.
16. Nadat alle vereiste hardware-stations zijn gekoppeld, klikt u op **sluit**.
17. Klik op de pagina hardware station selecteren op het laatst geselecteerde hardware-station om deze te activeren. **opmerking:** als apparaten vaak verschillende hardware-stations gebruiken, raden we aan dat u moderne POS kassiers een hardware-station selecteren configureert wanneer ze beginnen met de betalingsmethode wordt gevraagd. Klik op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**registreert**. Selecteert u het journaal en stel de **selecteren bij betaling** optie naar **Ja**. Gebruik de **1090** distributieplanning te synchroniseren van wijzigingen in de kanaaldatabase.

## <a name="extensibility"></a>Uitbreidbaarheid
Zie voor informatie over extensibility scenario's voor de hardware-station, [Hardware Station extensibility](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Beveiliging
Volgens de huidige normen voor beveiliging, moeten de volgende instellingen worden gebruikt in een productieomgeving: **opmerking:** het station hardware installatieprogramma wordt automatisch doorgevoerd voor deze wijzigingen in het register als onderdeel van de installatie via self-service.

-   Secure Sockets Layer (SSL) moet worden uitgeschakeld.
-   Alleen Transport Layer Security (TLS) versie 1.2 (of de huidige versie van de hoogste) worden ingeschakeld en gebruikt. **opmerking:**, SSL en alle versies van TLS behalve TLS 1.2 zijn standaard uitgeschakeld. Als u wilt bewerken of inschakelen van deze waarden, de volgende stappen uit:
    1.  Druk op de Windows-logo belangrijke + R opent een **uitgevoerd** venster.
    2.  In de **openen** veld **Regedit**, en klik vervolgens op **OK**.
    3.  Als een **beheer van gebruikersaccount** berichtvenster verschijnt, klikt u op **Ja**.
    4.  In de **Register-Editor** venster, gaat u naar **HKEY\_lokale\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. De volgende sleutels zijn automatisch ingevoerd als u wilt toestaan voor TLS 1.2 alleen:
        -   TLS-1.2Server: ingeschakeld = 1
        -   TLS-1.2Server:DisabledByDefault = 0
        -   TLS-1.2Client: ingeschakeld = 1
        -   TLS-1.2Client:DisabledByDefault = 0
        -   TLS-1.1Server: ingeschakeld = 0
        -   TLS-1.1Client: ingeschakeld = 0
        -   TLS-1.0Server: ingeschakeld = 0
        -   TLS-1.0Client: ingeschakeld = 0
        -   SSL-3.0Server: ingeschakeld = 0
        -   SSL-3.0Client: ingeschakeld = 0
        -   SSL-2.0Server: ingeschakeld = 0
        -   SSL-2.0Client: ingeschakeld = 0
-   Er wordt geen extra netwerkpoorten is geopend, tenzij ze nodig om bekende, opgegeven zijn.
-   Cross-oorsprong resources delen moet worden uitgeschakeld en de toegestane oorsprongen die worden geaccepteerd moet opgeven.
-   Alleen vertrouwde certificate authorities moeten worden gebruikt om certificaten die worden gebruikt op computers met de hardware-station te verkrijgen.

**opmerking:** is zeer belangrijk dat u richtlijnen voor beveiliging voor IIS en de betaling kaart bedrijfstak (PCI)-vereisten.

## <a name="peripheral-simulator"></a>Randapparatuursimulator
Zie voor meer informatie, [detailhandel randapparatuur simulator](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested-randapparatuur
### <a name="ipc-built-in-hardware-station"></a>Indirecte productiekosten (ingebouwd) hardware-station

De volgende randapparatuur zijn getest met behulp van het station van indirecte productiekosten hardware die is ingebouwd in moderne POS voor Windows.

#### <a name="printer"></a>Printer

| Fabrikant | Model    | Interface | Opmerkingen                |
|--------------|----------|-----------|-------------------------|
| Epson        | TM T88IV | OPOS      |                         |
| Epson        | TM T88V  | OPOS      |                         |
| Ster         | TSP650II | OPOS      |                         |
| Ster         | TSP650II | Aangepast    | Verbonden via een netwerk   |
| Ster         | mPOP     | OPOS      | Verbonden via Bluetooth |
| HP           | F7M67AA  | OPOS      | Geactiveerde USB             |

#### <a name="bar-code-scanner"></a>Scanner voor streepjescodes

| Fabrikant  | Model         | Interface | Opmerkingen |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Symbool        | LS2208        | OPOS      |          |
| HP geïntegreerd | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>Pinapparaat

| Fabrikant | Model  | Interface | Opmerkingen                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Aanpassing van de betalingsconnector vereist |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Fabrikant | Model | Interface | Opmerkingen                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Aangepast    | Aanpassing van de betalingsconnector vereist                                |
| VeriFone     | MX925 | Aangepast    | Vereist aanpassing van de betalingsconnector; verbonden via een netwerk- en USB |
| VeriFone     | MX915 | Aangepast    | Vereist aanpassing van de betalingsconnector; verbonden via een netwerk- en USB |

#### <a name="cash-drawer"></a>Kassalade

| Fabrikant | Model     | Interface | Opmerkingen                |
|--------------|-----------|-----------|-------------------------|
| Ster         | mPOP      | OPOS      | Verbonden via Bluetooth |
| APG          | Atwood    | Aangepast    | Verbonden via een netwerk   |
| Ster         | SMD2 1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Regelweergave

| Fabrikant  | Model   | Interface | Opmerkingen |
|---------------|---------|-----------|----------|
| HP geïntegreerd | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Handtekeningregistratie

| Fabrikant | Model  | Interface | Opmerkingen |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Schaal

| Fabrikant | Model         | Interface | Opmerkingen |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Fabrikant | Model       | Interface | Opmerkingen |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Specifieke IIS hardware station

De volgende randapparatuur zijn getest met behulp van met een speciaal (niet gedeeld) IIS hardware gebruikt samen met moderne POS voor Windows en Cloud-POS.

#### <a name="printer"></a>Printer

| Fabrikant | Model    | Interface | Opmerkingen                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM T88IV | OPOS      |                           |
| Epson        | TM T88V  | OPOS      |                           |
| Ster         | TSP650II | OPOS      |                           |
| Ster         | TSP650II | Aangepast    | Verbonden via een netwerk     |
| Ster         | TSP100   | OPOS      | TSP650II-stuurprogramma's zijn vereist |
| HP           | F7M67AA  | OPOS      | Geactiveerde USB               |

#### <a name="bar-code-scanner"></a>Scanner voor streepjescodes

| Fabrikant  | Model   | Interface | Opmerkingen |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Symbool        | LS2208  | OPOS      |          |
| HP geïntegreerd | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>Pinapparaat

| Fabrikant | Model  | Interface | Opmerkingen                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Aanpassing van de betalingsconnector vereist |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Fabrikant | Model | Interface | Opmerkingen                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Aangepast    | Aanpassing van de betalingsconnector vereist                                |
| VeriFone     | MX925 | Aangepast    | Vereist aanpassing van de betalingsconnector; verbonden via een netwerk- en USB |
| VeriFone     | MX915 | Aangepast    | Vereist aanpassing van de betalingsconnector; verbonden via een netwerk- en USB |

#### <a name="cash-drawer"></a>Kassalade

| Fabrikant | Model     | Interface | Opmerkingen              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Aangepast    | Verbonden via een netwerk |
| Ster         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Regelweergave

| Fabrikant  | Model   | Interface | Opmerkingen |
|---------------|---------|-----------|----------|
| HP geïntegreerd | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Handtekeningregistratie

| Fabrikant | Model  | Interface | Opmerkingen |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Schaal

| Fabrikant | Model         | Interface | Opmerkingen |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Fabrikant | Model       | Interface | Opmerkingen |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Gedeelde IIS hardware station

De volgende randapparatuur zijn getest met behulp van een gedeelde IIS hardware gebruikt samen met moderne POS voor Windows en Cloud-POS. **opmerking:** alleen een printer, de betaling terminal en de kassalade worden ondersteund.

#### <a name="printer"></a>Printer

| Fabrikant | Model    | Interface | Opmerkingen                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM T88IV | OPOS      |                           |
| Epson        | TM T88V  | OPOS      |                           |
| Ster         | TSP650II | OPOS      |                           |
| Ster         | TSP650II | Aangepast    | Verbonden via een netwerk     |
| Ster         | TSP100   | OPOS      | TSP650II-stuurprogramma's zijn vereist |
| HP           | F7M67AA  | OPOS      | Geactiveerde USB               |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Fabrikant | Model | Interface | Opmerkingen                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Aangepast    | Vereist aanpassing van de betalingsconnector; verbonden via een netwerk- en USB |
| VeriFone     | MX915 | Aangepast    | Vereist aanpassing van de betalingsconnector; verbonden via een netwerk- en USB |

#### <a name="cash-drawer"></a>Kassalade

| Fabrikant | Model     | Interface | Opmerkingen              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Aangepast    | Verbonden via een netwerk |
| Ster         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Problemen oplossen
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderne POS kan het station hardware detecteren in de lijst voor selectie, maar kan niet worden voltooid de koppeling

**Oplossing:** te controleren of de volgende lijst met mogelijke fout punten:

-   De computer waarop de moderne POS vertrouwt het certificaat dat wordt gebruikt op de computer waarop de hardware-station wordt uitgevoerd.
    -   Om te controleren of deze instellingen in een webbrowser, gaat u naar de volgende URL: https://&lt;computernaam&gt;:&lt;poortnummer&gt;/HardwareStation/ping.
    -   Deze URL wordt een ping gebruikt om te verifiëren dat de computer kan worden geopend en de browser geeft aan of het certificaat vertrouwd wordt. (bijvoorbeeld in Internet Explorer, een pictogram van een hangslot wordt weergegeven in de adresbalk. Wanneer u op dit pictogram klikt, controleert Internet Explorer of het certificaat momenteel vertrouwd wordt. U kunt het certificaat installeren op de lokale computer aan de hand van de details van het certificaat dat wordt weergegeven.)
-   Op de computer waarop de hardware-station wordt uitgevoerd, wordt de poort die wordt gebruikt door de hardware-station in de firewall geopend.
-   De hardware-station is de zakelijke rekeninggegevens in het hulpprogramma installeren door zakelijke informatie die wordt uitgevoerd aan het einde van het installatieprogramma hardware station goed geïnstalleerd.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderne POS kan het hardware-station niet vinden in de lijst voor selectie

**Oplossing:** een van de volgende factoren kunnen dit probleem veroorzaken:

-   Het station hardware is niet correct ingesteld in het hoofdkantoor. Gebruik de stappen eerder in dit onderwerp om te controleren of het hardwareprofiel station en de hardware-station correct zijn ingevuld.
-   De taken nog niet is uitgevoerd om de kanaalconfiguratie bijwerken. In dit geval wordt de taak 1070 voor kanaalconfiguratie uitvoeren.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Nieuwe contant lade-instellingen niet worden opgenomen in moderne POS

**Oplossing:** de huidige batch sluiten. Wijzigingen in de kassalade niet worden gewijzigd in moderne POS totdat de huidige batch wordt gesloten.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Moderne POS rapport is een probleem is met een randapparatuur detailhandel

**Oplossing:** Hier volgen enkele veelvoorkomende oorzaken van dit probleem:

-   Zorg ervoor dat andere apparaat stuurprogramma configuratieprogramma's worden gesloten. Als deze hulpprogramma's geopend zijn, kunnen ze niet moderne POS of het station hardware beroep op het apparaat.
-   Als de retail-randapparatuur wordt gedeeld met verschillende POS-apparaten, schakelt u dat deze deel uitmaakt van een van de volgende categorieën:
    -   Kassalade
    -   Printer voor ontvangstbewijzen
    -   Betalingsterminal 

    Als de randapparatuur niet tot een van deze categorieën behoren, worden de hardware-station is niet ontworpen om de randapparatuur die worden gedeeld met verschillende POS-apparaten.
-   Soms stuurprogramma kunnen leiden tot de gebruikte control-objecten (CCOs) niet langer goed werkt. Als een apparaat is onlangs geïnstalleerd, maar niet goed werkt of er andere problemen, kunt u het probleem vaak oplossen door de CCOs opnieuw te installeren. U kunt downloaden van de CCOs <http://monroecs.com/oposccos_current.htm>.
-   Als u regelmatig randapparatuur wijzigt tijdens het testen van of oplossen, moet u wellicht opnieuw instellen van IIS in plaats van de cache vernieuwd wachten. Als u wilt IIS opnieuw instelt, de volgende stappen uit:
    1.  Uit de **starten** menu, het type **CMD**.
    2.  In de lijst met zoekresultaten met de rechtermuisknop op **MS-DOS-prompt**, en klik vervolgens op **als administrator uitvoeren**.
    3.  In de **MS-DOS-prompt** venster, type **iisreset/restart** en druk op Enter.
    4.  Nadat IIS opnieuw is opgestart, start u moderne POS.
-   Terwijl u wijzigingen moet frequente randapparatuur, aanbrengen vaak ook nog te starten en de POS-client afsluit, kan het proces dllhost van een eerdere POS-sessie de huidige sessie kan storen. In dit geval kan een apparaat niet worden gebruikt totdat u de dynamic link library (DLL) host die wordt beheerd door de vorige sessie sluiten. U sluit de DLL-host door de volgende stappen uit:
    1.  Uit de **starten** menu, het type **taakbeheer**.
    2.  Klik in de lijst met zoekresultaten op **taakbeheer**.
    3.  Klik in taakbeheer op de **Details** en klik op de kolomkop met de naam **naam** in de tabel alfabetisch sorteren op naam.
    4.  Blader omlaag tot u dllhost.exe vinden.
    5.  Selecteer elke host DLL-bestand en klik vervolgens op **taak beëindigen**.
    6.  Nadat de DLL-hosts zijn afgesloten, start u moderne POS.


<a name="see-also"></a>Zie ook
--------

[Randapparatuur simulator detailhandel](retail-peripheral-simulator.md)


