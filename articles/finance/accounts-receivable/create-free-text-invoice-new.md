---
title: Een vrije-tekstfactuur invoeren
description: In dit onderwerp wordt uitgelegd hoe u vrije-tekstfacturen maakt.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 726d4979059417871a00626c55da32fa4286cb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991112"
---
# <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u vrije-tekstfacturen maakt. Gebruik voor de procedure het demobedrijf **USMF**.

## <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

1. Ga naar **Klanten (of Verkoopgrootboek) \> Facturen \> Alle vrije-tekstfacturen**.
2. Selecteer **Nieuw**.
3. Selecteer een waarde in het veld **Klantrekening**.

    * De rekening die als de klantrekening wordt geselecteerd, wordt standaard als de factuurrekening gebruikt.
    * De boekhoudstatus begint met **Onderhanden** als de factuur niet is geboekt.
    * Het factuurnummer wordt toegewezen wanneer de factuur wordt geboekt.
    * Als u SEPA-mandaten (Single Euro Payments Area) gebruikt, wordt het mandaat voor automatische afschrijving automatisch ingevoerd wanneer u de klantrekening selecteert.

4. Voer een waarde in het veld **Beschrijving** in.
5. Geef in het veld **Hoofdrekening** een rekeningnummer op dat geen dimensies heeft. Verderop in dit onderwerp gaat u dimensies invoeren.

    U kunt ook een of meerdere tekens voor de hoofdrekening invoeren en de zoekopdracht gebruiken om uw rekening te zoeken.

6. Selecteer het sneltabblad **Regeldetails** om dimensies aan de hoofdrekening toe te voegen.
7. Selecteer het tabblad **Financiële dimensieregel**.

    * De dimensies gelden uitsluitend voor de geselecteerde regel.
    * De btw-groep wordt overgenomen van de klant. Als de klant geen btw-groep heeft, wordt de btw-groep van de hoofdrekening gebruikt.
    * De btw-groep van het artikel wordt overgenomen van de hoofdrekening. Als de hoofdrekening geen btw-groep voor het artikel heeft, wordt de in de btw-parameters in het grootboek opgegeven btw-groep voor het artikel gebruikt.

8. Optioneel: voer in het veld **Hoeveelheid** een getal in.
9. Optioneel: voer een getal in het veld **Eenheidsprijs** in.

    Het bedrag wordt berekend als de hoeveelheid keer de eenheidsprijs. U kunt die berekening echter negeren door een bedrag in te voeren.

10. Selecteer **Btw** om de voor de factuur berekende btw te bekijken.

    U kunt de btw-bedragen op deze pagina bekijken of u kunt de bedragen op het tabblad **Correctie** negeren.

11. Selecteer **OK**.
12. Selecteer **Toeslagen** om een toeslag aan de factuur toe te voegen.
13. Voer een waarde in het veld **Toeslagcode** in.
14. Voer een getal in het veld **Waarde van toeslagen** in.
15. Sluit de pagina.
16. Selecteer **Totalen** om een overzicht van de factuurdetails en -totalen weer te geven.
17. Selecteer **Sluiten**.
18. Selecteer **Boeken** om de factuur te boeken. U hebt nog altijd een mogelijkheid om te annuleren voordat u werkelijk boekt.

    * U kunt de timing van het afdrukken van facturen wijzigen. Selecteer **Huidige** om elke factuur af te drukken wanneer deze wordt bijgewerkt. Selecteer **Na** om af te drukken nadat alle facturen zijn bijgewerkt.
    * Als u wilt wijzigen hoe de kredietlimiet van de klant wordt gecontroleerd voordat de factuur wordt geboekt, wijzigt u de waarde in het veld **Kredietlimiettype**.
    * Als u de factuur wilt afdrukken, stelt u de optie in op **Ja**.
    * Als u de factuur wilt boeken, stelt u de optie in op **Ja**. U kunt de factuur afdrukken zonder deze te boeken.

19. Selecteer **OK**.

## <a name="copy-lines"></a>Regels kopiëren
Als u regels in een vrije-tekstfactuur wilt kopiëren, selecteert u een of meer regels en selecteert u vervolgens **Geselecteerde regels kopiëren**. U kunt opgeven hoeveel kopieën u wilt maken en u kunt ook notities en bijlagen kopiëren. U kunt de verdelingen kopiëren of opnieuw laten maken wanneer u boekt.

Nadat u de regels hebt gekopieerd, kunt u de gegevens zo nodig bewerken.

## <a name="create-a-free-text-invoice-from-a-template"></a>Een vrije-tekstfactuur maken op basis van een sjabloon
U kunt een vrije-tekstfactuur maken op basis van een sjabloon. Wanneer u **Nieuw van sjabloon** op het tabblad **Factuur** selecteert, kunt u een sjabloonnaam en de klantrekening voor de nieuwe vrije-tekstfactuur selecteren. Standaardwaarden, zoals de betalingsvoorwaarden en betalingsmethode, kunnen automatisch van de klant worden overgenomen, of u kunt de waarden gebruiken die zijn opgeslagen in de sjabloon.

Er wordt een nieuwe vrije-tekstfactuur gemaakt en u kunt de waarden indien nodig bewerken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]