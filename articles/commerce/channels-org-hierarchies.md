---
title: Organisatiehiërarchieën instellen
description: In dit onderwerp wordt beschreven hoe u organisatiehiërarchieën instelt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ce0732f32a9a80fc5b0ede7ae9f1c1ab9a68a89b2fb0b1821cb5df123ca5ca4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746011"
---
# <a name="set-up-organization-hierarchies"></a>Organisatiehiërarchieën instellen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u organisatiehiërarchieën instelt in Microsoft Dynamics 365 Commerce.

Voordat u kanalen gaat maken, moet u controleren of uw organisatiehiërarchieën zijn ingesteld.

Met organisatiehiërarchieën kunt u vanuit verschillende gezichtspunten kijken naar en rapporteren over uw bedrijf. U kunt bijvoorbeeld een hiërarchie instellen voor belastingaangifte. Vervolgens kunt u een andere hiërarchie instellen voor het rapporteren van financiële gegevens die niet wettelijk vereist zijn, maar die voor interne rapportage worden gebruikt.

Voordat u een organisatiehiërarchie maakt, moet u organisaties maken. Zie voor meer informatie [Rechtspersonen maken](channels-legal-entities.md) of [Operationele eenheden maken](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Zie de volgende onderwerpen voor meer informatie.
- [Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Uw organisatiehiërarchie plannen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Een organisatiehiërarchie maken](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Een organisatiehiërarchie maken

Volg deze stappen om om een organisatiehiërarchie te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Organisatiehiërarchieën**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer een waarde in het veld **Naam** in.
1. Selecteer in de sectie **Doel** de optie **Doel toewijzen**.
1. Zoek en selecteer de gewenste record in de lijst. Selecteer een doel om aan uw organisatiehiërarchie toe te wijzen.
1. Selecteer in de sectie **Toegewezen hiërarchieën** de optie **Toevoegen**.
1. Markeer in de lijst de geselecteerde rij. Zoek de hiërarchie u zojuist hebt gemaakt.
1. Selecteer **OK**.

De volgende afbeelding toont een voorbeeld van een organisatiehiërarchie die is gemaakt voor een fictieve reeks winkels van Adventure Works.

![Voorbeeld van een organisatiehiërarchie.](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Organisaties aan een hiërarchie toevoegen

Volg deze stappen om organisaties toe te voegen aan een hiërarchie.

1. Zoek en selecteer de gewenste record in de lijst. Selecteer uw hiërarchie.
1. Selecteer **Weergeven** in het actievenster.
1. Voer zo nodig organisaties toe.
1. Als u een organisatie wilt toevoegen, selecteert u **Bewerken** en vervolgens **Invoegen**. Wanneer u klaar bent met het aanbrengen van wijzigingen, kunt u een concept opslaan en de wijzigingen publiceren.

De volgende afbeelding toont een rechtspersoon die is toegevoegd aan de hiërarchiebasis. Er zijn vier kostenplaatsen toegevoegd: de kanalen winkelcentrum, outlet, online en callcenter. Aan elke winkel kunnen diverse detailhandels-, callcenter- en onlinekanalen worden toegevoegd.

![Voorbeeld van hiërarchieontwerper.](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Uw organisatiehiërarchie plannen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Rechtspersonen maken](channels-legal-entities.md)

[Operationele eenheden maken](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
