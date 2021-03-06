---
title: Elektronische facturering in Regulatory Configuration Services (RCS) configureren
description: In dit onderwerp wordt uitgelegd hoe u Elektronische facturering configureert in Dynamics 365 Regulatory Configuration Services (RCS).
author: gionoder
ms.date: 05/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6c1d309744c4c8dd0d17f5259551d31c257ede61
ms.sourcegitcommit: 633d51834d7d29b745824924315a3898dc471f1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/19/2021
ms.locfileid: "6075138"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Elektronische facturering in Regulatory Configuration Services (RCS) configureren

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over de configuratiemogelijkheden van Elektronische facturering in Dynamics 365 Regulatory Configuration Services (RCS).

Via de configuratiemogelijkheden van Elektronische facturering kunt u voldoen aan zakelijke en wettelijke vereisten voor elektronische facturen zonder dat u code hoeft uit te schrijven. En in de scenario's waarin elektronische facturen elektronisch moeten worden goedgekeurd door een webservice, helpen de configuratiemogelijkheden u ook om te voldoen aan de vereisten voor het uitwisselen van berichten met een webservice, zonder code te hoeven schrijven.

## <a name="electronic-reporting"></a>Elektronische rapportage

Elektronische rapportage (ER) biedt ondersteuning voor Elektronische facturering.

De gegevensmodeltoewijzing en -indelingen zijn configureerbare onderdelen die worden gemaakt en bijgehouden via ER en worden gebruikt in Elektronische facturering. De ER-indelingsontwerper is een hulpmiddel voor het maken en onderhouden van bestandsindelingen. Deze wordt gebruikt om de functies voor elektronische facturering te configureren.

Zie [Overzicht van elektronische rapportage (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) voor meer informatie.

## <a name="electronic-invoicing-features"></a>Functies voor elektronische facturering

De functies voor elektronische facturering zijn verantwoordelijk voor het genereren van elektronische facturen via Elektronische facturering. Deze bevatten de configuratieregels en gebruiken deze voor de verwerking van de gegevens die Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management naar Elektronische facturering en elektronische facturen verzenden.

De functies ondersteunen ook scenario's waarbij naleving met de bestandsindelingsspecificaties vereist is en de uitvoer zelfstandig elektronisch bestand is. In de meeste gevallen worden de specificaties van de bestandsindeling door de belastingdienst gepubliceerd.

De functies ondersteunen ten slotte de uitwisseling van berichten met externe webservices die worden gehost door de belastingdienst of door een geaccrediteerde partij, en autorisatie- of goedkeuringsaanvragen in de elektronische factuur.

### <a name="availability-of-electronic-invoicing-features"></a>Beschikbaarheid van elektronische factureringsfuncties

De beschikbaarheid van de functies voor elektronische facturering is afhankelijk van het land of de regio. Sommige functies zijn algemeen beschikbaar, maar andere functies zijn nog in preview.

#### <a name="generally-available-features"></a>Functies voor algemene beschikbaarheid

In de volgende tabel worden de functies voor elektronische facturering weergegeven die algemeen beschikbaar zijn.

| Land/regio | Functienaam                         | Bedrijfsdocument |
|----------------|--------------------------------------|-------------------|
| Egypte          | Elektronische factuur Egypte (EG) | Verkoopfacturen en projectfacturen |

#### <a name="preview-features"></a>Voorbeeldfuncties

In de volgende tabel worden de functies voor elektronische facturering weergegeven die momenteel in preview zijn.

| Land/regio | Functienaam                         | Bedrijfsdocument |
|----------------|--------------------------------------|-------------------|
| Oostenrijk        | Elektronische facturen Oostenrijk (AT)    | Verkoopfacturen en projectfacturen |
| België        | Elektronische factuur België (BE)      | Verkoopfacturen en projectfacturen |
| Brazilië         | Braziliaans NF-e (BR)                  | Fiscaal documentmodel 55, correcties, annuleringen en afkeuringen |
| Brazilië         | Braziliaans NFS-e ABRASF Curitiba (BR) | Service belastingdocumenten |
| Denemarken        | Elektronische factuur Denemarken (DK)       | Verkoopfacturen en projectfacturen |
| Estland        | Elektronische factuur Estland (EE)     | Verkoopfacturen en projectfacturen |
| Finland        | Elektronische factuur Finland (FI)      | Verkoopfacturen en projectfacturen |
| Frankrijk         | Elektronische factuur Frankrijk (FR)       | Verkoopfacturen en projectfacturen |
| Duitsland        | Elektronische factuur Duitsland (DE)       | Verkoopfacturen en projectfacturen |
| Italië          | FatturaPA (IT)                       | Verkoopfacturen en projectfacturen |
| Mexico         | Mexicaans CFDI (ERP)                    | Verkoopfacturen, pakbonnen, voorraadoverboekingen, betalingscomplementen en annuleringen |
| Nederland    | Elektronische factuur Nederland (NL)        | Verkoopfacturen en projectfacturen |
| Noorwegen         | Elektronische factuur Noorwegen (NO)    | Verkoopfacturen en projectfacturen |
| Spanje          | Elektronische factuur Spanje (ES)      | Verkoopfacturen en projectfacturen |
| Europa         | PEPPOL Elektronische factuur            | PEPPOL verkoopfacturen en projectfacturen |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Configureerbare onderdelen van elektronische factureringsfuncties

De elektronische factureringsfuncties bestaan uit de volgende groepen configureerbare onderdelen:

- **Indelingen**: met indelingen kunt u configureren wat Elektronische facturering moet genereren wanneer een elektronisch document een elektronische factuur wordt. Indelingen omvatten de indelingsconfiguratie voor de elektronische factuur en voor bestanden en berichten die worden gebruikt om aanvragen in te dienen en antwoorden te ontvangen wanneer communicatie met een externe webservice vereist is.
- **Acties**: met acties kunt u configureren hoe Elektronische facturering de transformatie genereert van een elektronisch document dat Finance en Supply Chain Management heeft ingediend naar een elektronische factuur.
- **Toepasbaarheidsregels**: met regels voor toepasbaarheid kunt u de context configureren waarmee in Elektronische facturering rekening moet worden gehouden om een elektronische factureringsfunctie te verwerken.
- **Variabelen**: met variabelen kunt u de ondersteuning configureren voor de constructie van de configuratielogica. Variabelen kunnen werken als de invoer van waarden om een specifieke actie uit te voeren. Ze kunnen ook werken als een uitwisseling van waarden tussen Finance en Supply Chain Management en Elektronische facturering.
- **Elektronische documentmodeltoewijzing**: met de toewijzing van het elektronische documentmodel kunt u de ER-modeltoewijzing configureren. De modeltoewijzing definieert de gegevenstoewijzing van de abstracte factuur die in Elektronische facturering is geïntegreerd wanneer elektronische documenten worden ingediend.
- **Factuurcontextmodel**: met het factuurcontextmodel kunt u het ER-factuurcontextmodel configureren en de context van een elektronische factureringsfunctie definiëren.
- **Antwoordtypen**: met antwoordtypen kunt u configureren wat Elektronische facturering moet bijwerken in Finance en Supply Chain Management als gevolg van de verwerking van elektronische facturen.

### <a name="formats"></a>Indelingen

In de volgende lijsten worden de configuraties van de ER-indelingen vermeld die beschikbaar zijn voor de elektronische factureringsfuncties.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Oostenrijkse (AT) elektronische facturen: verkoop- en projectfacturen voor Oostenrijk

- OIOUBL Verkoopfactuur
- OIOUBL Projectfactuur
- OIOUBL Verkoopcreditnota
- OIOUBL Projectcreditnota

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgische (BE) elektronische factuur: verkoop- en projectfacturen voor België

- UBL Verkoopfactuur BE
- UBL Projectfactuur BE
- UBL Projectcreditnota BE
- UBL Verkoopcreditnota BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Federale overheid (BR) NF-e: NF-e Federal (Brazilië)

- NF-e exportindeling voor indienen (BR)
- NF-e exportindeling voor correctiebrief (BR)
- NF-e exportindeling voor annuleren (BR)
- NF-e exportindeling voor weigeren (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Braziliaans NFS-e (BR) ABRASF Curitiba-stad

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF opvragen Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Deense (DK) elektronische factuur: verkoop- en projectfacturen voor Denemarken

- OIOUBL Verkoopfactuur
- OIOUBL Projectfactuur
- OIOUBL Verkoopcreditnota
- OIOUBL Projectcreditnota

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Nederlandse (NL) elektronische factuur: verkoop- en projectfacturen voor Nederland

- UBL Verkoopfactuur NL
- UBL Projectfactuur NL
- UBL Projectcreditnota NL
- UBL Verkoopcreditnota NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egyptische (EG) elektronische factuur: verkoop- en projectfacturen voor Egypte

- Verkoopfactuur (EG) (Facturering)
- Projectfactuur (EG) (Facturering)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estse (EE) elektronische factuur: verkoop- en projectfacturen voor Estland

- Verkoopfactuur (EE)
- Projectfactuur (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Finse (FI) elektronische factuur: verkoop- en projectfacturen voor Finland

- Verkoopfactuur (FI)
- Projectfactuur (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Franse (FR) elektronische factuur: verkoop- en projectfacturen voor Frankrijk

- UBL Verkoopfactuur FR
- UBL Projectfactuur FR
- UBL Projectcreditnota FR
- UBL Verkoopcreditnota FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Duitse (DE) elektronische factuur: verkoop- en projectfacturen voor Duitsland

- Verkoopfactuur (DE)
- Projectfactuur (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italiaanse (IT) elektronische factuur: verkoop- en projectfacturen voor Italië

- Verkoopfactuur (IT)
- Projectfactuur (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Mexicaanse (MX) CFDI: CFDI voor Mexico

- CFDI factuurindeling (MX)
- CFDI Pakbon (MX)
- CFDI Voorraadoverboeking (MX)
- CFDI betalingsindeling (MX)
- CFDI indeling factuur annuleren (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Noorse (NO) elektronische factuur: verkoop- en projectfacturen voor Noorwegen

- OIOUBL Verkoopfactuur
- OIOUBL Projectfactuur
- OIOUBL Verkoopcreditnota
- OIOUBL Projectcreditnota

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL elektronische factuur: PEPPOL verkoop- en projectfacturen

- PEPPOL Verkoopfactuur
- PEPPOL Projectfactuur
- PEPPOL Verkoopcreditnota
- PEPPOL Projectcreditnota

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Spaanse (ES) elektronische factuur: verkoop- en projectfacturen voor Spanje

- Verkoopfactuur (ES)
- Projectfactuur (ES)

Behalve de configuraties van de ER-indeling die buiten het vak beschikbaar zijn voor gebruik met de elektronische factureringsservice, kunt u ook uw eigen ER-indelingsconfiguraties maken. De indelingsconfiguraties die worden gemaakt voor gebruik met elektronische factureringsfuncties, bieden echter geen ondersteuning voor directe verwijzing naar tabellen van Financiën of Supply Chain Management of naar de bijbehorende metagegevens. Alleen verwijzingen naar de ER-modeltoewijzing worden ondersteund.

### <a name="actions"></a>Acties

In de volgende tabel staan de beschikbare acties en of deze momenteel in het algemeen beschikbaar zijn of nog in preview zijn.

| Actie                                        | Beschrijving                                                                  | Beschikbaarheid         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Document transformeren                            | De indeling voor elektronische rapportage uitvoeren om het document te transformeren.                   | Algemeen beschikbaar  |
| Xml-document ondertekenen                             | Xml-documenten ondertekenen met een digitale handtekening.                                   | Preview           |
| Json-document ondertekenen voor Belastingdienst | Json-documenten ondertekenen met een digitale handtekening voor de Egyptische belastingdienst.       | Algemeen beschikbaar  |
| Integreren met de Egyptische ETA-service           | Communiceren met de Egyptische belastingdienst.                                     | Algemeen beschikbaar  |
| Braziliaanse SEFAZ-service aanroepen                  | Integreren met Braziliaanse SEFAZ-service voor het indienen van belastingdocument.       | Preview           |
| Mexicaanse PAC-service aanroepen                      | Integreren met Mexicaanse VS-service voor CFDI-indiening.                      | Preview           |
| Reactie verwerken                              | Het antwoord analyseren dat u van het webserviceoproep hebt ontvangen.                     | Algemeen beschikbaar  |
| MS Power Automate gebruiken                         | Integreer met stroom die is ingebouwd in Microsoft Power Automate.                       | Preview           |

### <a name="applicability-rules"></a>Toepasbaarheidsregels

Toepasselijkheidsregels zijn configureerbare clausules die zijn gedefinieerd op het niveau van de functie Elektronische facturering. De regels zijn geconfigureerd om een context te bieden voor de uitvoering van functies voor elektronische facturering via de set met mogelijkheden voor Elektronische facturering.

Wanneer een bedrijfsdocument van Finance of Supply Chain Management wordt ingediend bij elektronische facturering, bevat het bedrijfsdocument geen expliciete verwijzing waarmee de mogelijkhedenset voor Elektronische facturering een bepaalde elektronische factureringsfunctie kan aanroepen om de indiening te verwerken.

Wanneer het bedrijfsdocument echter correct is geconfigureerd, bevat het de nodige elementen waarmee kan worden opgelost welke functie voor elektronische facturering moet worden geselecteerd en vervolgens de elektronische factuur kan genereren.

Met de toepasselijkheidsregels kan de mogelijkheid voor Elektronische facturering worden ingesteld om de exacte elektronische factureringsfuncties te vinden die moeten worden gebruikt om de indiening te verwerken. Dit gebeurt door de inhoud van het ingediende bedrijfsdocument af te stemmen met de clausules uit de Toepasselijkheidsregels.

Twee functies voor elektronische facturering met gerelateerde toepasselijkheidsregels worden bijvoorbeeld geïmplementeerd in de mogelijkhedenset Elektronische facturering.

| Functie voor elektronische facturering | Toepasbaarheidsregels        |
|------------------------------|--------------------------- |
| V                            | <p>Land = BR</p><p>en</p><p>Rechtspersoon = BRMF</p>  |
| B                            | <p>Land = MX</p><p>en</p><p>Rechtspersoon = MXMF</p>  |

Als een bedrijfsdocument van Finance of Supply Chain Management wordt ingediend bij de mogelijkhedenset voor Elektronische facturering, bevat het bedrijfsdocument de volgende ingevulde kenmerken:

- Land = BR
- Rechtspersoon = BRMF

De mogelijkhedenset voor Elektronische facturering selecteert de elektronische factureringsfunctie **A** om de indiening te verwerken en de elektronische factuur te genereren.

Dit gebeurt op dezelfde manier als het bedrijfsdocument het volgende bevat:

- Land = MX
- Rechtspersoon = MXMF

Elektronische factureringsfunctie **B** wordt is geselecteerd om de elektronische factuur te genereren.

De configuratie van toepasselijkheidsregels kan niet dubbelzinnig zijn. Dit betekent dat twee of meer elektronische factureringsfuncties niet dezelfde clausules kunnen hebben, anders leidt dit tot geen selectie. Als er sprake is van een duplicatie van elektronische factureringsfuncties, gebruikt u om dubbelzinnigheid te voorkomen aanvullende clausules zodat de mogelijkhedenset voor elektronische facturering onderscheid kan maken tussen de twee elektronische factureringsfuncties.

De elektronische factureringsfunctie **C** is bijvoorbeeld een kopie van de elektronische factureringsfunctie **A**.

| Functie voor elektronische facturering | Toepasbaarheidsregels        |
|------------------------------|--------------------------- |
| V                            | <p>Land = BR</p><p>en</p><p>Rechtspersoon = BRMF</p>  |
| C                            | <p>Land = BR</p><p>en</p><p>Rechtspersoon = BRMF</p>  |

In dit voorbeeld staat functie **C** voor een zakelijke documentinzending die het volgende bevat:

- Land = BR
- Rechtspersoon = BRMF

De mogelijkheid voor elektronische facturering kan niet onderscheiden welke functie voor elektronische facturering moet worden gebruikt om de indiening te verwerken, omdat de inzendingen exact dezelfde clausules bevatten.

Om onderscheid te maken tussen de twee functies via toepasselijkheidsregels, moet een nieuwe clausule worden toegevoegd aan een van de functies zodat de mogelijkhedenset voor elektronische facturering de juiste functie voor elektronische facturering kan selecteren.

| Functie voor elektronische facturering | Toepasbaarheidsregels        |
|------------------------------|--------------------------- |
| V                            | <p>Land = BR</p><p>en</p><p>Rechtspersoon = BRMF</p>  |
| C                            | <p>Land = BR</p><p>en</p><p>Rechtspersoon = BRMF</p><p>en</p><p>Model=55</p>  |

Om het maken van complexere clausules te ondersteunen zijn de volgende bronnen beschikbaar:

Logische operators:
- En
- Of

Typen operators:
- Equal
- Not equal
- Greater than
- Less than
- Groter dan of gelijk aan
- Kleiner dan of gelijk aan
- Contains
- Begint met

Gegevenstypen:
- Tekenreeks
- Nummer
- Booleaans
- Datum
- UUID

Mogelijkheid om clausules te groeperen en de groep op te heffen.
Het voorbeeld ziet er zo uit.

| Functie voor elektronische facturering | Toepasbaarheidsregels        |
|------------------------------|--------------------------- |
| C                            | <p>Land = BR</p><p>en</p><p>(Rechtspersoon = BRMF</p><p>of</p><p>Model=55)</p>  |


## <a name="configuration-providers"></a>Configuratieproviders

Configuratieproviders bieden de elektronische factureringsfuncties en de bijbehorende ER-onderdelen, zoals de modeltoewijzing, de indelingsconfiguratie en het contextmodel. Ze publiceren de elektronische factureringsfuncties en ER-onderdelen in de gekoppelde algemene opslagplaats. Van hieruit kunnen andere organisaties ze downloaden.

Voordat u de functies voor elektronische facturering configureert via RFS, moet u uw eigen organisatie configureren als configuratieprovider in de module **Elektronische rapportage**. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor informatie over de manier waarop u een configuratieprovider als **Actief** kunt instellen.

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Elektronische factureringsfuncties weergeven in de algemene opslagplaats

Als u wilt bladeren door de elektronische factureringsfuncties die beschikbaar zijn in de algemene opslagplaats voor een specifieke configuratieprovider, synchroniseert u het RCS-exemplaar van uw organisatie. Nadat de synchronisatie is voltooid, wordt de lijst met beschikbare elektronische factureringsfuncties bijgewerkt.

## <a name="importing-electronic-invoicing-features"></a>Functies voor elektronische facturering importeren

Voordat u de functies voor elektronische facturering gebruikt of configureert, moet u deze importeren in het RFS-exemplaar van uw organisatie. Tijdens de importbewerking wordt een lokale kopie gemaakt van de functies en worden alle ER-onderdelen die door de functies worden gebruikt (bijvoorbeeld indelingsconfiguraties en modelconfiguraties), naar het RFS-exemplaar van uw organisatie gekopieerd.

U kunt de elektronische factureringsfuncties vanuit elke configuratieprovider importeren.

## <a name="creating-electronic-invoicing-features"></a>Functies voor elektronische facturering maken

U kunt een functie voor elektronische facturering helemaal opnieuw maken of u kunt deze afleiden van een andere functie voor elektronische facturering.

Wanneer u een elektronische factureringsfunctie handmatig maakt, moet u de ER-onderdelen handmatig toevoegen (bijvoorbeeld configuraties van functieversies en andere configuraties, zoals de instellingen van de functieversie en de toepassing). Wanneer u een functie maakt door deze van een andere functie af te leiden, neemt de nieuwe functie alle configuraties over van het origineel. 

## <a name="electronic-invoicing-feature-version"></a>Versie van een functie voor elektronische facturering

De functies voor elektronische facturering hebben bepaalde versies. Wanneer een nieuwe versie wordt gemaakt, wordt het versienummer automatisch verhoogd. U kunt een ingangsdatum voor de nieuwe versie definiëren.

Versies van elektronische factureringsfuncties volgen een levenscyclus met maximaal drie statussen:

- **Concept**: als een functieversie deze status heeft, kunt u de configuratiekenmerken en alle andere onderdelen hiervan bewerken (bijvoorbeeld bestandsindelingsconfiguraties).
- **Voltooid**: als een functieversie deze status heeft, is deze gepubliceerd in de algemene opslagplaats die aan uw organisatie is gekoppeld. U kunt de functieversie of een van de ER-onderdelen niet meer bewerken.
- **Gepubliceerd**: als een functieversie deze status heeft, is deze gepubliceerd in Elektronische facturering. U kunt de functieversie of een van de ER-onderdelen niet meer bewerken.

### <a name="feature-configurations"></a>Functieconfiguraties

Functieconfiguraties bevatten alle ER-indelingsconfiguraties die door de elektronische factureringsfuncties worden gebruikt. Alle elektronische bestanden die door een elektronische factureringsfunctie tijdens de verwerking worden gebruikt, zijn afkomstig van de indelingsconfiguraties die zijn toegevoegd aan de functieconfiguraties van die functie.

Vanuit de functieconfiguraties hebt u toegang tot de ER-indelingsontwerper. Deze ontwerper is het ER-hulpprogramma dat wordt gebruikt om indelingsconfiguraties te maken.

### <a name="feature-setup"></a>Functie-instellingen

Functie-instellingen worden gebruikt in combinatie met functieconfiguraties. Elke functie-instelling omvat een verzameling acties, regels voor toepasbaarheid en variabelen die het verwachte gedrag geven, zodat een elektronische factureringsfunctie aan een specifieke vereiste van de elektronische factuur kan voldoen.

### <a name="application-setup"></a>Toepassingsinstelling

De toepassingsinstellingen moeten zijn gekoppeld aan een eerder gemaakte gekoppelde toepassing.

Via de toepassingsinstellingen kunt u het onderdeel van een elektronische factureringsfunctie configureren dat in Finance en Supply Chain Management moet worden uitgevoerd. Ten minste drie configureerbare onderdelen zijn verplicht, ongeacht de elektronische factureringsfunctie:

- **Tabelnaam**: de entiteit in Finance en Supply Chain Management waarin de geboekte facturen staan, en waar de elektronische factureringsfunctie op is gebaseerd.
- **Context**: de naam van het factuurcontextmodel dat is geconfigureerd via ER.
- **Zakelijke documenttoewijzing**: de naam van het factuurtoewijzingsmodel dat is geconfigureerd via ER.

> [!IMPORTANT]
> De configuratie die in de instellingen van de toepassing is ingevoerd, kan worden bekeken in Finance en Supply Chain Management. Ga naar **Organisatiebeheer \> Instellen \> Parameter voor elektronische documenten**. Selecteer op het tabblad **Elektronisch document** de optie **Implementeren** en selecteer de optie **Verbonden toepassing**.

### <a name="deploying-feature-versions"></a>Functieversies implementeren

In RCS gebruikt u de opdracht **Implementeren** om een versie van een elektronische factureringsfunctie te publiceren. Selecteer **Implementeren** en selecteer vervolgens een van de volgende opties om het doel van de implementatie te definiëren: 

- **Serviceomgeving**: als het doel van de implementatie de serviceomgeving is, wordt de versie van de elektronische factureringsfunctie naar de serviceomgeving gepubliceerd. Elektronische facturering is dan klaar om elektronische documenten te ontvangen en te verwerken die door Finance en Supply Chain Management worden verzonden.
- **Verbonden toepassing**: wanneer het doel van de implementatie de verbonden toepassing is, wordt de configuratie die wordt geleverd door de toepassingsinstellingen geschreven in het Finance en Supply Chain Management-exemplaar dat eerder aan de toepassing is verbonden.

Alleen versies van elektronische factureringsfunctie met de status **Voltooid** kunnen worden geïmplementeerd in een serviceomgeving of een verbonden toepassing.

### <a name="removing-feature-versions"></a>Functieversies verwijderen

In RCS gebruikt u de opdracht **Implementatie verwijderen** om een specifieke versie van een elektronische factureringsfunctie te verwijderen uit een serviceomgeving in Elektronische facturering.

> [!IMPORTANT]
> De opdracht **Implementatie verwijderen** werkt alleen in serviceomgevingen. Deze functie verwijdert geen versies van elektronische factureringsfuncties uit verbonden toepassingen.

### <a name="rebasing-electronic-invoicing-features"></a>Functies voor elektronische facturering rebasen

Wanneer een elektronische factureringsfunctie van een andere is afgeleid, werkt de opdracht **Rebase** de afgeleide functie bij met de wijzigingen die in de oorspronkelijke functie zijn aangebracht.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Elektronische facturen uitgeven in Finance en Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
