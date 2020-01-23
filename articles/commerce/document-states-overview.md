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
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914882"
---
# <a name="document-states-and-lifecycle"></a>Statussen en levenscyclus document

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.

## <a name="document-state-descriptions"></a>Omschrijvingen van documenstatus

Het onderwerp [Pagina-elementen](page-elements-overview.md) geeft een overzicht van diverse documenttypen in het Content Management System (CMS). Deze documenttypen kunnen verschillende statussen hebben in het ontwerpprogramma. De documentstatussen helpen bij het voorkomen van gegevensconflicten en het afdwingen van versiebeheer. De status bepaalt wie de documenten kan wijzigen, wanneer de documenten kunnen worden gewijzigd en wanneer wijzigingen door anderen kunnen worden bekeken.

In de volgende tabel ziet u de mogelijke documentstatussen van pagina-elementen in Commerce.

| Documentstatus | Beschrijving |
|---|---|
| Uitgecheckt | Wanneer een CMS-item naar u is uitgecheckt, kan het niet door andere geverifieerde systeemgebruikers worden bewerkt. Alle wijzigingen die u in het item aanbrengt, zijn alleen voor u zichtbaar. |
| Ingecheckt | Wanneer een CMS-item is ingecheckt, zijn alle wijzigingen zichtbaar voor andere geverifieerde systeemgebruikers en kunnen deze gebruikers het item uitchecken en bewerken. Bij het inchecken wordt een documentversierecord gemaakt in de historie van het item. |
| Gepubliceerd | Wanneer een CMS-item wordt gepubliceerd, wordt het op uw live site geplaatst en is het detecteerbaar voor niet-geverifieerde externe gebruikers op internet. Items kunnen alleen worden gepubliceerd als ze zijn ingecheckt. |
| Opgeslagen | Wijzigingen die zijn aangebracht in een uitgecheckt CMS-item, kunnen in het CMS-item worden opgeslagen voordat het item wordt ingecheckt of gepubliceerd. Deze opgeslagen wijzigingen zijn pas zichtbaar voor andere geverifieerde systeemgebruikers als het item is ingecheckt. Het item is pas zichtbaar voor externe gebruikers als het is gepubliceerd. |
| Verwijderde items uitchecken | Wanneer een uitgecheckt CMS-item wordt verwijderd, worden alle opgeslagen wijzigingen verwijderd en keert het item terug naar de versie die het laatst is ingecheckt. |

## <a name="additional-resources"></a>Aanvullende resources

[Manieren om inhoud toe te voegen](add-manage-content.md)

[Woordenlijst voor paginamodellen](page-elements-overview.md)

[Werken met publicatiegroepen](publish-groups.md)

[Werken met modules](work-with-modules.md)

[Werken met fragmenten](work-with-fragments.md)

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Sitenavigatie aanpassen](customize-site-navigation.md)
