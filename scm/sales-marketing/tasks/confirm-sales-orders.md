--- 
title: Verkooporders bevestigen
description: Deze procedure demonstreert hoe verkooporders worden bevestigd.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b0853e6a326a90b022bedc3b898d6c1b218c5fa2
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="confirm-sales-orders"></a>Verkooporders bevestigen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure demonstreert hoe verkooporders worden bevestigd. U ziet hoe u één order bevestigt en hoe u meerdere orders tegelijk bevestigt. Deze taken worden meestal uitgevoerd door een verkooporderverwerker. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. Voordat u begint, moet u ervoor zorgen dat er meerdere openstaande verkooporders voor dezelfde klant zijn. Als u USMF gebruikt, kunt u klant US-027 gebruiken.


## <a name="confirm-a-single-sales-order"></a>Eén verkooporder bevestigen
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Zoek en selecteer in de lijst de order die u wilt bevestigen.
3. Klik op de koppeling in het verkoopordernummer om de geselecteerde order te openen.
4. Klik in het actievenster op Verkopen.
5. Klik op Verkooporder bevestigen.
6. Vouw de sectie Parameters uit of samen.
    * Zorg dat het veld Boeking Ja actief is.  
7. Stel de optie Bevestiging afdrukken in op Ja.
    * Het veld Kredietlimiet controleren geeft de methode op die wordt gebruikt om het resterende krediet van een klant te berekenen. Dit wordt standaard gekopieerd van de pagina Parameters van module Klanten. Als u de kredietlimietcontrole wilt overslaan wanneer u een specifieke verkooporder bevestigt, stelt u Kredietlimiet controleren in op Geen. U moet er echter rekening mee houden dat ook als dit veld is ingesteld op Geen, de kredietlimietcontrole nog steeds wordt uitgevoerd als de optie Verplichte kredietlimiet is geselecteerd in de klanthoofdgegevens.  
8. Klik op OK.
9. Klik op Ja.
10. Sluit de pagina.
11. Klik in het actievenster op Opties.
12. Klik op Weergave wijzigen.
13. Klik op Weergave kopteksten.
    * Wanneer een order wordt bevestigd, wordt de Documentstatus ingesteld op Bevestiging.  
14. Klik in het actievenster op Verkopen.
15. Klik op Bevestiging verkooporder.
16. Sluit de pagina.

## <a name="confirm-multiple-sales-orders-at-once"></a>Meerdere verkooporders in één keer bevestigen
1. Ga naar Verkoop en marketing > Verkooporders > Orderbevestiging > Verkooporder bevestigen.
2. Klik op Selecteren.
3. Zoek en selecteer in de lijst op het tabblad Bereik de record die verwijst naar het veld Klantrekening.
4. Klik in het veld Criteria op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer in de lijst de klantrekening die meerdere orders heeft die u massaal wilt bevestigen.
    * Als u USMF gebruikt, kunt u rekening US-027 selecteren.  
6. Klik op OK.
    * Het tabblad Overzicht bevat een lijst met orders die aan de querycriteria voldoen. Deze worden in de bevestiging opgenomen.  
    * Het veld Overzicht bijwerken voor geeft de parameter op waarmee meerdere orders worden samengevat in één bevestigingsdocument. Standaard wordt de optie gekopieerd van de instelling Standaardwaarden voor bijwerking van samenvatting op de pagina Parameters van module Klanten.  
7. Selecteer 'Order' in het veld Overzicht bijwerken voor.
    * De minimale parameters die vereist zijn voor het maken van overzichtsupdates, zijn Factuurrekening en Valuta. Dit betekent dat overzichtsupdates die verschillende factuurrekeningen en verschillende valuta hebben, niet zijn toegestaan. Extra parameters kunnen worden ingesteld op de pagina Overzicht van updateparameters, die vanaf de pagina Parameters van module Klanten toegankelijk is.  
8. Klik in het veld Verkooporder op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Selecteer in de lijst het verkoopordernummer dat u in de overzichtsorder wilt opnemen.
10. Klik op Schikken.
11. Klik op OK.
12. Klik op OK.


