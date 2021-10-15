---
title: De kwaliteit van goederen inspecteren
description: In dit onderwerp wordt beschreven hoe u kwaliteitsorders verwerkt.
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
ms.openlocfilehash: cc2fbbedb608b38c6855fbd48ff0c3e26ee3e0bc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575843"
---
# <a name="inspect-the-quality-of-goods"></a>De kwaliteit van goederen inspecteren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u kwaliteitsorders verwerkt. Kwaliteitscontroles worden gewoonlijk uitgevoerd door een kwaliteitsmedewerker.

Als de standaarddemogegevens zijn geïnstalleerd, kunt u deze gebruiken om de procedures in dit onderwerp uit te voeren. Om de demogegevens te gebruiken, selecteert u de rechtspersoon *USMF* voordat u begint. Vervolgens moet u inkooporder *000016* bevestigen en een productontvangstbon boeken. Een kwaliteitsorder wordt automatisch gegenereerd.

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
