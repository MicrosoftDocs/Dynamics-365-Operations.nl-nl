---
title: Tarieven configureren
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
ms.openlocfilehash: a2626e9fc5f15bbdad0f6accf64bc4b211939ed0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008676"
---
# <a name="configure-rates"></a>Tarieven configureren

[!include [banner](includes/preview-feature.md)]

Tarieven in Microsoft Dynamics 365 Human Resources bepalen hoeveel werkgevers en werknemers bijdragen voor een vergoeding. De waarde kan een bedrag of flex-kredieten zijn, afhankelijk van uw configuratie.

Gebruik tarieven om te bepalen hoeveel werknemers en werkgevers betalen voor elke vergoeding op basis van verschillende factoren. Dekkingstarieven hebben een ingangsdatum, dus kunt u een historisch overzicht van de tarieven bijhouden. 

## <a name="set-up-rates"></a>Tarieven instellen

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Tarieven**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Tarief | Een unieke naam die het vergoedingstarief aanduidt. |
   | Beschrijving | Een beschrijving van het vergoedingstarief. |
   | Geldig vanaf | De datum waarop het tarief van kracht wordt. De huidige systeemdatum is de standaardwaarde. 
   | Vervaldatum | De einddatum van het tarief. 12/31/2154 (wat voor nooit staat) is de standaardwaarde. |
   | Niveaus gebruiken | Het niveau dat moet worden gebruikt voor de berekening van het vergoedingstarief. Eén niveau voor een vergoedingstarief van één niveau of een dubbel niveau voor een vergoedingstarief van twee niveaus. Een voorbeeld van een dubbel niveau is een niveau dat is gebaseerd op geslacht en leeftijd. |
   | Betalingsfrequentie | De betalingsfrequentie waarmee wordt bepaald hoe vaak het premietarief voor vergoedingen wordt betaald aan de vergoedingsprovider. Als de betalingsfrequentie bijvoorbeeld maandelijks is, vertegenwoordigt het vergoedingstarief het maandelijkse betalingsbedrag. |
   | Berekening betalingsfrequentie | De methode voor de berekening van het betalingsfrequentie: Standaard of Jaarlijks. |
   | Afronding betalingsfrequentie | De methode voor het afronden van het tarief: Standaard of Afgekapt. |
   | Werknemersbedrag niet-roker | Het bedrag dat de vergoedingsprovider berekent voor een werknemer die niet rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dat moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Werkgeversbedrag niet-roker | Het bedrag dat de vergoedingsprovider berekent voor een werknemer die niet rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Werknemersbedrag roker | Het bedrag dat de vergoedingsprovider berekent voor een werknemer die rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dat moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Werkgeversbedrag roker | Het bedrag dat de vergoedingsprovider berekent voor een werknemer die rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dat moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Administratiebedrag | Het administratieve bedrag door een externe beheerder in rekening wordt gebracht. Dit is het bedrag dat de werkgever betaalt aan de externe beheerder en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Tarief voor flexibele kredieten | Het aantal flex-kredieten dat de vergoeding kost. Dit geldt alleen voor tarieven voor vergoedingsplannen die zijn gekoppeld aan flex-kredietprogramma's. Als u niveautarieven gebruikt, wordt het flex-krediettarief gedefinieerd in Acties > Niveautarieven. |
   | Ingangsdatum wijzigen | De datum waarop de wijziging van het vergoedingstarief van kracht wordt. Het systeem wijzigt automatisch het vergoedingstarief en werkt alle vergoedingsplannen bij die aan dit tarief zijn gekoppeld, zolang u de updateverwerking voor de tariefwijziging uitvoert. U moet deze datum niet instellen, tenzij u wilt dat de vergoedingen voor werknemers automatisch worden bijgewerkt op basis van dit tarief. Dit wordt normaal gesproken gereserveerd voor de automatische verwerking van toekomstige tariefwijzigingen. De ingangsdatum van de wijziging moet tussen de ingangs- en vervaldatum van het vergoedingstarief liggen. |
   | Tariefswijziging voltooid | Het selectievakje Tariefwijziging voltooid wordt automatisch ingeschakeld nadat de wijzigingen in de vergoedingstarief zijn voltooid door de updateverwerking voor de tariefwijziging. |

4. Als u wijzigingen in de instellingen van het vergoedingstarief wilt bijhouden en beheren, selecteert u **Acties** en selecteert u vervolgens **Versies onderhouden**.

5. Selecteer **Opslaan**. 

## <a name="set-up-tier-rates"></a>Niveautarieven instellen

U kunt niveautarieven gebruiken in uw tariefinstelling als het tarief varieert afhankelijk van verschillende factoren. U kunt bijvoorbeeld tariefniveaus configureren om aan te geven dat bij een leeftijd tot 34,99 het bedrag voor niet-rokers 2 bedraagt. Als uw leeftijd hoger is dan 39,99, is het bedrag voor niet-rokers 3.

U kunt ook dubbele niveaus gebruiken. Als u **Dubbel niveau** selecteert voor de waarde **Niveaus gebruiken** in het formulier **Tariefinstellingen**, kunt u tarieven definiëren op basis van twee dimensies. U kunt bijvoorbeeld een systeem met dubbel tarief configureren om aan te geven dat bij een man met een leeftijd tot 34,99 het bedrag voor niet-rokers 2 bedraagt. Als u een man bent en uw leeftijd is hoger dan 39,99, dan bedraagt het bedrag voor niet-rokers 3. Als u een vrouw bent en uw leeftijd is hoger dan 34,99, dan bedraagt het bedrag voor niet-rokers 1,8. Als u een vrouw bent en uw leeftijd is hoger dan 39,99, dan bedraagt het bedrag voor niet-rokers 2,8.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Tarieven**.

2. Selecteer een of meer tarieven in de lijst, selecteer **Acties**en selecteer vervolgens **Niveautarieven**.

3. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- | 
   | Beschrijving | De waarde van het veld Beschrijving wordt toegepast vanuit de beschrijving in de record met tariefinstellingen. Dit helpt u bij het vaststellen aan welke tariefinstellingen de niveautarieven zijn gekoppeld. |
   | Laagcode | Selecteer een laagcode. Laagcodes worden gedefinieerd in het formulier Laagcodes. Het systeem geeft automatisch de beschrijving weer van de laagcode in het raster aan de linkerkant. |
   | Niveautype | Geeft aan welk veld moet worden gebruikt als een selectiecriterium voor het berekeningsproces van het niveautarief. Bijvoorbeeld:</br></br><ul><li>Als Leeftijd wordt gebruikt, gebruikt het systeem de geboortedatum van de werknemer in het berekeningsproces voor het vergoedingstarief.</li><li>Als Salaris wordt gebruikt, gebruikt het systeem het jaarlijks vergoedingssalaris van de werknemer in het berekeningsproces voor het vergoedingstarief.</li><li>Als Functietype wordt gebruikt, wordt in het systeem de huidige actieve positierecord van de werknemer gebruikt om het functietype te bepalen op basis van de functierecord die aan de positie is gekoppeld.</li></ul></br></br>De niveautypen zijn Leeftijd, Salaris, Fysiek, Geslacht, Voltijdse equivalent, Functietype, Compensatieregio en Niveau. | 
   | Niveau | De waarde die moet worden gebruikt bij het niveautype tijdens het berekeningsproces voor het vergoedingstarief. Bijvoorbeeld:</br></br><ul><li>Als het niveautype Leeftijd is, is dit de leeftijdswaarde.</li><li>Als het niveautype Salaris is, is dit het salarisbedrag.</li><li> Als het niveautype Functietype is, is dit het functietype.</li></ul></br></br>Bij een niveautype Leeftijd of Salaris gebruikt het systeem een oplopende benadering bij het selecteren van het niveautarief. Dit betekent dat de waarde in het veld Niveau de ondergrens van het niveau vertegenwoordigt. Bij een nvieautype van Functietype gebruikt het systeem de exacte overeenkomst bij het selecteren van het niveautarief. |
   | Berekeningstype | Geeft aan hoe het bedrag in het veld voor het berekeningsbedrag moet worden gebruikt en welke formuleberekening moet worden uitgevoerd, indien nodig. Als het berekeningstype een vast bedrag is, gebruikt het systeem de bedragvelden in ongewijzigde vorm. Als het berekeningstype een bedrag per $ is van het salaris of de dekking, gebruikt het systeem het berekeningsbedrag en de berekeningsrichting bij de rekenkundige berekening.</br></br>Als het berekeningstype een bedrag per $ van het salaris is, gebruikt het systeem de volgende rekenkundige vergelijking:</br></br>Jaarlijks vergoedingssalaris gedeeld door het berekeningsbedrag (naar boven of naar beneden afgerond) maal de bedragen voor rokers of niet-rokers voor werknemer of werkgever.</br></br>Als het berekeningstype een bedrag per $ van de dekking is, gebruikt het systeem de volgende rekenkundige vergelijking:</br></br>Dekkingsbedrag gedeeld door het berekeningsbedrag (naar boven of naar beneden afgerond) maal de bedragen voor rokers of niet-rokers voor werknemer of werkgever.</br></br>In beide berekeningen wordt de berekeningsrichting gebruikt om te bepalen of het jaarlijkse vergoedingssalaris of het dekkingsbedrag gedeeld door het bedrag van de berekening naar boven of beneden moet worden afgerond. |
   | Bedrag van berekening | Het bedrag dat moet worden gebruikt tijdens het berekeningsproces van het vergoedingstarief. Dit bedrag is de deler tijdens de rekenkundige berekening van het niveautarief. |
   | Richting van berekening | De richting (Verhogen of Verlagen) waarin het berekende resultaatbedrag moet worden afgerond. Het systeem ondersteunt drie berekeningsrichtingen: Leeg (exacte methode), Verhogen en Verlagen.</br></br><ul><li>Als dit veld leeg is, wordt de exacte berekening van het bedrag per salaris/dekkingsbedrag gebruikt, gedeeld door het bedrag van de berekening. Als deze waarde een breuk bevat, wordt deze door het systeem gebruikt in de berekening.</li><li>Bij Verhogen verhoogt het systeem de rekenkundige berekening van het salaris/dekkingsbedrag gedeeld door het bedrag van de berekening naar het volgende gehele getal, wat betekent dat 12,25 zou worden verhoogd naar 13.</li><li>Bij Verlagen verlaagt het systeem de rekenkundige berekening van het salaris/dekkingsbedrag gedeeld door het bedrag van de berekening naar het huidige gehele getal, wat betekent dat 12,25 zou worden verlaagd naar 12.</li></ul> |
   | Werknemersbedrag niet-roker | Het bedrag dat een vergoedingsprovider berekent voor een werknemer die niet rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Werkgeversbedrag niet-roker | Het bedrag dat een vergoedingsprovider berekent voor een werknemer die niet rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Werknemersbedrag roker | Het bedrag dat een vergoedingsprovider berekent voor een werknemer die niet rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Werkgeversbedrag roker | Het bedrag dat een vergoedingsprovider berekent voor een werknemer die niet rookt. Dit is het bedrag dat de werkgever betaalt aan de vergoedingsprovider en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Administratiebedrag | Het administratieve bedrag door een externe beheerder in rekening wordt gebracht. Dit is het bedrag dat de werkgever betaalt aan de externe beheerder en dit moet worden gebaseerd op de betalingsfrequentie voor de tariefinstellingen. |
   | Flex-krediet voor niet-rokerstarief | Het aantal flex-kredieten dat de vergoeding kost, gebaseerd op de berekening die is gedefinieerd voor het tariefniveau voor niet-rokers. Als het berekeningstype bijvoorbeeld 'Per $ dekkingsbedrag' is, het berekeningsbedrag 10.000 bedraagt en het flex-krediet voor niet-rokerstarief 6 is, wil dat zeggen dat als een werknemer die niet rookt een dekking van $ 10.000 kiest, dit 6 flex-kredieten zal kosten. Als zij een dekking van $ 20.000 kiezen, kost dit 12 flex-kredieten enzovoort. |
   | Flex-krediet voor rokerstarief | Het aantal flex-kredieten dat de vergoeding kost, gebaseerd op de berekening die is gedefinieerd voor het tariefniveau voor rokers. |

5. Selecteer **Opslaan**. 
