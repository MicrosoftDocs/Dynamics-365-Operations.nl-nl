---
title: Handmatig bijwerken van activatellers
description: Dit onderwerp beschrijft het handmatig bijwerken van activatellers in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875590"
---
# <a name="manual-update-of-asset-counters"></a>Handmatig bijwerken van activatellers

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Tellers worden gebruikt om registraties voor een activum te maken over bijvoorbeeld het aantal uren van bewerking of het aantal geproduceerde hoeveelheden.

Als het type dat voor een teller is geselecteerd, is ingesteld op het overnemen van tellerwaarden (**Activabeheer** > **Instellen** > **Activatypen** > **Tellers** > sneltabblad **Algemeen** > wisselknop **Waarden van activumteller overnemen** ingesteld op Ja), dan wordt elk onderliggend activum dat hetzelfde tellertype gebruikt, automatisch bijgewerkt wanneer u een nieuwe tellerregel van dat type maakt.

In **Alle activa** kunt u waarden van uren- of hoeveelheidstellers voor een activum registreren op basis van uw tellingen voor het activum.

1. Klik op **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.

2. Selecteer het activum in de lijst en klik op **Tellers**. In het formulier **Activatellers** ziet u een lijst met alle eerdere tellerregistraties voor het geselecteerde activum.

3. Klik op **Nieuw** om een nieuwe registratie te maken. De activum-id wordt automatisch ingevoegd.

4. Selecteer de betreffende teller in het veld **Teller**. Alleen tellers voor het geselecteerde activumtype in het activum zijn beschikbaar. De gerelateerde eenheid wordt automatisch in het veld **Eenheid** ingevoegd.

5. Selecteer de datum en tijd voor de registratie van de teller.

6. Voer in het veld **Waarde** de numerieke waarde na de laatste tellerregistratie in of voer in het veld **Samengevoegde waarde** de totale tellerwaarde in.

- Als u fysiek een nieuwe teller voor een activum installeert, moet u de wijziging voor het activum registreren in **Activumtellers**. Vervolgens moet u twee registratieregels met identieke tijdstempels maken. Op de regel voor de nieuwe teller schakelt u het selectievakje **Teller op nul zetten** in. Wanneer u de twee registratieregels maakt, moet de eerste regel de regel zijn voor de teller die u wilt vervangen. In het veld **Totalen** is het totaal aantal tellingen de som van het tellertotaal van alle geregistreerde waarden voor dat tellertype.  
- Als het selectievakje **Teller op nul zetten** voor een activum met behulp van een onderhoudsplan is ingeschakeld met het intervaltype 'Eenmaal vanaf…' of 'Eenmaal bereikt…', is de teller nog steeds actief op de nieuwe tellerregel omdat u een afzonderlijke tellerregel maakt en opnieuw begint met een nieuwe teller.

![Figuur 1](media/11-work-orders.png)


Als u tellerregistraties voor verschillende activa moet maken, kunt u dit doen in **Activabeheer** > **Query's** > **Activa** > **Activumtellers**.

>[!NOTE]
>U kunt een bereik instellen voor het definiëren van afwijkingen in handmatige registraties van tellers en het type bericht dat moet worden weergegeven als registraties buiten het gedefinieerde bereik vallen. Zie het onderwerp [Tellers](../setup-for-objects/counters.md) voor het instellen van tellers.
