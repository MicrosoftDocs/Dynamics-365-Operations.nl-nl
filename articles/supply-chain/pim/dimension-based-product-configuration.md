---
title: Overzicht van Op dimensies gebaseerde productconfiguraties
description: Een op dimensies gebaseerde productconfiguratie vertegenwoordigt een eenvoudige oplossing voor het maken van veel productvarianten op basis van één productmodel en de bijbehorende stuklijst.
author: cvocph
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 604b9e14d7a218ab75ebeff5b686f380ef88b34e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354684"
---
# <a name="dimension-based-product-configuration-overview"></a>Overzicht van Op dimensies gebaseerde productconfiguraties

[!include [banner](../includes/banner.md)]

Een op dimensies gebaseerde productconfiguratie vertegenwoordigt een eenvoudige oplossing voor het maken van veel productvarianten op basis van één productmodel en de bijbehorende stuklijst.

De op dimensies gebaseerde productconfiguratie is een van de drie ingebouwde productconfiguratietechnologieën. De twee andere technologieën zijn vooraf gedefinieerde varianten en vormen een op beperkingen gebaseerde configuratie. In alle drie de technologieën wordt een productmodel gebruikt als beginpunt en de technologieën bieden gebruikers de mogelijkheid om vele productvarianten voor één productmodel te maken.

## <a name="key-concepts"></a>Belangrijke concepten
De op dimensies gebaseerde productconfiguratie is gebaseerd op de volgende belangrijke concepten:

-   Productmodellen
-   Configuratieproductdimensie
-   Configuratiegroepen
-   Stuklijst
-   Configuratieroute
-   Configuratieregels

### <a name="product-masters"></a>Productmodellen

Een productmodel is het beginpunt voor elk productconfiguratieproces. Voor op dimensies gebaseerde productconfiguratie hebt u een productmodel nodig met deze specifieke configuratietechnologie en een productdimensiegroep die de configuratieproductdimensie bevat.

### <a name="configuration-product-dimension"></a>Configuratieproductdimensie

De configuratieproductdimensie wordt gebruikt om de productvarianten te identificeren voor een productmodel met de op dimensies gebaseerde configuratietechnologie. De waarde van de configuratiedimensie wordt ingevoerd door de gebruiker en moet helpen om de afzonderlijke productvarianten te identificeren.

### <a name="configuration-groups"></a>Configuratiegroepen

Configuratiegroepen worden gedefinieerd in een centrale opslagplaats en kunnen alle voor op dimensies gebaseerde productconfiguratiemodellen worden gebruikt. Configuratiegroepen worden gekoppeld aan de afzonderlijke stuklijstregels en houden een groep regels bij elkaar die elkaar wederzijds uitsluiten. Dit betekent dat slechts één regel in een groep voor één productvariant kan worden geselecteerd.

### <a name="bill-of-materials-bom"></a>Stuklijst

De stuklijst vertegenwoordigt de bouwstenen voor op dimensies gebaseerde productconfiguratie. De stuklijst moet alle andere producten bevatten die in elke productvariant kunnen worden gebruikt. Elke regel in de stuklijst kan naar een configuratiegroep verwijzen. Als een regel niet naar een configuratiegroep verwijst, wordt deze in alle productvarianten opgenomen.

### <a name="configuration-route"></a>Configuratieroute

De configuratieroute bepaalt de volgorde van de configuratiegroepen, zoals deze tijdens het productconfiguratieproces voor de gebruiker worden weergegeven.

### <a name="configuration-rules"></a>Configuratieregels

De configuratieregels vormen een mechanisme om ervoor te zorgen dat een product dat in één configuratiegroep in een stuklijst is opgenomen, opname of uitsluiting van een product in een andere configuratiegroep in dezelfde stuklijst afdwingt.

## <a name="product-modeling-process"></a>Productmodelleringsproces
De natuurlijke volgorde voor het bouwen van een productmodel voor een op dimensies gebaseerd product begint met het definiëren van de relevante configuratiegroepen. Het is belangrijk ervoor te zorgen dat alle producten die in de stuklijst worden gebruikt, zijn vrijgegeven aan het bedrijf waarvoor het productmodel is gebouwd. Met deze bouwstenen kan de gebruiker de stuklijst maken en configuratiegroepen toewijzen aan alle relevante stuklijstregels. Wanneer de stuklijst is voltooid, kan een configuratieroute voor het bestellen van de configuratiegroepen in de juiste volgorde worden gedefinieerd. [![Op dimensies gebaseerd productmodelproces.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Als er bepaalde producten van verschillende configuratiegroepen zijn die niet of wel samen moeten worden gebruikt, kunt u configuratieregels maken waarmee deze productrelaties worden afgedwongen. Nadat de stuklijst is gekoppeld aan een op dimensies gebaseerd productmodel via een stuklijstversie en beide zijn goedgekeurd en geactiveerd, kunt u productconfiguraties maken en een naam voor elke configuratie invoeren. De configuraties kunnen worden gedefinieerd voordat eventuele transacties worden gegenereerd of in geval de behoefte aan een bepaalde configuratie ontstaat.

### <a name="suggested-use"></a>Voorgesteld gebruik

De op dimensies gebaseerde configuratietechnologie is het meest geschikt voor producten met beperkte veranderlijkheid en de combinatie van de grootte, kleur, stijl en configuratie van de standaardproductdimensies niet geschikt is voor het identificeren van een specifieke productvariant. Een voorbeeld is een fiets met framehoogte, wielformaat, remtypen en verschillende versnellingen.

### <a name="next-step"></a>Volgende stap 

De volgende acht taakbegeleiders worden vermeld in de volgorde waarin u ze moet voltooien. 

1.  [Een op dimensies gebaseerd productmodel maken](tasks/create-dimension-based-product-master.md)
2.  [Een op dimensies gebaseerd productmodel vrijgeven](tasks/release-dimension-based-product-master.md)
3.  [Basisinstellingen voor een vrijgegeven productmodel voltooien](tasks/complete-basic-setup-released-product-master.md)
4.  [Configuratiegroepen definiëren](tasks/define-configuration-groups.md)
5.  [Een stuklijst maken voor een op dimensies gebaseerd productmodel](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Configuratieroutes definiëren](tasks/define-configuration-route.md)
7.  [Configuratieregels maken](tasks/create-configuration-rules.md)
8.  [Op dimensies gebaseerde configuraties maken](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]