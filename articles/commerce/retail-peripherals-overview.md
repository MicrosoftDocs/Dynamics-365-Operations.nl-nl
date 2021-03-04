---
title: Randapparaten
description: In dit onderwerp worden de concepten beschreven die verband houden met Commerce-randapparaten.
author: rubencdelgado
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dd2ce6b223c99d890691d5fdb9f93a5ceaf33a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411497"
---
# <a name="peripherals"></a>Randapparaten

[!include[banner](includes/banner.md)]

In dit onderwerp worden de concepten beschreven die verband houden met randapparaten in winkels. Hierin worden de verschillende manieren beschreven waarop randapparaten kunnen worden aangesloten op het POS en de onderdelen die de verbinding met het POS afhandelen.

## <a name="concepts"></a>Concepten

### <a name="pos-registers"></a>POS-kassa's

Navigatie: klik op **Retail en Commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **Kassa's**. De POS-kassa is een entiteit waarmee de kenmerken worden gedefinieerd van een specifiek exemplaar van het POS. Deze kenmerken omvatten het hardwareprofiel of de instellingen voor randapparaten die worden gebruikt bij de kassa, de winkel waaraan de kassa is toegewezen en de visuele ervaring voor de gebruiker die zich bij die kassa aanmeldt.

### <a name="devices"></a>Apparaten

Navigatie: klik op **Retail en Commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **Apparaten**. Een apparaat is een entiteit die een fysiek exemplaar vertegenwoordigt van een apparaat dat is toegewezen aan een POS-kassa. Bij het maken van een apparaat, wordt het toegewezen aan een POS-kassa. De apparaatentiteit houdt informatie bij over wanneer een POS-kassa wordt geactiveerd, het type client dat wordt gebruikt en het toepassingspakket dat is geïmplementeerd op een specifiek apparaat. 

Apparaten kunnen worden toegewezen aan de volgende toepassingstypen: Retail Modern POS, Detailhandelcloud-POS, Retail Modern POS - Windows Phone, Retail Modern POS - Android en Retail Modern POS - iOS.

### <a name="modern-pos"></a>Moderne POS

Modern POS is het POS-programma voor Microsoft Windows. Het kan worden geïmplementeerd op de besturingssystemen Windows 10.

### <a name="cloud-pos"></a>Cloud-POS

Cloud POS is een versie van het programma Modern POS, die kan worden geopend in een webbrowser.

### <a name="modern-pos-for-ios"></a>Modern POS voor iOS

Modern POS voor iOS is een iOS-versie van het Modern POS-programma dat kan worden geïmplementeerd op iOS-apparaten.

### <a name="modern-pos-for-android"></a>Modern POS voor Android

Modern POS voor Android is een Android-versie van het Modern POS-programma die kan worden geïmplementeerd op Android-apparaten.

### <a name="pos-peripherals"></a>POS-randapparaten

POS-randapparaten zijn apparaten die expliciet worden ondersteund voor POS-functies. Deze randapparaten worden meestal onderverdeeld in specifieke klassen. Zie de sectie 'Apparaatklassen' van dit onderwerp voor meer informatie over deze klassen.

### <a name="hardware-station"></a>Hardware Station

Navigatie: klik op **Detailhandel en commerce** &gt; **Kanalen** &gt; **Winkels** &gt; **Alle winkels**. Selecteer een winkel en klik vervolgens op het sneltabblad **Hardwarestations**. De instelling **Hardwarestation** is een instelling op afzetkanaalniveau, die wordt gebruikt voor het definiëren van situaties waarin de logica voor randapparaten wordt geïmplementeerd. Deze instelling op het afzetkanaalniveau wordt gebruikt om de kenmerken van het hardwarestation te bepalen. Hiermee wordt ook een overzicht gemaakt van hardwarestations, die beschikbaar zijn voor een Modern POS-exemplaar in een bepaalde winkel. Het hardwarestation is ingebouwd in de Modern POS-programma's voor Windows en Android. Het hardwarestation kan ook onafhankelijk worden geïmplementeerd als een zelfstandig Microsoft Internet Information Services-programma (IIS). In dit geval vindt toegang plaats via een netwerk.

### <a name="hardware-profile"></a>Hardwareprofiel

Navigatie: Klik op **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**. Het hardwareprofiel is een lijst apparaten die zijn geconfigureerd voor een POS-kassa of een hardwarestation. Het hardwareprofielen kan rechtstreeks aan de POS-kassa of een hardwarestation worden toegewezen.

## <a name="devices-classes"></a>Apparaatklassen
POS-randapparaten worden meestal onderverdeeld in klassen. In deze sectie worden een overzicht gegeven (samen met een beschrijving) van de apparaten die Modern POS ondersteunt.

### <a name="printer"></a>Printer

Printers omvatten traditionele POS-kassabonprinters en full-page printers. Printers worden ondersteund via interfaces voor Object Linking and Embedding for Retail POS (OPOS) en Microsoft Windows-stuurprogramma's. Tot twee printers kunnen tegelijkertijd worden gebruikt. Deze functionaliteit ondersteunt scenario's waarin kassabonnen voor contanttransacties van klanten worden afgedrukt op kassabonprinters, terwijl klantorders, die meer informatie bevatten, worden afgedrukt op een full-page printer. Kassabonprinters kunnen rechtstreeks op een computer zijn aangesloten via USB, aangesloten op een netwerk via Ethernet, of aangesloten via Bluetooth.

### <a name="scanner"></a>Scanner

Tot twee streepjescodescanners kunnen tegelijkertijd worden gebruikt. Deze functionaliteit ondersteunt scenario's waarin een meer mobiele scanner is vereist voor het scannen van grote of zware artikelen, terwijl een vaste geïntegreerde scanner wordt gebruikt voor de meeste artikelen van standaardformaat, om de afrekentijden te reduceren. Scanners worden ondersteund via OPOS, universeel Windows-platform (UWP) of keyboard-wedge-interfaces. Een scanner kan worden aangesloten op een computer met USB of Bluetooth.

### <a name="msr"></a>MSR

Een USB-magneetstriplezer (MSR) kunt u instellen met behulp van OPOS-stuurprogramma's. Als u een zelfstandige MSR wilt gebruiken voor betalingstransacties met elektronische betaling (EFT), moet de MSR worden beheerd door een betalingsconnector. Zelfstandige MSR's kunnen worden gebruikt voor invoer van klantloyaliteitsgegevens, aanmelden van werknemers en invoer van geschenkbongegevens, onafhankelijk van de betalingsconnector.

### <a name="cash-drawer"></a>Kassalade

Twee kassaladen worden ondersteund per hardwareprofiel. Deze functionaliteit maakt het mogelijk om twee actieve ploegen per kassa tegelijkertijd beschikbaar te hebben. Bij een gedeelde dienst of een kassalade die wordt gebruikt door meerdere mobiele POS-apparaten tegelijk, is per hardwareprofiel slechts één kassalade toegestaan. Kassaladen kunnen rechtstreeks op een computer zijn aangesloten via USB, aangesloten op een netwerk via Ethernet, of aangesloten op een kassabonprinter via een RJ12-aansluiting. In sommige gevallen kunnen kassaladen ook worden aangesloten met Bluetooth.

### <a name="line-display"></a>Regelweergave

Regelweergaven worden gebruikt om producten, transactiesaldi en andere nuttige informatie aan de klant te tonen tijdens een transactie. U kunt één regelweergave op de computer aansluiten via USB met OPOS-stuurprogramma's.

### <a name="signature-capture"></a>Handtekeningregistratie

Apparaten voor handtekeningregistratie kunnen rechtstreeks op een computer worden aangesloten via USB met OPOS-stuurprogramma's. Als registratie van de handtekening is geconfigureerd, wordt de klant gevraagd op het apparaat zijn handtekening te zetten. Nadat de handtekening is gezet, wordt deze aan de kassamedewerker getoond voor acceptatie.

### <a name="scale"></a>Weegschaal

U kunt één weegschaal op de computer aansluiten via USB met OPOS-stuurprogramma's. Als een product dat is gemarkeerd als 'gewogen' product wordt toegevoegd aan een transactie, leest het POS het gewicht van de weegschaal, wordt het product aan de transactie toegevoegd en wordt de hoeveelheid gebruikt die de weegschaal aangeeft.

### <a name="pin-pad"></a>Pinapparaat

Pinapparaten (P.I.N. = persoonlijk identificatienummer) worden ondersteund via OPOS, maar ze moeten worden beheerd via een betalingsconnector.

### <a name="secondary-display"></a>Tweede display

Wanneer een secundaire display is geconfigureerd, wordt de Windows-display nr. 2 gebruikt om algemene informatie weer te geven. De tweede display is bedoeld om uitbreidingen van ISV's (Independent Software Vendors) te ondersteunen. Dit is om dat de tweede display standaard niet configureerbaar is en slechts beperkt inhoud weergeeft.

### <a name="payment-device"></a>Betalingsapparaat

Ondersteuning voor betalingsapparaten wordt geïmplementeerd via de betalingsconnector. Betalingsapparaten kunnen een of meer van de functies uitvoeren die andere apparaatklassen bieden. Een betalingsapparaat kan bijvoorbeeld functioneren als een MSR/kaartlezer, regelweergave, apparaat voor handtekeningregistratie of pinapparaat. Ondersteuning voor betalingsapparaten wordt onafhankelijk geïmplementeerd van de ondersteuning voor zelfstandige apparaten, die wordt geleverd voor andere apparaten die in het hardwareprofiel zijn opgenomen.

## <a name="supported-interfaces"></a>Ondersteunde interfaces
### <a name="opos"></a>OPOS

Om te garanderen dat het grootste aantal apparaten kan worden gebruikt met Commerce, is de industriestandaard OLE voor POS het primaire platform voor randapparatuur dat wordt ondersteund. De OLE voor POS-norm is opgesteld door de National Retail Federation (NRF), die communicatieprotocollen voor randapparatuur opstelt die de norm in de branche zijn. OPOS is een algemeen geaccepteerde implementatie van de OLE voor POS-norm. Deze is ontwikkeld in de jaren 1990 en sinds die tijd verschillende malen geactualiseerd. OPOS biedt een apparaatstuurprogramma-architectuur die eenvoudige integratie van POS-hardware met Windows-gebaseerde POS-systemen mogelijk maakt. OPOS-besturingselementen handelen de communicatie af tussen hardware en de POS-software. Een OPOS-besturingselement bestaat uit twee onderdelen:

-   **Control object**: Het control object voor een apparaatklasse (zoals een regelweergave) biedt de interface voor het softwareprogramma. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) biedt een gestandaardiseerde reeks OPOS Control objects aan, die bekend staan als de Common Control Objects (CCO's). De CCO's worden gebruikt voor het testen van de POS-component van Commerce. Daarom helpt het testen te garanderen dat, als Commerce een apparaatklasse via OPOS ondersteunt, vele typen apparaten worden ondersteund, onder voorwaarde dat de fabrikant een serviceobject levert dat is samengesteld voor OPOS. U hoeft niet expliciet elk apparaattype te testen.
-   **Serviceobject**: Het serviceobject verzorgt de communicatie tussen het Control Object (CCO) en het apparaat. Meestal wordt voor fysieke apparaten het serviceobject geleverd door de fabrikant van het apparaat. In sommige gevallen moet u misschien het serviceobject downloaden vanaf de website van de fabrikant. Er kan bijvoorbeeld een meer recente serviceobject beschikbaar zijn. Het adres van de website van de fabrikant vindt u in de documentatie bij uw hardware.

[![Controleobject en serviceobject](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Ondersteuning voor de OPOS-implementatie van OLE voor POS helpt te garanderen dat, als de apparaatfabrikanten en POS-uitgevers de standaard correct implementeren, POS-systemen en ondersteunde apparaten kunnen samenwerken, zelfs als ze daarvoor niet samen zijn getest. 

> [!NOTE]
> OPOS-ondersteuning garandeert niet de ondersteuning voor alle apparaten met OPOS-stuurprogramma's. Commerce moet eerst ondersteuning voor dat apparaattype of klasse bieden via OPOS. Bovendien zijn serviceobjecten mogelijk niet altijd up-to-date met de meest recente versie van de CCO's. Ook moet u er rekening mee houden dat, in het algemeen, de kwaliteit van serviceobjecten kan variëren.

### <a name="windows"></a>Windows

Het afdrukken van kassabonnen op het POS is geoptimaliseerd voor OPOS. Het afdrukken werkt met OPOS vaak veel sneller dan afdrukken via Windows. Daarom is het een goed idee om OPOS te gebruiken, vooral in omgevingen waar kassabonnen met 40 kolommen worden afgedrukt en de transactietijden kort moeten zijn. Voor de meeste apparaten gebruikt u OPOS-besturingselementen. Sommige OPOS-kassabonprinters ondersteunen echter ook Windows-stuurprogramma's. Als u een Windows-stuurprogramma gebruikt, hebt u toegang tot de nieuwste lettertypen en kunt één printer via het netwerk bereikbaar maken voor meerdere kassa's. Windows-stuurprogramma's hebben echter nadelen. Dit zijn enkele van veel voorkomende nadelen:

-   Met Windows-stuurprogramma's worden afbeeldingen gerenderd vóór het afdrukken. Daarom gaat het afdrukken vaan trager dan op printers die gebruikmaken van OPOS-besturingselementen.
-   Apparaten die via de printer zijn verbonden ('daisy-chained' oftewel in serie geschakeld) werken mogelijk niet correct met Windows-stuurprogramma's. Bijvoorbeeld gaat de kassalade niet open of de bonprinter functioneert niet zoals u verwacht.
-   OPOS ondersteunt ook een uitgebreidere reeks variabelen die specifiek zijn voor kassabonprinters, zoals papiersnijden of bon afdrukken.
-   Windows-printers worden niet ondersteund via het IIS-hardwarestation. 

Als OPOS-besturingselementen beschikbaar zijn voor uw Windows-printer, functioneert de printer naar verwachting nog steeds correct met Commerce.

### <a name="universal-windows-platform"></a>Universeel Windows-platform

UWP is, voor de randapparatuur, gerelateerd aan Windows-ondersteuning voor plug en play-apparaten. Wanneer u een Plug en Play-apparaat aansluit op een Windows-versie die dat type apparaat ondersteunt, is geen stuurprogramma vereist om het apparaat te kunnen gebruiken zoals het is bedoeld. Als in Windows bijvoorbeeld een Bluetooth-luidspreker wordt gedetecteerd, is automatisch bekend dat het apparaat het klassetype **Luidspreker** heeft. Het apparaat wordt daarna dus ook behandeld als een luidspreker. Het is niet nodig om het nog verder te configureren. Voor wat betreft POS-apparaten worden veel USB-apparaten na het aansluiten herkend als als HID-apparaten (Human Interface Devices). Het kan echter zijn dat de functionaliteit van het apparaat niet kan worden bepaald, omdat het apparaat niet opgeeft van welke klasse of type het is. In Windows 10 zijn apparaatklassen voor streepjescodescanners en MSR's toegevoegd. Als een apparaat zichzelf bij Windows 10 aanmeld als een apparaat uit een van deze klassen, zal worden geluisterd naar gebeurtenissen van dat apparaat op de overeenkomende momenten. Modern POS ondersteunt UWP MSR's en scanners. Als het gereed is om invoer van een van deze apparaten te ontvangen en een apparaat uit een van deze klassen is aangesloten, kan dat apparaat worden gebruikt. Als bijvoorbeeld een UWP-streepjescodescanner is aangesloten op een computer met Windows 10 en aanmelding met streepjescode is geconfigureerd voor Modern POS, wordt de streepjescodescanner actief op het aanmeldingsscherm. Het is niet nodig om het nog verder te configureren. Aanvullende klassen van point-of-service UWP-apparaten worden toegevoegd aan Windows. Deze klassen bevatten klassen voor kassaladen en kassabonprinters. Ondersteuning voor deze nieuwe apparaatklassen in Modern POS is gepland voor de toekomst.

### <a name="keyboard-wedge"></a>Keyboard-wedge

Keyboard-wedge-apparaten verzenden gegevens naar de computer alsof deze gegevens zijn ingevoerd op een toetsenbord. Standaard krijgen dus het veld dat actief is op het POS de gegevens die worden gescand of ingelezen. In sommige gevallen kan dit gedrag kan ertoe leiden dat het verkeerde type gegevens in een veld worden gescand. Een streepjescode kan bijvoorbeeld worden gescand in een veld dat is bedoeld voor het vastleggen van creditcard-gegevens. In veel gevallen bevat het POS logica waarmee wordt bepaald of de gescande of ingelezen gegevens een streepjescode of magneetstrip op een kaart betreffen. Daarmee kunnen de gegevens dan correct worden verwerkt. Wanneer apparaten zijn ingesteld als OPOS in plaats van keyboard-wedge-apparaten, is er echter meer controle over hoe de gegevens van deze apparaten kunnen worden gebruikt, omdat meer 'bekend' is over het apparaat waarvan de gegevens afkomstig zijn. Gegevens uit een streepjescodescanner worden bijvoorbeeld automatisch herkend als een streepjescode en de bijbehorende record wordt gemakkelijker en sneller gevonden in de database, dan wanneer een algemene zoektekenreeks wordt gebruikt zoals bij keyboard-wedge-apparaten.

### <a name="native-printer"></a>Native printer

Native (ofwel 'Apparaat', zoals het type wordt aangeduid in het hardwareprofiel) printers kunnen worden geconfigureerd om de gebruiker te vragen een printer te selecteren die is geconfigureerd voor de computer. Wanneer een printer van het type **Apparaat** type is geconfigureerd, wordt de gebruiker gevraagd een printer in een lijst selecteren wanneer Modern POS een printopdracht detecteert. Dit gedrag verschilt van het gedrag van Windows-stuurprogramma's, omdat het printertype **Windows** in het hardwareprofiel geen lijst met printers toont. In plaats daarvan is hier vereist dat een benoemde printers wordt opgegeven in het veld **Apparaatnaam**.

### <a name="network"></a>Netwerk

Kassalade, kassabonprinters en betalingsterminals met een netwerkadres kunnen worden gebruikt via een netwerk, rechtstreeks via het Interprocess Communications (IPC) hardwarestation dat is geïntegreerd in de toepassing Modern POS voor Windows, of via het IIS-hardwarestation voor andere Modern POS-clients.

## <a name="hardware-station-deployment-options"></a>Implementatieopties voor het hardwarestation

### <a name="dedicated"></a>Toegewezen

Moderne POS-clients voor Windows en Android bevatten **speciale** of ingebouwde hardwarestations. Deze clients kunnen rechtstreeks met randapparatuur communiceren via bedrijfslogica die in de toepassingen is ingebouwd. De Android-toepassing ondersteunt alleen netwerkapparaten. Voor meer informatie over ondersteuning van randapparatuur voor Android gaat u naar het artikel [POS Hybrid-app instellen in Android en iOS](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp).

Als u het speciale hardwarestation wilt gebruiken, wijst u een hardwareprofiel toe aan een kassa die gebruikmaakt van de toepassingen Modern POS voor Windows of Android. Vervolgens maakt u een hardwarestation van het type **Specifiek** voor de winkel waar de kassa wordt gebruikt. Start Modern POS in de niet-lademodus en gebruik de bewerking **Hardwarestations beheren** om de mogelijkheden voor het hardwareadres in te schakelen. Het speciale hardwarestation is standaard actief. Meld u vervolgens af bij Modern POS. Als u zich opnieuw aanmeldt en een ploeg opent, kunt u gebruikmaken van de randapparatuur die in het hardwareprofiel is geconfigureerd. 

### <a name="shared"></a>Gedeeld 

Dit wordt ook wel het 'IIS'-hardwarestation genoemd. 'IIS' geeft hierbij aan dat de POS-toepassing via Microsoft Internet Information Services verbinding maakt met het hardwarestation. De POS-toepassing maakt verbinding met het IIS-hardwarestation via webservices die worden uitgevoerd op een computer waarop de apparaten zijn aangesloten. Wanneer het gedeelde hardwarestation wordt gebruikt, kunnen de randapparaten die zijn aangesloten op een hardwarestation worden gebruikt door iedere POS-kassa in hetzelfde netwerk als het IIS-hardwarestation. Omdat alleen Modern POS voor Windows en Android ingebouwde ondersteuning heeft voor randapparaten, moeten alle andere Modern POS-toepassingen voor communicatie met POS-randapparaten die zijn geconfigureerd in het hardwareprofiel, gebruik maken van het IIS-hardwarestation. Daarom vereist elk exemplaar van de IIS-hardwarestation een computer waarop de webservice wordt uitgevoerd en de toepassing die met de apparaten communiceert. 

Het gedeelde hardwarestation kan worden gebruikt om meerdere verkooppunten van verkoopclients toe te staan om randapparatuur te delen of om een vastgelegde set of randapparatuur voor een enkel verkooppunt te beheren. 

Wanneer een hardwarestation wordt gebruikt om het delen van randapparatuur tussen meerdere POS-clients te ondersteunen, mogen alleen kassaladen, kassabonprinters en betalingsterminals worden gebruikt. U kunt niet rechtstreeks andere apparaten aansluiten zoals zelfstandige streepjescodescanners, MSR's, regelweergaven, weegschalen en dergelijke. Als u dit wel doet, zullen conflicten optreden wanneer meerdere POS-apparaten die randapparatuur op hetzelfde moment proberen aan te spreken. Hier ziet u hoe conflicten voor ondersteunde apparaten worden beheerd:

-   **Kassalade:** De kassalade wordt geopend door middel van een gebeurtenis die wordt verzonden naar het apparaat. Het enige probleem dat kan optreden bij het aanroepen van een kassalade, is wanneer de kassalade al is geopend. Bij gedeelde hardwarestations moet de kassalade in het hardwareprofiel worden ingesteld op **Gedeeld**. Deze instelling voorkomt dat het POS controleert of de kassalade al geopend is bij het verzenden van opdrachten voor openen.
-   **Kassabonprinter:** Als twee opdrachten voor het afdrukken van kassabonnen tegelijk naar het hardwarestation worden verzonden, kan, afhankelijk van het apparaat, één van de opdrachten verloren gaan Sommige apparaten hebben intern geheugen of pooling waarmee dit probleem kan worden voorkomen. Als een printopdracht mislukt, ontvangt de kassamedewerker een foutbericht. Vanaf het POS kan de printopdracht opnieuw worden verzonden.
-   **Betalingsterminal:** Als een kassamedewerker een transactie wil laten betalen op een betalingsterminal die al wordt gebruikt, komt een bericht terug dat de terminal in gebruik is. De kassamedewerker wordt gevraag het later opnieuw te proberen. Meestal ziet de kassamedewerker dat een terminal in gebruik is en wacht totdat de andere transactie is voltooid voordat de transactie opnieuw wordt aangeboden.

In een toekomstige versie wordt validatie ingevoerd, om te detecteren of niet-ondersteunde apparaten zijn ingesteld voor een hardwareprofiel dat is toegewezen aan een gedeeld hardwarestation. Als een niet-ondersteund apparaat wordt gedetecteerd, krijgt de gebruiker een bericht waarin wordt gemeld dat het apparaat niet wordt ondersteund voor gedeelde hardware stations. In het geval van gedeelde hardwarestations is de optie **Selecteren bij offertes** ingesteld op **Ja** op het kassaniveau. De POS-gebruiker wordt vervolgens gevraagd een hardwarestation selecteren, wanneer op het POS een betalingsmethode wordt geselecteerd voor een transactie. Als het hardwarestation pas op het moment van het aanbieden wordt geselecteerd, wordt de selectie van het hardwarestation rechtstreeks aan de POS-werkstroom voor mobiele scenario's toegevoegd. Een extra voordeel is dat de regelweergave op de betalingsterminal niet wordt gebruikt in gedeelde scenario's. Als de betalingsterminal wordt gebruikt als de regelweergave, kunnen andere gebruikers deze terminal mogelijk niet gebruiken totdat de transactie is voltooid. In mobiele scenario's kunnen gedurende een langere periode regels worden toegevoegd aan een transactie. Daarom is de optie **Selecteren bij offertes** vereist, om te kunnen garanderen dat het apparaat maximaal beschikbaar is.

### <a name="network-peripherals"></a>Op netwerk aangesloten randapparaten

Met de aanduiding Netwerk voor apparaten in het hardwareprofiel kunnen kassaladen, kassabonprinters en betalingsterminals worden aangesloten via een netwerkverbinding.

#### <a name="modern-pos-for-windows"></a>Modern POS voor Windows

U kunt op twee plaatsen IP-adressen voor netwerkrandapparaten opgeven. Als de Modern POS-Windows-client één set netwerkrandapparaten gebruikt, moet u de IP-adressen voor die apparaten instellen via de optie **IP-configuratie** optie in het actievenster van de kassa. Bij apparaten die worden gedeeld tussen de POS-kassa's kan een hardwareprofiel, waaraan netwerkapparaten zijn toegewezen, rechtstreeks aan een gedeeld hardwarestation worden toegewezen. Om IP-adressen toe te wijzen, selecteert u dat hardwarestation op de pagina **Winkels** en gebruikt u vervolgens de optie **IP-configuratie** in de sectie **Hardwarestations** om de netwerkapparaten op te geven die aan dat hardwarestation zijn toegewezen. Voor hardwarestations die alleen netwerkapparaten hebben, hoeft u niet het hardwarestation zelf te implementeren. In dit geval is het hardwarestation alleen nodig om apparaten met netwerkadressen conceptueel te groeperen op basis van hun locatie in de winkel.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS en Modern POS voor iOS

De logica die fysiek aangesloten randapparaten en randapparaten in een netwerk aanstuurt, bevindt zich in het hardwarestation. Daarom moet voor alle POS-clients, met uitzondering van Modern POS voor Windows en Android, een IIS-hardwarestation worden geïmplementeerd en actief zijn, zodat het POS kan communiceren met randapparaten, ongeacht of deze apparaten fysiek zijn aangesloten op een hardwarestation of benaderd worden via het netwerk.

## <a name="setup-and-configuration"></a>Instellingen en configuratie
### <a name="hardware-station-installation"></a>Het hardwarestation installeren

Zie [Hardwarestation configureren en installeren](retail-hardware-station-configuration-installation.md) voor meer informatie.

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS voor Windows installeren en configureren

Zie [Modern POS (MPOS) configureren, installeren en activeren](retail-modern-pos-device-activation.md) voor meer informatie.

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Modern POS voor Android en iOS installeren en configureren

Zie [POS Hybrid-app instellen in Android en iOS](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp) voor meer informatie.

### <a name="opos-device-setup-and-configuration"></a>Een OPOS-apparaat installeren en configureren

Zie de sectie 'Ondersteunde interfaces' in dit document voor meer informatie over OPOS-onderdelen. OPOS-stuurprogramma's worden gewoonlijk geleverd door de fabrikant van het apparaat. Wanneer een OPOS-stuurprogramma is geïnstalleerd, wordt een sleutel toegevoegd aan het Windows-register op een van de volgende locaties:

-   **32-bitssysteem:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bitssysteem:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Binnen de registerlocatie ServiceOPOS worden geconfigureerde apparaten ingedeeld op basis van hun OPOS-apparaatklasse. Meerdere stuurprogramma's worden opgeslagen.

## <a name="supported-scenarios-by-hardware-station-type"></a>Ondersteunde scenario's op type hardwarestation
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Ondersteuning voor clients: IPC-hardwarestation versus IIS-hardwarestation

In de volgende tabel ziet u de ondersteunde topologieën en implementatiescenario's.

| Client      | IPC-hardwarestation | ISS-hardwarestation |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud-POS   | Nee                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nee                   | Ja                  |

### <a name="network-peripherals"></a>Op netwerk aangesloten randapparaten

Netwerkrandapparaten kunnen rechtstreeks worden ondersteund via het hardwarestation dat is geïntegreerd in de toepassingen Modern POS voor Windows en Android. Voor alle overige clients moet u een ISS-hardwarestation implementeren.

| Client      | IPC-hardwarestation | ISS-hardwarestation |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud-POS   | Nee                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nee                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Ondersteunde apparaattypen op type hardwarestation
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS voor Windows met een IPC-hardwarestation (geïntegreerd)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ondersteunde apparaatklasse</th>
<th>Ondersteunde interfaces</th>
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
<li>UWP (instellen is niet nodig)</li>
<li>Keyboard-wedge (instellen is niet nodig)</li>
</ul></td>
</tr>
<tr class="even">
<td>Wisseluitschrijver</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk </br><strong>Opmerking:</strong> u kunt slechts één lade instellen als <strong>Gebruik van gedeelde ploeg toestaan</strong> is geconfigureerd voor de lade.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk </br><strong>Opmerking:</strong> u kunt slechts één lade instellen als <strong>Gebruik van gedeelde ploeg toestaan</strong> is geconfigureerd voor de lade.</li>
</ul></td>
</tr>
<tr class="even">
<td>Scanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (instellen is niet nodig)</li>
<li>Keyboard-wedge (instellen is niet nodig)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (instellen is niet nodig)</li>
<li>Keyboard-wedge (instellen is niet nodig)</li>
</ul></td>
</tr>
<tr class="even">
<td>Schaal</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Pinapparaat</td>
<td>OPOS (ondersteuning beschikbaar via de aanpassing van de betalingsconnector)</td>
</tr>
<tr class="even">
<td>Handtekeningregistratie</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Betalingsterminal</td>
<td><ul>
<li>Aangepaste apparaatondersteuning</li>
<li>Netwerk (zie de documentatie van de betalingsconnector voor meer informatie)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-clients met een speciaal, 'gedeeld' ISS-hardwarestation

> [!NOTE]
> Als het IIS-hardwarestation 'toegezegd' is, bestaat er een één-op-één-relatie tussen de POS-client en het hardwarestation.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ondersteunde apparaatklasse</th>
<th>Ondersteunde interfaces</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
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
<li>Netwerk </br><strong>Opmerking:</strong> u kunt per hardwareprofiel slechts één lade instellen als <strong>Gebruik van gedeelde ploeg toestaan</strong> is geconfigureerd voor de lade.</li>
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
<td>OPOS (ondersteuning beschikbaar via de aanpassing van de betalingsconnector)</td>
</tr>
<tr class="odd">
<td>Handtek. registreren</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Betalingsterminal</td>
<td><ul>
<li>Aangepaste apparaatondersteuning</li>
<li>Netwerk (zie de documentatie van de betalingsconnector voor meer informatie)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-shared-an-iis-hardware-station"></a>Alle Modern POS-clients delen een ISS-hardwarestation

> [!NOTE]
> Als het IIS-hardwarestation 'gedeeld' is, kunnen meerdere apparaten tegelijk gebruikmaken van het hardwarestation. Gebruik in dit scenario alleen de apparaten die worden vermeld in de onderstaande tabel. Als u apparaten probeert te delen die hier niet worden vermeld, zoals streepjescodescanners en MSR's, treden fouten op wanneer meerdere apparaten het zelfde randapparaat willen aanspreken. In de toekomst worden dergelijke configuraties expliciet voorkomen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ondersteunde apparaatklasse</th>
<th>Ondersteunde interfaces</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Wisseluitschrijver</td>
<td><ul>
<li>OPOS</li>
<li>Netwerk </br><strong>Opmerking:</strong> u kunt per hardwareprofiel slechts één lade instellen als <strong>Gebruik van gedeelde ploeg toestaan</strong> is geconfigureerd voor de lade.</li>
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
<td>Betalingsterminal</td>
<td><ul>
<li>Aangepaste apparaatondersteuning</li>
<li>Netwerk (zie de documentatie van de betalingsconnector voor meer informatie)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Configuratie voor ondersteunde scenario's
Zie voor meer informatie over het maken van hardwareprofielen het onderwerp [Kanaalclients, waaronder kassa's en hardwarestations, definiëren en onderhouden](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS voor Windows met een IPC-hardwarestation (geïntegreerd)

Deze configuratie is de meestgebruikte configuratie voor traditionele, vaste POS-kassa's. In dit scenario wordt de informatie van het hardwareprofiel rechtstreeks toegewezen aan de kassa. Het EFT-terminalnummer moet ook worden ingesteld op de kassa. Volg deze stappen om deze configuratie in te stellen.

1.  Maak een hardwareprofiel aan waarin de vereiste randapparaten zijn geconfigureerd.
2.  Wijs het hardwareprofiel toe aan de POS-kassa.
3.  Maak een hardwarestation van het type **Specifiek** voor de winkel waar de POS-kassa wordt gebruikt. Eeen beschrijving is optioneel. 

    > [!NOTE]
    > U hoeft geen andere eigenschappen in te stellen voor het hardwarestation. Alle overige vereiste informatie, zoals het hardwareprofiel, komen uit de kassa zelf.

4.  Klik op **Detailhandel en commerce** &gt; **IT detailhandel en commerce** &gt; **Distributieplanning**.
5.  Selecteer de distributieplanning **1090** om het nieuwe hardwareprofiel naar de winkel te synchroniseren. Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.
6.  Selecteer de distributieplanning **1040** om het nieuwe hardwarestation naar de winkel te synchroniseren. Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.
7.  Modern POS voor Windows installeren en activeren
8.  Start Modern POS voor Windows en ga de aangesloten randapparaten gebruiken.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Modern POS voor Android met een IPC-hardwarestation (geïntegreerd)

**Nieuw voor 10.0.8**: Epson-netwerkprinters en kassaladen die via de DK poort op deze printers zijn aangesloten, worden nu ondersteund voor de app Modern POS voor Android. Ga naar het artikel [POS Hybrid-app instellen in Android en iOS](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp) voor meer informatie.

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-clients met een speciaal, gedeeld ISS-hardwarestation

Deze configuratie kan worden gebruikt voor alle Modern POS-clients met een hardwarestation dat uitsluitend door één POS-kassa wordt gebruikt. Volg deze stappen om deze configuratie in te stellen.

1.  Maak een hardwareprofiel aan waarin de vereiste randapparaten zijn geconfigureerd.
2.  Maak een hardwarestation van het type **Specifiek** voor de winkel waar de POS-kassa wordt gebruikt.
3.  Stel op het specifieke hardwarestation de volgende eigenschappen in:
    -   **Hostnaam:** De naam van de computer waarop het hardwarestation wordt uitgevoerd. 
    
        > [!NOTE]
        > Cloud POS kan **localhost** omzetten om de lokale computer te bepalen waarop Cloud POS wordt uitgevoerd. Het certificaat dat is vereist om Cloud POS aan het hardwarestation te koppelen, moet echter ook de computernaam 'Localhost' hebben. Om problemen te voorkomen, is het raadzaam dat u een exemplaar van elk specifiek hardwarestation voor de winkel noemt, al naar gelang wat nodig is. Voor elk hardwarestation moet de hostnaam de specifieke computernaam zijn waarin het hardwarestation wordt geïmplementeerd.
    
    -   **Poort:** De poort die u wilt gebruiken voor het hardwarestation voor communicatie met de Modern POS-client.
    -   **Hardwareprofiel:** Als het hardwareprofiel niet is opgegeven op het hardwarestation zelf, wordt het hardwareprofiel gebruikt dat is toegewezen aan de kassa.
    -   **EFT POS-nummer:** De EFT-terminal-ID die moet worden gebruikt wanneer EFT-autorisaties worden verzonden. Deze ID wordt geleverd door de creditcardverwerker.
    -   **Pakketnaam:** Het hardwarestationpakket dat moet worden gebruikt wanneer het hardwarestation wordt geïmplementeerd.

4.  Klik op **Detailhandel en commerce** &gt; **IT detailhandel en commerce** &gt; **Distributieplanning**.
5.  Selecteer de distributieplanning **1090** om het nieuwe hardwareprofiel naar de winkel te synchroniseren. Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.
6.  Selecteer de distributieplanning **1040** om het nieuwe hardwarestation naar de winkel te synchroniseren. Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.
7.  Installeer het hardwarestation. Zie voor meer informatie over het installeren van het hardwarestation het onderwerp [Retail Hardware Station configureren en installeren](retail-hardware-station-configuration-installation.md).
8.  Installeer en activeer Modern POS. Zie [Modern POS (MPOS) configureren, installeren en activeren](retail-modern-pos-device-activation.md) voor meer informatie over het installeren van Modern POS.
9.  Meld u aan bij Modern POS en selecteer **Niet-ladebewerkingen uitvoeren**.
10. Start de bewerking **Hardwarestations beheren**.
11. Klik op **Beheren**.
12. Ga naar de pagina voor beheer van hardwarestations en stel de optie in om het hardwarestation in te schakelen.
13. Selecteer het hardwarestation dat u wilt gebruiken en klik op **Koppelen**.
14. Nadat het hardware-station is gekoppeld, klikt u op **Sluiten**.
15. Ga naar de pagina voor het selecteren van het hardwarestation en klik op het laatst geselecteerde hardwarestation om dit te activeren.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-clients met een gedeeld ISS-hardwarestation

Deze configuratie kan worden gebruikt voor alle Modern POS-clients die hardwarestations met andere apparaten delen. Volg deze stappen om deze configuratie in te stellen.

1.  Maak een hardwareprofiel aan waarin de vereiste randapparaten zijn geconfigureerd.
2.  Maak een hardwarestation van het type **Gedeeld** voor de winkel waar de POS-kassa wordt gebruikt.
3.  Stel op het gedeelde hardwarestation de volgende eigenschappen in:
    -   **Hostnaam:** De naam van de computer waarop het hardwarestation wordt uitgevoerd.
    -   **Beschrijving:** Tekst die helpt het hardwarestation te identificeren, zoals **Retouren** of **Voorzijde winkel**.
    -   **Poort:** De poort die u wilt gebruiken voor het hardwarestation voor communicatie met de Modern POS-client.
    -   **Hardwareprofiel:** Bij gedeelde hardwarestations moet elk hardwarestation een hardwareprofiel hebben. Hardwareprofielen kunnen worden gedeeld tussen hardwarestations, maar aan elk hardwarestation moet er een zijn toegewezen. Bovendien is het raadzaam om gebruik te maken van gedeelde ploegen, als meerdere apparaten gebruik maken van hetzelfde gedeelde hardwarestation. Om een gedeelde ploeg in te stellen, klikt u op **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**. Selecteer voor elk gedeelde hardwareprofiel de kassalade en stel de optie **Gedeelde ploeglade** in op **Ja**.
    -   **EFT POS-nummer:** De EFT-terminal-ID die moet worden gebruikt wanneer EFT-autorisaties worden verzonden. Deze ID wordt geleverd door de creditcardverwerker.
    -   **Pakketnaam:** Het hardwarestationpakket dat moet worden gebruikt wanneer het hardwarestation wordt geïmplementeerd.

4.  Herhaal stap 2 en 3 voor elk extra hardwarestation dat nodig is in de winkel.
5.  Klik op **Detailhandel en commerce** &gt; **IT detailhandel en commerce** &gt; **Distributieplanning**.
6.  Selecteer de distributieplanning **1090** om het nieuwe hardwareprofiel naar de winkel te synchroniseren. Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.
7.  Selecteer de distributieplanning **1040** om het nieuwe hardwarestation naar de winkel te synchroniseren. Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.
8.  Installeer het hardwarestation op elke hostcomputer die u in stap 2 en 3 hebt ingesteld. Zie voor meer informatie over het installeren van het hardwarestation het onderwerp [Retail Hardware Station configureren en installeren](retail-hardware-station-configuration-installation.md).
9.  Installeer en activeer Modern POS. Zie [Modern POS (MPOS) configureren, installeren en activeren](retail-modern-pos-device-activation.md) voor meer informatie over het installeren van Modern POS.
10. Meld u aan bij Modern POS en selecteer **Niet-ladebewerkingen uitvoeren**.
11. Start de bewerking **Hardwarestations beheren**.

12. Klik op **Beheren**.
13. Ga naar de pagina voor beheer van hardwarestations en stel de optie in om het hardwarestation in te schakelen.
14. Selecteer het hardwarestation dat u wilt gebruiken en klik op **Koppelen**.
15. Herhaal stap 14 voor elk hardwarestation dat Modern POS gaat gebruiken.
16. Nadat alle vereiste hardwarestations zijn gekoppeld, klikt u op **Sluiten**.
17. Ga naar de pagina voor het selecteren van het hardwarestation en klik op het laatst geselecteerde hardwarestation om dit te activeren. 

> [!NOTE]
> Als apparaten vaak verschillende hardwarestations gebruiken, raden we aan om Modern POS te configureren om kassiers te vragen een hardwarestation te selecteren, op het moment dat ze beginnen de betalingsmethode te selecteren. Klik op **Detailhandel en commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **Kassa's**. Selecteer de kassa en stel de optie **Selecteren bij offertes** in op **Ja**. Gebruik de distributieplanning **1090** om wijzigingen te synchroniseren naar de kanaaldatabase.

## <a name="extensibility"></a>Uitbreidbaarheid
Zie voor informatie over uitbreidbaarheidsscenario's voor het hardwarestation het onderwerp [Uitbreidbaarheid van hardwarestations](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Beveiliging
Volgens de huidige beveiligingsnormen moeten de volgende instellingen worden gebruikt in een productieomgeving: 

### <a name="hardware-station-installer"></a>Het hardwarestation installeren
Het installatieprogramma van het hardwarestation voert automatisch deze wijzigingen in het register door als onderdeel van de installatie via self-service.
 
-   Secure Sockets Layer (SSL) moet zijn uitgeschakeld.
-   Alleen Transport Layer Security (TLS) versie 1.2 (of de actuele hoogste versie) mag zijn ingeschakeld en worden gebruikt. 

### <a name="ssl-and-tls"></a>SSL en TLS
Standaard zijn SSL en alle versies van TLS behalve TLS 1.2 uitgeschakeld. Ga als volgt te werk om deze waarden te bewerken of in te schakelen:
    1.  Druk op de Windows-toets+R om een venster **Uitvoeren** te openen.
    2.  Typ in het veld **Openen** de tekst **Regedit** en klik vervolgens op **OK**.
    3.  Als een venster **Gebruikersaccountbeheer** wordt geopend, klikt u op **Ja**.
    4.  Navigeer in het venster **Register-editor** naar de sleutel **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. De volgende sleutels zijn automatisch ingevoerd om alleen TLS 1.2 toe te staan:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Geen extra netwerkpoorten mogen geopend zijn, tenzij ze vereist zijn om bekende en opgegeven redenen.
-   Cross-origin resource sharing (CORS) moet zijn uitgeschakeld en de toegestane origins die worden geaccepteerd, moeten zijn opgeven.
-   Alleen vertrouwde certificeringsinstanties moeten worden gebruikt om certificaten te krijgen, die worden gebruikt op computers waarop het hardwarestation draait.

> [!NOTE]
> Het is zeer belangrijk dat u beveiligingsrichtlijnen voor IIS en de vereisten van de Payment Card Industry (PCI) bestudeert.

## <a name="peripheral-simulator"></a>Randapparatuursimulator
Zie voor meer informatie het onderwerp [Randapparatuursimulator voor Commerce](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Door Microsoft geteste randapparaten
### <a name="ipc-built-in-hardware-station"></a>IPC-hardwarestation (geïntegreerd)

De volgende randapparaten zijn getest met het IPC-hardwarestation dat is geïntegreerd in Modern POS voor Windows.

#### <a name="printer"></a>Printer

| Fabrikant | Model    | Interface | Opmerkingen                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88   | Aangepast    | Aangesloten via netwerk   |
| Star         | TSP650II | Aangepast    | Aangesloten via netwerk   |
| Star         | mPOP     | OPOS      | Aangesloten via Bluetooth |
| HP           | F7M67AA  | OPOS      | USB met voeding             |

#### <a name="bar-code-scanner"></a>Streepjescodelezer

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
| VeriFone     | MX925 | Aangepast    | Vereist aanpassing van de betalingsconnector; aangesloten via een netwerk en USB |
| VeriFone     | MX915 | Aangepast    | Vereist aanpassing van de betalingsconnector; aangesloten via een netwerk en USB |

#### <a name="cash-drawer"></a>Kassalade

| Fabrikant | Model     | Interface | Opmerkingen                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Aangesloten via Bluetooth |
| APG          | Atwood    | Aangepast    | Aangesloten via netwerk   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Aangepast    | Aangesloten op Epson-netwerkprinter via DK-poort |

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

### <a name="dedicated-iis-hardware-station"></a>Specifiek ISS-hardwarestation

De volgende randapparaten zijn getest met een specifiek (niet-gedeeld) IIS-hardwarestation, samen met Modern POS voor Windows en Cloud POS.

#### <a name="printer"></a>Printer

| Fabrikant | Model    | Interface | Opmerkingen                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Epson        | TM-T88V  | Aangepast    | Aangesloten via netwerk     |
| Star         | TSP650II | Aangepast    | Aangesloten via netwerk     |
| HP           | F7M67AA  | OPOS      | USB met voeding               |

#### <a name="bar-code-scanner"></a>Streepjescodelezer

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
| VeriFone     | MX925 | Aangepast    | Vereist aanpassing van de betalingsconnector; aangesloten via een netwerk en USB |
| VeriFone     | MX915 | Aangepast    | Vereist aanpassing van de betalingsconnector; aangesloten via een netwerk en USB |

#### <a name="cash-drawer"></a>Kassalade

| Fabrikant | Model     | Interface | Opmerkingen              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Aangepast    | Aangesloten via netwerk |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Aangepast    | Aangesloten op Epson-netwerkprinter via DK-poort |

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

### <a name="shared-iis-hardware-station"></a>Gedeeld ISS-hardwarestation

De volgende randapparaten zijn getest met een gedeeld IIS-hardwarestation, samen met Modern POS voor Windows en Cloud POS. 

> [!NOTE]
> Alleen een printer, betalingsterminal en kassalade worden ondersteund.

#### <a name="printer"></a>Printer

| Fabrikant | Model    | Interface | Opmerkingen                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Epson        | TM-T88   | Aangepast    | Aangesloten via netwerk     |
| Star         | TSP650II | Aangepast    | Aangesloten via netwerk     |
| Star         | TSP100   | OPOS      | Vereist TSP650II-stuurprogramma's |
| HP           | F7M67AA  | OPOS      | USB met voeding               |

#### <a name="payment-terminal"></a>Betalingsterminal

| Fabrikant | Model | Interface | Opmerkingen                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Aangepast    | Vereist aanpassing van de betalingsconnector; aangesloten via een netwerk en USB |
| VeriFone     | MX915 | Aangepast    | Vereist aanpassing van de betalingsconnector; aangesloten via een netwerk en USB |

#### <a name="cash-drawer"></a>Kassalade

| Fabrikant | Model     | Interface | Opmerkingen              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Aangepast    | Aangesloten via netwerk |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Aangepast    | Aangesloten op Epson-netwerkprinter via DK-poort |


## <a name="troubleshooting"></a>Problemen oplossen
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kan het hardwarestation detecteren in de lijst voor selectie, maar kan de koppeling niet voltooien

**Oplossing:** Loop de onderstaande lijst met mogelijke storingsoorzaken door:

-   De computer waarop de Modern POS draait, vertrouwt het certificaat dat wordt gebruikt op de computer waarop het hardwarestation draait.
    -   Om deze configuratie te controleren, gaat u in een webbrowser naar de volgende URL: https://&lt;Computernaam&gt;:&lt;Poortnummer&gt;/HardwareStation/ping.
    -   Deze URL gebruikt een ping om te verifiëren dat toegang tot de computer mogelijk is en de browser geeft aan of het certificaat vertrouwd wordt. (In Internet Explorer bijvoorbeeld wordt een pictogram van een hangslot weergegeven in de adresbalk. Wanneer u op dit pictogram klikt, controleert Internet Explorer of het certificaat momenteel vertrouwd wordt. U kunt het certificaat installeren op de lokale computer aan de hand van de details van het certificaat dat wordt weergegeven.
-   Op de computer waarop het hardwarestation draait, wordt de poort die het hardwarestation gebruikt in de firewall geopend.
-   Het hardwarestation heeft de verkopersaccountgegevens correct geïnstalleerd via het hulpprogramma Verkopersgegevens installeren, dat wordt uitgevoerd aan het einde van het installatieprogramma voor het hardwarestation.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS kan het hardwarestation niet vinden in de lijst voor selectie

**Oplossing:** Dit kan worden veroorzaakt door één van de volgende:

-   Het hardwarestation is niet correct ingesteld in het hoofdkantoor. Verifieer met de stappen eerder in dit onderwerp of het hardwarestationprofiel en het hardwarestation correct zijn ingevoerd.
-   De taken voor het bijwerken van de afzetkanaalconfiguratie zijn nog niet uitgevoerd. Voer in dit geval taak 1070 voor afzetkanaalconfiguratie uit.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>In Modern POS zijn de nieuwe instellingen voor de kassalade niet zichtbaar.

**Oplossing:** Sluit de huidige batch. Wijzigingen in de kassalade worden pas bijgewerkt in Modern POS als de huidige batch is gesloten.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS meldt een probleem met een randapparaat

**Oplossing:** hier volgen enkele veelvoorkomende oorzaken van dit probleem:

-   Zorg ervoor dat andere configuratieprogramma's voor apparaatstuurprogramma's zijn gesloten. Als deze hulpprogramma's geopend zijn, verhinderen ze mogelijk dat Modern POS of het hardwarestation het apparaat aanspreken.
-   Als het randapparaat wordt gedeeld met verschillende POS-apparaten, overtuig u er dan van dat het apparaat deel uitmaakt van een van de volgende categorieën:
    -   Kassalade
    -   Kassabonprinter
    -   Betalingsterminal

    Als het randapparaat niet tot een van deze categorieën behoort, is het hardwarestation niet ontworpen om het randapparaat in te schakelen om te worden gedeeld tussen verschillende POS-apparaten.
-   Soms kunnen stuurprogramma ertoe leiden dat de Common Control Objects (CCO's) niet meer goed functioneren. Als een onlangs geïnstalleerd apparaat niet goed werkt of er andere problemen optreden, kunt u het probleem vaak oplossen door de CCO's opnieuw te installeren. Als u de CCO´s wilt downloaden, gaat u naar <http://monroecs.com/oposccos_current.htm>.
-   Als u regelmatig randapparatuur wijzigt tijdens testen of probleemoplossing, moet u wellicht IIS resetten in plaats van te wachten totdat de cache zichzelf vernieuwt. Ga als volgt te werk om IIS te resetten:
    1.  Typ in het menu **Start** de opdracht **CMD**.
    2.  Klik in de lijst met zoekresultaten met de rechtermuisknop op **Opdrachtprompt** en klik vervolgens op **Uitvoeren als beheerder**.
    3.  Typ in het venster **Opdrachtprompt** de tekst **iisreset/restart** en druk op Enter.
    4.  Start Modern POS opnieuw op nadat IIS opnieuw is opgestart.
-   Wanneer u vaak randapparaten aanpast en ook regelmatig de POS-client opstart en afsluit, kan het proces dllhost van een eerdere POS-sessie de huidige sessie storen. In dit geval kan het niet mogelijk zijn om een apparaat te gebruiken, totdat u de dll-host afsluit die de vorige sessie beheert. Ga als volgt te werk om de dll-host te sluiten:
    1.  Typ in het menu **Start** de opdracht **Taakbeheer**.
    2.  Klik in de lijst met zoekresultaten op **Taakbeheer**.
    3.  Klik in Taakbeheer op het tabblad **Details** en klik op de kolomkop met de naam **Naam** in de tabel alfabetisch op naam te sorteren.
    4.  Schuif omlaag tot u dllhost.exe vinden.
    5.  Selecteer alle dll-hosts en klik vervolgens op **Taak beëindigen**.
    6.  Nadat de DLL-hosts zijn afgesloten, start u moderne POS opnieuw op.


<a name="additional-resources"></a>Aanvullende resources
--------

[Randapparatuursimulator voor Commerce](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]