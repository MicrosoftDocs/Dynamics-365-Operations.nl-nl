---
title: Een bankrekening afstemmen
description: In dit onderwerp wordt beschreven hoe u een bankrekening afstemt.
author: panolte
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e06a38a19a16a07d77d0c9aceaa4e3206646dd0561996681b417b785058f3938
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739354"
---
# <a name="reconcile-a-bank-account"></a>Een bankrekening afstemmen

[!include[banner](../includes/banner.md)]

Wanneer een bankafschrift ontvangt, moet u de banktransacties van de rechtspersoon afstemmen met de transacties op het bankafschrift.

U kunt een rekeningafschrift niet afstemmen op een bankrekening als een van de cheques of stortingsbewijzen die op het afschrift staan vermeld op dit moment de status **In afwachting van annulering** heeft. Nadat een controleur een cheque heeft geboekt of de intrekking van een cheque of stortingsbewijs heeft geweigerd, is de status niet meer **In afwachting van annulering** en kunt u de bankrekening afstemmen.

1.  Ga naar **Contanten en bankbeheer** \> **Bankrekeningen** \> **Bankrekeningen**. Selecteer de bankrekening die u wilt afstemmen met het bankafschrift en selecteer **Afstemmen** > **Rekening afstemmen**.

2.  Voer gegevens in de velden **Datum bankafschrift** en **Bankafschrift** in. In het veld **Eindsaldo** voert u het saldo in van de bankrekening zoals dit wordt vermeld op het afschrift.

3.  Selecteer **Transacties** om de pagina **Rekeningafstemming** te openen.

4.  Voor elke transactie die wordt opgenomen op het bankafschrift schakelt u het selectievakje **Verrekend** in, als het bedrag in Dynamics 365 Finance overeenkomt met het bedrag op het bankafschrift. U kunt ook de waarde in het veld **Banktransactietype** invoeren of wijzigen. Deze veldwaarde is belangrijk voor de banktransactiestatistieken en voor een aantal rapporten.
    

    > [!NOTE]
    > <P>Schakel het selectievakje <STRONG>Verrekend</STRONG> niet in voor transacties die niet worden vermeld op het bankafschrift. Deze transacties verdwijnen pas van deze pagina als ze zijn afgestemd op een toekomstig bankafschrift.</P>
    > <P>Het selectievakje <STRONG>Verrekend</STRONG> is niet beschikbaar als de transactie de status <STRONG>In afwachting van annulering</STRONG> heeft. Transacties kunnen deze status krijgen als Finance zo is ingesteld dat omkeringen of annuleringen ter controle moeten worden verzonden voordat deze worden geboekt. Nadat een controleur de intrekking of annulering heeft geboekt of afgewezen, is de status niet meer <STRONG>In afwachting van annulering</STRONG> en kunt u de bankrekening afstemmen met het afschrift.</P>

    
    Om het selectievakje **Verrekend** in te schakelen voor een interval van cheques die allemaal op het bankafschrift worden vermeld, klikt u op **Cheque-interval markeren** en geeft u het interval op.

5.  Als het bedrag voor een bankrekeningtransactie niet overeenkomt met het bedrag voor de transactie op het bankafschrift, voert u het bedrag van de correctie in het veld **Correctiebedrag** in.
    

    > [!NOTE]
    > <P>Als de boekperiode van de te corrigeren transactie is afgesloten, kunt u het veld <STRONG>Correctiebedrag</STRONG> niet gebruiken. In plaats daarvan maakt u een regel met een transactiedatum die in een open boekperiode valt voor de correctie. In dit geval moet u de financiële dimensies toevoegen die zijn gebruikt op de oorspronkelijke transactie evenals de hoofdtegenrekening.</P>



6.  Maak transacties voor invoer, zoals kosten en rente, die op het bankrekeningoverzicht worden vermeld maar niet zijn vastgelegd in Finance. Voer het **Banktransactietype** en de juiste financiële dimensies in.

7.  Aangezien de transacties op het bankafschrift zijn gemarkeerd als **Verrekend**, nadert het bedrag in het veld **Niet-afgestemd**, dat continu wordt herberekend terwijl u wijzigingen aanbrengt, nul. Wanneer deze waarde gelijk is aan nul, selecteert u **Rekening afstemmen** om de afstemming en de transacties en correcties die u hebt gemaakt, te boeken.
    
    Nadat de afstemming is geboekt, kunnen de transacties die zijn meegenomen niet meer worden gewijzigd of gecorrigeerd, en worden ze niet meer weergegeven in toekomstige rekeningafstemmingen.

8.  Gebruik het rapport **Niet-afgestemde banktransacties** om banktransacties weer te geven die nog niet zijn afgestemd. Als u het bankafschrift voor een bankrekening wilt weergeven, gebruikt u het rapport **Bankafschrift**.

## <a name="cancel-bank-statement-reconciliation"></a>Afstemming van bankafschriften annuleren 

Met de functie Afstemming bankafschrift annuleren kunt u de afstemming van bankafschriften annuleren. Als u deze functie wilt gebruiken, schakelt u de functie **Afstemming bankafschrift annuleren** in de werkruimte **Functiebeheer** in. U moet ook de parameter **Bewerken van bankafschriften toestaan** inschakelen. Als u dit wilt doen, gaat u naar **Contanten en bankbeheer > Instellen > Parameters voor Contanten en bankbeheer > Bankafstemming**.
 
Afstemmingen van bankafschriften kunnen alleen worden geannuleerd in de chronologische volgorde waarin ze zijn geboekt. Wanneer een afstemming van bankafschriften wordt geannuleerd, worden nieuwe transacties en correcties teruggedraaid en worden alle andere transacties als niet-afgestemd gemarkeerd.
 
Als u de afstemming van bankafschriften wilt annuleren, selecteert u het bankafschrift en selecteert u **Bankafschrift > Bankafstemming annuleren**. Geef op de pagina **Bankafstemming annuleren** de **Redencode**, een **Opmerking bij reden** en de **Annuleringsdatum** op. Selecteer **OK** om te beginnen met annuleren. Opmerking: de annuleringsdatum van het bankafschrift moet op of na de datum van het bankafschrift liggen. Nadat de afstemming van het bankafschrift is geannuleerd, wordt het veld **Annuleringsdatum** voor het bankafschrift bijgewerkt met de opgegeven **Annuleringsdatum**. Selecteer de knop **Transacties** om de transacties weer te geven waarvoor de afstemming is geannuleerd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]