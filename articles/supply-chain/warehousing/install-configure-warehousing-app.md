---
title: Microsoft Dynamics 365 for Finance and Operations - Warehousing installeren en configureren
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 for Finance and Operations - Warehousing installeert en configureert.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: 0f83735ec42e945c5e0abf8d72b83936e076e60e
ms.contentlocale: nl-nl
ms.lasthandoff: 02/27/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operations - Warehousing installeren en configureren

[!include[banner](../includes/banner.md)]


> [!NOTE]

> In dit onderwerp wordt beschreven hoe u magazijnbeheer voor cloudimplementaties configureert. Als u wilt weten hoe u magazijnbeheer configureert voor on-premises implementaties, raadpleegt u [Magazijnbeheer voor on-premises implementaties](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 for Finance and Operations - Warehousing installeert en configureert.

Finance and Operations - Warehousing is een app die beschikbaar is via Google Play Store en Windows Store. Voor de huidige versie van Finance and Operations wordt deze app geleverd als een zelfstandig onderdeel. Dit betekent dat u het zelf moet implementeren op apparaten die worden gebruikt voor magazijntaken. Om de app in uw Finance and Operations-omgeving te kunnen gebruiken, moet u de app downloaden op elk apparaat en configureren om verbinding te maken met uw Finance and Operations-omgeving. In dit onderwerp wordt beschreven hoe u de app op uw apparaten installeert. Ook wordt uitgelegd hoe u de app configureert om verbinding te maken met uw Finance and Operations-omgeving.

## <a name="prerequisites"></a>Vereisten
De app is beschikbaar op Android- en Windows-besturingssystemen. Als u deze toepassing wilt gebruiken, moet u een van de volgende ondersteunde besturingssystemen op uw apparaten hebben geïnstalleerd. Ook moet u een van de volgende ondersteunde versies van Finance and Operations hebben. Gebruik de informatie in de volgende tabel om te evalueren of uw hardware- en softwareomgeving voorbereid is voor ondersteuning van de installatie.

| Platform                    | Versie                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (alle versies)                                                                                                                                                   |
| Finance en Operations | Microsoft Dynamics 365 for Operations, versie 1611 <br>– of – <br>Microsoft Dynamics AX, versie 7.0/7.0.1 en Microsoft Dynamics AX-platform, update 2 met hotfix KB 3210014 |

## <a name="get-the-app"></a>De app verkrijgen
-   Windows (UWP)
     - [Finance and Operations - Warehousing via Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Warehousing in de Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Warehousing in de Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Een webservicetoepassing maken in Azure Active Directory
Als u de app wilt laten samenwerken met een specifieke Finance and Operations-server, moet u een webservicetoepassing registreren in een Azure Active Directory voor de Finance and Operations-tenant. Uit veiligheidsoverwegingen wordt aangeraden dat u een webservicetoepassing maakt voor elk apparaat dat u gebruikt. Als u een webservicetoepassing wilt maken in Azure Active Directory (Azure AD), voert u de volgende stappen uit:

1.  Ga in een webbrowser naar <https://portal.azure.com>.
2.  Voer de naam en het wachtwoord in voor de gebruiker die toegang heeft tot het Azure-abonnement.
3.  Klik in Azure Portal in het linkernavigatievenster op **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Zorg dat het Active Directory-exemplaar het exemplaar is dat wordt gebruikt door Finance and Operations.
5.  Klik in de lijst op **App-registraties**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Klik in het bovenste deelvenster op **Nieuwe toepassingsregistratie**. De wizard **Toepassing toevoegen** wordt gestart.
7.  Voer een naam voor de toepassing in en selecteer **Webtoepassing/web-API**. Voer de aanmeldings-URL in. Dit is de URL van uw web-app. Deze URL is dezelfde als de URL van uw implementatie, maar dan met 'ouath' achteraan toegevoegd. Klik op **Maken**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Selecteer de app in de lijst. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Vergeet de **toepassings-id** niet. U hebt deze later nodig. De **toepassings-id** wordt hierna aangeduid als de **client-id**.
10. Klik op **Sleutels** in het **deelvenster Instellingen**. Maak een sleutel door een sleutelomschrijving en een duur in te voeren in het gedeelte **Wachtwoorden**. 
11. Klik op **Opslaan** en kopieer de sleutel. Naar deze sleutel wordt later verwezen als **Clientgeheim**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Een gebruikersaccount in Finance and Operations maken en configureren
Om ervoor te zorgen dat Finance and Operations uw Azure AD-toepassing kan gebruiken, moet u de volgende configuratiestappen uitvoeren:

1.  Maak een nieuwe gebruikersaccount in Azure Active Directory voor de Finance and Operations-tenant. Het doel van deze gebruikersaccount is toegang te verkrijgen tot de specifieke aangepaste service van de app Warehousing, die de Finance and Operations-server weergeeft. Na het voltooien van deze stap hebt u WMDP-gebruikersreferenties, die bestaan uit een WMDP-e-mailadres en een WMDP-wachtwoord. Voor meer informatie over de basisstappen voor het toevoegen van gebruikers aan Azure AD en Finance and Operations, raadpleegt u deze zelfstudie: [Aanmelden voor een Finance and Operations-abonnement](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Maak een Finance and Operations-gebruiker die met de gebruikersreferenties van de app Warehousing overeenkomt.
    1.  Ga in Finance and Operations naar **Systeembeheer** &gt; **Algemeen** &gt; **Gebruikers**.
    2.  Maak een nieuwe gebruiker.
    3.  Wijs de gebruiker van het mobiele apparaat voor Magazijnbeheer toe, zoals in de volgende schermopname wordt weergegeven. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Koppel uw Azure Active Directory-toepassing aan de gebruiker van de app Magazijnbeheer.
    1.  Ga in Finance and Operations naar **Systeembeheer** &gt; **Instellen** &gt; **Azure Active Directory-toepassingen**.
    2.  Maak een nieuwe regel.
    3.  Voer de **Client-ID** in (verkregen in het laatste gedeelte), geef deze een naam en selecteer de eerder gemaakte gebruiker. Het is raadzaam al uw apparaten te labelen, zodat u eenvoudig de toegang ervan tot Finance and Operations van deze pagina kunt verwijderen voor het geval u ze kwijt raakt. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>De toepassing configureren
U moet de app configureren op het apparaat om verbinding te maken met de Finance and Operations-server via de Azure AD-toepassing. Hiervoor moet u de volgende stappen uitvoeren.

1.  Ga in de app naar **Verbindingsinstellingen**.
2.  Schakel het veld **Demomodus** uit. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Voer de volgende gegevens in: 
    + **Client-id Azure Active Directory**: De client-id wordt verkregen in stap 9 in "Een webservicetoepassing maken in Active Directory". 
    + **Clientgeheim Azure Active Directory**: Het clientgeheim wordt verkregen in stap 11 in "Een webservicetoepassing maken in Active Directory". 
    + **Resource Azure Active Directory**: De resource van Azure AD toont de hoofd-URL van Finance and Operations. **Opmerking**: dit veld mag niet met een slash (/) worden afgesloten. 
    + **Tenant Azure Active Directory**: de Azure AD-tenant die wordt gebruikt met de Finance and Operations-server: `https://login.windows.net/your-AD-tenant-ID`. Bijvoorbeeld: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Opmerking**: dit veld mag niet met een slash (/) worden afgesloten. 
    + **Bedrijf**: Voer de rechtspersoon in Finance and Operations in waarmee de toepassing verbinding moet maken. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Selecteer de knop **Terug** in de linkerbovenhoek van de toepassing. De toepassing maakt nu verbinding met uw Finance and Operations-server en het aanmeldingsscherm wordt voor de magazijnmedewerker weergegeven. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Toegang voor een apparaat verwijderen
In geval van een verloren of beschadigd apparaat moet u de toegang tot Finance and Operations voor het apparaat verwijderen. In de volgende stappen wordt het aanbevolen proces beschreven om toegang uit te schakelen.

1.  Ga in Finance and Operations naar **Systeembeheer** &gt; **Instellen** &gt; **Azure Active Directory-toepassingen**.
2.  Verwijder de regel die overeenkomt met het apparaat waarvoor u toegang wilt verwijderen. Vergeet de **client-id** niet die wordt gebruikt voor het verwijderde apparaat. U hebt deze later nodig.
3.  Meld u aan bij de Azure-portal op <https://portal.azure.com>.
4.  Klik op het pictogram **Active Directory** in het linkermenu en zorg dat u zich in de juiste map bevindt.
5.  Klik in de lijst op **App-registraties** en klik vervolgens op de toepassing die u wilt configureren. De pagina **Instellingen** wordt weergegeven met informatie over de configuratie.
6.  Zorg ervoor dat de **client-id** van de toepassing hetzelfde is als bij stap 2 in deze sectie.
7.  Klik op de knop **Verwijderen** in het bovenste deelvenster.
8.  Klik op **Ja** in het bevestigingsbericht.

