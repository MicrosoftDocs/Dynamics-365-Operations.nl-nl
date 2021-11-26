---
title: Herwaardering voor vreemde valuta van bank
description: Dit onderwerp biedt een overzicht van het proces voor herwaardering voor vreemde valuta van bank. Dit onderwerp bevat informatie over instellingen, de uitvoering van het proces, de berekening voor het proces en de omkering van herwaarderingstransacties.
author: roschlom
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3df6a22e06abbfa75a12ffddac242dd34f5beba5
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2021
ms.locfileid: "7754115"
---
# <a name="bank-foreign-currency-revaluation"></a>Herwaardering voor vreemde valuta van bank

[!include [banner](../includes/banner.md)]


Dit onderwerp biedt een overzicht van het proces voor herwaardering voor vreemde valuta van bank. In dit onderwerp wordt uitgelegd hoe u het proces kunt instellen en uitvoeren en geeft informatie over de berekening voor het proces. Ook wordt uitgelegd hoe u herwaarderingstransacties kunt omkeren als omkering vereist is.

Als onderdeel van een periode-einde vereisen de boekhoudconventies dat bankrekeningsaldo's in vreemde valuta worden geherwaardeerd met verschillende typen wisselkoersen (huidig, historisch, gemiddeld, enzovoort). De functie voor herwaardering van vreemde valuta van de bank kan worden gebruikt om een of meer bankrekeningen te herwaarderen. De functie is ook een globale functie. U kunt daarom via één pagina banken herwaarderen voor alle rechtspersonen waartoe u toegang hebt.

> [!NOTE]
> Wanneer u het herwaarderingsproces uitvoert, wordt het saldo in elke bankrekening die in een vreemde valuta is geboekt, geherwaardeerd. De niet-gerealiseerde winst- en verliestransacties die worden gemaakt tijdens het herwaarderingsproces worden door het systeem gegenereerd. Er kunnen twee transacties worden gemaakt, één voor de valuta voor boekhouding en één voor de aangiftevaluta, indien van toepassing. Elke journaalregel wordt geboekt naar de niet-gerealiseerde winst/verlies en de hoofdrekening die wordt geherwaardeerd.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Voorbereiding van herwaardering van vreemde valuta

Voordat u het herwaarderingsproces kunt uitvoeren, zijn de volgende instellingen vereist.

- Geef op de pagina **Grootboek** het wisselkoerstype op. Als geen wisselkoerstype is gedefinieerd voor de hoofdrekening, wordt dit wisselkoerstype gebruikt tijdens de herwaardering van vreemde valuta.
- Geef op de pagina **Grootboek** de rekeningen op voor gerealiseerde winst, gerealiseerd verlies, niet-gerealiseerde winst en niet-gerealiseerd verlies voor herwaardering van valuta. Gerealiseerde winst- en gerealiseerde verliesrekeningen worden gebruikt wanneer klanten- en leverancierstransacties worden vereffend. Niet-gerealiseerde winst- en verliesrekeningen worden gebruikt voor het herwaarderen van openstaande transacties en grootboekhoofdrekeningen.
- Selecteer op de pagina **Rekeningen voor valutaherwaardering** de verschillende rekeningen voor valutaherwaardering voor elke valuta en elk bedrijf. Als u geen rekeningen hebt gedefinieerd, worden rekeningen van de pagina **Grootboek** gebruikt.

## <a name="enable-foreign-currency-revaluation"></a>Herwaardering van vreemde valuta inschakelen

U moet de functie voor herwaardering van vreemde valuta voor de bank inschakelen voordat u herwaarderingen van vreemde valuta kunt verwerken.

1. Ga naar **Contanten en bankbeheer \> Instellen \> Parameters voor Contanten en bankbeheer**.
2. Stel op het tabblad **Algemeen** onder **Herwaardering van vreemde valuta** de optie **Herwaardering bank instellen** in op **Ja** om de functie voor de huidige rechtspersoon in te schakelen. 
3. Voeg op het tabblad **Nummerreeksen** een nummerreeks voor herwaardering van vreemde valuta toe.
4. Vernieuw de browser om **Herwaardering van vreemde valuta** in de sectie **Periodieke taken** van de gebiedspagina te zien.

U moet de functie inschakelen voor elke rechtspersoon die herwaardering van vreemde valuta gebruikt. Als u bent toegewezen aan de rol van systeembeheerder of functiebeheerder, kunt u deze stap overslaan door de functie met de naam **Herwaardering bank inschakelen zonder parameter** in het werkgebied **Functiebeheer**.

> [!NOTE]
> Als uw rechtspersoon een Russische, Poolse of Hongaarse land-/regiocode gebruikt, kunt u al herwaardering van vreemde valuta voor de bank uitvoeren. U kunt de herwaardering van vreemde valuta die wordt gebruikt door andere landen of regio's, niet gebruiken.

## <a name="process-foreign-currency-revaluation"></a>Herwaardering van vreemde valuta verwerken

Nadat de instelling is voltooid, gebruikt u de pagina **Herwaardering van vreemde valuta** in Contanten en bankbeheer voor de herwaardering van een of meer bankrekeningen voor alle rechtspersonen. U kunt het proces in realtime uitvoeren of inplannen om het in batch uit te voeren.

Op de pagina **Herwaardering van vreemde valuta** wordt de historie van elk herwaarderingsproces weergegeven. De historie geeft aan wanneer het proces is uitgevoerd en welke criteria zijn gedefinieerd, en de historie bevat een koppeling naar het boekstuk dat is gemaakt voor de herwaardering. Ook ziet u of een vorige herwaardering is omgekeerd. Als u het herwaarderingsproces wilt uitvoeren, selecteert u **Herwaardering van vreemde valuta** in het actievenster om het dialoogvenster **Bank - herwaardering van vreemde valuta** te openen.

In het veld **Datum herwaardering** wordt de afsluitdatum gedefinieerd voor het berekenen van het saldo in vreemde valuta dat wordt geherwaardeerd. De som van alle banktransacties die hebben plaatsgevonden tot en met deze datum wordt geherwaardeerd.

Met het veld **Wisselkoersdatum** wordt de datum van de wisselkoers gedefinieerd die wordt gebruikt om de valutasaldi te herwaarderen. U kunt bijvoorbeeld de saldi vanaf 31 januari herwaarderen, maar de wisselkoers gebruiken die is gedefinieerd voor 1 februari.

Het herwaarderingsproces kan voor een of meer rechtspersonen worden uitgevoerd. Met de zoekopdracht worden alleen de rechtspersonen weergegeven waartoe u toegang hebt. Selecteer de rechtspersonen waarvoor u de bankrekeningen wilt selecteren die in aanmerking komen voor herwaardering van vreemde valuta. Alle bankrekeningen voor deze rechtspersonen worden weergegeven in het raster.

Stel de optie **Bekijken alvorens te boeken** in op **Ja** als u de resultaten van de herwaardering wilt bekijken voordat u deze boekt. De herwaardering van vreemde valuta heeft een voorbeeld dat kan worden geboekt. U hoeft het herwaarderingsproces niet opnieuw uit te voeren. U kunt de resultaten in het voorbeeld exporteren naar Microsoft Excel om een de historie te bewaren van de wijze waarop de bedragen zijn berekend. U kunt geen batchverwerking gebruiken als u een voorbeeld van de herwaarderingsresultaten wilt bekijken.

Selecteer **OK** om de herwaardering van vreemde valuta te verwerken. Er wordt ook een record gemaakt voor het bijhouden van de historie van elke uitvoering. Er wordt een afzonderlijke record gemaakt voor elke rechtspersoon en boekingslaag.

## <a name="calculate-unrealized-gainloss"></a>Niet-gerealiseerde winst/verlies berekenen

In Contanten en bankbeheer wordt de bankvaluta beschouwd als zijnde de basisvaluta en wordt deze niet geherwaardeerd. Het saldo van de bankrekening in de valuta voor boekhouding wordt geherwaardeerd met de wisselkoersen tussen de bankvaluta en de valuta voor boekhouding op de **Wisselkoersdatum**. Het saldo van de bankrekening in de valuta voor boekhouding wordt ook geherwaardeerd met de wisselkoersen tussen de bankvaluta en de valuta voor boekhouding op de **Wisselkoersdatum**.

Er wordt een transactie gemaakt voor het verschil tussen het saldo van de bankrekening en het nieuwe saldo dat wordt berekend voor de valuta voor boekhouding. Een andere transactie wordt gemaakt voor het verschil tussen het saldo van de bankrekening en het nieuwe saldo dat wordt berekend voor de aangiftevaluta. De posten voor deze transacties worden gemarkeerd als afgestemd. 

Er wordt geen invoer gemaakt voor de valuta voor boekhouding als de bankvaluta overeenkomt met de valuta voor boekhouding. Zo ook wordt er geen invoer gemaakt voor de aangiftevaluta als de bankvaluta overeenkomt met de aangiftevaluta.

De herwaarderingstransactie voor vreemde valuta wordt ook gesplitst voor de dimensies die aanwezig zijn in de banktransacties. De splitsing wordt gebaseerd op het saldo voor elke dimensie. Bijvoorbeeld: het totale banksaldo is 10.000, maar het saldo voor de business unit 001 is 4000, terwijl het saldo voor business unit 002 6.000 is. In dit geval wordt 40 procent van het bedrag van de herwaardering geboekt naar de herwaarderingsrekening die business unit 001 heeft, en 60 procent wordt geboekt naar de herwaarderingsrekening die business unit 002 heeft. Als de rekeningstructuur geen business unit bevat, wordt het volledige bedrag geboekt naar de herwaarderingsrekening.

## <a name="reverse-foreign-currency-revaluation"></a>Herwaardering van vreemde valuta omkeren

Als u de herwaarderingtransactie moet omkeren, selecteert u **Transactie omkeren** in het actievenster van de pagina **Herwaardering van vreemde valuta**. Er wordt een nieuw historisch record voor herwaardering van vreemde valuta gemaakt om de historische audittrail te onderhouden voor wanneeer de herwaardering heeft plaatsgevonden of is omgekeerd.

Als u omkeren verschillende herwaarderingen wilt omkeren, moet u eerst de meest recente herwaardering omkeren. Vervolgens gaat u verder met het omkeren van oudere herwaarderingen in volgorde van datum. U kunt vervolgens nieuwe herwaarderingen verwerken voor de perioden die u hebt omgekeerd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
