---
title: Interface voor materiaalverwerkingsapparatuur (MHAX)
description: In dit artikel wordt beschreven hoe u de interface voor materiaalverwerkingsapparatuur (Material Handling Equipment Interface, MHAX) in kunt stellen zodat u verbinding kunt maken met externe fysieke MH-systemen (Material Handling).
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dc46c9fea94c3d86f9511c2bea4ea64455c936f9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068354"
---
# <a name="material-handling-equipment-interface-mhax"></a>Interface voor materiaalverwerkingsapparatuur (MHAX)

[!include [banner](../../includes/banner.md)]

Met de *interface voor materiaalverwerkingsapparatuur* (MHAX) kunt u externe fysieke MH-systemen (Material Handling) koppelen aan een magazijn dat wordt beheerd door magazijnbeheerprocessen (WMS) in Microsoft Dynamics 365 Supply Chain Management. De interface tussen het WMS- en MH-systemen bestaat uit twee wachtrijen: een voor uitgaande gebeurtenissen (WMS naar MH) en een voor inkomende gebeurtenissen (MH naar WMS). Het WMS-systeem genereert uitgaande gebeurtenissen op basis van werkregels die zijn gemaakt tijdens verschillende processen voor het aanmaken en uitvoeren van werk. Het MH-systeem controleert vervolgens het WMS-systeem regelmatig op nieuwe gebeurtenissen en verwerkt de responsen. Nadat het MH-systeem de verwerking van de gebeurtenissen in overeenstemming met werkinstructies heeft voltooid, verstuurt het inkomende gebeurtenissen, zoals die voor de voltooiing van een werkregel of voor het verzamelen van een tekort aan artikelen voor een order.

In de volgende afbeelding ziet u de verschillende elementen en de volgorde waarin de processen plaatsvinden wanneer u MHAX-integratie gebruikt.

![MHAX-onderdelen en interacties.](media/mhax-components.png "MHAX-onderdelen en interacties")

Hier vindt u een uitleg van de interacties die in de vorige afbeelding worden weergegeven:

1. Tijdens het maken of uitvoeren van het werk worden uitgaande gebeurtenissen gemaakt in de uitgaande wachtrij.
2. De MH-apparatuur maakt verbinding met de MH-apparatuurservice, controleert of er nieuwe gebeurtenissen aanwezig zijn die relevant zijn voor de service en verwerkt deze gebeurtenissen.
3. Wanneer de MH-apparatuur gereed is om verslag uit te brengen, maakt deze opnieuw verbinding met de service en worden inkomende gebeurtenissen verzonden. Deze gebeurtenissen worden onmiddellijk verwerkt door de wachtrijverwerker.
4. Op basis van de gegevens van de inkomende gebeurtenissen kan de wachtrijverwerker bestaand werk uitvoeren of wijzigen of nieuw werk maken.

## <a name="turn-on-the-mhax-feature"></a>De MHAX-functie inschakelen

Voordat u de MHAX-functie kunt gebruiken, moet u zowel de functie als de bijbehorende configuratiesleutel inschakelen.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
2. Schakel in de werkruimte voor **[functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** de functie in met de naam *Interface voor materiaalverwerkingsapparatuur* (Material handling equipment interface).
3. Plaats uw systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
5. Vouw **Handel \> Magazijn- en transportbeheer** uit en schakel vervolgens het selectievakje **Interface voor materiaalverwerkingsapparatuur** in.
6. Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>MHAX-parameters instellen

U moet enkele algemene parameters instellen op de pagina **Parameters voor de interface voor materiaalverwerkingsapparatuur** om de functie te configureren.

1. Ga naar **Interface voor materiaalverwerkingsapparatuur \> Instellen \> Parameters voor de interface voor materiaalverwerkingsapparatuur**.
2. Stel op het tabblad **Algemeen** de volgende velden in:

    - **Gebruikers-id**: Selecteer een werknemer. Deze werknemer wordt gebruikt om alle werkbewerkingen uit te voeren (orderverzamelen en wegzetten) die door de inkomende wachtrij worden verwerkt.
    - **Binnenkomende-bericht-id inschakelen**: Wanneer deze optie op *Ja* wordt ingesteld en er een tweede bericht binnenkomt met dezelfde id, wordt dit bericht afgewezen en wordt in een foutbericht melding gemaakt dat het bericht al bestaat. Als deze optie is ingesteld op *Nee*, zijn meerdere binnenkomende berichten met dezelfde id's toegestaan.

3. Selecteer op het tabblad **Nummerreeksen** de nummerreeksen voor het hele systeem die moeten worden gebruikt om unieke id's te genereren voor de binnenkomende wachtrijartikelen, uitgaande wachtrijartikelen en werkregelparen.

## <a name="outbound-events"></a>Uitgaande gebeurtenissen

Op bepaalde punten tijdens het maken of uitvoeren van werk bepaalt het systeem of er uitgaande gebeurtenissen moeten worden gegenereerd die naar het MH-systeem moeten worden verzonden. Als er een abonnement is geconfigureerd voor een specifiek punt tijdens de magazijnverwerking, wordt de gebeurtenis door het systeem gegenereerd volgens de instellingen van het abonnement.

### <a name="structure-of-outbound-events"></a>Structuur van uitgaande gebeurtenissen

Elke uitgaande gebeurtenis wordt aangeduid met een unieke uitgaande-wachtrij-id. Het type uitgaande transactie bepaalt het type gebeurtenis. Het magazijn en de id van het abonnement dat de gebeurtenis heeft gegenereerd, worden ook in de gebeurtenis vastgelegd.

Als u gegevens naar het MH-systeem wilt overbrengen, bevat de uitgaande gebeurtenis 10 velden voor gegevens (**data01** tot en met **data10**). Deze gegevensvelden hebben een een-op-één-toewijzing (1:1) naar bestaande databasevelden. Deze worden met name uit velden in de werkregel- en headertabellen gehaald. De velden kunnen vrijelijk worden geselecteerd. U stelt deze in wanneer u het abonnement maakt.

Naast de 10 gegevensvelden met een 1:1-toewijzing naar bestaande databasevelden, kan de gebeurtenis een aanvullend gegevensveld bevatten dat *payload* wordt genoemd. De inhoud van dit veld wordt gegenereerd door aangepaste X++-code die, bekend staat als *payloadgenerator*. Alle payloadgenerators die moeten worden gebruikt, worden ingesteld in het abonnement.

Om er zeker van te zijn dat het MH-systeem elke uitgaande wachtrij-id maar één keer ontvangt, wordt een statusveld gebruikt om aan te geven of een gebeurtenis gereed is om naar het externe systeem te worden verzonden of om aan te geven dat deze al is verzonden.

### <a name="outbound-queue-subscriptions"></a>Abonnementen voor de uitgaande wachtrij

Voordat er gebeurtenissen worden gegenereerd, moet er een abonnement worden ingesteld om aan de MHAX-functie te laten weten of en hoe gebeurtenissen moeten worden gegenereerd. Gegenereerde gebeurtenissen worden gelabeld met een abonnement-id. Op deze manier kunnen meerdere MH-systemen verbinding maken met hetzelfde WMS-systeem, terwijl hun gebeurtenissen van elkaar gescheiden blijven. Wanneer de MHAX-service wordt gecontroleerd op nieuwe gebeurtenissen, is een abonnement een van de beschikbare opties voor het ophalen van de gebeurtenissen.

Als u een abonnement wilt maken, gaat u naar **Interface voor materiaalverwerkingsapparatuur \> Instellen \> Abonnementen**. Voor elk abonnement zijn de volgende parameters beschikbaar:

- **Abonnement-id**: een unieke naam waarmee het abonnement wordt aangeduid.
- **Beschrijving**: een vrije-tekstbeschjrijving van het abonnement.
- **Magazijn**: de specifieke magazijnen waarop gebeurtenissen moeten worden gefilterd.
- **Type uitgaande transactie**: het type gebeurtenissen dat het abonnement moet bevatten.
- **Payloadgenerator**: een optionele code-extensie die extra informatie kan invoeren in het veld **Payload** van de uitgaande gebeurtenis.

Er kan aan elk abonnement een query worden gekoppeld. Met deze query worden werkregels en headers gefilterd ter beperking van het werk dat gebruikmaakt van het abonnement voor het genereren van gebeurtenissen. Als u een query aan een abonnement wilt toevoegen, selecteert u het selectievakje **Query uitvoeren** voor het relevante abonnement op de pagina **Abonnementen** en selecteert u vervolgens **Query bewerken** in het actievenster. De standaard query-editoreditor van Supply Chain Management wordt weergegeven.

Het abonnement bevat bovendien een *abonnementstoewijzing* waarmee velden vanuit de werkheader of de werkregel worden toegewezen aan enkele of alle 10 vrije gegevensvelden van de uitgaande gebeurtenis, indien nodig. Als u gegevens naar de MHAX-service wilt retourneren, zult u gewoonlijk de werkregelrecord-id of de *werkregelpaar-id* opnemen. (De werkregelpaar-is is een nieuwe eigenschap waarmee het systeem één retouropdracht kan gebruiken voor het verwerken regels voor verzamelen en wegzetten.) De resterende velden zijn afhankelijk van de use case. Verderop in dit artikel worden enkele voorbeelden gegeven.

Als u een abonnementstoewijzing wilt instellen, selecteert u het desbetreffende abonnement op de pagina **Abonnementen** en selecteert u vervolgens **Abonnementstoewijzing** in het actievenster. In het dialoogvenster **Abonnementstoewijzing** dat verschijnt, kunt u een tabel en een veld toewijzen voor elk beschikbare gegevensveld dat u nodig hebt.

### <a name="outbound-event-types"></a>Typen uitgaande gebeurtenissen

In deze sectie worden de verschillende typen gebeurtenissen beschreven die beschikbaar zijn. (Gebeurtenistypen worden ook wel *transactietypen* genoemd.) Er wordt ook uitgelegd wanneer elk type gebeurtenis wordt gemaakt in het WMS-systeem.

#### <a name="work-creation-events"></a>Werkaanmaakgebeurtenissen

Gebeurtenissen voor het aanmaken van werk worden gemaakt nadat het werk door de toepassing is gegenereerd. Dit gedrag is van toepassing op de meeste typen werkaanmaakprocessen, maar vooral op het aanmaken van orderverzamel- en aanvulwerk. Wanneer er werk wordt aangemaakt met de status *Open*, waarmee wordt aangegeven dat het werk gereed is om door een werknemer te worden uitgevoerd, wordt er in het algemeen een werkaanmaakgebeurtenis gegenereerd. Bovendien worden gebeurtenissen voor het aanmaken van werk gegenereerd voor basis verplaatsingswerk (niet verplaatsing-per-sjabloonwerk), zelfs als dat werk niet als 'open werk' is gemaakt.

Een belangrijk uitzondering op deze dit gedrag is het cyclustellingswerk, dat momenteel niet wordt ondersteund. Voorraadtellingen in het MH-systeem vallen buiten het bereik van MHAX en de resultaten van tellingen moeten worden geïmporteerd in een voorraadtellingsjournaal.

Nadat het werk is gemaakt, verwerkt de MHAX-service de werkregels die zijn gegenereerd en wijst de service een werkregelpaar-id toe aan alle gegenereerde werkregels voor elke werkheader. Het doel is om alle werkregels voor orderverzameling te groeperen met de opeenvolgende wegzetbewerkingen onder één werkregelpaar-id. (De groepen corresponderen met de orderverzamel-/wegzetparen in werksjablonen.) Op deze manier kunt u één id gebruiken om de voltooiing van het werk voor alle gerelateerde regels voor orderverzamelen en wegzetten te rapporteren. Het groeperingsproces begint met de eerste regel en gaat door met dezelfde id totdat het volgende paar van werkregels voor wegzetten/orderverzamelen wordt aangetroffen. De lopende id wordt toegewezen aan de wegzetregel van dat paar. Een nieuwe id wordt vervolgens gebruikt voor de orderverzamelregel van het paar. Dit proces wordt voortgezet totdat alle regels in de werkheader zijn verwerkt.

Een speciale functie van werkaanmaakgebeurtenissen is de optie **Geblokkeerde wave**. Als deze op *Ja* wordt ingesteld in de werkheader, hebben de gebeurtenissen die worden gegenereerd, de status *Geblokkeerd* in plaats van de gewone status *Gereed* die wordt gebruikt om ze naar het MH-systeem te sturen. De markering **Geblokkeerde wave** in de werkheader geeft aan dat de werkheader nog niet gereed is om te worden uitgevoerd door werknemers, bijvoorbeeld omdat het aanvullingswerk nog niet is voltooid. Wanneer de markering **Geblokkeerde wave** wordt gewist, wordt de blokkering van de gebeurtenissen die al zijn gegenereerd, opgeheven en kunnen deze gebeurtenissen door het MH-systeem uit de wachtrij worden opgehaald.

#### <a name="work-initiation-events"></a>Werkinitiatiegebeurtenissen

Gebeurtenissen voor het initiëren van werk worden geactiveerd wanneer de werkstatus verandert van *Open* in *Onderhanden* tijdens het bijwerken van het werk.

#### <a name="work-completion-events"></a>Werkvoltooiingsgebeurtenissen

Gebeurtenissen voor het voltooien van werk worden geactiveerd wanneer de werkstatus verandert van *Onderhanden* in *Gesloten* tijdens het bijwerken van het werk.

#### <a name="work-cancellation-events"></a>Werkannuleringsgebeurtenissen

Gebeurtenissen voor het annuleren van werk worden geactiveerd wanneer de werkstatus verandert van elke andere status dan *Geannuleerd* in de status *Geannuleerd* tijdens het bijwerken van het werk. Bovendien worden alle andere gebeurtenissen die gerelateerd zijn aan de werkheader, verwijderd uit de wachtrij voor alle abonnementen. Op deze manier wordt voorkomen dat externe systemen gebeurtenissen verwerken die niet vereist zijn.

#### <a name="pickput-completion-events"></a>Voltooiingsgebeurtenissen voor orderverzamelen/wegzetten

Gebeurtenissen voor het voltooien van orderverzamel-/wegzetwerk worden geactiveerd wanneer de status van de orderverzamel-/wegzetregel verandert van *Onderhanden* in *Gesloten* tijdens het bijwerken van de werkregel.

### <a name="monitor-the-outbound-queue"></a>De uitgaande wachtrij bewaken

Als u uw uitgaande wachtrij wilt controleren, gaat u naar **Interface voor materiaalverwerkingsapparatuur \> Algemeen \> Uitgaande wachtrij**. Op de pagina **Uitgaande wachtrij** wordt elk artikel in de uitgaande wachtrij en de status daarvan weergegeven. Selecteer een wachtrij-artikel om de details daarvan weer te geven. Deze details omvatten het transactietype van het artikel, het abonnement dat is gebruikt en de waarden voor elk gegevensveld (**data01** through **data10**) en de payload.

### <a name="clean-up-the-outbound-queue"></a>De uitgaande wachtrij opschonen

Uiteindelijk zal uw uitgaande wachtrij vol raken met wachtrijartikelen die al zijn verzonden. Als u deze artikelen wilt verwijderen, gaat u naar de **Interface voor materiaalverwerkingsapparatuur \> Periodieke taken \> Opschonen \> Uitgaande wachtrij opschonen**.

## <a name="inbound-events"></a>Binnenkomende gebeurtenissen

In deze sectie worden de verschillende typen binnenkomende gebeurtenissen beschreven die het MH-systeem kan rapporteren aan het WMS-systeem. Verder wordt uitgelegd dat gegevens moeten worden geleverd door het MH-systeem en wat elke binnenkomende gebeurtenis in het WMS-systeem doet.

### <a name="structure-of-inbound-events"></a>Structuur van binnenkomende gebeurtenissen

Wanneer een binnenkomende gebeurtenis wordt ingediend, moet het externe systeem het binnenkomende transactietype leveren samen met maximaal 10 parameters (**data01** through **data10**). Optionele validatie kan voorkomen dat de MHAX-service dezelfde binnenkomende gebeurtenis vaker dan één keer ontvangt. Als u deze validatie wilt inschakelen, moet elke binnenkomende gebeurtenis een unieke bericht-id hebben. Als er een dubbele bericht-id wordt ontvangen en als de optie **Binnenkomende-bericht-id inschakelen** wordt ingesteld op *Ja* op de pagina **Parameters voor de interface voor materiaalverwerkingsapparatuur**, wordt het bericht afgewezen. Er wordt een foutbericht weergegeven waarin staat dat het bericht al bestaat.

Naast de gegevensvelden van binnenkomende gebeurtenissen wijst het systeem een unieke binnenkomende-wachtrij-id aan de gebeurtenis toe.

### <a name="inbound-event-types"></a>Typen binnenkomende gebeurtenissen

In deze sectie worden de typen binnenkomende gebeurtenissen (transactietypen) beschreven die worden ondersteund en worden de gegevens vermeld die moeten worden geleverd om gebeurtenissen te verwerken.

#### <a name="work-confirm-events"></a>Werkbevestigingsgebeurtenissen

Voor werkbevestigingsgebeurtenissen moeten de gegevensvelden van binnenkomende gebeurtenissen de volgende informatie bevatten:

- **data01**: de werkregelpaar-id.
- **data02**: de werkregelrecord-id (`RecId`-waarde).

    > [!NOTE]
    > *Of* het veld **data01** *of* het veld **data02** moet aanwezig zijn.

- **data03**: de id van de nummerplaat van waaraf moet worden verzameld.
- **data04** : de id van de doelnummerplaat van de werkheader.

Als de werkregelpaar-id is opgegeven, worden alle orderverzamel- en wegzetwerkregels of aangepaste werkregels die zijn gemarkeerd door de werkregelpaar-id en die de status *Open* of *Onderhanden* hebben, achter elkaar uitgevoerd. Als een werkregelrecord-id (`RecId`-waarde) is opgegeven, moet de werkregel een orderverzamel- of wegzetwerkregel of een aangepaste werkregel zijn met de status *Open* of *Onderhanden*.

Voor orderverzamelregels die afkomstig zijn van door een nummerplaat beheerde locaties, moet in het veld **data03** de nummerplaat worden opgegeven van waaruit artikelen moeten worden verzameld voor een order, ongeacht of de regels zijn gemarkeerd door de werkregelrecord-id of de werkregelpaar-id. In het veld **data04** moet de doelnummerplaat van de werkheader voor de orderverzamelbewerking worden opgegeven.

Op wegzetregels worden geen verdere informatie geaccepteerd. Deze worden alleen uitgevoerd op basis van de locatie van de huidige werkregel en de doelnummerplaat van het werk. Als de wegzetbewerking naar een andere locatie moet worden uitgevoerd, wijzigt u de locatie van de werkregel, zoals beschreven in de sectie [Gebeurtenissen overschrijven](#override-events) verderop in dit artikel.

Aangepaste werkregels vereisen of ondersteunen geen extra informatie in de binnenkomende gebeurtenis.

#### <a name="short-pick-events"></a>Tekortverzamelgebeurtenissen

Voor gebeurtenissen voor het verzamelen van een tekort moeten de gegevensvelden van binnenkomende gebeurtenissen de volgende informatie bevatten:

- **data02**: de werkrecord-id (`RecId`-waarde).
- **data03**: de id van de nummerplaat van waaraf moet worden verzameld.
- **data04**: de hoeveelheid die moet worden verzameld.
- **data05:** de uitzonderingscode voor tekort verzamelen.
- **data06**: de id van de doelnummerplaat van de werkheader.

> [!NOTE]
> Het veld **Data01** wordt niet gebruikt voor gebeurtenissen voor het verzamelen van tekorten.

Deze gebeurtenis lijkt op de werkbevestigingsgebeurtenis, maar is alleen van toepassing op orderverzamelregels.

#### <a name="override-events"></a><a id="override-events"></a>Gebeurtenissen overschrijven

Voor het overschrijven van gebeurtenissen moeten de gegevensvelden van binnenkomende gebeurtenissen de volgende informatie bevatten:

- **data01**: de werkrecord-id (`RecId`-waarde).
- **data02**: de id van de nieuwe locatie.

De werkregel moet de status *Open* of *Onderhanden* hebben en de nieuwe locatie moet bestaan.

#### <a name="license-plate-receipt-events"></a>Nummerplaatontvangstgebeurtenissen

Voor gebeurtenissen voor de ontvangst van nummerplaten moeten de gegevensvelden van binnenkomende gebeurtenissen de volgende informatie bevatten:

- **data01**: de id van de binnenkomende nummerplaat die moet worden ontvangen.

Het systeem voert een nummerplaatontvangstbewerking uit op basis van de nummerplaat die wordt doorgegeven als de waarde van het veld **data01**.

### <a name="monitor-the-inbound-queue"></a>De binnenkomende wachtrij bewaken

Als u uw binnenkomende wachtrij wilt controleren, gaat u naar **Interface voor materiaalverwerkingsapparatuur \> Algemeen \> Binnenkomende wachtrij**. Op de pagina **Binnenkomende wachtrij** wordt elk artikel in de binnenkomende wachtrij en de status daarvan weergegeven. Selecteer een wachtrij-artikel om de details daarvan weer te geven. Deze details omvatten het transactietype van het artikel, de bericht-id en de waarden voor elk gegevensveld (**data01** tot en met **data10**).

Als er een fout of een ander type logboekartikel is opgetreden tijdens het verwerken van binnenkomende gebeurtenissen, kunt u de fout inspecteren door **Foutenlogboek** te selecteren in het actievenster.

### <a name="inbound-event-processing"></a>De verwerking van binnenkomende gebeurtenissen

Binnenkomende gebeurtenissen worden eerst naar de database geschreven en vervolgens onmiddellijk(synchroon) uitgevoerd. Als er tijdens de verwerking een fout optreedt, wordt de gebeurtenis nog steeds naar de wachtrij geschreven, maar wordt de status ingesteld op *Fout*. De MHAX-service retourneert een foutbericht naar het MH-systeem en slaat het foutenlogboek op in de binnenkomende-gebeurtenisrecord voor later onderzoek.

Gebeurtenissen met de status *Fout* kunnen later opnieuw worden verwerkt als het probleem dat de fout veroorzaakt, is opgelost. Volg een van deze stappen om de gebeurtenissen opnieuw te verwerken:

- Ga naar **Interface voor materiaalverwerkingsapparatuur \> Algemeen \> Binnenkomende wachtrij**. Selecteer de relevante binnenkomende wachtrij en selecteer **Opnieuw verwerken** in het actievenster.
- Ga naar **Interface voor materiaalverwerkingsapparatuur \> Algemeen \> Binnenkomende wachtrij met fout opnieuw verwerken**. Er wordt een standaarddialoogvenster voor batchtaken weergegeven. Hier kunt u een recordfilter instellen en een batchtaak plannen of uitvoeren om de wachtrij opnieuw te verwerken.

Alle werkbewerkingen (orderverzamel- en wegzetbewerkingen) worden uitgevoerd met de werknemer die is geselecteerd in het veld **Gebruikers-id** op de pagina **Parameters voor de interface voor materiaalverwerkingsapparatuur**.

### <a name="clean-up-the-inbound-queue"></a>De binnenkomende wachtrij opschonen

Uiteindelijk zal uw binnenkomende wachtrij vol raken met wachtrijartikelen die al zijn verwerkt. Als u deze artikelen wilt verwijderen, gaat u naar **Interface voor materiaalverwerkingsapparatuur \> Periodieke taken \> Opschonen \> Binnenkomende wachtrij opschonen**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Snel een overzicht krijgen met de wachtrijbeheerder

Als u snel een overzicht wilt hebben van alle activiteiten die te maken hebben met uw binnenkomende en uitgaande wachtrijen, gaat u naar **Interface voor materiaalverwerkingsapparatuur \> Werkruimten \> Wachtrijbeheerder**. De pagina **Wachtrijbeheerder** biedt een set tabbladen en informatie die u kunt gebruiken om uw wachtrijen te bewaken en te bekijken. Op deze pagina vindt u ook nuttige koppelingen naar de meeste andere pagina's die in dit artikel worden genoemd.

## <a name="connect-to-the-mhax-service"></a>Verbinding maken met de MHAX-service

MHAX wordt geïmplementeerd als aangepaste service. Deze service is dan ook toegankelijk via SOAP- en REST-aanroepen. Hier vindt u de adressen van de SOAP- en REST-eindpunten:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Berichten ophalen uit de uitgaande wachtrij

Gebruik een van de volgende methoden om berichten op te halen uit de uitgaande wachtrij:

- Gebruik `readOutboundSubscriptionQueue` om gebeurtenissen op te halen op basis van de abonnements-id.
- Gebruik `readOutboundWarehouseQueue` om de gebeurtenissen uit meerdere abonnementen op te halen op basis van het gebeurtenistype en de magazijn-id.
