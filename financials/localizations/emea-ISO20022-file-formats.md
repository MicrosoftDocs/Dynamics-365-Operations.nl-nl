---
title: ISO20022-bestanden importeren
description: In dit onderwerp wordt uitgelegd hoe u betalingsbestanden in de ISO 20022-indelingen camt.054 en pain.002 importeert in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: neserovleo
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 77a0d4c2a31128fb7d082238d443f297fd40664f
ms.openlocfilehash: 90e21bb939bd96a3420decb5f9bc07c017c3e946
ms.contentlocale: nl-nl
ms.lasthandoff: 07/31/2017

---

# <a name="import-iso20022-files"></a>ISO20022-bestanden importeren

## <a name="overview"></a>Overzicht
U kunt betalingsbestanden met de volgende indelingen importeren:

 - **ISO20022 camt.054 kredietbrief**: inkomende betalingen importeren uit een bestand in deze indeling in het klantbetalingsjournaal.
 - **ISO20022 pain.002 retourstatus** en **ISO20022 camt.054 debetadvies**: retourbestanden importeren in deze indelingen in het AP-betalingsoverboekingsjournaal.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Vereisten voor het importeren van het camt.054-bestand met kredietbrief
U moet aan de volgende vereisten voldoen om bankmeldingen in de indeling camt.054.001.002 te importeren in het klantbetalingsjournaal.

1. Importeer de configuratie voor de elektronische rapportage (ER) **ISO20022 camt.054** uit Microsoft Dynamics Lifecycle Services (LCS). Selecteer vervolgens op de pagina **Betalingsmethode van klant** in het veld **Indelingsconfiguratie importeren** die configuratie. Zie [Bestandsindelingen voor betalingsmethoden](emea-select-file-formats-for-the-method-of-payments.md) voor meer informatie.
2. Voer op de pagina **Alle klanten** een naam en een organisatienummer voor elke klant in.
3. Stel op de pagina **Bankrekening van klant** een record voor de bankrekening van de klant in door de volgende informatie in te voeren: IBAN of bankrekeningnummer en SWIFT-code of routeringsnummer.
4. Stel op de pagina **Bankrekeningen** bankrekeningen voor de rechtspersonen in door de volgende informatie in te voeren: IBAN of bankrekeningnummer en SWIFT-code of routeringsnummer, valuta en adres.

    > [!NOTE]
    > Als u van plan bent Geavanceerde bankafstemming te gebruiken, stelt u op het sneltabblad **Afstemming** de optie **Geavanceerde bankafstemming** in op **Ja**. Als u niet-geboekte geïmporteerde betalingen wilt afstemmen, stelt u de optie **Bankafschriften gebruiken als bevestiging van elektronische betalingen** in op **Ja**.

5. Optioneel: stel op de pagina **Toewijzing van transactiecode** de toewijzing in tussen banktransactiecodes in de bestands- en banktransactietypen.
6. Als het bestand transactietoeslagen bevat die u samen met de inkomende betaling wilt boeken, maakt u een post voor bijzondere betalingskosten op de pagina **Bijzondere kosten voor klantbetalingen**. Klik vervolgens op de pagina **Betalingsmethoden** en koppel de bijzondere betalingskosten aan de bankrekening in de instelling voor betalingskosten.
7. Als de ESR-betalingen worden geïmporteerd en ISR-verwijzingen bevatten (van toepassing voor rechtspersonen in Zwitserland), voert u de volgende instellingen uit:

    - Voer in het veld **Betalingen van klant, rekeninglengte** de lengte van de klantcode in die wordt gebruikt in de ISR-verwijzingen of voor automatische identificatie van de klant.
    - Zorg ervoor dat het klantnummer en het factuurnummer (nummerreeksen) alleen cijfers bevatten. Ze mogen geen andere tekens bevatten. Het factuurnummer mag geen voorloopnullen bevatten.
    - Voer ESR, BESR en routeringsnummer in voor de bankrekening van de rechtspersoon. Zie voor meer informatie [Verouderde ESR-functie](emea-che-esr-customer-payments-import.md), omdat dezelfde instellingen vereist zijn.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Het bestand camt.054 met de kredietbrief in het klantbetalingsjournaal importeren
1. Klik op de pagina **Journaalregels met betalingen van klant** op **Functies** > **Betalingen importeren**.
2. Selecteer de betalingsmethode met de vereiste instellingen voor de indeling ISO20022 camt.054.
3. Geef de vereiste parameters en het bestandspad op en klik op **OK**.

Het bestand wordt geïmporteerd.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Vereisten voor het importeren van bestanden in de ISO20022-indelingen voor pain.002 retourstatus en ISO20022 camt.054 debetadvies in het AP-betalingsoverboekingsjournaal.
Voltooi eerst de volgende vereisten voor het importeren van bankberichten in de volgende ISO20022-indelingen op de pagina **Leverancierbetalingen**: pain.002.001.003 statusretourberichten en camt.054.001.002 debetadvies.

1. Importeer ER-configuraties **ISO20022 camt.054** en **ISO20022 pain.002** uit LCS.
2. Selecteer op de pagina **Betalingsmethode van leverancier** in de velden **Configuratie van retourindeling** en **Secundaire configuratie van retourindeling** de ER-configuraties die u hebt geïmporteerd. U moet de algemene elektronische retourindeling voor de geselecteerde betalingsmethode activeren.
3. Stel op de pagina **Toewijzing van indelingsstatus retourneren** de toewijzing van statuscodes in tussen pain.002 en Journaal met betalingen van leverancier.

    Hier volgt een voorbeeld van een statusinstellingen.

    Retourstatus | Betalingsstatus
    --------------|---------------
    RJCT          | Afgewezen
    ACCP          | Geaccepteerd
    ACSP          | Ontvangen

4. Stel op de **Foutcodes voor retourindelingen** de foutcodes en omschrijvingen voor pain.002 in conform de externe redencodes voor de ISO20022-status.

    Hier volgt een voorbeeld van een deel van de foutcode-instellingen.

    Code | Naam
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Als het camt.054-bestand transactietoeslagen bevat die u samen met de inkomende betaling wilt boeken, maakt u een post voor bijzondere betalingskosten op de pagina **Bijzondere kosten voor leverancierbetalingen**. Klik vervolgens op de pagina **Betalingsmethoden** en koppel de bijzondere betalingskosten aan de bankrekening in de instelling voor betalingskosten.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Bestanden met de pain.002-retourstatus of camt.054-debetadvies importeren in het Journaal met betalingen van leverancier
1. Open de pagina **Betalingsoverboekingen** in het menu Leveranciers.
2. Op de pagina **Betalingsoverboekingen** klikt u op **Retourbestand - leverancier**.
3. Selecteer de betalingsmethode met de vereiste instellingen voor de ISO20022-bestanden en klik op **OK**.
4. Selecteer de bestandsindeling die u wilt importeren en klik op **OK**.
5. Geef de vereiste parameters en het bestandspad op en klik op **OK**.

Als u het bestand pain.002 importeert, wordt de status van de leveranciersbetalingsregels bijgewerkt, op basis van de informatie in het geïmporteerde bestand.

Als u het bestand camt.054 importeert, moet u de volgende aanvullende parameters opgeven:

- **ID van bijzondere kosten**: met de ID van bijzondere kosten definieert u nieuwe regels voor betalingskosten die op de betalingsjournaalregel van de leverancier worden gemaakt, als het bestand camt.054 een bedrag voor toeslagen omvat.
- **Nieuwe journaalnaam** en **Nieuwe journaalomschrijving**: voer de naam en de omschrijving van het journaal in waarnaar de verwerkte transacties worden overgeboekt. Na de overboeking moeten de nieuwe boekstuknummers worden toegewezen in het nieuwe journaal.
- **Automatische afschrijvingstransacties importeren**: stel deze optie in op **Ja** als uitgaande automatische afschrijvingen moeten worden geïmporteerd in het leveranciersbetalingsjournaal.
- **Journaalnaam** : definieer een nieuwe journaalnaam voor de geïmporteerde automatische afschrijvingstransacties.
- **Transacties vereffenen**: stel deze optie in op **Ja** als geïmporteerde leveranciersbetalingen moeten worden vereffend met facturen die zijn gevonden in het systeem.

U kunt de geïmporteerde informatie bekijken op de pagina **Betalingsoverboekingen**. 

## <a name="additional-details"></a>Extra details

Wanneer u een indelingsconfiguratie van LCS importeert, kunt u de hele configuratiestructuur importeren, wat betekent dat de Model- en de Modeltoewijzingsconfiguraties zijn opgenomen. In het model voor betaling vanaf versie 8 bevinden de toewijzingen zich in aparte ER-configuraties in de oplossingenstructuur (toewijzing betalingsmodel 1611, toewijzing betalingsmodel aan bestemming ISO20022, enzovoort). Er zijn veel verschillende betalingsindelingen in één model (Betalingsmodel), dus is het van belang om de toewijzingen afzonderlijk te verwerken voor eenvoudige oplossingsbeheer. Bekijk bijvoorbeeld dit scenario: u gebruikt ISO20022-betalingen om kredietoverboekingsbestanden te genereren en vervolgens importeert u de retourberichten van de bank. In dit scenario moet u de volgende configuraties gebruiken:

 - **Betalingsmodel**
 - **Betalingsmodeltoewijzing 1611**: deze toewijzing wordt gebruikt voor het genereren van het exportbestand
 - **Betalingsmodeltoewijzing naar bestemming ISO20022**: deze configuratie bevat alle toewijzingen die worden gebruikt om de gegevens (toewijzingsrichting 'naar bestemming') te importeren
 - **ISO20022 kredietoverdracht**: deze configuratie omvat een indelingsonderdeel dat verantwoordelijk is voor het genereren van exportbestanden (pain.001) op basis van betalingsmodeltoewijzing 1611, alsmede een indeling om het toewijzingsonderdeel vorm te geven dat samen met de betalingsmodeltoewijzing naar bestemming ISO20022 wordt gebruikt om geëxporteerde betalingen te registreren in het systeem voor verdere importdoeleinden (import in technische tabel CustVendProcessedPayments)
 - **ISO20022 kredietoverdracht (CE)**, waarbij CE overeenkomt met de landextensie: afgeleide indeling voor de ISO20022 kredietoverdracht met dezelfde structuur en met bepaalde landspecifieke verschillen
 - **Pain.002**: deze indeling wordt samen met de betalingsmodeltoewijzing naar bestemming ISO20022 gebruikt om het bestand pain.002 te importeren in het journaal met leverancierbetalingsoverboekingen
 - **Camt.054**: deze indeling wordt samen met de betalingsmodeltoewijzing naar bestemming ISO20022 gebruikt om het bestand camt.054 te importeren in het journaal met leverancierbetalingsoverboekingen Dezelfde indelingsconfiguratie wordt gebruikt voor de importfunctionaliteit voor klantbetalingen, maar de andere toewijzing wordt gebruikt in de configuratie van betalingsmodeltoewijzing voor bestemming ISO20022.

Raadpleeg voor meer informatie over de elektronische aangifte [Overzicht van elektronische rapportage](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="additional-resources"></a>Aanvullende resources
- [Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [Configuratie van ISO20022-kredietoverdracht importeren](./tasks/import-iso20022-credit-transfer-configuration.md)
- [Configuratie van ISO20022 automatische afschrijving importeren](./tasks/import-iso20022-direct-debit-configuration.md)
- [Bankrekeningen voor ISO20022-kredietoverdrachten voor een bank instellen](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [Klanten en bankrekeningen van klanten instellen voor ISO20022-automatische overschrijvingen](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [Betalingsmethode voor ISO20022-kredietoverdracht instellen](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [Betalingsmethode voor ISO20022 automatische incasso instellen](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [Leveranciers en bankrekeningen voor leveranciers voor ISO20022-kredietoverdrachten instellen](./tasks/set-up-vendor-iso20022-credit-transfers.md)

