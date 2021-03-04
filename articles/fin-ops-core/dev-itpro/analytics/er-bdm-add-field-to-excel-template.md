---
title: Nieuwe velden toevoegen aan een sjabloon voor bedrijfsdocumenten in Microsoft Excel
description: Dit onderwerp bevat informatie over het toevoegen van nieuwe velden aan een sjabloon voor bedrijfsdocumenten in Microsoft Excel met de functie voor beheer van bedrijfsdocumenten.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: fcfbcb021b192cef75d59b0db1796e994f3dc27d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681370"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Nieuwe velden toevoegen aan een sjabloon voor bedrijfsdocumenten in Microsoft Excel

[!include[banner](../includes/banner.md)]

U kunt nieuwe velden toevoegen aan een sjabloon die wordt gebruikt om bedrijfsdocumenten te genereren in Microsoft Excel-indeling. Deze velden kunnen worden toegevoegd als tijdelijke aanduidingen die worden gebruikt om gegenereerde documenten te vullen met vereiste informatie uit de toepassing. Voor elk veld dat u toevoegt, kunt u ook een binding met de gegevensbronnen opgeven om op te geven welke toepassingsgegevens in het veld moeten worden ingevoerd wanneer de sjabloon wordt gebruikt om bedrijfsdocumenten te genereren.

Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren. In dit voorbeeld ziet u hoe u een sjabloon bijwerkt om de velden in te vullen in formulieren met vrije-tekstfacturen die worden gegenereerd.

## <a name="configure-business-document-management-to-edit-templates"></a>Beheer van bedrijfsdocumenten configureren om sjablonen te bewerken

Omdat Beheer van bedrijfsdocumenten (BDM) is gebouwd op basis van het kader voor [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md), moet u de vereiste ER- en BDM-parameters configureren voordat u aan de slag kunt met Beheer van bedrijfsdocumenten.

1.  Meld u als systeembeheerder aan bij het exemplaar van Microsoft Dynamics 365 Finance.
2.  Voer de volgende stappen van het voorbeeld in het onderwerp [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) uit:

    1.  Configureer ER-parameters.
    2.  Schakel Beheer van bedrijfsdocumenten in.

U kunt Beheer van bedrijfsdocumenten nu gebruiken om sjablonen voor bedrijfsdocumenten te bewerken.

## <a name="import-er-solutions-that-contain-a-template"></a>ER-oplossingen die een sjabloon bevatten importeren

In het voorbeeld in deze procedure wordt de officieel gepubliceerde ER-oplossing gebruikt. U moet de ER-configuraties van deze oplossing importeren in uw huidige exemplaar van Finance.

De ER-indelingsconfiguratie **Vrije-tekstfactuur (Excel)** van deze oplossing bevat de sjabloon voor bedrijfsdocumenten in Excel-indeling die kan worden bewerkt met Beheer van bedrijfsdocumenten. Importeer de meest recente versie van deze ER-indelingsconfiguratie uit Microsoft Dynamics Lifecycle Service (LCS). De bijbehorende configuraties voor ER-gegevensmodellen en ER-modeltoewijzingen worden automatisch geïmporteerd.

Zie [De levenscyclus van de configuratie van elektronische rapportage beheren](general-electronic-reporting-manage-configuration-lifecycle.md) voor meer informatie over het importeren van ER-configuraties.

![LCS-bibliotheek voor gedeelde activa](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>De sjabloon voor de ER-oplossing bewerken

1.  Meld u aan als een gebruiker met toegang tot het werkgebied **Beheer van bedrijfsdocumenten**.
2.  Open het werkgebied **Beheer van bedrijfsdocumenten**.

    ![Het werkgebied Beheer van bedrijfsdocumenten](./media/BDM-AddFldExcel-Workspace.png)

3.  Selecteer in het raster de sjabloon **Vrije-tekstfactuur (Excel)**.
4.  Selecteer in het rechterdeelvenster de optie **Nieuwe sjabloon** om een nieuwe sjabloon te maken die is gebaseerd op de geselecteerde sjabloon.
5.  Voer in het veld **Titel** de tekst **Vrije-tekstfactuur (Excel) Contoso** in als de titel van de nieuwe sjabloon.
6.  Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.

De pagina BDM-sjablooneditor wordt weergegeven. U kunt Microsoft 365 gebruiken om de geselecteerde sjabloon online te bewerken in het ingesloten besturingselement.

![De pagina BDM-sjablooneditor](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Het label voor een nieuw veld toevoegen aan de sjabloon

1.  Op de pagina BDM-sjablooneditor schakelt u in het Excel-lint op het tabblad Weergave de selectievakjes **Koppen** en **Rasterlijnen** in voor de bewerkbare Excel-sjabloon.

    ![De ingeschakelde selectievakjes Koppen en Rasterlijnen](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Selecteer de cellen **E8:F8**.
3.  Selecteer op het Excel-lint op het tabblad **Start** de optie **Samenvoegen en centreren** om de geselecteerde cellen samen te voegen in een nieuwe samengevoegde cel **E8:F8**.
4.  Voer **URL** in de samengevoegde cel **E8:F8** in.
5.  Selecteer de samengevoegde cel **E7: F7**, selecteer **Opmaak kopiëren/plakken** en selecteer vervolgens de samengevoegde cel **E8:F8** als u de cel op dezelfde manier wilt opmaken als de samengevoegde cel **E7:F7**.

    ![Nieuw veldlabel toegevoegd aan de sjabloon](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>De sjabloon opmaken om ruimte te reserveren voor een nieuw veld

1.  Selecteer op de pagina BDM-sjablooneditor de samengevoegde cel **G8:H8**.
2.  Selecteer op het Excel-lint op het tabblad **Start** de optie **Samenvoegen en centreren** om de geselecteerde cellen samen te voegen in een nieuwe samengevoegde cel **G8:H8**.
3.  Selecteer de samengevoegde cel **G7: H7**, selecteer **Opmaak kopiëren/plakken** en selecteer vervolgens de samengevoegde cel **G8:H8** als u de cel op dezelfde manier wilt opmaken als de samengevoegde cel **G7:H7**.

    ![Gereserveerde ruimte voor het nieuwe veld](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  In het veld **Naam** selecteert u **CompanyInfo**.

    Het bereik **CompanyInfo** van de huidige Excel-sjabloon bevat alle velden die worden gebruikt om de koptekst van een gegenereerd rapport te vullen met de details van het huidige bedrijf als verkoper.

    ![Geselecteerd bereik CompanyInfo](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Een nieuw veld aan de sjabloon toevoegen

1.  Selecteer op de pagina **BDM-sjablooneditor** in het actievenster de optie **Indeling weergeven**.
2.  Selecteer **Toevoegen** in het deelvenster **Sjabloonstructuur**.

    > [!NOTE]
    > U moet de sectie aanpassen van de sjabloon die u als nieuw veld wilt gebruiken. U hebt deze correctie al doorgevoerd door de samengevoegde cel **G8:H8** op te maken.

    ![Een nieuw veld aan de sjabloon toevoegen](./media/BDM-AddFldExcel-AddCell.png)

3.  Selecteer **Excel\cel** om een nieuw veld toe te voegen als een cel in de sjabloon.

    U kunt **Excel\bereik** selecteren als u een nieuw bereik aan de sjabloon wilt toevoegen. Het ingevoerde bereik kan meerdere cellen bevatten. U kunt deze cellen later toevoegen.
    
    Het sjabloononderdeel **CompanyInfo** is automatisch geselecteerd in het deelvenster **Sjabloonstructuur** omdat dit het meest geschikte bovenliggende onderdeel in de huidige sjabloonstructuur is voor het veld dat u toevoegt.
    
4.  Voer in het veld **Excel-bereik** de waarde **CompanyURL_Value** in.
5.  Selecteer **OK**.

    ![Het veld CompanyURL_Value dat aan de sjabloonstructuur is toegevoegd](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Selecteer in het deelvenster **Sjabloonstructuur** de knop met het weglatingsteken (...) en selecteer **Bindingen weergeven**.

    ![Bindingen weergeven geselecteerd](./media/BDM-AddFldExcel-ShowBindings.png)

    In het deelvenster **Sjabloonstructuur** worden nu de gegevensbronnen weergegeven die in de onderliggende ER-indeling beschikbaar zijn.

7.  Selecteer **CompanyInfo_Value** als het veld dat u wilt binden aan een gegevensbron van de onderliggende ER-indeling.
8.  Vouw in de sectie **Gegevensbronnen** van het deelvenster **Sjabloonstructuur** de items **Model \> InvoiceBase \> CompanyInfo** uit.
9.  Selecteer onder **CompanyInfo** het item **WebsiteURI** uit.

    ![Het geselecteerde item WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. Selecteer **Binden**.
11. Selecteer in het deelvenster **Sjabloonstructuur** de optie **Opslaan** en sluit de pagina BDM-sjablooneditor.

In het werkgebied **Beheer van bedrijfsdocumenten** wordt op het tabblad **Sjabloon** in het rechterdeel de bijgewerkte sjabloon weergegeven. In het raster is het veld **Status** voor de bewerkte sjabloon gewijzigd in **Concept** en is het veld **Revisie** niet meer leeg. Dit betekent dat het proces van het bewerken van deze sjabloon is gestart.

![Bewerkte sjabloon in het werkgebied Beheer van bedrijfsdocumenten](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Bedrijfsinstellingen controleren

1.  Ga naar **Organisatiebeheer \> Organisaties \> Rechtspersonen**.
2.  Controleer op het sneltabblad **Gegevens contactpersoon** of de bedrijfs-URL is ingevoerd.

![Bedrijfs-URL die is ingevoerd op de pagina Rechtspersonen](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Bedrijfsdocumenten genereren om de bijgewerkte sjabloon te testen

1.  Wijzig in de toepassing het bedrijf in **USMF** en ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.
2.  Selecteer de factuur **FTI-00000002** en selecteer **Afdrukbeheer**.
3.  Vouw in het linkerdeelvenster **Module - Klanten \> Documenten \> Vrije-tekstfactuur** uit.
4.  Selecteer onder **Vrije-tekstfactuur** het niveau **Oorspronkelijk document** om het bereik van facturen voor verwerking op te geven.
5.  Selecteer in het rechterdeel venster in het veld **Rapportindeling** de sjabloon **Vrije-tekstfactuur (Excel) Contoso** voor het opgegeven documentniveau.

    ![De sjabloon Vrije-tekstfactuur (Excel) Contoso is geselecteerd](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Druk op **ESC** om de huidige pagina te sluiten.
7.  Selecteer **Afdrukken \> Selectie**.
8.  Down load het gegenereerde document en open het in Excel.

    ![Vrije-tekstfactuur in Excel](./media/BDM-AddFldExcel-PreviewReport.png)

De gewijzigde sjabloon wordt gebruikt om het rapport met vrije-tekstfacturen voor het geselecteerde artikel te genereren. Als u wilt analyseren hoe dit rapport wordt beïnvloed door wijzigingen die u aanbrengt in de sjabloon, voert u dit rapport uit in één toepassingssessie direct nadat u de sjabloon hebt gewijzigd in een andere toepassingssessie.

## <a name="related-links"></a>Verwante koppelingen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)

[Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]