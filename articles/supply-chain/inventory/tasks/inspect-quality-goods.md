---
title: De kwaliteit van goederen inspecteren
description: In dit artikel wordt beschreven hoe u kwaliteitsorders verwerkt.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219029"
---
# <a name="inspect-the-quality-of-goods"></a>De kwaliteit van goederen inspecteren

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u kwaliteitsorders verwerkt. Kwaliteitscontroles worden gewoonlijk uitgevoerd door een kwaliteitsmedewerker.

Als de standaard [demogegevens](../../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd, kunt u deze gebruiken om de procedures in dit artikel uit te voeren. Om de demogegevens te gebruiken, selecteert u de rechtspersoon *USMF* voordat u begint. Vervolgens moet u inkooporder *000016* bevestigen en een productontvangstbon boeken. Een kwaliteitsorder wordt automatisch gegenereerd.

## <a name="step-1-select-a-quality-order"></a>Stap 1: Een kwaliteitsorder selecteren

Volg deze stappen om een kwaliteitsorder te selecteren.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Selecteer de kwaliteitsorder die is gegenereerd voordat u deze procedure startte.

## <a name="step-2-record-test-results"></a>Stap 2: Testresultaten vastleggen

Volg deze stappen om testresultaten te registreren.

1. Selecteer **Resultaten**.
1. Selecteer **Bewerken**.
1. Voer in het veld **Resultaathoeveelheid** een getal in.
1. Selecteer de gewenste record in het veld **Resultaat**. In dit voorbeeld is het resultaat gebaseerd op een vooraf gedefinieerd resultaat. Normaliter registreert u een specifieker testresultaat, bijvoorbeeld een afmeting of andere dimensie.
1. Selecteer **Opslaan**.
1. Sluit de pagina.

## <a name="step-3-validate-the-quality-order"></a>Stap 3: De kwaliteitsorder valideren

Volg deze stappen om de kwaliteitsorder te valideren.

1. Selecteer **Valideren**.
1. Selecteer in het veld **Gevalideerd door** de gebruiker die de inspectie uitvoert.
1. Selecteer **Selecteren**.
1. Selecteer **OK**.
1. Sluit de pagina.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
