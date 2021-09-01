---
title: Kortingen voor betaling verwerken
description: Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.
author: omulvad
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89848d9a5258fcb40f863261a6ba5d067296182989f0d10eb48b8e2a7dec008a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781777"
---
# <a name="process-rebates-for-payment"></a>Kortingen voor betaling verwerken

[!include [banner](../../includes/banner.md)]

Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's. U kunt deze guide gebruiken in het demobedrijf USMF. De preconditie voor deze guide is dat u een of meer kortingsclaims hebt met de status Markeren. Als u USMF gebruikt, moet u de guide Klantkortingen genereren en verwerken uitvoeren voordat u deze guide start.


## <a name="convert-rebate-claims-to-credit-note"></a>Kortingsclaims converteren naar een creditnota
1. Ga naar Alle klanten.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het actievenster op Incasso.
5. Klik op Transacties vereffenen.
6. Klik op Functies.
7. Klik op Kortingsprogramma.
    * De pagina Kortingen bevat de kortingsclaims die u hebt verwerkt in de klantkortingsworkbench en die de status Markeren hebben.    
8. Klik op Bewerken.
    * Plaats vinkjes in het veld Markeren voor de claims die u wilt opnemen in de creditnota.   
9. Klik op Functies.
10. Klik op Creditnota maken.
    * Er wordt een bericht weergegeven dat aangeeft dat het journaal is geboekt. (Dit is het klantenverbruiksjournaal, zoals opgegeven op de pagina Parameters van module Klanten.) Hierdoor wordt het echte creditbedrag verplaatst naar het saldo van de klant. Dat betekent dat de rekening van de klant is gecrediteerd en dat de kortingstoerekeningsrekening is gedebiteerd.  
11. Sluit de pagina.
12. Klik op Annuleren.
    * Dit vernieuwt de pagina zodat u de updates kunt zien.  
13. Klik in het actievenster op Incasso.
14. Klik op Transacties vereffenen.
    * Merk op dat een transactie voor een negatief bedrag, die het totale kortingsbedrag vertegenwoordigt, zonder factuurreferentie is toegevoegd aan het klantsaldo.   
15. Klik op Annuleren.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]