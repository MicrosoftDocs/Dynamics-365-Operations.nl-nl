---
title: Standaard opgeslagen weergaven voor Supply Chain Management
description: In dit artikel worden de standaard opgeslagen weergaven beschreven die beschikbaar zijn en wordt uitgelegd hoe u deze weergaven kunt inschakelen.
author: kamaybac
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f94fffb9aa2c208b8c2c0005a2892853eda66a01
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334830"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Standaard opgeslagen weergaven voor Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management bevat diverse opgeslagen weergaven die u kunt inschakelen en waar nodig gebruiken. Sommige van deze standaard opgeslagen weergaven zijn geoptimaliseerd en genoemd naar een specifieke rol of taak (bijvoorbeeld "Kwaliteitsbeheer" of "Ontvangen"). Andere zijn in zoverre geoptimaliseerd dat ze alleen de velden en instellingen bevatten die volgens de gebruiksstatistieken van Microsoft het vaakst door klanten worden gebruikt. Deze opgeslagen weergaven worden meestal *vereenvoudigde weergaven* genoemd. In dit artikel worden de standaard opgeslagen weergaven beschreven die beschikbaar zijn en wordt uitgelegd hoe u deze weergaven kunt inschakelen en aanpassen.

Zie [Opgeslagen weergaven](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) voor volledige details over het werken met opgeslagen weergaven, waaronder de standaard opgeslagen weergaven, nadat u deze hebt ingeschakeld.

## <a name="customizing-the-standard-saved-views"></a>De standaard opgeslagen weergaven aanpassen

U kunt de standaard opgeslagen weergaven aanpassen, net zoals u uw eigen opgeslagen weergaven kunt aanpassen. Wanneer u een standaard opgeslagen weergave echter aanpast, raden we u sterk aan om de aangepaste versie op te slaan onder een nieuwe naam. Anders kunnen uw aanpassingen worden overschreven wanneer u Supply Chain Management bijwerkt.

Zie [Opgeslagen weergaven](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) voor meer informatie over het aanpassen en hernoemen van opgeslagen weergaven.

## <a name="available-saved-views-and-how-to-enable-them"></a>Beschikbare opgeslagen weergaven en hoe u deze kunt inschakelen

Als u opgeslagen weergaven wilt gebruiken, ongeacht of u de standaard opgeslagen weergaven gebruikt, moet u de functie *Opgeslagen weergaven* in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen (vanaf versie 10.0.21 is deze functie standaard ingeschakeld).

De resterende secties van dit artikel bevatten tabellen die de standaard opgeslagen weergaven beschrijven die momenteel beschikbaar zijn voor elke relevante module. Elke tabel bevat de naam van elke opgeslagen weergave, de pagina waarop u deze kunt vinden en een omschrijving ervan. Elke tabel toont ook de naam van de functie die de opgeslagen weergave bevat. Als u een standaard opgeslagen weergave in het systeem wilt bekijken, moet u de opgegeven functie in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen. Vanaf versie 10.0.25 zijn alle weergegeven weergaven standaard ingeschakeld.

## <a name="saved-views-for-the-inventory-management-module"></a>Opgeslagen weergaven voor de module Voorraadbeheer

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Voorraadbeheer.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Voorhanden lijst | Financiële items | Met deze vereenvoudigde weergave kunt u zich richten op financiële gegevens bij het beheren van voorhanden voorraad. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Voorhanden lijst | Kwaliteitscontrole | Met deze vereenvoudigde weergave kunt u zich richten op kwaliteitsbeheer bij het beheren van voorhanden voorraad. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Voorhanden lijst | Ontvangen | Met deze vereenvoudigde weergave kunt u zich richten op bewerkingen voor ontvangst bij het beheren van voorhanden voorraad. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Voorhanden lijst | Verzenden | Met deze vereenvoudigde weergave kunt u zich richten op bewerkingen voor verzending bij het beheren van voorhanden voorraad. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Transacties | Vereenvoudigd | Met deze vereenvoudigde weergave kunt u de voorraadstatus controleren zonder dat u wordt afgeleid door financiële gegevens en andere velden die minder vaak worden gebruikt. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Transferorders | Verzenden | Met deze vereenvoudigde weergave kunt u zich richten op bewerkingen voor verzending bij het beheren van overboekingsorders. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Transferorders | Ontvangen | Met deze vereenvoudigde weergave kunt u zich richten op bewerkingen voor ontvangst bij het beheren van overboekingsorders. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Transferorders | Kwaliteitscontrole | Met deze vereenvoudigde weergave kunt u zich richten op kwaliteitsbeheer bij het beheren van overboekingsorders. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Transferorders | Financiële items | Met deze vereenvoudigde weergave kunt u zich richten op financiële gegevens bij het beheren van overboekingsorders. | Opgeslagen weergaven voor voorraadbeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |

## <a name="saved-views-for-the-master-planning-module"></a>Opgeslagen weergaven voor de module Hoofdplanning

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Hoofdplanning.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Geplande orders: pagina met details van geplande order | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om te werken met de details van één geplande order. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergaven voor geplande orders<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Geplande orders: lijstpagina met geplande orders | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om te werken met de lijst met geplande orders. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergaven voor geplande orders<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Opgeslagen weergaven voor de module Inkoop en sourcing

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Inkoop en sourcing.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Inkooporderdetails | Order maken | Deze vereenvoudigde weergave is geoptimaliseerd voor het maken van nieuwe inkooporders. | Opgeslagen weergaven voor inkooporders<br><br>Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Inkooporderdetails | Voorraadbeheer | Deze vereenvoudigde weergave is geoptimaliseerd voor het uitvoeren van voorraadgerelateerde activiteiten, zoals het ondernemen van actie op voorraad die is ontvangen, de ontvangst van voorraad, het controleren van nettobehoeften en het aanpassen van orderhoeveelheden. | Opgeslagen weergaven voor inkooporders<br><br>Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Inkooporderdetails | Financieel beheer | Deze vereenvoudigde weergave is geoptimaliseerd voor het uitvoeren van financiële activiteiten, zoals het factureren en controleren van prijzen, totalen en toeslagen. | Opgeslagen weergaven voor inkooporders<br><br>Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Inkooporderdetails | Order goedkeuren | Deze vereenvoudigde weergave is geoptimaliseerd voor het goedkeuren van inkooporders. | Opgeslagen weergaven voor inkooporders<br><br>Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |

## <a name="saved-views-for-the-product-information-management-module"></a>Opgeslagen weergaven voor de module Productgegevensbeheer

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Productgegevensbeheer.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Lijst met vrijgegeven producten | Producten maken | Een vereenvoudigde paginaweergave die alleen de velden bevat die het vaakst worden gebruikt bij het maken van producten. | Opgeslagen weergaven voor vrijgegeven producten<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Vrijgegeven productdetails | Producten maken | Een vereenvoudigde paginaweergave die alleen de velden bevat die het vaakst worden gebruikt bij het maken van producten. | Opgeslagen weergaven voor vrijgegeven producten<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Vrijgegeven productdetails | Beheer van logistieke gegevens | Een vereenvoudigde paginaweergave die alleen de velden bevat die het vaakst worden gebruikt bij het beheren van logistieke gegevens voor producten. | Opgeslagen weergaven voor vrijgegeven producten<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Vrijgegeven productdetails | Beheer van aankoopgegevens | Een vereenvoudigde paginaweergave die alleen de velden bevat die het vaakst worden gebruikt bij het beheren van aankoopgegevens voor producten. | Opgeslagen weergaven voor vrijgegeven producten<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Vrijgegeven productdetails | Beheer van verkoopgegevens | Een vereenvoudigde paginaweergave die alleen de velden bevat die het vaakst worden gebruikt bij het beheren van verkoopgerelateerde gegevens van producten. | Opgeslagen weergaven voor vrijgegeven producten<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |

## <a name="saved-views-for-the-production-control-module"></a>Opgeslagen weergaven voor de module Productiebeheer

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Productiebeheer.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Pagina Stuklijst productieorder | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergaven voor productiebeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Pagina Details van productieorder | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergaven voor productiebeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Pagina Productieorderverzamellijst | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergaven voor productiebeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |
| Lijstpagina Productieorders | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergaven voor productiebeheer<br><br>(Standaard ingeschakeld vanaf versie 10.0.21. Verplicht vanaf versie 10.0.29.) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Opgeslagen weergaven voor de module Verkoop en marketing

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Verkoop en marketing.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Pakbonjournaal | Journaalcontrole | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om pakbonjournalen te controleren. | Opgeslagen weergaven voor de module Verkoop en marketing<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Verkooporder | Order maken | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om verkooporders te maken. | Opgeslagen weergaven voor de module Verkoop en marketing<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Verkooporder | Order controleren | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om verkooporders te controleren. | Opgeslagen weergaven voor de module Verkoop en marketing<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Verkoopofferte | Offerte maken | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om verkoopoffertes te maken. | Opgeslagen weergaven voor de module Verkoop en marketing<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |

## <a name="saved-views-for-the-warehouse-management-module"></a>Opgeslagen weergaven voor de module Magazijnbeheer

In de volgende tabel worden de opgeslagen weergaven beschreven die beschikbaar zijn voor de module Magazijnbeheer.

| Pagina | Weergavenaam | Omschrijving weergeven | Functienaam |
|---|---|---|---|
| Alle ladingen | Inkomende verwerking | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om inkomende ladingen te verwerken. | Opgeslagen weergaven voor de verwerking van ladingen<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Alle ladingen | Uitgaande verwerking | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om uitgaande ladingen te verwerken. | Opgeslagen weergaven voor de verwerking van ladingen<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Alle verzendingen | Inkomende verwerking | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om inkomende zendingen te verwerken. | Opgeslagen weergaven voor verzendingsverwerking<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Alle verzendingen | Uitgaande verwerking | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt om uitgaande zendingen te verwerken. | Opgeslagen weergaven voor verzendingsverwerking<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Alle waves | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergave voor de verwerking van waves<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Workbench ladingplanning | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergave voor de workbench voor ladingplanning<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |
| Werkgegevens | Vereenvoudigd | Deze vereenvoudigde weergave bevat alleen de velden die het vaakst worden gebruikt. Op deze manier biedt de weergave een sneller overzicht en een gestroomlijnd werkproces. | Opgeslagen weergave voor de pagina Werkgegevens<br><br>(Standaard ingeschakeld vanaf versie 10.0.25. Verplicht vanaf versie 10.0.29.) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]