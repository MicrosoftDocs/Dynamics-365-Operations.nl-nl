---
title: Simulator voor detailhandelrandapparaten
description: In dit onderwerp wordt de tool voor randapparaatsimulatie beschreven, die wordt geleverd met Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 11a4633b0a1254f3a8cbdcba8d7aa99bb7c936c1
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="retail-peripheral-simulator"></a>Simulator voor detailhandelrandapparaten

[!include[banner](includes/banner.md)]


In dit onderwerp wordt de tool voor randapparaatsimulatie beschreven, die wordt geleverd met Microsoft Dynamics 365 for Operations - Retail.

<a name="overview"></a>Overzicht
--------

De simulator voor detailhandelrandapparaten in Microsoft Dynamics 365 for Operations - Retail is een hulpprogramma waarmee u randapparaten kunt instellen, testen en troubleshooten, die worden gebruikt in detailhandelomgevingen. Met de randapparaatsimulator kunt u het testen van retailrandapparaten stroomlijnen en problemen isoleren die worden veroorzaakt door onjuiste instellingen of slecht functionerende stuurprogramma's. De randapparaatsimulator bevat een pc-programma met virtuele versies van apparaten die Dynamics 365 for Operations - Retail ondersteunt. Voor elk virtueel apparaat is er een sectie, waarin u de interactie ziet tussen het apparaat en het detailhandel-POS. Ook kunt u hiermee gegevens invoeren die geldig is voor verschillende POS-scenario's. De randapparaatsimulator ondersteunt interactie tussen het POS en de volgende virtuele apparaten:

-   **Printer**: De randapparaatsimulator kan ontvangstbewijzen weergeven die zijn geconfigureerd voor een POS-printer.
-   **Regelweergave**: U kunt een virtuele regelweergave configureren, waarop de activiteit op een fysieke regelweergave wordt weergegeven.
-   **Magneetstriplezer (MSR)**: U kunt gesimuleerde magneetstripgebeurtenissen verzenden naar het POS vanuit de randapparaatsimulator.
-   **Lade**: U kunt een fysieke kassalade simuleren.
-   **Lade 2**: Als u een tweede kassalade instelt in de randapparaatsimulator, kunt u scenario's simuleren voor een enkele POS-kassa met twee actieve diensten.
-   **Scanner**: De virtuele streepjescodescanner die de randapparaatsimulator ondersteunt, kan gebeurtenissen voor scannen van codes genereren.
-   **Schaal**: Met een virtuele schaal kunt u de interactie tussen gewogen artikelen en het POS simuleren.
-   **Toetsenblok voor persoonlijke identificatienummers (PIN)**: U kunt bewerkingen met een PIN-toetsenblok simuleren. **Opmerking:** Ondersteuning voor een fysiek pinapparaat moet u implementeren via de betalingsconnector.
-   **Handtekeningregistratie**: De randapparaatsimulator bevat een virtueel apparaat voor handtekeningregistratie dat u kunt instellen om te vragen om handtekeningen die vereist zijn voor bepaalde betalingsmogelijkheden, zoals betalingen van klantenrekeningen.

Met de randapparaatsimulator kunt u ook keyboard-wedge-gebeurtenissen simuleren, die worden veroorzaakt door een streepjescodescanner en MSR. De virtuele randapparaatsimulator ondersteunt specifiek OPOS-apparaten (Object Linking and Embedding voor Retail POS).

## <a name="key-scenarios"></a>Belangrijke scenario's
### <a name="troubleshooting"></a>Problemen oplossen

U kunt met de randapparaatsimulator problemen bij het instellen van apparaten oplossen. Als u geen randapparaatsimulator of een tweede apparaat van dezelfde klasse hebt, kan het lastig zijn om te bepalen hoe problemen ontstaan. Met de randapparaatsimulator kunt u echter virtuele apparaten instellen en dezelfde codepaden en zakelijke logica uitvoeren die worden gebruikt voor fysieke apparaten. Vanuit het perspectief van de randapparaatsimulator is het belangrijkste verschil tussen de virtuele apparaten en fysieke apparaten het serviceobject ofwel apparaatstuurprogramma. Voor fysieke apparaten wordt het serviceobject geleverd door de fabrikant van het apparaat. Bij de randapparaatsimulator worden de serviceobjecten daarentegen geleverd als onderdeel van de simulator. Als er in de randapparaatsimulator geen problemen zijn en een apparaat niet goed werkt nadat de apparaatnaam in het hardwareprofiel is gewijzigd in de naam van een echt apparaat, kunt u ervan uitgaan dat er een probleem is met het serviceobject dat de fabrikant heeft geleverd.

### <a name="training"></a>Opleiding

U kunt met de randapparaatsimulator een realistische laag toevoegen aan de training van kassamedewerkers als u niet over een fysieke hardwareconfiguratie beschikt. Wanneer de randapparaatsimulator deel uitmaakt van trainingsscenario's kan de kassamedewerker efficiënter werken met het POS door invoer te verschaffen zoals barcodescans van producten en uitlezing van geschenkbonnen en door te zien welke ontvangstbewijzen worden afgedrukt voor specifieke transacties.

### <a name="testing"></a>Testen

U kunt met de randapparaatsimulator streepjescodes van producten, ontvangstbewijsindelingen en dergelijke testen zonder dat u fysieke hardware in een virtuele omgeving hoeft te implementeren. Omdat de fysieke hardware niet is vereist en u niet een POS-client op een hardwarestation of een fysieke computer hoeft te implementeren, kunt u sneller wijzigingen testen die zijn aangebracht in de back office.

## <a name="set-up-the-peripheral-simulator"></a>De randapparaatsimulator instellen
### <a name="set-up-a-hardware-profile"></a>Een hardwareprofiel instellen

1.  Om de randapparaatsimulator in te stellen, gaat u naar **Detailhandel en commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Klik op **Nieuw** om een nieuw profiel te maken.
3.  Voer in de velden **Profielnummer** en **Beschrijving** waarden in.
4.  Aan de hand van de volgende tabel kunt u de virtuele apparaten instellen die u wilt testen. Hier volgt een uitleg van de kolommen in de tabel:
    -   **Apparaat**: In deze kolom vindt u de naam van het sneltabblad dat u uitvouwt om het apparaat in te stellen.
    -   **Apparaattype**: In deze kolom vindt u de waarde die u selecteert in het veld dat wordt aangeduid met de naam van het apparaat.
    -   **Apparaatnaam**: In deze kolom vindt u de exacte waarde die u voor de apparaatnaam invoert. **Belangrijk:** De namen die hier worden genoemd, zijn vereist omdat het hardwarestation deze specifieke namen gebruikt om de apparaten aan te spreken. Als u deze specifieke namen niet gebruikt, kan het apparaat niet worden gebruikt.

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

**Opmerking:** Er zijn geen specifieke instellingen in het hardwareprofiel vereist om keyboard-wedge-gebeurtenissen van de streepjescodesscanner en MSR te simuleren.

### <a name="assign-the-hardware-profile-to-a-register"></a>Het hardwareprofiel toewijzen aan een kassa

1.  Nadat u het hardwareprofiel hebt gemaakt, gaat u naar **Detailhandel en commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen**&gt;**Kassa's**.
2.  Klik in de lijst **POS-kassa's** op de koppeling in het veld **Kassanummer** voor de kassa waarvoor u de randapparaatsimulator wilt gebruiken.
3.  Klik op **Bewerken**.
4.  Selecteer in de sectie **Profielen** in het veld **Hardwareprofiel** het hardwareprofiel dat u hebt gemaakt voor virtuele randapparaten.
5.  Klik op **Opslaan**.

### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen synchroniseren met de afzetkanaaldatabase

1.  Ga naar **Detailhandel en commerce** &gt; **Detailhandel-IT** &gt; **Distributieplanning**.
2.  Selecteer de distributieplanning **1090**.
3.  Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.

Nadat de gegevens zijn gesynchroniseerd, zijn de nieuwe hardwareprofiel en wijzigingen in de kassa beschikbaar in de afzetkanaaldatabase.

## <a name="install-the-peripheral-simulator"></a>De randapparaatsimulator installeren
1.  Ga naar **Detailhandel en commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Klik op **Downloaden** en vervolgens op **PeripheralSimulator**. **Opmerking:** U moet pop-upblockers uitschakelen voordat u de randapparaatsimulator kunt downloaden.
3.  Nadat het downloaden is voltooid, opent u de map **Downloads** en dubbelklikt u op **VirtualPeripherals.msi** om het installatieprogramma te starten.
4.  De randapparaatsimulator installeren met de standaardinstellingen.

Naast de randapparaatsimulator moet u de Common Control Objects van Monroe Consulting Services installeren. Anders functioneert de randapparaatsimulator niet correct. Om de Common Control Objecten te downloaden, gaat u naar <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>De randapparaatsimulator gebruiken
Om de randapparaatsimulator te starten, klikt u op **Starten** op uw computer. U typt **Detailhandel randapparaatsimulator** en selecteert vervolgens de app als deze wordt weergegeven in de zoekresultaten. Nadat u de randapparaatsimulator hebt gestart, klikt u op een apparaatnaam om de ondersteunde apparaten te zien. Deze apparaten wordt weergegeven als tabbladen aan de linkerkant van het venster. Klik op het tabblad voor een bepaald apparaat om dat apparaat weer te geven.

### <a name="line-display-capabilities"></a>Mogelijkheden voor regelweergave

De regelweergave is het eerste apparaat dat wordt vermeld in de randapparaatsimulator. Als de virtuele regelweergave is geconfigureerd, worden hierin regelartikelen getoond terwijl zij in de POS-transactie worden gescand. De weergave bevat naast regelartikelen het totaalbedrag dat is verschuldigd, wanneer een betalingsmethode wordt geselecteerd op het POS. Ook wordt het saldo getoond dat nog openstaat als een betalingsmethode wordt uitgevoerd, maar er nog een saldo openstaat voor de transactie. Wanneer het POS niet wordt gebruikt, kan een bericht worden weergegeven om aan te geven dat de kassa gesloten is. Moet u het bericht configureren op het sneltabblad **Weergaveregel** in het hardwareprofiel.

### <a name="cash-drawer-capabilities"></a>Mogelijkheden voor kassaladen

De kassalade is het tweede apparaat dat wordt vermeld in de randapparaatsimulator. Wanneer het hardwareprofiel is geconfigureerd voor gebruik van virtuele kassalades, opent het POS de kassalade voor de actieve ploeg in reactie op ladebewerkingen zoals kassacontroles, en zodat de kassamedewerker wisselgeld kan nemen of contant geld kan invoegen bij standaard contante transacties. De virtuele kassalades hebben de labels **Hoofdlade** en **Secundaire lade**. Deze labels vertegenwoordigen in het hardwareprofiel respectievelijk Lade en Lade 2. Wanneer een lade is gesloten, wordt een afbeelding van een gesloten kassalade weergegeven en de knop op de gesloten kassalade draagt de tekst **Lade openen**. Als u op deze knop klikt, wordt de afbeelding vervangen door een afbeelding van een geopende kassalade om aan te geven dat de lade nu geopend is. De knop op de geopende kassalade draagt nu de tekst **Lade sluiten**. Meerdere bewerkingen op het POS kunnen ertoe leiden dat de kassalade wordt geopend. De meeste bewerkingen kunnen niet worden voortgezet zolang de kassalade geopend is. De uitzonderingen zijn sommige einde-dagprocedures. Als de POS-gebruiker een foutbericht ontvangt waarin wordt gemeld dat een bewerking niet kan worden uitgevoerd zolang de kassalade geopend is, moet de gebruiker de virtuele of fysieke kassalade sluiten om door te gaan. Als een kassalade is gemarkeerd als **Gedeeld** in het hardwareprofiel, controleert het systeem niet of de lade vóór een bewerking dicht is. De bewerking gaat door zoals gebruikelijk, zelfs als de kassalade open staat. Dit gedrag ondersteunt scenario's waarbij kassalades worden gedeeld door verkoopmedewerkers en één medewerker een kassalade gebruikt, terwijl een andere medewerker niet-gerelateerde taken uitvoert op zijn of haar eigen POS-apparaat. Wijzigingen die zijn aangebracht in de kassalade zijn niet zichtbaar totdat de huidige ploeg afsluit en een nieuwe ploeg opent.

### <a name="msr-capabilities"></a>Mogelijkheden voor magneetstriplezer (MSR)

De randapparaatsimulator biedt krachtige ondersteuning voor virtuele MSR-bewerkingen, in de OPOS-modus of in de keyboard-wedge-modus. Voor de OPOS-modus is vereist dat de MSR is geconfigureerd in het hardwareprofiel om te functioneren als een OPOS-apparaat. In de keyboard-wedge-modus worden alleen maar gebeurtenissen met keyboard-wedge-gegevens naar Microsoft Windows verzonden. Naast de verschillen in configuratie kennen de OPOS- en de keyboard-wedge-modus de volgende verschillen:

-   De POS-client schakelt OPOS MSR-apparaten in voor specifieke scenario's, zoals scenario's waarin gegevens van magneetstrips kunnen worden gebruikt voor invoer van loyaliteitskaarten of geschenkbonnen.
-   In de keyboard-wedge-modus verzendt de randapparaatsimulator keyboard-wedge-gegevens naar het veld dat wordt geactiveerd wanneer de gegevens worden verzonden. Dit gedrag lijkt op wat er gebeurt als de gegevens worden ingevoerd met behulp van een toetsenbord. Als u de MSR wilt gebruiken als een keyboard-wedge, moet de gebruiker overschakelen naar Retail Modern POS (MPOS) om ervoor te zorgen dat gegevens worden ontvangen in het juiste veld. U kunt daarom een vertraging configureren, zodat de gebruiker tijd heeft om ervoor te zorgen heeft dat de gegevens worden verzonden naar het juiste veld.

#### <a name="testing-gift-and-payment-card-swipes"></a>Uitlezen van geschenk- en betalingskaarten testen

Met de virtuele MSR die de randapparaatsimulator biedt, kunt u ook specifieke MSR-gegevens configureren om scenario's te testen voor het uitlezen van geschenk- en betalingskaarten. Om een kaart te maken, klikt u op het plusteken (**+**) en selecteert u het type kaart. Vervolgens geeft u het kaartnummer of de traceringsgegevens op die u naar het POS wilt laten zenden, samen met de vervaldatum (maand en jaar) voor de kaart die u definieert. De waarde die u selecteert in het veld **Kaarttype** is alleen een label dat kan worden toegewezen aan een kaart. Met dit label kunt u gemakkelijker kaarten herkennen, wanneer ze in de randapparaatsimulator worden gelezen. U kunt de kaarten selecteren die zijn geconfigureerd in de randapparaatsimulator met behulp van de knoppen pijl-links (**&lt;**) en pijl-rechts (**&gt;**) boven de afbeelding van de kaart. U kunt kaarten bewerken en verwijderen met behulp van de knoppen **Bewerken** en **Verwijderen** naast de plus-knop (**+**).

### <a name="pin-pad"></a>Pinapparaat

U kunt de pinapparaatsimulator configureren om een OPOS-pinapparaat te simuleren. Wanneer een transactie met een elektronische betaling (EFT) wordt uitgevoerd op het POS en invoer van een PIN is vereist, roept de hardwarestation het PIN-apparaat aan om te vragen om invoer van PIN. Om dit te laten werken, vereist het pinapparaat in de randapparaatsimulator ondersteuning voor de EFT-betalingsconnector.

### <a name="printer"></a>Printer

De virtuele randapparaatprinter geeft ontvangstbewijzne net zo weer als deze worden afgedrukt op het POS. Als een afdrukbewerking meerdere ontvangstbewijzen genereert, kunt u door de ontvangstbewijzen bladeren.

#### <a name="configure-receipt-printing"></a>Afdrukken van ontvangstbewijzen configureren

1.  Ga naar **Detailhandel en commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Selecteer het hardwareprofiel dat u hebt gemaakt voor virtuele randapparaten.
3.  Klik op het sneltabblad **Printer** op **Bewerken**.
4.  Selecteer in het veld **Id ontvangstbewijsprofiel** een ontvangstbewijsprofiel.
5.  Klik op **Opslaan**.

### <a name="scale"></a>Schaal

Wanneer een weegschaalproduct wordt toegevoegd aan de POS-transactie en een weegschaal is geconfigureerd, haalt het POS het gewicht op bij de schaal. Voor de virtuele en de fysieke schaal moet het product of het gewicht worden opgegeven, voordat het product wordt toegevoegd aan de transactie. Voordat u het weegschaalproduct aan de transactie toevoegt, gaat u naar de weegschaal in de randapparaatsimulator. Met de plus-knop (**+**) en de min-knop (**:**) past u het gewicht aan dat de schaal moet doorgeven. U kunt het gewenste gewicht ook rechtstreeks in het veld **Huidige waarde** invoeren. U kunt de gewichtseenheden van de weegschaal aanpassen door middel van de knoppen Plus (**+**), **Bewerken** en **Verwijderen**. Op deze manier kunnen eenheden worden opgegeven op basis van de producten die worden gewogen of de landinstelling waar de weegschaal wordt gebruikt.

#### <a name="configure-a-scale-product"></a>Een weegschaalproduct configureren

1.  Ga naar **Detailhandel en** **commerce** &gt; **Producten en categorieën** &gt; **Vrijgegeven producten per categorie**.
2.  Open de productrecord.
3.  Selecteer het product dat moet worden gewogen.
4.  Wijzig op het sneltabblad **Detailhandel** de waarde van de optie **Weegschaalproduct** van **Nee** naar **Ja**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen synchroniseren met de afzetkanaaldatabase

1.  Ga naar **Detailhandel en commerce** &gt; **Detailhandel-IT** &gt; **Distributieplanning**.
2.  Selecteer de distributieplanning **1040**.
3.  Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.

Na gegevenssynchronisatie haalt het POS, wanneer een weegschaalproduct wordt toegevoegd aan de POS-transactie en een weegschaal is geconfigureerd, het gewicht op bij de schaal.

### <a name="signature-capture"></a>Handtekeningregistratie

Het virtuele apparaat voor handtekeningregistratie vraagt de gebruiker om een handtekening te zetten op het virtuele handtekeningapparaat, wanneer een handtekening is vereist voor de gebruikte betalingsmethode. De gebruiker kan de handtekening laten weergeven op het POS. De kassamedewerker kan de handtekening vervolgens accepteren. De handtekening wordt vervolgens opgeslagen, samen met de betaling en wordt gesynchroniseerd met de back office samen met andere transactiegegevens.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Een handtekening bij een betalingsmethode vereisen

1.  Ga naar **Detailhandel en commerce** &gt; **Afzetkanalen** &gt; **Detailhandelwinkels** &gt; **Alle detailhandelwinkels**.
2.  Selecteer de gewenste winkel.
3.  Klik op **Bewerken**.
4.  Klik op **Instellingen** en klik in de sectie **Instellingen** op **Betalingsmethoden**.
5.  Klik op **Bewerken**.
6.  Selecteer de betalingsmethode waarvoor een handtekening is vereist.
7.  Stel in de sectie **Algemeen** onder **Handtekeningregistratie** de optie **Apparaat voor handtekeningregistratie gebruik** in op **Ja**.
8.  Voer in het veld **Minimumbedrag handtekeningregistratie** het minimumbedrag in dat de vraag om handtekeningregistratie moet activeren.

#### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen synchroniseren met de afzetkanaaldatabase

1.  Ga naar **Detailhandel en commerce** &gt; **Detailhandel-IT** &gt; **Distributieplanning**.
2.  Selecteer de distributieplanning **1070**.
3.  Klik op **Nu uitvoeren** om wijzigingen met het POS te synchroniseren.

Als na gegevenssynchronisatie een betalingsmethode wordt gebruikt waarvoor een handtekening wordt vereist en waarbij het bedrag voldoet aan de handtekeningdrempel, wordt gevraagd om een handtekening te zetten op het virtuele handtekeningapparaat.

## <a name="additional-configuration"></a>Aanvullende configuratie
U kunt het configuratiebestand van de randapparaatsimulator bewerken, om beter de scenario's af te handelen die wilt testen. U vindt het configuratiebestand op C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. In het configuratiebestand worden de eenheden gedefinieerd die beschikbaar zijn voor het testen op de weegschaal, de kaarttypen die beschikbaar zijn voor het testen en streepjescodetypen. Door de tekstwaarden in het configuratiebestand aan te passen, kunt u bijvoorbeeld een nieuw kaarttype of maateenheid toevoegen, die kan worden geselecteerd tijdens de uitvoering. De nieuwe waarden worden weergegeven nadat de toepassing opnieuw is opgestart.

## <a name="troubleshooting"></a>Problemen oplossen
Activiteiten voor de randapparaatsimulator worden vastgelegd in de randapparaatsimulator. U vindt het logboekbestand op C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. De randapparaatsimulator zendt ook meldingen van problemen ook naar het Windows-gebeurtenissenlogboek. Dit kunt u openen via **Logboeken voor toepassingen en services** &gt; **Microsoft** &gt; **DynamicsAX**. Als wijzigingen die u hebt aangebracht in het hardwareprofiel of andere gebieden niet zichtbaar zijn wanneer u MPOS of de randapparaatsimulator gebruikt, controleert u de plannertaken voor distributie waarmee u de gegevens synchroniseert met de afzetkanaaldatabase. Als de wijzigingen zijn gesynchroniseerd, maar nog steeds niet zichtbaar zijn in het POS, moet u de POS-client opnieuw opstarten. Wijzigingen in geconfigureerde kassaladen worden pas van kracht wanneer u een nieuwe dienst aanmaakt. Als u wijzigingen in de kassaladen aanbrengt, moet u er daarom altijd op letten dat u de bestaande dienst afsluit om de nieuwe instellingen van de kassalade te testen. Het gebeurt soms wanneer het stuurprogramma van een fabrikant wordt geïnstalleerd nadat de Common Control Objects van Monroe Consulting Services zijn geïnstalleerd, het stuurprogramma de Common Control Objects verhindert om correct te functioneren. In dit geval moet u de Common Control Objects opnieuw installeren.

<a name="see-also"></a>Zie ook
--------

[Overzicht van randapparatuur voor de detailhandel](retail-peripherals-overview.md)




