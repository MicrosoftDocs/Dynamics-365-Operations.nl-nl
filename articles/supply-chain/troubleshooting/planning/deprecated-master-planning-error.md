---
title: Er wordt een foutbericht weergegeven wanneer u de ingebouwde hoofdplanning-engine gebruikt
description: Wanneer u de afgeschafte, ingebouwde hoofdplanning-engine gebruikt, wordt een foutbericht weergegeven.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294048"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Er wordt een foutbericht weergegeven wanneer u de ingebouwde hoofdplanning-engine gebruikt

Foutcode: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Symptomen

Wanneer u voor de hoofdplanning de afgeschafte, ingebouwde hoofdplanning-engine gebruikt, wordt het volgende foutbericht weergegeven:

> Dit foutbericht wordt weergegeven omdat de ingebouwde engine voor hoofdplanning werd gebruikt voor scenario's die worden ondersteund door Planningsoptimalisatie. U moet nu migreren naar Planningsoptimalisatie, omdat de huidige ingebouwde hoofdplanning wordt afgeschaft. De uitvoering van deze hoofdplanning is succesvol voltooid. Als uw migratie sterke afhankelijkheden heeft van functies die in behandeling zijn, kan een uitzondering voor het gebruik van de ingebouwde hoofdplanningsengine worden aangevraagd. Vul de volgende vragenlijst in om aan de slag te gaan en, indien relevant, vraag een uitzondering aan van de migratie naar Planningsoptimalisatie. [Plannings- en uitzonderingsvragenlijst voor optimalisatie](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Oorzaak

Als u de planning uitvoert zonder productiebeheerfuncties te gebruiken, kunt u overwegen een migratie uit te voeren naar Planningsoptimalisatie. De ingebouwde hoofdplanning-engine wordt afgeschaft. Als u deze wilt blijven gebruiken zonder het foutbericht te ontvangen, moet u daarom een uitzondering aanvragen bij Microsoft.

## <a name="resolution"></a>Oplossing

Zie [Migratie naar Planningsoptimalisatie voor hoofdplanning](/dynamics365/supply-chain/master-planning/new-master-planning-engine) voor meer informatie over het migreren naar Planningsoptimalisatie of het toepassen van een uitzondering, zodat u in plaats te migreren de afgeschafte, ingebouwde planning-engine kunt blijven gebruiken.
