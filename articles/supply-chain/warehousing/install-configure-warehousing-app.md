---
title: De magazijnapp installeren en verbinden
description: In dit onderwerp wordt uitgelegd hoe u de magazijnapp op al uw mobiele apparaten installeert en configureert om verbinding te maken met uw Microsoft Dynamics 365 Supply Chain Management-omgeving. U kunt elk apparaat handmatig configureren of u kunt verbindingsinstellingen importeren via een bestand of door een QR-code te scannen.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 411a97427bbb16388e0f60b8ecb5dd3e5a79e87e
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142270"
---
# <a name="install-and-connect-the-warehouse-app"></a>De app voor magazijnbeheer installeren en verbinden

[!include [banner](../includes/banner.md)]

> [!NOTE]
> In dit onderwerp wordt beschreven hoe u de oude magazijnapp kunt configureren. Raadpleeg [De mobiele app Magazijnbeheer installeren en verbinden](install-configure-warehouse-management-app.md) als u wilt weten hoe u de nieuwe mobiele app Magazijnbeheer kunt configureren (momenteel in een openbare preview).

> [!NOTE]
> In dit onderwerp wordt beschreven hoe u de magazijnapp voor cloudimplementaties configureert. Als u op zoek bent naar informatie over hoe u de magazijnapp configureert voor on-premises implementaties, raadpleegt u [Magazijnbeheer voor on-premises implementaties](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

De magazijnapp is beschikbaar in Google Play Store en Microsoft Store. Deze wordt als zelfstandig onderdeel geleverd. Daarom moet u de app op elk apparaat downloaden en vervolgens configureren om verbinding te maken met uw Microsoft Dynamics 365 Supply Chain Management-omgeving.

In dit onderwerp wordt uitgelegd hoe u de magazijnapp op al uw mobiele apparaten installeert en configureert om verbinding te maken met uw Supply Chain Management-omgeving. U kunt elk apparaat handmatig configureren of u kunt verbindingsinstellingen importeren via een bestand of door een QR-code te scannen.

## <a name="system-requirements"></a>Systeemvereisten

De magazijnapp is beschikbaar voor de besturingssystemen Windows en Android. Als u de meest recente versie van de app wilt gebruiken, moet u een van de volgende besturingssystemen op uw mobiele apparaten hebben geïnstalleerd:

- Windows 10 (Universal Windows Platform \[UWP\]) makersupdate najaar 1709 (build 10.0.16299) of hoger
- Android 4.4 of hoger

> [!NOTE]
> Als u oudere Windows-apparaten moet ondersteunen waarop de meest recente versie van Windows niet kan worden uitgevoerd, kunt u nog steeds versie 1.6.3.0 van de magazijnapp downloaden vanuit de Microsoft Store. Deze versie wordt uitgevoerd onder Windows 10 (UWP) update voor november 1511 (build 10.0.10586) of hoger. Houd er echter rekening mee dat deze versie van de magazijnapp geen grootschalige implementatie van verbindingsinstellingen ondersteunt. Daarom moet u [de verbinding handmatig configureren](#config-manually) op elk apparaat waarop deze versie van de app wordt uitgevoerd.

## <a name="get-the-warehouse-app"></a>De magazijnapp installeren

Gebruik een van de volgende koppelingen om de app te downloaden:

- **Windows (UWP):** [Dynamics 365 for Finance and Operations - Magazijnbeheer in de Microsoft Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Warehousing - Dynamics 365 in de Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Voor kleinere implementaties wilt u de app mogelijk vanuit de relevante store op elk apparaat installeren en vervolgens handmatig de verbinding configureren voor de omgevingen die u gebruikt. In versie 1.7.0.0 en hoger van de magazijnapp kunt u echter ook de implementatie en/of configuratie van de app automatiseren. U zult deze aanpak wellicht handig vinden als u veel apparaten beheert en een oplossing voor beheer van mobiele apparaten gebruikt, zoals [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune). Zie [Apps aan Microsoft Intune toevoegen](https://docs.microsoft.com/mem/intune/apps/apps-add) voor informatie over het gebruik van Intune om toepassingen toe te voegen.

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Een webservicetoepassing maken in Azure Active Directory

Als u de magazijnapp wilt inschakelen voor interactie met een specifieke Supply Chain Management-server, moet u een webservicetoepassing voor de Supply Chain Management-tenant registreren in Azure Active Directory (Azure AD). In de volgende procedure wordt één manier weergegeven om deze taak te voltooien. Zie de koppelingen na de procedure voor gedetailleerde informatie en alternatieven.

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

    - **Certificaat uploaden**: upload een certificaat voor gebruik als geheim. We raden deze benadering aan, omdat het veiliger is en ook meer kan worden geautomatiseerd. Als u de magazijnapp uitvoert op Windows-apparaten, noteert u de waarde voor **Vingerafdruk** die wordt weergegeven nadat u het certificaat hebt geüpload. U hebt deze waarde nodig wanneer u het certificaat op Windows-apparaten configureert.
    - **Nieuw clientgeheim**: maak een sleutel door een beschrijving en een duur voor de sleutel in te voeren in de sectie **Wachtwoorden** en selecteer vervolgens **Toevoegen**. Maak een kopie van de sleutel en sla deze veilig op.

    ![Certificaat en geheimen](media/app-connect-azure-authentication.png "Certificaat en geheimen")

Zie de volgende bronnen voor meer informatie over het instellen van webservicetoepassingen in Azure AD.

- Zie [Procedure: Azure PowerShell gebruiken om een service-principal te maken met een certificaat](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell) voor instructies voor het gebruik van Windows PowerShell om webservicetoepassingen in te stellen in Azure AD.
- Zie de volgende onderwerpen voor gedetailleerde informatie over het handmatig maken van een webservicetoepassing in Azure AD.

    - [Snelstart: Een toepassing registreren op het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Procedure: de portal gebruiken om een Azure AD-toepassing en een service-principal te maken die toegang hebben tot bronnen](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Een gebruikersaccount in Supply Chain Management maken en configureren

Voer de volgende stappen uit om Supply Chain Management in staat te stellen om uw Azure AD-toepassing te gebruiken.

1. Maak een gebruiker die met de gebruikersreferenties voor de magazijnapp:

    1. Ga in Supply Chain Management naar **Systeembeheer \> Gebruikers \> Gebruikers**.
    1. Maak een gebruiker.
    1. Wijs de gebruiker van het mobiele apparaat voor magazijnbeheer toe.

    ![De gebruiker van het mobiele apparaat voor magazijnbeheer toewijzen](media/app-connect-app-users.png "De gebruiker van het mobiele apparaat voor magazijnbeheer toewijzen")

1. Koppel uw Azure AD-toepassing aan de gebruiker van de magazijnapp:

    1. Ga naar **Systeembeheer \> Instellingen \> Azure Active Directory-toepassingen**.
    1. Maak een regel.
    1. Voer de client-id in waarvan u een notitie hebt gemaakt in de vorige sectie, geef deze een naam en selecteer de gebruiker die u zojuist hebt gemaakt. We adviseren u om al uw apparaten te labelen. Als u deze dan kwijtraakt, kunt u hun toegang tot Supply Chain Management eenvoudig verwijderen vanaf deze pagina.

    ![Azure Active Directory-toepassingen](media/app-connect-aad-apps.png "Azure Active Directory-toepassingen")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Verifiëren via een certificaat of clientgeheim

Verificatie met Azure AD biedt een veilige manier om een mobiel apparaat te verbinden met Supply Chain Management. U kunt verifiëren via een clientgeheim of een certificaat. Als u verbindingsinstellingen gaat importeren, is het raadzaam een certificaat te gebruiken in plaats van een clientgeheim. Omdat het clientgeheim altijd veilig moet worden opgeslagen, kunt u het niet importeren vanuit een bestand met verbindingsinstellingen of een QR-code, zoals verderop in dit onderwerp wordt beschreven.

Certificaten kunnen worden gebruikt als geheimen om de identiteit van de toepassing te bewijzen wanneer een token wordt aangevraagd. Het openbare gedeelte van het certificaat wordt geüpload naar de app-registratie in de Azure-portal, terwijl het volledige certificaat moet worden geïmplementeerd op elk apparaat waarop de magazijnapp is geïnstalleerd. Uw organisatie is verantwoordelijk voor het beheer van het certificaat wat betreft rotatie en dergelijke. U kunt zelfondertekende certificaten gebruiken, maar u moet altijd met niet-exporteerbare certificaten werken.

U moet het certificaat lokaal beschikbaar maken voor elk apparaat waarop u de magazijnapp uitvoert. Zie [Certificaten voor verificatie gebruiken in Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-configure) voor informatie over het beheren van certificaten voor door Intune beheerde apparaten als u Intune gebruikt.

## <a name="configure-the-application-by-importing-connection-settings"></a>De toepassing configureren door verbindingsinstellingen te importeren

Om het gemakkelijker te maken om de toepassing op veel mobiele apparaten te onderhouden en te implementeren, kunt u de verbindingsinstellingen importeren in plaats van deze handmatig op elk apparaat in te voeren. In deze sectie wordt uitgelegd hoe u de instellingen maakt en importeert.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Een bestand met verbindingsinstellingen of QR-code maken

U kunt verbindingsinstellingen importeren vanuit een bestand of een QR-code. Voor beide benaderingen moet u eerst een instellingenbestand maken dat gebruikmaakt van de JSON-indeling (JavaScript Object Notation) en -syntaxis. Het bestand moet een lijst met verbindingen bevatten met de afzonderlijke verbindingen die moeten worden toegevoegd. De volgende tabel bevat een overzicht van de parameters die u moet opgeven in het bestand met verbindingsinstellingen.

| Parameter | Omschrijving |
| --- | --- |
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

Meestal gebruikt u een hulpprogramma voor apparaatbeheer of een script voor het distribueren van de bestanden met verbindingsinstellingen naar elk apparaat dat u beheert. Als u de standaardnaam en -locatie gebruikt wanneer u het bestand met verbindingsinstellingen opslaat op elk apparaat, wordt dit door de magazijnapp automatisch geïmporteerd, zelfs tijdens de eerste uitvoering nadat de app is geïnstalleerd. Als u een aangepaste naam of locatie voor het bestand gebruikt, moet de app-gebruiker de waarden opgeven tijdens de eerste uitvoering. De opgegeven naam en locatie worden echter naderhand door de app gebruikt.

Telkens wanneer de app wordt gestart, worden de verbindingsinstellingen van de vorige locatie opnieuw geïmporteerd om te bepalen of er wijzigingen zijn aangebracht. De app werkt alleen verbindingen bij die dezelfde naam hebben als de verbindingen in het bestand met verbindingsinstellingen. Door de gebruiker gemaakte verbindingen waarbij andere namen worden gebruikt, worden niet bijgewerkt.

U kunt een verbinding niet verwijderen via het bestand met verbindingsinstellingen.

Zoals aangegeven, is *connections.json* de standaardbestandsnaam. De standaardbestandslocatie is afhankelijk van het feit of u een Windows-apparaat of een Android-apparaat gebruikt:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Gewoonlijk worden de paden automatisch gemaakt na de eerste uitvoering van de app. U kunt ze echter handmatig maken als u het bestand met verbindingsinstellingen vóór de installatie naar het apparaat moet overzetten.

> [!NOTE]
> Als de app wordt verwijderd, worden het standaardpad en de inhoud hiervan verwijderd.

### <a name="import-the-connection-settings"></a>De verbindingsinstellingen importeren

Volg deze stappen om verbindingsinstellingen te importeren vanuit een bestand of een QR-code.

1. Open de magazijnapp op uw mobiele apparaat.
1. Ga naar **Verbindingsinstellingen**.
1. Stel de optie **Demomodus gebruiken** in op _Nee_.

    ![Optie Demomodus gebruiken](media/app-connect-app-demo-mode.png "Optie Demomodus gebruiken")

1. Selecteer **Bestand selecteren** of **QR-code scannen**, afhankelijk van hoe u de instellingen wilt importeren:

    - Als u de verbindingsinstellingen vanuit een bestand importeert, kan de app het bestand mogelijk al hebben gevonden als de standaardnaam en de standaardlocatie zijn gebruikt bij het opslaan van het bestand. Selecteer anders **Bestand selecteren**, blader naar het bestand op het lokale apparaat en selecteer het. Als u een aangepaste locatie selecteert, wordt deze door de app opgeslagen en de volgende keer automatisch gebruikt.
    - Als u de verbindingsinstellingen importeert door een QR-code te scannen, selecteert u **QR-code scannen**. De app vraagt u om toestemming om de camera van het apparaat te gebruiken. Nadat u toestemming hebt gegeven, wordt de camera gestart, zodat u deze kunt gebruiken voor het scannen. Afhankelijk van de kwaliteit van de camera van het apparaat en de complexiteit van de QR-code kan het lastig zijn om een correcte scan te krijgen. Probeer in dat geval de complexiteit van de QR-code te verminderen door slechts één verbinding per QR-code te genereren. (Momenteel kunt u alleen de camera van het apparaat gebruiken om de QR-code te scannen.)

    ![Verbindingsinstellingen importeren](media/app-connect-app-select-file.png "Verbindingsinstellingen importeren")

1. Wanneer de verbindingsinstellingen zijn geladen, selecteert u de knop **Vorige** (pijl naar links) in de linkerbovenhoek van de pagina.

    ![Verbindingsinstellingen geladen](media/app-connect-app-settings-loaded.png "Verbindingsinstellingen geladen")

1. Als u met een Android-apparaat werkt en een certificaat voor verificatie gebruikt, vraagt het apparaat u om het certificaat te selecteren.

    ![Certificaatprompt kiezen op een Android-apparaat](media/app-connect-app-choose-cert.png "Certificaatprompt kiezen op een Android-apparaat")

1. De app maakt verbinding met uw Supply Chain Management-server en geeft de aanmeldingspagina weer.

    ![Aanmeldingspagina](media/app-connect-sign-in.png "Aanmeldingspagina")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>De toepassing handmatig configureren

U kunt de app handmatig configureren op het apparaat zodat deze verbinding maakt met de Supply Chain Management-server via de Azure AD-toepassing.

1. Open de magazijnapp op uw mobiele apparaat.
1. Ga naar **Verbindingsinstellingen**.
1. Stel de optie **Demomodus gebruiken** in op _Nee_.

    ![Demomodus uitgeschakeld](media/app-connect-app-select-file.png "Demomodus uitgeschakeld")

1. Tik op het veld **Verbinding selecteren** om de instellingen uit te vouwen die nodig zijn om de verbindingsgegevens handmatig in te voeren.

    ![Handmatige verbindingsvelden](media/app-connect-manual-connect.png "Handmatige verbindingsvelden")

1. Voer de volgende gegevens in:

    - **Clientgeheim gebruiken**: stel deze optie in op _Ja_ als u een clientgeheim wilt gebruiken voor verificatie met Supply Chain Management. Stel deze in op _Nee_ om een certificaat voor verificatie te gebruiken. (Zie [Een webservicetoepassing maken in Azure Active Directory](#create-service) voor meer informatie.)
    - **Verbindingsnaam**: voer een naam in voor de nieuwe verbinding. Deze naam wordt weergegeven in het veld **Verbinding selecteren** wanneer u de verbindingsinstellingen de volgende keer opent. De naam die u invoert, moet uniek zijn. (Met andere woorden, de naam moet verschillen van alle andere verbindingsnamen die op het apparaat zijn opgeslagen als er daar nog andere verbindingsnamen zijn opgeslagen.).
    - **Client-id Active Directory**: geef de client-id op waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service).
    - **Clientgeheim Active Directory**: dit veld is alleen beschikbaar wanneer de optie **Clientgeheim gebruiken** is ingesteld op _Ja_. Voer het clientgeheim in waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service).
    - **Vingerafdruk Active Directory-certificaat**: dit veld is alleen beschikbaar voor Windows-apparaten wanneer de optie **Clientgeheim gebruiken** is ingesteld op _Nee_. Voer de vingerafdruk voor het certificaat in waarvan u een notitie hebt gemaakt terwijl u bezig was met het instellen van Azure AD in de sectie [Een webservicetoepassing maken in Azure Active Directory](#create-service).
    - **Resource Active Directory**: geef de basis-URL op van Supply Chain Management.

        > [!NOTE]
        > Sluit deze waarde niet af met een slash (/).

    - **Tenant Active Directory**: voer de Azure AD-tenant in die u gebruikt met de Supply Chain Management-server. Deze waarde heeft de vorm `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Hier volgt een voorbeeld: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Sluit deze waarde niet af met een slash (/).

    - **Bedrijf**: voer de rechtspersoon in Supply Chain Management in waarmee u de toepassing verbinding wilt laten maken.

1. Selecteer de knop **Opslaan** in de rechterbovenhoek van de pagina.
1. Als u met een Android-apparaat werkt en een certificaat voor verificatie gebruikt, vraagt het apparaat u om het certificaat te selecteren.
1. De app maakt verbinding met uw Supply Chain Management-server en geeft de aanmeldingspagina weer.

## <a name="remove-access-for-a-device"></a>Toegang voor een apparaat verwijderen

In geval van een verloren of beschadigd apparaat moet u de toegang tot Supply Chain Management voor het apparaat verwijderen. In de volgende stappen wordt het aanbevolen proces beschreven om de toegang uit te schakelen.

1. Ga naar **Systeembeheer \> Instellingen \> Azure Active Directory-toepassingen**.
1. Verwijder de regel die overeenkomt met het apparaat waarvoor u de toegang wilt verwijderen. Noteer de client-id die wordt gebruikt voor het verwijderde apparaat, omdat u deze later nodig hebt.

    Als u slechts één client-id hebt geregistreerd en meerdere apparaten dezelfde client-id gebruiken, moet u de nieuwe verbindingsinstellingen naar die apparaten overbrengen. Anders raken zij de toegang kwijt.

1. Meld u aan bij de Azure-portal op [https://portal.azure.com](https://portal.azure.com/).
1. Selecteer in het linkernavigatievenster de optie **Active Directory** en controleer of u zich in de juiste map bevindt.
1. Selecteer in de lijst **Beheren** de optie **App-registraties** en selecteer vervolgens de toepassing die u wilt configureren. De pagina **Instellingen** wordt weergegeven met informatie over de configuratie.
1. Controleer of de client-id van de toepassing overeenkomt met de client-id waarvan u in stap 2 een notitie hebt gemaakt.
1. Selecteer **Verwijderen** op de werkbalk.
1. Selecteer **Ja** in het bevestigingsbericht dat wordt weergegeven.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]