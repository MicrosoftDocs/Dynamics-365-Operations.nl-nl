---
title: Door gebruiker gedefinieerde certificaatprofielen voor winkels
description: Dit artikel biedt een overzicht van de certificaatprofielen die beschikbaar zijn in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558432"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Door gebruiker gedefinieerde certificaatprofielen voor winkels

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van de certificaatprofielen die beschikbaar zijn in Microsoft Dynamics 365 Commerce. Met deze functionaliteit wordt de functie [Geheimen voor detailhandelafzetkanalen beheren](../dev-itpro/manage-secrets.md) uitgebreid door ondersteuning voor lokale certificaten toe te voegen.

Als het verkooppunt (POS/Point of Sale) wordt uitgevoerd in de offlinemodus, heeft het geen toegang tot de certificaten die zijn opgeslagen in de Microsoft Azure Key Vault. In plaats daarvan moet het lokale certificaat worden gebruikt. De volgende mogelijkheden worden ondersteund:

- Het gebruik van lokale certificaten in terugvalscenario's voor Key Vault
- Het gebruik van lokale certificaten zonder Key Vault (bijvoorbeeld in een on-premises installatie)
- Een geleidelijke update van certificaten, waarbij sommige winkels en terminals een nieuwe versie van het certificaat gebruiken, maar andere winkels en terminals de vorige versie blijven gebruiken

Met de functie voor certificaatprofielen kunt u een standaardcertificaat opgeven en de volgorde instellen waarin certificaten in hetzelfde certificaatprofiel worden doorzocht. Deze functionaliteit biedt ook een vergelijkbare instellingsmethode voor lokale certificaten en sleutelkluiscertificaten. U kunt bedrijfsspecifieke instellingen voor certificaten toevoegen, maar de unieke ID tussen bedrijven voor elk certificaat kan worden gebruikt in de Commerce-kanalen.

### <a name="scenarios"></a>Scenario's

De functionaliteit voor certificaatprofielen ondersteunt de volgende scenario's in Commerce-kanalen:

- Het gebruik van een lokaal certificaat in terugvalscenario's voor Key Vault. Hieronder volgen enkele voorbeelden van deze terugvalscenario´s:

    - De sleutelkluisopslag is niet toegankelijk.
    - Er is geen certificaat gevonden in de sleutelkluisopslag.
    - Het verkooppunt (POS) wordt uitgevoerd in de offlinemodus.

- Gebruik lokale certificaten, maar zonder deze op te slaan in Key Vault (bijvoorbeeld in een on-premises installatie).
- Voer een geleidelijke update van certificaten uit, waarbij een nieuwe versie van het certificaat alleen wordt gebruikt in winkels of op terminals waarin de nieuwe versie al beschikbaar is.
- Gebruik hetzelfde certificaat in meerdere bedrijven.

## <a name="set-up-certificate-profiles"></a>Certificaatprofielen instellen

In de volgende procedure wordt uitgelegd hoe u certificaatprofielen instelt.

### <a name="set-up-key-vault"></a>Key Vault instellen

Voordat u een digitaal certificaat kunt gebruiken dat is opgeslagen in Key Vault, moeten de volgende stappen worden uitgevoerd.

1. Een Key Vault-opslagaccount en een sleutelkluis aanmaken. Het wordt aangeraden de opslagaccount in dezelfde geografische regio in te zetten als de Commerce Scale Unit.
1. Upload het digitale certificaat naar het Key Vault-opslagaccount.
1. Autoriseer de AOS-toepassing (Application Object Server) om geheimen uit het Key Vault-storageaccount te lezen.

Zie [Aan de slag met Azure Key Vault](/azure/key-vault/key-vault-get-started) voor meer informatie over het werken met de sleutelkluis.

### <a name="set-up-system-parameters"></a>Systeemparameters instellen

Voordat u certificaatprofielen configureert in de Commerce-kanalen, moet u Commerce inschakelen om beide certificaten te gebruiken die zijn opgeslagen in Key Vault- en certificaatprofielen.

Volg deze stappen als u systeemparameters in Commerce headquarters wilt instellen.

1. Stel op de pagina **Systeemparameters** de optie **Geavanceerd certificaatarchief gebruiken** in op **Ja**.
1. Schakel in de werkruimte **Functiebeheer** de functie **Door gebruiker gedefinieerde certificaatprofielen voor winkels** in.

### <a name="set-up-key-vault-parameters"></a>Key Vault-parameters instellen

Op de pagina **Key Vault-parameters** moet u de volgende parameters specificeren om toegang te krijgen tot de Key Vault-opslag:

- **Naam** en **Beschrijving**: de naam en beschrijving van de Key Vault-opslagaccount.
- **URL Key Vault**: de URL van de Key Vault-storageaccount.
- **Key Vault-client**: een interactieve client-id van de toepassing Azure Active Directory (Azure AD) die aan de Key Vault-opslagaccount is gekoppeld voor verificatiedoeleinden. Deze client moet leestoegang om geheimen uit de opslagaccount te kunnen lezen.
- **Geheime sleutel voor Key Vault**: voer een geheime sleutel in die hoort bij de Azure AD-toepassing die voor verificatie wordt gebruikt in de Key Vault-opslagaccount.
- **Naam**, **Beschrijving** en **Geheime verwijzing**: de naam, beschrijving en geheime verwijzing van het certificaat.

Zie [Azure Key Vault-client instellen](../../finance/localizations/setting-up-azure-key-vault-client.md) voor meer informatie.

### <a name="configure-a-certificate-profile"></a>Een certificaatprofiel configureren

Voer deze stappen uit een certificaatprofiel te configureren in Commerce headquarters.

1. Ga naar **Systeembeheer \> Instellingen \> Certificaatprofielen**.
1. Selecteer in het actievenster **Nieuw** om een record te maken.
1. Geef waarden op in de velden **Certificaatprofilel**, **Naam** en **Beschrijving**.

    > [!NOTE]
    > Het certificaatprofiel is een unieke ID van een certificaat voor alle bedrijven en Commerce-onderdelen.

1. Selecteer **Toevoegen** op het sneltabblad **Rechtspersoon**.
1. Selecteer de rechtspersoon (bedrijf) waarvoor het huidige certificaatprofiel moet worden gebruikt onder **Rechtspersoon**

    Als het certificaatprofiel moet worden gebruikt voor meerdere rechtspersonen, herhaalt u stap 4 en 5 om een regel toe te voegen voor elke aanvullende rechtspersoon.

1. Selecteer **Instellingen** om de pagina **Instellingen certificaatprofiel** te openen. Op deze pagina kunt u bedrijfsspecifieke instellingen voor het certificaatprofiel invoeren. Specificeer welke certificaten kunnen worden gebruikt wanneer het huidige certificaatprofiel wordt aangeroepen in de Commerce-kanalen. Voeg zoveel certificaten toe als u nodig hebt, en stel prioriteiten voor de certificaten in. Als een certificaat met een hogere prioriteit niet beschikbaar is, wordt het volgende certificaat gebruikt op basis van de prioriteit. Zie de sectie [Workflow: certificaten zoeken in de Commerce runtime](#workflow-searching-certificates-in-the-commerce-runtime) voor meer informatie.

    > [!NOTE]
    > Het veld **Prioriteit** wordt automatisch ingesteld. Een waarde van **1** staat voor de hoogste prioriteit. Wanneer een nieuwe regel op de pagina **Instellingen certificaatprofiel** wordt toegevoegd, wordt de prioriteit van de regel ingesteld op een nummer dat één hoger is dan de prioriteit van de vorige regel. Als u de prioriteit van een bepaalde regel wilt wijzigen, selecteert u de regel en selecteert u vervolgens **Omhoog** om de prioriteit te verhogen of **Omlaag** om de prioriteit te verlagen.

1. Wanneer u een nieuwe regel toevoegt op de pagina **Instellingen certificaatprofiel**, stelt u de volgende velden in:

    - **Locatietype**: selecteer de locatie waar het certificaat is opgeslagen. Dit veld heeft twee mogelijke waarden: **Lokaal certificaat** en **Sleutelkluis**.
    - **Sleutelkluiscertificaat**: dit veld is verplicht als u het veld **Locatietype** instelt op **Sleutelkluis**. Gebruik dit veld om een geheim voor een sleutelkluiscertificaat op te geven.
    - **Winkelnaam**: dit veld is optioneel en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**. Gebruik dit veld om een standaardwinkelnaam op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.
    - **Winkellocatie**: dit veld is optioneel en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**. Gebruik dit veld om een standaardwinkellocatie op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.

        > [!NOTE]
        > De standaardwinkelnaam en -winkellocatie worden toegevoegd om het zoeken naar lokale certificaten in Commerce Runtime te vereenvoudigen. X509StoreProvider heeft een lijst met mappen waarin certificaten worden opgeslagen. Als de standaardwinkelnaam en de standaardwinkellocatie niet worden opgegeven, probeert X509StoreProvider een certificaat in de andere mappen in de lijst te vinden. Zie [StoreName Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) en [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation) voor meer informatie over de beschikbare waarden voor de winkelnaam en de winkellocatie.

    - **Vingerafdruk**: dit veld is vereist en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**. Gebruik dit veld om de vingerafdruk van het certificaat op te geven.

        > [!IMPORTANT]
        > U moet ervoor zorgen dat de gebruiker die de toepassing beheert die het lokale certificaat moet gebruiken (bijvoorbeeld Modern POS in de offlinemodus) minimaal alleen-lezen toegang heeft tot de persoonlijke sleutel van het certificaat.

    - **Opmerkingen**: dit veld is optioneel en gebruikers kunnen opmerkingen in dit veld invoeren.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Werkstroom: certificaten zoeken in Commerce Runtime

Dit is de basiswerkstroom die wordt gebruikt om te zoeken naar een certificaat wanneer een certificaatprofiel wordt aangeroepen in Commerce Runtime.

1. In het systeem wordt bepaald of het certificaatprofiel bedrijfsspecifieke instellingen voor de huidige rechtspersoon heeft.
1. Er wordt geprobeerd het certificaat te vinden aan de hand van de waarden op de pagina **Instellingen certificaatprofiel** voor de regel waarvan het veld **Prioriteit** is ingesteld op **1**.

    - Als het veld **Locatietype** is ingesteld op **Sleutelkluis**, wordt de waarde van het veld **Geheim voor sleutelkluiscertificaat** gebruikt om te zoeken naar het certificaat op de pagina **Parameters sleutelkluis**. Het certificaat wordt vervolgens gezocht in de sleutelkluisopslag.
    - Als het veld **Locatietype** is ingesteld op **Lokaal certificaat**, zoekt X509StoreProvider eerst naar het certificaat met behulp van de standaardwinkelnaam en de standaardwinkellocatie, als deze parameters zijn opgegeven. Vervolgens wordt in alle andere mappen in de lijst met mappen gezocht.

1. Als het certificaat niet wordt gevonden, wordt het proces herhaald voor de regel waarvan het veld **Prioriteit** is ingesteld op **2**, enzovoort.

> [!NOTE]
> Als het certificaatprofiel geen instellingen heeft voor de huidige rechtspersoon of als de zoekopdracht naar het certificaat niet succesvol is voor alle regels op de pagina **Instellingen certificaatprofiel**, wordt het certificaat niet gevonden.

### <a name="caching-the-results-of-certificate-searches"></a>De resultaten van zoekopdrachten naar certificaten in de cache opslaan

De resultaten van zoekopdrachten naar certificaten worden in de cache opgeslagen. De standaardvervaltijd voor een cache is één uur. Deze tijd kan echter worden aangepast en kan worden ingesteld op een maximumwaarde van 24 uur.

## <a name="gradual-update"></a>Geleidelijke update

Als er een nieuwe versie van het certificaat wordt ingevoerd, maar deze niet in alle winkels tegelijk kan worden bijgewerkt, kan het certificaat geleidelijk worden bijgewerkt met de functionaliteit voor certificaatprofielen.

1. Zoek naar een certificaatprofiel en de regel die moeten worden bijgewerkt en selecteer vervolgens **Instellingen**.
1. Voeg een regel toe en geef instellingen op die betrekking hebben op de meest recente versie van het certificaat.
1. Verhoog de waarde van **Prioriteit** van de nieuwe regel. Gebruik de knop **Omhoog** om de regel zo te verplaatsen dat deze boven de regel staat voor de vorige versie van hetzelfde certificaat.
> [!NOTE]
> In Commerce Runtime wordt de nieuwe versie van het certificaat als eerste aangeroepen. Als het certificaat in een specifieke winkel of op een specifieke terminal niet is bijgewerkt, wordt de vorige versie aangeroepen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
