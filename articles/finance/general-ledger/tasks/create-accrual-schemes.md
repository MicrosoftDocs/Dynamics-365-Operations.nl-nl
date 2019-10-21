---
title: Toerekeningsschema's maken
description: In dit onderwerp wordt uitgelegd hoe u een toerekeningsschema maakt.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f8cf8546187ae1c65d4966887e1c5842dff431
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175370"
---
# <a name="create-accrual-schemes"></a>Toerekeningsschema's maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u een toerekeningsschema maakt. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar **Navigatievenster > Modules > Grootboek > Journaalinstellingen > Toerekeningsschema's**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Toerekeningsidentificatie**.
4. Typ een waarde in het veld **Omschrijving van toenameschema**.
5. Geef in het veld **Debet** de gewenste waarden op. De opgegeven hoofdrekening zal de hoofddebetrekening op de journaalboekstukregel vervangen en zal ook worden gebruikt voor de omkering van de uitstelling op basis van de transitorische grootboekposten.  
6. Geef in het veld **Credit** de gewenste waarden op. De opgegeven hoofdrekening zal de hoofdcreditrekening op de journaalboekstukregel vervangen en zal ook worden gebruikt voor de omkering van de uitstelling op basis van de transitorische grootboekposten.  
7. Selecteer in het veld **Boekstuk** hoe u wilt dat het boekstuk wordt bepaald wanneer de transacties worden geboekt.
8. Typ in het veld **Beschrijving** een waarde om de transacties die zullen worden geboekt te beschrijven.
9. Selecteer in het veld **Periodefrequentie** hoe vaak de transacties moeten voorkomen.
10. Voer in het veld **Aantal voorvallen per periode** een getal in.
11. Selecteer in het veld **Transacties boeken** wanneer de transacties moeten worden geboekt, zoals **Maandelijks**.

