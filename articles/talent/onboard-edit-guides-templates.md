---
title: Handleidingen en sjablonen voor onboarding bewerken in Dynamics 365 Talent - Onboard
description: In dit onderwerp wordt uitgelegd hoe u activiteiten en andere informatie toevoegt aan onboardinghandleidingen en -sjablonen in Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460822"
---
# <a name="edit-onboarding-guides-and-templates"></a>Onboardinghandleidingen en -sjablonen bewerken

[!include [banner](includes/banner.md)]

Nadat u in Microsoft Dynamics 365 Talent: Onboard een onboardinghandleiding of -sjabloon hebt gemaakt, moet u een inleiding, activiteiten, contactpersonen en resources toevoegen. Met Onboard kunt u inhoud met opmaak opnemen in uw onboardinghandleidingen, zoals:

- YouTube-video's
- Microsoft Sway-presentaties
- Microsoft PowerApps-apps
- Microsoft Stream-video's
- Microsoft Forms-formulieren
- Iframes die webinhoud bevatten

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Introducties of activiteiten bewerken die zijn geïmporteerd via een sjabloon

Als u een onboardinghandleiding maakt op basis van een sjabloon of als u activiteiten van de ene in een andere sjabloon importeert, wordt er een knop **Vergrendelen** weergegeven voor de geïmporteerde activiteiten. Deze worden *beheerde activiteiten* genoemd.

[![Beheerde activiteiten](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Wanneer u een beheerde activiteit selecteert, wordt de bronsjabloon boven aan de activiteit weergegeven.

[![Bron van beheerde activiteit](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Als u een activiteit in een sjabloon bewerkt, wordt de wijziging doorgevoerd in alle sjablonen en niet-verzonden handleidingen die op die sjabloon zijn gebaseerd. Als u een niet-verzonden handleiding selecteert op basis van een sjabloon die u hebt bewerkt en vervolgens het tabblad **Activiteiten** in de handleiding selecteert, wordt er een bericht weergegeven dat uw handleiding is gewijzigd. Selecteer **OK** om de melding te sluiten. 

[![Meldingsbericht](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Naast de bijgewerkte activiteiten wordt een zwarte punt weergegeven.

[![Gewijzigde activiteit](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

U kunt beheerde activiteiten niet buiten de oorspronkelijke sjabloon bewerken, behalve om een toegewezene, vervaldatum of andere informatie toe te voegen in het rechtergedeelte van de activiteit.

Als u een beheerde activiteit wilt bewerken of als u niet wilt dat een activiteit updates van de desbetreffende sjabloon ontvangt, selecteert u de knop **Vergrendelen** voor die activiteit. De knop **Vergrendelen** verdwijnt. De activiteit wordt niet meer door de oorspronkelijke sjabloon beheerd en er worden geen updates meer van die sjabloon ontvangen. Updates die u aanbrengt in een activiteit hebben geen invloed op de oorspronkelijke sjabloon.

Als u een activiteit uit een handleiding verwijdert en wijzigingen aanbrengt vanuit de sjabloon van die handleiding, blijft de activiteit verwijderd in de handleiding.

> [!NOTE]
> Contactpersonen en resources worden niet beheerd via sjablonen. Secties worden niet beheerd, dus als u een sectie in een sjabloon toevoegt of bewerkt, worden de wijzigingen niet doorgevoerd in de handleidingen of sjablonen die deze sjabloon gebruiken.
> 
> Als u nieuwe activiteiten aan een sjabloon toevoegt, worden de nieuwe activiteiten doorgevoerd in handleidingen en sjablonen op basis van die sjabloon. De nieuwe activiteiten worden bovenaan weergegeven.

## <a name="import-activities-from-another-template"></a>Activiteiten importeren uit een andere sjabloon

U kunt activiteiten uit een of meer sjablonen in een handleiding of sjabloon importeren.

1. Selecteer de handleiding of sjabloon die u wilt bewerken.

2. Selecteer het tabblad **Activiteiten**.

3. Selecteer het tabblad **Importeren** in de sectie rechts.

   [![Activiteiten importeren](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Als u de taken op een nieuw tabblad in de browser wilt bekijken, selecteert u de knop **Openen in een nieuw tabblad** van een sjabloon.

   [![Activiteiten importeren](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Sleep de gewenste sjabloon naar de plaats in uw handleidingsjabloon waar u de activiteiten wilt weergeven. Ga verder met het bewerken van uw handleiding of sjabloon.

De geïmporteerde activiteiten bevatten een knop **Vergrendeling**, waarmee wordt aangegeven dat die activiteiten worden beheerd door de sjabloon waaruit u hebt geïmporteerd. Wanneer u wijzigingen aanbrengt in de sjabloon die u hebt geïmporteerd, worden deze activiteiten bijgewerkt in de sjabloon waarin u deze hebt geïmporteerd. De wijzigingen worden echter niet automatisch doorgevoerd in de handleidingen die zijn gemaakt op basis van de sjabloon waarin u hebt geïmporteerd.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Wijzigingen in een sjabloon doorvoeren in andere sjablonen of handleidingen

Als u een sjabloon bewerkt die activiteiten bevat die in andere sjablonen of handleiding worden gebruikt, moet u de wijzigingen doorvoeren als u wilt dat deze in de andere sjablonen of handleidingen worden weergegeven.

Als u niet zeker weet of de activiteiten van uw sjabloon worden gebruikt in andere sjablonen of handleidingen, selecteert u het tabblad **Gebruikt in** om te zien waar deze activiteiten worden weergegeven.

   [![Handleidingen en sjablonen weergeven waarin activiteiten worden gebruikt](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Uw wijzigingen doorvoeren:

1. Sla uw wijzigingen op door de knop **Opslaan** te selecteren. Als u dit niet doet, wordt u gevraagd om de wijzigingen in de volgende stap op te slaan.

2. Selecteer **Deze wijzigingen doorvoeren**.

   
## <a name="add-or-edit-an-introduction"></a>Een inleiding toevoegen of bewerken

1. Voer op het tabblad **Inleiding** een titel voor uw handleiding en een openingsbericht in. Selecteer **Dit bericht gebruiken** als u de voorbeeldtekst wilt gebruiken.

    [![Het tabblad Inleiding in een onboardingsjabloon](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Gebruik de opmaakknoppen om tekst op te maken of afbeeldingen of koppelingen toe te voegen.
3. Selecteer **Opslaan** om uw werk op te slaan.

## <a name="add-or-edit-activities"></a>Activiteiten toevoegen of bewerken

1. Sleep op het tabblad **Activiteiten** items van rechts naar het bewerkingsgebied.
2. Als u uw handleiding in secties wilt indelen, sleept u het item **Nieuwe sectie** naar het bewerkingsgebied en voert u een naam en een optionele omschrijving voor de sectie in.

    ![[Een nieuwe sectie toevoegen aan een onboardinghandleiding of -sjabloon](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Als u activiteiten wilt toevoegen die uw nieuw aangenomen werknemer moet uitvoeren, sleept u het item **Nieuwe activiteit** naar het bewerkingsgebied en voert u een naam en omschrijving voor de activiteit in.

    ![[Een nieuwe activiteit toevoegen aan een onboardinghandleiding of -sjabloon](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Inhoud met opmaak toevoegen aan uw onboardinghandleiding:

    - Als u een YouTube-video wilt toevoegen, sleept u het item **YouTube** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en voert u de URL voor de YouTube-video in.
    - Als u een Sway-presentatie of -nieuwsbrief wilt toevoegen, sleept u het item **Sway** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en voert u de ingesloten URL voor de Sway-presentatie of -nieuwsbrief in.
    - Als u een Microsoft Power Apps-app wilt toevoegen, sleept u het item **Power Apps** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en selecteert u de Power Apps-app of voert u de id van de Power Apps-app in.
    - Als u een Microsoft Stream-video wilt toevoegen, sleept u het item **Microsoft Stream** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en voert u de URL voor de Microsoft Stream-video in.
    - Als u een Microsoft Forms-formulier wilt toevoegen, sleept u het item **Microsoft Forms** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in, voert u de URL voor het Microsoft Forms-formulier in en geeft u de grootte van het schermgebied op.
    - Als u een iframe met webinhoud wilt toevoegen, sleept u het item **Webinhoud (iframe)** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in, voert u de URL voor de webinhoud in en geeft u de grootte van het schermgebied op.

    ![[Inhoud met opmaak toevoegen aan een onboardinghandleiding of -sjabloon](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Optioneel: wijs in het gebied rechts van elke activiteit de activiteit toe aan een specifieke persoon of rol, voeg een vervaldatum en contactpersoon toe en wijs een categoriekleur toe. Wanneer u een activiteit toewijst aan een persoon of rol, wordt voor elke persoon een taak gemaakt. Deze taak wordt weergegeven in het menu **Taken** in Onboard.

    [![Een activiteit toewijzen in een onboarding-gids of -sjabloon](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Selecteer **Opslaan** om uw werk op te slaan.

Als u een activiteit of sectie wilt verwijderen, selecteert u de knop **Verwijderen** (het prullenbaksymbool) in de rechterbovenhoek van de activiteit of sectie.

Als u activiteiten en secties opnieuw wilt indelen, sleept u deze naar een nieuwe locatie.

## <a name="add-or-edit-contacts"></a>Contactpersonen toevoegen of bewerken

U kunt contactpersonen toevoegen die uw nieuwe aanstelling van de eerste dag kunnen helpen. Deze contactpersonen kunnen wervers, teamleden en onboardingbuddy's, mentoren, beheerders en IT-ondersteuningsmedewerkers zijn.

1. Selecteer **Nieuw contactpersoon** op het tabblad **Contactpersonen**.
2. Voer in het dialoogvenster **Teamlid toevoegen** de naam of het e-mail adres van de contactpersoon in, voer een korte omschrijving in die aangeeft hoe de contactpersoon de nieuw aangenomen werknemer kan helpen en selecteer vervolgens **Toevoegen**. 

    ![[Contactpersonen toevoegen aan een onboardinghandleiding of -sjabloon](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    U kunt ook een of meer contactpersonen selecteren onder **Suggesties**.

3. Selecteer **Opslaan** om uw werk op te slaan.

Als u een contactpersoon wilt verwijderen, selecteert u de knop **Verwijderen** (het prullenbaksymbool) rechts van de contactpersoon.

Als u een contactpersoon wilt bewerken, selecteert u de knop **Bewerken** (het potloodsymbool) rechts van de contactpersoon.

## <a name="add-or-edit-resources"></a>Resources toevoegen of bewerken

U kunt nuttige bestanden, kaarten en koppelingen toevoegen aan de sectie **Resources** van uw onboardinghandleiding.

1. Selecteer **Nieuwe resource** op het tabblad **Resources**.
2. Volg één van deze stappen:

    - Als u een bestand wilt toevoegen, selecteert u het tabblad **Bestand** en sleept u het bestand naar het opgegeven gebied. U kunt ook op een willekeurige plaats in dat gebied klikken om naar het bestand op uw computer te bladeren of u kunt **Bladeren in OneDrive** selecteren. Voer een naam in voor het bestand en selecteer vervolgens **Toevoegen**.
    - Als u een koppeling wilt toevoegen, selecteert u het tabblad **Koppeling**, voert u een naam en adres voor de koppeling in en selecteert u **Toevoegen**.
    - Als u een kaart wilt toevoegen, selecteert u het tabblad **Kaart**, voert u een naam en adres voor de kaart in en selecteert u **Toevoegen**. Onboard bevat in dat geval een kaart van het adres dat u opgeeft.

    ![[Een resource toevoegen aan een onboardinghandleiding of -sjabloon](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Selecteer **Opslaan** om uw werk op te slaan.

Als u een resource wilt verwijderen, selecteert u de knop **Verwijderen** (het prullenbaksymbool) rechts van de resource.

Als u een contactpersoon wilt bewerken, selecteert u de knop **Bewerken** (het potloodsymbool) rechts van de resource.

## <a name="next-steps"></a>Volgende stappen

- [Inhoud delen met andere bijdragers](./onboard-share-template.md)
- [De status van taken en onboardingmedewerkers weergeven](./onboard-view-status.md)
- [Aanstellingsteams maken in Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Zie ook

- [De Onboard-app uitproberen of kopen](https://dynamics.microsoft.com/talent/onboard/)
- [Nieuwe of gewijzigde functies in Dynamics 365 Talent](./whats-new.md)
- [Vrijgaveplannen](https://docs.microsoft.com/business-applications-release-notes/index)
- [Ondersteuning voor Microsoft Dynamics 365 Talent](./talent-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]