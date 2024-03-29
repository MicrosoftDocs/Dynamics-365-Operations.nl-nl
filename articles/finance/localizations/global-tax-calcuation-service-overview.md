---
title: Overzicht van belastingberekening
description: In dit artikel worden het algehele bereik en de functies voor belastingberekening uitgelegd.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689879"
---
# <a name="tax-calculation-overview"></a>Overzicht van belastingberekening

[!include [banner](../includes/banner.md)]

Belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen. De belastingengine kan volledig worden geconfigureerd. De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting. De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.

De functie voor het berekenen van belastingen wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.

> [!IMPORTANT]
> Wanneer u de Belastingberekening inschakelt, kunnen bepaalde bewerkingen op gerelateerde gegevens worden uitgevoerd in een ander datacentrum dan het datacentrum dat uw servicegegevens onderhoudt. Controleer de [Algemene voorwaarden](https://go.microsoft.com/fwlink/?linkid=2156043) voor u Belastingberekening inschakelt. Uw privacy is belangrijk voor ons. Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.

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
- Brazilië
- Canada
- Europa
- Frankrijk
- India
- Japan
- Zuid-Afrika
- Zwitserland
- Verenigde Arabische Emiraten
- Verenigd Koninkrijk
- Verenigde Staten

> [!NOTE]
> Een eerdere versie van Dynamics 365, zoals Dynamics AX 2012, of on-premises implementaties van Dynamics 365 wordt niet door Belastingberekening ondersteund.

## <a name="versions"></a>Versies
Het is raadzaam om uw btw-berekeningsconfiguratie te importeren en in te stellen met de versie die overeenkomt met uw versie van Finance of Supply Chain Management.

| Versie van Finance of Supply Chain Management | Versie van belastingconfiguratie               |
| --------------- | --------------------------------------- |
| 10.0.31         | Belastingberekeningsconfiguratie 40.56.240 |
| 10.0.30         | Belastingberekeningsconfiguratie 40.55.239 |
| 10.0.29         | Belastingberekeningsconfiguratie 40.55.236 |
| 10.0.28         | Belastingberekeningsconfiguratie 40.54.234 |
| 10.0.27         | Belastingberekeningsconfiguratie 40.54.234 |


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

In de volgende tabel staan de transacties die in de bijbehorende versie worden ondersteund.

| Versie | Transacties |
|---------|--------------|
| 10.0.29 | Periodieke journalen |
| 10.0.28 | Journaal met betalingen van leverancier<br> Journaal met betalingen van klant | 
| 10.0.26 | Algemene journalen<br> Leveranciersfacturenjournaal |
| 10.0.23 | Vrije-tekstfactuur |
| 10.0.21| Sales<br><ul><li>Verkoopofferte</li><li>Verkooporder</li><li>Bevestiging</li><li>Orderverzamellijst</li><li>Pakbon</li><li>Verkoopfactuur</li><li>Creditnota</li><li>Retourorder</li><li>Diverse toeslagen voor koptekst</li><li>Diverse toeslagen voor regels</li></ul>Inkoop<br><ul><li>Inkooporder</li><li>Bevestiging</li><li>Ontvangstlijst</li><li>Ontvangst van producten</li><li>Inkoopfactuur</li><li>Diverse toeslagen voor koptekst</li><li>Diverse toeslagen voor regels</li><li>Creditnota</li><li>Retourorder</li><li>Opdracht tot inkoop</li><li>Diverse toeslagen voor regel van opdracht tot inkoop</li><li>Offerteaanvraag</li><li>Diverse toeslagen voor koptekst van offerteaanvraag</li><li>Diverse toeslagen voor regel van offerteaanvraag</li></ul>Voorraad<ul><li>Transferorder – verzenden</li><li>Transferorder – ontvangen</li></ul>|

## <a name="supported-countriesregions"></a>Ondersteunde landen/regio's

Belastingberekening kan worden uitgevoerd met ondersteunde localisatiefuncties. In de volgende tabel staan de landen/regio's voor het primaire adres van een rechtspersoon.

| Versie | Land/regio |
|---------|----------------|
| 10.0.26 | - China <br>- Tsjechische Republiek<br>- Spanje |
| 10.0.24 | Mexico |
| 10.0.23 | - Thailand <br>- Japan <br>- Maleisië <br>- Singapore |
| 10.0.22 | - Australië<br>- Bahrein <br>- Canada<br>- Egypte <br>- Hongkong SAR <br>- Koeweit <br>- Nieuw-Zeeland <br>- Oman <br>- Qatar <br>- Saoedi-Arabië <br>- Zuid-Afrika <br>- Verenigde Arabische Emiraten |
| 10.0.21 | - Oostenrijk <br>- België <br>- Denemarken <br>- Estland <br>- Finland <br>- Frankrijk <br>- Duitsland <br>- Hongarije <br>- IJsland <br>- Ierland <br>- Italië <br>- Letland <br>- Litouwen <br>- Nederland <br>- Noorwegen <br>- Polen <br>- Zweden <br>- Zwitserland <br>- Verenigd Koninkrijk <br>- Verenigde Staten |

Voor een land dat of regio die niet door Microsoft is gelokaliseerd, kan de btw-berekening ook worden ingeschakeld en worden uitgevoerd met andere algemene functies.

## <a name="related-resources"></a>Gerelateerde bronnen

[Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md)

[Meerdere btw-registratienummers](./emea-multiple-vat-registration-numbers.md)

[Ondersteuning voor belastingfunctie voor transferorder](./tasks/tax-feature-support-for-transfer-order.md)

[Uitbreiding in belastingservice maken](./tax-service-add-data-fields-tax-integration-by-extension.md)
