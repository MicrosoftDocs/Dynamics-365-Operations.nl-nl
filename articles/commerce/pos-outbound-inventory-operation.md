---
title: Uitgaande voorraadbewerking in POS
description: In dit onderwerp worden de mogelijkheden van uitgaande voorraadbewerking van het verkooppunt (POS) beschreven.
author: hhaines
manager: annbe
ms.date: 02/11/2020
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
ms.openlocfilehash: c3e50d20162340c599fb6719ae6f45654dba990a
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071852"
---
# <a name="outbound-inventory-operation-in-pos"></a>Uitgaande voorraadbewerking in POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In Microsoft Dynamics 365 Commerce versie 10.0.10 en hoger worden inkomende en uitgaande bewerkingen op het verkooppunt (POS) vervangen door de bewerking voor orderverzameling en ontvangst.

> [!NOTE]
> In versie 10.0.10 en hoger worden alle nieuwe functies in de POS-toepassing die verband houden met de ontvangst van winkelvoorraad op basis van inkooporders en transferorders, toegevoegd aan de bewerking voor inkomende bewerkingen. Als u momenteel orderverzameling en ontvangst in POS gebruikt, kunt u het beste een strategie ontwikkelen voor het overbrengen van deze bewerking naar de nieuwe inkomende en uitgaande bewerkingen. Hoewel de orderverzamelings- en ontvangstbewerking niet uit het product wordt verwijderd, vinden er geen verdere investeringen in die bewerking plaats, vanuit functioneel of prestatieperspectief, na versie 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Vereiste: een asynchroon documentraamwerk configureren

De uitgaande bewerking omvat prestatieverbeteringen om ervoor te zorgen dat gebruikers met grote hoeveelheden ontvangstboekingen in een groot aantal winkels of bedrijven en grote voorraaddocumenten deze documenten kunnen verwerken naar Commerce Headquarters zonder dat er time-outs of storingen optreden. Deze verbeteringen vereisen het gebruik van een asynchroon documentraamwerk.

Wanneer een asynchroon documentraamwerk wordt gebruikt, kunt u wijzigingen in uitgaande documenten doorvoeren vanuit POS naar Commerce Headquarters en vervolgens naar andere taken gaan terwijl de verwerking naar Commerce Headquarters op de achtergrond plaatsvindt. U kunt de status van het document controleren via de documentlijstpagina **Uitgaande bewerking** in POS om er zeker van te zijn dat de boeking is geslaagd. In de POS-toepassing kunt u ook de lijst met actieve documenten voor uitgaande bewerking gebruiken om documenten weer te geven die niet naar Commerce Headquarters konden worden geboekt. Als de verwerking van een document mislukt, kunnen POS-gebruikers hierin correcties aanbrengen en het document vervolgens opnieuw proberen te verwerken naar Commerce Headquarters.

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

De batchtaken die u maakt, worden gebruikt voor het verwerken van documenten die zijn mislukt of waarvoor een time-out is opgetreden. Ze worden ook gebruikt wanneer het aantal actieve voorraaddocumenten dat vanuit POS wordt verwerkt, groter is dan een door het systeem geconfigureerde waarde.

1. Ga naar **Systeembeheer \> Query's \> Batchtaken**.
2. Maak op de pagina **Batchtaak** twee batchtaken:

    - Configureer de ene taak om de klasse **RetaildocumentOperationMonitorBatch** uit te voeren.
    - Configureer de andere taak om de klasse **RetailDocumentOperationProcessingBatch** uit te voeren.

3. Plan de nieuwe batchtaken plannen zodanig dat deze op periodieke basis worden uitgevoerd. Zo kunt u de planning bijvoorbeeld zo instellen dat de taken om de vijf minuten worden uitgevoerd.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Vereiste: Uitgaande bewerking toevoegen aan de POS-schermindeling

Voordat uw organisatie de functionaliteit voor uitgaande bewerkingen kan gebruiken, moet deze de POS-bewerking **Uitgaande bewerking** configureren op een of meer van uw [POS-schermindelingen](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Voordat u de nieuwe bewerking in een productieomgeving implementeert, moet u ervoor zorgen dat u deze grondig test en de gebruikers traint in het gebruik hiervan.

## <a name="overview"></a>Overzicht

Met de uitgaande bewerking kunnen POS-gebruikers de volgende taken uitvoeren:

- Zendingen voor transferorderdocumenten boeken in gevallen waarin de winkel van de gebruiker het aangewezen uitgaande magazijn is.
- Informatie weergeven over historische transferorderzendingen die zijn geboekt door de winkel.
- Nieuwe aanvragen voor uitgaande transferorders maken.

Wanneer de uitgaande bewerking vanuit de POS-toepassing wordt gestart, wordt er een lijstpaginaweergave getoond. In deze weergave worden openstaande transferorderdocumenten weergegeven met voorraadregels die de huidige winkel van de gebruiker moet verzenden en vervullen. Als gebruikers een document willen zoeken om te selecteren, kunnen zij door de lijst bladeren of de zoekfunctie gebruiken.

De lijst met uitgaande voorraaddocumenten bestaat uit drie tabbladen.

- **Actief**: dit tabblad bevat transferorders met de status **Aangevraagd** of **Gedeeltelijk verzonden**. De orders bevatten regels of hoeveelheden op regels die moeten worden verzonden door de huidige winkel van de gebruiker. Op dit tabblad worden ook orders weergegeven met de status **Verwerkt in HQ** (dat wil zeggen dat er wordt gewacht op bevestiging van een geslaagde boeking vanuit Commerce Headquarters) of **Verwerking mislukt** (dat wil zeggen dat de boeking naar Commerce Headquarters niet is geslaagd en dat de gebruiker gegevens moet corrigeren en de orders opnieuw moet indienen).
- **Concept**: dit tabblad toont nieuwe aanvragen voor uitgaande transferorders die door de winkel van de gebruiker zijn gemaakt. De documenten zijn echter alleen lokaal opgeslagen. Ze zijn nog niet ingediend bij Commerce Headquarters voor verwerking.
- **Voltooid**: op dit tabblad wordt een lijst weergegeven met transferorderdocumenten die de winkel volledig heeft verzonden in de afgelopen zeven dagen. Dit tabblad is alleen bedoeld voor informatieve doeleinden. Alle gegevens over de documenten zijn alleen-lezen gegevens voor de winkel.

Wanneer u documenten op een van de tabbladen bekijkt, kan het veld **Status** helpen beter inzicht te krijgen in de fase waarin het document zich bevindt.

- **Concept**: het transferorderdocument is alleen lokaal opgeslagen in de kanaaldatabase van de winkel. Er is nog geen informatie over de aanvraag voor de transferorder ingediend bij Commerce Headquarters.
- **Aangevraagd**: de inkooporder of transferorder is gemaakt in Commerce Headquarters en is volledig open. De huidige winkel van de gebruiker heeft nog geen verzendingen verwerkt in het document.
- **Gedeeltelijk verzonden**: het transferorderdocument bevat een of meer regels of gedeeltelijke regelhoeveelheden die zijn geboekt als verzonden door het uitgaande magazijn. Deze verzonden regels kunnen via de inkomende bewerking worden ontvangen.
- **Volledig verzonden**: de transferorder heeft alle regels en volledige regelhoeveelheden geboekt als verzonden door het uitgaande magazijn.
- **In uitvoering**: deze status wordt gebruikt om gebruikers van het apparaat te informeren dat een andere gebruiker actief werkt aan het document.
- **Onderbroken**: deze status wordt weergegeven nadat de optie **Ontvangen onderbreken** is geselecteerd om het ontvangstproces tijdelijk te stoppen.
- **Verwerkt in HQ**: het document is vanuit de POS-toepassing ingediend bij Commerce Headquarters, maar het is nog niet geboekt naar Commerce Headquarters. Het document doorloopt het proces voor asynchrone documentboeking. Nadat het document is geboekt naar Commerce Headquarters, moet de status worden bijgewerkt naar **Volledig ontvangen** of **Gedeeltelijk ontvangen**.
- **Verwerking mislukt**: het document is geboekt naar Commerce Headquarters en afgewezen. In het **detailvenster** wordt de reden voor de mislukte boeking weergegeven. Het document moet worden bewerkt om gegevensproblemen op te lossen en moet vervolgens opnieuw worden ingediend bij Commerce Headquarters voor verwerking.

Wanneer u een documentregel in de lijst selecteert, wordt een **detailvenster** weergegeven. Dit deelvenster bevat aanvullende informatie over het document, zoals gegevens over zending en datum. Via een voortgangsbalk wordt aangegeven hoeveel artikelen nog moeten worden verwerkt. Als het document niet is verwerkt in Commerce Headquarters, worden in het **detailvenster** ook foutberichten weergegeven die betrekking hebben op de fout.

In de lijstpaginaweergave voor het document kunt u **Orderdetails** op de appbalk selecteren om de details van het document weer te geven. U kunt ook ontvangstverwerking activeren voor in aanmerking komende documentregels.

In de lijstpaginaweergave voor documenten kunt u ook een nieuwe uitgaande transferorder voor een winkel maken.

## <a name="transfer-order-shipping-process"></a>Verzendproces voor transferorders

Nadat u een transferorderdocument hebt geselecteerd op het tabblad **Actief**, kunt u **Orderdetails** selecteren om het afhandelingsproces te starten. De weergave **Volledige orderlijst** wordt weergegeven. Op deze pagina worden alle documentregels weergegeven die het artikel bevatten. Het bevat ook details van de bestelde hoeveelheid.

Bij elke scan van een streepjescode wordt de hoeveelheid in het veld **Nu verzonden** bijgewerkt met één eenheid. U kunt ook een verzendhoeveelheid invoeren door **Product verzenden** te selecteren op de appbalk, een artikel-id in te voeren en vervolgens de hoeveelheid in te voeren. Als het artikel op locatie wordt gecontroleerd, kunt u de verzendlocatie voor de documentregel bevestigen of instellen.

In de weergave **Volledige orderlijst** kunt u handmatig een regel selecteren in de lijst en vervolgens de hoeveelheid voor **Nu verzonden** bijwerken voor de geselecteerde regel in het **detailvenster**.

### <a name="over-delivery-shipping-validations"></a>Validaties van zendingen met meerlevering

Tijdens het ontvangstproces voor de documentregels worden validaties uitgevoerd. Deze omvatten validaties voor meerlevering. Als een gebruiker meer voorraad probeert te ontvangen dan via een inkooporder is besteld, maar de meerlevering niet is geconfigureerd of de ontvangen hoeveelheid hoger is dan de tolerantie voor meerlevering die is geconfigureerd voor de inkooporderregel, ontvangt de gebruiker een fout en kan hij of zij de extra hoeveelheid niet ontvangen.

### <a name="shipping-location-controlled-items"></a>Op locatie gecontroleerde artikelen verzenden

Als de artikelen die worden verzonden op locatie worden gecontroleerd, kunnen gebruikers kiezen vanaf welke locatie de voorraad moet worden uitgegeven tijdens het verzendproces. We raden u aan een standaardlocatie voor uitgifte voor uw winkelmagazijn te configureren om dit proces efficiënter te laten uitvoeren. Zelfs als een standaardlocatie is geconfigureerd, kunnen gebruikers de uitgiftelocatie op geselecteerde regels negeren als dat nodig is.

De bewerking houdt rekening met de configuratie **Lege ontvangst is toegestaan** in de opslagdimensie **Locatie** en vereist niet dat er een locatiedimensie wordt ingevoerd als lege ontvangst is geconfigureerd. Als lege ontvangstlocaties niet zijn toegestaan voor een artikel, wordt in de POS-toepassing een fout weergegeven en moet een locatie worden ingevoerd voordat de ontvangst kan worden geboekt.

### <a name="ship-all"></a>Alles verzenden

U kunt zo nodig **Alles verzenden** selecteren op de appbalk om snel de hoeveelheid voor **Nu verzonden** bij te werken voor alle documentregels naar de maximumwaarde die beschikbaar is voor het afhandelen van deze regels.

### <a name="cancel-fulfillment"></a>Uitvoering annuleren

Gebruik de functie **Afhandeling annuleren** op de appbalk alleen als u het document wilt verlaten en geen wijzigingen wilt opslaan. Bijvoorbeeld wanneer u in eerste instantie het verkeerde document hebt geselecteerd en geen van de vorige verzendgegevens wilt opslaan.

### <a name="pause-fulfillment"></a>Uitvoering onderbreken

Als u de transferorder afhandelt, kunt u de functie **Afhandeling onderbreken** gebruiken als u het proces tijdelijk wilt onderbreken. Mogelijk wilt u bijvoorbeeld een andere bewerking gaan uitvoeren vanaf het POS, zoals het bellen naar een klant of het vertragen van de boeking van de verzending naar Commerce Headquarters.

Wanneer u **Afhandeling onderbreken** selecteert, wordt de status van het document gewijzigd in **Onderbroken**. De gebruiker weet dan dat er gegevens in het document zijn ingevoerd, maar dat het document nog niet is doorgevoerd. Wanneer u klaar bent om het afhandelingsproces te hervatten, selecteert u het onderbroken document en selecteert u vervolgens **Orderdetails**. Alle hoeveelheden voor **Nu verzonden** die eerder zijn opgeslagen, blijven behouden en kunnen worden bekeken in de weergave **Volledige orderlijst**.

### <a name="finish-fulfillment"></a>Uitvoering voltooien

Wanneer u alle hoeveelheden voor **Nu verzonden** voor producten hebt ingevoerd, moet u **Afhandeling voltooien** selecteren op de appbalk.

Bij het gebruik van asynchrone documentverwerking wordt de ontvangst ingediend via een asynchroon documentraamwerk. De tijd die nodig is om het document te boeken, is afhankelijk van de grootte van het document (het aantal regels) en het algemene verwerkingsverkeer dat op de server plaatsvindt. Dit proces neemt doorgaans slechts enkele seconden in beslag. Als het boeken van documenten mislukt, wordt de gebruiker hiervan op de hoogte gesteld via de documentlijst **Uitgaande bewerking** op het tabblad **Actief**, waarbij de documentstatus wordt bijgewerkt naar **Verwerking mislukt**. De gebruiker kan vervolgens het mislukte document in POS selecteren om de foutmeldingen en de reden voor de fout te bekijken in het **detailvenster**. Een mislukt document blijft niet-geboekt en de gebruiker moet teruggaan naar de documentregels door **Orderdetails** te selecteren in POS. De gebruiker moet het document vervolgens bijwerken met correcties op basis van de fouten. Nadat een document is gecorrigeerd, kan de gebruiker het opnieuw proberen te verwerken door **Afhandeling voltooien** te selecteren op de appbalk.

## <a name="create-an-outbound-transfer-order"></a>Een uitgaande transferorder maken

Gebruikers kunnen vanuit POS nieuwe transferorderdocumenten maken. U kunt het proces starten door **Nieuw** te selecteren op de appbalk terwijl u zich in de hoofddocumentlijst **Uitgaande bewerking** bevindt. U wordt vervolgens gevraagd een magazijn of winkel te selecteren bij **Verplaatsen naar** waaraan uw huidige winkel voorraad zal leveren. De waarden zijn beperkt tot de selectie die is gedefinieerd in de configuratie van de afhandelingsgroep van de winkel. In een uitgaande transferaanvraag is uw huidige winkel altijd het magazijn bij **Verplaatsen naar** voor de transferorder. Die waarde kan niet worden gewijzigd.

U kunt naar behoefte waarden invoeren in de velden **Verzenddatum**, **Ontvangstdatum** en **Leveringsmethode**. U kunt ook een notitie toevoegen die samen met de koptekst van de transferorder wordt opgeslagen als bijlage bij het document in Commerce Headquarters.

Nadat de kopregelgegevens zijn gemaakt, kunt u producten toevoegen aan de transferorder. Als u het toevoegen van artikelen en aangevraagde hoeveelheden wilt starten, scant u streepjescodes of selecteert u **Product toevoegen**.

Nadat regels in de uitgaande transferorder zijn ingevoerd, moet u **Opslaan** selecteren om de wijzigingen in het document lokaal op te slaan of **Aanvraag indienen** om de orderdetails in te dienen bij Commerce Headquarters voor verdere verwerking. Als u **Opslaan** selecteert, wordt het conceptdocument opgeslagen in de kanaaldatabase en kan het uitgaande magazijn het document pas uitvoeren nadat het via **Aanvraag indienen** is verwerkt. Selecteer **Opslaan** alleen als u de aanvraag voor verwerking in Commerce Headquarters nog niet wilt doorvoeren.

Als een document lokaal wordt opgeslagen, kunt u het vinden op het tabblad **Concepten** van de documentlijst **Inkomende bewerking**. Hoewel een document de status **Concept** heeft, kunt u het bewerken door **Bewerken** te selecteren. U kunt regels bijwerken, toevoegen of verwijderen als dat nodig is. U kunt ook het hele document verwijderen terwijl het de status **Concept** heeft door **Verwijderen** te selecteren op het tabblad **Concepten**.

Nadat het conceptdocument is ingediend bij Commerce Headquarters, wordt het weergegeven op het tabblad **Actief** en heeft het de status **Aangevraagd**. Op dat moment kunnen alleen gebruikers in het uitgaande magazijn het document bewerken door **Uitgaande bewerking** te selecteren in de POS-toepassing. Gebruikers in het inkomende magazijn kunnen de transferorder weergeven op het tabblad **Actief** van de documentlijst **Inkomende bewerking**, maar ze kunnen deze niet bewerken of verwijderen. De bewerkingsvergrendeling zorgt ervoor dat er geen conflicten optreden omdat een inkomende aanvrager de transferorder wijzigt op het moment dat de uitgaande verzender bezig is en met het verzamelen en verzenden van de order. Als er wijzigingen vereist zijn vanuit de inkomende winkel of het inkomende magazijn nadat de transferorder is ingediend, moet contact met de uitgaande vervoerder worden opgenomen en moet worden gevraagd de wijzigingen in te voeren.

Nadat het document de status **Aangevraagd** heeft gekregen, is deze gereed voor afhandeling door het uitgaande magazijn. Wanneer de zending wordt verwerkt met behulp van de uitgaande bewerking, wordt de status van de transferorderdocumenten bijgewerkt van **Aangevraagd** naar **Volledig verzonden** of **Gedeeltelijk verzonden**. Nadat de documenten de status **Volledig verzonden** of **Gedeeltelijk verzonden** hebben gekregen, kan de inkomende winkel of het inkomende magazijn ontvangsten met deze documenten boeken door middel van het ontvangstproces voor inkomende bewerking.

Volledig verzonden transferorders worden naar het tabblad **Voltooid** van de documentlijst **Uitgaande bewerking** verplaatst. Hier blijven zij gedurende zeven dagen zichtbaar voor gebruikers in de uitgaande winkel of het uitgaande magazijn, in de alleen-lezen modus.

## <a name="related-topics"></a>Verwante onderwerpen

[Inkomende voorraadbewerking in POS](pos-inbound-inventory-operation.md)
