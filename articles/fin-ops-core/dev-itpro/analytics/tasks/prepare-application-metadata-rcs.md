---
title: Metagegevens van de toepassing voorbereiden voor gebruik in RCS
description: In de stappen in dit onderwerp wordt uitgelegd hoe een gebruiker een nieuwe configuratie voor een elektronische rapportage (ER) kan maken die de metagegevens bevat voor het ontwerpen van ER‑modelconfiguratie in Regulatory Configuration Service (RCS).
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
ms.openlocfilehash: e3a33eefca98e14ed0435f8f1a7a9f90a69498ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182158"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="4810e-103">Metagegevens van de toepassing voorbereiden voor gebruik in RCS</span><span class="sxs-lookup"><span data-stu-id="4810e-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4810e-104">De volgende stappen leggen uit hoe een gebruiker met de rol Systeembeheerder of Ontwikkelaar Elektronische Rapportage een nieuwe configuratie voor een elektronische rapportage (ER) kan maken die de metagegevens van de toepassing bevat voor het ontwerpen van ER‑modelconfiguratie in Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="4810e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="4810e-105">Deze configuratie wordt gebruikt voor het ontwerpen van een voorbeeld van een ER‑modeltoewijzingsconfiguratie om transacties van buitenlandse handel te openen.</span><span class="sxs-lookup"><span data-stu-id="4810e-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="4810e-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4810e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="4810e-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="4810e-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4810e-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="4810e-108">Prerequisites</span></span>
1.  <span data-ttu-id="4810e-109">Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="4810e-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="4810e-110">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="4810e-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="4810e-111">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="4810e-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="4810e-112">Klik op **Metagegevensconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="4810e-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="4810e-113">Stel dat RCS zal worden gebruikt om een ER-oplossing te ontwerpen voor Finance and Operations‑toepassing die elektronische documenten zal genereren die informatie bevatten uit het bedrijfsdomein voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="4810e-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="4810e-114">Als u de toewijzing wilt opgeven tussen het ER-gegevensmodel en de bronnen van vereiste gegevens, moeten we in RCS toegang hebben tot de metagegevens van de Finance and Operations‑toepassing.</span><span class="sxs-lookup"><span data-stu-id="4810e-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="4810e-115">Als onderdeel van het ontwerpproces van de ER-oplossing moeten we dus een nieuwe ER-metagegevensconfiguratie configureren die alle vereiste metagegevens bevat voor het genereren van ER‑rapporten voor het geselecteerde bedrijfsdomein.</span><span class="sxs-lookup"><span data-stu-id="4810e-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="4810e-116">Metagegevensconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="4810e-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="4810e-117">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="4810e-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="4810e-118">Type 'Metadata buitenlandse handel' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="4810e-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="4810e-119">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="4810e-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="4810e-120">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="4810e-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="4810e-121">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="4810e-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4810e-122">U kunt alle metagegevens voor de gehele toepassing of voor geselecteerde modellen of modules selecteren.</span><span class="sxs-lookup"><span data-stu-id="4810e-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="4810e-123">Houd er in dit geval rekening mee dat de volgende metagegevens automatisch worden toegevoegd: tabellen met records, inventarisaties en uitgebreide gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="4810e-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="4810e-124">Als er aanvullende typen metagegevens nodig zijn, moeten deze handmatig worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4810e-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="4810e-125">We hebben wat metagegevens die zijn gerelateerd aan transacties voor buitenlandse handel door metagegevensitems handmatig te selecteren.</span><span class="sxs-lookup"><span data-stu-id="4810e-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="4810e-126">Klik op **Gegevensbron toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="4810e-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="4810e-127">Klik op **Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="4810e-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="4810e-128">Gebruik het snelfilter om in het veld **Naam** te filteren met een waarde van 'Intrastat'.</span><span class="sxs-lookup"><span data-stu-id="4810e-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="4810e-129">Selecteer de **Intrastat** -tabelrecord.</span><span class="sxs-lookup"><span data-stu-id="4810e-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="4810e-130">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="4810e-130">Click **OK**.</span></span>
  
<span data-ttu-id="4810e-131">We hebben metagegevens over de Intrastat-tabelrecords toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4810e-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="4810e-132">Vouw in de structuur **Tabelrecords Intrastat**\>**Relaties** uit.</span><span class="sxs-lookup"><span data-stu-id="4810e-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="4810e-133">Selecteer in de structuur **Tabelrecords Intrastat**\>**Relaties\ IntrastatCommodity (tabelrecords EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="4810e-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="4810e-134">Klik op **Metagegevens toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="4810e-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4810e-135">Metagegevens over vereiste relaties voor geselecteerde tabelrecords moeten handmatig worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4810e-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="4810e-136">Klik op **Gegevensbron toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="4810e-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="4810e-137">Klik **Opsomming**.</span><span class="sxs-lookup"><span data-stu-id="4810e-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="4810e-138">Gebruik het snelfilter om in het veld **Naam** te filteren met een waarde van 'IntrastatDirection'.</span><span class="sxs-lookup"><span data-stu-id="4810e-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="4810e-139">Selecteer het record **Opsomming IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="4810e-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="4810e-140">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="4810e-140">Click **OK**.</span></span> 
21. <span data-ttu-id="4810e-141">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4810e-141">Click **Save**.</span></span>  
22. <span data-ttu-id="4810e-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4810e-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="4810e-143">De conceptversie van metagegevensconfiguratie voltooien</span><span class="sxs-lookup"><span data-stu-id="4810e-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="4810e-144">Klik op **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="4810e-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="4810e-145">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="4810e-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="4810e-146">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="4810e-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="4810e-147">Selecteer de voltooide versie **1**.</span><span class="sxs-lookup"><span data-stu-id="4810e-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="4810e-148">De voltooide versie van de metagegevensconfiguratie van de toepassing exporteren als een XML-bestand</span><span class="sxs-lookup"><span data-stu-id="4810e-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="4810e-149">Klik op **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="4810e-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="4810e-150">Klik op **Exporteren als XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="4810e-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="4810e-151">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="4810e-151">Click **OK**.</span></span> 
    
<span data-ttu-id="4810e-152">De gemaakte ER‑metagegevensconfiguratie is opgeslagen als XML-bestand dat kan worden geïmporteerd naar RCS en gebruikt als de bron van informatie over metagegevens voor het bedrijfsdomein voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="4810e-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="4810e-153">Op basis van deze informatie kunnen we de toewijzing opgeven tussen de metagegevens van de toepassing en het ER-gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="4810e-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
