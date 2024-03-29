---
title: Uitgaande voorraadbewerking in POS
description: In dit artikel worden de mogelijkheden van uitgaande voorraadbewerking van het verkooppunt (POS) beschreven.
author: hhainesms
ms.date: 07/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: dfef19b19c3fb1abd5078cacfeeaaabafcf162f9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272763"
---
# <a name="outbound-inventory-operation-in-pos"></a>Uitgaande voorraadbewerking in POS

[!include [banner](includes/banner.md)]


In Microsoft Dynamics 365 Commerce versie 10.0.10 en hoger worden inkomende en uitgaande bewerkingen op het verkooppunt (POS) vervangen door de bewerking voor orderverzameling en ontvangst.

> [!NOTE]
> In versie 10.0.10 en hoger worden alle nieuwe functies in de POS-toepassing die verband houden met de ontvangst van winkelvoorraad op basis van inkooporders en overboekingsorders, toegevoegd aan de bewerking voor inkomende bewerkingen. Als u momenteel orderverzameling en ontvangst in POS gebruikt, kunt u het beste een strategie ontwikkelen voor het overbrengen van deze bewerking naar de nieuwe inkomende en uitgaande bewerkingen. Hoewel de orderverzamelings- en ontvangstbewerking niet uit het product wordt verwijderd, vinden er geen verdere investeringen in die bewerking plaats, vanuit functioneel of prestatieperspectief, na versie 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Vereiste: een asynchroon documentraamwerk configureren

De uitgaande bewerking omvat prestatieverbeteringen om ervoor te zorgen dat gebruikers met grote hoeveelheden ontvangstboekingen in een groot aantal winkels of bedrijven en grote voorraaddocumenten deze documenten kunnen verwerken naar Commerce Headquarters (HQ) zonder dat er time-outs of storingen optreden. Deze verbeteringen vereisen het gebruik van een asynchroon documentraamwerk.

Wanneer een asynchroon documentraamwerk wordt gebruikt, kunt u wijzigingen in uitgaande documenten doorvoeren vanuit POS naar Commerce Headquarters (HQ) en vervolgens naar andere taken gaan terwijl de verwerking naar Commerce Headquarters (HQ) op de achtergrond plaatsvindt. U kunt de status van het document controleren via de documentlijstpagina **Uitgaande bewerking** in POS om er zeker van te zijn dat de boeking is geslaagd. In de POS-toepassing kunt u ook de lijst met actieve documenten voor uitgaande bewerking gebruiken om documenten weer te geven die niet naar Commerce Headquarters (HQ) konden worden geboekt. Als de verwerking van een document mislukt, kunnen POS-gebruikers hierin correcties aanbrengen en het document vervolgens opnieuw proberen te verwerken naar Commerce Headquarters (HQ).

> [!IMPORTANT]
> Het asynchrone documentraamwerk moet worden geconfigureerd voordat een bedrijf de uitgaande bewerking in POS probeert te gebruiken.

Voer de volgende procedures uit om een asynchroon documentraamwerk te configureren.

### <a name="create-and-configure-a-number-sequence"></a>Een nummerreeks maken en configureren

1. Ga naar **Organisatiebeheer \> Nummerreeksen \> Nummerreeksen**.
2. Maak op de pagina **Nummerreeksen** een nummerreeks.
3. Voer in de velden **Nummerreekscode** en **Naam** door de gebruiker gedefinieerde waarden in.
4. Selecteer op het sneltabblad **Verwijzingen** de optie **Toevoegen**.
5. Selecteer in het veld **Gebied** de optie **Commerce-parameters**.
6. Selecteer in het veld **Verwijzing** de optie **Bewerkings-id van detailhandeldocument**.
7. Stel op het sneltabblad **Algemeen** in de sectie **Instellen** de optie **Continu** in op **Nee** om er zeker van te zijn dat er geen prestatieproblemen optreden.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Twee batchtaken maken en plannen voor de taken voor documentverwerking en -controle

> [!NOTE]
> In Commerce versie 10.0.13 en hoger hoeft u de batchtaken niet via het raamwerk van de batchtaak te configureren. De batchprocessen kunnen worden geconfigureerd vanuit het menu **Detailhandel en commerce > IT detailhandel en commerce**. Gebruik de menuopties **Controle bewerking detailhandelsdocument** en **Verwerking bewerking detailhandelsdocument** om de batchtaken te configureren

De batchtaken die u maakt, worden gebruikt voor het verwerken van documenten die zijn mislukt of waarvoor een time-out is opgetreden. Ze worden ook gebruikt wanneer het aantal actieve voorraaddocumenten dat vanuit POS wordt verwerkt, groter is dan een door het systeem geconfigureerde waarde.

1. Ga naar **Systeembeheer \> Query's \> Batchtaken**.
2. Maak op de pagina **Batchtaak** twee batchtaken:

    - Configureer de ene taak om de klasse **RetaildocumentOperationMonitorBatch** uit te voeren.
    - Configureer de andere taak om de klasse **RetailDocumentOperationProcessingBatch** uit te voeren.

3. Plan de nieuwe batchtaken plannen zodanig dat deze op periodieke basis worden uitgevoerd. Zo kunt u de planning bijvoorbeeld zo instellen dat de taken om de vijf minuten worden uitgevoerd.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Vereiste: Uitgaande bewerking toevoegen aan de POS-schermindeling

Voordat uw organisatie de functionaliteit voor uitgaande bewerkingen kan gebruiken, moet deze de POS-bewerking **Uitgaande bewerking** configureren op een of meer van uw [POS-schermindelingen](/dynamics365/unified-operations/retail/pos-screen-layouts). Voordat u de nieuwe bewerking in een productieomgeving implementeert, moet u ervoor zorgen dat u deze grondig test en de gebruikers traint in het gebruik hiervan.

## <a name="overview"></a>Overzicht

Met de uitgaande bewerking kunnen POS-gebruikers de volgende taken uitvoeren:

- Zendingen voor overboekingsorderdocumenten boeken in gevallen waarin de winkel van de gebruiker het aangewezen uitgaande magazijn is.
- Informatie weergeven over historische overboekingsorderzendingen die zijn geboekt door de winkel.
- Nieuwe aanvragen voor uitgaande overboekingsorders maken.

Wanneer de uitgaande bewerking vanuit de POS-toepassing wordt gestart, wordt er een lijstpaginaweergave getoond. In deze weergave worden openstaande overboekingsorderdocumenten weergegeven met voorraadregels die de huidige winkel van de gebruiker moet verzenden en vervullen. Als gebruikers een document willen zoeken om te selecteren, kunnen zij door de lijst bladeren of de zoekfunctie gebruiken.

De lijst met uitgaande voorraaddocumenten bestaat uit drie tabbladen.

- **Actief**: dit tabblad bevat overboekingsorders met de status **Aangevraagd** of **Gedeeltelijk verzonden**. De orders bevatten regels of hoeveelheden op regels die moeten worden verzonden door de huidige winkel van de gebruiker. Op dit tabblad worden ook orders weergegeven met de status **Verwerkt in HQ** (dat wil zeggen dat er wordt gewacht op bevestiging van een geslaagde boeking vanuit Commerce Headquarters (HQ)) of **Verwerking mislukt** (dat wil zeggen dat de boeking naar Commerce Headquarters (HQ) niet is geslaagd en dat de gebruiker gegevens moet corrigeren en de orders opnieuw moet indienen).
- **Concept**: dit tabblad toont nieuwe aanvragen voor uitgaande overboekingsorders die door de winkel van de gebruiker zijn gemaakt. De documenten zijn echter alleen lokaal opgeslagen. Ze zijn nog niet ingediend bij Commerce Headquarters (HQ) voor verwerking.
- **Voltooid**: op dit tabblad wordt een lijst weergegeven met overboekingsorderdocumenten die de winkel volledig heeft verzonden in de afgelopen zeven dagen. Dit tabblad is alleen bedoeld voor informatieve doeleinden. Alle gegevens over de documenten zijn alleen-lezen gegevens voor de winkel.

Wanneer u documenten op een van de tabbladen bekijkt, kan het veld **Status** helpen beter inzicht te krijgen in de fase waarin het document zich bevindt.

- **Concept**: het overboekingsorderdocument is alleen lokaal opgeslagen in de kanaaldatabase van de winkel. Er is nog geen informatie over de aanvraag voor de overboekingsorder ingediend bij Commerce Headquarters (HQ).
- **Aangevraagd**: de inkooporder of overboekingsorder is gemaakt in Commerce Headquarters (HQ) en is volledig open. De huidige winkel van de gebruiker heeft nog geen verzendingen verwerkt in het document.
- **Gedeeltelijk verzonden**: het overboekingsorderdocument bevat een of meer regels of gedeeltelijke regelhoeveelheden die zijn geboekt als verzonden door het uitgaande magazijn. Deze verzonden regels kunnen via de inkomende bewerking worden ontvangen.
- **Volledig verzonden**: de overboekingsorder heeft alle regels en volledige regelhoeveelheden geboekt als verzonden door het uitgaande magazijn.
- **In uitvoering**: deze status wordt gebruikt om gebruikers van het apparaat te informeren dat een andere gebruiker actief werkt aan het document.
- **Onderbroken**: deze status wordt weergegeven nadat de optie **Ontvangen onderbreken** is geselecteerd om het ontvangstproces tijdelijk te stoppen.
- **Verwerkt in HQ**: het document is vanuit de POS-toepassing ingediend bij Commerce Headquarters (HQ), maar het is nog niet geboekt naar Commerce Headquarters (HQ). Het document doorloopt het proces voor asynchrone documentboeking. Nadat het document is geboekt naar Commerce Headquarters (HQ), moet de status worden bijgewerkt naar **Volledig ontvangen** of **Gedeeltelijk ontvangen**.
- **Verwerking mislukt**: het document is geboekt naar Commerce Headquarters (HQ) en afgewezen. In het **detailvenster** wordt de reden voor de mislukte boeking weergegeven. Het document moet worden bewerkt om gegevensproblemen op te lossen en moet vervolgens opnieuw worden ingediend bij Commerce Headquarters (HQ) voor verwerking.

Wanneer u een documentregel in de lijst selecteert, wordt een **detailvenster** weergegeven. Dit deelvenster bevat aanvullende informatie over het document, zoals gegevens over zending en datum. Via een voortgangsbalk wordt aangegeven hoeveel artikelen nog moeten worden verwerkt. Als het document niet is verwerkt in Commerce Headquarters (HQ), worden in het **detailvenster** ook foutberichten weergegeven die betrekking hebben op de fout.

In de lijstpaginaweergave voor het document kunt u **Orderdetails** op de appbalk selecteren om de details van het document weer te geven. U kunt ook ontvangstverwerking activeren voor in aanmerking komende documentregels.

In de lijstpaginaweergave voor documenten kunt u ook een nieuwe uitgaande overboekingsorder voor een winkel maken.

## <a name="transfer-order-shipping-process"></a>Verzendproces voor overboekingsorders

Nadat u een overboekingsorderdocument hebt geselecteerd op het tabblad **Actief**, kunt u **Orderdetails** selecteren om het afhandelingsproces te starten. De weergave **Volledige orderlijst** wordt weergegeven. Op deze pagina worden alle documentregels weergegeven die het artikel bevatten. Het bevat ook details van de bestelde hoeveelheid.

Bij elke scan van een streepjescode wordt de hoeveelheid in het veld **Nu verzonden** bijgewerkt met één eenheid. U kunt ook een verzendhoeveelheid invoeren door **Product verzenden** te selecteren op de appbalk, een artikel-id in te voeren en vervolgens de hoeveelheid in te voeren. Als het artikel op locatie wordt gecontroleerd, kunt u de verzendlocatie voor de documentregel bevestigen of instellen.

In de weergave **Volledige orderlijst** kunt u handmatig een regel selecteren in de lijst en vervolgens de hoeveelheid voor **Nu verzonden** bijwerken voor de geselecteerde regel in het **detailvenster**.

### <a name="over-delivery-shipping-validations"></a>Validaties van zendingen met meerlevering

Tijdens het afhandelingsproces voor de documentregels worden validaties uitgevoerd. Deze omvatten validaties voor meerlevering. Als een gebruiker meer voorraad probeert te verzenden dan op een transferorder is besteld, maar de meerlevering niet is geconfigureerd of de verzonden hoeveelheid hoger is dan de tolerantie voor meerlevering die is geconfigureerd voor de transferorderregel, krijgt de gebruiker een foutmelding en kan de gebruiker de extra hoeveelheid niet verzenden.

### <a name="underdelivery-close-lines"></a>Sluitregels voor minderlevering

In Commerce versie 10.0.12 is functionaliteit toegevoegd waarmee POS-gebruikers resterende hoeveelheden kunnen sluiten of annuleren tijdens de uitgaande orderverzending als het uitgaande magazijn vaststelt dat de volledige aangevraagde hoeveelheid niet kan worden verzonden. Hoeveelheden kunnen ook later worden gesloten of geannuleerd. Als u deze mogelijkheid wilt gebruiken, moet het bedrijf zo zijn geconfigureerd dat de minderlevering van overboekingsorders is toegestaan. Daarnaast moet een minderleveringspercentage worden gedefinieerd voor de overboekingsorderregel.

Ga naar **Voorraadbeheer \> Instellingen \> Parameters voor voorraad- en magazijnbeheer** om het bedrijf zo te configureren dat minderlevering van overboekingsorders in Commerce Headquarters (HQ) is toegestaan. Schakel op de pagina **Parameters voor voorraad- en magazijnbeheer** op het tabblad **overboekingsorders** de parameter **Minderlevering accepteren** in. Voer vervolgens taak **1070** van de distributieplanner uit om de parameterwijzigingen te synchroniseren met uw winkelkanaal.

Minderleveringspercentages voor een overboekingsorderregel kunnen vooraf worden gedefinieerd voor producten als onderdeel van de productconfiguratie in Commerce Headquarters. U kunt ze ook instellen of overschrijven op een specifieke overboekingsorderregel via commerce Headquarters (HQ).

Nadat een organisatie het configureren van de minderlevering van overboekingsorders heeft voltooid, zien POS-gebruikers een nieuwe optie **Resterende hoeveelheid sluiten** in het deelvenster **Details** wanneer ze een uitgaande overboekingsorderregel selecteren via de functie **Uitgaande bewerking**. Wanneer de gebruiker de zending voltooit door de bewerking **Afhandeling voltooien** te gebruiken, kan hij of zij een aanvraag naar Commerce Headquarters (HQ) verzenden om de resterende niet-verzonden hoeveelheid te annuleren. Als de gebruiker de resterende hoeveelheid sluit, voert Commerce een validatie uit om te controleren of de hoeveelheid die wordt geannuleerd binnen het minderleveringspercentage valt dat is gedefinieerd voor de overboekingsorderregel. Als de tolerantie voor minderleveringen wordt overschreden, wordt een foutbericht weergegeven en kan de gebruiker de resterende hoeveelheid niet sluiten totdat de hoeveelheid die eerder is verzonden en de hoeveelheid die nu wordt verzonden, overeenkomt met de tolerantie voor minderlevering.

Nadat de zending is gesynchroniseerd met Commerce Headquarters (HQ), worden de hoeveelheden die zijn gedefinieerd in het veld **Nu verzenden** voor de overboekingsorderregel in het POS bijgewerkt naar de status Verzonden in Commerce Headquarters (HQ). Alle niet-verzonden hoeveelheden die voorheen als hoeveelheden voor "resterend verzenden" zouden werden beschouwd (dat wil zeggen, hoeveelheden die later zullen worden verzonden), worden in plaats daarvan als geannuleerde hoeveelheden beschouwd. De hoeveelheid "resterend verzenden" voor de overboekingsorderregel wordt ingesteld op **0** (nul) en de regel wordt als volledig verzonden beschouwd.

### <a name="shipping-location-controlled-items"></a>Op locatie gecontroleerde artikelen verzenden

Als de artikelen die worden verzonden op locatie worden gecontroleerd, kunnen gebruikers kiezen vanaf welke locatie de voorraad moet worden uitgegeven tijdens het verzendproces. We raden u aan een standaardlocatie voor uitgifte voor uw winkelmagazijn te configureren om dit proces efficiënter te laten uitvoeren. Zelfs als een standaardlocatie is geconfigureerd, kunnen gebruikers de uitgiftelocatie op geselecteerde regels negeren als dat nodig is.

De bewerking houdt rekening met de configuratie **Lege ontvangst is toegestaan** in de opslagdimensie **Locatie** en vereist niet dat er een locatiedimensie wordt ingevoerd als lege ontvangst is geconfigureerd. Als lege ontvangstlocaties niet zijn toegestaan voor een artikel, wordt in de POS-toepassing een fout weergegeven en moet een locatie worden ingevoerd voordat de ontvangst kan worden geboekt.

### <a name="ship-all"></a>Alles verzenden

U kunt zo nodig **Alles verzenden** selecteren op de appbalk om snel de hoeveelheid voor **Nu verzonden** bij te werken voor alle documentregels naar de maximumwaarde die beschikbaar is voor het afhandelen van deze regels.

### <a name="cancel-fulfillment"></a>Uitvoering annuleren

Gebruik de functie **Afhandeling annuleren** op de appbalk alleen als u het document wilt verlaten en geen wijzigingen wilt opslaan. Bijvoorbeeld wanneer u in eerste instantie het verkeerde document hebt geselecteerd en geen van de vorige verzendgegevens wilt opslaan.

### <a name="pause-fulfillment"></a>Uitvoering onderbreken

Als u de overboekingsorder afhandelt, kunt u de functie **Afhandeling onderbreken** gebruiken als u het proces tijdelijk wilt onderbreken. Mogelijk wilt u bijvoorbeeld een andere bewerking gaan uitvoeren vanaf het POS, zoals het bellen naar een klant of het vertragen van de boeking van de verzending naar Commerce Headquarters (HQ).

Wanneer u **Afhandeling onderbreken** selecteert, wordt de status van het document gewijzigd in **Onderbroken**. De gebruiker weet dan dat er gegevens in het document zijn ingevoerd, maar dat het document nog niet is doorgevoerd. Wanneer u klaar bent om het afhandelingsproces te hervatten, selecteert u het onderbroken document en selecteert u vervolgens **Orderdetails**. Alle hoeveelheden voor **Nu verzonden** die eerder zijn opgeslagen, blijven behouden en kunnen worden bekeken in de weergave **Volledige orderlijst**.

### <a name="review"></a>Controleren

Vóór de definitieve verbintenis van de afhandeling naar Commerce Headquarters (HQ) kunt u de functie **Controleren** gebruiken om het uitgaande document te valideren. Met deze functie wordt u gewaarschuwd voor mogelijk ontbrekende of onjuiste gegevens die een verwerkingsfout kunnen veroorzaken en krijgt u de kans om problemen op te lossen voordat u het verzoek tot uitvoering indient. Als u de functie **Controleren** wilt inschakelen op de app-balk, schakelt u de functie **Validatie inschakelen voor inkomende en uitgaande POS-voorraadbewerkingen** in via Functiebeheer in Commerce Headquarters (HQ).

Met de functie **Controleren** worden de volgende problemen in een uitgaand document gevalideerd:
- **Over-verzen ding**: de Nu verzonden-hoeveelheid is groter dan de bestelde hoeveelheid. De ernst van dit probleem wordt bepaald door de meerleveringconfiguratie in Commerce Headquarters (HQ).
- **Onder-verzen ding**: de Nu verzonden-hoeveelheid is kleiner dan de bestelde hoeveelheid. De ernst van dit probleem wordt bepaald door de onderleveringconfiguratie in Commerce Headquarters (HQ).
- **Serienummer**: serienummer is niet opgegeven of niet beschikbaar voor een geserialiseerd artikel waarvoor een serienummer moet worden geregistreerd in de voorraad.
- **Locatie niet ingesteld**: locatie is niet opgegeven voor een artikel dat door locatie wordt beheerd, waarbij de locatie niet leeg mag zijn.
- **Verwijderde regels**: de order heeft regels die zijn verwijderd door een Commerce Headquarters (HQ)-gebruiker die niet bekend is bij de POS-toepassing.

Als u de parameter **Automatische validatie** op **Ja** instelt in **Commerce parameters** > **Voorraad** > **Winkelvoorraadbewerkingen**, wordt de validatie automatisch uitgevoerd wanneer u de functie **Uitvoering voltooien** selecteert.

### <a name="finish-fulfillment"></a>Uitvoering voltooien

Wanneer u alle hoeveelheden voor **Nu verzonden** voor producten hebt ingevoerd, moet u **Afhandeling voltooien** selecteren op de appbalk.

Bij het gebruik van asynchrone documentverwerking wordt de ontvangst ingediend via een asynchroon documentraamwerk. De tijd die nodig is om het document te boeken, is afhankelijk van de grootte van het document (het aantal regels) en het algemene verwerkingsverkeer dat op de server plaatsvindt. Dit proces neemt doorgaans slechts enkele seconden in beslag. Als het boeken van documenten mislukt, wordt de gebruiker hiervan op de hoogte gesteld via de documentlijst **Uitgaande bewerking** op het tabblad **Actief**, waarbij de documentstatus wordt bijgewerkt naar **Verwerking mislukt**. De gebruiker kan vervolgens het mislukte document in POS selecteren om de foutmeldingen en de reden voor de fout te bekijken in het **detailvenster**. Een mislukt document blijft niet-geboekt en de gebruiker moet teruggaan naar de documentregels door **Orderdetails** te selecteren in POS. De gebruiker moet het document vervolgens bijwerken met correcties op basis van de fouten. Nadat een document is gecorrigeerd, kan de gebruiker het opnieuw proberen te verwerken door **Afhandeling voltooien** te selecteren op de appbalk.

## <a name="create-an-outbound-transfer-order"></a>Een uitgaande overboekingsorder maken

Gebruikers kunnen vanuit POS nieuwe overboekingsorderdocumenten maken. U kunt het proces starten door **Nieuw** te selecteren op de appbalk terwijl u zich in de hoofddocumentlijst **Uitgaande bewerking** bevindt. U wordt vervolgens gevraagd een magazijn of winkel te selecteren bij **Verplaatsen naar** waaraan uw huidige winkel voorraad zal leveren. De waarden zijn beperkt tot de selectie die is gedefinieerd in de configuratie van de afhandelingsgroep van de winkel. In een uitgaande transferaanvraag is uw huidige winkel altijd het magazijn bij **Verplaatsen naar** voor de overboekingsorder. Die waarde kan niet worden gewijzigd.

U kunt naar behoefte waarden invoeren in de velden **Verzenddatum**, **Ontvangstdatum** en **Leveringsmethode**. U kunt ook een notitie toevoegen die samen met de koptekst van de overboekingsorder wordt opgeslagen als bijlage bij het document in Commerce Headquarters (HQ).

Nadat de kopregelgegevens zijn gemaakt, kunt u producten toevoegen aan de overboekingsorder. Als u het toevoegen van artikelen en aangevraagde hoeveelheden wilt starten, scant u streepjescodes of selecteert u **Product toevoegen**.

Nadat regels in de uitgaande overboekingsorder zijn ingevoerd, moet u **Opslaan** selecteren om de wijzigingen in het document lokaal op te slaan of **Aanvraag indienen** om de orderdetails in te dienen bij Commerce Headquarters (HQ) voor verdere verwerking. Als u **Opslaan** selecteert, wordt het conceptdocument opgeslagen in de kanaaldatabase en kan het uitgaande magazijn het document pas uitvoeren nadat het via **Aanvraag indienen** is verwerkt. Selecteer **Opslaan** alleen als u de aanvraag voor verwerking in Commerce Headquarters (HQ) nog niet wilt doorvoeren.

Als een document lokaal wordt opgeslagen, kunt u het vinden op het tabblad **Concepten** van de documentlijst **Inkomende bewerking**. Hoewel een document de status **Concept** heeft, kunt u het bewerken door **Bewerken** te selecteren. U kunt regels bijwerken, toevoegen of verwijderen als dat nodig is. U kunt ook het hele document verwijderen terwijl het de status **Concept** heeft door **Verwijderen** te selecteren op het tabblad **Concepten**.

Nadat het conceptdocument is ingediend bij Commerce Headquarters (HQ), wordt het weergegeven op het tabblad **Actief** en heeft het de status **Aangevraagd**. Op dat moment kunnen alleen gebruikers in het uitgaande magazijn het document bewerken door **Uitgaande bewerking** te selecteren in de POS-toepassing. Gebruikers in het inkomende magazijn kunnen de overboekingsorder weergeven op het tabblad **Actief** van de documentlijst **Inkomende bewerking**, maar ze kunnen deze niet bewerken of verwijderen. De bewerkingsvergrendeling zorgt ervoor dat er geen conflicten optreden omdat een inkomende aanvrager de overboekingsorder wijzigt op het moment dat de uitgaande verzender bezig is en met het verzamelen en verzenden van de order. Als er wijzigingen vereist zijn vanuit de inkomende winkel of het inkomende magazijn nadat de overboekingsorder is ingediend, moet contact met de uitgaande vervoerder worden opgenomen en moet worden gevraagd de wijzigingen in te voeren.

Nadat het document de status **Aangevraagd** heeft gekregen, is deze gereed voor afhandeling door het uitgaande magazijn. Wanneer de zending wordt verwerkt met behulp van de uitgaande bewerking, wordt de status van de overboekingsorderdocumenten bijgewerkt van **Aangevraagd** naar **Volledig verzonden** of **Gedeeltelijk verzonden**. Nadat de documenten de status **Volledig verzonden** of **Gedeeltelijk verzonden** hebben gekregen, kan de inkomende winkel of het inkomende magazijn ontvangsten met deze documenten boeken door middel van het ontvangstproces voor inkomende bewerking.

Volledig verzonden overboekingsorders worden naar het tabblad **Voltooid** van de documentlijst **Uitgaande bewerking** verplaatst. Hier blijven zij gedurende zeven dagen zichtbaar voor gebruikers in de uitgaande winkel of het uitgaande magazijn, in de alleen-lezen modus.

## <a name="related-articles"></a>Gerelateerde artikelen

[Inkomende voorraadbewerking in POS](pos-inbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
