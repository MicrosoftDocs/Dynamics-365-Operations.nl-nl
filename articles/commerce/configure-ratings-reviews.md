---
title: Beoordelingen en recensies configureren
description: In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002192"
---
# <a name="configure-ratings-and-reviews"></a>Beoordelingen en recensies configureren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een inkoopbeslissing nemen, door te laten zien wat andere klanten van deze producten vinden. Voor e-commerce-websites zijn beoordelingen en recensies ook een mechanisme voor het verzamelen van klantfeedback over producten. 

Beoordelingen worden weergegeven op pagina's met productlijsten, lijstpagina's categorieën of zoekresultaten en andere sitepagina's. Beoordelingshistogrammen en productrecensies worden weergegeven op pagina's met productgegevens (PDP). Met een knop **Schrijf een recensie** kunnen klanten beoordelingen en recensies voor een product verzenden.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Beoordelings- en recensiemodules op pagina's met productgegevens 

Drie modules geven een overzicht van beoordelingen en recensies voor pagina's met productgegevens:

- Module voor recensie schrijven
- Module met productrecensie
- Module met beoordelingshistogram
 
In de volgende afbeelding ziet u hoe de modules voor beoordelingen en recensies er uitzien op een PDP.

![Beoordelings- en recensiemodules op een PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Zie [Overzicht van sjablonen en indelingen](templates-layouts-overview.md) voor informatie over het optimaliseren van de PDP-sjablonen en -indelingen zodat u de configuraties voor beoordelingen en revisies kunt delen tussen meerdere PDP-pagina's op uw e-commerce-site.

In de volgende afbeelding ziet u hoe in het dialoogvenster **Module toevoegen** modules voor beoordelingen en recensies in Dynamics 365 Commerce worden weergegeven.

![Het dialoogvenster Module toevoegen](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Module voor recensie schrijven

De module voor het schrijven van een recensie bevat een knop **Schrijf een recensie** waarmee gebruikers zich kunnen aanmelden, een beoordeling kunnen toewijzen en een recensie van een product kunnen schrijven. Met deze module kunnen gebruikers ook een beoordeling of een recensie bewerken die ze eerder hebben ingediend. Deze module wordt meestal weergegeven boven het beoordelingshistogram en de lijstmodules met productrecensies op een PDP.

In de volgende afbeelding ziet u het dialoogvenster **Schrijf een recensie** dat wordt weergegeven wanneer een klant **Schrijf een recensie** selecteert. De klant kan dit dialoog venster gebruiken om een beoordeling en een recensie in te dienen.

![Het dialoogvenster Schrijf een recensie](media/rnr-eCommerce-write-review-module.png)

In de volgende tabel wordt de eigenschap van de module voor het schrijven van een recensie weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.

| Naam van eigenschap. | Waarde        | Beschrijving eigenschap                 |
|---------------|--------------|--------------------------------------|
| Naam          | Recensie schrijven | De naam van de module voor het schrijven van een recensie. |

### <a name="ratings-histogram-module"></a>Module met beoordelingshistogram

In de module met het beoordelingshistogram wordt een beoordelingshistogram weergegeven. Deze module wordt meestal weergegeven tussen de module Schrijf een recensie en de module met de productrecensielijst op een PDP-pagina.

Voor de module met het beoordelingshistogram is geen configuratie vereist. U hoeft de module alleen aan de PDP-sjabloon toe te voegen. 

De volgende illustraties laten zien hoe een PDP-sjabloon eruitziet in Dynamics 365 Commerce wanneer de modules voor beoordelingen en recensies zijn geconfigureerd voor weergave op productbeschrijvingen.

![PDP-sjabloon wanneer beoordelingen en recensies zijn geconfigureerd voor weergave in productbeschrijvingen](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Module met productrecensie

In de module met productrecensies wordt een lijst met productrecensies weergegeven met opties voor sorteren, filteren en paginering. Deze module wordt normaal gesproken weergegeven na de module met het beoordelingshistogram.

In de volgende tabel worden de eigenschappen van de module voor productrecensielijsten weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.

| Naam van eigenschap.              | Waarde | Beschrijving eigenschap |
|----------------------------|-------| ---------------------|
| Recensies die op elke pagina worden weergegeven | 10    | Het aantal recensies dat tegelijk op een PDP moet worden weergegeven. De knoppen **Volgende** en **Vorige** zijn opgenomen, zodat gebruikers door de pagina's met recensies kunnen navigeren. |

#### <a name="ratings-histogram--summary-view"></a>Beoordelingshistogram – overzichtsweergave

De module met de productrecensielijst bevat een vak waarin u een beoordelingshistogrammodule kunt toevoegen. In de volgende afbeelding ziet u hoe u een beoordelingshistogrammodule in de module met de productrecensielijst kunt toevoegen in Dynamics 365 Commerce.

![Een beoordelingshistogrammodule toevoegen aan de module met de productrecensielijst](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Een site met beoordelingen en recensies configureren

Configuratiewaarden voor beoordelingen en recensies, zoals de tenant-id, de lengte van de recensietekst en de lengte van de recensietitel worden op siteniveau geconfigureerd. 

Voer de volgende stappen uit om een site te configureren voor het weergeven van beoordelingen en recensies. 

1. Ga naar **Startpagina \> Sites**.
1. Selecteer de naam van uw site. 
1. Ga naar **Sitebeheer \> Uitbreidbaarheid**. 
1. Voer in het veld **Maximale lengte recensietekst** het maximumaantal tekens in dat de recensietekst kan bevatten (bijvoorbeeld **1000**). 
1. Voer in het veld **Maximale lengte recensietitel** het maximumaantal tekens in dat de recensietitel kan bevatten (bijvoorbeeld **55**). 
1. Selecteer **Opslaan en publiceren**. 

In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.

![Een site met beoordelingen en recensies configureren](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Een productbeoordeling koppelen aan de sectie Recensies van een PDP

Een productbeoordeling wordt onder de producttitel boven aan de PDP weergegeven. De productbeoordeling kan zo worden geconfigureerd dat deze wordt gekoppeld aan de sectie **Recensies** van dezelfde PDP. 

Voer de volgende stappen uit om een productbeoordeling te koppelen aan de sectie **Recensies** van de PDP.

1. Open de PDP-sjabloon. 
1. Ga naar **Instellingen van module voor koopvakcontainer**.
1. Selecteer onder **Koopvak** de optie **Productbeoordelingen** en schakel vervolgens het selectievakje **Klikken koppelen aan module met volledige recensies** in.

In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.

![Een productbeoordeling koppelen aan de sectie Recensies van een PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>De koppeling naar de pagina Privacy en beleid configureren

Volg deze stappen om de koppeling naar de pagina Privacy en beleid te configureren

1. Ga naar **Startpagina \> Sites**.
1. Selecteer de naam van uw site. 
1. Ga naar **Sitebeheer \> Uitbreidbaarheid**
1. Selecteer op het tabblad **Routes** onder **RNR privacy en beleid** de optie **Een koppeling toevoegen**. Als er al een koppeling is ingevoerd en u deze wilt vervangen, selecteert u de koppeling. 
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** de koppeling voor de pagina Privacy en beleid en selecteer vervolgens **OK.** 
1. Selecteer **Opslaan en publiceren**. 

In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.

![De koppeling naar de pagina Privacy en beleid configureren](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Productbeoordelingen synchroniseren in Dynamics 365 Retail](sync-product-ratings.md)
