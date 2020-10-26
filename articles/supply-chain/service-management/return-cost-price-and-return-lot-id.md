---
title: Kostprijs retour en retourpartij-id
description: U wilt dat de kosten van de geretourneerde producten gelijk zijn aan de kosten van de producten op het moment waarop u de producten aan de klant verkocht. U kunt dit bewerkstelligen met behulp van de **Retourpartij-id**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d5ac48dd390e2f57a7312e3c54af53dd49fd4f7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975579"
---
# <a name="return-cost-price-and-return-lot-id"></a>Kostprijs retour en retourpartij-id        

[!include [banner](../includes/banner.md)]



De kosten van de producten die worden geretourneerd aan de voorraad, worden berekend met behulp van de huidige kosten van de producten. U wilt echter dat de kosten van de geretourneerde producten gelijk zijn aan de kosten van de producten op het moment waarop u de producten aan de klant verkocht. U kunt dit doen met behulp van de **Retourpartij-id** op het sneltabblad **Regeldetails** in het formulier **Verkooporder**.

Neem bijvoorbeeld het volgende scenario. U maakt een klantfactuur. Vervolgens geeft de klant de geleverde producten aan u terug. U kunt producten terug in voorraad brengen. Wanneer u in dit geval de klant crediteert voor de geretourneerde producten, worden de kosten van deze producten berekend met behulp van de huidige kosten van de producten. Als u echter het veld **Retourpartij-id** gebruikt, wordt de kostprijs van de geretourneerde producten berekend met behulp van de kosten op de factuur van de oorspronkelijke verkoop aan de klant.

Gebruik een van de volgende methoden om een andere dan de huidige kostprijs voor een klantenretour te gebruiken.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Methode 1: De kostprijs retour handmatig invoeren

Wanneer u items aan een retourorder toevoegt, worden items standaard geretourneerd naar de voorraad met de huidige kostprijs. Voer de volgende stappen uit om een andere kostprijs retour op te geven.

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.

2.  Klik in het **Actievenster** in de groep **Nieuw** op **Retourorder**.

3.  Selecteer in het formulier **Retourorder maken** een klantrekening en klik vervolgens op **OK**.

4.  Selecteer in het formulier **Retourorder - RMA-nummer: %1, %2** een artikel en voer vervolgens een negatieve hoeveelheid in het veld **Hoeveelheid** in.

5.  Klik op het sneltabblad **Regeldetails**.

6.  Voer op het tabblad **Algemeen** een waarde in het veld **Kostprijs retour** in. Deze waarde wordt gebruikt wanneer de goederen worden geretourneerd naar de voorraad. Als u geen waarde invoert, wordt de huidige kostprijs gebruikt wanneer de goederen worden geretourneerd naar de voorraad.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Methode 2: De kostprijs op basis van de klantenfactuurregel automatisch genereren

Dit is de aanbevolen methode om retourregels te maken. Gebruik de kosten van de producten op de tijd wanneer u de producten aan de klant verkocht, maak een retourorder en geef een verkoopregel om te retourneren.

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.

2.  Klik in het **Actievenster** in de groep **Nieuw** op **Retourorder**.

3.  Selecteer in het formulier **Retourorder maken** een klantrekening en klik vervolgens op **OK**.

4.  Klik in het formulier **Retourorder - RMA-nummer: %1, %2** in het **Actievenster** op **Verkooporder** zoeken.

5.  Selecteer in het formulier **Verkooporder zoeken** de te retourneren factuurregel en klik vervolgens op **OK**.
    
    Op het sneltabblad **Regeldetails** op het tabblad **Algemeen** wordt in het veld **Retourpartij-id** de waarde van de oorspronkelijke verkoopregel weergegeven. Bovendien bevat het veld **Kostprijs retour** de kostprijs van de oorspronkelijke verkoopregel.

## <a name="cost-calculation-example"></a>Voorbeeld van de kostenberekening

Wanneer u het veld **Kostprijs retour** op een retourorderregel gebruikt om de retourkostprijs op te geven, wordt de kostprijs op de retourorderregel gebruikt. Als u de functionaliteit voorraad sluiten of herberekenen uitvoert, wordt de kostprijs aangepast naar de oorspronkelijke verkoopregel. De kosten op de retourorderregel worden automatisch aangepast aan dezelfde kosten per stuk.

1.  Maak een product met de naam Test en geef het weer vrij. Geef in het formulier **Vrijgegeven productdetails** de volgende informatie op:
    
    1.  Selecteer op het sneltabblad **Kosten beheren** in het veld **Artikelgroep** de groep **Onderdelen**.
    
    2.  Selecteer op het sneltabblad **Algemeen** in het veld **Artikelmodelgroep** **DEF**.
    
    3.  Typ op het sneltabblad **Inkoop** in het veld **Prijs** 10,00 als de kostprijs van het artikel.
    
    4.  Klik in het **Actievenster** op **Dimensiegroepen**. Selecteer in het veld **Opslagdimensiegroep** **Alleen locatie en magazijn**. Selecteer in het veld **Traceringsdimensiegroep** **Geen actieve traceringsdimensies**.

2.  Maak een inkooporder voor 10 stuks van het artikel Test op 6,00 per stuk en boek vervolgens een factuur voor de inkooporder.
    
    Maak een tweede inkooporder voor 10 stuks van het artikel Test op 8,00 per stuk en boek vervolgens een factuur voor de inkooporder.

3.  Boek een factuur voor een verkooporder voor vijf stuks van het artikel Test.
    
    In dit geval wordt de kostprijs van de verkooporderregel berekend op 35,00 (5 stuks \* 7,00 gemiddelde kostprijs per stuk).

4.  Maak een retourorder maken voor de klant. Selecteer in het formulier **Verkooporder zoeken** de factuurregel en klik vervolgens op **OK**.

5.  Controleer in het formulier **Retourorder - RMA-nummer: %1, %2** of een retourorder wordt gegenereerd om het testartikel te retourneren. De hoeveelheid van de retourorder wordt ingesteld op-5,00.
    
    Het veld **Retourpartij-id** bevat een partij-ID. Deze partij-ID is overgenomen uit de oorspronkelijke verkooporder van het artikel dat aan de klant is verkocht. Het veld **Kostprijs retour** bevat de kostprijs van de oorspronkelijke verkoopregel.

6.  Registreer de ontvangst van de retourartikelen.

7.  Boek een pakbon voor de geretourneerde artikelen.

8.  Boek een factuur voor de retourorder. Selecteer op de lijstpagina **Alle verkooporders** een verkooporder waarvoor **Geretourneerde order** het ordertype is.

9.  Open het formulier **Voorraadtransacties**. Controleer of de kosten van de retour bepaald zijn op 7,00 per stuk door de waarde in het veld **Kostprijs retour** te gebruiken voor een totaal van 35,00 in het veld **Kosten**. U kunt het formulier **Voorraadtransacties** via het formulier **Retourorder - RMA-nummer: %1, %2** openen. Klik in het raster **Regels** op **Voorraad** \> **Transacties**.

10. Gebruik in voorraad- en magazijnbeheer het formulier **Afsluiten en corrigeren** om de procedure **3. Sluiten** uit te voeren.
    
    Met deze actie worden de kosten gecorrigeerd op de oorspronkelijke verkoopregel waarvan de kostprijs was berekend op -35,00 (5 stuks \* 7,00) naar -30,00 (5 stuks \* 6,00). Dit is omdat de voorraadmodelgroep First in, First out (FIFO gebruikt) en 6,00 per stuk de FIFO-kosten van de eerste inkooporder is. De actie past bovendien de kosten op de retourverkoopregel aan naar de kostprijs per stuk op de oorspronkelijke verkoopregel. Dus wordt de kostprijs van de retourregel aangepast van 35,00 naar 30,00.




