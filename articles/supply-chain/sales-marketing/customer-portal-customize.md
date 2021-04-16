---
title: De klantportal aanpassen en gebruiken
description: In dit onderwerp wordt uitgelegd hoe u de klantportal aanpast nadat deze aan uw systeem is toegevoegd.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 16d5c13c0fbff8c5033b0d1e9dd0d07851521126
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840768"
---
# <a name="customize-and-use-the-customer-portal"></a>De klantportal aanpassen en gebruiken

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de verschillende pagina's beschreven die standaard beschikbaar zijn in de klantportal. Hierin wordt uitgelegd wat u met de pagina's kunt doen en hoe u deze kunt aanpassen.

De klantportal bevat een paar webpagina's en standaard acties. Het volgende siteoverzicht bevat die webpagina's en acties, en de rollen waarmee de acties kunnen worden uitgevoerd.

![Siteoverzicht van klantportal](media/customer-portal-site-map.png "Siteoverzicht van klantportal")

## <a name="typical-customizations"></a>Standaard aanpassingen

In de volgende onderwerpen vindt u informatie over Power Apps-portals en hoe u portals kunt aanpassen:

- [Werken met sjablonen](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates): dit onderwerp biedt een algemeen overzicht van de werking van Power Apps-portals en over hoe u portals eenvoudig kunt aanpassen.
- [Portalinhoud beheren](https://docs.microsoft.com/dynamics365/portals/manage-portal-content): in dit onderwerp wordt uitgelegd hoe u de inhoud die u in uw portal opneemt, kunt beheren en aanpassen.
- [CSS bewerken](https://docs.microsoft.com/powerapps/maker/portals/edit-css): hier vindt u informatie over het aanbrengen van meer complexe aanpassingen in de gebruikersinterface van uw portal.
- [Een thema maken voor uw portal](https://docs.microsoft.com/dynamics365/portals/create-theme): hier vindt u informatie over het maken van een UI-thema voor uw portal.
- [De portalinhoud eenvoudig maken en publiceren](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content): hier vindt u informatie over het beheren van de onderliggende gegevens en tabellen die u gebruikt voor uw portal.
- [Een contactpersoon configureren voor gebruik in een portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts): in dit onderwerp wordt uitgelegd hoe u gebruikersrollen maakt en aanpast, en hoe beveiliging en verificatie in Power Apps-portals worden uitgevoerd.
- [Notities voor tabelformulieren en webformulieren configureren in portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes): in dit onderwerp wordt uitgelegd hoe u documenten en extra opslagruimte aan uw portal toevoegt.
- [Foutafhandeling voor portalwebsite](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log): in dit onderwerp wordt uitgelegd hoe u foutlogboeken voor portals kunt weergeven en in uw Microsoft Azure-blobopslagaccount kunt opslaan.

## <a name="customize-the-order-creation-process"></a>Het proces voor het maken van orders aanpassen

Wanneer een gebruiker een order indient via de klantportal, wordt de order automatisch gesynchroniseerd met de bijbehorende Dynamics 365 Supply Chain Management-omgeving. Omdat de gebruiker een externe klant is, is bepaalde vereiste informatie opzettelijk verborgen. Deze informatie wordt automatisch ingevuld wanneer het formulier wordt ingediend.

In deze sectie wordt beschreven hoe u contactpersonen kunt instellen om fouten te voorkomen. U vindt informatie over de velden die automatisch worden ingesteld en hoe u de waarde van deze velden kunt wijzigen als dat nodig is.

### <a name="the-out-of-box-order-creation-process"></a>Het standaardproces voor het maken van orders

Dit zijn de standaard stappen voor het indienen van een order vanuit de klantportal.

1. Selecteer op de startpagina de tegel **Order maken** om de wizard **Order maken** te openen.
1. Stel op de pagina **Ordergegevens** de volgende velden in:

    - **Gevraagde ontvangstdatum**: geef de datum van de levering op.
    - **Afleveradres**: voer het adres in waar de order moet worden geleverd.
    - **Bedrijf**: selecteer de naam van het bedrijf van de klant. Dit veld wordt automatisch ingesteld voor gebruikers die geen beheerder zijn.
    - **Bestelnummer**: voer het bestelnummer van de order in. Dit veld is niet verplicht.
    - **Land/regio van verzending**: voer het land of de regio in waarnaar de artikelen worden geleverd. Dit veld wordt automatisch ingesteld voor gebruikers die geen beheerder zijn.

    ![Pagina Ordergegevens](media/customer-portal-order-information.png "Pagina Ordergegevens")

1. Selecteer **Volgende**.
1. Selecteer op de pagina **Artikelen** de optie **Artikel toevoegen**.

    ![Pagina Artikelen](media/customer-portal-items.png "Pagina Artikelen")

1. Stel in het dialoogvenster **Artikelgegevens** de volgende velden in:

    - **Productnaam**: een product zoeken en selecteren dat u aan de order wilt toevoegen.
    - **Hoeveelheid**: voer de hoeveelheid van het geselecteerde product in.
    - **Eenheid**: geef de maateenheid op (bijvoorbeeld **stuks**, **kg** of **doos**).
    - **Geraamd nettobedrag**: de waarde wordt berekend als de geschatte prijs van het artikel × de hoeveelheid voor de geselecteerde eenheid.

    ![Dialoogvenster Artikelgegevens](media/customer-portal-item-information.png "Dialoogvenster Artikelgegevens")

1. Selecteer **Indienen** om het artikel aan de order toe te voegen.
1. Herhaal stap 4 tot en met 6 totdat u alle artikelen hebt toegevoegd die u wilt bestellen.
1. Wanneer u klaar bent met het toevoegen van artikelen, selecteert u **Volgende** op de pagina **Artikelen**.
1. De pagina **Ordergegevens** biedt een overzicht van de order. Controleer de inhoud van de order en de leveringsgegevens. Als alles correct lijkt, selecteert u **Indienen** om de order in te dienen.

    ![Pagina Ordergegevens](media/customer-portal-order-submit.png "Pagina Ordergegevens")

### <a name="standard-data-setup"></a>Standaardgegevens instellen

Voor een soepele gebruikerservaring worden in de klantportal automatisch waarden ingevuld voor verschillende vereiste velden. Deze waarden zijn gebaseerd op informatie in de contactpersoonrecord van de klant die de order indient.

Voor elke [contactpersoonrij](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) die hoort bij een klant die de klantportal gebruikt om orders te verzenden, moeten er waarden worden opgegeven voor de volgende vereiste velden. Anders worden er fouten weergegeven.

- **Bedrijf**: de rechtspersoon waarbij de order hoort
- **Potentiële klant**: de klantrekening die aan de geselecteerde order is gekoppeld.
- **Prijslijst**: de aangepaste prijslijst voor de klant
- **Valuta**: de valuta van de prijs
- **Land/regio van verzending**: het land of de regio waarnaar de artikelen worden geleverd

De volgende velden worden automatisch ingesteld voor de tabel met de verkooporder:

- **Taal**: de taal van de order (standaard wordt de waarde uit de contactpersoonrecord opgehaald.)
- **Land/regio van verzending**: het land of de regio waar de artikelen worden geleverd (standaard wordt de waarde uit de contactpersoonrecord gehaald.)
- **Contactpersoon**: de gebruiker die contact kan maken met informatie over de order (standaard wordt de waarde uit de contactpersoonrecord gehaald.)
- **Bedrijf**: de rechtspersoon waarbij de order hoort (standaard wordt de waarde uit de contactpersoonrecord gehaald.)
- **Potentiële klant**: de klantrekening die aan de order is gekoppeld (standaard wordt de waarde uit de contactpersoonrecord gehaald.)
- **Te factureren klant**: het te factureren account van de order (standaard wordt de waarde uit de contactpersoonrecord gehaald.)
- **Naam verkooporder**: de naam van de verkooporder (de standaardwaarde is **verkooporder**.)
- **Valuta**: de valuta van de prijs (standaard wordt de waarde uit de contactpersoonrecord opgehaald.)
- **Prijslijst**: de aangepaste prijslijst voor de klant (standaard wordt de waarde uit de contactpersoonrecord opgehaald.)
- **Omschrijving afleveradres**: het afleveradres van de verkooporder (de standaardwaarde is **omschrijving leveringsadres** .)

### <a name="modify-the-order-creation-process"></a>Het proces voor het maken van orders wijzigen

U kunt de weergave en de gebruikersinterface van de klantportal wijzigen als u het basisproces voor het maken van de order niet wijzigt. Als u het proces voor het maken van orders wilt wijzigen, moet u rekening houden met een aantal punten.

Verwijder de volgende kolommen niet uit de tabel met de verkooporder in Microsoft Dataverse, omdat deze zijn vereist om een verkooporder te maken voor twee keer wegschrijven:

- **Bedrijf**: de rechtspersoon waarbij de order hoort
- **Naam**: de naam van de verkooporder
- **Valuta**: de valuta van de prijs
- **Prijslijst**: de aangepaste prijslijst voor de klant
- **Land/regio van verzending**: het land of de regio waarnaar de artikelen worden geleverd
- **Potentiële klant**: de klantrekening die aan de geselecteerde order is gekoppeld.
- **Taal**: de taal van de order (meestal is dit de taal van de potentiële klant.)
- **Omschrijving afleveradres**: het afleveradres van de verkooporder

Voor artikelen zijn de volgende kolommen vereist:

- **Product**: het product dat u wilt bestellen
- **Hoeveelheid**: de hoeveelheid van het geselecteerde product
- **Eenheid**: de maateenheid (bijvoorbeeld **stuks**, **kg** of **doos**)
- **Land/regio van verzending**: het land of de regio van levering
- **Omschrijving afleveradres**: het afleveradres van de order

U moet ervoor zorgen dat uw klantportal waarden voor al deze kolommen bevat.

Zie [Formulieren voor snel maken aanmaken of bewerken voor een gestroomlijnde gegevensinvoer](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms) als u kolommen aan de pagina wilt toevoegen of kolommen wilt verwijderen.

Zie de volgende informatie in de documentatie over Power Apps-portals als u de manier wilt wijzigen waarop de kolommen worden ingesteld en hoe waarden worden ingesteld wanneer de pagina wordt opgeslagen:

- [Veld vooraf invullen](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Waarde instellen bij opslaan](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>De startpagina aanpassen

Alle besturingselementen in de klantportal zijn ingebouwde besturingselementen voor Power Apps-portals. U kunt deze aanpassen door de stappen uit te voeren in [Een pagina samenstellen](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in de documentatie voor Power Apps-portals.

Het enige aangepaste besturingselement dat in de sjabloon voor de klantportal is opgenomen, wordt gebruikt om de tegels op de startpagina te maken.

![Tegels op de startpagina](media/customer-portal-home-page-tiles.png "Tegels op de startpagina")

Volg deze stappen om de tegels te wijzigen.

1. Open de [Portalbeheer-app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).
1. Selecteer **Paginasjablonen** in het navigatievenster aan de linkerkant.

    ![Navigatievenster van portalbeheer](media/customer-portal-nav.png "Navigatievenster van portalbeheer")

1. Selecteer de paginasjabloon met de **Home**.
1. Selecteer in het veld **Websjabloon** de koppeling **Home** om de broncode voor die pagina te openen.

    ![Veld Websjabloon](media/customer-portal-web-template.png "Veld Websjabloon")

1. U ziet nu alle broncode voor de startpagina en kunt deze naar wens wijzigen.

## <a name="resources"></a>Bronnen

Zie de volgende bronnen voor meer informatie over hoe u de klantportal kunt instellen en aanpassen:

- [Documentatie over Power Apps-portals](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Documentatie over twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Informatie over Portallevenscyclus](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Een portal bijwerken](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portalconfiguratie migreren](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 voor Customer Engagement-apps](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]