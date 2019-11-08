---
title: Bestanden in XML-indeling importeren met optionele kenmerken
description: Dit onderwerp bevat informatie over het ontwerpen van ER‑indelingen waarmee XML-kenmerken worden opgegeven voor het parseren van inkomende elektronische documenten in XML-indeling.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182825"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="5a44c-103">Bestanden in XML-indeling importeren met optionele kenmerken</span><span class="sxs-lookup"><span data-stu-id="5a44c-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="5a44c-104">U kunt ER-indelingen (elektronische rapportage) ontwerpen om inkomende elektronische documenten te parseren in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="5a44c-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="5a44c-105">U kunt bepaalde kenmerken van XML-elementen als optioneel specificeren in de ontworpen ER‑indeling.</span><span class="sxs-lookup"><span data-stu-id="5a44c-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="5a44c-106">Hiermee kunt u binnenkomende bestanden met en zonder dergelijke XML-kenmerken op de juiste manier verwerken.</span><span class="sxs-lookup"><span data-stu-id="5a44c-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="5a44c-107">Vervolgens kunt u de inhoud van deze bestanden gebruiken om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="5a44c-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="5a44c-108">Als u meer wilt weten over deze functie, voltooit u de stappen in het onderwerp [RCS Bestanden in XML-indeling met optionele kenmerken importeren](tasks/import-files-xml-format-optional-attributes.md), die deel uitmaken van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677).</span><span class="sxs-lookup"><span data-stu-id="5a44c-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="5a44c-109">U kunt deze taakbegeleiding en het bijbehorend voorbeeld downloaden uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="5a44c-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="5a44c-110">Omschrijving inhoud</span><span class="sxs-lookup"><span data-stu-id="5a44c-110">Content description</span></span>       | <span data-ttu-id="5a44c-111">Bestand</span><span class="sxs-lookup"><span data-stu-id="5a44c-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a44c-112">Voorbeeldbestand in XML‑indeling</span><span class="sxs-lookup"><span data-stu-id="5a44c-112">Sample file in XML format</span></span> | <span data-ttu-id="5a44c-113">IncomingdocumentToLearnHowToHandleOptionalAttributes.xml.</span><span class="sxs-lookup"><span data-stu-id="5a44c-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="5a44c-114">Taakbegeleiding</span><span class="sxs-lookup"><span data-stu-id="5a44c-114">Task guide</span></span>                | <span data-ttu-id="5a44c-115">RCS Bestanden in XML-indeling met optionele kenmerken importeren.axtr</span><span class="sxs-lookup"><span data-stu-id="5a44c-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="5a44c-116">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER‑indelingsconfiguratie kan ontwerpen om bestanden in XML‑indeling met optionele kenmerken te importeren.</span><span class="sxs-lookup"><span data-stu-id="5a44c-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="5a44c-117">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) voltooien.</span><span class="sxs-lookup"><span data-stu-id="5a44c-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="5a44c-118">Voordat u begint, moet u het bestand IncomingdocumentToLearnHowToHandleOptionalAttributes.xml downloaden uit het Microsoft Downloadcenter en lokaal opslaan (https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="5a44c-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="5a44c-119">Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="5a44c-120">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="5a44c-121">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in het onderwerp [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5a44c-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="5a44c-122">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="5a44c-123">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="5a44c-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="5a44c-124">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="5a44c-125">Typ in het veld **Naam** 'Model voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="5a44c-126">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="5a44c-127">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-127">Click **Designer**.</span></span>
5. <span data-ttu-id="5a44c-128">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="5a44c-129">Typ het veld **Naam** 'Basis'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="5a44c-130">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-130">Click **Add**.</span></span>
8. <span data-ttu-id="5a44c-131">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="5a44c-132">Typ het veld **Naam** 'Lijst'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="5a44c-133">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="5a44c-134">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-134">Click **Add**.</span></span>
12. <span data-ttu-id="5a44c-135">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="5a44c-136">Typ in het veld **Naam** 'Code'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="5a44c-137">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="5a44c-138">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-138">Click **Add**.</span></span>
16. <span data-ttu-id="5a44c-139">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-139">Click **Save**.</span></span>
17. <span data-ttu-id="5a44c-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5a44c-140">Close the page.</span></span>
18. <span data-ttu-id="5a44c-141">Klik op **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-141">Click **Change status**.</span></span>
19. <span data-ttu-id="5a44c-142">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-142">Click **Complete**.</span></span>
20. <span data-ttu-id="5a44c-143">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="5a44c-144">Een indeling maken voor het importeren van gegevens</span><span class="sxs-lookup"><span data-stu-id="5a44c-144">Create a format for data import</span></span>
1. <span data-ttu-id="5a44c-145">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="5a44c-146">Voer in het veld **Nieuw** in 'Indeling gebaseerd op gegevensmodel Model voor importeren van xml‑bestand'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="5a44c-147">Typ in het veld **Naam** 'Indeling voor importeren van XML-bestand'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="5a44c-148">Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="5a44c-149">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="5a44c-150">Een indeling ontwerpen om het binnenkomende bestand in XML-indeling te parseren</span><span class="sxs-lookup"><span data-stu-id="5a44c-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="5a44c-151">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-151">Click **Designer**.</span></span>
2. <span data-ttu-id="5a44c-152">Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="5a44c-153">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5a44c-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="5a44c-154">Typ het veld **Naam** 'basis'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="5a44c-155">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-155">Click **OK**.</span></span>
6. <span data-ttu-id="5a44c-156">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="5a44c-157">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5a44c-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="5a44c-158">Typ in het veld **Naam** 'document'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="5a44c-159">Selecteer in het veld **Multiplicity** **Eén veel**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="5a44c-160">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-160">Click **OK**.</span></span>
11. <span data-ttu-id="5a44c-161">Selecteer in de structuur **basis\document**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="5a44c-162">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="5a44c-163">Selecteer **XML\Attribute** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5a44c-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="5a44c-164">Typ in het veld **Naam** 'id'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="5a44c-165">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-165">Click **OK**.</span></span>
16. <span data-ttu-id="5a44c-166">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="5a44c-167">Een indelingstoewijzing ontwerpen om geparseerde informatie op te slaan in het gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="5a44c-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="5a44c-168">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="5a44c-169">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-169">Click **New**.</span></span>
3.  <span data-ttu-id="5a44c-170">Typ of selecteer een waarde in het veld **Definitie**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="5a44c-171">Typ in het veld **Naam** 'Toewijzing'.</span><span class="sxs-lookup"><span data-stu-id="5a44c-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="5a44c-172">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-172">Click **Save**.</span></span>
6.  <span data-ttu-id="5a44c-173">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="5a44c-174">Vouw in de structuur **indeling** uit.</span><span class="sxs-lookup"><span data-stu-id="5a44c-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="5a44c-175">Vouw in de structuur **format\root: XML Element(root)** uit.</span><span class="sxs-lookup"><span data-stu-id="5a44c-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="5a44c-176">Selecteer in de structuur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5a44c-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5a44c-177">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5a44c-177">(document)\*\*.</span></span>
10. <span data-ttu-id="5a44c-178">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-178">Click **Bind**.</span></span>
11. <span data-ttu-id="5a44c-179">Vouw in de structuur \**format\root: XML Element(root)\document: XML Element 1..* uit</span><span class="sxs-lookup"><span data-stu-id="5a44c-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5a44c-180">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5a44c-180">(document)\*\*.</span></span>
12. <span data-ttu-id="5a44c-181">Selecteer in de structuur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5a44c-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5a44c-182">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="5a44c-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="5a44c-183">Vouw in de structuur **Lijst = format.root.document** uit.</span><span class="sxs-lookup"><span data-stu-id="5a44c-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="5a44c-184">Selecteer in de structuur **Lijst = format.root.document\Code** uit.</span><span class="sxs-lookup"><span data-stu-id="5a44c-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="5a44c-185">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-185">Click **Bind**.</span></span>
16. <span data-ttu-id="5a44c-186">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-186">Click **Save**.</span></span>
17. <span data-ttu-id="5a44c-187">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5a44c-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="5a44c-188">Indelingstoewijzing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="5a44c-188">Run format mapping</span></span>
1. <span data-ttu-id="5a44c-189">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-189">Click **Run**.</span></span>
2. <span data-ttu-id="5a44c-190">Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="5a44c-191">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5a44c-192">Het geselecteerde bestand is niet geïmporteerd omdat het indelingsontwerp ervan uitgaat dat er een 'id'‑kenmerk bestaat voor het element 'document ', maar het geïmporteerde bestand bevat geen kenmerk.</span><span class="sxs-lookup"><span data-stu-id="5a44c-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="5a44c-193">Indelingsstructuur wijzigen om het XML-kenmerk als optioneel te verwerken</span><span class="sxs-lookup"><span data-stu-id="5a44c-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="5a44c-194">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5a44c-194">Close the page.</span></span>
2. <span data-ttu-id="5a44c-195">Vouw in de structuur **basis\document** uit.</span><span class="sxs-lookup"><span data-stu-id="5a44c-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="5a44c-196">Selecteer in de structuur **basis\document\id**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="5a44c-197">Selecteer **Ja** in veld **Lege tekenreeks voor ontbrekend kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="5a44c-198">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="5a44c-199">Indelingstoewijzing uitvoeren voor het testen van de wijzigingen</span><span class="sxs-lookup"><span data-stu-id="5a44c-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="5a44c-200">Klik op **Indeling aan model toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="5a44c-201">Klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-201">Click **Run**.</span></span>
3. <span data-ttu-id="5a44c-202">Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="5a44c-203">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a44c-203">Click **OK**.</span></span>
5. <span data-ttu-id="5a44c-204">Bekijk het gegenereerde bestand.</span><span class="sxs-lookup"><span data-stu-id="5a44c-204">Review the generated file.</span></span> <span data-ttu-id="5a44c-205">Zie dat hetzelfde bestand is geïmporteerd omdat het indelingsontwerp nu het 'id'‑kenmerk voor het element 'document' beschouwt als optioneel.</span><span class="sxs-lookup"><span data-stu-id="5a44c-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>