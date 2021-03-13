---
title: Producten voor tweeërlei gebruik
description: In dit onderwerp wordt uitgelegd hoe u producten kunt bijhouden die zijn geïdentificeerd als producten voor tweeërlei gebruik. U kunt certificaatnummers opslaan voor elk relevant product en land van bestemming en geldige certificaatnummers afdrukken op relevante facturen, pakbonnen en/of verkooporders.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4623b6eaa18b65f0f61cb8c227115d59f3ff9c08
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007689"
---
# <a name="dual-use-goods"></a>Producten voor tweeërlei gebruik

[!include [banner](../includes/banner.md)]

Producten voor tweeërlei gebruik zijn meestal artikelen met zowel civiele als militaire toepassingen. Een chemische stof kan bijvoorbeeld worden gebruikt als meststof of explosief. Veel landen hebben speciale regelingen die van toepassing zijn op de uitvoer, invoer en het transport van producten voor tweeërlei gebruik. Het is daarom belangrijk dat bedrijven die betrokken zijn bij internationaal handelsverkeer van producten voor tweeërlei gebruik, de verschillende beleidsregels en certificaten bijhouden.

Met de functie voor tweeërlei gebruik kunnen bedrijven producten bijhouden die zijn geïdentificeerd als producten voor tweeërlei gebruik. Ze kunnen certificaatnummers opslaan voor elk relevant product en land van bestemming en geldige certificaatnummers afdrukken op relevante facturen, pakbonnen en/of verkooporders. Zo zorgt u ervoor dat bij de verzending van uw producten altijd up-to-date certificeringen worden opgenomen.

Hier volgt een aantal scenario:

1. De pagina **Landinstellingen voor tweeërlei gebruik** in uw systeem geeft aan dat voor verzendingen naar Frankrijk een certificering vereist is.
2. De pagina **Vrijgegeven productdetails** voor product X-100 geeft aan dat het een product voor tweeërlei gebruik is. Samen geven de code, categorie, groep en regime de exportcontroleclassificatie aan waartoe het product behoort.
3. Op de pagina met **Certificaten voor tweeërlei gebruik** vindt u een certificaat voor product X-100 wanneer het naar Frankrijk wordt verzonden. Dit certificaat is verlopen op 1 januari 2020.
4. Op 17 juni 2020 maakt u een verkooporder voor een klantbedrijf dat in Frankrijk is gevestigd. De order bevat product X-100.
5. Wanneer u de verkooporder opslaat, ziet u de volgende systeemmelding:

    1. Bevat de order producten voor tweeërlei gebruik?
    2. Als de order producten voor tweeërlei gebruik bevat, zijn er dan voor het land van bestemming certificaten voor tweeërlei gebruik nodig?
    3. Als voor het land certificaten voor tweeërlei gebruik vereist zijn, bestaat er dan een geldig certificaat voor elk product voor tweeërlei gebruik voor het land van bestemming?

6. De order bevat product X-100, het product wordt verzonden naar Frankrijk en er bestaat een Frans certificaat voor het product. Het certificaat is echter verlopen. Daarom wordt het volgende waarschuwingsbericht weergegeven: "De certificaten voor tweeërlei gebruik voor een of meer artikelen voor tweeërlei gebruik in deze verkooporder zijn niet geldig. Wilt u doorgaan met het bevestigen?"

In dit onderwerp wordt uitgelegd hoe u alle instellingen configureert die vereist zijn voor het instellen van producten voor tweeërlei gebruik en die dit scenario ondersteunen.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Vereisten voor tweeërlei gebruik voor elk land definiëren

Verschillende landen hebben verschillende vereisten voor producten voor tweeërlei gebruik. U gebruikt de pagina **Landinstellingen voor tweeërlei gebruik** om bij te houden voor welk land wel en voor welk land geen certificaat nodig is. De informatie die u hier opgeeft, wordt gecontroleerd wanneer u verkooporders maakt en u wordt eraan herinnerd om de vereiste certificeringen te leveren.

Voer de volgende stappen uit om de informatie in te stellen over vereisten voor tweeërlei gebruik voor verschillende landen.

1. Ga naar **Productinformatiebeheer \> Instellingen \> Productconformiteit \> Producten voor tweeërlei gebruik \> Landinstellingen voor tweeërlei gebruik**.
2. Selecteer een bestaande landinstelling om deze te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe landinstelling te maken.
3. Stel de volgende waarden in voor de geselecteerde of nieuwe landinstellingen.

    | Veld | Omschrijving |
    |---|---|
    | Land/regio | Selecteer het land waarvoor u de vereisten traceert. |
    | Certificaat vereist | Schakel dit selectievakje in voor landen waarvoor een certificering vereist is voor producten voor tweeërlei gebruik. Schakel deze optie uit voor landen waarvoor deze certificering niet is vereist. |

## <a name="create-dual-use-categories"></a>Categorieën voor tweeërlei gebruik maken

Producten voor tweeërlei gebruik worden vaak ingedeeld op basis van hun exportcontroleclassificatienummer (ECCN). ECCN is een alfanumerieke code waarmee artikelen worden ingedeeld op basis van factoren zoals het basisproduct en de technologie. Op de pagina **Categorieën voor tweeërlei gebruik** kunt u een lijst maken van de categorieën die u gebruikt voor rapportagedoeleinden.

Ga als volgt te werk om categorieën voor tweeërlei gebruik in te stellen:

1. Ga naar **Productinformatiebeheer \> Instellingen \> Productconformiteit \> Producten voor tweeërlei gebruik \> Categorieën voor tweeërlei gebruik**.
2. Selecteer een bestaande categorie om deze te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe categorie te maken.
3. Stel de volgende waarden in voor de geselecteerde of nieuwe categorie.

    | Velden | Omschrijving |
    |---|---|
    | Code voor dubbel gebruik | Voer de volledige ECCN in (bijvoorbeeld *3A001*).|
    | Categorie voor dubbel gebruik | Voer het CCL-onderdeel (Commerce Control List) van de ECC-code voor de categorie in. Voor de ECCN-code *3A001* is deze waarde bijvoorbeeld *3*. |
    | Groep voor tweeërlei gebruik | Voer het gedeelte voor de productgroep van de ECCN-code in. Voor de ECCN-code *3A001* is deze waarde bijvoorbeeld *A*. |
    | Regime voor tweeërlei gebruik | Voer de regimecode in voor het artikel. Met deze code wordt de reden aangegeven waarom het artikel wordt geclassificeerd als een product voor tweeërlei gebruik. Voor de ECCN-code *3A001* is deze waarde bijvoorbeeld *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Categorieën voor tweeërlei gebruik toepassen op producten

Voer de volgende stappen uit om een product te identificeren voor tweeërlei gebruik en een categorie voor tweeërlei gebruik toe te passen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer of maak een product om de pagina **Vrijgegevens productgegevens** te openen.
1. Stel op het sneltabblad **Buitenlandse handel** de optie **Producten voor tweeërlei gebruik** in op **Ja** om het huidige product te identificeren als een goed voor tweeërlei gebruik.
1. Stel het veld **Code voor tweeërlei gebruik** in op de code die van toepassing is op het huidige product. (U hebt deze code gedefinieerd op de pagina **Categorieën voor tweeërlei gebruik**.)

Deze instelling wordt gecontroleerd wanneer u een verkooporder maakt.

## <a name="set-up-dual-use-certificates"></a>Certificaten voor tweeërlei gebruik instellen

U gebruikt de pagina **Certificaten voor tweeërlei gebruik** om de vereiste certificaten voor voor tweeërlei gebruik voor elk product en land in te stellen en te beheren. U kunt de details van elk certificaat bijhouden, zoals het land en de geldigheidsdatums. U kunt ook opties instellen om op te geven waar deze informatie moet worden afgedrukt. De gegevens kunnen bijvoorbeeld worden afgedrukt op de factuur, de pakbon en/of de verkooporder. Deze instelling wordt gecontroleerd wanneer u een verkooporder maakt.

1. Ga naar **Productinformatiebeheer \> Instellingen \> Productconformiteit \> Producten voor tweeërlei gebruik \> Certificaten voor tweeërlei gebruik**.
2. Selecteer een bestaand certificaat om dit te bewerken of selecteer **Nieuw** in het actievenster om een nieuw certificaat te maken.
3. Stel de volgende waarden in voor het geselecteerde of nieuwe certificaat.

    | Veld | Omschrijving |
    |---|---|
    | artikelnummer | Selecteer het artikelnummer van het product voor tweeërlei gebruik waarop dit certificaat van toepassing is. |
    | Land/regio | Het land of de regio van bestemming waar u dit certificaat moet gebruiken. |
    | Certificaatnummer | Het nummer dat wordt weergegeven op het certificaat dat aan de leverancier of klant is uitgegeven. |
    | Geldig | Selecteer de eerste datum waarop het huidige certificaat geldig is.|
    | Vervaldatum | Selecteer de laatste datum waarop het huidige certificaat geldig is. |
    | Afdrukken op factuur | Schakel dit selectievakje in om het certificaatnummer af te drukken op facturen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik. |
    | Afdrukken op pakbon | Schakel dit selectievakje in om het certificaatnummer af te drukken op pakbonnen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik. |
    | Afdrukken op verkooporder | Schakel dit selectievakje in om het certificaatnummer af te drukken op verkooporders die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik. |
