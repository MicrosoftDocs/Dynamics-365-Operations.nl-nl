---
title: Creditcardtransacties importeren en onderhouden
description: In dit onderwerp wordt uitgelegd hoe u onkostengerelateerde creditcardtransacties importeert en onderhoudt. Deze transacties kunt u zo instellen dat deze automatisch periodiek worden geïmporteerd of u kunt de transacties handmatig invoeren wanneer dit nodig is.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "322646"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Creditcardtransacties importeren en onderhouden

[!include [banner](../includes/banner.md)]

Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat deze automatisch periodiek worden geïmporteerd. De transacties kunnen zo nodig ook handmatig worden geïmporteerd. De creditcardtransacties worden geïmporteerd via de gegevensentiteit Creditcardtransacties.

Zie [Gegevensentiteiten](../../dev-itpro/data-entities/data-entities.md) voor meer informatie over gegevensentiteiten.

## <a name="import-credit-card-transactions"></a>Creditcardtransacties importeren

1. Op de pagina **Creditcardtransacties** selecteert u **Transacties importeren**. De eerste keer dat u gegevensbeheer opent, moet de lijst met gegevensentiteiten worden bijgewerkt voordat u kunt doorgaan.
2. Voer in het veld **Naam** een unieke beschrijving van de importtaak in.
3. Selecteer in het veld **Indeling van brongegevens** de indeling in van het bestand met de creditcardtransacties die u wilt importeren.
4. Selecteer **Uploaden** en zoek en selecteer het bestand dat u wilt importeren.
5. Als het bestand is geüpload, valideert u de toewijzing van het bestand met creditcardtransacties en de kolommen van de gegevensentiteit Creditcardtransacties door de koppeling **Kaart weergeven** op de tegel te selecteren. Als er toewijzingsfouten zijn of als u de toewijzing moet wijzigen, brengt u de wijzigingen aan via het tabblad **Visualisering van toewijzing** of **Gegevens toewijzen**.
6. Als u de creditcardtransacties wilt automatiseren, selecteert u **Terugkerende gegevenstaak maken**. Vervolgens stelt u het terugkeerpatroon in om te bepalen hoe vaak creditcardtransacties moeten worden geïmporteerd. Wanneer u klaar bent, selecteert u **OK**.
7. Als u het geselecteerde bestand nu wilt importeren, selecteert u **Importeren**.
8. Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens controleren om te zien welke fouten u moet corrigeren om een geslaagde import te kunnen garanderen.

> [!NOTE]
> Als u meerdere bestandsindelingen moet importeren, moet u voor elk type indeling aparte importtaken maken.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>De creditcardtransacties van vertrokken werknemers opnieuw toewijzen

Nadat een werknemerrecord is beëindigd, wordt de AD DS-account (Active Directory Domain Services) van die werknemer uitgeschakeld. Er kunnen echter nog actieve creditcardtransacties zijn die nog moeten worden opgevoerd en vergoed. Via de pagina **Creditcardtransacties** kunt u de werknemer voor een creditcardtransactie opnieuw toewijzen, als de oorspronkelijke werknemer niet meer bij het bedrijf werkt.

Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**. Vervolgens selecteert u een andere werknemer om de creditcardtransacties aan toe te wijzen. Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen deze voor een onkostennota worden geselecteerd en worden betaald via het normale proces voor terugbetaling van onkosten.
