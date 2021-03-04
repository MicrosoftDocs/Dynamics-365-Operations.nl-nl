---
title: Automatisering van incassoproces
description: In dit onderwerp wordt beschreven hoe u strategieën voor het incassoproces instelt waarmee automatisch klantfacturen worden geïdentificeerd waarvoor een e-mailherinnering of incasso-activiteit (zoals een telefoongesprek) vereist is of een aanmaningsbrief naar de klant moet worden verzonden.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: db59bad2ed3caf38f22bd4d6059e57747d1d983f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441833"
---
# <a name="collections-process-automation"></a>Automatisering van incassoproces

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u strategieën voor het incassoproces instelt waarmee automatisch klantfacturen worden geïdentificeerd waarvoor een e-mailherinnering of incasso-activiteit (zoals een telefoongesprek) vereist is of een aanmaningsbrief naar de klant moet worden verzonden. 

Organisaties besteden veel tijd aan het doorzoeken van verouderde balansrapporten, klantrekeningen en openstaande facturen om te bepalen met welke klanten contact moet worden opgenomen over een openstaande factuur of een openstaand rekeningsaldo. Dit onderzoek kost tijd die de incassomedewerker ook had kunnen besteden aan het communiceren met klanten om achterstallige saldi te innen of factuurgeschillen te verhelpen. Door het incassoproces te automatiseren, kunt u een strategie instellen voor uw incassoproces. Zo kunt u incasso-activiteiten consistent toepassen door aangepaste e-mailherinneringen of een geprogrammeerd proces voor het verzenden van aanmaningen te bieden. 

## <a name="collections-process-setup"></a>Instelling van incassoproces
U kunt de pagina **Instelling van incassoproces** (**Crediteringen en aanmaningen > Instellingen > Instelling van incassoproces**) gebruiken om een automatisch incassoproces te maken waarmee activiteiten worden gepland, e-mailberichten worden verzonden en klantaanmaningen worden gemaakt en geboekt. De processtappen zijn gebaseerd op de leidende of oudste openstaande factuur. In elke stap wordt deze factuur gebruikt om te bepalen welke communicatie of activiteit voor een bepaalde klant moet plaatsvinden.  

### <a name="process-hierarchy"></a>Proceshiërarchie
Elke klantverzameling kan slechts aan één proceshiërarchie worden toegewezen. De hiërarchiepositie van deze stap geeft aan welk proces prioriteit krijgt als een klant is opgenomen in meerdere verzamelingen waaraan een proceshiërarchie is toegewezen. De verzameling-id bepaalt welke klanten worden toegewezen aan het proces. 

De stille dagen worden gebruikt om ervoor te zorgen dat niet te vaak contact met een klant wordt opgenomen door het geautomatiseerde proces.  Als het aantal stille dagen bijvoorbeeld op twee is ingesteld, wordt door het geautomatiseerde proces gedurende ten minste twee dagen geen contact met de klant gemaakt, ook niet als de oorspronkelijke leidende factuur volledig is vereffend. 

Als u klanten wilt uitsluiten van de procesautomatisering als het rekeningsaldo of factuursaldo lager is dan een gedefinieerde waarde, stelt u het veld **Uitsluiten van proces** in op **Ja** en voert u de waarde van het bedrag in.

## <a name="process-details"></a>Procesgegevens
**Beschrijving** wordt gebruikt om het doel of de naam van de stap in de hiërarchie aan te duiden.

**Actietype** bepaalt of met de stap een activiteit wordt gemaakt, een e-mailbericht wordt verzonden of een aanmaning wordt gemaakt.

**Bedrijfsdocument** bepaalt welke sjabloon wordt gebruikt om het actietype te maken.  Dit kan een sjabloon voor een activiteit, een e-mailsjabloon of een aanmaning per klant zijn. 

De actietypen kunnen worden gemaakt voor of na de vervaldatum van de factuur, gebaseerd op de instelling die wordt weergegeven in de kolom **Dagen in relatie tot vervaldatum factuur**.

Wanneer u een actietype voor e-mail selecteert, wordt de ontvanger gebruikt om te bepalen of het een contactpersoon voor een klant, verkoopgroep of incassomedewerker is. De waarde in het veld **Contactpersoon voor zakelijk doel** bepaalt vervolgens welke contactpersoon van de account van die klant de communicatie ontvangt.

## <a name="business-document-details"></a>Bedrijfsdocumentdetails
De details van bedrijfsdocumenten zijn afhankelijk van het actietype dat is geselecteerd in de procesdetails.  Wanneer het actietype een activiteit is, worden de details van de activiteitsjabloon weergegeven.  Deze gegevens omvatten de naam van de activiteitsjabloon, het type activiteit dat wordt gemaakt, het doel van de activiteit, het aantal dagen dat is gepland om de activiteit te voltooien en de details van de activiteit.  Deze activiteit wordt vervolgens gekoppeld aan de leidende factuur die de ontvanger vertelt over de actie die nodig is om de activiteit te voltooien.

Als het actietype een e-mailbericht in de procesgegevens is, bevat deze sectie twee sneltabbladen.  Het eerste wordt gebruikt voor het definiëren van de sjabloon-id, e-mailbeschrijving, standaardtaal, de gebruikersnaam die wordt toegewezen aan e-mailberichten die automatisch worden verzonden en het e-mailadres van de gekoppelde afzenders. Op het tweede sneltabblad kan de hoofdtekst van het e-mailbericht worden gemaakt nadat de waarden in de velden **Taal** en **Onderwerp** zijn opgeslagen via **Bewerken**.  Hierdoor wordt een venster geopend waarin HTML-inhoud kan worden geüpload. U kunt ook het bericht typen dat handmatig wordt gemaakt in het vak linksonder in het venster.  

> [!Note]
> U kunt een e-mailbericht van Outlook opslaan met de gewenste hoofdtekst van de communicatie in HTML-indeling. Deze kan vervolgens worden geüpload om de sjabloon te implementeren. <br> <br> Als het actietype Aanmaning is geselecteerd, bevat het instellingenformulier geen sectie voor bedrijfsdocumentdetails.


## <a name="fasttab-reference"></a>Verwijzing sneltabblad
In de volgende tabellen worden de pagina's en velden weergegeven waar de opgegeven sneltabbladen kunnen worden geopend. Daarnaast wordt een beschrijving gegeven van de informatie op dat tabblad. 

### <a name="process-hierarchy"></a>Proceshiërarchie

|     Pagina                                                  |     Veld                         |     Beschrijving                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Instelling van incassoproces <br> Procesautomatisering       |                                   |     Incassoprocessen maken en beheren op basis van toewijzingen van klantverzamelingen.                                                                                                                             |
|     Instelling van incassoproces <br> Procesautomatisering       |     Hiërarchie                     |     Definieert de prioriteit van procesautomatisering om een klant toe te wijzen als deze deel uitmaakt van meerdere verzamelingen.                                                                                                   |
|     Instelling van incassoproces <br> Procesautomatisering       |     Groeps-ID                       |     Query's waarmee een groep klantrecords wordt gedefinieerd.                                                                                                                                                        |
|     Instelling van incassoproces <br> Procesautomatisering       |     Stiltedagen                    |     Beperken hoe vaak een processtap kan worden voltooid. Als er bijvoorbeeld twee stille dagen zijn ingesteld, wordt de volgende processtap ten minste twee dagen niet uitgevoerd als de leidende factuur verandert.     |
|     Instelling van incassoproces <br> Procesautomatisering       |     Uitsluiten van proces        |     Wanneer **Naar ouderdom gerangschikt saldo van klant kleiner dan** of **Factuurbedrag kleiner dan** wordt geselecteerd, wordt een klant van de procesautomatisering uitgesloten als niet aan de waardecriteria wordt voldaan.                                   |

### <a name="process-details"></a>Procesgegevens
|     Pagina                                                  |     Veld                                         |      Beschrijving                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Instelling van incassoproces <br> Procesautomatisering       |                                                   |     De stappen definiëren die zijn uitgevoerd op basis van de leidende factuur.                                                                                                |
|                                                           |     Beschrijving                                   |     Vrije-tekstveld dat wordt gebruikt om een naam en/of beschrijving van de stap op te geven.                                                                           |
|                                                           |     Actietype                                   |     Activiteit, e-mail of aanmaning die wordt gemaakt door de processtap.                                                                     |
|                                                           |     Bedrijfsdocument                           |     De activiteit of e-mailsjabloon die tijdens de processtap wordt gebruikt.                                                                        |
|                                                           |     Wanneer                                          |     Definieert of de processtap vóór of na de vervaldatum van de leidende factuur plaatsvindt, in combinatie met het veld **Dagen in relatie tot vervaldatum factuur**.        |
|                                                           |     Dagen in relatie tot vervaldatum factuur        |     In combinatie met het veld **Wanneer** wordt hiermee de timing van de processtap aangegeven.                                                                          |
|                                                           |     Ontvanger                                     |     Geeft aan of een e-mailbericht wordt verzonden naar een contactpersoon voor een klant, verkoopgroep of incassomedewerker.                                                   |
|                                                           |     Contactpersoon voor zakelijke doel                    |     Bepaalt welk e-mailadres van de geadresseerde wordt gebruikt bij e-mailcommunicatie.                                                                                 |

### <a name="business-process-activity-template-details"></a>Details van activiteitensjabloon voor bedrijfsproces 
|     Pagina                                                  |     Veld                     |      Beschrijving                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Instelling van incassoproces <br> Procesautomatisering       |                               |     De sectie van het instellingsproces waarmee de details van de activiteitensjabloon worden aangegeven.                                                                      |
|     Instelling van incassoproces <br> Procesautomatisering       |     Activiteitensjabloon       |     Identificeert het type, het doel en het aantal dagen voor voltooiing en biedt details over de activiteit die wordt gemaakt tijdens een activiteitenprocesstap.       |

### <a name="business-document-email-template-details"></a>Details van e-mailsjabloon voor bedrijfsdocument 
|     Pagina                                                  |     Veld     |      Beschrijving                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Instelling van incassoproces <br> Procesautomatisering       |               |     Identificeert de e-mail beschrijving, de standaardtaal, de afzendernaam en het e-mailadres dat wordt gemaakt tijdens een e-mailprocesstap.        |


### <a name="collections-history"></a>Aanmaningshistorie 
|     Pagina                              |     Veld     |      Beschrijving                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Instelling van incassoproces       |               |     De recente historie van de geselecteerde proceshiërarchie.     |

### <a name="collection-process-assignment"></a>Toewijzing van incassoproces
|     Pagina                              |     Veld     |      Beschrijving                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Instelling van incassoproces       |               |     Klanten weergeven die aan een incassoproces zijn toegewezen.  
|     Handmatige toewijzing               |               |     Klanten weergeven die handmatig aan een proces zijn toegewezen of klanten selecteren die aan een proces moeten worden toegewezen. |
|     Preview procestoewijzing      |               |     Een voorbeeld weergeven van de klanten die aan een strategie worden toegewezen wanneer deze wordt uitgevoerd.   |
|     Preview van klanttoewijzing     |               |     De strategie weergeven waaraan een bepaalde klant is toegewezen.    |
 
### <a name="parameters"></a>Parameters
|     Pagina                                                                  |     Veld                                             |      Beschrijving                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Parameters van module Klanten > Automatisering van incassoproces     |     Percentage klanten per batchtaak          |     Instellen om het aantal batchtaken per automatiseringsproces te bepalen.                                          |
|     Parameters van module Klanten > Automatisering van incassoproces     |     Aanmaningen automatisch boeken           |     Actietypen voor aanmaningen boeken de brief tijdens het automatiseren.                                      |
|     Parameters van module Klanten > Automatisering van incassoproces     |     Activiteiten maken voor automatisering                |     Activiteiten maken en sluiten voor actietypen voor niet-activiteiten om alle geautomatiseerde stappen voor een rekening weer te geven.        |
|     Parameters van module Klanten > Automatisering van incassoproces     |     Aantal dagen om automatisering van incassoproces te behouden     |     Het aantal dagen dat de incassogeschiedenis wordt opgeslagen.                                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]