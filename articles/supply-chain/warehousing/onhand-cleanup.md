---
title: Taak voor het opruimen van voorhanden artikelen in magazijnbeheer
description: Dit onderwerp beschrijft de taak voor het opruimen van voorhanden artikelen, waardoor de systeemprestaties worden verbeterd door gerelateerde maar onnodige records te identificeren en te verwijderen.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 93c77434a912554dab486b42c0c9fffd68cf9435
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225998"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Taak voor het opruimen van voorhanden artikelen in magazijnbeheer

De prestaties van query's die worden gebruikt om de voorhanden voorraad te berekenen, worden beïnvloed door het aantal records in de desbetreffende tabellen. Een manier om de prestaties te verbeteren is om het aantal records te verminderen dat moet worden doorzocht.

Dit onderwerp beschrijft de taak voor het opruimen van voorhanden artikelen, waarmee overbodige records worden verwijderd uit de tabellen InventSum en WHSInventReserve. In deze tabellen wordt informatie over voorhanden artikelen opgeslagen voor artikelen die zijn ingeschakeld voor magazijnbeheerverwerking. (Deze artikelen worden ook wel WHS-artikelen genoemd.) Het verwijderen van deze records kan de prestaties van berekeningen van voorhanden voorraad aanzienlijk verbeteren.

## <a name="what-the-cleanup-job-does"></a>Wat de opruimtaak doet

Met de taak voor het opruimen van voorhanden artikelen worden alle records in de tabellen WHSInventReserve en InventSum verwijderd die als veldwaarden *0* (nul) hebben. Deze records kunnen worden verwijderd omdat ze niet bijdragen aan de informatie over voorhanden artikelen. De taak verwijdert alleen records die zich onder het niveau **Locatie** bevinden.

Als negatieve fysieke voorraad is toegestaan, kan de opruimtaak mogelijk niet alle relevante items verwijderen. De reden voor deze beperking is dat de taak een bijzonder scenario moet toestaan waarbij een nummerplaat meerdere serienummers heeft en een van dezeserie nummers negatief is geworden. Stel dat het systeem nul voorhanden voorraad op het niveau van de nummerplaat heeft wanneer een nummerplaat beschikt over + 1 st. van serienummer 1 en –1 st. van serienummer 2. Voor dit speciale scenario wordt geprobeerd eerst vanaf lagere niveaus te verwijderen.

## <a name="schedule-and-configure-the-cleanup-job"></a>De opruimtaak plannen en configureren

De taak voor het opruimen van voorhanden artikelen is beschikbaar op **Voorraadbeheer \> Periodieke taken \> opruimen \> Opruimen van voorhanden artikelen in magazijnbeheer**. Gebruik de standaardtaakinstellingen om het bereik en het schema voor het uitvoeren van de taak te bepalen. Daarnaast worden de volgende instellingen geboden:

- **Verwijderen indien niet bijgewerkt voor dit aantal dagen**: voer het minimum aantal dagen in dat moet worden gewacht voordat een voorhanden artikel wordt verwijderd waarvoor de hoeveelheid is gedaald naar nul. Met deze instelling kunt u het risico beperken dat voorhanden items worden verwijderd die nog worden gebruikt. Als u wilt dat het opruimen zo snel mogelijk wordt uitgevoerd, geeft u *0* (nul) op of laat u het veld leeg.
- **Maximale uitvoeringstijd (uren)**: voer de maximale uitvoeringstijd van de opruimingstaak in uren in. Als de taak niet is voltooid voordat deze tijd is verstreken, wordt het werk opgeslagen dat tot dusverre met de taak is uitgevoerd en vervolgens wordt de taak gesloten. Deze mogelijkheid is vooral relevant voor implementaties met een hoog voorraadgebruik. In deze gevallen moet u de taak zo plannen dat deze wordt uitgevoerd op momenten dat de systeembelasting zo licht mogelijk is. Als u wilt dat de batchtaak wordt uitgevoerd totdat deze is voltooid, geeft u *0* (nul) op of laat u het veld leeg. Deze instelling is alleen beschikbaar als de gerelateerde functie is [ingeschakeld in uw systeem](#max-execution-time).

Hoewel u de taak tijdens normale kantooruren kunt uitvoeren, raden we u aan om de taak buiten kantooruren uit te voeren. Op deze manier kunt u conflicten voorkomen die zich kunnen voordoen als een gebruiker met een record werkt die ook wordt opgeruimd.

Als de taak een record voor een artikel probeert te verwijderen terwijl die record door een andere gebruiker wordt gebruikt, treedt er een impasse op voor de opruimtaak of de gebruiker.

Wanneer de taak wordt uitgevoerd, heeft deze een toegewezen grootte van 100. Met andere woorden, er wordt geprobeerd één keer door te voeren voor elke 100 verwijderingen. Omdat sommige verwijderingen echter zijn gebaseerd op een set, kunnen er scenario's zijn waarin meer dan 100 records in dezelfde transactie kunnen worden verwijderd. Hierdoor kunnen er soms nog steeds vergendelingsescalaties optreden.

## <a name="possible-user-impact"></a>Mogelijke gevolgen voor de gebruiker

Gebruikers kunnen last hebben van het probleem als met de taak voor het opruimen van voorhanden artikelen alle records voor een bepaald niveau (zoals het nummerplaatniveau) worden verwijderd. In dit geval werkt de functionaliteit voor de observatie dat voorraad voorheen beschikbaar was op een nummerplaat mogelijk niet correct omdat de relevante voorhanden artikelen niet meer beschikbaar zijn. Dit kan bijvoorbeeld worden ervaren in de volgende situaties:

- In de **Voorhanden voorraad** wanneer de gebruiker de voorwaarde **Hoeveelheid \<\>0** deselecteert of de voorwaarde **Afgesloten transacties** selecteert in de instellingen **Weergave van dimensies**.
- In een **Fysieke voorraad per voorraaddimensie**-rapport voor perioden in het verleden wanneer de gebruiker de parameter **Begindatum** instelt.

De prestatieverbetering die de opschoningstaak oplevert moet deze kleine verliezen in functionaliteit echter goed maken.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>De instelling voor maximale uitvoeringstijd beschikbaar maken

De instelling **Maximale uitvoeringstijd** is standaard niet beschikbaar. Als u deze functie wilt gebruiken, moet u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de gerelateerde functie in uw systeem in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Maximale uitvoeringstijd voor de taak voor het opruimen van voorhanden artikelen in magazijnbeheer*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]