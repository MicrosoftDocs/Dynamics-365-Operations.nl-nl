---
title: ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling
description: In dit onderwerp wordt beschreven hoe rapportindelingen die zijn ontworpen om rapporten als Excel-werkmappen te genereren, kunnen worden geconfigureerd om rapporten als Word-documenten te genereren.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 413be634e80b87781444e1c1445c78691f4b4b0b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944287"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="e3b9c-103">ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling</span><span class="sxs-lookup"><span data-stu-id="e3b9c-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3b9c-104">Om rapporten als Microsoft Word-documenten te genereren, [configureert](../er-design-configuration-word.md) u een nieuwe [Electronic reporting (ER)](../general-electronic-reporting.md) [indeling](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="e3b9c-105">U kunt een ER-indeling die oorspronkelijk is ontworpen om rapporten te genereren als Excel-werkmappen ook hergebruiken.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="e3b9c-106">In dat geval moet u de Excel-sjabloon vervangen door een Word-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="e3b9c-107">De volgende procedures laten zien hoe een gebruiker met de rol Systeembeheerder of de rol Ontwikkelaar elektronische rapportage een ER-indeling kan configureren om rapporten te genereren als Word-bestanden door een ER-indeling opnieuw te gebruiken die is ontworpen om rapporten te genereren als Excel-bestanden.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="e3b9c-108">Deze procedures kunnen in het GBSI-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3b9c-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e3b9c-109">Prerequisites</span></span>

<span data-ttu-id="e3b9c-110">Als u deze procedures wilt uitvoeren, moet u eerst de stappen volgen in de taakbegeleiding [Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="e3b9c-111">U moet ook de volgende sjablonen downloaden en lokaal opslaan voor het voorbeeldrapport:</span><span class="sxs-lookup"><span data-stu-id="e3b9c-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="e3b9c-112">Sjabloon van betalingsrapport (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="e3b9c-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [<span data-ttu-id="e3b9c-113">Gebonden sjabloon van betalingsrapport (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="e3b9c-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

<span data-ttu-id="e3b9c-114">Deze procedures zijn voor een functie die is toegevoegd in Dynamics 365 for Operations versie 1611 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="e3b9c-115">De bestaande ER-rapportconfiguratie selecteren</span><span class="sxs-lookup"><span data-stu-id="e3b9c-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="e3b9c-116">Ga in Dynamics 365 Finance naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e3b9c-117">Controleer of de configuratieprovider **Litware, Inc.** als **actief** is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="e3b9c-118">Als dat niet zo is, voert u de stappen in de taakhandleiding [Configuratieproviders maken en ze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md) uit.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="e3b9c-119">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="e3b9c-120">U maakt opnieuw gebruik van de bestaande ER-configuratie die oorspronkelijk is opgezet voor het genereren van de rapportuitvoer in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="e3b9c-121">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **Voorbeeldwerkbladrapport**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3b9c-122">De conceptversie van de geselecteerde ER-indeling kan worden bewerkt op het tabblad **Versies**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="e3b9c-123">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-123">Select **Designer**.</span></span>
6. <span data-ttu-id="e3b9c-124">Op de pagina **Indelingsontwerper** ziet u dat de titel van het hoofdindelingselement aangeeft dat er momenteel een Excel-sjabloon wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![De bestaande configuratie selecteren](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="e3b9c-126">De gedownloade Word-sjabloon controleren</span><span class="sxs-lookup"><span data-stu-id="e3b9c-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="e3b9c-127">Open in de Word-bureaubladtoepassing het sjabloonbestand **SampleVendPaymDocReport.docx** dat u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="e3b9c-128">Controleer of de sjabloon alleen de indeling bevat van het document dat u wilt genereren als ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![De lay-out van de Word-sjabloon in de bureaubladtoepassing](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="e3b9c-130">De Excel-sjabloon vervangen door de Word-sjabloon en een aangepast XML-onderdeel toevoegen</span><span class="sxs-lookup"><span data-stu-id="e3b9c-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="e3b9c-131">Momenteel wordt het Excel-document gebruikt als sjabloon voor het genereren van de uitvoer in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="e3b9c-132">U vervangt deze sjabloon door de Word-sjabloon SampleVendPaymDocReport.docx die u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="e3b9c-133">U breidt de Word-sjabloon ook uit met een aangepast XML-onderdeel.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="e3b9c-134">Selecteer in Finance op de pagina **Indelingsontwerper** op het tabblad **Indeling** de optie **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="e3b9c-135">Selecteer op de pagina **Bijlagen** de optie **Verwijderen** om de bestaande Excel-sjabloon te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="e3b9c-136">Selecteer **Ja** om de wijziging te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="e3b9c-137">Selecteer **Nieuw** \> **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3b9c-138">U moet een documenttype selecteren dat is [geconfigureerd](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in de ER parameters om sjablonen in ER-indeling op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="e3b9c-139">Selecteer **Bladeren** en blader vervolgens naar het bestand **SampleVendPaymDocReport.docx** dat u eerder hebt gedownload en selecteer het.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="e3b9c-140">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-140">Select **OK**.</span></span>
6. <span data-ttu-id="e3b9c-141">Sluit de pagina **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="e3b9c-142">Typ of selecteer op de pagina **Indelingsontwerper** in het veld **Sjabloon** het bestand **SampleVendPaymDocReport.docx** dat die Word-sjabloon moet gebruiken in plaats van de Excel-sjabloon die eerder werd gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="e3b9c-143">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-143">Select **Save**.</span></span>

    <span data-ttu-id="e3b9c-144">De actie **Opslaan** legt niet alleen de configuratiewijzigingen vast, maar werkt ook tegelijk de gekoppelde Word-sjabloon bij.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="e3b9c-145">De hiërarchische structuur van de ontworpen indeling wordt toegevoegd aan het gekoppelde Word-document als een nieuw aangepast XML-onderdeel met de naam **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="e3b9c-146">De gekoppelde Word-sjabloon bevat de indeling van het document dat wordt gegenereerd als ER-uitvoer en de structuur van gegevens die ER in deze sjabloon tijdens runtime invult.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="e3b9c-147">De titel van het hoofdindelingselement geeft aan dat er momenteel een Word-sjabloon wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![De Excel-sjabloon vervangen door de Word-sjabloon en een aangepast XML-onderdeel toevoegen](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="e3b9c-149">Selecteer op het tabblad **Opmaak** de optie **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="e3b9c-150">U kunt nu de elementen van het aangepaste XML-onderdeel **Rapport** aan de inhoudsbesturingselementen van het Word-document toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="e3b9c-151">Als u ervaring hebt met het ontwerpen van Word-documenten als formulieren die [inhoudsbesturingselementen](/office/client-developer/word/content-controls-in-word) bevatten die toegewezen zijn aan elementen van [aangepaste XML-onderdelen](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), voert u alle stappen in de volgende procedure uit om het document te maken.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="e3b9c-152">Zie [Formulieren maken die gebruikers in Word kunnen invullen of afdrukken](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="e3b9c-153">Sla anders de volgende procedure over.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="e3b9c-154">Een Word-document met een aangepast XML-onderdeel ophalen en gegevenstoewijzing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="e3b9c-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="e3b9c-155">Selecteer in Finance op de pagina **Bijlagen** de optie **Openen** om de geselecteerde sjabloon te downloaden uit Finance en deze lokaal op te slaan als Word-document.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="e3b9c-156">Open in de Word-bureaubladtoepassing het document dat u zojuist hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="e3b9c-157">Selecteer op het tabblad **Ontwikkelaar** het deelvenster **XML-toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3b9c-158">Als het tabblad **Ontwikkelaar** niet op het lint wordt weergegeven, past u het lint aan om het toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="e3b9c-159">Selecteer in het deelvenster **XML-toewijzing** in het veld **Aangepast XML-onderdeel** het aangepaste XML-onderdeel **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="e3b9c-160">Wijs de elementen van het geselecteerde aangepaste XML-onderdeel **Rapport** en de inhoudsbesturingselementen van het Word-document toe.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="e3b9c-161">Sla het bijgewerkte Word-document lokaal op als **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="e3b9c-162">De Word-sjabloon controleren waarin het aangepaste XML-onderdeel is toegewezen aan inhoudsbesturingselementen</span><span class="sxs-lookup"><span data-stu-id="e3b9c-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="e3b9c-163">Open in de Word-bureaubladtoepassing het sjabloonbestand **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="e3b9c-164">Controleer of de sjabloon de indeling bevat van het document dat u wilt genereren als ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="e3b9c-165">De inhoudsbesturingselementen die worden gebruikt als tijdelijke aanduidingen voor gegevens die ER in deze sjabloon tijdens runtime zal invoeren, zijn gebaseerd op de toewijzingen die zijn geconfigureerd tussen elementen van het aangepaste XML-onderdeel **Rapport** en de inhoudsbesturingselementen van het Word-document.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Voorbeeld van Word-sjabloon in de bureaubladtoepassing](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="e3b9c-167">De Word-sjabloon uploaden waarin het aangepaste XML-onderdeel is toegewezen aan inhoudsbesturingselementen</span><span class="sxs-lookup"><span data-stu-id="e3b9c-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="e3b9c-168">Selecteer in Finance op de pagina **Bijlagen** de optie **Verwijderen** om de Word-sjabloon te verwijderen die geen toewijzingen bevat tussen elementen van het aangepaste XML-onderdeel **Rapport** en inhoudsbesturingselementen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="e3b9c-169">Selecteer **Ja** om de wijziging te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="e3b9c-170">Selecteer **Nieuw** \> **Bestand** om een nieuw sjabloonbestand toe te voegen dat toewijzingen bevat tussen elementen van het aangepaste XML-onderdeel **Rapport** en inhoudsbesturingselementen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3b9c-171">U moet een documenttype selecteren dat is [geconfigureerd](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in de ER parameters om sjablonen in ER-indeling op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="e3b9c-172">Selecteer **Bladeren**, en blader naar en selecteer het bestand **SampleVendPaymDocReportBounded.docx** dat u hebt gedownload of voorbereid door de procedure uit te voeren in het gedeelte [Een Word-document met een aangepast XML-onderdeel ophalen en gegevenstoewijzing uitvoeren](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="e3b9c-173">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-173">Select **OK**.</span></span>
5. <span data-ttu-id="e3b9c-174">Sluit de pagina **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="e3b9c-175">Selecteer op de pagina **Indelingsontwerper** in het veld **Sjabloon** het document dat u zojuist hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="e3b9c-176">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-176">Select **Save**.</span></span>
8. <span data-ttu-id="e3b9c-177">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="e3b9c-178">De geconfigureerde indeling als uitvoerbaar markeren</span><span class="sxs-lookup"><span data-stu-id="e3b9c-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="e3b9c-179">Als u de conceptversie van de bewerkbare indeling wilt uitvoeren, moet u deze [uitvoerbaar](../er-quick-start2-customize-report.md#MarkFormatRunnable) maken.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="e3b9c-180">Selecteer in Finance op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="e3b9c-181">Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="e3b9c-182">Selecteer zo nodig **Bewerken** om de huidige pagina bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="e3b9c-183">Stel voor de momenteel geselecteerde **Voorbeeldwerkbladrapport**-configuratie de optie **Concept uitvoeren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="e3b9c-184">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="e3b9c-185">De indeling uitvoeren voor het maken van uitvoer in Word-indeling</span><span class="sxs-lookup"><span data-stu-id="e3b9c-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="e3b9c-186">Ga in Finance naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="e3b9c-187">Selecteer in een eerder ingevoerd betalingsjournaal **Regels**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="e3b9c-188">Selecteer op de pagina **Leveranciersbetalingen** alle rijen in het raster.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="e3b9c-189">Selecteer **Betalingsstatus** \> **Geen**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-189">Select **Payment status** \> **None**.</span></span>

    ![Betalingen voor verwerking op de pagina Leveranciersbetalingen](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="e3b9c-191">Selecteer **Betalingen genereren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="e3b9c-192">Voer de volgende stappen uit in het dialoogvenster:</span><span class="sxs-lookup"><span data-stu-id="e3b9c-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="e3b9c-193">Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="e3b9c-194">Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="e3b9c-195">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-195">Select **OK**.</span></span>

7. <span data-ttu-id="e3b9c-196">Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="e3b9c-197">De gegenereerde uitvoer wordt weergegeven in Word-indeling en bevat de details van de verwerkte betalingen.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="e3b9c-198">Analyseer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-198">Analyze the generated output.</span></span>

    ![Gegenereerde uitvoer in Word-indeling](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="e3b9c-200">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e3b9c-200">Additional resources</span></span>

- [<span data-ttu-id="e3b9c-201">Een nieuwe ER-configuratie ontwerpen om rapporten in Word-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="e3b9c-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="e3b9c-202">Afbeeldingen en vormen insluiten in documenten die u genereert met ER</span><span class="sxs-lookup"><span data-stu-id="e3b9c-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
