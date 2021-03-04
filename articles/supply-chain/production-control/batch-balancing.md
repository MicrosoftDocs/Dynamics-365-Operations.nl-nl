---
title: Batchverdeling
description: In dit onderwerp wordt het proces voor batchverdeling beschreven.
author: johanhoffmann
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2ef0a43480e547c6bd19d5f9b7377ed8b73425e7
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425792"
---
# <a name="batch-balancing"></a>Batchverdeling

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe het proces voor batchverdeling wordt ondersteund. 

Bekijk een [video over batchverdeling](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be) voor meer informatie.

In het batchverdelingsproces wordt de hoeveelheid ingrediënten die wordt gebruikt in een productiebatch berekend op basis van de concentratie van de actieve ingrediënten in geselecteerde productbatches.

<a name="products-that-have-an-active-ingredient"></a>Producten met een actief ingrediënt
---------------------------------------

Een product kan worden gedefinieerd door de concentratie van een actief ingrediënt. Het actieve ingrediënt van een product wordt gemodelleerd met behulp van een productspecifiek batchkenmerk met een minimumwaarde, een maximumwaarde en een doelniveau.

Het doelniveau van een batchkenmerk geeft het geschatte percentage van een actief ingrediënt in een product. De minimale en maximale waarden geven de geaccepteerde afwijking van het doelniveau aan. Deze kunnen bijvoorbeeld worden gebruikt als een toegestane tolerantie voor batches bij productontvangst.

Een product kan slechts één actieve ingrediënt hebben. Als u het actieve ingrediënt van een product wilt opgeven, moet u eerst een productspecifiek batchkenmerk definiëren. Vervolgens koppelt u het kenmerk als een basiskenmerk van het product.

Op het productniveau moet u ook opgeven hoe het niveau van het actieve ingrediënt voor een batch van het product moet worden geregistreerd: als onderdeel van het inkoopontvangstproces of als onderdeel van een kwaliteitsorderproces.

Als u een basiskenmerk wilt koppelen aan een product, zijn de volgende instellingen vereist:

-   Het product moet een batchartikel zijn. Als u een productbatch wilt maken, moet u een traceringsdimensiegroep toewijzen aan het product dat een actieve batchdimensie heeft.

-   Het kenmerk dat de ingrediëntniveaus aangeeft moet worden gedefinieerd als een productspecifiek batchkenmerk voor het product.

U kunt de werkelijke waarde van het actieve ingrediënt voor een batch opzoeken en bewerken op de pagina **Voorraadbatchkenmerken**. 

-  Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Traceringsdimensies** \> **Batches** \> **Voorraadbatchkenmerken**.

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Ingrediënttypen en hoe ze werken in het proces voor batchverdeling
---------------------------------------------------------------------

Een formuleregel die is gemaakt, kan een van deze ingrediënttypen hebben:

-   None

-   Actief

-   Compenseren

-   Opvulling

De rest van deze sectie geeft voorbeelden die laten zien hoe elk ingrediënttype werkt. De voorbeelden zijn gebaseerd op de volgende formule met een totale batchgrootte van 100 liter.

| **Type ingrediënt** | **Artikelnummer** | **Hoeveelheid formuleregel** | **Eenheid** |
|---------------------|-----------------|---------------------------|----------|
| None                | V               | 20                        | Liter    |
| Actief              | B               | 30                        | Liter    |
| Compenseren        | E               | 10                        | Liter    |
| Opvulling              | M               | 40                        | Liter    |

### <a name="active"></a>Actief

Wanneer een product met een basiskenmerk wordt toegevoegd aan een formuleregel, wordt dit aangeduid als een *actief ingrediënt* van de formule. Batchorders met formules die actieve bestanddelen bevatten, kunnen worden gebruikt voor het proces voor batchverdeling. Voor elk ingrediënt in de formule wordt in het proces voor batchverdeling de hoeveelheid geschat dat nodig is om het product te produceren. De raming van hoeveelheden wordt gebaseerd op de concentratie van de actieve ingrediënten in de geselecteerde batches.

**Voorbeeld**

Ingrediënt B heeft basiskenmerk X en een doelniveau van 30. Het is opgenomen in een formule die 30 liter van ingrediënt B nodig heeft voor elke 100 liter van het product. Er wordt een batchorder gemaakt met een batchgrootte van 100 liter. De batchorder wordt gestart en tijdens het batchverdelingsproces selecteert de gebruiker een batch van ingrediënt B die een potentieniveau van 35 heeft. Omdat het potentieniveau van 35 hoger is dan het doelniveau van 30, wordt de verdeelde hoeveelheid van ingrediënt B verlaagd door de verhouding van de potentiewaarde met het doelniveau van de batch te gebruiken. Dit wordt vermenigvuldigd met de geschatte hoeveelheid. De berekening van de verdeelde hoeveelheid ziet er zo uit:

(30 ÷ 35) x 30 liter = 25,71 liter

| **Artikelnummer** | **Type ingrediënt** | **Geraamde hoeveelheid** | **Uitgebalanceerde hoeveelheid** | **Actieve hoeveelheid** | **Eenheid** | **Basiswaarde** |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| V               | None                | 20                     | 20                    |                     | Liter    |                |
| B               | Actief              | 30                     | 25,71                 | 9,00                | Liter    | 30,00          |
| E               | Compenseren        | 10                     | 14,72                 |                     | Liter    |                |
| M               | Opvulling              | 40                     | 39,57                 |                     | Liter    |                |

### <a name="none"></a>None

Bij het toepassen van het batchverdelingsproces met het ingrediënttype **Geen**, zijn de geraamde hoeveelheid en de verdeelde hoeveelheid van de formuleregel in de batchorder hetzelfde.

**Voorbeeld**

Ingrediënt A wordt toegewezen aan een ingrediënt van het type **Geen** en toegevoegd aan een formule voor een afgewerkt product. De formule vereist 10 liter van ingrediënt A voor elke 100 liter van het eindproduct. Als voor een batchorder 200 liter nodig is, worden de geraamde hoeveelheid en de verdeelde hoeveelheid van ingrediënt A berekend als 20 liter.

### <a name="compensating"></a>Compenseren

Een compensatie-ingrediënt kan een verschil of aanvulling veroorzaken op het effect van het actieve ingrediënt in een product. Daarom is de hoeveelheid van een verbruikt compensatie-ingrediënt afhankelijk van het potentie van het product:

-   **Tegengesteld effect**: als de hoeveelheid van het actieve ingrediënt meer is dan verwacht, moet u minder van het compensatie-ingrediënt toevoegen.

-   **Aanvullend effect**: als de hoeveelheid van het actieve ingrediënt minder is dan verwacht, moet u meer van het compensatie-ingrediënt toevoegen.

De relatie tussen een actief ingrediënt en een aanvullend ingrediënt wordt ingesteld op de pagina **Compensatiemethode**.

Volg deze stappen om de relaties tussen ingrediënten in te stellen.

1.  Selecteer **Productgegevensbeheer** \> **Stuklijsten en formules** \> **Formules**, open een formuleregel en selecteer vervolgens **Ingrediënten** om de pagina **Compensatiemethode** te openen.

2.  Selecteer de regel die een compensatiemethode aangeeft en selecteer vervolgens het actieve ingrediënt om te compenseren.

>   In de compensatiemethode kunt u ook een positieve of negatieve compensatiefactor invoeren om op te geven hoeveel moet worden gecompenseerd en of de methode principe tegengesteld of aanvullend moet zijn. Een positieve factor geeft aan een aanvullend effect en een negatieve factor geeft een tegengesteld effect.

**Voorbeeld**

Ingrediënt B is een actief ingrediënt met basiskenmerk X en doelniveau 30. Dit is opgenomen in een formule die 30 liter van ingrediënt B vereist voor elke 100 liter van het product. Ingrediënt C is een compensatie-ingrediënt en een hoeveelheid van 10 wordt opgenomen in dezelfde formule. De compensatiefactor 1,10 is ingesteld voor de compensatiemethode. Daarom wordt de verdeelde hoeveelheid van de compensatie-ingrediënt verminderd met het verschil tussen de verdeelde hoeveelheid van het actieve ingrediënt en de geschatte vereiste hoeveelheid vermenigvuldigd met 1,10.

In het voorbeeld voor het **actieve** ingrediënttype is de verdeelde hoeveelheid van het vereiste actieve ingrediënt berekend als 25,71 en de geschatte vereiste hoeveelheid als 30. In dit geval wordt de verdeelde hoeveelheid van jet compensatie-ingrediënt berekend als volgt:

1.  Het verschil tussen de geschatte en de verdeelde hoeveelheid wordt bepaald:

>   25,71 – 30 = –4,29

2.  Het resultaat wordt vermenigvuldigd door de compensatiefactor:

>   4,29 × 1.10 = –4,72

3.  De geraamde hoeveelheid van de compensatie wordt verminderd met –4,72 om de verdeelde compensatiehoeveelheid te bepalen :

>   10 – (–4,72) = 14,72

Omdat 1,10 een positieve compensatiefactor is, heeft deze compensatiemethode een aanvullend effect. In dit geval wordt het actieve ingrediënt sterker dan verwacht. Daarom is meer van het compensatie-ingrediënt vereist.

### <a name="filler"></a>Opvulling

Een *vul-ingrediënt* is een neutraal ingrediënt dat wordt gebruikt voor het bereiken van de gewenste uitvoerhoeveelheid van het eindproduct. Correcties in de vul-hoeveelheden worden berekend op basis van variaties in het actieve ingrediënt en het compensatie-ingrediënt vergeleken met de standaardhoeveelheid.

**Voorbeeld**

U hebt een product met de ingrediënten A, B, C en D voor een formulegrootte van 100 liter. U hebt de verdeelde hoeveelheid van alle soorten ingrediënttypen berekend, behalve het **vul**-ingrediënttytpe dat wordt gebruikt op één regel.
De verdeelde hoeveelheid van het vul-ingrediënt wordt berekend als het verschil tussen de batchgrootte van 100 liter en de som van de ingrediënten A, B en C:

100 – (20 + 25,71 + 14,72) = 39,57

<a name="the-batch-balancing-process"></a>Het batchverdelingsproces
---------------------------

Het batchverdelingsproces wordt uitgevoerd vanaf de pagina **Batchverdeling**.
Selecteer **Kostenbeheer** \> **Batchorders** en vervolgens op het tabblad **Proces** **Batchverdeling**. Batchverdeling is beschikbaar voor batchorders met de status **Begonnen**.

In het algemeen kan batchverdeling worden toegepast op batchorders als de formule ten minste één formuleregel heeft waarbij het ingrediënttype **Actief** is. (Zie de sectie 'Batchorders die niet van toepassing zijn voor batchverdeling' verderop in dit onderwerp voor de uitzondering op deze regel.)

Het batchverdelingsproces kan worden opgedeeld in twee subprocessen:

1.  Batchingrediënten verdelen

2.  Bevestigen en de formule vrijgeven

### <a name="balance-batch-ingredients"></a>Batchingrediënten verdelen

In het subproces Ingrediënten batchverdeling wordt de hoeveelheid ingrediënten die wordt gebruikt voor de productiebatch berekend op basis van de actieve ingrediënten in geselecteerde productbatches. De regel is dat de berekening alleen kan worden voltooid als er volledige dekking is van alle ingrediënten. U kunt slechts een gedeelte van de batch verdelen waarvoor de batchorder is ingesteld voor de productie.

[!NOTE]
U kunt een berekening niet opslaan en het batchverdelingsproces later voltooien. Als u de pagina **Batchverdeling** sluit, moet u de berekening herhalen om het proces te voltooien.

### <a name="confirm-and-release-the-formula"></a>Bevestigen en de formule vrijgeven

Nadat de ingrediënthoeveelheden zijn berekend, kunt u bevestigen en de formule vrijgeven. Het vrijgaveproces verschilt, afhankelijk van of de producten zijn ingeschakeld voor de magazijnbeheerprocessen:

-   Als een product voor de magazijnbeheerprocessen is ingeschakeld, wordt de formuleregel vrijgegeven aan het magazijn volgens de principes voor de magazijnbeheerprocessen. De formuleregel wordt vrijgegeven in hoeveelheden die overeenkomen met de verdeelde hoeveelheden en voor de specifieke batches die zijn geselecteerd voor de actieve ingrediënten.

> [!NOTE]
>   Formuleregels kunnen alleen worden vrijgegeven aan het magazijn als onderdeel van het batchverdelingsproces. Hoewel er andere opties voor het vrijgeven van materialen voor productie aan het magazijn zijn, kunnen deze opties niet worden gebruikt voor formuleregels.

-   Als een product niet is ingeschakeld voor de magazijnbeheerprocessen, wordt een orderverzamellijst voor de productie gemaakt voor het product wanneer u de formule bevestigt en vrijgeeft.

U kunt in één formule producten combineren die wel of niet zijn ingeschakeld voor magazijnbeheerprocessen. Wanneer de twee typen producten zijn opgenomen in één formule, worden de producten die zijn ingeschakeld voor de magazijnbeheerprocessen vrijgegeven aan het magazijn. Voor de producten die niet zijn ingeschakeld voor de magazijnbeheerprocessen, wordt een orderverzamellijst gemaakt wanneer u de formule bevestigt en vrijgeeft.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Batchorders die niet van toepassing zijn voor batchverdeling

Er is één uitzondering op de regel dat batchorders van toepassing zijn voor batchverdeling als de formule ten minste één formuleregel heeft waarbij het ingrediënttype **Actief** is.

Als een formule een actief ingrediënt bevat voor een product dat voor de magazijnbeheerprocessen is ingeschakeld, maar het batchnummer lager is dan de locatie in de reserveringshiërarchie, is de batchorder niet van toepassing voor batchverdeling.

Een batchorder die niet van toepassing is voor batchverdeling, loopt via de normale procescyclus voor batchorders.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]