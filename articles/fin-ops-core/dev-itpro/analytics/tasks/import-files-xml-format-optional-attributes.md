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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182181"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="e966f-103">RCS‑bestanden in XML-indeling importeren met optionele kenmerken</span><span class="sxs-lookup"><span data-stu-id="e966f-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e966f-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER‑indelingsconfiguratie kan ontwerpen om bestanden in XML‑indeling met optionele kenmerken te importeren.</span><span class="sxs-lookup"><span data-stu-id="e966f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="e966f-105">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="e966f-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="e966f-106">Voordat u begint, moet u het bestand IncomingdocumentToLearnHowToHandleOptionalAttributes.xml downloaden uit het [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) en lokaal opslaan.</span><span class="sxs-lookup"><span data-stu-id="e966f-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="e966f-107">Ga naar **Alle werkgebieden** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="e966f-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="e966f-108">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="e966f-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e966f-109">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e966f-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="e966f-110">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="e966f-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="e966f-111">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="e966f-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="e966f-112">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="e966f-113">Typ in het veld **Naam** 'Model voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="e966f-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="e966f-114">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="e966f-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="e966f-115">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="e966f-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="e966f-116">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="e966f-117">Typ het veld **Naam** 'Basis'.</span><span class="sxs-lookup"><span data-stu-id="e966f-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="e966f-118">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e966f-118">Click **Add**.</span></span>
8.  <span data-ttu-id="e966f-119">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="e966f-120">Typ het veld **Naam** 'Lijst'.</span><span class="sxs-lookup"><span data-stu-id="e966f-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="e966f-121">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="e966f-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="e966f-122">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e966f-122">Click **Add**.</span></span>
12. <span data-ttu-id="e966f-123">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="e966f-124">Typ in het veld **Naam** 'Code'.</span><span class="sxs-lookup"><span data-stu-id="e966f-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="e966f-125">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="e966f-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="e966f-126">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e966f-126">Click **Add**.</span></span>
16. <span data-ttu-id="e966f-127">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e966f-127">Click **Save**.</span></span>
17. <span data-ttu-id="e966f-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e966f-128">Close the page.</span></span>
18. <span data-ttu-id="e966f-129">Klik op **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e966f-129">Click **Change status**.</span></span>
19. <span data-ttu-id="e966f-130">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="e966f-130">Click **Complete**.</span></span>
20. <span data-ttu-id="e966f-131">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e966f-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="e966f-132">Een indeling maken voor het importeren van gegevens</span><span class="sxs-lookup"><span data-stu-id="e966f-132">Create a format for data import</span></span>
1.  <span data-ttu-id="e966f-133">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="e966f-134">Voer in het veld **Nieuw** in 'Indeling gebaseerd op gegevensmodel Model voor importeren van xml‑bestand'.</span><span class="sxs-lookup"><span data-stu-id="e966f-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="e966f-135">Typ in het veld **Naam** 'Indeling voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="e966f-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="e966f-136">Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.</span><span class="sxs-lookup"><span data-stu-id="e966f-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="e966f-137">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="e966f-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="e966f-138">Een indeling ontwerpen om het binnenkomende bestand in XML-indeling te parseren</span><span class="sxs-lookup"><span data-stu-id="e966f-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="e966f-139">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="e966f-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="e966f-140">Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="e966f-141">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e966f-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="e966f-142">Typ het veld **Naam** 'basis'.</span><span class="sxs-lookup"><span data-stu-id="e966f-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="e966f-143">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e966f-143">Click **OK**.</span></span>
6.  <span data-ttu-id="e966f-144">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="e966f-145">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e966f-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="e966f-146">Typ in het veld **Naam** 'document'.</span><span class="sxs-lookup"><span data-stu-id="e966f-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="e966f-147">Selecteer in het veld **Multiplicity** **Eén veel**.</span><span class="sxs-lookup"><span data-stu-id="e966f-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="e966f-148">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e966f-148">Click **OK**.</span></span>
11. <span data-ttu-id="e966f-149">Selecteer in de structuur **basis\document**.</span><span class="sxs-lookup"><span data-stu-id="e966f-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="e966f-150">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="e966f-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="e966f-151">Selecteer **XML\Attribute** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e966f-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="e966f-152">Typ in het veld **Naam** 'ID'.</span><span class="sxs-lookup"><span data-stu-id="e966f-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="e966f-153">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e966f-153">Click **OK**.</span></span>
16. <span data-ttu-id="e966f-154">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e966f-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="e966f-155">Een indelingstoewijzing ontwerpen om geparseerde informatie op te slaan in het gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="e966f-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="e966f-156">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="e966f-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="e966f-157">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e966f-157">Click **New**.</span></span>
3. <span data-ttu-id="e966f-158">Typ of selecteer een waarde in het veld **Definitie**.</span><span class="sxs-lookup"><span data-stu-id="e966f-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="e966f-159">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e966f-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e966f-160">Typ in het veld **Naam** 'Toewijzing'.</span><span class="sxs-lookup"><span data-stu-id="e966f-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="e966f-161">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e966f-161">Click **Save**.</span></span>
7. <span data-ttu-id="e966f-162">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="e966f-162">Click **Designer**.</span></span>
8. <span data-ttu-id="e966f-163">Vouw in de structuur **indeling** uit.</span><span class="sxs-lookup"><span data-stu-id="e966f-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="e966f-164">Vouw in de structuur **format\root: XML Element(root)** uit.</span><span class="sxs-lookup"><span data-stu-id="e966f-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="e966f-165">Selecteer in de structuur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="e966f-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="e966f-166">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="e966f-166">(document)\*\*.</span></span>
11. <span data-ttu-id="e966f-167">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="e966f-167">Click **Bind**.</span></span>
12. <span data-ttu-id="e966f-168">Vouw in de structuur \**format\root: XML Element(root)\document: XML Element 1..* uit</span><span class="sxs-lookup"><span data-stu-id="e966f-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="e966f-169">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="e966f-169">(document)\*\*.</span></span>
13. <span data-ttu-id="e966f-170">Selecteer in de structuur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="e966f-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="e966f-171">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="e966f-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="e966f-172">Vouw in de structuur **Lijst = format.root.document** uit.</span><span class="sxs-lookup"><span data-stu-id="e966f-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="e966f-173">Selecteer in de structuur **Lijst = format.root.document\Code** uit.</span><span class="sxs-lookup"><span data-stu-id="e966f-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="e966f-174">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="e966f-174">Click **Bind**.</span></span>
17. <span data-ttu-id="e966f-175">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e966f-175">Click **Save**.</span></span>
18. <span data-ttu-id="e966f-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e966f-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="e966f-177">Indelingstoewijzing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="e966f-177">Run format mapping</span></span>
1. <span data-ttu-id="e966f-178">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="e966f-178">Click **Run**.</span></span>
2. <span data-ttu-id="e966f-179">Klik op **Bladeren** en Selecteer **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="e966f-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="e966f-180">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e966f-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="e966f-181">Het geselecteerde bestand is niet geïmporteerd omdat het indelingsontwerp ervan uitgaat dat er een 'id'‑kenmerk bestaat voor het element 'document ', maar het geïmporteerde bestand bevat geen kenmerk.</span><span class="sxs-lookup"><span data-stu-id="e966f-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="e966f-182">Indelingsstructuur wijzigen om het XML-kenmerk als optioneel te verwerken</span><span class="sxs-lookup"><span data-stu-id="e966f-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="e966f-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e966f-183">Close the page.</span></span>
2. <span data-ttu-id="e966f-184">Vouw in de structuur **basis\document** uit.</span><span class="sxs-lookup"><span data-stu-id="e966f-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="e966f-185">Selecteer in de structuur **basis\document\id**.</span><span class="sxs-lookup"><span data-stu-id="e966f-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="e966f-186">Selecteer **Ja** in veld **Lege tekenreeks voor ontbrekende kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="e966f-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="e966f-187">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e966f-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="e966f-188">Indelingstoewijzing uitvoeren voor het testen van de wijzigingen</span><span class="sxs-lookup"><span data-stu-id="e966f-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="e966f-189">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="e966f-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="e966f-190">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="e966f-190">Click **Run**.</span></span>
3. <span data-ttu-id="e966f-191">Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="e966f-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="e966f-192">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e966f-192">Click **OK**.</span></span>
5. <span data-ttu-id="e966f-193">Bekijk het gegenereerde bestand.</span><span class="sxs-lookup"><span data-stu-id="e966f-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="e966f-194">Hetzelfde bestand is geïmporteerd als het opmaakontwerp, beschouw nu het kenmerk ' id ' voor het element 'document ' als optioneel.</span><span class="sxs-lookup"><span data-stu-id="e966f-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
