---
title: Btw-codes instellen
description: In dit onderwerp wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834825"
---
# <a name="set-up-sales-tax-codes"></a>Btw-codes instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 for Finance and Operations. Btw-codes worden gemaakt voor elke indirecte belasting of heffing die de rechtspersoon moet doorberekenen, innen en afdragen aan belastingdiensten.

Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar **Navigatievenster > Belasting > Indirecte belastingen > Btw > Btw-codes**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Btw-code**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer een **Vereffeningsperiode** door de vervolgkeuzelijst te openen, om op te geven welke btw-dienst en met welke intervallen deze btw moet worden aangegeven en betaald.
6. Selecteer een **Grootboekboekingsgroep** om de hoofdrekeningen op te geven om btw naar het grootboek te boeken.
7. Vouw het sneltabblad **Berekening** uit. Het sneltabblad bevat meerdere velden die bepalen hoe de btw-bedragen worden berekend. Vul deze velden naar wens in.  
8. Selecteer in het **actievenster**, bovenaan de interface, de optie **Btw-code**.
9. Selecteer **Waarden**.
10. Voer de waarde voor deze btw-code in de kolom **Waarde** in.
    - Als op het sneltabblad **Berekening** Bedrag per eenheid is geselecteerd, wordt in het veld Oorsprong de waarde vermenigvuldigd met de hoeveelheid op de transactie om het btw-bedrag te berekenen.  Als de btw-code geen eenheidgebaseerde belasting is, is de waarde een percentage dat wordt toegepast op de oorsprong voor deze btw-code om het btw-bedrag te berekenen.     
11. Selecteer **Opslaan**.
12. Sluit de pagina.
13. Selecteer **Opslaan**.

