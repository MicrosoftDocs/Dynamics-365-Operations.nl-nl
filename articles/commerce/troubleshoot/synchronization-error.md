---
title: Problemen met synchronisatie van asynchrone orders
description: In dit artikel worden algemene redenen beschreven voor het mislukken van het maken van asynchrone orders in Microsoft Dynamics 365 Commerce en worden stappen voor het oplossen van problemen beschreven, zodat systeemgebruikers en partners begrijpen wat er is misgegaan.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815751"
---
# <a name="asynchronous-order-synchronization-issues"></a>Problemen met synchronisatie van asynchrone orders

[!include [banner](../../includes/banner.md)]

In dit artikel worden algemene redenen beschreven voor het mislukken van het maken van asynchrone orders in Microsoft Dynamics 365 Commerce en worden stappen voor het oplossen van problemen beschreven, zodat systeemgebruikers en partners begrijpen wat er is misgegaan.

## <a name="symptom"></a>Symptoom

Asynchrone orders die worden gemaakt op basis van Dynamics 365 Commerce e-commerce of verkooppunt (POS) worden niet weergegeven in Commerce headquarters.

## <a name="troubleshooting"></a>Problemen oplossen

Het maken van orders kan om verschillende redenen mislukken in Headquarters, afhankelijk van de fase waarin het proces voor het maken van orders mislukt. In de volgende stappen voor het oplossen van problemen passeren de mogelijke hoofdoorzaken de revu.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Controleren of de transactie die aan de asynchrone order is gerelateerd Headquarters heeft bereikt

Ga voor e-commerceorders in Headquarters naar **Retail en Commerce \> Query's en rapporten \> Transacties onlinewinkel**. Als u een bevestigingsnummer voor de order hebt, filtert u de transacties door het bevestigingsnummer in te voeren in het veld **Afzetkanaalverwijzings-id**. Als u geen bevestigingsnummer hebt, filtert u de transacties door het rekeningnummer van de klant in te voeren.

Open voor POS-orders de pagina **Winkeltransacties** en filter de records op het nummer van het ontvangstbewijs of het rekeningnummer van de klant. Als de transactie niet is gevonden, voert u de kanaaltransactietaak **P-0001** uit, waarmee transacties van de kanalen naar Headquarters worden gesynchroniseerd. Als de taak **P-0001** mislukt, opent u een ondersteuningsticket voor de mislukte taak. Als de taak **P-0001** slaagt, maar de transacties nog steeds niet verschijnt in Headquarters, opent u een ondersteuningsticket met de relevante informatie.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>De synchronisatiestatus controleren als de transactie aanwezig is in Headquarters, maar niet is gekoppeld aan een verkooporder

Als de transactie aanwezig is in Headquarters maar de verkooporder nog niet is gemaakt, opent u de pagina **Transacties onlinewinkel** en selecteert u het sneltabblad **Synchronisatiestatus**. Als met de taak **Orders synchroniseren** is geprobeerd deze transactie te synchroniseren, moet in het veld **Orderstatus in behandeling** de status **Geslaagd** of **Mislukt** worden weergegeven. Als de status **Geslaagd** is, moet het verkooporderveld aanwezig zijn in deze transactie. Als de status **Mislukt** is, kunt u de foutdetails bekijken in het veld **Details orderfout** op het sneltabblad **Synchronisatiestatus**. Als geen van beide statussen worden weergegeven, is er geen poging gedaan om de transactie te verwerken. In dit geval kunt u **Synchronisatieorder** boven aan de pagina selecteren om de synchronisatietaak uit te voeren.

Zorg ervoor dat de taak **Orders synchroniseren** zo is gepland dat deze periodiek wordt uitgevoerd, zodat asynchrone transacties in Headquarters kunnen worden gemaakt als orders.

De volgende secties bevatten informatie over enkele veelvoorkomende fouten en de voorgestelde oplossingen.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>In het veld Details orderfout wordt het volgende foutbericht weergegeven: 'Nummerreeks is overschreden'

Nummerreeksen worden gebruikt om verkooporders te maken in Headquarters. Als alle toegestane nummers voor een nummerreeks volledig zijn gebruikt, wordt dit foutbericht gegenereerd. De nummerreeks die wordt gebruikt om verkooporders te maken, kunt u vinden onder **Debiteuren-parameters \> Nummerreeksen \> Verkooporder**. Als u deze fout wilt oplossen, herstelt u de bestaande nummerreeks of vervangt u deze door een nieuwe nummerreeks.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>In het veld Details orderfout wordt het volgende foutbericht weergegeven: 'Er moet een standaardbetalingsservice zijn voor het verwerken van creditcardtransacties'

U kunt deze fout te corrigeren door te bevestigen dat er in Headquarters een standaardbetaling is gedefinieerd. Als geen standaardbetaling is gedefinieerd, moet u deze definiëren. Ga naar **Klanten \> Betalingsinstelling \> Betalingsservice** en zorgt u ervoor dat de optie **Standaardverwerker voor nieuwe creditcards** is ingesteld op **Ja** voor één betalingsservice.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>In het veld Details orderfout wordt een foutbericht voor de rekeningstructuur weergegeven

De tekst van het foutbericht voor de rekeningstructuur kan verschillen, zoals in de volgende voorbeelden wordt weergegeven. De fouten hebben echter een veelvoorkomende hoofdoorzaak met betrekking tot de configuratie van de rekeningstructuur gemeen.

- 'Boekingsresultaten voor journaalbatchnummer 0009656328 boekstuk ARP-000959899 1,00 voor boekstuk ARP-000959899 in bedrijf usrt worden geboekt als te veel betaald of te weinig betaald'
- 'Boekingsresultaten voor journaalbatchnummer 0009656328 boekstuk ARP-000959899 boekstuk ARP-000959901 rekeningstructuur, voor de combinatie 618160, zijn niet geldig voor grootboek Gedeelde zakelijke hoofdrekening'
- 'Boekingsresultaten voor journaalbatchnummer 0009656328 boekstuk ARP-000959899 boekstuk ARP-000959901 Gerapporteerd door bedrijfsrekening usrt'
- 'Boekingsresultaten voor journaalbatchnummer 0009656328 boekstuk ARP-000959899 Boeking is geannuleerd'
    
Controleer de rekeningstructuren op nauwkeurigheid om deze fouten te corrigeren. Zie [Rekeningstructuren configureren](/dynamics365/finance/general-ledger/configure-account-structures) voor meer informatie.
    
Nadat de fout is hersteld, selecteert u de mislukte transactie en selecteert u vervolgens **Order synchroniseren** boven aan de pagina om de synchronisatietaak uit te voeren.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Andere typen fouten waarvoor de transactiegegevens mogelijk moeten worden hersteld

Als u andere typen fouten wilt herstellen waarvoor mogelijk de transactiegegevens moeten worden hersteld, kunt u de mogelijkheid 'Transacties bewerken en controleren' gebruiken. Zie [Transacties bewerken en controleren](../edit-order-trans.md) voor meer informatie.
