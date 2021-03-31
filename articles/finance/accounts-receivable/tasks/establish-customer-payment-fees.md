---
title: Tarieven voor klantbetalingen vaststellen
description: Maak betalingskosten voor klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e88eb888d3151fcc69f1bf11b2624a7e6d36444e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220222"
---
# <a name="establish-customer-payment-fees"></a>Tarieven voor klantbetalingen vaststellen

[!include [banner](../../includes/banner.md)]

Maak betalingskosten voor klantbetalingen.

Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga in het **navigatievenster** naar **Modules > Klanten > Instelling van betalingen > Bijzondere betalingskosten**.
2. Klik op **Nieuw**.
3. Typ een ID van bijzondere kosten in het veld **ID van bijzondere kosten**. De ID van bijzondere kosten wordt weergegeven in betalingsjournalen. Maak deze dus beschrijvend om te begrijpen welke bijzondere kosten in rekening worden gebracht.  
4. Geef in het veld **Naam** een naam voor de bijzondere kosten op.
5. Typ in het veld **Beschrijving van bijzondere kosten** een omschrijving voor de bijzondere kosten.
6. Geef in het veld **Toeslag** op of de bijzondere kosten in rekening worden gebracht aan de klant of aan een grootboekrekening. Als de bijzondere kosten aan de klant in rekening worden gebracht, selecteert u Klant. Als de bijzondere kosten in rekening worden gebracht aan uw organisatie als onkosten, selecteert u Grootboek. Selecteer Klant voor deze taak.  
7. Selecteer in het veld **Journaaltype** het type journaal dat deze bijzondere betalingskosten kan gebruiken. Als deze kosten worden gebruikt voor klantbetalingen, zal het journaaltype waarschijnlijk Klantbetaling zijn.  
8. Klik op **Opslaan**.
9. Klik op **Instellingen van bijzondere betalingskosten**. De instelling van bijzondere kosten wordt gebruikt om de criteria te definiëren voor wanneer de bijzondere kosten voor betaling in rekening worden gebracht.  Zo kunt u bijvoorbeeld definiëren dat de kosten worden berekend als de bankrekening USMF OPER en de betalingsmethode cheque is.  
10. Selecteer Tabel, Groep of Alle in het veld **Groeperingen** om te definiëren aan welke bankrekeningen deze bijzondere kosten in rekening worden gebracht. Als u Alle selecteert, kunnen deze kosten in rekening worden gebracht aan alle bankrekeningen.  Als u Tabel selecteert, kunnen deze bijzondere kosten alleen in rekening worden gebracht aan de bankrekening die u selecteert. Als u Groep selecteert, kunnen deze kosten alleen in rekening worden gebracht aan de bankrekeningen in de geselecteerde bankgroep.  
11. Selecteer een bankgroep of een bankrekening in het veld **Bankrelatie**. Als u Tabel hebt geselecteerd, worden met de zoekopdracht bankrekeningen weergegeven. Als u Groep hebt geselecteerd, worden met de zoekopdracht bankgroepen weergegeven.  
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Selecteer in het veld **Betalingsmethode** de betalingsmethode waarvoor deze kosten worden beoordeeld. Zo kunt u bijvoorbeeld bijzondere kosten in rekening brengen aan uw klanten als zij betalingen als cheque uitvoeren in plaats van als elektronische betaling.  
14. Zoek en selecteer de gewenste record in de lijst.
15. Voer, indien van toepassing, in het veld **Betalingsvaluta** een betalingsvaluta in. De betalingsvaluta wordt gebruikt als extra criterium voor het in rekening brengen van de bijzondere kosten.  Zo kan uw bank bijvoorbeeld extra bijzondere kosten in rekening brengen voor betalingen die in de valuta USD worden ontvangen, omdat zij doorgaans alleen transacties uitvoeren in de valuta EUR.  
16. Selecteer of de bijzondere kosten een percentage, bedrag of interval zijn.
17. Voer in het veld **Percentage/bedrag** ofwel een percentage of een bedrag van de bijzondere kosten in. Als in het veld Percentage/Bedrag de waarde Procent wordt gebruikt, is de hier ingevoerde waarde een percentage. Als in het veld Percentage/Bedrag de waarde Bedrag wordt gebruikt, is de waarde die u hier invoert een bedrag. Als de waarde in het veld Percentage/Bedrag Interval is, gebruikt u het tabblad Interval om de niveaus te definiëren.  
18. Selecteer in het veld **Valuta van kosten** de valuta van de bijzondere kosten. Dit is de valuta waarin de bijzondere kosten worden gemaakt.  
19. Klik op **Opslaan**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]