---
title: Een e-commerce-evaluatieomgeving configureren
description: Deze handleiding bevat stapsgewijze instructies voor het inrichten en configureren van uw Microsoft Dynamics 365 Commerce Preview-omgeving.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771675"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Een e-commerce-evaluatieomgeving configureren

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Deze handleiding bevat stapsgewijze instructies voor het inrichten en configureren van uw Microsoft Dynamics 365 Commerce Preview-omgeving. Voordat u begint, is het raadzaam om de documentatie door te nemen om een idee te krijgen van wat het proces inhoudt en wat de handleiding bevat.

*Opmerking: als u nog geen toegang hebt gekregen tot Microsoft Dynamics 365 Commerce Preview, kunt u toegang tot de preview-versie aanvragen via de [website van Commerce](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Overzicht
Om de omgeving correct te kunnen inrichten moet het project worden gemaakt met een specifieke productnaam en een specifiek type. De omgeving en Retail Cloud Scale Unit beschikken ook over specifieke parameters die u nodig hebt om later te beginnen met het inrichten van e-Commerce. De instructies in deze handleiding bevatten alle vereiste stappen die u moet uitvoeren en parameters die u moet gebruiken.

Nadat de inrichting is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden. Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren. Als u later van gedachte verandert, kunt u de optionele stappen altijd later uitvoeren.

Als u vragen hebt over de inrichtingsstappen of als u problemen ondervindt, laat het ons dan weten op [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Vereisten
De volgende vereisten gelden voor het inrichten van uw Dynamics 365 Preview-omgeving:
* U hebt toegang tot de **Lifecycle Services-portal (LCS).**
* U bent **geaccepteerd in het Dynamics 365 Commerce Preview-programma**
* U hebt de vereiste machtigingen om een project te maken voor **Potentiële presales** uitverkoop of **Migreren, oplossingen maken en informatie over**
* U bent lid van de rol **Omgevingsbeheerder** of **Projecteigenaar** in het project waar u de omgeving gaat inrichten
* U hebt beheerderstoegang tot uw Azure-abonnement of contact met een abonnementsbeheerder die de twee stappen kan uitvoeren waarvoor beheerdersmachtigingen namens u nodig zijn
* U hebt uw **AAD-tenant-id** bij de hand
* U hebt een **AAD-beveiligingsgroep** gemaakt om te gebruiken als **e-Commerce-systeembeheerdersgroep** en u hebt de id bij de hand
* U hebt een **AAD-beveiligingsgroep** gemaakt die u kunt **moderatorgroep voor beoordelingen en revisies** en u hebt de id bij de hand (kan dezelfde beveiligingsgroep zijn als de systeembeheerdersgroep hierboven)
## <a name="provisioning-preview-environment"></a>Preview-omgeving inrichten
Deze instructies hebben betrekking op de inrichting van een Microsoft Dynamics 365 Commerce Preview-omgeving. Nadat u deze stappen hebt voltooid, hebt u een Preview-omgeving die kan worden geconfigureerd. Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-Portal.

*De toegang tot de Preview is gekoppeld aan het LCS-account en de LCS-organisatie die u hebt opgegeven in de Preview-toepassing. U moet hetzelfde account gebruiken voor de inrichting. Als u een ander LCS-account of een andere LCS-tenant moet gebruiken voor de Preview-omgeving, moet u deze gegevens verstrekken. Zie "Aanvullende informatiebronnen" hieronder.*
### <a name="before-starting"></a>Voordat u begint
##### <a name="grant-access-to-e-commerce-applications"></a>Toegang verlenen tot e-Commerce-toepassingen

*Opmerking: **de persoon die zich aanmeldt, moet een AAD-tenantbeheerder zijn**. Als u deze stap niet hebt voltooid, zal de rest van de inrichtingsstappen mislukken.*

1. Voor deze stap hebt u uw **AAD-tenant-id** nodig. U moet toestaan dat de e-Commerce-toepassingen toegang krijgen tot uw Azure-abonnement. De meest eenvoudige manier om dit te bereiken is het assembleren van een URL als hieronder:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Klik niet rechtstreeksop de URL**, kopieer en plak deze in uw browser of teksteditor en vervang **\{AAD_TENANT_ID\}** door uw **AAD-tenant-id** voordat u naar de URL navigeert.
3. U ziet het aanmeldvenster voor Microsoft AAD. Bevestig dat u "Dynamics 365 Commerce (preview)" toegang wilt geven tot uw abonnement.
4. U wordt naar een pagina gestuurd waarin wordt bevestigd of de bewerking is geslaagd.

##### <a name="log-in-to-the-lcs"></a>Aanmelden bij LCS
1. Aanmelden bij LCS-portal: https://lcs.dynamics.com
1. Controleer of u bent aangemeld bij hetzelfde LCS-account als u hebt gebruikt om toegang aan te vragen tot de Preview-versie.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Controleer of de Preview-functies beschikbaar zijn en zijn ingeschakeld
1. Schuif op de voorpagina LCS helemaal naar rechts en klik op de tegel **Beheer van voorbeeldfuncties**.
1. Schuif omlaag naar "PARTICULIERE VOORBEELDFUNCTIES" en controleer of de volgende functies beschikbaar en ingeschakeld zijn:
    1. **Evaluatie van e-Commerce**
    1. **Programma-omgevingen voor Commerce Preview**
1. Als u deze functies niet kunt zien in de lijst, kunt u contact met ons opnemen via uw zakelijke e-mail, LCS-account en tenantgegevens. Zie **Extra informatiebronnen** hieronder voor informatie over hoe u contact met ons kunt opnemen.

![Tegel Beheer van voorbeeldfuncties](./media/preview1.png)

![Voorbeeldfuncties](./media/preview2.png)
### <a name="create-project"></a>Project maken
##### <a name="creating-new-project"></a>Een nieuw project maken
1. Klik op **+** om een nieuw project te maken.
1. Als u een partner bent, kiest u **Migreren, oplossingen maken en informatie over**.
1. Als u een klant bent, kiest u **Potentiële presales**.
1. Voer waar nodig een naam, omschrijving en bedrijfstak in.
1. Selecteer bij **Productnaam** de optie **Dynamics 365 Retail**.
1. Selecteer bij **Productversie** de optie **Dynamics 365 Retail**.
1. Selecteer bij **Methodologie** **Implementatiemethodologie voor Dynamics Retail**.
1. U kunt rollen en gebruikers uit een bestaand project importeren als dat gewenst is.
1. Klik op **Maken**.
1. U gaat naar de projectweergave.
##### <a name="add-azure-connector"></a>Azure-connector toevoegen
1. Als u een partner bent, klikt u op **Projectinstellingen** in de tegels met hulpmiddelen aan de rechterkant.
1. Als u een klant bent, kiest u **Projectinstellingen** in het bovenste menu.
1. Selecteer **Azure-connectors**.
1. Klik op **+Toevoegen** als u een Azure-connector wilt toevoegen.
1. Voer een naam in.
1. Voer uw **Azure-abonnements-id** in.
1. Schakel **Configureren om Azure Resource Manager (ARM) te gebruiken** in.
1. Controleer of **Azure-abonnement AAD-tenantdomein (of id)** juist is. Neem zo nodig contact op met uw Azure-abonnementsbeheerder.
1. Klik op **Volgende**.
1. Volg de instructies op het scherm om de vereiste toepassingen toegang te verlenen tot uw abonnement. Neem zo nodig contact op met uw Azure-abonnementsbeheerder:
    1. Aanmelden bij Azure-portal: https://portal.azure.com/
    1. Controleer of u de juiste namenlijst hebt geselecteerd.
    1. Klik op **Abonnementen** in het menu aan de linkerkant.
    1. Zoek het juiste abonnement in de lijst en selecteer dit. Gebruik zo nodig de zoekfunctie.
    1. Kies **Toegangscontrole (IAM)** in het menu.
    1. Klik op **Toevoegen** onder **Een roltoewijzing toevoegen** aan de rechterkant. Het deelvenster **Roltoewijzing toevoegen** wordt geopend.
    1. Selecteer bij **Rol**de optie **Bijdrager**.
    1. Laat bij **Toegang toewijzen aan** **Azure AD-gebruiker, -groep of serviceprincipal** staan.
    1. Klik onder **Selecteren** op **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Selecteer **Dynamics Deployment Services [wsfed-enabled]** in de lijst.
    1. Klik op **Opslaan**.
1. Klik op **Volgende**.
1. Volg de instructies op het scherm om de vereiste toepassingen toegang te verlenen tot uw abonnement. Neem zo nodig contact op met uw Azure-abonnementsbeheerder.
1. Klik op **Volgende**.
1. Kies voor **Azure-regio** de optie **Oost VS**, **Oost VS 2**, **West VS** of **West US 2**.
1. Klik op **Verbinden**.
1. De Azure-connector wordt weergegeven in de lijst.
### <a name="import-extension"></a>Extensie importeren
1. Ga terug naar de voorpagina van uw project door op de projectnaam bovenaan te klikken.
1. Als u een partner bent, klikt u op **Activabibliotheek** in de tegels met hulpmiddelen aan de rechterkant.
1. Als u een klant bent, kiest u **Activabibliotheek** in het bovenste menu.
1. Selecteer **Implementeerbaar softwarepakket** in de lijst aan de linkerkant.
1. Klik in het actievenster op **IMPORTEREN**.
1. Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met activa onder **GEDEELDE ACTIVABIBLIOTHEEK**.
1. Klik op **Kiezen**.
1. U keert terug naar de activabibliotheek en de extensie wordt weergegeven in de lijst.

![Project maken - versies](./media/import.png)
### <a name="deploy-environment"></a>Omgeving implementeren

*Opmerking: de stappen 6, 7 en/of 8 worden mogelijk niet weergegeven, omdat de schermen met één optie worden overgeslagen. Controleer in de weergave **Omgevingsparameters** of u de tekst "Dynamics 365 Commerce (Preview) - Demo (10.0.6 met Platform update 30)" ziet, direct boven het veld **Omgevingsnaam**. Zie de schermafbeelding hieronder.*

1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Klik op **+ Toevoegen** om een omgeving toe te voegen.
1. Selecteer bij **Applicatieversie** de optie **10.0.6**.
1. Selecteer bij **Platformversie** de optie **Platform update 30**.
1. Klik op **Volgende**.
1. Kies **DEMO** voor omgevingstopologie.
1. Voor omgevingstopologie kiest u **Dynamics 365 Commerce (Preview) - demo**.
1. Als u één Azure-connector eerder hebt geconfigureerd, wordt deze gebruikt voor deze omgeving. Als u meerdere Azure-connectors hebt geconfigureerd, kunt u kiezen welke connector u wilt gebruiken: **Oost-US**, **Oost VS 2**, **West US** of **West US 2** (aanbevolen voor de beste end-to-end prestaties)
1. Voer een **Omgevingsnaam** in.
1. Pas de grootte van de VM naar wens aan. (We adviseren de VM SKU **D13 v2**.)
1. Laat **Geavanceerde instellingen** ongewijzigd.
1. Nadat u de prijzen en licentievoorwaarden op het scherm hebt bekeken, vinkt u het vakje aan om de overeenkomst aan te duiden.
1. Klik op **Volgende**.
1. Klik in het bevestigingsscherm voor de implementatie klikt u op **Implementeren** nadat u hebt gecontroleerd of de details juist zijn.
1. U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.
1. Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens worden geïmplementeerd. Het duurt enige tijd voordat alle omgevingswerkstromen zijn voltooid. Controleer deze na enkele uren (ongeveer 6 – 9 uur).
1. Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.

![Project maken - versies](./media/project1.png)

![Project maken - topologie 1](./media/project2.png)

![Project maken - topologie 2](./media/project3.png)

![Project maken - omgevingsparameters](./media/project4.png)
### <a name="initialize-rcsu"></a>RCSU initialiseren
1. Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.
1. Klik in de omgevingsweergave aan de rechterkant van het scherm op **Volledige details**. In de weergave met omgevingsdetails wordt weergegeven.
1. Klik onder **OMGEVINGSFUNCTIES** op **Beheren**.
1. Klik op het tabblad **Detailhandel** op **initialiseren**. De weergave RCSU-initialisatieparameters wordt weergegeven.
1. Kies voor **REGIO** de optie **Oost VS**, **Oost VS 2**, **West VS** of **West US 2**.
1. Voor **VERSIE** selecteert u eerst **Een versie opgeven** in de vervolgkeuzelijst en geeft u vervolgens **9.16.19262.5** op in het tekstveld dat hieronder wordt weergegeven. *Opmerking: zorg ervoor dat u **de exacte versie** die hier wordt vermeld opgeeft om te voorkomen dat u RCSU later moet bijwerken om de versie te corrigeren.*
1. Schakel **Extensie toepassen** in.
1. Kies in de lijst met extensies de **Extensie voor Commerce Preview-demobasis**.
1. Klik op **Initialiseren**.
1. Klik in het bevestigingsscherm voor de implementatie klikt u op **Ja** nadat u hebt gecontroleerd of de details juist zijn.
1. U keert terug naar de weergave **Beheer detailhandel** terwijl het tabblad **Detailhandel** is geactiveerd. Uw RCSU is in de wachtrij geplaatst voor inrichting.
1. Wacht totdat de RCSU-status **GESLAAGD** is voordat u verdergaat (duurt ongeveer 2-5 uur).
### <a name="initialize-e-commerce"></a>e-Commerce initialiseren
1. Schakel over naar het tabblad **e-Commerce** (Preview).
1. Klik op **Instellen** nadat u hebt ingestemd met de Preview-voorwaarden.
1. Voer een naam in voor **Tenantnaam e-Commerce**. Dit wordt echter wel weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.
1. Voor **Naam Retail Cloud Scale Unit** selecteert u uw RCSU in de lijst (de lijst mag slechts één optie hebben).
1. **Geografie van e-Commerce** wordt automatisch ingevuld en kan niet worden gewijzigd.
1. Klik op **Volgende** om door te gaan.
1. Voer bij **Ondersteunde hostnamen** een geldig domein in (bijvoorbeeld www.fabrikam.com).
1. Voer bij **AAD-beveiligingsgroep voor systeembeheer** de AAD SG-id in die u wilt gebruiken als beheergroep voor het e-Commerce-systeem.
1. Voor **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** voert u de AAD SG-id in die u wilt gebruiken als moderatorgroep voor beoordelingen en recensies.
1. Laat de **B2C**-waarden leeg (7 velden die beginnen met B2C).
1. Laat **Service voor beoordelingen en recensies inschakelen** ingeschakeld.
1. Klik op **Initialiseren**.
1. U keert terug naar de weergave **Beheer detailhandel** terwijl het tabblad **e-Commerce (Preview)** is geactiveerd. Uw e-Commerce-initialisatie is gestart.
1. Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **GEÏNITIALISEERD** is.
1. Onder **KOPPELINGEN** aan de rechterkant.
    * Noteer de koppeling voor de **e-Commerce-site**. Dit is de koppeling naar de hoofdmap van de C2-site.
    * Noteer de koppeling voor het **beheerhulpprogramma van de e-Commerce-site**. Dit is de koppeling naar het hulpprogramma voor sitebeheer (C1-ontwerpgereedschap).
## <a name="post-provisioning-steps"></a>Stappen na inrichting
In deze fase is de omgeving volledig ingericht, maar er zijn nog configuratiestappen die moeten worden uitgevoerd voordat u de omgeving kunt gaan evalueren.
### <a name="before-starting"></a>Voordat u begint
1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsinformatie rechts.
1. Klik op **Aanmelden** om een menu te openen en kies **Aanmelden bij omgeving**.

Zorg ervoor dat de rechtspersoon **USRT** is geselecteerd (rechtsboven).

### <a name="configure-pos"></a>POS configureren
##### <a name="associate-worker-with-your-identity"></a>Werknemer aan uw identiteit koppelen
1. Ga naar het menu links en ga naar **Modules > Detailhandel > Werknemers> Werknemers**.
1. Zoek en selecteer record **000713 - Andrew Collette**.
1. Klik op **Detailhandel** in het actievenster.
1. Klik op **Bestaande identiteit koppelen**.
1. Typ uw e-mailadres in het veld **E-mail** (rechts van **Zoeken met behulp van e-mail**).
1. Klik op **Zoeken**.
1. Selecteer de record met uw naam.
1. Klik op **OK**.
1. Klik op **Opslaan**.
##### <a name="activate-cloud-pos"></a>Cloud POS activeren
1. Meld u aan bij de LCS-portal.
1. Ga naar uw project.
1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsinformatie rechts.
1. Klik op **Aanmelden** om een menu te openen en kies **Aanmelden bij cloud-verkooppunt**, waarna POS wordt geladen.
1. Klik op **Volgende**.
1. Meld u aan om uw AAD-account.
1. Kies onder **Winkelnaam** **San Francisco**.
1. Klik op **Volgende**.
1. Onder **Kassa en apparaat** kiest u **SANFRAN-1**.
1. Klik op **Activeren**.
1. U wordt afgemeld en het POS-aanmeldingsscherm verschijnt.
1. U kunt zich nu aanmelden bij Cloud POS met operator-id **000713** en wachtwoord **123**.
### <a name="site-setup"></a>Instellingen voor site
1. Meld u aan bij het **hulpprogramma voor sitebeheer** met de URL die u eerder hebt genoteerd.
1. Klik op **Fabrikam** om het dialoogvenster met instellingen voor de site te openen.
1. Selecteer bij domein het domein dat u eerder hebt ingevoerd bij het initialiseren van e-Commerce.
1. Selecteer bij standaardkanaal de optie **Uitgebreide Fabrikam online winkel**. *Opmerking: Zorg ervoor dat u de **uitgebreide** online winkel selecteert*
1. Voor de standaardtaal selecteert u **en-us**.
1. Laat het **pad** ongewijzigd.
1. Klik op **OK**.
1. U wordt naar de lijst met pagina's op de site gestuurd.
### <a name="enable-jobs"></a>Taken inschakelen
1. Meld u aan bij de omgeving (HQ).
1. Ga met het menu links naar **Detailhandel > Query's en rapporten > Batchtaken**.
1. Voer de volgende stappen uit voor alle taken in de onderstaande lijst:
    * **E-mailmelding voor detailhandelorder verwerken**.
    * **Beschikbaarheid product**.
    * **P-0001**.
    * **Taak orders synchroniseren**.
1. Gebruik het Snelfilter om de taak te zoeken aan de hand van de naam (hierboven vermeld).
1. Als de status van de taak **Blokkeren** is, voert u de volgende stappen uit:
    1. Selecteer de record.
    1. Open vanuit het actievenster het lint **Batchtaak** en klik op **Status wijzigen**.
    1. Selecteer **Wachten** en klik op **OK**.
### <a name="run-full-data-sync"></a>Volledige gegevenssynchronisatie uitvoeren
1. Ga met het menu links naar **Modules > Detailhandel > Instelling van hoofdkantoor > Detailhandel planner > Kanaaldatabase**.
1. Het **standaard** kanaal wordt geselecteerd in de lijst aan de linkerkant. *Selecteer het andere beschikbare kanaal (met de naam **scXXXXXXXXX**)*.
1. Klik op **Volledige gegevenssynchronisatie** in het actievenster.
1. Voer **9999** in als de distributieplanning.
1. Klik op **OK**.
1. Klik op **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Nadat u deze stappen hebt uitgevoerd kunt u de voorbeeldomgeving evalueren!
Gebruik de URL van het **beheerhulpprogramma van de e-Commerce-site** om naar het C1-ontwerpgereedschap te navigeren en de URL van de **e-Commerce-site** om naar de C2-site te navigeren.

## <a name="additional-resources"></a>Aanvullende resources
### <a name="how-to-find-your-aad-tenant-id"></a>De AAD-tenant-id zoeken
De AAD-tenant-id is een GUID en ziet er als volgt uit: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Vanuit Azure-portal
1. Aanmelden bij Azure-portal: https://portal.azure.com/
1. Controleer of u de juiste namenlijst hebt geselecteerd.
1. Klik op **Azure Active Directory** in het menu aan de linkerkant.
1. Kies **Eigenschappen** onder **Beheren**.
1. AAD-tenant-id wordt weergegevenonder **Directory-id**.
##### <a name="from-openid-connect-metadata"></a>Vanuit metagegevens van OpenID Connect
Maak **OpenID-URL** door **\{YOUR_DOMAIN\}** te vervangen door uw domein, bijvoorbeeld microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration wordt https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Ga naar de **OpenID-URL** met uw domein.
1. AAD-tenant-id is zichtbaar in meerdere eigenschapswaarden.
1. Zoek **authorization_endpoint** en extraheer de GUID direct na **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>De id van uw AAD-beveiligingsgroep zoeken
De id van de AAD-beveiligingsgroep is een GUID en ziet er als volgt uit: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Bij deze stap wordt ervan uitgegaan dat de gebruiker lid is van de groep waarvan de id wordt gezocht.
1. Ga naar de grafiekverkenner: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Klik op **Aanmelden bij Microsoft** en meld u aan met uw referenties.
1. Klik links op **Meer voorbeelden weergeven** nadat u zich hebt aangemeld.
1. Schakel **Groepen** in het rechterdeelvenster in.
1. Sluit het rechterdeelvenster.
1. Klik op **Alle groepen waartoe ik behoor**.
1. Zoek uw groep in het tekstvak **Voorbeeld van antwoord**.
1. De id van de beveiligingsgroep wordt vermeld onder de eigenschap **Id**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Creditcardgegevens testen voor het uitvoeren van testinkopen
Voor het uitvoeren van testtransacties op de site kunt u de volgende creditcardgegevens testen:

Kaartnummer: 4111-1111-1111-1111, vervaldatum: 10/20, CVV: 737

*Opmerking: Gebruik nooit echte creditcardgegevens op de testsite!*
### <a name="useful-links"></a>Nuttige koppelingen
* [LCS (Lifecycle Services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure-portal](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)
* [Help-bronnen voor Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Ondersteuning voor Microsoft Dynamics 365 Commerce Preview
Als u problemen ondervindt tijdens het uitvoeren van de inrichting, gaat u naar de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer) voor hulp. 

Als u problemen ondervindt bij het openen van de Yammer-groep, kunt u ons via e-mail bereiken op **Dynamics365Commerce@microsoft.com**. Dit e-mailadres wordt niet actief gecontroleerd, dus het kan even duren voordat u een reactie ontvangt.
***
## <a name="prerequisites-for-optional-features"></a>Vereisten voor optionele functies
Als u de transactionele e-mailfuncties wilt evalueren, moet aan de volgende voorwaarden worden voldaan:
* U hebt een e-mailserver beschikbaar (SMTP-server), die kan worden gebruikt vanuit het Azure-abonnement waar u de voorbeeldomgeving inricht.
* U hebt het FQDN/IP-adres, het SMTP-poortnummer en de verificatiegegevens van de server beschikbaar.

Als u functies voor beheer van digitale activa wilt evalueren, moet u aan de volgende voorwaarden voldoen:
* U hebt de **CMS-tenantnaam** bij de hand. Hieronder vindt u instructies voor het zoeken naar deze naam.
### <a name="configure-image-backend-optional"></a>Backend van afbeelding configureren (optioneel)
##### <a name="finding-your-media-base-url"></a>De basis-URL van media zoeken
*Opmerking: voordat u deze stap kunt voltooien, moet u de **site-instellingen** voltooien.*
1. Meld u aan bij het hulpprogramma voor sitebeheer met de URL die u eerder hebt genoteerd.
1. Open de site **Fabrikam**.
1. Kies **Activa** in het menu aan de linkerkant.
1. Selecteer één afbeeldingsactivum.
1. Ga naar de **Openbare URL** vanuit de eigenschappencontrole aan de rechterkant. Deze bevat een URL.
    * Voorbeeld-URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Vervang de laatste id in de URL (MA1nQC in de voorbeeld-URL hierboven) door de volgende tekenreeks: **search?fileName=**
    * Voorbeeld-URL na vervanging: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Dit is uw **basis-URL voor media**. Noteer deze.
##### <a name="updating-the-media-base-url"></a>Basis-URL voor media bijwerken
1. Meld u aan bij de omgeving (HQ).
1. Ga met het menu links naar **Modules > Detailhandel > Afzetkanaalinstellingen > Afzetkanaalprofielen**.
1. Klik op **Bewerken**.
1. Vervang vanuit de **Profieleigenschappen** de eigenschapswaarde voor **Basis-URL voor mediaserver** door de **Basis-URL voor media** die u eerder hebt gemaakt.
1. Selecteer het andere kanaal in de lijst aan de linkerkant, onder **standaard** kanaal.
1. Klik onder **Profieleigenschappen** op **+ Toevoegen**.
1. Kies voor de toegevoegde eigenschap **Basis-URL voor mediaserver** als eigenschapssleutel en voor eigenschapswaarde voert u de **Basis-URL voor media** in die u eerder hebt gemaakt.
1. Klik op **Opslaan**.

### <a name="configure-email-server-optional"></a>E-mailserver configureren (optioneel)
Houd er rekening mee dat de SMTP-server of e-mailservice die u hier invoert, toegankelijk moet zijn vanuit het Azure-abonnement dat u voor de omgeving gebruikt.
1. Meld u aan bij de omgeving (HQ).
1. Ga met het menu links naar **Modules > Detailhandel > Instelling van hoofdkantoor > Parameters > E-mailparameters**.
1. Klik op het tabblad **SMTP-instellingen**.
1. Typ in het veld **Server voor uitgaande e-mail** de FQDN of het IP-adres van uw SMTP-server of e-mailservice.
1. Voer in het veld **SMTP-poortnummer** het poortnummer in (standaard is dit 25 wanneer u SSL niet gebruikt).
1. Typ in het veld **Gebruikersnaam** een waarde (als verificatie is vereist).
1. Typ in het veld **Wachtwoord** een waarde (als verificatie is vereist).
1. Klik op **Opslaan**.
1. Klik op **Vernieuwen**.
1. Klik op het tabblad **Testbericht**.
1. Selecteer **SMTP** in het veld E-mailprovider.
1. Voer in het veld **Verzenden naar** het e-mailadres in waar u het testbericht wilt afleveren.
1. Klik op **Testbericht verzenden**.
### <a name="configure-email-templates-optional"></a>E-mailsjablonen configureren (optioneel)
De e-mailsjabloon voor elke transactionele gebeurtenis waarnaar u e-mailberichten wilt verzenden, moet worden bijgewerkt met een geldig e-mailadres van de afzender.
1. Ga met het menu links naar **Modules > Organisatiebeheer > Instellingen > Parameters > E-mailsjablonen van organisatie**.
1. Klik op **Lijst weergeven**.
1. Voor elke sjabloon in de lijst:
    1. Typ in het veld **E-mail afzender** het e-mail adres van de afzender voor deze e-mailsjabloon.
    1. Optioneel Typ in het veld **Naam afzender** een naam die wordt gebruikt als afzender voor deze e-mailsjabloon.
1. Klik op **Opslaan**.
### <a name="customizing-email-templates-optional"></a>E-mailsjablonen aanpassen (optioneel)
U kunt de e-mailsjablonen aanpassen om andere afbeeldingen te gebruiken of de koppelingen in de sjabloon bijwerken om terug te koppelen naar uw Preview-omgeving. In de volgende stappen wordt uitgelegd hoe u de standaard sjablonen kunt downloaden, aanpassen en bijwerken in het systeem.
1. Download met een browser [het .zip-bestand met standaard e-mailsjablonen voor Microsoft Dynamics 365 Commerce Preview](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) met de volgende HTML-documenten op uw lokale computer.
    1. Sjabloon voor orderbevestiging
    1. Sjabloon voor uitgifte van geschenkbon
    1. Sjabloon voor nieuwe order
    1. Sjabloon voor verpakkingsorder
    1. Sjabloon voor orderverzameling
1. Pas de sjablonen aan met een tekst- of HTML-editor. Zie hieronder voor een lijst met ondersteunde tokens.
1. Meld u aan bij de omgeving (HQ).
1. Ga met het menu links naar **Modules > Detailhandel > Instelling van hoofdkantoor > Parameters > E-mailsjablonen van organisatie**.
1. Vouw de lijst links uit om alle sjablonen te bekijken.
1. Voer de volgende stappen uit voor elk van de sjablonen die u wilt aanpassen:
    1. Selecteer de sjabloon in de lijst.
    1. Selecteer onder **Inhoud van e-mailbericht** de toepasselijke taalversie in de lijst (standaard **en-us**).
    1. Klik onder **Inhoud van e-mailbericht** op **Bewerken**. Het deelvenster **E-mailsjabloon uploaden** wordt geopend.
    1. Klik op **Bladeren** en zoek het HTML-bestand met de aangepaste inhoud.
    1. Klik op **Uploaden**, de sjabloon wordt geüpload naar het systeem en er wordt een voorbeeld weergegeven.
    1. Klik op **OK**.
    1. (Optioneel) Pas de eigenschap **Onderwerp** van de sjabloon aan.
    1. Klik op **Opslaan**.

#### <a name="supported-tokens-in-the-email-template"></a>Ondersteunde tokens in de e-mailsjabloon
Deze tokens worden als de e-mail wordt weergegeven, vervangen door de werkelijke waarden die van toepassing zijn op de klant en de order.

**Verkooporder**: de volgende tokens gelden voor de algehele verkooporder.

|Naam van token|Token |
|---|---|
|Ordernummer|%salesid%|
|Naam van klant|%customername%|
|Afleveradres|%deliveryaddress%|
|Factureringsadres|%customeraddress%|
|Besteldatum|%shipdate%|
|Bezorgingsmodus|%modeofdelivery%|
|Korting|%discount%|
|Btw|%tax%|
|Ordertotaal|%total%|

**Verkoopregel**: de volgende tokens worden voor elk product in de order ingevuld.

*Opmerking: plaats de tokens voor **Productlijst - begin** en **Productlijst - eind** aan het begin en einde van het HTML-blok dat voor elk product wordt herhaald.*

|Naam van token|Token |
|---|---|
|Productlijst - begin|\<!--%tablebegin.salesline% -->|
|Productlijst - eind|\<!--%tableend.salesline%-->|
|Productnaam|%lineproductname%|
|Beschrijving|%lineproductdescription%|
|Hoeveelheid|%linequantity%|
|Regel met eenheidsprijs|%lineprice% (controleren)|
|totaal regelartikel|%linenetamount%|
|regelkorting|%linediscount%|
|Verzenddatum|%lineshipdate%|
|Aanschaffingsmethode|%linedeliverymode%|
|afleveradres|%linedeliveryaddress%|
|Verkoopeenheid van regel|%lineunit%|

