---
title: Functies in Human resources beheren
description: Informatie over het in- of uitschakelen van nieuwe functies in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9454125428a0bb9b8d60d8e1733f7e56144d4a3e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058531"
---
# <a name="manage-features-in-human-resources"></a>Functies in Human resources beheren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Als onderdeel van onze doorlopende implementatie van nieuwe mogelijkheden voor Microsoft Dynamics 365 Human Resources willen we klanten zo snel mogelijk laten kennismaken met nieuwe functies. We bieden previews-functies die bijna gereed zijn voor algemene beschikbaarheid en die uitgebreid zijn getest. Het enige wat we nog willen doen is een definitieve ronde van feedback van klanten en validatie voordat we de functies algemeen vrijgeven.

Ga voor meer informatie over nieuwe functies in Human Resources naar [Nieuw in Human Resources](hr-admin-whats-new.md) en [Releaseplan voor Dynamics 365 en Power Platform](/dynamics365/release-plans/?panel=products1#pivot=products).

Het werkgebied **Functiebeheer** bevat een lijst met functies die in elke versie worden geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven. Zie [Overzicht Functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)voor meer informatie over Functiebeheer.

Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus. De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode. Zodra u nieuwe functies in het werkgebied **Functiebeheer** ziet, kunt u deze inschakelen. Sommige functies zijn mogelijk standaard ingeschakeld.

Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen. Het werkgebied **Functiebeheer** geeft aan wanneer een preview-functie verplicht wordt. Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen. U kunt verplichte functies niet uitschakelen. Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.

## <a name="enable-or-disable-preview-features"></a>Preview-functies in- of uitschakelen

Als u toegang tot preview-functies wilt hebben, moet u deze eerst in uw omgeving inschakelen. Het in- of uitschakelen van voorbeeldfuncties is omgevingsspecifiek.

> [!IMPORTANT]
> Preview-functies zijn alleen beschikbaar in **Sandbox**-omgevingen. Als u een preview-functie inschakelt, schakelt u deze in voor alle gebruikers in uw organisatie die zich in die omgeving bevinden. Als u de preview-functie uitschakelt, wordt deze ontoegankelijk voor uw gebruikers. Preview-functies hebben beperkte ondersteuning in Human Resources. Ze gebruiken mogelijk minder privacy- en beveiligingsmaatregelen en zijn niet opgenomen in de serviceovereenkomst voor Human Resources. U moet de voorbeeldfuncties niet gebruiken voor de verwerking van persoonsgegevens (dat wil zeggen informatie die uw identiteit aangeeft) of andere gegevens die onderworpen zijn aan wettelijke of bestuursrechtelijke conformiteitsvereisten.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer de tegel **Functiebeheer**.

3. Als u een preview-functie wilt inschakelen, selecteert u deze in de lijst en selecteert u **Inschakelen**. Als u een preview-functie wilt uitschakelen, selecteert u deze in de lijst en selecteert u **Uitschakelen**.

## <a name="enable-or-disable-benefits-management"></a>Vergoedingenbeheer in- of uitschakelen

Als u Vergoedingenbeheer wilt inschakelen, gebruikt u dezelfde procedure als in [Het in- of uitschakelen van preview-functies](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Nadat u Vergoedingenbeheer in een **productie** omgeving hebt ingeschakeld, kunt u dit niet meer uitschakelen. U kunt Vergoedingenbeheer echter wel uitschakelen in **sandbox**-omgevingen.

Zie het [overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie over de configuratie en het gebruik van Vergoedingenbeheer.

Vergoedingenbeheer vervangt functionaliteit in het werkgebied **Vergoedingen**. Wanneer u de preview-functie van Vergoedingenbeheer inschakelt, kunt u de volgende formulieren niet meer openen in het werkgebied **Vergoedingen**:

- **Vergoedingen**
- **Vergoedingselementen**
- **Tarieven bijdrageberekening**
- **Resultaten inschrijving op vergoedingen**
- **Resultaten van vergoedingen laten vervallen en verlengen**
- **Regeltypen van beleid om in aanmerking te komen voor een vergoeding**
- **Beleid inzake geschiktheid voor vergoedingen**
- **Geschiktheidsgebeurtenissen**

U kunt de informatie in deze formulieren in de alleen-lezenmodus weergeven. Als u de gegevens wilt bewerken, moet u eerst de functie voor Vergoedingenbeheer uitschakelen (alleen van toepassing op **sandbox**-omgevingen).

## <a name="enable-or-disable-leave-and-absence"></a>Verlof en verzuim in- of uitschakelen

Als u Verlof en verzuim wilt inschakelen, gebruikt u dezelfde procedure als in [Het in- of uitschakelen van preview-functies](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> U kunt de functie **Meerdere verloftypen** niet uitschakelen in Verlof en verzuim nadat u deze hebt ingeschakeld. Dit geldt voor zowel **sandbox**- als **productie** omgevingen.

Meer informatie over preview-functies voor verlof en verzuim vindt u in [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Feedback verzenden

Wij horen graag over uw ervaringen met deze preview-functies. We raden u aan uw feedback regelmatig op de volgende websites te plaatsen wanneer u deze of andere functies gebruikt:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) : deze site is een goede bron waar gebruikers gebruikstoepassingen kunnen bespreken, vragen kunnen stellen en hulp van de community kunnen krijgen.
- Laat ons weten welke functies u wilt zien in het product en ook eventuele wijzigingen die volgens u in de bestaande functies moeten worden aangebracht. Ideeën voor producten op [Human Resources-ideeën](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Let op: vermeld geen persoonlijke gegevens (gegevens die uw identiteit vrijgeven) als u feedback of een productbeoordeling indient. Verzamelde gegevens worden mogelijk verder geanalyseerd en worden niet gebruikt om verzoeken te beantwoorden krachtens van toepassing zijnde privacywetgeving. Persoonlijke gegevens die afzonderlijk voor deze programma's worden verzameld, zijn onderworpen aan de [privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Zie ook

- [Nieuw in Human Resources](hr-admin-whats-new.md)
- [Releaseplan voor Dynamics 365 en Power Platform](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]