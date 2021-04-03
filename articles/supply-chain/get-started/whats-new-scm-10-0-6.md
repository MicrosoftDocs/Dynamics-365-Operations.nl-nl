---
title: Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.6 (november 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 77fdc3ae092fc8f214ae3ba68866244385e32b74
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263417"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="1a495-103">Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.6 (november 2019)</span><span class="sxs-lookup"><span data-stu-id="1a495-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a495-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="1a495-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="1a495-105">Deze versie heeft buildnummer 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="1a495-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="1a495-106">Hoewel de datum voor algemene beschikbaarheid in november is, zijn de nieuwe functies beschikbaar voor vroege vrijgave in oktober.</span><span class="sxs-lookup"><span data-stu-id="1a495-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="1a495-107">Zie voor meer informatie over versie 10.0.6 [Aanvullende resources](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="1a495-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="1a495-108">V2 van gegevensentiteit productconfiguratiemodellen</span><span class="sxs-lookup"><span data-stu-id="1a495-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="1a495-109">Er wordt een tweede versie voor de gegevensentiteit productconfiguratiemodellen vrijgegeven (productconfiguratiemodellen V2).</span><span class="sxs-lookup"><span data-stu-id="1a495-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="1a495-110">Voor de standaardsjabloon 418-productconfiguratiemodellen moet ook de nieuwe gegevensentiteit productconfiguratiemodellen V2 worden gebruikt in de import- en exportraamwerksjablonen.</span><span class="sxs-lookup"><span data-stu-id="1a495-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="1a495-111">De sjabloon wordt niet automatisch bijgewerkt, zodat u de sjabloon handmatig op basis van de standaard moet laden.</span><span class="sxs-lookup"><span data-stu-id="1a495-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="1a495-112">De V2-entiteit exporteert één rij als afzonderlijk bestand in een bijlage in plaats van inline, waarbij de groottebeperkingen van de V1-entiteit worden opgelost.</span><span class="sxs-lookup"><span data-stu-id="1a495-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="1a495-113">Wat moet u doen om deze wijziging door te voeren?</span><span class="sxs-lookup"><span data-stu-id="1a495-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="1a495-114">Aangezien de V1-entiteit is afgeschaft, moet u beginnen met de migratie van V1 naar V2.</span><span class="sxs-lookup"><span data-stu-id="1a495-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="1a495-115">Als u de sjabloon 418-productconfiguratiemodellen gebruikt, kunt u op de knop standaardsjablonen laden klikken en de sjabloon 418-productconfiguratiemodellen opnieuw laden.</span><span class="sxs-lookup"><span data-stu-id="1a495-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="1a495-116">Als u de compatibiliteit met bestaande systemen wilt behouden, kunt u voorlopig de bestaande sjabloon en de (afgeschafte) V1-entiteit blijven gebruiken totdat u uw integraties naar de nieuwe sjabloon verplaatst.</span><span class="sxs-lookup"><span data-stu-id="1a495-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="1a495-117">Verbeteringen in Functiebeheer</span><span class="sxs-lookup"><span data-stu-id="1a495-117">Feature management enhancements</span></span>
<span data-ttu-id="1a495-118">Met Functiebeheer kunt u nu standaard alle nieuwe functies inschakelen, bevestiging vereisen om een functie in te schakelen en alle functies inschakelen die nog niet zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1a495-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="1a495-119">Verantwoordelijke partij voor inkoopovereenkomst</span><span class="sxs-lookup"><span data-stu-id="1a495-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="1a495-120">U hebt nu de mogelijkheid om primaire en secundaire verantwoordelijke partijen te definiëren in het formulier Classificatie van inkoopovereenkomst en resulterende inkoopovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="1a495-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="1a495-121">Zo krijgt de gebruiker toegang tot de gebruiker die de overeenkomsten overziet.</span><span class="sxs-lookup"><span data-stu-id="1a495-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="1a495-122">De koppeling Offerteaanvraag op de inkooporderregel</span><span class="sxs-lookup"><span data-stu-id="1a495-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="1a495-123">U kunt vanuit de inkooporderregels een verwijzingskoppeling toevoegen die weer verwijst naar de offerteaanvraagregels waaruit deze afkomstig zijn, zodat de gebruiker eenvoudig kan worden voorzien van het ondersteunende offertedocument.</span><span class="sxs-lookup"><span data-stu-id="1a495-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a495-124">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1a495-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1a495-125">Correcties</span><span class="sxs-lookup"><span data-stu-id="1a495-125">Bug fixes</span></span>
<span data-ttu-id="1a495-126">Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.6, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="1a495-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="1a495-127">Platformupdate 30</span><span class="sxs-lookup"><span data-stu-id="1a495-127">Platform update 30</span></span>
<span data-ttu-id="1a495-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 bevat platformupdate 30.</span><span class="sxs-lookup"><span data-stu-id="1a495-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="1a495-129">Zie [Nieuw of gewijzigd in platformupdate 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md) voor meer informatie over platformupdate 30.</span><span class="sxs-lookup"><span data-stu-id="1a495-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="1a495-130">Dynamics 365: releasewave 2-plan van 2019</span><span class="sxs-lookup"><span data-stu-id="1a495-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="1a495-131">Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?</span><span class="sxs-lookup"><span data-stu-id="1a495-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="1a495-132">Bekijk [Dynamics 365: releasewave 2-plan van 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="1a495-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="1a495-133">We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.</span><span class="sxs-lookup"><span data-stu-id="1a495-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="1a495-134">Verwijderde en afgeschafte functies voor Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1a495-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="1a495-135">In het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1a495-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="1a495-136">Een *verwijderde* functie is niet langer beschikbaar in het product.</span><span class="sxs-lookup"><span data-stu-id="1a495-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="1a495-137">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="1a495-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="1a495-138">Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).</span><span class="sxs-lookup"><span data-stu-id="1a495-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="1a495-139">Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden.</span><span class="sxs-lookup"><span data-stu-id="1a495-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="1a495-140">Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.</span><span class="sxs-lookup"><span data-stu-id="1a495-140">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]