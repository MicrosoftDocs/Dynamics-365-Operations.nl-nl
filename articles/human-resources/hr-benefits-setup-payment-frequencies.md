---
title: Betalingsfrequenties instellen
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5fe0a16c4abbb9241fcdac88fd56e92bf04788c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008677"
---
# <a name="set-up-payment-frequencies"></a>Betalingsfrequenties instellen

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources gebruikt betalingsfrequenties om het jaarlijkse vergoedingssalaris te berekenen, het bedrag van de vergoedingspremie te bepalen dat een werknemer elke salarisperiode betaalt en de frequentie te definiëren waarmee betalingen aan leveranciers worden gedaan.

Bij de betalingsfrequenties voor vergoedingen wordt gebruikgemaakt van conversiefactoren om betalingstermijnen voor vergoedingen te converteren tussen maandelijkse, halfmaandelijkse, tweewekelijkse, wekelijkse en dagelijkse betalingsfrequenties. Hierdoor kunnen bedrijven de onderlinge afhankelijkheid definiëren tussen de betalingsfrequenties in een vergoedingsplan.

In de velden voor de conversiefactoren wordt de conversiefactor van de betalingsfrequentie naar de standaard betalingsperioden aangegeven en kan het systeem berekeningen tussen betalingsfrequenties uitvoeren. Het bedrag van de conversiefactor wordt ook gebruikt om het premiebedrag voor de vergoeding te bepalen die een werknemer bij elke betalingsfrequentie moet betalen.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Betalingsfrequenties**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Betalingsfrequentie | Een unieke naam voor de betalingsfrequentie. |
   | Beschrijving | Een beschrijving van de betalingsfrequentie. |
   | Periode | De juiste periode die het beste overeenkomt met de betalingsfrequentie van de vergoedingsprovider en de werknemer. De periodelijst is samengesteld uit de standaard betalingsperioden. |
   | Aantal betalingsperioden | Het aantal salarisperioden dat aangeeft hoe vaak de vergoedingsprovider of werknemers worden betaald. Dit bedrag wordt gebruikt om het jaarlijkse bedrag van het jaarlijkse vergoedingssalaris voor een werknemer te berekenen. |
   | Jaarlijkse conversiefactor | De jaarlijkse conversiefactor voor de betalingsfrequentie. De jaarlijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/1 jaar) = 12 |
   | Halfjaarlijkse conversiefactor | De halfjaarlijkse conversiefactor voor de betalingsfrequentie. De halfjaarlijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/2 keer per jaar) = 6 |
   | Driemaandelijkse conversiefactor | De driemaandelijkse conversiefactor voor de betalingsfrequentie. De driemaandelijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/4 kwartalen) = 3 |
   | Maandelijkse conversiefactor | De maandelijkse conversiefactor voor de betalingsfrequentie. De maandelijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/12 maanden) = 1 |
   | Halfmaandelijkse conversiefactor | De halfmaandelijkse conversiefactor voor de betalingsfrequentie. De halfmaandelijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/24 (2x per maand)) = 0,5 | 
   | Tweewekelijkse conversiefactor | De jaarlijkse conversiefactor voor de betalingsfrequentie. De jaarlijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/26 weken) = 0,461538 |
   | Wekelijkse conversiefactor | De jaarlijkse conversiefactor voor de betalingsfrequentie. De jaarlijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/52 weken) = 0,230769 |
   | Dagelijkse conversiefactor | De jaarlijkse conversiefactor voor de betalingsfrequentie. De jaarlijkse conversiefactor voor de maandelijkse salarisfrequentie is bijvoorbeeld: </br></br>(12 maandelijkse betalingen/365 dagen) = 0,032877 |

4. Selecteer **Opslaan**. 
