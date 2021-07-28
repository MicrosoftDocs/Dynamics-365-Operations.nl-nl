---
title: Zelfstudie over het instellen en installeren van Regression Suite Automation Tool
description: Dit onderwerp is een zelfstudie waarin wordt beschreven hoe u RSAT (Regression Suite Automation Tool) instelt en installeert.
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: fc9b330926dfc12890d0bc32e68b4b531616fc2b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357547"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Zelfstudie over het instellen en installeren van Regression Suite Automation Tool

Dit onderwerp is een zelfstudie waarmee u RSAT en de bijbehorende hulpprogramma's kunt instellen en gebruiken.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Gebruik uw internetbrowser om deze pagina als PDF-bestand te downloaden en op te slaan.

## <a name="key-concepts"></a>Belangrijke concepten

- Begrijp de installatie en de vereiste instellingen voor de verschillende toepassingen die ondersteuning bieden voor RSAT (Regression Suite Automation Tool).
- Begrijp hoe u met de functie Taakregistratie, samen met Microsoft Dynamics Lifecycle Services (LCS) en Microsoft Azure DevOps testcases kunt maken, configureren, uitvoeren, onderzoeken en hiervan rapporten kunt maken.
- Stel functionele gebruikers in staat om zakelijke taken vast te leggen met Taakregistratie en de taakregistraties vervolgens om te zetten in een reeks geautomatiseerde tests zonder broncode te hoeven schrijven.

## <a name="before-you-begin"></a>Voordat u begint

### <a name="prerequisites"></a>Vereisten

- Voor deze zelfstudie is een omgeving met Microsoft Dynamics 365 for Finance and Operations 10.0 (april 2019) of hoger vereist. Voor klanten die Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 gebruiken, wordt Platformupdate 20 (PU20) of hoger ook ondersteund.
- De gebruiker moet over beheerdersrechten voor de omgeving beschikken.
- U moet toegang hebben tot de LCS en Azure DevOps (voorheen Microsoft Visual Studio Team Services \[VSTS\]) van de klanttenant.
- De gebruiker die testsuites maakt en beheert, moet een licentie voor Azure DevOps Test Plans of Test Manager hebben. Ook de volgende licenties bieden u toegang tot testplannen:
    - Visual Studio Enterprise-licentie
    - Visual Studio Test Professional-licentie
    - Abonnementslicentie voor MSDN-platforms
- RSAT moet via een webbrowser toegang hebben tot de testomgeving.
- U kunt alleen testparameters genereren en bewerken als u Microsoft Excel hebt geïnstalleerd.

## <a name="configure-azure-devops"></a>Azure DevOps configureren

### <a name="user-eligibility"></a>Geschiktheid van gebruikers

Controleer of de gebruiker is gemaakt in Azure DevOps en een abonnementsniveau heeft dat toegang biedt tot Azure Test Plans. Een Azure DevOps Test Plans-licentie is alleen vereist als de gebruiker testcases maakt en beheert (dus niet alle RSAT-gebruikers hebben deze licentie nodig). Zie [Licentievereisten](/azure/devops/test/manual-test-permissions#license-requirements) voor informatie over de licentievereisten.

### <a name="create-a-new-azure-devops-project"></a>Een nieuw Azure DevOps-project maken

RSAT gebruikt Azure Devops voor het beheer van testcases en testsuites, rapportage en het onderzoeken van resultaten van testuitvoeringen.

> [!NOTE]
> U kunt een bestaand Azure DevOps-project gebruiken. Als het bestaande Azure DevOps-project echter zo is ingesteld dat een aangepaste sjabloon wordt gebruikt, wordt het foutbericht Fouten bij VSTS-synchronisatie weergegeven wanneer u testcases vanuit Modelleertool bedrijfsprocessen synchroniseert naar Azure DevOps (zie het gedeelte [De synchronisatie van BPM naar Azure DevOps testen](#test-the-synchronization-from-bpm-to-azure-devops)). Als de volgende aanbevelingen zijn opgevolgd voor de aangepaste sjabloon, kunt u de testcases synchroniseren naar Azure DevOps. (Deze aanbevolen procedures worden vermeld in het foutbericht.)

- Verwijder geen werkitemtypen of out-of-the-box-velden.
- Verwijder geen status van een werkitemtype.
- Voeg geen vereiste velden toe aan een werkitemtype.

![Foutbericht met een lijst met aanbevolen procedures.](./media/setup_rsa_tool_02.png)

Anders raden we u voor deze zelfstudie aan om een nieuw Azure DevOps-project te maken. Zie [Problemen bij synchronisatie naar Modelleertool bedrijfsprocessen met een aangepaste Azure DevOps-processjabloon (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/) voor meer informatie.

1. Open de URL van Azure DevOps (`https://dev.azure.com/<Azure DevOps Name>`).
2. Selecteer **Project maken** in de rechterbovenhoek van de Azure DevOps-pagina.

    ![De knop Project maken.](./media/setup_rsa_tool_03.png)

3. Vul de volgende velden in en selecteer **Maken**:

    - **Projectnaam**
    - **Versiebeheer**: selecteer **Team Foundation Version Control**. De standaardoptie, **Git**, wordt niet ondersteund.
    - **Werkitemproces**

    ![Het dialoogvenster Nieuw project maken.](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Een persoonlijke toegangstoken maken

In deze zelfstudie gebruikt u de LCS-oplossing BPM (Modelleertool bedrijfsprocessen) om een testcase-bibliotheek te maken en uw testcases met Azure DevOps te synchroniseren. U hebt een persoonlijk toegangstoken nodig om BPM met Azure DevOps te synchroniseren.

1. Selecteer het profielpictogram in de rechterbovenhoek van de pagina voor uw Azure DevOps-project en selecteer **Beveiliging**.

    ![De opdracht Beveiliging.](./media/setup_rsa_tool_05.png)

2. Selecteer in het linkerdeelvenster onder **Beveiliging** de optie **Persoonlijke toegangstokens**. Selecteer vervolgens **Nieuwe token**.

    ![De knop Nieuwe token op het tabblad Persoonlijke toegangstokens in Gebruikersinstellingen.](./media/setup_rsa_tool_06.png)

3. Vul de volgende velden in en selecteer **Maken**:

    - **Naam**
    - **Verval (UTC)**: selecteer **Aangepast** en gebruik vervolgens de datumkiezer om de laatste beschikbare datum te selecteren.
    - **Bereiken**: selecteer de optie **Volledige toegang**.

    ![Het dialoogvenster Een nieuwe persoonlijke toegangstoken maken.](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Noteer de gemaakte persoonlijke toegangstoken. U hebt deze later nodig wanneer u de RSAT-configuratie instelt.

    ![Persoonlijk toegangstoken.](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>Het LCS-project configureren

U hebt een LCS-project (Lifecycle Services) nodig voor de hoofdtestbibliotheek. LCS BPM wordt gebruikt als de hoofdbibliotheek voor uw testcases. BPM wordt gebruikt om test bibliotheken te beheren en te distribueren voor LCS-projecten. Een Microsoft-partner of onafhankelijke softwareleverancier (ISV) die testbibliotheken maakt, brengt testcases in de vorm van BPM-bibliotheken uit. In BPM worden testcases ingedeeld op bedrijfsprocessen. In BPM wordt de uitvoeringsvolgorde of -frequentie van uw testdoorloop niet bepaald. Deze details worden beheerd in Azure DevOps, zoals later in dit onderwerp wordt beschreven.  

Voor uw LCS-project kunt u bestaande klantimplementaties of partnerprojecten gebruiken.

### <a name="update-the-lcs-language"></a>De CSL-taal bijwerken

> [!NOTE]
> Bedrijfsprocessen wordt correct weergegeven in de gebruikersinterface als de LCS-voorkeurstaal is ingesteld op **Engels (Verenigde Staten)**.

1. Ga naar het LCS-implementatieproject.
2. Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Taalvoorkeur**.

    ![Taalvoorkeur bijwerken.](./media/setup_rsa_tool_09.png)

3. Selecteer in het veld **Voorkeurstaal** de optie **Engels (Verenigde Staten)** en selecteer vervolgens **Opslaan**.

    ![Het tabblad Voorkeurstaal in Gebruikersinstellingen.](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS configureren om verbinding te maken met het Azure DevOps-project

Als u eerder een nieuw Azure DevOps-project hebt gemaakt, configureert u het LCS-project om hiermee verbinding te maken. Als uw LCS-project al is verbonden met uw Azure DevOps-project, kunt u doorgaan met het volgende gedeelte.

1. Ga naar het LCS-implementatieproject.
2. Selecteer de knop **Menu** en vervolgens **Project settings**.

    ![De opdracht Project settings.](./media/setup_rsa_tool_11.png)

3. Selecteer **Visual Studio Team Services** in het linkerdeelvenster en selecteer vervolgens **Setup Visual Studio Team Services**.

    ![Het tabblad Visual Studio Team Services in Project settings.](./media/setup_rsa_tool_12.png)

4. Geef in het veld **Azure DevOps site URL** de URL van de Azure DevOps-site op. Voer in het veld **Personal access token** de persoonlijke toegangstoken in die eerder is gemaakt.

    > [!NOTE]
    > Hoewel VSTS nu bekend staat als Azure DevOps, gebruikt u de oude URL om uw Azure DevOps-project te maken. De URL voor Azure DevOps die in deze zelfstudie wordt gebruikt, is bijvoorbeeld `https://dev.azure.com/D365FOFastTrack/`. In de volgende afbeelding wordt deze echter ingevoerd als `https://D365FOFastTrack.visualstudio.com/`.

    ![Stap 1 in Setup Visual Studio Team Services.](./media/setup_rsa_tool_13.png)

5. Selecteer **Continue**.
6. Selecteer in het veld **Visual Studio Team Services project** het VSTS-project op de geselecteerde site die moet worden gekoppeld aan het LCS-project. Het veld **Process template** is standaard ingesteld op **Agile**. Neem voor een aangepaste sjabloon de richtlijn voor de aanbevolen procedure in [Een nieuw Azure DevOps-project maken](#create-a-new-azure-devops-project) door. Selecteer vervolgens **Continue**.

    ![Stap 2 in Setup Visual Studio Team Services.](./media/setup_rsa_tool_14.png)

7. Controleer de instellingen en selecteer vervolgens **Opslaan**.

    ![Stap 3 in Setup Visual Studio Team Services.](./media/setup_rsa_tool_15.png)

8. Selecteer **Authorize** om LCS te autoriseren om namens u toegang tot de geconfigureerde Azure DevOps-site te krijgen en functies in te schakelen die worden geïntegreerd met VSTS.

    ![De knop Authorize.](./media/setup_rsa_tool_16.png)

9. Er wordt een berichtvenster weergegeven waarin wordt aangegeven dat u naar een externe site wordt omgeleid om LCS te autoriseren om namens u verbinding met Visual Studio Team Services te maken. Daarnaast wordt gevraagd of u wilt doorgaan. Selecteer **Ja**.

    ![Berichtvenster.](./media/setup_rsa_tool_17.png)

10. Selecteer **Accepteren**.

    ![Toegang verlenen.](./media/setup_rsa_tool_18.png)

11. Als u geautoriseerd bent als gebruiker, moet u door de UI worden omgeleid naar de pagina met LCS-projectinstellingen.

    ![Geautoriseerde gebruiker.](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Een nieuwe BPM-bibliotheek maken

1. Ga naar het LCS-implementatieproject.
2. Selecteer de knop **Menu** en vervolgens **Business process modeler**.

    ![De opdracht Business process modeler.](./media/setup_rsa_tool_20.png)

3. Selecteer **New library**.

    ![De knop New library.](./media/setup_rsa_tool_21.png)

4. Voer in het veld **Library name** een naam in en selecteer **Create**. Geef de BPM-bibliotheek voor deze zelfstudie de naam **RSAT**.

    ![Het dialoogvenster Create new library.](./media/setup_rsa_tool_22.png)

5. Open de nieuwe BPM-bibliotheek **RSAT**.
6. Selecteer het proces **Sample Core Business Process** en selecteer vervolgens **Edit mode** rechts.

    ![De knop Edit mode.](./media/setup_rsa_tool_23.png)

7. Wijzig de waarde van de velden **Name** en **Description** in **Een product maken**. Selecteer **Save**.

    ![De velden Name en Description.](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Omgeving

### <a name="version-requirement"></a>Versievereiste

Een test- of sandbox-omgeving met versie 10 is vereist. Voor klanten die versie 7.3 gebruiken, wordt Platformupdate 20 of hoger ook ondersteund.

> [!NOTE]
> RSAT moet via een webbrowser toegang hebben tot uw testomgeving.

### <a name="user-criteria"></a>Gebruikerscriteria

De gebruiker moet over beheerdersrechten voor deze omgeving beschikken.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Help-instellingen configureren om verbinding te maken met LCS

Deze stap is vereist om verbinding te maken met LCS zodat taakregistraties kunnen worden opgeslagen in de juiste BPM-bibliotheek in LCS via de client.

1. Open de client.
2. Ga naar **Systeembeheer \> Instellen \> Systeemparameters**.
3. Selecteer op het tabblad **Help** in het veld **Help-configuratie van Lifecycle Services** het betreffende LCS-project (**RSAT** voor deze zelfstudie).

    ![Het veld Help-configuratie van Lifecycle Services op het tabblad Help.](./media/setup_rsa_tool_25.png)

    BPM-bibliotheken worden ingevuld onder het desbetreffende LCS-project.

4. Selecteer **Opslaan**.
5. Mogelijk moet u de browser vernieuwen om de bijgewerkte Help-inhoud weer te geven.

    ![Melding over het vernieuwen van de browser.](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Taakregistraties

> [!NOTE]
> Controleer of al uw taakregistraties starten op het hoofddashboard. Houd afzonderlijke opnamen kort en concentreer u op één bedrijfstaak, zoals het maken van een verkooporder.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Een taakregistratie maken en opslaan in de BPM-bibliotheek

Maak een bijbehorende taakregistratie die u kunt koppelen aan het eenvoudige bedrijfsproces dat in de nieuwe BPM-bibliotheek is gemaakt.

1. Open de client.
2. Selecteer op het hoofddashboard de knop **Instellingen** (het tandwielsymbool) en selecteer **Taakregistratie**.

    ![Taakrecorder selecteren in het menu Instellingen.](./media/setup_rsa_tool_27.png)

3. Selecteer **Registratie maken**.

    ![De knop Registratie maken.](./media/setup_rsa_tool_28.png)

4. Vul de velden **Naam van registratie** en **Omschrijving van registratie** in en selecteer **Starten**.

    ![De velden Naam van registratie en Omschrijving van registratie.](./media/setup_rsa_tool_29.png)

5. Registreer de stappen voor het maken van een product. Wanneer u klaar bent, selecteert u **Stoppen** om de registratie te stoppen.

    ![Stappen voor het maken van een product.](./media/setup_rsa_tool_30.png)

6. Selecteer **Opslaan in Lifecycle Services**.

    ![Taakregistratie opslaan in Lifecycle Services.](./media/setup_rsa_tool_31.png)

    Bibliotheekgegevens worden vanuit LCS geladen.

    ![Bibliotheekgegevens laden.](./media/setup_rsa_tool_32.png)

7. Selecteer de BPM-bibliotheek waaraan u de taakregistratie wilt koppelen. Selecteer voor deze zelfstudie de BPM-bibliotheek **RSAT** die eerder is gemaakt en het bedrijfsproces **Een product maken** daaronder. Selecteer vervolgens **OK**.

    ![De taakregistratie koppelen aan een BPM-bibliotheek en een bedrijfsproces.](./media/setup_rsa_tool_33.png)

    Het bericht Opgeslagen naar Lifecycle Services wordt weergegeven.

    ![Bericht over de opslag naar LCS.](./media/setup_rsa_tool_34.png)

8. Voer de volgende stappen uit als u de taakregistratie lokaal wilt opslaan en vervolgens wilt uploaden naar BPM via LCS:

    1. Als de registratie is voltooid, selecteert u **Opslaan op deze pc**.

        ![Opslaan op deze pc.](./media/setup_rsa_tool_35.png)

    2. Selecteer in de meldingsbalk van de browser de optie **Opslaan** of **Opslaan als** om het bestand op uw lokale computer op te slaan.

        ![Meldingsbalk.](./media/setup_rsa_tool_36.png)

    3. Ga naar de BPM-bibliotheek **RSAT** en selecteer het bedrijfsproces waarvoor u de taakregistratie wilt opslaan.
    4. Selecteer op het tabblad **Overzicht** de optie **Uploaden**.

        ![De knop Uploaden.](./media/setup_rsa_tool_37.png)

    5. Selecteer **Bladeren** en selecteer het AXTR-bestand dat u eerder hebt opgeslagen. Selecteer vervolgens **Uploaden**.

        ![Het AXTR-bestand selecteren om te uploaden.](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>De synchronisatie van BPM naar Azure DevOps testen

Nu een taakregistratie aan het bedrijfsproces is gekoppeld, moet u controleren of het bedrijfs proces en de gekoppelde taakregistratie naar Azure DevOps kunnen worden gesynchroniseerd als een functie en een testcase (respectievelijk) met behulp van de VSTS-synchronisatiefunctie in LCS.

> [!NOTE]
> Welk bijbehorend type werkitem in Azure DevOps wordt gemaakt, is afhankelijk van de processjabloon die u hebt geselecteerd toen u het LCS-project configureerde met Azure DevOps, zoals wordt beschreven in het gedeelte [Een nieuw Azure DevOps-project maken](#create-a-new-azure-devops-project).

1. Ga naar de BPM-bibliotheek en open de bibliotheek **RSAT** die u eerder hebt gemaakt.
2. Selecteer de knop met het weglatingsteken (**...**) en selecteer **VSTS synchroniseren**.

    ![De opdracht VSTS synchroniseren.](./media/setup_rsa_tool_39.png)

    Als de VSTS-synchronisatie is voltooid, wordt het tabblad **Vereisten** links weergegeven met het bijbehorende Azure DevOps-werkitem.

    > [!NOTE]
    > Het werkitem dat in Azure DevOps wordt gemaakt, heeft de BPM-bibliotheeknaam als titelvoorvoegsel.

    ![Het tabblad Vereisten.](./media/setup_rsa_tool_40.png)

3. Vernieuw de pagina.
4. Selecteer de knop met het weglatingsteken (**...**). De extra optie **Testcases synchroniseren** wordt weergegeven. Selecteer deze optie.

    ![De opdracht Testcases synchroniseren.](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Als de optie **Testcases synchroniseren** niet beschikbaar is als u de pagina hebt vernieuwd, gaat u naar de hoofdpagina voor BPM en selecteert u **Testcases synchroniseren** voor de hele bibliotheek zelf. Op deze manier dwingt u op effectieve wijze een synchronisatie af voor de hele bibliotheek.
    >
    > ![Testcases synchroniseren selecteren voor de hele bibliotheek.](./media/setup_rsa_tool_42.png)

    Als de synchronisatie van testcases is voltooid, wordt een nieuwe testcase gemaakt op het tabblad **Vereisten**.

    ![Nieuwe testcase op het tabblad Vereisten.](./media/setup_rsa_tool_43.png)

5. Ga naar uw Azure DevOps-project en selecteer **Borden \> Werkitems**.

    ![De opdracht Werkitems onder Borden.](./media/setup_rsa_tool_44.png)

6. Controleer of het werkitem en de testcase die u via BPM-synchronisatie hebt gemaakt, bestaan.

    ![Werkitem en testcase.](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT installeren en configureren

RSAT kan worden geïnstalleerd op elke computer waarop Windows 10 wordt uitgevoerd en waarmee verbinding kan worden gemaakt met de omgeving via een webbrowser (Internet Explorer of Google Chrome).

> [!NOTE]
> Voordat u een nieuwe versie van het hulpprogramma installeert, is het raadzaam om de vorige versie te verwijderen.

### <a name="install-an-authentication-certificate"></a>Een verificatiecertificaat installeren

Als u verificatie wilt inschakelen, moet u een certificaat genereren en installeren op de computer waarop RSAT wordt uitgevoerd.

#### <a name="generate-a-certificate"></a>Een certificaat genereren

1. Als u een certificaatbestand wilt genereren, opent u een Microsoft Windows PowerShell-venster als beheerder en voert u de volgende opdracht uit.

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Open certificaatbeheer door **certlm.msc** in te voeren in het dialoogvenster **Uitvoeren** en controleer of het certificaat **D365 Automated testing certificate** is gemaakt onder **Persoonlijk \> Certificaten**.

    > [!NOTE]
    > Voer **certlm.msc** in en niet **certmgr.msc**, aangezien de certificaten zijn opgeslagen op de lokale computer.

    ![Het certificaat D365 Automated testing certificate.](./media/setup_rsa_tool_46.png)

3. Klik met de rechtermuisknop op het certificaat en selecteer **Kopiëren**.
4. Ga naar **Vertrouwde basiscertificeringsinstanties \> Certificaten**.

    ![De map Certificaten onder de map Vertrouwde basiscertificeringsinstanties.](./media/setup_rsa_tool_47.png)

5. Selecteer in het menu **Actie** de optie **Plakken** om het certificaat naar de locatie **Vertrouwde basiscertificeringsinstanties** te kopiëren.

    ![De opdracht Plakken in het menu Actie.](./media/setup_rsa_tool_48.png)

6. Om de vingerafdruk van het geïnstalleerde certificaat op te halen, zonder spaties of speciale tekens, opent u een Windows PowerShell-venster als beheerder en voert u de volgende opdrachten uit.

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Sla de vingerafdruk op omdat u deze later nodig hebt wanneer u de WIF-bestanden voor AOS (Application Object Server) bijwerkt en de RSAT-configuratie instelt.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>De AOS-computer configureren om de verbinding te vertrouwen

> [!NOTE]
> Als de omgeving een Tier 2+-omgeving is, moet de vingerafdruk van het certificaat in het bestand wif.config worden bijgewerkt voor **alle** AOS-computers voor de omgeving.

1. Breng een RDP-verbinding (Remote Desktop Protocol) tot stand met de AOS-computer. Details voor aanmelden zijn beschikbaar op de pagina met omgevingsdetails in LCS.
2. Open Microsoft Internet Information Services (IIS) en vind **AOSService** in de lijst met sites.

    ![AOSService in de lijst met sites.](./media/setup_rsa_tool_49.png)

3. Klik met de rechtermuisknop op **Verkennen** om de map **\<Drive\>: \\AosService\\WebRoot** te openen. Zoek het bestand **wif.config**.

    ![Wif.config-bestand in de map WebRoot.](./media/setup_rsa_tool_50.png)

4. Werk het bestand **wif.config** bij door een nieuwe instantievermelding en -naam toe te voegen voor uw certificaat, zoals in het volgende voorbeeld.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Als meerdere gebruikers dezelfde toepassing gebruiken, moet iedere gebruiker afzonderlijke vingerafdrukken genereren en moeten alle vingerafdrukken worden toegevoegd aan de sectie **\<keys\>**.

5. Als er meer dan één AOS-computer is, herhaalt u stap 3 en 4 voor elke extra computer.

    > [!NOTE]
    > In tegenstelling tot oudere Tier 2-omgevingen worden nieuwe Tier 2-omgevingen geïmplementeerd met twee AOS-exemplaren.

6. Voer **iisreset** uit op alle AOS-computers.

    > [!NOTE]
    > Als u niet beschikt over beheerdersrechten om **iisreset** uit te voeren op een Tier 1-computer, selecteert u op de pagina Omgevingsdetails in LCS de optie Onderhouden > Services opnieuw starten.

#### <a name="tier-2-environment"></a>Tier 2+-omgeving

Als een Tier 2+-omgeving (standaardacceptatietest voor sandbox of hoger) wordt gebruikt, verifieert of configureert u de volgende registerinstelling op de computer waarop RSAT is geïnstalleerd. Deze stap is vereist omdat u zo verificatie- of RSAT-verbindingsfouten kunt voorkomen.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT installeren

1. Ga naar <https://www.microsoft.com/download/details.aspx?id=57357> en selecteer **Downloaden**.
2. Selecteer alle bestanden en vervolgens **Volgende**.

    ![Alle bestanden selecteren.](./media/setup_rsa_tool_51.png)

3. Dubbelklik op het MSI-pakket om het installatieprogramma uit te voeren. Nadat de installatie is voltooid, selecteert u **Voltooien**.

    ![RSAT-installatiebestand.](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Selenium- en browserstuurprogramma's installeren

In oudere versies van RSAT moest u Selenium- en browserstuurprogramma's installeren. U hoeft deze stuurprogramma's niet meer te installeren omdat deze automatisch worden geïnstalleerd.

1. De eerste keer dat u RSAT opent, wordt u gevraagd Selenium automatisch te downloaden en te installeren. Zie het gedeelte [RSAT configureren](#configure-rsat) voor meer informatie.
2. Voordat u een testcase kunt uitvoeren, wordt u gevraagd om automatisch het browserstuurprogramma te downloaden en te installeren dat hoort bij de standaardbrowser die is geselecteerd in de RSAT-configuratie. Zie het gedeelte [Testcases laden en uitvoeren](#load-and-run-test-cases) voor meer informatie.

## <a name="get-started-with-rsat"></a>Aan de slag met RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Een testplan en testsuites maken

1. Ga naar het Azure DevOps-project en selecteer **Testplannen**.

    ![De opdracht Testplannen.](./media/setup_rsa_tool_53.png)

2. Selecteer **Nieuw testplan**.

    ![De knop Nieuw testplan.](./media/setup_rsa_tool_54.png)

3. Vul het veld **Naam** in en selecteer **Maken**. Geef het testplan voor deze zelfstudie de naam **RSAT-testplan**.

    ![Het dialoogvenster Nieuw testplan.](./media/setup_rsa_tool_55.png)

4. Selecteer het plusteken (**+**) en selecteer **Statische suite** om een statische suite te maken onder het nieuwe testplan. Geef de nieuwe testsuite de naam **T01 – Maken naar voorraad**.

    > [!NOTE]
    > U kunt ook een suite op basis van query's maken, als u wilt dat de nieuwe testcases vanuit BPM automatisch in de RSAT-testsuite worden opgenomen.

    ![Een statische suite maken.](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Testcases koppelen aan testsuites

1. Selecteer **Bestaande toevoegen** rechts om bestaande testcases toe te voegen aan de testsuite.

    ![De knop Bestaande toevoegen.](./media/setup_rsa_tool_57.png)

2. Selecteer op de pagina **Testcases toevoegen aan suite** de optie **Query uitvoeren** en selecteer de testcase die u wilt toevoegen aan de testsuite. Selecteer voor deze zelfstudie de testcase **Een nieuw product maken**. Selecteer **Testcases toevoegen** in de rechterbenedenhoek van de pagina (deze knop wordt niet weergegeven in de volgende afbeelding).

    ![De knop Query uitvoeren.](./media/setup_rsa_tool_58.png)

    De testcase wordt toegevoegd aan de testsuite **T01-Maken naar voorraad**.

    ![Testcase toegevoegd aan de testsuite.](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>RSAT configureren

1. Open RSAT.

    ![RSAT-pictogram.](./media/setup_rsa_tool_60.png)

2. Er wordt een waarschuwingsbericht weergegeven dat Selenium vereist is voor Regression Suite Automation Tool en u wordt gevraagd of u Selenium automatisch wilt downloaden en installeren. Selecteer **Ja**.

    ![Waarschuwingsbericht dat voor Regression Suite Automation Tool Selenium is vereist.](./media/setup_rsa_tool_61.png)

3. Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en vul in het dialoogvenster dat wordt weergegeven de volgende velden in:

    - **Azure DevOps Url** – Voer de URL van uw Azure DevOps-project in, bijvoorbeeld `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Toegangstoken** – Voer de toegangstoken in op basis waarvan door het hulpprogramma verbinding kan orden gemaakt met Azure DevOps. Gebruik de persoonlijke toegangstoken die u eerder in deze zelfstudie hebt gemaakt. Zie [Toegang verifiëren met persoonlijke toegangstokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) voor meer informatie.
    - **Projectnaam**: selecteer de naam van uw Azure DevOps-project.
    - **Testplan**: selecteer het Azure DevOps-testplan dat uw testcases bevat. Zie [Testplannen en testsuites maken](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) voor meer informatie. Nadat u een testplan hebt geselecteerd, selecteert u **Verbinding testen** om de verbinding met Azure DevOps te testen.
    - **Hostnaam**: voer de hostnaam in van de testomgeving, zoals **\<myaos\>.cloudax.dynamics.com**. Neem het voorvoegsel **https://** of **http://** niet op.
    - **SOAP-hostnaam**: voer de naam van de SOAP-host van de testomgeving in. Meestal komt de SOAP-hostnaam overeen met de hostnaam, maar heeft deze het achtervoegsel **soap**. Hier is een voorbeeld: **\<myaos\>soap.cloudax.dynamics.com**. Neem het voorvoegsel **https://** of **http://** niet op.

        > [!NOTE]
        > Als u de hostnaam en de SOAP-hostnaam wilt vinden, opent u IIS Manager, klikt u met de rechtermuisknop op **Sites \> AOSService** en selecteert u **Bindingen bewerken**. De kolom **Hostnaam** bevat de hostnaam en SOAP-hostnaam (de SOAP-hostnaam bevat het achtervoegsel **soap** in de URL).

        ![Hostnaam en SOAP-hostnaam in de kolom Hostnaam.](./media/setup_rsa_tool_63.png)

    - **Gebruikersnaam beheerder**: voer het e-mailadres van een beheerder in de testomgeving in.
    - **Vingerafdruk**: voer de vingerafdruk van het verificatiecertificaat in, zoals eerder in deze zelfstudie wordt beschreven.
    - **Werkmap**: geef de maplocatie voor het opslaan van testautomatiseringsbestanden op, zoals Excel-testgegevensbestanden. U kunt bijvoorbeeld **C:\\Temp\\RegressionTool** invoeren of selecteren.

        > [!NOTE]
        > Als de naam van de map spaties bevat, mislukt de uitvoering omdat de map in dat geval niet wordt gevonden. Dit is een bekend probleem dat moet worden opgelost in de nieuwste versie van het hulpprogramma.

    - **Standaardbrowser**: selecteer **Internet Explorer** of **Google Chrome**. Zorg dat de juiste browserstuurprogramma's zijn geïnstalleerd.
    - **Time-out testuitvoering**: geef de time-outperiode in minuten op voor testuitvoeringen. Wanneer de time-outperiode is verstreken, worden alle actieve vensters gesloten en mislukken lopende testcases.
    - **Time-out van testactie**: in dit veld wordt de time-outperiode in minuten voor serveraanvragen in de Finance and Operation-omgeving beheerd. Meestal volstaat de standaardwaarde (2 minuten). Voor langzamere omgevingen kunt u echter de waarde verhogen als er fouten optreden die betrekking hebben op time-outs.
    - **Bedrijfsnaam**: voer de bedrijfsnaam in die moet worden gebruikt als uw standaardbedrijf wanneer Excel-parameterbestanden worden gemaakt. U kunt het bedrijf later wijzigen door het Excel-parameterbestand te bewerken.

    ![Het dialoogvenster Instellingen.](./media/setup_rsa_tool_62.png)

4. Selecteer **Toepassen** om de instellingen toe te passen en op te slaan.

    Als u de huidige instellingen wilt opslaan in een configuratiebestand op uw computer, selecteert u **Opslaan als**. Als u uw huidige instellingen wilt herstellen op basis van een configuratiebestand op uw computer, selecteert u **Openen**.

5. Selecteer **Sluiten** om het dialoogvenster te sluiten.

### <a name="load-and-run-test-cases"></a>Testcases laden en uitvoeren

1. Selecteer **Laden** om het **RSAT-testplan** te laden vanuit het Azure DevOps-project.

    ![De knop Laden.](./media/setup_rsa_tool_64.png)

2. Selecteer de testcase **Een nieuw product laden** vanuit de testsuite en selecteer vervolgens **Nieuw \> Testuitvoering en parameterbestanden genereren**.

    ![De opdracht Testuitvoering en parameterbestanden genereren in het menu Nieuw.](./media/setup_rsa_tool_65.png)

    Het Excel-parameterbestand wordt gemaakt in de lokale map die u hebt opgegeven in de RSAT-configuratie (bijvoorbeeld **C:\\Temp\\RegressionTool**).

    ![Het gemaakte Excel-parameterbestand.](./media/setup_rsa_tool_66.png)

3. Selecteer **Uploaden** als u de parameterbestanden wilt opslaan. Testautomatiseringsbestanden van alle geselecteerde testcases worden voor toekomstig gebruik naar Azure DevOps geüpload. (Deze bestanden omvatten Excel-testparameterbestanden.)

    Op deze manier kunt u **Laden** selecteren om de parameterbestanden (en automatiseringsbestanden) van de testcase direct vanuit Azure DevOps te laden. U hoeft de parameterbestanden niet opnieuw te genereren. Deze benadering wordt later belangrijk, wanneer u de wijzigingen in het parameterbestand wilt behouden en niet wilt dat ze worden overschreven.

4. Als u wilt controleren of de automatiseringsbestanden en parameterbestanden in Azure DevOps zijn opgeslagen, gaat u naar het Azure DevOps-project, selecteert u **Borden \> WerkItems** en selecteert u vervolgens **Een nieuw product maken** . Op het tabblad **Bijlagen** ziet u vier bestanden:

    - **.cs** – C\#-automatiseringsbestand
    - **.dll** – Gecompileerd automatiseringsbestand als een assembly
    - **.xlsx** – Excel-parameterbestand
    - **.xml** – Registratiebestand

    ![Bestanden op het tabblad Bijlagen.](./media/setup_rsa_tool_67.png)

5. Selecteer de testcase die u wilt uitvoeren en selecteer **Uitvoeren**.

    > [!NOTE]
    > Als u Internet Explorer gebruikt, moet u er voordat u testcases uitvoert voor zorgen dat de bureaubladresolutie is ingesteld op **100%** in **Windows-beeldscherminstellingen \> Schaal en lay-out**. Als u deze instelling niet kunt wijzigen op een virtuele machine (VM), wijzigt u deze op de client (laptop) waarvan u de VM wilt openen. De resolutie-instellingen worden vervolgens overgenomen door de beeldscherminstellingen van de VM.

    ![Bureaubladresolutie ingesteld op 100%.](./media/setup_rsa_tool_68.png)

6. Als de browserstuurprogramma's niet op het systeem zijn geïnstalleerd, wordt er een waarschuwingsbericht weergegeven dat u voor deze bewerking stuurprogramma \<browser name\> nodig hebt. Daarnaast wordt u gevraagd of u het automatisch nu wilt downloaden en installeren? Selecteer **Ja**.

    ![Waarschuwingsbericht voor Internet Explorer.](./media/setup_rsa_tool_69.png)

    ![Waarschuwingsbericht voor Chrome.](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Als u Chrome als browser gebruikt en er een foutbericht wordt weergegeven waarin wordt aangegeven dat de sessie niet is gemaakt omdat de Chrome-versie niet juist is, downloadt u de meest recente versie van <http://chromedriver.chromium.org/downloads> naar de map **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.

    ![Foutbericht voor Chrome.](./media/setup_rsa_tool_71.png)

    De testcase wordt uitgevoerd en het veld **Resultaat** wordt bijgewerkt.

    ![Bijgewerkt resultaatveld.](./media/setup_rsa_tool_72.png)

    Als u deze zelfstudie hebt gevolgd zoals deze is geschreven, mislukt de testcase **Een nieuw product maken** omdat met de taakregistratie voor het maken van een product de productnaam is opgeslagen als een hard gecodeerde waarde. Als u dezelfde testcase opnieuw uitvoert, wordt er een foutbericht weergegeven omdat het product al bestaat.

    ![Het veld Resultaat ingesteld op Mislukt.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>De testresultaten weergeven

1. Dubbelklik op de mislukte testcase.

    U ontvangt een foutbericht.

    ![Foutmelding.](./media/setup_rsa_tool_73.png)

2. Selecteer **Details** om het volledige foutbericht weer te geven.

    ![Volledige foutbericht.](./media/setup_rsa_tool_74.png)

3. Als u een gedetailleerde versie van het fout bericht in Azure DevOps wilt weergeven, selecteert u **Openen in Azure DevOps**. In Azure DevOps kunt u de status van de testcase en het gedetailleerde foutbericht bekijken.

    ![Gedetailleerd foutbericht in Azure DevOps.](./media/setup_rsa_tool_75.png)

4. Als u de testresultaten rechtstreeks in het Azure DevOps-project wilt weergeven, gaat u naar **Testplannen \> Testplannen \> Uitvoeringen**. Dubbelklik op de testuitvoering waarover u meer details wilt weergeven.

    ![Lijst met testuitvoeringen in Azure DevOps.](./media/setup_rsa_tool_76.png)

5. Op het tabblad **Uitvoeringsoverzicht** wordt aangegeven dat de testcase is mislukt, maar het werkelijke foutbericht wordt niet weergegeven. Als u het gedetailleerde foutbericht wilt weergeven, selecteert u het tabblad **Testresultaten**.

    ![Het tabblad Uitvoeringsoverzicht.](./media/setup_rsa_tool_77.png)

    Het tabblad **Testresultaten** bevat informatie over de testcase, het resultaat en het foutbericht.

    ![Het tabblad Testresultaten.](./media/setup_rsa_tool_78.png)

6. Dubbelklik op de relevante record om het gedetailleerde foutbericht weer te geven.

    ![Gedetailleerd foutbericht.](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Alle foutberichten zijn ook lokaal beschikbaar in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. U kunt de resultaten van de testuitvoering ook exporteren vanuit het niveau van het testplan door **Exporteren** te selecteren.

    ![Een testplan exporteren.](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Het Excel-parameterbestand wijzigen

1. Open RSAT.
2. Selecteer de testcase en selecteer vervolgens **Bewerken** om het Excel-parameterbestand te openen.

    In het blad **EcoResProductCreate** is de waarde van het veld **Productnummer** hard gecodeerd. U moet dit veld bijwerken naar een nieuw productnummer voordat u de testcase opnieuw uitvoert.

3. Als u een uniek productnummer voor elke uitvoering wilt genereren zonder elke keer het Excel-parameterbestand opnieuw te hoeven openen en het productnummer handmatig te hoeven bijwerken, gebruikt u de volgende Excel-formule.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Naast het tabblad **Algemeen** bevat het Excel-parameterbestand een gegevenstabblad voor elke formulierpagina die de testcase bezoekt.

    ![Het veld Productnummer.](./media/setup_rsa_tool_81.png)

4. Selecteer **Opslaan** en sluit de Excel-werkmap.
5. Selecteer **Uploaden** om het Excel-parameterbestand naar Azure DevOps op te slaan.

    ![Bericht over geslaagde upload.](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Als u testcases in een specifieke gebruikerscontext wilt uitvoeren, typt u de e-mail-id van de gebruiker in het veld **Gebruiker testen** op het tabblad **Algemeen** van het Excel-parameterbestand. In de meest recente versie van RSAT is de indeling van de velden in het Excel-parameterbestand bijgewerkt, maar het concept blijft hetzelfde.
    >
    > ![Het veld Gebruiker testen.](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>De resultaten valideren

- Selecteer **Uitvoeren** om de testcase opnieuw uit te voeren en controleer of de testcase is geslaagd. U kunt de testresultaten weergeven op de wijze die wordt beschreven in de sectie [De testresultaten weergeven](#view-the-test-results).

    ![Het veld Resultaat ingesteld op Geslaagd.](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Koppelen van testcases

Eén belangrijke functie van RSAT is dat testcases kunnen worden aaneengeschakeld (waarden kunnen worden doorgegeven aan andere tests). Testcases worden uitgevoerd volgens de gedefinieerde volgorde in het Azure DevOps-testplan. (Deze volgorde kan ook worden bijgewerkt in het testprogramma zelf.) Als u variabelen wilt doorgeven van de ene testcase naar de andere, is het daarom zeer belangrijk dat de tests de juiste volgorde hebben.

In deze sectie maakt u een opgeslagen variabele in de eerste testcase, maakt u een tweede testcase en geeft u de opgeslagen variabele uit de eerste testcase door aan de tweede testcase. Vervolgens voert u de testcases uit als een aangeschakelde testcase in RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Een bestaande taakregistratie wijzigen om een opgeslagen variabele te maken

1. Open de client.
2. Selecteer de knop **Instellingen** (het tandwielsymbool) en selecteer **Taakregistratie**.
3. Selecteer **Opname bewerken**.

    ![De knop Opname bewerken.](./media/setup_rsa_tool_85.png)

4. Selecteer **Openen vanuit Lifecycle Services**.

    ![De knop Openen vanuit Lifecycle Services.](./media/setup_rsa_tool_86.png)

5. Selecteer **Selecteer de Lifecycle Services-bibliotheek**.

    ![De knop Selecteer de Lifecycle Services-bibliotheek.](./media/setup_rsa_tool_87.png)

    BPM-bibliotheken worden geladen uit LCS.

    ![BPM-bibliotheken laden.](./media/setup_rsa_tool_88.png)

6. Nadat de BPM-bibliotheken vanuit LCS zijn geladen, selecteert u de BPM-bibliotheek **RSAT** en het bedrijfsproces **Een nieuw product maken** waaraan de taakregistratie is gekoppeld. Selecteer vervolgens **OK**.

    ![Een BMP-bibliotheek en een bedrijfsproces selecteren.](./media/setup_rsa_tool_89.png)

7. De naam van de betreffende taakregistratie wordt ingevoerd in het veld **Naam van registratie**. Selecteer **Starten**.

    ![Naam van de taakregistratie in het veld Naam van registratie.](./media/setup_rsa_tool_90.png)

8. Ga naar **Productgegevensbeheer \> Producten** en selecteer **Nieuw** om de pagina te openen waarop de oorspronkelijke taakregistratie **Een product maken** is geregistreerd.
9. Selecteer **Stap invoegen**.

    > [!NOTE]
    > De nieuwe stap wordt ingevoegd **na** de stap die u in het deelvenster hebt geselecteerd.

    ![De knop Stap invoegen.](./media/setup_rsa_tool_91.png)

10. Klik met de rechtermuisknop in het veld **Productnummer** en selecteer vervolgens **Taakregistratie \> Kopiëren**.

    ![De opdracht Kopiëren.](./media/setup_rsa_tool_92.png)

11. Er wordt een nieuwe stap toegevoegd in het deelvenster. Noteer de waarde in het veld **Productnummer**. U hebt deze later nog nodig.

    ![Nieuwe stap toegevoegd.](./media/setup_rsa_tool_93.png)

12. Selecteer **Klaar met bewerken**.
13. Selecteer **Opslaan in Lifecycle Services** en koppel de nieuwe taakregistratie aan dezelfde BPM-bibliotheek en hetzelfde bedrijfsproces als de oorspronkelijke taakregistratie. Zie de sectie [Een taakregistratie maken en opslaan in de BPM-bibliotheek](#create-a-task-recording-and-save-it-to-the-bpm-library) voor meer informatie.
14. Ga naar de BPM-bibliotheek en selecteer **Testcases synchroniseren** om de taakregistratie te overschrijven die aan de testcase is gekoppeld in Azure DevOps, zoals wordt beschreven in [De synchronisatie van BPM naar Azure DevOps testen](#test-the-synchronization-from-bpm-to-azure-devops).
15. Open RSAT en selecteer **Laden** om alle testcases opnieuw in de testsuite te laden. U moet de automatiserings- en parameterbestanden voor de betreffende testcase opnieuw genereren door de testcase te selecteren en vervolgens **Nieuw \> Testuitvoering en parameterbestanden genereren** te selecteren, zoals wordt beschreven in de [Testcases laden en uitvoeren](#load-and-run-test-cases).

    > [!NOTE]
    > Als het Excel-parameter bestand geopend was, mislukt de nieuwe generatie. Zorg er daarom voor dat het Excel-parameterbestand voor de testcase is gesloten voordat u het nieuwe Excel-parameterbestand genereert.

16. Selecteer **Bewerken** om het nieuwe Excel-parameterbestand te openen. De nieuwe invoer **Opgeslagen variabele** wordt weergegeven op regel 9. Deze variabele, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, wordt opgeslagen in het XML-bestand van de taakregistratie en kan in volgende tests worden gebruikt.

    ![Het item Opgeslagen variabele.](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Een nieuwe testcase maken

1. Ga naar de BPM-bibliotheek **RSAT**.
2. Selecteer het proces **Sample Support Business Process** en selecteer vervolgens **Edit mode** rechts.
3. Wijzig de waarde van de velden **Name** en **Description** in **Een product vrijgeven**. Selecteer **Save**.

    ![Naam en omschrijving gewijzigd in Een product vrijgeven.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Een nieuwe taakregistratie maken met een functie Valideren

- Maak een taakregistratie om het eerder gemaakte product vrij te geven aan de rechtspersoon USRT. Zie de sectie [Een taakregistratie maken en opslaan in de BPM-bibliotheek](#create-a-task-recording-and-save-it-to-the-bpm-library) voor meer informatie.

    > [!NOTE]
    > Voor aangeschakelde testcases raden wij u aan altijd de benodigde record te zoeken of te filteren door de *waarde van het veld handmatig in te voeren*. Op die manier kan worden bepaald voor welke record de actie moet worden uitgevoerd in de volgende testcase.

    ![Nieuwe taakregistratie met een functie Valideren.](./media/setup_rsa_tool_96.png)

    Zoals u in de vorige afbeelding kunt zien, kunt u, nadat u het product hebt gevonden met het snelfilter, voordat u **Producten vrijgeven** selecteert de waarde van het veld **Productnummer** valideren om er zeker van te zijn dat de product-id de product-id is die u eerder hebt gemaakt. Als u de waarde wilt valideren, klikt u met de rechtermuisknop in het veld **Productnummer** en selecteert u **Taakregistratie \> Valideren \> Huidige waarde**.

    ![De huidige waarde valideren.](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>De taakregistratie opslaan in BPM

1. Als de taakregistratie is voltooid, selecteert u **Opslaan in Lifecycle Services**.

    ![Voltooide taakregistratie opslaan in Lifecycle Services.](./media/setup_rsa_tool_98.png)

2. Bibliotheekgegevens worden vanuit LCS geladen.

    ![Bibliotheekgegevens laden vanuit LCS.](./media/setup_rsa_tool_99.png)

3. Selecteer de BPM-bibliotheek waaraan u de taakregistratie wilt koppelen. Selecteer voor deze zelfstudie de BPM-bibliotheek **RSAT** die eerder is gemaakt en het bedrijfsproces **Een product vrijgeven** daaronder. Selecteer vervolgens **OK**.

#### <a name="sync-bpm-to-azure-devops"></a>BPM synchroniseren naar Azure DevOps

1. Ga naar de BPM-bibliotheek en open de bibliotheek **RSAT**.
2. Selecteer **VSTS synchroniseren** en vervolgens **Testcases synchroniseren**. Zie de sectie [De synchronisatie van BPM naar Azure DevOps testen](#test-the-synchronization-from-bpm-to-azure-devops) voor meer informatie.

    Als de synchronisatie is voltooid, worden het nieuwe werkitem en de bijbehorende testcase voor het bedrijfsproces **Een product vrijgeven** weergegeven in Azure DevOps in **Borden \> Werkitems**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>De nieuwe testcase toevoegen aan de bestaande testsuite

1. Ga naar **Testplannen \> Testplannen** en selecteer het plan **RSAT-testplan**.
2. Selecteer **Bestaande toevoegen**.
3. Selecteer **Query uitvoeren** op de pagina **Testcases toevoegen aan suite**.
4. Selecteer de nieuwe testcase die voor **Een product vrijgeven** is gemaakt en selecteer vervolgens **Testcases toevoegen** in de rechterbenedenhoek van de pagina (deze knop wordt niet weergegeven in de volgende afbeelding).

    ![De pagina Testcases toevoegen aan suite.](./media/setup_rsa_tool_100.png)

    De testsuite bevat nu twee testcases.

    ![Twee testcases in de testsuite.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Testcases in RSAT laden

1. Open RSAT en selecteer **Laden**.
2. De testcases worden geladen en er wordt een waarschuwing weergegeven om aan te geven dat de actie Excel-testgegevensbestanden overschrijft en lokale wijzigingen verloren gaan. Daarnaast wordt gevraagd of u wilt doorgaan. Selecteer **Ja** als u de Excel-parameterbestanden wilt bijwerken in het lokale systeem, maar niet de Excel-parameterbestanden die zijn geüpload naar Azure DevOps.

    ![Met deze actie worden Excel-testgegevensbestanden overschreven.](./media/setup_rsa_tool_102.png)

    Beide testcases worden geladen, samen met het Excel-parameterbestand voor de eerste testcase. Omdat u **Uploaden** hebt geselecteerd bij de laatste uitvoering, worden de parameterbestanden opgehaald uit Azure DevOps.

    ![Testcases geladen.](./media/setup_rsa_tool_103.png)

3. Selecteer alleen de tweede testcase en selecteer vervolgens **Nieuw \> Testuitvoering en parameterbestanden genereren**.

#### <a name="edit-the-excel-parameter-file"></a>Het Excel-parameterbestand bewerken

1. Selecteer alleen de tweede testcase en selecteer vervolgens **Bewerken** om het bijbehorende Excel-parameterbestand te openen.
2. Kopieer de opgeslagen variabele **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (zie de sectie [Een bestaande taakregistratie wijzigen om een opgeslagen variabele te maken](#modify-an-existing-task-recording-to-create-a-saved-variable)) uit de eerste testcase in alle velden waarin het productnummer wordt gebruikt. In dit geval kopieert u de variabele naar de velden **Productnummer** en **Productnummer valideren** op het blad **EcoResproductListPage**.

    ![De velden Productnummer en Productnummer valideren.](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Variabelen kunnen alleen tijdens dezelfde testuitvoering worden doorgegeven tussen tests. De namen van de variabelen moeten exact overeenkomen.

3. Selecteer **Opslaan** en sluit de Excel-werkmap.
4. Selecteer **Uploaden** om de wijzigingen op te slaan die u in het Excel-parameterbestand hebt aangebracht.

#### <a name="run-the-chained-test-cases"></a>De aaneengeschakelde testcases uitvoeren

1. Selecteer beide testcases die u wilt uitvoeren en selecteer **Uitvoeren**.
2. Controleer of de testcases zijn geslaagd.

    ![Het veld Resultaat ingesteld op Geslaagd voor beide testcases.](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]