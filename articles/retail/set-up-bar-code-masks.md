---
title: Streepjescodemaskers instellen
description: In dit onderwerp wordt beschreven hoe u streepjescodemaskertekens en streepjescodemaskers instelt en hoe u streepjescodemaskers toewijst aan streepjescodes.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 958cac2e85ae7fa514f6f26cbb6178d8fdec9783
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="set-up-bar-code-masks"></a>Streepjescodemaskers instellen

[!include[banner](includes/banner.md)]


In dit onderwerp wordt beschreven hoe u streepjescodemaskertekens en streepjescodemaskers instelt en hoe u streepjescodemaskers toewijst aan streepjescodes.

<a name="set-up-bar-code-mask-characters"></a>Tekens van streepjescodemaskers instellen
-------------------------------

Streepjescodemaskers worden gebruikt om streepjescodes te maken en snel streepjescodes te identificeren die in het POS worden gescand. Maskers bestaan uit tekens die fungeren als tijdelijke aanduidingen, die aangeven wat de indeling van de gemaakte streepjescodes is. Als u een streepjescodemasker wilt configureren, moet u de tekens van streepjescodemaskers instellen. Ga naar **Retail** &gt; **Voorraadbeheer** &gt; **Streepjescodes en etiketten** &gt; **Maskertekens**. Klik op **Nieuw** om tekens voor het streepjescodemasker te maken. Tekens van streepjescodemaskers kunnen worden gemaakt om de volgende gegevens in de streepjescode aan te geven.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Veld**            | **Beschrijving**                                                                                                 |
| **Product**          | Tijdelijke aanduiding voor product-ID.                                                                                     |
| **Willekeurig getal**       | Geeft een getal op dat vastgelegd wordt in streepjescodes.                                                  |
| **Controlecijfer**      | Geeft aan dat de streepjescode-indeling in een streepjescodemasker een controlecijfer gebruikt om de geldigheid van een streepjescode te bevestigen. |
| **Cijfergrootte**       | Geeft de grootte aan in een streepjescode die wordt gemaakt voor een productvariant die een maataanduiding bevat.                                 |
| **Cijferkleur**      | Geeft de kleur aan in een streepjescode die wordt gemaakt voor een productvariant die een kleur bevat.                               |
| **Cijferstijl**      | Geeft de stijl aan in een streepjescode die wordt gemaakt voor een productvariant die een stijl bevat.                             |
| **EAN-licentiecode** | Tijdelijke aanduiding voor een EAN-licentie die is uitgegeven voor EAN-licentiecodes.                                                       |
| **Prijs**            | Geeft de prijs aan in streepjescodes met ingesloten prijs.                                                                   |
| **Hoeveelheid**         | Geeft de hoeveelheid aan in streepjescodes met ingesloten hoeveelheid/willekeurig gewicht.                                                |
| **Werknemer**         | Geeft het segment in de streepjescode aan met het id-nummer van werknemers, dat wordt gebruikt bij POS-aanmelding via streepjescode.                                  |
| **Klant**         | Geeft het segment met het klant-ID in de streepjescode aan.                                                                                  |
| **Gegevensinvoer**       | *Nog niet geïmplementeerd.*                                                                                          |
| **Kortingscode**    | *Afgeschaft* vanaf Dynamics 365 for Retail, versie lente 2017. Voorheen: Geeft de kortingscode aan voor een streepjescode die wordt gebruikt om een korting toe te voegen aan een POS-transactie.                                                                   |
| **Couponcode**      | Geeft een couponcode voor een streepjescode aan, waarmee een korting wordt toegevoegd aan een detailhandelorder. Deze code vervangt de kortingscode.     |
| **Geschenkbon**        | Geeft een geschenkbonnummer aan bij de uitgifte van een geschenkbon of betaling daarmee.                                               |
| **Loyaliteitskaart**     | Voegt een loyaliteitsklant aan de transactie toe en kan worden gebruikt wanneer met een loyaliteitskaart wordt betaald.                             |

## <a name="define-bar-code-masks"></a>Streepjescodemaskers definiëren
Nadat de tekens van streepjescodemaskers zijn opgegeven voor de benodigde streepjescodemaskers, gaat u naar **Retail** &gt; **Voorraadbeheer** &gt; **Streepjescodes en etiketten** &gt; **Instellingen streepjescodemasker**. Op deze pagina definieert u de streepjescodemaskers die gebruik maken van de eerder opgegeven tekens. Deze streepjescodemaskers wordt gebruikt bij het genereren van streepjescodes en helpen ook bij het identificeren van streepjescodes die worden gescand op het POS.

1.  Klik op **Nieuw** om een nieuw streepjescodemasker te maken.
2.  Voer waarden in de velden **Masker-ID** en **Omschrijving** in en selecteer vervolgens een type streepjescodemasker in het veld **Type**.
3.  Selecteer in de sectie **Algemeen** een waarde in het veld **Streepjescodestandaard** en geef vervolgens het streepjescodevoorvoegsel op indien deze vereist is.
4.  Voeg in de sectie **Segment streepjescodemasker** de streepjescodesegmenten op die worden gebruikt in de te maken streepjescode.

Als u bijvoorbeeld een streepjescodemasker wilt maken maakt met het masker-ID 'Product', doet u het volgende:

1.  Maak een nieuw streepjescodemasker en selecteer als type 'Product'.
2.  Selecteer een streepjescodestandaard, bijvoorbeeld 'Code 39'.
3.  Geef een voorvoegsel op waarmee de streepjescode snel herkend kan worden. Bijvoorbeeld '22'
4.  Voeg een maskersegment toe. Het maskersegment 'Product' wordt geselecteerd.
5.  Geef een lengte op voor het productsegment, bijvoorbeeld '10'. De lengte moet overeenkomen met de lengte van een product-ID die veel wordt gebruikt in de winkel. Het masker wordt weergegeven als een voorbeeld in de sectie **Algemeen** onder **Masker**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Streepjescodemaskers toewijzen aan streepjescodes
Streepjescodemaskers moeten worden toegewezen aan streepjescodes voordat ze kunnen worden gebruikt. Als we het vorige voorbeeld voortzetten, wijst u als volgt het streepjescodemasker toe aan een streepjescode:

1.  Ga naar **Organisatiebeheer** &gt; **Instellen** &gt; **Streepjescodes**. Klik op **Nieuw** om een nieuwe streepjescode te maken.
2.  Voer waarden in in de velden **Instelling van** **streepjescodes** and **Instellen **.
3.  Selecteer in de sectie **Algemeen** in het veld **Type streepjescode** de waarde 'Code 39'. Selecter in het **Masker-****id** het masker 'Product' dat u eerder hebt gemaakt.
4.  Voer onder **Grootte** de waarde '12' in.
5.  Klik op **Opslaan**.

Het streepjescodemasker kan nu worden gebruikt voor het maken van streepjescodes voor producten. De bovenstaande stappen zijn voorbeelden van het maken van streepjescodemaskers voor producten, maar ze laten ook zien hoe u streepjescodemaskers maakt voor de andere ondersteunde typen streepjescode. U moet streepjescodemaskers, -typen en -lengte aanpassen voor gebruik in uw eigen omgeving.



