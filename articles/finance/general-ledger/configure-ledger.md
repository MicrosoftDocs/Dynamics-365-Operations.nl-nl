---
title: Grootboeken configureren
description: Dit onderwerp bevat informatie over het configureren van grootboeken voor elke rechtspersoon. Het bevat informatie over het selecteren van valuta's, fiscale kalenders, het rekeningschema en de rekeningstructuren die bij elke rechtspersoon moeten worden gebruikt.
author: kweekley
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: aad10770750d2614da804380a7bba03d348e8c9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826198"
---
# <a name="configure-ledgers"></a>Grootboeken configureren

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over het configureren van grootboeken voor elke rechtspersoon. Het bevat informatie over het selecteren van valuta's, fiscale kalenders, het rekeningschema en de rekeningstructuren die bij elke rechtspersoon moeten worden gebruikt.

## <a name="selecting-the-chart-of-accounts"></a>Het rekeningschema selecteren

Voor elke rechtspersoon in Microsoft Dynamics 365 Finance moeten details over het grootboek worden geconfigureerd. Op de pagina **Grootboek** kunt u het rekeningschema en de rekeningstructuren selecteren die voor de geselecteerde rechtspersoon worden gebruikt. U kunt uw rekeningschema en de rekeningstructuren delen door de pagina **Grootboek** in elke rechtspersoon te configureren om hetzelfde rekeningschema en dezelfde rekeningstructuren te gebruiken. U kunt ook een deel van de configuratie met alle rechtspersonen delen en specifieke configuraties in elke rechtspersoon hebben.

Als uw rechtspersonen verschillende rekeningschema's of verschillende rekeningstructuren moeten hebben, kan de functie voor het overschrijven van de rechtspersoon nuttig zijn. Door hetzelfde rekeningschema en dezelfde rekeningstructuren voor meerdere rechtspersonen te gebruiken en vervolgens uitzonderingen te beheren via overschrijvingen van rechtspersonen, kunt u het onderhoud in de loop van de tijd vereenvoudigen.

Als u het rekeningschema voor een rechtspersoon wilt configureren, gaat u naar **Grootboek \> Grootboek instellen \> Grootboek**. Selecteer **Rekeningschema's** op de pagina **Grootboek** en selecteer vervolgens in de lijst het rekeningschema dat u wilt gebruiken. Houd er rekening mee dat het rekeningschema niet kan worden gewijzigd nadat u een waarde hebt geselecteerd en transacties in de rechtspersoon hebt geboekt.

Zie [Rekeningschema plannen](plan-chart-of-accounts.md) voor meer informatie over het plannen en configureren van het rekeningschema en de hoofdrekeningen.

## <a name="selecting-account-structures"></a>Rekeningstructuren selecteren

Elke rechtspersoon in Dynamics 365 Finance kan worden geconfigureerd voor het gebruik van een of meer rekeningstructuren. Elke rekeningstructuur definieert de financiële dimensies en de combinaties van hoofdrekeningen en financiële dimensies die worden toegestaan wanneer transacties worden geboekt. U kunt dezelfde rekeningstructuren in meer dan één rechtspersoon gebruiken.

Als u meerdere rekeningstructuren hebt, kunt u alleen rekeningstructuren selecteren die geen overlappende combinaties van hoofdrekeningen en financiële dimensies hebben. Een van uw rekeningstructuren is bijvoorbeeld geconfigureerd om een bedrijfseenheid toe te voegen voor hoofdrekeningen tussen 1000 en 1999. In een andere rekeningstructuur hebt u een financiële dimensie voor de afdeling toegevoegd voor hoofdrekeningen die met 1 beginnen. In dit geval kan slechts één van de rekeningstructuren aan dezelfde rechtspersoon worden toegevoegd.

Als u rekeningstructuren wilt configureren voor het grootboek, klikt u op de pagina **Grootboek** op het sneltabblad **Rekeningstructuren** op **Toevoegen**, selecteert u een rekeningstructuur in de lijst en vervolgens **Selecteren**. Het kan enkele minuten duren voordat de rekeningstructuren zijn toegevoegd en opgeslagen. De rekeningstructuren die u selecteert, moeten actief zijn. Anders zijn de details van de rekeningstructuren niet effectief in de rechtspersonen waaraan ze zijn gekoppeld.

Als u een rekeningstructuur wilt verwijderen, selecteert u op het sneltabblad **Rekeningstructuren** op de pagina **Grootboek** de optie **Verwijderen**. Als u een rekeningstructuur uit het grootboek verwijdert, verwijdert u geen transacties die zijn geboekt met behulp van de configuratie van die rekeningstructuur.

Zie [Rekeningstructuren configureren](configure-account-structures.md) voor meer informatie over het instellen van uw rekeningstructuren.

## <a name="configuring-calendars-for-the-ledger"></a>Kalenders voor grootboek configureren

Een andere component van het grootboek is de fiscale kalender. Voor elke rechtspersoon moet een fiscale kalender worden geselecteerd. U kunt dezelfde fiscale kalender in meer dan één rechtspersoon gebruiken. Wanneer u een fiscale kalender voor het grootboek selecteert, wordt er een kopie gemaakt. Deze kopie wordt de grootboekkalender genoemd. Met de grootboekkalender kunt u de status van de perioden en de modules in elke periode selecteren.

Als u de kalender voor de geselecteerde rechtspersoon wilt openen en bijwerken, selecteert u op de pagina **Grootboek** in het actievenster de optie **Grootboekkalender**.

Selecteer **Fiscale kalenders** en selecteer vervolgens de kalender in de lijst. Als u de fiscale kalender wijzigt nadat er transacties zijn geboekt in de rechtspersoon, selecteert u **Grootboekperioden herberekenen**. In het dialoogvenster dat wordt weergegeven, kunt u de grootboeksaldi voor de perioden in uw kalender bijwerken. U kunt het beste het proces **Grootboekperioden herberekenen** uitvoeren in de **batch** modus en op een tijdstip waarop niet-kritieke processen in het systeem plaatsvinden. Afhankelijk van het aantal transacties en combinaties van financiële dimensies kan dit proces enige tijd in beslag nemen.

Als er geen fiscale kalender is geselecteerd voor een rechtspersoon, wordt een foutbericht weergegeven wanneer u een transactie in die rechtspersoon probeert te boeken.

Zie voor meer informatie [Fiscale kalenders, boekjaren en boekperioden](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Een salderende financiële dimensie gebruiken

Nadat u het rekeningschema hebt geselecteerd en een of meer rekeningstructuren hebt toegevoegd, kunt u desgewenst één financiële dimensie selecteren om te gebruiken als salderende financiële dimensie. De dimensie die u selecteert, moet bestaan in alle rekeningstructuren. En deze moet ook in alle boekhoudingsposten worden gesaldeerd. Met andere woorden, de debet- en creditbedragen moeten gelijk zijn voor de hoofdrekening en de salderende financiële dimensie. Het systeem maakt automatisch transacties om de posten te salderen op basis van de hoofdrekeningen die zijn opgegeven in de velden **Interunit - credit** en **Interunit - debet** op de pagina **Rekeningen voor automatische transacties**.

Zie [Evenwichtige journalen voor interunit-boekhouding](example-balanced-journals-interunit-accounting.md) voor meer informatie over salderende posten.

## <a name="configuring-currencies-for-the-ledger"></a>Valuta's voor grootboek configureren

De pagina **Grootboek** wordt ook gebruikt voor het beheren en definiëren van de valuta die wordt gebruikt wanneer transacties naar het grootboek worden geboekt. U moet de valuta voor boekhouding opgeven. Dit is de valuta die in de kolom **Valuta voor boekhouding** in het grootboek wordt gebruikt in alle boekstukken. Bovendien kunt u in de kolom **Aangiftevaluta** desgewenst een tweede valuta selecteren. Als u een aangiftevaluta selecteert, worden alle transacties in deze valuta geregistreerd in de kolom **Aangiftevaluta** in het grootboek van alle boekstukken.

Als transacties in een andere valuta worden geboekt, wordt het transactiebedrag van de transactievaluta automatisch door het systeem geconverteerd naar de valuta voor boekhouding en de aangiftevaluta op het boekstuk. Selecteer op de pagina **Grootboek** in het veld **Wisselkoerstype valuta voor boekhouding** het type wisselkoers dat is geconfigureerd voor de wisselkoersen die moeten worden gebruikt voor het omrekenen van waarden van de transactievaluta naar de valuta voor boekhouding op een boekstuk. Als u een aangiftevaluta hebt geselecteerd, moet u ook het veld **Wisselkoerstype voor aangiftevaluta** instellen om de wisselkoers aan te geven die moet worden gebruikt voor het omrekenen van waarden van de transactievaluta naar de aangiftevaluta op een boekstuk.

Als u budgetfunctionaliteit gebruikt, kunt u ook het veld **Wisselkoerstype budget** instellen om de wisselkoers aan te geven die moet worden gebruikt om budgettransacties van de ene valuta naar de andere te converteren.

Als u twee valuta's gebruikt of als u één valuta gebruikt maar transacties worden geboekt in een andere valuta, moet u het sneltabblad **Rekeningen voor valutaherwaardering** op de pagina **Grootboek** configureren. Op dit sneltabblad definieert u de gerealiseerde en niet-gerealiseerde winst- en verliesrekeningen die standaard worden gebruikt wanneer transacties worden geboekt, als er geen rekening is opgegeven op de pagina **Rekeningen voor valutaherwaardering**. (De pagina **Rekeningen voor valutaherwaardering** wordt gebruikt om verschillende rekeningen voor gerealiseerde en niet-gerealiseerde winsten en verliezen voor elke valuta te configureren.)

Gerealiseerde winsten en verliezen zijn winsten en verliezen die zijn gemaakt op basis van voltooide transacties. Deze worden vastgelegd in de winst- en verliesrekening. Niet-gerealiseerde winsten en verliezen zijn winsten en verliezen die zijn gerealiseerd, maar waarvoor de transactie niet is voltooid. Met andere woorden: u hebt bijvoorbeeld een factuur geboekt, maar de factuur is nog niet vereffend en betaald. Niet-gerealiseerde winsten en verliezen worden op de balans geregistreerd.

Raadpleeg [Twee valuta's](dual-currency.md) voor meer informatie over het werken met twee valuta's.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]