---
title: Standaardkosten in een niet-productieomgeving bijwerken
description: Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een niet-productieomgeving.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0386ca1e5e7bf6e578ba2abf1b2c9eefe4dd2a02
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Standaardkosten in een niet-productieomgeving bijwerken

[!include[banner](../includes/banner.md)]


Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een niet-productieomgeving.

In de volgende richtlijnen wordt ervan uitgegaan dat u een methode met twee kostprijsberekeningsversies gebruikt voor het bijwerken van standaardkosten. Bij deze methode bevat één kostprijsberekeningsversie de standaardkosten die oorspronkelijk zijn gedefinieerd voor de bevriezingsperiode en de tweede kostprijsberekeningsversie bevat de incrementele updates. Elke update wordt als een kostenrecord ingevoerd die is ingesloten in de tweede kostprijsberekeningsversie en wordt uiteindelijk geactiveerd. In een alternatieve methode met één kostprijsberekeningsversie wordt de oorspronkelijke gedefinieerde verzameling standaardkosten gebruikt. De methode met twee kostprijsberekeningsversies vereist dat u een tweede kostprijsberekeningsversie definieert. Dit zijn de richtlijnen voor het definiëren van deze kostprijsberekeningsversie:

-   Wijs het kostprijsberekeningstype **Standaardkosten** toe.
-   Wijs een significante id aan de kostprijsberekeningsversie toe die iets zegt over de inhoud, bijvoorbeeld **2016-UPDATES**.
-   Controleer of de inhoud kostenrecords bevat.
-   Sta de invoer van kostenrecords toe voor alle sites. Als u een site opgeeft, kunnen alleen kostenrecords voor die site worden ingevoerd.
-   Stel het terugvalprincipe **Geen** in. Het terugvalprincipe is alleen van toepassing op kostenberekeningen voor gefabriceerde artikelen.

Als u de standaardkosten voor nieuwe artikelen wilt corrigeren, aanpassen of bijwerken, gaat u als volgt te werk.

1.  Gebruik de pagina **Instellingen** **kostprijsberekeningsversie** om kostengegevens in te schakelen die in de tweede kostprijsberekeningsversie moeten worden ingevoerd. Voorkom desgewenst de activering van kosten die in behandeling zijn, zodat activering pas is toegestaan nadat de kosten die in behandeling zijn, volledig en correct zijn gedefinieerd. U kunt desgewenst ook een datum in het veld **Begindatum** invoeren. Normaal gesproken kunt u het beste de datum gebruiken vanaf wanneer u de incrementele updates wilt activeren. U kunt ook het veld **Begindatum** leeg laten voor de kostprijsberekeningsversie en vervolgens een datum invoeren in het veld **Begindatum** voor elke kostprijsrecord.
2.  Gebruik de pagina **Artikelprijs** als u updates als artikelkostenrecords wilt invoeren die zijn ingesloten in de tweede kostprijsberekeningsversie.
3.  Gebruik het rapport **Artikelprijzen** als u de nauwkeurigheid en volledigheid van de artikelkostenrecords wilt opgeven die zijn ingesloten in de tweede kostprijsberekeningsversie.
4.  Gebruik het formulier **Onderhoud kostprijsberekeningsversie** om de blokkeringsvlag te wijzigen om activering toe te staan van kostenrecords die in behandeling zijn en die zijn ingesloten in de tweede kostprijsberekeningsversie.
5.  Gebruik de pagina **Prijzen activeren** (die u opent vanaf de pagina **Onderhoud kostprijsberekeningsversie**) om alle artikelkostenrecords die in behandeling zijn en die zijn ingesloten in de tweede kostprijsberekeningsversie, te activeren. U kunt ook de kostenrecords die in behandeling zijn voor afzonderlijke artikelen, activeren door op de knop **Activeren** te klikken op de pagina **Artikelprijs**.
6.  Gebruik de pagina **Instellingen kostprijsberekeningsversie** om de blokkeringsvlaggen te wijzigen die zijn ingesloten in de tweede kostprijsberekeningsversie. Met het blokkeringsbeleid voorkomt u de invoer van nieuwe kosten die in behandeling zijn en de activering van kosten die in behandeling zijn.





