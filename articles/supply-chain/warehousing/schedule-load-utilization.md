---
title: Gebruikte capaciteit plannen
description: In dit onderwerp wordt uitgelegd hoe u de lading voor een magazijn kunt instellen en plannen.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425234"
---
# <a name="schedule-load-utilization"></a>Gebruikte capaciteit plannen

[!include[banner](../includes/banner.md)]

U kunt de gebruikte capaciteit voor geselecteerde locatietypen plannen en u kunt ook de huidige en toekomstige capaciteit voorspellen. U kunt de lading voorspellen voor een of meerdere locaties, voor de ladingseenheden (zone of magazijn) of een combinatie van een zone en een magazijn.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>De belasting voor een magazijn of site plannen en bekijken

Om de belasting voor sites, magazijnen of zones te plannen, maakt u een ruimteverbruiksinstelling en koppelt u deze aan een hoofdplan.

In de ruimtegebruiksinstellingen gebruikt u locatietypen, zoals **Bulklocatie** en **Orderverzamellocatie**, om op te geven hoe ruimtegebruik moet worden voorspeld. U kunt ook een opslagladingmodus opgeven, zoals **Zone**.

De projectie van toekomstig ruimteverbruik is gebaseerd op informatie die is berekend in het gekoppelde hoofdplan. De hoofdpannen voorspellen de resourceplanning voor inkomende en uitgaande orders voor productie en bewerkingen. De projectie van beschikbare ruimte is gebaseerd op de relatie tussen de ruimteverbruikinstelling en het geselecteerde hoofdplan.

Door de opslagladingmodus te gebruiken die u hebt geselecteerd in de ruimtegebruiksinstellingen, kunt u opgeven of de lading moet worden voorspeld voor elk magazijn of elke zone en of dat voorspellingen informatie moeten bevatten over zowel magazijnen als zones. U kunt tevens opgeven of geblokkeerde locaties moeten worden uitgesloten van de berekening van gebruikte capaciteit.

U kunt het ruimtegebruik voorspellen door het rapport **Gebruikte capaciteit magazijn** te genereren. Wanneer u dit rapport genereert, kunt u opgeven of de gebruikte capaciteit moet worden voorspeld voor elke locatie, voor verschillende locaties of voor de geselecteerde ladingeenheid, zoals een zone of een magazijn.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Ruimteverbruikinstelling voor een magazijn maken

1. Selecteer **Voorraadbeheer** \> **Instellen** \> **Magazijnbewaking** \> **Ruimtegebruik**.
2. Selecteer **Nieuw** om een ruimtegebruiksinstelling te maken. Geef een ID en een naam voor de nieuwe instelling op.
3. Geef in het veld **Opslagmodus lading** aan of het overzicht van het ruimtegebruik informatie moet geven op magazijn, zone of magazijn en zone.
4. Stel de optie **Geblokkeerde locaties uitsluiten** in op **Ja** om geblokkeerde voorraadlocaties uit te sluiten van de berekening van beschikbare ruimte. U kunt een voorraadlocatie voor invoer en uitvoer blokkeren door een blokkeringsreden voor de locatie op te geven in het veld **Invoer geblokkeerd** of **Uitvoer geblokkeerd** op het sneltabblad **Overig** op de pagina **Voorraadlocaties**.
5. Selecteer op het sneltabblad **Locatietype** de locatietypen die in de berekening van het ruimtegebruik moeten worden meegenomen. U moet ten minste één locatietype voor de projectie selecteren.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Een ruimteverbruikinstelling koppelen aan een hoofdplan

1. Selecteer **Voorraadbeheer** \> **Periodieke taken** \> **Gebruikte capaciteit plannen**.
2. Selecteer een hoofdplan in het veld **Hoofdplan**.
3. Geef in het veld **Aantal dagen** het aantal dagen op dat moet worden opgenomen in de voorspelling van huidige en toekomstige werkbelastingen.
4. Selecteer in het veld **Ruimtegebruik** de ruimtegebruiksinstelling voor gebruik bij de voorspelling van huidige en toekomstige werkbelastingen.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>De belastingsverbruikprojectie opgeven en informatie bekijken

1. Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Fysieke-voorraadrapporten** \> **Gebruikte capaciteit magazijn**.
2. Selecteer in het veld **Weergeven op** het niveau van de ruimtegebruiksvoorspelling:

    - **Locatie**: voorspel het ruimtegebruik voor elke locatie. Deze projectie is handig als u bijvoorbeeld de magazijnen voor een site wilt weergevenm zodat u kunt het ruimteverbruik tussen de magazijnen kunt verdelen.
    - **Ladingeenheid**: voorspel het ruimtegebruik voor zones of magazijnen. De beschikbare ruimte wordt vervolgens voorspeld volgens de waarde die u hebt geselecteerd in het veld **Opslagmodus lading** op de pagina **Ruimtegebruik** bij het maken van de instellingen voor ruimtegebruik.

3. Voer een van de volgende stappen uit, afhankelijk van de waarde die u hebt geselecteerd in de vorige stap:

    - Als u **Locatie** in het veld **Weergeven op** hebt geselecteerd, is het veld **Locatie** beschikbaar. Selecteer een of meer locaties die u in de voorspelling wilt meenemen.
    - Als u **Ladingeenheid** in het veld **Weergeven op** hebt geselecteerd, is het veld **Ladingeenheid** beschikbaar. Selecteer de ladingeenheid.

4. Selecteer in het veld **Type lading** **Volume** of **Gewicht** om de operationele eenheid van het magazijn op te geven waarvoor ruimte moet worden voorspeld.
5. Selecteer in het veld **Instellingen ruimtegebruik** de ruimtegebruiksinstelling waarop de voorspelling moet worden gebaseerd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]