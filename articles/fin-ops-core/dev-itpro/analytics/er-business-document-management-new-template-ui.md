---
title: Gebruikersinterface in Microsoft Office-stijl voor beheer van bedrijfsdocumenten (bevat video)
description: Dit onderwerp biedt uitleg over het gebruik van de nieuwe documentgebruikersinterface in de functie voor bedrijfsdocumentbeheer van het ER-raamwerk.
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: b0c481e73daf74803d3582e4089e76dcd383e8a4
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937551"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Gebruikersinterface in Microsoft Office-stijl voor beheer van bedrijfsdocumenten

[!include [banner](../includes/banner.md)]

Beheer van bedrijfsdocumenten stelt zakelijke gebruikers in staat zakelijke documentsjablonen te bewerken met een Microsoft 365-service of de juiste Microsoft Office-bureaubladtoepassing. Wijzigingen kunnen ontwerpwijzigingen of nieuwe implementaties bevatten, of gebruikers kunnen tijdelijke aanduidingen toevoegen om extra gegevens op te nemen zonder de broncode te hoeven wijzigen. Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) voor meer informatie over het werken met beheer van bedrijfsdocumenten.

De nieuwe gebruikersinterface (UI) is duidelijker en gemakkelijker te gebruiken. In het gebied **Bedrijfsdocument** worden alleen de sjablonen weergegeven die beschikbaar zijn voor de huidige provider. In de vorige gebruikersinterface bevatte het tabblad **Sjabloon** alle sjablonen die beschikbaar waren voor eventuele leveranciers. Daarnaast werden alle sjablonen getoond die door elke gebruiker met dezelfde rol waren gemaakt en bewerkt.

Met de knop **Nieuw document** kunt u een sjabloon maken en bewerken in een configuratie voor elektronische rapporteringsindeling die door een andere provider wordt geleverd. In het voorbeeld in dit onderwerp is de provider Microsoft. U kunt ook een sjabloon maken door uw eigen sjabloon te uploaden naar de Excel-indeling.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

De video [Het maken van een nieuw bedrijfsdocument met Bedrijfsdocumentbeheer](https://youtu.be/gAIYl-mM_pw) (hierboven weergegeven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>De nieuwe documentgebruikersinterface in Beheer van bedrijfsdocumenten beschikbaar maken

Als u de nieuwe documentgebruikersinterface wilt gebruiken in Beheer van bedrijfsdocumenten, moet u de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** inschakelen in het werkgebied **Functiebeheer**.

Voer de volgende stappen uit om deze functie in te schakelen voor alle rechtspersonen.

1. Selecteer in het werkgebied **Functiebeheer** op het tabblad **Alle** de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** in de lijst.
2. Selecteer **Nu inschakelen** om de geselecteerde functie in te schakelen.
3. Vernieuw de pagina om de nieuwe functie te openen.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Sjablonen bewerken die eigendom zijn van andere providers

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.

    ![Het werkgebied Beheer van bedrijfsdocumenten.](./media/BDM_overview_new_template1.png)

2. Selecteer op het tabblad **Selecteren** het document dat u als sjabloon wilt gebruiken, en selecteer vervolgens **Document maken**.

    ![Dialoogvenster Bedrijfsdocumenten.](./media/BDM_overview_new_template2.png)

3. Wijzig in het dialoogvenster Nieuw in het veld **Titel** de gewenste titel. De titeltekst wordt gebruikt als naam voor de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt. De conceptversie van deze configuratie (**Kopie FTI-rapport klant (GER)**) bevat de bewerkte sjabloon en wordt gebruikt om deze ER-indeling uit te voeren voor de huidige gebruiker. De oorspronkelijke sjabloon uit de ER-basisindelingsconfiguratie wordt gebruikt om deze ER-indeling voor elke andere gebruiker uit te voeren.
4. Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.
5. Wijzig in het veld **Opmerking** de opmerkingen voor de automatisch gemaakte revisie van de bewerkbare sjabloon.
6. Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.

    ![Dialoogvenster om document te maken.](./media/BDM_overview_new_template3.png)

De knop **Nieuw document** wordt gebruikt om een sjabloon te maken en bewerken in een ER-indelingsconfiguratie die door een andere provider wordt geleverd. In dit voorbeeld is de provider Microsoft. Wanneer u **Nieuw document** selecteert, ziet u alle sjablonen die eigendom zijn van huidige en andere providers. Nadat u de sjabloon hebt geselecteerd, wordt deze geopend om te worden bewerkt. De bewerkte sjabloon wordt vervolgens opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Een sjabloon uploaden met een bestaande Excel-indeling
Volg deze stappen om vereiste informatie te geven voordat u een sjabloon uploadt.

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.

    ![Het werkgebied Beheer van bedrijfsdocumenten.](./media/BDM_overview_new_template1.png)
    
2. Selecteer op de pagina **Een nieuwe sjabloon maken**, op het tabblad **Uploaden**, op het tabblad **Sjabloon** de optie **Bladeren** om te zoeken naar het Excel-bestand dat u als sjabloon wilt gebruiken. In de sectie **Sjabloon** worden de velden **Titel** en **Omschrijving** automatisch ingevuld. Deze geven de naam en omschrijving op van de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt. U kunt zo nodig deze velden bewerken.
3. Geef in de sectie **Documenttype** in het veld **Naam** het type bedrijfsdocument op. Deze waarde wordt gebruikt om de juiste gegevensbron (dat wil zeggen de ER-modelconfiguratie) te zoeken.

    ![Tabblad Sjabloon.](./media/BDM_overview_new_UI_import_21.jpg)

4. Selecteer op het tabblad **Gegevensbron** op het sneltabblad **Filter** de optie **Filter toepassen**. In de sectie **Gegevensbron** wordt het veld **Naam** automatisch ingevuld of kunt u handmatig een waarde selecteren. Met het filter kunt u zoeken naar de juiste gegevensbron op naam, omschrijving, land-/regiocode en type bedrijfsdocument.

    ![Tabblad Gegevensbron.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Het sneltabblad **Filter** wordt gebruikt om de juiste gegevensbron (dat wil zeggen de ER-modelconfiguratie) te zoeken. U kunt alle filtervelden bewerken om de meest geschikte gegevensbron te vinden voor het document dat u uploadt.
    > 
    > De voorwaarden op het sneltabblad **Filter** worden als **OR**-voorwaarden gebruikt.
    
5. Selecteer op het tabblad **Toewijzing** de optie **Automatisch detecteren**. Het veld **Hoofddefinitie** wordt automatisch ingevuld of u kunt handmatig een waarde selecteren. Op dit tabblad wordt de eindtoewijzing weergegeven voor de elementen van de sjabloon en het model.

    ![Tabblad Toewijzing.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Bij de toewijzing in de sectie **Sjabloonstructuur** wordt de volledige overeenkomst gebruikt tussen de labels of omschrijvingen in de gegevensbron in de taal van de gebruiker en de naam van de cel in de sjabloon.

6. Selecteer **Document maken** om te bevestigen dat u een sjabloon wilt maken en het bewerkingsproces te starten.

Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)voor meer informatie.

Als er geen provider is voor Elektronische rapportage, kunt u deze maken. Als er geen actieve provider is, kunt u kiezen om deze te activeren.

- Als u een provider wilt maken, wijzigt u de naam van de provider in het veld **Naam**, werkt u het internetadres van de nieuwe provider bij in het veld **Internetadres** en selecteert u **OK** om te bevestigen.

    ![Nieuwe provider maken in BDM.](./media/bdm_create_provider.png)
    
- Als u de bestaande provider wilt activeren, kiest u de naam van de provider in het veld **Configuratieprovider** en selecteert u **OK** om de provider als actief in te stellen.

    ![Provider activeren in BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Elke BDM-sjabloon verwijst naar de provider als auteur van de configuratie. Daarom is een actieve provider vereist voor de sjabloon.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
