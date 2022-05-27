---
title: Een e-commercesite voor B2B instellen
description: In dit onderwerp wordt beschreven hoe u een e-commercesite voor B2B (business-to-business) in Microsoft Dynamics 365 Commerce instelt.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 31266f84270f170e172eadea75a90397c5a6e8e6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691913"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>Een e-commercesite voor B2B instellen

[!include [banner](../../includes/banner.md)]

E-commercesites voor B2B bieden belangrijke mogelijkheden om de workflow te optimaliseren voor een B2B-gebruiker. In dit onderwerp wordt beschreven hoe u een e-commercesite voor B2B in Microsoft Dynamics 365 Commerce instelt. U doorloopt de modules en locatie-instellingen die geconfigureerd moeten worden om B2B-specifieke scenario's mogelijk te maken.

## <a name="prerequisites"></a>Vereisten

- Als u een B2B-e-commercesite wilt instellen, moet u specifieke functies in Commerce Headquarters inschakelen en configureren, zoals wordt beschreven in dit onderwerp.
- Basiservaringen, zoals de detectie van producten, productdetailpagina's, de winkelwagen en het uitchecken, worden ondersteund door dezelfde modules die worden gebruikt voor e-commercesites voor B2C (business-to-consumer). Site-auteurs moeten vertrouwd zijn met alle modules die worden ondersteund door Dynamics 365 Commerce. Zie [Overzicht van modulebibliotheek](../starter-kit-overview.md) voor meer informatie.
- Dit onderwerp gaat ervanuit dat site-auteurs de basisprincipes begrijpen van Commerce Site Builder, sjablonen, fragmenten en pagina's, zodat ze de B2B-functies voor e-commercesites kunnen inschakelen.

## <a name="site-level-settings"></a>Instellingen op siteniveau

U hebt toegang tot siteniveau-instellingen in Site Builder via **Site-instellingen \> Extensies**. De volgende twee siteniveau-instellingen zijn van toepassing op B2B-scenario's:

- **Betalingen van klantaccounts inschakelen**: met deze eigenschap kunnen gebruikers orders betalen via klantaccounts. De beschikbare waarden zijn **Ingeschakeld voor B2B-klanten**, **Ingeschakeld voor B2C-klanten**, **Ingeschakeld voor alle klanten** en **Uitgeschakeld voor alle klanten**. Als uw B2B-site klantaccounts ondersteunt, moet u **Ingeschakeld voor B2B-klanten** selecteren.
- **Limieten voor orderhoeveelheid inschakelen**: met deze eigenschap kunt u beperkingen instellen voor het aantal artikelen dat voor elk product of elke categorie kan worden besteld. De beschikbare waarden zijn **Ingeschakeld voor B2B-klanten**, **Ingeschakeld voor B2C-klanten**, **Ingeschakeld voor alle klanten** en **Uitgeschakeld voor alle klanten**.

> [!NOTE]
> Wanneer u een upgrade naar de nieuwste versie van de modulebibliotheek uitvoert, moet u aanvullende stappen uitvoeren om ervoor te zorgen dat de eerder beschreven site-instellingen beschikbaar zijn in uw omgeving. Zie [Het bestand app.settings.json bijwerken](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer informatie.

## <a name="create-business-partner-sign-up-pages"></a>Aanmeldingspagina's voor zakenpartners maken

Om een zakenpartner te worden, moeten gebruikers eerst een aanvraag indienen. Op de B2B-startpagina wordt een koppeling naar de aanvraagpagina voor zakenpartners beschikbaar, zodat gebruikers het proces kunnen starten. Nadat gebruikers een aanvraag voor zakenpartners hebben ingediend, ontvangen ze bevestiging dat de aanvraag is ingediend. 

### <a name="create-a-business-partner-request-page"></a>Een aanvraagpagina voor zakenpartners maken

De module **Aanmelden bij partner** op een aanvraagpagina voor zakenpartners wordt gebruikt om gebruikersaanvragen te starten om zakenpartners te worden. Met deze module kunt u de vereiste gebruikersinformatie voor het aanmeldingsproces verzamelen. Verder wordt de module **Adres bedrijfsaccount** gebruikt om het adres van de gebruiker vast te leggen.

Volg deze stappen om de aanvraagpagina voor zakenpartners in te stellen en te configureren in Site Builder.

1. Maak een sjabloon met de naam **Aanmelden**. Deze sjabloon moet de volgende modules bevatten:

    - Aanmelden bij partner
    - Breadcrumb
    - Koptekst
    - Voettekst
    - Inhoudsblokkering
    - Tekstblok
    - Productverzameling

1. Gebruik de sjabloon **Aanmelden** om een pagina te maken met de naam **Aanvraag voor zakenpartner**.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de startpagina en voer **Start** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Aanmelden bij partner** toe onder de module **Breadcrumb**. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Een zakenpartner worden** in.
1. Voeg in het vak **Aanmelden bij partner** een module **Adres bedrijfsaccount** toe.
1. Voeg in het vak **Container** een module **Tekstblok** toe onder de module **Aanmelden bij partner**. Hier kunt u een aantal algemene voorwaarden voor het aanmeldingsproces definiëren.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.

### <a name="create-a-business-partner-request-confirmation-page"></a>Een aanvraagbevestigingspagina voor zakenpartners maken

Nadat een aanvraag voor een zakenpartner is ingediend, moet er een bevestigingspagina voor de gebruiker worden weergegeven om de indiening te bevestigen. 

Volg deze stappen om de aanvraagbevestigingspagina in te stellen en te configureren in Site Builder.

1. Gebruik de sjabloon **Aanmelden** die u eerder hebt gemaakt om een pagina te maken met de naam **Bevestiging voor partneraanvraag**.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Inhoudsblok** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Aanvraag ingediend** in. Voer in het veld **Tekst met opmaak** de tekst **Uw aanvraag is ingediend** in. Configureer onder **Koppelingen** een koppeling naar de startpagina en voer **Terug naar winkelen** in als koppelingstekst.
1. Voeg nog een module **Container** toe en voeg er een module **Productverzameling** aan toe.
1. Configureer de module **Productverzameling** met de aanbevelings- of categorielijst die u op de pagina wilt plaatsen.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.

Volg deze stappen om een koppeling toe te voegen aan de aanvraagbevestigingspagina in Site Builder.

1. Ga naar de pagina **Aanvraag voor zakenpartner** die u eerder hebt gemaakt en selecteer **Bewerken**. 
1. Selecteer het modulevlak **Aanmelden bij partner**. Configureer in het eigenschappenvenster onder **Koppeling naar de pagina Bevestiging aanmelden** de koppeling naar de aanvraagpagina voor zakenpartners die u eerder hebt gemaakt. 
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Een koppeling voor het aanvragen van een zakenpartner toevoegen aan de startpagina

Nadat de aanmeldings- en bevestigingspagina's voor aanvragen voor bedrijfspartners zijn gemaakt, moet u de aanmeldingspagina toegankelijk maken via een koppeling op de startpagina. U kunt deze taak voltooien door de koppeling aan een module **Inhoudsblok** op de startpagina toe te voegen.

Volg deze stappen om een koppeling voor het aanvragen van een zakenpartner toe te voegen aan de startpagina in Site Builder.

1. Ga naar de startpagina voor uw site en selecteer **Bewerken**.
1. Selecteer een modulevak **Inhoudsblok**. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de aanvraagpagina voor een zakenpartner die u eerder hebt gemaakt en voer **Aanmelden als een zakenpartner** of vergelijkbare tekst in als de koppelingstekst. Voeg waar nodig een afbeelding toe.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="account-management-landing-page"></a>Landingspagina accountbeheer

De landingspagina voor accountbeheer bevat alle informatie over accountbeheer die vereist is voor zowel B2B- als B2C-e-commercesites. Alleen aangemelde gebruikers kunnen deze pagina weergeven.

Volg deze stappen om een landingspagina voor B2B-accountbeheer in Site Builder te maken en te configureren.

1. Maak een sjabloon met de naam **Accountbeheer**. Deze sjabloon moet de volgende modules bevatten:

    - Koptekst
    - Voettekst
    - Breadcrumb
    - Welkomstegel voor rekening
    - Algemene tegel voor rekening
    - Adrestegel voor account
    - Tegel voor wensenlijst rekening
    - Adrestegel voor rekening
    - Loyaliteitstegel voor rekening
    - Tegel voor klantsaldo voor account
    - Tegel met ordersjablonen van rekening
    - Organisatiegebruikers
    - Lijst met zakelijke organisaties
    - Saldo van klantrekening
    - Ordersjabloonregels
    - Lijst met ordersjablonen
    - Tegel voor facturen van account
    - Facturenlijst
    - Factuurdetails

1. Gebruik de sjabloon **Accountbeheer** om een pagina met de naam **Mijn account** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**. 
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de startpagina en voer **Start** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Welkomsttegel** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Welkom** in.
1. Voeg in het vak **Hoofd** nog een module **Container** toe (**Container 2**). Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**. Stel de waarde voor **onderliggende items weergegeven** in op **Twee**. 
1. Voeg in het vak **Container 2** een module **Algemene accounttegel** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Mijn profiel** in. Configureer onder **Koppelingen** een koppeling naar de pagina **Mijn profiel**. 
1. Voeg in het vak **Container 2** nog een module **Algemene accounttegel** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Orderhistorie** in. Configureer onder **Koppelingen** een koppeling naar de pagina Orderhistorie.
1. Voeg in het vak **Hoofd** nog een module **Container** toe (**Container 3**). Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**. Stel de waarde voor **onderliggende items weergegeven** in op **Twee**. 
1. Voeg in het vak **Container 3** een module **Adrestegel voor account** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Mijn adres** in. Configureer onder **Koppelingen** een koppeling naar de pagina **Mijn adres**. 
1. Voeg in het vak **Container 3** een module **Verlanglijsttegel voor account** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Mijn verlanglijst** in. Configureer onder **Koppelingen** een koppeling naar de pagina **Mijn verlanglijst**.
1. Voeg in het vak **Hoofd** nog een module **Container** toe (**Container 4**). Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**. Stel de waarde voor **onderliggende items weergegeven** in op **Twee**. 
1. Voeg in het vak **Container 4** een module **Organisatiegebruikers** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Organisatiegebruikers** in. 
1. Voeg in het vak **Container 4** een module **Tegel voor klantsaldo voor account** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Accountkrediet** in. 
1. Voeg in het vak **Hoofd** nog een module **Container** toe (**Container 5**). Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**. Stel de waarde voor **onderliggende items weergegeven** in op **Twee**. 
1. Voeg in de module **Container 5** een module **Tegel met ordersjablonen van account** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Ordersjablonen** in. 
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

> [!NOTE] 
> Sommige secties die u in stap 13 tot en met 18 hebt toegevoegd, worden niet weergegeven op het canvas WYSIWYG in Site Builder omdat voor deze onderdelen een aangemeld B2B-account nodig is.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Pagina's en modules voor klantsaldi maken en configureren 

Klantaccounts kunnen worden gebruikt om te betalen voor orders. Het beschikbare saldo in een klantaccount kan worden weergegeven vanuit de pagina voor accountbeheer van een gebruiker.

### <a name="create-a-customer-balance-page"></a>Een pagina voor klantsaldo maken 

Voordat aangemelde B2B-gebruikers hun klantsaldo kunnen weergeven, moet u een klantsaldopagina maken. 

Voer de volgende stappen uit om een pagina voor klantsaldo in Site Builder te maken.

1. Gebruik de sjabloon **Accountbeheer** die u eerder hebt gemaakt om een pagina met de naam **Klantsaldo** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** nog een module **Container** toe (**Container 3**). Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**. Stel de waarde voor **onderliggende items weergegeven** in op **Twee**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de landingspagina voor accountbeheer en voer **Mijn account** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Klantaccountsaldo** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Accountsaldo** in.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.
1. Ga naar de landingspagina voor accountbeheer (**Mijn account**) die u eerder hebt gemaakt.
1. Voeg een koppeling naar de klantsaldopagina toe in het eigenschappenvenster voor de module **Tegel voor klantsaldo voor account**. 
1. Sla de pagina op en publiceer deze.

De pagina met het klantsaldo is nu gemaakt en gebruikers kunnen deze pagina openen via de landingspagina voor accountbeheer.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Een uitcheckpagina configureren zodat het klantsaldo kan worden gebruikt als betaalwijze

De module **Klantaccountbetaling** is vereist om het klantsaldo te gebruiken als betaalwijze. Deze module moet als betaalwijze aan de uitcheckpagina worden toegevoegd. Zie [Kassamodule](../add-checkout-module.md) voor informatie over het configureren van een uitcheckpagina en de modules die voor uitchecken vereist zijn, waaronder alle betalingsgegevens.

Nadat u een uitcheckpagina hebt geconfigureerd, moet u de module **Klantaccountbetaling** toevoegen aan de betalingssectie en vervolgens de pagina opslaan en publiceren. B2B-gebruikers kunnen zich vervolgens aanmelden bij de e-commercesite en hun beschikbare klantsaldo toepassen op orders tijdens het uitchecken.

Via **Site Builder \> Extensies** kunt u er bovendien voor zorgen dat de eigenschap **Betalingen van klantaccounts inschakelen** is ingesteld op **Ingeschakeld voor B2B-klanten**.

## <a name="create-order-template-pages"></a>Ordersjabloonpagina's maken

U kunt twee ordersjabloonpagina's instellen voor een B2B-e-commercesite: een pagina met een lijst met ordersjablonen en een pagina met ordersjabloonregels.

Op een pagina met een lijst met ordersjablonen wordt een lijst weergegeven met alle beschikbare ordersjablonen. Deze wordt ingesteld op basis van de module **Lijst met ordersjablonen**. Via de pagina met de lijst met ordersjablonen kunt u een sjabloon maken of verwijderen en de artikelen in een sjabloon aan de winkelwagen toevoegen.

Op een pagina met ordersjabloonregels worden de details weergegeven van de ordersjabloon die is geselecteerd op een pagina met een lijst met ordersjablonen. Deze wordt ingesteld op basis van de module **Ordersjabloonregels**. Wanneer een gebruiker de naam van een sjabloon selecteert op een pagina met een lijst met ordersjablonen, wordt de pagina met ordersjabloonregels weergegeven met de details van de sjabloon. De gebruiker kan vervolgens de items in de sjabloon weergeven en bewerken.

### <a name="create-an-order-templates-list-page"></a>Een pagina met een lijst met ordersjablonen maken

Voer de volgende stappen uit om een pagina met een lijst met ordersjablonen in Site Builder te maken.

1. Gebruik de sjabloon **Accountbeheer** die u eerder hebt gemaakt om een pagina met de naam **Ordersjablonen** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de landingspagina voor accountbeheer en voer **Mijn account** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Lijst met ordersjablonen** toe.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.
1. Ga naar de landingspagina voor accountbeheer (**Mijn account**) die u eerder hebt gemaakt.
1. Configureer in het eigenschappenvenster voor de module **Tegel met ordersjablonen van account** onder **Koppelingen** een koppeling naar de pagina met de lijst met ordersjablonen die u zojuist hebt gemaakt.
1. Sla de pagina op en publiceer deze.

De pagina met de lijst met ordersjablonen is nu gemaakt en gebruikers kunnen deze pagina openen via de landingspagina voor accountbeheer.

### <a name="create-an-order-template-lines-page"></a>Een pagina met ordersjabloonregels maken

Voer de volgende stappen uit om een pagina met ordersjabloonregels in Site Builder te maken.

1. Gebruik de sjabloon **Accountbeheer** die u eerder hebt gemaakt om een pagina met de naam **Ordersjabloonregels** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de landingspagina voor accountbeheer en voer **Mijn account** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Ordersjabloonregels** toe.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.

## <a name="onboard-business-partner-users"></a>Gebruikers van zakenpartner onboarden

Via de pagina met organisatiegebruikers kan de beheerder van een zakenpartnerorganisatie extra gebruikers van die organisatie onboarden naar de B2B-e-commercesite. Deze wordt ingesteld op basis van de module **Lijst met zakelijke organisaties**. Via de pagina met organisatiegebruikers kan een beheerder gebruikers toevoegen of verwijderen, accountsaldi definiëren en overzichten voor een gebruiker aanvragen.

Voer de volgende stappen uit om een pagina met organisatiegebruikers in Site Builder te maken.

1. Gebruik de sjabloon **Accountbeheer** die u eerder hebt gemaakt om een pagina met de naam **Organisatiegebruikers** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de landingspagina voor accountbeheer en voer **Mijn account** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Lijst met zakelijke organisaties** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Organisatiegebruikers** in.
1. Schakel in het eigenschappenvenster van de module **Lijst met zakelijke organisaties** de eigenschappen **Tabel sorteren** en **Tabel pagineren** in. Stel het aantal pagina's in op **5**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.
1. Ga naar de landingspagina voor accountbeheer (**Mijn account**) die u eerder hebt gemaakt.
1. Configureer in het eigenschappenvenster voor de module **Tegel met organisatiegebruikers** onder **Koppelingen** een koppeling naar de pagina met organisatiegebruikers die u zojuist hebt gemaakt. 
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="create-invoice-pages"></a>Factuurpagina's maken

Op een lijstpagina met facturen wordt een lijst met alle beschikbare facturen weergegeven. Deze wordt ingesteld op basis van de module **Facturenlijst**. Vanaf de factuurlijstpagina kunnen gebruikers facturen betalen of aanvragen. 

Een pagina met factuurdetails toont de details van de factuur die op een facturenlijstpagina is geselecteerd. Deze wordt ingesteld op basis van de module **Factuurdetails**. Wanneer een gebruiker een factuur-id selecteert op een lijstpagina voor facturen, wordt de pagina met factuurgegevens weergegeven met de details van de factuur.

### <a name="create-an-invoices-list-page"></a>Een lijstpagina voor facturen maken

Voer de volgende stappen uit om een pagina met een lijst met facturen in Site Builder te maken.

1. Gebruik de sjabloon **Accountbeheer** die u eerder hebt gemaakt om een pagina met de naam **Facturenlijst** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de landingspagina voor accountbeheer en voer **Mijn account** in als koppelingstekst.
1. Voeg in het vak **Container** een module **Facturenlijst** toe. Voer in het eigenschappenvenster van de module onder **Koptekst** de tekst **Facturen** in.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.
1. Ga naar de landingspagina voor accountbeheer (**Mijn account**) die u eerder hebt gemaakt.
1. Configureer in het eigenschappenvenster voor de module **Tegel met accountfacturen** onder **Koppelingen** een koppeling naar de lijstpagina met facturen die u zojuist hebt gemaakt. 
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="create-an-invoice-details-page"></a>Een pagina met factuurdetails maken

Voer de volgende stappen uit om een pagina met factuurdetails in Site Builder te maken.

1. Gebruik de sjabloon **Accountbeheer** die u eerder hebt gemaakt om een pagina met de naam **Factuurdetails** te maken.
1. Voeg in het vak **Koptekst** het koptekstfragment toe dat vooraf is geconfigureerd met de koptekst van de site.
1. Voeg in het vak **Voettekst** het koptekstfragment toe dat vooraf is geconfigureerd met de voettekst van de site.
1. Voeg in het vak **Hoofd** een module **Container** toe. Stel in het eigenschappenvenster van de module **Breedte** in op **Container vullen**.
1. Voeg in het vak **Container** een module **Breadcrumb** toe. Configureer in het eigenschappenvenster van de module onder **Koppelingen** een koppeling naar de landingspagina voor accountbeheer en voer **Mijn account** in als koppelingstekst. Configureer vervolgens een koppeling naar de lijstpagina met facturen en voer **Facturenlijsten** in als de koppelingstekst.
1. Voeg in het vak **Container** een module **Factuurdetails** toe.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Publiceer de URL voor de pagina.

## <a name="add-a-quick-add-module-to-the-cart-page"></a>Voeg een module voor snel toevoegen toe aan de winkelwagenpagina

De module snel toevoegen biedt een manier om snel meerdere artikelen aan de winkelwagen toe te voegen door artikelnummers (ook wel voorraadeenheden genoemd \[SKU\]) te gebruiken. De module snel toevoegen wordt toegevoegd aan de winkelwagenpagina van een site.

Voer de volgende stappen uit om een module voor snel toevoegen toe te voegen aan een winkelwagenpagina in Commerce Site Builder.

1. Ga naar **Sjablonen** en selecteer de winkelwagenpaginasjabloon van uw site.
1. Selecteer **Bewerken**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Snel toevoegen** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer de winkelwagenpagina van uw site.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Stel in het eigenschappendeelvenster voor de **Container**-module de eigenschap **Breedte** in op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Snel toevoegen** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

> [!NOTE] 
> De module voor snel toevoegen is beschikbaar vanaf Commerce versie 10.0.17. Als u een oudere versie van Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer instructies.

## <a name="add-a-bulk-purchase-module-to-a-product-details-page"></a>Een module voor bulkaankopen toevoegen aan een pagina met productgegevens

De module voor bulkaankopen op een pagina met productgegevens biedt een op een matrix gebaseerde ervaring waarmee een inkoper snel meerdere varianten van een product aan de winkelwagen kan toevoegen. Als een sitegebruiker meerdere varianten van hetzelfde product moet bestellen, hoeft deze gebruiker nu niet meer de combinatie van productdimensies te selecteren, de hoeveelheid te definiëren, de variant aan de winkelwagen toe te voegen en het proces voor andere vervolgens combinaties van productdimensies te herhalen.

Voer de volgende stappen uit om de module voor bulkaankopen aan een pagina met productgegevens toe te voegen in Commerce Site Builder.

1. Ga naar **Sjablonen** en selecteer de pagina met productgegevens van uw site.
1. Selecteer **Bewerken**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Bulkaankoop** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer de pagina met productgegevens van uw site.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Stel in het eigenschappendeelvenster voor de module **Container** de eigenschap **Breedte** in op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Bulkaankoop** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

> [!NOTE] 
> De module voor bulkaankopen is beschikbaar vanaf Commerce 10.0.24. Als u een oudere versie van Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer instructies.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](../starter-kit-overview.md)

[Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[Overzicht van pagina schrijven](../authoring-home-overview.md)

[Overzicht sjablonen en indelingen](../templates-layouts-overview.md)

[Werken met fragmenten](../work-with-fragments.md)

[Een nieuwe sitepagina toevoegen](../add-new-page.md)

[Kassamodule](../add-checkout-module.md)

[Inhoudsblokkenmodule](../add-hero-module.md)

[Productverzamelingsmodule](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
