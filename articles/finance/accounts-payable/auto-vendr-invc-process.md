---
title: Overzicht van geautomatiseerde processen voor leveranciersfacturering
description: In dit onderwerp wordt de mogelijkheid beschreven om uw leveranciersfactuurverwerking te automatiseren en de voordelen van het gebruik van een geautomatiseerd proces.
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2020
ms.locfileid: "3905005"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Overzicht van geautomatiseerde processen voor leveranciersfacturering

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt de mogelijkheid beschreven om uw leveranciersfactuurverwerking te automatiseren en de voordelen van het gebruik van een geautomatiseerd proces. Deze mogelijkheid bestaat uit functies die worden ingeschakeld in Functiebeheer. Deze functies zijn alleen van toepassing op leveranciersfacturen en niet op facturen die worden verwerkt via de pagina **Factuurjournaal** of **Facturenregisterjournaal**.

Organisaties werken vaak met derden om papieren facturen te verwerken met behulp van een OCR-serviceprovider (Optical Character Recognition). De serviceprovider retourneert door machines leesbare metagegevens van facturen. Voor hulp bij automatisering kunt u met de automatiseringsfuncties van Leveranciers deze artefacten vanuit Leveranciers gebruiken.

U kunt een aantal factureringsprocessen voor leveranciers in Leveranciers automatiseren. Deze processen omvatten het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels met leveranciersfactuurregels die in behandeling zijn. In het geautomatiseerde proces wordt informatie weergegeven over de voortgang van een leveranciersfactuur wanneer deze elk proces doorloopt. Met deze mogelijkheid kunnen crediteurenmedewerkers en -managers leveranciersfacturen efficiënter verwerken. Het vermindert ook de fouten en inefficiënties die kunnen optreden wanneer informatie handmatig wordt ingevoerd en verwerkt.

De automatiseringsprocessen kunnen worden gebruikt om de volgende taken uit te voeren:

- Automatisch geïmporteerde facturen indienen bij het werkstroomsysteem.
- Productontvangstbonregels vereffenen met leveranciersfactuurregels in behandeling.
- Boekingen simuleren voordat een leveranciersfactuur wordt geboekt.
- Werkstroomhistorie snel en efficiënt weergeven.
- De resultaten van automatisering van leveranciersfactuurverwerking weergeven en analyseren.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Automatisering van leveranciersfacturen – geïmporteerde leveranciersfacturen indienen bij het werkstroomsysteem

Als onderdeel van een contactloos factureringsproces van Leveranciers kunt u het systeem automatisch een geïmporteerde factuur laten indienen bij het werkstroomsysteem. Het proces wordt op de achtergrond uitgevoerd met een frequentie die u (per uur of per dag) opgeeft. De mogelijkheid om geïmporteerde facturen automatisch in te dienen bij het werkstroomsysteem vereist dat uw proces begint met een geïmporteerde factuur. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet een geautomatiseerde boekingstaak worden opgenomen in de werkstroomconfiguratie.

'Facturen die gerelateerd zijn aan inkooporders (IO´s) en facturen die een niet-IO-inkoopcategorie en niet-voorraadregels bevatten, kunnen automatisch bij het werkstroomsysteem worden ingediend. Facturen die handmatig worden ingevoerd en facturen die worden gemaakt via de werkruimte **Facturering via leverancierssamenwerking** moeten handmatig worden ingediend bij het werkstroomsysteem.

De automatiseringsfunctie voorziet in een flexibel kader waarmee u bedrijfsspecifieke regels kunt definiëren voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels voor leveranciersfactuurregels in behandeling.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Automatisering van leveranciersfacturen – productontvangstbonnen vereffenen met factuurregels die een drieweg-overeenstemmingsbeleid hebben

Het systeem kan automatisch geboekte productontvangstbonnen vereffenen met factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Het proces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Als onderdeel van dit proces kunt u het maximum aantal keren opgeven dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Het proces wordt op de achtergrond uitgevoerd, elk uur of per dag. U kunt het geautomatiseerde vereffeningsproces uitvoeren als onderdeel van het proces voor het indienen van facturen bij het werkstroomsysteem. U kunt het ook als een zelfstandig proces uitvoeren.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Automatisering van leveranciersfacturen – boeking van leveranciersfacturen vooraf valideren

Met boekingssimulatie worden de validatiestappen voltooid die worden uitgevoerd tijdens het boekingsproces voor leveranciersfacturen, maar er worden geen rekeningen bijgewerkt. Om het proces uit te voeren kunt u één factuur of meerdere facturen selecteren op de pagina **Leveranciersfacturen in behandeling**.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Automatisering van leveranciersfacturen – een verbeterde ervaring voor het weergeven van historische werkstroomgegevens voor leveranciersfacturen

Er wordt een gemakkelijk te lezen weergave van de werkstroomhistorie van leveranciersfacturen verschaft. Er kan rechtstreeks toegang worden verkregen tot de werkstroomhistorie van leveranciersfacturen via de leveranciersfactuur. Er zijn dus minder klikacties nodig om die informatie te vinden.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Automatisering van leveranciersfacturen – analyse en metrische gegevens

Met de werkruimte **Leveranciersfactuurregistratie** kunt u zich concentreren op leveranciersfacturen die niet via het geautomatiseerde proces zijn gemaakt. Tegels in de werkruimte bevatten informatie over leveranciersfacturen die niet met succes zijn ingediend bij het werkstroomsysteem, niet zijn geïmporteerd of vereffend met productontvangstbonnen. Er worden ook metrische gegevens van Microsoft Power BI verschaft om crediteurenmanagers inzicht te geven in de efficiëntie van de automatisering van leveranciersfacturen.
