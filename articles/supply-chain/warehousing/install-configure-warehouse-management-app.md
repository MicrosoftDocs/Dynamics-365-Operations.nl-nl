---
title: De mobiele app Magazijnbeheer installeren en verbinden
description: In dit onderwerp wordt uitgelegd hoe u de mobiele app Magazijnbeheer op al uw mobiele apparaten installeert en configureert om verbinding te maken met uw Microsoft Dynamics 365 Supply Chain Management-omgeving.
author: MarkusFogelberg
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f46c5d4ec78a1e5ed708687e8da6eb379697d5f4
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908947"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>De mobiele app Magazijnbeheer installeren en verbinden

[!include [banner](../includes/banner.md)]

> [!NOTE]
> In dit onderwerp wordt beschreven hoe u de nieuwe mobiele app Magazijnbeheer configureert. Zie [De magazijnapp installeren en verbinden](../../supply-chain/warehousing/install-configure-warehousing-app.md) als u informatie zoekt over het configureren van de oude magazijnapp (die nu is afgeschaft).

In dit onderwerp wordt uitgelegd hoe u de mobiele app Magazijnbeheer downloadt en op al uw mobiele apparaten installeert en hoe u de app configureert om verbinding te maken met uw Supply Chain Management-omgeving. U kunt elk apparaat handmatig configureren of u kunt verbindingsinstellingen importeren via een bestand of door een QR-code te scannen.

## <a name="system-requirements"></a>Systeemvereisten

De mobiele app Magazijnbeheer is beschikbaar voor de besturingssystemen van zowel Windows als Google Android. Als u de app wilt gebruiken, moet een van de volgende besturingssystemen op uw mobiele apparaten zijn geïnstalleerd:

- Windows 10 (Universal Windows Platform \[UWP\]) oktober 2018 update 1809 (build 10.0.17763) of later
- Android 4.4 of hoger

## <a name="turn-on-the-feature"></a>De functie inschakelen

Voordat u een app kunt gebruiken, moet een gerelateerde functie zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *gebruikersinstellingen, pictogrammen en staptitels voor de nieuwe magazijnapp*

## <a name="get-the-warehouse-management-mobile-app"></a>De mobiele app Magazijnbeheer downloaden

Voor kleinere implementaties kunt u de app vanuit de relevante store op elk apparaat installeren en vervolgens handmatig de verbinding configureren voor de omgevingen die u gebruikt.

Voor grotere implementaties kunt u de implementatie en/of configuratie van de app automatiseren. Dit kan handiger zijn als u meerdere apparaten beheert. U kunt bijvoorbeeld een oplossing voor het beheer van mobiele apparaten en een oplossing voor het beheer van mobiele toepassingen gebruiken, zoals [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Zie [Apps aan Microsoft Intune toevoegen](/mem/intune/apps/apps-add) voor informatie over het gebruik van Intune om toepassingen toe te voegen.

### <a name="install-the-app-from-an-app-store"></a>De app installeren vanuit een app store

De gemakkelijkste manier om de app op één apparaat te installeren, is de app te installeren vanuit een app store, die altijd de meest recente, algemene versie bevat. Microsoft Intune kan ook toepassingen ophalen van de app stores. Gebruik een van de volgende koppelingen om de app vanuit een app store te installeren:

- **Windows (UWP):** [Magazijnbeheer in Microsoft Store](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Magazijnbeheer in Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>De app downloaden vanuit Microsoft App Center

In plaats daarvan kunt u de app downloaden via het Microsoft App Center. Het App Center voorziet in installeerbare pakketten die u extern kunt laden. Naast de huidige versie kunt u met het App Center ook eerdere versies downloaden en preview-versies weergeven met toekomstige functies die u kunt proberen. Gebruik een van de volgende koppelingen om huidige, vorige of preview-versies van de mobiele app Magazijnbeheer te downloaden vanuit het Microsoft App Center:

- **Windows (UWP):** [Magazijnbeheer (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Zie [Een build installeren vanuit App Center](/appcenter/distribution/installation) voor instructies voor het installeren van een gedownload pakket op een Windows-apparaat en het instellen van de vereiste certificaten.

- **Android:** [Magazijnbeheer (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Als u een preview-versie downloadt, zijn er enkele extra stappen vereist om deze te installeren. Zie voor details [Android-apps testen](/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Een webservicetoepassing maken in Azure Active Directory

Als u de mobiele app Magazijnbeheer wilt inschakelen voor interactie met een specifieke Supply Chain Management-server, moet u een webservicetoepassing voor de Supply Chain Management-tenant registreren in Azure Active Directory (Azure AD). In de volgende procedure wordt één manier weergegeven om deze taak te voltooien. Zie de koppelingen na de procedure voor gedetailleerde informatie en alternatieven.

1. Ga in een webbrowser naar [https://portal.azure.com](https://portal.azure.com/).
1. Voer de naam en het wachtwoord in van de gebruiker die toegang heeft tot het Azure-abonnement.
1. Selecteer in de Azure-portal in het linkernavigatievenster de optie **Azure Active Directory**.

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. Controleer of u werkt met het exemplaar van Azure AD dat wordt gebruikt door Supply Chain Management.
1. Selecteer in de lijst **Beheren** de optie **App-registraties**.

    ![App-registraties](media/app-connect-azure-register.png "App-registraties")

1. Selecteer op de werkbalk de optie **Nieuwe registratie** om de wizard **Een toepassing registreren** te openen.
1. Voer een naam voor de toepassing in, selecteer de optie **Alleen accounts in deze organisatieadreslijst** en selecteer vervolgens **Registreren**.

    ![Wizard Een toepassing registreren](media/app-connect-azure-register-wizard.png "Wizard Een toepassing registreren")

1. Uw nieuwe app-registratie wordt geopend. Noteer de waarde in het veld **Toepassings-id (client)**. U hebt deze later nog nodig. Deze id wordt later in dit onderwerp aangeduid als de *client-id*.

    ![Id van toepassing (client)](media/app-connect-azure-app-id.png "Id van toepassing (client)")

1. Selecteer in de lijst **Beheren** de optie **Certificaat en geheimen**. Selecteer vervolgens een van de volgende knoppen, afhankelijk van hoe u de app wilt configureren voor verificatie. (Zie de sectie [Verifiëren via een certificaat of clientgeheim](#authenticate) verderop in dit onderwerp voor meer informatie.)

    - **Certificaat uploaden**: upload een certificaat voor gebruik als geheim. We raden deze benadering aan, omdat het veiliger is en ook meer kan worden geautomatiseerd. Als u de mobiele app Magazijnbeheer uitvoert op Windows-apparaten, noteert u de waarde voor **Vingerafdruk** die wordt weergegeven nadat u het certificaat hebt geüpload. U hebt deze waarde nodig wanneer u het certificaat op Windows-apparaten configureert.
    - **Nieuw clientgeheim**: maak een sleutel door een beschrijving en een duur voor de sleutel in te voeren in de sectie **Wachtwoorden** en selecteer vervolgens **Toevoegen**. Maak een kopie van de sleutel en sla deze veilig op.

    ![Certificaat en geheimen](media/app-connect-azure-authentication.png "Certificaat en geheimen")

Zie de volgende bronnen voor meer informatie over het instellen van webservicetoepassingen in Azure AD.

- Zie [Procedure: Azure PowerShell gebruiken om een service-principal te maken met een certificaat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) voor instructies voor het gebruik van Windows PowerShell om webservicetoepassingen in te stellen in Azure AD.
- Zie de volgende onderwerpen voor gedetailleerde informatie over het handmatig maken van een webservicetoepassing in Azure AD.

    - [Snelstart: Een toepassing registreren op het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app)
    - [Procedure: de portal gebruiken om een Azure AD-toepassing en een service-principal te maken die toegang hebben tot bronnen](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Een gebruikersaccount in Supply Chain Management maken en configureren

Voer de volgende stappen uit om Supply Chain Management in staat te stellen om uw Azure AD-toepassing te gebruiken.

1. Maak een gebruiker die met de gebruikersreferenties voor de mobiele app Magazijnbeheer overeenkomt:

    1. Ga in Supply Chain Management naar **Systeembeheer \> Gebruikers \> Gebruikers**.
    1. Maak een gebruiker.
    1. Wijs de gebruiker van het mobiele apparaat voor magazijnbeheer toe.

    ![De gebruiker van het mobiele apparaat voor magazijnbeheer toewijzen](media/app-connect-app-users.png "De gebruiker van het mobiele apparaat voor magazijnbeheer toewijzen")

1. Koppel uw Azure AD-toepassing aan de gebruiker van de mobiele app Magazijnbeheer:

    1. Ga naar **Systeembeheer \> Instellingen \> Azure Active Directory-toepassingen**.
    1. Maak een regel.
    1. Voer de client-id in waarvan u een notitie hebt gemaakt in de vorige sectie, geef deze een naam en selecteer de gebruiker die u zojuist hebt gemaakt. We adviseren u om al uw apparaten te labelen. Als een apparaat dan kwijtraakt, kunt u de toegang ervan tot Supply Chain Management eenvoudig verwijderen vanaf deze pagina.

    ![Azure Active Directory-toepassingen](media/app-connect-aad-apps.png "Azure Active Directory-toepassingen")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Verifiëren via een certificaat of clientgeheim

Verificatie met Azure AD biedt een veilige manier om een mobiel apparaat te verbinden met Supply Chain Management. U kunt verifiëren via een clientgeheim of een certificaat. Als u verbindingsinstellingen gaat importeren, is het raadzaam een certificaat te gebruiken in plaats van een clientgeheim. Omdat het clientgeheim altijd veilig moet worden opgeslagen, kunt u het niet importeren vanuit een bestand met verbindingsinstellingen of een QR-code, zoals verderop in dit onderwerp wordt beschreven.

Certificaten kunnen worden gebruikt als geheimen om de identiteit van de toepassing te bewijzen wanneer een token wordt aangevraagd. Het openbare gedeelte van het certificaat wordt geüpload naar de app-registratie in de Azure-portal, terwijl het volledige certificaat moet worden geïmplementeerd op elk apparaat waarop de mobiele app Magazijnbeheer is geïnstalleerd. Uw organisatie is verantwoordelijk voor het beheer van het certificaat wat betreft rotatie en dergelijke. U kunt zelfondertekende certificaten gebruiken, maar u moet altijd met niet-exporteerbare certificaten werken.

U moet het certificaat lokaal beschikbaar maken voor elk apparaat waarop u de mobiele app Magazijnbeheer uitvoert. Zie [Certificaten voor verificatie gebruiken in Microsoft Intune](/mem/intune/protect/certificates-configure) voor informatie over het beheren van certificaten voor door Intune beheerde apparaten als u Intune gebruikt.

## <a name="configure-the-application-by-importing-connection-settings"></a>De toepassing configureren door verbindingsinstellingen te importeren

Om het gemakkelijker te maken om de toepassing op veel mobiele apparaten te onderhouden en te implementeren, kunt u de verbindingsinstellingen importeren in plaats van deze handmatig op elk apparaat in te voeren. In deze sectie wordt uitgelegd hoe u de instellingen maakt en importeert.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Een bestand met verbindingsinstellingen of QR-code maken

U kunt verbindingsinstellingen importeren vanuit een bestand of een QR-code. Voor beide benaderingen moet u eerst een instellingenbestand maken dat gebruikmaakt van de JSON-indeling (JavaScript Object Notation) en -syntaxis. Het bestand moet een lijst met verbindingen bevatten met de afzonderlijke verbindingen die moeten worden toegevoegd. De volgende tabel bevat een overzicht van de parameters die u moet opgeven in het bestand met verbindingsinstellingen.

| Parameter | Omschrijving |
|---|---|
| ConnectionName | Geef de naam op van de verbindingsinstelling. De tekst mag maximaal 20 tekens lang zijn. Omdat deze waarde de unieke id voor een verbindingsinstelling is, moet u ervoor zorgen dat deze uniek is in de lijst. Als er al een verbinding met dezelfde naam op het apparaat aanwezig is, wordt deze overschreven door de instellingen van het geïmporteerde bestand. |
| ActiveDirectoryClientAppId | Geef de client-id op waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Geef de basis-URL van Supply Chain Management op. |
| ActiveDirectoryTenant | Geef de Azure AD-tenant op die u gebruikt met de server voor Supply Chain Management. Deze waarde heeft de vorm `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Hier volgt een voorbeeld: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
| Bedrijf | Geef de rechtspersoon in Supply Chain Management op waarmee de toepassing verbinding moet maken. |
| ConnectionType | (Optioneel) Geef op of de verbindingsinstelling een certificaat of clientgeheim moet gebruiken om verbinding te maken met een omgeving. Geldige waarden zijn *"certificate"* en *"clientsecret"*. De standaardwaarde is *"certificate"*.<p>**Opmerking:** clientgeheimen kunnen niet worden geïmporteerd.</p> |
| IsEditable | (Optioneel) Geef op of de app-gebruiker de verbindingsinstelling moet kunnen bewerken. Geldige waarden zijn *"true"* en *"false"*. De standaardwaarde is *"true"*. |
| IsDefault | (Optioneel) Geef op of de verbinding de standaardverbinding is. Een verbinding die is ingesteld als de standaardverbinding wordt automatisch ingeschakeld wanneer de app wordt geopend. U kunt slechts één verbinding instellen als de standaardverbinding. Geldige waarden zijn *"true"* en *"false"*. De standaardwaarde is *"false"*. |
| CertificateThumbprint | (Optioneel) Voor Windows-apparaten kunt u de vingerafdruk van het certificaat voor de verbinding opgeven. Voor Android-apparaten moet de gebruiker van de app het certificaat selecteren wanneer een verbinding voor het eerst wordt gebruikt. |

Het volgende voorbeeld toont een geldig bestand met verbindingsinstellingen dat twee verbindingen bevat. Zoals u ziet, is de lijst met verbindingen (met de naam *'ConnectionList'* in het bestand) een object dat een matrix heeft waarin elke verbinding als een object wordt opgeslagen. Elk object moet tussen accolades ({}) worden geplaatst en worden gescheiden door komma's, terwijl de matrix tussen vierkante haken (\[\]) moet staan.

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

U kunt de gegevens opslaan als een JSON-bestand of een QR-code met dezelfde inhoud genereren. Als u de gegevens als een bestand opslaat, is het aan te raden de standaardnaam, *connections.json* te gebruiken, met name als u de gegevens opslaat op de standaardlocatie op elk mobiel apparaat.

### <a name="save-the-connection-settings-file-on-each-device"></a>Het bestand met de verbindingsinstellingen opslaan op elk apparaat

Meestal gebruikt u een hulpprogramma voor apparaatbeheer of een script voor het distribueren van de bestanden met verbindingsinstellingen naar elk apparaat dat u beheert. Als u de standaardnaam en -locatie gebruikt wanneer u het bestand met verbindingsinstellingen opslaat op elk apparaat, wordt dit door de mobiele app Magazijnbeheer automatisch geïmporteerd, zelfs tijdens de eerste uitvoering nadat de app is geïnstalleerd. Als u een aangepaste naam of locatie voor het bestand gebruikt, moet de app-gebruiker de waarden opgeven tijdens de eerste uitvoering. De opgegeven naam en locatie worden echter naderhand door de app gebruikt.

Telkens wanneer de app wordt gestart, worden de verbindingsinstellingen van de vorige locatie opnieuw geïmporteerd om te bepalen of er wijzigingen zijn aangebracht. De app werkt alleen verbindingen bij die dezelfde naam hebben als de verbindingen in het bestand met verbindingsinstellingen. Door de gebruiker gemaakte verbindingen waarbij andere namen worden gebruikt, worden niet bijgewerkt.

U kunt een verbinding niet verwijderen via het bestand met verbindingsinstellingen.

Zoals aangegeven, is *connections.json* de standaardbestandsnaam. De standaardbestandslocatie is afhankelijk van het feit of u een Windows-apparaat of een Android-apparaat gebruikt:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Gewoonlijk worden de paden automatisch gemaakt na de eerste uitvoering van de app. U kunt ze echter handmatig maken als u het bestand met verbindingsinstellingen vóór de installatie naar het apparaat moet overzetten.

> [!NOTE]
> Als de app wordt verwijderd, worden het standaardpad en de inhoud hiervan verwijderd.

### <a name="import-the-connection-settings"></a>De verbindingsinstellingen importeren

Volg deze stappen om verbindingsinstellingen te importeren vanuit een bestand of een QR-code.

1. Start de mobiele app Magazijnbeheer op uw mobiele apparaat. De eerste keer dat u de app start, wordt een welkomstbericht weergegeven. Selecteer **Een verbinding selecteren**.

    ![Welkomstbericht](media/app-configure-welcome-screen.png "Welkomstbericht")

1. Als u de verbindingsinstellingen vanuit een bestand importeert en de standaardnaam en -locatie zijn gebruikt bij het opslaan van het bestand, kan de app het bestand mogelijk al hebben gevonden. Ga in dit geval verder naar stap 4. Anders selecteert **Verbinding instellen** en gaat u door naar stap 3.

    ![Verbinding instellen](media/app-configure-set-up-connection.png "Verbinding instellen")

1. Selecteer in het dialoogvenster **Verbindingsinstellingen** de optie **Uit bestand toevoegen** of **Uit QR-code toevoegen**, afhankelijk van hoe u de instellingen wilt importeren:

    - Als u de verbindingsinstellingen vanuit een bestand importeert, selecteert u **Uit bestand toevoegen**, bladert u naar het bestand op het lokale apparaat en selecteert u dit bestand. Als u een aangepaste locatie selecteert, wordt deze door de app opgeslagen en de volgende keer automatisch gebruikt.
    - Als u de verbindingsinstellingen importeert door een QR-code te scannen, selecteert u **Uit QR-code toevoegen**. De app vraagt u om toestemming om de camera van het apparaat te gebruiken. Nadat u toestemming hebt gegeven, wordt de camera gestart, zodat u deze kunt gebruiken voor het scannen. Afhankelijk van de kwaliteit van de camera van het apparaat en de complexiteit van de QR-code kan het lastig zijn om een correcte scan te krijgen. Probeer in dat geval de complexiteit van de QR-code te verminderen door slechts één verbinding per QR-code te genereren. (Momenteel kunt u alleen de camera van het apparaat gebruiken om de QR-code te scannen.)

    ![Menu Verbindingsinstellingen](media/app-configure-connection-setup-flyout.png "Menu Verbindingsinstellingen")

1. Wanneer de verbindingsinstellingen zijn geladen, wordt de geselecteerde verbinding weergegeven.

    ![Verbindingsinstellingen geladen](media/app-configure-select-connection.png "Verbindingsinstellingen geladen")

1. Als u met een Android-apparaat werkt en een certificaat voor verificatie gebruikt, vraagt het apparaat u om het certificaat te selecteren.

    ![Certificaatprompt selecteren op een Android-apparaat](media/app-configure-select-certificate.png "Certificaatprompt selecteren op een Android-apparaat")

1. De app maakt verbinding met uw Supply Chain Management-server en geeft de aanmeldingspagina weer.

    ![Aanmeldingspagina](media/app-configure-sign-in-page.png "Aanmeldingspagina")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>De toepassing handmatig configureren

Als u geen bestand of QR-code hebt, kunt u de app handmatig configureren op het apparaat zodat deze verbinding maakt met de Supply Chain Management-server via de Azure AD-toepassing.

1. Start de mobiele app Magazijnbeheer op uw mobiele apparaat.
1. Selecteer **Verbindingsinstellingen** als de app is gestart in de **demonstratiemodus**. Als de pagina **Aanmelden** wordt weergegeven wanneer de app wordt gestart, selecteert u **Verbinding wijzigen**.
1. Selecteer **Verbinding instellen**.

    ![Verbinding instellen](media/app-configure-set-up-connection.png "Verbinding instellen")

1. Selecteer **Handmatig invoeren**.

    ![Menu Verbindingsinstellingen](media/app-configure-connection-setup-flyout.png "Menu Verbindingsinstellingen")

    De pagina **Nieuwe verbinding** wordt weergegeven en toont de instellingen die nodig zijn om de verbindingsgegevens handmatig in te voeren.

    ![Handmatige verbindingsvelden](media/app-configure-input-manually.png "Handmatige verbindingsvelden")

1. Voer de volgende gegevens in:

    - **Clientgeheim gebruiken**: stel deze optie in op _Ja_ als u een clientgeheim wilt gebruiken voor verificatie met Supply Chain Management. Stel deze in op _Nee_ om een certificaat voor verificatie te gebruiken. (Zie voor meer informatie de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service) eerder in dit onderwerp.)
    - **Verbindingsnaam**: voer een naam in voor de nieuwe verbinding. Deze naam wordt weergegeven in het veld **Verbinding selecteren** wanneer u de verbindingsinstellingen de volgende keer opent. De naam die u invoert, moet uniek zijn. (Met andere woorden, de naam moet verschillen van alle andere verbindingsnamen die op het apparaat zijn opgeslagen als er daar nog andere verbindingsnamen zijn opgeslagen.)
    - **Client-id Active Directory**: geef de client-id op waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service).
    - **Clientgeheim Active Directory**: dit veld is alleen beschikbaar wanneer de optie **Clientgeheim gebruiken** is ingesteld op _Ja_. Voer het clientgeheim in waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service).
    - **Vingerafdruk Active Directory-certificaat**: dit veld is alleen beschikbaar voor Windows-apparaten en alleen wanneer de optie **Clientgeheim gebruiken** is ingesteld op _Nee_. Voer de vingerafdruk voor het certificaat in waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service).
    - **Resource Active Directory**: geef de basis-URL op van Supply Chain Management.

        > [!IMPORTANT]
        > Sluit deze waarde niet af met een slash (/).

    - **Tenant Active Directory**: voer de Azure AD-tenant in die u gebruikt met de Supply Chain Management-server. Deze waarde heeft de vorm `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Hier volgt een voorbeeld: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!IMPORTANT]
        > Sluit deze waarde niet af met een slash (/).

    - **Bedrijf**: voer de rechtspersoon (bedrijf) in Supply Chain Management in waarmee u de toepassing verbinding wilt laten maken.

1. Selecteer de knop **Opslaan** in de rechterbovenhoek van de pagina.
1. Als u met een Android-apparaat werkt en een certificaat voor verificatie gebruikt, vraagt het apparaat u om het certificaat te selecteren.
1. De app maakt verbinding met uw Supply Chain Management-server en geeft de aanmeldingspagina weer.

## <a name="remove-access-for-a-device"></a>Toegang voor een apparaat verwijderen

Als een apparaat is verloren of beschadigd, moet u de toegang tot Supply Chain Management voor het apparaat verwijderen. In de volgende stappen wordt het aanbevolen proces beschreven om de toegang uit te schakelen.

1. Ga naar **Systeembeheer \> Instellingen \> Azure Active Directory-toepassingen**.
1. Verwijder de regel die overeenkomt met het apparaat waarvoor u de toegang wilt verwijderen. Noteer de client-id die wordt gebruikt voor het apparaat, omdat u deze later nodig hebt.

    Als u slechts één client-id hebt geregistreerd en meerdere apparaten dezelfde client-id gebruiken, moet u de nieuwe verbindingsinstellingen naar die apparaten overbrengen. Anders raken zij de toegang kwijt.

1. Meld u aan bij de Azure-portal op [https://portal.azure.com](https://portal.azure.com/).
1. Selecteer in het linkernavigatievenster de optie **Active Directory** en controleer of u zich in de juiste map bevindt.
1. Selecteer in de lijst **Beheren** de optie **App-registraties** en selecteer vervolgens de toepassing die u wilt configureren. De pagina **Instellingen** wordt weergegeven met informatie over de configuratie.
1. Controleer of de client-id van de toepassing overeenkomt met de client-id waarvan u in stap 2 een notitie hebt gemaakt.
1. Selecteer **Verwijderen** op de werkbalk.
1. Selecteer **Ja** in het bevestigingsbericht dat wordt weergegeven.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]