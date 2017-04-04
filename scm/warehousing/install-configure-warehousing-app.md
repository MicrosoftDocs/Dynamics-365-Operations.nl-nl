---
title: 'Installeren en configureren van Microsoft Dynamics 365 voor bewerkingen & #8211; Magazijnbeheer'
description: In dit onderwerp wordt beschreven hoe installeren en configureren van Microsoft Dynamics 365 for Operations - magazijnbeheer.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installeren en configureren van Microsoft Dynamics 365 voor bewerkingen & #8211; Magazijnbeheer

In dit onderwerp wordt beschreven hoe installeren en configureren van Microsoft Dynamics 365 for Operations - magazijnbeheer.

Dynamics 365 for Operations - opslag is een toepassing die beschikbaar zijn op Google afspelen winkel en de Windows Store. Voor de huidige versie van Microsoft Dynamics 365 voor bewerkingen, wordt deze toepassing worden geleverd als een zelfstandige onderdelen, wat afdrachten deployment op apparaten die worden gebruikt voor het magazijn taken betekent. Zodat u de app in uw Dynamics 365 voor operationele omgevingen gebruiken, moet u downloaden van een toepassing op elk apparaat en configureer het verbinding maken met uw Dynamics 365 voor operationele omgevingen. In dit onderwerp wordt beschreven hoe de app op uw apparaten installeren. Ook wordt uitgelegd hoe de app verbinding maken met uw Dynamics 365 voor bewerkingen omgeving configureren.

## <a name="prerequisites"></a>Vereisten
De app is beschikbaar op Android en Windows-besturingssystemen. Als u wilt deze toepassing gebruiken, moet u een van de volgende ondersteunde besturingssystemen geïnstalleerd op uw apparaten hebben. Ook moet een van de volgende ondersteunde versies van Dynamics 365 voor bewerkingen. De informatie in de volgende tabel gebruiken om te evalueren of uw hardware en software-omgeving klaar is voor de ondersteuning van de installatie.

| Platform                    | Versie                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows-10 (alle versies)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 voor bewerkingen 1611 - of - Microsoft Dynamics Dynamics AX versie 7.0/7.0.1 en Microsoft Dynamics AX-platform bijwerken 2 met hotfix KB 3210014 |

## <a name="get-the-app"></a>De app ophalen
-   Windows (UWP) - [Dynamics 365 for Operations - magazijnbeheer op de Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - magazijnbeheer in de winkel Google afspelen](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Een service webtoepassing maken in Active Directory
De toepassing om te communiceren met een specifieke Dynamics 365 for Operations server, zodat moet u een webtoepassing service registreren in een Azure Active Directory voor de Dynamics 365 voor pachters bewerkingen. Uit veiligheidsoverwegingen wordt aangeraden dat u maakt een web service-toepassing voor elk apparaat dat u gebruikt. Een service als webtoepassing wilt maken in Azure Active Directory (Azure AD), gaat u als volgt:

1.  Ga in een webbrowser naar <https://manage.windowsazure.com>.
2.  Voer de naam en wachtwoord voor de gebruiker die toegang tot het abonnement Azure heeft.
3.  Klik in Azure Portal in het linkernavigatievenster op **Active Directory**. [](./media/wh-01-active-directory-example.png)[![W-01-actief-directory-voorbeeld](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Selecteer het Active Directory-exemplaar dat wordt gebruikt door Dynamics 365 voor bewerkingen in het raster.
5.  Klik op de bovenste werkbalk **toepassingen**. [![W-02-actief-directory-toepassingen](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klik in het onderste deelvenster op **Add**. De **toepassing toevoegen** wizard wordt gestart.
7.  Voer een naam voor de toepassing en selecteer **webtoepassing en/of web-API**. [![Wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  De URL aanmelding, namelijk de URL van de toepassing in uw pachters, de hoofdmap bewerkingen URL invoeren. De URL voor eenmalige aanmelding wordt momenteel niet actief gebruikt in de toepassing worden geverifieerd, maar is een verplicht veld. Voer de dezelfde URL in het veld App-ID-URI. [![W-04-ad--eigenschappen toevoegen](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Ga naar de **configureren** tabblad. [![W-05-ad-configureren-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Blader omlaag tot u ziet de **machtigingen aan andere toepassingen** sectie. Klik op **toepassing toevoegen**. [![Wh-06-AD-App-Add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Selecteer **Microsoft Dynamics ERP** in de lijst. Klik op de **voltooien** knop in de rechterhoek van de pagina. [![W-07-ad-select-machtigingen](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. In de **machtigingen delegeren**, selecteert u alle selectievakjes uit. Click **Save**. [![W-08-ad--machtigingen delegeren](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Maak een notitie van de volgende informatie:
    -   **Client-ID** - bladeren om de pagina ziet u **Client-ID** weergegeven.
    -   **Sleutel** : In de **sleutels** sectie, een sleutel maken door te selecteren en de sleutel te kopiëren. Deze sleutel wordt later worden hierna aangeduid als de **geheim Client**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Maken en configureren van een gebruikersaccount in Dynamics 365 for Operations
Dynamics 365 for Operations om uw Azure AD-toepassing te gebruiken, zodat moet u de volgende configuratiestappen uitvoeren:

1.  Een nieuwe gebruikersaccount in Azure Active Directory voor de Dynamics 365 voor pachters bewerkingen maken. Het doel van deze gebruikersaccount is toegang tot de specifieke aangepaste service van de magazijnbeheer app waarmee de Dynamics 365 for Operations server. Na het voltooien van deze stap hebt u de gebruikersreferenties WMDP, die bestaan uit een WMDP e-mailadres en wachtwoord WMDP. Voor meer informatie over de basisstappen voor het toevoegen van gebruikers aan Azure AD en Dynamics 365 voor bewerkingen, verwijzen naar deze zelfstudie: [aanmelden voor een Microsoft Dynamics 365 voor bewerkingen abonnement](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Maak een Dynamics 365 voor bewerkingen-gebruiker die met de magazijnbeheer app gebruikersreferenties overeenkomt.
    1.  In Dynamics 365 voor bewerkingen, gaat u naar **Systeembeheer**&gt;**veelgebruikte**&gt;**gebruikers**.
    2.  Maak een nieuwe gebruiker.
    3.  De gebruiker van de mobiele telefoon magazijn toewijzen zoals in de volgende schermopname. [![Wh-09-Add-User-Security-Role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Uw Azure Active Directory-toepassing koppelen aan de magazijnbeheer app-gebruiker.
    1.  In Dynamics 365 voor bewerkingen, gaat u naar **Systeembeheer**&gt;**Setup**&gt;**Azure Active Directory-toepassingen**.
    2.  Maak een nieuwe regel.
    3.  Voer de **Client-ID** (verkregen in de laatste sectie), een naam geven en selecteer de eerder gemaakte gebruiker. Het is raadzaam dat u al uw apparaten labelen, zodat u eenvoudig hun toegang naar Dynamics 365 for Operations vanaf deze pagina verwijderen kunt als ze verloren zijn. [![W-10-ad-toepassingen-formulier](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>De toepassing configureren
U moet de app configureren op het apparaat verbinding maken met de Dynamics 365 for Operations server via de Azure AD-toepassing. U doet dit door de volgende stappen.

1.  Ga in de app naar **verbindingsinstellingen**.
2.  Schakel de **demomodus** veld. [![Wh-11-App-Connection-Settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Voer de volgende informatie:- **Azure Active directory-client-ID** -de ID wordt verkregen in stap 13 in 'Een webtoepassing service in Active Directory maken' client. - **Geheim azure Active directory-client** -het geheim van de client wordt verkregen in stap 13 in 'Een webtoepassing service in Active Directory maken'. - **Azure Active directory-resource** : de bron van de directory Azure AD ziet u de Dynamics 365 voor bewerkingen basis-URL. **opmerking**: dit veld met een slash (/) niet worden afgesloten. - **Azure Active directory pachters** -de huurder Azure AD directory met de Dynamics 365 worden gebruikt voor bewerkingen server: https://login.windows.Net/&lt;uw-AD-pachters-ID&gt;. Bijvoorbeeld: https://login.windows.Net/contosooperations.onmicrosoft.com. 
**opmerking**: dit veld met een slash (/) niet worden afgesloten. - **Bedrijf** -de rechtspersoon in Dynamics 365 voor bewerkingen die u wilt dat de toepassing om verbinding te invoeren. [![W-12-app--verbindingsinstellingen](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Selecteer de **terug** knop in de linkerbovenhoek van de toepassing. De toepassing wordt nu een verbinding met uw Dynamics 365 for Operations server en het aanmeldingsscherm voor de magazijnmedewerker worden weergegeven. [![W-13-aanmeldingsaccount-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Toegang voor een apparaat verwijderen
In geval van een apparaat verloren of beschadigde, moet u de toegang tot Dynamics 365 voor bewerkingen voor het apparaat verwijderen. De volgende stappen beschrijven het aanbevolen proces toegang uitschakelen.

1.  In Dynamics 365 voor bewerkingen, gaat u naar **Systeembeheer**&gt;**Setup**&gt;**Azure Active Directory-toepassingen**.
2.  Verwijder de regel die overeenkomt met het apparaat waarnaar u wilt verwijderen van access. Schrijft u de **Client-ID** gebruikt voor het verwijderde apparaat.
3.  Meld u aan de Azure klassiek portal op <https://manage.windowsazure.com>.
4.  Klik op de **Active Directory** pictogram in het menu links en klik vervolgens op de gewenste map.
5.  Klik in het bovenste menu op **toepassingen**, en klik vervolgens op de toepassing die u wilt configureren. De **werkbalk Snel starten** pagina met eenmalige aanmelding en andere configuratie-informatie wordt weergegeven.
6.  Klik op de **configureren** tabblad, blader naar beneden en ervoor te zorgen dat de **Client-ID** van de sollicitatie is hetzelfde als bij stap 2 in deze sectie.
7.  Klik op de **verwijderen** knop in de werkbalk.
8.  Klik op **Ja** in het bevestigingsbericht.



