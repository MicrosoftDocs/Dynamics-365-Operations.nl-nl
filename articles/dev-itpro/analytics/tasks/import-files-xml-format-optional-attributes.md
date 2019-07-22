---
title: RCS‑bestanden in XML-indeling importeren met optionele kenmerken
description: Dit onderwerp biedt informatie over de manier waarop een gebruiker ER‑opmaakconfiguraties kan ontwerpen om bestanden in XML-indeling met optionele kenmerken te importeren.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727070"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="c745c-103">RCS‑bestanden in XML-indeling importeren met optionele kenmerken</span><span class="sxs-lookup"><span data-stu-id="c745c-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c745c-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER‑indelingsconfiguratie kan ontwerpen om bestanden in XML‑indeling met optionele kenmerken te importeren.</span><span class="sxs-lookup"><span data-stu-id="c745c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="c745c-105">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="c745c-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="c745c-106">Voordat u begint, moet u het bestand IncomingdocumentToLearnHowToHandleOptionalAttributes.xml downloaden uit het [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) en lokaal opslaan.</span><span class="sxs-lookup"><span data-stu-id="c745c-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="c745c-107">Ga naar **Alle werkgebieden** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="c745c-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="c745c-108">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="c745c-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="c745c-109">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c745c-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="c745c-110">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="c745c-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c745c-111">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="c745c-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="c745c-112">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="c745c-113">Typ in het veld **Naam** 'Model voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="c745c-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="c745c-114">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="c745c-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="c745c-115">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="c745c-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="c745c-116">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="c745c-117">Typ het veld **Naam** 'Basis'.</span><span class="sxs-lookup"><span data-stu-id="c745c-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="c745c-118">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c745c-118">Click **Add**.</span></span>
8.  <span data-ttu-id="c745c-119">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="c745c-120">Typ het veld **Naam** 'Lijst'.</span><span class="sxs-lookup"><span data-stu-id="c745c-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="c745c-121">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="c745c-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="c745c-122">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c745c-122">Click **Add**.</span></span>
12. <span data-ttu-id="c745c-123">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="c745c-124">Typ in het veld **Naam** 'Code'.</span><span class="sxs-lookup"><span data-stu-id="c745c-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="c745c-125">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="c745c-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="c745c-126">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c745c-126">Click **Add**.</span></span>
16. <span data-ttu-id="c745c-127">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c745c-127">Click **Save**.</span></span>
17. <span data-ttu-id="c745c-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c745c-128">Close the page.</span></span>
18. <span data-ttu-id="c745c-129">Klik op **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="c745c-129">Click **Change status**.</span></span>
19. <span data-ttu-id="c745c-130">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="c745c-130">Click **Complete**.</span></span>
20. <span data-ttu-id="c745c-131">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c745c-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="c745c-132">Een indeling maken voor het importeren van gegevens</span><span class="sxs-lookup"><span data-stu-id="c745c-132">Create a format for data import</span></span>
1.  <span data-ttu-id="c745c-133">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="c745c-134">Voer in het veld **Nieuw** in 'Indeling gebaseerd op gegevensmodel Model voor importeren van xml‑bestand'.</span><span class="sxs-lookup"><span data-stu-id="c745c-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="c745c-135">Typ in het veld **Naam** 'Indeling voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="c745c-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="c745c-136">Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.</span><span class="sxs-lookup"><span data-stu-id="c745c-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="c745c-137">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="c745c-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="c745c-138">Een indeling ontwerpen om het binnenkomende bestand in XML-indeling te parseren</span><span class="sxs-lookup"><span data-stu-id="c745c-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="c745c-139">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="c745c-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="c745c-140">Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="c745c-141">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c745c-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="c745c-142">Typ het veld **Naam** 'basis'.</span><span class="sxs-lookup"><span data-stu-id="c745c-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="c745c-143">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c745c-143">Click **OK**.</span></span>
6.  <span data-ttu-id="c745c-144">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="c745c-145">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c745c-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="c745c-146">Typ in het veld **Naam** 'document'.</span><span class="sxs-lookup"><span data-stu-id="c745c-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="c745c-147">Selecteer in het veld **Multiplicity** **Eén veel**.</span><span class="sxs-lookup"><span data-stu-id="c745c-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="c745c-148">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c745c-148">Click **OK**.</span></span>
11. <span data-ttu-id="c745c-149">Selecteer in de structuur **basis\document**.</span><span class="sxs-lookup"><span data-stu-id="c745c-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="c745c-150">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c745c-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="c745c-151">Selecteer **XML\Attribute** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c745c-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="c745c-152">Typ in het veld **Naam** 'ID'.</span><span class="sxs-lookup"><span data-stu-id="c745c-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="c745c-153">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c745c-153">Click **OK**.</span></span>
16. <span data-ttu-id="c745c-154">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c745c-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="c745c-155">Een indelingstoewijzing ontwerpen om geparseerde informatie op te slaan in het gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="c745c-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="c745c-156">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="c745c-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="c745c-157">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c745c-157">Click **New**.</span></span>
3. <span data-ttu-id="c745c-158">Typ of selecteer een waarde in het veld **Definitie**.</span><span class="sxs-lookup"><span data-stu-id="c745c-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="c745c-159">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c745c-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c745c-160">Typ in het veld **Naam** 'Toewijzing'.</span><span class="sxs-lookup"><span data-stu-id="c745c-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="c745c-161">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c745c-161">Click **Save**.</span></span>
7. <span data-ttu-id="c745c-162">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="c745c-162">Click **Designer**.</span></span>
8. <span data-ttu-id="c745c-163">Vouw in de structuur **indeling** uit.</span><span class="sxs-lookup"><span data-stu-id="c745c-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="c745c-164">Vouw in de structuur **indeling\root: XML-element(root)** uit.</span><span class="sxs-lookup"><span data-stu-id="c745c-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="c745c-165">Selecteer in de structuur \**format\root: XML‑element(root)\document: XML‑element 1..*</span><span class="sxs-lookup"><span data-stu-id="c745c-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c745c-166">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="c745c-166">(document)\*\*.</span></span>
11. <span data-ttu-id="c745c-167">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="c745c-167">Click **Bind**.</span></span>
12. <span data-ttu-id="c745c-168">Vouw in de structuur \**format\root: XML‑element(root)\document: XML‑element 1..* uit.</span><span class="sxs-lookup"><span data-stu-id="c745c-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c745c-169">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="c745c-169">(document)\*\*.</span></span>
13. <span data-ttu-id="c745c-170">Selecteer in de structuur \**format\root: XML‑element(root)\document: XML‑element 1..*</span><span class="sxs-lookup"><span data-stu-id="c745c-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c745c-171">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="c745c-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="c745c-172">Vouw in de structuur **Lijst = format.root.document** uit.</span><span class="sxs-lookup"><span data-stu-id="c745c-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="c745c-173">Selecteer in de structuur **Lijst = format.root.document\Code** uit.</span><span class="sxs-lookup"><span data-stu-id="c745c-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="c745c-174">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="c745c-174">Click **Bind**.</span></span>
17. <span data-ttu-id="c745c-175">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c745c-175">Click **Save**.</span></span>
18. <span data-ttu-id="c745c-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c745c-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="c745c-177">Indelingstoewijzing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="c745c-177">Run format mapping</span></span>
1. <span data-ttu-id="c745c-178">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="c745c-178">Click **Run**.</span></span>
2. <span data-ttu-id="c745c-179">Klik op **Bladeren** en Selecteer **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="c745c-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="c745c-180">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c745c-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="c745c-181">Het geselecteerde bestand is niet geïmporteerd omdat het indelingsontwerp ervan uitgaat dat er een 'id'‑kenmerk bestaat voor het element 'document ', maar het geïmporteerde bestand bevat geen kenmerk.</span><span class="sxs-lookup"><span data-stu-id="c745c-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="c745c-182">Indelingsstructuur wijzigen om het XML-kenmerk als optioneel te verwerken</span><span class="sxs-lookup"><span data-stu-id="c745c-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="c745c-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c745c-183">Close the page.</span></span>
2. <span data-ttu-id="c745c-184">Vouw in de structuur **basis\document** uit.</span><span class="sxs-lookup"><span data-stu-id="c745c-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="c745c-185">Selecteer in de structuur **basis\document\id**.</span><span class="sxs-lookup"><span data-stu-id="c745c-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="c745c-186">Selecteer **Ja** in veld **Lege tekenreeks voor ontbrekende kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="c745c-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="c745c-187">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c745c-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="c745c-188">Indelingstoewijzing uitvoeren voor het testen van de wijzigingen</span><span class="sxs-lookup"><span data-stu-id="c745c-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="c745c-189">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="c745c-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="c745c-190">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="c745c-190">Click **Run**.</span></span>
3. <span data-ttu-id="c745c-191">Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="c745c-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="c745c-192">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c745c-192">Click **OK**.</span></span>
5. <span data-ttu-id="c745c-193">Bekijk het gegenereerde bestand.</span><span class="sxs-lookup"><span data-stu-id="c745c-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="c745c-194">Hetzelfde bestand is geïmporteerd als het opmaakontwerp, beschouw nu het kenmerk ' id ' voor het element 'document ' als optioneel.</span><span class="sxs-lookup"><span data-stu-id="c745c-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
