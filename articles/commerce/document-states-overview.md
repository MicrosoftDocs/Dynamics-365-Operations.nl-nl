---
title: Statussen en levenscyclus document
description: In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411382"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="20d21-103">Statussen en levenscyclus document</span><span class="sxs-lookup"><span data-stu-id="20d21-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20d21-104">In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.</span><span class="sxs-lookup"><span data-stu-id="20d21-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="20d21-105">Omschrijvingen van documenstatus</span><span class="sxs-lookup"><span data-stu-id="20d21-105">Document state descriptions</span></span>

<span data-ttu-id="20d21-106">Het onderwerp [Pagina-elementen](page-elements-overview.md) geeft een overzicht van diverse documenttypen in het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="20d21-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="20d21-107">Deze documenttypen kunnen verschillende statussen hebben in het ontwerpprogramma.</span><span class="sxs-lookup"><span data-stu-id="20d21-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="20d21-108">De documentstatussen helpen bij het voorkomen van gegevensconflicten en het afdwingen van versiebeheer.</span><span class="sxs-lookup"><span data-stu-id="20d21-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="20d21-109">De status bepaalt wie de documenten kan wijzigen, wanneer de documenten kunnen worden gewijzigd en wanneer wijzigingen door anderen kunnen worden bekeken.</span><span class="sxs-lookup"><span data-stu-id="20d21-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="20d21-110">In de volgende tabel ziet u de mogelijke documentstatussen van pagina-elementen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="20d21-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="20d21-111">Documentstatus</span><span class="sxs-lookup"><span data-stu-id="20d21-111">Document state</span></span>      | <span data-ttu-id="20d21-112">Site builder-actie</span><span class="sxs-lookup"><span data-stu-id="20d21-112">Site builder action</span></span>        | <span data-ttu-id="20d21-113">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="20d21-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="20d21-114">Uitgecheckt</span><span class="sxs-lookup"><span data-stu-id="20d21-114">Checked out</span></span>         | <span data-ttu-id="20d21-115">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="20d21-115">Select **Edit**.</span></span>           | <span data-ttu-id="20d21-116">Het desbetreffende document is naar u uitgecheckt.</span><span class="sxs-lookup"><span data-stu-id="20d21-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="20d21-117">Terwijl een document in deze status is, kan het niet worden gewijzigd door andere geverifieerde systeemgebruikers en zijn wijzigingen die u in het document aanbrengt alleen voor u zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="20d21-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="20d21-118">Opgeslagen</span><span class="sxs-lookup"><span data-stu-id="20d21-118">Saved</span></span>               | <span data-ttu-id="20d21-119">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="20d21-119">Select **Save**.</span></span>           | <span data-ttu-id="20d21-120">Wijzigingen die zijn aangebracht in een uitgecheckt document, worden opgeslagen in de database, maar het document is nog niet ingecheckt of gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="20d21-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="20d21-121">De opgeslagen wijzigingen zijn pas zichtbaar voor andere geverifieerde systeemgebruikers als de auteur **Bewerken voltooien** selecteert.</span><span class="sxs-lookup"><span data-stu-id="20d21-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="20d21-122">Het item is pas zichtbaar voor externe gebruikers als het is gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="20d21-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="20d21-123">Verwijderde items uitchecken</span><span class="sxs-lookup"><span data-stu-id="20d21-123">Discarded check out</span></span> | <span data-ttu-id="20d21-124">Selecteer **Bewerkingen negeren**.</span><span class="sxs-lookup"><span data-stu-id="20d21-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="20d21-125">Alle wijzigingen in het uitgecheckte document worden genegeerd en het artikel wordt teruggezet naar de laatste versie die is ingecheckt.</span><span class="sxs-lookup"><span data-stu-id="20d21-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="20d21-126">Ingecheckt</span><span class="sxs-lookup"><span data-stu-id="20d21-126">Checked in</span></span>          | <span data-ttu-id="20d21-127">Selecteer **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="20d21-127">Select **Finish editing**.</span></span> | <span data-ttu-id="20d21-128">Het bewerkte document wordt ingecheckt.</span><span class="sxs-lookup"><span data-stu-id="20d21-128">The edited document is checked in.</span></span> <span data-ttu-id="20d21-129">Alle wijzigingen zijn zichtbaar voor andere geverifieerde systeemgebruikers en die gebruikers kunnen het document vervolgens bewerken.</span><span class="sxs-lookup"><span data-stu-id="20d21-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="20d21-130">Bij het inchecken wordt een documentversierecord gemaakt in de historie van het item.</span><span class="sxs-lookup"><span data-stu-id="20d21-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="20d21-131">Gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="20d21-131">Published</span></span>           | <span data-ttu-id="20d21-132">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="20d21-132">Select **Publish**.</span></span>        | <span data-ttu-id="20d21-133">Het document wordt gepubliceerd en de wijzigingen worden op uw live site geplaatst en kunnen door externe gebruikers worden gedetecteerd.</span><span class="sxs-lookup"><span data-stu-id="20d21-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="20d21-134">Artikelen kunnen alleen worden gepubliceerd als ze het eerst zijn ingecheckt door **Bewerken voltooien** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="20d21-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="20d21-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="20d21-135">Additional resources</span></span>

[<span data-ttu-id="20d21-136">Manieren om inhoud toe te voegen</span><span class="sxs-lookup"><span data-stu-id="20d21-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="20d21-137">Woordenlijst voor paginamodellen</span><span class="sxs-lookup"><span data-stu-id="20d21-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="20d21-138">Werken met groepen publiceren</span><span class="sxs-lookup"><span data-stu-id="20d21-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="20d21-139">Het delen van inhoud door meerdere kanalen inschakelen en gebruiken</span><span class="sxs-lookup"><span data-stu-id="20d21-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="20d21-140">Werken met modules</span><span class="sxs-lookup"><span data-stu-id="20d21-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="20d21-141">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="20d21-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="20d21-142">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="20d21-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="20d21-143">Sitenavigatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="20d21-143">Customize site navigation</span></span>](customize-site-navigation.md)
