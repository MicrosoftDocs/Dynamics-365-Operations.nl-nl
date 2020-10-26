---
title: Inkomende voorraadbewerking in POS
description: In dit onderwerp worden de mogelijkheden van inkomende voorraadbewerking van het verkooppunt (POS) beschreven.
author: hhaines
manager: annbe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 89021a85c2b215695d7cc25215c049205f71956d
ms.sourcegitcommit: 6e0d6d291d4881b16a677373f712a235e129b632
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/08/2020
ms.locfileid: "3971492"
---
# <a name="inbound-inventory-operation-in-pos"></a>Inkomende voorraadbewerking in POS

[!include [banner](includes/banner.md)]

In Microsoft Dynamics 365 Commerce versie 10.0.10 en hoger worden inkomende en uitgaande bewerkingen op het verkooppunt (POS) vervangen door de bewerking voor orderverzameling en ontvangst.

> [!NOTE]
> In Commerce versie 10.0.10 en hoger worden alle nieuwe functies in de POS-toepassing die verband houden met de ontvangst van winkelvoorraad op basis van inkooporders en transferorders, toegevoegd aan de POS-bewerking voor **Inkomende bewerking**. Als u momenteel orderverzameling en ontvangst in POS gebruikt, kunt u het beste een strategie ontwikkelen voor het overbrengen van deze bewerking naar de nieuwe inkomende en uitgaande bewerkingen. Hoewel de orderverzamelings- en ontvangstbewerking niet uit het product wordt verwijderd, vinden er geen verdere investeringen in die bewerking plaats, vanuit functioneel of prestatieperspectief, na versie 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Vereiste: een asynchroon documentraamwerk configureren

De inkomende bewerking omvat prestatieverbeteringen om ervoor te zorgen dat gebruikers met grote hoeveelheden ontvangstboekingen in een groot aantal winkels of bedrijven en grote voorraaddocumenten deze documenten kunnen verwerken naar Commerce Headquarters zonder dat er time-outs of storingen optreden. Deze verbeteringen vereisen het gebruik van een asynchroon documentraamwerk.

Wanneer een asynchroon documentraamwerk wordt gebruikt, kunt u wijzigingen in inkomende documenten doorvoeren vanuit POS naar Commerce Headquarters en vervolgens naar andere taken gaan terwijl de verwerking naar Commerce Headquarters op de achtergrond plaatsvindt. U kunt de status van het document controleren via de documentlijstpagina **Inkomende bewerking** in POS om er zeker van te zijn dat de boeking is geslaagd. In de POS-toepassing kunt u ook de lijst met actieve documenten voor inkomende bewerking gebruiken om documenten weer te geven die niet naar Commerce Headquarters konden worden geboekt. Als de verwerking van een document mislukt, kunnen POS-gebruikers hierin correcties aanbrengen en het document vervolgens opnieuw proberen te verwerken naar Commerce Headquarters.

> [!IMPORTANT]
> Het asynchrone documentraamwerk moet worden geconfigureerd voordat een bedrijf de inkomende bewerking in POS probeert te gebruiken.

Voer de volgende procedures uit om een asynchroon documentraamwerk te configureren.

### <a name="create-and-configure-a-number-sequence"></a>Een nummerreeks maken en configureren

1. Ga naar **Organisatiebeheer \> Nummerreeksen \> Nummerreeksen**.
2. Maak op de pagina **Nummerreeksen** een nummerreeks.
3. Voer in de velden **Nummerreekscode** en **Naam** door de gebruiker gedefinieerde waarden in.
4. Selecteer op het sneltabblad **Verwijzingen** de optie **Toevoegen**.
5. Selecteer in het veld **Gebied** de optie **Commerce-parameters**.
4. Selecteer in het veld **Verwijzing** de optie **Bewerkings-id van detailhandeldocument**.
5. Stel op het sneltabblad **Algemeen** in de sectie **Instellen** de optie **Continu** in op **Nee** om er zeker van te zijn dat er geen prestatieproblemen optreden.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Twee batchtaken maken en plannen voor de taken voor documentverwerking en -controle

> [!NOTE]
> In Commerce versie 10.0.13 en hoger hoeft u deze batchtaken niet via het raamwerk van de batchtaak te configureren. De batchprocessen kunnen worden geconfigureerd vanuit het menu **Detailhandel en commerce > IT detailhandel en commerce**. Gebruik de menuopties **Controle bewerking detailhandelsdocument** en **Verwerking bewerking detailhandelsdocument** om de batchtaken te configureren.

De batchtaken die u maakt, worden gebruikt voor het verwerken van documenten die zijn mislukt of waarvoor een time-out is opgetreden. Ze worden ook gebruikt wanneer het aantal actieve voorraaddocumenten dat vanuit POS wordt verwerkt, groter is dan een door het systeem geconfigureerde waarde.

1. Ga naar **Systeembeheer \> Query's \> Batchtaken**.
2. Maak op de pagina **Batchtaak** twee batchtaken:

    - Configureer de ene taak om de klasse **RetaildocumentOperationMonitorBatch** uit te voeren.
    - Configureer de andere taak om de klasse **RetailDocumentOperationProcessingBatch** uit te voeren.

2. Plan de nieuwe batchtaken plannen zodanig dat deze op periodieke basis worden uitgevoerd. Zo kunt u de planning bijvoorbeeld zo instellen dat de taken om de vijf minuten worden uitgevoerd.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Vereiste: Inkomende bewerking toevoegen aan de POS-schermindeling

Voordat uw organisatie de functionaliteit voor inkomende bewerkingen kan gebruiken, moet deze de POS-bewerking **Inkomende bewerking** configureren op een of meer van uw [POS-schermindelingen](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Voordat u de nieuwe bewerking in een productieomgeving implementeert, moet u ervoor zorgen dat u deze grondig test en de gebruikers traint in het gebruik hiervan.

## <a name="overview"></a>Overzicht

Met de inkomende bewerking kunnen POS-gebruikers de volgende taken uitvoeren:

- Voorraad ontvangen in winkelvoorraad vanuit bevestigde inkooporderdocumenten of verzonden transferorderdocumenten.
- Informatie weergeven over historische voorraadontvangsten voor een periode van zeven dagen nadat het document volledig is ontvangen.
- Nieuwe aanvragen voor inkomende transferorders maken.

Wanneer de inkomende bewerking vanuit de POS-toepassing wordt gestart, wordt er een lijstpaginaweergave getoond. In deze weergave worden openstaande inkooporder- en transferorderdocumenten weergegeven met voorraadregels die staan gepland voor ontvangst door de huidige winkel. Als gebruikers een specifiek document willen zoeken en selecteren, kunnen zij door de lijst bladeren of de zoekfunctie gebruiken.

De lijst met inkomende voorraaddocumenten bestaat uit drie tabbladen:

- **Actief**: dit tabblad toont documenten die volledig of gedeeltelijk geopend zijn en die regels of hoeveelheden op regels bevatten die nog moeten worden ontvangen.
- **Concept**: dit tabblad toont nieuwe aanvragen voor inkomende transferorders die door de winkel zijn gemaakt. De documenten zijn echter alleen lokaal opgeslagen. Ze zijn nog niet ingediend bij Commerce Headquarters voor verwerking.
- **Voltooid**: op dit tabblad wordt een lijst weergegeven met inkooporder- of transferorderdocumenten die de winkel volledig heeft ontvangen in de afgelopen zeven dagen. Dit tabblad is alleen bedoeld voor informatieve doeleinden. Alle gegevens over de documenten zijn alleen-lezen gegevens voor de winkel.

Wanneer u documenten op een van de tabbladen bekijkt, kan het veld **Status** helpen beter inzicht te krijgen in de fase waarin het document zich bevindt.

- **Concept**: het transferorderdocument is alleen lokaal opgeslagen in de kanaaldatabase van de winkel. Er is nog geen informatie over de aanvraag voor de transferorder ingediend bij Commerce Headquarters.
- **Aangevraagd**: de inkooporder of transferorder is gemaakt in Commerce Headquarters en is volledig open. Er zijn nog geen ontvangsten voor het document verwerkt. Voor documenten van het type inkooporderdocument kan de ontvangst op elk gewenst moment plaatsvinden terwijl de status **Aangevraagd** is.
- **Gedeeltelijk verzonden**: het transferorderdocument bevat een of meer regels of gedeeltelijke regelhoeveelheden die zijn geboekt als verzonden door het uitgaande magazijn. Deze verzonden regels kunnen via de inkomende bewerking worden ontvangen.
- **Volledig verzonden**: de transferorder heeft alle regels en volledige regelhoeveelheden geboekt als verzonden door het uitgaande magazijn. Het hele document kan via de inkomende bewerking worden ontvangen.
- **Gedeeltelijk ontvangen**: sommige regels of hoeveelheden in het inkooporder- of transferorderdocument zijn ontvangen door de winkel, maar sommige regels blijven openstaan.
- **Volledig ontvangen**: alle regels en hoeveelheden in het inkooporder- of transferorderdocument zijn volledig ontvangen. De documenten zijn alleen toegankelijk op het tabblad **Voltooid** en zijn alleen-lezen voor winkelgebruikers.
- **In uitvoering**: deze status wordt gebruikt om gebruikers van het apparaat te informeren dat een andere gebruiker actief werkt aan het document.
- **Onderbroken**: deze status wordt weergegeven nadat de optie **Ontvangen onderbreken** is geselecteerd om het ontvangstproces tijdelijk te stoppen.
- **Verwerkt in HQ**: het document is vanuit de POS-toepassing ingediend bij Commerce Headquarters, maar het is nog niet geboekt naar Commerce Headquarters. Het document doorloopt het proces voor asynchrone documentboeking. Nadat het document is geboekt naar Commerce Headquarters, moet de status worden bijgewerkt naar **Volledig ontvangen** of **Gedeeltelijk ontvangen**.
- **Verwerking mislukt**: het document is geboekt naar Commerce Headquarters en afgewezen. In het **detailvenster** wordt de reden voor de mislukte boeking weergegeven. Het document moet worden bewerkt om gegevensproblemen op te lossen en moet vervolgens opnieuw worden ingediend bij Commerce Headquarters voor verwerking.

Wanneer u een documentregel in de lijst selecteert, wordt een **detailvenster** weergegeven. Dit deelvenster bevat aanvullende informatie over het document, zoals gegevens over zending en datum. Via een voortgangsbalk wordt aangegeven hoeveel artikelen nog moeten worden verwerkt. Als het document niet is verwerkt in Commerce Headquarters, worden in het **detailvenster** ook foutberichten weergegeven die betrekking hebben op de fout.

In de lijstpaginaweergave voor het document kunt u **Orderdetails** op de appbalk selecteren om de details van het document weer te geven. U kunt ook ontvangstverwerking activeren voor in aanmerking komende documentregels.

In de lijstpaginaweergave voor documenten kunt u ook een nieuwe ingaande transferorderaanvraag voor een winkel maken. De documenten blijven de status **Concept** houden en kunnen worden aangepast of verwijderd totdat ze voor verwerking naar Commerce Headquarters worden verzonden. Nadat de regels zijn ingediend bij Commerce Headquarters, kunnen de transferorderregels niet meer worden gewijzigd vanuit de POS-toepassing.

## <a name="receiving-process"></a>Ontvangstproces

Nadat u een inkooporder- of transferorderdocument hebt geselecteerd op het tabblad **Actief**, kunt u **Orderdetails** selecteren om het ontvangstproces te starten.

De weergave **Nu ontvangen** wordt standaard weergegeven. Deze weergave is geoptimaliseerd voor het scannen van streepjescodes. De weergave kan worden gebruikt voor het samenstellen van een lijst met artikelen die zijn gescand, zodat deze artikelen kunnen worden ontvangen. Als u het ontvangstproces wilt starten, kunt u beginnen met het scannen van streepjescodes voor artikelen.

Wanneer streepjescodes van artikelen worden gescand in de weergave **Nu ontvangen**, worden de artikelen gevalideerd op basis van het geselecteerde inkooporder- of transferorderdocument om ervoor te zorgen dat elk gescand artikel overeenkomt met een geldig artikel in het document. In de weergave **Nu ontvangen** wordt aangenomen dat elke scan van een streepjescode de ontvangst van een hoeveelheid van één eenheid vertegenwoordigt, tenzij een hoeveelheid is ingesloten in de streepjescode. U kunt in deze weergave herhaaldelijk streepjescodes scannen om een lijst samen te stellen met alle artikelen en hoeveelheden voor de ontvangst.

### <a name="example-scenario"></a>Voorbeeldscenario

Een gebruiker ontvangt een inkooporder die 10 eenheden van streepjescode 5657900266 bevat. De gebruiker kan die streepjescode 10 keer scannen om het veld **Nu ontvangen** met één eenheid per scan bij te werken. Wanneer de gebruiker de scans heeft voltooid, wordt in het veld **Nu ontvangen** voor de regel van het artikel aangegeven dat er een hoeveelheid van 10 is ontvangen.

In een scenario waarbij de artikelhoeveelheid groot is, kan de gebruiker de hoeveelheid handmatig invoeren in plaats van de streepjescode voor elk ontvangen artikel te scannen. In dat geval kan de gebruiker de streepjescode één keer scannen om het artikel aan de lijst **Nu ontvangen** toe te voegen. De gebruiker kan vervolgens de bijbehorende regel selecteren in de weergave **Nu ontvangen** en vervolgens in het **detailvenster** dat aan de rechterkant van de pagina wordt weergegeven het veld **Ontvangsthoeveelheid** voor het artikel bijwerken.

Hoewel de weergave **Nu ontvangen** is geoptimaliseerd voor het scannen van streepjescodes, kunnen gebruikers ook **Product ontvangen** op de appbalk selecteren en vervolgens de artikel-id of streepjescodegegevens invoeren via een dialoogvenster. Nadat het ingevoerde artikel is gevalideerd, wordt de gebruiker gevraagd de ontvangsthoeveelheid in te voeren.

De weergave **Nu ontvangen** biedt gebruikers een gerichte manier om te zien welke producten zij ontvangen. U kunt ook de weergave **Volledige orderlijst** gebruiken. Deze weergave toont de volledige lijst met documentregels voor het geselecteerde inkooporder- of transferorderdocument. Gebruikers kunnen handmatig regels selecteren in de lijst en vervolgens in het **detailvenster** het veld **Ontvangsthoeveelheid** voor de geselecteerde regel bijwerken. In de weergave **Volledige orderlijst** kunnen gebruikers streepjescodes scannen of de functie **Product ontvangen** gebruiken om de artikel-id of streepjescode en gegevens over de ontvangen hoeveelheid in te voeren, zonder eerst de overeenkomende artikelregel in de lijst te hoeven selecteren.

### <a name="over-receiving-validations"></a>Validaties van meerontvangsten

Tijdens het ontvangstproces voor de documentregels worden validaties uitgevoerd. Deze omvatten validaties voor meerlevering. Als een gebruiker meer voorraad probeert te ontvangen dan via een inkooporder is besteld, maar de meerlevering niet is geconfigureerd of de ontvangen hoeveelheid hoger is dan de tolerantie voor meerlevering die is geconfigureerd voor de inkooporderregel, ontvangt de gebruiker een fout en kan hij of zij de extra hoeveelheid niet ontvangen.

Meerontvangst is niet toegestaan voor transferorderdocumenten. Gebruikers ontvangen altijd fouten als ze meer proberen te ontvangen dan voor de transferorderregel is verzonden.

### <a name="close-purchase-order-lines"></a>Inkooporderregels sluiten

U kunt de resterende hoeveelheid op een inkomende inkooporder tijdens het ontvangstproces sluiten als de vervoerder heeft bevestigd dat deze niet de volledige gevraagde hoeveelheid kan verzenden. Hiertoe moet het bedrijf zo zijn geconfigureerd dat de minderlevering van inkooporders is toegestaan. Daarnaast moet een tolerantiepercentage voor minderlevering worden gedefinieerd voor de inkooporderregel.

Ga naar **Inkoopbeheer** > **Instellen** > **Parameters voor Inkoopbeheer** om het bedrijf te configureren voor het toestaan van minderlevering van inkooporders in Commerce Headquarters . Schakel op het tabblad **Levering** de parameter **Minderlevering accepteren** in. Voer vervolgens distributieplanningstaak **1070** (**Kanaalconfiguratie**) uit om de instellingswijzigingen toe te passen op kanalen.

Tolerantiepercentages voor minderlevering voor een inkoopregel kunnen vooraf worden gedefinieerd voor producten als onderdeel van de productconfiguraties in Commerce Headquarters. U kunt ze ook instellen of overschrijven op een specifieke inkoopregel in Commerce Headquarters.

Nadat een organisatie de configuraties voor minderlevering van inkooporders heeft voltooid, zien POS-gebruikers een nieuwe optie **Resterende hoeveelheid sluiten** in het deelvenster **Details** wanneer ze een binnenkomende inkooporderregel selecteren in de bewerking **Binnenkomende voorraadbewerking**. Als de gebruiker de resterende hoeveelheid sluit, voert POS een validatie uit om te controleren of de hoeveelheid die wordt gesloten binnen het tolerantiepercentage voor minderlevering valt dat is gedefinieerd voor de inkooporderregel. Als de tolerantie voor minderleveringen wordt overschreden, wordt een foutbericht weergegeven en kan de gebruiker de resterende hoeveelheid niet sluiten totdat de eerder ontvangen hoeveelheid plus de hoeveelheid **Nu ontvangen** gelijk is aan of hoger is dan de minimale hoeveelheid die moet worden ontvangen, op basis van het tolerantiepercentage voor minderlevering. 

Met de optie **Resterende hoeveelheid sluiten** ingeschakeld voor een inkooporderregel, wanneer de gebruiker de ontvangst voltooit via de actie **Ontvangst voltooien**, wordt er ook een sluitingsverzoek verzonden naar Commerce Headquarters en worden eventuele niet ontvangen hoeveelheden van deze orderregel geannuleerd. Op dat moment wordt de regel als volledig ontvangen beschouwd. 

### <a name="receiving-location-controlled-items"></a>Op locatie gecontroleerde artikelen ontvangen

Als de artikelen die worden ontvangen op locatie worden gecontroleerd, kunnen gebruikers de locatie selecteren waar zij de artiekelen willen ontvangen tijdens het ontvangstproces. We raden u aan een standaardlocatie voor ontvangst voor uw winkelmagazijn te configureren om dit proces efficiënter te laten uitvoeren. Zelfs als een standaardlocatie is geconfigureerd, kunnen gebruikers de ontvangstlocatie op geselecteerde regels negeren als dat nodig is.

De bewerking houdt rekening met de configuratie **Lege ontvangst is toegestaan** in de opslagdimensie **Locatie** en vereist niet dat er een locatiedimensie wordt ingevoerd als lege ontvangst is geconfigureerd. Als lege ontvangstlocaties niet zijn toegestaan voor een artikel, wordt in de POS-toepassing een fout weergegeven en moet een locatie worden ingevoerd voordat de ontvangst kan worden geboekt.

### <a name="receive-all"></a>Alles ontvangen

U kunt zo nodig **Alles ontvangen** selecteren op de appbalk om snel de hoeveelheid voor **Nu ontvangen** bij te werken voor alle documentregels naar de maximumwaarde die beschikbaar is voor het ontvangen van deze regels.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Ontvangst van ongeplande artikelen op inkooporders

In Commerce versie 10.0.14 en hoger kunnen gebruikers een product ontvangen dat oorspronkelijk niet op de inkooporder stond. Als u deze functie wilt inschakelen, schakelt u **Regels aan inkooporder toevoegen tijdens POS-ontvangst**.  

Deze functie werkt alleen voor de ontvangst van inkooporders. Het is niet mogelijk om artikelen te ontvangen op overboekingsorders wanneer de artikelen niet eerder zijn besteld en verzonden vanuit het uitgaande magazijn.

Gebruikers kunnen geen nieuwe producten aan een inkooporder toevoegen tijdens POS-ontvangst als de [werkstroom voor wijzigingsbeheer](https://docs.microsoft.com/dynamics365/supply-chain/procurement/purchase-order-approval-confirmation) van inkooporders is ingeschakeld in Commerce Headquarters (HQ). Als u wijzigingsbeheer wilt inschakelen, moeten alle wijzigingen in een inkooporder eerst worden goedgekeurd voordat ontvangst wordt toegestaan. Aangezien een ontvanger door dit proces nieuwe regels aan de inkooporder kan toevoegen, mislukt de ontvangst als de werkstroom voor wijzigingsbeheer is ingeschakeld. Als wijzigingsbeheer is ingeschakeld voor alle inkooporders of voor de leverancier die is gekoppeld aan de inkooporder die actief is in POS, kan de gebruiker geen nieuwe producten aan de inkooporder toevoegen tijdens POS-ontvangst.

De functionaliteit waarmee het toevoegen van regels is ingeschakeld, kan niet worden gebruikt als tijdelijke oplossing voor het ontvangen van extra hoeveelheden producten die al op de inkooporder staan. Meerontvangsten worden beheerd via de standaardinstellingen voor [meerontvangsten](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation#over-receiving-validations) voor de productregel op de inkooporder.

Als **Regels aan inkooporder toevoegen tijdens POS-ontvangst** is ingeschakeld en een gebruiker ontvangt met de **Inkomende bewerking** in POS, dan ontvangt de gebruiker een bericht over het toevoegen van het artikel aan de inkooporder wanneer hij of zij de streepjescode scant of het productnummer invoert van een product dat niet wordt herkend als een artikel op de huidige inkooporder, maar wel wordt herkend als een geldig artikel. Als de gebruiker het artikel toevoegt aan de inkooporder, wordt de hoeveelheid die is ingevoerd in **Nu ontvangen** beschouwd als de bestelde hoeveelheid voor de inkooporderregel.

Wanneer het ontvangstbewijs van de inkooporder is voltooid en bij HQ is ingediend voor verwerking, worden de toegevoegde regels in het hoofddocument van de inkooporder gemaakt. Aan de inkooporderregel in HQ wordt de markering **Toegevoegd via POS** toegevoegd op het tabblad **Algemeen** van de inkooporderregel. De markering **Toegevoegd via POS** geeft aan dat de inkooporderregel is toegevoegd via het POS-ontvangstproces en dat vóór de ontvangst geen regel op de inkooporder was.

### <a name="cancel-receiving"></a>Ontvangst annuleren

Gebruik de functie **Ontvangst annuleren** op de appbalk alleen als u het document wilt verlaten en geen wijzigingen wilt opslaan. Bijvoorbeeld wanneer u in eerste instantie het verkeerde document hebt geselecteerd en geen van de vorige ontvangstgegevens wilt opslaan.

### <a name="pause-receiving"></a>Ontvangst onderbreken

Als u voorraad ontvangt, kunt u de functie **Ontvangst onderbreken** gebruiken als u het ontvangstproces tijdelijk wilt onderbreken. Mogelijk wilt u bijvoorbeeld een andere bewerking gaan uitvoeren vanaf het POS, zoals het bellen naar een klant of het vertragen van de boeking van de ontvangst.

Wanneer u **Ontvangst onderbreken** selecteert, wordt de status van het document gewijzigd in **Onderbroken**. Gebruikers weten dan dat er gegevens voor het document zijn ingevoerd, maar dat het document nog niet is doorgevoerd. Wanneer u klaar bent om het ontvangstproces te hervatten, selecteert u het onderbroken document en selecteert u vervolgens **Orderdetails**. Alle hoeveelheden voor **Nu ontvangen** die eerder zijn opgeslagen, blijven behouden en kunnen worden bekeken in de weergave **Volledige orderlijst**.

### <a name="review"></a>Controleren

Vóór de definitieve verbintenis van de ontvangst naar Commerce Headquarters (HQ) kunt u de functie Controleren gebruiken om het inkomende document te valideren. Met deze functie wordt u gewaarschuwd voor mogelijk ontbrekende of onjuiste gegevens die een verwerkingsfout kunnen veroorzaken en krijgt u de kans om problemen op te lossen voordat u het ontvangstverzoek indient. Als u de functie **Controleren** wilt inschakelen op de app-balk, schakelt u de functie **Validatie inschakelen voor inkomende en uitgaande POS-voorraadbewerkingen** in via het werkgebied **Functiebeheer** in Commerce Headquarters (HQ).

Met de functie **Controleren** worden de volgende problemen in een inkomend document gevalideerd:

- **Over-ontvangst**: de Nu ontvangen-hoeveelheid is groter dan de bestelde hoeveelheid. De ernst van dit probleem wordt bepaald door de meerleveringconfiguratie in Commerce Headquarters (HQ).
- **Onder-ontvangst**: de Nu ontvangen-hoeveelheid is kleiner dan de bestelde hoeveelheid. De ernst van dit probleem wordt bepaald door de onderleveringconfiguratie in Commerce Headquarters (HQ).
- **Serienummer**: het serienummer is niet opgegeven of gevalideerd voor een geserialiseerd artikel waarvoor een serienummer moet worden geregistreerd in de voorraad.
- **Locatie niet ingesteld**: de locatie is niet opgegeven voor een artikel dat door locatie wordt beheerd, waarbij de locatie niet leeg mag zijn.
- **Verwijderde regels**: de order heeft regels die zijn verwijderd door een Commerce Headquarters (HQ)-gebruiker die niet bekend is bij de POS-toepassing.

Stel de parameter **Automatische validatie inschakelen** in op **Ja** in **Commerce-parameters** > **Voorraad** > **Winkelvoorraad** om de validatie automatisch te laten uitvoeren wanneer u de functie **Ontvangst voltooien** selecteert.

### <a name="finish-receiving"></a>Ontvangst beëindigen

Wanneer u alle hoeveelheden voor **Nu ontvangen** voor producten hebt ingevoerd, moet u **Ontvangst voltooien** selecteren op de appbalk.

Wanneer gebruikers een inkooporderontvangst voltooien, wordt er gevraagd om een waarde op te geven in het veld **Ontvangstbewijsnummer** als deze functionaliteit is geconfigureerd. Meestal is deze waarde gelijk aan de identificatie van de pakbon van de leverancier. De gegevens bij **Ontvangstbewijsnummer** worden opgeslagen in het productontvangstbonjournaal in Commerce Headquarters. Er worden geen ontvangstbewijsnummers vastgelegd voor transferorderontvangsten.

Bij het gebruik van asynchrone documentverwerking wordt de ontvangst ingediend via een asynchroon documentraamwerk. De tijd die nodig is om het document te boeken, is afhankelijk van de grootte van het document (het aantal regels) en het algemene verwerkingsverkeer dat op de server plaatsvindt. Dit proces neemt doorgaans slechts enkele seconden in beslag. Als het boeken van documenten mislukt, wordt de gebruiker hiervan op de hoogte gesteld via de documentlijst **Inkomende bewerking** op het tabblad Actief, waarbij de documentstatus wordt bijgewerkt naar **Verwerking mislukt**. De gebruiker kan vervolgens het mislukte document in POS selecteren om de foutmeldingen en de reden voor de fout te bekijken in het **detailvenster**. Een mislukt document blijft niet-geboekt en de gebruiker moet teruggaan naar de documentregels door **Orderdetails** te selecteren in POS. De gebruiker moet het document vervolgens bijwerken met correcties op basis van de fouten. Nadat een document is gecorrigeerd, kan de gebruiker het opnieuw proberen te verwerken door **Afhandeling voltooien** te selecteren op de appbalk.

## <a name="create-an-inbound-transfer-order"></a>Een inkomende transferorder maken

Gebruikers kunnen vanuit POS nieuwe transferorderdocumenten maken. U kunt het proces starten door **Nieuw** te selecteren op de appbalk terwijl u zich in de hoofddocumentlijst **Inkomende bewerking** bevindt. U wordt vervolgens gevraagd een magazijn of winkel te selecteren bij **Verplaatsen van** vanwaaruit de voorraad zal worden geleverd aan uw winkellocatie. De waarden zijn beperkt tot de selectie die is gedefinieerd in de configuratie van de afhandelingsgroep van de winkel. In een inkomende transferaanvraag is uw huidige winkel altijd het magazijn bij **Verplaatsen naar** voor de transferorder. Die waarde kan niet worden gewijzigd.

U kunt naar behoefte waarden invoeren in de velden **Verzenddatum**, **Ontvangstdatum** en **Leveringsmethode**. U kunt ook een notitie toevoegen die samen met de koptekst van de transferorder wordt opgeslagen als bijlage bij het document in Commerce Headquarters.

Nadat de kopregelgegevens zijn gemaakt, kunt u producten toevoegen aan de transferorder. Als u het toevoegen van artikelen en aangevraagde hoeveelheden wilt starten, selecteert u **Product toevoegen**. In het **detailvenster** kunt u ook een regelspecifieke notitie aan de journaalregels toevoegen. Deze notities worden opgeslagen als een regelbijlage.

Nadat regels in de inkomende transferorder zijn ingevoerd, moet u **Opslaan** selecteren om de wijzigingen in het document lokaal op te slaan of **Aanvraag indienen** om de orderdetails in te dienen bij Commerce Headquarters voor verdere verwerking. Als u **Opslaan** selecteert, wordt het conceptdocument opgeslagen in de kanaaldatabase en kan het uitgaande magazijn het document pas uitvoeren nadat het via **Aanvraag indienen** is verwerkt. Selecteer **Opslaan** alleen als u de aanvraag voor verwerking in Commerce Headquarters nog niet wilt doorvoeren.

Als een document lokaal wordt opgeslagen, kunt u het vinden op het tabblad **Concepten** van de documentlijst **Inkomende bewerking**. Hoewel een document de status **Concept** heeft, kunt u het bewerken door **Bewerken** te selecteren. U kunt regels bijwerken, toevoegen of verwijderen als dat nodig is. U kunt ook het hele document verwijderen terwijl het de status **Concept** heeft door **Verwijderen** te selecteren op het tabblad **Concepten**.

Nadat het conceptdocument is ingediend bij Commerce Headquarters, wordt het weergegeven op het tabblad **Actief** en heeft het de status **Aangevraagd**. Op dit punt kan het aangevraagde inkomende transferorderdocument niet meer worden bewerkt door gebruikers in de inkomende winkel of het inkomende magazijn. Alleen gebruikers in het uitgaande magazijn kunnen het document bewerken door **Uitgaande bewerking** te selecteren in de POS-toepassing. De bewerkingsvergrendeling zorgt ervoor dat er geen conflicten optreden omdat een inkomende aanvrager de transferorder wijzigt op het moment dat de uitgaande verzender bezig is en met het verzamelen en verzenden van de order. Als er wijzigingen vereist zijn vanuit de inkomende winkel of het inkomende magazijn nadat de transferorder is ingediend, moet contact met de uitgaande vervoerder worden opgenomen en moet worden gevraagd de wijzigingen in te voeren.

Nadat het document de status **Aangevraagd** heeft gekregen, wordt het weergegeven op het tabblad **Actief**. Het kan echter nog niet worden ontvangen door de inkomende winkel of het inkomende magazijn. Nadat het uitgaande magazijn de transferorder geheel of gedeeltelijk heeft verzonden, kan de inkomende winkel of het inkomende magazijn ontvangsten in POS boeken. Wanneer de transferorderdocumenten worden verwerkt door de uitgaande zijde, wordt hun status bijgewerkt van **Aangevraagd** naar **Verzonden** of **Gedeeltelijk verzonden**. Nadat de documenten de status **Verzonden** of **Gedeeltelijk verzonden** hebben gekregen, kan de inkomende winkel of het inkomende magazijn ontvangsten met deze documenten boeken door middel van het ontvangstproces voor inkomende bewerking.

## <a name="related-topics"></a>Verwante onderwerpen

[Uitgaande voorraadbewerking in POS](pos-outbound-inventory-operation.md)
