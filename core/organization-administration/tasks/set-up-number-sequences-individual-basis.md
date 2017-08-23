--- 
title: Nummerreeksen op een individuele basis instellen
description: Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben.
author: sericks007
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5c63022586f24cc1a50f7734910f15b237d35216
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Nummerreeksen op een individuele basis instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben. Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een verwijzing genoemd. Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen. U kunt alle vereiste nummerreeksen tegelijkertijd instellen met de wizard Nummerreeksen instellen of u kunt individuele nummerreeksen maken of wijzigen met de pagina Nummerreeksen.

1. Ga naar Organisatiebeheer > Nummerreeksen > Nummerreeksen.
2. Klik op Nummerreeks.
3. Typ een waarde in het veld Nummerreekscode.
4. Typ een waarde in het veld Naam.
5. Vouw de sectie Bereikparameters uit.
    * Selecteer op het sneltabblad Bereikparameters een bereik voor de nummerreeks en selecteer bereikwaarden.     De scope bepaalt welke organisaties de nummerreeks gebruiken. Bovendien kunnen nummerreeksen die een ander bereik hebben dan Gedeeld, segmenten hebben die overeenkomen met hun bereik. Een nummerreeks met een bereik van Rechtspersoon kan bijvoorbeeld een segment voor rechtspersoon hebben. Zie voor meer informatie over bereiken het Help-onderwerp "Overzicht van nummerreeksen".  
6. Vouw de sectie Segmenten uit.
    * Definieer op het sneltabblad Segmenten de notatie voor de nummerreeks door segmenten toe te voegen, te verwijderen en opnieuw te ordenen.  
    * De nummerreeksen van alle bereiken kunnen constante segmenten en alfanumerieke segmenten bevatten. Constante segmenten bevatten een set alfanumerieke tekens die niet veranderen. Gebruik dit segmenttype om een koppelteken of andere scheidingstekens toe te voegen tussen nummerreekssegmenten. De alfanumerieke segmenten bevatten een combinatie van hekjes (#) en ampersands (&). Deze tekens stellen letters en cijfers voor die omhoog gaan telkens als een nummer uit de reeks wordt gebruikt. Gebruik een hekje (#) om stijgende nummers aan te geven en een en-teken (&) om stijgende letters aan te geven. De indeling #####_2014 maakt bijvoorbeeld de reeks 00001_2014, 00002_2014, enzovoort.     Er moet ten minste één alfanumeriek segment zijn. Bereiksegmenten, zoals bedrijf of rechtspersoon, zijn niet verplicht. Als u geen bereiksegmenten in de indeling opneemt, worden getallen nog steeds voor de geselecteerde verwijzing per bereik gegenereerd.  
7. Vouw de sectie Verwijzingen uit.
    * Selecteer op het sneltabblad Verwijzingen het documenttype of de record waaraan u deze nummerreeks wilt toewijzen.     Deze stap is optioneel voor reeksen die voor speciale gebruikspatronen van toepassingen worden gedefinieerd. In deze gevallen wordt een nieuw nummer gegenereerd met de waarde van een nummerreekscode of ID zonder een verwijzing te gebruiken. Een voorbeeld van een gebruikspatroon voor speciale toepassingen is een reeks boekstukken die voor specifieke journaalnamen wordt gebruikt. We raden het gebruik van zulke patronen echter niet aan.  
8. Vouw de sectie Algemeen uit.
    * Geef op het sneltabblad Algemeen op of de nummerreeks handmatig is en doorlopend of niet-doorlopend. Voer ook de laagste en hoogste nummers in die in de nummerreeks kunnen worden gebruikt.     Een niet-doorlopende nummerreeks wijzigen in een doorlopende nummerreeks wordt niet aanbevolen. De nummerreeks zal niet echt continu worden. Deze wijziging kan ook overtredingen van dubbele sleutels veroorzaken in de database. Doorlopende nummerreeksen hebben bovendien een grotere invloed op de prestaties.   
9. Klik op Opslaan.


