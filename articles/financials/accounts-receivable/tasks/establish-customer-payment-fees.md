--- 
title: Tarieven voor klantbetalingen vaststellen
description: Maak betalingskosten voor klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 659f4560747cea73c61a9b748a980946ca252bd6
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-fees"></a>Tarieven voor klantbetalingen vaststellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Maak betalingskosten voor klantbetalingen.

Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Klanten > Betalingsinstelling > Betalingskosten.
2. Klik op Nieuw.
3. Typ een ID van bijzondere kosten in het veld ID van bijzondere kosten.
    * De ID van bijzondere kosten wordt weergegeven in betalingsjournalen. Maak deze dus beschrijvend om te begrijpen welke bijzondere kosten in rekening worden gebracht.  
4. Geef in het veld Naam een naam voor de bijzondere kosten op.
5. Typ in het veld Beschrijving van bijzondere kosten een omschrijving voor de bijzondere kosten.
6. Selecteer of de bijzondere kosten in rekening worden gebracht aan de klant of aan een grootboekrekening.
    * Als de bijzondere kosten aan de klant in rekening worden gebracht, selecteert u Klant. Als de bijzondere kosten in rekening worden gebracht aan uw organisatie als onkosten, selecteert u Grootboek. Selecteer Klant voor deze taak.  
7. Selecteer het type journaal dat deze bijzondere betalingskosten kan gebruiken.
    * Als deze kosten worden gebruikt voor klantbetalingen, zal het journaaltype waarschijnlijk Klantbetaling zijn.  
8. Klik op Opslaan.
9. Klik op Instellingen van bijzondere betalingskosten.
    * De instelling van bijzondere kosten wordt gebruikt om de criteria te definiëren voor wanneer de bijzondere kosten voor betaling in rekening worden gebracht.  Zo kunt u bijvoorbeeld definiëren dat de kosten worden berekend als de bankrekening USMF OPER en de betalingsmethode cheque is.  
10. Selecteer Tabel, Groep of Alle om te definiëren aan welke bankrekeningen deze bijzondere kosten in rekening worden gebracht.
    * Als u Alle selecteert, kunnen deze kosten in rekening worden gebracht aan alle bankrekeningen.  Als u Tabel selecteert, kunnen deze bijzondere kosten alleen in rekening worden gebracht aan de bankrekening die u selecteert. Als u Groep selecteert, kunnen deze kosten alleen in rekening worden gebracht aan de bankrekeningen in de geselecteerde bankgroep.  
11. Selecteer een bankgroep of een bankrekening.
    * Als u Tabel hebt geselecteerd, worden met de zoekopdracht bankrekeningen weergegeven. Als u Groep hebt geselecteerd, worden met de zoekopdracht bankgroepen weergegeven.  
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Selecteer de betalingsmethode waarvoor deze bijzondere kosten in rekening worden gebracht.
    * Zo kunt u bijvoorbeeld bijzondere kosten in rekening brengen aan uw klanten als zij betalingen als cheque uitvoeren in plaats van als elektronische betaling.  
14. Zoek en selecteer de gewenste record in de lijst.
15. Voer, indien relevant, een betalingsvaluta in.
    * De betalingsvaluta wordt gebruikt als extra criterium voor het in rekening brengen van de bijzondere kosten.  Zo kan uw bank bijvoorbeeld extra bijzondere kosten in rekening brengen voor betalingen die in de valuta USD worden ontvangen, omdat zij doorgaans alleen transacties uitvoeren in de valuta EUR.  
16. Selecteer of de bijzondere kosten een percentage, bedrag of interval zijn.
17. Voer een percentage of bedrag van de bijzondere kosten in.
    * Als in het veld Percentage/Bedrag de waarde Procent wordt gebruikt, is de hier ingevoerde waarde een percentage. Als in het veld Percentage/Bedrag de waarde Bedrag wordt gebruikt, is de waarde die u hier invoert een bedrag. Als de waarde in het veld Percentage/Bedrag Interval is, gebruikt u het tabblad Interval om de niveaus te definiëren.  
18. Selecteer in het veld Valuta van kosten de valuta van de bijzondere kosten.
    * Dit is de valuta waarin de bijzondere kosten worden gemaakt.  
19. Klik op Opslaan.


