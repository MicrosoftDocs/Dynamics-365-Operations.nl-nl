---
title: Btw-codes instellen
description: In dit artikel wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 Finance.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b12133583f40cc17cb85f6dbd86697592af25caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858463"
---
# <a name="set-up-sales-tax-codes"></a>Btw-codes instellen

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u btw-codes instelt. Btw-codes worden gemaakt voor elke indirecte belasting of heffing die de rechtspersoon moet doorberekenen, innen en afdragen aan belastingdiensten.

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

    Als op het sneltabblad **Berekening** in het veld **Oorsprong** de optie **Bedrag per eenheid** is geselecteerd, wordt de waarde vermenigvuldigd met de hoeveelheid op de transactie om het btw-bedrag te berekenen.  Als de btw-code geen belasting is die op een eenheid is gebaseerd, is de waarde een percentage dat wordt toegepast op de oorsprong voor deze btw-code om het btw-bedrag te berekenen.     

11. Selecteer **Opslaan**.
12. Sluit de pagina.
13. Selecteer **Opslaan**.

Als u vanaf Microsoft Dynamics 365 Finance 10.0.22 de functie [Belastingservice](../../localizations/global-tax-calcuation-service-overview.md) gebruikt en [**Meerdere btw-registratienummers ondersteunen**](../../localizations/emea-multiple-vat-registration-numbers.md) is ingeschakeld in de werkruimte **Functiebeheer**, kunt u het veld **Type belasting** gebruiken om het type belastingcode op te geven. De volgende waarden zijn beschikbaar:

- Standaard-btw
- Gereduceerde btw
- Btw 0%
- Accijns
- Anders

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
