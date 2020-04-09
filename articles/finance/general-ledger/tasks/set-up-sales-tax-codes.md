---
title: Btw-codes instellen
description: In dit onderwerp wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 Finance.
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
ms.openlocfilehash: 26dc61e340afcf1ce99d37c43d5942dc8792b765
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144738"
---
# <a name="set-up-sales-tax-codes"></a>Btw-codes instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u btw-codes instelt. Btw-codes worden gemaakt voor elke indirecte belasting of heffing die de rechtspersoon moet doorberekenen, innen en afdragen aan belastingdiensten.

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

