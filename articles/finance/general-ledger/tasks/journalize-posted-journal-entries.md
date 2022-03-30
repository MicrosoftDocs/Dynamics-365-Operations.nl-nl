---
title: Geboekte journaalposten journaliseren
description: Deze procedure laat zien hoe u geboekte journaalposten journaliseert.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400870"
---
# <a name="journalize-posted-journal-entries"></a>Geboekte journaalposten journaliseren

[!include [banner](../../includes/banner.md)]

Het journaliseerproces in het grootboek biedt een manier om geboekte boekstukgegevens voor uw grootboek te groeperen en rapporteren. Op basis van de door u verstrekt criteria, wordt een lijst met boekstukken gegenereerd met een unieke nummerreeks die de grootboekwaarde **Journaalnummer** als verwijzing heeft.

Volg deze stappen om geboekte journaalposten te journaliseren. Deze procedure gebruikt het demobedrijf **USMF**.

1. Ga naar **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**.
2. Selecteer een waarde in het veld **Uitgebreid grootboekjournaal**. Als u **Ja** selecteert, wordt andere rapportuitvoer aangemaakt.
3. Geef aan of de periode kan worden afgesloten als het journaalproces niet is uitgevoerd. Als u **Ja** selecteert, kan de periode niet worden gesloten tot het journaalproces voor die periode is voltooid.
4. Sluit de pagina.
5. Ga naar **Grootboek** \> **Periodieke taken** \> **Journaliseren** en selecteer **Filter**.
6. Selecteer de rij voor de filtercriteria die u wilt definiëren.
7. Typ of selecteer de filtercriteria in het veld **Criteria**.
8. Selecteer **OK** om de pagina te sluiten.
9. Selecteer **OK** om het journaalproces te starten. Een rapport wordt gegenereerd nadat het proces is voltooid.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
