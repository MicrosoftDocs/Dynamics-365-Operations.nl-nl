---
title: Een preview-omgeving van Commerce inrichten
description: In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934743"
---
# <a name="provision-a-commerce-preview-environment"></a>Een preview-omgeving van Commerce inrichten

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce inricht.

Voordat u begint, is het raadzaam om dit hele onderwerp door te nemen om een idee te krijgen van wat het proces inhoudt en wat dit onderwerp bevat.

> [!NOTE]
> Als u nog geen toegang hebt gekregen tot de preview van Dynamics 365 Commerce, kunt u toegang tot de preview-versie aanvragen via de [website van Commerce](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Overzicht

Als u uw preview-omgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype. De omgeving en Retail Cloud Scale Unit (RCSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later inricht. De instructies in dit onderwerp beschrijven alle vereiste stappen die u moet voltooien en de parameters die u moet gebruiken.

Nadat de inrichting van de preview-omgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden. Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren. U kunt de optionele stappen altijd later voltooien.

Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw preview-omgeving voor Commerce configureert nadat u deze hebt ingericht. Zie [Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw preview-omgeving van Commerce configureert.

Als u vragen hebt over de inrichtingsstappen of als u problemen ondervindt, laat het Microsoft dan weten in de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Vereisten

Aan de volgende voorwaarden moeten zijn voldaan voordat u uw preview-omgeving van Commerce inricht:

- U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).
- U bent geaccepteerd voor het Dynamics 365 Commerce Preview-programma.
- U hebt de vereiste machtigingen om een project te maken voor **Potentiële presales** uitverkoop of **Migreren, oplossingen maken en informatie over**.
- U bent lid van de rol **Omgevingsbeheerder** of **Projecteigenaar** in het project waar u de omgeving gaat inrichten.
- U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of contact met een abonnementsbeheerder die de twee stappen kan uitvoeren waarvoor beheerdersmachtigingen namens u nodig zijn.
- U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand. (Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)

### <a name="find-your-azure-ad-tenant-id"></a>Uw Azure AD-tenant-id zoeken

Uw Azure AD-tenant-id is een globale unieke id (GUID) met een indeling zoals **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Uw Azure AD-tenant-id zoeken via de Azure-portal

1. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
1. Controleer of u de juiste map hebt geselecteerd.
1. Selecteer **Azure Active Directory** in het linkermenu.
1. Selecteer **Eigenschappen** onder **Beheren**. Uw Azure AD-tenant-id wordt weergegeven onder **Directory-id**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Uw Azure AD-tenant-id zoeken in metagegevens van OpenID Connect

Maak een OpenID-URL door **\{UW\_DOMEIN\}** te vervangen door uw domein, bijvoorbeeld `microsoft.com`. `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` wordt bijvoorbeeld `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Ga naar de OpenID-URL die uw domein bevat.

    U vindt uw Azure AD-tenant-id in meerdere eigenschapswaarden.

1. Ga naar **authorization\_endpoint** en extraheer de GUID direct na `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>De id van uw Azure AD-beveiligingsgroep zoeken

De id van uw Azure AD-beveiligingsgroep is een GUID met een indeling als **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Bij deze procedure wordt ervan uitgegaan dat u lid bent van de groep waarvoor u de id probeert te vinden.

1. Open de [grafiekverkenner](https://developer.microsoft.com/graph/graph-explorer#).
1. Selecteer **Aanmelden bij Microsoft** en meld u aan met uw referenties.
1. Selecteer **Meer voorbeelden weergeven** links.
1. Schakel **Groepen** in het rechterdeelvenster in.
1. Sluit het rechterdeelvenster.
1. Selecteer **Alle groepen waartoe ik behoor**.
1. Zoek uw groep in het veld **Voorbeeld van antwoord**. De beveiligingsgroep-id wordt weergegeven onder de eigenschap **id**.

## <a name="provision-your-commerce-preview-environment"></a>Uw preview-omgeving van Commerce inrichten

In deze procedures wordt uitgelegd hoe u een preview-omgeving van Commerce inricht. Als u dit hebt gedaan, is de preview-omgeving van Commerce gereed voor configuratie. Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.

> [!IMPORTANT]
> Preview-toegang is gekoppeld aan de LCS-account en organisatie die u hebt opgegeven in uw preview-toepassing. U moet dezelfde account gebruiken om de preview-omgeving van Commerce in te richten. Als u een andere LCS-account of tenant voor de preview-omgeving van Commerce moet gebruiken, moet u deze gegevens aan Microsoft verstrekken. Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) verderop in dit onderwerp voor contactgegevens.

### <a name="grant-access-to-e-commerce-applications"></a>Toegang verlenen tot e-Commerce-toepassingen

> [!IMPORTANT]
> De persoon die zich aanmeldt, moet een Azure AD-tenantbeheerder met de Azure AD-tenant-id zijn. Als u deze stap niet kunt voltooien, mislukken de resterende inrichtingsstappen ook.

Ga als volgt te werk om e-Commerce-toepassingen te autoriseren voor toegang tot uw Azure-abonnement.

1. Stel een URL in de volgende indeling samen:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Kopieer en plak de URL in uw browser of teksteditor en vervang **\{AAD\_TENANT\_ID\}** door uw Azure AD-tenant-id. Open de URL.
1. Meld u aan in het dialoogvenster voor aanmelding bij Azure AD en bevestig dat u **Dynamics 365 Commerce (preview)** toegang wilt verlenen tot uw abonnement. U wordt omgeleid naar een pagina waarop wordt aangegeven of de bewerking is geslaagd.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Controleren of de preview-functies beschikbaar zijn en zijn ingeschakeld in LCS

Ga als volgt te werk om te controleren of de preview-functies beschikbaar zijn en zijn ingeschakeld in LCS.

1. Meld u aan bij de [LCS-portal](https://lcs.dynamics.com) met dezelfde LCS-account die u hebt gebruikt om toegang tot de preview aan te vragen.
1. Schuif op de LCS-startpagina helemaal naar rechts en selecteer de tegel **Beheer van voorbeeldfuncties**.

    ![Tegel Beheer van voorbeeldfuncties](./media/preview1.png)

1. Schuif omlaag naar **Particuliere voorbeeldfuncties** en controleer of de volgende functies beschikbaar en ingeschakeld zijn:

    - Evaluatie van e-Commerce
    - Programma-omgevingen voor Commerce Preview

    ![Particuliere voorbeeldfuncties](./media/preview2.png)

1. Als deze functies niet worden weergegeven in de lijst, neemt u contact op met Microsoft en geef u uw zakelijke e-mailadres, LCS-account en tenantgegevens op. Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) voor contactgegevens.

### <a name="create-a-new-project"></a>Een nieuw project maken

Ga als volgt te werk om een nieuw project te maken in LCS.

1. Selecteer op de LCS-startpagina het plusteken (**+**) om een project te maken.
1. Volg een van de volgende stappen uit in het rechterdeelvenster:

    - Als u een partner bent, selecteert u **Migreren, oplossingen maken en informatie over**.
    - Als u een klant bent, selecteert u **Potentiële presales**.

1. Voer een naam, beschrijving en branche in.
1. Selecteer **Dynamics 365 Retail** in het veld **Productnaam**.
1. Selecteer **Dynamics 365 Retail** in het veld **Productversie**.
1. Selecteer **Implementatiemethodologie voor Dynamics Retail** in het veld **Methodologie**.
1. Optioneel: u kunt rollen en gebruikers importeren uit bestaand project.
1. Selecteer **Maken**. De projectweergave wordt weergegeven.

### <a name="add-the-azure-connector"></a>De Azure-connector toevoegen

Ga als volgt te werk om de Azure-connector toe te voegen aan uw LCS-project.

1. Volg één van deze stappen:

    - Als u een partner bent, selecteert u de tegel **Projectinstellingen** uiterst rechts.
    - Als u een klant bent, selecteert u **Projectinstellingen** in het bovenste menu.

1. Selecteer **Azure-connectors**.
1. Selecteer **Toevoegen** om de Azure-connector toe te voegen.
1. Voer een naam in.
1. Voer uw Azure-abonnements-id in.
1. Schakel de optie **Configureren om Azure Resource Manager (ARM) te gebruiken** in.
1. Controleer of de waarde **Azure-abonnement AAD-tenantdomein (of id)** juist is. Neem zo nodig contact op met uw Azure-abonnementsbeheerder.
1. Selecteer **Volgende**.
1. Volg de instructies op de pagina om de vereiste toepassingen toegang te verlenen tot uw abonnement. Neem zo nodig contact op met uw Azure-abonnementsbeheerder.

    1. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
    1. Zorg ervoor dat de juiste map is geselecteerd en selecteer vervolgens in het menu aan de linkerkant **Abonnementen**.
    1. Zoek het juiste abonnement in de lijst en selecteer dit. Gebruik de zoekfunctie zoals vereist.
    1. Selecteer **Toegangscontrole (IAM)** in het menu.
    1. Selecteer **Toevoegen** rechts onder **Een roltoewijzing toevoegen**. Het deelvenster **Roltoewijzing toevoegen** wordt geopend.
    1. Selecteer in het veld **Rol** de waarde **Bijdrager**.
    1. Laat in het veld **Toegang toewijzen aan** de standaardwaarde **Azure AD-gebruiker, -groep of serviceprincipal** ingeschakeld.
    1. Klik onder **Selecteren** op **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Selecteer **Dynamics Deployment Services \[wsfed-enabled\]** in de lijst.
    1. Selecteer **Opslaan**.

1. Selecteer **Volgende**.
1. Volg de instructies op de pagina om de vereiste toepassingen toegang te verlenen tot uw abonnement. Neem zo nodig contact op met uw Azure-abonnementsbeheerder.
1. Selecteer **Volgende**.
1. Kies voor **Azure-regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.
1. Selecteer **Verbinding maken**. De Azure-connector wordt weergegeven in de lijst.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Extensie voor demobasis van Commerce-preview importeren

Voer de volgende stappen uit om de extensie voor de demobasis van de Commerce-preview in uw project te importeren.

1. Open de startpagina voor uw project door de projectnaam bovenaan te selecteren.
1. Volg één van deze stappen:

    - Als u een partner bent, selecteert u de tegel **Activabibliotheek** uiterst rechts.
    - Als u een klant bent, selecteert u **Activabibliotheek** in het bovenste menu.

1. Selecteer **Implementeerbaar softwarepakket** in de lijst aan de linkerkant.
1. Selecteer **Importeren**.
1. Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met activa onder **Bibliotheek voor gedeelde activa**.
1. Selecteer **Verzamelen**. U keert terug naar de activabibliotheek en de extensie wordt weergegeven in de lijst.

In de volgende afbeelding ziet u de acties die moeten worden ondernomen op de LCS-pagina **Activabibliotheek**.

![De extensie voor de demobasis van de Commerce-preview importeren](./media/import.png)

### <a name="deploy-the-environment"></a>De omgeving implementeren

Ga als volgt te werk om de omgeving te implementeren.

> [!NOTE]
> Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen. Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce (Preview) - Demo (10.0.6 met Platform update 30)** direct boven het veld **Omgevingsnaam** ziet. Zie de afbeelding die na stap 8 wordt weergegeven.

1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer **Toevoegen** om een omgeving toe te voegen.
1. Selecteer **10.0.6** in het veld **Toepassingsversie**.
1. Selecteer bij **Platformversie** de optie **Platformupdate 30**.

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. Selecteer **Volgende**.
1. Selecteer **Demo** als de omgevingstopologie.

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. Selecteer **Dynamics 365 Commerce (Preview) - Demo** als de omgevingstopologie. Als u één Azure-connector eerder hebt geconfigureerd, wordt deze gebruikt voor deze omgeving. Als u meerdere Azure-connectors hebt geconfigureerd, kunt u kiezen welke connector u wilt gebruiken: **VS - oost**, **VS - oost 2**, **VS - west**, **VS - west 2**. (Voor de beste end-to-end-prestaties raden we aan **VS - west 2** te selecteren.)

    ![De omgevingstopologie 2 selecteren](./media/project3.png)

1. Voer op de pagina **Omgeving implementeren** een omgevingsnaam in. Laat geavanceerde instellingen ongewijzigd.

    ![De pagina Omgeving implementeren](./media/project4.png)

1. Pas de VM-grootte naar wens aan. (We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)
1. Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.
1. Selecteer **Volgende**.
1. Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**. U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.

    Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd. Het duurt even voordat de werkstromen van de omgeving zijn voltooid. Controleer dit daarom na ongeveer zes tot negen uur.

1. Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.

### <a name="initialize-rcsu"></a>RCSU initialiseren

Ga als volgt te werk om RCSU te initialiseren.

1. Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsweergave rechts. De weergave met omgevingsdetails wordt weergegeven.
1. Selecteer **Beheren** onder **Omgevingsfuncties**.
1. Selecteer **Initialiseren** op het tabblad **Retail**. De weergave RCSU-initialisatieparameters wordt weergegeven.
1. Kies voor **Regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.
1. Selecteer in het veld **Versie** de optie **Een versie opgeven** in de lijst en geef **9.16.19262.5** op in het veld dat wordt weergegeven. Geef de exacte versie op die hier wordt aangegeven. Anders moet u RCSU later bijwerken naar de juiste versie.
1. Schakel de optie **Extensie toepassen** in.
1. Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met extensies.
1. Selecteer **Initialiseren**.
1. Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**. U keert terug naar de weergave **Beheer detailhandel** waar het tabblad **Detailhandel** is geselecteerd. Uw RCSU is in de wachtrij geplaatst voor inrichting.
1. Voordat u verdergaat, moet u controleren of de RCSU-status **Gelukt** is. Initialisatie duurt ongeveer twee tot vijf uur.

### <a name="initialize-e-commerce"></a>e-Commerce initialiseren

Ga als volgt te werk om e-Commerce te initialiseren.

1. Controleer op het tabblad **e-Commerce (preview)** de toestemming voor de preview en selecteer vervolgens **Instellen**.
1. Voer een naam in bij **Tenantnaam e-Commerce**. Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.
1. Selecteer uw RCSU in de lijst in het veld **Naam Retail Cloud Scale Unit**. (De lijst moet slechts één optie hebben.)

    Het veld **Geografie van e-Commerce** wordt automatisch ingevuld en kan niet worden gewijzigd.

1. Selecteer **Volgende** om door te gaan.
1. Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.
1.  Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken. Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven. Selecteer een beveiligingsgroep in de lijst.
2.  Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken. Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven. Selecteer een beveiligingsgroep in de lijst.
1. Laat **Service voor beoordelingen en recensies inschakelen** ingeschakeld.
1. Als u de stap voor toestemming van Microsoft Azure Active Directory (Azure AD) zoals beschreven in de sectie Toegang verlenen tot e-Commerce-toepassingen al hebt voltooid, schakelt u het selectievakje in om uw toestemming te bevestigen. Als u deze stap nog niet hebt voltooid, moet u dat doen voordat u verdergaat met de initialisatie. Selecteer de koppeling in de tekst naast het selectievakje om het dialoogvenster voor toestemming te openen en de stap te voltooien.
1. Selecteer **Initialiseren**. U keert terug naar de weergave **Beheer detailhandel** waarin het tabblad **e-Commerce (Preview)** is geselecteerd. De initialisatie van e-Commerce is gestart.
1. Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.
1. Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:

    * **e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.
    * **Beheerhulpprogramma van de e-Commerce-site**: de koppeling naar het beheerhulpprogramma van de site.

## <a name="commerce-preview-environment-support"></a>Ondersteuning voor preview-omgeving van Commerce

Als u problemen ondervindt tijdens het uitvoeren van de inrichting, gaat u naar de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer) voor hulp.

Als u problemen ondervindt wanneer u probeert toegang te krijgen tot de Yammer-groep, kunt u per e-mail contact opnemen met Microsoft via <Dynamics365Commerce@microsoft.com>. Dit e-mailadres wordt niet actief gecontroleerd. Verwacht daarom een vertraging in het antwoord.

## <a name="next-steps"></a>Volgende stappen

Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw preview-omgeving voor Commerce.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Commerce preview-omgeving](cpe-overview.md)

[Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md)

[Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md)

[Veelgestelde vragen over de preview-omgeving van Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)

[Help-bronnen voor Dynamics 365 Retail](../retail/index.md)
