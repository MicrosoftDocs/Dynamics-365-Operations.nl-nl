---
title: Volgorde voor productietaken bepalen voor procesfabricage
description: In deze procedure worden als voorbeeld verfproducten gebruikt om aan te geven hoe u geplande orders op basis van de prioriteit van kleur en pakketgrootte kunt ordenen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e54cfa60fa9efd511aef8c074484b9b1a738e8cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572740"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Volgorde voor productietaken bepalen voor procesfabricage

[!include [banner](../../includes/banner.md)]

In deze procedure worden als voorbeeld verfproducten gebruikt om aan te geven hoe u geplande orders op basis van de prioriteit van kleur en pakketgrootte kunt ordenen. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USPI. Deze procedure is bedoeld voor de productieplanner.


## <a name="run-master-planning-for-uspi"></a>Hoofdplanning uitvoeren voor USPI
1. Ga naar Hoofdplanning > Hoofdplanning > Uitvoeren > Hoofdplanning.
2. Klik in het veld Hoofdplan op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer MasterPlan.  
4. Klik op OK.
    * Hiermee wordt de hoofdplanning gestart, waaronder het volgordeproces. Dit proces kan enkele minuten in beslag nemen.  

## <a name="view-planned-orders-for-the-paint-products"></a>Geplande orders weergeven voor de verfproducten
1. Ga naar Hoofdplanning > Hoofdplanning > Geplande orders.
2. Vouw het feitenvak Artikeldetails uit.
3. Vouw het feitenvak Schemadetails uit.
4. Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer MasterPlan.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P300'.
    * Ontgrendel om naar rechts te schuiven om de orderdatum en de leveringsdatum te bekijken. Deze artikelen hebben een orderdatum van Vandaag en de leveringsdatums voor de geplande orders worden niet geordend na de prioriteit van kleur en pakketgrootte, zoals getoond in de productnaam. U kunt de muis boven een artikelnummer plaatsen om de productnaam en de prioriteit te bekijken.  

## <a name="sequence-planned-orders-for-paint"></a>Geplande orders ordenen voor verf
1. Sluit de pagina.
2. Ga naar Hoofdplanning > Hoofdplanning > Geordende geplande orders.
3. Vouw het feitenvak Artikeldetails uit.
4. Vouw het feitenvak Schemadetails uit.
    * Opmerking: hier ziet u dat de begindatum en - tijd voor de geplande orders volgens kleur en pakketgrootte binnen een bucketperiode na 28 dagen zijn geordend. Deze perioden worden gedefinieerd door een getal in het veld Campagne. Het formulier voor geordende geplande orders fungeert als het standaardformulier voor geplande orders, en de productieplanner kan de geplande orders hier fiatteren.  
5. Markeer alle rijen.
6. Klik op Accepteren.
    * Hiermee worden de geplande orders bijgewerkt met de geselecteerde volgordeactie van Uitstellen of Vervroegen.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>De volgorde van de geplande orders verifiëren
1. Sluit de pagina.
2. Ga naar Hoofdplanning > Hoofdplanning > Geplande orders.
3. Vouw het feitenvak Artikeldetails uit.
4. Vouw het feitenvak Schemadetails uit.
5. Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer MasterPlan.  
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P300'.
    * De orders worden nu geordend op basis van de prioriteit van grootte en kleur en het begin van de geplande orders op de vroegste orderdatum en leveringsdatum. Valideer de kolom Orderdatum of de begindatum in het feitenvak Schemadetails.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]