---
title: Grootboektoewijzingsjournaal verwerken
description: Gebruik de pagina Toewijzingsaanvraag verwerken om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingjournaal kan ook rechtstreeks naar het grootboek worden geboekt.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550816"
---
# <a name="process-ledger-allocation-journal"></a>Grootboektoewijzingsjournaal verwerken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebruik de pagina Toewijzingsaanvraag verwerken om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingjournaal kan ook rechtstreeks naar het grootboek worden geboekt. Voordat u een toewijzingsjournaal kunt maken, moet u minstens één actieve Grootboektoewijzingsregel maken. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Grootboek > Toewijzingen > Toewijzingsaanvraag verwerken.
2. Klik in het veld Regel op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer het gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Voer in het veld Begindatum een datum in.
    * De Begindatum is zeer belangrijk wanneer het Grootboek de Gegevensbron voor de regel is. Deze datum bepaalt welke grootboeksaldi voor toewijzing worden opgenomen.     Selecteer Stoppen in het veld Nul bron. Hierdoor wordt het toewijzingsproces gestopt en wordt een bericht weergegeven waarin wordt gemeld dat er een bronbedrag is geselecteerd.  
6. Selecteer 'Alleen voorstel' in het veld Voorstelopties.
    * Selecteer Alleen voorstel om het resultaat in Toewijzingsjournalen te controleren en eventueel goed te keuren vóór het boeken van de toewijzing naar het Grootboek.  
7. Voer in het veld Boekingsdatum GB een datum in.
8. Klik op OK.
9. Ga naar Grootboek > Toewijzingen > Toewijzingsjournalen.
10. Klik op Regels.
11. Klik op Boeken.
12. Klik op Boeken.

