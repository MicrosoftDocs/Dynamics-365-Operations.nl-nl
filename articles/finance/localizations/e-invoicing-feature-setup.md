---
title: Werken met functie-instellingen
description: In dit artikel wordt uitgelegd hoe u elektronische facturering instelt.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 0d64757871c12ae914f7ace4cc0121a08a32a9d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272239"
---
# <a name="work-with-feature-setups"></a>Werken met functie-instellingen

[!include [banner](../includes/banner.md)]

Als u het genereren van elektronische bestanden en andere verwerkingsstappen (bijvoorbeeld digitaal ondertekenen van bestanden, het indienen van deze bestanden bij de webservice van de overheid en het ontvangen van een antwoord, of het opslaan ervan) wilt instellen, stelt u de verwerkingspijplijn, de toepasbaarheidsregels en variabelen voor elektronische factureringsfuncties in.

De instellingsinformatie wordt gecombineerd in het concept *functie-instellingen* en kan worden gemaakt, verwijderd en aangepast. De informatie kan ook worden bekeken voor de voltooide versies van elektronische factureringsfuncties.

U kunt zoveel functie-instellingsitems maken als u nodig hebt om verschillende scenario's te definiëren voor het genereren, verwerken en ontvangen van elektronische bestanden. Hoewel deze functie-instellingsitems onafhankelijke verwerkingsacties en uitvoeringsvoorwaarden hebben, worden ze gemaakt als onderdeel van één elektronische factureringsfunctie en nemen ze de levenscyclus en het implementatieproces daarvan over.

## <a name="add-a-feature-setup"></a>Een functie-instelling toevoegen

1. Meld u aan bij uw RCS-account (Regulatory Configuration Service).
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
3. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering de status **Concept** heeft.
4. Selecteer **Toevoegen** op het tabblad **Instellingen**.
5. Selecteer een van de volgende opties in het dialoogvenster **Functie-instelling maken** in de veldgroep **Nieuw**:
 
    - **Aangepaste instellingen**: maak nieuwe functie-instellingen met lege kanalen, een lege lijst voor de verwerkingspijplijn, een lege sectie voor toepasbaarheidsregels en een standaardset variabelen, afhankelijk van het instellingstype.
    - **Vanuit functie-instellingen**: maak een kopie van een andere functie-instelling in het bereik van de huidige elektronische factureringsfunctie.

6. Als u in de laatste stap de optie **Aangepast instellen** hebt geselecteerd, voert u een naam en omschrijving van het artikel in voor de functie-instelling en selecteert u vervolgens een van de volgende opties in de veldgroep **Instellingstype**:

    - **Verwerkingspijplijn**: selecteer deze optie om uitgaande elektronische documenten te genereren en te verwerken. Voor dit instellingstype wordt een lege lijst voor de verwerkingspijplijn, een lege sectie voor toepasbaarheidsregels en een standaardset variabelen gemaakt. U kunt niet werken met de kanalen voor inkomende elektronische documenten.
    - **Gegevenskanaal**: selecteer deze optie om het proces in te stellen van de ontvangst van inkomende elektronische documenten vanuit een van de gedefinieerde kanalen en deze rechtstreeks zonder aanvullende acties door te geven aan Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management. Voor dit instellingstype wordt een vooraf gedefinieerde lijst met parameters voor de gegevenskanalen, een lege sectie voor toepasbaarheidsregels en een set standaardvariabelen gemaakt. U kunt dan geen acties toevoegen aan de verwerkingspijplijn.
    - **Gegevenskanaal en verwerkingspijplijn**: dit instellingstype lijkt op het instellingstype **Gegevenskanaal**. Voordat een inkomend elektronisch document wordt doorgegeven aan Finance of Supply Chain Management, kunt u echter extra acties instellen in de verwerkingspijplijn.

7. Als u in de laatste stap de optie **Gegevenskanaal** of **Gegevenskanaal en verwerkingspijplijn** hebt geselecteerd, moet u inhet veld **Gegevenskanaal selecteren** het kanaal selecteren waarin u het gegevenskanaal wilt integreren.
8. Selecteer **Maken**.

Nadat u een functie-instelling hebt gemaakt, kunt u **Bewerken** selecteren om deze te configureren.

## <a name="edit-a-feature-setup"></a>Een functie-instelling bewerken

Afhankelijk van het type functie-instelling kunt u het proces configureren van het genereren van uitgaande elektronische bestanden en ze indienen bij externe kanalen, of inkomende documenten ontvangen en deze doorgeven aan uw toepassing Finance of Supply Chain Management.

### <a name="data-channel"></a>Gegevenskanaal

Bij *een gegevenskanaal* wordt het elektronische bestand verwerkt of rechtstreeks doorgegeven aan Finance of Supply Chain Management. Deze optie is niet beschikbaar voor functie-instellingen van het type **Verwerkingspijplijn**.

Voer de naam van het kanaal in om een gegevenskanaal in te stellen. Definieer vervolgens de parameters op basis van het geselecteerde kanaaltype. De id van het gegevenskanaal moet verwijzen naar de variabele die specifiek is gemaakt om het gegevenskanaal te identificeren. Deze wordt gebruikt als referentie in Finance of Supply Chain Management.

Op het tabblad **Bijlagenfilter** moet u een set filters definiëren om specifieke bestanden van het kanaal op te halen. U kunt meerdere regels maken als u verwacht dat bestanden verschillende bestandsnaamextensies zullen hebben, of als bestanden anders moeten worden verwerkt afhankelijk van de bestandsnaam. Hier staan de hoofdparameters:

- **Naam**: voer de naam in van het bestand waar het systeem tijdens de verwerking naar zal verwijzen. In de toepassingen van Finance en Supply Chain Management kunt u de bestanden bekijken in het indieningslogboek.
- **Filter**: definieer het filter om bestanden te selecteren.
- **Optioneel**: als dit selectievakje is gewist, is het bestand verplicht. In dit geval wordt een foutbericht weergegeven als de kanalen geen bestanden bevatten die overeenkomen met het filter. Deze parameter is van toepassing op e-mails.

Als het kanaal een postvak is en een inkomende e-mail meerdere bijlagen bevat, kunt u regels configureren om te definiëren hoe bijlagen moeten worden verwerkt. De service kan elke bijlage als een afzonderlijke elektronische factuur beschouwen of één bijlage als hoofdfactuur en alle andere bijlagen als toevoegingen behandelen.

### <a name="processing-pipeline"></a>Verwerkingspijplijn

Een *verwerkingspijplijn* is een *set acties* die opeenvolgend worden uitgevoerd totdat ze met succes zijn voltooid. U kunt een verwerkingspijplijn gebruiken om het proces in te stellen voor het genereren van elektronische bestanden en het uitvoeren van andere stappen (bijvoorbeeld het digitaal ondertekenen van bestanden, het indienen van bestanden bij externe webservices, het bekijken van het antwoord en het ontvangen en verwerken van inkomende documenten).

De lijst met acties is vooraf gedefinieerd. Met de knoppen **Nieuw** en **Verwijderen** kunt u de combinatie opgeven van acties die op een logische manier het vereiste proces definiëren voor het indienen of ontvangen van documenten.

De volgorde van de acties is belangrijk. U kunt de volgorde wijzigen met de knoppen **Omhoog** en **Omlaag**.

Elke actie heeft een set parameters die u kunt configureren of aanpassen. De specifieke set parameters is afhankelijk van het type actie.

- **Actie**: selecteer het type actie.
- **Actienaam**: voer de naam in voor de actie. Deze naam wordt weergegeven in indieningslogboeken en in berichten in de toepassingen Finance en Supply Chain Management.
- **Omschrijving**: geef meer informatie op over het doel van de actie in het proces.
- **Opnieuw proberen inschakelen**: als u dit selectievakje inschakelt, kunt u een actie selecteren in het veld **Actie opnieuw proberen** en extra parameters configureren op het tabblad **Parameters opnieuw proberen**.

    Met de functionaliteit voor opnieuw proberen kunt u het gedrag van de service configureren als een bepaalde actie niet kan worden uitgevoerd. Als de externe webservice waarmee u verbinding probeert te maken niet reageert, kunt u bijvoorbeeld opgeven hoe vaak de verbinding opnieuw moet geprobeerd, met welk interval en op basis van welke actie in de verwerkingspijplijn.

- **Resultaten exporteren**: u kunt dit selectievakje selecteren voor *één* actie in de verwerkingspijplijn. Het elektronische bestand dat door de actie wordt geproduceerd in de toepassing Finance of Supply Chain Management kan vervolgens worden geëxporteerd via de pagina **Indieningslogboek van elektronische documenten**.

### <a name="applicability-rules"></a>Toepasbaarheidsregels

*Toepasbaarheidsregels* zijn configureerbare clausules om een context te bieden voor de uitvoering van functies voor elektronische facturering via de set met mogelijkheden voor Elektronische facturering.
Bedrijfsdocumenten die uit Finance of Supply Chain Management worden ingediend bij elektronische facturering, bevatten geen expliciete verwijzing waarmee de Elektronische factureringsfunctie voor het aanroepen van een bepaalde elektronische factureringsfunctie wordt ingeschakeld en een specifiek functie-instellingsitem om de indiening te verwerken. Wanneer een bedrijfsdocument echter correct is geconfigureerd, bevat het de vereiste elementen waarmee Elektronische facturering wordt ingeschakeld om te bepalen welke versie van de elektronische factuur en de verwerkingsijplijn moeten worden geselecteerd en uitgevoerd.

Met de toepasselijkheidsregels kan de mogelijkheid voor Elektronische facturering worden ingesteld om de exacte elektronische factureringsfuncties te vinden die moeten worden gebruikt om de indiening te verwerken. Om de juiste functies te vinden worden de **contextvelden** uit het ingediende bedrijfsdocument afgestemd met componenten van de toepasbaarheidsregels.

U kunt als volgt werken met toepasbaarheidsregels:

- Selecteer **Nieuw** om een nieuwe component aan een set toepasbaarheidsregels toe te voegen.
- Selecteer **Verwijderen** om een component te verwijderen.
- Selecteer meerdere records en gebruik de knop **Groeperen** of **Groep opheffen** om een combinatie van artikelen of logische overzichten te maken. Selecteer bijvoorbeeld de regels die u wilt groeperen en selecteer vervolgens **Clausule groeperen**. Als clausules worden gegroepeerd, wordt een nieuwe kolom aan het raster toegevoegd. Met deze kolom wordt de logische operator voor de gegroepeerde clausule opgegeven. Momenteel worden de volgende typen operators ondersteund:

    - Equal
    - Not equal
    - Groter dan/kleiner dan
    - Groter dan of gelijk aan/Kleiner dan of gelijk aan
    - Bevat
    - Beginnen met

    > [!NOTE]
    > Als u de groepering van een clausule opheft, begint u altijd vanaf het binnenste groeperingsniveau.

### <a name="variables"></a>Variabelen

*Variabelen* geven u meer flexibiliteit bij het instellen van een verwerkingspijplijn en de gegevensstroom tussen acties. U kunt in sommige actieparameters verwijzen naar een variabele om gegevens of elektronische bestanden tijdelijk op te slaan. Sommige variabelen worden gebruikt om gegevens door te geven tussen de toepassingen Financie en Supply Chain Management en de elektronische factureringsservice.

Sommige variabelen worden standaard door het systeem gemaakt. De variabele **BusinessDocumentDataModel** bevat bijvoorbeeld bedrijfsgegevens in een JSON-structuur (JavaScript Object Notation) die tijdens het indieningsproces in de aanroep van de gekoppelde toepassing wordt geleverd.

U kunt kiezen uit de volgende variabeletypen:

- **Constante**: een container voor het opslaan van tijdelijke gegevens die worden gebruikt bij de verwerking van pijplijnacties.
- **Van client**: de inhoud van de variabele wordt opgehaald van de Dynamics 365-client tijdens de uitvoering van het verzendproces.
- **Naar client**: de inhoud van de variabele wordt beschikbaar gemaakt voor import door de Dynamics 365-client tijdens de uitvoering van het verzendproces.
- **Gegevenstype**: selecteer het gegevenstype van de informatie die is opgeslagen in de variabele.

### <a name="parameters"></a>Parameters

De optie **Verminderen van bedrijfsgegevens uitschakelen** wordt gebruikt om de structuur te optimaliseren van de payload net bedrijfsgegevens die tijdens het elektronisch indienen van documenten afkomstig zijn uit Finance of Supply Chain Management. Optimalisatie helpt bij het reduceren van de gegevens die naar de elektronische factureringsservice gaan voor verdere transformatie naar het vereiste elektronische bestand. De standaardwaarde is **Nee**.

- **Ja**: Financie of Supply Chain Management verzendt een JSON-bestand van de structuur **Factuurmodel** of **Belastingmodel** (voor Brazilië) die is gedefinieerd in de module **Elektronische rapportage** Alle elementen van het model worden gevuld met bedrijfsgegevens aan de toepassingszijde, ongeacht de uiteindelijke elektronische bestandsstructuur. Modellen bevatten meestal meer bedrijfsgegevens dan voor de doelbestandsstructuur nodig is, en er kan meer tijd nodig zijn om deze gegevens in de toepassing te genereren. De waarde **Ja** voor deze optie is vereist in het zeldzame geval dat u verschillende uitvoerbestanden in één elektronische factureringsfunctie en functie-instelling wilt genereren. De waarde **Ja** is handig wanneer u problemen met scenario's, de structuur van de elektronische bestanden en de volledigheid van de bedrijfsgegevens wilt oplossen.
- **Nee**: Finance of Supply Chain Management roepen het eerst de service aan zonder bedrijfsgegevens. Het doel van deze aanroep is informatie op te halen over de ER-configuratie (Electronic Reporting) die wordt gebruikt voor elektronische bestandstransformatie in de verwerkingspijplijn. Deze informatie wordt teruggestuurd naar de toepassing, waar deze wordt gebruikt om de subset van zakelijke gegevens te bepalen die moet worden opgenomen in het JSON-bestand van de structuur met **Factuurmodel** of **Fiscaal model** (voor Brazilië). De waarde **Nee** voor deze optie verkleint het volume van zakelijke gegevens die de toepassing bij de service indient, omdat de toepassing alleen de zakelijke gegevens kan indienen die nodig zijn om een elektronisch bestand te genereren.

### <a name="validate-a-feature-setup"></a>Een functie-instelling valideren

U kunt de validatie uitvoeren om de consistentie van de gehele configuratie te controleren. Als bijvoorbeeld een verplichte parameter voor een actie leeg is gelaten, wordt deze inconsistentie tijdens de validatie ontdekt en ontvangt u een waarschuwingsbericht.

- Selecteer op de pagina **Instellingen functieversie** in het actievenster **Valideren**.

## <a name="delete-a-feature-setup"></a>Een functie-instelling verwijderen

1. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering de status **Concept** heeft.
2. Selecteer op het tabblad **Instellingen** de optie **Verwijderen**.
3. Selecteer **Ja** in het berichtvak dat verschijnt om te bevestigen dat u de functie-instellingen wilt verwijderen.
