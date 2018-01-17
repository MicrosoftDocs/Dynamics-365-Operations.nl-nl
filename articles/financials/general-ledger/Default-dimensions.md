---
title: "Financiële dimensies en boeken"
description: Wanneer u een rekeningschema plant en instelt, moet u overwegen hoe de verschillende onderdelen samenwerken bij het boeken van een document of journaal. Deze onderdelen omvatten rekeningstructuren, geavanceerde regels, en salderende en vaste dimensies. In dit onderwerp wordt uitgelegd wat elk onderdeel is en hoe de onderdelen samenwerken.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fa494ab9c3b3f0540ec042f952344c15796845e6
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="financial-dimensions-and-posting"></a>Financiële dimensies en boeken 

[!include[banner](../includes/banner.md)]

Wanneer u een rekeningschema plant en instelt, moet u overwegen hoe de verschillende onderdelen samenwerken bij het boeken van een document of journaal. Deze onderdelen omvatten rekeningstructuren, geavanceerde regels, en salderende en vaste dimensies. In dit onderwerp wordt uitgelegd wat elk onderdeel is en hoe de onderdelen samenwerken.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Rekeningschema en onderdelen van financiële dimensie

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition bevat een uitgebreid, op regels gebaseerd systeem om geldige combinaties van hoofdrekeningen en financiële dimensiewaarden te definiëren. Deze sectie bevat een kort overzicht van de functionaliteit van elk onderdeel en uitlegt waar u het onderdeel kunt vinden.

### <a name="account-structures"></a>Rekeningstructuren

Een rekeningstructuur is vereist bij het instellen van uw grootboek. U moet ten minste één rekeningstructuur definiëren en activeren en deze toewijzen aan het grootboek. De rekeningstructuur moet de hoofdrekening bevatten. Definieer de volgorde van de segmenten die het beste past bij uw bedrijf. Nadat de hoofdrekening is gedefinieerd, kan het systeem de rekeningstructuur bepalen die wordt gebruikt. Door de hoofdrekening eerst of bij het begin van een structuur te plaatsen, kunt u de grenswaarden bepalen en zorgen dat het systeem de laatste bekende geldige waarde als standaardwaarde toepast. U kunt maximaal 10 extra financiële dimensies hebben in de rekeningstructuur. De rekeningstructuur bepaalt welke dimensiewaarden in combinatie met andere waarden geldig zijn. Tevens definieert de structuur of dimensiewaarden moeten worden ingevoerd.

### <a name="advanced-rules"></a>Geavanceerde regels

Geavanceerde regels zijn een optioneel onderdeel bij het instellen van het rekeningschema. U kunt zo veel geavanceerde regels aan een rekeningstructuur toevoegen als u wilt. Geavanceerde regels worden vaak gebruikt voor het verwerken van scenario's waarin extra financiële dimensies moeten worden bijgehouden als aan specifieke criteria wordt voldaan. Als u bijvoorbeeld een reisonkostenrekening gebruikt, wilt u mogelijk extra informatie bijhouden, zoals het evenement dat door de werknemer wordt bezocht. Als er meerdere geavanceerde regels zijn, worden deze in alfabetische volgorde toegepast, op basis van de namen van de regels. De segmenten die door een regel worden toegevoegd, kunnen alleen worden toegepast na de segmenten van de rekeningstructuur.

### <a name="balancing-dimension"></a>Salderende dimensie

U kunt desgewenst een salderende financiële dimensie definiëren. Op de pagina **Grootboek** kunt u de financiële dimensie definiëren die moet salderen. Wanneer vervolgens transacties worden geboekt naar die financiële dimensie, worden door het systeem automatisch posten gemaakt en geboekt zodat de financiële dimensie in evenwicht is.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Standaard/vaste financiële dimensies voor de hoofdrekening

Standaarddimensies zijn afkomstig uit verschillende locaties, zoals stamrecords (bijvoorbeeld klant- of leverancierrecords), kopteksten in documenten en de hoofdrekening. In dit onderwerp komen standaarddimensies voor de hoofdrekening per rechtspersoon aan de orde. U kunt definiëren of een hoofdrekening heeft de waarde **Niet vast** of **Vast** heeft voor elke financiële dimensie die wordt gebruikt in alle rekeningstructuren voor het grootboek. Als een financiële dimensie **Niet vast** is, wordt een standaardwaarde gebruikt die kan worden overschreven. Dit probleem geldt voor alle standaardwaarden in het systeem, zelfs standaardwaarden die afkomstig zijn uit stamrecords. Als een financiële dimensie is ingesteld op de waarde **Vast**, wordt die waarde altijd toegepast, ongeacht of deze afkomstig is uit een standaardwaarde of is opgegeven door de gebruiker.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Volgorde waarin standaarddimensies worden toegepast tijdens het boeken

Gebruikers hebben vaak vragen over de volgorde waarin de verschillende onderdelen worden uitgevoerd. Het is belangrijk dat u de volgorde weet waarin standaarddimensies worden toegepast, omdat dit van invloed is op de aanpak bij het instellen.

> [!NOTE]
> Deze informatie geldt alleen voor het gebruik van standaarddimensies in de toepassing. Als u gegevens importeert met behulp van Microsoft Excel of het Data Management Framework, is het gedrag anders.

### <a name="example-1"></a>Voorbeeld 1

**Rekeningstructuur**

| Hoofdrekening            | Bedrijfseenheid           | Departement              | Kostenplaats             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Alle waarden zijn toegestaan. | Alle waarden zijn toegestaan. | Alle waarden zijn toegestaan. | Alle waarden zijn toegestaan. |

**Hoofdrekening**

| Hoofdrekening | Naam          | Rechtspersoon | Departement                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Productverkopen | USMF         | Vast – 022 Sales en Marketing |

In de volgende afbeelding ziet u de vaste standaarddimensie die is ingesteld op de hoofdrekening 401100.

[![Financiële standaarddimensies](./media/default-dimensions.png)](./media/default-dimensions.png)

In dit eenvoudige voorbeeld wordt een algemeen journaal gebruikt waarin de afdelingsdimensie is ingesteld op de standaardwaarde **023** (Operations). We geven een grootboekrekening op en voeren boekingen uit. De volgende afbeelding toont de standaard financiële dimensie in de koptekst van het grootboek.

[![Algemene journalen](./media/general-journal.png)](./media/general-journal.png)

De standaarddimensie in de journaalkoptekst zorgt dat afdeling 023 standaard wordt toegepast op de verkooprekeningregel. In de volgende afbeelding ziet u de algemene journaalregel, waar de standaarddimensiewaarde **023** uit de koptekst wordt toegepast.

[![Journaalboekstuk](./media/journal-voucher.png)](./media/journal-voucher.png)

Wanneer de regel wordt geboekt, wordt echter de vaste dimensie is toegepast en wordt de regel geboekt naar afdeling 022. De volgende afbeelding toont het geboekte boekstuk, waarbij de vaste dimensie is toegepast voor de verkooprekening.

[![Boekstuktransacties](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Voorbeeld 2

Dit voorbeeld gebruikt dezelfde instelling als het eerste voorbeeld. We voegen echter een tweede component toe en gebruiken de afdelingsdimensie als een salderende dimensie. In het volgende voorbeeld is **Afdeling** ingesteld als de salderende financiële dimensie voor het grootboek USMF.

[![Grootboek](./media/ledger.png)](./media/ledger.png)

Wanneer de instellingen voor dezelfde journaalkoptekst worden gebruikt en dezelfde transactie wordt geboekt, wordt eerst de vaste dimensie toegepast. De salderingslogica wordt toegepast om te garanderen dat elke afdeling een salderende post heeft. In de volgende afbeelding ziet u de boekstuktransacties met de salderingspost nadat de vaste dimensie is toegepast.

[![Boekstuktransacties](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Voorbeeld 3

In dit voorbeeld wordt een geavanceerde regel toegevoegd. De geavanceerde regel geeft aan dat als verkooprekening 401100 en afdeling 022 (Sales en Marketing) worden gebruikt, het systeem moet een aanvullend segment bijhouden met de naam Klant.

Dit voorbeeld is belangrijk vanwege de volgorde. De rekeningstructuur wordt bepaald nadat de hoofdrekening is ingevoerd. Als u naar de instellingen van de rekeningstructuur verwijst, wordt bepaald of hoofdrekening, bedrijfseenheid, afdeling en kostenplaats relevant zijn. Op dit moment is de geavanceerde regel nog niet geactiveerd, omdat vaste dimensies pas worden toegepast als de standaarddimensies voor het journaalboekstuk zijn vereffend tijdens het boeken. In het volgende voorbeeld is het segment Klant niet aanwezig, omdat nog niet is voldaan aan de criteria voor de geavanceerde regel.

[![Grootboekrekening](./media/drop-down.png)](./media/drop-down.png)

De boeking is niet gelukt, omdat de vaste dimensie is toegepast aan het einde van het proces. Bij het valideren van de dimensies wordt bepaald dat het segment Klant vereist is als de hoofdrekening 401100 en de afdeling 022. De boeking kan niet worden uitgevoerd vanwege de validatiefout. De volgende afbeelding toont het bericht dat verschijnt nadat bij de dimensievalidatie is vastgesteld dat Klant een vereist segment is.

[![Berichtdetails](./media/message.png)](./media/message.png)

In dit voorbeeld moet u de standaardwaarde overschrijven, zodat de geavanceerde regel wordt geactiveerd en u het segment Klant kunt invoeren. Deze oplossing is echter niet altijd mogelijk en gebruikers zijn zich niet altijd bewust van de boekingsregels. Het is daarom belangrijk dat u de volgorde weet waarin de standaarddimensies worden toegepast bij het instellen van uw rekeningschema.

Als u wilt bereiken wat u in dit voorbeeld ziet, kunt u de configuratie op verschillende manieren wijzigen. U kunt bijvoorbeeld een nieuwe rekeningstructuur voor verkooprekeningen maken en het segment Klant opnemen in de structuur. U kunt ook meer rijen in een bestaande rekeningstructuur toevoegen en de hoofdrekening en geldige afdelingswaarden opgeven. In de aanvullende structuur voor de klant is het wellicht nuttig om over een afzonderlijke rekeningstructuur te beschikken met verkooprekeningen waarin het segment Klant aanwezig is.

## <a name="additional-resources"></a>Aanvullende resources 

Enkele van de volgende bronnen verwijzen naar een eerdere versie van Finance and Operations. Veel van de informatie over de toepassing van standaarddimensies en veel concepten zijn hetzelfde als in de eerdere versie, en de verwijzingen zijn nog steeds geldig.

[Evenwichtige journalen voor interunit-boekhouding](example-balanced-journals-interunit-accounting.md)

[Uw rekeningschema plannen](plan-chart-of-accounts.md) 

[Uw rekeningschema plannen in AX 2012 (blog)](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/): deze koppeling opent deel 1 van een reeks van zeven delen.

[Standaardinstellingen voor dimensies in boekhoudingsverdelingen](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Standaardinstellingen voor dimensies in dimensieraamwerk](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)

