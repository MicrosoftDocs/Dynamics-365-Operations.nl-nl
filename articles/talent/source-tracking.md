---
title: Bronnen volgen voor kandidaatprofielen en sollicitaties
description: Dit onderwerp bevat informatie over het bijhouden van de bron voor kandidaatprofielen en -sollicitaties.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
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
ms.openlocfilehash: 5b368e97a716cd1ce4f668c2a97326877a2d3dff
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551882"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Bronnen volgen voor kandidaatprofielen en sollicitaties

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> Functionaliteit die in dit onderwerp wordt vermeld, is beschikbaar als onderdeel van een preview-versie. De inhoud en de functies kunnen worden gewijzigd. Als u deze functie wilt gebruiken, vraagt u een beheerder om deze in te schakelen via de **Beheerinstellingen** in Attract. Een toekomstige versie bevat rapporten voor het bijhouden van bronnen. Zie voor meer informatie [Toegang tot voorbeeldfuncties in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

Als kandidaten solliciteren op een functie, wordt in Attract automatisch de bron van hun sollicitaties bijgehouden. Hierdoor kunt u beschikken over waardevolle informatie waarmee u uw inspanningen met betrekking tot personeelswerving beter kunt inzetten. Wervers en aanstellende managers kunnen ook een sollicitatiebron selecteren tijdens het handmatig toevoegen van een kandidaat aan een functie of talentenpool.

U kunt de sollicitatiebron in de activiteitdetails van de sollicitatie bekijken op het tabblad **Activiteit**, alsmede in de sollicitatiehistorie die beschikbaar is onder **Profiel** in talentenpools. U kunt de profielbron van een kandidaat vinden in de kandidaatdetails op het tabblad **Profiel** in zowel sollicitaties als talentenpools.

> [!NOTE] 
> U kunt processjablonen vinden in de [Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Vooraf geconfigureerde bronnen

De standaardlijst met bronnen bevat de meest voorkomende sollicitatiebronnen. Sommige brontypen, zoals **Functiebord** en **Sociaal netwerk**, bevatten aanvullende brondetails. Bijvoorbeeld: **Sociaal netwerk** bevat Facebook en Twitter. Met het brontype **Verwijzing** kunt u een interne werknemer als verwijzing opgeven. De standaardlijst met bronnen bron bevat de volgende vooraf geconfigureerde bronnen:

-   Attract-vacaturesite

-   Bureau

-   Vacaturebeurs

-   Bedrijfsmarketing

-   Conferenties en beurzen

-   Beroepsvereniging

-   Functiebord

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Tijdschriften en publicaties

-   Sociaal netwerk

    -   Facebook

    -   Twitter

-   Werving op universiteiten

-   LinkedIn

-   Advertenties

-   Verwijzing

-   Toegevoegd door werver

-   Overig

## <a name="customize-the-source-list"></a>De lijst met bronnen aanpassen 

U kunt de lijst met bronnen aanpassen om aanvullende sollicitatiebronnen op te nemen. Als u deze lijst wilt aanpassen, volgt u de instructies in [Optiesets uitbreiden in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Bewerk de entiteit **TalentSource** om aanvullende bronnen op te nemen. 

Als u een negatieve impact op de gebruikersinterface (UI) wilt voorkomen, moet u de **TalentCategory**-opsommingswaarden (geen namen) niet bewerken of verwijderen voor het volgende:

- **Verwijzing**
- **LinkedIn**
- **Overig**

In plaats daarvan kunt u de **TalentSource**-opsomming uitbreiden om andere typen bronnen toe te voegen.
