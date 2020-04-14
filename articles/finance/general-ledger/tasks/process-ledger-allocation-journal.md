---
title: Grootboektoewijzingsjournaal verwerken
description: In dit onderwerp wordt uitgelegd hoe u een toewijzingsaanvraag in Dynamics 365 Finance kunt verwerken.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144954"
---
# <a name="process-ledger-allocation-journal"></a>Grootboektoewijzingsjournaal verwerken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een toewijzingsaanvraag kunt verwerken. Gebruik de pagina Toewijzingsaanvraag verwerken om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingjournaal kan ook rechtstreeks naar het grootboek worden geboekt. Voordat u een toewijzingsjournaal kunt maken, moet u minstens één actieve Grootboektoewijzingsregel maken. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga in het navigatievenster naar **Modules > Grootboek > Toewijzingen > Toewijzingsaanvraag verwerken**.
2. Selecteer in het veld **Regel** de gewenste record in het vervolgkeuzemenu.
3. Voer in het veld **Begindatum** een datum in.

    - De **Begindatum** is zeer belangrijk wanneer het Grootboek de Gegevensbron voor de regel is. Deze datum bepaalt welke grootboeksaldi voor toewijzing worden opgenomen.  
    - Selecteer **Stoppen** in het veld **Nul bron**. Hierdoor wordt het toewijzingsproces gestopt en wordt een bericht weergegeven waarin wordt gemeld dat er een bronbedrag is geselecteerd.  

4. Selecteer **Alleen voorstel** in het veld **Voorstelopties**. Selecteer **Alleen voorstel** om het resultaat in Toewijzingsjournalen te controleren en eventueel goed te keuren vóór het boeken van de toewijzing naar het Grootboek.  
5. Voer in het veld Boekingsdatum GB een datum in.
6. Selecteer **OK**.
7. Ga in het navigatievenster naar **Modules > Grootboek > Toewijzingen > Toewijzingsjournalen**.
8. Selecteer **Regels**
9. Selecteer **Boeken**.
10. Selecteer **Boeken**.

