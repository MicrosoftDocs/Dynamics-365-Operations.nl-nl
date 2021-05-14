---
title: Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden
description: Dit onderwerp bevat informatie over de functie waarmee schaaleenheden kunnen worden gebruikt om geselecteerde processen uit te voeren vanuit de magazijnbeheer-workload.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9bdb9529c8b630182a2036e9d116909f9e92bb83
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944408"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Niet alle magazijnbeheerbedrijfsfunctionaliteit wordt volledig ondersteund voor magazijnen met een werkbelasting voor een schaaleenheid. Zorg ervoor dat u alleen de processen gebruikt die in dit onderwerp expliciet worden ondersteund.

## <a name="warehouse-execution-on-scale-units"></a>Magazijnuitvoering op schaaleenheden

Deze functie schakelt schaaleenheden in om geselecteerde processen van de magazijnbeheermogelijkheden uit te voeren.

In dit onderwerp worden magazijnuitvoeringen in een magazijn dat is gedefinieerd als een schaaleenheid een *Warehouse Execution System* (*WES*) genoemd.

## <a name="prerequisites"></a>Vereisten

U moet beschikken over een Dynamics 365 Supply Chain Management-hub en een schaaleenheid die met de magazijnbeheerworkload is geïmplementeerd. Zie [Gebruik schaaleenheden om de ondersteuning voor workloads in Supply Chain Management te vergroten](cloud-edge-landing-page.md) voor meer informatie over de architectuur en het implementatieproces.

## <a name="how-the-wes-workload-works-on-scale-units"></a>Hoe de WES-workload werkt op schaaleenheden

Voor de processen in de magazijnbeheer-workload worden de gegevens gesynchroniseerd tussen de hub en de schaaleenheden.

Een schaaleenheid kan alleen de gegevens behouden waarvan deze eigenaar is. Het concept gegevenseigendom voor schaaleenheden helpt multi-masterconflicten te voorkomen. Het is daarom belangrijk dat u begrijpt welke processen eigendom zijn van de hub en welke van de schaaleenheden.

De schaaleenheden zijn eigenaar van de volgende gegevens:

- **Gegevens verzendingswave verwerken**: geselecteerde wave-procesmethoden worden behandeld als onderdeel van de wave-verwerking in de schaaleenheid.
- **Werkverwerkingsgegevens**: Magazijnwerk dat is gemaakt op een schaaleenheid wordt eigendom van deze specifieke schaaleenheid. De volgende typen verwerking van werkorders worden ondersteund:

  - **Voorraadmutaties** (handmatig verplaatsen en verplaatsen door sjabloonwerk)
  - **Cyclustelling** en het goedkeurings-/afwijzingsproces als onderdeel van telbewerkingen
  - **Inkooporders** (wegzetwerk via een magazijnorder wanneer inkooporders niet aan ladingen zijn gekoppeld)
  - **Verkooporders** (eenvoudig verzamel- en laadwerk)
  - **overboekingsorders** (alleen uitgaand met eenvoudig order verzamelen en laden)

- **Ontvangstgegevens voor magazijnorders**: deze gegevens worden alleen gebruikt voor inkooporders die handmatig naar een magazijn zijn vrijgegeven.
- **Nummerplaatgegevens**: nummerplaten kunnen op de hub en de schaaleenheid worden gemaakt. Er is toegewezen conflictafhandeling verstrekt. Deze gegevens zijn niet magazijnspecifiek.

## <a name="outbound-process-flow"></a>Uitgaande processtroom

De hub is eigenaar van de volgende gegevens:

- Alle brondocumenten, zoals verkooporders en overboekingsorders
- Ordertoewijzing en verwerking van uitgaande belasting
- De processen voor vrijgeven naar magazijn, verzendingen en waves maken, en voltooien van waves

De schaaleenheden zijn eigenaar van de feitelijke wave-verwerking (zoals werktoewijzing, aanvullingswerk en het maken van de vraag) nadat de wave is vrijgegeven. Daarom kunnen magazijnmedewerkers het uitgaande werk verwerken met behulp van een mobiele app Magazijnbeheer die is verbonden met de schaaleenheid.

![Waveverwerkingsstroom](./media/wes-wave-processing-ga.png "Waveverwerkingsstroom")

### <a name="process-work-and-ship"></a>Werk verwerken en verzenden

Zodra het uiteindelijke werkproces de voorraad op een uiteindelijke verzendlocatie (Laaddeur) plaatst, meldt de schaaleenheid aan de hub dat de voorraadtransacties van het brondocument moeten worden bijgewerkt naar *Verzameld*. Totdat dit proces wordt uitgevoerd en gesynchroniseerd, wordt de voorhanden voorraad op de workload van de schaaleenheid fysiek gereserveerd op magazijnniveau.

Zodra de hub de transacties heeft bijgewerkt naar *Verzameld*, kan het de bevestiging van de uitgaande zending en de bijbehorende verkooppakbon of transferorderzending verwerken voor de lading.

![Verwerkingsstroom voor uitgaande goederen](./media/WES-outbound-processing-19.png "Verwerkingsstroom voor uitgaande goederen")

## <a name="inbound-process-flow"></a>Inkomende processtroom

De hub is eigenaar van de volgende gegevens:

- Alle brondocumenten, zoals inkooporders en verkoopretourorders
- Inkomende ladingverwerking
- Alle kosten en financiële updates

> [!NOTE]
> De inkomende inkooporderstroom is conceptueel verschillend van de uitgaande stroom. U kunt hetzelfde magazijn voor de schaaleenheid of de hub gebruiken, afhankelijk van of de inkooporder naar het magazijn is vrijgegeven. Wanneer u een order naar het magazijn hebt vrijgegeven, kunt u alleen met die order werken terwijl u zich hebt aangemeld bij de schaaleenheid.
>
> Als u het proces *Vrijgeven naar magazijn* gebruikt, worden [*magazijnorders*](cloud-edge-warehouse-order.md) gemaakt en wordt het eigendom van de gerelateerde ontvangende stroom toegewezen aan de schaaleenheid. De hub kan inkomende ontvangst niet registreren.

U moet zich aanmelden bij de hub om het proces *Vrijgeven aan magazijn* te gebruiken. Ga naar een van de volgende pagina's om uit te voeren of te plannen:

- **Inkoopbeheer > Inkooporders > Alle inkooporders > Magazijn > Acties > Vrijgeven aan magazijn**
- **Magazijnbeheer > Vrijgave naar magazijn > Automatische vrijgave van inkooporders**

Wanneer u **Automatische vrijgave van inkooporders** gebruikt, kunt u specifieke inkooporderregels selecteren op basis van een query. Een standaardscenario is het instellen van een terugkerende batchtaak waarbij alle bevestigde inkooporderregels worden vrijgegeven die naar verwachting de volgende dag zullen binnenkomen.

De medewerker kan het ontvangstproces uitvoeren met behulp van een mobiele app Magazijnbeheer die is verbonden met de schaaleenheid. De gegevens worden vervolgens door de schaaleenheid geregistreerd en gerapporteerd voor de inkomende magazijnorder. Het maken en verwerken van de volgende wegzetactie wordt ook afgehandeld door de schaaleenheid.

Als u het proces van *vrijgave naar magazijn* niet gebruikt en dus geen *magazijnorders* gebruikt, kan de hub de magazijnontvangst en de werkverwerking onafhankelijk van schaaleenheden verwerken.

![Inkomende processtroom](./media/wes-inbound-ga.png "Inkomende processtroom")

Wanneer u registratie van inkomende goederen uitvoert via een ontvangstproces van een magazijnapp voor de magazijnorder van de schaaleenheid, meldt de workload van de schaaleenheid aan de hub dat de gerelateerde inkooporderregeltransacties moeten worden bijgewerkt naar *Geregistreerd*. Als dit is voltooid, kunt u een productontvangstbon voor een inkooporder uitvoeren op de hub.

![Verwerkingsstroom voor inkomende goederen](./media/WES-inbound-processing-19.png "Verwerkingsstroom voor inkomende goederen")

## <a name="supported-processes-and-roles"></a>Ondersteunde processen en rollen

Niet alle magazijnbeheerprocessen worden in een WES-workload voor een schaaleenheid ondersteund. Daarom is het raadzaam rollen toe te wijzen die overeenkomen met de functionaliteit die voor elke gebruiker beschikbaar is.

Ter vereenvoudiging van dit proces is een voorbeeldrol met de naam *Magazijnbeheerder bij workload* opgenomen in de demogegevens bij **Systeembeheer \> Beveiliging \> Beveiligingsconfiguratie**. Het doel van deze rol is magazijnbeheerders toegang geven tot de WES op de schaaleenheid. De rol geeft toegang tot de pagina's die relevant zijn in de context van een workload die op een schaaleenheid wordt gehost.

Gebruikersrollen op een schaaleenheid worden toegewezen als onderdeel van de oorspronkelijke gegevenssynchronisatie van de hub naar de schaaleenheid.

Als u de rollen wilt wijzigen die aan een gebruiker zijn toegewezen, gaat u naar **Systeembeheer \> Beveiliging \> Gebruikers aan rollen toewijzen**. Gebruikers die alleen als magazijnbeheerders werken, moeten alleen de rol *Magazijnbeheerder bij workload* toegewezen krijgen. Op deze manier zorgt u ervoor dat gebruikers alleen toegang hebben tot de ondersteunde functies. Verwijder alle andere rollen die aan deze gebruikers zijn toegewezen.

Gebruikers die als magazijnbeheerders werken op de hub én schaaleenheden, moeten de bestaande rol *Magazijnmedewerker* toegewezen krijgen. Houd er rekening mee dat magazijnmedewerkers toegang hebben tot functies (zoals de ontvangstverwerking van overboekingsorders) die in de gebruikersinterface worden weergegeven, maar die momenteel niet worden ondersteund voor schaaleenheden.

## <a name="supported-wes-processes"></a>Ondersteunende WES-processen

De volgende processen voor magazijnuitvoering kunnen worden ingeschakeld voor een WES-workload op een schaaleenheid:

- Geselecteerde wavemethoden voor verkoop- en overboekingsorders (toewijzing, vraagaanvulling, containervorming, maken van werk en afdrukken van wavelabels)

- Magazijnwerk voor verkoop- en transferorders verwerken met de magazijn-app (inclusief aanvullingswerk)
- Zoeken in voorhanden voorraad met behulp van de magazijn-app
- Voorraadmutaties maken en uitvoeren met behulp van de magazijn-app
- Werk voor een telcyclus maken en verwerken met de magazijn-app
- Voorraadcorrecties maken met de magazijn-app
- Inkooporders registreren en wegzetwerk doen met de magazijn-app

De volgende werkordertypen worden momenteel ondersteund voor WES-workloads op schaaleenheid-implementaties:

- Verkooporders
- Overboekingsuitgifte
- Aanvulling
- Voorraadmutatie
- Cyclustelling
- Inkooporders (gekoppeld aan magazijnorders)

Er wordt momenteel geen verwerking van andere typen brondocumenten of magazijnwerk ondersteund voor schaaleenheden. Voor bijvoorbeeld een WES-workload voor een schaaleenheid kunt u geen proces voor het ontvangen van overboekingsorders (ontvangst transfer) uitvoeren; dit moet worden uitgevoerd door het hub-exemplaar.

> [!NOTE]
> Menu-items en knoppen voor mobiele apparaten voor niet-ondersteunde functies worden niet weergegeven in de _mobiele app Magazijnbeheer_ wanneer deze is verbonden met een schaaleenheidimplementatie.

> [!WARNING]
> Als u een workload uitvoert voor een schaaleenheid, kunt u geen niet-ondersteunde processen voor dat specifieke magazijn op de hub uitvoeren. De tabellen die later in dit onderwerp worden verstrekt, documenteren de ondersteunde capaciteiten.
>
> Geselecteerde magazijnwerktypen kunnen zowel voor de hub als voor schaaleenheden worden gemaakt. Deze werktypen kunnen echter alleen worden beheerd door de eigenaar van de hub of schaaleenheid (de implementatie waardoor de gegevens zijn gemaakt).
>
> Zelfs wanneer een specifiek proces voor schaaleenheid wordt ondersteund, moet u er rekening mee houden dat niet alle benodigde gegevens worden gesynchroniseerd van de hub naar de schaaleenheid of van de schaaleenheid naar de hub, wat kan resulteren in onverwachte systeemverwerking. Voorbeelden zijn:
> 
> - Als u een query voor een locatie-instructie gebruikt die een gegevenstabelrecord samenvoegt die alleen bij de hubimplementatie bestaat.
> - Als u volumetrische laadfunctionaliteiten voor locatiestatus en/of locatie gebruikt. Deze gegevens worden niet gesynchroniseerd tussen de implementaties en werken daarom alleen bij het bijwerken van de locatievoorraad die beschikbaar is op een van de implementaties.

De volgende magazijnbeheerfunctionaliteit wordt momenteel niet ondersteund voor schaaleenheidworkloads:

- Inkomende verwerking van inkooporderregels die aan een belasting zijn toegewezen
- Inkomende verwerking van inkooporders voor een project
- Inkomende en uitgaande verwerking voor items met actieve traceringsdimensies **Eigenaar** en/of **Serienummer**
- Verwerking van voorraad met een blokkeringsstatuswaarde
- Een voorraadstatus wijzigen tijdens een werkverplaatsingsproces
- Order-toegezegde flexibel reserveringsbeleid voor dimensies op magazijnniveau
- Gebruik van de functionaliteit *Magazijnlocatiestatus* (de gegevens worden niet gesynchroniseerd tussen de implementaties)
- Gebruik van de functionaliteit *Positionering van locatie nummerplaat*
- Gebruik van *Productfilters* en *Productfiltergroepen*, inclusief de instelling **Aantal dagen om batches te mengen**
- Integratie met kwaliteitsbeheer
- Verwerking met catch weight-artikelen
- Verwerking met artikelen alleen ingeschakeld voor Transportbeheer (TMS)
- Verwerking met negatieve voorhanden voorraad
- Magazijnwerkverwerking met aangepaste werktypen
- Magazijnwerkverwerking met verzendingsnotities
- Magazijnwerkverwerking met materiaalverwerking/magazijnautomatisering
- Gebruik van de installatiekopie met productmodelgegevens (bijvoorbeeld in de mobiele app Magazijnbeheer)

> [!WARNING]
> Een aantal magazijnfuncties is niet beschikbaar voor magazijnen met de werkbelasting van magazijnbeheer voor een schaaleenheid en wordt ook niet ondersteund voor de werkbelasting van de hub of schaaleenheid.
> 
> Andere capaciteiten kunnen bij beide worden verwerkt, maar vereisen in sommige scenario's zorgvuldig gebruik, bijvoorbeeld wanneer de voorhanden voorraad voor hetzelfde magazijn wordt bijgewerkt voor de hub als de schaaleenheid vanwege het asynchrone bijwerkproces van gegevens.
> 
> Specifieke functies (zoals *blokkeren van werk*) die worden ondersteund voor zowel de hub als schaaleenheden, worden alleen ondersteund voor de eigenaar van de gegevens.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Uitgaand (wordt alleen ondersteund voor verkoop- en overboekingsorders)

In de volgende tabel ziet u welke uitgaande functies worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                                      | Hub | WES-workload op een schaaleenheid |
|--------------------------------------------------------------|-----|------------------------------|
| Brondocumenten verwerken                                   | Ja | No |
| Laad- en transportbeheer verwerken                | Ja | No |
| Vrijgeven aan magazijn                                         | Ja | No |
| Gepland cross-docken                                        | No  | No |
| Zendingen samenvoegen                                       | Ja | No |
| Verzendingswaves verwerken                                     | Ja, maar alleen initialiseren en voltooien van de wave wordt op de hub verwerkt. Dit houdt in dat de verwerking van uitgaande transfer- en verkooporders alleen kan worden uitgevoerd door de schaaleenheid.|<p>Nee, de initialisatie en voltooiing worden uitgevoerd door de hub en **Ladingopbouw en sorteren** worden niet ondersteund.<p><b>Opmerking:</b> toegang tot de hub is vereist voor het voltooien van de wave-status als onderdeel van de wave-verwerking.</p> |
| Zendingen onderhouden voor wave                                  | Ja | No |
| Magazijnwerk verwerken (inclusief nummerplaat afdrukken)        | No  | <p>Ja, maar alleen voor de bovengenoemde ondersteunde capaciteiten. |
| Orderverzamelen van cluster                                              | No  | Ja|
| Handmatige verpakkingsverwerking, incl. verwerking van werk 'Orderverzameling voor ingepakte container' | No <P>Bepaalde verwerking kan worden uitgevoerd nadat een oorspronkelijk orderverzamelproces is verwerkt door een schaaleenheid. Dit wordt echter afgeraden vanwege volgende geblokkeerde bewerkingen.</p>  | No |
| Container verwijderen uit groep                                  | No  | No |
| Uitgaande sorteringen verwerken                                  | No  | No |
| Lading-gerelateerde documenten afdrukken                           | Ja | No |
| Vrachtbrief en ASN-generatie                            | Ja | No |
| Verzendbevestiging                                             | Ja | No |
| Zendingsbevestiging met 'Bevestigen en overboeking'            | No  | No |
| Verwerking van pakbon en facturering                        | Ja | No |
| Korte orderverzameling (verkoop- en overboekingsorders)                    | No  | No |
| Meerverzameling (verkoop- en overboekingsorders)                     | No  | No |
| Wijziging van werklocaties (verkoop- en overboekingsorders)         | No  | Ja|
| Werk voltooien (verkoop- en overboekingsorders)                    | No  | Ja|
| Werkrapport afdrukken                                            | Ja | No |
| Wavelabel                                                   | No  | Ja|
| Werk splitsen                                                   | No  | Ja|
| Werkverwerking - Gestuurd door 'Transportlading'            | No  | No |
| Opgenomen hoeveelheid reduceren                                       | No  | No |
| Werk omkeren                                                 | No  | No |
| Verzendbevestiging omkeren                                | Ja | No |

### <a name="inbound"></a>Inkomend

In de volgende tabel ziet u welke inkomende functies worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                                          | Hub | WES-workload op een schaaleenheid<BR>*(Artikelen met "Ja" zijn alleen van toepassing op magazijnorders)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Bron&nbsp;documenten&nbsp;verwerken                             | Ja | No |
| Laad- en transportbeheer verwerken                    | Ja | No |
| Bevestiging inkomende zending                                    | Ja | No |
| Vrijgave inkooporder naar magazijn (magazijnorderverwerking) | Ja | No |
| Annulering van magazijnorderregels<p>Dit wordt alleen ondersteund als er geen registratie voor de regel heeft plaatsgevonden.</p> | Ja | No |
| Ontvangen en wegzetten van inkooporderartikel                       | <p>Ja,&nbsp;wanneer&nbsp;er&nbsp;geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, wanneer een inkooporder geen deel uitmaakt van een <i>belasting</i></p> |
| Ontvangen van inkooporderregel en wegzetten                       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, wanneer een inkooporder geen deel uitmaakt van een <i>belasting</i></p></p> |
| Ontvangen en wegzetten van retourorder                              | Ja | No |
| Nummerplaat ontvangen en wegzetten                       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Artikelontvangst laden                                              | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen en wegzetten van nummerplaat                             | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen en wegzetten van artikel voor overboekingorder                       | Ja | No |
| overboekingsorderregel ontvangen en wegzetten                       | Ja | No |
| Werk annuleren (inkomende)                                            | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, maar alleen als de optie <b>Ontvangst ongedaan maken bij annulering van werk</b> (op de pagina <b>Parameters voor magazijnbeheer</b>) wordt uitgeschakeld</p> |
| Inkooporder productontvangstbon verwerken                        | Ja | No |
| Ontvangen van inkooporder met minderlevering                      | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Ja, maar alleen door een annuleringsaanvraag vanuit de hub te maken |
| Ontvangen van inkooporder met meerlevering                       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | Ja  |
| Ontvangen met aanmaak van werk *Cross-docken*                 | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen met aanmaak van werk *Kwaliteitsorder*                  | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen met aanmaak van werk *Bemonstering kwaliteitsartikel*          | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen met aanmaak van werk *Kwaliteit in kwaliteitscontrole*       | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen met aanmaak van kwaliteitsorder                            | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Werkverwerking - Gestuurd door *Clusteropslag*                 | Ja | No |
| Werkverwerking met *Kort orderverzamelen*                               | Ja | No |
| Nummerplaatlading                                           | Ja | Ja |

### <a name="warehouse-operations-and-exception-handing"></a>Magazijnbewerkingen en uitzonderingen afhandelen

In de volgende tabel ziet u welke functies voor magazijnbewerkingen en het afhandelen van uitzonderingen worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                            | Hub | WES-workload op een schaaleenheid |
|----------------------------------------------------|-----|------------------------------|
| Nummerplaatonderzoek                              | Ja | Ja                          |
| Artikelonderzoek                                       | Ja | Ja                          |
| Locatieonderzoek                                   | Ja | Ja                          |
| Magazijn wijzigen                                   | Ja | Ja                          |
| Mutatie                                           | Ja | Ja                          |
| Mutatie door sjabloon                               | Ja | Ja                          |
| Magazijntransfer                                 | Ja | No                           |
| Transferorders maken vanuit de magazijn-app           | Ja | No                           |
| Correctie (in/uit)                                | Ja | Ja, maar niet voor het scenario 'Correctie uit', waarin voorraadreservering moet worden verwijderd met de instelling **Reserveringen verwijderen** voor de voorraadcorrectietypen.</p>                           |
| Wijziging van voorraadstatus                            | Ja | No                           |
| Cyclustelling en Telverschillen verwerken | Ja | Ja                           |
| Label opnieuw afdrukken (nummerplaat afdrukken)             | Ja | Ja                          |
| Nummerplaat-build                                | Ja | No                           |
| Nummerplaat onderbreken                                | Ja | No                           |
| Verpakken naar geneste nummerplaten                                | Ja | No                           |
| Inchecken chauffeur                                    | Ja | No                           |
| Uitchecken chauffeur                                   | Ja | No                           |
| Batchbeschikkingscode wijzigen                      | Ja | Ja                          |
| Geopende werklijst weergeven                             | Ja | Ja                          |
| Nummerplaten consolideren                         | Ja | No                           |
| Verwerking van min/max en zonedrempelaanvulling| Ja <p>Het wordt afgeraden dezelfde locaties als onderdeel van de query's op te nemen.</p>| Ja                          |
| Aanvulling van vakken verwerken                  | Ja  | Ja<p>Houd er rekening mee dat de instelling moet worden uitgevoerd voor de schaaleenheid</p>                           |
| Werk blokkeren en deblokkeren                             | Ja | Ja                          |
| Gebruiker wijzigen                                        | Ja | Ja                          |
| Werkgroep voor werk wijzigen                           | Ja | Ja                          |
| Werk annuleren                                        | Ja | Ja                          |


### <a name="production"></a>Productie

Productiescenario's voor magazijnbeheer worden momenteel niet ondersteund voor schaaleenheidworkloads, zoals aangegeven in de volgende tabel.

| Proces | Hub | WES-workload op een schaaleenheid |
|---------|-----|------------------------------|
| <p>Alle magazijnbeheerprocessen die betrekking hebben op productie. Hieronder volgen een aantal voorbeelden:</p><li>Vrijgeven aan magazijn</li><li>Productie-waves verwerken</li><li>Orderverzameling van grondstoffen</li><li>RAF en eindproducten wegzetten</li><li>Coproducten en bijproducten wegzetten</li><li>Kanban wegzetten</li><li>Kanbanorderverzameling</li><li>Productieorder beginnen</li><li>Productie-uitval</li><li>Laatste pallet van productie</li><li>Materiaalverbruik registreren</li><li>Lege Kanban</li></ul> | Ja | No |

## <a name="maintaining-scale-units-for-wes"></a>Schaaleenheden voor WES onderhouden

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
