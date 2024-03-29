---
title: Indeling voor betalingsbonnen voor projectfacturen instellen
description: In dit artikel wordt uitgelegd hoe u afgedrukte betalingsbonnen aan projectfacturen koppelt en een betalingsverwijzing voor het boeken en vereffenen levert.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f9e956f6c6a5d7a783bfc3a475ff4ca60473f17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879433"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Indeling voor betalingsbonnen voor projectfacturen instellen

[!include [banner](../../includes/banner.md)]

Bedrijven koppelen om klanten van dienst te zijn vaak afgedrukte betalingsbonnen aan facturen en leveren een betalingsverwijzing voor het boeken en vereffenen. De betalingsbon kan naast verkoopfacturen en vrije-tekstfacturen worden gebruikt voor project- of servicefacturen, aanmaningen, rentenota's en rekeningoverzichten. Als u pakbonnen wilt verwerken, stelt u eerst uw crediteur-ID-nummer en indelingen voor betalingsbonbijlagen in.

Bij deze procedure wordt het demobedrijf DEMF gebruikt. 

Deze functionaliteit is alleen beschikbaar voor rechtspersonen waarvan het primaire adres in Denemarken is.


## <a name="set-up-a-creditor-id-number"></a>Een crediteur-ID-nummer instellen
1. Ga naar Organisatiebeheer > Organisaties > Rechtspersonen.
2. Vouw de sectie Bankrekeninggegevens uit of samen.
3. Klik op Bewerken.
4. Typ een waarde in het veld FI-crediteur-id.
5. Klik op Opslaan.
6. Sluit de pagina.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Een betalingsbonindeling voor facturen, nota's, aanmaningen en overzichten instellen
1. Ga naar Klanten > Instellingen > Formulieren > Formulierinstelling.
2. Klik op het tabblad Factuur.
3. Selecteer een optie in het veld Bijlage 'gekoppelde betaling' bij klantfactuur.
    * Geen: er wordt geen betalingsbon afgedrukt. Kies deze optie als het betalingsbedrag in een andere valuta dan de Deense kroon (DKK) is.   FIK 751: druk een FIK 751-betalingsbon af als u het betalingsbedrag en de vervaldatum handmatig op de betalingsbon wilt schrijven.   FIK 752: druk een FIK 752-betalingsbon af als u een door de computer gegenereerde betalingsbon wilt gebruiken waarop het betalingsbedrag en de vervaldatum zijn voorgedrukt.  
4. Klik op Opslaan.
5. Klik op het tabblad Vrije-tekstfactuur.
6. Selecteer een optie in het veld Bijlage 'gekoppelde betaling' bij vrije-tekstfactuur.
    * Geen: er wordt geen betalingsbon afgedrukt. Kies deze optie als het betalingsbedrag in een andere valuta dan de Deense kroon (DKK) is.   FIK 751: druk een FIK 751-betalingsbon af als u het betalingsbedrag en de vervaldatum handmatig op de betalingsbon wilt schrijven.   FIK 752: druk een FIK 752-betalingsbon af als u een door de computer gegenereerde betalingsbon wilt gebruiken waarop het betalingsbedrag en de vervaldatum zijn voorgedrukt.  
7. Klik op Opslaan.
8. Klik op het tabblad Rentenota.
9. Selecteer een optie in het veld Bijlage 'gekoppelde betaling' bij rentenota.
    * Geen: er wordt geen betalingsbon afgedrukt. Kies deze optie als het betalingsbedrag in een andere valuta dan de Deense kroon (DKK) is.   FIK 751: druk een FIK 751-betalingsbon af als u het betalingsbedrag en de vervaldatum handmatig op de betalingsbon wilt schrijven.   FIK 752: druk een FIK 752-betalingsbon af als u een door de computer gegenereerde betalingsbon wilt gebruiken waarop het betalingsbedrag en de vervaldatum zijn voorgedrukt.  
10. Klik op Opslaan.
11. Klik op het tabblad Aanmaning.
12. Selecteer een optie in het veld Bijlage 'gekoppelde betaling' bij aanmaning.
    * Geen: er wordt geen betalingsbon afgedrukt. Kies deze optie als het betalingsbedrag in een andere valuta dan de Deense kroon (DKK) is.   FIK 751: druk een FIK 751-betalingsbon af als u het betalingsbedrag en de vervaldatum handmatig op de betalingsbon wilt schrijven.   FIK 752: druk een FIK 752-betalingsbon af als u een door de computer gegenereerde betalingsbon wilt gebruiken waarop het betalingsbedrag en de vervaldatum zijn voorgedrukt.  
13. Klik op Opslaan.
14. Klik op het tabblad Rekeningoverzicht.
15. Selecteer een optie in het veld Bijlage 'gekoppelde betaling' bij rekeningoverzicht.
    * Geen: er wordt geen betalingsbon afgedrukt. Kies deze optie als het betalingsbedrag in een andere valuta dan de Deense kroon (DKK) is.   FIK 751: druk een FIK 751-betalingsbon af als u het betalingsbedrag en de vervaldatum handmatig op de betalingsbon wilt schrijven.   FIK 752: druk een FIK 752-betalingsbon af als u een door de computer gegenereerde betalingsbon wilt gebruiken waarop het betalingsbedrag en de vervaldatum zijn voorgedrukt.  
16. Klik op Opslaan.
17. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
