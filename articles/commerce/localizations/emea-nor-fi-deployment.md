---
title: Implementatierichtlijnen voor kassa's voor Noorwegen
description: Dit artikel biedt richtlijnen voor het inschakelen van de kassafunctionaliteit voor de Microsoft Dynamics 365 Commerce-lokalisatie voor Noorwegen.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 1f2226432237662e28b9e26017020ab81bb6026b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899062"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Implementatierichtlijnen voor kassa's voor Noorwegen

[!include[banner](../includes/banner.md)]

Dit artikel biedt richtlijnen voor het inschakelen van de kassafunctionaliteit voor de Microsoft Dynamics 365 Commerce-lokalisatie voor Noorwegen. De lokalisatie bestaat uit verschillende extensies van onderdelen. Met deze extensies kunt u bijvoorbeeld aangepaste velden afdrukken op ontvangstbewijzen , extra controlegebeurtenissen, verkooptransacties en betalingstransacties registreren in POS (Point-of-Sale), verkooptransacties digitaal ondertekenen en rapporten afdrukken in lokale indelingen. Zie [Kassafunctionaliteit voor Noorwegen](./emea-nor-cash-registers.md) voor meer informatie over de lokalisatie voor Noorwegen. Zie [Commerce instellen voor Noorwegen](./emea-nor-cash-registers.md#setting-up-commerce-for-norway) voor meer informatie over het configureren van Commerce voor Noorwegen.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor deze lokalisatiefunctionaliteit. U moet de versie van het voorbeeld voor digitaal ondertekenen voor Noorwegen gebruiken in de vorige versie van de Retail Software Development Kit (SDK) op een virtual machine (VM) voor ontwikkelaars in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor kassa's voor Noorwegen (verouderd)](./emea-nor-loc-deployment-guidelines.md) voor meer informatie.
>
> Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

## <a name="set-up-fiscal-registration-for-norway"></a>Fiscale registratie voor Noorwegen

Het voorbeeld van integratie van fiscale registratieservice voor Noorwegen is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\SequentialSignatureNorway** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider en een fiscale connector. Dit zijn extensies van de Commerce runtime (CRT). Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

Voltooi de instellingsstappen voor de fiscale registratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Een fiscaal registratieproces instellen](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Zorg ervoor dat u een notitie maakt van de instellingen van het fiscale registratieproces dat [specifiek voor Noorwegen](#configure-the-fiscal-registration-process) is.
1. [Instellingen voor het afhandelen van fouten uitvoeren](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Het fiscale registratieproces configureren

Volg deze stappen om het fiscale registratieproces voor Noorwegen in te schakelen in Commerce Headquarters.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector vanuit de Commerce SDK:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. De laatst beschikbare vertakkingsversie openen (bijvoorbeeld **[versie/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Open **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Download het configuratiebestand van de fiscale documentprovider op **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** (bijvoorbeeld [het bestand voor versie/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Download het configuratiebestand van de fiscale connector op **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** (bijvoorbeeld [het bestand voor versie/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde parameters**. Stel op het tabblad **Algemeen** de optie **Fiscale integratie inschakelen** in op **Ja**.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectors** en laad het configuratiebestand voor de fiscale connector die u eerder hebt gedownload.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale documentproviders** en laad het configuratiebestand voor de fiscale documentprovider die u eerder hebt gedownload.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Functionele connectorprofielen**. Maak een nieuw functioneel connectorprofiel en selecteer de documentprovider en connector die u eerder hebt geladen.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**. Maak een nieuw technisch connectorprofiel en selecteer de connector die u eerder hebt geladen. Het connectortype instellen op **Intern**.
1. Ga naar **Retail en commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen** en maak een nieuwe fiscale connectorgroep voor het functionele connectorprofiel dat u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**. Maak een nieuw fiscaal registratieproces en een stap in het fiscale registratieproces en selecteer de fiscale connectorgroep die u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**. Selecteer een functionaliteitsprofiel dat is gekoppeld aan de winkel waar het registratieproces moet worden geactiveerd. Selecteer op het sneltabblad **Fiscaal registratieproces** het fiscale registratieproces dat u eerder hebt gemaakt. Selecteer op het sneltabblad **Fiscale services** het technische connectorprofiel dat u eerder hebt gemaakt. 
1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**. Open het distributieschema en selecteer taken **1070** en **1090** om gegevens over te brengen naar de kanaaldatabase.

### <a name="configure-the-digital-signature-parameters"></a>Parameters voor digitale handtekeningen configureren

U moet certificaten configureren die worden gebruikt voor het digitaal ondertekenen van verkooptransacties in een winkel. Een digitaal certificaat dat is opgeslagen in Azure Key Vault wordt gebruikt voor het ondertekenen. Voor de offlinemodus van Modern POS kan het ondertekenen ook worden uitgevoerd door een digitaal certificaat te gebruiken dat is opgeslagen in de lokale opslag van de machine waarop Modern POS is geïnstalleerd.

Voordat u een digitaal certificaat kunt gebruiken dat is opgeslagen in de sleutelkluisopslag, moeten de volgende stappen worden uitgevoerd.

1. De sleutelkluisopslag moet worden gemaakt. Het wordt aangeraden de opslag in dezelfde geografische regio in te zetten als de Commerce Scale Unit.
1. Het certificaat moet als een geheim in base64-indeling worden geüpload naar de sleutelkluisopslag.
1. De AOS-toepassing (Application Object Server) moet zijn gemachtigd om geheimen uit de sleutelkluisopslag te lezen.

Zie [Aan de slag met Azure Key Vault](/azure/key-vault/key-vault-get-started) voor meer informatie over het werken met de sleutelkluis.

Vervolgens moet u op de pagina **Parameters voor sleutelkluis** de parameters voor het openen van de sleutelkluisopslag opgeven:

- **Naam** en **Beschrijving**: de naam en beschrijving van de sleutelkluisopslag.
- **URL sleutelkluis**: de URL van de sleutelkluisopslag.
- **Client sleutelkluis**: een interactieve client-id van de toepassing Azure Active Directory (Azure AD) die aan de sleutelkluisopslag is gekoppeld voor verificatiedoeleinden. Deze client moet leestoegang hebben tot geheimen vanuit de opslag.
- **Geheime sleutel voor sleutelkluis**: voer een geheime sleutel in die hoort bij de Azure AD-toepassing die voor verificatie wordt gebruikt in de sleutelkluisopslag.
- **Naam**, **Beschrijving** en **Geheime verwijzing**: de naam, beschrijving en geheime verwijzing van het certificaat.

Vervolgens moet u een connector configureren voor de certificaten die zijn opgeslagen in sleutelkluis- of lokale certificaatopslag. Deze connector wordt gebruikt voor het ondertekenen aan de kanaalzijde.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**.
1. Geef op het sneltabblad **Instellingen** de volgende parameters voor digitale handtekeningen op:

    - **Geheime naam**: selecteer de naam van het bedrijf dat u eerder hebt geconfigureerd op de pagina **Parameters voor sleutelkluis**.
    - **Lokale certificaatvingerafdruk:** verstrek een vingerafdruk voor een certificaat dat lokaal is opgeslagen.
    - **Hashalgoritme**: geef een van de cryptografische hashalgoritmen op die worden ondersteund door Microsoft .NET, zoals **SHA1**.
    - **Winkelnaam certificaat**: dit veld is optioneel. Gebruik dit veld om een standaardwinkelnaam op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.
    - **Winkellocatie certificaat**: dit veld is optioneel. Gebruik dit veld om een standaardwinkellocatie op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.
    - **Eerst lokaal certificaat proberen**: selecteer deze optie als u het certificaat van de lokale winkel standaard wilt gebruiken voor het ondertekenen van gegevens in plaats van het certificaat uit de sleutelkluis.
    - **Statuscontrole activeren**: zie [Statuscontrole fiscale registratie](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check) voor meer informatie over de statuscontrolefunctie.

> [!NOTE]
> - Alleen het **SHA1** cryptografische hashalgoritme is momenteel acceptabel voor Noorwegen.
> - De standaardwinkelnaam en -winkellocatie worden toegevoegd om het zoeken naar lokale certificaten in CRT te vereenvoudigen. X509StoreProvider heeft een lijst met mappen waarin certificaten worden opgeslagen. Als de standaardwinkelnaam en de standaardwinkellocatie niet worden opgegeven, probeert X509StoreProvider een certificaat in alle mappen in de lijst te vinden.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

### <a name="development-environment"></a>Ontwikkelingsomgeving

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Retail SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
1. Open de oplossing **SequentialSignatureNorway.sln** onder **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway** en bouw deze.
1. Installeer CRT-extensies:

    1. Zoek het installatieprogramma voor CRT-extensies:

        - **Commerce Scale Unit:** zoek in de map **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** het installatieprogramma **ScaleUnit.SequentialSignNorway.Installer**.
        - **Lokale CRT op Modern POS**: zoek in de map **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** het installatieprogramma **ModernPos.SequentialSignNorway.Installer**.

    1. Start het installatieprogramma voor CRT-extensies vanaf de opdrachtregel:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Lokale CRT op Modern POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Productieomgeving

Volg de stappen in [Een bouwpijplijn instellen voor een voorbeeld van fiscale integratie](fiscal-integration-sample-build-pipeline.md) voor het instellen en vrijgeven van de Cloud Scale Unit en selfservice implementeerbare pakketten voor het voorbeeld van fiscale integratie. Het YAML-sjabloonbestand **SequentialSignatureNorway build-pipeline.yaml** is te vinden in de map **Pipeline\\YAML_Files** van de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>De digitale handtekening inschakelen in de offline modus voor Modern POS

Als u de digitale handtekening wilt inschakelen in de offline modus voor Modern POS, moet u deze stappen volgen nadat u Modern POS hebt geactiveerd op een nieuw apparaat.

1. Meld u aan bij POS.
1. Zorg er op de pagina **Databaseverbindingsstatus** voor dat de offline database volledig is gesynchroniseerd. Wanneer de waarde van het veld **Downloads in behandeling** gelijk is aan **0** (nul), is de database volledig gesynchroniseerd.
1. Meld u af bij POS.
1. Wacht totdat de offline database volledig is gesynchroniseerd.
1. Meld u aan bij POS.
1. Zorg er op de pagina **Databaseverbindingsstatus** voor dat de offline database volledig is gesynchroniseerd. Wanneer de waarde van het veld **Transacties zijn in behandeling in offline database** gelijk is aan **0** (nul), is de database volledig gesynchroniseerd.
1. Open Modern POS opnieuw.
