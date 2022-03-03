---
title: Categorieaanvragen van leveranciers
description: In dit onderwerp wordt beschreven hoe leveranciers inkoopcategorieën voor hun account kunnen aanvragen. Ook wordt hierin het goedkeuringsproces beschreven dat wordt voltooid door inkoopagents.
author: Henrikan
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5d06f05ca27ed8fe58a9a24fcde8c0082662b866
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103090"
---
# <a name="category-requests-from-vendors"></a>Categorieaanvragen van leveranciers

[!include [banner](../includes/banner.md)]

Met het proces voor categorieaanvragen kunnen leveranciers verzoeken om nieuwe inkoopcategorieën aan hun account te koppelen. Deze inkoopcategorieën kunnen vervolgens worden gebruikt door de bijbehorende inkoop- en sourcingprocessen. (Zie voor meer informatie [Overzicht van inkoopcatalogi](procurement-catalogs.md).)

Categorieaanvragen worden geïnitieerd door leveranciers in het werkgebied **Leveranciergegevens**. Vervolgens worden ze ter beoordeling en goedkeuring naar uw instelling verzonden. Goedgekeurde categorieën worden toegevoegd aan de lijst met inkoopcategorieën in de account van de leverancier.

## <a name="turn-the-category-requests-from-vendors-feature-on-or-off"></a>De functie Categorieaanvragen van leveranciers in- of uitschakelen

Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Leveranciers toestaan zich aan te melden voor inkoopcategorieën via leverancierssamenwerking* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Als deze functie is ingeschakeld, kunt u nog steeds handmatig inkoopcategorieën toevoegen aan leveranciersaccounts. Meer informatie over dit onderwerp vindt u in [Leveranciers goedkeuren voor specifieke inkoopcategorieën](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Vereisten voor leverancierssamenwerking

Voordat een leverancier kan werken met categorieaanvragen, moet dit worden ingesteld voor leverancierssamenwerking.

De leverancier moet minimaal één gebruiker voor leverancierssamenwerking hebben. Alleen leveranciersgebruikers met de beveiligingsrol *Leverancierbeheerder (extern)* kunnen categorieaanvragen maken en indienen.

Zie voor meer informatie [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>De workflow Leveranciercategorieaanvragen instellen

De workflow *Leveranciercategorieaanvragen* moet worden ingesteld in de workflows voor inkoop en sourcing. Leveranciers dienen nieuwe categorieaanvragen in die u kunt controleren en goedkeuren. Aangevraagde inkoopcategorieën worden aan een leverancieraccount toegevoegd nadat een categorieaanvraag is goedgekeurd.

In het volgende voorbeeld ziet u hoe u een eenvoudige workflow voor *Leveranciercategorieaanvragen* met één fiatteur instelt. U moet uw interne processen evalueren om de juiste workflowinstellingen voor uw instelling te bepalen.

1. Ga naar **Inkoop en sourcing \> Instellen \> Workflows voor inkoop en sourcing**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in het dialoogvenster de **workflow Leveranciercategorieaanvragen** om de workfloweditor te openen.
1. Meld u aan bij de workfloweditor.
1. Selecteer **Eigenschappen** in het actievenster.
1. Voer in het veld **Indieningsinstructies** op de pagina **Eigenschappen** van de workflow een tekst met instructies in. De instructies worden weergegeven voor leveranciers wanneer ze een categorieaanvraag indienen.
1. Sluit de pagina **Eigenschappen**.
1. Sleep het workflowelement **Nieuwe categorieaanvraag goedkeuren** naar het canvas.
1. Sleep een koppeling van het workflowelement **Start** naar het workflowelement **Nieuwe categorieaanvraag goedkeuren**.
1. Sleep een koppeling van het workflowelement **Nieuwe categorieaanvraag goedkeuren** naar het workflowelement **Einde**.
1. Dubbeltik of -klik op het workflowelement **Nieuwe categorieaanvraag goedkeuren**.
1. Selecteer het workflowelement **Stap 1** en houd dit vast (of klik er met de rechtermuisknop op) en selecteer **Eigenschappen**.
1. Voer in het veld **Onderwerp werkitem** op de pagina **Eigenschappen** van het workflowelement een tekst met het onderwerp in. Deze tekst wordt weergegeven als de waarde van het veld **Onderwerp** op de pagina **Aan mij toegewezen werkitems**.
1. Voer in het veld **Instructies werkitem** de tekst van de instructies in. De instructies worden weergegeven voor fiatteurs wanneer ze **Workflow** selecteren in het actievenster van een categorieaanvraag.
1. Selecteer in het linkerdeelvensters **Toewijzing**.
1. Stel op het tabblad **Toewijzingstype** de optie **Gebruikers toewijzen aan dit workflowelement** in op *Gebruiker*.
1. Selecteer op het tabblad **Gebruiker** in de lijst **Beschikbare gebruikers** een fiatteur. Selecteer bijvoorbeeld een gebruiker in de afdeling Inkoop.
1. Selecteer de knop Pijl-rechts (**\>**) om de fiatteur te verplaatsen naar de lijst **Geselecteerde gebruikers**.
1. Sluit de pagina **Eigenschappen**.
1. Selecteer **Opslaan en sluiten**.
1. Voer in het veld **Versieopmerkingen** notities in voor de workflow.
1. Selecteer **OK** om de workflow op te slaan.
1. Als u klaar bent om de workflow te testen, selecteert u **De nieuwe versie activeren**. Als u dit niet wilt, selecteert u **De nieuwe versie niet activeren**.
1. Selecteer **OK** om het instellen van de workflow af te ronden.

> [!TIP]
> Als uw instelling niet vereist dat categorieaanvragen moeten worden goedgekeurd, moet u de workflow voor automatische goedkeuring configureren.

Meer informatie over het instellen van workflows vindt u in [Overzicht van werkstroomsysteem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Een categorieaanvraag maken en indienen

In deze sectie wordt beschreven hoe leveranciers het werkgebied **Leveranciergegevens** kunnen gebruiken om categorieaanvragen te maken, te bewerken, weer te geven en in te dienen.

### <a name="start-a-new-request"></a>Een nieuw aanvraag starten

Volg deze stappen om een nieuwe categorieaanvraag te starten.

1. Selecteer in het werkgebied **Leveranciersgegevens** de tegel **Categorieaanvragen**.
1. Selecteer op de pagina **Categorieaanvragen** in het actievenster de optie **Nieuwe categorieaanvraag**.
1. Zoek in het dialoogvenster **Nieuwe categorieaanvraag** de categorie die u wilt aanvragen door in de structuur te navigeren en/of het filter boven aan de lijst te gebruiken. Schakel het selectievakje in voor elke gewenste categorie.

    Let op de volgende punten:

    - Categorieën die momenteel actief zijn in uw leveranciersaccount worden weergegeven als geselecteerd en kunnen niet worden verwijderd.
    - U kunt meerdere inkoopcategorieën aanvragen in één categorieaanvraag.

1. Selecteer **OK** om de conceptaanvraag te maken.

    De nieuwe conceptaanvraag verschijnt nu op de pagina **Categorieaanvragen**.

1. Open de nieuwe conceptaanvraag om deze te controleren en zo nodig te bewerken.

    - Om de lijst met categorieën weer te geven die momenteel in de aanvraag zijn opgenomen, selecteert u het sneltabblade **Aangevraagde categorieën**.
    - Als u de actieve categorieën wilt zien, opent u het feitenvak **Actieve categorieën** rechts in de pagina.
    - Als u een categorie wilt toevoegen aan de aanvraag, selecteert u **Toevoegen** in de werkbalk op het sneltabblad **Aangevraagde categorieën**.
    - Als u een categorie uit de aanvraag wilt verwijderen, selecteert u de categorie op het sneltabblad **Aangevraagde categorieën** en selecteert u vervolgens **Verwijderen** in de werkbalk.
    - Als u een document aan de aanvraag wilt toevoegen, selecteert u **Bijlagen** in het actievenster. Gekoppelde documenten zijn beschikbaar voor fiatteurs wanneer deze de categorieaanvraag controleren.
    - Als u een bijlage uit de aanvraag wilt verwijderen, selecteert u **Bijlagen** in het actievenster. Selecteer het document dat u wilt verwijderen en selecteer vervolgens **Verwijderen** in het actievenster.

1. Als u klaar bent om de aanvraag in te dienen, selecteert u **Indienen** in het actievenster. Sluit anders de pagina en sla de resterende stappen van deze procedure over. U kunt op een later tijdstip weer teruggaan naar de aanvraag.
1. Lees eventuele indieningsinstructies die worden getoond en selecteer vervolgens **Indienen**.
1. Voer in het vak **Opmerkingen** aanvullende gegevens in die vereist zijn. Selecteer vervolgens **Indienen** om de aanvraag af te ronden.

### <a name="edit-a-draft-or-recalled-request"></a>Een conceptaanvraag of ingetrokken aanvraag bewerken

Volg deze stappen om een conceptaanvraag of ingetrokken categorieaanvraag te bewerken.

1. Selecteer in het werkgebied **Leveranciersgegevens** de tegel **Categorieaanvragen**.
1. Selecteer het concept of de ingetrokken aanvraag om deze te openen.
1. Bewerk de aanvraag waar nodig en sluit deze of dien deze in zoals beschreven in de vorige procedure.

### <a name="submit-a-draft-or-recalled-request"></a>Een conceptaanvraag of ingetrokken aanvraag indienen

Volg deze stappen om een conceptaanvraag of ingetrokken categorieaanvraag in te dienen.

1. Selecteer in het werkgebied **Leveranciersgegevens** de tegel **Categorieaanvragen**.
1. Selecteer het concept of de ingetrokken aanvraag die u wilt indienen.
1. Selecteer **Indienen** in het actievenster.
1. Lees eventuele indieningsinstructies die worden getoond en selecteer vervolgens **Indienen**.
1. Voer in het vak **Opmerkingen** aanvullende gegevens in die vereist zijn. Selecteer vervolgens **Indienen** om de aanvraag af te ronden.

    De status van de categorieaanvraag wordt gewijzigd in een van de volgende waarden:

    - _In afwachting van controle_: de aanvraag bevindt zich in de workflow.
    - _In afwachting van goedkeuring_: goedkeuring is verplicht.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Een ingediende aanvraag intrekken die nog niet is goedgekeurd

Volg deze stappen om een categorieaanvraag in te trekken die is ingediend, maar nog niet is goedgekeurd.

1. Selecteer in het werkgebied **Leveranciersgegevens** de tegel **Categorieaanvragen**.
1. Selecteer de in behandeling zijnde aanvraag die u wilt intrekken.
1. Selecteer **Intrekken** in het actievenster.
1. Voer in het vak **Opmerking invoeren** aanvullende gegevens in die vereist zijn. Selecteer vervolgens **Indienen** om de aanvraag af te ronden.

    De status van de categorieaanvraag wordt gewijzigd in _Geannuleerd_. De aanvraag behoudt deze status tot u deze verwijdert of opnieuw indient.

### <a name="delete-a-draft-or-recalled-request"></a>Een conceptaanvraag of ingetrokken aanvraag verwijderen

Volg deze stappen om een conceptaanvraag of ingetrokken categorieaanvraag te verwijderen.

1. Selecteer in het werkgebied **Leveranciersgegevens** de tegel **Categorieaanvragen**.
1. Selecteer het concept of de ingetrokken aanvraag die u wilt verwijderen.
1. Selecteer in het actievenster **Verwijderen**.
1. Selecteer **Ja** om de verwijdering te bevestigen.

### <a name="view-completed-requests"></a>Voltooide aanvragen weergeven

Als u voltooide aanvragen wilt weergeven, opent u het werkgebied **Leveranciersgegevens** en selecteert u de tegel **Categorieaanvragen**. Categorieaanvragen die zijn voltooid, hebben een van de volgende statussen:

- _Goedgekeurd_: De aanvraag is goedgekeurd. Als u de nieuw toegevoegde categorieën wilt weergeven, gaat u terug naar het werkgebied **Leveranciergegevens** en opent u de vervolgkeuzelijst **Meer details** in het linkerdeelvenster. Selecteer vervolgens **Categorieën**.
- _Afgewezen_: De aanvraag is afgewezen. U kunt zo nodig een nieuwe categorieaanvraag maken.

## <a name="review-category-requests"></a>Categorieaanvragen beoordelen

In deze sectie wordt uitgelegd hoe u categorieaanvragen kunt goedkeuren, afwijzen en delegeren die leveranciers hebben ingediend, en hoe u voltooide aanvragen kunt weergeven. Deze workflowacties zijn voor de hele categorieaanvraag.

### <a name="view-category-requests"></a>Categorieaanvragen weergeven

Volg deze stappen om categorieaanvragen weer te geven.

1. Ga naar **Inkoopbeheer \> Leveranciers \> Aanvragen voor leverancierssamenwerking \> Categorieaanvragen**.

    De pagina **Categorieaanvragen** wordt geopend. De standaardpaginaweergave toont categorieaanvragen met de status *In behandeling*.

1. Als u alle aanvragen wilt weergeven, selecteert u *Alle* in het veld **Aanvragen weergeven**.
1. Open een aanvraag om deze te beoordelen en zo nodig te bewerken.

    - Om de lijst met categorieën weer te geven die momenteel in de aanvraag zijn opgenomen, selecteert u het sneltabblade **Aangevraagde categorieën**.
    - Als u de actieve categorieën wilt zien, opent u het feitenvak **Actieve categorieën** rechts in de pagina.
    - Als documenten zijn ingediend, wordt op de knop **Bijlagen** (paperclip) in het actievenster het aantal gekoppelde documenten getoond. Als u gekoppelde documenten wilt weergeven, klikt u op de knop **Bijlagen**. Selecteer vervolgens het document dat u wilt weergeven en selecteer **Openen** om het weer te geven.
    - Als u een document aan de aanvraag wilt toevoegen, selecteert u **Bijlagen** in het actievenster. Gekoppelde documenten zijn beschikbaar voor fiatteurs wanneer deze de categorieaanvraag controleren.
    - Als u een bijlage uit de aanvraag wilt verwijderen, selecteert u **Bijlagen** in het actievenster. Selecteer het document dat u wilt verwijderen en selecteer vervolgens **Verwijderen** in het actievenster.
    - Als u de geschiedenis van de workflow wilt bekijken, selecteert u **Workflow** in het actievenster. Selecteer In de workflowopties **Meer** en vervolgens **Workflowhistorie**. De pagina **Workflowhistorie** wordt geopend.

### <a name="approve-a-pending-category-request"></a>Een in behandeling zijnde categorieaanvraag goedkeuren

Volg deze stappen om een in behandeling zijnde categorieaanvraag goed te keuren.

1. Ga naar **Inkoopbeheer \> Leveranciers \> Aanvragen voor leverancierssamenwerking \> Categorieaanvragen**.
1. Selecteer de aanvraag die in behandeling is die u wilt goedkeuren.
1. Beoordeel de categorieaanvraag.
1. Optioneel: selecteer een redencode in het veld **Redencode** op het sneltabblad **Algemeen**. Voer vervolgens in het veld **Opmerking bij reden** een opmerking voor de redencode in.
1. Selecteer in het actievenster de optie **Workflow**.
1. Selecteer in de workflowopties de optie **Goedkeuren**.
1. Voer in het veld **Opmerkingen** aanvullende gegevens in die vereist zijn. Selecteer vervolgens **Goedkeuren** om de aanvraag af te ronden.

    De status van de categorieaanvraag wordt gewijzigd in _Goedgekeurd_ en de inkoopcategorieën worden toegevoegd aan de leveranciersaccount.

### <a name="reject-a-pending-category-request"></a>Een in behandeling zijnde categorieaanvraag afwijzen

Volg deze stappen om een in behandeling zijnde categorieaanvraag af te wijzen.

1. Ga naar **Inkoopbeheer \> Leveranciers \> Aanvragen voor leverancierssamenwerking \> Categorieaanvragen**.
1. Selecteer de aanvraag die in behandeling is die u wilt afwijzen.
1. Beoordeel de categorieaanvraag.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer een redencode in het veld **Redencode** op het sneltabblad **Algemeen**. Voer vervolgens in het veld **Opmerking bij reden** een opmerking voor de redencode in.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster de optie **Workflow**.
1. Selecteer In de workflowopties **Meer** en vervolgens **Afwijzen**.
1. Voer in het veld **Opmerkingen** aanvullende gegevens in die vereist zijn. Selecteer vervolgens **Afwijzen** om de aanvraag af te ronden.

    De status van de categorieaanvraag wordt gewijzigd in _Afgewezen_. Hierna kan de leverancier desgewenst een nieuwe categorieaanvraag maken.

### <a name="delegate-a-pending-category-request"></a>Een in behandeling zijnde categorieaanvraag delegeren

Volg deze stappen om een in behandeling zijnde categorieaanvraag aan een andere gebruiker te delegeren.

1. Ga naar **Inkoopbeheer \> Leveranciers \> Aanvragen voor leverancierssamenwerking \> Categorieaanvragen**.
1. Selecteer de in behandeling zijnde aanvraag die u wilt delegeren.
1. Selecteer in het actievenster de optie **Workflow**.
1. Selecteer In de workflowopties **Meer** en vervolgens **Delegeren**.
1. Selecteer in het veld **Gebruiker** de gebruiker waaraan u de categorieaanvraag wilt toewijzen ter beoordeling.
1. Voer in het veld **Opmerkingen** aanvullende gegevens in die vereist zijn.
1. Selecteer **Delegeren** om de delegering te voltooien. De geselecteerde gebruiker kan de categorieaanvraag nu beoordelen.

### <a name="view-procurement-categories-for-a-vendor"></a>Inkoopcategorieën voor een leverancier weergeven

Volg deze stappen om inkoopcategorieën weer te geven voor een leverancier nadat een categorieaanvraag is goedgekeurd.

1. Ga naar **Inkoop en sourcing \> Leveranciers \> Alle leveranciers**.
1. Selecteer op de pagina **Alle leveranciers** de leverancier van wie u de inkoopcategorieën wilt bekijken.
1. Open in het actievenster het tabblad **Algemeen** en selecteer in de groep **Instellen** de optie **Categorieën**.

    De pagina **Categorieën** wordt geopend. Op het sneltabblad **Inkoop** worden inkoopcategorieën getoond die zijn toegevoegd via de categorieaanvraag.

1. Op het sneltabblad **Inkoop** kunt u indien nodig wijzigingen invoeren. U kunt bijvoorbeeld het veld **Categoriestatus leverancier** instellen op _Voorkeur_.
