---
title: Belangrijke factuurgegevens in leverancierssysteem met een leveranciersfactuur
description: Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d3f9fc1fb7724632dbc9c4c3e1e28c6e85eaf61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827789"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Belangrijke factuurgegevens in leverancierssysteem met een leveranciersfactuur

[!include [banner](../../includes/banner.md)]

Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Alle inkooporders**.
2. Klik op **Nieuw**.
3. Klik in het veld **Leverancier** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek een leverancier om te selecteren. Bijvoorbeeld, blader omlaag naar US-104.
5. Selecteer leverancier US-104.
6. Klik op **OK**.
7. Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Selecteer een voorraadartikel. Selecteer voor dit voorbeeld artikelnummer 1000.
9. Vouw het sneltabblad **Regeldetails** uit.
10. Ga naar het tabblad **Instellen**. U kunt het overeenstemmingsbeleid negeren om geen overeenstemming, tweeweg-overeenstemming of drieweg-overeenstemming te gebruiken.  
11. Klik in het actievenster op **Inkoop**.
12. Klik op **Bevestigen**.

## <a name="receive-the-products"></a>De producten ontvangen
1. Klik in het actievenster op **Ontvangen**.
2. Klik op **Productontvangstbon**.
3. Voer in het veld **Productontvangstbon** het nummer van de productontvangstbon in. Voer bijvoorbeeld PR123 in.
4. Klik op **OK** om de productontvangstbon te boeken.
5. Sluit de pagina.

## <a name="create-a-vendor-invoice"></a>Een leveranciersfactuur maken
1. Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Inkooporders die zijn ontvangen maar niet gefactureerd**.
2. Selecteer de inkooporder die is gemaakt.
3. Klik in het actievenster op **Factuur**.
4. Klik op **Factuur**.
5. Voer in het veld **Nummer** het factuurnummer in.
6. Typ een waarde in het veld **Factuurbeschrijving**.
7. Voer een datum in het veld **Factuurdatum** in.
8. Voer 1200 in het veld **Eenheidsprijs** in.
9. Klik op **Regel toevoegen**.
10. Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek in de lijst het artikelnummer van de installatietoeslag. Bijvoorbeeld S0001
12. Selecteer het artikelnummer van de installatietoeslag. Merk op dat geen afstemming is uitgevoerd sinds u de wijzigingen hebt aangebracht.  
13. Klik op **Vereffeningsstatus bijwerken**.
14. Klik in het actievenster op **Controleren**.
15. Klik op **Vereffeningsgegevens**. De nieuwe regel met services hoeft niet te worden afgestemd zodat de status "Niet uitgevoerd" blijft.  
16. Selecteer de productontvangstbon voor het voorraadartikel dat u hebt ontvangen. De regel met de productontvangstbon is afgestemd maar de hoeveelheid of prijs komt niet overeen, waardoor de afstemming mislukt.  
17. Voer een nummer in het veld **Eenheidsprijs** in. Nu de eenheidsprijs overeenkomt, wordt de status gewijzigd in Geslaagd. Als uw beleid verschillen toestaat of als afstemmen alleen een waarschuwing is, kunt u de factuur toch boeken.  
18. Sluit de pagina.
19. Klik op **Boeken**.
20. Het formulier sluiten. Merk op dat de inkooporder niet meer wordt weergegeven als ontvangen maar als niet gefactureerd.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]