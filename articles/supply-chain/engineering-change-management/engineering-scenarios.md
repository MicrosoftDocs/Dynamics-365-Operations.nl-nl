---
title: De functies van Technisch wijzigingsbeheer
description: Dit onderwerp biedt een end-to-end-overzicht waarin wordt aangegeven hoe u met Technisch wijzigingsbeheer kunt werken.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b6270bbb6780786ed4535ca2987ed44448bd81ad
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425903"
---
# <a name="engineering-change-management-feature-walkthrough"></a>De functies van Technisch wijzigingsbeheer

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een end-to-end-overzicht waarin wordt aangegeven hoe u met Technisch wijzigingsbeheer kunt werken. U doorloopt de belangrijkste scenario's:

- Basisconfiguratie van functies
- Hoe een technisch bedrijf een nieuw technisch product maakt
- Hoe een technisch bedrijf een technisch product vrijgeeft aan een lokaal bedrijf
- Hoe een lokaal bedrijf een product kan beoordelen en accepteren dat door een technisch bedrijf is vrijgegeven
- Hoe een lokaal bedrijf een technisch product kan gebruiken in standaardtransacties
- Hoe u een technisch product toevoegt aan een verkooporder
- Hoe u om wijzigingen in een technisch product vraagt door een aanvraag voor technische wijzigingen te maken
- Hoe u aangevraagde wijzigingen plant en implementeert door een order voor technische wijzigingen te maken
- Hoe u een gewijzigd product vrijgeeft

Alle oefeningen in dit onderwerp gebruiken de standaardvoorbeeldgegevens voor Microsoft Dynamics 365 Supply Chain Management. Elke oefening borduurt voort op de vorige oefening. Daarom wordt u aangeraden de oefeningen op volgorde te doorlopen, van begin tot einde, met name als u de functie voor het beheer van technische wijzigingen nog nooit eerder hebt gebruikt. Op deze manier krijgt u een compleet beeld van de functie.

## <a name="set-up-for-the-sample-scenario"></a>Instellen voor het voorbeeldscenario

Als u het voorbeeldscenario wilt volgen dat in dit onderwerp wordt gegeven, moet u eerst de functie voorbereiden door demogegevens beschikbaar te maken en een paar aangepaste records toe te voegen.

Voordat u een van de oefeningen in de rest van dit onderwerp probeert uit te voeren, volgt u de instructies in de volgende subsecties. In deze subsecties worden ook verschillende belangrijke instellingspagina's geïntroduceerd die u kunt gebruiken wanneer u technisch wijzigingsbeheer instelt voor uw organisatie.

### <a name="make-standard-demo-data-available"></a>Standaarddemogegevens beschikbaar maken

Werk op een systeem waarop de [standaarddemogegevens zijn geïnstalleerd](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). De standaarddemogegevens voegen gegevens toe voor verschillende demorechtspersonen (bedrijven en organisaties). Terwijl u de oefeningen doorloopt, gebruikt u de bedrijfskiezer aan de rechterkant van de navigatiebalk om te schakelen tussen een bedrijf (*DEMF*) dat is ingesteld als een *technische organisatie* en een ander bedrijf (*USMF*) dat is ingesteld als *operationele organisatie*.

### <a name="set-up-an-engineering-organization"></a>Een technische organisatie instellen

Een technische organisatie is eigenaar van de technische gegevens en is verantwoordelijk voor productontwerp en productwijzigingen. Ga als volgt te werk om uw technische organisatie in te stellen.

1. Ga naar **Technisch wijzigingsbeheer &gt; Instellen &gt; Technische organisaties**.
1. Selecteer **Nieuw** om een rij toe te voegen aan het raster en stel de volgende waarden in:

    - **Engineeringorganisatie:** *DEMF*
    - **Naam van organisatie:** *Contoso Entertainment System Duitsland*

    ![Een technische organisatie toevoegen](media/engineering-org.png "Een technische organisatie toevoegen")

### <a name="set-up-the-version-product-dimension-group"></a>De productdimensiegroep voor de versie instellen

1. Ga naar **Productgegevensbeheer &gt; Instellen &gt; Dimensie- en variantgroepen &gt; Productdimensiegroepen**.
1. Selecteer **Nieuw** om een productdimensiegroep te maken.
1. Stel het veld **Naam** in op *Versie*.
1. Selecteer **Opslaan** om de nieuwe dimensie op te slaan en waarden naar het sneltabblad **Productdimensies** te laden.
1. Op sneltabblad **Productdimensies** stelt u **Versie** in als een actieve productdimensie.

    ![Een productdimensiegroep toevoegen](media/product-dimension-groups.png "Een productdimensiegroep toevoegen")

### <a name="set-up-product-lifecycle-states"></a>Statussen van productlevenscyclus instellen

Omdat een technisch product een levenscyclus loopt, is het van belang dat u kunt bepalen welke transacties zijn toegestaan voor elke levenscyclusstatus. Voer de onderstaande stappen uit om de verschillende statussen van de productlevenscyclus in te stellen.

1. Ga naar **Technisch wijzigingsbeheer &gt; Instellen &gt; Levenscyclusstatus van product**.
1. Selecteer **Nieuw** om een levenscyclusstatus toe te voegen en stel de volgende waarden in:

    - **Status:** *Operationeel*
    - **Beschrijving:** *Operationeel*

1. Selecteer **Opslaan** om de nieuwe levenscyclusstatus op te slaan en waarden naar het sneltabblad **Ingeschakelde bedrijfsprocessen** te laden.
1. Selecteer op het sneltabblad **Ingeschakelde bedrijfsprocessen** de bedrijfsprocessen die beschikbaar moeten zijn. Laat voor dit voorbeeld het veld **Beleid** ingesteld op *Ingeschakeld* voor alle bedrijfsprocessen.

    ![Bedrijfsprocessen voor een levenscyclusstatus inschakelen](media/product-lifecycle-states-1.png "Bedrijfsprocessen voor een levenscyclusstatus inschakelen")

1. Selecteer **Nieuw** om nog een levenscyclusstatus toe te voegen en stel de volgende waarden in:

    - **Status:** *Prototype*
    - **Beschrijving:** *Prototype*

1. Selecteer **Opslaan** om de nieuwe levenscyclusstatus op te slaan en waarden naar het sneltabblad **Ingeschakelde bedrijfsprocessen** te laden.
1. Selecteer op het sneltabblad **Ingeschakelde bedrijfsprocessen** de bedrijfsprocessen die beschikbaar moeten zijn. Stel voor dit voorbeeld het veld **Beleid** in op *Ingeschakeld met waarschuwing* voor alle bedrijfsprocessen.

    ![Bedrijfsprocessen voor een levenscyclusstatus inschakelen (met waarschuwingen)](media/product-lifecycle-states-2.png "Bedrijfsprocessen voor een levenscyclusstatus inschakelen (met waarschuwingen)")

### <a name="set-up-a-version-number-rule"></a>Een versienummerregel instellen

1. Ga naar **Technisch wijzigingsbeheer &gt; Instellen &gt; Regel voor productversienummer**.
1. Selecteer **Nieuw** om een regel toe te voegen en stel de volgende waarden in:

    - **Naam:** *Auto*
    - **Nummerregel:** *Auto*
    - **Indeling:** *V-\#\#*

    ![Een regel voor een productversienummer toevoegen](media/version-number-rule.png "Een regel voor een productversienummer toevoegen")

### <a name="set-up-a-product-release-policy"></a>Een beleid voor productvrijgave instellen

1. Ga naar **Technisch wijzigingsbeheer &gt; Instellen &gt; Vrijgavebeleid voor producten**.
1. Selecteer **Nieuw** om een vrijgavebeleid toe te voegen en stel de volgende waarden in:

    - **Naam:** *Onderdelen*
    - **Beschrijving:** *Onderdelen*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Producttype:** *Artikel*
    - **Sjablonen Toepassen:** *Altijd*
    - **Actief:** *Ja*

1. Selecteer **Alle producten** op het sneltabblad **Toevoegen** om een regel toe te voegen en stel de volgende waarden voor de regel in:

    - **Bedrijf:** *DEMF*
    - **Sjabloon vrijgegeven product:** *D0006*

1. Selecteer **Toevoegen** om nog een regel toe te voegen en stel de volgende waarden in:

    - **Bedrijfsrekening-ID:** *USMF*
    - **Sjabloon vrijgegeven product:** *D0006*
    - **Stuklijst ontvangen:** schakel dit selectievakje in.
    - **Goedkeuring van stuklijst kopiëren:** schakel dit selectievakje in.
    - **Activering van stuklijst kopiëren:** schakel dit selectievakje in.
    - **Route ontvangen:** schakel dit selectievakje in.
    - **Goedkeuring van route kopiëren:** schakel dit selectievakje in.
    - **Activering van route kopiëren:** schakel dit selectievakje in.

    ![Een beleid voor productvrijgave toevoegen](media/product-release-policy.png "Een beleid voor productvrijgave toevoegen")

### <a name="set-up-an-engineering-product-category"></a>Een categorie voor technische producten instellen 

Categorieën van technische producten vormen de basis voor het maken van technische producten (producten waarvoor versiebeheer wordt uitgevoerd en die worden beheerd via Technisch wijzigingsbeheer). Ga als volgt te werk om categorieën van technische producten in te stellen.

1. Ga naar **Technisch wijzigingsbeheer &gt; Details van categorieën voor technische producten**.
1. Selecteer **Nieuw** om een categorie te maken.
1. Stel op het sneltabblad **Details** de volgende waarden in:

    - **Naam:** *Onderdelen*
    - **Engineeringorganisatie:** *DEMF*
    - **Producttype:** *Artikel*
    - **Versie in transacties traceren:** *Ja*
    - **Productdimensiegroep:** *Versie*
    - **Levenscyclusstatus van product bij maken:** *Operationeel*
    - **Versienummerregel:** *Auto*
    - **Geldigheid afdwingen:** *Nee*
    - **Regelnomenclatuur voor nummer gebruiken:** *Nee*
    - **Regelnomenclatuur voor naam gebruiken:** *Nee*
    - **Regelnomenclatuur voor beschrijving gebruiken:** *Nee*

1. Stel op het sneltabblad **Vrijgavebeleid** het veld **Beleid voor productvrijgave** in op *Onderdelen*.
1. Selecteer **Opslaan**.

    ![Een categorie voor technische producten toevoegen](media/product-category-details.png "Een categorie voor technische producten toevoegen")

### <a name="set-up-product-acceptance-conditions"></a>Voorwaarden voor productacceptatie instellen

1. Gebruik de bedrijfskiezer aan de rechterkant van de navigatiebalk om over te schakelen naar de rechtspersoon (het bedrijf) *USMF*.
1. Ga naar **Technisch wijzigingsbeheer &gt; Instellen &gt; Parameters voor technisch wijzigingsbeheer**.
1. Stel op het tabblad **Vrijgavebeheer** in de sectie **Acceptatie van producten** het veld **Acceptatie van producten** in op *Handmatig*.

    ![Voorwaarden voor productacceptatie instellen](media/engineering-change-management-parameters.png "Voorwaarden voor productacceptatie instellen")

## <a name="create-a-new-engineering-product"></a>Een nieuw technisch product maken

Een technisch product is een product waarvoor versiebeheer wordt uitgevoerd en dat wordt beheerd via Technisch wijzigingsbeheer. Met andere woorden, u kunt de wijzigingen tijdens de levensduur beheren en de wijzigingsgegevens worden opgeslagen via orders voor technische wijzigingen. Volg deze stappen om technische producten te maken.

1. Zorg ervoor dat u zich in de rechtspersoon van uw technische organisatie bevindt (*DEMF* voor dit voorbeeld). Gebruik zo nodig de bedrijfskiezer rechts op de navigatiebalk.
1. Open de pagina **Vrijgegeven producten** door een van deze stappen uit te voeren:

    - Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.
    - Ga naar **Technisch wijzigingsbeheer &gt; Algemeen &gt; Vrijgegeven producten**.

1. Selecteer **Technisch product** in de groep **Nieuw** op het tabblad **Product** in het actievenster.
1. Stel in het dialoogvenster **Nieuw product** de volgende waarden in:

    - **Categorie voor technische producten:** *Onderdelen*
    - **Productnummer:** *Z0001*
    - **Productnaam:** *Luidsprekerset*

    ![Een technische product toevoegen](media/new-product-dialog.png "Een technische product toevoegen")

    Het veld **Versie** wordt automatisch ingesteld op basis van de regel voor productversienummers die u eerder hebt ingesteld.

1. Selecteer **OK** om het product te maken en het dialoogvenster te sluiten.
1. De pagina met details voor het nieuwe product wordt geopend. De waarden zijn al ingevuld voor sommige velden, zoals **Opslagdimensiegroep**, **Traceringsdimensiegroep** en/of **Artikelmodelgroep**. Deze velden zijn automatisch ingesteld omdat het product wordt vrijgegeven in de rechtspersoon *DEMF* en gebruikmaakt van het beleid voor productvrijgave *Onderdelen*, dat is gekoppeld aan de categorie *Onderdelen* voor technische producten. Omdat u eerder artikel *D0006* hebt gebruikt als sjabloon voor het instellen van een regel voor de rechtspersoon *DEMF*, zijn de ingevulde waarden overgenomen uit artikel *D0006*.

    ![Vrijgegeven productdetails](media/product-details.png "Vrijgegeven productdetails")

1. Selecteer in het actievenster op het tabblad **Technicus** in de groep **Technisch wijzigingsbeheer** de optie **Technische versies** om de versies van het product weer te geven.

    ![Engineeringversies](media/engineering-versions-list.png "Engineeringversies")

1. Op de pagina **Technische versies** ziet u dat er slechts één versie voor het product is en dat deze actief is.
1. Selecteer de versie om de details weer te geven.

    ![Details van technische versie](media/engineering-version-details.png "Details van technische versie")

1. Selecteer **Stuklijst maken** op het sneltabblad **Stuklijst** van de pagina **Technische versie**.
1. Stel in het dialoogvenster **Stuklijst maken** de volgende waarden in:

    - **Stuklijstnummer:** Z0001
    - **Naam:** Luidsprekerset
    - **Locatie:** 1

    ![Een BOM maken](media/create-bom.png "Een BOM maken")

1. Selecteer **OK** om de stuklijst toe te voegen en het dialoogvenster te sluiten.
1. Selecteer **Stuklijst** op het sneltabblad **Stuklijst**.
1. Voeg op de pagina **Stuklijst** op het sneltabblad **Stuklijstregels** drie regels toe, één elk voor de artikelnummers *D0001*, *D0003* en *D0006*.

    ![Stuklijstregels toevoegen](media/bom.png "Stuklijstregels toevoegen")

1. Selecteer **Opslaan**.
1. Sluit de pagina.
1. Selecteer **Goedkeuren** op het sneltabblad **Stuklijst** van de pagina **Technische versie**.
1. Selecteer in het dialoogvenster dat verschijnt **OK**.

    ![De stuklijst goedkeuren](media/approve-dialog.png "De stuklijst goedkeuren")

1. Selecteer **Activeren** op het sneltabblad **Stuklijst** van de pagina **Technische versie**.
1. Zoals u ziet zijn de selectievakjes **Actief** en **Goedgekeurd** ingeschakeld voor de stuklijst.

    ![Actieve en goedgekeurde stuklijst](media/approved-bom.png "Actieve en goedgekeurde stuklijst")

1. Sluit de pagina.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Een technisch product vrijgeven aan een lokaal bedrijf

Het product is nu ontworpen door de technische afdeling. Voor dit voorbeeld is het product een prototype dat is ontworpen voor een klant. Aangezien de klant een klant is van de rechtspersoon *USMF*, moet het product worden vrijgegeven aan die rechtspersoon.

1. Houd de rechtspersoon ingesteld op *DEMF*. (Gebruik zo nodig de bedrijfskiezer rechts op de navigatiebalk.)
1. Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.
1. Selecteer het product *Z0001*.
1. Selecteer in het actievenster op het tabblad **Product** in de groep **Onderhouden** de optie **Productstructuur vrijgeven** om de wizard **Producten vrijgeven** te openen.
1. Schakel op de pagina **Technische producten selecteren voor vrijgave** het selectievakje **Selecteren** in voor product *Z0001*.

    ![De technische producten selecteren die moeten worden vrijgegeven](media/select-eng-product-to-release.png "De technische producten selecteren die moeten worden vrijgegeven")

1. Selecteer **Vrijgavedetails**.
1. De pagina **Productvrijgavedetails** wordt weergegeven, waar u de details en de productstructuur kunt controleren van het product dat wordt vrijgegeven. De optie **Stuklijst verzenden** is ingesteld op *Ja*. Daarom worden zowel product *Z0001* als alle onderliggende artikelen uit de stuklijst vrijgegeven.

    U kunt elk onderliggend item in het linkerdeelvenster selecteren om de details weer te geven. Als een onderliggend artikel een stuklijst heeft, kunt u ook de stuklijst van dat onderliggende artikel selecteren voor vrijgave.

    ![De productvrijgavedetails controleren](media/product-release-details.png "De productvrijgavedetails controleren")

1. Sluit de pagina om terug te keren naar de wizard **Producten vrijgeven**.
1. Selecteer **Volgende** om de pagina **Producten voor vrijgave selecteren** te openen. Als u standaardproducten (niet-technische producten) selecteert, worden deze weergegeven op deze pagina. Wanneer u een standaardproduct vrijgeeft door **Productstructuur vrijgeven** te selecteren, worden de bijbehorende stuklijst en route ook vrijgegeven.

    ![De standaardproducten selecteren die moeten worden vrijgegeven](media/select-std-product-to-release.png "De standaardproducten selecteren die moeten worden vrijgegeven")

1. Selecteer **Volgende** om de pagina **Productvarianten voor vrijgave selecteren** te openen. Voor dit voorbeeld zijn er geen varianten.
1. Selecteer **Volgende** om de pagina **Bedrijven selecteren** te openen.
1. Selecteer de bedrijven waaraan het product moet worden vrijgegeven. Schakel voor dit voorbeeld het selectievakje voor **USMF** in.

    ![De bedrijven selecteren waaraan moet worden vrijgegeven](media/select-release-companies.png "De bedrijven selecteren waaraan moet worden vrijgegeven")

1. Selecteer **Volgende** om de pagina **Selectie bevestigen** te openen.
1. Selecteer **Voltooien**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Het product controleren en accepteren voordat u het in het lokale bedrijf vrijgeeft

De technische afdeling heeft nu de gegevens vrijgegeven aan de lokale bedrijven waar het product wordt gebruikt. Voor dit voorbeeld is het lokale bedrijf *USMF*.

Omdat u het veld **Productacceptatie** hebt ingesteld op *Handmatig* op de pagina **Parameters voor technisch wijzigingsbeheer** voor het bedrijf *USMF*, moeten producten handmatig worden goedgekeurd voordat ze aan dat bedrijf worden vrijgegeven. Met andere woorden, ze moeten worden beoordeeld en geaccepteerd voordat ze worden vrijgegeven.

Voer de volgende stappen uit om het product te beoordelen en vrij te geven in het bedrijf *USMF*.

1. Stel de rechtspersoon in op *USMF*. (Gebruik de bedrijfskiezer rechts op de navigatiebalk.)
1. Ga naar **Technisch wijzigingsbeheer &gt; Algemeen &gt; Productreleases &gt; Openstaande productreleases**.

    Op de pagina **Openstaande productreleases** wordt het product *Z0001* weergegeven met de status *In afwachting van acceptatie*.

    ![Openstaande productreleases](media/open-product-releases.png "Openstaande productreleases")

1. Selecteer de waarde in de kolom **Productnummer** om de pagina **Productvrijgavedetails** te openen. Let op de volgende details:

    - Het sneltabblad **Algemeen** bevat informatie over de productvrijgave, zoals het vrijgevende bedrijf (*DEMF* voor dit voorbeeld), de vrijkomende site (*1*) en de ontvangende site (*1*). Omdat u geen ontvangende site hebt opgegeven in de wizard **Producten vrijgeven**, wordt de waarde van de vrijgevende site gekopieerd naar de ontvangende site.
    - Het sneltabblad **Vrijgavedetails** bevat informatie over het product en de versie die is vrijgegeven. Hier kunt u instellingen zoals de ingangsdatums wijzigen.
    - Op het sneltabblad **Route** wordt de route van het product weergegeven. In dit voorbeeld hebt u echter geen routes vrijgegeven.

    ![Productreleasegegevens](media/product-release-details-2.png "Productreleasegegevens")

1. Wanneer u klaar bent met het controleren van de informatie, kunt u het product accepteren en kunt u het op deze manier vrijgeven in het bedrijf *USMF*. Selecteer in het actievenster **Acties &gt; Accepteren**.
1. Het product is nu vrijgegeven in het bedrijf *USMF*. Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Artikel *Z0001* wordt weergegeven.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Het product gebruiken in transacties in het lokale bedrijf

De hoofdgegevensbeheerder voor het bedrijf *USMF* wil er zeker van zijn dat het product zich in de status *Prototype* bevindt, zodat gebruikers worden gewaarschuwd als ze dit per ongeluk toevoegen aan processen waaraan ze werken.

1. Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.
1. Selecteer product *Z0001* om de bijbehorende detailpagina te openen. (U kunt het filter gebruiken om het product te zoeken.)
1. Selecteer in het actievenster op het tabblad **Technicus** in de groep **Technisch wijzigingsbeheer** de optie **Technische versies**.
1. Selecteer op de pagina **Technische versies** versienummer *V-01* om de bijbehorende detailpagina te openen.
1. Selecteer in het actievenster op het tabblad **Product** in de groep **Levenscyclusstatus** de optie **Levenscyclusstatus wijzigen**.
1. Stel in het dialoogvenster met vervolgkeuzemenu **Levenscyclusstatus wijzigen** het veld **Status** in op *Prototype* en selecteer vervolgens **OK**.

    ![De levenscyclusstatus wijzigen](media/change-lifecycle-state.png "De levenscyclusstatus wijzigen")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Het technische product toevoegen aan een verkooporder

Het product kan nu aan een klant worden verkocht. Om het product aan een verkooporder toe te voegen, volgt u deze stappen.

1. Ga naar **Verkoop en marketing &gt; Verkooporders &gt; Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** het veld **Klantaccount** in op *US-0002* en selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Voeg op het sneltabblad **Verkooporderregels** een rij toe en stel het veld **Artikelnummer** in op *Z000*.
1. Selecteer **Opslaan** in het actievenster.

    Er wordt een waarschuwingsbericht weergegeven waarin wordt gemeld dat het artikel de status *Prototype* heeft. Omdat het bericht echter slechts een waarschuwing is, is de verkooporder wel gemaakt.

    ![Verkooporder voor een technisch product](media/sales-order-eng-product.png "Verkooporder voor een technisch product")

## <a name="request-changes-in-the-engineering-product"></a>Wijzigingen in het technische product aanvragen

Het product is naar een klant verzonden, maar de klant was niet geheel tevreden en geeft feedback met suggesties voor verbetering. Terwijl de klant met een verkoopmedewerker telefoneert, kan de verkoopmedewerker de wijzigingen aanvragen die de klant beschrijft.

1. Ga naar **Verkoop en marketing &gt; Verkooporders &gt; Alle verkooporders**.
1. Zoek en open de verkooporder die u in de vorige oefening hebt gemaakt.
1. Selecteer op het sneltabblad **Verkooporderregels** de optie **Technisch wijzigingsbeheer &gt; Nieuwe aanvraag voor technische wijziging**.

    ![Een aanvraag voor een technische wijziging maken op basis van een verkooporder](media/sales-order-eng-change-request.png "Een aanvraag voor een technische wijziging maken op basis van een verkooporder")

1. Vul de aanvraag voor de technische wijziging in op basis van de feedback van de klant. Stel de volgende waarden in voor dit voorbeeld:

    - **Wijzigingsaanvraag:** *555*
    - **Titel:** *Klantwijziging Z0001*
    - **Prioriteit:** *laag*
    - **Categorie:** wijziging instellen
    - **Ernst:** *Gemiddeld*

1. Selecteer op het sneltabblad **Informatie** de optie **Nieuw &gt; Notitie** om een notitie toe te voegen aan het raster.
1. Geef in het veld **Beschrijving** voor de nieuwe notitie aan dat artikel *D0003* uit de stuklijst moet worden verwijderd. Als u meer informatie voor de notitie moet toevoegen, kunt u tekst invoeren in het veld **Notities**.

    ![Technische-wijzigingsaanvraag](media/eng-change-request.png "Technische-wijzigingsaanvraag")

1. Selecteer **Opslaan** in het actievenster.
1. Het artikel is automatisch toegevoegd aan het sneltabblad **Producten** en de bron van de aanvraag voor de technische wijziging (de verkooporder) is toegevoegd op het sneltabblad **Bron**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Wijzigingen aanbrengen in het product met een order voor technische wijzigingen

De verkoopmedewerker weet dat het product belangrijk is en speciaal voor de klant is ontworpen. Daarom belt de verkoopmedewerker een technicus in het bedrijf *DEMF* om hem/haar te informeren over de wijzigingsaanvraag. Op deze manier kan de technicus het proces versnellen.

De technicus controleert nu de aanvraag van de klant en maakt een wijzigingsorder voor het product.

1. Aangezien de technicus werkt voor *DEMF*, moet u de rechtspersoon instellen op *DEMF*. (Gebruik de bedrijfskiezer rechts op de navigatiebalk.)
1. Ga naar **Technisch wijzigingsbeheer &gt; Algemeen &gt; Aanvragen van technische wijzigingen**.
1. Open wijzigingsaanvraag *555*.
1. Controleer de informatie en keur de wijziging goed. Selecteer vervolgens in het actievenster op het tabblad **Wijzigingsaanvraag** in de groep **Status wijzigen** de optie **Goedkeuren**.
1. Ga naar **Technisch wijzigingsbeheer &gt; Algemeen &gt; Orders voor technische wijzigingen**.
1. Selecteer in het actievenster de optie **Nieuw** om een wijzigingsorder te maken en stel hiervoor de volgende waarden in:

    - **Wijzigingsorder** *555*
    - **Titel:** *Klantwijziging Z0001*
    - **Categorie:** *Klantwijziging*
    - **Prioriteit:** *Laag*
    - **Ernst:** *Gemiddeld*

1. Selecteer op het sneltabblad **Getroffen producten** de optie **Nieuw &gt; Bestaande producten toevoegen** om een rij aan het raster toe te voegen en stel vervolgens de volgende waarden in:

    - **Product:** *Z0001*
    - **Impact:** *Nieuwe versie*

    ![Een order voor technische wijzigingen maken](media/eng-change-order.png "Een order voor technische wijzigingen maken")

1. Omdat u het veld **Impact** instelt op *Nieuwe versie*, wordt in het veld **Nieuwe versie** op het tabblad **Details** van het sneltabblad **Productdetails** aangegeven wat het nieuwe versie nummer wordt (*V-02* voor dit voorbeeld).

    ![Productdetails voor een order voor technische wijzigingen](media/eng-change-order-product-details.png "Productdetails voor een order voor technische wijzigingen")

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Productdetails** op het tabblad **Stuklijst** de optie **Regels** om de stuklijst voor versie *V-01* van het product *Z0001* te openen.

    ![Stuklijstregels voor technisch product](media/eng-product-bom-lines.png "Stuklijstregels voor technisch product")

1. Selecteer de regel voor artikelnummer *D0003* en selecteer vervolgens **Verwijderen** in het actievenster. De waarde van het veld **Wijzigingstype** voor deze regel wordt gewijzigd in *Verwijderd*.
1. Selecteer **Opslaan** in het actievenster.

    ![Gewijzigde stuklijstregels voor technisch product](media/eng-product-bom-lines-modified.png "Gewijzigde stuklijstregels voor technisch product")

1. Sluit de pagina **Stuklijstregel** om terug te keren naar de pagina **Order voor technische wijziging**.
1. Op het sneltabblad **Productdetails** op het tabblad **Stuklijst** ziet u dat de waarde van het veld **Type wijzigen** voor stuklijst *Z0001* nu *Gewijzigd* is.

    ![Order voor technische wijzigingen met een gewijzigde stuklijst](media/eng-change-order-changed-bom.png "Order voor technische wijzigingen met een gewijzigde stuklijst")

    De inkooporder moet nu worden goedgekeurd voordat de wijzigingen kunnen worden verwerkt. Wanneer de wijzigingen worden verwerkt, worden de producten bijgewerkt met de wijzigingen die zijn opgenomen in de order voor technische wijzigingen. Voor dit voorbeeld is de persoon die de order voor technische wijzigingen maakt, opgegeven als de fiatteur.

1. Selecteer vervolgens in het actievenster op het tabblad **Wijzigingsorder** in de groep **Status wijzigen** de optie **Goedkeuren**.
1. Selecteer **Verwerken** om de gegevens van het product bij te werken.
1. Selecteer **Voltooien** om de wijzigingsorder te markeren als voltooid.

## <a name="release-the-changed-product"></a>Het gewijzigde product vrijgeven

Het product kan nu weer worden vrijgegeven aan het bedrijf *USMF* en vervolgens naar de klant worden verzonden. Voer de volgende stappen uit om het product rechtstreeks vrij te geven vanuit de order voor technische wijzigingen.

1. Open de order voor technische wijzigingen die u in de vorige oefening hebt gemaakt, als deze nog niet is geopend.
1. Selecteer vervolgens in het actievenster op het tabblad **Wijzigingsorder** in de groep **Productreleases** de optie **Zoeken**.
1. De zoekresultaten laten zien aan welke bedrijven de producten zijn vrijgegeven. Sluit de zoekresultaten.
1. Selecteer in het actievenster op het tabblad **Wijzigingsorder** in de groep **Productreleases** op **Weergeven** om het dialoogvenster **Vrijgaven** te openen waarin u de resultaten van de vorige zoekopdracht kunt bekijken.
1. Selecteer elk bedrijf waarnaar u producten wilt vrijgeven.
1. Selecteer **OK** om het dialoogvenster **Vrijgaven** te sluiten en terug te gaan naar de wijzigingsorder.
1. Selecteer in het actievenster op het tabblad **Wijzigingsorder** in de groep **Productreleases** de optie **Verwerken** om de betrokken producten vrij te geven voor de geselecteerde bedrijven. U kunt ook **Productstructuur vrijgeven** selecteren om het vrijgaveproces te starten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]