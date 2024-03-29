---
title: Verkoopovereenkomsten invoeren
description: In dit artikel leest u hoe u een verkoopovereenkomst maakt waarmee een van uw klanten toezegt in een bepaalde periode een product voor een bepaald bedrag te kopen in ruil voor speciale kortingen.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b3aa72057753a9592fd47275dc996a3a904d86b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897482"
---
# <a name="enter-sales-agreements"></a>Verkoopovereenkomsten invoeren

[!include [banner](../../includes/banner.md)]

In dit artikel leest u hoe u een verkoopovereenkomst maakt waarmee een van uw klanten toezegt in een bepaalde periode een product voor een bepaald bedrag te kopen in ruil voor speciale kortingen. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="set-up-sales-agreement-header"></a>Koptekst van de verkoopovereenkomst instellen
1. Ga in het navigatievenster naar **Modules > Verkoop en marketing > Verkoopovereenkomsten > Verkoopovereenkomsten**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Klantrekening** de gewenste record in het vervolgkeuzemenu.
4. Selecteer in het veld **Classificatie van verkoopovereenkomst** de gewenste record in het vervolgkeuzemenu.
5. Vouw de sectie **Algemeen** uit.
6. Selecteer **Toezegging productwaarde** in het veld **Standaardtoezegging**. Een toezeggingstype is een verplicht criterium dat u aan de overeenkomst moet toewijzen om te bepalen hoe het contact van de overeenkomst wordt afgehandeld. Met de vier vooraf gedefinieerde typen kunt u het toezeggingsdoel van de klant instellen, dat als een hoeveelheid of waarde wordt uitgedrukt. Het toezeggingstype voor hoeveelheid kan alleen voor een bepaald product worden toegepast, maar op de op waarde gebaseerde typen zijn van toepassing op verkoop van zowel specifieke als niet-specifieke producten.  
7. Stel in het veld **Vervaldatum** de datum in op een toekomstige datum waarop u wilt dat de overeenkomst vervalt.
8. Selecteer **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Toezeggingsregels voor productwaarde instellen
1. Selecteer **Regel toevoegen**.
2. Selecteer in het veld **Artikelnummer** de gewenste record in het vervolgkeuzemenu. Het type van toezegging dat u voor de overeenkomst hebt gekozen beïnvloedt het soort informatie dat u voor de overeenkomstregels kunt invoeren. Bij een op waarde gebaseerde overeenkomst moet u bijvoorbeeld het totale nettobedrag (in de goedgekeurde valuta) opgeven waartoe de klant zich verbindt om bij u goederen te kopen. In dit voorbeeld zijn de velden **Hoeveelheid** en **Eenheid** op de regel niet beschikbaar omdat u een overeenkomst voor de klant maakt om een specifieke waarde van een product te kopen.   
3. Typ in het veld **Nettobedrag** het monetaire bedrag waartoe de klant zich verbindt om te kopen.
4. Typ in het veld **Kortingspercentage** een procentuele waarde die van toepassing zal zijn op de verkooporderregels van de klant die aan deze overeenkomst zijn gekoppeld.
5. Vouw de sectie **Regeldetails** uit.
6. Selecteer **Ja** het veld **Max is afgedwongen**.
    - Als u **Max is afgedwongen** selecteert, mag het totale bedrag alle verkooporderregels die de speciale prijzen, kortingen en/of betalingsvoorwaarden van de toezegging gebruiken het bedrag niet overschrijden dat op de toezegging wordt opgegeven.  
    - De minimum- en maximumvrijgavebedragen geven een waardebereik op dat moet worden verkocht bij elke verkooporder die de geselecteerde overeenkomst gebruikt.   
7. Vouw de sectie **Koptekst verkoopovereenkomst** uit. Tenzij de status van de overeenkomst is ingesteld op **Van kracht**, kunnen verkooporders niet aan de overeenkomst worden gekoppeld en daarom niet bijdragen aan de voltooiing van die overeenkomst. U kunt de status op dit moment handmatig wijzigen. De status wijzigt echter normaal wanneer u de overeenkomst voor de klant bevestigt.  
8. Klik in het actievenster op **Verkoopovereenkomst**.
9. Selecteer **Bevestiging**. Zorg ervoor dat de optie **Overeenkomst als effectief markeren** is ingesteld op **Ja**.  
10. Selecteer **Ja** in het veld **Rapport afdrukken**.
11. Selecteer **OK**.
12. Sluit de pagina. De overeenkomst is nu effectief. U kunt de orders van de klant beginnen te koppelen aan de overeenkomst voor het starten, om het toegezegde doel te verrekenen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]