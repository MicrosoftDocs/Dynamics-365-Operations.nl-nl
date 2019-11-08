---
title: De toepassingsmetagegevens gebruiken met de ER‑configuratie
description: In de stappen in dit onderwerp wordt uitgelegd hoe een gebruiker van de Regulatory Configuration Service (RCS) een nieuwe Elektronisch Rapportage modeltoewijzing kan ontwerpen met behulp van de metagegevens in Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
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
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bfe007995c894d6cc86d07ef2b52da65e32e950
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182733"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="41941-103">De toepassingsmetagegevens gebruiken met de ER‑configuratie</span><span class="sxs-lookup"><span data-stu-id="41941-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41941-104">In de volgende stappen wordt uitgelegd hoe een gebruiker van Regulatory Configuration Service (RCS) in de rol van systeembeheerder of ER-ontwikkelaar een nieuwe ER-modeltoewijzing kan maken met gebruik van de metagegevens van de toepassing.</span><span class="sxs-lookup"><span data-stu-id="41941-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="41941-105">De metagegevens van de toepassing worden benaderd via een ER-metagegevensconfiguratie die een voorbeeldset bevat van metagegevens voor de toegang tot buitenlandse handelstransacties.</span><span class="sxs-lookup"><span data-stu-id="41941-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="41941-106">Als u deze stappen wilt uitvoeren, moet u eerst in RCS de stappen voltooien in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md)‑procedure.</span><span class="sxs-lookup"><span data-stu-id="41941-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="41941-107">Voer vervolgens de stappen uit in het onderwerp, [(ER) Toepassingsmetagegevens voorbereiden voor gebruik in RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="41941-107">Then complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="41941-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="41941-108">Prerequisites</span></span>
1. <span data-ttu-id="41941-109">Ga naar **Alle werkgebieden** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="41941-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="41941-110">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="41941-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="41941-111">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="41941-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="41941-112">Importeren metagegevensconfiguratie</span><span class="sxs-lookup"><span data-stu-id="41941-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="41941-113">Klik op **Metagegevensconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="41941-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="41941-114">De ER metagegevensconfiguratie importeren die metadata bevat uit de toepassing die is geconfigureerd voor het genereren van elektronische documenten voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="41941-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="41941-115">Deze ER metagegevensconfiguratie is geëxporteerd als XML-bestand terwijl de stappen in de [(ER) Toepassingsmetagegevens voorbereiden voor gebruik in RCS](prepare-application-metadata-rcs.md)‑procedure zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="41941-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="41941-116">Klik op **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="41941-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="41941-117">Klik op **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="41941-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="41941-118">Klik op **Bladeren** en selecteer het bestand 'Buitenlandse handel metagegevens.xml'.</span><span class="sxs-lookup"><span data-stu-id="41941-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="41941-119">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="41941-119">Click **OK**.</span></span> 
7. <span data-ttu-id="41941-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="41941-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="41941-121">Een gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="41941-121">Create data model configuration</span></span>
1. <span data-ttu-id="41941-122">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="41941-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="41941-123">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="41941-124">Type 'Model buitenlandse handel' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="41941-125">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="41941-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="41941-126">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="41941-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="41941-127">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="41941-128">Typ het veld **Naam** 'Basis'.</span><span class="sxs-lookup"><span data-stu-id="41941-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="41941-129">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="41941-129">Click **Add**.</span></span> 
9. <span data-ttu-id="41941-130">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="41941-131">Typ 'Transactie' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="41941-132">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="41941-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="41941-133">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="41941-133">Click **Add**.</span></span> 
13. <span data-ttu-id="41941-134">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="41941-135">Typ 'Code basisproduct' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="41941-136">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="41941-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="41941-137">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="41941-137">Click **Add**.</span></span> 
17. <span data-ttu-id="41941-138">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="41941-139">Typ 'Gefactureerd bedrag' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="41941-140">Selecteer in het veld **Itemtype** **Werkelijk**.</span><span class="sxs-lookup"><span data-stu-id="41941-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="41941-141">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="41941-141">Click **Add**.</span></span> 
21. <span data-ttu-id="41941-142">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="41941-143">Typ 'Datum' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="41941-144">Selecteer in het veld **Itemtype** **Datum**.</span><span class="sxs-lookup"><span data-stu-id="41941-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="41941-145">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="41941-145">Click **Add**.</span></span> 
25. <span data-ttu-id="41941-146">Klik op **Basisverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="41941-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="41941-147">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="41941-147">Click **OK**.</span></span> 
27. <span data-ttu-id="41941-148">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="41941-148">Click **Save**.</span></span> 
28. <span data-ttu-id="41941-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="41941-149">Close the page.</span></span> 
29. <span data-ttu-id="41941-150">Klik op **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="41941-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="41941-151">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="41941-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="41941-152">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="41941-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="41941-153">Configuratie modeltoewijzing maken</span><span class="sxs-lookup"><span data-stu-id="41941-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="41941-154">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="41941-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="41941-155">Voer in het veld **Nieuw** 'Modeltoewijzing gebaseerd op gegevensmodel Buitenlandse handelsmodel' in.</span><span class="sxs-lookup"><span data-stu-id="41941-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="41941-156">Type 'Buitenlandse handel toewijzing' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="41941-157">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="41941-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="41941-158">Vouw de sectie **Vereisten** uit.</span><span class="sxs-lookup"><span data-stu-id="41941-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="41941-159">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="41941-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="41941-160">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="41941-160">Click **New**.</span></span> 
8. <span data-ttu-id="41941-161">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="41941-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="41941-162">Selecteer in het veld **Vereist onderdeeltype** **Configuratie**.</span><span class="sxs-lookup"><span data-stu-id="41941-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="41941-163">Selecteer configuratie **Metagegevens buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="41941-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="41941-164">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="41941-164">Click **Save**.</span></span> 
12. <span data-ttu-id="41941-165">De verwijzing naar versie 1 van de configuratie van de 'Metagegevens buitenlandse handel' is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="41941-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="41941-166">De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.</span><span class="sxs-lookup"><span data-stu-id="41941-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="41941-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="41941-167">Close the page.</span></span> 
14. <span data-ttu-id="41941-168">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="41941-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="41941-169">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="41941-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="41941-170">Selecteer in de structuur **Dynamics 365 for Operations'\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="41941-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="41941-171">Klik op **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="41941-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="41941-172">Typ 'intrastat' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="41941-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="41941-173">Selecteer **Intrastat** tabelrecords.</span><span class="sxs-lookup"><span data-stu-id="41941-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="41941-174">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="41941-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="41941-175">De enige twee tabellen zijn aangeboden, omdat de enige twee tabellen zijn toegevoegd aan de set metagegevens die momenteel in gebruik zijn.</span><span class="sxs-lookup"><span data-stu-id="41941-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="41941-176">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="41941-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="41941-177">Vouw in de structuur **Intrastat** uit.</span><span class="sxs-lookup"><span data-stu-id="41941-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="41941-178">Selecteer **Intrastat\BedragMST** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="41941-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="41941-179">Vouw in de structuur **Transactie = Intrastat** uit.</span><span class="sxs-lookup"><span data-stu-id="41941-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="41941-180">Selecteer in de structuur **Transacties = Intrastat\Gefactureerd bedrag**.</span><span class="sxs-lookup"><span data-stu-id="41941-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="41941-181">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="41941-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="41941-182">Selecteer **Intrastat\TransDatum** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="41941-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="41941-183">Selecteer **Transactie = Intrastat\Datum** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="41941-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="41941-184">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="41941-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="41941-185">Vouw in de structuur **Intrastat\>Relaties** uit.</span><span class="sxs-lookup"><span data-stu-id="41941-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="41941-186">Vouw in de structuur **Intrastat\>Relaties\IntrastatBasisproduct** uit.</span><span class="sxs-lookup"><span data-stu-id="41941-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="41941-187">Selecteer in de structuur **Intrastat\>Relaties\IntrastatBasisproduct\Code**.</span><span class="sxs-lookup"><span data-stu-id="41941-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="41941-188">Selecteer in de structuur **Transacties = Intrastat\Basisproductcode**.</span><span class="sxs-lookup"><span data-stu-id="41941-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="41941-189">Klik op **Binden**.</span><span class="sxs-lookup"><span data-stu-id="41941-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="41941-190">Klik op **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="41941-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="41941-191">We hebben elementen van het gegevensmodel gebonden met items van gegevensbronnen die worden beschreven met behulp van toepassingsmetagegevens van de ER metagegevensconfiguratie waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="41941-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="41941-192">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="41941-192">Click **Save**.</span></span> 
37. <span data-ttu-id="41941-193">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="41941-193">Close the page.</span></span> 
38. <span data-ttu-id="41941-194">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="41941-194">Close the page.</span></span> 
39. <span data-ttu-id="41941-195">Indien nodig kunt u de bestaande set metagegevens uitbreiden en vervolgens de nieuwe, voltooide versie van de ER-metagegevensconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="41941-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="41941-196">U kunt deze vervolgens importeren in RCS en de vereisten van de geconfigureerde configuratie van de modeltoewijzing bijwerken naar een nieuwe versie van de geïmporteerde metagegevensconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="41941-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="41941-197">Deze manier om informatie op te halen over de metagegevens van de toepassing is de enige die beschikbaar is voor lokaal geïmplementeerde toepassingen (wanneer een LBD (Local Business Data) of on-premises implementatiemodel wordt gebruikt).</span><span class="sxs-lookup"><span data-stu-id="41941-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        