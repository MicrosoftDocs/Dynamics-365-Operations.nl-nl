---
title: Toeslagcodes maken
description: In dit artikel wordt uitgelegd hoe u toeslagcodes configureert voor Leveranciers en Klanten.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65952cb989672e4eac2dd6101ee9c7c9424daed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866078"
---
# <a name="create-charges-codes"></a>Toeslagcodes maken

In dit artikel wordt uitgelegd hoe u toeslagcodes configureert voor Leveranciers en Klanten. Als uw organisatie vereist dat verkoop- of inkoopbedragen worden bijgehouden naast regelartikelen op een verkoop- of inkooporder, kunt u hiervoor toeslagcodes gebruiken. Zo betaalt u bijvoorbeeld vrachtkosten en verzekering op een inkooporder, en komen deze bedragen afzonderlijk voor op de inkooporder. In dit geval kunt u opgeven of de bedragen worden geboekt naar kostenrekeningen of toegevoegd aan de kosten van de artikelen.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Toeslagcodes instellen voor Klanten

Als u toeslagcodes wilt maken voor Klanten, gaat u als volgt te werk.

1. Ga naar **Klanten** &gt; **Instelling van toeslagen** &gt; **Toeslagcode**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Toeslagcode** een code voor de toeslag in.
3. Voer in het veld **Omschrijving** een omschrijving voor de toeslag in.
4. Optioneel: selecteer in het veld **Btw-groep voor artikel** een btw-groep.
5. Geef op het sneltabblad **Boeking** op hoe de toeslag automatisch moet worden gedebiteerd en gecrediteerd.
6. Als u **Grootboekrekening** selecteerde als het debet-/credittype, moet u een boekingstype opgeven in de velden **Boeking** en de hoofdrekening opgeven in de velden **Rekening**.

### <a name="example"></a>Voorbeeld

Uw klant betaalt de toeslag. Daarom wordt deze toegevoegd aan de totalen van de verkooporder. U stelt de volgende boekingsinformatie in:

- Selecteer in het veld **Type** in de sectie **Debet** de optie **Klant/leverancier** de factuurtoeslag toe te voegen aan de klantenrekening.
- Selecteer **Grootboekrekening** in het veld **Type** in de sectie **Credit**. Selecteer vervolgens in het veld **Rekening** de hoofdrekening voor inkomsten uit factuurtoeslagen.

> [!NOTE]
> U kunt een andere valuta gebruiken voor de toeslagtransactie, als het debettype of credittype voor de geselecteerde toeslagcode is ingesteld op **Grootboekrekening** of **Artikel**.

U kunt de tekst van de toeslagen afdrukken in de taal van de klant. Klik op **Vertalingen** om tekst op te geven voor de toeslagcodes in andere talen.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Toeslagcodes instellen voor Leveranciers

Als u toeslagcodes wilt maken voor Leveranciers, gaat u als volgt te werk.

1. Volg één van deze stappen:

    - Ga naar **Klanten** &gt; **Instelling** van **toeslagen** &gt; **Toeslagcode**.
    - Ga naar **Inkoop en sourcing** &gt; **Instellingen** &gt; **Toeslagen** &gt; **Toeslagcode**.

2. Selecteer **Nieuw**.
3. Voer in het veld **Toeslagcode** een code voor de toeslag in.
3. Voer in het veld **Omschrijving** een omschrijving voor de toeslag in.
4. Optioneel: selecteer in het veld **Btw-groep voor artikel** een btw-groep.
5. Optioneel: voer in het veld **Maximumbedrag** het maximumbedrag in dat is toegestaan voor de toeslagcode.

    Dit veld wordt gebruikt voor het valideren van toeslagen voor leveranciersfacturen. Schakel het selectievakje **Factuurmatching validatie inschakelen** in op het tabblad **Factuurvalidatie** van de pagina **Parameters van module Leveranciers** om de validatie van toeslagen in te schakelen.

    > [!IMPORTANT]
    > Om toeslagen voor facturen te valideren, moet u ook een exemplaar van een beleidsregeltype maken dat is gebaseerd op toeslagen voor het specifieke leveranciersfactuurbeleid.

6. Geef op het sneltabblad **Boeking** op hoe de toeslag automatisch moet worden gedebiteerd en gecrediteerd.
7. Als u **Grootboekrekening** selecteerde als het debet-/credittype, moet u een boekingstype opgeven in de velden **Debetboeking** en **Creditboeking** en de hoofdrekening opgeven in de velden **Debetrekening** en **Creditrekening**.
8. Schakel het selectievakje **Inkooporder en factuurwaarden vergelijken** in als u de toeslagen voor een factuur waarop de toeslagen in de desbetreffende inkooporderkop of op de desbetreffende inkooporderregels staan, met elkaar wilt laten vergelijken.

### <a name="example"></a>Voorbeeld

U kunt de toeslag registreren als een kost die deel uit maakt van het totaal van de inkooporder of leveranciersfactuur. Ga als volgt te werk om de boekingsgegevens in te stellen. 

- Selecteer in het veld **Type** in de sectie **Credit** de optie **Klant/leverancier** de factuurtoeslag toe te voegen aan de leveranciersrekening.
- Selecteer **Grootboekrekening** in het veld **Type** in de sectie **Debet**. Selecteer vervolgens in het veld **Rekening** de hoofdrekening voor de kosten uit factuurtoeslagen.

Volg deze stappen om boekingsgegevens zo in te stellen dat de eenheidskosten bij de artikelkosten worden opgeteld.

- Selecteer in het veld **Type** in de sectie **Credit** de optie **Klant/leverancier** de factuurtoeslag toe te voegen aan de leveranciersrekening.
- Selecteer in het veld **Type** in de sectie **Debet** , de optie **Artikel** om de toeslag toe te voegen aan de artikelkostprijs.

> [!NOTE]
> Mogelijk wilt u een andere valuta gebruiken dan de valuta die is opgegeven op de inkooporder of factuur. U kunt een andere valuta invoeren als het debet- of credittype voor de geselecteerde toeslagencode is ingesteld op **Grootboekrekening** of **Artikel**.

U kunt de tekst van de toeslagen afdrukken in de taal van de klant. Klik op **Vertalingen** om tekst op te geven voor de toeslagcodes in andere talen.
