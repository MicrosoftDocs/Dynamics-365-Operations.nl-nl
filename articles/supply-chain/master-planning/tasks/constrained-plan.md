---
title: Een plan met beperkingen genereren
description: In dit artikel ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65884d556724cd6132fe328e95a5bec78885c174
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904009"
---
# <a name="generate-a-constrained-plan"></a>Een plan met beperkingen genereren

[!include [banner](../../includes/banner.md)]

In dit artikel ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt. Het plan garandeert dat de productie niet start voordat de materialen beschikbaar zijn en dat resources niet worden overboekt. 

Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de productieplanner.


## <a name="set-up-a-constrained-plan"></a>Een plan met beperkingen instellen
1. Selecteer op de startpagina het werkgebied **Hoofdplanning**.
2. Selecteer **Hoofdplannen** in de lijst met koppelingen aan de rechterkant van het werkgebied.
3. Zoek en selecteer de gewenste record in de lijst. Voorbeeld: **StaticPlan**  
4. Selecteer **Ja** in het veld **Eindige capaciteit**.
5. Voer `30` in het veld **Tijdlimiet beperkte capaciteit** in.
6. Vouw de sectie **Time fences in dagen** uit.
7. Selecteer **Ja** in het veld **Capaciteit**.
8. Voer in het veld **Time fence capaciteitsplanning (dagen)** een getal in. Voorbeeld: `60`  
9. Selecteer **Ja** in het veld **Berekende vertragingen**.
10. Voer in het veld **Time fence vertragingen berekenen (dagen)** een getal in. Voorbeeld: `60` 
11. Vouw de sectie **Berekende vertragingen** uit.
12. Selecteer **Ja** in alle velden van **De berekende vertraging optellen bij de behoeftedatum**.
13. Sluit de pagina.

## <a name="create-a-constrained-plan"></a>Plan met beperkingen maken
1. Selecteer **Uitvoeren**.
2. Typ of selecteer in het veld **Hoofdplan** het plan waarvoor u beperkingen hebt ingesteld.  
3. Selecteer **OK**.
4. Selecteer **Geplande orders**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]