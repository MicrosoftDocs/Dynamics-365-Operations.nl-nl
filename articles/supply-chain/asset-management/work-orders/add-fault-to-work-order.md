---
title: Fout aan werkorder toevoegen
description: In dit artikel wordt beschreven hoe u foutregistraties toevoegt aan werkorders in Activabeheer.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7905dcd4c29872ec2601359baefa78545140397c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857890"
---
# <a name="add-fault-to-work-order"></a>Fout aan werkorder toevoegen

[!include [banner](../../includes/banner.md)]



Aan een werkorder kunt u fouten toevoegen die in de foutontwerper zijn ingesteld. Er moeten een of meer foutrecords worden gekoppeld aan de activumtypen die worden gebruikt voor het activum dat is geselecteerd in de werkorder. Zie [Foutbeheer](../setup-for-work-orders/fault-management.md) voor meer informatie over de instelling.

1. Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder waarvoor u een foutregistratie wilt maken en selecteer vervolgens in het actievenster op het tabblad **Werkorder** in de groep **Activum** de optie **Fout in activum**.

3. Selecteer op het sneltabblad **Symptomen** de optie **Regel toevoegen**. In het veld **Fout** wordt automatisch een volgnummer voor de fout ingevoerd.

4. Selecteer het relevante symptoom in het veld **Foutsymptoom**.

5. Selecteer in de velden **Foutgebied** en **Fouttype** de juiste waarden.

6. Het veld **Foutdatum** wordt automatisch ingesteld op de huidige datum. U kunt desgewenst een andere datum selecteren.

7. Voeg op het sneltabblad **Oorzaken voor geselecteerd symptoom** een regel toe waarin de oorzaak van het probleem wordt beschreven.

8. Voeg op het sneltabblad **Oplossingen voor geselecteerd symptoom** een regel toe waarin een mogelijke oplossing voor het probleem wordt beschreven.

9. Selecteer **Opslaan**.

In de onderstaande afbeelding ziet u een voorbeeld van een foutregistratie.

![Figuur 1.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Activafouten weergeven

In de lijst **Activafouten** kunt u een overzicht weergeven van alle fouten die zijn geregistreerd voor activa.

Op de lijstpagina **Activafouten** kunt u een overzicht weergeven van alle fouten die zijn geregistreerd voor activa. Open de pagina door **Activabeheer** > **Query's** > **Activafout** > **Activafouten** te selecteren.


## <a name="print-asset-fault-report"></a>Rapport met activafouten afdrukken

Via de lijstpagina **Alle activa** kunt u een rapport met activafouten afdrukken waarin alle foutregistraties en een grafisch overzicht van foutstatistieken worden weergegeven.

1. Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.

2. Selecteer het activum waarvoor u een foutrapport wilt afdrukken.

3. Selecteer in het actievenster op het tabblad **Algemeen** in de groep **Rapporten** de optie **Activumfout**.

4. Voer een specifieke periode in of selecteer een fouttype.

5. Selecteer **OK** om het rapport af te drukken.

>[!NOTE]
>U kunt een foutrapport voor verschillende activa of activatypen afdrukken door **Activabeheer** > **Rapporten** > **Activa** > **Fout in activum** te selecteren.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]