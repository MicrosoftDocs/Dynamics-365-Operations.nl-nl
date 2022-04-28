---
title: Btw-codes instellen
description: In dit onderwerp wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 Finance.
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
ms.openlocfilehash: 69e2cf9a16fe0e694154cccf9b49944b49c79b90
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565848"
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
