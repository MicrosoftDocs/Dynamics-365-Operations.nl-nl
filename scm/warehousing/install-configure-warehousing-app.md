---
title: Microsoft Dynamics 365 for Operations - Magazijnbeheer installeren en configureren
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 for Operations - Magazijnbeheer installeert en configureert.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bbf6df8d43889e7a62bfe28921997c45c8b4c632
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Operations - Magazijnbeheer installeren en configureren

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 for Operations - Magazijnbeheer installeert en configureert.

Dynamics 365 for Operations - Magazijnbeheer is een toepassing die beschikbaar is via Google Play Store en Windows Store. Voor de huidige versie van Microsoft Dynamics 365 for Operations wordt deze app geleverd als een zelfstandig onderdeel. Dit betekent dat u het zelf moet implementeren op apparaten die worden gebruikt voor magazijntaken. Om de app in uw Dynamics 365 for Operations-omgeving te kunnen gebruiken, moet u de app downloaden op elk apparaat en configureren om verbinding te maken met uw Dynamics 365 for Operations-omgeving. In dit onderwerp wordt beschreven hoe u de app op uw apparaten installeert. Ook wordt uitgelegd hoe u de app configureert om verbinding te maken met uw Dynamics 365 for Operations-omgeving.

## <a name="prerequisites"></a>Vereisten
De app is beschikbaar op Android- en Windows-besturingssystemen. Als u deze toepassing wilt gebruiken, moet u een van de volgende ondersteunde besturingssystemen op uw apparaten hebben geïnstalleerd. Ook moet u een van de volgende ondersteunde versies van Dynamics 365 for Operations hebben. Gebruik de informatie in de volgende tabel om te evalueren of uw hardware- en softwareomgeving voorbereid is voor ondersteuning van de installatie.

| Platform                    | Versie                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (alle versies)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations versie 1611 - of - Microsoft Dynamics Dynamics AX versie 7.0/7.0.1 en Microsoft Dynamics AX-platform update 2 met hotfix KB 3210014 |

## <a name="get-the-app"></a>De app verkrijgen
-   Windows (UWP) - [Dynamics 365 for Operations - Magazijnbeheer via Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Magazijnbeheer via Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Een webservicetoepassing maken in Active Directory
Als u de app wilt laten samenwerken met een specifieke Dynamics 365 for Operations-server, moet u een webservicetoepassing registreren in een Azure Active Directory voor de Dynamics 365 for Operations-tenant. Uit veiligheidsoverwegingen wordt aangeraden dat u een webservicetoepassing maakt voor elk apparaat dat u gebruikt. Als u een webservicetoepassing wilt maken in Azure Active Directory (Azure AD), voert u de volgende stappen uit:

1.  Ga in een webbrowser naar <https://manage.windowsazure.com>.
2.  Voer de naam en het wachtwoord in voor de gebruiker die toegang heeft tot het Azure-abonnement.
3.  Klik in Azure Portal in het linkernavigatievenster op **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Selecteer in het raster het Active Directory-exemplaar dat wordt gebruikt door Dynamics 365 for Operations.
5.  Klik op de bovenste werkbalk op **Toepassingen**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klik in het onderste deelvenster op **Toevoegen**. De wizard **Toepassing toevoegen** wordt gestart.
7.  Voer een naam voor de toepassing in en selecteer **Webtoepassing en/of web-API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Voer de URL voor aanmelding in. Dit is de toepassings-URL in uw tenant, de hoofd-URL van Operations. De URL voor aanmelding wordt momenteel niet actief gebruikt bij het verifiëren van de app, maar het is een verplicht veld. Voer dezelfde URL in het veld App-ID-URI in. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Ga naar het tabblad **Configureren**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Blader omlaag totdat u de sectie **Machtigingen voor andere toepassingen** ziet. Klik op **Toepassing toevoegen**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Selecteer **Microsoft Dynamics ERP** in de lijst. Klik op de knop **Controle voltooien** in de rechterhoek van de pagina. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Schakel in de lijst **Machtigingen delegeren** alle selectievakjes in. Klik op **Opslaan**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Houd rekening met de volgende informatie:
    -   **Client-ID**: als u op de pagina omhoog bladert, ziet u **Client-ID**.
    -   **Sleutel**: maak in de sectie **Sleutels** een sleutel door duur te selecteren, en kopieer de sleutel. Naar deze sleutel wordt later verwezen als **Clientgeheim**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Een gebruikersaccount in Dynamics 365 for Operations maken en configureren
Om ervoor te zorgen dat Dynamics 365 for Operations uw Azure AD-toepassing kan gebruiken, moet u de volgende configuratiestappen uitvoeren:

1.  Maak een nieuwe gebruikersaccount in Azure Active Directory voor de Dynamics 365 for Operations-tenant. Het doel van deze gebruikersaccount is toegang te verkrijgen tot de specifieke aangepaste service van de app Magazijnbeheer die de Dynamics 365 for Operations-server weergeeft. Na het voltooien van deze stap hebt u WMDP-gebruikersreferenties, die bestaan uit een WMDP-e-mailadres en een WMDP-wachtwoord. Voor meer informatie over de basisstappen voor het toevoegen van gebruikers aan Azure AD en Dynamics 365 for Operations, raadpleegt u deze zelfstudie: [Aanmelden voor een Microsoft Dynamics 365 for Operations-abonnement](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Maak een Dynamics 365 for Operations-gebruiker die met de gebruikersreferenties van de app Magazijnbeheer overeenkomt.
    1.  Ga in Dynamics 365 for Operations naar **Systeembeheer** &gt; **Algemeen** &gt; **Gebruikers**.
    2.  Maak een nieuwe gebruiker.
    3.  Wijs de gebruiker van het mobiele apparaat voor Magazijnbeheer toe, zoals in de volgende schermopname wordt weergegeven. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Koppel uw Azure Active Directory-toepassing aan de gebruiker van de app Magazijnbeheer.
    1.  Ga in Dynamics 365 for Operations naar **Systeembeheer** &gt; **Instellen** &gt; **Azure Active Directory-toepassingen**.
    2.  Maak een nieuwe regel.
    3.  Voer de **Client-ID** in (verkregen in het laatste gedeelte), geef deze een naam en selecteer de eerder gemaakte gebruiker. Het is raadzaam al uw apparaten te labelen, zodat u eenvoudig de toegang ervan tot Dynamics 365 for Operations van deze pagina kunt verwijderen voor het geval u ze kwijt raakt. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>De toepassing configureren
U moet de app configureren op het apparaat om verbinding te maken met de Dynamics 365 for Operations-server via de Azure AD-toepassing. Hiervoor moet u de volgende stappen uitvoeren.

1.  Ga in de app naar **Verbindingsinstellingen**.
2.  Schakel het veld **Demomodus** uit. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Voer de volgende informatie in:- **Client-ID Azure Active Directory**: de ID wordt verkregen in stap 13 in "Een webservicetoepassing in Active Directory maken". - **Clientgeheim Azure Active Directory**: het clientgeheim wordt verkregen in stap 13 in "Een webservicetoepassing maken in Active Directory". - **Resource Azure Active Directory**: de recource van Azure AD toont de hoofd-URL van Dynamics 365 for Operations. **Opmerking**: dit veld mag niet met een slash (/) worden afgesloten. - **Tenant Azure Active Directory**: de Azure Active Directory-tenant die wordt gebruikt met de Dynamics 365 for Operations-server: https://login.windows.net/&lt;your-AD-tenant-ID&gt;. Bijvoorbeeld: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Opmerking**: dit veld mag niet met een slash (/) worden afgesloten. - **Bedrijf**: voer de rechtspersoon in Dynamics 365 for Operations in waarmee de toepassing verbinding moet maken. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Selecteer de knop **Terug** in de linkerbovenhoek van de toepassing. De toepassing maakt nu verbinding met uw Dynamics 365 for Operations-server en het aanmeldingsscherm wordt voor de magazijnmedewerker weergegeven. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Toegang voor een apparaat verwijderen
In geval van een verloren of beschadigd apparaat moet u de toegang tot Dynamics 365 for Operations voor het apparaat verwijderen. In de volgende stappen wordt het aanbevolen proces beschreven om toegang uit te schakelen.

1.  Ga in Dynamics 365 for Operations naar **Systeembeheer** &gt; **Instellen** &gt; **Azure Active Directory-toepassingen**.
2.  Verwijder de regel die overeenkomt met het apparaat waarvoor u toegang wilt verwijderen. Noteer de **Client-ID** die wordt gebruikt voor het verwijderde apparaat.
3.  Meld u bij de klassieke Azure-portal aan via <https://manage.windowsazure.com>.
4.  Klik op het pictogram **Active Directory** in het linkermenu en klik vervolgens op de gewenste directory.
5.  Klik in het bovenste menu op **Toepassingen** en klik vervolgens op de toepassing die u wilt configureren. De pagina **Snel starten** wordt weergegeven met informatie over eenmalige aanmelding en andere configuratie-informatie.
6.  Klik op het tabblad **Configureren**, blader omlaag en zorg ervoor dat de **Client-ID** van de toepassing hetzelfde is als in stap 2 in dit gedeelte.
7.  Klik op de knop **Verwijderen** op de opdrachtbalk.
8.  Klik op **Ja** in het bevestigingsbericht.





