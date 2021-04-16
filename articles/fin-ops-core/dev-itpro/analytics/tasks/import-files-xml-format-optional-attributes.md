---
title: RCS‑bestanden in XML-indeling importeren met optionele kenmerken
description: Dit onderwerp biedt informatie over de manier waarop een gebruiker ER‑opmaakconfiguraties kan ontwerpen om bestanden in XML-indeling met optionele kenmerken te importeren.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744862"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="accbb-103">RCS‑bestanden in XML-indeling importeren met optionele kenmerken</span><span class="sxs-lookup"><span data-stu-id="accbb-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="accbb-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER‑indelingsconfiguratie kan ontwerpen om bestanden in XML‑indeling met optionele kenmerken te importeren.</span><span class="sxs-lookup"><span data-stu-id="accbb-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="accbb-105">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="accbb-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="accbb-106">Voordat u begint, moet u het bestand IncomingdocumentToLearnHowToHandleOptionalAttributes.xml downloaden uit het [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) en lokaal opslaan.</span><span class="sxs-lookup"><span data-stu-id="accbb-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="accbb-107">Ga naar **Alle werkgebieden** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="accbb-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="accbb-108">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="accbb-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="accbb-109">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="accbb-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="accbb-110">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="accbb-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="accbb-111">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="accbb-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="accbb-112">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="accbb-113">Typ in het veld **Naam** 'Model voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="accbb-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="accbb-114">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="accbb-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="accbb-115">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="accbb-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="accbb-116">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="accbb-117">Typ het veld **Naam** 'Basis'.</span><span class="sxs-lookup"><span data-stu-id="accbb-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="accbb-118">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="accbb-118">Click **Add**.</span></span>
8.    <span data-ttu-id="accbb-119">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="accbb-120">Typ het veld **Naam** 'Lijst'.</span><span class="sxs-lookup"><span data-stu-id="accbb-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="accbb-121">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="accbb-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="accbb-122">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="accbb-122">Click **Add**.</span></span>
12.    <span data-ttu-id="accbb-123">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="accbb-124">Typ in het veld **Naam** 'Code'.</span><span class="sxs-lookup"><span data-stu-id="accbb-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="accbb-125">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="accbb-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="accbb-126">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="accbb-126">Click **Add**.</span></span>
16.    <span data-ttu-id="accbb-127">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="accbb-127">Click **Save**.</span></span>
17.    <span data-ttu-id="accbb-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="accbb-128">Close the page.</span></span>
18.    <span data-ttu-id="accbb-129">Klik op **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="accbb-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="accbb-130">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="accbb-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="accbb-131">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="accbb-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="accbb-132">Een indeling maken voor het importeren van gegevens</span><span class="sxs-lookup"><span data-stu-id="accbb-132">Create a format for data import</span></span>
1.    <span data-ttu-id="accbb-133">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="accbb-134">Voer in het veld **Nieuw** in 'Indeling gebaseerd op gegevensmodel Model voor importeren van xml‑bestand'.</span><span class="sxs-lookup"><span data-stu-id="accbb-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="accbb-135">Typ in het veld **Naam** 'Indeling voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="accbb-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="accbb-136">Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.</span><span class="sxs-lookup"><span data-stu-id="accbb-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="accbb-137">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="accbb-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="accbb-138">Een indeling ontwerpen om het binnenkomende bestand in XML-indeling te parseren</span><span class="sxs-lookup"><span data-stu-id="accbb-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="accbb-139">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="accbb-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="accbb-140">Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="accbb-141">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="accbb-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="accbb-142">Typ het veld **Naam** 'basis'.</span><span class="sxs-lookup"><span data-stu-id="accbb-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="accbb-143">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="accbb-143">Click **OK**.</span></span>
6.    <span data-ttu-id="accbb-144">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="accbb-145">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="accbb-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="accbb-146">Typ in het veld **Naam** 'document'.</span><span class="sxs-lookup"><span data-stu-id="accbb-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="accbb-147">Selecteer in het veld **Multiplicity** **Eén veel**.</span><span class="sxs-lookup"><span data-stu-id="accbb-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="accbb-148">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="accbb-148">Click **OK**.</span></span>
11.    <span data-ttu-id="accbb-149">Selecteer in de structuur **basis\document**.</span><span class="sxs-lookup"><span data-stu-id="accbb-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="accbb-150">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="accbb-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="accbb-151">Selecteer **XML\Attribute** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="accbb-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="accbb-152">Typ in het veld **Naam** 'ID'.</span><span class="sxs-lookup"><span data-stu-id="accbb-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="accbb-153">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="accbb-153">Click **OK**.</span></span>
16.    <span data-ttu-id="accbb-154">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="accbb-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="accbb-155">Een indelingstoewijzing ontwerpen om geparseerde informatie op te slaan in het gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="accbb-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="accbb-156">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="accbb-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="accbb-157">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="accbb-157">Click **New**.</span></span>
3. <span data-ttu-id="accbb-158">Typ of selecteer een waarde in het veld **Definitie**.</span><span class="sxs-lookup"><span data-stu-id="accbb-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="accbb-159">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="accbb-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="accbb-160">Typ in het veld **Naam** 'Toewijzing'.</span><span class="sxs-lookup"><span data-stu-id="accbb-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="accbb-161">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="accbb-161">Click **Save**.</span></span>
7. <span data-ttu-id="accbb-162">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="accbb-162">Click **Designer**.</span></span>
8. <span data-ttu-id="accbb-163">Vouw in de structuur **indeling** uit.</span><span class="sxs-lookup"><span data-stu-id="accbb-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="accbb-164">Vouw in de structuur **format\root: XML Element(root)** uit.</span><span class="sxs-lookup"><span data-stu-id="accbb-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="accbb-165">Selecteer in de structuur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="accbb-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="accbb-166">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="accbb-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="accbb-167">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="accbb-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="accbb-168">Vouw in de structuur \**format\root: XML Element(root)\document: XML Element 1..* uit</span><span class="sxs-lookup"><span data-stu-id="accbb-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="accbb-169">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="accbb-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="accbb-170">Selecteer in de structuur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="accbb-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="accbb-171">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="accbb-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="accbb-172">Vouw in de structuur **Lijst = format.root.document** uit.</span><span class="sxs-lookup"><span data-stu-id="accbb-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="accbb-173">Selecteer in de structuur **Lijst = format.root.document\Code** uit.</span><span class="sxs-lookup"><span data-stu-id="accbb-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="accbb-174">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="accbb-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="accbb-175">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="accbb-175">Click **Save**.</span></span>
18.    <span data-ttu-id="accbb-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="accbb-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="accbb-177">Indelingstoewijzing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="accbb-177">Run format mapping</span></span>
1. <span data-ttu-id="accbb-178">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="accbb-178">Click **Run**.</span></span>
2. <span data-ttu-id="accbb-179">Klik op **Bladeren** en Selecteer **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="accbb-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="accbb-180">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="accbb-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="accbb-181">Het geselecteerde bestand is niet geïmporteerd omdat het indelingsontwerp ervan uitgaat dat er een id‑kenmerk bestaat voor het element document, maar het geïmporteerde bestand bevat geen kenmerk.</span><span class="sxs-lookup"><span data-stu-id="accbb-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="accbb-182">Indelingsstructuur wijzigen om het XML-kenmerk als optioneel te verwerken</span><span class="sxs-lookup"><span data-stu-id="accbb-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="accbb-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="accbb-183">Close the page.</span></span>
2. <span data-ttu-id="accbb-184">Vouw in de structuur **basis\document** uit.</span><span class="sxs-lookup"><span data-stu-id="accbb-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="accbb-185">Selecteer in de structuur **basis\document\id**.</span><span class="sxs-lookup"><span data-stu-id="accbb-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="accbb-186">Selecteer **Ja** in veld **Lege tekenreeks voor ontbrekende kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="accbb-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="accbb-187">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="accbb-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="accbb-188">Indelingstoewijzing uitvoeren voor het testen van de wijzigingen</span><span class="sxs-lookup"><span data-stu-id="accbb-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="accbb-189">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="accbb-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="accbb-190">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="accbb-190">Click **Run**.</span></span>
3. <span data-ttu-id="accbb-191">Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="accbb-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="accbb-192">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="accbb-192">Click **OK**.</span></span>
5. <span data-ttu-id="accbb-193">Bekijk het gegenereerde bestand.</span><span class="sxs-lookup"><span data-stu-id="accbb-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="accbb-194">Hetzelfde bestand is geïmporteerd als het opmaakontwerp, beschouw nu het kenmerk 'id' voor het element 'document' als optioneel.</span><span class="sxs-lookup"><span data-stu-id="accbb-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]