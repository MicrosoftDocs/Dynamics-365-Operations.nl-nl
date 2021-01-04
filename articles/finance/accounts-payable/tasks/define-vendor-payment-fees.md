---
title: Bijzondere kosten voor leveranciersbetalingen definiëren
description: Stel bijzondere kosten voor leveranciersbetalingen in.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 404bd1e22caa8098f114a2dcc67dd420509cce2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441802"
---
# <a name="define-vendor-payment-fees"></a>Bijzondere kosten voor leveranciersbetalingen definiëren

[!include [banner](../../includes/banner.md)]

Stel bijzondere kosten voor leveranciersbetalingen in. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Leveranciers > Betalingsinstelling > Betalingskosten.
2. Klik op Nieuw.
3. Typ een waarde in het veld ID van bijzondere kosten.
    * De id van bijzondere kosten moet aangeven wanneer deze kosten worden gebruikt, zoals "EFT-kosten".  
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Beschrijving van bijzondere kosten.
    * Voeg een omschrijving toe om nadere details te verstrekken over wanneer de kosten in rekening worden gebracht.  
6. Selecteer in het veld Toeslag de optie Leverancier of Grootboek.
    * Grootboek wordt gebruikt wanneer het tarief in rekening wordt gebracht aan uw organisatie.  Leverancier wordt gebruikt wanneer de kosten in rekening worden gebracht aan de leverancier.  
7. Voer een hoofdrekening in waaraan de bijzondere kosten in rekening worden gebracht.
    * Deze optie is alleen beschikbaar als Grootboek wordt geselecteerd als optie bij Toeslag.  
8. Selecteer het journaal waarin deze kosten kunnen worden gebruikt. 
    * Voor bijzondere kosten leveranciersbetaling selecteert u het journaal "Voorschot van leverancier".  
9. Klik op Opslaan.
10. Klik op Instellingen van bijzondere betalingskosten.
    * Ga naar de instellingen voor de bijzondere betalingskosten om te definiëren wanneer de kosten standaard moeten worden opgenoemn in het journaal dat u hebt geselecteerd.  
11. Selecteer Tabel, Groep of Alle.
    * Tabel wordt gebruikt om één bankrekening te selecteren, Groep wordt gebruikt om een bankgroep te selecteren en Alle dient om deze kosten in te stellen voor alle bankrekeningen  
12. Selecteer een bankgroep of een bankrekening.
    * De zoekopdracht geeft bankgroepen weer als u Groep hebt geselecteerd en bankrekeningen als u Tabel hebt geselecteerd.  
13. Selecteer de betalingsmethode waarvoor deze bijzondere kosten in rekening worden gebracht.
14. Selecteer de betalingsspecificatie voor de geselecteerde betalingsmethode.
    * De betalingsspecificatie wordt gebruikt met de betalingsmethoden van EFT (Electronic Funds Transfer).  
15. Selecteer of de bijzondere kosten een percentage, bedrag of interval zijn.
16. Voer het percentage of bedrag van de bijzondere kosten in.
    * Als Kosten een percentage is, voert u het percentage in. Als Kosten een bedrag is, voert u het bedrag van de bijzondere kosten in. Als Kosten een interval is, gebruikt u het tabblad Interval om de gelaagde kosten te definiëren.  
17. Selecteer in het veld Valuta van kosten de valuta waarvoor de bijzondere kosten worden berekend.
    * Deze valuta is voor de bijzondere kosten. De betalingsvaluta wordt gebruikt om te bepalen wanneer de regel voor bijzondere kosten moet worden beoordeeld op basis van de valuta van de betaling. Zo kan uw bank bijvoorbeeld bijzondere kosten in rekening brengen wanneer een betaling wordt gedaan in EUR, terwijl voor alle andere betalingen geen kosten worden berekend.  
18. Klik op Opslaan.

