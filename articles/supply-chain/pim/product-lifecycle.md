---
title: Overzicht van Levenscyclusstatus van producten
description: Een levenscyclusstatus documenteert de levenscyclusstatus van een vrijgegeven product of productvariant.
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 51a6b19e84f368bf72b664e120f262ddcf7c7611
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425902"
---
# <a name="product-lifecycle-state-overview"></a>Overzicht van Levenscyclusstatus van producten

[!include [banner](../includes/banner.md)]

Een levenscyclusstatus documenteert de levenscyclusstatus van een vrijgegeven product of productvariant. Statussen voor de productlevenscyclus worden gedefinieerd door de gebruiker, doorgaans een productmanager of een manager van producthoofdgegevens. Specifieke bedrijfsprocessen, zoals de hoofdplanning, kunnen worden beïnvloed door een specifieke levenscyclusstatus.

Een vrijgegeven product of productvariant kan worden gekoppeld aan een status voor de productlevenscyclus waarmee wordt gedocumenteerd in welke levenscyclusstatus een bepaald product of een bepaalde productvariant zich momenteel bevindt. U kunt een onbeperkt aantal statussen voor de productlevenscyclus definiëren door een statusnaam en -omschrijving toe te wijzen. U kunt één levenscyclusstatus selecteren als de standaardstatus voor nieuwe vrijgegeven producten. Vrijgegeven productvarianten nemen bij het maken de status voor de productlevenscyclus van hun vrijgegeven productmodel over. Wanneer de levenscyclusstatus van een vrijgegeven productmodel wordt gewijzigd, kunt u ervoor kiezen om alle bestaande varianten met dezelfde oorspronkelijke status bij te werken.  

## <a name="create-a-new-product-lifecycle-state"></a>Nieuwe status van levenscyclus van producten maken

- Als u een nieuwe status voor de productlevenscyclus wilt maken, gaat u naar [Een nieuwe status voor de productlevenscyclus maken](tasks/new-product-lifecycle-state.md).

- Als u een standaardstatus voor de productlevenscyclus wilt maken, gaat u naar [Een standaardstatus voor de productlevenscyclus maken](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Statussen voor de productlevenscyclus koppelen aan vrijgegeven producten  

Er zijn verschillende manieren om een status voor de productlevenscyclus te koppelen aan vrijgegeven producten of productvarianten.

- Bij het maken van een nieuw vrijgegeven product wordt de **status voor de productlevenscyclus** automatisch toegewezen.
- Bij vrijgave van een product aan een rechtspersoon wordt de **status voor de productlevenscyclus** automatisch toegewezen.
- Bij vrijgave van een productvariant aan een rechtspersoon wordt de **status voor de productlevenscyclus** die is gekoppeld aan het vrijgegeven productmodel in deze rechtspersoon automatisch toegewezen aan de nieuwe variant.

U kunt de status voor de productlevenscyclus handmatig bijwerken via:

- De lijstpagina **Vrijgegeven producten** of **Detailweergave**.
- De lijstpagina **Vrijgegeven productvarianten** of **Detailweergave**.
- Zoek de verouderde producten of productvarianten op basis van vraag en koppel een levenscyclusstatus.  

Meer informatie:

- Als u de status van een productlevenscyclus wilt koppelen aan een vrijgegeven productmodel, gaat u naar [De status van een productlevenscyclus toewijzen aan een vrijgegeven productmodel](tasks/product-lifecycle-state-released-product-master.md).

- Als u de status van een productlevenscyclus wilt koppelen aan een vrijgegeven product, gaat u naar [De status van een productlevenscyclus toewijzen aan een vrijgegeven product](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Effect op hoofdplanning

De status van een productlevenscyclus heeft maar één controlemarkering: **Is actief voor planning**. Standaard is deze ingesteld op **Ja** voor alle gemaakte statussen voor de productlevenscyclus, maar dit kan worden gewijzigd in **Nee**. Bij **Nee** zijn de gekoppelde vrijgegeven producten of vrijgegevens productvarianten:

- Uitgesloten van de hoofdplanning.
- Uitgesloten van berekeningen op stuklijstniveau.

Voor gedetailleerde informatie over het gebruik van de status van een productlevenscyclus om producten uit te sluiten van de hoofdplanning en berekeningen op stuklijstniveau, gaat u naar [Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning](tasks/exclude-products-master-planning.md).

> [!NOTE]
> Uit prestatieoverwegingen is het raadzaam om alle verouderde vrijgegeven producten of productvarianten te koppelen, vooral wanneer u werkt met niet-herbruikbare productconfiguratievarianten, met een status voor de productlevenscyclus die is gedeactiveerd voor de hoofdplanning.  

## <a name="default-migration-import-and-export"></a>Standaardmigratie, -import en -export

De statussen voor productlevenscycli worden ondersteund door gegevensentiteiten en de status van de levenscyclus kan op een variabele status worden ingesteld via de entiteit voor vrijgegeven productgegevens of vrijgegeven variantgegevens.

## <a name="find-obsolete-products-and-products-variants"></a>Verouderde producten en productvarianten zoeken

U kunt een simulatieanalyse uitvoeren om te zoeken naar de verouderde vrijgegeven producten of productvarianten, en om de status van de productlevenscyclus bij te werken. Als u verouderde producten wilt vinden, gaat u naar [Verouderde productvarianten zoeken en een status voor de productlevenscyclus toewijzen](tasks/obsolete-product-variants.md). In dit onderwerp wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten. U ziet ook hoe u de simulatieresultaten kunt bekijken en kunt bepalen hoeveel producten en productvarianten worden gekoppeld aan een nieuwe status voor de productlevenscyclus wanneer u de update zonder simulatie uitvoert.  

Wanneer u de analyse in een simulatiemodus uitvoert, worden de als verouderd aangeduide producten en productvarianten weergegeven in een specifiek formulier, waar ze eenvoudig kunnen worden gecontroleerd. Met de analyse wordt gezocht naar transacties en bepaalde hoofdgegevens ter identificatie van producten waarvoor geen vraag bestaat in een variabele periode en er geen hoofdgegevens zijn die kunnen resulteren in vraag. Nieuw vrijgegeven producten in een variabele periode kunnen worden uitgesloten van de analyse. Wanneer de analysesimulatie het verwachte resultaat retourneert, kan de gebruiker de analyse uitvoeren en een nieuwe status voor de productlevenscyclus instellen voor alle producten die door de analyse als verouderd zijn aangeduid.  

> [!NOTE]
> Alle analyses en updates moeten in dezelfde rechtspersoon worden uitgevoerd.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Criteria voor het selecteren en bijwerken van vrijgegeven producten of productvarianten

Gebruik de volgende criteria voor het selecteren en bijwerken van de vrijgegeven producten en productvarianten:

- De status van de productlevenscyclus van het product of de productvariant moet afwijken van de nieuwe gewenste status.
- Het product of de productvariant is enkele dagen geleden gemaakt op basis van het aantal dagen dat u in het dialoogvenster voor selectie hebt ingevoerd.
- Er zijn geen openstaande productieorders (= status < beëindigd) voor het product of de productvariant.
- Er zijn geen openstaande voorraadtransacties (= statusuitgifte ReservPhysical naar QuotationIssue of statusontvangst Registered naar QuotationReceipt) voor het product of de productvariant.
- Er zijn geen voorraadtransacties binnen het laatste aantal dagen voor het product of de productvariant.
- Er is geen toekomstige vraag of aanbodprognose voor het product of de productvariant.  
- Er is geen minimaal voorraadniveau ingesteld in de artikelbehoefteplanning voor het product of de productvariant.
- Geen actieve kanbanregel met vaste hoeveelheid voor het product of de productvariant.  
- Geen serviceorderregel voor het product of de productvariant.
- Geen actieve of toekomstige verkoop- of inkoopovereenkomstregels voor het product of de productvariant.
- Het product of de productvariant wordt niet gebruikt in een stuklijst die is gekoppeld aan een niet-verlopen goedgekeurde stuklijstversie voor een product dat of variant die actief is voor de planning.

## <a name="related-topics"></a>Verwante onderwerpen

- [Nieuwe status van levenscyclus van producten maken](tasks/new-product-lifecycle-state.md)
- [Standaardstatus van levenscyclus van producten maken](tasks/default-product-lifecycle-state.md)
- [De status van een productlevenscyclus toewijzen aan een vrijgegeven productmodel](tasks/product-lifecycle-state-released-product-master.md)
- [De status van een productlevenscyclus toewijzen aan een vrijgegeven product](tasks/product-lifecycle-state-released-product.md)
- [Verouderde productvarianten zoeken en een status voor de productlevenscyclus toewijzen](tasks/obsolete-product-variants.md)
- [Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning](tasks/exclude-products-master-planning.md)
