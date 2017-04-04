---
title: Streepjescodemaskers instellen
description: Dit onderwerp wordt beschreven hoe u tekens van streepjescodemaskers, gemaakte streepjescodemaskers instelt en hoe u kunt streepjescodes toewijzen aan streepjescodes maskers.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Streepjescodemaskers instellen

Dit onderwerp wordt beschreven hoe u tekens van streepjescodemaskers, gemaakte streepjescodemaskers instelt en hoe u kunt streepjescodes toewijzen aan streepjescodes maskers.

<a name="set-up-bar-code-mask-characters"></a>Tekens van streepjescodemaskers instellen
-------------------------------

Streepjescodemaskers worden gebruikt voor het maken van streepjescodes en snel identificeren van streepjescodes die naar het punt van verkoop (POS) worden gescand. Maskers bestaan uit tekens die fungeren als tijdelijke aanduidingen die aangeven van de indeling voor de streepjescodes die worden gemaakt. Als u wilt een streepjescodemasker is geconfigureerd, moet u de tekens van streepjescodemaskers instellen. Ga naar **detailhandel en commerce**&gt;**voorraadbeheer**&gt;**streepjescodes en etiketten**&gt;**masker tekens**. Klik op **New** tekens van streepjescodemaskers maken. Tekens van streepjescodemaskers kunnen worden gemaakt om aan te geven van de volgende gegevens in de streepjescode.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Tijdelijke aanduiding voor de product-ID.                                                                                     |
| **Any number**       | Hiermee geeft een getal dat zal niet gecodeerd in de streepjescodes.                                                  |
| **Check digit**      | Geeft aan dat de streepjescode in een streepjescodemasker een controlecijfer wordt op basis van de geldigheid van een streepjescode te bevestigen. |
| **Size digit**       | Geeft de grootte in een streepjescode voor een productvariant met onder andere grootte gemaakt.                                 |
| **Color digit**      | Geeft de kleur in een streepjescode voor een productvariant inclusief kleur gemaakt.                               |
| **Style digit**      | Geeft aan stijl in een streepjescode voor een productvariant waarin een stijl gemaakt.                             |
| **EAN license code** | Tijdelijke aanduiding voor het EAN-licentie is uitgegeven voor een EAN-licentiecodes.                                                       |
| **Prijs**            | Geeft aan prijs prijs ingesloten streepjescodes.                                                                   |
| **Quantity**         | Geeft de hoeveelheid in hoeveelheid of willekeurige gewicht ingesloten streepjescodes.                                                |
| **Employee**         | Geeft aan segment van de streepjescode voor werknemer-id-nummer gebruikt voor de streepjescode POS-aanmelding.                                  |
| **Customer**         | Geeft aan klant-ID-segment.                                                                                  |
| **Gegevensinvoer**       | *Nog niet geïmplementeerd.*                                                                                          |
| **Discount code**    | Geeft de code voor korting voor een streepjescode die wordt gebruikt voor een korting toevoegen aan een punt van verkooptransactie             |
| **Geschenkbon**        | Geeft een geschenkbonnummer bij de afgifte of betaling van de geschenkbon.                                               |
| **Loyalty card**     | Een loyaliteitsklant aan de transactie toegevoegd en kan worden gebruikt wanneer de betaling van de loyaliteitskaart.                             |

## <a name="define-bar-code-masks"></a>Streepjescodemaskers definiëren
Nadat de tekens van streepjescodemaskers zijn opgegeven voor de benodigde streepjescodemaskers, gaat u naar **detailhandel en commerce**&gt;**voorraadbeheer**&gt;**streepjescodes en etiketten**&gt;**streepjescode maskerinstellingen**. Op deze pagina kunt u de streepjescodemaskers die gebruikmaken van de eerder opgegeven tekens. Deze streepjescode maskers wordt gebruikt bij het genereren van streepjescodes en wordt ook helpen bij het identificeren van streepjescodes gescand op het POS.

1.  Klik op **New** kunt u een nieuw streepjescodemasker te maken.
2.  Voer waarden in de **masker-ID** en **omschrijving** velden en selecteer vervolgens een type streepjescodemasker de **Type** veld.
3.  In de **algemeen** sectie, selecteert u een waarde in de **streepjescodestandaard** veld en geef vervolgens het voorvoegsel streepjescode indien deze vereist is.
4.  In de **segment streepjescodemasker** sectie achtereenvolgens streepjescode segmenten die worden gebruikt in de streepjescode moet worden gemaakt.

Als u bijvoorbeeld als u wilt een streepjescodemasker maakt met masker-ID "product": zou u het volgende doen:

1.  Een nieuw streepjescodemasker te maken en selecteer type 'product'.
2.  Selecteer een streepjescodestandaard, bijvoorbeeld 'Code 39'.
3.  Een voorvoegsel moet worden gebruikt voor het herkennen van de streepjescode bevatten. Bijvoorbeeld '22'.
4.  Een segment masker toevoegen. Het masker "product" segment wordt geselecteerd.
5.  Een lengte voor het product segment, bijvoorbeeld '10' bevatten. De lengte moet overeenkomen met de lengte van een product-ID die vaak worden gebruikt in de winkel. Het masker wordt weergegeven als een voorbeeld in de **algemeen** sectie onder **masker**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Streepjescodemaskers om streepjescodes af te wijzen
Streepjescodemaskers moeten worden toegewezen aan streepjescodes voordat ze kunnen worden gebruikt. Bezig met het vorige voorbeeld het streepjescodemasker toewijzen aan een streepjescode, handelt u als volgt:

1.  Ga naar **Organisatiebeheer**&gt;**Setup**&gt;**streepjescodes**. Klik op **New** om een nieuwe streepjescode te maken.
2.  Voer waarden in de **streepjescode****setup** en ** instellingen ** velden.
3.  In de **algemeen** gedeelte in de **streepjescodetype** veld, selecteert u 'Code 39'. In de **masker****ID** veld, selecteert u het "product" masker eerder hebt gemaakt.
4.  Onder **grootte**, '12' invoert.
5.  Click **Save**.

Het streepjescodemasker kan nu worden gebruikt voor het maken van streepjescodes voor producten. De bovenstaande stappen zijn voorbeelden van het maken van streepjescodemaskers voor producten, maar ze ook illustreren hoe streepjescodemaskers voor de andere ondersteunde streepjescode typen maken. Streepjescodemaskers, typen en lengte moeten worden aangepast voor gebruik in uw omgeving.


