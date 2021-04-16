---
title: De structuur van een bedrijfsdocumentsjabloon bijwerken
description: In dit onderwerp wordt uitgelegd hoe u de structuur van een bedrijfsdocumentsjabloon kunt bijwerken met de functie Beheer van bedrijfsdocumenten.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750479"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="0aa3a-103">De structuur van een bedrijfsdocumentsjabloon bijwerken</span><span class="sxs-lookup"><span data-stu-id="0aa3a-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0aa3a-104">In het deelvenster **Sjabloonstructuur** van de sjablooneditor voor [Beheer van bedrijfsdocumenten](er-business-document-management.md) kunt u een bedrijfsdocumentsjabloon wijzigen door [nieuwe velden toe te voegen](er-bdm-add-field-to-excel-template.md) aan een sjabloon in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="0aa3a-105">De structuur van de sjabloon wordt vervolgens automatisch bijgewerkt in Dynamics 365 Finance, zodat deze de wijzigingen weergeeft die u hebt aangebracht in het deelvenster **Sjabloonstructuur**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="0aa3a-106">U kunt een sjabloon ook aanpassen door de online functionaliteit van Office 365 te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="0aa3a-107">U kunt bijvoorbeeld een nieuw benoemd item, zoals een afbeelding of vorm, toevoegen aan het bewerkbare werkblad.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="0aa3a-108">In dit geval wordt de structuur van de sjabloon niet automatisch bijgewerkt in Finance en wordt het artikel dat u hebt toegevoegd niet weergegeven in het deelvenster **Sjabloonstructuur**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="0aa3a-109">Werk de sjabloonstructuur handmatig bij in Finance door **Structuur bijwerken** te selecteren op de pagina van de sjablooneditor.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="0aa3a-110">Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="0aa3a-111">Voorbeeld: de structuur van een bedrijfsdocumentsjabloon bijwerken</span><span class="sxs-lookup"><span data-stu-id="0aa3a-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="0aa3a-112">In dit voorbeeld ziet u hoe een systeembeheerder de structuur van een bedrijfsdocumentsjabloon in Finance kan bijwerken nadat de sjabloon is gewijzigd in Office Online.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="0aa3a-113">In de volgende secties worden de stappen beschreven die hierbij worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="0aa3a-114">Een sjabloon voor een bedrijfsdocument voorbereiden voor bewerking</span><span class="sxs-lookup"><span data-stu-id="0aa3a-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="0aa3a-115">Voer de volgende procedures uit in [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa3a-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="0aa3a-116">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="0aa3a-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="0aa3a-117">ER-oplossingen importeren</span><span class="sxs-lookup"><span data-stu-id="0aa3a-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="0aa3a-118">Beheer van bedrijfsdocumenten inschakelen</span><span class="sxs-lookup"><span data-stu-id="0aa3a-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="0aa3a-119">Parameters configureren</span><span class="sxs-lookup"><span data-stu-id="0aa3a-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="0aa3a-120">Een bedrijfsdocumentsjabloon bewerken</span><span class="sxs-lookup"><span data-stu-id="0aa3a-120">Edit a business document template</span></span>

1. <span data-ttu-id="0aa3a-121">Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="0aa3a-122">Selecteer op de pagina **Een nieuwe sjabloon maken** de sjabloon **Vrije-tekstfactuur (ER-voorbeeld) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="0aa3a-123">Selecteer **Document maken**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-123">Select **Create document**.</span></span>
4. <span data-ttu-id="0aa3a-124">Voer in het veld **Titel** de tekst **FTI-voorbeeld Litware** in.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="0aa3a-125">Selecteer **OK** om de nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0aa3a-126">Als u zich nog niet hebt aangemeld bij Office Online, wordt u [naar de aanmeldingspagina voor Office 365 geleid](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="0aa3a-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="0aa3a-127">Selecteer de knop **Vorige** in de browser om terug te keren naar uw Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="0aa3a-128">De nieuwe sjabloon wordt geopend om te worden bewerkt in het ingesloten Excel online-besturingselement op de pagina van de sjablooneditor.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="0aa3a-129">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een bedrijfsdocumentsjabloon te bewerken](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="0aa3a-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="0aa3a-130">De huidige structuur van de bewerkbare sjabloon controleren</span><span class="sxs-lookup"><span data-stu-id="0aa3a-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="0aa3a-131">Selecteer in Excel online in het lint op het tabblad **Weergeven** in de groep **Weergeven** de optie **Rasterlijnen**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="0aa3a-132">Selecteer in de bewerkbare sjabloon de rechthoek boven de titel van de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="0aa3a-133">Deze rechthoek is een afbeelding met de naam **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="0aa3a-134">Als het deelvenster **Sjabloonstructuur** verborgen is, selecteert u **Structuur weergeven**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="0aa3a-135">Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="0aa3a-136">Zoals u ziet, wordt het item **rptHeaderCompLogo** in de sjabloonstructuur in Finance weergegeven als onderliggend item van **Rapport \> Factuur \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="0aa3a-137">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om de huidige structuur van een bewerkbare sjabloon te controleren](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="0aa3a-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="0aa3a-138">De structuur van een bedrijfsdocumentsjabloon bijwerken door een afbeelding te verwijderen</span><span class="sxs-lookup"><span data-stu-id="0aa3a-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="0aa3a-139">Selecteer in Excel online in de bewerkbare sjabloon de afbeelding **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="0aa3a-140">Voer een van de volgende stappen uit om de geselecteerde foto uit de bewerkbare sjabloon te verwijderen:</span><span class="sxs-lookup"><span data-stu-id="0aa3a-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="0aa3a-141">Selecteer de toets **Delete** op het toetsenbord.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="0aa3a-142">Selecteer de afbeelding en houd deze ingedrukt (of klik met de rechtermuisknop) en selecteer **Knippen**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0aa3a-143">Het item **rptHeaderCompLogo** is momenteel nog steeds aanwezig in de sjabloonstructuur in Finance, hoewel de foto niet meer in de Excel-sjabloon is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="0aa3a-144">Selecteer **Structuur bijwerken** om de structuur van de bewerkbare sjabloon te synchroniseren in Excel en Finance.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="0aa3a-145">Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="0aa3a-146">Zoals u ziet , is het item **rptHeaderCompLogo** niet meer opgenomen in de sjabloonstructuur in Finance.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="0aa3a-147">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een afbeelding te verwijderen uit een bedrijfsdocumentsjabloon](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="0aa3a-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="0aa3a-148">De structuur van een bedrijfsdocumentsjabloon bijwerken door een afbeelding toe te voegen</span><span class="sxs-lookup"><span data-stu-id="0aa3a-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="0aa3a-149">Selecteer in Excel online in het lint op het tabblad **Invoegen** in de groep **Illustraties** de optie **Afbeelding**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="0aa3a-150">Selecteer **Bestand kiezen**, blader naar de afbeelding die u wilt toevoegen, selecteer deze en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="0aa3a-151">Selecteer **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-151">Select **Insert**.</span></span>
4. <span data-ttu-id="0aa3a-152">Verplaats de nieuwe foto totdat deze op de juiste plaats staat.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="0aa3a-153">Excel benoemt standaard de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-153">By default, Excel names the picture.</span></span> <span data-ttu-id="0aa3a-154">De naam kan bijvoorbeeld **Afbeelding 2** zijn.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="0aa3a-155">Selecteer **Structuur bijwerken** om de structuur van de bewerkbare sjabloon te synchroniseren in Excel en Finance.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="0aa3a-156">Vouw in het deelvenster **Sjabloonstructuur** de optie **Rapport \> Factuur \> rptHeader \> rptHeaderPart1** uit.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="0aa3a-157">Zoals u ziet , is de nieuwe afbeelding nu opgenomen als item in de sjabloonstructuur in Finance.</span><span class="sxs-lookup"><span data-stu-id="0aa3a-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="0aa3a-158">[![De werkruimte Beheer van bedrijfsdocumenten gebruiken om een afbeelding toe te voegen aan een bedrijfsdocumentsjabloon](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="0aa3a-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="0aa3a-159">Verwante koppelingen</span><span class="sxs-lookup"><span data-stu-id="0aa3a-159">Related links</span></span>

[<span data-ttu-id="0aa3a-160">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="0aa3a-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0aa3a-161">Overzicht van Beheer van bedrijfsdocumenten</span><span class="sxs-lookup"><span data-stu-id="0aa3a-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]