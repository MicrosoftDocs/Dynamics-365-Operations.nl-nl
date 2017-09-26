---
title: Kostenwijzigingen simuleren via een kostprijsberekeningsversie voor geplande kosten
description: In dit artikel wordt uitgelegd hoe u de effecten van kostenwijzigingen op de berekende kosten van een gefabriceerd artikel simuleert met een aparte kostprijsberekeningsversie voor geplande kosten.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 07dc838b38b060d45930a24b13be3dc283457282
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Kostenwijzigingen simuleren via een kostprijsberekeningsversie voor geplande kosten

[!include[banner](../includes/banner.md)]


In dit artikel wordt uitgelegd hoe u de effecten van kostenwijzigingen op de berekende kosten van een gefabriceerd artikel simuleert met een aparte kostprijsberekeningsversie voor geplande kosten.

U kunt de effecten van kostenwijzigingen op de berekende kosten van een gefabriceerd artikel simuleren met een aparte kostprijsberekeningsversie voor geplande kosten. Gebruik deze aparte kostprijsberekeningsversie voor het invoeren van kostenrecords die in behandeling zijn en incrementele kostenwijzigingen reflecteren, en voor het berekenen van het kosteneffect op gefabriceerde artikelen. Aangezien het terugvalprincipe van actieve kosten wordt gebruikt in de stuklijstberekeningen, hoeven alleen de incrementele kostenwijzigingen te worden ingevoerd.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Richtlijnen om de gesimuleerde kostprijsberekeningsversie te definiëren
Volg de onderstaande richtlijnen wanneer u de kostprijsberekeningsversie voor simulaties definieert.

-   Wijs een kostprijsberekeningstype van **Geplande kosten** toe.
-   Wijs een omschrijvende id voor de kostprijsberekeningsversie toe, zoals **Simulatie**.
-   Controleer of de inhoud kostenrecords bevat.
-   Sta de invoer van kostenrecords toe. Blokkeer de invoer van kosten die in behandeling zijn niet.
-   Sta de invoer van kostenrecords toe voor alle sites. Wanneer u een site opgeeft, wordt het invoeren van kostenrecords beperkt tot die site.
-   Verhinder de activering van kosten die in behandeling zijn. Voor kostenrecords in de gesimuleerde kostprijsberekeningsversie moeten alleen kosten worden ingevoerd die in behandeling zijn.
-   Voer geen begindatum in. Er wordt een berekeningsdatum ingevoerd voor elke stuklijstberekening die de gesimuleerde kostprijsberekeningsversie gebruikt.
-   Geef het terugvalprincipe **Huidige actief** op. Door het terugvalprincipe kunnen incrementele kostenwijzigingen worden ingevoerd voor simulatiedoeleinden, terwijl de huidige actieve kosten worden gebruikt als de bron voor alle andere kostenrecords. Hierbij wordt ervan uitgegaan dat alle huidige actieve kosten bestaan voor alle andere kostenrecords.
-   Geef een kostprijsmodel van **Versiekostprijs** op, maar beperk berekeningen niet. De simulaties kunnen bijvoorbeeld ook het kostprijsmodel **Stuklijstberekeningsgroep** gebruiken om de bron van kostbijdragegegevens voor ingekochte artikelen aan te geven.
-   Geef het explosiemodel **Meerdere niveaus** aan, maar beperk berekeningen niet. De simulaties kunnen andere explosiemodi gebruiken.

## <a name="costing-versions"></a>Kostprijsberekeningsversies
De volgende scenario's illustreren hoe de simulatiekostprijsberekeningsversie wordt gebruikt om het effect van kostenwijzigingen te simuleren. Voordat u een gesimuleerde kostenwijziging invoert, verwijdert u de kostenrecords die in behandeling zijn in de simulatiekostprijsberekeningsversie, zodat u met een schone lei begint. Gebruik de pagina **Artikelprijs** om de kostenrecords die in behandeling zijn en betrekking hebben op artikelprijzen en kostencategorieprijzen, weer te geven en te verwijderen.

-   Simuleer de kostenwijziging voor een ingekocht artikel. De kostenwijziging kan bijvoorbeeld een verwachte verhoging of verlaging in de kosten van kritieke ingekochte materialen weerspiegelen. Als u de verschillende kosten voor een ingekocht artikel wilt definiëren, gebruikt u de pagina **Artikelprijs** om een kostenrecord die in behandeling is, in te voeren in de simulatiekostprijsberekeningsversie.
-   Simuleer de kostenwijziging voor een kostencategorie. De kostenwijziging kan bijvoorbeeld een verwachte verhoging of verlaging in arbeidstarieven of in de uurtarieven voor bronnen voor bedrijfsactiviteiten weerspiegelen. Als u de verschillende kosten voor een kostencategorie wilt definiëren, gebruikt u de pagina **Kostencategorieprijs** om een kostenrecord die in behandeling is, in de simulatiekostprijsberekeningsversie in te voeren.
-   Simuleer de kostenwijziging in een berekeningsformule voor indirecte kosten. De kostenwijziging kan bijvoorbeeld een verwachte verhoging of verlaging in productieoverhead weerspiegelen. Als u de wijziging in een berekeningsformule van indirecte kosten wilt definiëren, gebruikt u de pagina **Instellingen kostenblad** om een kostenrecord die in behandeling is, in de simulatiekostprijsberekeningsversie in te voeren, en om de wijziging te valideren en op te slaan.

Nadat u de gesimuleerde kostenwijzigingen hebt ingevoerd, berekent u de kosten voor gefabriceerde artikelen waarvoor de kostenwijzigingen gevolgen hebben. Gebruik de pagina **Berekening** voor de simulatiekostprijsberekeningsversie, en geef de geselecteerde gefabriceerde artikelen aan waarvoor de kostenwijzigingen gevolgen zullen hebben. De stuklijstberekeningen zijn van toepassing op alle gefabriceerde artikelen, tenzij u specifieke artikelen selecteert. U kunt de stuklijstberekeningsoptie ook gebruiken voor updates van gebruikslocaties. Geef de artikelkostenrecords in de simulatiekostprijsberekeningsversie weer om te analyseren hoe de gesimuleerde kostenwijzigingen van invloed zijn op de kosten van de geselecteerde gefabriceerde artikelen. Gebruik de pagina **Artikelprijs** en de pagina **Artikelkosten berekenen** om de kosten weer te geven en te analyseren.




