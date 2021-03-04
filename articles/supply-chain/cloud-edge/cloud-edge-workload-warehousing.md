---
title: Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden
description: Dit onderwerp bevat informatie over de functie waarmee schaaleenheden kunnen worden gebruikt om geselecteerde processen uit te voeren vanuit de magazijnbeheer-workload.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516758"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Niet alle bedrijfsfuncties worden volledig ondersteund in de openbare preview wanneer workloadschaaleenheden worden gebruikt. Zorg ervoor dat u alleen de processen gebruikt die in dit onderwerp expliciet worden ondersteund.

## <a name="warehouse-execution-on-scale-units"></a>Magazijnuitvoering op schaaleenheden

Deze functie schakelt schaaleenheden in om geselecteerde processen van de magazijnbeheermogelijkheden uit te voeren. Cloud-schaaleenheden voeren hun workloads uit in de cloud met behulp van de toegewezen verwerkingscapaciteit in de door u geselecteerde Microsoft Azure-regio. Voor edge-schaaleenheden kunt u bepaalde workloads onafhankelijk on-premises uitvoeren, zelfs als de schaaleenheden tijdelijk niet verbonden zijn met de cloud.

In dit onderwerp worden magazijnuitvoeringen in een magazijn dat is gedefinieerd als een schaaleenheid een *Warehouse Execution System* (*WES*) genoemd.

## <a name="prerequisites"></a>Vereisten

U moet beschikken over een Dynamics 365 Supply Chain Management-hub en een schaaleenheid die met de magazijnbeheerworkload is geïmplementeerd. Zie [Cloud- en edge-schaaleenheden voor productie- en magazijnbeheerworkloads](cloud-edge-landing-page.md) voor meer informatie over de architectuur en het implementatieproces.

## <a name="how-the-wes-workload-works-on-scale-units"></a>Hoe de WES-workload werkt op schaaleenheden

Voor de processen in de magazijnbeheer-workload worden de gegevens gesynchroniseerd tussen de hub en de schaaleenheden.

Een schaaleenheid kan alleen de gegevens behouden waarvan deze eigenaar is. Het concept gegevenseigendom voor schaaleenheden helpt multi-masterconflicten te voorkomen. Het is daarom belangrijk dat u begrijpt welke processen eigendom zijn van de hub en welke van de schaaleenheden.

De schaaleenheden zijn eigenaar van de volgende gegevens:

- **Wave-verwerkingsgegevens**: geselecteerde wave-procesmethoden worden behandeld als onderdeel van de schaaleenheid voor wave-verwerking.
- **Werkverwerkingsgegevens**: de volgende typen werkorderverwerking worden ondersteund:

    - Voorraadmutaties (handmatig verplaatsen en verplaatsen door sjabloonwerk)
    - Inkooporders (wegzetwerk via een magazijnorder)
    - Verkooporders (eenvoudig verzamel- en laadwerk)

- **Ontvangstgegevens voor magazijnorders**: deze gegevens worden alleen gebruikt voor inkooporders die handmatig naar een magazijn worden vrijgegeven.
- **Nummerplaatgegevens**: nummerplaten kunnen op de hub en de schaaleenheid worden gemaakt. Er is toegewezen conflictafhandeling verstrekt. Deze gegevens zijn niet magazijnspecifiek.

## <a name="outbound-process-flow"></a>Uitgaande processtroom

De hub is eigenaar van de volgende gegevens:

- Alle brondocumenten, zoals verkooporders en transferorders
- Ordertoewijzing en verwerking van uitgaande belasting
- De processen voor vrijgeven naar magazijn, verzendingen en waves maken

De schaaleenheden zijn eigenaar van de feitelijke wave-verwerking (zoals werktoewijzing, aanvullingswerk en het maken van de vraag) nadat de wave is vrijgegeven. Daarom kunnen magazijnmedewerkers het uitgaande werk verwerken met behulp van een magazijn-app die is verbonden met de schaaleenheid.

![Waveverwerkingsstroom](./media/wes_wave_processing_flow.png "Waveverwerkingsstroom")

## <a name="inbound-process-flow"></a>Inkomende processtroom

De hub is eigenaar van de volgende gegevens:

- Alle brondocumenten, zoals inkooporders en verkoopretourorders
- Inkomende ladingverwerking

> [!NOTE]
> De inkomende inkooporderstroom verschilt conceptueel van de uitgaande stroom, waarbij de schaaleenheid die de verwerking doet, afhankelijk is van het feit of de order is vrijgegeven in een magazijn.

Als u het proces *vrijgeven naar magazijn* gebruikt, worden magazijnorders gemaakt en wordt het eigendom van de gerelateerde ontvangende stroom toegewezen aan de schaaleenheid. De hub kan inkomende ontvangst niet registreren.

De medewerker kan het ontvangstproces uitvoeren met behulp van een magazijn-app die is verbonden met de schaaleenheid. De gegevens worden vervolgens door de schaaleenheid geregistreerd en gerapporteerd voor de inkomende magazijnorder. Het maken en verwerken van de volgende wegzetactie wordt ook afgehandeld door de schaaleenheid.

Als u het proces van *vrijgave naar magazijn* niet gebruikt en dus geen *magazijnorders* gebruikt, kan de hub de magazijnontvangst en de werkverwerking onafhankelijk van schaaleenheden verwerken.

![Inkomende processtroom](./media/wes_Inbound_flow.png "Inkomende processtroom")

## <a name="supported-processes-and-roles"></a>Ondersteunde processen en rollen

Niet alle magazijnbeheerprocessen worden in een WES-workload voor een schaaleenheid ondersteund. Daarom is het raadzaam rollen toe te wijzen die overeenkomen met de functionaliteit die voor elke gebruiker beschikbaar is.

Ter vereenvoudiging van dit proces is een voorbeeldrol met de naam *Magazijnbeheerder bij workload* opgenomen in de demogegevens bij **Systeembeheer \> Beveiliging \> Beveiligingsconfiguratie**. Het doel van deze rol is magazijnbeheerders toegang geven tot de WES op de schaaleenheid. De rol geeft toegang tot de pagina's die relevant zijn in de context van een workload die op een schaaleenheid wordt gehost.

Gebruikersrollen op een schaaleenheid worden toegewezen als onderdeel van de oorspronkelijke gegevenssynchronisatie van de hub naar de schaaleenheid.

Als u de rollen wilt wijzigen die aan een gebruiker zijn toegewezen, gaat u naar **Systeembeheer \> Beveiliging \> Gebruikers aan rollen toewijzen** op de schaaleenheid. Gebruikers die alleen als magazijnbeheerders werken, moeten alleen de rol *Magazijnbeheerder bij workload* toegewezen krijgen. Op deze manier zorgt u ervoor dat gebruikers alleen toegang hebben tot de ondersteunde functies. Verwijder alle andere rollen die aan deze gebruikers zijn toegewezen.

Gebruikers die als magazijnbeheerders werken op de hub én schaaleenheden, moeten de bestaande rol *Magazijnmedewerker* toegewezen krijgen. Houd er rekening mee dat magazijnmedewerkers toegang hebben tot functies (zoals de transfer van inkooporders) die in de gebruikersinterface worden weergegeven, maar die momenteel niet worden ondersteund op schaaleenheden.

## <a name="supported-wes-processes"></a>Ondersteunende WES-processen

De volgende processen voor magazijnuitvoering kunnen worden ingeschakeld voor een WES-workload op een schaaleenheid:

- Geselecteerde wave-methoden voor verkooporders en vraagaanvulling
- Werkorders van verkooporders en vraagaanvulling uitvoeren met behulp van de magazijn-app
- Zoeken in voorhanden voorraad met behulp van de magazijn-app
- Voorraadmutaties maken en uitvoeren met behulp van de magazijn-app
- Inkooporders registreren en wegzetwerk doen met de magazijn-app

De volgende werkordertypen worden momenteel ondersteund voor WES-workloads op schaaleenheid-implementaties:

- Verkooporders
- Aanvulling
- Voorraadmutatie
- Inkooporders die zijn gekoppeld aan magazijnorders

Er wordt momenteel geen andere verwerking van brondocumenten ondersteund op schaaleenheden. Voor een WES-workload op een schaaleenheid kunt u de volgende acties bijvoorbeeld niet uitvoeren:

- Een transferorder vrijgeven.
- De uitgaande verzamel- en verzendwerkzaamheden voor het magazijn verwerken.

> [!IMPORTANT]
> Als u een workload gebruikt op een schaaleenheid, kunt u geen niet-ondersteunde processen voor het specifieke magazijn op de hub uitvoeren.

De volgende magazijnbeheerfunctionaliteit wordt momenteel niet ondersteund voor schaaleenheden:

- Inkomende en uitgaande verwerking voor items met actieve traceringsdimensies (zoals batch- of serienummerdimensies)
- Verwerking van wijzigingen in de voorraadstatus
- Verwerking van voorraad met een blokkeringsstatuswaarde
- Integratie met kwaliteitsbeheer
- Integratie met productie
- Verwerking van catch weight-artikelen
- Verwerking van meerlevering en onderlevering
- Verwerking van negatieve voorhanden voorraad

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Uitgaand (wordt alleen ondersteund voor verkooporders en vraagaanvulling)

In de volgende tabel ziet u welke uitgaande functies worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

> [!WARNING]
> Omdat alleen verkooporderverwerking wordt ondersteund, kan de uitgaande magazijnbeheerverwerking niet worden gebruikt voor transferorders.
>
> Sommige magazijnfuncties zijn niet beschikbaar in magazijnen waarop de magazijnbeheer-workloads worden uitgevoerd in een schaaleenheid.

| Proces                                                      | Hub | WES-workload op een schaaleenheid |
|--------------------------------------------------------------|-----|------------------------------|
| Brondocumenten verwerken                                   | Ja | No |
| Laad- en transportbeheer verwerken                | Ja | No |
| Vrijgeven aan magazijn                                         | Ja | No |
| Zendingen samenvoegen                                       | No  | No |
| Cross-docken (verzamelwerk)                                 | No  | No |
| Verzendingswaves verwerken                                     | Nee, maar voltooien van de wave-status wordt op de hub verwerkt |<p>Ja, maar de volgende mogelijkheden worden niet ondersteund:</p><ul><li>Parallelwerk maken</li><li>Ladingopbouw en sorteren</li><li>Containervorming</li><li>Wavelabels afdrukken</li></li></ul><p><b>Opmerking:</b> toegang tot de hub is vereist voor het voltooien van de wave-status als onderdeel van de wave-verwerking.</p> |
| Magazijnwerk verwerken (inclusief nummerplaat afdrukken)     | No  | <p>Ja, maar alleen voor de volgende mogelijkheden:</p><ul><li>Orderverzamelen (zonder het gebruik van actieve traceringsdimensies)</li><li>Orders laden (zonder het gebruik van actieve traceringsdimensies)</li></ul> |
| Orderverzamelen van cluster                                              | No  | No |
| Verpakkingen verwerken                                           | No  | No |
| Uitgaande sorteringen verwerken                                  | No  | No |
| Lading-gerelateerde documenten afdrukken                           | Ja | No |
| Vrachtbrief en ASN-generatie                            | Ja | No |
| Verzendbevestiging en pakbonverwerking                | Ja | No |
| Korte orderverzameling (verkooporders)                                 | No  | No |
| Werkannulering                                            | No  | No |
| Wijziging van werklocaties (verkooporders)                      | No  | No |
| Werk voltooien (verkooporders)                                 | No  | No |
| Werk blokkeren en deblokkeren                                       | No  | No |
| Gebruiker wijzigen                                                  | No  | No |
| Werkrapport afdrukken                                            | No  | No |
| Wavelabel                                                   | No  | No |
| Werk omkeren                                                 | No  | No |

### <a name="inbound"></a>Inkomend

In de volgende tabel ziet u welke inkomende functies worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                                          | Hub | WES-workload op een schaaleenheid |
|------------------------------------------------------------------|-----|------------------------------|
| Bron&nbsp;documenten&nbsp;verwerken                                       | Ja | No |
| Laad- en transportbeheer verwerken                    | Ja | No |
| Verzendbevestiging                                            | Ja | No |
| Vrijgave inkooporder naar magazijn (magazijnorderverwerking) | Ja | No |
| Ontvangen en wegzetten van inkooporderartikel                        | <p>Ja,&nbsp;wanneer&nbsp;er&nbsp;geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, wanneer er een magazijnorder is en wanneer een inkooporder geen deel uitmaakt van een <i>lading</i>. U moet echter twee menuopdrachten voor mobiele apparaten gebruiken, één voor ontvangst (<i>Ontvangst van een inkooporderartikel</i>) en een andere, met de optie <b>Bestaand werk gebruiken</b> ingeschakeld om het wegzetten te verwerken.</p><p>Nee, wanneer er geen magazijnorder is.</p> |
| Ontvangen van inkooporderregel en wegzetten                        | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen en wegzetten van retourorder                               | Ja | No |
| Nummerplaat ontvangen en wegzetten                        | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Artikelontvangst laden                                              | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen en wegzetten van nummerplaat                              | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |
| Ontvangen en wegzetten van artikel voor overboekingorder                        | Ja | No |
| Transferorderregel ontvangen en wegzetten                        | Ja | No |
| Werkannulering                                                | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | <p>Ja, maar de optie <b>Ontvangst ongedaan maken bij annulering van werk</b> (op de pagina <b>Parameters voor magazijnbeheer</b>) wordt niet ondersteund.</p> |
| Inkooporder productontvangstbon verwerken                        | Ja | No |
| Cross-dock-werk maken als onderdeel van de ontvangst                 | <p>Ja, wanneer er geen magazijnorder is</p><p>Nee, wanneer er een magazijnorder is</p> | No |

### <a name="warehouse-operations-and-exception-handing"></a>Magazijnbewerkingen en uitzonderingen afhandelen

In de volgende tabel ziet u welke functies voor magazijnbewerkingen en het afhandelen van uitzonderingen worden ondersteund en waar deze worden ondersteund, wanneer de workloads van magazijnbeheer worden gebruikt in cloud- en edge-schaaleenheden.

| Proces                                            | Hub | WES-workload op een schaaleenheid |
|----------------------------------------------------|-----|------------------------------|
| Nummerplaatonderzoek                              | Ja | Ja                          |
| Artikelonderzoek                                       | Ja | Ja                          |
| Locatieonderzoek                                   | Ja | Ja                          |
| Magazijn wijzigen                                   | Ja | Ja                          |
| Mutatie                                           | No  | Ja                          |
| Mutatie door sjabloon                               | No  | Ja                          |
| Correctie (in/uit)                                | Ja | No                           |
| Cyclustelling en Telverschillen verwerken | Ja | No                           |
| Label opnieuw afdrukken (nummerplaat afdrukken)             | Ja | No                           |
| Nummerplaat-build                                | Ja | No                           |
| Nummerplaat onderbreken                                | Ja | No                           |
| Inchecken chauffeur                                    | Ja | No                           |
| Uitchecken chauffeur                                   | Ja | No                           |
| Batchbeschikkingscode wijzigen                      | Ja | No                           |
| Geopende werklijst weergeven                             | Ja | No                           |
| Nummerplaten consolideren                         | No  | No                           |
| Container verwijderen uit groep                        | No  | No                           |
| Werk annuleren                                        | No  | No                           |
| Min./max. aanvulling verwerken                   | No  | No                           |
| Aanvulling van vakken verwerken                  | No  | No                           |

### <a name="production"></a>Productie

Magazijnbeheerintegratie voor productiescenario's wordt momenteel niet ondersteund, zoals aangegeven in de volgende tabel.

| Proces | Hub | WES-workload op een schaaleenheid |
|---------|-----|------------------------------|
| <p>Alle magazijnbeheerprocessen die betrekking hebben op productie. Hieronder volgen een aantal voorbeelden:</p><li>Vrijgeven aan magazijn</li><li>Productie-waves verwerken</li><li>Orderverzameling van grondstoffen</li><li>Eindproducten wegzetten</li><li>Coproducten en bijproducten wegzetten</li><li>Kanban wegzetten</li><li>Kanbanorderverzameling</li><li>Productieorder beginnen</li><li>Productie-uitval</li><li>Laatste pallet van productie</li><li>Materiaalverbruik registreren</li><li>Lege Kanban</li></ul> | No | No |

## <a name="maintaining-scale-units-for-wes"></a>Schaaleenheden voor WES onderhouden

Er worden verschillende batchtaken uitgevoerd op de hub en schaaleenheden.

In de implementatie van de hub kunt u de batchtaken handmatig onderhouden. U kunt de volgende drie taken beheren in **Magazijnbeheer \> Periodieke taken \> Backoffice workloadbeheer**:

- Bijwerkgebeurtenissen voor werkstatus verwerken
- Overdrachtsgebeurtenissen van de controle op de waveuitvoering verwerken
- Ontvangsten van bronorders registreren

Op de workload in schaaleenheden kunt u de volgende twee batchtaken beheren in **Magazijnbeheer \> Periodieke taken \> Workloadbeheer**:

- Wavetabelrecords verwerken
- Overdrachtsgebeurtenissen van de controle op de waveuitvoering verwerken


[!INCLUDE[footer-include](../../includes/footer-banner.md)]