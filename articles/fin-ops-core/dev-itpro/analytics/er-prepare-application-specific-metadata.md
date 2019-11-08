---
title: Toepassingsspecifieke metagegevens voorbereiden voor RCS en ER
description: In dit onderwerp wordt uitgelegd hoe u toepassingsspecifieke metagegevens voorbereidt voor Regulatory Configuration Service (RCS) en Elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 74750397dc344d74c018c27114357d3d05b95b7e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550102"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="6f285-103">Toepassingsspecifieke metagegevens voorbereiden voor RCS en ER</span><span class="sxs-lookup"><span data-stu-id="6f285-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6f285-104">In dit onderwerp vindt u een aantal voorbeelden van de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="6f285-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="6f285-105">Toepassingsmetagegevens die kunnen worden gebruikt in RCS voorbereiden</span><span class="sxs-lookup"><span data-stu-id="6f285-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="6f285-106">Toepassingsmetagegevens openen door gebruik van een ER-configuratie</span><span class="sxs-lookup"><span data-stu-id="6f285-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="6f285-107">Toepassingsmetagegevens openen door gebruik van verbonden toepassingen</span><span class="sxs-lookup"><span data-stu-id="6f285-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="6f285-108">Toepassingsmetagegevens die kunnen worden gebruikt in RCS voorbereiden</span><span class="sxs-lookup"><span data-stu-id="6f285-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="6f285-109">De volgende procedure laat zien hoe een gebruiker met de rol van **Systeembeheerder** of **Ontwikkelaar van elektronische rapportage** een ER-configuratie kan maken die metagegevens bevat voor de toepassing en die wordt gebruikt om ER‑modeltoewijzingsconfiguraties te ontwerpen in de Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="6f285-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="6f285-110">De configuratie van de voorbeeld ER modeltoewijzingsconfiguratie die in dit voorbeeld wordt gemaakt, wordt gebruikt om transacties van buitenlandse handel te openen.</span><span class="sxs-lookup"><span data-stu-id="6f285-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="6f285-111">Voor dit voorbeeld gaat u RCS gebruiken om een ER-oplossing te ontwerpen voor de toepassing die wordt gebruikt om elektronische documenten te genereren die informatie bevatten uit het bedrijfsdomein voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="6f285-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="6f285-112">Als u de toewijzing wilt opgeven tussen het ER-gegevensmodel en de bronnen van vereiste gegevens, moet u toegang hebben tot de toepassingsmetagegevens in RCS.</span><span class="sxs-lookup"><span data-stu-id="6f285-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="6f285-113">Als onderdeel van het ontwerpproces van de ER-oplossing moet u dus een nieuwe ER-metagegevensconfiguratie configureren die alle vereiste metagegevens bevat om ER‑rapporten voor het geselecteerde bedrijfsdomein te genereren.</span><span class="sxs-lookup"><span data-stu-id="6f285-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="6f285-114">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6f285-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="6f285-115">Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="6f285-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="6f285-116">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="6f285-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="6f285-117">Als u deze configuratieprovider niet ziet, voltooi dan de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6f285-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="6f285-118">Selecteer **Metagegevensconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="6f285-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="6f285-119">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="6f285-120">Voer in het vervolgkeuzemenu in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="6f285-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="6f285-121">Voer voor dit voorbeeld **Metagegevens buitenlandse handel** in.</span><span class="sxs-lookup"><span data-stu-id="6f285-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="6f285-122">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="6f285-123">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-123">Select **Designer**.</span></span>
8. <span data-ttu-id="6f285-124">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f285-125">U kunt alle metagegevens voor de gehele toepassing of voor geselecteerde modellen of modules selecteren.</span><span class="sxs-lookup"><span data-stu-id="6f285-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="6f285-126">Houd er in beide gevallen rekening mee dat de volgende metagegevens automatisch worden toegevoegd: tabellen met records, inventarisaties en uitgebreide gegevenstypen (EDT's).</span><span class="sxs-lookup"><span data-stu-id="6f285-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="6f285-127">Als er aanvullende typen metagegevens nodig zijn, moeten deze handmatig worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="6f285-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="6f285-128">U moet metagegevens toevoegen die zijn gerelateerd aan transacties voor buitenlandse handel en handmatig metagegevensitems selecteren.</span><span class="sxs-lookup"><span data-stu-id="6f285-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="6f285-129">Selecteer **Gegevensbron toevoegen \> Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="6f285-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="6f285-130">Filter op de waarde **Intrastat** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="6f285-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="6f285-131">Selecteer de **Intrastat** -tabelrecord.</span><span class="sxs-lookup"><span data-stu-id="6f285-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="6f285-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-132">Select **OK**.</span></span>

<span data-ttu-id="6f285-133">U moet metagegevens over de Intrastat-tabelrecords toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f285-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="6f285-134">Selecteer in de structuur **Tabelrecords Intrastat \> \>Relaties \> IntrastatCommodity (tabelrecords EcoResCategory**).</span><span class="sxs-lookup"><span data-stu-id="6f285-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="6f285-135">Selecteer **Metagegevens toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f285-136">Metagegevens over vereiste relaties voor de geselecteerde tabelrecords moeten hand matig worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="6f285-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="6f285-137">Selecteer **Gegevensbron toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="6f285-138">Selecteer **Opsomming**.</span><span class="sxs-lookup"><span data-stu-id="6f285-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="6f285-139">Filter op de waarde **IntrastatDirection** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="6f285-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="6f285-140">Selecteer het **IntrastatDirection** opsommingsrecord.</span><span class="sxs-lookup"><span data-stu-id="6f285-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="6f285-141">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-141">Select **OK**.</span></span>
20. <span data-ttu-id="6f285-142">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6f285-142">Select **Save**.</span></span>
21. <span data-ttu-id="6f285-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f285-143">Close the page.</span></span>
22. <span data-ttu-id="6f285-144">De conceptversie van de metagegevensconfiguratie voltooien:</span><span class="sxs-lookup"><span data-stu-id="6f285-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="6f285-145">Selecteer **Status wijzigen \> Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="6f285-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="6f285-146">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-146">Select **OK**.</span></span>
    3. <span data-ttu-id="6f285-147">Selecteer de voltooide versie 1.</span><span class="sxs-lookup"><span data-stu-id="6f285-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="6f285-148">De voltooide versie van de metagegevensconfiguratie van de toepassing exporteren als een XML-bestand:</span><span class="sxs-lookup"><span data-stu-id="6f285-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="6f285-149">Selecteer **Uitwisselen \> Bestand exporteren als XML**.</span><span class="sxs-lookup"><span data-stu-id="6f285-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="6f285-150">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-150">Select **OK**.</span></span>

<span data-ttu-id="6f285-151">De metagegevensconfiguratie die u hebt gemaakt, wordt opgeslagen als het bestand **Buitenlandse handel metagegevens.xml**.</span><span class="sxs-lookup"><span data-stu-id="6f285-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="6f285-152">U kunt dit nu importeren in RCS, zodat het kan worden gebruikt als de bron van metagegevens voor het bedrijfsdomein voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="6f285-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="6f285-153">Op basis van deze informatie kunt u de toewijzing opgeven tussen de toepassingsmetagegevens en het ER-gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="6f285-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="6f285-154">Toepassingsmetagegevens openen met gebruik van een ER-configuratie</span><span class="sxs-lookup"><span data-stu-id="6f285-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="6f285-155">De volgende procedure laat zien hoe een gebruiker met de rol **Systeembeheerder** of **Ontwikkelaar elektronische rapportage** een nieuwe ER-modeltoewijzing kan ontwerpen door metagegevens uit de toepassing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6f285-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="6f285-156">De metagegevens van de toepassing worden benaderd via een ER-metagegevensconfiguratie die een voorbeeldset bevat van metagegevens voor de toegang tot buitenlandse handelstransacties.</span><span class="sxs-lookup"><span data-stu-id="6f285-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="6f285-157">Voordat u deze procedure kunt uitvoeren, moet u eerst de volgende procedures voltooien:</span><span class="sxs-lookup"><span data-stu-id="6f285-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="6f285-158">Een configuratieprovider maken en deze als actief markeren</span><span class="sxs-lookup"><span data-stu-id="6f285-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="6f285-159">Toepassingsmetagegevens die kunnen worden gebruikt in RCS voorbereiden</span><span class="sxs-lookup"><span data-stu-id="6f285-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="6f285-160">Ga naar **Alle werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="6f285-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="6f285-161">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="6f285-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="6f285-162">Als u deze configuratieprovider niet ziet, voltooi dan de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6f285-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="6f285-163">Importeer de ER‑metagegevensconfiguratie die metagegevens voor de toepassing bevat en die is geconfigureerd voor het genereren van elektronische documenten voor het domein buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="6f285-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="6f285-164">U hebt deze metagegevensconfiguratie gemaakt en als XML-bestand geëxporteerd in de procedure [Voorbereiden van metagegevens die kunnen worden gebruikt in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="6f285-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="6f285-165">Selecteer **Metagegevensconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="6f285-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="6f285-166">Selecteer **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="6f285-167">Selecteer **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="6f285-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="6f285-168">Blader om het bestand **Buitenlandse handel metagegevens.xml** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="6f285-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="6f285-169">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-169">Select **OK**.</span></span>
    6. <span data-ttu-id="6f285-170">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f285-170">Close the page.</span></span>

4. <span data-ttu-id="6f285-171">Een gegevensmodelconfiguratie maken:</span><span class="sxs-lookup"><span data-stu-id="6f285-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="6f285-172">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="6f285-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="6f285-173">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="6f285-174">Voer in het vervolgkeuzemenu in het veld **Naam** **Model buitenlandse handel** in.</span><span class="sxs-lookup"><span data-stu-id="6f285-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="6f285-175">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="6f285-176">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="6f285-177">Selecteer **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f285-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="6f285-178">Typ het veld **Naam** **Basis**.</span><span class="sxs-lookup"><span data-stu-id="6f285-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="6f285-179">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="6f285-180">Selecteer **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f285-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="6f285-181">Typ in het veld **Naam** **Transactie**.</span><span class="sxs-lookup"><span data-stu-id="6f285-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="6f285-182">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="6f285-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="6f285-183">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="6f285-184">Selecteer **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f285-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="6f285-185">Typ in het veld **Naam** **Code basisproduct**.</span><span class="sxs-lookup"><span data-stu-id="6f285-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="6f285-186">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="6f285-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="6f285-187">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-187">Select **Add**.</span></span>

    9. <span data-ttu-id="6f285-188">Selecteer **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f285-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="6f285-189">Typ in **Gefactureerd bedrag** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f285-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="6f285-190">Selecteer in het veld **Itemtype** **Werkelijk**.</span><span class="sxs-lookup"><span data-stu-id="6f285-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="6f285-191">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-191">Select **Add**.</span></span>

    10. <span data-ttu-id="6f285-192">Selecteer **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f285-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="6f285-193">Typ in het veld **Naam** **Datum**.</span><span class="sxs-lookup"><span data-stu-id="6f285-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="6f285-194">Selecteer in het veld **Itemtype** **Datum**.</span><span class="sxs-lookup"><span data-stu-id="6f285-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="6f285-195">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="6f285-196">Selecteer **Toevoegen \> Basisverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="6f285-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="6f285-197">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-197">Select **OK**.</span></span>
    13. <span data-ttu-id="6f285-198">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6f285-198">Select **Save**.</span></span>
    14. <span data-ttu-id="6f285-199">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f285-199">Close the page.</span></span>
    15. <span data-ttu-id="6f285-200">Selecteer **Status wijzigen \> Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="6f285-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="6f285-201">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-201">Select **OK**.</span></span>

5. <span data-ttu-id="6f285-202">Een configuratie modeltoewijzing maken:</span><span class="sxs-lookup"><span data-stu-id="6f285-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="6f285-203">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="6f285-204">Voer in het uitklapdialoogvenster in het veld **Nieuw** in **Modeltoewijzing gebaseerd op gegevensmodel Buitenlandse handelsmodel**.</span><span class="sxs-lookup"><span data-stu-id="6f285-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="6f285-205">Voer in het veld **Naam** in **Toewijzing buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="6f285-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="6f285-206">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="6f285-207">Selecteer op het sneltabblad **Vereisten** **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="6f285-208">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6f285-208">Select **New**.</span></span>
    7. <span data-ttu-id="6f285-209">Selecteer in het veld **Vereist onderdeeltype** **Configuratie**.</span><span class="sxs-lookup"><span data-stu-id="6f285-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="6f285-210">Selecteer de configuratie **Metagegevens buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="6f285-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="6f285-211">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6f285-211">Select **Save**.</span></span> <span data-ttu-id="6f285-212">Zie dat de verwijzing is toegevoegd aan versie 1 van de configuratie **Metagegevens buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="6f285-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="6f285-213">De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer de modeltoewijzing wordt ontworpen.</span><span class="sxs-lookup"><span data-stu-id="6f285-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="6f285-214">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f285-214">Close the page.</span></span>
    11. <span data-ttu-id="6f285-215">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="6f285-216">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="6f285-217">Selecteer in de structuur **Dynamics 365 for Operations \> Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="6f285-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="6f285-218">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="6f285-219">Voer in het veld **Naam** **Intrastat** in.</span><span class="sxs-lookup"><span data-stu-id="6f285-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="6f285-220">Selecteer **Intrastat** tabelrecords.</span><span class="sxs-lookup"><span data-stu-id="6f285-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="6f285-221">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6f285-222">Er zijn slechts twee tabellen zijn aangeboden, omdat slechts twee tabellen zijn toegevoegd aan de set metagegevens die momenteel in gebruik is.</span><span class="sxs-lookup"><span data-stu-id="6f285-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="6f285-223">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="6f285-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="6f285-224">Selecteer **Intrastat \> BedragMST** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6f285-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="6f285-225">Selecteer in de structuur **Transactie = Intrastat \> Gefactureerd bedrag**.</span><span class="sxs-lookup"><span data-stu-id="6f285-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="6f285-226">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="6f285-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="6f285-227">Selecteer **Intrastat \> TransDatum** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6f285-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="6f285-228">Selecteer **Transactie = Intrastat \> Datum** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6f285-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="6f285-229">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="6f285-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="6f285-230">Selecteer in de structuur **Intrastat \> \>Relaties \> IntrastatBasisproduct \> Code**.</span><span class="sxs-lookup"><span data-stu-id="6f285-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="6f285-231">Selecteer in de structuur **Transactie = Intrastat \> Basisproductcode**.</span><span class="sxs-lookup"><span data-stu-id="6f285-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="6f285-232">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="6f285-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="6f285-233">Selecteer **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="6f285-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6f285-234">Nadat de validatie is voltooid hebt u elementen van het gegevensmodel gebonden aan items van de gegevensbronnen die worden beschreven met behulp van de toepassingsmetagegevens van de ER metagegevensconfiguratie waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="6f285-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="6f285-235">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6f285-235">Select **Save**.</span></span>

<span data-ttu-id="6f285-236">Als u wenst, kunt u de bestaande set metagegevens uitbreiden in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="6f285-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="6f285-237">Vervolgens kunt u de nieuwe, voltooide versie van de ER metagegevensconfiguratie exporteren, en deze importeren in RCS en de vereisten van de geconfigureerde configuratie modeltoewijzing bijwerken om naar een nieuwe versie van de geïmporteerde metagegevensconfiguratie te verwijzen.</span><span class="sxs-lookup"><span data-stu-id="6f285-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="6f285-238">Deze methode om informatie op te halen over de metagegevens van de toepassing is de enige methode voor lokaal geïmplementeerde toepassingen (als een \[LBD\] (Local Business Data) of on-premises implementatiemodel wordt gebruikt voor de toepassing).</span><span class="sxs-lookup"><span data-stu-id="6f285-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="6f285-239">Metagegevens van de toepassing openen door gebruik van verbonden toepassingen</span><span class="sxs-lookup"><span data-stu-id="6f285-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="6f285-240">De volgende procedure laat zien hoe een gebruiker met de rol **Systeembeheerder** of **Ontwikkelaar elektronische rapportage** een nieuwe ER-modeltoewijzing kan ontwerpen door metagegevens van de toepassing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6f285-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="6f285-241">Toepassingsmetagegevens worden online benaderd via een RCS verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="6f285-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="6f285-242">Er wordt een voorbeeld ER modeltoewijzing geconfigureerd voor het openen van transacties van buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="6f285-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="6f285-243">Als u de stappen in deze procedure wilt voltooien, moet u eerst de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) in RCS voltooien.</span><span class="sxs-lookup"><span data-stu-id="6f285-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="6f285-244">Als u de procedure [Open toepassingsmetagegevens met gebruik van een ER‑configuratie](#access-application-metadata-by-using-an-er-configuration) eerder in dit onderwerp niet hebt voltooid, gaat u naar de pagina [Taakbegeleiders voor elektronische rapportage voor Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) voor het vooraf downloaden van de volgende ER‑configuratiebestanden en deze lokaal opslaan: **Buitenlandse handel metagegevens.xml**, **Buitenlandse handel model.xml en** en **Buitenlandse handel toewijzing.xml**.</span><span class="sxs-lookup"><span data-stu-id="6f285-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="6f285-245">De vereiste ER-configuraties verkrijgen</span><span class="sxs-lookup"><span data-stu-id="6f285-245">Get required ER configurations</span></span>

<span data-ttu-id="6f285-246">Als u de stappen in de procedure [Gebruik de toepassingsmetagegevens met gebruik van een ER‑configuratie](#access-application-metadata-by-using-an-er-configuration) al eerder in dit onderwerp hebt voltooid, beschikt u al over alle vereiste ER‑configuraties (de configuraties buitenlandse handel metagegevens, model en toewijzing) in het huidige RCS‑exemplaar.</span><span class="sxs-lookup"><span data-stu-id="6f285-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="6f285-247">In dat geval kunt u deze procedure overslaan.</span><span class="sxs-lookup"><span data-stu-id="6f285-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="6f285-248">Ga naar **Alle werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="6f285-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="6f285-249">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="6f285-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="6f285-250">Laad de configuratiebestanden **Buitenlandse handel metagegevens.xml**, **Buitenlandse handel model.xml** en **Buitenlandse handel toewijzing.xml** door de volgende stappen voor elk van deze te herhalen:</span><span class="sxs-lookup"><span data-stu-id="6f285-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="6f285-251">Selecteer **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="6f285-252">Selecteer **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="6f285-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="6f285-253">Selecteer **Bladeren** en selecteer een bestand.</span><span class="sxs-lookup"><span data-stu-id="6f285-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="6f285-254">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f285-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="6f285-255">De verbinding bij de toepassing registreren</span><span class="sxs-lookup"><span data-stu-id="6f285-255">Register the connection with the application</span></span>

1. <span data-ttu-id="6f285-256">Ga naar **Alle werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="6f285-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="6f285-257">Selecteer **Verbonden toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="6f285-258">Controleer of de geconfigureerde toepassing is gebaseerd Microsoft Azure en toegankelijk is voor gebruikers van RCS.</span><span class="sxs-lookup"><span data-stu-id="6f285-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="6f285-259">De huidige RCS-gebruiker moet toegang hebben tot de geconfigureerde toepassing terwijl deze is geregistreerd als gebruiker van deze toepassing in een rol die hem of haar de bevoegdheid geeft om de metagegevens van de toepassing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6f285-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="6f285-260">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6f285-260">Select **New**.</span></span>
5. <span data-ttu-id="6f285-261">Voer in het veld **Naam** in **MyConnectedApp** in als de naam van de verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="6f285-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="6f285-262">Geef in het veld **Toepassing** de URL van de toepassing op.</span><span class="sxs-lookup"><span data-stu-id="6f285-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="6f285-263">Geef in het veld **Tenant** de provider van de toepassing op.</span><span class="sxs-lookup"><span data-stu-id="6f285-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="6f285-264">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6f285-264">Select **Save**.</span></span> 
9. <span data-ttu-id="6f285-265">Wanneer u de verbinding met de geconfigureerde toepassing controleert, selecteert u op de pagina **Maak verbinding met externe toepassing** de link **Selecteer hier om verbinding te maken met de geselecteerde externe toepassing**.</span><span class="sxs-lookup"><span data-stu-id="6f285-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="6f285-266">Selecteer **Verbinding controleren** om de toegang tot de geconfigureerde toepassing te valideren.</span><span class="sxs-lookup"><span data-stu-id="6f285-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="6f285-267">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="6f285-267">Select **Close**.</span></span>

<span data-ttu-id="6f285-268">Wanneer u de procedure voltooid en de verbindingsvalidatie slaagt, worden de versie- en tenantgegevens voor de geconfigureerde toepassing bijgewerkt in het huidige raster.</span><span class="sxs-lookup"><span data-stu-id="6f285-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="6f285-269">De bestaande modeltoewijzingsconfiguratie controleren</span><span class="sxs-lookup"><span data-stu-id="6f285-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="6f285-270">Ga naar **Alle werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="6f285-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="6f285-271">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="6f285-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="6f285-272">Selecteer in de structuur **Buitenlandse handel model \> Buitenlandse handel toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="6f285-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="6f285-273">Selecteer het sneltabblad **Vereisten**.</span><span class="sxs-lookup"><span data-stu-id="6f285-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f285-274">Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="6f285-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="6f285-275">De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.</span><span class="sxs-lookup"><span data-stu-id="6f285-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="6f285-276">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-276">Select **Designer**.</span></span>
5. <span data-ttu-id="6f285-277">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-277">Select **Designer**.</span></span>
6. <span data-ttu-id="6f285-278">Selecteer in de structuur **Dynamics 365 for Operations \> Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="6f285-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="6f285-279">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-279">Select **Add root**.</span></span>
8. <span data-ttu-id="6f285-280">Typ of selecteer een waarde in het veld **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="6f285-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f285-281">Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="6f285-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="6f285-282">De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.</span><span class="sxs-lookup"><span data-stu-id="6f285-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="6f285-283">Selecteer **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="6f285-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="6f285-284">De verbonden toepassing toewijzen aan een modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="6f285-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="6f285-285">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="6f285-285">Select **Edit**.</span></span>
2. <span data-ttu-id="6f285-286">Selecteer in het veld **Verbonden toepassing** de toepassing **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="6f285-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f285-287">Deze toewijzing verwijst naar de metagegevens van de geselecteerde verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="6f285-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="6f285-288">Wanneer een toewijzing tegelijkertijd verwijst naar de configuratie van de metagegevens en de gekoppelde toepassing, dan worden de metagegevens van de verbonden toepassing gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6f285-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="6f285-289">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-289">Select **Designer**.</span></span>
4. <span data-ttu-id="6f285-290">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6f285-290">Select **Designer**.</span></span>
5. <span data-ttu-id="6f285-291">Selecteer in de structuur **Dynamics 365 for Operations \> Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="6f285-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="6f285-292">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6f285-292">Select **Add root**.</span></span>
7. <span data-ttu-id="6f285-293">Typ of selecteer een waarde in het veld **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="6f285-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f285-294">Op dit punt worden meer dan twee toepassingstabellen aangeboden, omdat deze toewijzing alle metagegevens van de verbonden toepassing gebruikt die hieraan is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6f285-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="6f285-295">Selecteer **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="6f285-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="6f285-296">Selecteer **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="6f285-296">Select **Validate**.</span></span>

<span data-ttu-id="6f285-297">U hebt nu elementen van het gegevensmodel verbonden met items van de gegevensbronnen die worden beschreven met behulp van details van de metagegevens van de verbonden toepassing die is toegewezen voor deze toewijzing.</span><span class="sxs-lookup"><span data-stu-id="6f285-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="6f285-298">Wanneer u deze modeltoewijzing moet evalueren door de metagegevens van een andere versie van de applicatie te gebruiken, registreer dan een andere verbonden toepassing, en wijs deze toe aan deze modeltoewijzing en valideer deze tegen de nieuwe metagegevens.</span><span class="sxs-lookup"><span data-stu-id="6f285-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f285-299">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6f285-299">Additional resources</span></span>

<span data-ttu-id="6f285-300">U kunt ook de taakbegeleider **Metagegevens van de toepassing die kunnen worden gebruikt in RCS voorbereiden** in de toepassing bekijken, evenals de taakbegeleiders **Metagegevens van de toepassing openen met gebruik van een ER-configuratie** en **Metagegevens van de toepassing openen met gebruik van verbonden toepassingen** in RCS.</span><span class="sxs-lookup"><span data-stu-id="6f285-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="6f285-301">Deze taakbegeleiders kunt u downloaden van de pagina [Taakbegeleiders voor Elektronische rapportage voor Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="6f285-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
