---
title: Handmatig bijwerken van activatellers
description: Dit artikel beschrijft het handmatig bijwerken van activatellers in Activabeheer.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30c672286c16a4353556a507019960edb93f8b1b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016589"
---
# <a name="manual-update-of-asset-counters"></a>Handmatig bijwerken van activatellers

[!include [banner](../../includes/banner.md)]



Tellers worden gebruikt om registraties te maken voor een activum, zoals registraties over het aantal uren dat het activum in bewerking is geweest of de hoeveelheid die is geproduceerd.

Het tellertype dat voor een teller is geselecteerd, kan worden ingesteld op het overnemen van tellerwaarden. Met andere woorden, de optie **Waarden van activumteller overnemen** wordt ingesteld op **Ja** op het sneltabblad **Algemeen** van de pagina **Tellers** (**Activabeheer** > **Instellen** > **Typen activa** > **Tellers**). Wanneer u in dit geval een nieuwe tellerregel maakt van dat type, wordt elk onderliggend activum dat hetzelfde tellertype heeft, automatisch bijgewerkt.

Op de pagina **Alle activa** kunt u waarden van uren- of hoeveelheidstellers voor een activum registreren op basis van uw tellingen voor het activum.

1. Selecteer **Activabeheer** > **Activa** > **Alle activa**.

2. Selecteer het activum en selecteer vervolgens in het actievenster op het tabblad **Activa** in de groep **Preventief** de optie **Tellers**. Op de pagina **Activatellers** ziet u een lijst met alle eerdere tellerregistraties voor het geselecteerde activum.

3. Selecteer **Nieuw** om een nieuwe registratie te maken. De activum-id wordt automatisch in het veld **Activum** ingevoerd.

4. Selecteer de betreffende teller in het veld **Teller**. Alleen tellers die samenhangen met het geselecteerde activumtype in het activum zijn beschikbaar voor selectie. De gerelateerde eenheid wordt automatisch in het veld **Eenheid** ingevoerd.

5. Selecteer in het veld **Geregistreerd** de datum en tijd voor de registratie van de teller.

6. Voer in het veld **Waarde** het aantal sinds de registratie van het laatste item in. U kunt ook in het veld **Samengevoegde waarde** het aantal van de totale telling invoeren.

Let op de volgende punten:

- Als u fysiek een nieuwe teller voor een activum installeert, moet u de wijziging voor het activum registreren op de pagina **Activumtellers**. Vervolgens moet u twee registratieregels maken met identieke tijdstempels. De eerste regel moet de teller betreffen die u wilt vervangen. Schakel op de regel die bij de nieuwe teller hoort het selectievakje **Teller op nul zetten** in. In het veld **Totalen** is het totaal aantal tellingen de som van de tellertotalen van alle geregistreerde waarden voor dat tellertype.

- Als het selectievakje **Teller op nul zetten** voor een activum met behulp van een onderhoudsplan is ingeschakeld met het intervaltype 'Eenmaal vanaf…' of 'Eenmaal bereikt…', is de teller nog steeds actief op de nieuwe tellerregel omdat u een afzonderlijke tellerregel maakt en opnieuw begint met een nieuwe teller.

In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Activumtellers**.

![Figuur 1.](media/11-work-orders.png)

Op de pagina **Activumtellers** (**Activabeheer** > **Query's** > **Activa** > **Activatellers**) kunt u zo nodig tellerregistraties maken voor meerdere activa tegelijk.

>[!NOTE]
>U kunt een bereik instellen om afwijkingen in handmatige tellerregistraties te definiëren. U kunt ook het type bericht opgeven dat wordt weergegeven als registraties buiten het gedefinieerde bereik vallen. Zie [Tellers](../setup-for-objects/counters.md) voor meer informatie over het instellen van tellers.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]