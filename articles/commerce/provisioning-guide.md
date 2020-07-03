---
title: Een preview-omgeving inrichten voor Dynamics 365 Commerce
description: In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426460"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Een preview-omgeving inrichten voor Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een preview-omgeving voor Dynamics 365 Commerce inricht.

Voordat u begint, kunt u het beste dit onderwerp snel doorlezen om een idee te krijgen van wat nodig is voor het proces.

> [!NOTE]
> Als u nog geen toegang hebt gekregen tot de preview van Dynamics 365 Commerce, kunt u toegang tot de preview-versie aanvragen via de [website van Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Overzicht

Als u uw preview-omgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype. De omgeving en Commerce Scale Unit (CSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later inricht. De instructies in dit onderwerp beschrijven alle vereiste stappen voor het voltooien van de inrichting en de parameters die u moet gebruiken.

Nadat de inrichting van de preview-omgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden. Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren. U kunt de optionele stappen altijd later voltooien.

Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw preview-omgeving voor Commerce configureert nadat u deze hebt ingericht. Zie [Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw preview-omgeving van Commerce configureert.

Als u vragen hebt over de inrichtingsstappen of als u problemen ondervindt, laat het Microsoft dan weten in de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Vereisten

Aan de volgende voorwaarden moeten zijn voldaan voordat u uw preview-omgeving van Commerce inricht:

- U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).
- U bent een bestaande Microsoft Dynamics 365-partner of -klant en kunt een Dynamics 365 Commerce-project maken.
- U bent geaccepteerd voor het Dynamics 365 Commerce Preview-programma.
- U hebt de vereiste machtigingen om een project te maken voor **Migreren, oplossingen maken en informatie over**.
- U bent lid van de rol **Omgevingsbeheerder** of **Projecteigenaar** in het project waar u de omgeving gaat inrichten.
- U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of contact met een abonnementsbeheerder die de twee stappen kan uitvoeren waarvoor beheerdersmachtigingen namens u nodig zijn.
- U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand. (Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)

## <a name="provision-your-commerce-preview-environment"></a>Uw preview-omgeving van Commerce inrichten

In deze procedures wordt uitgelegd hoe u een preview-omgeving van Commerce inricht. Als u dit hebt gedaan, is de preview-omgeving van Commerce gereed voor configuratie. Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.

> [!IMPORTANT]
> Preview-toegang is gekoppeld aan de LCS-account en organisatie die u hebt opgegeven in uw Commerce preview-toepassing. U moet dezelfde account gebruiken om de preview-omgeving van Commerce in te richten. Als u een andere LCS-account of tenant voor de preview-omgeving van Commerce moet gebruiken, moet u deze gegevens aan Microsoft verstrekken. Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) verderop in dit onderwerp voor contactgegevens.

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
> Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen. Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce - Demo (10.0.* x* met Platform update *xx*)** direct boven het veld **Omgevingsnaam** ziet. Zie de afbeelding die na stap 8 wordt weergegeven voor nadere details.

1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer **Toevoegen** om een omgeving toe te voegen.
1. Selecteer in het veld **Toepassingsversie** de meest recente versie. Als u specifiek een andere toepassingsversie dan de meest recente versie wilt selecteren, moet u geen eerdere versie dan **10.0.8** selecteren.
1. Gebruik in het veld **Platformversie** de platform versie die automatisch wordt gekozen voor de toepassingsversie die u hebt geselecteerd. 

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. Selecteer **Volgende**.
1. Selecteer **Demo** als de omgevingstopologie.

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. Selecteer **Dynamics 365 Commerce - Demo** als de omgevingstopologie. Als u één Azure-connector eerder hebt geconfigureerd, wordt deze gebruikt voor deze omgeving. Als u meerdere Azure-connectors hebt geconfigureerd, kunt u kiezen welke connector u wilt gebruiken: **VS - oost**, **VS - oost 2**, **VS - west**, **VS - west 2**. (Voor de beste end-to-end-prestaties raden we aan **VS - west 2** te selecteren.)

    ![De omgevingstopologie 2 selecteren](./media/project3.png)

1. Voer op de pagina **Omgeving implementeren** een omgevingsnaam in. Laat geavanceerde instellingen ongewijzigd.

    ![De pagina Omgeving implementeren](./media/project4.png)

1. Pas de VM-grootte naar wens aan. (We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)
1. Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.
1. Selecteer **Volgende**.
1. Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**. U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.

    Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd. Het duurt even voordat de werkstromen van de omgeving zijn voltooid. Controleer dit daarom na ongeveer zes tot negen uur.

1. Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit initialiseren (cloud)

Ga als volgt te werk om CSU te initialiseren.

1. Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsweergave rechts. De weergave met omgevingsdetails wordt weergegeven.
1. Selecteer **Beheren** onder **Omgevingsfuncties**.
1. Selecteer **Initialiseren** op het tabblad **Commerce**. De weergave CSU-initialisatieparameters wordt weergegeven.
1. Kies voor **Regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.
1. Selecteer in het veld **Versie** de optie **Een versie opgeven** in de lijst en geef **9.18.20014.4** op in het veld dat wordt weergegeven. Geef de exacte versie op die hier wordt aangegeven. Anders moet u RCSU later bijwerken naar de juiste versie.
1. Schakel de optie **Extensie toepassen** in.
1. Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met extensies.
1. Selecteer **Initialiseren**.
1. Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**. De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **Commerce** is geselecteerd. Uw CSU is in de wachtrij geplaatst voor inrichting.
1. Voordat u verdergaat, moet u controleren of de CSU-status **Gelukt** is. Initialisatie duurt ongeveer twee tot vijf uur.

### <a name="initialize-e-commerce"></a>e-Commerce initialiseren

Ga als volgt te werk om e-Commerce te initialiseren.

1. Controleer op het tabblad **e-Commerce** de toestemming voor de preview en selecteer vervolgens **Instellen**.
1. Voer een naam in bij **Tenantnaam e-Commerce**. Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.
1. Selecteer in het veld **Naam Commerce Scale Unit** uw CSU in de lijst. (De lijst moet slechts één optie hebben.)

    Het veld **Geografie van e-Commerce** wordt automatisch ingevuld en kan niet worden gewijzigd.

1. Selecteer **Volgende** om door te gaan.
1. Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.
1.  Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken. Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven. Selecteer de juiste beveiligingsgroep in de lijst.
2.  Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken. Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven. Selecteer de juiste beveiligingsgroep in de lijst.
1. Laat **Service voor beoordelingen en recensies inschakelen** ingeschakeld.
1. Selecteer **Initialiseren**. De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **e-Commerce** is geselecteerd. De initialisatie van e-Commerce is gestart.
1. Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.
1. Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:

    * **e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.
    * **Beheerhulpprogramma van de e-Commerce-site**: de koppeling naar het beheerhulpprogramma van de site.

## <a name="commerce-preview-environment-support"></a>Ondersteuning voor preview-omgeving van Commerce

Als u problemen ondervindt tijdens het uitvoeren van de inrichting, gaat u naar de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer) voor hulp.

## <a name="next-steps"></a>Volgende stappen

Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw preview-omgeving voor Commerce.

## <a name="additional-resources"></a>Aanvullende resources

[Omgevingsoverzicht Dynamics 365 Commerce-preview](cpe-overview.md)

[Een Dynamics 365 Commerce-preview-omgeving configureren](cpe-post-provisioning.md)

[Optionele functies voor een Dynamics 365 Commerce-preview-omgeving configureren](cpe-optional-features.md)

[Veelgestelde vragen over Dynamics 365 Commerce-preview-omgeving](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (cloud)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)

