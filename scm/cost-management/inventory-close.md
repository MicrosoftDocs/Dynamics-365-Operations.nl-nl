---
title: Voorraad sluiten
description: Als onderdeel van het proces voor uitgiftetransacties met ontvangsttransacties te vereffenen, kunt u ook het grootboek bijwerken om de aangebrachte correcties weer te geven.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9ff992be8a2a4f1cc0cd3146f138d12267bb74ee
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-close"></a>Voorraad sluiten

[!include[banner](../includes/banner.md)]


Als onderdeel van het proces voor uitgiftetransacties met ontvangsttransacties te vereffenen, kunt u ook het grootboek bijwerken om de aangebrachte correcties weer te geven.

Met het proces voor het afsluiten van voorraden worden uitgiftetransacties vereffend met ontvangsttransacties op basis van de methode voor het waarderen van voorraden die in de artikelmodelgroep van het artikel is geselecteerd. Als onderdeel van het vereffeningsproces kunt u opgeven dat het grootboek moet worden bijgewerkt, zodat het de correcties bevat die zijn gemaakt. Uitgiftetransacties worden echter geboekt volgens de berekende gemiddelde, lopende kostprijs, totdat de voorraad wordt afgesloten of opnieuw berekend. 

Na het afsluiten van de voorraad kunt u niet meer boeken in perioden vóór de door u ingestelde datum van de voorraadafsluiting, tenzij u het voltooide proces van het afsluiten van de voorraad omkeert. Bijvoorbeeld: als de voorraadafsluiting wordt uitgevoerd voor de periode die op 31 januari eindigt, kunt u geen transacties boeken met een datum die valt vóór 31 januari. 

Artikelen in voorraad worden toegewezen aan een van de twee voorraadtypen: artikel of service. De voorraadafsluiting voert dezelfde functies voor beide typen uit. Echter, voor artikelen van het type Service vereffent voorraadafsluiting wel uitgiften met ontvangsten. 

Hoe dikwijls de voorraadafsluiting wordt uitgevoerd, verschilt per bedrijf. Echter, het transactievolume moeten helpen bepalen hoe vaak u de voorraadafsluiting uitvoert. In de meeste bedrijven is het afsluiten van de voorraad onderdeel van de procedures voor het afsluiten van een maand en het afstemmen.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Voorraadherberekening en het grootboek
Als in een maand of een andere voorraadperiode de voorraad en het grootboek moeten worden gecorrigeerd, kunt u de voorraad opnieuw berekenen in plaats van af te sluiten. Bij het herberekenen van de voorraad worden voorraadtransacties gecorrigeerd maar niet vereffend. 

Tijdens voorraadherberekening wordt de voorhanden voorraad aangepast, worden voorraadtransacties gecorrigeerd en worden voorraadherberekeningen en voorraadafsluiting uitgevoerd. Deze taken beïnvloeden elke grootboekrekening die aan de oorspronkelijke voorraadtransactie is gekoppeld. 

**Voorbeeld** 

Als u een inkooporder van een verkooporder maakt, worden de algemene grootboekrekeningen bijgewerkt die zijn gebruikt voor de originele verkooporder. Zelfs als de grootboekrekeningen voor de artikelgroep die is toegewezen aan dit artikel zijn gewijzigd na het boeken van de verkooporder en er bij de herberekening van de voorraad een correctiebedrag is gemaakt, wordt het correctiebedrag toch geboekt op de originele grootboekrekeningen, en niet op de nieuwe grootboekrekeningen die zijn toegewezen aan het artikel. Het gecorrigeerde bedrag wordt niet geboekt naar de nieuwe grootboekrekeningen die zijn toegewezen aan het artikel. 

Nadat het bijwerken is voltooid, kunt u het grootboekboekstuk controleren dat is geboekt ten gevolge van het voltooien van een van deze taken.

1.  Selecteer op de pagina **Afsluiten en corrigeren**, op het tabblad **Overzicht**, de update voor controle.
2.  Klik op **Details** en selecteer vervolgens **Boekstuk**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Gevolgen van het voorraadafsluitingsproces voor het grootboek
Verschillende taken die u kunt voltooien op de pagina **Afsluiten en corrigeren**, resulteren in het bijwerken van het grootboek. Het grootboek wordt bijvoorbeeld bijgewerkt wanneer u correcties in de voorhanden voorraad aanbrengt, correcties in voorraadtransacties doorvoert, herberekening van de voorraad uitvoert en voorraadafsluiting uitvoert. 

De grootboekrekeningen die vanwege deze taken worden bijgewerkt, worden gekoppeld aan de oorspronkelijke voorraadtransactie. Als bijvoorbeeld een verkooporder wordt vereffend met een inkooporder, worden de grootboekrekeningen die zijn gebruikt voor de oorspronkelijke verkooporder, gecorrigeerd. Dit geldt zelfs wanneer de grootboekrekeningen voor de artikelgroep die aan het artikel is toegewezen, zijn gewijzigd nadat de verkooporder is geboekt. Nadat door een voorraadafsluiting een vereffeningsbedrag is gemaakt, wordt het vereffeningsbedrag nog steeds naar de oorspronkelijke grootboekrekeningen geboekt, en niet naar de nieuwe grootboekrekeningen die aan het artikel zijn toegewezen. Het grootboek kan ook worden bijgewerkt door het omkeren van een voorraadafsluiting. 

**Opmerkingen:**

-   De voorraad hoeft niet te worden afgesloten als u waarderen van de standaardkostprijs gebruikt.
-   Voordat u de afsluitingsprocedure uitvoert, kunt u een lijst met artikelen weergeven die tijdens de update niet kunnen worden vereffend.
-   Wij raden aan de voorraad buiten de kantoortijden af te sluiten om computerbronnen gelijkelijker te verdelen.

## <a name="the-inventory-close-log"></a>Het voorraadafsluitingslogboek weergeven
Nadat de voorraadafsluiting is voltooid, kan in het berichtencentrum een bericht worden aangegeven dat de kostprijs per eenheid wellicht onjuist is omdat een transactie niet volledig is vereffend. 

Voordat dit bericht wordt weergegeven, worden het artikelnummer en de desbetreffende transactie gerapporteerd. In dit bericht staat dat het kostenbedrag dat is gebruikt voor deze transactie, niet is bijgewerkt vanwege de voorraadafsluiting. Dit bericht verschijnt wanneer een transactie van het type uitgifte niet kan worden vereffend. 

Tijdens het voorraadafsluitingsproces worden alle financiële dimensies nagelopen om te controleren of er op een bepaalde afsluitdatum meer uitgiften dan ontvangsten zijn. Een dergelijk type onevenwicht kan optreden wanneer een voorraadtransactie van een inkooporder niet volledig financieel is geboekt omdat de leveranciersfactuur niet is ontvangen of omdat stuklijstcomponenten die in een productie zijn opgenomen op een hoger niveau, niet financieel zijn geboekt. (De kosten van subproductie worden niet berekend.) In dit geval worden bij de volgende afsluiting niet alle uitgiften gecorrigeerd in de juiste kostprijs, omdat er onvoldoende ontvangstgegevens beschikbaar zijn. 

Voor elke uitvoering van de afsluitingsprocedure geeft het systeem aan of een logboek met de waarschuwingen is opgeslagen en kan worden weergegeven. 

Als u veel waarschuwingen in het bericht ontvangt, is het raadzaam de volgende acties te ondernemen:

-   Werk ontvangsten financieel bij.
-   Haal de afsluitdatum naar voren.
-   Herzie de zakelijke procedures.

Er kunnen omstandigheden zijn waarin het niet mogelijk is om iets aan de waarschuwingen te doen. Als er bijvoorbeeld markering wordt toegepast waarbij de gemarkeerde inkooporder een financiële datum heeft na de afsluitdatum, kan de afsluitdatum niet worden gewijzigd.

## <a name="reversing-a-completed-inventory-close"></a>Een voltooide voorraadafsluiting omkeren
Soms zult u een voltooide voorraadafsluiting moeten omkeren en de vereffeningen weer moeten instellen zoals deze waren voordat er correcties werden doorgevoerd. Wanneer u een voltooide voorraadafsluiting omkeert, wordt de voorraad opnieuw geopend en kan die in de periode die door de voorraadafsluiting wordt gedekt, worden geboekt. U kunt ook gerelateerde wijzigingen maken in het grootboek. Nadat u de aanpassingen hebt gemaakt, kunt u de voorraadafsluiting nogmaals uitvoeren voor de periode waarmee u werkt. 

**Opmerking:** alleen de laatste afgesloten voorraadperiode kan opnieuw worden geopend. Als u een eerdere voorraadafsluiting wilt omkeren, moet u de volgende voorraadafsluitingen een voor een omkeren, te beginnen met de meest recente afsluiting.




