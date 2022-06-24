---
title: Commerce-analyses (preview)
description: In dit artikel wordt uitgelegd hoe u de analysemogelijkheden installeert en gebruikt in Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 9ffa0affa0b80af65dd2aa37ef2fe969752ae332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887161"
---
# <a name="commerce-analytics-preview"></a>Commerce-analyses (preview)

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u Commerce-analyses (preview) installeert. Dit is de functionele analysemogelijkheid die deel uitmaakt van Microsoft Dynamics 365 Commerce.

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

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filters op het hoogste niveau

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

#### <a name="products"></a><a name="ProductsPage"></a> Producten

- Verkoop
- Marge
- Retouren

#### <a name="customers"></a><a name="CustomersPage"></a> Klanten

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
> Commerce-analyses (preview) is in preview beschikbaar in de regio's Verenigde Staten, Canada, Verenigd Koninkrijk, Europa, Azië - Zuidoost, Azië - Oost, Australië en Japan. Als uw omgeving voor financiën en bedrijfsactiviteiten zich in een van deze regio's bevindt, kunt u deze functie in uw omgeving inschakelen met behulp van Microsoft Dynamics Lifecycle Services (LCS). Voordat u deze functie kunt gebruiken, raadpleegt u [Export naar Azure Data Lake configureren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commerce-analyses (preview) inschakelen en configureren

Als u Commerce-analyses (preview) wilt installeren, moet u machtigingen hebben om resources te maken in een Azure-abonnement. U moet tevens machtigingen voor het installeren van invoegtoepassingen in LCS hebben.

Als u Commerce-analyses (preview) wilt inschakelen en configureren, voert u de volgende stappen uit.

1. [Het voorbeeld van het ontvangstformulier voor Commerce-analyses (preview) indienen](#joinPreview)
2. [Selecteer en configureer de invoegtoepassing Exporteren naar Data Lake](#enableExportToDataLake).
3. [Een Azure Synapse workspace installeren en configureren](#configureAzureSynapse).
4. [Voeg geheimen toe aan de sleutelkluis](#addSecrets).
5. [De invoegtoepassing Commerce-analyses (preview) inschakelen en configureren](#enableCommerceAnalyticsAddin).
6. [De Power BI-sjabloonapp installeren](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Het voorbeeld van het ontvangstformulier voor Commerce-analyses (preview) indienen

Dien het [voorbeeld van het ontvangstformulier voor Commerce-analyses (preview)](https://forms.office.com/r/vW5VLJGXZ2) in. Nadat uw aanvraag is verwerkt, wordt een bevestigingsbericht per e-mail verzonden naar het e-mailadres dat u hebt opgegeven in het formulier.

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>De invoegtoepassing Exporteren naar Data Lake inschakelen en configureren

> [!IMPORTANT]
> Wanneer u de invoegtoepassing Exporteren naar Data Lake configureert, wordt het selectievakje **Real-time gegevenswijzigingen** op de instellingspagina voor de invoegtoepassing Exporteren naar Data Lake ingeschakeld om te voorkomen dat wijzigingen in real-time gegevens mogelijk zijn. De functie **Real-time gegevenswijzigingen** is een preview-functie en wordt momenteel niet ondersteund door Commerce-analyses. Als u de functie inschakelt, kan Commerce-analyses uw gegevens niet verwerken in het data lake en zullen de meeste Power BI-rapporten geen gegevens bevatten.

Commerce-analyses (preview) is afhankelijk van de functie Exporteren naar Data Lake voor het exporteren van Commerce Headquarters-gegevens naar Data Lake en ervoor te zorgen dat de gegevens bijgewerkt blijven. Voordat u Commerce-analyses (preview) configureert, moet u Exporteren naar Data Lake inschakelen en configureren door de stappen in [Exporteren naar Azure Data Lake configureren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) uit te voeren.

Maak tijdens het configureren van de invoegtoepassing Exporteren naar Data Lake een notitie over de volgende informatie, omdat u deze later moet invoeren:

- <a name="keyVault"></a>De DNS-naam (Domain Name System) van de sleutelkluis die u hebt opgegeven.
- De door u opgegeven geheime namen die de toepassings-ID en het toepassingsgeheim bevatten. Zie [Geheimen toevoegen aan de sleutelkluis](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) voor meer informatie.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Een Azure Synapse workspace installeren en configureren

Voor Commerce-analyses (preview) moet Synapse SQL on-demand in uw Azure Synapse workspace worden ingericht. Om een Azure Synapse workspace te installeren en configureren voer u de volgende stappen uit.

1. Installeer een Azure Synapse workspace in uw Azure-abonnement. Zie [Snelstart: Een Synapse workspace maken](/azure/synapse-analytics/quickstart-create-workspace) voor meer informatie.
1. <a name="serverlessep"></a>Nadat de werkruimte is ingericht, opent u de pagina met het resourceoverzicht en noteert u de waarde bij **Serverless SQL-eindpunt**. U moet deze waarde opslaan in de sleutelkluis van het volgende onderdeel.
1. Selecteer op de overzichtspagina de koppeling **Synapse Studio openen** om de Azure Synapse Studio voor uw werkruimte te openen.
1. Selecteer in het linkervenster de optie **Beheren**. Als u de menunamen wilt weergeven, moet u mogelijk de vouwkoppeling selecteren in het linkermenu.
1. Selecteer **Toegangsbeheer** onder **Beveiligingsgroep**. 
1. Selecteer **Toevoegen**.
1. Stel in het deelvenster **Roltoewijzing toevoegen** de opties in zoals in de volgende tabel wordt beschreven.

    | Optie | Waarde |
    |--------|-------|
    | Bereik | Selecteer **Werkruimte**. |
    | Rol | Selecteer **Synapse SQL-beheerder**.|
    | Gebruiker selecteren | Zoek de naam van de toepassing die u hebt [gemaakt tijdens de installatie van de invoegtoepassing Exporteren naar Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Selecteer de toepassing wanneer deze in de zoekresultaten wordt weergegeven. De toepassing wordt nu weergegeven in de sectie **Geselecteerde gebruiker(s), groep(en) of serviceprincipal(s)**. |

1. Selecteer **Toepassen** om de roltoewijzing te voltooien. Aan de toepassing worden Synapse SQL-beheerdersbevoegdheden toegekend. Zo kunnen de vereiste weergaven worden gemaakt tijdens de configuratie van de LCS-invoegtoepassing Commerce-analyses (Preview).

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Geheimen toevoegen aan de sleutelkluis

Voeg in dezelfde [sleutelkluis](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) die u hebt gebruikt bij het configureren van de invoegtoepassing Exporteren naar Data Lake, de geheimen toe die in de volgende tabel worden weergegeven. Voor elke geheim moet u een naam en de opgegeven waarde opgegeven.

| Voorgestelde geheime naam | Geheime waarde | Voorbeeld van geheime waarde |
|---------|---------|---------|
| synapse-sql-server | De Serverless SQL-eindpuntwaarde die u hebt genoteerd tijdens het [configureren van de Azure Synapse workspace](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | Het wachtwoord dat moet worden ingesteld voor de alleen-lezen SQL-gebruiker. Het Power BI-rapport gebruikt dit wachtwoord om verbinding te maken met de serverless SQL. Volg het wachtwoordbeleid van uw organisatie om het wachtwoord in te stellen. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>De invoegtoepassing Commerce-analyses (preview) inschakelen en configureren

Als u de invoegtoepassing Commerce-analyses (preview) wilt installeren in LCS, moet u een omgevingsbeheerder in LCS zijn voor de omgeving die u wilt gebruiken.

Als u de invoegtoepassing Commerce-analyses (preview) wilt installeren en configureren, voert u de volgende stappen uit.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/) en ga naar uw omgeving.
2. Selecteer op de pagina **Omgeving** op het tabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
3. Selecteer **Commerce-analyses (preview)** in het dialoogvenster.
4. Voer in het dialoogvenster **Invoegtoepassingen instellen** de volgende informatie in.

    | Gegevens | Bron | Voorbeeldwaarde |
    |---|---|---|
    | Azure Active Directory (Azure AD) tenant-id | Meld u aan bij de [Azure-portal](https://portal.azure.com/) en open de **Azure Active Directory**-service. Open vervolgens de pagina **Eigenschappen** en kopieer de waarde in het veld **Tenant-id**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | DNS-naam van uw Azure Key Vault | Voer de DNS-naam van uw sleutelkluis in. U hebt deze waarde genoteerd tijdens het [configureren van de invoegtoepassing Exporteren naar Data Lake](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Naam van het geheim dat de toepassings-id bevat | Voer de naam van het geheim dat de toepassings-id opslaat in. U hebt deze waarde genoteerd tijdens het [configureren van de invoegtoepassing Exporteren naar Data Lake](#keyVault). | `app-id` |
    | Naam van het geheim dat het toepassingsgeheim bevat | Voer de naam van het geheim dat de toepassingsgeheim opslaat in. U hebt deze waarde genoteerd tijdens het [configureren van de invoegtoepassing Exporteren naar Data Lake](#keyVault). | `app-secret` |
    | Naam van het geheim dat het serverless SQL-eindpunt bevat voor Azure Synapse | Voer de naam van het geheim in waarin het serverless SQL-eindpunt is opgeslagen. U hebt dit geheim gemaakt tijdens het [toevoegen van de geheimen aan de sleutelwaarde](#addSecrets). | `synapse-sql-server` |
    | Naam van het geheim met het wachtwoord dat u kunt instellen voor alleen-lezen SQL-gebruikers in Azure Synapse | Voer de naam in van het geheim met het wachtwoord dat u wilt instellen voor de alleen-lezen serverless SQL-gebruiker. Deze gebruiker wordt voor u gemaakt en moet in het Power BI-rapport worden gebruikt om verbinding te maken met de serverless SQL-server. U hebt dit geheim gemaakt tijdens het [toevoegen van de geheimen aan de sleutelwaarde](#addSecrets). | `readonly-sql-pwd` |

1. Accepteer de voorwaarden van de aanbieding door het selectievakje in te schakelen en vervolgens **Installeren** te selecteren.

    Het systeem installeert en configureert de invoegtoepassing Commerce-analyses (preview) voor de omgeving. Dit proces kan mogelijk enkele minuten in beslag nemen. Nadat het is voltooid, zou **Commerce-analyses (preview)** moeten worden weergegeven op de pagina **Omgeving** en zou de status **Geïnstalleerd** moeten worden.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>De Power BI-sjabloonapp installeren

Als u de Power BI-sjabloonapp voor Commerce-analyses (preview) wilt installeren, voert u de volgende stappen uit.

1. Meld u aan bij de [Power BI-portal](https://powerbi.microsoft.com/) met uw organisatie-id.
1. Installeer de Power BI-sjabloonapp voor Commerce-analyses (preview) door naar [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) te gaan. U kunt ook naar de [AppSource-pagina voor Dynamics 365 Commerce-analyses](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) gaan en **Nu ophalen** selecteren.
1. Als u de app voor het eerst installeert, gaat u verder met stap 5. Als u deze al eerder hebt geïnstalleerd, worden de volgende opties voor het bijwerken van de app weergegeven:

    - **De werkruimte en de app bijwerken**: werk de bestaande sjabloonapp bij en overschrijf de bestaande app-instellingen, zoals de naam van het app-exemplaar en de machtigingsconfiguraties.
    - **Alleen inhoud van werkruimte bijwerken zonder de app bij te werken**: werk de bestaande sjabloonapp bij, maar houd uw bestaande app-instellingen. *Deze optie is de aanbevolen optie voor app-updates.*
    - **Een andere kopie van de app installeren in een nieuwe werkruimte**: maak een nieuwe werkruimte en maak vervolgens een kopie van de bestaande sjabloonapp in de werkruimte. De bestaande werkruimte blijft intact.

1. Selecteer een van de opties voor bijwerken en selecteer vervolgens **Installeren**.
1. Open de geïnstalleerde app door **Apps** te selecteren in het linkerdeelvenster en vervolgens de app te selecteren.
1. Koppel de app aan uw gegevensbron door **Verbinden** te selecteren. Als u de app al eerder hebt geïnstalleerd, selecteert u de koppeling **Uw gegevens verbinden** op de gele berichtenbalk.
1. Stel de volgende velden in.

    | Veld | Waarde |
    |---|---|
    | Server | Voer het serverless SQL-eindpunt in dat u hebt genoteerd nadat u de [Azure Synapse workspace hebt gemaakt](#serverlessep). |
    | Database | Voer **CommerceAnalytics** in. |
    | Taal | Selecteer een waarde in de lijst. Dit veld wordt gebruikt voor gelokaliseerde product- en categorienamen. De waarde is hoofdlettergevoelig. |
    | Datumbereik | Selecteer een waarde in de lijst. Gegevens voor het geselecteerde aantal maanden worden in de Power BI-gegevensset geïmporteerd. De waarde die u selecteert, is van invloed op de grootte van de gegevensset en de tijd die nodig is voor synchronisatie. |

1. Selecteer **Volgende**. Wanneer u wordt gevraagd de referenties in te voeren voor de verbinding met de Azure Synapse SQL-database, stelt u de veldwaarden in zoals wordt weergegeven in de volgende tabel.

    | Veld | Waarde |
    |---|---|
    | Verificatiemethode | Selecteer **Basis**. |
    | Gebruikersnaam | Voer **reportreadonlyuser** in. |
    | Wachtwoord | Voer het wachtwoord in dat u hebt [opgeslagen voor de alleen-lezen SQL-gebruiker in de sleutelkluis](#roUser). |

1. Selecteer **Aanmelden en verbinden**.
1. Wacht tot de gegevensset is bijgewerkt. Selecteer vervolgens **App bewerken** om de werkruimte voor de app te openen, waar u de updatestatus van gegevensset kunt bekijken. In de werkruimte voor de app kunt u desgewenst ook automatische updateschema's voor uw gegevensset instellen, machtigingen beheren en de naam van het app-exemplaar wijzigen.

### <a name="privacy"></a><a name="privacy"></a>Privacy

Uw privacy is belangrijk voor ons. Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
