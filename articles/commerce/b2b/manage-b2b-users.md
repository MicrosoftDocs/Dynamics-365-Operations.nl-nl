---
title: Gebruikers van zakenpartners op B2B-e-commercewebsite beheren
description: In dit onderwerp wordt beschreven hoe beheerders gebruikers van zakenpartners op B2B-e-commercewebsites (business-to-business) kunnen toevoegen, bewerken en verwijderen.
author: josaw1
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 090dc9af49840e559b4c1ad1500718fde9764aa2
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713688"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Gebruikers van zakenpartners op B2B-e-commercewebsite beheren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe beheerders gebruikers van zakenpartners op B2B-e-commercewebsites (business-to-business) kunnen toevoegen, bewerken en verwijderen.

B2B-e-commercewebsites vereisen dat organisaties zich registreren om zakenpartners te worden. Nadat een organisatie registratiegegevens heeft ingediend bij een B2B-e-commercewebsite, doorloopt de organisatie een kwalificatieproces. Als de organisatie is gekwalificeerd, wordt deze geregistreerd als zakenpartner.

Nadat een organisatie als zakenpartner is geregistreerd, wordt de gebruiker van de organisatie die de aanvraag heeft gestart om een zakenpartner te worden, geïdentificeerd als de beheerdergebruiker en krijgt deze bevoegdheden om extra geautoriseerde gebruikers van de B2B-e-commercewebsite te registreren. Deze geautoriseerde gebruikers kunnen vervolgens orders plaatsen namens de zakenpartner.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>De functie voor de B2B-e-commercemogelijkheden inschakelen in Commerce Headquarters

Met de mogelijkheden van B2B-e-commerce in Commerce Headquarters kunnen organisaties zakenpartners onboarden en beheerdergebruikers definiëren. Met deze functie kunnen beheerders ook gebruikers en teams van zakenpartners maken en beheren en specifieke rollen aan ze toewijzen. Tot slot kunnen van gebruikers van zakenpartners met de functie ordersjablonen maken en bestaande orders gebruiken om producten opnieuw te bestellen.

Als u de functie voor de mogelijkheden van B2B-e-commerce wilt inschakelen in Commerce Headquarters, gaat u als volgt te werk.

1. Ga naar **Werkruimten \> Functiebeheer**.
1. Filter op het tabblad **Alle** op het veld **Module** de functies met de term **Retail en commerce**.
1. Zoek en selecteer de functie met de naam **Het gebruik van B2B e-commercemogelijkheden inschakelen** en selecteer vervolgens **Nu inschakelen**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Een nummerreeks maken en deze toevoegen aan gedeelde Commerce-parameters

Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben. Zie [Overzicht van nummerreeksen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) voor meer informatie over nummerreeksen.

Volg deze stappen om een nummerreeks te maken en deze toe te voegen aan gedeelde Commerce-parameters in Commerce Headquarters.

1. Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Nummerreeksen \> Nummerreeksen** en maak een nummerreeks.
1. Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters** en voeg de nieuwe nummerreeks toe aan de verwijzing **Klanthiërarchie-id**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>De beheerdergebruiker instellen voor een nieuwe zakenpartner

Potentiële zakenpartners kunnen het onboardingproces voor een B2B-e-commercewebsite starten door een onboardingaanvraag in te dienen via een koppeling op de site. Nadat een potentiële gebruiker van een zakenpartner de koppeling heeft geselecteerd, kan deze de details verstrekken die zijn vereist voor het onboarden en aanmelden. Nadat de aanvraag is ingediend, verschijnt er een bevestigingspagina van de indiening. Als de indiening wordt goedgekeurd, wordt de aanvrager (dat wil zeggen de gebruiker die de onboardingaanvraag heeft gestart) de beheerdergebruiker van de zakenpartner.

Volg deze stappen om een beheerdergebruiker van een zakenpartner in Commerce Headquarters in te stellen en goed te keuren.

1. Ga naar **IT retail en commerce \> Distributieplanning**.
1. Voer de taak **P-0001** uit om alle onboardingaanvragen van zakenpartners op te nemen in Commerce Headquarters.
1. Nadat de taak **P-0001** is uitgevoerd, gaat u naar **IT retail en commerce \> Klant** en voert u de taak **Klanten en zakenpartner synchroniseren vanuit de asynchrone modus** uit Nadat deze taak is uitgevoerd, worden de onboardingaanvragen gemaakt als prospectrecords in Commerce Headquarters. Het veld **Type-id** van deze records is ingesteld op **B2B-prospect**.
1. Ga naar **Klanten \> Alle prospects** en open de pagina Prospects.
1. Selecteer de prospectrecord voor de nieuwe zakenpartner om de pagina met details van de prospect te openen.
1. Selecteer op het tabblad **Algemeen** de optie **Omzetten \> Goedkeuren/afwijzen** om de onboardingaanvraag goed te keuren of af te wijzen. Wanneer er een bevestigingsbericht wordt weergegeven, bevestigt u dat u wilt doorgaan met het proces en keurt u de aanvraag goed. Vervolgens wordt een e-mailbericht naar het e-mailadres van de aanvrager verzonden om te bevestigen dat hun organisatie als zakenpartner is goedgekeurd.

    Nadat u de aanvraag hebt goedgekeurd, wordt het veld **Status** van de prospectrecord ingesteld op **Goedgekeurd**. Daarnaast worden er twee nieuwe klantrecords in het systeem gemaakt: een klantrecord **Organisatietype** voor de organisatie van de zakenpartner en een klantrecord **Type persoon** voor de aanvrager. Er wordt ook een klanthiërarchierecord voor de zakenpartner gemaakt. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Ga naar **IT retail en commerce \> Distributieschema** en voer de taak **1010** (**Klanten**) uit om de nieuwe klant- en klanthiërarchierecords in de kanaaldatabase op te nemen.

Nadat de aanvraag is goedgekeurd en de klant- en klanthiërarchierecords met de kanaaldatabase zijn gesynchroniseerd, kan de aanvrager zich aanmelden bij de B2B-e-commercewebsite via het e-mailadres dat zij hebben opgegeven op het moment dat ze de aanvraag indienden. Gebruikers kunnen het aanmeldingsproces gebruiken om het wachtwoord voor hun account te definiëren. Als u wilt dat de identiteitsprovider (Azure AD B2C)-record wordt gekoppeld aan de B2B-klantrecord die is gemaakt bij het registreren of aanmelden, volgt u de instructies in [Automatisch koppelen van identiteitsrecords aan klantrekeningen inschakelen](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>B2B-prospects waarschuwen wanneer ze zijn goedgekeurd of afgewezen

Wanneer u een aanvraag voor onboarding van een B2B-prospect goedkeurt of afwijst, kunt u automatisch een e-mailmelding naar de prospect verzenden. 

Volg deze stappen om e-mailmeldingen in Commerce Headquarters in te stellen voor gebeurtenissen van het meldingstype B2B-prospect goedgekeurd of B2B-prospect afgewezen.

1. Maak e-mailsjablonen voor e-mails die worden verzonden naar prospects wanneer het meldingstype B2B-prospect goedgekeurd of B2B-prospect afgewezen wordt geactiveerd.

    Zie [Meldingstypen](../email-templates-transactions.md#notification-types) voor informatie over de tijdelijke aanduidingen die de meldingstypen B2B-prospect goedgekeurd en B2B-prospect afgewezen ondersteunen. Zie [Een e-mailsjabloon maken](../email-templates-transactions.md#create-an-email-template) voor informatie over het maken van e-mailsjablonen. 

1. Voeg de meldingstypen B2B-prospect goedgekeurd en B2B prospect afgewezen toe aan uw profiel voor e-mailmeldingen en wijs ze toe aan de e-mailsjablonen die u hebt gemaakt. Zie [Een profiel voor e-mailmeldingen instellen](../email-notification-profiles.md) voor meer informatie over hoe u profielen voor e-mailmeldingen instelt. 

## <a name="onboard-additional-business-partner-users"></a>Extra gebruikers van zakenpartners onboarden

De beheerdergebruiker van de zakenpartner kan indien nodig extra gebruikers van de zakenpartner onboarden bij de B2B-e-commercewebsite.

Volg deze stappen om extra gebruikers van zakenpartners bij een B2B-e-commercewebsite te onboarden.

1. Meld u als beheerder aan bij de B2B-e-commercewebsite.
1. Ga naar **Mijn account \> Organisatiegebruikers \> Details weergeven** en selecteer **Een gebruiker toevoegen**.
1. Voer de vereiste informatie in en klik op **Opslaan**. Het status van de nieuwe gebruiker wordt ingesteld op **In behandeling**.

    Nadat de taken **P-0001** en **Klanten en zakenpartner synchroniseren vanuit de asynchrone modus** zijn uitgevoerd, wordt er in Commerce Headquarters een klantrecord **Type persoon** voor de nieuwe gebruiker gemaakt. Deze klantrecord is ook gekoppeld aan de klanthiërarchierecord van de relevante zakenpartner. Daarnaast wordt er een e-mailbericht verzonden naar het e-mailadres van de nieuwe gebruiker om de gebruiker op de hoogte te stellen dat deze is toegevoegd als gebruiker van de organisatie van de zakenpartner en zich nu kunnen aanmelden bij de B2B-e-commercewebsite.

1. Voer de taak **1010** (**Klanten**) uit om de nieuwe gebruiker van de zakenpartner te synchroniseren met de kanaaldatabase.

Nadat de klantrecord is gesynchroniseerd, wordt de status van de gebruiker op de B2B-e-commercewebsite ingesteld op **Actief** en kan de nieuwe gebruiker zich aanmelden bij de B2B-e-commercewebsite via het e-mailadres. Gebruikers kunnen het aanmeldingsproces gebruiken om het wachtwoord voor hun account te definiëren. Als u wilt dat de identiteitsprovider (Azure AD B2C)-record wordt gekoppeld aan de B2B-klantrecord die is gemaakt bij het registreren of aanmelden, volgt u de instructies in [Automatisch koppelen van identiteitsrecords aan klantrekeningen inschakelen](../identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Gebruikersdetails van zakenpartners bewerken

Als u de details van gebruikers van zakenpartners wilt bewerken, gaat u als volgt te werk.

1. Meld u als beheerder aan bij de B2B-e-commercewebsite.
1. Ga naar **Mijn account \> Organisatiegebruikers \> Details weergeven**, selecteer de knop **Bewerken** (potloodsymbool),breng de vereiste wijzigingen aan en selecteer **Opslaan**. De wijzigingen worden pas van kracht nadat de taken **P-0001**, **Klanten en zakenpartner synchroniseren vanuit de asynchrone modus** en **1010** (**Klanten**) zijn uitgevoerd.

## <a name="remove-a-business-partner-user"></a>Een gebruiker van een zakenpartner verwijderen

Een beheerder kan bestaande gebruikers van een organisatie van een zakenpartners zo nodig verwijderen uit de lijst met gebruikers die toegang hebben tot de B2B-e-commercewebsite.

Volg deze stappen om een gebruiker van een zakenpartner te verwijderen.

1. Meld u als beheerder aan bij de B2B-e-commercewebsite.
1. Ga naar **Mijn account \> Organisatiegebruikers \> Details weergeven** en selecteer de knop **Verwijderen** (X-symbool). Wanneer er een bevestigingsbericht wordt weergegeven, bevestigt u dat u de gebruiker wilt verwijderen. De wijziging wordt pas van kracht nadat de taken **P-0001**, **Klanten en zakenpartner synchroniseren vanuit de asynchrone modus** en **1010** (**Klanten**) zijn uitgevoerd.

> [!NOTE]
> Wanneer u een gebruiker verwijdert uit de lijst met gebruikers die toegang hebben tot de B2B-e-commercewebsite, wordt de bijbehorende klantrecord uit de klanthiërarchierecord van de zakenpartner verwijderd. De klantrecord zelf wordt echter niet verwijderd uit Commerce Headquarters.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Zakenpartner en gebruikers onboarden in Commerce Headquarters

Beheerders kunnen zakenpartners en gebruikers rechtstreeks in Commerce Headquarters onboarden.

Volg deze stappen om zakenpartners en gebruikers rechtstreeks in Commerce Headquarters te onboarden.

1. Maak een klantrecord **Organisatietype** voor de organisatie van de organisatie van de zakenpartner.
1. Maak klantrecords **Type persoon** voor gebruikers van zakenpartners. Zorg ervoor dat er voor elke klant een primair e-mailadres is opgegeven.
1. Stel voor elke klantrecord **Type persoon** die moet worden aangewezen als beheerdergebruiker van de organisatie van de zakenpartner op het sneltabblad **Retail** de optie **B2B-beheerder** in op **Ja**.
1. Maak een klanthiërarchie-id. Voer in het veld **Naam** een naam in.
1. Voer in het veld **Organisatietype** de klant voor de organisatie van de zakenpartner in.
1. Selecteer **Toevoegen** en selecteer vervolgens een klant in het veld **Naam**.
1. Herhaal dit proces om extra klanten aan de hiërarchie toe te voegen.

## <a name="additional-information"></a>Aanvullende gegevens

- Alle taken die in dit onderwerp worden genoemd, kunnen volgens een planning worden uitgevoerd in een batchindeling. De verwachting is dat de zakenpartners indien nodig batchtaken moeten configureren.
- Momenteel kan slechts één gebruikers-/klantrecord worden aangewezen als beheerdergebruiker en deze rol kan alleen worden gewijzigd in Commerce Headquarters. Er is geen ondersteuning voor zelfservicemogelijkheden waarmee zakenpartners meerdere beheerders kunnen aanwijzen of beheerders kunnen wijzigen van B2B-e-commercewebsites.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Hoewel er bestedingslimieten kunnen worden gedefinieerd voor gebruikers, is het afdwingen van uitgavenlimieten tijdens het orderinvoerproces nog niet geïmplementeerd.
- Alle bedrijfslogica en validatie voor de ervaring van een gebruiker op een B2B-e-commercewebsite zijn gebaseerd op de configuratie van de klantrecord die is toegewezen aan de gebruiker in Commerce Headquarters.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2B-e-commercesite instellen](set-up-b2b-site.md)

[Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken](org-model.md)

[De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites](payment-method.md)

[De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites](quantity-limits.md)

[Overzicht van Nummerreeksen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
