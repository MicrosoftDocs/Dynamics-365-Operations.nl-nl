---
title: Leases in vreemde valuta registreren
description: In dit onderwerp wordt uitgelegd hoe u leases in andere valuta's kunt vastleggen dan de boekhoudings- of aangiftevaluta.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 91bf3f91614f0dd4835c253456128c9ced046749c0e13383590e01dfd436c921
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766332"
---
# <a name="record-leases-in-foreign-currencies"></a>Leases in vreemde valuta registreren

[!include [banner](../includes/banner.md)]

Activaleaserekeningen voor leases in andere valuta's dan de boekhoudingsvaluta of de aangiftevaluta worden ingesteld op de pagina **Grootboek instellen**. Alle leases moeten in de transactievaluta worden ingevoerd. Met andere woorden, ze moeten worden ingevoerd in de valuta die is opgegeven in het leasecontract. In dit onderwerp wordt uitgelegd hoe u leases in andere valuta's kunt vastleggen dan de boekhoudings- of aangiftevaluta.

Als u een lease invoert in een vreemde valuta, wordt de activa met gebruiksrecht afgeschreven in zowel de boekhoudvaluta als de aangiftevaluta. Deze valuta's worden geconfigureerd op de pagins **Grootboek instellen**. Dit gedrag wordt ook gebruikt voor vaste activa. Wanneer u een lease maakt in een vreemde valuta, selecteert u de transactievaluta in het veld **Valuta**.

De wisselkoers van de boekhoudvaluta is de standaardwaarde in het veld **Wisselkoers valuta voor boekhouding**. De wisselkoers van de aangiftevaluta is de standaardwaarde in het veld **Wisselkoers voor aangiftevaluta**. Deze wisselkoersen waren van kracht op de aanvangsdatum van de lease. De velden **Wisselkoers valuta voor boekhouding** en **Wisselkoers voor aangiftevaluta** bevinden zich in het sneltabblad **Wisselkoersinformatie voor financiën en aangifte** op de pagina **Leasegegevens**.

1. Schakel het selectievakje **Vaste wisselkoers** in om de automatisch ingevoerde wisselkoers te negeren en voer vervolgens de nieuwe wisselkoers in.
2. Voer in de andere velden de vereiste informatie voor de lease in en selecteer vervolgens **Schema's maken**.
3. Selecteer op de pagina **Leasegegevens** de optie **Boeken**.
4. Controleer op de pagina **Leaseboek** op het tabblad **Wisselkoersinformatie voor financiën en aangifte** de waarden van de velden **Boekhoudingsvaluta initiële activum met gebruiksrecht** en **Aangiftevaluta initiële activum met gebruiksrecht**. Elk van deze velden bevat het vertaalde RoU-activumsaldo in de bijbehorende valuta. Deze velden worden bijgewerkt telkens wanneer u financiële gegevens wijzigt. Selecteer **Schema's maken** voordat u het betalingsschema bevestigt.

    In de eerste journaalboeking voor toerekening wordt het RoU-activum vastgelegd dat de wisselkoersen gebruikt die worden vermeld op de lease. De journaalboeking bevat ook de waarden van de velden **Boekhoudingsvaluta initiële activum met gebruiksrecht** en **Aangiftevaluta initiële activum met gebruiksrecht**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Opvolgende meting voor leases in vreemde valuta

Het afschrijvingsschema toont de verwachte afschrijvingsonkostenbedragen in de aangiftevaluta, de valuta voor de boekhouding en de transactievaluta.

Als u de RoU-activumsaldi en de afschrijvingsbedragen in de aangiftevaluta of de valuta voor boekhouding wilt weergeven, opent u de pagina **Afschrijvingsschema activa** en selecteert u het selectievakje **Valutabedrag voor boekhouding weergeven** of **Aangiftevalutabedrag weergeven**.

Wanneer u de journaalboekingen voor afschrijvingsonkosten maakt op basis van een lease die wordt uitgedrukt in een vreemde valuta, gebruikt de boeking de wisselkoersen die worden vermeld op de lease. De boeking gebruikt ook de waarden van de velden **Boekhoudingsvaluta initiële activum met gebruiksrecht** en **Aangiftevaluta initiële activum met gebruiksrecht**.

Het laatste afschrijvingsonkostenbedrag kan worden berekend met behulp van een iets andere wisselkoers, zodat het RoU-activum volledig is afgeschreven in zowel de valuta voor boekhouding als de aangiftevaluta.

Als de lease opnieuw is geclassificeerd als **Uitgestelde gebruiksvergoeding**, worden de wisselkoersen van de boekhoudingvaluta en de aangiftevaluta automatisch gewist door het systeem, indien deze reeds zijn gedefinieerd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
