---
title: Statussen en levenscyclus document
description: In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ad8547fe6b36caf75ce78cb09fb2caf901c63afe43fa4755bb9e5c69427829d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727576"
---
# <a name="document-states-and-lifecycle"></a>Statussen en levenscyclus van document

[!include [banner](includes/banner.md)]

In dit onderwerp worden de verschillende documentstatussen van pagina-elementen in Microsoft Dynamics 365 Commerce beschreven.

## <a name="document-state-descriptions"></a>Omschrijvingen van documenstatus

Het onderwerp [Pagina-elementen](page-elements-overview.md) geeft een overzicht van diverse documenttypen in het Content Management System (CMS). Deze documenttypen kunnen verschillende statussen hebben in het ontwerpprogramma. De documentstatussen helpen bij het voorkomen van gegevensconflicten en het afdwingen van versiebeheer. De status bepaalt wie de documenten kan wijzigen, wanneer de documenten kunnen worden gewijzigd en wanneer wijzigingen door anderen kunnen worden bekeken.

In de volgende tabel ziet u de mogelijke documentstatussen van pagina-elementen in Commerce.

| Documentstatus      | Site builder-actie        | Omschrijving                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Uitgecheckt         | Selecteer **Bewerken**.           | Het desbetreffende document is naar u uitgecheckt. Terwijl een document in deze status is, kan het niet worden gewijzigd door andere geverifieerde systeemgebruikers en zijn wijzigingen die u in het document aanbrengt alleen voor u zichtbaar. |
| Opgeslagen               | Selecteer **Opslaan**.           | Wijzigingen die zijn aangebracht in een uitgecheckt document, worden opgeslagen in de database, maar het document is nog niet ingecheckt of gepubliceerd. De opgeslagen wijzigingen zijn pas zichtbaar voor andere geverifieerde systeemgebruikers als de auteur **Bewerken voltooien** selecteert. Het item is pas zichtbaar voor externe gebruikers als het is gepubliceerd. |
| Verwijderde items uitchecken | Selecteer **Bewerkingen negeren**.  | Alle wijzigingen in het uitgecheckte document worden genegeerd en het artikel wordt teruggezet naar de laatste versie die is ingecheckt. |
| Ingecheckt          | Selecteer **Bewerken voltooien**. | Het bewerkte document wordt ingecheckt. Alle wijzigingen zijn zichtbaar voor andere geverifieerde systeemgebruikers en die gebruikers kunnen het document vervolgens bewerken. Bij het inchecken wordt een documentversierecord gemaakt in de historie van het item. |
| Gepubliceerd           | Selecteer **Publiceren**.        | Het document wordt gepubliceerd en de wijzigingen worden op uw live site geplaatst en kunnen door externe gebruikers worden gedetecteerd. Artikelen kunnen alleen worden gepubliceerd als ze het eerst zijn ingecheckt door **Bewerken voltooien** te selecteren. |

## <a name="additional-resources"></a>Aanvullende bronnen

[Manieren om inhoud toe te voegen](add-manage-content.md)

[Woordenlijst voor paginamodellen](page-elements-overview.md)

[Werken met groepen publiceren](publish-groups.md)

[Het delen van inhoud door meerdere kanalen inschakelen en gebruiken](cross-channel-sharing.md)

[Werken met modules](work-with-modules.md)

[Werken met fragmenten](work-with-fragments.md)

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Sitenavigatie aanpassen](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]