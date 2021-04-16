---
title: Schema voor onderhoudsplannen
description: In dit onderwerp wordt het plannen van onderhoudsplannen in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c19f999a94e6ad8451c208cf204d0b59306b77d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837796"
---
# <a name="schedule-maintenance-plans"></a>Schema voor onderhoudsplannen

[!include [banner](../../includes/banner.md)]

 

Door preventief onderhoud te plannen, worden kalenderitems voor activa gegenereerd op basis van de onderhoudsplannen die voor de activa zijn ingesteld. U kunt kalenderitems plannen op basis van geselecteerde onderhoudsplannen, activatypen en activa.

1. Klik op **Activabeheer** > **Periodiek** > **Preventief onderhoud** > **Onderhoudsplannen plannen**.

2. U kunt een tijdsinterval selecteren in de velden **Periode** en **Periodefrequentie**.

>[!NOTE]
>De velden **Periode** en **Periodefrequentie** geven aan hoe lang op voorhand u onderhoudsschemaregels wilt laten maken op basis van de onderhoudsplannen die u hebt gemaakt (op tijd gebaseerd of op basis van een teller). In onderstaande afbeelding worden onderhoudsschemaregels (= werkordervoorstellen) gemaakt op basis van de huidige datum en drie maanden.

3. Selecteer Ja op de wisselknop **Automatisch maken indien opgegeven op de regel** als werkorders automatisch moeten worden gemaakt volgens de regel van het onderhoudsplan.

>[!NOTE]
>Als deze wisselknop is ingesteld op Ja *en* het selectievakje **Automatisch maken** in **Onderhoudsplannen** ook is ingeschakeld op regels van onderhoudsplannen, worden werkorders gemaakt op basis van de regels in het onderhoudsplan en worden onderhoudsschemaregels met de status 'Werkorder gemaakt' ook gemaakt. Als er maar één optie is geselecteerd (**Automatisch maken indien opgegeven op de regel** in dit dialoogvenster of het selectievakje **Automatisch maken** in het formulier **Onderhoudsplannen**), worden alleen regels van onderhoudsplannen gemaakt die de status Gemaakt hebben. In dat geval worden er geen werkorders gemaakt.

4. Het is mogelijk om kalenderitems te genereren op basis van onderhoudsplannen (tijd of teller), activa, activatypen, functionele locaties en -locatietypen. Klik op de knop **Filter** en selecteer zo nodig uw opties.

- Wat de planning van onderhoudsplannen en functionele locaties betreft: als u de instellingen van activatypen, fabrikanten en modellen in onderhoudsplannen bijwerkt in **Alle functionele locaties** > **sneltabblad Onderhoudsplannen** nadat u onderhoudsplannen hebt gepland, worden bestaande onderhoudsplannen die betrekking hebben op die functionele locatie automatisch verwijderd. Als u nieuwe kalenderitems wilt maken die overeenkomen met de bijgewerkte instellingen voor onderhoudsplannen op de functionele locatie, moet u een nieuw schema voor onderhoudsplannen voor die functionele locatie uitvoeren. Lees meer over het instellen van activatypen, fabrikanten en modellen op functionele locaties in [Functionele locaties maken](../functional-locations/create-functional-locations.md).

>*Voorbeeld*: u wilt een onderhoudsplan voor een bepaalde functionele locatie maken. Dat betekent dat alle activa die op die functionele locatie zijn ingesteld op een bepaald moment worden opgenomen wanneer u het onderhoudsplan plant. In dat geval maakt u een onderhoudsplan en selecteert u de specifieke functionele locatie. U voegt echter GEEN objecten toe aan het onderhoudsplan. Het resultaat is dat wanneer u dat onderhoudsplan plant, de onderhoudsschemaregels worden gemaakt voor alle activa die op dat moment aan de functionele locatie zijn gekoppeld.

- Als u wijzigingen aanbrengt in activatypen, fabrikanten en modellen in **Activatypen**, worden deze wijzigingen alleen toegepast op nieuwe activa die het bijgewerkte activatype gebruiken. Meer informatie over het instellen van activatypen vindt u in [Activatypen](../setup-for-objects/object-types.md).  

5. Klik op **OK** om het genereren van onderhoudsschema-items voor activa te starten. De gegenereerde items worden weer op de lijstpagina **Hele onderhoudsschema**. In de volgende afbeelding ziet u een voorbeeld van de dialoog **Onderhoudsplanning**.

![Figuur 1](media/09-preventive-maintenance.png)

- In het dialoogvenster **Onderhoudsplannen plannen** kunt u batchtaken instellen op het sneltabblad **Op de achtergrond uitvoeren** als u kalenderitems automatisch met regelmatige intervallen wilt genereren.  
- Als u preventief onderhoud plant, worden onderhoudsschemaregels waarvan de verwachte begindatum en -tijd vóór de systeemdatum en -tijd ligt, niet gemaakt.  

In onderstaande afbeelding ziet u een grafische weergave van een onderhoudsplan op tijdbasis.  

![Figuur 2](media/10-preventive-maintenance.jpg)

Voor onderhoudsplannen op basis van een teller worden er twee verschillende tellerregistratiecycli weergegeven. Deze zijn gebaseerd op een onderhoudsplan dat is ingesteld voor activum 'V0001', waarbij het activum (een auto) naar verwachting maandelijks circa 2000 km rijdt.

In het eerste voorbeeld wordt de verwachte 2000 km niet elke maand bereikt. In het tellergebaseerd onderhoudsplan is de drempel 2000 km. Dus bij de planning van een onderhoudsplan zou er een onderhoudsschemaregel worden gemaakt telkens wanneer de drempel van 2000 kilometer wordt bereikt. In voorbeeld 1 zijn er vier registratieregels, maar de drempel van 2000 kilometer wordt slechts eenmaal bereikt. Dit betekent dat er maar één onderhoudsschemaregel wordt gemaakt wanneer u onderhoudsplannen voor dit activum plant, bijvoorbeeld voor een periode van drie maanden.

In de volgende afbeelding wordt er maandelijks 2000 km of meer geregistreerd. Er worden dus drie onderhoudsregels gemaakt als u onderhoudsplannen voor dit activum plant voor een periode van 3 maanden. 

De voorbeelden die hier worden beschreven, laten zien dat alle tellerregistraties voor een activum een trending slijtage voor het activum vertonen. Deze trend wordt gebruikt als rekenbasis op het moment van de planning van het onderhoudsplan.

![Figuur 3](media/11-preventive-maintenance.png)

![Figuur 4](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]