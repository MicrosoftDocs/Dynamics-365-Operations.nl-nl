---
title: Materiaalverbruik registeren met een mobiel apparaat
description: In dit onderwerp wordt een workflow beschreven waarmee u het grondstoffenverbruik in productie kunt registreren door middel van een mobiel apparaat.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 525b5a21047f0f39b9cd15448c4096d17c0e2dbd
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a>Materiaalverbruik registeren met een mobiel apparaat
In dit onderwerp wordt een workflow beschreven waarmee u het grondstoffenverbruik in productie kunt registreren door middel van een mobiel apparaat.

<a name="introduction"></a>Introductie
------------

Deze werkstroom is relevant als er een harde vereiste is voor traceerbaarheid van materialen. In dat geval moet vanwege de traceerbaarheid van de materialen de precieze tijd en hoeveelheden voor het verbruik worden gerapporteerd. Dit proces kunt u zien in tegenstelling tot bewerkingen met voor- of achterwaarts afboeken, waarbij een offset bestaat tussen het tijdstip van registratie en het tijdstip waarop het werkelijke verbruik plaatsvindt. Dit verklaart waarom een strategie van automatisch verbruik niet kan worden toegepast voor bepaalde materialen met traceerbaarheidsvereisten. We bekijken een eenvoudig scenario dat toelicht hoe u een workflow instelt voor het inschakelen van registratie van het grondstoffenverbruik in de productie door middel van een handheldapparaat. [![een workflow instellen om de registratie van grondstoffenverbruik via een handheldapparaat in te schakelen](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Scenariodetails

Een continu productieproces (5) verbruikt het batchmateriaal-grondstof RM-100. Het materiaal is voorhanden op locatie Bulk-001 (1) op nummerplaat PL-1 met twee batches, B1 en B2, beide met een hoeveelheid van 100 kg. Magazijnwerk (2) wordt vrijgegeven voor RM-100. Het materiaal wordt opgehaald vanuit Bulk-001 en naar de productinvoerlocatie PIL-01 (3) gebracht, die is gedefinieerd als niet met nummerplaten gecontroleerd. De machine-operator weegt materiaal van de productie-invoerlocatie (3) af en registreert het gewicht en batchnummer als verbruikt (4). Van de productie-invoerlocatie wordt een gedeelte van het materiaal handmatig toegevoegd aan het productieproces in gedefinieerde intervallen. Wanneer de machine-operator materiaal toevoegt, wordt dit op een schaal gewogen en het batchnummer wordt geregistreerd.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>De werkstroom instellen om met een handheldapparaat verbruik te registreren
Maak een eindproduct FG-100, met een stuklijst die de batchmateriaal-grondstof RM-100 bevat. Voeg twee batches B1 en B2 toe van RM-100 in een hoeveelheid van 100 naar locatie Bulk-001 op nummerplaat PL-1. Het afboekprincipe op de stuklijstregel voor RM-100 is ingesteld op **Handmatig**. Stel de productie-invoerlocatie in op PIL-01. U doet dit door deze locatie als de standaardproductie-invoerlocatie te kiezen in magazijn 51.

1.  Maak een nieuwe menuopdracht voor een mobiel apparaat: 

-    **Naam menuopdracht**: Materiaalverbruik registreren. 
-    **Titel**: Materiaalverbruik registreren. 
-    **Modus**: Indirect. 
-    **Activiteitscode**: Materiaalverbruik registeren.

2.  Voeg de menuopdracht toe aan het apparaatmenu **Productie mobiel**.
3.  Maak een productieorder voor het eindproduct: 

-    **Artikelnummer**: FG-100 
-    **Locatie**: 5 
-    **Magazijn**: 51 
-    **Hoeveelheid**: 150

De productieorder wordt **Geraamd** en **Vrijgegeven** en magazijnwerk wordt gemaakt.

4.  Voltooi het werk door middel van de workflow voor verzamelen van grondstoffen voor het draagbare apparaat.

Dit brengt het materiaal uit de bulklocatie naar de productie-invoerlocatie PIL-01. Nadat het werk is voltooid, heeft het materiaal de status **Verzameld op de productie-invoerlocatie**. De status nadat het werk is verwerkt, kan **Verzameld** of **Fysiek gereserveerd** zijn. Dit wordt geconfigureerd met de parameter **Status uitgeven na plaatsing op magazijnformulier**.

5.  Start de productieorder vanuit de client of op het handheldapparaat door middel van de menuopdracht **Productie - begin**.

Nadat de productieorder is gestart, kunt u met de workflow voor de handheld materiaalverbruik registreren. We beginnen met een verbruik van 25 kg van batch B1 te registreren.

6.  Selecteer de menuopdracht **Materiaalverbruik** **registreren** in het menu voor het handheldapparaat en voer de volgende gegevens in: 

-    Het productieordernummer. 
-    De locatie waar het materiaal wordt verbruikt, in dit geval PIL-01. 
-    Artikelnummer RM-100. 
-    Batchnummer B1. 
-    De hoeveelheid 25.

7.  Selecteer **OK**.

Merk op dat het bericht 'De journaalregel is gemaakt.' wordt weergegeven op het beeldscherm. Op de productieorder ziet u een openstaand journaal van het type **Productieverzamellijst** voor artikelnummer RM-100 en batch nummer B1. 

U kunt nu doorgaan met uw registratie, bijvoorbeeld op batchnummer B2. Elke keer dat u **OK** selecteert, wordt een nieuwe journaalregel toegevoegd aan het openstaande journaal. 

Nadat u de registratie hebt afgerond, selecteert u **Gereed**. Het journaal wordt geboekt en de werkstroom eindigt.

### <a name="additional-comments"></a>Aanvullende opmerkingen 

-   Als een gebruiker de werkstroom annuleert nadat een journaalregel is gemaakt, heeft het journaal een niet-geboekte status. Als de gebruiker later de workflow gebruikt voor dezelfde productieorder, worden de regels toegevoegd aan het openstaande journaal in plaats van aan een nieuw journaal.
-   De nieuwe werkstroom ondersteunt ook de registratie van serienummers.
-   Het is alleen mogelijk om een artikelnummer te registreren dat is gedefinieerd in de stuklijst of in de formule voor de geselecteerde productieorder of batchorder.
-   Materiaal kan ook worden overgebruikt. Als bijvoorbeeld wordt geschat dat het materiaal wordt verbruikt met de hoeveelheid van 100 kg, kan het vervolgens worden overgebruikt met een hoeveelheid van 105 kg.



