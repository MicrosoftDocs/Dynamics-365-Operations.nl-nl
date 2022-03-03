---
title: Overzicht van belastingberekening
description: In dit onderwerp worden het algehele bereik en de functies voor belastingberekening uitgelegd.
author: wangchen
ms.date: 11/17/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1dff1767b8e19215a2b27f87c45325e6abd1266e
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105432"
---
# <a name="tax-calculation-overview"></a>Overzicht van belastingberekening

[!include [banner](../includes/banner.md)]

Belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen. De belastingengine kan volledig worden geconfigureerd. De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting. De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.

Belastingberekening wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.

> [!IMPORTANT]
> Wanneer u de Belastingberekening inschakelt, kunnen bepaalde bewerkingen op gerelateerde gegevens worden uitgevoerd in een ander datacentrum dan het datacentrum dat uw servicegegevens onderhoudt. Controleer de [Algemene voorwaarden](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) voor u Belastingberekening inschakelt. Uw privacy is belangrijk voor ons. Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.

Belastingberekening is een op microservices gebaseerde belastingengine die exponentiële schaalbaarheid biedt en u kan helpen de volgende taken uit te voeren:

- Bepaal automatisch de juiste btw-groep, btw-groep voor artikel en belastingcodes via een uitgebreid bepalingsmechanisme.
- Ondersteun meerdere belastingregistratienummers één rechtspersoon en bepaal automatisch het juiste belastingregistratienummer voor belastbare transacties.
- Ondersteun belastingbepaling, -berekening en -posten en vereffening voor transferorders.
- Definieer configureerbare belastingberekeningsformules en voorwaarden voor uw specifieke bedrijfsbehoeften.
- Deel de belastingbepalings- en berekeningsoplossing voor alle rechtspersonen om minder onderhoud te hoeven uitvoeren en fouten te voorkomen.
- Ondersteun bepaling van het belastingregistratienummer voor klanten en leveranciers.
- Ondersteun de bepaling van lijstcodes.
- Ondersteun parameters voor belastingberekening op belastingsjurisdictieniveau.

Als u de Belastingberekening wilt gebruiken, installeert u de invoegtoepassing Belastingberekening vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS). Voltooi vervolgens de instellingen in [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) en schakel Belastingberekening in bij Finance en Supply Chain Management. Zie [Aan de slag met belastingservice](global-get-started-with-tax-calculation-service.md) voor meer informatie.

## <a name="availability"></a>Beschikbaarheid

Belastingberekening is vanaf versie 10.0.21 algemeen beschikbaar voor alle klanten in productieomgevingen.

Er komen telkens nieuwe functies bij. Controleer regelmatig de meest actuele releaseplanning voor meer informatie over de dekking en het bereik van ondersteunde functies.

Belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure. Er zullen meer Azure-regio's worden toegevoegd op basis van klantbehoeften.

- Azië-Pacific
- Australië
- Canada
- Europa
- Japan
- Verenigd Koninkrijk
- Verenigde Staten

> [!NOTE]
> Een eerdere versie van Dynamics 365, zoals Dynamics AX 2012, of on-premises implementaties van Dynamics 365 wordt niet door Belastingberekening ondersteund.

## <a name="versions"></a>Versies
Het is raadzaam om uw btw-berekeningsconfiguratie te importeren en in te stellen met de versie die overeenkomt met uw versie van Finance of Supply Chain Management.

| Versie van Finance of Supply Chain Management | Versie van belastingconfiguratie               |
| --------------- | --------------------------------------- |
| 10.0.18         | Belastingconfiguratie - Europa 30.12.82     |
| 10.0.19         | Belastingberekeningsconfiguratie 36.38.193 |
| 10.0.20         | Belastingberekeningsconfiguratie 40.43.208 |
| 10.0.21         | Belastingberekeningsconfiguratie 40.48.215 |
| 10.0.22         | Belastingberekeningsconfiguratie 40.48.215 |
| 10.0.23         | Belastingberekeningsconfiguratie 40.50.221 |
| 10.0.24         | Belastingberekeningsconfiguratie 40.50.225 |
| 10.0.25         | Belastingberekeningsconfiguratie 40.50.225 |


## <a name="data-flow"></a>Gegevensstroom

Hier volgt een overzicht van het gegevensstroomproces voor Belastingberekening. 

1. In RCS kunt u belastbare documentmodelconfiguraties en modeltoewijzingsconfiguraties weergeven en importeren. Zie [Gegevensvelden in belastingconfiguraties toevoegen](tax-service-add-data-fields-tax-configurations.md) als u configuraties voor een geavanceerd scenario moet uitbreiden.
2. In RCS kunt u belastingfuncties maken of onderhouden. U kunt belastingsfuncties gebruiken om belastingtarieven en toepasbaarheidsregels te onderhouden.
3. Nadat de installatie van de belastingfunctie is voltooid, publiceert u de belastingconfiguraties en belastingfuncties van RCS naar de algemene opslagplaats.
4. Selecteer in Financiën welke installatieversie van de belastingfunctie voor een specifieke rechtspersoon moet worden gebruikt.
5. Verwerk in Finance en Supply Chain Management transacties op de gebruikelijke manier. Wanneer Belastingberekening nodig is, verzamelt de client informatie uit de transactie, zoals de verkooporder of inkooporder, en wordt de informatie als nettolading verpakt. Er wordt vervolgens een aanvraag verzonden om de belasting te berekenen.
6. De belastingberekeningsaanvraag wordt van de client ontvangen en de berekening wordt voltooid. Het belastingresultaat wordt vervolgens aan de client geretourneerd.
7. De Dynamics 365-client ontvangt het belastingresultaat en geeft het resultaat van de belastingberekening weer op een btw-pagina.

## <a name="supported-transactions"></a>Ondersteunde transacties

Belastingberekening kan worden ingeschakeld per transacties. 

De volgende transacties worden ondersteund in versie 10.0.21: 

- Verkopen

    - Verkoopofferte
    - Verkooporder
    - Bevestiging
    - Orderverzamellijst
    - Pakbon
    - Verkoopfactuur
    - Creditnota
    - Retourorder
    - Diverse toeslagen voor koptekst
    - Diverse toeslagen voor regels

- Inkoop

    - Inkooporder
    - Bevestiging
    - Ontvangstlijst
    - Ontvangst van producten
    - Inkoopfactuur
    - Diverse toeslagen voor koptekst
    - Diverse toeslagen voor regels
    - Creditnota
    - Retourorder
    - Opdracht tot inkoop
    - Diverse toeslagen voor regel van opdracht tot inkoop
    - Offerteaanvraag
    - Diverse toeslagen voor koptekst van offerteaanvraag
    - Diverse toeslagen voor regel van offerteaanvraag

- Voorraad

    - Transferorder – verzenden
    - Transferorder – ontvangen

De volgende transacties worden ondersteund in versie 10.0.23: 

- Vrije-tekstfactuur

## <a name="supported-countriesregions"></a>Ondersteunde landen/regio's

Belastingberekening kan per rechtspersoon worden ingeschakeld. 

De volgende landen/regio's voor het primaire adres van een rechtspersoon worden ondersteund in versie 10.0.21:

- Oostenrijk
- België
- Denemarken
- Estland
- Finland
- Frankrijk
- Duitsland
- Hongarije
- IJsland
- Italië
- Letland
- Litouwen
- Nederland
- Noorwegen
- Polen
- Zweden
- Zwitserland
- Verenigd Koninkrijk
- Verenigde Staten

De volgende landen/regio's voor het primaire adres van een rechtspersoon worden ondersteund in versie 10.0.22:

- Australië
- Bahrein
- Canada
- Egypte
- Hongkong SAR
- Koeweit
- Nieuw-Zeeland
- Oman
- Qatar
- Saoedi-Arabië
- Zuid-Afrika
- Verenigde Arabische Emiraten

De volgende landen/regio's voor het primaire adres van een rechtspersoon worden ondersteund in versie 10.0.23:

- Thailand
- Japan
- Maleisië
- Singapore

De volgende landen/regio's voor het primaire adres van een rechtspersoon worden ondersteund in versie 10.0.24:

- Mexico

## <a name="related-resources"></a>Gerelateerde bronnen

[Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md)

[Meerdere btw-registratienummers](./emea-multiple-vat-registration-numbers.md)

[Ondersteuning voor belastingfunctie voor transferorder](./tasks/tax-feature-support-for-transfer-order.md)

[Uitbreiding in belastingservice maken](./tax-service-add-data-fields-tax-integration-by-extension.md)
