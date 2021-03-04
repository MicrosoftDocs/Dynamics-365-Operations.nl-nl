---
title: Geboekte leasetransacties terugboeken
description: In dit onderwerp wordt uitgelegd hoe u een geboekte leasetransactie terugboekt. Transacties die via Activa leasen zijn gemaakt, kunnen worden teruggeboekt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442163"
---
# <a name="reverse-posted-lease-transactions"></a>Geboekte leasetransacties terugboeken

[!include [banner](../includes/banner.md)]

Transacties die via Activa leasen zijn gemaakt, kunnen worden teruggeboekt. Transacties die via Activa leasen worden teruggeboekt, werken uw leasedata bij. Daarom worden ook de boekwaarden van de leaseverplichtingen en het RoU-activum bijgewerkt.

Voer de volgende stappen uit om een transactie voor een lease terug te boeken.

1. Selecteer de transactie op de pagina **Activumtransactie** of de pagina **Transacties verplichtingen** en selecteer vervolgens **Transactie terugboeken**.
2. In het dialoogvenster dat wordt weergegeven, kunt u de datum bewerken waarop de terugboekpost wordt geboekt. Het veld **Datum** wordt standaard ingesteld op de transactieboekingsdatum van de transactie die u hebt geselecteerd. De terugboekpost kan niet eerder worden geboekt dan de oorspronkelijke boekingsdatum van de geselecteerde transactie.
3. Selecteer **OK**. Een journaalboeking wordt geboekt waarmee de geselecteerde boeking wordt teruggeboekt. De terugboeking wordt weergegeven op de pagina **Activatransacties** of **Transacties verplichtingen** en het nettototaal van het huidige saldo dat op de pagina wordt weergegeven, wordt bijgewerkt.

Wanneer u **Terugboeking traceren** selecteert, wordt er een dialoogvenster weergegeven waarin zowel de oorspronkelijke transacties als de teruggeboekte transacties worden weergegeven, samen met een gekoppeld nummer dat een *Traceernummer* wordt genoemd. Als u de terugboekingen begrijpelijker wilt maken en de zichtbaarheid wilt verbeteren, kunt u terugboekingen ook volgen met behulp van de leaseschema's.

In het veld **Laatste journaalnummer** op de pagina **Schema** worden de journaalnummers van transacties weergegeven. Wanneer een transactie wordt teruggeboekt, wordt dit veld bijgewerkt met het journaalnummer van een terugboekingstransactie. Bovendien is het selectievakje **Teruggeboekt** ingeschakeld om aan te geven dat de transactie is teruggeboekt en het vled **Geboekt** is geselecteerd.

## <a name="revoke-a-reversed-transaction"></a>Een teruggeboekte transactie intrekken

Voer de volgende stappen uit om een teruggeboekte transactie in te trekken.

1. Op de pagina **Schema** of de pagina **Transacties** selecteert u de oorspronkelijke transactie.
2. Volg één van deze stappen:

    - Als u de transactie op de pagina **Schema** hebt geselecteerd, volgt u de stappen voor het maken van een journaal in [Maandelijkse journaalposten maken in een batch](create-monthly-journals-batch.md). U moet het journaal handmatig boeken.
    - Als u de transactie op de pagina **Transacties** hebt geselecteerd, selecteert u **Transactie terugboeken**. Er wordt een bericht weergegeven waarin wordt gemeld dat, door dit in te trekken, u een eerdere terugboeking intrekt, en dat u de boekingsdatum voor de intrekking kunt bewerken. Algemene bedrijfsvalidaties zijn echter van invloed op de data die in het veld **Datum** kunnen worden ingevoerd. 

3. Selecteer **OK**. Een journaalboeking wordt geboekt waarmee de geselecteerde boeking wordt teruggeboekt. De terugboeking wordt weergegeven op de pagina **Transacties** en het huidige netto totaalsaldo wordt hersteld naar de waarde vóór de eerste terugboeking. De invloed die de terugboeking op de saldi had, wordt hierdoor geannuleerd.

Wanneer u **Terugboeking traceren** selecteert, wordt er een dialoogvenster weergegeven waarin zowel de oorspronkelijke transacties als de teruggeboekte transacties worden weergegeven, samen met een gekoppeld traceernummer.

U kunt intrekkingen ook traceren met de betreffende pagina **Schema's**. Het veld **Terugboeken** is gewist, terwijl het veld **Journaal geboekt** is geselecteerd. Bovendien wordt het veld **Laatste journaalnummer** bijgewerkt met het journaalnummer van de intrekkingstransactie en wordt het veld **Journaalnummer** bijgewerkt met het terugboekingsjournaalnummer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]