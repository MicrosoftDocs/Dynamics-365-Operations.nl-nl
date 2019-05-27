---
title: Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen
description: Dit onderwerp beschrijft de stappen voor het voorbereiden van het beheer van kosten voor gefabriceerde artikelen.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbd7344f3d542cbd46e3568d8a7911ab4ab53b17
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545943"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft de stappen voor het voorbereiden van het beheer van kosten voor gefabriceerde artikelen. De stappen voor gefabriceerde artikelen verschillen enigszins van de stappen voor ingekochte artikelen.

Beleidsregels die aan gefabriceerde artikelen zijn toegewezen, kunnen gevolgen hebben voor de kostprijsberekeningen voor de bovenliggende gefabriceerde artikelen. Voer de volgende stappen uit om kosten voor gefabriceerde artikelen te onderhouden.

1. Wijs een artikelmodelgroep toe aan het gefabriceerde artikel. 

   Met de artikelmodelgroep wordt aangegeven dat standaardkosten worden gebruikt.

2. Wijs een artikelgroep toe aan het gefabriceerde artikel. 

   De artikelgroep bevat grootboekrekeningen die van toepassing zijn op het gefabriceerde artikel. De grootboekrekeningen voor een gefabriceerd artikel dat een standaardkostenvoorraadmodel heeft, omvatten verschillende productieafwijkingen, de kostenwijzigingsafwijking en de herwaardering van de voorraadkosten.

3. Wijs de voorraadmaateenheid toe aan het artikel. 

   De kosten van het artikel worden altijd uitgedrukt in de voorraadmaateenheid van het artikel.

4. Wijs geen kostengroep aan het gefabriceerde artikel toe, tenzij het artikel als ingekocht artikel wordt beschouwd.

5. Wijs een stuklijstberekeningsgroep toe aan het gefabriceerde artikel. 

   De stuklijstberekeningsgroep van het artikel definieert waarschuwingsvoorwaarden die van toepassing zijn. Op die manier kunnen, wanneer een stuklijstberekening wordt uitgevoerd, waarschuwingsberichten worden gegenereerd over mogelijke oorzaken van berekeningsfouten. Een waarschuwingsbericht kan bijvoorbeeld aangeven wanneer er geen actieve stuklijst of route bestaat. De stuklijstberekeningsgroep bevat een beleid voor het stoppen van een explosie, dat aangeeft wanneer een gefabriceerd artikel als ingekocht artikel moet worden beschouwd.

6. Als het gefabriceerde artikel constante kosten heeft, wijst u er een standaardorderhoeveelheid aan toe. 

   De standaardorderhoeveelheid is een boekhoudpartijgrootte voor het afschrijven van constante kosten. Voorbeelden van constante kosten zijn instellingstijden in routebewerkingen en een constante onderdeelhoeveelheid in de stuklijst.

7. Definieer de stuklijst voor het gefabriceerde artikel. 

   Er kunnen een of meer stuklijstversies worden gedefinieerd voor het gefabriceerde artikel. Verifieer dat de gewenste versies zijn gemarkeerd als goedgekeurd en actief, en dat ze de gewenste ingangsdatums hebben. De stuklijstversie kan het hele bedrijf of een specifieke locatie beslaan.

8. Definieer de route voor het gefabriceerde artikel. 

   Er kunnen een of meer routeversies worden gedefinieerd voor het gefabriceerde artikel. Verifieer dat de gewenste versies zijn gemarkeerd als goedgekeurd en actief, en dat ze de gewenste ingangsdatums hebben. De routeversie moet locatiespecifiek zijn.

Als u routegegevens wilt gebruiken voor kostprijsberekening, zijn er extra voorbereidende stappen vereist. Zo moeten de kostencategorieën die aan routebewerkingen zijn toegewezen, juist en volledig zijn.

<a name="related-topics"></a>Verwante onderwerpen
--------

[Constante kosten voor een gefabriceerd artikel afschrijven](amortize-constant-costs-manufactured-item.md)

[Producten instellen die kunnen worden geproduceerd of kunnen worden aangeschaft](manufactured-items-treated-as-purchased-items.md)

