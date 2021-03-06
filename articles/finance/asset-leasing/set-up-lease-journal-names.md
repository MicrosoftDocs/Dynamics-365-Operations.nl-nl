---
title: Leasejournaalnamen instellen
description: In dit onderwerp wordt uitgelegd hoe u leasejournaalnamen definieert. Leasejournaalnamen specificeren in welke journalen invoer vanuit Activa leasen wordt geboekt.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880881"
---
# <a name="set-up-lease-journal-names"></a>Leasejournaalnamen instellen

[!include [banner](../includes/banner.md)]

Leasejournaalnamen specificeren in welke journalen transacties van Activa leasen worden geboekt. Alleen journaalnamen die zijn toegewezen aan het journaaltype **Activa leasen** worden weergegeven in de velden **Initiële toerekening** en **Maandelijkse journaalnaam** op de pagina **Parameters voor activa leasen**. Alleen het journaaltype **Leveranciersfactuurregistratie** kan worden toegewezen aan het veld **Factuurjournaalnaam**.

Voer de volgende stappen uit om leasejournaalnamen te configureren.

1. Ga naar **Activa leasen \> Instellingen \> Parameters voor activa leasen**.
2. Ga op het tabblad **Algemeen** naar het veld **Journaalnaam initiële toerekening**, en selecteer een journaal. Alle journaalboekingen voor initiële toerekening worden naar deze journaalnaam geboekt.
3. Selecteer een journaal in het veld **Factuurjournaalnaam**. Als de optie **Betalen aan leverancier** is ingesteld op **Ja** voor het leaseboek, worden leasefacturen onkostenfacturen naar deze journaalnaam geboekt.
4. Selecteer een journaal in het veld **Leasejournaalnaam**. Alle afschrijvingsposten, renteposten en herindelingsposten op korte termijn worden naar deze journaalnaam geboekt. Als de optie **Betalen aan leverancier** is ingesteld op **Nee** voor het leaseboek, worden boekingen voor leasebetalingen en onkostenbetalingen ook naar deze journaalnaam geboekt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
