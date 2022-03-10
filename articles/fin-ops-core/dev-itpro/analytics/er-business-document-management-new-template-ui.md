---
title: Gebruikersinterface in Microsoft Office-stijl voor beheer van bedrijfsdocumenten (bevat video)
description: Dit onderwerp biedt uitleg over het gebruik van de nieuwe documentgebruikersinterface in de functie voor bedrijfsdocumentbeheer van het ER-raamwerk.
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e33830e2147d92ad5ee53ad11da55a50613b8ef9
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074736"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Gebruikersinterface in Microsoft Office-stijl voor beheer van bedrijfsdocumenten

[!include [banner](../includes/banner.md)]

Beheer van bedrijfsdocumenten stelt zakelijke gebruikers in staat zakelijke documentsjablonen te bewerken met een Microsoft Office 365-service of de juiste Microsoft Office-bureaubladtoepassing. Wijzigingen kunnen ontwerpwijzigingen of nieuwe implementaties bevatten, of gebruikers kunnen tijdelijke aanduidingen toevoegen om extra gegevens op te nemen zonder de broncode te hoeven wijzigen. Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) voor meer informatie over het werken met beheer van bedrijfsdocumenten.

De nieuwe gebruikersinterface (UI) is duidelijker en gemakkelijker te gebruiken. Het gebied **Bedrijfsdocument** bevat alleen de sjablonen die eigendom zijn van de huidige [actieve](tasks/er-configuration-provider-mark-it-active-2016-11.md) [provider](general-electronic-reporting.md#Provider) en zich in het huidige exemplaar van Dynamics 365 Finance bevinden. In de vorige gebruikersinterface bevatte het tabblad **Sjabloon** alle sjablonen die beschikbaar waren voor providers. Daarnaast werden alle sjablonen getoond die door elke gebruiker met dezelfde rol waren gemaakt en bewerkt.

Met de knop **Nieuw document** in het werkgebied **Bedrijfsdocumentbeheer** kunt u een sjabloon in een [configuratie](general-electronic-reporting.md#Configuration) in [ER-indeling (Electronic Reporting)](general-electronic-reporting.md) maken en bewerken die wordt geleverd door een andere provider en die zich in het huidige Finance-exemplaar bevindt, of u kunt een nieuwe sjabloon uploaden vanuit een Excel-werkmap. Daarnaast kunt u in versie 10.0.25 en hoger de knop **Nieuw document** gebruiken om een sjabloon te maken en te bewerken in een ER-indelingsconfiguratie die is opgeslagen in de [Algemene opslagplaats](general-electronic-reporting.md#Repository).

In de voorbeelden in dit onderwerp is de actieve provider Contoso en u gebruikt deze om een sjabloon te maken die is gebaseerd op een sjabloon die door Microsoft is verschaft. U kunt ook een sjabloon maken door uw eigen sjabloon te uploaden naar de Excel-indeling.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

De video [Een nieuw bedrijfsdocument maken met Bedrijfsdocumentbeheer](https://youtu.be/gAIYl-mM_pw) (hierboven weergegeven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>De nieuwe documentgebruikersinterface in Beheer van bedrijfsdocumenten beschikbaar maken

Als u de nieuwe documentgebruikersinterface wilt gebruiken in Beheer van bedrijfsdocumenten, moet u de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** inschakelen in het werkgebied **Functiebeheer**.

Voer de volgende stappen uit om deze functie in te schakelen voor alle rechtspersonen.

1. Selecteer in het werkgebied **Functiebeheer** op het tabblad **Alle** de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** in de lijst.
2. Selecteer **Nu inschakelen** om de geselecteerde functie in te schakelen.
3. Vernieuw de pagina om de nieuwe functie te openen.

## <a name="add-or-activate-a-provider"></a>Een provider toevoegen of activeren

Elke sjabloon van een bedrijfsdocument wordt opgeslagen in een ER-indelingsconfiguratie die is gemarkeerd als eigendom van een specifieke configuratieprovider. Wanneer u een nieuwe sjabloon maakt, wordt een nieuwe ER-indelingsconfiguratie gemaakt om deze te bewaren. Daarom moet voor die configuratie een provider worden geïdentificeerd. De actieve provider van het ER-raamwerk wordt hiervoor gebruikt. Als er geen provider in ER is, kunt u er een maken. Als er geen actieve *provider* is, kunt u een van de bestaande providers activeren. Wanneer dat nodig is, wordt er een dialoogvenster geopend waarin u een provider kunt toevoegen of activeren, terwijl u een nieuwe sjabloon gaat toevoegen.

### <a name="add-a-new-provider"></a>Een nieuwe provider toevoegen

Voer de volgende stappen uit in het dialoogvenster **Configuratieprovider** om een nieuwe provider te maken:

1.  Voer de naam van de nieuwe provider in het veld **Naam** op het tabblad **Configuratieprovider kiezen** in.
2.  Voer in het veld **Internetadres** het internetadres (URL) van de nieuwe provider in. 
3.  Selecteer **OK**.

    ![Een nieuwe provider maken in beheer van bedrijfsdocumenten.](./media/bdm_create_provider.png)

De toegevoegde provider wordt automatisch geactiveerd.

### <a name="activate-a-provider"></a>Een provider activeren

Voer de volgende stappen uit in het dialoogvenster **Configuratieprovider** om een provider te activeren:

1.  Selecteer de provider in het veld **Configuratieprovider** op het tabblad **Configuratieprovider kiezen**.
2.  Selecteer **OK**.

    ![Een provider activeren in beheer van bedrijfsdocumenten.](./media/bdm_choose_provider.png)

De geselecteerde provider wordt automatisch geactiveerd.

> [!NOTE]
> Elke sjabloon voor bedrijfsdocumentbeheer bevindt zich in een ER-indelingsconfiguratie die naar de provider verwijst als configuratie-auteur. Daarom is een actieve provider vereist voor elke sjabloon.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Een sjabloon bewerken die eigendom is van een andere provider

Met dit voorbeeld wordt aangegeven hoe de knop **Nieuw document** in het werkgebied **Bedrijfsdocumentbeheer** wordt gebruikt om een sjabloon in een configuratie in ER-indeling (Electronic Reporting) te maken en te bewerken die wordt geleverd door een andere provider en zich in het huidige Finance-exemplaar bevindt. In dit voorbeeld is de actieve provider Contoso die de ER-indelingsconfiguratie gebruikt die door Microsoft wordt verschaft. Nadat u **Nieuw document** hebt geselecteerd, worden op het tabblad **Selecteren** op de pagina **Een nieuwe sjabloon maken** alle sjablonen van het huidige Finance-exemplaar weergegeven die het eigendom zijn van de huidige provider en andere providers. Selecteer een sjabloon om deze te openen. Vervolgens kunt u een nieuwe bewerkbare kopie van de sjabloon maken. De bewerkte sjabloon wordt opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.

    ![Het werkgebied Beheer van bedrijfsdocumenten.](./media/BDM_overview_new_template1.png)

2. Selecteer op de pagina **Een nieuwe sjabloon maken** op het tabblad **Selecteren** het document dat u wilt gebruiken als sjabloon en selecteer vervolgens **Document maken**.

    ![Dialoogvenster Bedrijfsdocumenten.](./media/BDM_overview_new_template2.png)

3. Wijzig in het dialoogvenster Nieuw in het veld **Titel** de gewenste titel. De titeltekst wordt gebruikt als naam voor de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt. De conceptversie van deze configuratie (**Kopie FTI-rapport klant (GER)**) bevat de bewerkte sjabloon en wordt gebruikt om deze ER-indeling uit te voeren voor de huidige gebruiker. De oorspronkelijke sjabloon uit de ER-basisindelingsconfiguratie wordt gebruikt om deze ER-indeling voor elke andere gebruiker uit te voeren.
4. Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.
5. Wijzig in het veld **Opmerking** de opmerkingen voor de automatisch gemaakte revisie van de bewerkbare sjabloon.
6. Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.

    ![Dialoogvenster om document te maken.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Een sjabloon uploaden waarin een bestaande Excel-werkmap wordt gebruikt

Met dit voorbeeld wordt aangegeven hoe de knop **Nieuw document** in het werkgebied **Bedrijfsdocumentbeheer** wordt gebruikt om een sjabloon in een configuratie in ER-indeling (Electronic Reporting) te maken en te bewerken op basis van de beschikbare Excel-werkmap. In dit voorbeeld is Contoso de actieve provider en gebruikt u de configuraties ER-[gegevensmodel](er-overview-components.md#data-model-component) en ER-[modeltoewijzing](er-overview-components.md#model-mapping-component) die door Microsoft worden verschaft. Nadat u **Nieuw document** hebt geselecteerd, selecteert u het tabblad **Uploaden** op de pagina **Een nieuwe sjabloon maken**. Hier kunt u de details van een upload van een Excel-werkmap opgeven. Nadat u de Excel-werkmap hebt geüpload, wordt deze omgezet in een bedrijfsdocumentsjabloon die wordt geopend voor bewerking. De bewerkte sjabloon wordt opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.

Volg deze stappen om vereiste informatie te geven voordat u een sjabloon uploadt.

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.
2. Selecteer op de pagina **Een nieuwe sjabloon maken**, op het tabblad **Uploaden**, op het tabblad **Sjabloon** de optie **Bladeren** om te zoeken naar het Excel-bestand dat u als sjabloon wilt gebruiken. In de sectie **Sjabloon** worden de velden **Titel** en **Omschrijving** automatisch ingevuld. Deze geven de naam en omschrijving op van de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt. U kunt zo nodig deze velden bewerken.
3. Geef in de sectie **Documenttype** in het veld **Naam** het type bedrijfsdocument op. Deze waarde wordt gebruikt om de juiste gegevensbron (dat wil zeggen de ER-modelconfiguratie) te zoeken.

    ![Het tabblad Sjabloon op het tabblad Uploaden van de pagina Een nieuwe sjabloon maken.](./media/BDM_overview_new_UI_import_21.jpg)

4. Selecteer op het tabblad **Gegevensbron** op het sneltabblad **Filter** de optie **Filter toepassen**. In de sectie **Gegevensbron** wordt het veld **Naam** automatisch ingevuld of kunt u handmatig een waarde selecteren. Met het filter kunt u zoeken naar de juiste gegevensbron op naam, omschrijving, land-/regiocode en type bedrijfsdocument.

    ![Het tabblad Gegevensbron op het tabblad Uploaden van de pagina Een nieuwe sjabloon maken.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Het sneltabblad **Filter** wordt gebruikt om de juiste gegevensbron (dat wil zeggen de ER-modelconfiguratie) te zoeken. U kunt alle filtervelden bewerken om de meest geschikte gegevensbron te vinden voor het document dat u uploadt.
    > 
    > De voorwaarden op het sneltabblad **Filter** worden als **OR**-voorwaarden gebruikt.

5. Selecteer op het tabblad **Toewijzing** de optie **Automatisch detecteren**. Het veld **Hoofddefinitie** wordt automatisch ingevuld of u kunt handmatig een waarde selecteren. Op dit tabblad wordt de eindtoewijzing weergegeven voor de elementen van de sjabloon en het model.

    ![Het tabblad Toewijzing op het tabblad Uploaden van de pagina Een nieuwe sjabloon maken.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Bij de toewijzing in de sectie **Sjabloonstructuur** wordt de volledige overeenkomst gebruikt tussen de labels of omschrijvingen in de gegevensbron in de taal van de gebruiker en de naam van de cel in de sjabloon.

6. Selecteer **Document maken** om te bevestigen dat u een sjabloon wilt maken en het bewerkingsproces te starten.

Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)voor meer informatie.

## <a name="upload-a-template-from-the-global-repository"></a>Een sjabloon uploaden vanuit de algemene opslagplaats

Met dit voorbeeld wordt aangegeven hoe de knop **Nieuw document** in het werkgebied **Bedrijfsdocumentbeheer** wordt gebruikt om een sjabloon in een configuratie in ER-indeling (Electronic Reporting) te maken en te bewerken die wordt verschaft door Microsoft en zich in de algemene opslagplaats bevindt. In dit voorbeeld is de actieve provider Contoso die de ER-indelingsconfiguratie gebruikt die door Microsoft wordt verschaft. Nadat u **Nieuw document** hebt geselecteerd, bevat het tabblad **Importeren uit algemene opslagplaats** op de pagina **Een nieuwe sjabloon maken** alle sjablonen voor bedrijfsdocumenten die zijn opgeslagen in de algemene opslagplaats maar ontbreken in het huidige Finance-exemplaar. Als u een sjabloon hebt geselecteerd, wordt deze geïmporteerd vanuit de algemene opslagplaats naar het huidige Finance-exemplaar om een nieuwe bewerkbare kopie te maken. De bewerkte sjabloon wordt opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.
2. Selecteer op de pagina **Een nieuwe sjabloon maken** op het tabblad **Importeren uit algemene opslagplaats** het document dat u wilt gebruiken als een sjabloon en selecteer vervolgens **Document maken**.

    ![Tabblad Importeren vanuit algemene opslagplaats op de pagina Een nieuwe sjabloon maken.](./media/BDM_overview_new_template22.png)

3. Selecteer In het berichtvak **Ja** om te bevestigen dat u het geselecteerde document van de algemene opslagplaats naar het huidige Finance-exemplaar wilt importeren. Volg de instructies op het scherm als u wordt gevraagd om autorisatie.
4. Wijzig in het dialoogvenster Nieuw in het veld **Titel** de gewenste titel. De titeltekst wordt gebruikt als naam voor de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt. De conceptversie van deze configuratie (**Notitie bij aanmaning (Excel) - kopie**) bevat de bewerkte sjabloon en wordt gebruikt om deze ER-indeling uit te voeren voor de huidige gebruiker. De oorspronkelijke sjabloon uit de ER-basisindelingsconfiguratie wordt gebruikt om deze ER-indeling voor elke andere gebruiker uit te voeren.
5. Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.
6. Wijzig in het veld **Opmerking** de opmerkingen voor de automatisch gemaakte revisie van de bewerkbare sjabloon.
7. Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
