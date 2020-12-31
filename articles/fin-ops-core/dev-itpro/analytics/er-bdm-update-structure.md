---
title: De structuur van een bedrijfsdocumentsjabloon bijwerken
description: In dit onderwerp wordt uitgelegd hoe u de structuur van een bedrijfsdocumentsjabloon kunt bijwerken met de functie Beheer van bedrijfsdocumenten.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd279b28c43e22bec6bf814845fe97828bc96d81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681323"
---
# <a name="update-the-structure-of-a-business-document-template"></a>De structuur van een bedrijfsdocumentsjabloon bijwerken 

[!include[banner](../includes/banner.md)]

In het deelvenster **Sjabloonstructuur** van de sjablooneditor voor [Beheer van bedrijfsdocumenten](er-business-document-management.md) kunt u een bedrijfsdocumentsjabloon wijzigen door [nieuwe velden toe te voegen](er-bdm-add-field-to-excel-template.md) aan een sjabloon in Microsoft Excel. De structuur van de sjabloon wordt vervolgens automatisch bijgewerkt in Dynamics 365 Finance, zodat deze de wijzigingen weergeeft die u hebt aangebracht in het deelvenster **Sjabloonstructuur**.

U kunt een sjabloon ook aanpassen door de online functionaliteit van Office 365 te gebruiken. U kunt bijvoorbeeld een nieuw benoemd item, zoals een afbeelding of vorm, toevoegen aan het bewerkbare werkblad. In dit geval wordt de structuur van de sjabloon niet automatisch bijgewerkt in Finance en wordt het artikel dat u hebt toegevoegd niet weergegeven in het deelvenster **Sjabloonstructuur**. Werk de sjabloonstructuur handmatig bij in Finance door **Structuur bijwerken** te selecteren op de pagina van de sjablooneditor.

Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Voorbeeld: de structuur van een bedrijfsdocumentsjabloon bijwerken

In dit voorbeeld ziet u hoe een systeembeheerder de structuur van een bedrijfsdocumentsjabloon in Finance kan bijwerken nadat de sjabloon is gewijzigd in Office Online. In de volgende secties worden de stappen beschreven die hierbij worden uitgevoerd.

### <a name="prepare-a-business-document-template-for-editing"></a>Een sjabloon voor een bedrijfsdocument voorbereiden voor bewerking

Voer de volgende procedures uit in [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) .

1. [ER-parameters configureren](er-business-document-management.md#configure-er-parameters)
2. [ER-oplossingen importeren](er-business-document-management.md#import-er-solutions)
3. [Beheer van bedrijfsdocumenten inschakelen](er-business-document-management.md#enable-business-document-management)
4. [Parameters configureren](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Een bedrijfsdocumentsjabloon bewerken

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.
2. Selecteer op de pagina **Een nieuwe sjabloon maken** de sjabloon **Vrije-tekstfactuur (ER-voorbeeld) (Excel)**.
3. Selecteer **Document maken**.
4. Voer in het veld **Titel** de tekst **FTI-voorbeeld Litware** in.
5. Selecteer **OK** om de nieuwe sjabloon te maken.

    > [!NOTE]
    > Als u zich nog niet hebt aangemeld bij Office Online, wordt u [naar de aanmeldingspagina voor Office 365 geleid](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page). Selecteer de knop **Vorige** in de browser om terug te keren naar uw Finance-omgeving.

    De nieuwe sjabloon wordt geopend om te worden bewerkt in het ingesloten Excel online-besturingselement op de pagina van de sjablooneditor.

[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een bedrijfsdocumentsjabloon te bewerken](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>De huidige structuur van de bewerkbare sjabloon controleren

1. Selecteer in Excel online in het lint op het tabblad **Weergeven** in de groep **Weergeven** de optie **Rasterlijnen**.
2. Selecteer in de bewerkbare sjabloon de rechthoek boven de titel van de sjabloon. Deze rechthoek is een afbeelding met de naam **rptHeaderCompLogo**.
3. Als het deelvenster **Sjabloonstructuur** verborgen is, selecteert u **Structuur weergeven**.
4. Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.
5. Zoals u ziet, wordt het item **rptHeaderCompLogo** in de sjabloonstructuur in Finance weergegeven als onderliggend item van **Rapport \> Factuur \> rptHeader \> rptHeaderPart1**.

[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om de huidige structuur van een bewerkbare sjabloon te controleren](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>De structuur van een bedrijfsdocumentsjabloon bijwerken door een afbeelding te verwijderen

1. Selecteer in Excel online in de bewerkbare sjabloon de afbeelding **rptHeaderCompLogo**.
2. Voer een van de volgende stappen uit om de geselecteerde foto uit de bewerkbare sjabloon te verwijderen:

    - Selecteer de toets **Delete** op het toetsenbord.
    - Selecteer de afbeelding en houd deze ingedrukt (of klik met de rechtermuisknop) en selecteer **Knippen**.

    > [!NOTE]
    > Het item **rptHeaderCompLogo** is momenteel nog steeds aanwezig in de sjabloonstructuur in Finance, hoewel de foto niet meer in de Excel-sjabloon is opgenomen.

3. Selecteer **Structuur bijwerken** om de structuur van de bewerkbare sjabloon te synchroniseren in Excel en Finance.
4. Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.
5. Zoals u ziet , is het item **rptHeaderCompLogo** niet meer opgenomen in de sjabloonstructuur in Finance.

[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een afbeelding te verwijderen uit een bedrijfsdocumentsjabloon](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>De structuur van een bedrijfsdocumentsjabloon bijwerken door een afbeelding toe te voegen

1. Selecteer in Excel online in het lint op het tabblad **Invoegen** in de groep **Illustraties** de optie **Afbeelding**.
2. Selecteer **Bestand kiezen**, blader naar de afbeelding die u wilt toevoegen, selecteer deze en selecteer vervolgens **OK**.
3. Selecteer **Invoegen**.
4. Verplaats de nieuwe foto totdat deze op de juiste plaats staat. Excel benoemt standaard de afbeelding. De naam kan bijvoorbeeld **Afbeelding 2** zijn.
5. Selecteer **Structuur bijwerken** om de structuur van de bewerkbare sjabloon te synchroniseren in Excel en Finance.
6. Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.
7. Zoals u ziet , is de nieuwe afbeelding nu opgenomen als item in de sjabloonstructuur in Finance.

[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een afbeelding toe te voegen aan een bedrijfsdocumentsjabloon](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Verwante koppelingen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)
