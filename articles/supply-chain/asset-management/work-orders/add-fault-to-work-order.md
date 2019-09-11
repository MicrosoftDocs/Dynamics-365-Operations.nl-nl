---
title: Fout aan werkorder toevoegen
description: In dit onderwerp wordt beschreven hoe u foutregistraties toevoegt aan werkorders in Activabeheer.
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875593"
---
# <a name="add-fault-to-work-order"></a>Fout aan werkorder toevoegen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Aan een werkorder kunt u fouten toevoegen die in de foutontwerper zijn ingesteld. Het activum dat is geselecteerd in de werkorder moet activumtypen bevatten waaraan een of meer foutrecords zijn gekoppeld. In de sectie [Foutbeheer](../setup-for-work-orders/fault-management.md) vindt u meer informatie over de instellingen.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer in de lijst de werkorder waarvoor u een foutregistratie wilt maken en klik op **Fout in activum**.

3. Klik op het sneltabblad **Symptomen** op **Regel toevoegen**. In het veld **Fout** wordt automatisch een volgnummer voor de fout ingevoegd.

4. Selecteer het betreffende symptoom in het veld **Foutsymptoom**.

5. Selecteer **Foutgebied** en **Fouttype**.

6. Het veld **Foutdatum** wordt automatisch ingesteld op de huidige datum. Selecteer een andere datum, indien nodig.

7. Voeg op het sneltabblad **Oorzaken voor geselecteerd symptoom** een regel toe waarin de oorzaak van het probleem wordt beschreven.

8. Voeg op het sneltabblad **Oplossingen voor geselecteerd symptoom** een regel toe waarin een mogelijke oplossing voor het probleem wordt beschreven.

9. Klik op **Opslaan**.

![Figuur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Activafouten weergeven

In de lijst **Activafouten** kunt u een overzicht weergeven van alle fouten die zijn geregistreerd voor activa.

Klik op **Activabeheer** > **Query's** > **Activafout** > **Activafouten** om de lijst te openen.


## <a name="print-asset-fault-report"></a>Rapport met activafouten afdrukken

Via de lijstpagina **Alle activa** kunt u een rapport met activafouten afdrukken waarin alle foutregistraties en een grafisch overzicht van foutstatistieken worden weergegeven.

1. Klik op **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.

2. Selecteer in de lijst **Activa** het activum waarvoor u een foutrapport wilt afdrukken.

3. Klik op het tabblad **Algemeen** in de sectie **Rapporten** op **Fout in activum**.

4. Voeg een specifieke periode in of selecteer een fouttype.

5. Klik op **OK** om het rapport af te drukken.

>[!NOTE]
>U kunt ook een foutrapport voor verschillende activa of activatypen afdrukken door te klikken op **Activabeheer** > **Rapporten** > **Activa** > **Fout in activum**.

