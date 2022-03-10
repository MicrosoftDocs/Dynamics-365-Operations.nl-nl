---
title: Overzicht van geautomatiseerde processen voor leveranciersfacturering
description: In dit onderwerp wordt de mogelijkheid beschreven om uw leveranciersfactuurverwerking te automatiseren en de voordelen van het gebruik van een geautomatiseerd proces.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4fef5011ead69028a7f667835fd5e5ba2401408d
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985651"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Overzicht van geautomatiseerde processen voor leveranciersfacturering

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de mogelijkheid beschreven om uw leveranciersfactuurverwerking te automatiseren en de voordelen van het gebruik van een geautomatiseerd proces. Deze mogelijkheid bestaat uit functies die worden ingeschakeld in Functiebeheer. Deze functies zijn alleen van toepassing op leveranciersfacturen en niet op facturen die worden verwerkt via de pagina **Factuurjournaal** of **Facturenregisterjournaal**.

Organisaties werken vaak met derden om papieren facturen te verwerken met behulp van een OCR-serviceprovider (Optical Character Recognition). De serviceprovider retourneert door machines leesbare metagegevens van facturen. Voor hulp bij automatisering kunt u met de automatiseringsfuncties van Leveranciers deze artefacten vanuit Leveranciers gebruiken.

U kunt een aantal factureringsprocessen voor leveranciers in Leveranciers automatiseren. Deze processen omvatten het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels met leveranciersfactuurregels die in behandeling zijn. In het geautomatiseerde proces wordt informatie weergegeven over de voortgang van een leveranciersfactuur wanneer deze elk proces doorloopt. Met deze mogelijkheid kunnen crediteurenmedewerkers en -managers leveranciersfacturen efficiënter verwerken. Het vermindert ook de fouten en inefficiënties die kunnen optreden wanneer informatie handmatig wordt ingevoerd en verwerkt.

De automatiseringsprocessen kunnen worden gebruikt om de volgende taken uit te voeren:

- Automatisch vooruitbetalingen op leveranciersfacturen toepassen
- Automatisch geïmporteerde facturen indienen bij het werkstroomsysteem.
- Productontvangstbonregels vereffenen met leveranciersfactuurregels in behandeling.
- Boekingen simuleren voordat een leveranciersfactuur wordt geboekt.
- Werkstroom- en automatiseringshistorie snel en efficiënt weergeven.
- De resultaten van automatisering van leveranciersfactuurverwerking weergeven en analyseren.
- De geautomatiseerde verwerking van meerdere facturen hervatten.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Geïmporteerde leveranciersfacturen indienen bij het werkstroomsysteem

Als onderdeel van een contactloos factureringsproces van Leveranciers kunt u het systeem automatisch een geïmporteerde factuur laten indienen bij het werkstroomsysteem. Het proces wordt op de achtergrond uitgevoerd met een frequentie die u (per uur of per dag) opgeeft. De mogelijkheid om geïmporteerde facturen automatisch in te dienen bij het werkstroomsysteem vereist dat uw proces begint met een geïmporteerde factuur. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet een geautomatiseerde boekingstaak worden opgenomen in de werkstroomconfiguratie.


Facturen die gerelateerd zijn aan inkooporders (IO's) en facturen die een niet-IO-inkoopcategorie en niet-voorraadregels bevatten, kunnen automatisch bij het werkstroomsysteem worden ingediend. Facturen die handmatig worden ingevoerd en facturen die worden gemaakt met de werkruimte **Facturering via leverancierssamenwerking** moeten handmatig worden ingediend bij het werkstroomsysteem. De verwerking van vooruitbetalingen moet handmatig worden uitgevoerd voor geïmporteerde facturen. U kunt vooruitbetalingen handmatig toepassen voor of na het boeken van de geïmporteerde factuur. U kunt handmatig vooruitbetalingen toepassen op niet-geboekte standaardfacturen met de pagina **Leveranciersfacturen**. Na het boeken is de vereffende vooruitbetaling beschikbaar om handmatig toe te passen op andere facturen van deze leverancier op de pagina **Leveranciers** (**Leveranciers \> Algemeen \> Leveranciers \> Alle leveranciers \> tabblad Factuur \> Toepassen**).

De automatiseringsfunctie voorziet in een flexibel kader waarmee u bedrijfsspecifieke regels kunt definiëren voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels voor leveranciersfactuurregels in behandeling.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Productontvangstbonnen vereffenen met factuurregels die een drieweg-overeenstemmingsbeleid hebben

Het systeem kan automatisch geboekte productontvangstbonnen vereffenen met factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Het proces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Als onderdeel van dit proces kunt u het maximum aantal keren opgeven dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Het proces wordt op de achtergrond uitgevoerd, elk uur of per dag. U kunt het geautomatiseerde vereffeningsproces uitvoeren als onderdeel van het proces voor het indienen van facturen bij het werkstroomsysteem. U kunt het ook als een zelfstandig proces uitvoeren.

## <a name="pre-validate-vendor-invoice-posting"></a>Leveranciersfactuurboeking vooraf valideren

Met boekingssimulatie worden de validatiestappen voltooid die worden uitgevoerd tijdens het boekingsproces voor leveranciersfacturen, maar er worden geen rekeningen bijgewerkt. Om het proces uit te voeren kunt u één factuur of meerdere facturen selecteren op de pagina **Leveranciersfacturen in behandeling**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Verbeterde ervaring voor het weergeven van werkstroomgegevens en historische informatie over automatisering voor leveranciersfacturen

Er wordt een gemakkelijk te lezen weergave van de werkstroomhistorie van leveranciersfacturen verschaft. Er kan rechtstreeks toegang worden verkregen tot de werkstroomhistorie van leveranciersfacturen via de leveranciersfactuur. Er zijn dus minder klikacties nodig om die informatie te vinden. Als uw organisatie de mogelijkheid heeft om geïmporteerde leveranciersfacturen automatisch in te dienen bij de werkstroom, wordt de automatiseringshistorie voor de geïmporteerde facturen gebruikt. Met de automatiseringshistorie kunt u de huidige processtap en de stappen die al zijn voltooid, herkennen. Wanneer een stap mislukt, bevat het systeem gedetailleerde informatie over de reden voor de fout.

## <a name="analytics-and-metrics"></a>Analyse en metrische gegevens

Met de werkruimte **Leveranciersfactuurregistratie** kunt u zich concentreren op leveranciersfacturen die niet via het geautomatiseerde proces zijn gemaakt. Tegels in de werkruimte bevatten informatie over leveranciersfacturen die niet met succes zijn ingediend bij het werkstroomsysteem, niet zijn geïmporteerd of vereffend met productontvangstbonnen. Er worden ook metrische gegevens van Microsoft Power BI verschaft om crediteurenmanagers inzicht te geven in de efficiëntie van de automatisering van leveranciersfacturen.


## <a name="resume-automation-processing-for-multiple-invoices"></a>De automatiseringsverwerking van meerdere facturen hervatten

Wanneer een geïmporteerde factuur niet via het geautomatiseerde proces naar de werkstroom is verzonden, wordt deze door het systeem verwijderd voor verdere geautomatiseerde verwerking. Een crediteurenadministrateur kan de factuur controleren en bewerken voordat deze door het geautomatiseerde proces opnieuw wordt ingediend bij de werkstroom. Wanneer een foutreden met dezelfde correctie voor meerdere facturen kan worden opgelost, kunt u het geautomatiseerde proces opnieuw starten op de pagina **Geautomatiseerde factuurverwerking hervatten**. 

## <a name="tracking-the-invoice-received-date-value"></a>De datumwaarde voor de ontvangst van de factuur traceren

De waarde **Datum factuurontvangst** geeft de datum aan waarop het bedrijf de factuur van de leverancier heeft ontvangen. Het biedt een uitgangspunt voor het bijhouden van de voortgang van de factuur door de geautomatiseerde processen. Deze waarde kan worden opgenomen in de geïmporteerde gegevens voor een leveranciersfactuur. Voor facturen die handmatig zijn gemaakt, kunt u de datum opgeven. Als er geen waarde wordt ingevoerd, wordt standaard de huidige datum gebruikt.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>De waarden voor Geïmporteerd factuurbedrag en Geïmporteerd btw-bedrag bijhouden

De waarden voor **Geïmporteerd factuurbedrag** en **Geïmporteerd btw-bedrag** voor leveranciersfacturen kunnen in het importbestand voor leveranciersfacturen worden opgegeven. Normaal gesproken zijn deze waarden afkomstig van een factuur die door een externe provider is gescand en in het importbestand is opgenomen. Wanneer de factuur in Leveranciers wordt verwerkt, berekent het systeem waarden op basis van de factuurgegevens. De factuur kan alleen worden geboekt als de geïmporteerde waarden overeenkomen met de berekende waarden. Overeenkomende waarden zorgen ervoor dat de factuur het verschuldigde bedrag aan de leverancier nauwkeurig weerspiegelen. Als uw organisatie toestaat dat geïmporteerde facturen automatisch bij het werkstroomsysteem worden ingediend, kunt u desgewenst vereisen dat de geïmporteerde totalen overeenkomen met de berekende totalen voordat de factuur bij het werkstroomsysteem kan worden ingediend.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automatisering leveranciersfactuur - automatiseringsverwerking hervatten voor meerdere facturen
Wanneer een geïmporteerde factuur niet via het geautomatiseerde proces naar de werkstroom is verzonden, wordt deze door het systeem verwijderd voor verdere geautomatiseerde verwerking. Een crediteurenadministrateur kan de factuur controleren en bewerken voordat deze door het geautomatiseerde proces opnieuw wordt ingediend bij de werkstroom. Wanneer een foutreden met dezelfde correctie voor meerdere facturen kan worden opgelost, kunt u het geautomatiseerde proces opnieuw starten op de pagina **Geautomatiseerde factuurverwerking hervatten**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
