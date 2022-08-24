---
title: Gebruikers van zakenpartners op B2B-e-commercewebsite beheren
description: In dit artikel wordt beschreven hoe u gebruikers van zakenpartners op B2B-e-commercewebsites (business-to-business) met Microsoft Dynamics 365 Commerce en in Commerce Headquarters kunt toevoegen, bewerken en verwijderen.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: a59220c16e195ff36980517baec6fb8246a18115
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281167"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Gebruikers van zakenpartners op B2B-e-commercewebsite beheren

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u gebruikers van zakenpartners op B2B-e-commercewebsites (business-to-business) met Microsoft Dynamics 365 Commerce en in Commerce Headquarters kunt toevoegen, bewerken en verwijderen.

> [!NOTE]
> - Het artikel [B2B-zakenpartners beheren met behulp van klanthiërarchieën](partners-customer-hierarchies.md) is een vereiste voor dit document.
> - Zorg ervoor dat u de entiteit Documenttypen in Commerce Headquarters initialiseert door het formulier **Documenttypen** te openen op **Organisatiebeheer \> Documentbeheer \> Documenttypen**.

B2B-e-commercewebsites vereisen dat organisaties zich registreren om zakenpartners te worden. Nadat een organisatie registratiegegevens heeft ingediend bij een B2B-e-commercewebsite, doorloopt de aanvraag voor registratie een kwalificatieproces. Als de organisatie is gekwalificeerd, wordt deze geregistreerd als zakenpartner.

Nadat een organisatie als zakenpartner is geregistreerd, wordt de gebruiker van de organisatie die de aanvraag heeft gestart om een zakenpartner te worden, geïdentificeerd als de beheerdergebruiker en krijgt deze bevoegdheden om extra geautoriseerde gebruikers van de B2B-e-commercewebsite te registreren. Deze geautoriseerde gebruikers kunnen vervolgens orders plaatsen namens de zakenpartner.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>De beheerdergebruiker instellen voor een nieuwe zakenpartner

Potentiële zakenpartners kunnen het onboardingproces voor een B2B-e-commercewebsite starten door een onboardingaanvraag in te dienen via een koppeling op de B2B-website. Ze kunnen vervolgens het aanpasbare formulier gebruiken om de details te leveren die vereist zijn voor ingebruikname en aanmelding. Nadat de aanvraag is ingediend, verschijnt er een bevestigingspagina van de indiening. Als de indiening wordt goedgekeurd, wordt het bedrijf waarvoor de aanvraag is ingediend een zakenpartner en wordt de aanvrager (de gebruiker die de onboardingaanvraag heeft gestart) de beheerdergebruiker voor de zakenpartner.

Volg deze stappen om een aanvraag voor een zakenpartner goed te keuren in Commerce Headquarters.

1. Ga naar **IT retail en commerce \> Distributieplanning**.
1. Voer de taak **P-0001** uit om alle onboardingaanvragen van zakenpartners op te nemen in Commerce Headquarters.
1. Nadat de taak **P-0001** is uitgevoerd, gaat u naar **IT retail en commerce \> Klant** en voert u de taak **Klanten en kanaalaanvragen synchroniseren** uit Nadat deze taak is uitgevoerd, worden de onboardingaanvragen gemaakt als prospects van het type **B2B-prospect** in Commerce Headquarters. 
1. Ga naar **Klanten \> Alle prospects** en selecteer de prospectrecord voor de nieuwe zakenpartner om de pagina met details van de prospect te openen.
1. Selecteer op het tabblad **Algemeen** de optie **Omzetten \> Goedkeuren/afwijzen** om de onboardingaanvraag goed te keuren. Wanneer het bevestigingsbericht wordt weergegeven, bevestigt u dat u wilt doorgaan met het proces en keurt u de aanvraag goed. Het veld **Status** van de prospectrecord wordt gewijzigd in **Goedgekeurd**. Vervolgens wordt een e-mailbericht naar het e-mailadres van de aanvrager verzonden om te bevestigen dat hun organisatie als zakenpartner is goedgekeurd. Er wordt ook een klanthiërarchie gemaakt, waarbij de indiener wordt toegevoegd als beheerder voor de zakenpartner.

    > [!NOTE]
    > Op dit moment wordt de bevestigings-e-mail onmiddellijk ter goedkeuring verzonden. Met de toekomstige Commerce-functionaliteit kan de beheerder de e-mails echter handmatig activeren.

1. Ga naar **IT retail en commerce \> Distributieschema** en voer de taak **1010 (Klanten)** uit om de nieuwe klant- en klanthiërarchierecords in de kanaaldatabase op te nemen.

> [!NOTE]
> Om er zeker van te zijn dat de nieuwe klantrecords naar de kanaaldatabase worden verzonden, moet ten minste één van de adresboeken die aan de klant zijn gekoppeld, worden opgenomen in het klantadresboek dat aan de online winkel is gekoppeld. U kunt dit proces automatiseren door het adresboek te configureren voor de standaardklant van de online winkel, zodat het systeem de waarde van het adresboek naar elke nieuwe klant kopieert.

Nadat de klanthiërarchierecords met de kanaaldatabase zijn gesynchroniseerd, kan de aanvrager zich aanmelden bij de B2B-e-commercewebsite via het e-mailadres dat is opgegeven op het moment van indiening van de aanvraag. Gebruikers kunnen het aanmeldingsproces gebruiken om het wachtwoord voor hun account te definiëren. Zie [Automatische koppeling inschakelen](../identity-record-linking.md) voor informatie over het inschakelen van de Azure Active Directory (Azure AD) B2C-identiteitsproviderrecord die is gekoppeld aan de B2B-klantrecord die is gemaakt bij prospectgoedkeuring.

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>B2B-prospects waarschuwen wanneer ze zijn goedgekeurd of afgewezen

Wanneer u een aanvraag voor onboarding van een B2B-prospect goedkeurt of afwijst, kan automatisch een e-mailmelding naar de prospect worden verzonden.

Volg deze stappen om e-mailmeldingen in Commerce Headquarters in te stellen voor gebeurtenissen van het meldingstype **B2B-prospect goedgekeurd** of **B2B-prospect afgewezen**.

1. Maak e-mailsjablonen voor e-mails die worden verzonden naar prospects wanneer het meldingstype **B2B-prospect goedgekeurd** of **B2B-prospect afgewezen** wordt geactiveerd. Zie [Meldingstypen](../email-templates-transactions.md#notification-types) voor informatie over de tijdelijke aanduidingen die deze meldingstypen ondersteunen. Zie [Een e-mailsjabloon maken](../email-templates-transactions.md#create-an-email-template) voor informatie over het maken van e-mailsjablonen.
1. Voeg de meldingstypen **B2B-prospect goedgekeurd** en **B2B-prospect afgewezen** toe aan uw profiel voor e-mailmeldingen en wijs ze toe aan de e-mailsjablonen die u hebt gemaakt. Zie [Een profiel voor e-mailmeldingen instellen](../email-notification-profiles.md) voor meer informatie over hoe u profielen voor e-mailmeldingen instelt.

## <a name="onboard-additional-business-partner-users"></a>Extra gebruikers van zakenpartners onboarden

De beheerdergebruiker van de zakenpartner kan indien nodig extra gebruikers van de zakenpartner onboarden bij de B2B-e-commercewebsite.

Volg deze stappen om extra gebruikers van zakenpartners bij een B2B-e-commercewebsite te onboarden.

1. Meld u als beheerder aan bij de B2B-e-commercewebsite.
1. Ga naar **Mijn account \> Organisatiegebruikers \> Details weergeven** en selecteer **Een gebruiker toevoegen**.
1. Voer de vereiste informatie in en klik op **Opslaan**. Het status van de nieuwe gebruiker wordt ingesteld op **In behandeling**.

Nadat de taken **P-0001** en **Klanten en kanaalaanvragen synchroniseren** zijn uitgevoerd, wordt er in Commerce Headquarters een klantrecord van het type **Persoon** voor de nieuwe gebruiker gemaakt. Deze klantrecord is ook gekoppeld aan de klanthiërarchierecord van de relevante zakenpartner. Daarnaast wordt er een e-mailbericht verzonden naar het e-mailadres van de nieuwe gebruiker om de gebruiker op de hoogte te stellen dat deze is toegevoegd als gebruiker van de organisatie van de zakenpartner en zich nu kunnen aanmelden bij de B2B-e-commercewebsite.

Voer nu de taak **1010 (Klanten)** uit om de nieuwe gebruiker van de zakenpartner te synchroniseren met de kanaaldatabase.

Nadat de klantrecord is gesynchroniseerd, wordt de status van de gebruiker op de B2B-e-commercewebsite ingesteld op **Actief** en kan de nieuwe gebruiker zich aanmelden bij de B2B-e-commercewebsite via het e-mailadres. Gebruikers kunnen het aanmeldingsproces gebruiken om het wachtwoord voor hun account te definiëren. Zie [Automatische koppeling inschakelen](/dynamics365/commerce/identity-record-linking.md) voor informatie over het inschakelen van de Azure AD B2C-identiteitsproviderrecord die is gekoppeld aan de B2B-klantrecord die is gemaakt in Commerce Headquarters.

## <a name="edit-business-partner-user-details"></a>Gebruikersdetails van zakenpartners bewerken

Als u de details van gebruikers van zakenpartners wilt bewerken, gaat u als volgt te werk.

1. Meld u als beheerder aan bij de B2B-e-commercewebsite.
1. Ga naar **Mijn account \> Organisatiegebruikers \> Details weergeven**, selecteer de knop **Bewerken** (potloodsymbool),breng de vereiste wijzigingen aan en selecteer **Opslaan**. De wijzigingen worden pas van kracht nadat de taken **P-0001**, **Klanten en kanaalaanvragen synchroniseren** en **1010 (Klanten)** zijn uitgevoerd.

## <a name="remove-a-business-partner-user"></a>Een gebruiker van een zakenpartner verwijderen

Een beheerder kan bestaande gebruikers van een organisatie van een zakenpartners zo nodig verwijderen uit de lijst met gebruikers die toegang hebben tot de B2B-e-commercewebsite.
Volg deze stappen om een gebruiker van een zakenpartner te verwijderen.
- Meld u als beheerder aan bij de B2B-e-commercewebsite.
- Ga naar **Mijn account > Organisatiegebruikers \> Details weergeven** en selecteer de knop **Verwijderen** (X-symbool). Wanneer er een bevestigingsbericht wordt weergegeven, bevestigt u dat u de gebruiker wilt verwijderen. De wijziging wordt pas van kracht nadat de taken **P-0001**, **Klanten en kanaalaanvragen synchroniseren** en **1010 (Klanten)** zijn uitgevoerd.

> [!NOTE]
> Wanneer u een gebruiker verwijdert uit de lijst met gebruikers die toegang hebben tot de B2B-e-commercewebsite, wordt de bijbehorende klantrecord uit de klanthiërarchierecord van de zakenpartner verwijderd. De klantrecord zelf wordt echter niet verwijderd uit Commerce Headquarters.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Bestaande klanten onboarden als zakenpartners op de B2B-e-commercewebsite

Beheerders kunnen zakenpartners en gebruikers rechtstreeks in Commerce Headquarters onboarden. Deze mogelijkheid is handig voor het onboarden van uw bestaande zakenpartners op de B2B-e-commercewebsite.

Volg deze stappen om zakenpartners en gebruikers rechtstreeks in Commerce Headquarters te onboarden.

1. Maak of selecteer een klant van het type **Organisatie** om als zakenpartner toe te voegen.
1. Maak of selecteer een klant van het type **Persoon** die u wilt toevoegen als beheerder of gebruiker voor de zakenpartner. Controleer of de primaire adressen aan de klanten zijn gekoppeld. Deze e-mailadressen worden gebruikt voor aanmelding bij de website. 

    > [!NOTE]
    > Er moet een unieke klantrecord kunnen worden gevonden voor gebruikers die zich bij de website moeten kunnen aanmelden. Als meerdere klanten met hetzelfde primaire e-mailadres voor de rechtspersoon zijn gevonden, kan de gebruiker zich niet aanmelden bij de website.

1. Maak een klanthiërarchie-id.
1. Voer in het veld **Naam** een naam in.
1. Voer in het veld **Organisatietype** de klant voor de organisatie van de zakenpartner in.
1. Selecteer op het sneltabblad **Hiërarchie** de optie **Toevoegen**.
1. Selecteer een klant van het type **Persoon** in het veld **Naam**.
1. Selecteer de rol **Beheerder** voor de klant die als beheerder moet worden aangewezen.
1. Herhaal dit proces om meer klanten aan de hiërarchie toe te voegen.

## <a name="additional-information"></a>Aanvullende gegevens

- Alle taken die in dit artikel worden genoemd, kunnen volgens een planning worden uitgevoerd in een batchindeling. De verwachting is dat de zakenpartners indien nodig batchtaken moeten configureren.
- Momenteel kan slechts één gebruikers-/klantrecord worden aangewezen als beheerdergebruiker en deze rol kan alleen worden gewijzigd in Commerce Headquarters. Er is geen ondersteuning voor zelfservicemogelijkheden waarmee zakenpartners meerdere beheerders kunnen aanwijzen of beheerders kunnen wijzigen van B2B-e-commercewebsites.
- Hoewel er bestedingslimieten kunnen worden gedefinieerd voor gebruikers, is het afdwingen van uitgavenlimieten tijdens het orderinvoerproces nog niet geïmplementeerd.
- Alle bedrijfslogica en validatie voor de ervaring van een gebruiker op een B2B-e-commercewebsite zijn gebaseerd op de configuratie van de klantrecord die is toegewezen aan de gebruiker in Commerce Headquarters.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2B-e-commercesite instellen](set-up-b2b-site.md)

[B2B-zakenpartners beheren met behulp van klanthiërarchieën](partners-customer-hierarchies.md)

[De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites](payment-method.md)

[De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites](quantity-limits.md)

[Overzicht van Nummerreeksen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
