---
title: De instelling Boeken op toeslagrekening in grootboek is niet ingeschakeld
description: Dit probleem doet zich voor wanneer een inkooporder wordt gefactureerd, als de optie Boeken op toeslagrekening in grootboek is ingeschakeld op het tabblad Factuur van de pagina Parameters van module Leveranciers.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476032"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>De instelling Boeken op toeslagrekening in grootboek is niet ingeschakeld

## <a name="symptoms"></a>Symptomen

Dit probleem doet zich voor wanneer een inkooporder wordt gefactureerd, als de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op het tabblad **Factuur** van de pagina **Parameters van module Leveranciers**.

## <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.
1. Stel op het tabblad **Factuur** de optie **Boeken op toeslagrekening in grootboek** in op *Ja*.
1. Ga naar **Voorraadbeheer \> Instellen \> Boeken \> Boeken**.
1. Controleer op het tabblad **Inkooporder** of u alle regels in de inkoopuitgave voor het product hebt verwijderd.
1. Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.
1. Inkooporder maken. Selecteer in het veld **Leveranciersrekening** de optie *1001 Acme Office Supplies*.
1. Voeg een inkooporderregel met de volgende instellingen toe:

    - **Artikelnummer:** *D0011 Laser Projector*
    - **Locatie:** *1*
    - **Magazijn:** *11*
    - **Hoeveelheid:** *4*

1. Selecteer in het actievenster op het tabblad **Inkoop** in de groep **Actie** de optie **Bevestigen**.
1. Selecteer in het Actievenster op het tabblad **Ontvangen** in de groep **Genereren** de optie **Productontvangstbon**.
1. Voer in het dialoogvenster **Productontvangstbon boeken** in het veld **Productontvangstbon** een willekeurig getal in en selecteer vervolgens **OK**.
1. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
1. Voer in het veld **Getal** een willekeurig getal in als het factuurnummer.
1. Werk de vereffeningsstatus bij en boek.
1. U ontvangt nu de volgende fout wanneer u een factuur genereert vanuit een inkooporder: 'Rekeningnummer voor inkoopuitgave van het transactietype bestaat niet'.

## <a name="resolution"></a>Oplossing

Dit is afhankelijk van de parameterinstellingen voor facturen en factuurgroepen. Zie het volgende blogbericht voor meer informatie: [Boekhouding voor inkooptoeslag en voorraadwijziging](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
