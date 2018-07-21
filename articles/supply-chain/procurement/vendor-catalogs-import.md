---
title: Leverancierscatalogi importeren
description: Dit onderwerp beschrijft het importproces van leverancierscatalogusgegevens.
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: 
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: d9e1202b7b4f995c9e54002df93c53c0976373fe
ms.contentlocale: nl-nl
ms.lasthandoff: 07/21/2018

---

# <a name="import-vendor-catalogs"></a><span data-ttu-id="77948-103">Leverancierscatalogi importeren</span><span class="sxs-lookup"><span data-stu-id="77948-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="77948-104">Leverancierscatalogi importeren</span><span class="sxs-lookup"><span data-stu-id="77948-104">Vendor catalogs import</span></span>

<span data-ttu-id="77948-105">In Microsoft Dynamics 365 for Finance and Operations kunnen inkoopprofessionals catalogi maken en onderhouden die werknemers van het bedrijf kunnen gebruiken wanneer ze artikelen en services voor intern gebruik bestellen.</span><span class="sxs-lookup"><span data-stu-id="77948-105">In Microsoft Dynamics 365 for Finance and Operations, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="77948-106">Wanneer u een aanschaffingscatalogus maakt, kunt u de artikelen en diensten toevoegen die u beschikbaar wilt maken voor werknemers door de gegevens van de productcatalogus te importeren of door de gegevens van de productcatalogus handmatig aan het productmodel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="77948-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="77948-107">U kunt catalogusgegevens die zijn ingediend door een leverancier uploaden uit de Microsoft Dynamics 365-client.</span><span class="sxs-lookup"><span data-stu-id="77948-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="77948-108">De productgegevens die een leverancier bij u indient in het formulier van een CMR-bestand (Catalog Maintenance Request) moeten de XML-bestandsindeling hebben.</span><span class="sxs-lookup"><span data-stu-id="77948-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="77948-109">Het CMR-bestand moet gegevens bevatten voor de producten die de leveranciers aan uw bedrijf levert.</span><span class="sxs-lookup"><span data-stu-id="77948-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="77948-110">Leverancierscatalogusgegevens importeren</span><span class="sxs-lookup"><span data-stu-id="77948-110">Import vendor catalog data</span></span>

<span data-ttu-id="77948-111">U moet de volgende taken uitvoeren om leverancierscatalogusgegevens te importeren:</span><span class="sxs-lookup"><span data-stu-id="77948-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="77948-112">Stel een project in in het werkgebied Gegevensbeheer waar u uw toewijzingsregels voor gegevens hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="77948-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="77948-113">Selecteer **Gegevensbeheer** en selecteer vervolgens **Rollen voor gegevensprojecten instellen**.</span><span class="sxs-lookup"><span data-stu-id="77948-113">Select **Data management** and then select **Set up roles for data projects**.</span></span> 

2.  <span data-ttu-id="77948-114">Stel een hiërarchie van aanschaffingscategorieën in en wijs uw leveranciers aan aanschaffingscategorieën toe.</span><span class="sxs-lookup"><span data-stu-id="77948-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="77948-115">Als u basisproductcodes gebruikt, voegt u de basisproductcodes aan de aanschaffingscategorieën toe.</span><span class="sxs-lookup"><span data-stu-id="77948-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="77948-116">Zie [Een hiërarchie van aanschaffingscategorieën instellen](../procurement/tasks/set-up-procurement-category-hierarchy.md) voor informatie over het instellen van een hiërarchie van aanschaffingscategorieën.</span><span class="sxs-lookup"><span data-stu-id="77948-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3.  <span data-ttu-id="77948-117">Configureer de leveranciers voor het importeren van catalogi.</span><span class="sxs-lookup"><span data-stu-id="77948-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="77948-118">Selecteer een leverancier en selecteer vervolgens **Inkoop** > **Instellen** > **Leverancier configureren voor importeren van catalogus**.</span><span class="sxs-lookup"><span data-stu-id="77948-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4.  <span data-ttu-id="77948-119">Configureer de workflow voor het importeren van catalogi.</span><span class="sxs-lookup"><span data-stu-id="77948-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="77948-120">Maak een CMR-bestandssjabloon en deel deze met uw leverancier.</span><span class="sxs-lookup"><span data-stu-id="77948-120">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="77948-121">Selecteer **Inkoop en sourcing** \> **Algemeen** \> **Catalogi** \> **Leverancierscatalogi** voor het maken van een leverancierscatalogus.</span><span class="sxs-lookup"><span data-stu-id="77948-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="77948-122">De catalog maintenance request (CMR)-bestanden die u van uw leverancier ontvangt, worden in deze catalogus gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="77948-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="77948-123">Upload het CMR-bestand.</span><span class="sxs-lookup"><span data-stu-id="77948-123">Upload the CMR file.</span></span>

7.  <span data-ttu-id="77948-124">De producten controleren, goedkeuren of afwijzen in de leverancierscatalogus.</span><span class="sxs-lookup"><span data-stu-id="77948-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="77948-125">De producten worden automatisch toegewezen aan de aanschaffingscategorieën in Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="77948-125">The products are automatically mapped to the procurement categories in Dynamics 365 for Finance and Operations.</span></span> 
    
<span data-ttu-id="77948-126">Goedgekeurde producten worden toegevoegd aan het productmodel en worden vrijgegeven aan de geselecteerde rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="77948-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="77948-127">Alleen goedgekeurde producten kunnen aan de aanschaffingscatalogus worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="77948-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="77948-128">Een sjabloon voor een catalogusimportbestand</span><span class="sxs-lookup"><span data-stu-id="77948-128">Generate a catalog import file template</span></span>

<span data-ttu-id="77948-129">De sjabloon voor het catalogusimportbestand is een XSD-bestand dat u kunt gebruiken voor het maken van een CMR-bestand voor de producten van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="77948-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor’s products.</span></span> <span data-ttu-id="77948-130">U kunt het CMR-bestand gebruiken voor het maken van een nieuwe catalogus, het vervangen van een bestaande catalogus of het wijzigen van een bestaande catalogus.</span><span class="sxs-lookup"><span data-stu-id="77948-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="77948-131">Selecteer **Inkoop en sourcing** \> **Catalogi** \> **Leverancierscatalogi** en dubbelklik op de catalogus die u wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="77948-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="77948-132">Download een bestaande sjabloon voor catalogusimport (XSD-bestand).</span><span class="sxs-lookup"><span data-stu-id="77948-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="77948-133">Op de pagina **Catalogus bijwerken** klikt u in het **actievenster**op het tabblad **Catalogi** in de groep **Verwante informatie** op **Catalogussjabloon genereren** en selecteert u **Aanschaffingscategorie**.</span><span class="sxs-lookup"><span data-stu-id="77948-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="77948-134">Met de optie **Aanschaffingscategorie** kunt u een catalogussjabloon genereren die de aanschaffingscategorieën bevat waarvoor de leverancier producten mag leveren.</span><span class="sxs-lookup"><span data-stu-id="77948-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="77948-135">Selecteer in het dialoogvenster **Opslaan als** de locatie waar u de sjabloon voor het catalogusbestand wilt opslaan, waarna u het bestand opslaat.</span><span class="sxs-lookup"><span data-stu-id="77948-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="77948-136">Voor meer informatie en voorbeelden verwijzen we naar dit blogbericht: [Leverancierscatalogi in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="77948-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>

