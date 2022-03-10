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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712905"
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
