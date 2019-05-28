---
title: Intelligente aanbevelingen
description: In dit onderwerp wordt uitgelegd hoe machine learning kan worden gebruikt voor aanbevelingen van functies en sollicitanten.
author: andreabichsel
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: fb31b413cfe3cd168bbb12ce6070325ff5f736da
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517693"
---
# <a name="intelligent-recommendations"></a>Intelligente aanbevelingen

[!include[banner](../includes/banner.md)]

Machine learning kan wervers en aanstellend managers helpen snel de beste kandidaten voor een positie te bepalen. Het kan prospects ook helpen de positie te vinden die het best past bij hun profiel en interesses. Naarmate deze functies worden gebruikt en feedback wordt gegeven, worden aanbevelingen beter.

> [!NOTE] 
> - De intelligente aanbevelingsfuncties zijn alleen beschikbaar met de [Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Functionaliteit die in dit onderwerp wordt vermeld, is beschikbaar als onderdeel van een preview-versie. De inhoud en de functies kunnen worden gewijzigd. Als u deze functie wilt gebruiken, vraagt u een beheerder om deze in te schakelen via de **Beheerinstellingen** in Attract. Stel **Kandidaataanbeveling**, **Functieaanbeveling** en **Prospectaanbeveling** in op **Aan**. Zie voor meer informatie [Toegang tot voorbeeldfuncties in Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature). 


## <a name="candidate-recommendations"></a>Aanbevelingen voor kandidaat

Aangezien vacatures tal van sollicitanten kunnen aantrekken, kan het lastig voor wervers en aanstellend managers om de kandidaten te zoeken van wie de vaardigheden en achtergrond het best overeenkomen met de positie. Door een analyse van de correlatie tussen de functieomschrijving en -vereisten en de gegevens uit de cv's en profielen van de kandidaten, kan machine learning worden gebruikt om kandidaataanbevelingen te produceren. Kandidaataanbevelingen kunnen wervers en aanstellend managers helpen het beste talent te bepalen en hen sneller naar de sollicitatiegesprekfase te verplaatsen. Voor elke functie, als er meer dan tien kandidaten of prospects met cv's of volledige profielen kandidaten zijn, worden de kandidaten of prospects die het best overeenkomen met de vereisten van de functie, weergegeven in de sectie **Te overwegen sollicitanten** op de pagina **Functie**.

Voor een aanbevolen kandidaat kunt u **Kandidaat weergeven** selecteren op de kandidaatkaart om het profiel van de kandidaat te bekijken en actie te ondernemen op zijn of haar sollicitatie. U kunt de ellipsisknop (**...**) gebruiken om het profiel van de kandidaat op een nieuw tabblad te openen. U kunt deze knop ook gebruiken om feedback te geven over de aanbeveling. Op deze manier kunt u de aanbevelingsengine afstemmen en toekomstige aanbevelingen verbeteringen. Eventuele aanbevelingen waarover u niet tevreden bent, worden verwijderd uit de sectie **Te overwegen sollicitanten** wanneer u de **Functie** vernieuwt. U kunt de feedbackkaart gebruiken om aan te geven waarom u de aanbeveling niet nuttig vond.

## <a name="job-recommendations"></a>Functieaanbevelingen 

Wanneer een potentiële werknemer de vacaturesite gebruikt om te solliciteren o een functie, worden in Attract andere openstaande posities in de organisatie aanbevolen. Deze aanbevelingen zijn gebaseerd op eerdere sollicitaties en op het cv of kandidaatprofiel van de prospect. Functieaanbevelingen helpen prospects daarom snel de taken te vinden die het best bij hen passen. Functieaanbevelingen worden verstrekt aan prospects als meer dan tien functies zijn geplaatst op de vacaturesite. Prospects kunnen de details van een geplaatste functie openen vanaf de aanbevelingskaart. Ze kunnen ook feedback over een aanbeveling geven om te helpen toekomstige aanbevelingen te verbeteren.

## <a name="prospect-recommendations"></a>Prospectaanbevelingen 

Wanneer een nieuwe positie beschikbaar wordt, kan het even duren voordat al uw eerdere sollicitanten en uw gehele talentnetwerk zijn bekeken. Om Attract u hierbij te laten helpen, kunt u intelligente Machine Learning-algoritmen gebruiken. Dit betekent dat Attract alle kandidaten bekijkt en degenen voorstelt die geschikt zijn zodra u de functie maakt. Als u deze aanbevelingen wilt bekijken, schakelt u de fase **Prospect** voor de functie in. Het kan wel een minuut duren voordat Attract uw gehele database met kandidaten heeft gescand om aanbevelingen te doen.

De aanbevelingen worden weergegeven als kaarten op het tabblad **Prospects** van een functie waarvoor de fase **Prospect** is ingeschakeld. Op deze kaarten worden de vaardigheden in het profiel van de prospect weergegeven, alsmede eventuele opleidingskwalificatiegegevens. Als u een interessante aanbeveling vindt, kunt u de kandidaat toevoegen als een prospect voor die functie.

> [!NOTE]
> Als u onlangs bent begonnen Attract te gebruiken, moet u wachten totdat u 10 of meer sollicitanten met volledige profielen of cv's hebt voordat u deze functie kunt gebruiken.

Om een mogelijk verschil in de aanbevelingen te voorkomen, scant Attract alleen kandidaatprofielen op vaardigheden, kwalificaties en andere trefwoorden die overeenkomen met de functieomschrijving. Bovendien verwijdert Attract persoonlijke gegevens uit de kandidaatprofielen vóór evaluatie.
