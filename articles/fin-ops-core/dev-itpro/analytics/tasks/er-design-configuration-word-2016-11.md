---
title: ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling
description: In dit onderwerp wordt beschreven hoe rapportindelingen die zijn ontworpen om rapporten als Excel-werkmappen te genereren, kunnen worden geconfigureerd om rapporten als Word-documenten te genereren.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769913fd0344eb276b3b1bd055255272ca5dfffd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092711"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling

[!include [banner](../../includes/banner.md)]

Om rapporten als Microsoft Word-documenten te genereren, [configureert](../er-design-configuration-word.md) u een nieuwe [Electronic reporting (ER)](../general-electronic-reporting.md) [indeling](../general-electronic-reporting.md#FormatComponentOutbound). U kunt een ER-indeling die oorspronkelijk is ontworpen om rapporten te genereren als Excel-werkmappen ook hergebruiken. In dat geval moet u de Excel-sjabloon vervangen door een Word-sjabloon.

De volgende procedures laten zien hoe een gebruiker met de rol Systeembeheerder of de rol Ontwikkelaar elektronische rapportage een ER-indeling kan configureren om rapporten te genereren als Word-bestanden door een ER-indeling opnieuw te gebruiken die is ontworpen om rapporten te genereren als Excel-bestanden.

Deze procedures kunnen in het GBSI-bedrijf worden uitgevoerd.

## <a name="prerequisites"></a>Vereisten

Als u deze procedures wilt uitvoeren, moet u eerst de stappen volgen in de taakbegeleiding [Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](er-design-reports-openxml-2016-11.md).

U moet ook de volgende sjablonen downloaden en lokaal opslaan voor het voorbeeldrapport:

- [Sjabloon van betalingsrapport (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=862266)
- [Gebonden sjabloon van betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=862266)

Deze procedures zijn voor een functie die is toegevoegd in Dynamics 365 for Operations versie 1611 (november 2016).

## <a name="select-the-existing-er-report-configuration"></a>De bestaande ER-rapportconfiguratie selecteren

1. Ga in Dynamics 365 Finance naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Controleer of de configuratieprovider **Litware, Inc.** als **actief** is gemarkeerd. Als dat niet zo is, voert u de stappen in de taakhandleiding [Configuratieproviders maken en ze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md) uit.
3. Selecteer **Rapportageconfiguraties**. U maakt opnieuw gebruik van de bestaande ER-configuratie die oorspronkelijk is opgezet voor het genereren van de rapportuitvoer in OPENXML-indeling.
4. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **Voorbeeldwerkbladrapport**.

    > [!NOTE]
    > De conceptversie van de geselecteerde ER-indeling kan worden bewerkt op het tabblad **Versies**.

5. Selecteer **Ontwerper**.
6. Op de pagina **Indelingsontwerper** ziet u dat de titel van het hoofdindelingselement aangeeft dat er momenteel een Excel-sjabloon wordt gebruikt.

![De bestaande configuratie selecteren](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>De gedownloade Word-sjabloon controleren

1. Open in de Word-bureaubladtoepassing het sjabloonbestand **SampleVendPaymDocReport.docx** dat u eerder hebt gedownload.
2. Controleer of de sjabloon alleen de indeling bevat van het document dat u wilt genereren als ER-uitvoer.

![De lay-out van de Word-sjabloon in de bureaubladtoepassing](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>De Excel-sjabloon vervangen door de Word-sjabloon en een aangepast XML-onderdeel toevoegen

Momenteel wordt het Excel-document gebruikt als sjabloon voor het genereren van de uitvoer in OPENXML-indeling. U vervangt deze sjabloon door de Word-sjabloon SampleVendPaymDocReport.docx die u eerder hebt gedownload. U breidt de Word-sjabloon ook uit met een aangepast XML-onderdeel.

1. Selecteer in Finance op de pagina **Indelingsontwerper** op het tabblad **Indeling** de optie **Bijlagen**.
2. Selecteer op de pagina **Bijlagen** de optie **Verwijderen** om de bestaande Excel-sjabloon te verwijderen. Selecteer **Ja** om de wijziging te bevestigen.
3. Selecteer **Nieuw** \> **Bestand**.

    > [!NOTE]
    > U moet een documenttype selecteren dat is [geconfigureerd](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in de ER parameters om sjablonen in ER-indeling op te slaan.

4. Selecteer **Bladeren** en blader vervolgens naar het bestand **SampleVendPaymDocReport.docx** dat u eerder hebt gedownload en selecteer het.
5. Selecteer **OK**.
6. Sluit de pagina **Bijlagen**.
7. Typ of selecteer op de pagina **Indelingsontwerper** in het veld **Sjabloon** het bestand **SampleVendPaymDocReport.docx** dat die Word-sjabloon moet gebruiken in plaats van de Excel-sjabloon die eerder werd gebruikt.
8. Selecteer **Opslaan**.

    De actie **Opslaan** legt niet alleen de configuratiewijzigingen vast, maar werkt ook tegelijk de gekoppelde Word-sjabloon bij. De hiërarchische structuur van de ontworpen indeling wordt toegevoegd aan het gekoppelde Word-document als een nieuw aangepast XML-onderdeel met de naam **Rapport**. De gekoppelde Word-sjabloon bevat de indeling van het document dat wordt gegenereerd als ER-uitvoer en de structuur van gegevens die ER in deze sjabloon tijdens runtime invult.

9. De titel van het hoofdindelingselement geeft aan dat er momenteel een Word-sjabloon wordt gebruikt.

    ![De Excel-sjabloon vervangen door de Word-sjabloon en een aangepast XML-onderdeel toevoegen](../media/er-design-configuration-word-2016-11-image03.gif)

10. Selecteer op het tabblad **Opmaak** de optie **Bijlagen**.

U kunt nu de elementen van het aangepaste XML-onderdeel **Rapport** aan de inhoudsbesturingselementen van het Word-document toewijzen.

Als u ervaring hebt met het ontwerpen van Word-documenten als formulieren die [inhoudsbesturingselementen](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) bevatten die toegewezen zijn aan elementen van [aangepaste XML-onderdelen](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), voert u alle stappen in de volgende procedure uit om het document te maken. Zie [Formulieren maken die gebruikers in Word kunnen invullen of afdrukken](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b) voor meer informatie. Sla anders de volgende procedure over.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Een Word-document met een aangepast XML-onderdeel ophalen en gegevenstoewijzing uitvoeren

1. Selecteer in Finance op de pagina **Bijlagen** de optie **Openen** om de geselecteerde sjabloon te downloaden uit Finance en deze lokaal op te slaan als Word-document.
3. Open in de Word-bureaubladtoepassing het document dat u zojuist hebt gedownload.
4. Selecteer op het tabblad **Ontwikkelaar** het deelvenster **XML-toewijzing**.

    > [!NOTE]
    > Als het tabblad **Ontwikkelaar** niet op het lint wordt weergegeven, past u het lint aan om het toe te voegen.

5. Selecteer in het deelvenster **XML-toewijzing** in het veld **Aangepast XML-onderdeel** het aangepaste XML-onderdeel **Rapport**.
6. Wijs de elementen van het geselecteerde aangepaste XML-onderdeel **Rapport** en de inhoudsbesturingselementen van het Word-document toe.
7. Sla het bijgewerkte Word-document lokaal op als **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>De Word-sjabloon controleren waarin het aangepaste XML-onderdeel is toegewezen aan inhoudsbesturingselementen

1. Open in de Word-bureaubladtoepassing het sjabloonbestand **SampleVendPaymDocReportBounded.docx**.
2. Controleer of de sjabloon de indeling bevat van het document dat u wilt genereren als ER-uitvoer. De inhoudsbesturingselementen die worden gebruikt als tijdelijke aanduidingen voor gegevens die ER in deze sjabloon tijdens runtime zal invoeren, zijn gebaseerd op de toewijzingen die zijn geconfigureerd tussen elementen van het aangepaste XML-onderdeel **Rapport** en de inhoudsbesturingselementen van het Word-document.

![Voorbeeld van Word-sjabloon in de bureaubladtoepassing](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>De Word-sjabloon uploaden waarin het aangepaste XML-onderdeel is toegewezen aan inhoudsbesturingselementen

1. Selecteer in Finance op de pagina **Bijlagen** de optie **Verwijderen** om de Word-sjabloon te verwijderen die geen toewijzingen bevat tussen elementen van het aangepaste XML-onderdeel **Rapport** en inhoudsbesturingselementen. Selecteer **Ja** om de wijziging te bevestigen.
2. Selecteer **Nieuw** \> **Bestand** om een nieuw sjabloonbestand toe te voegen dat toewijzingen bevat tussen elementen van het aangepaste XML-onderdeel **Rapport** en inhoudsbesturingselementen.

    > [!NOTE]
    > U moet een documenttype selecteren dat is [geconfigureerd](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in de ER parameters om sjablonen in ER-indeling op te slaan.

3. Selecteer **Bladeren**, en blader naar en selecteer het bestand **SampleVendPaymDocReportBounded.docx** dat u hebt gedownload of voorbereid door de procedure uit te voeren in het gedeelte [Een Word-document met een aangepast XML-onderdeel ophalen en gegevenstoewijzing uitvoeren](#get-word-doc).
4. Selecteer **OK**.
5. Sluit de pagina **Bijlagen**.
6. Selecteer op de pagina **Indelingsontwerper** in het veld **Sjabloon** het document dat u zojuist hebt gedownload.
7. Selecteer **Opslaan**.
8. Sluit de pagina **Indelingsontwerper**.

## <a name="mark-the-configured-format-as-runnable"></a>De geconfigureerde indeling als uitvoerbaar markeren

Als u de conceptversie van de bewerkbare indeling wilt uitvoeren, moet u deze [uitvoerbaar](../er-quick-start2-customize-report.md#MarkFormatRunnable) maken.

1. Selecteer in Finance op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
2. Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.
3. Selecteer zo nodig **Bewerken** om de huidige pagina bewerkbaar te maken.
4. Stel voor de momenteel geselecteerde **Voorbeeldwerkbladrapport**-configuratie de optie **Concept uitvoeren** in op **Ja**.
5. Selecteer **Opslaan**.

## <a name="run-the-format-to-create-output-in-word-format"></a>De indeling uitvoeren voor het maken van uitvoer in Word-indeling

1. Ga in Finance naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer in een eerder ingevoerd betalingsjournaal **Regels**.
3. Selecteer op de pagina **Leveranciersbetalingen** alle rijen in het raster.
4. Selecteer **Betalingsstatus** \> **Geen**.

    ![Betalingen voor verwerking op de pagina Leveranciersbetalingen](../media/er-design-configuration-word-2016-11-image05.png)

5. Selecteer **Betalingen genereren** in het actievenster.
6. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.
    2. Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.
    3. Selecteer **OK**.

7. Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.
8. De gegenereerde uitvoer wordt weergegeven in Word-indeling en bevat de details van de verwerkte betalingen. Analyseer de gegenereerde uitvoer.

    ![Gegenereerde uitvoer in Word-indeling](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Een nieuwe ER-configuratie ontwerpen om rapporten in Word-indeling te genereren](../er-design-configuration-word.md)
- [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]