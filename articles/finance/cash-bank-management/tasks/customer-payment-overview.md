---
title: Overzicht van klantbetalingen
description: Deze taakbegeleier behandelt verschillende methoden die worden gebruikt om klantenbetalingen in te voeren.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 688fae26e556fcc7d41e5f79d7dcce3327094e62f4a82b9c802efac8072f47b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779009"
---
# <a name="customer-payment-overview"></a>Overzicht van klantbetalingen

[!include [banner](../../includes/banner.md)]

Deze taakbegeleier behandelt verschillende methoden die worden gebruikt om klantenbetalingen in te voeren. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar het **Navigatiedeelvenster > Modules > Klanten > Betalingen > Betalingsjournaal**.
2. Klik op **Nieuw**.
3. Selecteer het betalingsjournaal waarin de klantbetalingen zullen worden opgeslagen.
4. Selecteer het journaal of voer het handmatig in.
5. Klik in het **actievenster** op **Klantbetalingen invoeren**. Klantbetalingen invoeren wordt gebruikt om één klantbetaling tegelijk te registreren. U kunt de betalingsgegevens bovenaan invoeren en vervolgens de facturen markeren die met de betaling zijn betaald, allemaal vanaf dezelfde pagina.  
6. Voer de klant in waarvan u de betaling hebt ontvangen. Als u niet weet wie de klant is, maar wel een transactie weet die is betaald, kunt u het veld Transactie gebruiken om de betaling in te voeren. Typ of selecteer de factuur in het veld Transactie. De klant wordt automatisch ingevuld nadat u de transactie hebt geselecteerd.
7. Voer in het veld **Betalingsreferentie** een betalingsreferentie in. De betalingsreferentie kan het chequenummer van de klant of een referentie naar een elektronische betaling van de klant zijn. De betalingsreferentie is alleen vereist als u ervoor kiest de betaling op te nemen op een depositostrook.  
8. Selecteer in het veld **Depositostrook** of de betaling wordt opgenomen op een depositostrook. 
9. Voer in het veld **Bedrag** het bedrag van de klantbetaling in. Het betalingsbedrag wordt niet standaard ingevuld. Het moet handmatig worden ingevoerd. 
10. Markeer de facturen die door de klant zijn betaald. Als de betaling een vooruitbetaling is, bent u niet verplicht facturen voor vereffening te markeren. De betaling kan nog steeds worden opgeslagen en geboekt. Vereffening met een factuur kan op een later tijdstip plaatsvinden.
11. Voer het bedrag in van de betaling die moet worden vereffend met de gemarkeerde factuur. Dit veld kan worden gebruikt wanneer de betaling is bestemd voor een gedeeltelijke betaling. Als u geen bedrag invoert, wordt het te vereffenen bedrag automatisch voor u vastgesteld.
12. Klik op **Opslaan in journaal**. Voordat u de betaling opslaat naar het journaal, zorgt u ervoor dat de tegenrekening wordt gedefinieerd. Bij gebruik van **Opslaan in journaal** wordt de betaling opgeslagen en naar het journaal verplaatst. U kunt vervolgens doorgaan met het invoeren van de volgende betaling.
13. Sluit de pagina.
14. Klik in het **actievenster** op Regels. Bij het openen van Regels, ziet u alle betalingen die u hebt geregistreerd op de pagina **Klantbetalingen invoeren** en hebt opgeslagen in het journaal. U kunt deze pagina ook gebruiken om nieuwe klantbetalingen in te voeren of bestaande klantbetalingen te bewerken voordat deze worden geboekt.
15. Klik op **Nieuw** om nog een betaling te maken. 
16. Selecteer de klant waarvan u de betaling hebt ontvangen. Als u niet weet wie de klant is maar wel een factuur weet die via de betaling is betaald, gebruikt u het veld Factuur om de factuur handmatig in te voeren of te selecteren. De klant wordt standaard ingevoerd nadat de factuur is geselecteerd.  
17. Klik op **Transacties vereffenen** om facturen die zijn betaald te markeren. U bent niet verplicht om de betaling te vereffenen met enige facturen. Als dit een vooruitbetaling is of als u niet weet welke factuur is betaald, kunt u de betaling invoeren en boeken. De betaling kan op een later moment voor een factuur worden vereffend.  
18. Markeer de facturen die zijn betaald met de betaling. 
19. Voer in het veld **Bedrag** het bedrag in van de betaling die wordt vereffend met de factuur.
20. Klik op **OK**.
21. Voer in het veld **Betalingsreferentie** een betalingsreferentie in. De betalingsreferentie is alleen vereist als u ervoor kiest de betaling op te nemen op een depositostrook.  
22. Klik in het **actievenster** op **Boeken** om de klantbetalingen te boeken. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]