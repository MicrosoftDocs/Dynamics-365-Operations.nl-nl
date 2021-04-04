---
title: Rapportage voor betalingssaldo instellen (België)
description: Gebruik deze procedure om BLWI-informatie (Belgisch Luxemburgs Wissel Instituut) in te stellen voor België.
author: v-oloski
manager: AnnBe
ms.date: 07/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Belgium
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 674842442e749d90fecca5d9ba6aed9258149a4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265438"
---
# <a name="set-up-payment-balance-reporting-belgium"></a>Rapportage voor betalingssaldo instellen (België)

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure om BLWI-informatie (Belgisch Luxemburgs Wissel Instituut) in te stellen voor België. Deze procedure is gemaakt met het demogegevensbedrijf USSI.

Deze functionaliteit is beschikbaar voor rechtspersonen die hun primaire adres in België hebben. Voordat u deze procedure voltooien kunt, moet u de registratie-id instellen voor België en het registratienummer invoeren dat moet worden gebruikt om de BLWI-aangifte te maken.


## <a name="set-up-a-blwi-countryregion-group"></a>Een BLWI-land-/regiogroep instellen
1. Ga naar Btw > Instellingen > Buitenlandse handel > Landen-/regiogroepen BLWI.
2. Klik op Nieuw.
3. Typ een waarde in het veld Groep-id.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Toevoegen.
6. Typ of selecteer een waarde in het veld Land/regio.
7. Typ een waarde in het veld Omschrijving.
8. Klik op Vertalingen.
9. Typ of selecteer een waarde in het veld Waarde.
10. Sluit de pagina.

## <a name="set-up-blwi-currencies"></a>BLWI-valuta's instellen
1. Ga naar Btw > Instellingen > Buitenlandse handel > BLWI-valuta's.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Valuta.
4. Schakel het selectievakje Rapporteren in deze valuta in.
5. Voer in het veld Kolomnummer een getal in.

## <a name="set-up-blwi-parameters"></a>BLWI-parameters instellen
1. Ga naar Btw > Instellingen > Buitenlandse handel > BLWI-parameters.
2. Selecteer Ja in het veld BLWI.
    * Deze parameter moet worden geactiveerd voordat u klant/leveranciertransacties boekt, zodat de transacties worden overgeboekt naar het betalingssaldo.  
3. Typ een waarde in het veld E-mailadres.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Telefoon.
6. Typ een waarde in het veld Fax.
7. Selecteer een optie in het veld BLWI-code in journalen controleren.
    * Selecteer de regel voor het controleren of een betalingsdoelcode in documenten is opgegeven in het veld BLWI-code controleren. De beschikbare opties zijn Geen, Waarschuwing en Fout. Als een transactie een klant/leverancier heeft die zich in een vreemd land/regio bevindt (dat wil zeggen het land/regio van de klant/leverancier verschilt van het land/regio van de rechtspersoon), de transactie geen toegewezen betalingsdoelcode heeft en de cheque is ingesteld op waarschuwing of fout, wordt een waarschuwing of foutbericht weergegeven tijdens de boeking. Deze validatie wordt toegepast op alle klant/leverancierstransacties, behalve betalingstransacties.  
8. Typ of selecteer een waarde in het veld Indelingstoewijzing.
    * Vereiste: u moet de configuratie van de BLWI-indeling (BE) voor elektronische rapportage (ER) uploaden vanuit Microsoft Dynamics Lifecycle Services (LCS).  

## <a name="set-up-payment-survey-codes"></a>Betalingsonderzoekscodes instellen
1. Ga naar Btw > Instellingen > Buitenlandse handel > Betalingsonderzoekscodes.
2. Klik op Nieuw.
3. Typ een waarde in het veld Onderzoekscode.
4. Selecteer een optie in het veld Maand/kwartaal.
5. Selecteer een optie in het veld Berekening.
    * Als u Omzet selecteert in het veld Berekeningstype, worden de klant/leverancierstransacties die worden geboekt tijdens de rapportperiode overgebracht naar het betalingssaldo en is het bedrag dat wordt gerapporteerd het totale bedrag van de geboekte transactie.  Als u Saldo selecteert, worden de klant/leverancierstransacties die openstaan (niet volledig vereffend of gesloten) aan het einde van de rapportageperiode, overgebracht naar het betalingssaldo en is het bedrag dat wordt gerapporteerd het openstaande (niet-vereffende) bedrag van de geboekte transactie aan het einde van de rapportageperiode.  
6. Typ een waarde in het veld Omschrijving.
7. Typ een waarde in het veld Overzicht land/regio.
8. Klik op Toevoegen.
9. Typ of selecteer een waarde in het veld Doelcode centrale bank.
10. Schakel het selectievakje Betaling opnemen in.
    * Houd er rekening mee dat betalingstransacties standaard niet worden overgeboekt naar het betalingssaldo. De gebruiker moet het veld Betaling opnemen activeren voor doelcodes.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]