---
title: Een logo toevoegen
description: In dit artikel wordt beschreven hoe u een logo aan uw site toevoegt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 624cd6f7000f5038b9996eb94caf79719d07f99f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871775"
---
# <a name="add-a-logo"></a>Een logo toevoegen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een logo aan uw site toevoegt in Microsoft Dynamics 365 Commerce.

Wanneer u uw site bouwt, is het toevoegen van uw bedrijfs- of merklogo aan de koptekst van de site waarschijnlijk een van de eerste dingen die u doet. De online modulebibliotheek van Dynamics 365 Commerce bevat een module die deze taak gemakkelijk maakt.

U kunt een logo direct aan een sjabloon, indeling of pagina toevoegen. Op deze manier kunt u eenvoudig het logo wijzigen dat op specifieke pagina's of groepen pagina's wordt weergegeven. In dit artikel komen echter de meest voorkomende scenario's aan bod, waarbij u uw logo toevoegt aan een koptekstfragment dat op alle pagina's van uw site kan worden hergebruikt.

## <a name="prerequisites"></a>Vereisten

Voordat u een logo aan alle pagina's van uw site kunt toevoegen, moet u deze taken uitvoeren.

1. Upload uw logo naar de mediabibliotheek.
1. Maak een koptekstfragment. Zie [Werken met fragmenten](work-with-fragments.md) voor meer informatie over het maken en gebruiken van fragmenten.
1. Neem het koptekstfragment op in de sjabloon die door de pagina's van uw site worden gebruiken voor hun indelings- en moduleopties. Zie [Werken met sjablonen](work-with-templates.md) voor meer informatie over het gebruik van sjablonen.

## <a name="add-a-logo-to-a-header-fragment"></a>Een logo toevoegen aan een koptekstfragment

Volg deze stappen om een logo toe te voegen aan het koptekstfragment voor uw site.

1. Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.
1. Selecteer het koptekstfragment dat u eerder hebt gemaakt en selecteer **Bewerken**.
1. Vouw de koptekstmodule uit.
1. Geef in het eigenschappenvenster voor de koptekstmodule een afbeelding op en een koppeling voor het logo. 
1. Sla het koptekstfragment op, voltooi de bewerking ervan en publiceer het fragment.

Als u het bijgewerkte koptekstfragment publiceert, wordt uw logo weergegeven op alle sitepagina's die gebruikmaken van de sjabloon die het koptekstfragment bevat.

## <a name="additional-resources"></a>Aanvullende resources

[Een thema voor de site selecteren](select-site-theme.md)

[Werken met CSS-overschrijvingsbestanden](css-override-files.md)

[Een favicon toevoegen](add-favicon.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
