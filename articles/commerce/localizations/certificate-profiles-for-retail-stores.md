---
title: Door gebruiker gedefinieerde certificaatprofielen voor winkels
description: Dit onderwerp biedt een overzicht van de manier waarop certificaten worden gebruikt in detailhandelwinkels.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0b8bf49a8eb78d0557ef105b40dd4cb5f0d24ce4
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973928"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Door gebruiker gedefinieerde certificaatprofielen voor winkels

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a>Overzicht

Dit onderwerp biedt een overzicht van de certificaatprofielen die beschikbaar zijn in Microsoft Dynamics 365 Commerce. Met deze functionaliteit wordt de functie [Geheimen voor detailhandelafzetkanalen beheren](../dev-itpro/manage-secrets.md) uitgebreid door ondersteuning voor lokale certificaten toe te voegen.

Als het verkooppunt (POS/Point of Sale) wordt uitgevoerd in de offlinemodus, heeft het geen toegang tot de certificaten die zijn opgeslagen in de sleutelkluis. In plaats daarvan moet het lokale certificaat worden gebruikt. De volgende mogelijkheden worden ondersteund:

- Het gebruik van lokale certificaten in terugvalscenario's voor sleutelkluis
- Het gebruik van lokale certificaten zonder een sleutelkluis (bijvoorbeeld in een on-premises installatie)
- Een geleidelijke update van certificaten, waarbij sommige winkels en terminals een nieuwe versie van het certificaat gebruiken, maar andere winkels en terminals de vorige versie blijven gebruiken

Met de functie voor certificaatprofielen kunt u een standaardcertificaat opgeven en de volgorde instellen waarin certificaten in hetzelfde certificaatprofiel worden doorzocht. Deze functionaliteit biedt ook een vergelijkbare instellingsmethode voor lokale certificaten en sleutelkluiscertificaten. U kunt bedrijfsspecifieke instellingen voor certificaten toevoegen, maar de unieke ID tussen bedrijven voor elk certificaat kan worden gebruikt in de Commerce-kanalen.

### <a name="scenarios"></a>Scenario's

De functionaliteit voor certificaatprofielen ondersteunt de volgende scenario's in Commerce-kanalen:

- Het gebruik van een lokaal certificaat in terugvalscenario's voor sleutelkluis. Hieronder volgen enkele voorbeelden van deze terugvalscenario´s:

    - De sleutelkluisopslag is niet toegankelijk.
    - Er is geen certificaat gevonden in de sleutelkluisopslag.
    - Het verkooppunt (POS) wordt uitgevoerd in de offlinemodus.

- Gebruik lokale certificaten, maar zonder deze op te slaan in de sleutelkluis (bijvoorbeeld in een on-premises installatie).
- Voer een geleidelijke update van certificaten uit, waarbij een nieuwe versie van het certificaat alleen wordt gebruikt in winkels of op terminals waarin de nieuwe versie al beschikbaar is.
- Gebruik hetzelfde certificaat in meerdere bedrijven.

## <a name="set-up-certificate-profiles"></a>Certificaatprofielen instellen

In de volgende procedure wordt uitgelegd hoe u certificaatprofielen instelt. Voer de volgende stappen uit om de instellingen te configureren voordat u certificaatprofielen in Commerce-kanalen gaat gebruiken.

1. Schakel in de werkruimte **Functiebeheer** de functie **Door gebruiker gedefinieerde certificaatprofielen voor winkels** in.
2. Ga naar **Systeembeheer \> Instellingen \> Certificaatprofielen**.
3. Maak een record en stel de velden **Certificaatprofiel**, **Naam** en **Beschrijving** voor de record in.

    > [!NOTE]
    > Het certificaatprofiel is een unieke ID van een certificaat voor alle bedrijven en Commerce-onderdelen.

3. Voeg op het tabblad **Rechtspersonen** een regel toe en selecteer de rechtspersoon (bedrijf) waarvoor het huidige certificaatprofiel moet worden gebruikt. Als het certificaatprofiel moet worden gebruikt voor meerdere rechtspersonen, herhaalt u deze stap om een regel toe te voegen voor elke aanvullende rechtspersoon.
4. Selecteer **Instellingen** om de pagina **Instellingen certificaatprofiel** te openen. Op deze pagina kunt u bedrijfsspecifieke instellingen voor het certificaatprofiel invoeren.

### <a name="certificate-profile-settings"></a>Instellingen voor certificaatprofielen

Wanneer u **Instellingen** voor certificaatprofielregels selecteert, wordt de pagina **Instellingen certificaatprofiel** weergegeven. Op deze pagina kunt u opgeven welke certificaten kunnen worden gebruikt wanneer het huidige certificaatprofiel wordt aangeroepen in de Commerce-kanalen. U kunt ook de volgorde opgeven waarin certificaten moeten worden doorzocht.

> [!NOTE]
> Het veld **Prioriteit** wordt automatisch ingesteld. Een waarde van **1** staat voor de hoogste prioriteit. Wanneer een nieuwe regel op de pagina **Instellingen certificaatprofiel** wordt toegevoegd, wordt de prioriteit van de regel ingesteld op een nummer dat één hoger is dan de prioriteit van de vorige regel. Als u de prioriteit van een bepaalde regel wilt wijzigen, selecteert u de regel en selecteert u vervolgens **Omhoog** om de prioriteit te verhogen of **Omlaag** om de prioriteit te verlagen.

Wanneer u een nieuwe regel toevoegt aan de pagina **Instellingen certificaatprofiel**, stelt u de volgende velden in:

- **Locatietype**: selecteer de locatie waar het certificaat is opgeslagen. Dit veld heeft twee mogelijke waarden: **Lokaal certificaat** en **Sleutelkluis**.
- **Sleutelkluiscertificaat**: dit veld is verplicht als u het veld **Locatietype** instelt op **Sleutelkluis**. Gebruik dit veld om een geheim voor een sleutelkluiscertificaat op te geven.

    > [!NOTE]
    > Voordat u een sleutelkluiscertificaat in certificaatprofielen gebruikt, moet u ervoor zorgen dat u een certificaat uploadt naar de sleutelkluisopslag en volgt u de instructies in [Client voor Azure-sleutelkluis instellen](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Winkelnaam**: dit veld is optioneel en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**. Gebruik dit veld om een standaardwinkelnaam op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.
- **Winkellocatie**: dit veld is optioneel en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**. Gebruik dit veld om een standaardwinkellocatie op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.

    > [!NOTE]
    > De standaardwinkelnaam en -winkellocatie worden toegevoegd om het zoeken naar lokale certificaten in Commerce Runtime te vereenvoudigen. X509StoreProvider heeft een lijst met mappen waarin certificaten worden opgeslagen. Als de standaardwinkelnaam en de standaardwinkellocatie niet worden opgegeven, probeert X509StoreProvider een certificaat in de andere mappen in de lijst te vinden.

- **Vingerafdruk**: dit veld is vereist en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**. Gebruik dit veld om de vingerafdruk van het certificaat op te geven.
- **Opmerkingen**: dit veld is optioneel en gebruikers kunnen opmerkingen in dit veld invoeren.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Werkstroom: certificaten zoeken in Commerce Runtime

Dit is de basiswerkstroom die wordt gebruikt om te zoeken naar een certificaat wanneer een certificaatprofiel wordt aangeroepen in Commerce Runtime.

1. In het systeem wordt bepaald of het certificaatprofiel bedrijfsspecifieke instellingen voor de huidige rechtspersoon heeft.
1. Er wordt geprobeerd het certificaat te vinden aan de hand van de waarden op de pagina **Instellingen certificaatprofiel** voor de regel waarvan het veld **Prioriteit** is ingesteld op **1**.

    - Als het veld **Locatietype** is ingesteld op **Sleutelkluis**, wordt de waarde van het veld **Geheim voor sleutelkluiscertificaat** gebruikt om te zoeken naar het certificaat op de pagina **Parameters sleutelkluis**. Het certificaat wordt vervolgens gezocht in de sleutelkluisopslag.
    - Als het veld **Locatietype** is ingesteld op **Lokaal certificaat**, zoekt X509StoreProvider eerst naar het certificaat met behulp van de standaardwinkelnaam en de standaardwinkellocatie, als deze parameters zijn opgegeven. Vervolgens wordt in alle andere mappen in de lijst met mappen gezocht.

1. Als het certificaat niet wordt gevonden, wordt het proces herhaald voor de regel waarvan het veld **Prioriteit** is ingesteld op **2**, enzovoort.

> [!NOTE]
> Als het certificaatprofiel geen instellingen heeft voor de huidige rechtspersoon of als de zoekopdracht naar het certificaat niet succesvol is voor alle regels op de pagina **Instellingen certificaatprofiel**, wordt het certificaat niet gevonden.

#### <a name="caching-the-results-of-certificate-searches"></a>De resultaten van zoekopdrachten naar certificaten in de cache opslaan

De resultaten van zoekopdrachten naar certificaten worden in de cache opgeslagen. De standaardvervaltijd voor een cache is één uur. Deze tijd kan echter worden aangepast en kan worden ingesteld op een maximumwaarde van 24 uur.

### <a name="gradual-update"></a>Geleidelijke update

Als er een nieuwe versie van het certificaat wordt ingevoerd, maar deze niet in alle winkels tegelijk kan worden bijgewerkt, kan het certificaat geleidelijk worden bijgewerkt met de functionaliteit voor certificaatprofielen.

1. Zoek naar een certificaatprofiel en de regel die moeten worden bijgewerkt en selecteer vervolgens **Instellingen**.
1. Voeg een regel toe en geef instellingen op die betrekking hebben op de meest recente versie van het certificaat.
1. Verhoog de waarde van **Prioriteit** van de nieuwe regel. Gebruik de knop **Omhoog** om de regel zo te verplaatsen dat deze boven de regel staat voor de vorige versie van hetzelfde certificaat.

> [!NOTE]
> In Commerce Runtime wordt de nieuwe versie van het certificaat als eerste aangeroepen. Als het certificaat in een specifieke winkel of op een specifieke terminal niet is bijgewerkt, wordt de vorige versie aangeroepen.
