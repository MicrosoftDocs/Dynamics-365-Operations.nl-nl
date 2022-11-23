---
title: Ouderdomsmomentopnamen voor klanten
description: Dit artikel bevat informatie over ouderdomsmomentopname voor klanten. Een ouderdomsmomentopname berekent saldi voor groep klanten op een bepaald tijdstip.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: e4ccc8ac9b5374ca0713167a17b8704727c687fd
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775231"
---
# <a name="customer-aging-snapshots"></a>Ouderdomsmomentopnamen voor klanten

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over ouderdomsmomentopname voor klanten. Een ouderdomsmomentopname berekent saldi voor groep klanten op een bepaald tijdstip. U kunt registraties voor ouderdomsmomentopnamen voor alle klanten of voor de klanten in een klantverzameling maken.

Informatie van ouderdomsmomentopnamen wordt weergegeven op de lijstpagina **Ouderdomssaldi** en op de pagina **Aanmaningen**. U moet een ouderdomsmomentopname maken voordat u de lijstpagina **Ouderdomssaldi** kunt gebruiken. De lijstpagina vermeldt uitsluitend informatie voor klanten voor wie een ouderdomsmomentopname is gemaakt.

De werkruimte **Klantcrediteringen en aanmaningen** toont ook de ouderdomsberekening voor de klant. Zie [Power BI-inhoud - klantcrediteringen- en aanmaningsbeheer](credit-collections-power-bi.md) voor meer informatie.

> [!NOTE]
> Als u de tijd wilt beperken die nodig is voor het maken van een ouderdomsmomentopname, moet u de volgende functies voor in de werkruimte **Functiebeheer** inschakelen: 
> - **Verbetering van rangschikking van klant naar ouderdom** 
> - **Prestatieverbetering van klanten naar ouderdom rangschikken met klantverzamelingen**  
>Als beide functies zijn ingeschakeld, kan **Klantverzamelingen** worden gebruikt bij het maken van de ouderdomsmomentopname. 

Wanneer u een ouderdomsmomentopname van klanten maakt, gebruikt u de volgende velden om informatie over de momentopname in te voeren:

- **Definitie van ouderdomsperiode**: selecteer de ouderdomsperiodedefinitie voor de ouderdomsmomentopname. U kunt één actieve ouderdomsmomentopname voor elke ouderdomsperiodedefinitie hebben. De ouderdomsmomentopname en de ouderdomsperiodedefinitie moeten afzonderlijk worden gemaakt.
- **Groeps-id**: u kunt dit veld desgewenst invullen. U kunt een groep gebruiken om de verzameling klanten te definiëren die in de ouderdomsmomentopname moet worden verwerkt. Als u een klantverzameling selecteert in dit veld, wordt een ouderdomsmomentopname alleen gemaakt voor de klantrekeningen die deel uitmaken van die klantverzameling. De geselecteerde klantverzameling moet van het type **Ouderdomsmomentopname** zijn. Als u dit veld leeg laat, wordt een ouderdomsmomentopname gemaakt voor alle klantrekeningen.


- **Criterium**: de ouderdomsmomentopname wordt berekend op basis van de datum die u selecteert:

    - **Transactiedatum**: de ouderdom van elke transactie wordt berekend op basis van de transactiedatum.
    - **Vervaldatum**: de ouderdom van elke transactie wordt berekend op basis van de vervaldatum.
    - **Documentdatum**: de ouderdom van elke transactie wordt berekend op basis van de documentdatum.

- **Ouderdom vanaf**: selecteer de datum die moet worden gebruikt in het veld **Huidige datum** voor de ouderdomsmomentopname. Ouderdomsperioden worden vervolgens berekend op basis van die datum. 

    - **Datum van vandaag**: gebruik de systeemdatum. Selecteer deze optie als het ouderdomsmomentopnameproces moet worden uitgevoerd in een terugkerende batchtaak. Telkens als de batchtaak wordt uitgevoerd, wordt de systeemdatum van die batchrun gebruikt.
    - **Geselecteerde datum**: gebruik een datum die u opgeeft. Als u deze optie selecteert, moet u een ouderdomsdatum invoeren.

   De huidige ouderdomsperiode is bijvoorbeeld 30 dagen. Als u **Datum van vandaag** selecteert in dit veld, begint de huidige ouderdomsperiode op de huidige datum en omvat vervolgens de vorige 29 dagen. Als u **Geselecteerde datum** selecteert en een datum invoert, begint de huidige ouderdomsperiode op de opgegeven datum en omvat vervolgens de vorige 29 dagen.

- **Aanmaningsstatus bijwerken**: stel deze optie in op **Ja** om de aanmaningsstatus van transacties op de pagina **Aanmaningen** bij te werken van **Beloofd te betalen** naar **Belofte om te betalen geschonden** als de ouderdomsdatum voorbij de datum in het veld **Beloofd te betalen** is. Stel deze optie in op **Nee** om de aanmaningsstatus ongewijzigd te laten op de pagina **Aanmaningen**.
- **Klanten met nulsaldo opnemen**: stel deze optie in op **Ja** als u alle klanten wilt opnemen, ongeacht het saldo. Als u alle klanten wilt opnemen, raden we u aan om zowel de functie **Verbetering van rangschikking van klant naar ouderdom** als de functie **Prestatieverbetering van klanten naar ouderdom rangschikken met klantverzamelingen** in te schakelen. Stel deze optie in op **Nee** als u alleen klanten met een saldo wilt opnemen. Deze instelling zorgt voor betere prestaties, omdat klanten die geen saldo hebben, worden overgeslagen.
- **Berekeningen van kredietlimiet overslaan tijdens ouderdomsproces** - als deze optie is ingesteld op **Ja**, worden **Subtotaalbedrag pakbon**, **Subtotaalbedrag voor openstaande order** en **Beschikbaar krediet** niet opnieuw berekend voor elke klant door het proces van rangschikking naar ouderdom. Deze saldi worden weergegeven op de pagina **Ouderdomssaldi**, in het feitenvak onder **Kredietlimiet**. Stel deze optie in op **Ja** voor snellere prestaties tijdens het ouderdomsrangschikkingsproces. Stel het in op **Nee** om de saldi opnieuw te berekenen bij het uitvoeren van het ouderdomsrangschikkingsproces. 
- **Bedrijfsbereik**: selecteer op het tabblad **Bedrijfsbereik** de rechtspersonen (bedrijven) die u wilt opnemen in de ouderdomsmomentopname. Alleen rechtspersonen waarvoor gecentraliseerde betalingen zijn ingesteld zijn beschikbaar om te selecteren. Transacties van de geselecteerde rechtspersonen worden vervolgens opgenomen in de ouderdomsperioden voor klanten met dezelfde partij-id in al deze rechtspersonen. De valutabedragen worden omgerekend naar de valuta van de rechtspersoon waarbij u bent aangemeld wanneer u de ouderdomsmomentopname maakt.

Het wordt aangeraden dit proces te plannen voor uitvoering in een batch.

> [!NOTE]
> Als u de batchprestaties wilt verbeteren bij het maken van ouderdomsmomentopnamen, voert u een getal in het veld **Maximum aantal batchtaken** op het sneltabblad **Standaardwaarden incasso** in op het tabblad **Aanmaningen** van de pagina **Parameters van module Klanten**. In het veld **Ouderdom van klantsaldi berekenen** raden we u aan te beginnen met een waarde tussen **12** en **20** en vervolgens de waarde aan te passen om de verwerking voor uw situatie te optimaliseren. Het wordt niet aangeraden een waarde groter dan **30** in te stellen, omdat dit van invloed is op de prestaties. 

