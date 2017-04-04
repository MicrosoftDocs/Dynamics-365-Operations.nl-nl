---
title: Een leveranciersbetaling omkeren
description: Dit artikel bevat de verschillen tussen het omkeren, verwijderen, ongeldig maken en afwijzen van een betaling. Bovendien worden de twee manieren om een leverancierscheque om te keren uitgelegd.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 716134b2230683050b234297e475d9331fbc7dab
ms.lasthandoff: 03/31/2017


---

# <a name="reverse-a-vendor-payment"></a>Een leveranciersbetaling omkeren

Dit artikel bevat de verschillen tussen het omkeren, verwijderen, ongeldig maken en afwijzen van een betaling. Bovendien worden de twee manieren om een leverancierscheque om te keren uitgelegd. 

Soms moet een leveranciersbetaling, nadat deze is geboekt, worden omgekeerd. Omkering verschilt van verwijderen, ongeldig maken of afwijzen van een betaling. U kunt een betaling alleen verwijderen als de status **Gemaakt** is. Deze status geeft aan dat de betaling is gemaakt maar nog niet is gegenereerd. Deze beperking altijd van toepassing is, ongeacht de betalingsmethode. U kunt niet-geboekte cheques vernietigen nadat ze zijn gegenereerd, maar voordat ze zijn geboekt. Als de gegenereerde betaling wordt uitgevoerd als een elektronische Fonds transfer (EFT), kunt u de betaling weigeren voordat deze wordt geboekt. Wijzigen voor het afwijzen van een betaling, de **betalingsstatus** waarde. Een betaling die is geannuleerd of geweigerd, kan worden hersteld na de **betalingsstatus** waarde wordt gewijzigd naar **geen**. 

Nadat een betaling is geboekt, worden omkeringen van cheques gebruikt. Betalingen die elektronisch zijn gemaakt, kunnen niet worden omgekeerd nadat ze zijn geboekt. In plaats daarvan wordt moet een nieuwe transactie worden gemaakt voor het bedrag van de betaling voor de aansprakelijkheid terug op de leveranciersrekening. Er zijn twee methoden voor het omkeren van geboekte cheques. Bij één methode worden omkeringen direct geboekt wanneer u op **Omkering van betaling** op de pagina **Cheque** klikt. Bij de andere methode wordt bij het klikken op **Betaling omkeren** op de pagina **Cheque** de omkering verzonden naar het journaal voor omkering van cheques in kas- en bankbeheer, waarbij een revisor de omkering vervolgens kan boeken of afwijzen. 

Controleer welke methode uw organisatie gebruikt op de pagina **Parameters voor cash- en bankbeheer**. Als de optie **Controleproces voor betalingsomkeringen gebruiken** is ingesteld op **Ja**, worden omkeringen verzonden naar het journaal voor omkering van cheques voor controle. De volgende tabel beschrijft hoe de methoden voor omkeren van cheques van elkaar verschillen.

| Als uw organisatie geen omkeringen van cheques controleert voor het boeken                                                                                                                                  | Als uw organisatie omkeringen van cheques controleert voor het boeken                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De cheque wordt onmiddellijk omgekeerd als u op **OK** op de pagina **Cheque** klikt.                                                                                                                      | De cheque wordt niet direct omgekeerd. Een journaal voor het omkeren van de cheque wordt gemaakt voor controle. Als het journaal voor omkering van de cheque wordt verwijderd, kan de cheque opnieuw worden omgekeerd.                                                                                                                                                                                                                                                                |
| De journaalregels voor de oorspronkelijke cheque worden omgekeerd.                                                                                                                                         | De grootboekrekening van de post voor de oorspronkelijke cheque wordt mogelijk niet geboekt. De financiële dimensies van het journaal van de oorspronkelijke cheque worden gebruikt als de standaard financiële dimensies in het journaal van de omkering van de cheque. U kunt deze standaardwaarden wijzigen. Wanneer het journaal van de chequeomkering wordt geboekt, worden de hoofdrekeningen voor Leveranciers automatisch ingevoerd vanaf de boekingsprofielen die misschien zijn gewijzigd. |
| De boekhoudstructuren die zijn gebruikt wanneer de oorspronkelijke cheque is geboekt, worden gebruikt om de cheque om te keren, zelfs als de rekeningstructuur is gewijzigd. De rekeningcombinatie wordt niet gevalideerd. | Als een rekeningstructuur werd gewijzigd nadat de oorspronkelijke cheque is geboekt, kan een nieuwe financiële dimensie zijn vereist voor de omkering van de cheque. Deze financiële dimensie wordt misschien niet automatisch ingevoerd vanaf het journaal van de oorspronkelijke betaling. De rekeningcombinatie wordt gevalideerd wanneer de omkering van de cheque wordt geboekt.                                                                                                        |
| Vaste dimensies worden niet toegepast op de omkering, om ervoor te zorgen dat dezelfde grootboekrekeningen worden omgekeerd.                                                                                      | Vaste dimensies worden toegepast op het journaal voor omkering van de cheque tijdens het boeken. De financiële dimensiewaarde bestaat mogelijk niet in de post voor de oorspronkelijke cheque, afhankelijk van wanneer de vaste dimensie werd gedefinieerd.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Omkeren van geboekte cheques zonder deze te controleren
Als uw organisatie omkeringen van cheques onmiddellijk wil boeken wanneer u op **Omkering van betaling** op de pagina **Cheques** klikt. Stel op de pagina **Parameters voor cash- en bankbeheer** de optie **Controleproces voor betalingsomkeringen gebruiken** in op **Nee**. Op de pagina **Cheques** kunt u de cheque selecteren die u wilt omkeren en **Omkering van betaling** selecteren. Geef vervolgens de datum op en selecteer een reden voor de omkering.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Geboekte cheques omkeren nadat deze zijn gecontroleerd in het journaal voor het omkeren van een cheque
Als uw organisatie omkeringen van cheques wil controleren voordat ze worden geboekt, maakt u een journaal voor chequeomkeringen voor controle en stelt u op de pagina **Parameters voor cash- en bankbeheer** de optie **Controleproces voor betalingsomkeringen gebruiken** in op **Ja**. Op de pagina **Cheques** kunt u de cheque selecteren die u wilt omkeren en **Omkering van betaling** selecteren. Geef vervolgens de datum op en selecteer een reden voor de omkering. U moet ook een journaalnaam selecteren om een journaal in het journaal voor chequeomkeringen te maken.

### <a name="review-a-reversal"></a>Een omkering controleren

Als u een gebruiker bent die omkeringen moet controleren, kunt u het journaal goedkeuren en boeken, ofwel de omkering afwijzen door het journaal te verwijderen. Op de pagina **Journaal voor chequeomkeringen** kunt u het omkeringsjournaal selecteren dat u wilt controleren, en vervolgens op **Regels** klikken. U kunt de omgekeerde cheque controleren en dan een van de volgende goedkeuringsopties selecteren:

-   Klik op **Boeken** of **Boeken en overboeken** als u het omkeringsjournaal wilt goedkeuren en boeken.
-   Als u de omkering wilt weigeren, verwijdert u het journaal voor chequeomkering.

> [!NOTE]
> Als u het journaal verwijderen, de omkering uit het systeem is verwijderd, maar blijft de originele cheque aanwezig op de **controleren op** pagina. De status van de cheque is niet langer **In afwachting van annulering**.

## <a name="results-of-posting-a-reversal"></a>Resultaten van het boeken van een omkering
Wanneer u een chequeomkering boekt, gebeurt het volgende:

-   De chequestatus wordt bijgewerkt naar de status **Annulering**.
-   Als de optie **Afstemmen** op de omkeringspagina tijdens de omkering was ingeschakeld, wordt de cheque afgestemd (de optie **Afgestemd** wordt ingeschakeld) en wordt deze niet weergegeven op de pagina **Rekeningafstemming**.
-   Het omkeringsboekstuk wordt tegengeboekt op de bankrekening waarmee de cheque is uitgegeven, om het bankrekeningsaldo te verhogen.
-   Het boekstuk wordt geboekt in het grootboek.
-   De wijzigingsgegevens worden bijgewerkt in de veldgroep **Geschiedenis** op de pagina **Cheque**.

> [!NOTE] 
> Wanneer u een cheque omkeert die is uitgegeven voor een intercompany-transactie, komen de tegenrekeningvermeldingen uit de instellingen van de intercompany-boekhouding, en niet uit de originele transactie. Als de cheque die is omgekeerd is uitgegeven voor een leveranciersbetaling, gebeurt ook het volgende:

-   De originele betaling van de factuur waarmee de betaling is vereffend, wordt ongedaan gemaakt (de vereffening wordt omgekeerd).
-   Een transactie wordt op de leveranciersrekening tegengeboekt voor de betalingsomkering, en de omgekeerde betaling wordt vereffend met de oorspronkelijke betaling. Het veld **Laatste vereffeningsboekstuk** op de pagina **Leverancierstransacties** voor het oorspronkelijke voorschot van leverancier wordt bijgewerkt met het boekstuknummer van de omgekeerde transactie.

Als de cheque die is omgekeerd is uitgegeven voor een klantrestitutie, gebeurt ook het volgende:

-   Een transactie wordt op de klantrekening tegengeboekt voor de betalingsomkering, en de vereffening tussen de oorspronkelijke betaling en het document waarmee de betaling oorspronkelijk was vereffend, wordt omgekeerd (er wordt een negatieve betaling gemaakt).
-   Er wordt een betalingsomkering toegepast op de oorspronkelijke betaling. Het veld **Laatste vereffeningsboekstuk** op de pagina **Klanttransacties** voor de oorspronkelijke klantbetaling wordt bijgewerkt met het boekstuknummer van de omgekeerde transactie.



