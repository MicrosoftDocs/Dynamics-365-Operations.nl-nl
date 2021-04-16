---
title: Elektronische facturering instellen
description: In dit onderwerp wordt uitgelegd hoe u elektronische facturering in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management instelt.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: fd0dda0adb292c10eea0a770ae0eae33d5f91f17
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839999"
---
# <a name="set-up-electronic-invoicing"></a>Elektronische facturering instellen

[!include [banner](../includes/banner.md)]


Het instellen van de functie Elektronische facturering betreft het proces om de vereiste configuratie te maken via de RCS-omgeving (Regulatory Configuration Services) en die configuratie te publiceren naar de server voor elektronische facturering. Met de instelling kunt u de configureerbare regels maken waarmee Elektronische facturering een beveiligd protocol via internet kan gebruiken om met een externe entiteit te communiceren en gegevens uit te wisselen via webservices.

De configureerbaarheid is gebaseerd op de indelingsconfiguratie voor elektronische rapportage als een middel om inhoud samen te stellen die via digitale bestanden wordt verzonden en ontvangen. Het is ook gebaseerd op de configuratie van communicatieacties om aanvragen te verzenden naar en reacties te ontvangen van externe webservices zonder dat u code hoeft te schrijven.

## <a name="overview"></a>Overzicht

'De functie Elektronische facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server voor elektronische facturering. Met de instelling van de functie wordt onder andere het gebruik van configuratie-indelingen voor elektronische rapportage gecombineerd om configureerbare export- en importbestanden te maken, en het gebruik van acties en actiestromen om het maken van configureerbare regels mogelijk te maken voor het verzenden van aanvragen, het importeren van reacties en het parseren van de reactie-inhoud.

In de volgende afbeelding worden de hoofdonderdelen van een functie voor elektronische facturering weergegeven.

![Overzicht van de functie voor elektronische facturering](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Vanwege variaties in factuurindelingen en actiestromen kan de functie-instelling variëren afhankelijk van het land of de regio of afhankelijk van bedrijfsvereisten.

## <a name="set-up-the-electronic-invoicing-feature"></a>De functie voor elektronische facturering instellen

Het instellingsproces moet in uw RCS-omgeving worden uitgevoerd. Voer de volgende stappen uit om een nieuwe functie voor elektronische facturering te maken.

1. Meld u aan bij uw RCS-omgeving.
2. Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Functies** de tegel **Elektronische facturering**.
3. Selecteer op de pagina **Functies voor elektronische facturering** de optie **Importeren** om het gegevensmodel voor elektronische rapportage vanuit de algemene opslagplaats te importeren.
4. Selecteer **Toevoegen** om een functie voor elektronische facturering te maken. U kunt de functie helemaal opnieuw maken of deze afleiden van een bestaande functie voor elektronische facturering.

    ![Een functie voor elektronische facturering toevoegen](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Als u een nieuwe functie voor elektronische facturering maakt, heeft deze een versienummer en is de standaardstatus ervan ingesteld op **Concept**.

### <a name="configurations"></a>Configuraties

Configuraties bevatten de configuraties voor elektronische rapportage die nodig zijn voor transformaties en voor het maken van de bestanden die tijdens de communicatie met externe webservices worden uitgewisseld. Een functie voor elektronische facturering kan zoveel configuraties van bestandsindelingen voor elektronische rapportage hebben als nodig is op basis van de technische integratiespecificatie die wordt opgegeven door de provider van de webservice.

Voer de volgende stappen uit om ER-indelingen toe te voegen aan de functie voor elektronische facturering.

1. Selecteer op de pagina **Functies voor elektronische facturering** op het tabblad **Configuraties** de optie **Toevoegen** om configuraties voor ER-bestandsindelingen toe te voegen voor de functie voor elektronische facturering.

    ![Configuraties voor de functie voor elektronische facturering toevoegen](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Wanneer u een geheel nieuwe functie voor elektronische facturering maakt, moet u alle configuraties voor de ER-bestandsindelingen handmatig toevoegen. Wanneer u een functie voor elektronische facturering afleidt van een bestaande functie, worden de configuraties voor ER-bestandsindelingen automatisch gemaakt, omdat deze worden overgenomen van de oorspronkelijke functie voor elektronische facturering.

2. Selecteer **Bewerken** om de pagina **Indelingsontwerper** te openen. Op deze pagina kunt u de configuratie voor de ER-bestandsindeling bewerken.

    ![Configuraties voor de functie voor elektronische facturering bewerken](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Terwijl u de indeling bewerkt, wordt de status van de configuratieversie ingesteld op **Concept**.

3. Gebruik de pagina **Indelingsontwerper** om de configuratie van de bestandsindeling te wijzigen. Zie [Configuraties voor elektronische documenten maken](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration) voor meer informatie.

    ![Pagina Indelingsontwerper](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Functie-instellingen

Met functie-instellingen worden de regels voor communicatie en beveiliging met een externe webservice opgenomen. Een functie voor elektronische facturering kan zoveel functie-instellingen hebben als nodig zijn op basis van de bedrijfsregel die u wilt toepassen.

Voer de volgende stappen uit om functie-instellingen toe te voegen aan de functie voor elektronische facturering.

1. Selecteer op de pagina **Functies voor elektronische facturering** op het tabblad **Instellingen** de optie **Toevoegen** om functie-instellingen toe te voegen aan de functie voor elektronische facturering.

    ![Functie-instellingen voor elektronische facturering toevoegen](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Wanneer u een geheel nieuwe functie voor elektronische facturering maakt, moet u alle benodigde functie-instellingen handmatig toevoegen. Wanneer u een functie voor elektronische facturering afleidt van een bestaande functie, worden alle functie-instellingen automatisch gemaakt, omdat deze worden overgenomen van de oorspronkelijke functie voor elektronische facturering.

2. Selecteer **Bewerken** om de instellingen van de functieversie te bewerken.

    ![Functie-instellingen voor elektronische facturering bewerken](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Gebruik de pagina **Instellingen functieversie** om acties, toepasbaarheidsregels en variabelen te configureren.

    ![Acties, regels voor toepasbaarheid en variabelen](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Acties

Acties zijn een vooraf gedefinieerde lijst met bewerkingen die in sequentiële volgorde worden uitgevoerd. Deze lijst bevat het overzicht van de stappen die nodig zijn voor de volledige uitvoering van de functie voor elektronische facturering. De acties kunnen, in dezelfde functie voor elektronische facturering, communicatie in beide richtingen bevatten: een aanvraag voor een bestemming verzenden en een reactie ontvangen en de inhoud ervan parseren.

Elke actie bevat een vooraf gedefinieerde lijst met parameters die vereist zijn voor de actie om het desbetreffende doel te bereiken. Er kunnen desgewenst extra parameters worden opgegeven.

#### <a name="actions-fasttab"></a>Sneltabblad Acties

Voer op de pagina **Instellingen functieversie** op het tabblad **Acties** op het sneltabblad **Acties** een of beide van de volgende stappen uit om acties te beheren:

- Selecteer **Nieuw** of **Verwijderen** om nieuwe acties toe te voegen of bestaande acties te verwijderen.
- Selecteer **Omhoog** of **Omlaag** om geselecteerde acties omhoog of omlaag in het raster te verplaatsen en daardoor de volgorde te wijzigen waarin ze worden uitgevoerd. Acties worden uitgevoerd in de volgorde waarin ze worden weergegeven in het raster, van boven naar beneden.

![Acties beheren](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Acties**.

| Veld        | Beschrijving |
|--------------|-------------|
| Actie       | Er zijn acht vooraf gedefinieerde acties:<ul><li><strong>Document ondertekenen</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Document transformeren</strong></li><li><strong>Reactie verwerken</strong></li><li><strong>REST-webservice aanroepen</strong></li><li><strong>Mexicaanse PAC-service aanroepen</strong></li><li><strong>Braziliaanse SEFAZ-service aanroepen</strong></li><li><strong>Italiaanse SDI-service aanroepen</strong></li></ul> |
| Naam actie  | De naam van de actie en de bijbehorende uitvoeringsvolgorde. |
| Beschrijving  | Een beschrijving van de actie. |
| Opnieuw proberen inschakelen | Met een ingeschakeld selectievakje wordt aangegeven dat de actie opnieuw kan worden uitgevoerd als de vorige poging is mislukt. |
| Actie opnieuw proberen | Bij een nieuwe poging is dit de actie van waaruit de nieuwe poging wordt gestart. De nieuwe poging eindigt vervolgens bij de huidige actie (inclusief nieuwe poging). Voor acties met nieuwe pogingen worden met de parameters **Minimaal uitstel** en **Maximaal uitstel** het minimale aantal en het maximale aantal pogingen opgegeven. |

#### <a name="parameters-fasttab"></a>Sneltabblad Parameters

Met het sneltabblad **Parameters** worden de parameters weergegeven voor de actie die is geselecteerd op het sneltabblad **Acties**.

![Sneltabblad Parameters](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Parameters**.

| Veld       | Beschrijving |
|-------------|-------------|
| Naam        | Een vooraf gedefinieerde lijst met parameters. Zie de sectie [Lijst met parameters per actie](#list-of-parameters-by-action) voor meer informatie. |
| Beschrijving | Een beschrijving van de parameter. |
| Waarde       | De waarde van de parameter. |

#### <a name="list-of-parameters-by-action"></a>Lijst met parameters per actie

De beschikbare parameters verschillen, afhankelijk van de actie die is geselecteerd op het sneltabblad **Acties**.

###### <a name="action-sign-document"></a>Actie: Document ondertekenen

| Parameter                             | Beschrijving |
|---------------------------------------|-------------|
| Invoerbestand                            | Het XML-documentbestand voor invoer dat moet worden ondertekend met een elektronische handtekening. |
| Certificaatnaam                      | De naam van het certificaat in de opslag. |
| Type handtekening                        | Het type te gebruiken handtekening. |
| Naam van handtekeningmethode                 | De naam van de handtekeningmethode die wordt gebruikt om een elektronische handtekening te genereren. |
| Naam van samenvattingsmethode                    | De samenvattingsmethode die wordt gebruikt om een samenvattingstekenreeks in de digitale handtekening te genereren. |
| Naam van canoniseringsmethode          | De canoniseringsmethode waarmee de handtekeninghash wordt berekend. |
| Naam verwijzingskenmerk              | De naam van het kenmerk waarmee wordt aangegeven waar de verwijzings-ID moet worden ingevoegd in het handtekeningelement. |
| Naam van element dat moet worden ondertekend               | De naam van het XML-element in het document dat moet worden ondertekend met een elektronische handtekening. Als er geen element is opgegeven, wordt het basiselement van het document ondertekend. |
| Naam van element waarin handtekening moet worden ingevoegd   | De naam van het XML-element waarin een gegenereerde digitale handtekening moet worden ingevoegd. Als er geen element is opgegeven, wordt de handtekening in het basiselement van het document ingevoegd. |
| XLST-bestand met samenvattingstransformatie       | Het XSLT-bestand (Extensible Style Sheet Language Transformations) dat regels voor samenvattingstransformatie bevat om de samenvattingstekenreeks voor een elektronische handtekening te genereren. |
| Pad voor het invoegen van de samenvattingstekenreeks          | Het pad in de indeling **\<elementName\> .\<Attribute.Path\>** van de locatie waar de gegenereerde samenvattingstekenreeks moet worden ingevoegd. |
| Locatie van certificaatnummer           | De naam van het element en het kenmerk waar het certificaatnummer moet worden geplaatst. |
| Locatie van certificaatgegevens          | De naam van het element en het kenmerk waar de certificaatgegevens (base64) moeten worden ingevoegd. |
| Het certificaatnummer heeft de ASCII-indeling | Een waarde waarmee wordt aangegeven of het nummer van het certificaat in ASCII-indeling is gecodeerd. |

###### <a name="action-filestoreactionname"></a>Actie: FileStoreActionName

| Parameter  | Beschrijving |
|------------|-------------|
| Invoerbestand | Het invoerbestand dat moet worden opgeslagen. |

###### <a name="action-transform-document"></a>Actie: Document transformeren

| Parameter                       | Beschrijving |
|---------------------------------|-------------|
| Invoerbestand                      | Het bronbestand dat de gegevens bevat die voor de actie moeten worden uitgevoerd. |
| Richting                       | Een waarde waarmee wordt aangegeven of de importindeling of de exportindeling moet worden gebruikt. |
| Configuratie-ID                | De indeling die moet worden uitgevoerd. |
| Configuratieversie           | Als er geen configuratieversie is opgegeven, wordt de meest recente versie gebruikt. |
| Configuratie-integratiepunt | Het bronbestand dat gegevens bevat voor de uitvoeringstijd van de rapportage. |

###### <a name="action-process-response"></a>Actie: Reactie verwerken

| Parameter                    | Beschrijving |
|------------------------------|-------------|
| Invoerbestand                   | De reactie die moet worden geanalyseerd. |
| Lijst rapportconfiguratie | Een lijst met configuraties waarmee reacties worden geparseerd. |

###### <a name="action-call-rest-web-service"></a>Actie: REST-webservice aanroepen

| Parameter                   | Beschrijving |
|-----------------------------|-------------|
| Webservice-URL             | De URL waarnaar aanvragen moeten worden verzonden. |
| Time-out webaanvraag         | De maximale tijd (in milliseconden) die moet worden gewacht op een reactie van een webservice. |
| Bewerkingstype aanvraag      | Het type van de HTTP-aanvraagbewerking (bijvoorbeeld **GET**, **POST** of **DELETE**). |
| Certificaatnamen           | De certificaatnamen. |
| Codering van reactietekst      | De verwachte codering van de HTTP-reactietekst, zodat deze juist kan worden gedecodeerd. |
| Inhoudstype van HTTP-aanvragen   | De headerinvoer van het inhoudstype van de HTTP-aanvraag. |
| Inhoudstekst van HTTP-aanvragen   | De tekst van de HTTP-aanvraag. (De tekst kan leeg zijn.) |
| HTTP-parameterquerywaarden | Parameterquerywaarden die worden gebruikt om de URL met variabele parameters te vullen. |
| Aanvraagroute               | Het routepad voor de HTTP-aanvraag. De variabele parameters kunnen worden geschreven in de notatie **\{paramName\}**. Hier is een voorbeeld: **"api/{id}/submit"**. |
| Lijst met routeparameters        | De routeparameters in de notatie sleutel-waarde, die worden gebruikt om variabelen in de route in te voegen. |
| Aangepaste HTTP-headers         | De aangepaste HTTP-headers die in de aanvraag moeten worden geplaatst. |
| Cookies van HTTP-aanvraag        | Een lijst met cookies in de notatie sleutel-waarde, die in de headeraanvraag van HTTP-cookies moeten worden geplaatst. |
| Beveiligingsprotocol           | Het beveiligingsprotocol dat moet worden gebruikt voor HTTP-aanvragen om met de server te communiceren. (Standaard wordt Transport Layer Security \[TLS\] 1.2 gebruikt.) |

###### <a name="action-call-mexican-pac-service"></a>Actie: Mexicaanse PAC-service aanroepen

| Parameter                | Beschrijving |
|--------------------------|-------------|
| Invoerbestand               | Het bestand dat XML-gegevens bevat die naar de webservice worden verzonden als een methode-invoerparameter. |
| URL-adres              | Het adres van de webservice (eindpunt). |
| Naam van webmethode (actie) | De naam van de webmethode (actie) die moet worden uitgevoerd. |
| Getuigschriften             | De certificaatketen die is vereist voor clientverificatie door de webservice. Het clientcertificaat moet het laatste certificaat in de keten zijn. De hoofdcertificaten en tussenliggende certificaten moeten het eerst komen. |
| Time-out webaanvraag      | De maximale tijd (in milliseconden) die moet worden gewacht op een reactie van een webservice. |
| Interval voor nieuwe poging           | Het interval tussen pogingen om een reactie van de webservice aan te roepen en te ontvangen. Als er geen interval is opgegeven, worden er geen extra nieuwe pogingen gedaan nadat de eerste aanroep is mislukt. |
| Aantal nieuwe pogingen              | Het maximum aantal pogingen om een reactie van de webservice aan te roepen en op te halen. |
| Opnieuw proberen tot               | De maximale tijd (in milliseconden) gedurende welke nieuwe aanroepen kunnen worden gedaan. |
| Minimaal uitstel         | Het minimale uitstel voor een exponentiële berekening van intervallen voor nieuwe pogingen. |
| Maximaal uitstel         | Het maximale uitstel voor een exponentiële berekening van intervallen voor nieuwe pogingen. |
| Beveiligingsprotocol        | Het beveiligingsprotocol dat moet worden gebruikt voor HTTP-aanvragen om met de server te communiceren. (Standaard wordt TLS 1.2 gebruikt.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Actie: Braziliaanse SEFAZ-service aanroepen

| Parameter                | Beschrijving |
|--------------------------|-------------|
| Invoerbestand               | Het bestand dat XML-gegevens bevat die naar de webservice worden verzonden als een methode-invoerparameter. |
| URL-adres              | Het adres van de webservice (eindpunt). |
| Naam van webmethode (actie) | De naam van de webmethode (actie) die moet worden uitgevoerd. |
| Getuigschriften             | De certificaatketen die is vereist voor clientverificatie door de webservice. Het clientcertificaat moet het laatste certificaat in de keten zijn. De hoofdcertificaten en tussenliggende certificaten moeten het eerst komen. |
| Time-out webaanvraag      | De maximale tijd (in milliseconden) die moet worden gewacht op een reactie van een webservice. |
| Interval voor nieuwe poging           | Het interval tussen pogingen om een reactie van de webservice aan te roepen en te ontvangen. Als er geen interval is opgegeven, worden er geen extra nieuwe pogingen gedaan nadat de eerste aanroep is mislukt. |
| Aantal nieuwe pogingen              | Het maximum aantal pogingen om een reactie van de webservice aan te roepen en op te halen. |
| Opnieuw proberen tot               | De maximale tijd (in milliseconden) gedurende welke nieuwe aanroepen kunnen worden gedaan. |
| Minimaal uitstel         | Het minimale uitstel voor een exponentiële berekening van intervallen voor nieuwe pogingen. |
| Maximaal uitstel         | Het maximale uitstel voor een exponentiële berekening van intervallen voor nieuwe pogingen. |
| Beveiligingsprotocol        | Het beveiligingsprotocol dat moet worden gebruikt voor HTTP-aanvragen om met de server te communiceren. (Standaard wordt TLS 1.2 gebruikt.) |

###### <a name="action-call-italian-sdi-service"></a>Actie: Italiaanse SDI-service aanroepen

| Parameter                | Beschrijving |
|--------------------------|-------------|
| Invoerbestand               | Het bestand dat XML-gegevens bevat die naar de webservice worden verzonden als een methode-invoerparameter. |
| URL-adres              | Het adres van de webservice (eindpunt). |
| Naam van webmethode (actie) | De naam van de webmethode (actie) die moet worden uitgevoerd. |
| Getuigschriften             | De certificaatketen die is vereist voor clientverificatie door de webservice. Het clientcertificaat moet het laatste certificaat in de keten zijn. De hoofdcertificaten en tussenliggende certificaten moeten het eerst komen. |
| Time-out webaanvraag      | De maximale tijd (in milliseconden) die moet worden gewacht op een reactie van een webservice. |
| Interval voor nieuwe poging           | Het interval tussen pogingen om een reactie van de webservice aan te roepen en te ontvangen. Als er geen interval is opgegeven, worden er geen extra nieuwe pogingen gedaan nadat de eerste aanroep is mislukt. |
| Aantal nieuwe pogingen              | Het maximum aantal pogingen om een reactie van de webservice aan te roepen en op te halen. |
| Opnieuw proberen tot               | De maximale tijd (in milliseconden) gedurende welke nieuwe aanroepen kunnen worden gedaan. |
| Minimaal uitstel         | Het minimale uitstel voor een exponentiële berekening van intervallen voor nieuwe pogingen. |
| Maximaal uitstel         | Het maximale uitstel voor een exponentiële berekening van intervallen voor nieuwe pogingen. |
| Beveiligingsprotocol        | Het beveiligingsprotocol dat moet worden gebruikt voor HTTP-aanvragen om met de server te communiceren. (Standaard wordt TLS 1.2 gebruikt.) |

### <a name="applicability-rules"></a>Toepasbaarheidsregels

Met toepasbaarheidsregels kunt u logische regels maken waarmee de gebruikscontext voor de functie-instelling wordt bepaald. Met de overeenkomst tussen de context die door het bedrijfsdocument wordt gegeven dat wordt verzonden voor verwerking samen met de criteria voor toepasbaarheidsregels, wordt dus bepaald welke functie voor elektronische facturering wordt gebruikt om die verzending te verwerken.

#### <a name="set-up-applicability-rules"></a>Toepasbaarheidsregels instellen

1. Selecteer op de pagina **Instellingen functieversie** op het tabblad **Toepasbaarheidsregels** de optie **Nieuw** om een toepasbaarheidsregel toe te voegen.

    ![Regels voor toepasbaarheid beheren](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Selecteer in het raster de clausules die moeten worden gegroepeerd.
3. Selecteer **Clausule groeperen**.

    ![Clausules groeperen](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Als clausules worden gegroepeerd, wordt een nieuwe kolom aan het raster toegevoegd. Met deze kolom wordt de logische operator voor de gegroepeerde clausules opgegeven.

    ![Logische operator voor gegroepeerde clausules](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Als u de groepering van clausules wilt opheffen, selecteert u de gegroepeerde clausules om de groepering op te heffen en vervolgens selecteert u **Groepering clausule opheffen**.

![Groepering van clausules opheffen](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Als u de groepering van een clausule opheft, begint u altijd vanaf het binnenste groeperingsniveau.

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het tabblad **Toepasbaarheidsregels**.

| Veld         | Beschrijving |
|---------------|-------------|
| En/of        | De logische operator. |
| Veld         | Het veld dat moet worden gebruikt om de regel samen te stellen. |
| Operatortype | Het type operator:<ul><li>Gelijk</li><li>Niet gelijk</li><li>Groter dan/kleiner dan</li><li>Groter dan of gelijk aan/Kleiner dan of gelijk aan</li><li>Bevat</li><li>Beginnen met</li></ul> |
| Waarde         | Het criterium voor de regel. |

### <a name="variables"></a>Variabelen

U kunt variabelen maken en deze vervolgens als de invoerwaarde gebruiken voor een parameter van een bepaalde actie. U kunt ze ook gebruiken voor uitwisseling van informatie tussen de services voor elektronische facturering en de client. Deze informatie is het resultaat van de uitvoering van een specifieke actie als onderdeel van de stroom van verzendingen.

#### <a name="set-up-variables"></a>Variabelen instellen

- Selecteer op de pagina **Instellingen functieversie** op het tabblad **Variabelen** de optie **Nieuw** of **Verwijderen** om variabelen te beheren.

    ![Variabelen beheren](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het tabblad **Variabelen**.

| Veld       | Beschrijving |
|-------------|-------------|
| Naam        | De naam van de variabele. |
| Beschrijving | Een korte beschrijving van de variabele. |
| Type        | Het type variabele:<ul><li><strong>Constante</strong>: de inhoud van de variabele is vast.</li><li><strong>Van client</strong>: de inhoud van de variabele wordt opgehaald van de Microsoft Dynamics 365-client tijdens de uitvoering van het verzendproces.</li><li><strong>Naar client</strong>: de inhoud van de variabele wordt beschikbaar gemaakt voor import door de Microsoft Dynamics 365-client tijdens de uitvoering van het verzendproces.</li></ul> |
| Gegevenstype   | Het gegevenstype van de variabele:<ul><li>Booleaans</li><li>Datum</li><li>Nummer</li><li>UUID</li><li>Tekenreeks</li><li>Bestand</li></ul> |
| Waarde       | De waarde van de variabele of de naam van de actie waarmee de waarde van de variabele wordt ingesteld. |

### <a name="validate-the-feature-setup"></a>De functie-instelling valideren

- Selecteer op de pagina **Instellingen functieversie** in het actievenster **Valideren** om de instelling van de functieversie te valideren.

   ![De knop Valideren selecteren](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Met de validatie wordt de consistentie van de gehele configuratie gecontroleerd. Als bijvoorbeeld een specifieke parameter voor een actie verplicht is, maar de waarde ervan leeg blijft, wordt deze inconsistentie tijdens de validatie ontdekt en ontvangt u een waarschuwing.

## <a name="environments"></a>Omgevingen

De omgeving voor elektronische facturering moet worden gekoppeld aan de functie voor elektronische facturering en hiervoor worden ingeschakeld. Omgevingen voor elektronische facturering moeten vooraf worden gemaakt en gepubliceerd via de configuratie van globalisatiefuncties in de RCS-account van uw organisatie.

Voer de volgende stappen uit om de omgeving voor elektronische facturering in te schakelen voor de functie voor elektronische facturering.

1. Selecteer op de pagina **Functies voor elektronische facturering** op het tabblad **Omgevingen** de optie **Inschakelen** om de omgeving voor elektronische facturering toe te voegen.
2. Voer in het veld **Geldig vanaf** de datum in waarop de nieuwe omgeving van kracht wordt.

![Een omgeving voor elektronische facturering inschakelen](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organisaties

De functie voor elektronische facturering kan in meerdere organisaties worden gedeeld.

- Selecteer op de pagina **Functies voor elektronische facturering** op het tabblad **Organisaties** de optie **Delen met** om de organisatie toe te voegen waarmee u de functie voor elektronische facturering wilt delen.

Selecteer **Delen ongedaan maken** als u het delen van de functie voor elektronische facturering met de organisatie wilt beëindigen.

## <a name="versions"></a>Versies

Met versies kan de levenscyclus van de functie voor elektronische worden beheerd door de status ervan te beheren. U kunt een nieuwe versie van een bestaande functie voor elektronische facturering maken of, wanneer de gehele configuratie voor de functie voor elektronische facturering is voltooid, kunt u de status van de functie wijzigen in **Voltooid** en vervolgens in **Publiceren**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-feature"></a>Een nieuwe versie van een bestaande functie voor elektronische facturering maken

1. Selecteer op de pagina **Functies voor elektronische facturering** in het raster aan de linkerzijde de functie voor elektronische facturering.
2. Selecteer op het tabblad **Versies** de optie **Nieuw** om een nieuwe versie van de functie voor elektronische facturering toe te voegen.

### <a name="change-the-status-of-the-electronic-invoicing-feature"></a>De status van de functie voor elektronische facturering wijzigen

Voer de volgende stappen uit om de levenscyclus van de functie voor elektronische facturering te beheren.

1. Selecteer op de pagina **Functies voor elektronische facturering** in het raster aan de linkerzijde de functie voor elektronische facturering.
2. Selecteer op het tabblad **Versies** de optie **Status wijzigen** en wijzig de status vervolgens van **Concept** in **Voltooid**.
3. U wordt gevraagd te bevestigen dat u de functie voor elektronische facturering en alle bijbehorende onderdelen wilt voltooien. Selecteer **Ja** als u de actie wilt bevestigen of **Nee** als u de actie wilt annuleren.

    > [!NOTE]
    > Als u **Ja** selecteert, wordt de status van configuratieversies , die onderdelen zijn van de functie voor elektronische facturering, automatisch gewijzigd van **Concept** in **Voltooid**.

4. Selecteer **Status wijzigen** en wijzig de status vervolgens van **Voltooid** in **Publiceren**.
5. U wordt gevraagd te bevestigen dat u de functie voor elektronische facturering en alle bijbehorende onderdelen wilt publiceren naar de algemene opslagplaats. Selecteer **Ja** als u de actie wilt bevestigen of **Nee** als u de actie wilt annuleren.

    > [!NOTE]
    > Als u **Ja** selecteert, wordt de status van configuratieversies automatisch gewijzigd van **Voltooid** in **Gedeeld**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
