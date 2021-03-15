---
title: Indextarieven instellen
description: In dit onderwerp wordt uitgelegd hoe u indextarieven instelt. Indextarieven zijn vereist als uw organisatie leasebetalingsbedragen met een set indextarieven koppelt.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f362bf4a6b5de3ce16330aea08880b07b4145792
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992859"
---
# <a name="set-up-index-rates"></a>Indextarieven instellen

[!include [banner](../includes/banner.md)]

Als leasebetalingen afhankelijk zijn van een index, kunnen de typen indextarieven worden toegevoegd en bijgehouden in het systeem. Voor het herwaarderen van de leasebetalingen vanuit de pagina **Type indextarief**, gebruikt het herwaarderingsproces het meest recente indextarief van de herwaarderingsdatum.

Volg deze stappen om typen indextarieven en indextarieven toe te voegen.

1. Ga naar **Activa leasen \> Instellingen \> Type indextarief**.
2. Selecteer **Nieuw**.
3. Voer in de betreffende velden het tarieftype en de naam van het indextarief in.
4. Selecteer het type indextarief en selecteer **Toevoegen** om een nieuwe waarde voor indextarief toe te voegen.
5. Selecteer de effectieve begindatum van het tarief en selecteer de waarde van het tarief.

U moet **Waardeverschil indextarief** of **Waarde indextarief** selecteren als de indextariefmethode.

- Selecteer de methode **Waardeverschil indextarief** om een nieuwe leasebetaling te berekenen op basis van het verschil tussen het indextarief op de begin datum en het meest recente indextarief. Het indextarief wordt gedefinieerd in het veld **Indextarief (%)**.
- Selecteer de methode **Waarde indextarief** om de leasebetaling te berekenen met behulp van het percentage dat is opgegeven in het veld **Indextarief (%)**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]