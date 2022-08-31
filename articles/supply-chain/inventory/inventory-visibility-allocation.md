---
title: Voorraadtoewijzing Inventory Visibility
description: In dit artikel wordt uitgelegd hoe u de voorraadtoewijzingsfunctie kunt instellen en gebruiken. Met deze functie kunt u speciale voorraad apart zetten om ervoor te zorgen dat u uw meest winstgevende kanalen of klanten kunt bedienen.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: f79497a24a5b4dd501bb0d13d9eaca7e98672533
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306109"
---
# <a name="inventory-visibility-inventory-allocation"></a>Voorraadtoewijzing voor voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Zakelijke achtergrond en doel

In veel gevallen moeten fabrikanten, detailhandelaren en andere bedrijfseigenaren in de keten van leveranciers vooraf voorraad toewijzen voor belangrijke verkoopkanalen, locaties of klanten of voor specifieke verkoopgebeurtenissen. Voorraadtoewijzing is een normale praktijk in het operationele planningsproces van de verkoop, en wordt uitgevoerd voordat de werkelijke verkoopactiviteiten plaatsvinden en er een verkooporder wordt gemaakt.

Een bedrijf dat fietsen verkoopt heeft bijvoorbeeld beperkte voorraad voor een zeer populaire fiets. Dit bedrijf verkoopt zowel online als in de winkel. In elk verkoopkanaal heeft het bedrijf enkele belangrijke bedrijfspartners (markten en grote detailhandelaren) die eisen dat een specifiek deel van de beschikbare voorraad van de fiets voor hen wordt bewaard. Het fietsbedrijf moet dus in staat zijn voorraaddistributie over kanalen te verdelen en ook de verwachtingen van de VIP-partners te beheren. De beste manier om beide doelen te behalen is door voorraadtoewijzing te gebruiken, zodat elk kanaal en elke detailhandelaar specifieke toegewezen hoeveelheden kunnen ontvangen die later aan consumenten kunnen worden verkocht.

Voorraadtoewijzing heeft twee basisbedrijfsdoeleinden:

- **Voorraadbeveiliging (ringfencing)**: organisaties willen beperkte voorraad vooraf toewijzen aan kanalen, regio's, VIP-klanten en dochtermaatschappijen met prioriteit. De toewijzingsfunctie Voorraadzichtbaarheid is erop gericht de toegewezen voorraad te beschermen zodat de andere toewijzingen, reserveringen of andere verkoopvraag geen invloed hebben op de eerder toegewezen voorraad.
- **Voorkomen dat er te veel wordt verkocht**: de toewijzingsfunctie Voorraadzichtbaarheid is erop gericht een beperking te leggen op de eerder toegewezen hoeveelheden, zodat de ontvangende partij (bijvoorbeeld een kanaal of klantengroep) deze hoeveelheden niet te veel verbruikt wanneer de werkelijke op een zachte reservering gebaseerde verkooptransactie van kracht wordt.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Toewijzingsdefinitie in de service voor voorraadzichtbaarheid

Hoewel met de toewijzingsfunctie in de service voor voorraadzichtbaarheid geen fysieke voorraadhoeveelheden apart worden gezet, verwijst de toewijzing wel naar beschikbare fysieke voorraadhoeveelheid om de oorspronkelijke voor *toewijzing beschikbare* virtuele poolhoeveelheid te definiëren. Voorraadtoewijzing in voorraadzichtbaarheid is een zachte toewijzing. Het vindt plaats voordat er werkelijke verkooptransacties plaatsvinden en is niet afhankelijk van verkooporders. U kunt bijvoorbeeld voorraad toewijzen aan uw belangrijkste verkoopkanalen of aan grote detailhandelaren voordat eindgebruikers het verkoopkanaal of de detailhandelswinkel bezoeken om hoeveelheden te kopen.

Het verschil tussen voorraadtoewijzing en [zachte reservering van voorraad](inventory-visibility-reservations.md) is dat zachte reservering meestal wordt gekoppeld aan werkelijke verkooptransacties (verkooporderregels). Als u de toewijzingsfunctie en de functie voor zachte reservering samen wilt gebruiken, is het raadzaam eerst voorraadtoewijzing uit te voeren en vervolgens een zachte reservering te maken voor de toegewezen hoeveelheden. Zie [Verbruiken als een zachte reservering](#consume-to-soft-reserved) voor meer informatie.

Met de functie voor voorraadtoewijzing kunnen verkoopplanners of belangrijke accountmanagers belangrijke voorraad beheren en vooraf toewijzen aan toewijzingsgroepen (zoals kanalen, regio's en klantengroepen). De functie ondersteunt ook realtime tracering, correctie en analyse van verbruik op basis van toegewezen hoeveelheden, zodat aanvulling of hertoewijzing op tijd kan worden uitgevoerd. Deze mogelijkheid om realtime zichtbaarheid te hebben in het toewijzings- en verbruikssaldo is met name belangrijk bij snelle verkoop of promotiegebeurtenissen.

## <a name="terminology"></a>Terminologie

De volgende termen en concepten zijn nuttig bij besprekingen over voorraadtoewijzing:

- **Toewijzingsgroep**: de groep die eigenaar is van de toewijzing, zoals een verkoopkanaal, klantengroep of ordertype.
- **Waarde toewijzingsgroep**: de waarde van elke toewijzingsgroep. *Web* of *winkel* kan bijvoorbeeld de waarde van de toewijzingsgroep voor het verkoopkanaal zijn, terwijl *VIP* of *normaal* de waarde van de klanttoewijzingsgroep is.
- **Toewijzingshiërarchie**: een middel om toewijzingsgroepen op een hiërarchische manier te combineren. U kunt bijvoorbeeld *kanaal* definiëren als hiërarchieniveau 1, *regio* als niveau 2 en *klantengroep* als niveau 3. Tijdens de voorraadtoewijzing moet u de toewijzingshiërarchievolgorde volgen wanneer u de waarde van de toewijzingsgroep opgeeft. U kunt bijvoorbeeld 200 rode fietsen toewijzen aan kanaal *Web*, regio *Londen* en klantengroep *VIP*.
- **Beschikbaar voor toewijzing**: de *virtuele gemeenschappelijke pool* die de hoeveelheid aangeeft die beschikbaar is voor verdere toewijzing. Het is een berekende meting die u met behulp van uw eigen formule kunt definiëren. Als u ook de functie voor zachte reservering gebruikt, raden we u aan dezelfde formule te gebruiken voor het berekenen van de hoeveelheid die beschikbaar is voor toewijzing en de hoeveelheid die beschikbaar is voor reservering.
- **Toegewezen:** een fysieke meting waarmee het toegewezen quotum wordt weergegeven dat kan worden verbruikt door de toewijzingsgroepen.
- **Verbruikt:** een fysieke meting waarmee hoeveelheden worden aangegeven die zijn verbruikt ten opzichte van de oorspronkelijk toegewezen hoeveelheid. Wanneer er nummers aan deze fysieke meting worden toegevoegd, wordt de toegewezen fysieke meting automatisch verlaagd.

In de volgende afbeelding ziet u de bedrijfswerkstroom voor voorraadtoewijzing.

![Bedrijfswerkstroom toewijzing voorraadzichtbaarheid.](media/inventory-visibility-allocation-flow.png "Bedrijfswerkstroom toewijzing voorraadzichtbaarheid.")

## <a name="set-up-inventory-allocation"></a>Voorraadtoewijzing instellen

De voorraadtoewijzingsfunctie bestaat uit de volgende onderdelen:

- De vooraf gedefinieerde, toewijzingsgerelateerde gegevensbron, fysieke metingen en berekende metingen.
- Aanpasbare toewijzingsgroepen met maximaal acht niveaus.
- Een set API´s (Application Programming Interfaces) voor toewijzing:
  - allocate
  - reallocate
  - unallocate
  - consume
  - query

Het proces van het configureren van de toewijzingsfunctie heeft twee stappen:

- De [gegevensbron](inventory-visibility-configuration.md#data-source-configuration) en de bijbehorende [metingen](inventory-visibility-configuration.md#data-source-configuration-physical-measures) instellen.
- De naam en hiërarchie van de toewijzingsgroep instellen.

### <a name="predefined-data-source"></a>Vooraf gedefinieerde gegevensbron

Wanneer u de toewijzingsfunctie inschakelt en de API voor het bijwerken van de configuratie aanroept, wordt door Voorraadzichtbaarheid één vooraf gedefinieerde gegevensbron en verschillende initiële metingen gemaakt.

De gegevensbron heeft de naam `@iv`.

Dit zijn de eerste fysieke metingen:

- `@iv`
  - `@allocated`
  - `@cumulative_allocated`
  - `@consumed`
  - `@cumulative_consumed`

Dit zijn de eerste berekende metingen:

- `@iv`
  - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Andere fysieke metingen toevoegen aan de berekende meting beschikbaar voor toewijzing

Als u gebruik wilt maken van de toewijzing, moet u de berekende meting beschikbaar voor toewijzing (`@iv.@available_to_allocate`) instellen. U hebt bijvoorbeeld gegevensbron `fno` en meting `onordered`, gegevensbron `pos` en meting `inbound` en u wilt toewijzing uitvoeren op de voorhanden voorraad voor de som van `fno.onordered` en `pos.inbound` In dit geval moet `@iv.@available_to_allocate` `pos.inbound` en `fno.onordered` in de formule bevatten. Dit is een voorbeeld:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Gegevensbron `@iv` is een vooraf gedefinieerde gegevensbron en de fysieke metingen die in `@iv` met prefix `@` worden gedefinieerd, zijn vooraf gedefinieerde metingen. Deze metingen zijn vooraf gedefinieerde configuraties voor de toewijzingsfunctie. U hoeft deze dus niet te wijzigen of te verwijderen omdat er onverwachte fouten optreden wanneer u de toewijzingsfunctie gebruikt.
>
> U kunt nieuwe fysieke metingen toevoegen aan de vooraf gedefinieerde meting `@iv.@available_to_allocate`, maar u moet de naam niet wijzigen.

### <a name="change-the-allocation-group-name"></a>De naam van de toewijzingsgroep wijzigen

Er kunnen maximaal acht toewijzingsgroepsnamen worden ingesteld. De groepen hebben een hiërarchie.

U stelt de groepsnamen op de pagina **Configuratie Power App Voorraadzichtbaarheid** in. Als u deze pagina wilt openen, opent u in uw Microsoft Dataverse-omgeving de app Voorraadzichtbaarheid en selecteert u **Configuratie \> Toewijzing**.

Als u bijvoorbeeld vier groepsnamen gebruikt en deze instelt op \[`channel`, `customerGroup`, `region`, `orderType`\], zijn deze namen geldig voor toewijzingsgerelateerde aanvragen wanneer u de API voor het bijwerken van configuraties oproept.

### <a name="allocation-using-tips"></a>Toewijzing met tips

- Voor elk product moet de toewijzingsfunctie op hetzelfde *dimensieniveau* worden gebruikt volgens de productindexhiërarchie die u in de [productindexhiërarchieconfiguratie](inventory-visibility-configuration.md#index-configuration) hebt ingesteld. Stel bijvoorbeeld dat uw indexhiërarchie \[`Site`, `Location`, `Color`, `Size`\] is. Als u een bepaalde hoeveelheid voor één product toewijst op het niveau \[`Site`, `Location`, `Color`\], moet u bij een volgende toewijzing van dit product toewijzen op hetzelfde niveau (\[`Site`, `Location`, `Color`\]). Als u het niveau \[`Site`, `Location`, `Color`, `Size`\] of \[`Site`, `Location`\] gebruikt, worden de gegevens inconsistent.
- Het wijzigen van de naam van de toewijzingsgroep heeft geen invloed op de gegevens die in de service zijn opgeslagen.
- De toewijzing moet plaatsvinden als het product de positieve voorhanden hoeveelheid heeft.
- Als u producten van een groep met een *hoog toewijzingsniveau* aan een subgroep wilt toewijzen, gebruikt u de `Reallocate`-API. Als u een toewijzingsgroepshiërarchie \[`channel`, `customerGroup`, `region`, `orderType`\] hebt en een product uit de toewijzingsgroep \[Online, VIP\] wilt toewijzen aan de subtoewijzingsgroep \[Online, VIP, EU\], gebruikt u de `Reallocate`-API om de hoeveelheid te verplaatsen. Als u de `Allocate`-API gebruikt, wordt de hoeveelheid toegewezen vanuit de virtuele gemeenschappelijke pool.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a>De toewijzings-API gebruiken

Er zijn momenteel vijf toewijzings-API's geopend:

- POST /api/environment/{environmentId}/allocation/allocate
- POST /api/environment/{environmentId}/allocation/unallocate
- POST /api/environment/{environmentId}/allocation/reallocate
- POST /api/environment/{environmentId}/allocation/consume
- POST /api/environment/{environmentId}/allocation/query

#### <a name="allocate"></a>Toewijzen

Roep de API `Allocate` aan om een product met specifieke dimensies toe te wijzen. Hier is het schema voor de aanvraagtekst.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

U wilt bijvoorbeeld een hoeveelheid van tien toewijzen voor product *Fiets*, site *1*, locatie *11*, kleur *rood*, kanaal *Online*, klantengroep *VIP* en regio *VS*. Om deze toewijzing uit te voeren, kunt u een aanroep doen met de volgende inhoud.

```json
{
    "id": "???",
    "productId": "Bike",
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

De hoeveelheid moet altijd groter zijn dan 0 (nul).

#### <a name="unallocate"></a>Unallocate

Gebruik de API `Unallocate` om de bewerking `Allocate` terug te draaien. Negatieve hoeveelheid is niet toegestaan in een `Allocate`-bewerking. De tekst van `Unallocate` is identiek aan de tekst van `Allocate`.

#### <a name="reallocate"></a>Reallocate

Gebruik de API `Reallocate` om een bepaalde toegewezen hoeveelheid naar een andere groepscombinatie te verplaatsen. Hier is het schema voor de aanvraagtekst.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

U kunt bijvoorbeeld twee fietsen met de dimensies \[site=1, locatie=11, kleur=rood\] verplaatsen van toewijzingsgroep \[Online, VIP, VS\] naar toewijzingsgroep \[Online, VIP, EU\] door de API `Reallocate` aan te roepen en de volgende tekst te verschaffen.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

#### <a name="consume"></a>Verbruiken

Gebruik de API `Consume` om de verbruikshoeveelheid voor toewijzing te boeken. U kunt deze API bijvoorbeeld gebruiken om toegewezen hoeveelheden te verplaatsen naar enkele werkelijke metingen. Hier is het schema voor de aanvraagtekst.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Er zijn bijvoorbeeld acht toegewezen fietsen met de dimensies \[site=1, locatie=11, kleur=rood\] voor toewijzingsgroep \[Online, VIP, VS\]. De volgende formule beschikbaar voor toewijzing wordt gebruikt:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

De acht fietsen worden toegewezen via meting `pos.inbound`.

Nu worden drie fietsen verkocht en uit de toewijzingspool genomen. Als u deze verplaatsing wilt registreren, kunt u een aanroep doen met de volgende aanvraagtekst.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Na deze aanroep wordt de toegewezen hoeveelheid voor het product verminderd met 3. Bovendien wordt door Voorraadzichtbaarheid een gebeurtenis voor het wijzigen van de voorhanden voorraad gegenereerd waarbij `pos.inbound` = *-3*. U kunt de waarde `pos.inbound` ook ongewijzigd laten en alleen de toegewezen hoeveelheid verbruiken. In dit geval moet u echter een andere fysieke meting maken om de verbruikte hoeveelheden te behouden of de vooraf gedefinieerde meting `@iv.@consumed` te gebruiken.

In deze aanvraag moet het tegenovergestelde modificatortype (Optellen of Aftrekken) worden gebruikt voor de fysieke meting die u in de verbruikstekst gebruikt, vergeleken met het modificatortype dat in de berekende meting is gebruikt. In deze verbruikstekst heeft `iv.inbound` dus de waarde `Subtraction` en niet `Addition`.

De gegevensbron `fno` kan niet in de verbruikstekst worden gebruikt, omdat we altijd hebben gesteld dat voorraadzichtbaarheid geen gegevens voor de gegevensbron `fno` kan wijzigen. De gegevensstroom verloopt in één richting, wat betekent dat alle hoeveelheidswijzigingen voor de gegevensbron `fno` afkomstig moeten zijn uit uw Supply Chain Management-omgeving.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Verbruiken als een zachte reservering

De API `Consume` kan de toegewezen hoeveelheid ook als een zachte reservering verbruiken. In dit geval wordt de toegewezen hoeveelheid met de `Consume`-bewerking verminderd en wordt vervolgens een zachte reservering voor die hoeveelheid gemaakt. Als u deze methode wilt gebruiken, moet u ook de functie voor [zachte reservering](inventory-visibility-reservations.md) van Voorraadzichtbaarheid gebruiken.

U hebt bijvoorbeeld een modificator voor zachte reservering (meting) ingesteld op `iv.softreserved`. De volgende formule wordt gebruikt voor de berekende meting die beschikbaar voor reservering is:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Als u deze instelling wilt gebruiken met de toewijzingsfunctie, voegt u `@iv.@allocated` aan `iv.available_to_reserve` toe om de volgende formule te produceren:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Wijzig vervolgens `@iv.@available_to_allocate` in dezelfde waarde.

Als u een hoeveelheid van 3 wilt verbruiken en deze hoeveelheid direct wilt reserveren, kunt u een aanroep doen met de volgende aanvraagtekst.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

In deze aanvraag heeft `iv.softreserved` de waarde `Addition` en niet `Subtraction`.

#### <a name="query"></a>Vraag

Gebruik de `Query`-API om toewijzingsgerelateerde informatie voor bepaalde producten op te halen. U kunt dimensiefilters en toewijzingsgroepsfilters gebruiken om de resultaten te beperken. De dimensies moeten exact overeenkomen met de dimensie die u wilt ophalen, bijvoorbeeld \[site=1, locatie=11\] heeft niet-gerelateerde resultaten vergeleken met \[site=1, locatie=11, kleur=rood\].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Gebruik bijvoorbeeld \[site=1, locatie=11, kleur=rood\] en lege groepsvelden om alle toewijzingsrecords op te halen:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Gebruik \[site=1, locatie=11, kleur=rood\] en groepen \[kanaal=Online, klantengroep=VIP, regio=VS\] om toewijzingsrecords voor deze groep op te halen:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
