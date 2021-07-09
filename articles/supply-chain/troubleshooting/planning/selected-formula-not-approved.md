---
title: Geselecteerd formulenummer is niet goedgekeurd voor een batchorder
description: Wanneer u een geplande order wilt fiatteren, wordt er een foutbericht weergegeven waarin staat dat het geselecteerde formulenummer niet is goedgekeurd voor een batchorder.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294043"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Geselecteerd formulenummer is niet goedgekeurd voor een batchorder

Foutcode: PRO2614

## <a name="symptoms"></a>Symptomen

Wanneer u een geplande order probeert te fiatteren, wordt het volgende foutbericht weergegeven:

> Het geselecteerde formulenummer is niet goedgekeurd voor een batchorder.

## <a name="cause"></a>Oorzaak

Het systeem valideert de goedkeuringsbewerking om ervoor te zorgen dat er een goedgekeurde formule beschikbaar is voor het actieve artikel. U moet de formule waarschijnlijk goedkeuren.

## <a name="resolution"></a>Oplossing

Voer de volgende stappen uit om een formule goed te keuren.

1. Ga naar **Productgegevensbeheer \> Stuklijsten en formules \> Formules**.
1. Selecteer de betreffende formule.
1. Selecteer in het actievenster op het tabblad **Formule** in de groep **Onderhouden** de optie **Formule goedkeuren**.
1. Selecteer een fiatteur in het dialoogvenster **Stuklijst of formule goedkeuren** en selecteer **OK**.
