---
title: Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden
description: Dit onderwerp bevat informatie over de functie waarmee schaaleenheden kunnen worden gebruikt om geselecteerde processen uit te voeren vanuit de magazijnbeheer-workload.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ae8e9791b590a32581b66853f55ea11bc389bb19
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891746"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Niet alle magazijnbeheerbedrijfsfunctionaliteit wordt volledig ondersteund voor magazijnen met een werkbelasting voor een schaaleenheid. Zorg ervoor dat u alleen de processen gebruikt die in dit onderwerp expliciet worden ondersteund.

## <a name="warehouse-execution-on-scale-units"></a>Magazijnuitvoering op schaaleenheden

Bij werkbelasting voor Warehouse Management kunnen cloud- en randschaaleenheden geselecteerde processen uitvoeren vanuit de Warehouse Management-mogelijkheden.

## <a name="prerequisites"></a>Vereisten

U moet beschikken over een Dynamics 365 Supply Chain Management-hub en een schaaleenheid die met de magazijnbeheerworkload is geïmplementeerd. Raadpleeg [Schaaleenheden in een gedistribueerde hybride topologie](cloud-edge-landing-page.md) voor meer informatie over de architectuur en het implementatieproces.

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Hoe de werkbelasting voor magazijnuitvoering werkt op schaaleenheden

Voor de processen in de magazijnbeheer-workload worden de gegevens gesynchroniseerd tussen de hub en de schaaleenheden.

Een schaaleenheid kan alleen de gegevens behouden waarvan deze eigenaar is. Het concept gegevenseigendom voor schaaleenheden helpt multi-masterconflicten te voorkomen. Het is daarom belangrijk dat u begrijpt welke procesgegevens eigendom zijn van de hub en welke van de schaaleenheden.

Afhankelijk van de bedrijfsprocessen kan dezelfde gegevensrecord van eigenaar wisselen tussen de hub en schaaleenheden. In het volgende gedeelte staat een voorbeeld van dit scenario.

> [!IMPORTANT]
> Sommige gegevens kunnen zowel op de hub als op de schaaleenheid worden aangemaakt. Voorbeelden zijn **Nummerplaten** en **Batchnummers**. Specifieke conflictverwerking wordt geleverd in gevallen waarin dezelfde unieke record wordt aangemaakt op zowel de hub als de schaaleenheid tijdens dezelfde synchronisatiecyclus. In dat geval mislukt de volgende synchronisatie en moet u naar **Systeembeheer > Opvragen > Werkbelastingvragen > Dubbele records**, waar u de gegevens kunt weergeven en samenvoegen.

## <a name="outbound-process-flow"></a>Uitgaande processtroom

Voordat u de werkbelasting van magazijnbeheer implementeert op een cloud- of randschaaleenheid, moet u ervoor zorgen dat u de functie *Ondersteuning van de eenheidseenheid voor het vrijgeven naar magazijn van uitgaande orders* hebt ingeschakeld voor uw zakelijke hub. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Warehouse Management*
- **Functienaam:** *ondersteuning van de schaaleenheid voor het vrijgeven naar magazijn van uitgaande orders*

Het proces voor eigendom van uitgaande gegevens is afhankelijk van of u het proces voor belastingplanning gebruikt. In alle gevallen is de hug eigenaar van de *brondocumenten*, zoals verkooporders en transferorders, alsmede het ordertoewijzingsproces en de bijbehorende ordertransactiegegevens. Wanneer u echter het ladingplanningsproces gebruikt, worden de ladingen op de hub gemaakt en dus in eerste instantie eigendom van de hub. Als onderdeel van het proces *Vrijgave naar magazijn* wordt het eigendom van de belastingsgegevens overgebracht naar de specifieke implementatie van de schaaleenheid, die vervolgens eigenaar wordt van de daaropvolgende *verzendingswaves verwerken* (zoals werktoewijzing, aanvullende werkzaamheden en het aanmaken van aanvraagwerk). Magazijnmedewerkers kunnen daarom alleen uitgaand verkoop- en transferorderwerk verwerken met een mobiele Warehouse Management-app die is gekoppeld aan de implementatie met de specifieke werkbelasting van de schaaleenheid.

Zodra het uiteindelijke werkproces de voorraad op een uiteindelijke verzendlocatie (laaddeur) plaatst, meldt de schaaleenheid aan de hub dat de voorraadtransacties van het brondocument moeten worden bijgewerkt naar *Verzameld*. Totdat dit proces wordt uitgevoerd en opnieuw wordt gesynchroniseerd, wordt de aanwezige voorraad op de werkbelasting van de schaaleenheid fysiek gereserveerd op magazijnniveau. U kunt de bevestiging van de uitgaande zending onmiddellijk verwerken zonder te wachten op deze synchronisatie. De daaropvolgende verkooppakbon en facturerings- of transferorderzending voor de belasting worden afgehandeld in de hub.

In het volgende diagram wordt de uitgaande stroom weergegeven en wordt aangegeven waar de afzonderlijke bedrijfsprocessen plaatsvinden. (Selecteer het diagram om het te vergroten.)

[![Verwerkingsstroom voor uitgaande goederen.](media/wes_outbound_warehouse_processes-small.png "Verwerkingsstroom voor uitgaande goederen")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Verwerking van uitgaande goederen met ladingplanning

Wanneer u het proces voor ladingsplanning gebruikt, worden belastingen en zendingen op de hub gemaakt en wordt het eigendom van de gegevens overgebracht naar de schaaleenheden als onderdeel van het proces *Vrijgave naar magazijn*, zoals in de volgende afbeelding wordt geïllustreerd.

![Verwerking van uitgaande goederen met ladingplanning.](./media/wes_outbound_processing_with_load_planning.png "Verwerking van uitgaande goederen met ladingplanning")

### <a name="outbound-processing-without-load-planning"></a>Verwerking van uitgaande goederen zonder ladingplanning

Wanneer u het proces ladingsplanning niet gebruikt, worden zendingen aangemaakt op de schaaleenheden. Ladingen worden ook op de schaaleenheden gemaakt als onderdeel van het wave-proces.

![Verwerking van uitgaande goederen zonder ladingplanning.](./media/wes_outbound_processing_without_load_planning.png "Verwerking van uitgaande goederen zonder ladingplanning")

## <a name="inbound-process-flow"></a>Inkomende processtroom

De hub is eigenaar van de volgende gegevens:

- Alle brondocumenten, zoals inkooporders en productieorders
- Inkomende ladingverwerking
- Alle kosten en financiële updates

> [!NOTE]
> De inkomende inkooporderstroom is conceptueel verschillend van de uitgaande stroom. U kunt hetzelfde magazijn op de schaaleenheid of de hub bedienen, afhankelijk van of de inkooporder is vrijgegeven naar magazijn. Nadat u een order naar het magazijn hebt vrijgegeven, kunt u alleen met die order werken zolang u bent aangemeld bij de schaaleenheid.
>
> Als u het proces *Vrijgeven naar magazijn* gebruikt, worden [*magazijnorders*](cloud-edge-warehouse-order.md) gemaakt en wordt het eigendom van de gerelateerde ontvangende stroom toegewezen aan de schaaleenheid. De hub kan inkomende ontvangst niet registreren.

U moet zich aanmelden bij de hub om het proces *Vrijgeven aan magazijn* te gebruiken. Ga voor de verwerking van een inkooporder naar een van de volgende pagina's om deze uit te voeren of te plannen:

- **Inkoopbeheer > Inkooporders > Alle inkooporders > Magazijn > Acties > Vrijgeven aan magazijn**
- **Magazijnbeheer > Vrijgave naar magazijn > Automatische vrijgave van inkooporders**

Wanneer u **Automatische vrijgave van inkooporders** gebruikt, kunt u specifieke inkooporderregels selecteren op basis van een query. Een standaardscenario is het instellen van een terugkerende batchtaak waarbij alle bevestigde inkooporderregels worden vrijgegeven die naar verwachting de volgende dag zullen binnenkomen.

De medewerker kan het ontvangstproces uitvoeren met behulp van een mobiele app Magazijnbeheer die is verbonden met de schaaleenheid. De gegevens worden vervolgens door de schaaleenheid geregistreerd en gerapporteerd voor de inkomende magazijnorder. Het maken en verwerken van de volgende wegzetactie wordt ook afgehandeld door de schaaleenheid.

Als u het proces van *vrijgave naar magazijn* niet gebruikt en dus geen *magazijnorders* gebruikt, kan de hub de magazijnontvangst en de werkverwerking onafhankelijk van schaaleenheden verwerken.

![Inkomende processtroom.](./media/wes-inbound-ga.png "Inkomende processtroom")

Wanneer een werknemer een inkomende registratie doet met behulp van een ontvangstproces voor de mobiele Warehouse Management-app voor de schaaleenheid, wordt een ontvangst geregistreerd op basis van de gerelateerde magazijnorder, die wordt opgeslagen in de schaaleenheid. De werkbelasting van de schaaleenheid geeft vervolgens het signaal aan de hub om de gerelateerde inkooporderregeltransacties bij te werken naar *Geregistreerd*. Als dit is voltooid, kunt u een productontvangstbon voor een inkooporder uitvoeren op de hub.

In het volgende diagram wordt de inkomende stroom weergegeven en wordt aangegeven waar de afzonderlijke bedrijfsprocessen plaatsvinden. (Selecteer het diagram om het te vergroten.)

[![Verwerkingsstroom voor inkomende goederen](media/wes_inbound_warehouse_processes-small.png "Verwerkingsstroom voor inkomende goederen")](media/wes_inbound_warehouse_processes.png)

## <a name="supported-processes-and-roles"></a>Ondersteunde processen en rollen

Niet alle magazijnbeheerprocessen worden in een werkbelasting voor magazijnuitvoering bij een schaaleenheid ondersteund. Daarom is het raadzaam rollen toe te wijzen die overeenkomen met de functionaliteit die voor elke gebruiker beschikbaar is.

Ter vereenvoudiging van dit proces is een voorbeeldrol met de naam *Magazijnbeheerder bij workload* opgenomen in de demogegevens bij **Systeembeheer \> Beveiliging \> Beveiligingsconfiguratie**. Het doel van deze rol is magazijnbeheerders toegang geven tot de werkbelasting voor magazijnuitvoering op de schaaleenheid. De rol geeft toegang tot de pagina's die relevant zijn in de context van een workload die op een schaaleenheid wordt gehost.

Gebruikersrollen op een schaaleenheid worden toegewezen als onderdeel van de oorspronkelijke gegevenssynchronisatie van de hub naar de schaaleenheid.

Als u de rollen wilt wijzigen die aan een gebruiker zijn toegewezen, gaat u naar **Systeembeheer \> Beveiliging \> Gebruikers aan rollen toewijzen**. Gebruikers die alleen als magazijnbeheerders werken, moeten alleen de rol *Magazijnbeheerder bij workload* toegewezen krijgen. Op deze manier zorgt u ervoor dat gebruikers alleen toegang hebben tot de ondersteunde functies. Verwijder alle andere rollen die aan deze gebruikers zijn toegewezen.

Gebruikers die als magazijnbeheerders werken op de hub én schaaleenheden, moeten de bestaande rol *Magazijnmedewerker* toegewezen krijgen. Houd er rekening mee dat magazijnmedewerkers toegang hebben tot functies (zoals de ontvangstverwerking van overboekingsorders) die in de gebruikersinterface worden weergegeven, maar die momenteel niet worden ondersteund voor schaaleenheden.

### <a name="supported-warehouse-execution-processes"></a>Ondersteunde magazijnuitvoeringsprocessen

De volgende processen voor magazijnuitvoering kunnen worden ingeschakeld voor een werkbelasting voor magazijnuitvoering op een schaaleenheid:

- Geselecteerde wave-methoden voor verkoop- en transferorders (validatie, lading aanmaken, toewijzing, vraagaanvulling, containervorming, aanmaken van werk en afdrukken van wave-labels)

- Magazijnwerk voor verkoop- en transferorders verwerken met de magazijn-app (inclusief aanvullingswerk)
- Zoeken in voorhanden voorraad met behulp van de magazijn-app
- Voorraadmutaties maken en uitvoeren met behulp van de magazijn-app
- Werk voor een telcyclus maken en verwerken met de magazijn-app
- Voorraadcorrecties maken met de magazijn-app
- Inkooporders registreren en wegzetwerk doen met de magazijn-app

De volgende typen werk kunnen worden aangemaakt op een schaaleenheid en kunnen daarom worden verwerkt als onderdeel van de werkbelasting van magazijnbeheer:

- **Voorraadmutaties** - handmatig verplaatsen en verplaatsen met behulp van sjabloonwerk.
- **Cyclustelling** - inclusief het goedkeurings-/afwijzingsproces voor discrepanties als onderdeel van telbewerkingen.
- **Inkooporders** - wegzetwerk via een magazijnorder wanneer inkooporders niet aan ladingen zijn gekoppeld.
- **Verkooporders** - eenvoudig verzamel- en laadwerk.
- **Transferprobleem** - eenvoudig verzamel- en laadwerk.
- **Aanvulling** - exclusief grondstoffen voor productie.
- **Eindproducten wegzetten** - na het gereedmelden van het productieproces.
- **Coproduct en bijproduct wegzetten** - na het gereedmelden van het productieproces.

Momenteel wordt verwerking van andere typen brondocumenten of magazijnwerk niet ondersteund voor schaaleenheden. Voor bijvoorbeeld een werkbelasting voor magazijnuitvoering voor een schaaleenheid kunt u geen proces voor het ontvangen van transferorders (ontvangst transfer) uitvoeren; dit moet worden uitgevoerd door het hub-exemplaar.

> [!NOTE]
> Menu-items en knoppen voor mobiele apparaten voor niet-ondersteunde functies worden niet weergegeven in de _mobiele app Magazijnbeheer_ wanneer deze is verbonden met een schaaleenheidimplementatie.
> 
> Als u een workload uitvoert voor een schaaleenheid, kunt u geen niet-ondersteunde processen voor dat specifieke magazijn op de hub uitvoeren. De tabellen die later in dit onderwerp worden verstrekt, documenteren de ondersteunde capaciteiten.
>
> Geselecteerde magazijnwerktypen kunnen zowel voor de hub als voor schaaleenheden worden gemaakt. Deze werktypen kunnen echter alleen worden beheerd door de eigenaar van de hub of schaaleenheid (de implementatie waardoor de gegevens zijn gemaakt).
>
> Zelfs wanneer een specifiek proces voor schaaleenheid wordt ondersteund, moet u er rekening mee houden dat niet alle benodigde gegevens worden gesynchroniseerd van de hub naar de schaaleenheid of van de schaaleenheid naar de hub, wat kan resulteren in onverwachte systeemverwerking. Voorbeelden van dit scenario omvatten:
> 
> - Als u een query voor een locatie-instructie gebruikt die een gegevenstabelrecord samenvoegt die alleen bij de hubimplementatie bestaat.
> - Als u volumetrische laadfunctionaliteiten voor locatiestatus en/of locatie gebruikt. Deze gegevens worden niet gesynchroniseerd tussen de implementaties en werken daarom alleen bij het bijwerken van de locatievoorraad die beschikbaar is op een van de implementaties.

De volgende magazijnbeheerfunctionaliteit wordt momenteel niet ondersteund voor schaaleenheidworkloads:

- Inkomende verwerking met inkooporderregels die aan een belasting zijn toegewezen.
- Inkomende verwerking van inkooporders voor een project.
- Het beheren van francokosten, inclusief reizen en traceren van goederen in transit.
- Inkomende en uitgaande verwerking voor items met actieve traceringsdimensies **Eigenaar** en/of **Serienummer**.
- Verwerking van voorraad met een blokkeringsstatuswaarde.
- Een voorraadstatus wijzigen tijdens een werkverplaatsingsproces.
- Order-toegezegd flexibel reserveringsbeleid voor dimensies op magazijnniveau.
- Gebruik van de functionaliteit *Magazijnlocatiestatus* (de gegevens worden niet gesynchroniseerd tussen de implementaties).
- Gebruik van de functionaliteit *Positionering van locatie nummerplaat*.
- Gebruik van *Productfilters* en *Productfiltergroepen*, inclusief de instelling **Aantal dagen om batches te mengen**.
- Integratie met kwaliteitsbeheer.
- Verwerking met catch weight-artikelen.
- Verwerking met artikelen alleen ingeschakeld voor Transportbeheer (TMS).
- Verwerking met negatieve voorhanden voorraad.
- Magazijnwerkverwerking met verzendingsnotities.
- Magazijnwerkverwerking met materiaalverwerking/warehouse automation.
- Installatiekopieën met productmodelgegevens (bijvoorbeeld in de mobiele Warehouse Management-app).
- Delen van gegevens tussen meerdere bedrijven voor producten.

> [!WARNING]
> Een aantal magazijnfuncties is niet beschikbaar voor magazijnen met de werkbelasting van magazijnbeheer voor een schaaleenheid en wordt ook niet ondersteund voor de werkbelasting van de hub of schaaleenheid.
> 
> Andere capaciteiten kunnen bij beide worden verwerkt, maar vereisen in sommige scenario's zorgvuldig gebruik, bijvoorbeeld wanneer de voorhanden voorraad voor hetzelfde magazijn wordt bijgewerkt voor de hub als de schaaleenheid vanwege het asynchrone bijwerkproces van gegevens.
> 
> Specifieke functies (zoals *blokkeren van werk*), die worden ondersteund voor zowel de hub als schaaleenheden, worden alleen ondersteund voor de eigenaar van de gegevens.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Uitgaand (wordt alleen ondersteund voor verkoop- en overboekingsorders)

In de volgende tabel ziet u welke uitgaande functies worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                                      | Hub | Werkbelasting magazijnuitvoering op een schaaleenheid |
|--------------------------------------------------------------|-----|------------------------------|
| Brondocumenten verwerken                                   | Ja | Nee |
| Laad- en transportbeheer verwerken                | Ja, maar alleen de processen voor ladingplanning. Verwerking van transportbeheer wordt niet ondersteund  | Nee |
| Vrijgeven aan magazijn                                         | Ja | Nee |
| Gepland cross-docken                                        | Nee  | Nee |
| Zendingen samenvoegen                                       | Ja, bij gebruik van ladingplanning | Ja |
| Verzendingswaves verwerken                                     | Nee  |Ja, behalve **Ladingopbouw en sorteren** |
| Zendingen onderhouden voor wave                                  | Nee  | Ja|
| Magazijnwerk verwerken (inclusief nummerplaat afdrukken)        | Nee  | Ja, maar alleen voor de eerdergenoemde ondersteunde mogelijkheden |
| Orderverzamelen van cluster                                              | Nee  | Ja|
| Handmatige verpakkingsverwerking, incl. verwerking van werk 'Orderverzameling voor ingepakte container' | Nee <P>Bepaalde verwerking kan worden uitgevoerd nadat een oorspronkelijk orderverzamelproces is verwerkt door een schaaleenheid. Dit wordt echter afgeraden vanwege volgende geblokkeerde bewerkingen.</p>  | Nee |
| Container verwijderen uit groep                                  | Nee  | Nee |
| Uitgaande sorteringen verwerken                                  | Nee  | Nee |
| Lading-gerelateerde documenten afdrukken                           | Ja | Ja|
| Vrachtbrief en ASN-generatie                            | Nee  | Ja|
| Verzendbevestiging                                             | Nee  | Ja|
| Zendingsbevestiging met 'Bevestigen en overboeking'            | Nee  | Ja|
| Verwerking van pakbon en facturering                        | Ja | Nee |
| Korte orderverzameling (verkoop- en overboekingsorders)                    | Nee  | Ja, zonder reserveringen voor brondocumenten te verwijderen|
| Meerverzameling (verkoop- en overboekingsorders)                     | Nee  | Ja|
| Wijziging van werklocaties (verkoop- en overboekingsorders)         | Nee  | Ja|
| Werk voltooien (verkoop- en overboekingsorders)                    | Nee  | Ja|
| Werkrapport afdrukken                                            | Ja | Ja|
| Wavelabel                                                   | Nee  | Ja|
| Werk splitsen                                                   | Nee  | Ja|
| Werkverwerking - Gestuurd door 'Transportlading'            | Nee  | Nee |
| Opgenomen hoeveelheid reduceren                                       | Nee  | Ja|
| Werk omkeren                                                 | Nee  | Ja|
| Verzendbevestiging omkeren                                | Nee  | Ja|

### <a name="inbound"></a>Inkomend

In de volgende tabel ziet u welke inkomende functies worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                                          | Hub | Werkbelasting magazijnuitvoering op een schaaleenheid<BR>*(Artikelen met "Ja" zijn alleen van toepassing op magazijnorders)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Bron&nbsp;documenten&nbsp;verwerken                             | Ja | Nee |
| Laad- en transportbeheer verwerken                    | Ja | Nee |
| Francoprijzen voor goederen in transit ontvangen                       | Ja | Nee |
| Bevestiging inkomende zending                                    | Ja | Nee |
| Vrijgave inkooporder naar magazijn (magazijnorderverwerking) | Ja | Nee |
| Annulering van magazijnorderregels<p>Dit wordt alleen ondersteund als er geen registratie voor de regel heeft plaatsgevonden tijdens de verwerking van de *annuleringsaanvraag*.</p> | Ja | Nee |
| Ontvangen en wegzetten van inkooporderartikel                       | <p>Ja,&nbsp;wanneer&nbsp;er&nbsp;geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, wanneer een inkooporder geen deel uitmaakt van een <i>belasting</i></p> |
| Ontvangen van inkooporderregel en wegzetten                       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, wanneer een inkooporder geen deel uitmaakt van een <i>belasting</i></p></p> |
| Ontvangen en wegzetten van retourorder                              | Ja | Nee |
| Nummerplaat ontvangen en wegzetten                       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Ja |
| Artikelontvangst laden                                              | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Ontvangen en wegzetten van nummerplaat                             | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Ontvangen en wegzetten van artikel voor overboekingorder                       | Ja | Nee |
| overboekingsorderregel ontvangen en wegzetten                       | Ja | Nee |
| Werk annuleren (inkomende)                                            | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, maar alleen als de optie <b>Ontvangst ongedaan maken bij annulering van werk</b> (op de pagina <b>Parameters voor magazijnbeheer</b>) wordt uitgeschakeld</p> |
| Inkooporder productontvangstbon verwerken                        | Ja | Nee |
| Ontvangen van inkooporder met minderlevering                      | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Ja, maar alleen door een annuleringsaanvraag vanuit de hub te maken |
| Ontvangen van inkooporder met meerlevering                       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Ja  |
| Ontvangen met aanmaak van werk *Cross-docken*                 | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Ontvangen met aanmaak van werk *Kwaliteitsorder*                  | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Ontvangen met aanmaak van werk *Bemonstering kwaliteitsartikel*          | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Ontvangen met aanmaak van werk *Kwaliteit in kwaliteitscontrole*       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Ontvangen met aanmaak van kwaliteitsorder                            | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Nee |
| Werkverwerking - Gestuurd door *Clusteropslag*                 | Ja | Nee |
| Werkverwerking met *Kort orderverzamelen*                               | Ja | Ja |
| Nummerplaatlading                                           | Ja | Ja |

### <a name="warehouse-operations-and-exception-handing"></a>Magazijnbewerkingen en uitzonderingen afhandelen

In de volgende tabel ziet u welke functies voor magazijnbewerkingen en het afhandelen van uitzonderingen worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                            | Hub | Werkbelasting magazijnuitvoering op een schaaleenheid |
|----------------------------------------------------|-----|------------------------------|
| Nummerplaatonderzoek                              | Ja | Ja                          |
| Artikelonderzoek                                       | Ja | Ja                          |
| Locatieonderzoek                                   | Ja | Ja                          |
| Magazijn wijzigen                                   | Ja | Ja                          |
| Mutatie                                           | Ja | Ja                          |
| Mutatie door sjabloon                               | Ja | Ja                          |
| Magazijntransfer                                 | Ja | Nee                           |
| Transferorders maken vanuit de magazijn-app           | Ja | Nee                           |
| Correctie (in/uit)                                | Ja | Ja, maar niet voor het scenario 'Correctie uit', waarin voorraadreservering moet worden verwijderd met de instelling **Reserveringen verwijderen** voor de voorraadcorrectietypen</p>                           |
| Wijziging van voorraadstatus                            | Ja | Nee                           |
| Cyclustelling en Telverschillen verwerken | Ja | Ja                           |
| Label opnieuw afdrukken (nummerplaat afdrukken)             | Ja | Ja                          |
| Nummerplaat-build                                | Ja | Nee                           |
| Nummerplaat onderbreken                                | Ja | Nee                           |
| Verpakken naar geneste nummerplaten                                | Ja | Nee                           |
| Inchecken chauffeur                                    | Ja | Nee                           |
| Uitchecken chauffeur                                   | Ja | Nee                           |
| Batchbeschikkingscode wijzigen                      | Ja | Ja                          |
| Geopende werklijst weergeven                             | Ja | Ja                          |
| Nummerplaten consolideren                         | Ja | Nee                           |
| Verwerking van min/max en zonedrempelaanvulling| Ja <p>Het wordt afgeraden dezelfde locaties als onderdeel van de query's op te nemen.</p>| Ja                          |
| Aanvulling van vakken verwerken                  | Ja  | Ja<p>Houd er rekening mee dat de instelling moet worden uitgevoerd voor de schaaleenheid</p>                           |
| Werk blokkeren en deblokkeren                             | Ja | Ja                          |
| Gebruiker wijzigen                                        | Ja | Ja                          |
| Werkgroep voor werk wijzigen                           | Ja | Ja                          |
| Werk annuleren                                        | Ja | Ja                          |

### <a name="production"></a>Productie

In de volgende tabel wordt een overzicht gegeven van productiescenario's voor magazijnbeheer die momenteel worden ondersteund voor de werkbelastingen van schaaleenheden.

| Proces | Hub | Werkbelasting magazijnuitvoering op een schaaleenheid |
|---------|-----|------------------------------|
| Gereedmelden en eindproducten wegzetten | Ja | Ja |
| Coproducten en bijproducten wegzetten | Ja | Ja |
| Productieorder beginnen | Ja | Ja |
| <p>Alle andere magazijnbeheerprocessen die betrekking hebben op productie, zoals.</p><li>Vrijgeven aan magazijn</li><li>Productie-waves verwerken</li><li>Orderverzameling van grondstoffen</li><li>Kanban wegzetten</li><li>Kanbanorderverzameling</li><li>Productie-uitval</li><li>Laatste pallet van productie</li><li>Materiaalverbruik registreren</li><li>Lege Kanban</li></ul> | Ja | Nee |
| Aanvulling van grondstoffen | Nee | Nee |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Schaaleenheden onderhouden voor magazijnuitvoering

Er worden verschillende batchtaken uitgevoerd op de hub en schaaleenheden.

In de implementatie van de hub kunt u de batchtaken handmatig onderhouden. U kunt de volgende batchtaken beheren in **Magazijnbeheer \> Periodieke taken \> Backoffice workloadbeheer**:

- Berichtverwerking van schaaleenheid naar hub
- Ontvangsten van bronorders registreren
- Magazijnorders voltooien

Op de workload in schaaleenheden kunt u de volgende batchtaken beheren in **Magazijnbeheer \> Periodieke taken \> Workloadbeheer**:

- Wavetabelrecords verwerken
- Berichtverwerking voor magazijnhub naar schaaleenheid
- Aanvragen voor updates van hoeveelheden voor magazijnorderregels verwerken

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
