---
title: Batchvrijgave van gedeeltelijk gereserveerde transferorders
description: In dit onderwerp wordt beschreven hoe u de batchvrijgave van gedeeltelijk gereserveerde transferorders vanaf een mobiel apparaat instelt en toepast.
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 3aa9b24c40efb053507b10a7a219857480e0b75e
ms.contentlocale: nl-nl
ms.lasthandoff: 12/14/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Batchvrijgave van gedeeltelijk gereserveerde transferorders

[!include[banner](../includes/banner.md)]

Met de functionaliteit voor batchvrijgave van gedeeltelijk gereserveerde transferorders kunt u transferorders met een batchtaak gedeeltelijk vrijgeven aan een magazijn.
Omdat u een gedeeltelijke hoeveelheid kunt vrijgeven, hoeft u niet te wachten tot de hele orderhoeveelheid in het magazijn beschikbaar is voordat u een order vrijgeeft.

De vrijgave van orders aan een magazijn is een geavanceerd magazijnbeheerproces. Dit proces omvat activiteiten, zoals orderverzamelen, verpakken en verzenden, die een magazijnmedewerker kan uitvoeren via een mobiel apparaat.

## <a name="where-it-applies"></a>Waar van toepassing

Voor deze functionaliteit worden transferorders met een batchtaak vrijgegeven aan een magazijn. Deze functie is handig wanneer u niet voldoende voorraad in het magazijn hebt, maar nog steeds artikelen van het ene naar het andere magazijn wilt overbrengen.

## <a name="how-it-is-set-up"></a>De instelling

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Uitvoeringscriteria opgeven voor transfer- en verkooporders

Voordat een order gedeeltelijk kan worden vrijgegeven aan een magazijn in een batch, moet aan de uitvoeringscriteria worden voldaan. Deze uitvoeringscriteria worden bepaald door het uitvoeringsbeleid.

Uitvoeringsbeleid voor transferorders en verkooporders wordt opgegeven op bedrijfsniveau. Afhankelijk van de instellingen van het uitvoeringsbeleid, wordt de vrijgave van orders in een batch goedgekeurd of afgekeurd. De orders worden vervolgens dienovereenkomstig verwerkt.

-   Als u uitvoeringsbeleid wilt maken voor transfer- en verkooporders, klikt u op **Magazijnbeheer** \> **Instellingen** \> **Vrijgave naar magazijn** \> **Uitvoeringsbeleid** en maakt u een uitvoeringsbeleid door een naam en een omschrijving in te voeren.

-   Als u een uitvoeringsverhouding, een waardetype en een bericht wilt opgeven dat moet worden weergegeven als het uitvoeringsbeleid wordt geschonden, klikt u op **Magazijnbeheer** \> **Instellingen** \> **Vrijgave naar magazijn** \> **Uitvoeringsbeleid** en stelt u de velden **Uitvoeringsverhouding**, **Waardetype** en **Berichten uitvoeringschending** in.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Het uitvoeringsbeleid opgeven voor transfer- en verkooporders

-   Als u het uitvoeringsbeleid voor transferorders wilt instellen, klikt u op **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** \> **Transferorders** \> **Magazijnbeheer** en selecteert u een uitvoeringsbeleid voor transferorders.

-   Als u het uitvoeringsbeleid voor verkooporders wilt instellen, klikt u op **Klanten** \> **Instellingen** \> **Parameters van module Klanten** \> **Magazijnbeheer** en selecteert u een uitvoeringsbeleid voor verkooporders.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Vrijgave in een batch toestaan en de hoeveelheid opgeven die in een batch moet worden vrijgegeven

Een batchtaak wordt gebruikt voor het vrijgeven van orders naar een magazijn in een batch. De parameters waarmee onderscheid wordt gemaakt tussen de orders die moeten worden uitgevoerd in een batchtaak, worden ingesteld voor de batchtaak zelf.

De parameter **Hoeveelheid** bepaalt of de gehele hoeveelheid of de fysiek gereserveerde hoeveelheid in de batch moet worden vrijgegeven. De parameter **Vrijgave van gedeeltelijk vrijgegeven orders toestaan** bepaalt of orders in de batch moeten worden geaccepteerd of afgewezen als ze eerder gedeeltelijk zijn vrijgegeven.

-   Als u de parameters **Hoeveelheid** en **Vrijgave van gedeeltelijk vrijgegeven orders toestaan** wilt instellen voor transferorders, klikt u op **Magazijnbeheer** \> **Vrijgave naar magazijn** \> **Transferorders automatisch vrijgeven**.

-   Als u de parameters **Hoeveelheid** en **Vrijgave van gedeeltelijk vrijgegeven orders toestaan** wilt instellen voor verkooporders, klikt u op **Magazijnbeheer** \> **Vrijgave naar magazijn** \> **Verkooporders automatisch vrijgeven**.

