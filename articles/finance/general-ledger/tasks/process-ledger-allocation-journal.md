---
title: Grootboektoewijzingsjournaal verwerken
description: In dit artikel wordt uitgelegd hoe u een toewijzingsaanvraag in Dynamics 365 Finance kunt verwerken.
author: aprilolson
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779387"
---
# <a name="process-ledger-allocation-journal"></a>Grootboektoewijzingsjournaal verwerken

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een toewijzingsaanvraag kunt verwerken. Gebruik de pagina **Toewijzingsaanvraag verwerken** om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingsjournaal kan ook rechtstreeks naar het grootboek worden geboekt. Voordat u een toewijzingsjournaal kunt maken, moet u minstens één actieve Grootboektoewijzingsregel maken. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga in het navigatievenster naar **Grootboek > Toewijzingen > Toewijzingsaanvraag verwerken**.
2. Selecteer in het veld **Regel** de gewenste record in het vervolgkeuzemenu.
3. Voer in het veld **Begindatum** een datum in.

    - De **Begindatum** is zeer belangrijk wanneer het Grootboek de Gegevensbron voor de regel is. Deze datum bepaalt welke grootboeksaldi voor toewijzing worden opgenomen.  
    - Selecteer **Stoppen** in het veld **Nul bron**. Hierdoor wordt het toewijzingsproces gestopt en wordt een bericht weergegeven waarin wordt gemeld dat er een bronbedrag is geselecteerd.  

4. Selecteer **Alleen voorstel** in het veld **Voorstelopties**. Selecteer **Alleen voorstel** om het resultaat in **Toewijzingsjournalen** te controleren en eventueel goed te keuren vóór het boeken van de toewijzing naar het Grootboek.  
5. Voer in het veld **Boekingsdatum GB** een datum in.
6. Selecteer **OK**.
7. Ga in het navigatievenster naar **Modules > Grootboek > Toewijzingen > Toewijzingsjournalen**.
8. Selecteer **Regels**
9. Selecteer **Boeken**.
10. Selecteer **Boeken**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
