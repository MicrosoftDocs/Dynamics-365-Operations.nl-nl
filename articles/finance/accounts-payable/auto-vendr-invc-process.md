---
title: Overzicht van geautomatiseerde processen voor leveranciersfacturering
description: In dit onderwerp wordt de mogelijkheid beschreven om uw leveranciersfactuurverwerking te automatiseren en de voordelen van het gebruik van een geautomatiseerd proces.
author: abruer
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9a033258feeccf172f1e2c03a9f49305054b24c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972126"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Overzicht van geautomatiseerde processen voor leveranciersfacturering

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de mogelijkheid beschreven om uw leveranciersfactuurverwerking te automatiseren en de voordelen van het gebruik van een geautomatiseerd proces. Deze mogelijkheid bestaat uit functies die worden ingeschakeld in Functiebeheer. Deze functies zijn alleen van toepassing op leveranciersfacturen en niet op facturen die worden verwerkt via de pagina **Factuurjournaal** of **Facturenregisterjournaal**.

Organisaties werken vaak met derden om papieren facturen te verwerken met behulp van een OCR-serviceprovider (Optical Character Recognition). De serviceprovider retourneert door machines leesbare metagegevens van facturen. Voor hulp bij automatisering kunt u met de automatiseringsfuncties van Leveranciers deze artefacten vanuit Leveranciers gebruiken.

U kunt een aantal factureringsprocessen voor leveranciers in Leveranciers automatiseren. Deze processen omvatten het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels met leveranciersfactuurregels die in behandeling zijn. In het geautomatiseerde proces wordt informatie weergegeven over de voortgang van een leveranciersfactuur wanneer deze elk proces doorloopt. Met deze mogelijkheid kunnen crediteurenmedewerkers en -managers leveranciersfacturen efficiënter verwerken. Het vermindert ook de fouten en inefficiënties die kunnen optreden wanneer informatie handmatig wordt ingevoerd en verwerkt.

De automatiseringsprocessen kunnen worden gebruikt om de volgende taken uit te voeren:

- Automatisch geïmporteerde facturen indienen bij het werkstroomsysteem.
- Productontvangstbonregels vereffenen met leveranciersfactuurregels in behandeling.
- Boekingen simuleren voordat een leveranciersfactuur wordt geboekt.
- Werkstroom- en automatiseringshistorie snel en efficiënt weergeven.
- De resultaten van automatisering van leveranciersfactuurverwerking weergeven en analyseren.
- De geautomatiseerde verwerking van meerdere facturen hervatten.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Automatisering van leveranciersfacturen – geïmporteerde leveranciersfacturen indienen bij het werkstroomsysteem

Als onderdeel van een contactloos factureringsproces van Leveranciers kunt u het systeem automatisch een geïmporteerde factuur laten indienen bij het werkstroomsysteem. Het proces wordt op de achtergrond uitgevoerd met een frequentie die u (per uur of per dag) opgeeft. De mogelijkheid om geïmporteerde facturen automatisch in te dienen bij het werkstroomsysteem vereist dat uw proces begint met een geïmporteerde factuur. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet een geautomatiseerde boekingstaak worden opgenomen in de werkstroomconfiguratie.

'Facturen die gerelateerd zijn aan inkooporders (IO´s) en facturen die een niet-IO-inkoopcategorie en niet-voorraadregels bevatten, kunnen automatisch bij het werkstroomsysteem worden ingediend. Facturen die handmatig worden ingevoerd en facturen die worden gemaakt via de werkruimte **Facturering via leverancierssamenwerking** moeten handmatig worden ingediend bij het werkstroomsysteem.

De automatiseringsfunctie voorziet in een flexibel kader waarmee u bedrijfsspecifieke regels kunt definiëren voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels voor leveranciersfactuurregels in behandeling.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Automatisering van leveranciersfacturen – productontvangstbonnen vereffenen met factuurregels die een drieweg-overeenstemmingsbeleid hebben

Het systeem kan automatisch geboekte productontvangstbonnen vereffenen met factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Het proces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Als onderdeel van dit proces kunt u het maximum aantal keren opgeven dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Het proces wordt op de achtergrond uitgevoerd, elk uur of per dag. U kunt het geautomatiseerde vereffeningsproces uitvoeren als onderdeel van het proces voor het indienen van facturen bij het werkstroomsysteem. U kunt het ook als een zelfstandig proces uitvoeren.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Automatisering van leveranciersfacturen – boeking van leveranciersfacturen vooraf valideren

Met boekingssimulatie worden de validatiestappen voltooid die worden uitgevoerd tijdens het boekingsproces voor leveranciersfacturen, maar er worden geen rekeningen bijgewerkt. Om het proces uit te voeren kunt u één factuur of meerdere facturen selecteren op de pagina **Leveranciersfacturen in behandeling**.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Automatisering van leveranciersfacturen – een verbeterde ervaring voor het weergeven van historische werkstroom- en automatiseringsgegevens voor leveranciersfacturen

Er wordt een gemakkelijk te lezen weergave van de werkstroomhistorie van leveranciersfacturen verschaft. Er kan rechtstreeks toegang worden verkregen tot de werkstroomhistorie van leveranciersfacturen via de leveranciersfactuur. Er zijn dus minder klikacties nodig om die informatie te vinden. Als uw organisatie de mogelijkheid heeft om geïmporteerde leveranciersfacturen automatisch in te dienen bij de werkstroom, wordt de automatiseringshistorie voor de geïmporteerde facturen gebruikt. Met de automatiseringshistorie kunt u de huidige processtap en de stappen die al zijn voltooid, herkennen. Wanneer een stap mislukt, bevat het systeem gedetailleerde informatie over de reden voor de fout.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Automatisering van leveranciersfacturen – analyse en metrische gegevens

Met de werkruimte **Leveranciersfactuurregistratie** kunt u zich concentreren op leveranciersfacturen die niet via het geautomatiseerde proces zijn gemaakt. Tegels in de werkruimte bevatten informatie over leveranciersfacturen die niet met succes zijn ingediend bij het werkstroomsysteem, niet zijn geïmporteerd of vereffend met productontvangstbonnen. Er worden ook metrische gegevens van Microsoft Power BI verschaft om crediteurenmanagers inzicht te geven in de efficiëntie van de automatisering van leveranciersfacturen.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automatisering leveranciersfactuur - automatiseringsverwerking hervatten voor meerdere facturen
Wanneer een geïmporteerde factuur niet via het geautomatiseerde proces naar de werkstroom is verzonden, wordt deze door het systeem verwijderd voor verdere geautomatiseerde verwerking. Een crediteurenadministrateur kan de factuur controleren en bewerken voordat deze door het geautomatiseerde proces opnieuw wordt ingediend bij de werkstroom. Wanneer een foutreden met dezelfde correctie voor meerdere facturen kan worden opgelost, kunt u het geautomatiseerde proces opnieuw starten op de pagina **Geautomatiseerde factuurverwerking hervatten**. 
