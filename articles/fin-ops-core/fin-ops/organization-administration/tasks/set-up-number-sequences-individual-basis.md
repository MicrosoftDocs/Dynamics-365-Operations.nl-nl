---
title: Nummerreeksen instellen op een individuele basis
description: In dit artikel wordt uitgelegd hoe op een individuele basis nummerreeksen kunnen worden ingesteld.
author: SunilGarg
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7be72d348957c5c6494958276b2baa9c67d63c58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904983"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Nummerreeksen instellen op een individuele basis

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe op een individuele basis nummerreeksen kunnen worden ingesteld. Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben. Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een verwijzing genoemd. Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen. U kunt alle vereiste nummerreeksen tegelijkertijd instellen met de wizard **Nummerreeksen instellen** of u kunt individuele nummerreeksen maken of wijzigen met de pagina **Nummerreeksen**.

1. Ga naar **Navigatiedeelvenster > Modules > Organisatiebeheer > Nummerreeksen > Nummerreeksen**.
2. Selecteer **Nummerreeksen selecteren**.
3. Typ een waarde in het veld **Nummerreekscode**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer op het sneltabblad **Bereikparameters** een bereik voor de nummerreeks en selecteer bereikwaarden in de vervolgkeuzelijst. De scope bepaalt welke organisaties de nummerreeks gebruiken. Bovendien kunnen nummerreeksen die een ander bereik hebben dan **Gedeeld**, segmenten hebben die overeenkomen met hun bereik. Een nummerreeks met een bereik van **Rechtspersoon** kan bijvoorbeeld een segment voor rechtspersoon hebben. Zie [Overzicht van nummerreeksen](../number-sequence-overview.md) voor meer informatie over bereiken. 
6. Vouw de sectie **Segmenten** uit.
    - Definieer de notatie voor de nummerreeks door segmenten toe te voegen, te verwijderen en opnieuw te ordenen.  
    - De nummerreeksen van alle bereiken kunnen *constante segmenten* en *alfanumerieke segmenten* bevatten. Constante segmenten bevatten een set alfanumerieke tekens die niet veranderen. Gebruik dit segmenttype om een koppelteken of andere scheidingstekens toe te voegen tussen nummerreekssegmenten. De alfanumerieke segmenten bevatten een combinatie van hekjes (#) en ampersands (&). Deze tekens stellen letters en cijfers voor die omhoog gaan telkens als een nummer uit de reeks wordt gebruikt. Gebruik een hekje (#) om stijgende nummers aan te geven en een en-teken (&) om stijgende letters aan te geven. De indeling `#####_2014` maakt bijvoorbeeld de reeks `00001_2014`, `00002_2014` enzovoort. Er moet ten minste één alfanumeriek segment zijn. Bereiksegmenten, zoals bedrijf of rechtspersoon, zijn niet verplicht. Als u geen bereiksegmenten in de indeling opneemt, worden getallen nog steeds voor de geselecteerde verwijzing per bereik gegenereerd.  
7. Vouw de sectie **Verwijzingen** uit. Selecteer het documenttype of registratie waaraan u deze nummerreeks wilt toewijzen. Deze stap is optioneel voor reeksen die voor speciale gebruikspatronen van toepassingen worden gedefinieerd. In deze gevallen wordt een nieuw nummer gegenereerd met de waarde van een nummerreekscode of ID zonder een verwijzing te gebruiken. Een voorbeeld van een gebruikspatroon voor speciale toepassingen is een reeks boekstukken die voor specifieke journaalnamen wordt gebruikt. We raden het gebruik van zulke patronen echter niet aan.  
8. Vouw de sectie **Algemeen** uit. Geef op het sneltabblad Algemeen op of de nummerreeks handmatig is en doorlopend of niet-doorlopend. Voer ook de laagste en hoogste nummers in die in de nummerreeks kunnen worden gebruikt. Een niet-doorlopende nummerreeks wijzigen in een doorlopende nummerreeks wordt niet aanbevolen. De nummerreeks zal niet echt continu worden. Deze wijziging kan ook overtredingen van dubbele sleutels veroorzaken in de database. Doorlopende nummerreeksen hebben bovendien een grotere invloed op de prestaties.   
9. Klik op **Opslaan**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
