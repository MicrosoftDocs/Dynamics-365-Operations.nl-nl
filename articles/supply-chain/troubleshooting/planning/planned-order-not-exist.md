---
title: Tijdens bewerkingen op meerdere orders kan het systeem geen geplande order vinden.
description: Er treedt een fout op bij het uitvoeren van bewerkingen op meerdere geplande orders en er zijn ten minste twee orders die tot dezelfde artikel-id behoren.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920797"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Tijdens bewerkingen op meerdere orders kan het systeem geen geplande order vinden.

Foutcode: SYS24774

## <a name="symptoms"></a>Symptomen

Het volgende foutbericht wordt weergegeven wanneer u probeert een bewerking uit te voeren op meerdere geplande orders tegelijk, en ten minste twee orders horen bij dezelfde artikel-id. De fout kan bijvoorbeeld optreden wanneer de orders worden gefiatteerd of het ordertype wordt gewijzigd.

> Geplande order %1 bestaat niet.

## <a name="cause"></a>Oorzaak

Wanneer het systeem het type order wil fiatteren of wijzigen, moet het bestaande geplande orders voor het artikel opnieuw in overweging nemen om er zeker van te zijn dat het geplande aanbod overeenkomt met de vraag en het bestaande aanbod. Als onderdeel van dit proces maakt het systeem opnieuw geplande orders voor het artikel. Daarom bestaat de tweede geplande order die het systeem verwacht te verwerken niet meer.

## <a name="workaround"></a>Tijdelijke oplossing

Keur de orders goed voordat u ze verwerkt. Op deze manier worden de orders niet verwijderd wanneer de eerste order voor het artikel wordt verwerkt.
