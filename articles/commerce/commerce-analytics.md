---
title: Commerce-analyses (preview)
description: In dit onderwerp wordt uitgelegd hoe u de analysemogelijkheden installeert en gebruikt in Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862768"
---
# <a name="commerce-analytics-preview"></a>Commerce-analyses (preview)

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Commerce-analyses (preview) installeert. Dit is de functionele analysemogelijkheid die deel uitmaakt van Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Live demo van Commerce-analyses (preview)

U kunt een [live demo van Commerce-analyses (preview)](https://aka.ms/CommerceAnalyticsDemo) uitproberen.

![Overzicht van Commerce-analyses (preview)](media/CommerceAnalytics_Summary.png)
![Betalingen in Commerce-analyses (preview)](media/CommerceAnalytics_Payments.png)
![Webactiviteit in Commerce-analyses (preview)](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Systeemarchitectuur van Commerce-analyses (preview)

### <a name="key-components"></a>Belangrijke onderdelen

Commerce-analyses (preview) bestaat uit de volgende belangrijke onderdelen:

- Gebruiksklare interactieve Power BI-rapporten
- SQL-weergaven in Azure Synapse Analytics
- Entiteits- en ontologiegegevens in Azure Data Lake
- Onbewerkte gegevens in Data Lake

![Belangrijke onderdelen van de systeemarchitectuur van Commerce-analyses](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Gegevensstroom

#### <a name="step-1-data-generation"></a>Stap 1: Gegevens genereren

Gegevens bestaan uit transactionele gegevens of gedragsgegevens uit een van de volgende bronnen:

- Een callcentermedewerker gebruikt de Commerce HQ-client om verkooporders te verwerken.
- Een kassamedewerker op het POS (Point of Sale) verwerkt verkooptransacties.
- Verkopen worden in aangepaste toepassingen gemaakt met headless commerce (Commerce Scale Unit).
- Een klant van een e-commercebedrijf grasduint op uw e-commercewebsite.
- Een klant van een e-commercebedrijf plaatst een order op uw e-commercewebsite.
- Gegevens worden geproduceerd door andere systemen, zoals Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Stap 2: Opnemen en voorverwerken

Transactionele gegevens gaan rechtstreeks naar Commerce HQ (voor orders die rechtstreeks worden vastgelegd in de Commerce HQ-client) of via Commerce Scale Unit (in geval van orders die op het POS worden vastgelegd, in e-commerce of in aangepaste clients die headless commerce gebruiken).

De functie Exporteren naar Data Lake wordt vervolgens gebruikt om de transactionele gegevens naar uw gegevens te kopiëren als onbewerkte gegevens. In het data lake worden de onbewerkte gegevens opgeslagen in de map Tabellen.

De gegevens van webactiviteiten voor e-commerce worden rechtstreeks naar het data lake verzonden. Gegevens die door andere systemen worden geproduceerd, zoals Dynamics 365 Connected Spaces, worden rechtstreeks door die systemen naar het data lake verzonden.

#### <a name="step-3-transformation-and-aggregation"></a>Stap 3: Transformeren en samenvoegen

Wanneer onbewerkte gegevens in uw data lake zijn opgenomen, worden deze gelezen door de service Commerce-analyses, getransformeerd, verzameld en teruggeschreven naar het data lake in de vorm van logische entiteiten (in de map Entities) en samengevoegde metrische gegevens (in de map Ontologies).

#### <a name="step-4-querying"></a>Stap 4: Query's uitvoeren

Azure Synapse Analytics wordt gebruikt om query's uit te voeren op gegevens in uw data lake via een T-SQL-interface (Transact-SQL). Deze interface bevat SQL-weergaven. SQL-weergaven maken het mogelijk om rechtstreeks gefedereerde query's uit te voeren op gegevens in het data lake, via een T-SQL-client (voor ad-hocanalyse) of via een visualisatieprogramma, zoals Power BI.

#### <a name="step-5-modeling-and-serving"></a>Stap 5: Modelleren en presenteren

Gegevens waarop query's zijn uitgevoerd door Azure Synapse Analytics gaan naar het semantische model van Power BI. Afhankelijk van het type gegevens worden deze periodiek in het geheugen geïmporteerd in Power BI of rechtstreeks opgevraagd tijdens runtime.

Ten slotte worden de gegevens weergegeven in Power BI-visuals, zodat gebruikers deze kunnen bekijken en er interacties mee kunnen aangaan.

## <a name="commerce-analytics-preview-functional-overview"></a>Functioneel overzicht van Commerce-analyses (preview)

### <a name="summary"></a>Samenvatting

De sjabloon voor de app Commerce-analyses bevat de volgende hoofdrapportpagina's:

1. [Filters op het hoogste niveau](#TopLevelFilters)
2. [Producten](#ProductsPage)
3. [Klanten](#CustomersPage)
4. [Kanalen](#ChannelsPage)
5. [Verkoop](#SalesPage)
6. [Marges](#MarginsPage)
7. [Retouren](#ReturnsPage)
8. [Kortingen](#DiscountsPage)
9. [Betalingen](#PaymentsPage)
10. [Klanten](#CustomersPage)
11. [Vergelijking](#ComparisonPage)
12. [Webactiviteit](#WebActivityPage)
13. [Webactiviteit - Filter op het hoogste niveau](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filters op het hoogste niveau

- Gegevensinstellingen

    - Jaar
    - Kwartaal
    - Maand
    - Week
    - Dag

- Afzetkanaalinstellingen

    - Rechtspersoon
    - Kanaaltype
    - Klanttype
    - Verkooptype
    - Kanaal
    - Organisatiehiërarchie

- Productinstellingen

    - Categoriehiërarchie
    - Categorie

####  <a name="products"></a><a name="ProductsPage"></a> Producten

- Verkoop
- Marge
- Retouren

####  <a name="customers"></a><a name="CustomersPage"></a> Klanten

- Verkoop
- Marge
- Retouren

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanalen

- Verkoop
- Marge
- Retouren

### <a name="sales"></a>Verkoop <a name="SalesPage"></a>

- Per afleverlocatie
- Per kanaal/winkel/terminal
- Per werknemer
- Per datum
- Per uur
- Per productcategorie

### <a name="margins"></a><a name="MarginsPage"></a> Marges

- Per afleverlocatie
- Per product
- Per datum

### <a name="returns"></a><a name="ReturnsPage"></a> Retouren

- Per geretourneerd bedrag

    - Per winkel
    - Per product
    - Per datum

- Per retourtransactie

    - Per winkel
    - Per product
    - Per datum

### <a name="discounts"></a><a name="DiscountsPage"></a> Kortingen

- Per winkel
- Per product
- Per datum
- Ontleding

    - Rechtspersoon
    - Winkel
    - Kortingstype
    - Kortingsnaam
    - Product

### <a name="payments"></a><a name="PaymentsPage"></a> Betalingen

- Per kanaal/terminal
- Per betalingsmethode/-type
- Per datum
- Ontleding

    - Rechtspersoon
    - Kanaaltype
    - Winkel
    - Terminal
    - Betaalwijze

### <a name="customers"></a><a name="CustomersPage"></a> Klanten

- Levensduurwaarde (LDW)

    De LDW wordt berekend op basis van het totale bedrag dat een klant uitgeeft via alle Dynamics 365 Commerce-verkoopkanalen (waaronder POS, e-commerce en callcenter).

- Recency

    De recency wordt berekend op basis van het aantal dagen sinds het laatste transactiecontact van een klant met de organisatie. Er wordt bij recency momenteel geen rekening gehouden met niet-transactionele contactsignalen, zoals browseactiviteiten via e-commerce.

- Frequentie

    Frequentie wordt berekend op basis van het transactiecontact van een klant met de organisatie. Er wordt bij frequentie momenteel geen rekening gehouden met niet-transactionele contactsignalen, zoals browseactiviteiten via e-commerce.

- Relatieduur

    De relatieduur wordt berekend op basis van het aantal dagen sinds de klantrecord is gemaakt in het systeem.

- Aantal transacties

### <a name="comparison"></a><a name="ComparisonPage"></a> Vergelijking

- Productvergelijking per tijdsperiode

    - Verkoop en verkoopverschil
    - Marge en margeverschil

- Klanten per tijdsperiode

    - Verkoop en verkoopverschil
    - Marge en margeverschil

### <a name="web-activity"></a><a name="WebActivityPage"></a> Webactiviteit

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Filters op het hoogste niveau

- Datumbereik
- Kanaaltype
- Kanaal
- Categoriehiërarchie

#### <a name="acquisitions"></a>Verwervingen

- Paginaweergaven

    - Per land of regio
    - Bijproduct
    - Per aanmeldingsstatus gebruiker
    - Per datum

- E-commerce-orders
- Conversiepercentage

    - Per datum

- Conversietrechter

    - Paginaweergave per paginatype (startpagina, categoriepagina of productdetailpagina)
    - Toevoegen aan winkelwagen
    - Betaling
    - Aankoop

#### <a name="sessions"></a>Sessies

Een sessie is een episode van een bezoek van een gebruiker aan uw e-commercewebsite. Een sessie wordt als beëindigd beschouwd na 30 minuten inactiviteit of 24 uur actief gebruik.

- Per land of regio
- Per oorsprong (externe verwijzer)
- Per aanmeldingsstatus gebruiker
- Aantal sessies

    - Per datum
    - Per pagina voor gegevensinvoer

- Order per sessie

    - Per datum

- Bouncepercentage voor sessies

    Een sessiebounce is een sessie waarbij een gebruiker direct vertrekt nadat hij of zij uw e-commercewebsite heeft bezocht. Zie [Bouncepercentage](https://en.wikipedia.org/wiki/Bounce_rate) voor meer informatie.

- Klikken per sessie

#### <a name="visitors"></a>Bezoekers

Een anonieme bezoeker van uw e-commercesite wordt uniek geïdentificeerd op basis van de specifieke browser en het specifieke apparaat dat de gebruiker gebruikt. Commerce-analyses houden geen anonieme analyses bij voor verschillende browsers of apparaten. Een anonieme bezoeker die dezelfde browser gebruikt voor hetzelfde apparaat wordt uniek geïdentificeerd in meerdere gebruikerssessies, totdat de gegevens in de cache van de browser zijn gewist of een periode (meestal 12 maanden) is verstreken, afhankelijk van wat zich het eerst voordoet.

Als bezoekers grasduinen op uw e-commercesite terwijl ze zijn aangemeld, kan Commerce-analyses extra informatie over hen leveren. Deze informatie is gebaseerd op de bestaande relatie die uw organisatie heeft met de bezoekers als gevolg van hun eerdere aankopen in alle Dynamics 365 Commerce-verkoopkanalen (waaronder POS, e-commerce en callcenter). De extra informatie omvat gegevens over recency, relatieduur, levensduurwaarde en frequentie.

- Marge van bezoeker
- Gemiddelde orders van bezoeker
- Gemiddelde verkoop van bezoeker
- Aantal bezoekers e-commerce

    - Per datum
    - Per locatie

        Momenteel kan Commerce-analyses alleen granulariteit op land-/regioniveau bieden voor locatie-inzichten voor e-commercebezoekers.

    - Per recency

        De recency wordt berekend op basis van het aantal dagen sinds het laatste transactiecontact van een klant met de organisatie. Er wordt bij recency momenteel geen rekening gehouden met niet-transactionele contactsignalen, zoals browseactiviteiten via e-commerce.

    - Per relatieduur

        De relatieduur wordt berekend op basis van het aantal dagen sinds de klantrecord is gemaakt in het systeem.

    - Per levensduurwaarde (LDW)

        De LDW wordt berekend op basis van het totale bedrag dat een klant uitgeeft via alle Dynamics 365 Commerce-verkoopkanalen (waaronder POS, e-commerce en callcenter).

    - Per frequentie

        Frequentie wordt berekend op basis van het transactiecontact van een klant met de organisatie. Er wordt bij frequentie momenteel geen rekening gehouden met niet-transactionele contactsignalen, zoals browseactiviteiten via e-commerce.

#### <a name="impressions"></a>Impressies

Een impressie is een enkele weergave van een productvisual door een e-commercebezoeker. Een e-commercebezoeker gaat bijvoorbeeld naar de startpagina van uw e-commercewebsite en bekijkt een yogamat als product in een lijstmodule **Best verkocht**. De bezoeker bekijkt vervolgens dezelfde yogamat in een lijstmodule **Selectie voor u**. In dit geval zijn er twee productimpressies. 

Momenteel worden impressies bijgehouden in de volgende onderdelen:

- Lijsten (bijvoorbeeld **Aanbevolen**, **Best verkocht**, **Selectie voor u** en **Trending**)
- Winkelwagenmodule
- Zoekresultaatcontainer
- Categorie zoekresultaatcontainer

Momenteel worden producten die worden weergegeven in een carrouselmodule of in aangepaste visuals niet meegeteld in aan impressies gerelateerde metrische gegevens.

De pagina **Impressierapport** bevat de volgende metrische gegevens:

- Aantal impressies

    - Per paginatype en module

        Het paginatype is het algemene type pagina dat voor elke pagina op uw e-commercewebsite is gedefinieerd. Het moduletype is het type visuele module voor e-commerce waarin het product wordt weergegeven.

        Voor het bekijken van impressies per module moet u mogelijk inzoomen op de pagina- en modulevisuals.

    - Per product
    - Per aanmeldingsstatus gebruiker
    - Per datum

- Aantal impressieklikken

    Een impressieklik vindt plaats wanneer een e-commercebezoeker een productvisual selecteert. Gewoonlijk wordt de bezoeker dan naar de productdetailpagina voor het product geleid.

- Doorklikpercentage voor impressies (CTR)

    De CTR wordt berekend als het totale aantal impressieklikken gedeeld door het totale aantal impressies.

## <a name="commerce-analytics-preview-installation"></a>Installatie van Commerce-analyses (preview)

> [!NOTE]
> Commerce-analyses (preview) is in preview beschikbaar in de regio's Verenigde Staten, Canada, Verenigd Koninkrijk, Europa, Azië - Zuidoost, Azië - Oost, Australië en Japan. Als uw Finance and Operations-omgeving zich in een van deze regio's bevindt, kunt u deze functie in uw omgeving inschakelen met behulp van Microsoft Dynamics Lifecycle Services (LCS). Voordat u deze functie kunt gebruiken, raadpleegt u [Export naar Azure Data Lake configureren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commerce-analyses (preview) inschakelen en configureren

Als u Commerce-analyses (preview) wilt installeren, moet u machtigingen hebben om resources te maken in een Azure-abonnement. U moet tevens machtigingen voor het installeren van invoegtoepassingen in LCS hebben. Hier volgt een overzicht van de stappen:

1. [Het voorbeeld van het ontvangstformulier voor Commerce-analyses (preview) indienen](#joinPreview).
2. [Exporteren naar Data Lake inschakelen en configureren](#enableExportToDataLake).
3. [De invoegtoepassing Commerce-analyses (preview) inschakelen en configureren](#enableCommerceAnalyticsAddin).
4. [Een SAS-token (Shared Access Signature) genereren voor uw opslagaccount](#getSASToken).
5. [De implementatiescripts downloaden voor Azure Synapse-weergaven](#downloadSynapseDeploymentScripts).
6. [Een Azure Synapse workspace installeren en configureren](#configureAzureSynapse).
7. [De Power BI-sjabloonapp installeren](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Het voorbeeld van het ontvangstformulier voor Commerce-analyses (preview) indienen

Dien het [voorbeeld van het ontvangstformulier voor Commerce-analyses (preview)](https://forms.office.com/r/vW5VLJGXZ2) in. Het kan tot drie werkdagen duren voordat het formulier is verwerkt. Nadat het is verwerkt, wordt een bevestigingsbericht per e-mail verzonden naar het e-mailadres dat u hebt opgegeven in het formulier.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Exporteren naar Data Lake inschakelen en configureren

Commerce-analyses (preview) is afhankelijk van de functie Exporteren naar Data Lake voor het exporteren van Commerce HQ-gegevens naar Data Lake en ervoor te zorgen dat de gegevens bijgewerkt blijven. Voordat u Commerce-analyses (preview) configureert, moet u Exporteren naar Data Lake inschakelen en configureren door de stappen in [Exporteren naar Azure Data Lake configureren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) uit te voeren.

Maak tijdens het configureren van Exporteren naar Data Lake een notitie over de volgende informatie, omdat u deze later moet invoeren:

- <a name="keyVault"></a>De DNS-naam (Domain Name System) van de sleutelkluis en de geheime namen waarin de toepassings-id en het toepassingsgeheim worden opgeslagen. Zie [Geheimen toevoegen aan de sleutelkluis](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) voor meer informatie.
- <a name="storageAccount"></a>De naam van het opslagaccount voor het Data Lake-exemplaar. Zie [Een Data Lake Storage (Gen2)-account maken in uw abonnement](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) voor meer informatie.

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>De invoegtoepassing Commerce-analyses (preview) inschakelen en configureren

Als u de invoegtoepassing Commerce-analyses (preview) wilt installeren in LCS, moet u een omgevingsbeheerder in LCS zijn voor de omgeving die u wilt gebruiken.

Als u de invoegtoepassing Commerce-analyses (preview) wilt installeren en configureren, voert u de volgende stappen uit.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/) en ga naar uw omgeving.
2. Selecteer op de pagina **Omgeving** op het tabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
3. Selecteer **Commerce-analyses (preview)** in het dialoogvenster.

    Als **Commerce-analyses (preview)** niet vermeld staat, moet u nagaan of u deelneemt aan het Insider Program.

4. Voer in het dialoogvenster **Invoegtoepassingen instellen** de volgende informatie in.

    | Gegevens | Bron | Voorbeeldwaarde |
    |---|---|---|
    | Azure AD-tenant-id voor uw omgeving | Meld u aan bij de [Azure-portal](https://portal.azure.com/) en open de **Azure Active Directory**-service. Open vervolgens de pagina **Eigenschappen** en kopieer de waarde in het veld **Map-id**. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | DNS-naam van uw sleutelkluis | Voer de [DNS-naam](#keyVault) van uw sleutelkluis in. U zou een notitie van deze waarde moeten hebben gemaakt in de vorige sectie. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Geheim dat de toepassings-id bevat | Voer de [naam van het geheim dat de toepassings-id opslaat](#keyVault) in. U zou een notitie van deze waarde moeten hebben gemaakt in de vorige sectie. | app-id |
    | Geheim dat het toepassingsgeheim bevat | Voer de [naam van het geheim dat de toepassingsgeheim opslaat](#keyVault) in. U zou een notitie van deze waarde moeten hebben gemaakt in de vorige sectie. | app-secret |

5. Accepteer de voorwaarden van de aanbieding door het selectievakje in te schakelen en vervolgens **Installeren** te selecteren.

    Het systeem installeert en configureert de invoegtoepassing Commerce-analyses (preview) voor de omgeving. Dit proces kan mogelijk enkele minuten in beslag nemen. Nadat het is voltooid, zou **Commerce-analyses (preview)** moeten worden weergegeven op de pagina **Omgeving** en zou de status **Geïnstalleerd** moeten worden.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>Een SAS-token genereren voor uw opslagaccount

Met een SAS-token kunnen externe entiteiten toegang krijgen tot uw opslagaccount en gedurende een eindige hoeveelheid tijd over een specifieke set bevoegdheden beschikken. Azure Synapse gebruikt het SAS-token voor het openen van de onderliggende gegevens in Data Lake.

> [!NOTE]
> Vanwege een bekende beperking van Commerce-analyses (preview) verliest het Azure Synapse-exemplaar toegang tot de data lake bij het verlopen van het SAS-token. Wanneer u het SAS-token genereert, moet u daarom de maximale vervaldatum instellen die is toegestaan in het beveiligingsbeleid van uw organisatie.

Volg deze stappen om een SAS-token te genereren:

1. Ga in de Azure-portal naar de [opslagaccount](#storageAccount) die u hebt gemaakt tijdens het configureren van Exporteren naar Data Lake.
2. Selecteer in het linkerdeelvenster onder de opslagaccount de optie **Handtekening voor gedeelde toegang**.
3. Stel op de pagina **SAS-opties** de volgende velden in.

    | Veld | Waarde |
    |---|---|
    | Toegestane services | Selecteer **Blob**. |
    | Toegestane resourcetypen | Selecteer **Service**, **Container** en **Object**. |
    | Toegestane machtigingen | Selecteer **Lezen**, **Schrijven**, **Verwijderen**, **Lijst**, **Toevoegen** en **Maken**. |
    | Machtigingen voor blob-versiebeheer | Selecteer **Schakelt het verwijderen van versies in**. |
    | Begin- en vervaldatum/-tijd | Stel waar nodig een begin- en einddatum en -tijd in voor het SAS-token. |
    | Toegestane IP-adressen | Laat dit veld leeg. |
    | Toegestane protocollen | Selecteer **Alleen HTTPS**. |
    | Voorkeursrouteringslaag | Selecteer **Basis (standaard)**. |
    | Ondertekeningssleutel | Selecteer naar wens **key1** of **key2**. |

4. Selecteer **SAS en verbindingsreeks genereren**.
5. Kopieer de waarde in het veld **SAS-token** en plak deze in een teksteditor zoals Kladblok.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>De implementatiescripts downloaden voor Azure Synapse-weergaven

Voor het maken en publiceren van de vereiste weergaven in een Azure Synapse workspace, moet u een set scripts uitvoeren. Voer de volgende stappen om de scripts te downloaden.

1. Ga in GitHub naar de opslagplaats (repo) [Microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions).
2. Download de scripts naar uw lokale computer door de repo te klonen of als een zip-bestand te downloaden.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Een Azure Synapse workspace installeren en configureren

Om een Azure Synapse workspace te installeren en configureren voer u de volgende stappen uit.

1. Installeer een Azure Synapse workspace in uw Azure-abonnement. Zie [Snelstart: Een Synapse workspace maken](/azure/synapse-analytics/quickstart-create-workspace) voor meer informatie.
2. Open in Kladblok of een andere teksteditor het scriptbestand **SetupSynapse.sql** vanuit de map op uw lokale computer waarnaar u de repo Dynamics365Commerce.Solutions hebt gekloond of gedownload in de vorige sectie. Het scriptbestand staat in de map /Pipeline/CommerceAnalyticsSynapse/. Vervang in het script tijdelijke tekst door waarden zoals weergegeven in de volgende tabel.

    | Tekst van tijdelijke aanduiding | Vervangingswaarde |
    |---|---|
    | placeholder_storageaccount | De naam van de [opslagaccount](#storageAccount) die u hebt gemaakt tijdens het configureren van Exporteren naar Data Lake. |
    | <a name="phContainer"></a>placeholder_container | De naam van de opslagcontainer die in uw Data Lake-exemplaar is gemaakt nadat u de invoegtoepassing Exporteren naar Data Lake hebt geïnstalleerd in LCS. Voor de containernaam moet u Opslagverkenner gebruiken in de Azure-portal om door uw opslagaccount te bladeren. |
    | placeholder_sastoken | Het [SAS-token](#getSASToken) dat u hebt gegenereerd. Zorg ervoor dat u het vraagteken (**?**) verwijdert vanaf het begin van de waarde van het SAS-token. |
    | <a name="phUserPwd"></a>placeholder_password | Een sterk wachtwoord van uw keuze. Maak een notitie van dit wachtwoord. Dit wordt ingesteld als het wachtwoord voor de nieuwe account **reportreadonlyuseraccount** die het script maakt. Voer **niet** het wachtwoord van de account **sqladminuser** in. |

3. Kopieer de bijgewerkte inhoud van het scriptbestand.
4. Ga in de Azure-portal naar de nieuwe Azure Synapse workspace. Selecteer op de pagina **Overzicht** de optie **Synapse Studio openen**.
5. Selecteer in Synapse Studio de optie **Nieuw \> SQL-script** en plak de inhoud van het scriptbestand in de SQL-scripteditor.
6. Zorg ervoor dat het veld **Database gebruiken** is ingesteld op **hoofd**.
7. Selecteer **Uitvoeren** en wacht tot het script is uitgevoerd. Als het script is uitgevoerd, worden de database for Commerce-analyses, de referenties voor het openen van de data lake en een alleen-lezen gebruikersaccount voor gebruik door Power BI bij het maken van verbinding met het Azure Synapse-exemplaar gemaakt.
8. Open Windows PowerShell op uw lokale computer in de beheermodus en ga naar de map/Pipeline/CommerceAnalyticsSynapse/ in de map waarin u de repo Dynamics365Commerce.Solutions hebt gekloond of gedownload.
9. Stel het uitvoeringsbeleid voor Windows PowerShell in door de volgende opdracht uit te voeren.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Als de SQL Server PowerShell-module niet al is geïnstalleerd, installeert u deze door de volgende opdracht uit te voeren.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Tijdens de installatie van de module wordt u mogelijk gevraagd om de NuGet-provider te installeren. Selecteer in dit geval **Y** om de NuGet-provider te installeren. U kunt ook gevraagd worden om te bevestigen dat u modules opnieuw installeert vanuit een onvertrouwde opslagplaats. In dit geval selecteert u **Y** om door te gaan met de installatie. U kunt optioneel de cmdlet **Set-PSRepository** uitvoeren om de opslagplaats **PSGallery** te vertrouwen.

11. Publiceer de Azure Synapse-weergaven door de volgende opdracht uit te voeren.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Als u deze opdracht uitvoert, vervangt u de tijdelijke aanduiding door waarden zoals weergegeven in de volgende tabel.

    | Waarde van tijdelijke aanduiding | Vervangingswaarde |
    |---|---|
    | SERVER_NAME | De naam van het Azure Synapse Serverless SQL-eindpunt. U kunt deze waarde ophalen van de pagina **Overzicht** voor de Azure Synapse workspace in de Azure-portal. |
    | PASSWORD | Het wachtwoord voor de **sqladminuser**-account. |
    | STORAGE_ACCOUNT | De naam van de opslagaccount voor Data Lake. |
    | CONTAINER_NAME | De naam van de container die is gemaakt door de functie Exporteren naar Data Lake. Deze container is dezelfde container als u hebt opgegeven als waarde voor [placeholder_container](#phContainer) in stap 2. |
    | DATA_ROOT_PATH | De mapnaam onder de container die alle gegevens bevat. |

    > [!NOTE]
    > U kunt de naam van de opslagaccount, de containernaam en het hoofdpad van de gegevens vinden door de Azure Storage-browser en uw Data Lake-opslagaccount te gebruiken in de Azure-portal.

12. Wacht tot de uitvoering van het script is voltooid. Bij een geslaagde uitvoering van het script worden SQL-weergaven gemaakt in het Azure Synapse Serverless SQL-exemplaar.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>De Power BI-sjabloonapp installeren

Als u de Power BI-sjabloonapp voor Commerce-analyses (preview) wilt installeren, voert u de volgende stappen uit.

1. Meld u aan bij de [Power BI-portal](https://powerbi.microsoft.com/) met uw organisatie-id.
2. Installeer de Power BI-sjabloonapp voor Commerce-analyses (preview) door naar [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) te gaan. Mogelijk ontvangt u een waarschuwing waarin wordt vermeld dat de app niet in AppSource wordt vermeld. Selecteer **Installeren**.
3. Als u de app voor het eerst installeert, gaat u verder met stap 5. Als u deze app al eerder hebt geïnstalleerd, worden de volgende opties voor het bijwerken van de app weergegeven:

    - **De werkruimte en de app bijwerken**: werk de bestaande sjabloonapp bij en overschrijf de bestaande app-instellingen, zoals de naam van het app-exemplaar en de machtigingsconfiguraties.
    - **Alleen inhoud van werkruimte bijwerken zonder de app bij te werken**: werk de bestaande sjabloonapp bij, maar houd uw bestaande app-instellingen. *Deze optie is de aanbevolen optie voor app-updates.*
    - **Een andere kopie van de app installeren in een nieuwe werkruimte**: maak een nieuwe werkruimte en maak vervolgens een kopie van de bestaande sjabloonapp in de werkruimte. De bestaande werkruimte blijft intact.

4. Selecteer een van de opties voor bijwerken en selecteer vervolgens **Installeren**.
5. Open de geïnstalleerde app door **Apps** te selecteren in het linkerdeelvenster en vervolgens de app te selecteren.
6. Koppel de app aan uw gegevensbron door **Verbinden** te selecteren. Als u de app al eerder hebt geïnstalleerd, selecteert u de koppeling **Uw gegevens verbinden** op de gele berichtenbalk.
7. Stel de volgende velden in.

    | Veld | Waarde |
    |---|---|
    | Server | Voer de naam in van het Azure Synapse Serverless SQL-eindpunt dat u hebt gemaakt in de vorige sectie. U kunt deze waarde ophalen van de pagina **Overzicht** voor de Azure Synapse workspace in de Azure-portal. |
    | Database | Voer **CommerceAnalytics** in. |
    | Taal | Selecteer een waarde in de lijst. Dit veld wordt gebruikt voor gelokaliseerde product- en categorienamen. De waarde is hoofdlettergevoelig. |
    | Datumbereik | Selecteer een waarde in de lijst. Gegevens voor het geselecteerde aantal maanden worden in de Power BI-gegevensset geïmporteerd. De waarde die u selecteert, is van invloed op de grootte van de gegevensset en de tijd die nodig is voor synchronisatie. |

8. Selecteer **Volgende**. U wordt gevraagd de referenties in te voeren voor verbinding met de Azure Synapse SQL-database. Stel de velden in aan de hand van de volgende tabel.

    | Veld | Waarde |
    |---|---|
    | Verificatiemethode | Selecteer **Basis**. |
    | Gebruikersnaam | Voer **reportreadonlyuser** in. |
    | Wachtwoord | Voer de waarde in die u hebt gebruikt voor de tijdelijke aanduiding [placeholder_password](#phUserPwd) in het script SetupSynapse.sql. Dit wachtwoord is het wachtwoord voor de account **reportreadonlyuser**. |

9. Selecteer **Aanmelden en verbinden**.
10. Wacht tot de gegevensset is bijgewerkt. Selecteer vervolgens de knop **App bewerken** om de werkruimte voor de app te openen, waar u de updatestatus van gegevensset kunt bekijken. In de werkruimte voor de app kunt u desgewenst ook automatische updateschema's voor uw gegevensset instellen, machtigingen beheren en de naam van het app-exemplaar wijzigen.

### <a name="privacy"></a><a name="privacy"></a>Privacy

Uw privacy is belangrijk voor ons. Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
