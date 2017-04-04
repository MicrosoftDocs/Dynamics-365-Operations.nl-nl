---
title: SEPA-mandaat instellen voor automatische afschrijving
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA-mandaat instellen voor automatische afschrijving



Een automatische SEPA-overschrijving maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend. De klant tekent een mandaat dat de crediteur autoriseert om een betaling te innen en dat de bank van de klant opdraagt om de inning te betalen. In dit onderwerp is opgezet om weer te geven van het proces voor het instellen van SEPA automatische incasso mandaten.

## <a name="prerequisites"></a>Vereisten
De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

| Categorie       | Vereiste                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/regio | Het primaire adres van de rechtspersoon moet zich in de volgende landen/regio's bevinden: Oostenrijk, België, Duitsland, Spanje, Frankrijk, Italië of Nederland. |

1. Een nummerreeks voor automatische incasso opdracht, voor dat elke automatische afschrijving mandaat beschikt over een uniek nummer instellen. Gebruik het formulier **Nummerreeksen** om een nummerreeks voor automatische overschrijvingsmandaten te maken. U wilt deze identificatie gebruiken om de nummerreeks op het automatische overschrijvingsdebetmandaatsysteem op de pagina **Parameters van module Klanten** toe te wijzen.

2. Instellen van klantparameters voor automatische incasso mandaten gebruik de **parameters van module klanten** pagina kunt u parameters voor automatische incasso mandaten instellen. Instellen van de parameters op de **automatische incasso** en wijzig de standaardparameters als nodig is. Klik vervolgens op de **nummerreeksen** tabblad, werkt de **ID automatische afschrijving mandaat** bij de nummerreeks die u eerder hebt ingesteld.

3. Een betalingsmethode instellen voor automatische incasso u bepaalt een betalingsmethode voor automatische incasso mandaten moet instellen. U gebruikt deze betalingsmethode om facturen op te vragen om automatische afschrijvingen voor te genereren. Gebruik de pagina **Betalingsmethoden** om de betalingsmethode in te stellen. Als u een betalingsmethode voor mandaten voor automatische afschrijving wilt instellen, moet u deze extra stappen voor een betalingsmethode uitvoeren:

-   Selecteer **Elektronische betaling** in het veld **Betalingstype**.
-   Optioneel: Als u verwacht dat elk van uw klanten meerdere bepaalt, in de **periode** veld **factuur**. Een aparte betaling gemaakt voor elke factuur en elke betaling het mandaat zoals die is opgegeven voor de factuur wordt gebruikt.
-   Selecteer de optie **Mandaat vereisen** om betalingen te maken door mandaten voor automatische afschrijving te gebruiken. De optie **Mandaat vereisen** is alleen beschikbaar als u **Elektronische betaling** in het veld **Betalingstype** selecteert.

Zie ook [automatische incasso-overzicht](sepa-direct-debit-overview.md) 

