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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8c3a905c90f5dd4ad3487f004a958c0dcd52115d
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893242"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="9f317-103">Nieuwe velden toevoegen aan een sjabloon voor bedrijfsdocumenten in Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="9f317-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9f317-104">U kunt nieuwe velden toevoegen aan een sjabloon die wordt gebruikt om bedrijfsdocumenten te genereren in Microsoft Excel-indeling.</span><span class="sxs-lookup"><span data-stu-id="9f317-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="9f317-105">Deze velden kunnen worden toegevoegd als tijdelijke aanduidingen die worden gebruikt om gegenereerde documenten te vullen met vereiste informatie uit de toepassing.</span><span class="sxs-lookup"><span data-stu-id="9f317-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="9f317-106">Voor elk veld dat u toevoegt, kunt u ook een binding met de gegevensbronnen opgeven om op te geven welke toepassingsgegevens in het veld moeten worden ingevoerd wanneer de sjabloon wordt gebruikt om bedrijfsdocumenten te genereren.</span><span class="sxs-lookup"><span data-stu-id="9f317-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="9f317-107">Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9f317-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="9f317-108">In dit voorbeeld ziet u hoe u een sjabloon bijwerkt om de velden in te vullen in formulieren met vrije-tekstfacturen die worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="9f317-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="9f317-109">Beheer van bedrijfsdocumenten configureren om sjablonen te bewerken</span><span class="sxs-lookup"><span data-stu-id="9f317-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="9f317-110">Omdat Beheer van bedrijfsdocumenten (BDM) is gebouwd op basis van het kader voor [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md), moet u de vereiste ER- en BDM-parameters configureren voordat u aan de slag kunt met Beheer van bedrijfsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="9f317-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="9f317-111">Meld u als systeembeheerder aan bij het exemplaar van Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9f317-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="9f317-112">Voer de volgende stappen van het voorbeeld in het onderwerp [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) uit:</span><span class="sxs-lookup"><span data-stu-id="9f317-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="9f317-113">Configureer ER-parameters.</span><span class="sxs-lookup"><span data-stu-id="9f317-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="9f317-114">Schakel Beheer van bedrijfsdocumenten in.</span><span class="sxs-lookup"><span data-stu-id="9f317-114">Turn on BDM.</span></span>

<span data-ttu-id="9f317-115">U kunt Beheer van bedrijfsdocumenten nu gebruiken om sjablonen voor bedrijfsdocumenten te bewerken.</span><span class="sxs-lookup"><span data-stu-id="9f317-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="9f317-116">ER-oplossingen die een sjabloon bevatten importeren</span><span class="sxs-lookup"><span data-stu-id="9f317-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="9f317-117">In het voorbeeld in deze procedure wordt de officieel gepubliceerde ER-oplossing gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9f317-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="9f317-118">U moet de ER-configuraties van deze oplossing importeren in uw huidige exemplaar van Finance.</span><span class="sxs-lookup"><span data-stu-id="9f317-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="9f317-119">De ER-indelingsconfiguratie **Vrije-tekstfactuur (Excel)** van deze oplossing bevat de sjabloon voor bedrijfsdocumenten in Excel-indeling die kan worden bewerkt met Beheer van bedrijfsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="9f317-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="9f317-120">Importeer de meest recente versie van deze ER-indelingsconfiguratie uit Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="9f317-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="9f317-121">De bijbehorende configuraties voor ER-gegevensmodellen en ER-modeltoewijzingen worden automatisch geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="9f317-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="9f317-122">Zie [De levenscyclus van de configuratie van elektronische rapportage beheren](general-electronic-reporting-manage-configuration-lifecycle.md) voor meer informatie over het importeren van ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="9f317-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS-bibliotheek voor gedeelde activa](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="9f317-124">De sjabloon voor de ER-oplossing bewerken</span><span class="sxs-lookup"><span data-stu-id="9f317-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="9f317-125">Meld u aan als een gebruiker met toegang tot het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="9f317-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="9f317-126">Open het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="9f317-126">Open the **Business document management** workspace.</span></span>

    ![Het werkgebied Beheer van bedrijfsdocumenten](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="9f317-128">Selecteer in het raster de sjabloon **Vrije-tekstfactuur (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="9f317-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="9f317-129">Selecteer in het rechterdeelvenster de optie **Nieuwe sjabloon** om een nieuwe sjabloon te maken die is gebaseerd op de geselecteerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9f317-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="9f317-130">Voer in het veld **Titel** de tekst **Vrije-tekstfactuur (Excel) Contoso** in als de titel van de nieuwe sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9f317-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="9f317-131">Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="9f317-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="9f317-132">De pagina BDM-sjablooneditor wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9f317-132">The BDM template editor page appears.</span></span> <span data-ttu-id="9f317-133">U kunt Microsoft 365 gebruiken om de geselecteerde sjabloon online te bewerken in het ingesloten besturingselement.</span><span class="sxs-lookup"><span data-stu-id="9f317-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![De pagina BDM-sjablooneditor](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="9f317-135">Het label voor een nieuw veld toevoegen aan de sjabloon</span><span class="sxs-lookup"><span data-stu-id="9f317-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="9f317-136">Op de pagina BDM-sjablooneditor schakelt u in het Excel-lint op het tabblad Weergave de selectievakjes **Koppen** en **Rasterlijnen** in voor de bewerkbare Excel-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9f317-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![De ingeschakelde selectievakjes Koppen en Rasterlijnen](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="9f317-138">Selecteer de cellen **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="9f317-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="9f317-139">Selecteer op het Excel-lint op het tabblad **Start** de optie **Samenvoegen en centreren** om de geselecteerde cellen samen te voegen in een nieuwe samengevoegde cel **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="9f317-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="9f317-140">Voer **URL** in de samengevoegde cel **E8:F8** in.</span><span class="sxs-lookup"><span data-stu-id="9f317-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="9f317-141">Selecteer de samengevoegde cel **E7: F7**, selecteer **Opmaak kopiëren/plakken** en selecteer vervolgens de samengevoegde cel **E8:F8** als u de cel op dezelfde manier wilt opmaken als de samengevoegde cel **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="9f317-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Nieuw veldlabel toegevoegd aan de sjabloon](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="9f317-143">De sjabloon opmaken om ruimte te reserveren voor een nieuw veld</span><span class="sxs-lookup"><span data-stu-id="9f317-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="9f317-144">Selecteer op de pagina BDM-sjablooneditor de samengevoegde cel **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="9f317-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="9f317-145">Selecteer op het Excel-lint op het tabblad **Start** de optie **Samenvoegen en centreren** om de geselecteerde cellen samen te voegen in een nieuwe samengevoegde cel **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="9f317-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="9f317-146">Selecteer de samengevoegde cel **G7: H7**, selecteer **Opmaak kopiëren/plakken** en selecteer vervolgens de samengevoegde cel **G8:H8** als u de cel op dezelfde manier wilt opmaken als de samengevoegde cel **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="9f317-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Gereserveerde ruimte voor het nieuwe veld](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="9f317-148">In het veld **Naam** selecteert u **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="9f317-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="9f317-149">Het bereik **CompanyInfo** van de huidige Excel-sjabloon bevat alle velden die worden gebruikt om de koptekst van een gegenereerd rapport te vullen met de details van het huidige bedrijf als verkoper.</span><span class="sxs-lookup"><span data-stu-id="9f317-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Geselecteerd bereik CompanyInfo](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="9f317-151">Een nieuw veld aan de sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="9f317-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="9f317-152">Selecteer op de pagina **BDM-sjablooneditor** in het actievenster de optie **Indeling weergeven**.</span><span class="sxs-lookup"><span data-stu-id="9f317-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="9f317-153">Selecteer **Toevoegen** in het deelvenster **Sjabloonstructuur**.</span><span class="sxs-lookup"><span data-stu-id="9f317-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f317-154">U moet de sectie aanpassen van de sjabloon die u als nieuw veld wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9f317-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="9f317-155">U hebt deze correctie al doorgevoerd door de samengevoegde cel **G8:H8** op te maken.</span><span class="sxs-lookup"><span data-stu-id="9f317-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Een nieuw veld aan de sjabloon toevoegen](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="9f317-157">Selecteer **Excel\cel** om een nieuw veld toe te voegen als een cel in de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9f317-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="9f317-158">U kunt **Excel\bereik** selecteren als u een nieuw bereik aan de sjabloon wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f317-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="9f317-159">Het ingevoerde bereik kan meerdere cellen bevatten.</span><span class="sxs-lookup"><span data-stu-id="9f317-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="9f317-160">U kunt deze cellen later toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f317-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="9f317-161">Het sjabloononderdeel **CompanyInfo** is automatisch geselecteerd in het deelvenster **Sjabloonstructuur** omdat dit het meest geschikte bovenliggende onderdeel in de huidige sjabloonstructuur is voor het veld dat u toevoegt.</span><span class="sxs-lookup"><span data-stu-id="9f317-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="9f317-162">Voer in het veld **Excel-bereik** de waarde **CompanyURL_Value** in.</span><span class="sxs-lookup"><span data-stu-id="9f317-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="9f317-163">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f317-163">Select **OK**.</span></span>

    ![Het veld CompanyURL_Value dat aan de sjabloonstructuur is toegevoegd](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="9f317-165">Selecteer in het deelvenster **Sjabloonstructuur** de knop met het weglatingsteken (...) en selecteer **Bindingen weergeven**.</span><span class="sxs-lookup"><span data-stu-id="9f317-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Bindingen weergeven geselecteerd](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="9f317-167">In het deelvenster **Sjabloonstructuur** worden nu de gegevensbronnen weergegeven die in de onderliggende ER-indeling beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="9f317-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="9f317-168">Selecteer **CompanyInfo_Value** als het veld dat u wilt binden aan een gegevensbron van de onderliggende ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="9f317-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="9f317-169">Vouw in de sectie **Gegevensbronnen** van het deelvenster **Sjabloonstructuur** de items **Model \> InvoiceBase \> CompanyInfo** uit.</span><span class="sxs-lookup"><span data-stu-id="9f317-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="9f317-170">Selecteer onder **CompanyInfo** het item **WebsiteURI** uit.</span><span class="sxs-lookup"><span data-stu-id="9f317-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Het geselecteerde item WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="9f317-172">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="9f317-172">Select **Bind**.</span></span>
11. <span data-ttu-id="9f317-173">Selecteer in het deelvenster **Sjabloonstructuur** de optie **Opslaan** en sluit de pagina BDM-sjablooneditor.</span><span class="sxs-lookup"><span data-stu-id="9f317-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="9f317-174">In het werkgebied **Beheer van bedrijfsdocumenten** wordt op het tabblad **Sjabloon** in het rechterdeel de bijgewerkte sjabloon weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9f317-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="9f317-175">In het raster is het veld **Status** voor de bewerkte sjabloon gewijzigd in **Concept** en is het veld **Revisie** niet meer leeg.</span><span class="sxs-lookup"><span data-stu-id="9f317-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="9f317-176">Dit betekent dat het proces van het bewerken van deze sjabloon is gestart.</span><span class="sxs-lookup"><span data-stu-id="9f317-176">These changes indicate that the process of editing this template has been started.</span></span>

![Bewerkte sjabloon in het werkgebied Beheer van bedrijfsdocumenten](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="9f317-178">Bedrijfsinstellingen controleren</span><span class="sxs-lookup"><span data-stu-id="9f317-178">Review company settings</span></span>

1.  <span data-ttu-id="9f317-179">Ga naar **Organisatiebeheer \> Organisaties \> Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="9f317-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="9f317-180">Controleer op het sneltabblad **Gegevens contactpersoon** of de bedrijfs-URL is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="9f317-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Bedrijfs-URL die is ingevoerd op de pagina Rechtspersonen](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="9f317-182">Bedrijfsdocumenten genereren om de bijgewerkte sjabloon te testen</span><span class="sxs-lookup"><span data-stu-id="9f317-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="9f317-183">Wijzig in de toepassing het bedrijf in **USMF** en ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="9f317-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="9f317-184">Selecteer de factuur **FTI-00000002** en selecteer **Afdrukbeheer**.</span><span class="sxs-lookup"><span data-stu-id="9f317-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="9f317-185">Vouw in het linkerdeelvenster **Module - Klanten \> Documenten \> Vrije-tekstfactuur** uit.</span><span class="sxs-lookup"><span data-stu-id="9f317-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="9f317-186">Selecteer onder **Vrije-tekstfactuur** het niveau **Oorspronkelijk document** om het bereik van facturen voor verwerking op te geven.</span><span class="sxs-lookup"><span data-stu-id="9f317-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="9f317-187">Selecteer in het rechterdeel venster in het veld **Rapportindeling** de sjabloon **Vrije-tekstfactuur (Excel) Contoso** voor het opgegeven documentniveau.</span><span class="sxs-lookup"><span data-stu-id="9f317-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![De sjabloon Vrije-tekstfactuur (Excel) Contoso is geselecteerd](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="9f317-189">Druk op **ESC** om de huidige pagina te sluiten.</span><span class="sxs-lookup"><span data-stu-id="9f317-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="9f317-190">Selecteer **Afdrukken \> Selectie**.</span><span class="sxs-lookup"><span data-stu-id="9f317-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="9f317-191">Down load het gegenereerde document en open het in Excel.</span><span class="sxs-lookup"><span data-stu-id="9f317-191">Download the generated document, and open it in Excel.</span></span>

    ![Vrije-tekstfactuur in Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="9f317-193">De gewijzigde sjabloon wordt gebruikt om het rapport met vrije-tekstfacturen voor het geselecteerde artikel te genereren.</span><span class="sxs-lookup"><span data-stu-id="9f317-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="9f317-194">Als u wilt analyseren hoe dit rapport wordt beïnvloed door wijzigingen die u aanbrengt in de sjabloon, voert u dit rapport uit in één toepassingssessie direct nadat u de sjabloon hebt gewijzigd in een andere toepassingssessie.</span><span class="sxs-lookup"><span data-stu-id="9f317-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="9f317-195">Verwante koppelingen</span><span class="sxs-lookup"><span data-stu-id="9f317-195">Related links</span></span>

[<span data-ttu-id="9f317-196">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="9f317-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="9f317-197">Overzicht van Beheer van bedrijfsdocumenten</span><span class="sxs-lookup"><span data-stu-id="9f317-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="9f317-198">Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling</span><span class="sxs-lookup"><span data-stu-id="9f317-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
