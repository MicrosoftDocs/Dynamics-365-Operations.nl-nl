---
title: De kwaliteit van goederen inspecteren
description: In dit onderwerp wordt uitgelegd hoe u een kwaliteitsorder verwerkt.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855681"
---
# <a name="inspect-the-quality-of-goods"></a>De kwaliteit van goederen inspecteren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u een kwaliteitsorder verwerkt. U kunt deze handleiding uitvoeren in het demobedrijf USMF. Voordat u deze voorbeeldprocedure start, moet u aankooporder "000016" bevestigen en een productontvangst boeken. Hiermee wordt automatisch een kwaliteitsorder gemaakt. Kwaliteitscontroles worden gewoonlijk uitgevoerd door een kwaliteitsmedewerker.


## <a name="select-a-quality-order"></a>Een kwaliteitsorder selecteren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Periodieke taken > Kwaliteitsbeheer > Kwaliteitsorders**.
2. Selecteer de kwaliteitsorder die is gemaakt voordat u deze procedure hebt gestart.  

## <a name="record-test-results"></a>Testresultaten vastleggen
1. Selecteer **Resultaten**.
2. Selecteer **Bewerken**.
3. Voer in het veld **Resultaathoeveelheid** een getal in.
4. Selecteer in het veld **Resultaat** de gewenste record in het vervolgkeuzemenu.  
- In dit voorbeeld is het resultaat gebaseerd op een vooraf gedefinieerd resultaat. Normaliter registreert u een specifieker testresultaat, bijvoorbeeld een formaat of andere dimensie.  
5. Selecteer **Opslaan**.
6. Sluit de pagina.

## <a name="validate-the-quality-order"></a>De kwaliteitsorder valideren
1. Selecteer **Valideren**.
2. Selecteer in het veld **Gevalideerd door** de gebruiker die de inspectie uitvoert in het vervolgkeuzemenu.  
3. Klik op **Selecteren**.
4. Selecteer **OK**.
5. Sluit de pagina.

