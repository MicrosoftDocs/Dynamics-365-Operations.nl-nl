---
title: Directe integratie van Italiaanse FatturaPA met SDI instellen
description: Dit artikel biedt informatie die u zal helpen om aan de slag te gaan met elektronische facturering voor Italië en om directe integratie van Italiaanse FatturaPA met het Exchange-systeem (SDI) in te stellen.
author: abaryshnikov
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 510cf05e7bbc925478f9a1a4ea2ea27fe397c570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853187"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Directe integratie van Italiaanse FatturaPA met SDI instellen

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektronische facturering voor Italië ondersteunt momenteel mogelijk niet alle functies die beschikbaar zijn voor elektronische facturen in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.

Dit artikel bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Italië in Finance en Supply Chain Management. U wordt door de configuratiestappen geleid die land-/regioafhankelijk zijn in de Regulatory Configuration Services (RCS). Deze stappen vullen de stappen aan die worden beschreven in [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit artikel uitvoert, moet aan de volgende vereisten zijn voldaan:

- Voer de stappen in [Aan de slag met servicebeheer voor Elektronische facturering](e-invoicing-get-started.md) uit.
- Importeer de functie **Italiaanse FatturaPA (IT)** voor elektronische facturering in RCS vanuit de algemene opslagplaats. Zie de functie [Een functie voor elektronische facturering importeren vanuit de sectie van de Microsoft-configuratieprovider](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) van het eerder genoemde artikel 'Aan de slag met elektronische facturering' voor meer informatie.
- Voeg koppelingen van de vereiste certificaten toe aan de serviceomgeving. De vereiste certificaten zijn het certificaat voor digitale handtekening, het CA-certificaat (Certificate Authority) en het Clients-certificaat. Zie de sectie [Een digitaal certificaatgeheim maken](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) van het artikel 'Aan de slag met servicebeheer via Elektronische facturering' voor meer informatie.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Landspecifieke configuratie voor de Italiaanse functie FatturaPA (IT) voor elektronische facturering

Voltooi de volgende procedure voordat u de toepassingsinstellingen implementeert naar uw verbonden Finance- of Supply Chain Management-app.

Deze sectie is een aanvulling op de sectie [Landspecifieke configuratie van toepassingsinstellingen](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) in het artikel 'Aan de slag met elektronische facturering'.

### <a name="create-a-new-feature"></a>Een nieuwe functie maken

1. Meld u aan bij RCS.
2. Markeer in de werkruimte voor **elektronische rapportage** in de sectie **Configuratieproviders** de configuratieprovider van uw bedrijf als actief.
3. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
4. Selecteer op de pagina **Functies voor elektronische facturering** de optie **Toevoegen** \> **Gebaseerd op bestaande functie**.
5. Selecteer onder **Microsoft-configuratieprovider** de optie **Italiaanse FatturaPA (IT)** als een basisfunctie, voer een naam in en selecteer vervolgens **Functie maken**.

### <a name="set-up-application-specific-parameters"></a>Toepassingsspecifieke parameters instellen

1. Selecteer op de pagina **Functies voor elektronische facturering** de functie die u wilt bewerken.
2. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
3. Selecteer op het tabblad **Configuraties** een configuratie en selecteer vervolgens **Toepassingsspecifieke parameters**.
4. Zorg er in de sectie **Opzoekopdrachten** voor dat u de **Lijst met Natura-subcategorieën voor omgekeerde toeslag** hebt geselecteerd.
5. Selecteer **Toevoegen** in de sectie **Voorwaarden**.
6. Voeg specifieke voorwaarden toe voor elke subcategorie die in het systeem is gedefinieerd en sla vervolgens uw wijzigingen op.

    > [!NOTE]
    > In de kolom **Naam** kunt u de waarde van de tijdelijke aanduiding **\*Leeg\*** of **\*Niet leeg\*** selecteren in plaats van een specifieke waarde.

### <a name="configure-a-processing-pipeline-for-export"></a>Een verwerkingspijplijn configureren voor export

1. Selecteer op de pagina **Functies voor elektronische facturering** de functie die u wilt bewerken.
2. Selecteer op het tabblad **Instellingen** de optie **Verkoopfacturen** en selecteer vervolgens **Bewerken**.
3. Doorloop de acties in de sectie **Verwerkingspijplijn** en stel alle vereiste velden in:

    - Geef voor de actie **Document ondertekenen** in het veld **Certificaatnaam** het certificaat voor digitale handtekening op.
    - Stel voor de actie **Indienen** de velden **URL-adres** en **Certificaten** in. De waarde van het veld **Certificaten** is een reeks certificaten, waarvan het eerste het hoofd-CA-certificaat (caentrate.cer) is en de tweede het Clients-certificaat.

4. Selecteer **Valideren** om er zeker van te zijn dat alle vereiste velden zijn ingesteld.
5. Sla uw wijzigingen op en sluit de pagina.
6. Selecteer op het tabblad **Instellingen** de optie **Projectfacturen** en selecteer vervolgens **Bewerken**.
7. Herhaal stap 3 tot en met 5 voor projectfacturen.

### <a name="configure-the-processing-pipeline-for-import"></a>De verwerkingspijplijn configureren voor import

1. Selecteer op de pagina **Functies voor elektronische facturering** de functie die u wilt bewerken.
2. Selecteer op het tabblad **Instellingen** de optie **Facturen importeren** en selecteer vervolgens **Bewerken**.
3. Voer in de sectie **Gegevenskanaal** op het tabblad **Parameters** in het veld **Gegevenskanaal** een tekenreekswaarde in.
4. Stel de velden voor de instelling in op het tabblad **Toepasbaarheidsregels**. U kunt de standaardclausule **Kanaal** gebruiken door de waarde die u in de vorige stap voor het veld **Gegevenskanaal** hebt ingesteld, door te geven aan het veld **Waarde**.

    ![Toepasbaarheidsregels instellen.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Selecteer **Valideren** om er zeker van te zijn dat alle vereiste velden zijn ingesteld.

### <a name="deploy-the-feature"></a>De functie implementeren

1. Voltooi, publiceer en implementeer de functie voor de serviceomgeving. Zie de sectie [De functie voor elektronische facturering implementeren in de serviceomgeving](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) van het artikel 'Aan de slag met elektronische facturering' voor meer informatie.
2. Implementeer de functie in de verbonden toepassing. Zie de sectie [De functie voor elektronische facturering implementeren met verbonden toepassing](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) van het artikel 'Aan de slag met elektronische facturering' voor meer informatie.

### <a name="set-up-finance"></a>Finance instellen

1. Meld u aan bij uw Finance-omgeving.
2. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**.
3. Selecteer **Opslagplaatsen** \> **Algemeen** \> **Openen**.
4. Selecteer en importeer de configuraties **Contextmodel klantfactuur** en **Importeren van leveranciersfacturen (IT)**.
5. Ga naar **Organisatiebeheer** \> **Instellen** \> **Parameters voor elektronische documenten**.
6. Zoek op het tabblad **Functies** naar de functie **Italiaanse elektronische factuur** en schakel vervolgens het selectievakje **Inschakelen** in.
7. Ga naar het tabblad **Elektronisch document** en zorg ervoor dat de velden voor **Klantfactuurjournaal** en **Projectfactuur** worden ingesteld volgens de informatie in [Dem toepassingsinstellingen configureren](e-invoicing-get-started.md#configure-the-application-setup).

### <a name="set-up-vendor-invoice-import"></a>Importeren van leveranciersfacturen instellen 

1. Markeer in Finance in de werkruimte **Elektronische rapportage** in de sectie **Configuratieproviders** de configuratieprovider van uw bedrijf als actief.
2. Selecteer **Rapportageconfiguraties**.
3. Selecteer **Contextmodel klantfactuur** en selecteer vervolgens **Configuratie maken**.
4. Selecteer **Afleiden van naam: Contextmodel klantfactuurcontextmodel, Microsoft** om een afgeleide configuratie te maken.
5. Selecteer **Ontwerper** in de versie **Concept**.
6. Selecteer in de structuur **Gegevensmodel** de optie **Model toewijzen aan gegevensbron**.
7. Selecteer in de structuur **Definities** de optie **DataChannel** en selecteer vervolgens **Ontwerper**.
8. Vouw in de structuur **Gegevensbronnen** de container **\$Context\_kanaal** uit.
9. Selecteer in het veld **Waarde** de optie **Bewerken**. 
10. Voer de naam van het gegevenskanaal in. De naam mag maximaal 10 tekens lang zijn. Deze moet overeenkomen met de waarde van de parameter **Gegevenskanaal** van het gegevenskanaal voor de elektronische factureringsfunctie in RCS.
11. Sla uw wijzigingen op en ga vervolgens naar **Rapportconfiguraties** \> **Configuratieversie voltooien**.
12. Selecteer op het tabblad **Externe kanalen** in de sectie **Kanalen** de optie **Toevoegen**.
13. Geef in het veld **Kanaal** de waarde voor **\$Contextkanaal** op.
14. Geef waarden op in de velden **Beschrijving** en **Bedrijf**.
15. Selecteer in het veld **Documentcontext** de nieuwe configuratie die u hebt afgeleid van **Contextmodel klantfactuur**. De toewijzingsbeschrijving moet **Context gegevenskanaal** zijn.
16. Selecteer op het tabblad **Bronnen importeren** de optie **Toevoegen** en stel de volgende waarden in:

    - **Naam:** OutputFile
    - **Naam van gegevensentiteit:** Leveranciersfactuurkoptekst (**Gegevensentiteit:** VendorInvoiceHeaderEntity)
    - **Modeltoewijzing:** Importeren van leveranciersfacturen (IT)

> [!NOTE]
> Als u leveranciersfacturen uit verschillende bronnen hebt geïmporteerd, kunt u verschillende externe kanalen en verschillende afgeleide configuraties maken met verschillende waarden voor **\$Contextkanaal**. U wilt bijvoorbeeld mogelijk leveranciersfacturen importeren voor verschillende rechtspersonen.

## <a name="proxy-server-setup"></a>Proxyserver instellen

Deze sectie bevat informatie die u helpt bij het instellen en configureren van de proxyservice voor communicatie tussen het Uitwisselingssysteem (SDI) en de service voor elektronische facturering.

### <a name="create-an-app-registration"></a>Een app-registratie maken

1. Gebruik het volgende Windows PowerShell-script om een zelf ondertekend certificaat te maken voor S2S-verificatie (Service-to-Service).

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Sla het .pfx-certificaatbestand op in de sleutelkluis en verwijder vervolgens de lokale kopie.
3. Meld u als beheerder aan bij de [Azure-portal](https://portal.azure.com).
4. Maak een app-registratie voor de SDI-proxyservice.

    1. Ga naar **App-registraties**, maak een registratie en stel de volgende waarden hiervoor in:

        - **Naam:** SDI-proxyclient
        - **Ondersteunde accounttypen:** alleen accounts in deze organisatiedirectory (enkele tenant)

    2. Selecteer **Registreren** en selecteer vervolgens de app-registratie die u zojuist hebt gemaakt.
    3. Ga naar **API-machtigingen** en selecteer **Beheerdersmachtigingen verlenen**.
    4. Ga naar **Certificaten en geheimen**, selecteer **Uploadcertificaat** en upload het .cer-certificaatbestand voor S2S-verificatie.
    5. Ga naar **Ondernemingstoepassingen** en selecteer de app die u hebt gemaakt.
    6. Sla de waarden **Toepassings-id** (client-id) en **Object-id** voor de app op.
    7. Het factureringsserviceteam moet de app toegang tot de service verlenen. Verzend de waarden van de volgende parameters naar <D365EInvoiceSupport@microsoft.com>:

        - AAD-tenant-id
        - LCS-omgevings-id
        - Toepassings-id
        - Object-id

5. Voeg in RCS de app toe aan de lijst met toepassingen voor uw serviceomgeving.

    1. Ga naar **Globalisatiefuncties** \> **Omgevingen** \> **Elektronische facturering** \> **Serviceomgevingen** en selecteer uw omgeving.
    2. Voeg in de sectie **Toepassingen** een rij toe aan het raster en voer de naam en object-id van de app in.

        ![De toepassing toevoegen aan de serviceomgeving.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Selecteer **Opslaan** en vervolgens **Publiceren**.

### <a name="create-an-azure-virtual-machine"></a>Een virtuele machine voor Azure maken

1. Ga op de [Azure-portal](https://portal.azure.com) naar **Virtuele machines** en selecteer **Nieuwe maken**.
2. Selecteer op het tabblad **Basisprincipes** uw abonnement en resourcegroep. De waarden moeten het abonnement en de resourcegroep zijn waar uw sleutelkluis en Blob-opslag zich bevinden.
3. Selecteer de regio. Deze waarde moet de regio zijn waar uw omgeving Finance is geïmplementeerd.
4. Voeg de gebruikersnaam en het wachtwoord van de beheerder toe en sla deze op in de sleutelkluis.
5. Selecteer in het veld **Binnenkomende poorten selecteren** de optie **HTTPS (443)** en **RPD (3389)**.

    > [!NOTE]
    > Het wordt aangeraden de poort **RDP (3389)** uit te schakelen wanneer het systeem in productie wordt genomen. U kunt deze opnieuw inschakelen als u verbinding moet maken met de virtuele machine (VM) voor het oplossen van problemen.

    ![De velden op het tabblad Basisprincipes instellen om een Azure VM te maken.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Schakel op het tabblad **Schijven** op het sneltabblad **Geavanceerd** het selectievakje **Beheerde schijven gebruiken** in. Laat het selectievakje **Tijdelijke besturingssysteemschijf** uitgeschakeld.

    ![De velden op het tabblad Schijven instellen om een Azure VM te maken.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Selecteer op het tabblad **Netwerken** onder het veld **Openbare IP** de optie **Nieuwe maken**.

    ![De velden op het tabblad Netwerken instellen om een Azure VM te maken.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Ga in het dialoogvenster **Openbaar IP-adres maken** naar de veldgroep **SKU** en selecteer de optie **Standaard**. Selecteer de optie **Statisch** in de veldgroep **Toewijzing**.

    ![Een openbaar IP-adres maken.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Schakel op het tabblad **Beheer** het selectievakje **Automatische afsluiting** uit om automatische afsluiting uit te schakelen.
10. Stel het veld **Updates van gastbesturingssysteem** in op **Handmatig** en stel vervolgens elk ander gewenst beleid in.
11. Controleer en maak de VM.
12. Ga in de nieuwe VM naar **Identiteit** \> **Systeem toegewezen** en stel de optie **Status** in op **Aan**.
13. Verleen de VM toegang tot de sleutelkluis.

    1. Ga in de sleutelkluis naar **Toegangscontrole (IAM)** \> **Roltoewijzingen**.
    2. Selecteer **Roltoewijzing toevoegen** en stel daarna de volgende velden in:

        1. Geef in het veld **Rol** de optie **Sleutelkluisgeheimen gebruiker** op.
        2. Geef in het veld **Toegang toewijzen aan** de optie **Virtuele machine** op.
        3. Geef in het veld **Abonnement** uw abonnement op.
        4. Geef in het veld **Selecteren** uw VM op.

    3. Ga naar **Toegangsbeleid**.
    4. Selecteer **Toegangsbeleid toevoegen** en stel daarna de volgende velden in:

        1. Selecteer in het veld **Geselecteerde principal** uw VM.
        2. Selecteer in de sectie **Certificaat** de machtigingen **Lijst** en **Ophalen**.

14. Ga in de [Azure-portal](https://portal.azure.com) naar **Openbare IP-adressen** en selecteer het IP-adres dat in de VM is gemaakt.
15. Ga naar **Configuratie** en stel de DNS-naam (Domain Name System) in.

### <a name="prepare-the-proxy-service-environment"></a>De proxyserviceomgeving voorbereiden

Volg deze stappen op de computer waarop de proxyservice wordt gehost.

1. Verbinding maken met de VM via verbinding met extern bureaublad.
2. Open de invoegtoepassing voor het lokale machinecertificaat. Zie [Procedure: Certificaten weergeven met de MMC-invoegtoepassing](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in) voor meer informatie.
3. Importeer het certificaat **caentrate.cer** voor productie en **CAEntratetest.cer** voor testen in het archief van [vertrouwde basiscertificeringsinstanties](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** is het hoofd-CA-certificaat dat door de instantie is verstrekt.)
4. Open in het Configuratiescherm de optie **Windows-functies in- of uitschakelen** of ga naar **Serverbeheer** \> **Rollen en functies toevoegen** voor het serverbesturingssysteem (OS) en schakel IIS-functies (Internet Information Services) in:

    - Hulpprogramma's voor webbeheer
        - IIS-beheerconsole
    - World Wide Web Services
        - Functies voor toepassingsontwikkeling
            - .NET-uitbreidbaarheid 4.7 (of 4.8)
            - ASP
            - ASP.NET 4.7 (of 4.8)
            - CGI
            - ISAPI-uitbreidingen
            - ISAPI-filters
        - Veelgebruikte HTTP-functies
            - Standaarddocument
            - Map voor browsen
            - HTTP-fouten
            - Statische inhoud
        - Status en diagnose
            - HTTP-logboekregistratie
            - Tracering
        - Prestatiefuncties
            - Compressie van statische inhoud
        - Beveiliging
            - Aanvragen filteren

    ![IIS-functies inschakelen.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>De SDI-proxyservice instellen in IIS

1. Ga in Microsoft Dynamics Lifecycle Services (LCS) naar de library voor gedeelde activa en selecteer **Gegevenspakket** als activatype.
2. Zoek **SDI-proxy voor elektronische factureringsservice** download deze naar de VM.
3. Configureer de service.

    1. Pak de archiefmap **SDI-proxy voor elektronische factureringsservice** uit die u hebt gedownload.
    2. Open in de map **src\\FattureService** het bestand **appsettings.json** en stel de volgende parameters in:

        - **KeyVaultUri**: geef het adres op van de sleutelkluis waarin het clientcertificaat voor de factureringsservice is opgeslagen.
        - **TenantId**: geef de GUID-waarde (Globally Unique Identifier) van de tenant van de klant op.
        - **EnvironmentId**: geef de id van de LCS-omgeving op.
        - **ClientId**: geef de app-id op van de registratie van de tussenliggende services-app in de tenant van de klant.
        - **ClientCertificateName**: geef de naam van het S2S-certificaat in de sleutelkluis op.
        - **SecurityServiceClientOptions.Endpoint**: geef de URL van de beveiligingsservice op.
        - **SecurityServiceClientOptions.Resource**: geef de scope op waarvoor u het token wilt verwerven.
        - **InvoicingServiceClientOptions.Endpoint**: geef het eindpunt van de factureringsservice op. Deze waarde moet gelijk zijn aan het eindpunt dat wordt gebruikt voor RCS en Finance.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId**: geef de naam van de serviceomgeving op. Deze waarde moet de naam van uw Finance-omgeving zijn.
        - **NotificationsFolder**: geef de map op waarin binnenkomende meldingenbestanden moeten worden opgeslagen.

    3. Zoek in het bestand **web.config** de volgende regel en voeg de vingerafdruk van het proxyservercertificaat toe.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Wanneer het systeem naar productie gaat, kunt u sommige waarden in het bestand web.config wijzigen om zo de hoeveelheid logboekinformatie die wordt verzameld te verminderen en schijfruimte te besparen. Wijzig in het knooppunt **\<system.diagnostics\>\<source\>** de waarde van **switchValue** in **Critical,Error**. Zie [Weergavefunctie voor MS Service Trace](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) voor meer informatie.

4. Open IIS Manager. Blijf in de structuur aan de linkerkant in het hoofdknooppunt. Selecteer aan de rechterkant de optie **Servercertificaten**.

    ![Servicecertificaten selecteren in IIS Manager.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Open het menu en selecteer **Importeren**.
6. Geef in het dialoogvenster **Certificaat importeren** in het veld **Certificaatbestand (.pfx)** het pad van het .pfx-bestand voor het proxyservercertificaat op.

    ![Het proxyservicecertificaatbestand opgeven.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Selecteer **Locaties** en houd deze ingedrukt (of klik met de rechtermuisknop) en selecteer vervolgens **Website toevoegen**.
8. Voer in het dialoogvenster **Website toevoegen**, in het veld **Sitenaam** een naam in voor de site.
9. Wijs in het veld **Fysiek pad** de map **src\\FattureService** aan.
10. Selecteer in het veld **Bindingstype** de optie **https**.
11. Geef in het veld **Hostnaam** de hostnaam op.
12. Laat de velden **IP-adres** en **Poort** ingesteld op de standaardwaarden.
13. Zorg ervoor dat het selectievakje **Indicatie servernaam vereisen** is uitgeschakeld, omdat SDI die technologie niet ondersteunt.
14. Selecteer in het veld **SSL-certificaat** het proxyservercertificaat dat u hebt geïmporteerd.
15. Geef in het veld **Toepassingsgroep** een groep op voor de locatie en maak een notitie van de naam van de groep (bijvoorbeeld **SdiAppPool**).

    ![Een website toevoegen.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Nadat u de website hebt gemaakt, opent u het menu voor **SSL-instellingen**.

    ![Het menu openen voor SSL-instellingen.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Schakel het selectievakje **SSL vereisen** in en schakel vervolgens in de veldgroep **Clientcertificaten** de optie **Vereisen** in.

    ![SSL-instellingen configureren.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Open **Map voor browsen** en selecteer **Inschakelen**.
19. Ga in een webbrowser naar **serverDNS/TrasmissioneFatture.svc**. Er moet een standaardpagina over de service worden weergegeven.

    ![De service controleren in een browser.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Maak de volgende mappen om logboeken en bestanden op te slaan:

    - **C:\\Logs\\**: sla hier logbestanden op. Deze bestanden kunnen worden bekeken met de [weergavefunctie voor MS Service Trace](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\Files\\**: sla hier alle responsbestanden op.

21. Ken in File Explorer de optie **NETWERKSERVICE** en **IIS AppPool\\SdiAppPool** (of **IIS AppPool\\DefaultAppPool** als u de standaardgroep gebruikt) toegang tot de mappen **Logs** en **Files**.

    1. Selecteer een van de mappen en houd dit ingedrukt (of klik er met de rechtermuisknop op) en selecteer **Eigenschappen**.
    2. Selecteer in het dialoogvenster **Eigenschappen** op het tabblad **Beveiliging** de optie **Bewerken**.
    3. Voeg de gebruikers toe als ze niet in de lijst staan.
    4. Herhaal stap 1 tot en met 3 voor de andere map.

    ![Machtigingen aan de servicegebruiker toevoegen.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Privacyverklaring 

Als u de functie **Italiaanse elektronische factuur** wilt inschakelen, moeten mogelijk beperkte gegevens worden verzonden. Deze gegevens omvatten de belastingregistratie-id van de organisatie. Een beheerder kan de Italiaanse functie voor elektronische facturering in- en uitschakelen. Voer de volgende stappen uit om de functie uit te schakelen.

1. Ga naar **Organisatiebeheer** \> **Instellen** \> **Parameters voor elektronische documenten**.
2. Selecteer op het tabblad **Functies** de rijen die de functie **Italiaanse elektronische factuur** bevatten en selecteer vervolgens **Nu uitschakelen**.

Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de sectie 'Privacyverklaring' in de documentatie over land-/regiospecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer voor Elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met Elektronische facturering](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
