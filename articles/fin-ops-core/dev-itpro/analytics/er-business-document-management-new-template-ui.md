---
title: Gebruikersinterface in Microsoft Office-stijl voor beheer van bedrijfsdocumenten
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
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881031"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="a8e18-103">Gebruikersinterface in Microsoft Office-stijl voor beheer van bedrijfsdocumenten</span><span class="sxs-lookup"><span data-stu-id="a8e18-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8e18-104">Beheer van bedrijfsdocumenten stelt zakelijke gebruikers in staat zakelijke documentsjablonen te bewerken met een Microsoft 365-service of de juiste Microsoft Office-bureaubladtoepassing.</span><span class="sxs-lookup"><span data-stu-id="a8e18-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="a8e18-105">Wijzigingen kunnen ontwerpwijzigingen of nieuwe implementaties bevatten, of gebruikers kunnen tijdelijke aanduidingen toevoegen om extra gegevens op te nemen zonder de broncode te hoeven wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="a8e18-106">Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) voor meer informatie over het werken met beheer van bedrijfsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="a8e18-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="a8e18-107">De nieuwe gebruikersinterface (UI) is duidelijker en gemakkelijker te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a8e18-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="a8e18-108">In het gebied **Bedrijfsdocument** worden alleen de sjablonen weergegeven die beschikbaar zijn voor de huidige provider.</span><span class="sxs-lookup"><span data-stu-id="a8e18-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="a8e18-109">In de vorige gebruikersinterface bevatte het tabblad **Sjabloon** alle sjablonen die beschikbaar waren voor eventuele leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a8e18-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="a8e18-110">Daarnaast werden alle sjablonen getoond die door elke gebruiker met dezelfde rol waren gemaakt en bewerkt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="a8e18-111">Met de knop **Nieuw document** kunt u een sjabloon maken en bewerken in een configuratie voor elektronische rapporteringsindeling die door een andere provider wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="a8e18-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="a8e18-112">In het voorbeeld in dit onderwerp is de provider Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8e18-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="a8e18-113">U kunt ook een sjabloon maken door uw eigen sjabloon te uploaden naar de Excel-indeling.</span><span class="sxs-lookup"><span data-stu-id="a8e18-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="a8e18-114">De video [Het maken van een nieuw bedrijfsdocument met Bedrijfsdocumentbeheer](https://youtu.be/gAIYl-mM_pw) (hierboven weergegeven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.</span><span class="sxs-lookup"><span data-stu-id="a8e18-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="a8e18-115">De nieuwe documentgebruikersinterface in Beheer van bedrijfsdocumenten beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="a8e18-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="a8e18-116">Als u de nieuwe documentgebruikersinterface wilt gebruiken in Beheer van bedrijfsdocumenten, moet u de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** inschakelen in het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="a8e18-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="a8e18-117">Voer de volgende stappen uit om deze functie in te schakelen voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="a8e18-118">Selecteer in het werkgebied **Functiebeheer** op het tabblad **Alle** de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a8e18-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="a8e18-119">Selecteer **Nu inschakelen** om de geselecteerde functie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="a8e18-120">Vernieuw de pagina om de nieuwe functie te openen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="a8e18-121">Sjablonen bewerken die eigendom zijn van andere providers</span><span class="sxs-lookup"><span data-stu-id="a8e18-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="a8e18-122">Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="a8e18-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Het werkgebied Beheer van bedrijfsdocumenten](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="a8e18-124">Selecteer op het tabblad **Selecteren** het document dat u als sjabloon wilt gebruiken, en selecteer vervolgens **Document maken**.</span><span class="sxs-lookup"><span data-stu-id="a8e18-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialoogvenster Bedrijfsdocumenten](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="a8e18-126">Wijzig in het dialoogvenster Nieuw in het veld **Titel** de gewenste titel.</span><span class="sxs-lookup"><span data-stu-id="a8e18-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="a8e18-127">De titeltekst wordt gebruikt als naam voor de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="a8e18-128">De conceptversie van deze configuratie (**Kopie FTI-rapport klant (GER)**) bevat de bewerkte sjabloon en wordt gebruikt om deze ER-indeling uit te voeren voor de huidige gebruiker.</span><span class="sxs-lookup"><span data-stu-id="a8e18-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="a8e18-129">De oorspronkelijke sjabloon uit de ER-basisindelingsconfiguratie wordt gebruikt om deze ER-indeling voor elke andere gebruiker uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="a8e18-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="a8e18-130">Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="a8e18-131">Wijzig in het veld **Opmerking** de opmerkingen voor de automatisch gemaakte revisie van de bewerkbare sjabloon.</span><span class="sxs-lookup"><span data-stu-id="a8e18-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="a8e18-132">Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialoogvenster om document te maken](./media/BDM_overview_new_template3.png)

<span data-ttu-id="a8e18-134">De knop **Nieuw document** wordt gebruikt om een sjabloon te maken en bewerken in een ER-indelingsconfiguratie die door een andere provider wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="a8e18-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="a8e18-135">In dit voorbeeld is de provider Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8e18-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="a8e18-136">Wanneer u **Nieuw document** selecteert, ziet u alle sjablonen die eigendom zijn van huidige en andere providers.</span><span class="sxs-lookup"><span data-stu-id="a8e18-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="a8e18-137">Nadat u de sjabloon hebt geselecteerd, wordt deze geopend om te worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="a8e18-138">De bewerkte sjabloon wordt vervolgens opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="a8e18-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="a8e18-139">Een sjabloon uploaden met een bestaande Excel-indeling</span><span class="sxs-lookup"><span data-stu-id="a8e18-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="a8e18-140">Volg deze stappen om vereiste informatie te geven voordat u een sjabloon uploadt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="a8e18-141">Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="a8e18-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Het werkgebied Beheer van bedrijfsdocumenten](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="a8e18-143">Selecteer op de pagina **Een nieuwe sjabloon maken**, op het tabblad **Uploaden**, op het tabblad **Sjabloon** de optie **Bladeren** om te zoeken naar het Excel-bestand dat u als sjabloon wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a8e18-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="a8e18-144">In de sectie **Sjabloon** worden de velden **Titel** en **Omschrijving** automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="a8e18-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="a8e18-145">Deze geven de naam en omschrijving op van de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="a8e18-146">U kunt zo nodig deze velden bewerken.</span><span class="sxs-lookup"><span data-stu-id="a8e18-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="a8e18-147">Geef in de sectie **Documenttype** in het veld **Naam** het type bedrijfsdocument op.</span><span class="sxs-lookup"><span data-stu-id="a8e18-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="a8e18-148">Deze waarde wordt gebruikt om de juiste gegevensbron (dat wil zeggen de ER-modelconfiguratie) te zoeken.</span><span class="sxs-lookup"><span data-stu-id="a8e18-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Tabblad Sjabloon](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="a8e18-150">Selecteer op het tabblad **Gegevensbron** op het sneltabblad **Filter** de optie **Filter toepassen**.</span><span class="sxs-lookup"><span data-stu-id="a8e18-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="a8e18-151">In de sectie **Gegevensbron** wordt het veld **Naam** automatisch ingevuld of kunt u handmatig een waarde selecteren.</span><span class="sxs-lookup"><span data-stu-id="a8e18-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="a8e18-152">Met het filter kunt u zoeken naar de juiste gegevensbron op naam, omschrijving, land-/regiocode en type bedrijfsdocument.</span><span class="sxs-lookup"><span data-stu-id="a8e18-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Tabblad Gegevensbron](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="a8e18-154">Het sneltabblad **Filter** wordt gebruikt om de juiste gegevensbron (dat wil zeggen de ER-modelconfiguratie) te zoeken.</span><span class="sxs-lookup"><span data-stu-id="a8e18-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="a8e18-155">U kunt alle filtervelden bewerken om de meest geschikte gegevensbron te vinden voor het document dat u uploadt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="a8e18-156">De voorwaarden op het sneltabblad **Filter** worden als **OR**-voorwaarden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a8e18-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="a8e18-157">Selecteer op het tabblad **Toewijzing** de optie **Automatisch detecteren**.</span><span class="sxs-lookup"><span data-stu-id="a8e18-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="a8e18-158">Het veld **Hoofddefinitie** wordt automatisch ingevuld of u kunt handmatig een waarde selecteren.</span><span class="sxs-lookup"><span data-stu-id="a8e18-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="a8e18-159">Op dit tabblad wordt de eindtoewijzing weergegeven voor de elementen van de sjabloon en het model.</span><span class="sxs-lookup"><span data-stu-id="a8e18-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Tabblad Toewijzing](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="a8e18-161">Bij de toewijzing in de sectie **Sjabloonstructuur** wordt de volledige overeenkomst gebruikt tussen de labels of omschrijvingen in de gegevensbron in de taal van de gebruiker en de naam van de cel in de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="a8e18-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="a8e18-162">Selecteer **Document maken** om te bevestigen dat u een sjabloon wilt maken en het bewerkingsproces te starten.</span><span class="sxs-lookup"><span data-stu-id="a8e18-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="a8e18-163">Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a8e18-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="a8e18-164">Als er geen provider is voor Elektronische rapportage, kunt u deze maken.</span><span class="sxs-lookup"><span data-stu-id="a8e18-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="a8e18-165">Als er geen actieve provider is, kunt u kiezen om deze te activeren.</span><span class="sxs-lookup"><span data-stu-id="a8e18-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="a8e18-166">Als u een provider wilt maken, wijzigt u de naam van de provider in het veld **Naam**, werkt u het internetadres van de nieuwe provider bij in het veld **Internetadres** en selecteert u **OK** om te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Nieuwe provider maken in BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="a8e18-168">Als u de bestaande provider wilt activeren, kiest u de naam van de provider in het veld **Configuratieprovider** en selecteert u **OK** om de provider als actief in te stellen.</span><span class="sxs-lookup"><span data-stu-id="a8e18-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Provider activeren in BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="a8e18-170">Elke BDM-sjabloon verwijst naar de provider als auteur van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="a8e18-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="a8e18-171">Daarom is een actieve provider vereist voor de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="a8e18-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
