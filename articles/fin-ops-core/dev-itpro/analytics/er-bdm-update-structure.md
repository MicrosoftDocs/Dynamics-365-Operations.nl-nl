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
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="9cd1f-103">De structuur van een bedrijfsdocumentsjabloon bijwerken</span><span class="sxs-lookup"><span data-stu-id="9cd1f-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9cd1f-104">In het deelvenster **Sjabloonstructuur** van de sjablooneditor voor [Beheer van bedrijfsdocumenten](er-business-document-management.md) kunt u een bedrijfsdocumentsjabloon wijzigen door [nieuwe velden toe te voegen](er-bdm-add-field-to-excel-template.md) aan een sjabloon in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="9cd1f-105">De structuur van de sjabloon wordt vervolgens automatisch bijgewerkt in Dynamics 365 Finance, zodat deze de wijzigingen weergeeft die u hebt aangebracht in het deelvenster **Sjabloonstructuur**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="9cd1f-106">U kunt een sjabloon ook aanpassen door de online functionaliteit van Office 365 te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="9cd1f-107">U kunt bijvoorbeeld een nieuw benoemd item, zoals een afbeelding of vorm, toevoegen aan het bewerkbare werkblad.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="9cd1f-108">In dit geval wordt de structuur van de sjabloon niet automatisch bijgewerkt in Finance en wordt het artikel dat u hebt toegevoegd niet weergegeven in het deelvenster **Sjabloonstructuur**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="9cd1f-109">Werk de sjabloonstructuur handmatig bij in Finance door **Structuur bijwerken** te selecteren op de pagina van de sjablooneditor.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="9cd1f-110">Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="9cd1f-111">Voorbeeld: de structuur van een bedrijfsdocumentsjabloon bijwerken</span><span class="sxs-lookup"><span data-stu-id="9cd1f-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="9cd1f-112">In dit voorbeeld ziet u hoe een systeembeheerder de structuur van een bedrijfsdocumentsjabloon in Finance kan bijwerken nadat de sjabloon is gewijzigd in Office Online.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="9cd1f-113">In de volgende secties worden de stappen beschreven die hierbij worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="9cd1f-114">Een sjabloon voor een bedrijfsdocument voorbereiden voor bewerking</span><span class="sxs-lookup"><span data-stu-id="9cd1f-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="9cd1f-115">Voer de volgende procedures uit in [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd1f-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="9cd1f-116">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="9cd1f-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="9cd1f-117">ER-oplossingen importeren</span><span class="sxs-lookup"><span data-stu-id="9cd1f-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="9cd1f-118">Beheer van bedrijfsdocumenten inschakelen</span><span class="sxs-lookup"><span data-stu-id="9cd1f-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="9cd1f-119">Parameters configureren</span><span class="sxs-lookup"><span data-stu-id="9cd1f-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="9cd1f-120">Een bedrijfsdocumentsjabloon bewerken</span><span class="sxs-lookup"><span data-stu-id="9cd1f-120">Edit a business document template</span></span>

1. <span data-ttu-id="9cd1f-121">Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="9cd1f-122">Selecteer op de pagina **Een nieuwe sjabloon maken** de sjabloon **Vrije-tekstfactuur (ER-voorbeeld) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="9cd1f-123">Selecteer **Document maken**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-123">Select **Create document**.</span></span>
4. <span data-ttu-id="9cd1f-124">Voer in het veld **Titel** de tekst **FTI-voorbeeld Litware** in.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="9cd1f-125">Selecteer **OK** om de nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9cd1f-126">Als u zich nog niet hebt aangemeld bij Office Online, wordt u [naar de aanmeldingspagina voor Office 365 geleid](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span><span class="sxs-lookup"><span data-stu-id="9cd1f-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span></span> <span data-ttu-id="9cd1f-127">Selecteer de knop **Vorige** in de browser om terug te keren naar uw Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="9cd1f-128">De nieuwe sjabloon wordt geopend om te worden bewerkt in het ingesloten Excel online-besturingselement op de pagina van de sjablooneditor.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="9cd1f-129">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een bedrijfsdocumentsjabloon te bewerken](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="9cd1f-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="9cd1f-130">De huidige structuur van de bewerkbare sjabloon controleren</span><span class="sxs-lookup"><span data-stu-id="9cd1f-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="9cd1f-131">Selecteer in Excel online in het lint op het tabblad **Weergeven** in de groep **Weergeven** de optie **Rasterlijnen**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="9cd1f-132">Selecteer in de bewerkbare sjabloon de rechthoek boven de titel van de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="9cd1f-133">Deze rechthoek is een afbeelding met de naam **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="9cd1f-134">Als het deelvenster **Sjabloonstructuur** verborgen is, selecteert u **Structuur weergeven**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="9cd1f-135">Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="9cd1f-136">Zoals u ziet, wordt het item **rptHeaderCompLogo** in de sjabloonstructuur in Finance weergegeven als onderliggend item van **Rapport \> Factuur \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="9cd1f-137">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om de huidige structuur van een bewerkbare sjabloon te controleren](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="9cd1f-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="9cd1f-138">De structuur van een bedrijfsdocumentsjabloon bijwerken door een afbeelding te verwijderen</span><span class="sxs-lookup"><span data-stu-id="9cd1f-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="9cd1f-139">Selecteer in Excel online in de bewerkbare sjabloon de afbeelding **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="9cd1f-140">Voer een van de volgende stappen uit om de geselecteerde foto uit de bewerkbare sjabloon te verwijderen:</span><span class="sxs-lookup"><span data-stu-id="9cd1f-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="9cd1f-141">Selecteer de toets **Delete** op het toetsenbord.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="9cd1f-142">Selecteer de afbeelding en houd deze ingedrukt (of klik met de rechtermuisknop) en selecteer **Knippen**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9cd1f-143">Het item **rptHeaderCompLogo** is momenteel nog steeds aanwezig in de sjabloonstructuur in Finance, hoewel de foto niet meer in de Excel-sjabloon is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="9cd1f-144">Selecteer **Structuur bijwerken** om de structuur van de bewerkbare sjabloon te synchroniseren in Excel en Finance.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="9cd1f-145">Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="9cd1f-146">Zoals u ziet , is het item **rptHeaderCompLogo** niet meer opgenomen in de sjabloonstructuur in Finance.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="9cd1f-147">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een afbeelding te verwijderen uit een bedrijfsdocumentsjabloon](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="9cd1f-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="9cd1f-148">De structuur van een bedrijfsdocumentsjabloon bijwerken door een afbeelding toe te voegen</span><span class="sxs-lookup"><span data-stu-id="9cd1f-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="9cd1f-149">Selecteer in Excel online in het lint op het tabblad **Invoegen** in de groep **Illustraties** de optie **Afbeelding**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="9cd1f-150">Selecteer **Bestand kiezen**, blader naar de afbeelding die u wilt toevoegen, selecteer deze en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="9cd1f-151">Selecteer **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-151">Select **Insert**.</span></span>
4. <span data-ttu-id="9cd1f-152">Verplaats de nieuwe foto totdat deze op de juiste plaats staat.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="9cd1f-153">Excel benoemt standaard de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-153">By default, Excel names the picture.</span></span> <span data-ttu-id="9cd1f-154">De naam kan bijvoorbeeld **Afbeelding 2** zijn.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="9cd1f-155">Selecteer **Structuur bijwerken** om de structuur van de bewerkbare sjabloon te synchroniseren in Excel en Finance.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="9cd1f-156">Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="9cd1f-157">Zoals u ziet , is de nieuwe afbeelding nu opgenomen als item in de sjabloonstructuur in Finance.</span><span class="sxs-lookup"><span data-stu-id="9cd1f-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="9cd1f-158">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een afbeelding toe te voegen aan een bedrijfsdocumentsjabloon](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="9cd1f-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="9cd1f-159">Verwante koppelingen</span><span class="sxs-lookup"><span data-stu-id="9cd1f-159">Related links</span></span>

[<span data-ttu-id="9cd1f-160">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="9cd1f-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="9cd1f-161">Overzicht van Beheer van bedrijfsdocumenten</span><span class="sxs-lookup"><span data-stu-id="9cd1f-161">Business document management overview</span></span>](er-business-document-management.md)
