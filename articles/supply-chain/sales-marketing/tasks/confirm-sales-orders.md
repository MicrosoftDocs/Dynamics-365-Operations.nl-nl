---
title: Verkooporders bevestigen
description: Deze procedure demonstreert hoe verkooporders worden bevestigd.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c09ef2f78353a75ecb2dfffef6965cb1ac0873
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991810"
---
# <a name="confirm-sales-orders"></a>Verkooporders bevestigen

[!include [banner](../../includes/banner.md)]

Deze procedure demonstreert hoe verkooporders worden bevestigd. U ziet hoe u één order bevestigt en hoe u meerdere orders tegelijk bevestigt. Deze taken worden meestal uitgevoerd door een verkooporderverwerker. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. Voordat u begint, moet u ervoor zorgen dat er meerdere openstaande verkooporders voor dezelfde klant zijn. Als u USMF gebruikt, kunt u klant US-027 gebruiken.


## <a name="confirm-a-single-sales-order"></a>Eén verkooporder bevestigen
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.
2. Zoek en selecteer in de lijst de order die u wilt bevestigen.
3. Klik op de koppeling in het verkoopordernummer om de geselecteerde order te openen.
4. Klik in het **actievenster** op **Verkopen**.
5. Klik op **Verkooporder bevestigen**.
6. Vouw de sectie **Parameters** uit. Controleer of de optie **Boeking** op 'Ja' is ingesteld.  
7. Stel de optie **Bevestiging afdrukken** in op 'Ja'. Het veld **Kredietlimiet controleren** geeft de methode op die wordt gebruikt om het resterende krediet van een klant te berekenen. Dit wordt standaard gekopieerd van de pagina Parameters van module Klanten. Als u de kredietlimietcontrole wilt overslaan wanneer u een specifieke verkooporder bevestigt, stelt u **Kredietlimiet controleren** in op 'Geen'. U moet er echter rekening mee houden dat ook als dit veld is ingesteld op 'Geen', de kredietlimietcontrole nog steeds wordt uitgevoerd als de optie **Verplichte kredietlimiet** is geselecteerd in de klanthoofdgegevens. 
8. Klik op **OK**.
9. Klik op **Ja**.
10. Sluit de pagina.
11. Klik in het **actievenster** op **Opties**.
12. Klik op **Weergave wijzigen**.
13. Klik op **Weergave kopteksten**. Wanneer een order wordt bevestigd, wordt de **Documentstatus** ingesteld op 'Bevestiging'. 
14. Klik in het **actievenster** op **Verkopen**.
15. Klik op **Bevestiging verkooporder**.
16. Sluit de pagina.

## <a name="confirm-multiple-sales-orders-at-once"></a>Meerdere verkooporders in één keer bevestigen
1. Ga naar **Verkoop en marketing > Verkooporders > Orderbevestiging > Verkooporder bevestigen**.
2. Klik op **Selecteren**.
3. Zoek en selecteer in de lijst op het tabblad **Bereik** de record die verwijst naar het veld **Klantrekening**.
4. Klik in het veld **Criteria** op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer in de lijst de klantrekening die meerdere orders heeft die u massaal wilt bevestigen. Als u USMF gebruikt, kunt u rekening US-027 selecteren.  
6. Klik op **OK**.
    - Het tabblad **Overzicht** bevat een lijst met orders die aan de querycriteria voldoen. Deze worden in de bevestiging opgenomen.  
    - Het veld **Overzicht bijwerken voor** in de sectie **Parameters** geeft de parameter op waarmee meerdere orders worden samengevat in één bevestigingsdocument. Standaard wordt de optie gekopieerd van de instelling **Standaardwaarden voor bijwerking van samenvatting** op de pagina **Parameters van module Klanten**.  
7. Selecteer 'Order' in het veld **Overzicht bijwerken voor**. De minimale parameters die vereist zijn voor het maken van overzichtsupdates, zijn **Factuurrekening** en **Valuta**. Dit betekent dat overzichtsupdates die verschillende factuurrekeningen en verschillende valuta hebben, niet zijn toegestaan. Extra parameters kunnen worden ingesteld op de pagina **Overzicht van updateparameters**, die vanaf de pagina **Parameters van module Klanten** toegankelijk is. 
8. Klik in het veld **Verkooporder** op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Selecteer in de lijst het verkoopordernummer dat u in de overzichtsorder wilt opnemen.
10. Klik op **Schikken**.
11. Klik op **OK**.
12. Klik op **OK**.

