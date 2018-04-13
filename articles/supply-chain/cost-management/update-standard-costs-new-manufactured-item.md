---
title: Standaardkosten bijwerken voor een nieuw gefabriceerd artikel
description: Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten voor een nieuw gefabriceerd artikel.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1cfb04a98f7d01f7766bea97157ca3c44c51e326
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Standaardkosten bijwerken voor een nieuw gefabriceerd artikel

[!INCLUDE [banner](../includes/banner.md)]

Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten voor een nieuw gefabriceerd artikel. 

In de volgende richtlijnen wordt ervan uitgegaan dat u een methode met twee kostprijsberekeningsversies gebruikt voor het bijwerken van standaardkosten. Bij deze benadering bevat de ene kostprijsberekeningsversie de standaardkosten die oorspronkelijk waren gedefinieerd voor de bevriezingsperiode, en de tweede de incrementele updates die horen bij de nieuw gefabriceerde artikelen. De incrementele updates worden als kostenrecords ingevoerd in de tweede kostprijsberekeningsversie, en uiteindelijk ingeschakeld. De methode met twee kostprijsberekeningsversies vereist dat u een tweede kostprijsberekeningsversie definieert. Dit zijn de richtlijnen voor het definiëren van deze kostprijsberekeningsversie:

-   Wijs een kostprijsberekeningstype **Standaardkosten** toe.
-   Wijs een significante id aan de kostprijsberekeningsversie toe die iets zegt over de inhoud, bijvoorbeeld **2016-UPDATES**.
-   In de **Prijstype toestaan**-veldgroep moet u ervoor zorgen dat **Kostprijs** is ingesteld op **Ja**.
-   Sta toe dat kostenrecords voor alle sites kunnen worden ingevoerd (dat wil zeggen laat het veld **Site** leeg). Als u een site opgeeft, kunnen alleen kostenrecords voor die site worden ingevoerd.
-   Gebruik een terugvalprincipe **Actief**.

Als u nieuwe productieartikelen wilt toevoegen tijdens de bevriezingsperiode, volgt u de volgende stappen.

1.  Gebruik de pagina **Kostprijsberekeningsversie** om kostenrecords in te schakelen die in de tweede kostprijsberekeningsversie met de incrementele updates moeten worden ingevoerd. Voorkom de activering van kosten die in behandeling zijn, waarbij activering is toegestaan nadat de kosten die in behandeling zijn volledig en correct zijn gedefinieerd. Geef een lege vanaf-datum als beleid op in de kostprijsberekeningsversie en geef de vanaf-datum vervolgens op wanneer u elke kostenrecord invoert. De vanaf-datum moet een datum zijn die valt voordat de nieuwe artikelen worden ingekocht of gefabriceerd.
2.  Gebruik de pagina **Artikelprijs** om kostenrecords in te voeren voor nieuw ingekochte artikelen. Voer voor elke kostenrecord de kostprijsberekeningsversie in die incrementele updates bevat, en gebruik een vanaf-datum die vóór de verwachte productiedatum van nieuw gefabriceerde artikelen valt.
3.  Bereken de kosten van nieuw gefabriceerde artikelen met behulp van de pagina **Berekening**. Open de pagina **Berekening** vanaf de pagina **Onderhoud kostprijsberekeningsversie**, en selecteer vervolgens de kostprijsberekeningsversie die de incrementele updates bevat. Gebruik de selectiecriteria om het nieuw gefabriceerde artikel en eventuele bijbehorende gefabriceerde onderdelen op te geven. In een productstructuur met meerdere niveaus moet u mogelijk ook het bovenliggende artikel opgeven dat de nieuwe gefabriceerde artikelen als een onderdeel bevat. Geef voor de stuklijstberekening een vanaf-datum op die overeenkomt met de begindatum van de productie voor de nieuw gefabriceerde artikelen. De vanaf-datum moet vallen tussen de begin- en einddatum voor de stuklijstversie en de routeversie van het artikel. **Opmerking:** Een ontbrekende kostenrecord kan duiden op een nieuw gefabriceerd artikel. Stuklijstberekeningen kunnen worden beperkt tot artikelen met ontbrekende kosten.
4.  Controleer de volledigheid en nauwkeurigheid van de berekende kosten voor nieuw gefabriceerde artikelen. Gebruik de pagina **Voltooid** om de berekende kosten te controleren voor het kostenrecord van elk artikel en eventuele Infologboek met waarschuwingsberichten. Of gebruik de pagina **Berekening** om de berekende kosten te controleren.
5.  Gebruik de pagina **Instellingen kostprijsberekeningsversie** om de blokkeringsvlag te wijzigen om de activering toe te staan van de kostenrecords die in behandeling zijn en die deel uitmaken van de tweede kostprijsberekeningsversie.
6.  Gebruik de pagina **Prijzen activeren** (die u opent vanaf de pagina **Onderhoud kostprijsberekeningsversie**) om alle in behandeling zijnde artikelkostenrecords in de tweede kostprijsberekeningsversie in te schakelen. U kunt ook de kostenrecords die in behandeling zijn voor afzonderlijke artikelen, inschakelen door op de knop **Activeren** te klikken op de pagina **Artikelprijs**.
7.  Gebruik de pagina **Instellingen kostprijsberekeningsversie** om de blokkeringsvlaggen in de tweede kostprijsberekeningsversie te wijzigen om extra gegevensonderhoud te voorkomen. Met het blokkeringsbeleid voorkomt u de invoer van nieuwe kosten die in behandeling zijn en de activering van kosten die in behandeling zijn.





