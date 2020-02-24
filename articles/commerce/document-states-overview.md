---
title: Statussen en levenscyclus document
description: In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002976"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="f8fd2-103">Statussen en levenscyclus document</span><span class="sxs-lookup"><span data-stu-id="f8fd2-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8fd2-104">In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="f8fd2-105">Omschrijvingen van documenstatus</span><span class="sxs-lookup"><span data-stu-id="f8fd2-105">Document state descriptions</span></span>

<span data-ttu-id="f8fd2-106">Het onderwerp [Pagina-elementen](page-elements-overview.md) geeft een overzicht van diverse documenttypen in het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="f8fd2-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="f8fd2-107">Deze documenttypen kunnen verschillende statussen hebben in het ontwerpprogramma.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="f8fd2-108">De documentstatussen helpen bij het voorkomen van gegevensconflicten en het afdwingen van versiebeheer.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="f8fd2-109">De status bepaalt wie de documenten kan wijzigen, wanneer de documenten kunnen worden gewijzigd en wanneer wijzigingen door anderen kunnen worden bekeken.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="f8fd2-110">In de volgende tabel ziet u de mogelijke documentstatussen van pagina-elementen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="f8fd2-111">Documentstatus</span><span class="sxs-lookup"><span data-stu-id="f8fd2-111">Document state</span></span> | <span data-ttu-id="f8fd2-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f8fd2-112">Description</span></span> |
|---|---|
| <span data-ttu-id="f8fd2-113">Uitgecheckt</span><span class="sxs-lookup"><span data-stu-id="f8fd2-113">Checked out</span></span> | <span data-ttu-id="f8fd2-114">Wanneer een CMS-item naar u is uitgecheckt, kan het niet door andere geverifieerde systeemgebruikers worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="f8fd2-115">Alle wijzigingen die u in het item aanbrengt, zijn alleen voor u zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="f8fd2-116">Ingecheckt</span><span class="sxs-lookup"><span data-stu-id="f8fd2-116">Checked in</span></span> | <span data-ttu-id="f8fd2-117">Wanneer een CMS-item is ingecheckt, zijn alle wijzigingen zichtbaar voor andere geverifieerde systeemgebruikers en kunnen deze gebruikers het item uitchecken en bewerken.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="f8fd2-118">Bij het inchecken wordt een documentversierecord gemaakt in de historie van het item.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="f8fd2-119">Gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="f8fd2-119">Published</span></span> | <span data-ttu-id="f8fd2-120">Wanneer een CMS-item wordt gepubliceerd, wordt het op uw live site geplaatst en is het detecteerbaar voor niet-geverifieerde externe gebruikers op internet.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="f8fd2-121">Items kunnen alleen worden gepubliceerd als ze zijn ingecheckt.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="f8fd2-122">Opgeslagen</span><span class="sxs-lookup"><span data-stu-id="f8fd2-122">Saved</span></span> | <span data-ttu-id="f8fd2-123">Wijzigingen die zijn aangebracht in een uitgecheckt CMS-item, kunnen in het CMS-item worden opgeslagen voordat het item wordt ingecheckt of gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="f8fd2-124">Deze opgeslagen wijzigingen zijn pas zichtbaar voor andere geverifieerde systeemgebruikers als het item is ingecheckt.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="f8fd2-125">Het item is pas zichtbaar voor externe gebruikers als het is gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="f8fd2-126">Verwijderde items uitchecken</span><span class="sxs-lookup"><span data-stu-id="f8fd2-126">Discarded check out</span></span> | <span data-ttu-id="f8fd2-127">Wanneer een uitgecheckt CMS-item wordt verwijderd, worden alle opgeslagen wijzigingen verwijderd en keert het item terug naar de versie die het laatst is ingecheckt.</span><span class="sxs-lookup"><span data-stu-id="f8fd2-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="f8fd2-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f8fd2-128">Additional resources</span></span>

[<span data-ttu-id="f8fd2-129">Manieren om inhoud toe te voegen</span><span class="sxs-lookup"><span data-stu-id="f8fd2-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="f8fd2-130">Woordenlijst voor paginamodellen</span><span class="sxs-lookup"><span data-stu-id="f8fd2-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="f8fd2-131">Werken met publicatiegroepen</span><span class="sxs-lookup"><span data-stu-id="f8fd2-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="f8fd2-132">Werken met modules</span><span class="sxs-lookup"><span data-stu-id="f8fd2-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="f8fd2-133">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="f8fd2-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f8fd2-134">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="f8fd2-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f8fd2-135">Sitenavigatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="f8fd2-135">Customize site navigation</span></span>](customize-site-navigation.md)
