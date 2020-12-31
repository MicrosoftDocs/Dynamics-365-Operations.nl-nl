---
title: Nieuwe documentgebruikersinterface in bedrijfsdocumentbeheer
description: Dit onderwerp biedt informatie over het gebruik van de nieuwe documentgebruikersinterface (UI) in de functie voor bedrijfsdocumentbeheer van het ER-raamwerk (elektronische rapportage).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681347"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="dc35c-103">Nieuwe documentgebruikersinterface in bedrijfsdocumentbeheer</span><span class="sxs-lookup"><span data-stu-id="dc35c-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc35c-104">Beheer van bedrijfsdocumenten stelt zakelijke gebruikers in staat zakelijke documentsjablonen te bewerken met een Microsoft 365-service of de juiste Microsoft Office-bureaubladtoepassing.</span><span class="sxs-lookup"><span data-stu-id="dc35c-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="dc35c-105">Wijzigingen kunnen ontwerpwijzigingen of nieuwe implementaties bevatten, of gebruikers kunnen tijdelijke aanduidingen toevoegen om extra gegevens op te nemen zonder de broncode te hoeven wijzigen.</span><span class="sxs-lookup"><span data-stu-id="dc35c-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="dc35c-106">Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) voor meer informatie over het werken met beheer van bedrijfsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="dc35c-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="dc35c-107">De nieuwe documentgebruikersinterface (UI) is duidelijker en gemakkelijker te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="dc35c-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="dc35c-108">In het gebied **Bedrijfsdocument** worden alleen de sjablonen weergegeven die beschikbaar zijn voor de huidige provider.</span><span class="sxs-lookup"><span data-stu-id="dc35c-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="dc35c-109">Met de knop **Nieuw document** kunnen gebruikers een sjabloon maken en bewerken in een configuratie voor elektronische rapporteringsindeling die door een andere provider wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="dc35c-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="dc35c-110">In het voorbeeld in dit onderwerp is de provider Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc35c-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="dc35c-111">De nieuwe documentgebruikersinterface in Beheer van bedrijfsdocumenten beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="dc35c-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="dc35c-112">Als u de nieuwe documentgebruikersinterface wilt gebruiken in Beheer van bedrijfsdocumenten, moet u de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** inschakelen in het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="dc35c-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="dc35c-113">Voer de volgende stappen uit om deze functie in te schakelen voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="dc35c-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="dc35c-114">Selecteer in het werkgebied **Functiebeheer** op het tabblad **Nieuw** de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="dc35c-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="dc35c-115">Selecteer **Nu inschakelen** om de geselecteerde functie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="dc35c-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="dc35c-116">Vernieuw de pagina om de nieuwe functie te openen.</span><span class="sxs-lookup"><span data-stu-id="dc35c-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="dc35c-117">Sjablonen bewerken die eigendom zijn van andere providers</span><span class="sxs-lookup"><span data-stu-id="dc35c-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="dc35c-118">Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.</span><span class="sxs-lookup"><span data-stu-id="dc35c-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Het werkgebied Beheer van bedrijfsdocumenten](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="dc35c-120">Selecteer in het dialoogvenster het document dat u als sjabloon wilt gebruiken, en selecteer vervolgens **Document maken**.</span><span class="sxs-lookup"><span data-stu-id="dc35c-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialoogvenster Bedrijfsdocumenten](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="dc35c-122">Wijzig in het dialoogvenster Nieuw in het veld **Titel** de gewenste titel.</span><span class="sxs-lookup"><span data-stu-id="dc35c-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="dc35c-123">De titeltekst wordt gebruikt als naam voor de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dc35c-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="dc35c-124">De conceptversie van deze configuratie (**Kopie FTI-rapport klant (GER)**) bevat de bewerkte sjabloon en wordt gebruikt om deze ER-indeling uit te voeren voor de huidige gebruiker.</span><span class="sxs-lookup"><span data-stu-id="dc35c-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="dc35c-125">De oorspronkelijke sjabloon uit de ER-basisindelingsconfiguratie wordt gebruikt om deze ER-indeling voor elke andere gebruiker uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="dc35c-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="dc35c-126">Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dc35c-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="dc35c-127">Wijzig in het veld **Opmerking** de opmerkingen voor de automatisch gemaakte revisie van de bewerkbare sjabloon.</span><span class="sxs-lookup"><span data-stu-id="dc35c-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="dc35c-128">Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="dc35c-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialoogvenster om document te maken](./media/BDM_overview_new_template3.png)

<span data-ttu-id="dc35c-130">De knop **Nieuw document** wordt gebruikt om een sjabloon te maken en bewerken in een ER-indelingsconfiguratie die door een andere provider wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="dc35c-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="dc35c-131">In dit voorbeeld is de provider Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc35c-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="dc35c-132">Wanneer u **Nieuw document** selecteert, ziet u alle sjablonen die eigendom zijn van huidige en andere providers.</span><span class="sxs-lookup"><span data-stu-id="dc35c-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="dc35c-133">Nadat u de sjabloon hebt geselecteerd, wordt deze geopend om te worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="dc35c-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="dc35c-134">De bewerkte sjabloon wordt vervolgens opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="dc35c-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="dc35c-135">Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="dc35c-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
