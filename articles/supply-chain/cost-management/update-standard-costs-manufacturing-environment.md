---
title: Standaardkosten in een productieomgeving bijwerken
description: Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een productieomgeving.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 726eccdc8a9350a292ba719784b5db99afdfad4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262424"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Standaardkosten in een productieomgeving bijwerken

[!include [banner](../includes/banner.md)]

Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een productieomgeving. 

Updates kunnen nieuwe artikelen, kostencategorieën of berekeningsformules voor indirecte kosten reflecteren. Ze kunnen ook correcties en wijzigingen in kosten aangeven. Het type update bepaalt welke stappen u moet uitvoeren om standaardkosten bij te werken, zoals in de volgende gevallen wordt geïllustreerd:

-   Voer verwachte wijzigingen in standaardkosten voor ingekochte artikelen in en wijzig vervolgens de status van de artikelkostprijsregistraties naar **Actief** op de toepasselijke datum. Bereken echter niet opnieuw de kosten van gefabriceerde artikelen die de ingekochte artikelen gebruiken.
-   Voer standaardkosten voor een nieuw, ingekocht artikel in, maar bereken niet opnieuw de kosten van gefabriceerde artikelen die een stuklijstversie hebben die het nieuwe ingekochte artikel als onderdeel bevat.
-   Corrigeer of wijzig de kosten van een ingekocht artikel, of wijzig de kostengroep die aan een ingekocht artikel is toegewezen, en bereken de kosten voor alle gefabriceerde artikelen die een stuklijstversie hebben die het ingekochte artikel als onderdeel bevat.
-   Wijzig de kosten voor een kostencategorie, en bereken de kosten voor alle gefabriceerde artikelen die een routeversie hebben die routebewerkingen bevat die de kostencategorie gebruiken.
-   Wijzig de kostencategorieën die zijn toegewezen aan routing-bewerkingen of de kostengroep die aan de kostencategorieën toegewezen is. Bereken vervolgens de kosten voor alle gefabriceerde artikelen die een routeversie hebben die routebewerkingen bevat die de kostencategorie gebruiken.
-   Wijzig een berekeningsformule voor indirecte kosten, en bereken de kosten voor alle gefabriceerde artikelen waarvoor de wijziging gevolgen heeft.
-   Wijzig een productiesite voor een gefabriceerd artikel of voeg een site toe, en bereken de productiekosten van het artikel voor de site.
-   Bereken de kosten voor een gefabriceerd artikel (opnieuw), en herbereken de kosten voor alle gefabriceerde artikelen die een stuklijstversie hebben die het gefabriceerde artikel als onderdeel bevat.
-   Bereken kosten voor een nieuw gefabriceerd artikel op basis van de gedefinieerde, goedgekeurde en actieve stuklijst- en route-informatie.

In alle gevallen dient u nauwkeurig te overwegen hoe de standaardkosten moeten worden bijgewerkt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]